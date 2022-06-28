<script setup lang="ts">
import TimezoneItem from './TimezoneItem.vue'
</script>

<template>
  <div>
    <div
      v-for="(zone, idx) of zones.value"
      :key="zone.name"
      px4
      py2
      border="b base"
      relative
    >
      <TimezoneItem :timezone="zone" />
      <div
        absolute
        left="-6"
        top-0
        bottom-0
        text-xl
        flex="~ col"
        justify-center
      >
        <button
          icon-btn
          i-carbon-close
          m--1px
          title="Remove"
          @click="removeZone(zone)"
        />
        <button
          v-if="idx !== 0"
          icon-btn
          i-carbon-caret-up
          m--1px
          title="Move up"
          @click="moveZone(zone, -1)"
        />
        <button
          v-if="idx !== zones.value.length - 1"
          icon-btn
          i-carbon-caret-down
          m--1px
          title="Move down"
          @click="moveZone(zone, 1)"
        />
      </div>
    </div>
  </div>
</template>
