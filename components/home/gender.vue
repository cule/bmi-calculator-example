<template>
  <section class="grid grid-cols-2 gap-2 mb-6">
    <div
      class="rounded-md bg-gray-800 p-4 w-full transition-all duration-300 cursor-pointer"
      @click="toggle('male')"
      :class="gender == 'male' ? null : 'opacity-25 shadow-md'"
    >
      <svg
        class="w-16 h-16 mx-auto"
        fill="#fff"
        stroke="#fff"
        viewBox="0 0 384 384"
      >
        <path
          d="M383.793 13.938c-.176-1.38-.48-2.708-.984-3.954-.016-.03-.016-.074-.024-.113 0-.008-.008-.016-.015-.023-.555-1.313-1.313-2.504-2.168-3.61-.211-.261-.418-.52-.641-.765-.914-1.032-1.906-1.985-3.059-2.762-.03-.024-.07-.031-.101-.055-1.114-.734-2.344-1.289-3.633-1.726-.32-.114-.633-.211-.961-.297C370.855.266 369.465 0 368 0H256c-8.832 0-16 7.168-16 16s7.168 16 16 16h73.367l-95.496 95.496C208.406 107.13 177.055 96 144 96 64.602 96 0 160.602 0 240s64.602 144 144 144 144-64.602 144-144c0-33.04-11.121-64.383-31.504-89.871L352 54.625V128c0 8.832 7.168 16 16 16s16-7.168 16-16V16c0-.336-.078-.656-.098-.984a16.243 16.243 0 00-.109-1.079zM144 352c-61.762 0-112-50.238-112-112s50.238-112 112-112c29.902 0 58.055 11.64 79.223 32.734C244.359 181.945 256 210.098 256 240c0 61.762-50.238 112-112 112zm0 0"
        />
      </svg>
      <p class="text-center mt-8 uppercase font-bold">male</p>
    </div>
    <div
      class="rounded-md bg-gray-800 p-4 w-full transition-all duration-300 cursor-pointer"
      @click="toggle('female')"
      :class="gender == 'female' ? null : 'opacity-25 shadow-md'"
    >
      <svg
        class="w-16 h-16 mx-auto"
        fill="#fff"
        stroke="#fff"
        viewBox="-56 0 384 384"
      >
        <path
          d="M272 136C272 61.008 210.992 0 136 0S0 61.008 0 136c0 69.566 52.535 127.016 120 134.977V304H88c-8.832 0-16 7.168-16 16s7.168 16 16 16h32v32c0 8.832 7.168 16 16 16s16-7.168 16-16v-32h32c8.832 0 16-7.168 16-16s-7.168-16-16-16h-32v-33.023c67.465-7.961 120-65.41 120-134.977zm-240 0C32 78.656 78.656 32 136 32s104 46.656 104 104-46.656 104-104 104S32 193.344 32 136zm0 0"
        />
      </svg>
      <p class="text-center mt-8 uppercase font-bold">female</p>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      gender: "male"
    };
  },
  methods: {
    toggle(val) {
      this.gender = val;
      this.$emit("genderListener", val);
    }
  }
};
</script>
