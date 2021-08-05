<template>
  <div class="home">
    <h3>Contact Info</h3>
    <p>{{ contactInfo.name }}</p>
    <p>{{ contactInfo.email }}</p>
    <p>{{ contactInfo.phone }}</p>

    <h3>Shipping Info</h3>
    <p>{{ shippingInfo.street }}</p>
    <p>{{ shippingInfo.state }}</p>
    <p>{{ shippingInfo.zip }}</p>
  </div>
</template>

<script>
export default {
  props: {
    contactInfo: Object,
    shippingInfo: Object
  }
}
</script>
