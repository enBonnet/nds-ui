<script lang="ts">
  import classnames from "classnames";
  export let size: "sm" | "md" | "lg" | "xl" = "md";
  export let color: "green" | "red" | "blue" | "base" = "base";
  const cn = classnames("button", size, color);
</script>

<button class={cn}>
  <slot />
</button>

<style>
  /* base */
  .button {
    position: relative;
    font-weight: 700;
    padding: 11px 22px;
    font-size: inherit;
    overflow: hidden;
    margin: 18px 0 20px;
    top: -8px;
    border-radius: 10px;
    color: #050505;
  }
  /* customizations */
  .button.green {
    border: solid 2px #165a38;
    background: #67daa2;
    box-shadow: 0 6px 0 0#165a38;
  }
  .button.green:hover {
    box-shadow: 0 4px 0 0#165a38,0 4px 4px 0 rgba(0,0,0,.4);
  }
  .button.green:active {
    top: 0;
    box-shadow: 0 0 0 0#165a38;
  }
  .button.red {
    border: solid 2px #5e1817;
    background: #df7d7c;
    box-shadow: 0 6px 0 0#5e1817;
  }
  .button.red:hover {
    box-shadow: 0 4px 0 0#5e1817,0 4px 4px 0 rgba(0,0,0,.4);
  }
  .button.red:active {
    top: 0;
    box-shadow: 0 0 0 0#5e1817;
  }
  .button.blue {
    border: solid 2px #16345a;
    background: #679fda;
    box-shadow: 0 6px 0 0#16345a;
  }
  .button.blue:hover {
    box-shadow: 0 4px 0 0#16345a,0 4px 4px 0 rgba(0,0,0,.4);
  }
  .button.blue:active {
    top: 0;
    box-shadow: 0 0 0 0#16345a;
  }
  .button.base {
    border: solid 2px #8d8a86;
    background: #c3c2c0;
    box-shadow: 0 6px 0 0#8d8a86;
  }
  .button.base:hover {
    box-shadow: 0 4px 0 0#8d8a86,0 4px 4px 0 rgba(0,0,0,.4);
  }
  .button.base:active {
    top: 0;
    box-shadow: 0 0 0 0#8d8a86;
  }
  /* status */
  .button:hover {
    cursor: pointer;
    top: -4px;
  }
  .button:focus {
    outline: solid 4px #d8b600;
    background: #ffd90c;
    outline-offset: -6px;
    color: #050505;
    text-decoration: none;
    opacity: 1;
  }
</style>