<template>
  <div class="min-h-screen bg-gray-100 flex items-center justify-center p-6">
    <div class="w-full max-w-2xl bg-white rounded-2xl shadow p-6">
      <h1 class="text-2xl font-bold mb-6">Settings</h1>

      <!-- Profile -->
      <section class="mb-6">
        <h2 class="text-lg font-semibold mb-3">Profile</h2>
        <div class="space-y-3">
          <input
            v-model="settings.username"
            type="text"
            placeholder="Username"
            class="w-full px-4 py-2 border rounded-lg focus:outline-none focus:ring"
          />
          <input
            v-model="settings.email"
            type="email"
            placeholder="Email"
            class="w-full px-4 py-2 border rounded-lg focus:outline-none focus:ring"
          />
        </div>
      </section>

      <!-- Preferences -->
      <section class="mb-6">
        <h2 class="text-lg font-semibold mb-3">Preferences</h2>
        <div class="flex items-center justify-between mb-3">
          <span>Dark Mode</span>
          <input type="checkbox" v-model="settings.darkMode" class="toggle" />
        </div>
        <div class="flex items-center justify-between">
          <span>Notifications</span>
          <input type="checkbox" v-model="settings.notifications" class="toggle" />
        </div>
      </section>

      <!-- Actions -->
      <div class="flex justify-end space-x-3">
        <button
          @click="reset"
          class="px-4 py-2 rounded-lg border"
        >
          Reset
        </button>
        <button
          @click="save"
          class="px-4 py-2 rounded-lg bg-blue-600 text-white"
        >
          Save
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SettingsPage",
  data() {
    return {
      settings: {
        username: "",
        email: "",
        darkMode: false,
        notifications: true,
      },
    };
  },
  methods: {
    save() {
      alert("Settings saved!\n" + JSON.stringify(this.settings, null, 2));
    },
    reset() {
      this.settings = {
        username: "",
        email: "",
        darkMode: false,
        notifications: true,
      };
    },
  },
};
</script>

<style>
/* Simple toggle style */
.toggle {
  width: 40px;
  height: 20px;
}
</style>
