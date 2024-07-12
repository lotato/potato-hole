<!-- src/views/Home.vue -->
<template>
  <div>
    <h1>暴击计算器</h1>
    <p>裸装攻击:</p>
    <input type="float" v-model="base_attack" placeholder="请输入裸装攻击" />
    <p>裸装暴击伤害:</p>
    <input type="float" v-model="base_crit_rate" placeholder="请输入裸装暴击率" />
    <p>裸装暴击率:</p>
    <input type="float" v-model="base_crit_damage" placeholder="请输入裸装暴击伤害" />
    <span>暴击伤害：{{ crit_damage }}</span>
  </div>
</template>

<script>
export default {
  name: "CritCalculator",
  data() {
    return {
      base_attack: 0,
      base_crit_rate: 0,
      base_crit_damage: 0,
    };
  },
  computed: {
    crit_damage() {
      return (
        this.base_attack *
        (1 + ((this.base_crit_rate / 100 - 1) * this.base_crit_damage) / 100)
      );
    },
  },
};
</script>
