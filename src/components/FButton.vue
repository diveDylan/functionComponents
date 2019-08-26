
<script>
export default {
  functional: true,
  name: 'FButton',
  render(h, context) {
    console.log('fbutton render:', context)
    const { data,children } = context
    return (
      h('el-button', data, children)
    )
  },
};
</script>

<style scoped lang="scss">

</style>
