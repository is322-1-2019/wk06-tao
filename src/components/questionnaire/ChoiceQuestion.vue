<template>
  <div>
      <p>Q{{questionNo}}. {{questionText}}</p>
    <div class="form-check">
      <label class="form-check-label">
        <input type="radio" class="form-check-input" name="optradio" />{{choice1}}
      </label>
    </div>
    <div class="form-check">
      <label class="form-check-label">
        <input type="radio" class="form-check-input" name="optradio" />{{choice2}}
      </label>
    </div>
    <div class="form-check">
      <label class="form-check-label">
        <input type="radio" class="form-check-input" name="optradio" />{{choice3}}
      </label>
    </div>
  </div>
</template>

<script>
export default {
    props: ['questionNo', 'questionText','choice1', 'choice2', 'choice3' ],
    data: function(){
        return {
            degree : 1,
        }
    }
}
</script>