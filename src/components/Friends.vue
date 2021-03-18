<template>
  <li>
    <h2>
      <button :click="toggleDetails">
        {‌{ detailsAreVisible ? 'Hide' : 'Show' }} Details
      </button>
      <ul v-if="detailsAreVisible">
        <li>{{ friend.phone }}</li>
        <li>{{ friend.mail }}</li>
      </ul>
    </h2>
  </li>
</template>

<script>
export default {
  data() {
    return {
      detailsAreVisible: false,
      friend: {
        id: "ned",
        name: "Neeraj",
        phone: "0123 456",
        email: "aaa@gmail.com",
      },
    };
  },
  methods: {
    toggleDetails() {
      this.detailsAreVisible = !this.detailsAreVisible;
    },
  },
};
</script>