<!-- * computer property is a value that depends on other state -->
<!-- and it automatically updates when that state chanegs  -->

<!-- 
When to use?

Whenever we want:

– derived values
– formatted values
– something that depends on other reactive data
– something we want cached 

-->

<!-- 
Why not just use a normal function?

Because computed() remembers the result
and only recalculates when needed.

Functions run every time you use them.
Computed runs only when its dependencies change. 

-->

<script setup>

    // Here we are importing hte computed Fn from vue
    import { computed, ref } from "vue";

    // Base reactive states
    const firstName = ref('raihan');
    const lastName = ref("muhammed");

    // Computed property that derives a new value from existing state
    // Automatically updates when firstName or lastName changes
    const fullName = computed(() => firstName.value + ' ' + lastName.value);

    // that means whenever firstname chanegs, full name also changes 
</script>

<template>
    <!-- Displaying the computed fullName -->
    <!-- fullName automatically updates when firstName or lastName changes -->
    <h1> Full Name : {{ fullName }}</h1>
</template>

<!--! Computed = reactive value generated from other reactive values. -->