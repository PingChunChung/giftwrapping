<template>
  <div class="mx-auto max-w-5xl py-4 px-4">
    <div class="flex gap-5">
      <Fancybox class="flex flex-col justify-between">
        <a data-fancybox href="https://lipsum.app/id/61/1600x1200">
          <img src="@/assets/img/prod_1_s.png" />
        </a>
        <a data-fancybox href="https://lipsum.app/id/61/1600x1200">
          <img src="@/assets/img/prod_1_s.png" />
        </a>
        <a data-fancybox href="https://lipsum.app/id/61/1600x1200">
          <img src="@/assets/img/prod_1_s.png" />
        </a>
        <a data-fancybox href="https://lipsum.app/id/61/1600x1200">
          <img src="@/assets/img/prod_1_s.png" />
        </a>
      </Fancybox>

      <Fancybox class="flex flex-col justify-between">
        <a data-fancybox href="https://lipsum.app/id/61/1600x1200">
          <img src="@/assets/img/prod_1.png" />
        </a>
      </Fancybox>

      <div class="flex flex-col gap-4">
        <h2 class="text-2xl font-bold">抽屜禮盒</h2>

        <p class="text-sm text-muted-200">
          包裝設計
          以三個英文字「i」為主體造形，融入整體設計當中，整體設計簡約卻不失質感的紙盒抽屜禮盒。
        </p>

        <hr class="border-muted-100" />

        <span>
          價格範圍：
          <span class="ml-[6px] text-muted-200">$350.00/個</span>
        </span>

        <div class="flex">
          <div class="flex">單一尺寸：</div>
          <div class="ml-[6px] text-muted-200">
            <div>長 x 寬 x 高(公釐mm)</div>
            <div>300 x 200 x 100</div>
          </div>
        </div>

        <span class="text-sm">備註：數量300以上以需客製化歡迎來訊</span>

        <span class="text-sm">誤差：±2mm為正常誤差值</span>

        <div class="flex gap-5">
          <div class="flex flex-1">
            <a
              href="javascript: void(0)"
              class="-mr-[2px] flex items-center justify-center rounded-l border-2 border-muted-100 px-2 duration-200 hover:bg-primary-100 hover:text-white"
              @click.prevent="minusNum()"
            >
              <i class="fa-solid fa-minus"></i>
            </a>
            <span
              class="flex w-full items-center justify-center border-2 border-muted-100"
            >
              {{ num }}
            </span>
            <a
              href="javascript: void(0)"
              class="-ml-[2px] flex items-center justify-center rounded-r border-2 border-muted-100 px-2 duration-200 hover:bg-primary-100 hover:text-white"
              @click.prevent="addNum()"
            >
              <i class="fa-solid fa-plus"></i>
            </a>
          </div>

          <a
            href="javascript: void(0)"
            class="flex flex-1 items-center justify-center rounded bg-primary-100 py-[10px] text-white duration-200 hover:bg-primary-200"
          >
            購買
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Fancybox from "@/components/plugins/Fancybox.vue";

export default {
  data() {
    return {
      num: 1,
    };
  },
  methods: {
    minusNum() {
      if (this.num > 1) this.num--;
    },
    addNum() {
      this.num++;
    },
  },
  components: {
    Fancybox,
  },
};
</script>

<style></style>
