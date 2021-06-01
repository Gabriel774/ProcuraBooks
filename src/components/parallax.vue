<template>
  <div id="inicio">
    <h1 class="titletxt">ProcuraBooks</h1>
    <h1 class="subtitle">O lar dos Books</h1>
  </div> 
</template>

<script>
export default {
  
};
</script>

<style scoped>
#inicio {
  background-image: url("./img/matthew-feeney-Nwkh-n6l25w-unsplash.jpg");
  height: 650px;
  width: 100%;
  background-attachment: fixed;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  text-align: center;
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
  margin: auto;
  flex-direction: column;
}
.titletxt {
  font-family: "Major Mono Display", monospace;
  font-size: 48pt;
  color: white;
  opacity: 0.89;
  text-shadow: 5px 5px 5px rgba(0, 0, 0, 0.541);
}

.subtitle {
  color: white;
  opacity: 0.89;
}

@media (max-width: 720px) {
  .titletxt {
    font-size: 28pt;
  }
  .subtitle {
    font-size: 18pt;
  }
}
@media (max-width: 340px) {
  .titletxt {
    font-size: 18pt;
  }
  .subtitle {
    font-size: 14pt;
  }
}
</style>