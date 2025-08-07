### Online CV - Jordan Mosselson

An online portfolio/CV designed to showcase my skills, experience, and projects in a clean, modern, and interactive format. This project is built using a combination of HTML, CSS, and vanilla JavaScript, leveraging the `Animate.css` library for scroll-triggered animations and `EmailJS` for a functional contact form.

#### Features

  * **Responsive Design:** The layout is optimized for both desktop and mobile devices, ensuring a seamless user experience.
  * **Dynamic Content:** A clean and well-structured presentation of my professional information.
  * **Scroll Animations:** Sections animate into view as you scroll down the page, providing a visually engaging experience using `Animate.css` and the `IntersectionObserver` API.
  * **Interactive Contact Form:** A modal contact form powered by `EmailJS` allows visitors to send me a message directly from the website without needing a backend server.
  * **Modular CSS:** The CSS is well-commented and structured with CSS variables for easy theming and maintenance.
  * **Project Showcase:** A dedicated section to highlight key projects with links to their respective GitHub repositories.

#### Technologies Used

  * **HTML5:** The semantic structure of the page.
  * **CSS3:** Styling, layout, and animations.
      * **Custom Properties (CSS Variables):** For a consistent and easily modifiable color scheme.
      * **Flexbox & Grid:** For responsive layouts.
  * **JavaScript:**
      * **`IntersectionObserver`:** To detect when an element enters the viewport, triggering the scroll animations.
      * **`EmailJS`:** A third-party service that handles the form submission and email sending.
  * **External Libraries:**
      * **Animate.css:** For a variety of entrance animations.
      * **Font Awesome:** For the icons used throughout the page.
      * **Google Fonts (Poppins):** For a modern and clean typeface.

#### Setup and Installation

To use this template for your own CV, you'll need to configure the `EmailJS` service for the contact form.

1.  **Sign up for EmailJS:**

      * Go to [EmailJS](https://www.emailjs.com/) and create a free account.

2.  **Add a new Email Service:**

      * Navigate to "Email Services" and add the email provider you want to use (e.g., Gmail, Outlook, etc.). Follow the instructions to connect your account.

3.  **Create an Email Template:**

      * Go to "Email Templates" and create a new template. You can use the provided template in the image as a guide. The template fields should correspond to the `name` attributes in the HTML form: `{{name}}`, `{{email}}`, `{{message}}`.

4.  **Copy Your Keys:**

      * Go to your "Account" page to find your **Public Key**.
      * Go to your "Email Services" and click on the service you created to find the **Service ID**.
      * Go to your "Email Templates" and click on the template you created to find the **Template ID**.

5.  **Update the JavaScript:**

      * Open the `index.html` file (or the file where your JavaScript is located).
      * In the `<script>` tag at the bottom, replace the placeholder values with your actual keys:

    <!-- end list -->

    ```javascript
    emailjs.init({
        publicKey: 'YOUR_EMAILJS_PUBLIC_KEY' // Replace with your Public Key
    });

    // ... inside the form event listener ...

    emailjs.sendForm('YOUR_EMAILJS_SERVICE_ID', 'YOUR_EMAILJS_TEMPLATE_ID', contactForm) // Replace with your Service ID and Template ID
    // ...
    ```

6.  **Customize the Content:**

      * Edit the HTML file to replace my information with your own details, including personal information, work experience, education, skills, and projects.

7.  **Host Your CV:**

      * You can host this static website on platforms like GitHub Pages, Netlify, or Vercel for free.

#### File Structure

```
.
├── index.html       # The main CV page
└── README.md        # This file
```
