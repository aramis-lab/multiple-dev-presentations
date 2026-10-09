<template>
	<footer class="absolute bottom-0 left-0 right-0 flex text-center text-white">
		<div class="flex-1 p-1" style="background:#191959">
			{{ $slidev.configs.author || "Unknown author" }}
		</div>
		<div class="flex-1 p-1" style="background:#262686">
			{{ $slidev.configs.title || "Unknown title" }}
		</div>
		<div class="flex-1 p-1" style="background:#3333B3">
			<div class="float-right">
				{{ $slidev.nav.currentPage }} /
				<SlidesTotal />
			</div>
            <span class="links">
              <a
                href="https://www.aramislab.fr/"
                target="_blank"
                rel="noopener"
                title="ARAMIS Lab"
                aria-label="ARAMIS Lab"
              >
                <img src="../images/full-logo-aramis.png" alt="ARAMIS Lab Logo" />
              </a>

              <a
                href="https://github.com/aramis-lab/multiple-dev-presentations"
                target="_blank"
                rel="noopener"
                title="Slides repository"
                aria-label="Slides repository"
              >
                <carbon:logo-github />
              </a>

              <a
                href="../index.html"
                target="_self"
                rel="noopener"
                title="Home page"
                aria-label="Home page"
              >
                <carbon:home />
              </a>
            </span>
		</div>
	</footer>
</template>

<script setup lang="ts">
import SlidesTotal from "@slidev/client/builtin/SlidesTotal.vue";
</script>

<style scoped>
.links {
  display: inline-flex;
  align-items: center;
  gap: 1rem;            /* space between the two icons */
  margin-left: auto;
}
.links a {
  display: inline-flex;
  color: inherit;
  border: none;
  text-decoration: none;
  font-size: 1.1em;     /* icon size */
  opacity: 0.8;
}
.links a:hover { opacity: 1; }
.links img {
  width: 4em;
  height: auto;
}
</style>