<script lang="ts">
    import Button from "./ui/button/button.svelte";
    import Input from "./ui/input/input.svelte";
    import Label from "./ui/label/label.svelte";
    import Textarea from "./ui/textarea/textarea.svelte";
</script>

<section class="w-full py-12 md:py-24 lg:py-32 bg-white dark:bg-gray-800">
    <div class="container px-4 md:px-6">
      <div class="flex flex-col items-center justify-center space-y-4 text-center">
        <div class="space-y-2">
          <h2 class="text-3xl font-bold tracking-tighter sm:text-4xl md:text-5xl">Get in Touch</h2>
          <p class="max-w-[700px] text-gray-500 md:text-xl dark:text-gray-400">
            Have a question or want to work together? Fill out the form below and we'll get back to you as soon as
            possible.
          </p>
        </div>
      </div>
      <div class="mx-auto mt-8 max-w-md space-y-4">
        <form class="space-y-4">
          <div class="grid grid-cols-1 gap-4 sm:grid-cols-2">
            <div class="space-y-2">
              <Label >Name</Label>
              <Input id="name" placeholder="Enter your name" />
            </div>
            <div class="space-y-2">
              <Label >Email</Label>
              <Input id="email" placeholder="Enter your email" type="email" />
            </div>
          </div>
          <div class="space-y-2">
            <Label >Message</Label>
            <Textarea class="min-h-[120px]" id="message" placeholder="Enter your message" />
          </div>
          <Button class="w-full" type="submit">
            Submit
          </Button>
        </form>
      </div>
    </div>
  </section>