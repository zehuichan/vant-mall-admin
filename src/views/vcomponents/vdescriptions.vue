<template>
  <demo-wrapper title="展示组件">
    <!--v-descriptions-->
    <demo-card title="v-descriptions">
      <v-descriptions :data="descriptions.data" :columns="descriptions.columns">
        <template #custom>
          自定义插槽
        </template>
      </v-descriptions>
      <demo-block title="template">
        <highlightjs language="html" :code="vdescriptions.template"/>
      </demo-block>
    </demo-card>
  </demo-wrapper>
</template>

<script>
  // mixins
  import comp from './comp'
  // mapping
  import {descriptions} from './mapping'
  // code
  import {vdescriptions} from './code'

  export default {
    name: 'vdescriptions',
    mixins: [comp],
    data() {
      return {
        descriptions,
        vdescriptions,
      }
    }
  }
</script>