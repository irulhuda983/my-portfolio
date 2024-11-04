<script setup>
import { ref } from "vue";

import mqrImage from "@/assets/img/projects/mqr.jpg";
import tspImage from "@/assets/img/projects/tsp.jpg";
import ekavlingImage from "@/assets/img/projects/ekavling.jpg";
import elatnisImage from "@/assets/img/projects/elatnis.jpg";
import melonkuImage from "@/assets/img/projects/melonku.jpg";
import ilmusemeruImage from "@/assets/img/projects/limusemeru.jpg";
import sidewiImage from "@/assets/img/projects/sidewi.jpg";
import silabforImage from "@/assets/img/projects/silabfor.jpg";
import r3storeImage from "@/assets/img/projects/r3store.jpg";
import sidataImage from "@/assets/img/projects/sidata.jpg";

const projects = ref([
  {
    name: "Mahameru Quick Response",
    url: "https://mahamerulantas.id/",
    desc: "Mahameru Quick Response dibuat menggunakan Vue JS dan Laravel, Tujuannya sebagai pusat informasi dari kegiatan yang ada pada DITLANTAS Polda Jatim sekaligus sebagai pemantauan untuk para personil.",
    image: mqrImage,
    tecnology: [""],
  },
  {
    name: "Teguran Presisi",
    url: "https://teguranpresisi.id/",
    desc: "Teguran Presisi dibuat menggunakan Vue Js dan Laravel, merupakan aplikasi yang bertujuan untuk pendataan pelanggaran lalu lintas serta pemberitahuan otomatis melalui broadcast whatsapp.",
    image: tspImage,
    tecnology: [""],
  },
  {
    name: "E-Kavling",
    url: "https://kavlingbumiterate.com/",
    desc: "Aplikasi e-Kavling dibuat menggunakan express dan vue, yang merupakan sebuah platform digital yang dirancang untuk mempermudah proses pembelian, penjualan, dan pengelolaan kavling tanah secara online.",
    image: ekavlingImage,
    tecnology: [""],
  },
  {
    name: "E-Latnis Setukpa",
    url: "https://elatnis.setukpa.id",
    desc: "Aplikasi Pelatihan Teknis Setukpa Lemdiklat.",
    image: elatnisImage,
    tecnology: [""],
  },
  {
    name: "Melonku",
    url: "https://melonku.id/",
    desc: "Melonku dirancang menggunakan Vue JS dan Express yang berfokus pada penjualan produk buah melon segar dan berkualitas langsung dari petani ke konsumen.",
    image: melonkuImage,
    tecnology: [""],
  },
  {
    name: "Ilmu Semeru",
    url: "https://barbuk.ilmusemeru.id",
    desc: "Ilmu Semeru membantu pengguna menemukan knedaraan bermotor yang berada di POLDA JATIM.",
    image: ilmusemeruImage,
    tecnology: [""],
  },
  {
    name: "Sidewi",
    url: "https://sidewi.bojonegorokab.go.id",
    desc: "SIDEWI merupakan platform digital yang bertujuan untuk mempromosikan, mengelola, dan memfasilitasi informasi terkait desa wisata.",
    image: sidewiImage,
    tecnology: [""],
  },
  {
    name: "Silabfor",
    url: "https://silabforpresisi.id",
    desc: "Platform Pendataan barang bukti Labfor.",
    image: silabforImage,
    tecnology: [""],
  },
  {
    name: "R3Store",
    url: "https://r3store.co",
    desc: "R3Store merupakan platform digital yang menyediakan layanan pembelian mata uang dan item dalam berbagai jenis game online secara cepat dan aman.",
    image: r3storeImage,
    tecnology: [""],
  },
  {
    name: "Sidata NU Care",
    url: "https://sidata.internalmanajemen.id",
    desc: "Sidata NU Care pusat informasi terpadu yang dirancang untuk mengumpulkan, mengelola, dan menyajikan data penting.",
    image: sidataImage,
    tecnology: [""],
  },
]);
</script>

<template>
  <div class="w-full grid grid-cols-1 lg:grid-cols-3 gap-x-5 gap-y-10">
    <a target="_blank" :href="project.url" v-for="(project, i) in projects" class="block w-full box-border">
      <div class="w-full box-border mb-5">
        <img :src="project.image" alt="" class="w-full rounded-xl" />
      </div>

      <div class="w-full">
        <h1 class="text-lg lg:text-xl font-bold text-white mb-2">{{ project.name }}</h1>
        <p class="text-xs lg:text-sm text-gray-400">{{ project.desc }}</p>
      </div>
    </a>
  </div>
</template>
