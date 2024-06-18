<script>
  import "../app.css";
  import Footer from "../components/Footer.svelte";
  import Header from "../components/Header.svelte";
  let innerHeight = 0;
  let innerWidth = 0;
  let y = 0;

  function goTop() {
    document.body.scrollIntoView({ behavior: "smooth" });
  }
</script>

<div
  class="relative flex flex-col max-w-[1400px] mx-auto w-full text-sm sm:text-base min-h-screen"
>
  <div
    class={"fixed bottom-5 right-5 duration-200 flex p-2 z-50 " +
      (y > 0
        ? "opacity-100 pointer-events-auto"
        : "opacity-0 pointer-events-none")}
  >
    <button
      on:click={goTop}
      class="ml-auto rounded-full bg-slate-900 text-violet-400 p-3 sm:p-4 hover:bg-slate-800 cursor-pointer"
    >
      <i class="fa-solid fa-arrow-up"></i>
    </button>
  </div>
  <Header {y} />
  <slot />
  <Footer />
</div>

<svelte:window bind:scrollY={y} bind:innerHeight bind:innerWidth />
