<template>
  <div class="demo">
    <div class="demo-grid">
      <a-demo/>
      <offset-demo/>
    </div>
    <div class="demo-grid">
      <single-demo/>
      <range-demo/>
    </div>
    <div class="demo-grid">
      <size-demo/>
      <clear-demo/>
    </div>
    <div class="demo-grid">
      <slots-demo/>
      <dynamic-type-demo/>
    </div>
  </div>
</template>

<script>
import SingleDemo from './demos/SingleDemo'
import RangeDemo from './demos/RangeDemo'
import SizeDemo from './demos/SizeDemo'
import ClearDemo from './demos/ClearDemo'
import SlotsDemo from './demos/SlotsDemo'
import DynamicTypeDemo from './demos/DynamicTypeDemo'
import OffsetDemo from './demos/OffsetDemo'
import ADemo from "./demos/ADemo";

export default {
  name: 'Demo',
  // eslint-disable-next-line vue/no-unused-components
  components: {ADemo, OffsetDemo, DynamicTypeDemo, SlotsDemo, ClearDemo, SizeDemo, RangeDemo, SingleDemo},
  data() {
    return {
      date: ''
    }
  },
  beforeCreate() {
  }
}
</script>

<style lang="less">
.demo {
  padding-bottom: 160px;
}

.demo-grid {
  display: flex;
  flex-direction: row;
  justify-content: space-around;

  > div {
    width: 400px;
  }
}

.date-label {
  font-weight: bold;
  padding: 10px;
}

.date-value {
  vertical-align: middle;

  &:before {
    content: 'value:';
    margin-right: 5px;
  }
}

.tips {
  color: #555555;
  background-color: #eaeaea;
  padding: 2px 5px;
}

div.tips {
  margin: 5px 0 0 0;
  border-left: 3px solid #333333;
  padding: 10px 5px;
}
</style>
