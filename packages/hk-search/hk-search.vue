<!--
 * @describe: 搜索组件
 * @Author: superDragon
 * @Date: 2019-06-26 15:38:53
 * @LastEditors: superDragon
 * @LastEditTime: 2019-06-26 15:38:53
 -->
<script>
export default {
  name: 'hk-search',
  props: {
    searchList: {
      type: Array,
      default: () => []
    },
    showSubmit: {
      type: Boolean,
      default: true
    },
    more: {
      type: Boolean,
      default: false
    }
  },
  data () {
    return {
      fold: true,
      form: {}
    }
  },
  render (h) {
    return (
      <div class="hk-search-all">
        <div class={this.more ? 'search-all-more' : 'search-all'}>
          <div
            class="hk-search"
            style={{ height: this.fold ? '40px' : 'auto', overflowY: this.fold ? 'hidden' : 'auto' }}
          >
            <hk-form
              ref="form"
              v-model={this.form}
              inline={true}
              items={this.searchList}
              onEnter={this.getParams}
            />
          </div>
          {this.showSubmit ? (
            <div class="hk-search-button">
              <hk-button onClick={this.getParams}>查询</hk-button>
            </div>
          ) : null}
        </div>
        {this.more ? (
          <div class="more" onClick={() => this.expend()}>
            <i class={this.fold ? 'el-icon-arrow-down' : 'el-icon-arrow-up'} />
          </div>
        ) : null}
      </div>
    )
  },
  methods: {
    expend () {
      this.fold = !this.fold
    },
    getParams () {
      let params = this.form
      Object.keys(params).forEach(key => {
        if (params[key] === '' || params[key] === null || params[key] === undefined) delete params[key]
      })
      this.$emit('submit', params)
    }
  }
}
</script>
