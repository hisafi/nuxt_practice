<template>
  <div class="container">
    <ul>
      <li>
        <label>身長</label>
        <input type="number" v-model="tall" />
        <span>{{tall}}cm</span>
      </li>
      <li>
        <label>体重</label>
        <input type="number" v-model="weight" />
        <span>{{weight}}kg</span>
      </li>
      <li>BMI(Body Mass Index) = {{ format(bmi) }}</li>
      <li>適正体重 = {{ format(standard_weight) }} kg</li>
      <li>適正体重との差 = kg</li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      tall: 180,
      weight: 80
    };
  },
  computed: {
    tall_m() {
      return this.tall / 100;
    },
    bmi() {
      return this.weight / (this.tall_m * this.tall_m);
    },
    standard_weight() {
      return this.tall_m * this.tall_m * 22;
    }
  },
  methods: {
    format(value) {
      const x100 = value * 100;
      return Math.round(x100) / 100;
    }
  }
};
</script>
