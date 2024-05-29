<script lang="ts">
    import GearCard from "./GearCard.svelte";
    import * as Carousel from "$lib/components/ui/carousel/index";
    import emblaCarouselSvelte from 'embla-carousel-svelte'
    import Autoplay from 'embla-carousel-autoplay'
    let carouselItems = [
        {
            id: 0,
            name: "Canon c70",
            img: "/gear/canon c70.jpg"
        },
        {
            id: 1,
            name: "Rode NTG-2",
            img: "/gear/Rode NTG-2.jpg"
        },
        {
            id: 2,
            name: "tascam portacapture x8",
            img: "/gear/tascam portacapture x8.jpg"
        },
        {
            id: 3,
            name: "Aputure 1200D",
            img: "/gear/Aputure 1200D.jpg"
        },
        {
            id: 4,
            name: "Nanlite forza 500D",
            img: "/gear/Nanlite forza 500D.jpg"
        },
        {
            id: 5,
            name: "Nanlite forza 300D",
            img: "/gear/Nanlite forza 300D.jpg"
        },
        {
            id: 6,
            name: "Aputure 120D",
            img: "/gear/Aputure 120D.jpg"
        },
        {
            id: 7,
            name: "Aputure 300D",
            img: "/gear/Aputure 300D.jpg"
        },
        {
            id: 8,
            name: "Aputure 60D",
            img: "/gear/Aputure 60D.jpg"
        },
        {
            id: 9,
            name: "Aputure B7C",
            img: "/gear/Aputure B7C.jpg"
        },
        {
            id: 10,
            name: "Aputure amaran F22X",
            img: "/gear/Aputure amaran F22X.jpg"
        },
        {
            id: 11,
            name: "Nanlite Pavoslim 120B",
            img: "/gear/Nanlite Pavoslim 120B.jpg"
        },
        {
            id: 12,
            name: "Edlekrone headplus",
            img: "/gear/Edlekrone headplus.jpg"
        },
        {
            id: 13,
            name: "Edlekrone sliderplus",
            img: "/gear/Edlekrone sliderplus.jpg"
        },
        {
            id: 14,
            name: "Edlekrone jibone",
            img: "/gear/Edlekrone jibone.jpg"
        },
    ]

    const plugin = Autoplay({ delay: 1000, stopOnInteraction: true });
</script>

<div class="min-h-[500px] pt-5 grid justify-center items-center">
    <div class="grid justify-center ">
        <div>
            <h1 class="bulma-title flex justify-center">Our Gear</h1>
            <div class=" w-[1000px]">
                <Carousel.Root opts={{align: "start", loop:true}} plugins={[plugin]} on:mouseenter={plugin.stop} on:mouseleave={plugin.reset}>
                    <Carousel.Content>
                        {#each carouselItems as item (item.id)}
                            
                            <Carousel.Item class="md:basis-1/2 lg:basis-1/4 flex justify-center pb-2"><GearCard name={item.name} img={item.img}/></Carousel.Item>
                        {/each}
                    </Carousel.Content>
                    <Carousel.Previous />
                    <Carousel.Next />
                </Carousel.Root>
            </div>
        </div>
       
    </div>
    
    
    
</div>