<script>
  import { Tabs, Tab, TabList, TabPanel } from "svelte-tabs";
  import Handsontable from "./Handsontable.svelte";
</script>

<style>
  main {
    font-family: sans-serif;
    text-align: center;
  }
</style>

<main>
  <h1>Select a tab</h1>
  <Tabs>
    <TabList>
      <Tab>Handsontable tab</Tab>
      <Tab>Empty tab</Tab>
    </TabList>

    <TabPanel>
      <h2>Handsontable tab</h2>
      <Handsontable />
    </TabPanel>

    <TabPanel>
      <h2>Empty tab</h2>
    </TabPanel>
  </Tabs>
</main>
