<template>
  <div
    class="fixed bottom-0 left-0 right-0 bg-white border-t h-20 border-gray-200"
  >
    <ul class="flex justify-around items-center h-full text-center">
      <li
        v-for="item in navigationItems"
        :key="item.text"
        class="hover:text-pink-700"
      >
        <NuxtLink :to="item.link">
          <UIcon :name="item.icon" class="text-gray-500 w-8 h-8 hover:text-pink-700" />
          <p class="text-sm mt-1">{{ item.text }}</p>
        </NuxtLink>
      </li>
    </ul>
  </div>
</template>
  
  <script>
export default {
  data() {
    return {
      navigationItems: [
        { icon: "heroicons:home-20-solid", text: "ໜ້າຫຼັກ", link: "/home" },
        {
          icon: "heroicons:ticket-16-solid",
          text: "ບັດຂອງຂ້ອຍ",
          link: "/ticket-view",
        },
      ],
    };
  },
};
</script>