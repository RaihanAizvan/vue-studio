<!-- 
 
We use if else in JS and day to day programming right
Vue-ilum athu aan..
but HTML-in akath.

That’s it.

v-if = if () {}
v-else-if = else if () {}
v-else = else {}

Vue just checks your condition and decides:

“ do we need to show this element or hide it.”

Same logic as JS…
but instead of running code,
it shows/hides UI. -->

<script setup>

    // Importing 'ref' to create reactive state values
    import { ref } from 'vue'

    // Creating a reactive variable 'count'
    // Whatever is stored in count.value will update the UI automatically
    const count = ref(0)

    // function to increase the count
    // count.value is used because 'ref' stores data inside the .value property
    function inc() {
        count.value++
    }

    //function to descrease the count
    function dec() {
        count.value--
    }
</script>

<template>
    <!-- Display the current value of count -->
    <!-- Vue automatically unwraps 'ref' values in templates -->
  <h1>Count: {{ count }}</h1>
  

   <!-- CONDITIONAL RENDERING -->

   <!-- v-if:
         This paragraph ONLY exists in the DOM if count > 5.
         Vue creates/removes the actual element. -->

  <p v-if="count > 5">Count is greater than 5</p>

    <!-- v-else-if:
         Checked if the first v-if is false.
         Runs only when count === 5 -->
  <p v-else-if="count === 5">Count is exactly 5</p>

    <!-- v-else:
         This is the final fallback means jsut else.
         Renders ONLY when all above conditions are false. -->
  <p v-else>Count is less than 5</p>

  <!-- Buttons to change the count -->
  <button @click="inc">Increment</button>
  <button @click="dec">Decrement</button>
</template>
