<template>
  <div>
    <h1>Spacing</h1>
    <table>
      <thead>
        <tr>
          <td>Variable</td>
          <td>Description</td>
          <td>Default Size</td>
          <td>Calculation</td>
        </tr>
      </thead>
      <tr v-for="space in spaces" :key="space">
          <td class="code">--space-{{ space.size }}</td>
          <td :class="{free : space.isFree}">{{space.description}}</td>
          <td>{{ space.size}}px</td>
          <td class="code">calc({{space.size}} * var(--def-space-increment));</td>
      </tr>
    </table>
  </div>
</template>

<script>
export default {
  data() {
    return {
      spaces: [
        { size: 2, description: "free", isFree: true },
        { size: 4, description: "To form a bound between two elements" },
        { size: 8, description: "Between elements in close relationship" },
        { size: 12, description: "free", isFree: true },
        { size: 16, description: "Default space between related UI elements" },
        { size: 24, description: "free", isFree: true },
        { size: 32, description: "Minimum between unrelated UI elements" },
        { size: 40, description: "free", isFree: true },
        { size: 48, description: "free", isFree: true },
        { size: 64, description: "free", isFree: true },
      ],
    };
  },
};
</script>

<style scoped>
table {
   width:100%;
   overflow-wrap: break-word;
}

thead {
    background-color: var(--color-background-3);
    color: var(--color-foreground-3);
}

thead td {
    padding: var(--space-16);
}
td {
    padding: var(--space-4) var(--space-16);
}
tr:nth-child(2n + 1) {
    background-color: var(--color-background-2);
}
.code {
    font-family: monospace;
    color:seagreen;
}

.free {
    font-style: italic;
    color: var(--color-foreground-2);
}
</style>