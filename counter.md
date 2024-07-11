# Counter Demo

<div ref="el" />

<script setup>
import { createElement } from 'hono/jsx'
import { createRoot } from 'hono/jsx/dom/client'
import { ref, onMounted } from 'vue'
import Counter from './Counter'

const el = ref()
onMounted(() => {
  const root = createRoot(el.value)
  root.render(createElement(Counter, {}, null))
})
</script>

<style scoped>
div:deep(button) {
  margin-top: 20px;
  display: inline-block;
  outline: 0;
  cursor: pointer;
  padding: 5px 16px;
  font-size: 14px;
  font-weight: 500;
  line-height: 20px;
  vertical-align: middle;
  border: 1px solid;
  border-radius: 6px;
  color: #24292e;
  background-color: #fafbfc;
  border-color: #1b1f2326;
  box-shadow: rgba(27, 31, 35, 0.04) 0px 1px 0px 0px, rgba(255, 255, 255, 0.25) 0px 1px 0px 0px inset;
  transition: 0.2s cubic-bezier(0.3, 0, 0.5, 1);
  transition-property: color, background-color, border-color;
}

div:deep(button:hover) {
  background-color: #f3f4f6;
  border-color: #1b1f2326;
  transition-duration: 0.1s;
}
</style>
