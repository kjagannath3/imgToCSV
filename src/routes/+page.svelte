<script lang="ts">
    let imageUrl: string | null = null;
    let imageData: File | null = null;
    /*function handleImageInput(event:Event) {
        const input = event.target as HTMLInputElement
        if (input.files && input.files.length > 0) {
            const file = input.files[0]


            if (file.type.startsWith('image')) {
                console.log("Image selected", file)
                const imagePreview = document.getElementById("imageUpload") as HTMLImageElement
                imagePreview.src = URL.createObjectURL(file)

            } else{
                console.error("selected file is not an image");

            }

        }
    }*/
    function handleImageInput(event: Event) {
        let selectedFile: File | null = null;
        const input = event.target as HTMLInputElement;
        if (input?.files && input.files.length > 0) {
            selectedFile = input.files[0];
            console.log(selectedFile);
        }
    }
</script>

<section>
    <h1 class="text-3xl">Welcome to Image to CSV Converter</h1>
    <p>Upload an image here to get CSV data</p>
    <input
        type="file"
        id="imageInput"
        accept="image/*"
        on:change={handleImageInput}
    />

    <button>click to generate csv data</button>
</section>
