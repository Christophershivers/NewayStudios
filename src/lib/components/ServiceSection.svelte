<script>
    import * as Carousel from "$lib/components/ui/carousel/index";
    import Card from "./card.svelte";
    let carouselItems = [
        {
            id: 0,
            name: "Interviews",
            img: "/interviews.jpg"
        },
        {
            id: 1,
            name: "Color Grading",
            img: "/color grade.jpg"
        },
        {
            id: 2,
            name: "Films",
            img: "/films.jpg"
        },
        {
            id: 3,
            name: "Editing",
            img: "/editing.jpg"
        },
        {
            id: 4,
            name: "Music Videos",
            img: "/music videos.jpg"
        },
        {
            id: 5,
            name: "Real Estate",
            img: "/real estate.jpg"
        },
    ]
</script>

<div class="min-h-[500px] flex justify-center items-center">
    <div class=" h-full grid content-center justify-center items-center">
        <div class="">
            <h1 class="bulma-title flex justify-center text-[#2E333D]">Our Serivces</h1>
            <div class=" max-w-[1000px]">
                <Carousel.Root opts={{align: "start"}}>
                    <Carousel.Content>
                      {#each carouselItems as item (item.id)}
                        <Carousel.Item class="md:basis-1/2 lg:basis-1/3 flex justify-center pb-2"><Card img = {item.img} name= {item.name} /></Carousel.Item>
                      {/each}
                    </Carousel.Content>
                    <Carousel.Previous />
                    <Carousel.Next />
                </Carousel.Root>
            </div>
        </div>
        
    </div>
</div>
