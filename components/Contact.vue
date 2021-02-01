<template>
    <div>
        <section class="container text-gray-600 body-font relative">
        <div class=" px-5 py-24 mx-auto flex sm:flex-nowrap flex-wrap">
            <div class="md:w-1/2 bg-gray-300 rounded-lg overflow-hidden p-10 flex items-end justify-start relative">
            <iframe width="100%" height="100%" class="absolute inset-0" frameborder="0" title="map" marginheight="0" marginwidth="0" scrolling="no" src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2456.0287477097636!2d-0.3314219842116116!3d52.0063540797202!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x487634db9c461a9b%3A0x54d854b8a194f30a!2sC%20D%20M%20Electrical%20Ltd!5e0!3m2!1sen!2suk!4v1612175407942!5m2!1sen!2suk" style="filter: grayscale(1) contrast(1.2) opacity(0.4);"></iframe>
            <div class="bg-white relative flex flex-wrap py-6 rounded shadow-md">
                <div class="lg:w-1/2 px-6">
                <h2 class="title-font font-semibold text-gray-900 tracking-widest text-xs">ADDRESS</h2>
                <p class="mt-1">The Art Of Ltd, Rectory Farm Business Park, C/O CDM Electrical Ltd, Meppershall Road, Upper Stondon, SG16 6LJ</p>
                </div>
                <div class="lg:w-1/2 px-6 mt-4 lg:mt-0 mx-auto">
                <h2 class="title-font font-semibold text-gray-900 tracking-widest text-xs">EMAIL</h2>
                <a href="mailto:info@theartof.uk" class="text-indigo-500 leading-relaxed">info@theartof.uk</a>
                <h2 class="title-font font-semibold text-gray-900 tracking-widest text-xs mt-4">PHONE</h2>
                <p class="leading-relaxed">m: <a href="tel:0786 0460 688" class="text-indigo-500 leading-relaxed">0786 0460 688</a></p>
                <p class="leading-relaxed">t: <a href="tel:0845 1701 231" class="text-indigo-500 leading-relaxed">0845 1701 231</a></p>
                </div>
            </div>
            </div>
            <div class="md:w-1/2 bg-white flex flex-col w-full md:px-8 md:py-8 mt-8 md:mt-0">
            <h2 class="text-gray-900 text-lg mb-1 font-medium title-font">Contact Us</h2>
            <p class="leading-relaxed mb-5 text-gray-600">Get in touch to find out more about how we can help</p>
            <form name="contact" method="POST" data-netlify="true" data-netlify-recaptcha="true">
                <input type="hidden" name="form-name" value="contact" />
                <div class="relative mb-4">
                <label for="name" class="leading-7 text-sm text-gray-600">Name</label>
                <input type="text" id="name" name="name" class="w-full bg-white rounded border border-gray-300 focus:border-indigo-500 focus:ring-2 focus:ring-indigo-200 text-base outline-none text-gray-700 py-1 px-3 leading-8 transition-colors duration-200 ease-in-out">
                </div>
                <div class="relative mb-4">
                    <label for="email" class="leading-7 text-sm text-gray-600">Email</label>
                    <input type="email" id="email" name="email" class="w-full bg-white rounded border border-gray-300 focus:border-indigo-500 focus:ring-2 focus:ring-indigo-200 text-base outline-none text-gray-700 py-1 px-3 leading-8 transition-colors duration-200 ease-in-out">
                </div>
                <div class="relative mb-4">
                    <label for="message" class="leading-7 text-sm text-gray-600">Message</label>
                    <textarea id="message" name="message" class="w-full bg-white rounded border border-gray-300 focus:border-indigo-500 focus:ring-2 focus:ring-indigo-200 h-32 text-base outline-none text-gray-700 py-1 px-3 resize-none leading-6 transition-colors duration-200 ease-in-out"></textarea>
                </div>
                <button class="text-white bg-indigo-500 border-0 py-2 px-6 focus:outline-none hover:bg-indigo-600 rounded text-lg">Submit</button>
                <p class="text-xs text-gray-500 mt-3">Click on the button to submit your message and we will get back to you shortly</p>
            </form>
            </div>
        </div>
        </section>
    </div>
</template>
