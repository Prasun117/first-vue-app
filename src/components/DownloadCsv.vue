<template>
  <div>
    <button @click="downloadCsv">click</button>
  </div>
</template>
<script>
export default {
  name: "download-csv",
  data() {
    return {
      data: [
        { path: "/content/java/util", type: "folder" },
        { path: "content/java/util/io.class", type: "file" },
      ],
    };
  },
  methods: {
    downloadCsv() {
      let dataRows = "Path,Filename";
      let flatdataForCsv = this.data.map((item, index, arr) => {
        let itemPathToArray = item.path.split("/");
        return [
          item.path,
          item.type === "folder"
            ? ""
            : itemPathToArray[itemPathToArray.length - 1],
        ];
      });
      let csvString = flatdataForCsv.reduce((init, next) => {
        console.log(next);
        return `${init}\n${next}`;
      }, dataRows);
      let anchor = document.createElement("a");
      anchor.href =
        "data:text/csv;charset=utf-8," + encodeURIComponent(csvString);
      anchor.target = "_blank";
      anchor.download = "Data.csv";
      anchor.click();
    },
  },
};
</script>

<style></style>
