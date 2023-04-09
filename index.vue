<script setup lang="ts">
import {onBeforeMount, ref} from 'vue'
interface Props {
  title: string
  id: string
  position: string
}
const props = defineProps<Props>()
const title = props.title
const id = props.id
const canvaClass = ref([])

const updateCanvaClass = onBeforeMount(()=>{
  const position = props.position
  const size = props.size
  let canvas_position: string = position === 'start' ? 'offcanvas-start': (position === 'bottom' ? 'offcanvas-bottom': position === 'top' ? 'offcanvas-top': 'offcanvas-end' )
  let canvas_size: string = size === 'xxl' ? 'offcanvas-xxl':
      (size === 'xl' ? 'offcanvas-xl': size === 'lg' ? 'offcanvas-lg':  size==='sm' ? 'offcanvas-end': '' )
  canvaClass.value.push(canvas_position)
  canvaClass.value.push(canvas_size)
})
</script>

<template>
  <div class="offcanvas of" :class="canvaClass" tabindex="-1" :id="id" aria-labelledby="offcanvasExampleLabel">
    <div class="offcanvas-header">
      <h5 class="offcanvas-title" id="offcanvasExampleLabel">{{ title }}</h5>
      <button type="button" class="btn-close text-reset" data-bs-dismiss="offcanvas" aria-label="Close"></button>
    </div>
    <div class="offcanvas-body">
      <slot />
    </div>
  </div>
</template>
