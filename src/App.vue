<template>

  <div class="cont">
    <h1>Hello World</h1>
  </div>
  <button class="button">Button</button>

  <div class="cont item"></div>
  <div class="circle"></div>
  <ul>
    <li class="li-1">Hello 1</li>
    <li class="li-2">Hello 2</li>
    <li class="li-3">Hello 3</li>
    <li class="li-4">Hello 4</li>
    <li class="li-5">Hello 5</li>
  </ul>
</template>

<style lang="scss">
@each $size in $sizesList {
  ul {
    .li-#{$size} {
      font-size: #{$size}5px;
    }
  }
}

body {
  background-color: setBackground(#ccc);
}

.cont {
  background-color: aqua;
  padding: 100px;

  h1 {
    font-size: $fontSize;
    font-weight: bold;
    color: red;
  }

  &.item {
    margin-top: 10px;
    border: 2px solid black;
    background-color: $color;

    &:hover {
      background-color: $myColor;
    }
  }
}

.circle {
  @include myCircle(10%);
  // background-color: setBackground(yellow);

}

.button {
  @extend %myButton;
}
</style>