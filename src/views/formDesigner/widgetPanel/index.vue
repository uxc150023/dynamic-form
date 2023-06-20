<!--
* @Description 
* @FilePath /src/views/formDesigner/widgetPanel/index.vue
* @Author zb
* @LastEditTime 2023-06-19 23:29:01
!-->
<template>
  <div>
    <draggable
      tag="ul"
      :list="containers"
      item-key="key"
      :group="{ name: 'dragGroup', pull: 'clone', put: false }"
      :clone="handleContainerWidgetClone"
      ghost-class="ghost"
      :sort="false"
      :move="checkContainerMove"
      @end="onContainerDragEnd"
    >
      <template #item="{ element: ctn }">
        <li
          class="container-widget-item"
          :title="ctn.displayName"
          @dblclick="addContainerByDbClick(ctn)"
        >
          <span
            ><svg-icon :icon-class="ctn.icon" class-name="color-svg-icon" />{{
              getWidgetLabel(ctn)
            }}</span
          >
        </li>
      </template>
    </draggable>
  </div>
</template>

<script setup lang="ts">
import { ref, onMounted } from 'vue'
import { containers } from '@/utils/widgetsConfig'

onMounted(() => {})
</script>

<script lang="ts">
export default { name: 'widgetPanel' }
</script>
<style lang="scss" scoped></style>
