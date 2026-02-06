<template>
  <div ref="mapEl" class="map"></div>
</template>

<script setup>
import { onMounted, ref } from 'vue'

const mapEl = ref(null)

const coords = [51.508675, -0.142156]

onMounted(() => {
  ymaps.ready(() => {
    const map = new ymaps.Map(
      mapEl.value,
      {
        center: coords,
        zoom: 15,
        controls: [],
      },
      {
        suppressMapOpenBlock: true,
      }
    )

    map.behaviors.disable([
      'scrollZoom',
      'dblClickZoom',
      'multiTouch',
      'rightMouseButtonMagnifier',
    ])

    map.behaviors.enable('drag')

    map.options.set({
      yandexMapDisablePoiInteractivity: true,
    })

    const placemark = new ymaps.Placemark(
      coords,
      {},
      {
        iconLayout: 'default#image',
        iconImageHref: new URL('@/assets/map/map-pin.svg', import.meta.url).href,
        iconImageSize: [32, 42],
        iconImageOffset: [-16, -42],
      }
    )

    map.geoObjects.add(placemark)
  })
})
</script>

<style scoped>
.map {
  width: 100%;
  height: 100%;
  min-height: 400px;
  filter: grayscale(1) brightness(0.93) contrast(1.25);
}
</style>
