<template>
  <div>
    <treeselect
      :multiple="true"
      :flat="true"
      :labelOnlySelectSelf="true"
      :autoSelectDescendants="true"
      :autoDeselectDescendants="true"
      :options="options"
      :alwaysOpen="true"
      placeholder="Select your favourite(s)..."
      v-model="value"
      />
    <treeselect-value :value="value" />
  </div>
</template>

<script>
  export default {
    data: () => ({
      value: [],
      options: [ {
        id: 'fruits',
        label: 'Fruits',
        isExpanded: true,
        children: [ {
          id: 'apple',
          label: 'Apple 🍎',
          isNew: true,
        }, {
          id: 'grapes',
          label: 'Grapes 🍇',
        }, {
          id: 'pear',
          label: 'Pear 🍐',
        }, {
          id: 'strawberry',
          label: 'Strawberry 🍓',
        }, {
          id: 'watermelon',
          label: 'Watermelon 🍉',
        } ],
      }, {
        id: 'vegetables',
        label: 'Vegetables',
        children: [ {
          id: 'corn',
          label: 'Corn 🌽',
        }, {
          id: 'carrot',
          label: 'Carrot 🥕',
        }, {
          id: 'eggplant',
          label: 'Eggplant 🍆',
        }, {
          id: 'tomato',
          label: 'Tomato 🍅',
        } ],
      } ],
    }),
  }
</script>
