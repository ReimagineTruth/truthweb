---
icon: globe-pointer
---

# Publishing Your Docs

#### **1. Choose a Documentation Platform**

There are several platforms where you can host and publish your documentation. Popular options include:

* **GitBook** : Ideal for creating and hosting professional documentation.
* **Read the Docs** : Great for open-source projects.
* **GitHub Pages** : Free hosting for static websites.
* **Netlify/Vercel** : For deploying static sites with custom domains.

For this example, we'll focus on **GitBook** and **GitHub Pages** , as they are beginner-friendly and widely used.

***

#### **2. Using GitBook**

**Step 1: Create a GitBook Account**

* Go to [GitBook ](https://www.gitbook.com/)and sign up for an account.
* Choose a free or paid plan based on your needs.

**Step 2: Import Your Documentation**

* Create a new project in GitBook.
* Import your Markdown files or copy-paste the content into GitBook's editor.
* Organize your content into sections (e.g., Introduction, Features, API, FAQs).

**Step 3: Customize the Design**

* Use GitBook's built-in themes or customize the appearance (fonts, colors, etc.).
* Add your logo and branding to make it consistent with TruthWeb.

**Step 4: Publish**

* Once your content is ready, click the **Publish** button.
* GitBook will generate a public URL for your documentation (e.g., ..

```
https://yourproject.gitbook.io)
```

**Step 5: Share the Link**

* Share the published URL with your users, developers, and community.
* Embed the link in your app, website, or marketing materials.

***

#### **3. Using GitHub Pages**

**Step 1: Prepare Your Documentation**

* Write your documentation in Markdown format (`.md` files).
* Organize the files into folders for better structure:\


```html
/docs
  ├── index.md        (Home page)
  ├── features.md     (Features section)
  ├── api.md          (API documentation)
  └── faq.md          (FAQs)
```

**Step 2: Create a GitHub Repository**

* Go to [GitHub ](https://github.com/)and create a new repository (e.g., `truthweb-docs`).
* Push your documentation files to the repository.

**Step 3: Enable GitHub Pages**

* Go to your repository's **Settings** > **Pages** .
* Select the branch (`main` or `gh-pages`) and folder (`/docs`) where your files are stored.
* Save the settings, and GitHub will generate a URL (e.g., `https://username.github.io/truthweb-docs`).

**Step 4: Customize the Site**

* Use a static site generator like **Jekyll** or **Docusaurus** to enhance the design.
* Add a `README.md` file for the homepage and include navigation links.

**Step 5: Publish**

* Once GitHub Pages is enabled, your documentation will be live at the generated URL.
* Share the link with your audience.

***

#### **4. Using Netlify or Vercel**

**Step 1: Prepare Your Static Site**

* Use a static site generator like **Docusaurus** , **Hugo** , or **Jekyll** to build your documentation.
* Export the site as static HTML, CSS, and JavaScript files.

**Step 2: Deploy to Netlify/Vercel**

* Sign up for [Netlify ](https://www.netlify.com/)or [Vercel ](https://vercel.com/).
* Connect your GitHub repository containing the static site files.
* Configure the build settings (e.g., build command, output directory).

**Step 3: Set Up a Custom Domain (Optional)**

* If you own a domain (e.g., `docs.truthweb.com`), configure it in Netlify/Vercel.
* Update DNS records to point to the platform's servers.

**Step 4: Publish**

* Once deployed, your documentation will be live at the provided URL or custom domain.

***

#### **5. Promote Your Documentation**

After publishing, ensure your documentation reaches the right audience:

* **Embed Links** : Add links to your documentation in the TruthWeb app, website footer, and email signatures.
* **Social Media** : Share the docs on platforms like Twitter, LinkedIn, and Facebook.
* **Community Forums** : Post updates in Pi Network forums and developer communities.
* **Email Campaigns** : Notify users about the new documentation via newsletters.

***

#### **6. Maintain and Update**

* Regularly update the documentation to reflect new features, bug fixes, and user feedback.
* Encourage contributions from the community by enabling pull requests (if hosted on GitHub).

***

By following these steps, you can successfully publish and share your **TruthWeb documentation** with the world. If you need help with a specific platform or step, feel free to ask!
