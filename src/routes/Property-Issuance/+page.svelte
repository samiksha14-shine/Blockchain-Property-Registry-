<script>
  let propertyId = '';
  let issuanceDetails = '';

  const handleSubmit = (event) => {
    event.preventDefault();
    // Handle form submission logic here
    console.log({ propertyId, issuanceDetails });
  };
</script>

<style>
  :global(body) {
    background: linear-gradient(to right, #1a202c, #2d3748, #1a202c); /* Gradient background matching other pages */
    color: #e2e8f0; /* Light text color */
  }
  .form-container {
    background: #2d3748; /* Slightly lighter dark background */
    border: 1px solid #4a5568; /* Border color */
  }
  .button {
    background: linear-gradient(to right, #f56565, #4299e1); /* Gradient matching website theme */
  }
</style>

<section class="bg-gradient-to-r from-black via-gray-800 to-black min-h-screen">
  <div class="flex flex-col items-center justify-center py-10 mx-auto md:h-screen lg:py-10">
    <div class="w-full max-w-md bg-gray-800 rounded-lg shadow-lg">
      <div class="p-6 space-y-6">
        <h1 class="text-2xl font-bold text-center text-gray-100 mb-4">Property Issuance</h1>
        <form on:submit={handleSubmit} class="form-container shadow-md rounded px-8 pt-6 pb-8 mb-4">
          <div class="mb-4">
            <label for="property-id" class="block text-gray-300 text-sm font-bold mb-2">Property ID:</label>
            <input
              type="text"
              id="property-id"
              bind:value={propertyId}
              required
              class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-100 leading-tight focus:outline-none focus:shadow-outline"
              placeholder="Enter Property ID"
            />
          </div>

          <div class="mb-4">
            <label for="issuance-details" class="block text-gray-300 text-sm font-bold mb-2">Issuance Details:</label>
            <textarea
              id="issuance-details"
              bind:value={issuanceDetails}
              required
              class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-100 leading-tight focus:outline-none focus:shadow-outline"
              placeholder="Enter Issuance Details"
            ></textarea>
          </div>

          <div class="flex items-center justify-between">
            <button
              type="submit"
              class="button hover:bg-opacity-80 text-white font-bold py-2 px-4 rounded focus:outline-none focus:shadow-outline"
            >
              Submit
            </button>
          </div>
        </form>
      </div>
    </div>
  </div>
</section>
