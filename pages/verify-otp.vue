<template>
  <div class="p-6 text-center" style="background-color: #f4f4f5">
    <div class="flex justify-between items-center">
      <UCloseButton />
    </div>

    <h2 class="text-xl font-semibold mt-6 h1">ເຂົ້າສູ່ລະບົບ</h2>
    <p class="text-gray-600 mt-2">
      ປ້ອນລະຫັດ OTP ຈຳນວນ 6 ໂຕເລກ ທີ່ສົ່ງໄປເບີ 20999999XX
    </p>

    <div class="mt-4">
      <UInput
      style="text-align: center!important;"
        v-model="phoneNumber"
        placeholder="XXX XXX"
        type="tel"
        class="w-full text-center py-2"
        size="xl"
      />
    </div>

    <UButton
      @click="goto()"
      :ui="{ rounded: 'rounded-full' }"
      block
      class="mt-32 bg-red-500 hover:bg-red-600 text-white p-5"
    >
      ຖັດໄປ
    </UButton>
  </div>
</template>
  

 
  <script>

definePageMeta({
  layout: "unauth",
});
const phoneNumber = ref("");
export default {
  setup() {
  },

  methods: {
    goto() {
      this.$router.push("/home");
    },
  },
};
</script>