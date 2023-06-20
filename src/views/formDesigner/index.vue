<!--
* @Description 
* @FilePath /src/views/formDesigner/index.vue
* @Author zb
* @LastEditTime 2023-06-19 23:27:38
!-->
<template>
  <div class="common-layout">
    <el-container>
      <el-aside width="300px">
        <WidgetPanel />
      </el-aside>
      <el-main>
        <FormPanel />
      </el-main>
      <el-aside width="300px">
        <SettingPanel />
      </el-aside>
    </el-container>
  </div>
</template>

<script setup lang="ts">
import { ref, onMounted } from 'vue'
import FormPanel from './formPanel/index.vue'
import SettingPanel from './settingPanel/index.vue'
import WidgetPanel from './widgetPanel/index.vue'

const props = defineProps({})
const emit = defineEmits([])
onMounted(() => {})
</script>

<script lang="ts">
export default { name: 'formDesigner' }
</script>
<style lang="scss" scoped></style>
