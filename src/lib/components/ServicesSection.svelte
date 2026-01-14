<script lang="ts">
    import ServiceCard from "./ServiceCard.svelte";

    const services = [
        {
            icon: "extension",
            title: "Sparepart",
            description:
                "Sedia lengkap sparepart original & universal: Throttle, Controller, Charger, dll.",
            tag: "Hot",
        },
        {
            icon: "battery_charging_full",
            title: "Perbaikan Baterai",
            description:
                "Diagnosa kesehatan baterai, dan penggantian baterai baru",
        },
        {
            icon: "cyclone",
            title: "Servis Dinamo",
            description:
                "Pembersihan kumparan, penggantian bearing/hall sensor, dan perbaikan suara kasar pada motor.",
        },
        {
            icon: "memory",
            title: "Perbaikan Controller",
            description:
                "Servis modul controller mati total, error code, mosfet terbakar, dan instalasi controller universal.",
        },
        {
            icon: "electrical_services",
            title: "Kelistrikan & Kabel",
            description:
                "Urut kabel body, perbaikan soket kendor, lampu mati, klakson, dan indikator speedometer.",
        },
        {
            icon: "tire_repair",
            title: "Ganti Ban",
            description:
                "Sedia ban tubeless dan ban dalam berbagai ukuran ring (14, 16, 10 inch) khusus sepeda listrik.",
        },
    ];
</script>

<section id="services" class="py-16 bg-white dark:bg-[#0f2023] relative">
    <div class="max-w-[1440px] mx-auto px-4 sm:px-6 lg:px-20">
        <div class="flex flex-col lg:flex-row items-start gap-12 lg:gap-20">
            <!-- Left Column: Header & Featured Image -->
            <div class="w-full lg:w-[40%] flex flex-col gap-8 sticky top-24">
                <div class="flex flex-col gap-4">
                    <h2
                        class="text-primary font-bold text-lg uppercase tracking-wider"
                    >
                        Layanan Kami
                    </h2>
                    <h3
                        class="text-3xl md:text-4xl font-extrabold text-[#101718] dark:text-white leading-tight"
                    >
                        Servis Profesional & Terpercaya
                    </h3>
                    <p
                        class="text-slate-600 dark:text-slate-400 text-lg leading-relaxed"
                    >
                        Daftar layanan lengkap untuk segala jenis kerusakan
                        sepeda listrik Anda. Transparan, cepat, dan bergaransi.
                    </p>

                    <a
                        class="inline-flex items-center text-primary font-bold hover:text-accent transition-colors gap-2 group w-fit mt-2"
                        href="#contact"
                    >
                        Lihat Selengkapnya
                        <span
                            class="material-symbols-outlined transition-transform group-hover:translate-x-1"
                            >arrow_forward</span
                        >
                    </a>
                </div>

                <!-- Featured Image (Hero Style) -->
                <div class="w-full relative">
                    <!-- Abstract background blob -->
                    <div
                        class="absolute -z-10 top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 w-[120%] h-[120%] bg-gradient-to-tr from-[#00b4d8]/20 to-[#ef233c]/10 rounded-full blur-3xl opacity-60"
                    ></div>
                    <div
                        class="relative overflow-hidden rounded-2xl shadow-xl bg-white dark:bg-gray-800 aspect-[4/5] group"
                    >
                        <!-- Image Overlay Gradient -->
                        <div
                            class="absolute inset-0 bg-gradient-to-t from-black/20 to-transparent z-10"
                        ></div>
                        <div
                            class="w-full h-full bg-cover bg-center transition-transform duration-700 group-hover:scale-105"
                            aria-label="Teknisi sepeda listrik sedang bekerja"
                            style="background-image: url('/services-featured.webp');"
                        ></div>
                    </div>
                </div>
            </div>

            <!-- Right Column: Service Grid -->
            <div class="w-full lg:w-[60%]">
                <div class="grid grid-cols-1 sm:grid-cols-2 gap-6">
                    {#each services as service}
                        <ServiceCard
                            icon={service.icon}
                            title={service.title}
                            description={service.description}
                            tag={service.tag}
                        />
                    {/each}
                </div>

                <div class="mt-8 flex justify-center md:hidden">
                    <button
                        class="w-full h-12 rounded-lg border border-primary text-primary font-bold hover:bg-primary hover:text-white transition-colors"
                    >
                        Lihat Semua Layanan
                    </button>
                </div>
            </div>
        </div>
    </div>
</section>
