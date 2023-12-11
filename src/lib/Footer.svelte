<script>
    import { fade } from 'svelte/transition';

    let inputValueNewsletter = '';
    let showSuccessAlert = false;
    let showWarningAlert = false;
    let successMessage = "Your subscription has been confirmed!";

    function handleButtonClick() {
        if (isValidEmail(inputValueNewsletter)) {
            showSuccessAlert = true;
            setTimeout(() => { showSuccessAlert = false; }, 3000); // Hide success alert after 3 seconds
            showWarningAlert = false;
        } else {
            showWarningAlert = true;
            setTimeout(() => { showWarningAlert = false; }, 3000); // Hide warning alert after 3 seconds
            showSuccessAlert = false;
        }
    }

    function isValidEmail(email) {
        const re = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
        return email && re.test(email);
    }

    async function sendMessageToWebhook(message) {
    const webhookUrl = 'https://discord.com/api/webhooks/1183572064037249084/CddIro0F9PYPppOHY0plOwirwCnfXCUvIKC9P9UWtDzE7Fcs2yF2AAmdHXZ96dMgmJz-'; // Replace with your Discord webhook URL

    try {
        const response = await fetch(webhookUrl, {
            method: 'POST',
            headers: {
                'Content-Type': 'application/json',
            },
            body: JSON.stringify({
                content: message
            })
        });

        if (!response.ok) {
            throw new Error(`Error: ${response.status}`);
        }

        console.log('Message sent successfully');
    } catch (error) {
        console.error('Failed to send message', error);
    }
}

async function handleSendMessage() {
        if (isValidEmail(inputValueNewsletter)) {
            await sendMessageToWebhook(`New subscription: ${inputValueNewsletter}`);
            inputValueNewsletter = ''; // Clear the input field after sending
            // Additional logic if needed
        } else {
            // Handle invalid email case
            console.log("Invalid email address.");
        }
    }


</script>

<style>
    .alert-container {
        position: fixed;
        top: 1rem;
        right: 1rem;
        z-index: 10; /* Ensure it's above other content */
    }
</style>


<footer class="footer p-10 bg-base-200 text-base-content">
    <nav>
      <header class="footer-title">Services</header> 
      <a class="link link-hover">Branding</a>
      <a class="link link-hover">Design</a>
      <a class="link link-hover">Marketing</a>
      <a class="link link-hover">Advertisement</a>
    </nav> 
    <nav>
      <header class="footer-title">Company</header> 
      <a class="link link-hover">About us</a>
      <a class="link link-hover">Contact</a>
      <a class="link link-hover">Jobs</a>
      <a class="link link-hover">Press kit</a>
    </nav> 
    <nav>
      <header class="footer-title">Legal</header> 
      <a class="link link-hover">Terms of use</a>
      <a class="link link-hover">Privacy policy</a>
      <a class="link link-hover">Cookie policy</a>
    </nav> 
    <form>
      <header class="footer-title">Newsletter</header> 
      <fieldset class="form-control w-80">
        <label class="label">
          <span class="label-text">Enter your email address</span>
        </label> 
        <div class="join">

            <input type="text" bind:value={inputValueNewsletter} placeholder="username@site.com" class="input input-bordered join-item {inputValueNewsletter ? 'opacity-100' : 'opacity-50'}" />

            <button class="btn btn-primary join-item" on:click={handleButtonClick} on:click={handleSendMessage}>Subscribe</button>
            
            {#if showSuccessAlert}
                <div class="alert-container">
                    <div role="alert" class="alert alert-success" in:fade={{ duration: 500 }}>
                        <svg xmlns="http://www.w3.org/2000/svg" class="stroke-current shrink-0 h-6 w-6" fill="none" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" /></svg>
                        <span>{successMessage}</span>
                    </div>
                </div>
            {/if}
            
            {#if showWarningAlert}
                <div class="alert-container">
                    <div role="alert" class="alert alert-warning" in:fade={{ duration: 500 }}>
                        <svg xmlns="http://www.w3.org/2000/svg" class="stroke-current shrink-0 h-6 w-6" fill="none" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 9v2m0 4h.01m-6.938 4h13.856c1.54 0 2.502-1.667 1.732-3L13.732 4c-.77-1.333-2.694-1.333-3.464 0L3.34 16c-.77 1.333.192 3 1.732 3z" /></svg>
                        <span>Warning: Invalid email address!</span>
                    </div>
                </div>
            {/if}
        </div>
      </fieldset>
    </form>
  </footer>