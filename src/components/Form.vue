<template>
  <div class="container">
    <h5 style="color:black !important;">Let's discuss your business ideas below!</h5>
    <form action="https://formsubmit.co/photographybuba@gmail.com" method="POST" class="form">
      <div class="d-flex justify-content-between">
        <input type="text" id="name" placeholder="Name*">
        <input type="email" name="email"  placeholder="Email*" required>
        <input type="hidden" name="_next" value="https://bubaphotography.com">
        <input type="text" name="subject"  placeholder="Subject*">
      </div>
      <textarea placeholder="Message*" name="text" class="col"></textarea>
      <button type="submit">Send</button>
      
    </form>
  </div>
</template>

<script>


</script>

<style setup>
h5 {
    margin:50px 0 80px 0;
}
input[type="text"],input[type="email"], textarea {
    display: inline-block;
    width: 29%;
    margin: 0 0% 30px;
    padding: 8px 0 12px;
    outline: none;
    border: 0;
    border-bottom: 1px solid #aaa;
    font-size: 14px;
    font-family: Playfairdisplay_regular;
}
textarea {
    width: 100%;
    height: 44px;
}
button {
    border: 0;
    padding: 9px 30px;
    border-radius: 3px;
    background-color: #333;
    color: #fff;
    font-size: 16px;
}


</style>