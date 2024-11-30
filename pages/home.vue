<template>
  <img src="/public/coverimage.png" alt="Cover Image" class="w-full mb-2" />
  
    <UTabs :items="items" v-model="activeTab">
      <template #icon="{ item, selected }">
        <UIcon
          :name="item.icon"
          class="w-4 h-4 flex-shrink-0 me-2"
          :class="[selected && 'text-primary-500 dark:text-primary-400']"
        />
      </template>

      <template #item="{ item }">
        <div v-if="item.key === 'ticket'">

          <UContainer>

         
          <UCard class="bg-white p-2 rounded shadow-md mb-3">
            <h1 class="text-xl font-bold">
              Coke Studio Summer Music 2024 (Ponchet, M.VIIZ)
            </h1>
            <p class=" text-zinc-500">
            <UIcon name="heroicons:calendar"></UIcon>
              ສຸກ, 20 ທັນວາ 2024
            </p>
            <p class="text-zinc-500">
              <UIcon name="heroicons:clock"></UIcon>
              13:00-22:00
            </p>
            <p class="text-zinc-500">
              <UIcon name="heroicons:map-pin-16-solid"></UIcon>
              ຫໍວັດທະນະທຳ
            </p>
          </UCard>

          <UCard class="mb-20">
            <div class="mb-4">
              <label for="couponCode" class="block mb-2">ປ້ອນລະຫັດຄູປອງເພື່ອແລກຮັບບັດເຂົ້າງານ</label>
              <UInput
               style="text-align: center!important;"
                id="couponCode"
                v-model="couponCode"
                size="xl"
                 class="w-full text-center"
                placeholder="ປ້ອນລະຫັດຄູປອງ"
              />
            </div>

            <!-- <UButton type="submit" class="bg-blue-500 hover:bg-blue-700 text-white"
        >ຕົກລົງ</UButton

      > -->

            <UButton
              @click="onSubmit()"
              :ui="{ rounded: 'rounded-full' }"
              block
              class="mt-2 bg-red-500 hover:bg-red-600 text-white p-5"
            >
              ຕົກລົງ
            </UButton>
          </UCard>
        </UContainer>
        </div>
      </template>
    </UTabs>


    <UModal v-model="isOpen">
      <div class="p-4 text-center">
       <UIcon
       name="heroicons:check-circle-16-solid"
       class="w-10 h-10"
       >

       </UIcon>
       <p class="text-lg">ສໍາເລັດ</p>
      </div>
    </UModal>
</template>

<script>
definePageMeta({
  layout: "auth",
});
export default {
  data() {
    return {
      isOpen: false,
      activeTab: null,
      items: [
        {
          key: "ticket",
          label: "ບັດເຂົ້າງານ",
          icon: "heroicons:ticket",
        },
        {
          key: "about",
          label: "ກ່ຽວກັບງານ",
          icon: "heroicons:information-circle",
        },
      ],
    };
  },
  methods: {
    onSubmit() {
        this.isOpen = true;
    }
  },
};
</script>

<style>
</style>