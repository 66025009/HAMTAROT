<template>
  <dialog id="ratingModal" class="modal">
    <div class="modal-box bg-gray text-black text-center space-y-4">
      <img
        class="mx-auto"
        src="/public/ICON/rating.png"
        alt="Star Icon"
        width="100px"
      />
      <h1 class="text-lg">
        <b>คุณพึงพอใจกับเว็บไซต์เรามากแค่ไหน?</b>
      </h1>
      <p class="flex justify-between px-10">
        <span>ปรับปรุง</span>
        <span>ดีมาก</span>
      </p>
      <div class="rating rating-lg flex justify-center space-x-2">
        <input
          type="radio"
          name="rating"
          class="mask mask-star-2 bg-orange-400"
          checked
        />
        <input
          type="radio"
          name="rating"
          class="mask mask-star-2 bg-orange-400"
        />
        <input
          type="radio"
          name="rating"
          class="mask mask-star-2 bg-orange-400"
        />
        <input
          type="radio"
          name="rating"
          class="mask mask-star-2 bg-orange-400"
        />
        <input
          type="radio"
          name="rating"
          class="mask mask-star-2 bg-orange-400"
        />
      </div>
      <div class="modal-action flex justify-center">
        <form method="dialog">
          <button class="btn btn-neutral">ให้คะแนน</button>
        </form>
      </div>
    </div>
  </dialog>
</template>

<script>
export default {
  mounted() {
    setTimeout(() => {
      const modal = document.getElementById("ratingModal");
      if (modal) {
        modal.showModal();
      }
    }, 5000);
  },
};
</script>
