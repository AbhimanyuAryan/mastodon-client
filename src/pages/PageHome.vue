<template>
  <q-page>
    <div class="q-py-lg q-px-md row items-end q-col-gutter-md">
      <div class="col">
        <q-input
          v-model="newtootContent"
          bottom-slots
          class="new-toot"
          autogrow
          placeholder="What's Happening"
          counter
          maxlength="280"
        >
          <template v-slot:before>
            <q-avatar size="xl">
              <img src="https://abhimanyuaryan.com/static/567052a18f9b22d3259f4fedd7553b37/eac94/avatar.jpg">
            </q-avatar>
          </template>
        </q-input>
      </div>
      <div class="col col-shrink">
        <q-btn
              :disabled="!newtootContent"
              class="q-mb-lg"
              unelevated
              rounded
              no-caps
              color="primary"
              label="Toot" />
      </div>
    </div>
    <q-separator
      size="10px"
      color="grey-2" 
      class="divider"/>
  </q-page>
</template>

<script>
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'PageHome',
  data() {
    return {
      newtootContent: ''
    }
  }
})
</script>

<style lang="sass">
.new-toot
  textarea
    font-size: 14px
    line-height: 1.4 !important

.divider
  border-top: 1px solid
  border-bottom: 1px solid
  border-color: $grey-3
</style>