<script lang="ts">
    let imageUrl: string | null = null;
    let imageData: File | null = null;
</script>

<section>
    <h1 class="text-3xl">Welcome to Image to CSV Converter</h1>
    <p>Upload an image here to get CSV data</p>
    <input
        type="file"
        id="imageInput"
        accept="image/*"
    />
    {#if imageUrl}

        <img src={imageUrl} alt="Uploaded Image" id="imageUpload" width="200" />
    {/if}

    <button>click to generate csv data</button>
</section>
