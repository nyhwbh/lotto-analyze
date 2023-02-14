<template>
  <div>
    <div class="tabs">
      <div :class="{ active: activeTab === 'tab1' }" @click="changeTab('tab1')">Tab 1</div>
      <div :class="{ active: activeTab === 'tab2' }" @click="changeTab('tab2')">Tab 2</div>
      <div :class="{ active: activeTab === 'tab3' }" @click="changeTab('tab3')">Tab 3</div>
    </div>
    <div class="content">
      <div v-if="activeTab === 'tab1'">Tab 1 Content</div>
      <div v-if="activeTab === 'tab2'">Tab 2 Content</div>
      <div v-if="activeTab === 'tab3'">Tab 3 Content</div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      activeTab: 'tab1',
    };
  },
  methods: {
    changeTab(tab) {
      this.activeTab = tab;
    },
  },
};
</script>

<style>
.tabs {
  display: flex;
  background-color: #eee;
}

.tabs div {
  flex: 1;
  text-align: center;
  padding: 10px 0;
  cursor: pointer;
}

.tabs .active {
  background-color: #fff;
}

.content {
  padding: 20px;
}
</style>