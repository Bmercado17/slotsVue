


<template>
    <form>
      <div class="help">
        <slot name="help"> </slot>
      </div>
      <div class="fields">
        <slot name="fields"></slot>
      </div>
      <div class="buttons">
        <slot name="buttons"></slot>
      </div>
      <!-- default slot dummy text on parent if nothing specified to go onto slot brackets -->
      <slot></slot>
    </form>
</template>