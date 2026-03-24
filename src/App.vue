<script setup lang="ts">
const navLinks = [
  { label: 'Contact', href: '#contact' },
]

const contactLinks = [
  { label: 'GitHub', href: 'https://github.com/teuncm' },
  { label: 'LinkedIn', href: 'https://www.linkedin.com/in/teun-mathijssen/' },
  { label: 'SoundCloud', href: 'https://soundcloud.com/tune_m' },
]

const profileImage = 'https://github.com/teuncm.png?size=512'
const currentYear = new Date().getFullYear()
</script>

<template>
  <div class="min-h-screen bg-neutral-50 text-neutral-900 antialiased">
    <div class="mx-auto flex min-h-screen w-[min(1080px,calc(100%-1rem))] flex-col py-2 sm:w-[min(1080px,calc(100%-2rem))] lg:w-[min(1080px,calc(100%-3rem))]">
      <header
        class="sticky top-2 z-20 mb-4 flex flex-wrap items-center justify-between gap-3 rounded-2xl border border-neutral-200 bg-white/90 px-4 py-3 shadow-sm backdrop-blur"
      >
        <a href="#home" class="flex min-w-0 items-center gap-3">
          <img
            :src="profileImage"
            alt="Portrait of Teun Mathijssen"
            class="h-10 w-10 rounded-full border border-neutral-200 object-cover"
          />
          <span class="min-w-0 leading-none">
            <strong class="block truncate text-sm font-semibold">Teun Mathijssen</strong>
            <small class="block text-[0.72rem] text-neutral-500">Personal website</small>
          </span>
        </a>

        <nav aria-label="Primary" class="order-3 flex w-full gap-2 overflow-x-auto pb-0.5 md:order-none md:w-auto">
          <a
            v-for="link in navLinks"
            :key="link.href"
            :href="link.href"
            class="flex-none rounded-full border border-transparent px-3 py-2 text-sm font-medium text-neutral-600 transition hover:border-neutral-300 hover:bg-neutral-100 hover:text-neutral-900 focus:outline-none focus-visible:border-neutral-400 focus-visible:bg-neutral-100"
          >
            {{ link.label }}
          </a>
        </nav>

      </header>

      <main class="flex-1">
        <section id="home" class="scroll-mt-24 pb-4 pt-6 sm:pt-8 lg:pt-10">
          <div class="grid gap-4 lg:grid-cols-[0.95fr_1.05fr] lg:items-center">
            <div class="overflow-hidden rounded-3xl border border-neutral-200 bg-white p-4 shadow-sm sm:p-5 lg:max-w-sm">
              <img
                :src="profileImage"
                alt="Portrait of Teun Mathijssen"
                class="aspect-square w-full rounded-2xl object-cover"
              />
            </div>

            <div class="rounded-3xl border border-neutral-200 bg-white p-6 shadow-sm sm:p-8 lg:p-10">
              <!-- <p class="mb-3 text-xs font-semibold uppercase tracking-[0.16em] text-neutral-500">
                Mobile-first personal site
              </p> -->
              <h1 class="max-w-[12ch] text-4xl font-semibold tracking-[-0.05em] text-neutral-950 sm:text-5xl lg:text-6xl">
                Hi, I&apos;m Teun!
              </h1>
              <p class="mt-4 max-w-2xl text-base leading-7 text-neutral-600 sm:text-lg">
                /tøyn/ (NL) or
                /tjuːn/ (EN)
                <br />
                MSc student at the University of Amsterdam, interested in anything tech, AI, signal processing and music.
              </p>

              <div class="mt-6 flex flex-wrap gap-3">
                <a
                  class="inline-flex min-h-11 items-center justify-center rounded-full bg-neutral-900 px-5 py-3 text-sm font-medium text-white transition hover:bg-neutral-800 focus:outline-none focus-visible:ring-2 focus-visible:ring-neutral-400"
                  href="#contact"
                >
                  Contact
                </a>
              </div>
            </div>
          </div>
        </section>

        <section id="contact" class="scroll-mt-24 pt-12 pb-8">
          <div class="grid gap-4 lg:grid-cols-[0.8fr_1.2fr] lg:items-start">
            <div>
              <p class="text-xs font-semibold uppercase tracking-[0.16em] text-neutral-500">
                Contact
              </p>
              <h2 class="mt-3 text-3xl font-semibold tracking-[-0.04em] text-neutral-950 sm:text-4xl">
                Just say hi.
              </h2>
            </div>

            <div class="rounded-3xl border border-neutral-200 bg-white p-6 text-neutral-600 shadow-sm sm:p-8">
              <p>
                Always open for something interesting.
              </p>

              <div class="mt-5 flex flex-wrap gap-3">
                <a
                  v-for="link in contactLinks"
                  :key="link.label"
                  :href="link.href"
                  class="inline-flex items-center justify-center rounded-full border border-neutral-300 bg-neutral-50 px-4 py-2 text-sm font-medium text-neutral-900 transition hover:bg-neutral-100 focus:outline-none focus-visible:ring-2 focus-visible:ring-neutral-300"
                >
                  {{ link.label }}
                </a>
              </div>
            </div>
          </div>
        </section>
      </main>

      <footer class="py-4 text-center text-sm text-neutral-500">
        <p>© {{ currentYear }} Teun Mathijssen</p>
      </footer>
    </div>
  </div>
</template>
