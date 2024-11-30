<template>
  <div class=" ">
    <div class="m-5 ticket">
      <div class="text-center dashed-border inverted-corners pt-5 pb-5 cardRight">
        <h1 class="text-xl font-bold">Coke Studio Summer Music 2024</h1>
        <p class="text-lg">(Ponchet, M.VIIZ)</p>
      </div>

      <div class="dashed-border">
        <div class="flex justify-center mb-4 mt-4">
          <!-- <img src="/public/coverimage.png" alt="QR Code" class="w-48 h-48" /> -->
          <QrcodeVue
          :value="'808386099367821599'"
          
          >
          </QrcodeVue>
        </div>
        <div>
          <p class="text-sm text-center font-bold">
            808386099367821599
          </p>
        </div>
        <div class="flex flex-row p-2">
          <div class="w-1/2 text-left">
            <p class="text-sm text-zinc-400">ເບີໂທຜູ້ຊື້</p>
            <p class="text-sm font-bold">20 9999 9999</p>
          </div>
          <div class="w-1/2 text-right">
            <p class="text-sm text-zinc-400">ປະເພດບັດ</p>
            <p class="text-sm font-bold">VIP Zone</p>
          </div>
        </div>
      </div>

      <div class="">
        <div class="flex flex-row p-2">
          <div class="w-1/2 text-left">
            <p class="text-sm text-zinc-400">ລາຄາ</p>
            <p class="text-sm font-bold">K 0</p>
          </div>
          <div class="w-1/2 text-right">
            <p class="text-sm text-zinc-400">ສະຖານະບັດ</p>
            <p class="text-sm text-green-500 font-bold">ຍັງບໍ່ທັນແລກ</p>
          </div>
        </div>
        <div class="mt-5">
          <div class="flex flex-row p-2">
            <div class="flex-1">
              <p class="text-sm text-zinc-400">ສະຖານທີ່</p>
              <p class="text-sm font-bold">ຫໍວັດທະນະທຳ</p>

              <p class="text-sm text-zinc-400">ວັນ ແລະ ເວລາກິດຈະກໍາ</p>
              <p class="text-sm font-bold">
                ສຸກ, 20 ທັນວາ 2024 &nbsp;
                <UIcon name="heroicons:at-symbol-16-solid"> </UIcon>
                &nbsp; 13:00 - 22:00
              </p>
            </div>
          </div>
        </div>
      </div>

      <div class="text-center   footer-color " >
        <img src="/public/logo.png" alt="Tickget Logo" class="w-24" />
      </div>
    </div>
  </div>
</template>
 <script>

import QrcodeVue from 'qrcode.vue'

definePageMeta({
  layout: "auth",
});
export default {
  components: {
    QrcodeVue,
  },
};
</script>
 
 <style lang="scss">
.dashed-border {
  border-bottom: 2px dashed #a0a0a0;
}

.inverted-corners {

 
}

.footer-color {
  background-color: #0f766e;
  border-bottom-left-radius: 10px;
  border-bottom-right-radius: 10px;
}

.ticket {
  /* border: dashed 1px black !important; */
  border-radius: 10px;
  background-color: white;
}

.cardRight {
  
  border-top-left-radius: 8px;
  border-bottom-right-radius: 8px;
  &:before,
  &:after {
    content: ""; 
    width: .9em;
    height: .9em;
    background: #302d2d;
    border-radius: 50%;
    left: -.5em;
  }
  &:before {
    top: -.4em;
  }
  &:after {
  bottom: -.4em;
  }
}


</style>