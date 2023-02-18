<template>
    <div>
        <div class="tabs">
            <div :class="{ active: activeTab === 'logIn' }" @click="changeTab('logIn')">Tab 1</div>
            <div :class="{ active: activeTab === 'joinIn' }" @click="changeTab('joinIn')">Tab 2</div>
        </div>
        <div class="content">
            <div v-if="activeTab === 'logIn'">Tab 1 Content</div>
            <div v-if="activeTab === 'joinIn'">Tab 2 Content</div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            activeTab: 'logIn',
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