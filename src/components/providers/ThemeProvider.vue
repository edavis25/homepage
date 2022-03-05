<script>
export default {
  name: 'ThemeProvider',
  props: {
    msg: String
  },
  methods: {
    setTheme(theme) {
      if (!this.themes.contains(theme)) {
        throw new Error('Invalid theme');
      }
      this.currentTheme = theme;
    }
  },
  data() {
    return {
      currentTheme: 'theme-90s',
      themes: ['theme-90s', 'theme-80s']
    };
  },
  mounted() {
    document.body.classList.add(this.currentTheme);
  },
  render() {
    return this.$slots.default({
      setTheme: this.setTheme,
      theme: this.currentTheme,
      themes: this.themes
    });
  },
  watch: {
    currentTheme(newVal, oldVal) {
      document.body.classList.remove(oldVal);
      document.body.classList.add(newVal);
    }
  }
}
</script>
