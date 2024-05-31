<template>
  <div class="wrapp">
    <div class="content">
      <h1 class="title">Animated <span>input text</span></h1>
      <div class="form">
        <div class="form__item">
          <input
            type="text"
            class="form__input-text"
            name="nameCompany"
            autocomplete="off"
            required
          />
          <label for="nameCompany" class="form__label">
            <span class="form__label-name">Name *</span>
            <div class="form__label-line">
              <div class="form__label-bg"></div>
            </div>
            <div class="form__label-sq"></div>
          </label>
        </div>
        <div class="form__item">
          <input
            type="text"
            class="form__input-text"
            name="telephoneCompany"
            autocomplete="off"
            required
          />
          <label for="telephoneCompany" class="form__label">
            <span class="form__label-name">Telephone *</span>
            <div class="form__label-line">
              <div class="form__label-bg"></div>
            </div>
            <div class="form__label-sq"></div>
          </label>
        </div>
        <div class="form__item">
          <input
            type="text"
            class="form__input-text"
            name="emailCompany"
            autocomplete="off"
            required
          />
          <label for="emailCompany" class="form__label">
            <span class="form__label-name">E-mail *</span>
            <div class="form__label-line">
              <div class="form__label-bg"></div>
            </div>
            <div class="form__label-sq"></div>
          </label>
        </div>

        <button class="form__btn">
          <span class="form__btn-txt">submit</span>
          <div class="form__btn-bg"></div>
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
:root {
  --pr-color: #fff;
  --second-color: #0a0a0a;
  --cubicbz: cubic bezier(0.9, 0, 0.1, 1);
  --fz-big: 80px;
  --bg-gradient1: linear-gradient(
    9deg,
    rgba(47, 230, 255, 1),
    rgba(15, 255, 98, 1) 86%
  );
  --bg-gradient2: linear-gradient(135deg, #242424 0%, #131313 100%);
  --transition: 0.4s;
}
body {
  background: var(--second-color);
}
.wrapp {
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  height: 100vh;
  z-index: 1;
}
.title {
  margin: 0;
  font-size: var(--fz-big);
  text-transform: uppercase;
  color: var(--pr-color);
  letter-spacing: 5px;
}
.title span {
  display: block;
  color: transparent;
  -webkit-text-stroke: 1px var(--pr-color);
}
.content {
  position: relative;
  width: 1025px;
}
.content::before {
  position: absolute;
  content: "";
  width: 2px;
  height: calc(100% - 19px);
  top: 19px;
  left: -50px;
  background: var(--bg-gradient1);
}
.form {
  margin-top: 50px;
}
.form__item {
  position: relative;
  max-width: 100%;
  margin-bottom: 30px;
}
.form__input-text {
  width: 100%;
  height: 60px;
  padding-left: 40px;
  padding-right: 10px;
  font-size: 16px;
  color: var(--pr-color);
  line-height: 47px;
  border: none;
  border-radius: 5px;
  outline: none;
  background: none;
}
.form__label {
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  height: 100%;
  pointer-events: none;
}
.form__label-name {
  position: absolute;
  left: 40px;
  top: 50%;
  color: var(--pr-color);
  font-size: 18px;
  line-height: 0.9;
  letter-spacing: 2px;
  text-transform: uppercase;
  transform: translateY(-50%);
  transform-origin: left;
  transition: all 0.4s;
}
.form__label-sq {
  position: absolute;
  width: 20px;
  height: 20px;
  top: 50%;
  left: 3px;
  opacity: 0.4;
  background: var(--bg-gradient1);
  transform: translateY(-50%) rotate(-45deg);
  transition: all 0.4s;
}
.form__label-line {
  position: absolute;
  width: 100%;
  height: 2px;
  bottom: 2px;
  background: var(--bg-gradient2);
  pointer-events: none;
  overflow: hidden;
}
.form__label-bg {
  width: 100%;
  height: 100%;
  background: var(--bg-gradient1);
  transform: translateX(-110%);
  transition: all 0.4s;
}

.form__input-text:focus + .form__label .form__label-name,
.form__input-text:valid + .form__label .form__label-name {
  transform: translateY(-33px) scale(0.7);
  color: #ffffff50;
}

.form__input-text:focus + .form__label .form__label-bg,
.form__input-text:valid + .form__label .form__label-bg {
  transform: translateX(0%);
}

.form__input-text:focus + .form__label .form__label-sq,
.form__input-text:valid + .form__label .form__label-sq {
  opacity: 1;
  transform: translateY(-50%) rotate(-405deg);
}
.form__btn {
  position: relative;
  display: block;
  width: 100%;
  padding: 30px 0;
  margin-top: 10px;
  outline: none;
  border: none;
  color: var(--pr-color);
  font-size: 18px;
  text-align: center;
  cursor: pointer;
  border-radius: 5px;
  background: var(--bg-gradient2);
  overflow: hidden;
  text-transform: uppercase;
}
.form__btn-txt {
  position: relative;
  letter-spacing: 4px;
  pointer-events: none;
  transition: all 0.4s;
  z-index: 2;
}
.form__btn:hover .form__btn-txt {
  letter-spacing: 15px;
  color: #0a0a0a;
}
.form__btn-bg {
  position: absolute;
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
  pointer-events: none;
  transform: translateX(-102%);
  background: var(--bg-gradient1);
  transition: all 0.4s;
  z-index: 1;
}
.form__btn:hover .form__btn-bg {
  transform: translateX(0);
}
</style>
