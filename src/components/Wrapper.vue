<script>
  export default {
    name: 'Wrapper',
    render: function(createElement) {
      return createElement(
        this.tagName, // tag name
        {
          class: 'wrapper',
          style: {
            color: '#222',
          },
        },
        this.$slots.default // array of children
      )
    },
    props: {
      tagName: {
        type: String,
        required: true
      }
    }
  }
</script>

<style>
  .wrapper {
    border: 1px dotted darksalmon;
    border-radius: 5px;
  }
</style>

