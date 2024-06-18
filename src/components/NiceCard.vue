<script lang="ts" setup></script>

<template>
  <div class="py-24 md:pt-36 bg-[#f9f9f9]">
    <div class="content-visibility-auto mx-auto max-w-6xl px-4 md:px-0">
      <h2
        class="mx-auto mb-6 px-4 text-center text-3xl font-bold c-slate-7 md:mb-12 md:text-5xl md:leading-[1.15]"
      >
        People's choice and Critics' choice
      </h2>

      <div
        class="mx-auto max-w-6xl p-6 pb-10 md:grid md:grid-cols-5 md:gap-0 lg:grid-cols-3"
      >
        <div class="col-span-3 md:px-0 lg:col-span-2">
          <div
            class="md:text-md mb-12 block rounded-xl text-lg md:mb-0 md:mr-6 md:b md:b-gray-2 md:bg-white md:p-12 md:shadow-xl lg:text-xl"
          >
            <p class="font-serif">
              “If you’re looking to restore (or introduce) a little order to
              your life, Craft will fall somewhere between
              <span class="highlight highlight--yellow"
                >‘immediately helpful’</span
              >
              and ‘enough to bring a tear to your eye.’ This productivity app is
              so<!-- -->
              <span class="highlight highlight--yellow"
                >versatile that it’s hard to define:</span
              >
              It’s for taking notes, writing to-do lists, organizing important
              documents, organizing unimportant documents, stashing away random
              scraps and, ultimately,<!-- -->
              <span class="highlight highlight--yellow"
                >transforming your digital detritus into a blissfully organized
                system</span
              >
              <!-- -->that’s easy to navigate and pleasing to look at.”
            </p>
            <div class="my-8 flex w-full justify-center md:mb-0">
              <img
                alt="Editor's Choice award"
                loading="lazy"
                width="364"
                height="88"
                decoding="async"
                data-nimg="1"
                class="w-48"
                style="color: transparent"
                srcset="
                  https://www.craft.do/_next/image?url=%2F_next%2Fstatic%2Fmedia%2Feditors-choice.69088fe2.png&amp;w=384&amp;q=100 1x,
                  https://www.craft.do/_next/image?url=%2F_next%2Fstatic%2Fmedia%2Feditors-choice.69088fe2.png&amp;w=750&amp;q=100 2x
                "
                src="https://www.craft.do/_next/image?url=%2F_next%2Fstatic%2Fmedia%2Feditors-choice.69088fe2.png&amp;w=750&amp;q=100"
              />
            </div>
          </div>
        </div>

        <div class="mt-6 md:col-span-2 md:mt-0 lg:col-span-1 lg:mt-0">
          <section class="mx-auto max-w-2xl md:h-full">
            <div
              class="flex flex-col justify-between gap-2 sm:flex-row md:h-full md:flex-col md:gap-4"
            >
              <div
                class="relative flex flex-grow flex-row items-center overflow-hidden rounded-xl bg-gradient-to-br from-[#257BDC] to-[#1A53B4] py-3 shadow-xl sm:py-0"
              >
                <img
                  alt="Apple AppStore logo"
                  loading="lazy"
                  width="300"
                  height="300"
                  decoding="async"
                  data-nimg="1"
                  class="z-10 ml-2 h-24 w-24"
                  style="color: transparent"
                  sizes="96px"
                  src="https://www.craft.do/_next/image?url=%2F_next%2Fstatic%2Fmedia%2Fapp-award.2db99a91.png&amp;w=3840&amp;q=75"
                />
                <div
                  class="flex cursor-default select-none flex-col justify-center pl-2 pr-4"
                >
                  <span class="text-lg font-bold text-white lg:text-xl"
                    >App Store Best of</span
                  ><span class="block text-sm text-white/75"
                    >Mac App of the Year</span
                  >
                </div>
              </div>
              <div
                class="relative flex flex-grow flex-row items-center overflow-hidden rounded-xl bg-gradient-to-br from-[#2D303A] to-[#010101] py-3 shadow-xl sm:py-0"
              >
                <img
                  alt="Apple Design Award logo"
                  loading="lazy"
                  width="300"
                  height="300"
                  decoding="async"
                  data-nimg="1"
                  class="z-10 ml-2 h-24 w-24"
                  style="color: transparent"
                  sizes="96px"
                  src="https://www.craft.do/_next/image?url=%2F_next%2Fstatic%2Fmedia%2Fdesign-award.58d0ac0d.png&amp;w=3840&amp;q=75"
                />
                <div
                  class="flex cursor-default select-none flex-col justify-center pl-2 pr-4"
                >
                  <span class="text-lg font-bold text-white lg:text-xl"
                    >Apple Design Awards</span
                  ><span class="block text-sm text-white/75">Finalist</span>
                </div>
              </div>
              <div
                class="relative flex flex-grow flex-row items-center overflow-hidden rounded-xl bg-gradient-to-br from-[#67BAE9] to-[#1347AD] py-3 shadow-xl sm:py-0"
              >
                <img
                  alt="The Webby Award 2024 logo"
                  loading="lazy"
                  width="146"
                  height="148"
                  decoding="async"
                  data-nimg="1"
                  class="z-10 ml-2 h-24 w-24 p-3"
                  style="color: transparent"
                  sizes="96px"
                  src="https://www.craft.do/_next/image?url=%2F_next%2Fstatic%2Fmedia%2Fwebby-award.31346cc5.png&amp;w=3840&amp;q=75"
                />
                <div
                  class="flex cursor-default select-none flex-col justify-center pl-2 pr-4"
                >
                  <span class="text-lg font-bold text-white lg:text-xl"
                    >The Webby Awards</span
                  ><span class="block text-sm text-white/75"
                    >People’s Voice Winner 2024</span
                  >
                </div>
              </div>
            </div>
          </section>
        </div>
      </div>
    </div>

    <div class="mx-auto mt-4 max-w-6xl">
      <div class="flex select-none flex-col items-center justify-center">
        <a
          id="click_btn_download_cta"
          class="rounded-full whitespace-nowrap select-none inline-flex items-center justify-center bg-blue-6 text-white shadow-sm transition-all duration-1000 relative overflow-hidden bg-blue-light hover:bg-[#4d82ec] w-fit px-8 py-3 text-lg font-bold hover:shadow-xl focus:outline-none"
          aria-label="Visit the download page"
          data-testid="click_btn_cta_app-store-award"
          href="/download"
          ><span>Get Started for Free</span></a
        >
      </div>
    </div>
  </div>
</template>
