<script>
    import { createEventDispatcher } from 'svelte';
  
    let name = '';
    let email = '';
    let message = '';
  
    const dispatch = createEventDispatcher();
  
    const handleSubmit = () => {
      const subject = encodeURIComponent('Freelance Contact Inquiry');
      const body = encodeURIComponent(`Name: ${name}\nEmail: ${email}\n\nMessage: ${message}`);
      
      // Create a mailto link
      const mailtoLink = `mailto:support@example.com?subject=${subject}&body=${body}`;
  
      // Open the user's default email client
      window.location.href = mailtoLink;
  
      // Reset form fields
      name = '';
      email = '';
      message = '';
  
      // Dispatch an event to notify the parent component or handle form submission
      dispatch('formSubmitted');
    };
  </script>
  
  <div class="w-fit ssm:w-[95%] p-10 h-fit rounded-lg flex flex-col items-center justify-center bg-neutral-900  mt-20 mb-20 m-auto">
    <h1 class="text-3xl font-semibold pb-4">Contact</h1>
    <form on:submit|preventDefault={handleSubmit}>
      <div class="form-input">
        <label for="name">Name:</label>
        <input type="text" class="input input-bordered w-full max-w-xs" id="name" bind:value={name} />
      </div>
  
      <div class="form-input">
        <label for="email">Email:</label>
        <input type="email" class="input input-bordered w-full max-w-xs" id="email" bind:value={email} />
      </div>
  
      <div class="form-input">
        <label for="message">Message:</label>
        <textarea id="message" class="textarea textarea-bordered w-full" bind:value={message}></textarea>
      </div>
  
      <button type="submit" class="btn btn-primary w-full bg-accent border-black mt-2">Submit</button>
    </form>
  </div>
  