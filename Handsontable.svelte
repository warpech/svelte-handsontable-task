<script>
  import { onMount } from "svelte";
  import Handsontable from "handsontable";

  let hot;
  let gridElement;
  let data = [
    ["", "Ford", "Tesla", "Toyota", "Honda"],
    ["2017", 10, 11, 12, 13],
    ["2018", 20, 11, 14, 13],
    ["2019", 30, 15, 12, 13],
  ];

  onMount(() => {
    hot = new Handsontable(gridElement, {
      data: data,
      columns: [
        { type: "text" },
        { type: "text" },
        { type: "text" },
        { type: "text" },
        { type: "text" },
      ],
      colHeaders: true,
      rowHeaders: true,
      dropdownMenu: true,
      filters: true,
    });
  });
</script>

<div bind:this={gridElement} />

<link
  href="https://cdn.jsdelivr.net/npm/handsontable@8.1.0/dist/handsontable.full.min.css"
  rel="stylesheet"
  media="screen" />
