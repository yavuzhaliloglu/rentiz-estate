<template>
  <div class="features">
    <ProfileDefaultInput :obj="obj">
      <CommonInputComponent
        v-for="(item, index) in inputlist.defaultInputs"
        :key="item.name"
        v-model="obj.defaults[index]"
        :type="item.type"
        :title="item.name"
        class="col-md-6"
      />
      <CommonSelectComponent
        v-for="(item, index) in inputlist.selectInputs"
        :key="item.name"
        v-model="obj.selects[index]"
        :title="item.name"
        :options="item.options"
        class="col-md-6"
      />

      <!-- <CommonSelectComponent
        v-model="obj.landStatus"
        :title="inputlist.landStatus.title"
        :options="inputlist.landStatus.options"
      />

      <CommonInputComponent
        v-model="obj.squareMeters"
        :title="inputlist.squareMeters.title"
        :type="inputlist.squareMeters.type"
      />

      <CommonInputComponent
        v-model="obj.parcel"
        :title="inputlist.parcel.title"
        :type="inputlist.parcel.type"
      /> -->
    </ProfileDefaultInput>
  </div>
</template>

<script>
export default {
  name: 'ArsaFeatures',
  layout: 'UserProfile',
  data() {
    return {
      inputlist: null,
      obj: {
        selects: [],
        defaults: []
      }
    }
  },
  created() {
    this.setValues()
  },
  methods: {
    setValues() {
      this.inputlist = this.$store.getters.getLandInputs
    }
  }
}
</script>

<style lang="scss" scoped></style>
