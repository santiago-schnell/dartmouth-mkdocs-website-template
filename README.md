# Dartmouth MkDocs Website Template

This repository provides a customizable website template built with [Materials for MkDocs](https://squidfunk.github.io/mkdocs-material/), designed specifically for Dartmouth College faculty, researchers, and students. It incorporates Dartmouth branding colors, typography, and common academic website layouts, allowing you to easily create a professional and cohesive online presence.

## Features

* **Dartmouth Branding**: Pre-configured with official Dartmouth Green, specific brand fonts (`National 2`, `Dartmouth Ruzika`), and consistent color palettes for light and dark modes.
* **Responsive Design**: Optimized for display on desktops, tablets, and mobile devices.
* **Custom Layouts**: Includes special CSS classes for:
    * **Hero Introduction Block**: A prominent section with an image and descriptive text for your home page.
    * **Content Cards**: Flexible card layouts for showcasing publications, personal projects, news, or team members.
    * **Cover Gallery**: A grid display for journal or book covers (optional, primarily for researchers).
    * **Research Project Sections**: Layouts for detailing individual research projects with floated images and summary boxes (optional, primarily for researchers).
    * **Custom Footer**: A Dartmouth-branded footer with social links and customizable text.
* **Light & Dark Mode**: Seamless theme switching with Dartmouth-specific color adjustments for both modes.
* **Markdown-centric**: Build your content using simple, powerful Markdown, enhanced by various MkDocs-Material extensions.
* **MathJax Support**: Ready for rendering LaTeX equations in your content.
* **Scroll-to-Top Button**: A convenient button appears on scroll to quickly return to the top of the page.

## Getting Started

Follow these steps to set up and deploy your Dartmouth website.

### 1. Prerequisites

Before you begin, ensure you have Python and `pip` (Python's package installer) installed on your system.

### 2. Installation

1.  **Clone this Repository (or download the template files):**
    ```bash
    git clone [https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template) your-website-name
    cd your-website-name
    ```

2.  **Install MkDocs and Materials for MkDocs:**
    ```bash
    pip install mkdocs mkdocs-material pymdown-extensions
    ```
    `pymdown-extensions` is crucial for many of the advanced Markdown features used in this template (e.g., admonitions, superfences, arithmatex).

3.  **Place Custom Fonts:**
    This template relies on custom Dartmouth fonts (`National 2` and `Dartmouth Ruzika`). You need to obtain these font files (`.otf` and `.ttf` formats) and place them in the correct location.
    Create the following directory structure inside your `docs` folder:
    ```
    your-website-name/
    └── docs/
        └── assets/
            └── fonts/
                ├── national2/
                │   ├── National2-Light.otf
                │   ├── National2-Regular.otf
                │   ├── National2-Medium.otf
                │   ├── National2-Bold.otf
                │   └── National2-Extrabold.otf
                └── dartmouth-ruzicka/
                    ├── DartmouthRuzicka-Regular.ttf
                    ├── DartmouthRuzicka-Italic.ttf
                    ├── DartmouthRuzicka-Bold.ttf
                    └── DartmouthRuzicka-BoldItalic.ttf
    ```
    The fonts are available: [dartmouth-ruzicka](https://drive.google.com/file/d/1OfXeDbLlSvYA2z9JEgKZTJC4qw4iwnDh/view?usp=sharing) and [national2](https://drive.google.com/file/d/1avYJ2OfrkdpbkYQkgePQgqQJ1gMkUh9i/view?usp=sharing). *Make sure the font filenames exactly match those specified in `extra.css`.*

### 3. Project Structure

Your project directory should look similar to this:

```
your-website-name/ # This is your project's root directory  
├── mkdocs.yml     # The configuration file you just provided  
├── README.md      # The comprehensive README for the template  
└── docs/          # This directory holds all your Markdown content and assets  
[cite_start]├── index.md               # Corresponds to 'Home'    
[cite_start]├── about.md               # Corresponds to 'About'  
[cite_start]├── research.md            # Corresponds to 'Research'  
[cite_start]├── publications/          # Directory for the 'Publications'  
[cite_start]│   ├── index.md           # Corresponds to 'Publications: Overview'  
[cite_start]│   ├── selected.md        # Corresponds to 'Publications: Selected Works'  
[cite_start]│   ├── preprints.md       # Corresponds to 'Publications: Preprints'  
[cite_start]│   └── covers.md          # Corresponds to 'Publications: Covers'  
[cite_start]├── teaching.md            # Corresponds to 'Teaching' (Optional)  
[cite_start]├── resources.md           # Corresponds to 'Resources' (Optional)  
[cite_start]├── contact.md             # Corresponds to 'Contact' (Optional)  
├── assets/                # Directory for static assets like images and fonts  
│   ├── images/  
[cite_start]│   │   ├── dartmouth-logo.png # Referenced in mkdocs.yml  
[cite_start]│   │   ├── favicon.ico        # Referenced in mkdocs.yml  
│   │   └── # ... add your profile picture, project images, etc. here (e.g., your_profile_picture.jpg, placeholder_research.jpg)  
│   └── fonts/             # Directory for custom font files  
│       ├── national2/     # Contains National 2 font files (.otf)  
│       │   ├── National2-Light.otf  
│       │   ├── National2-Regular.otf  
│       │   ├── National2-Medium.otf  
│       │   ├── National2-Bold.otf  
│       │   └── National2-Extrabold.otf  
│       └── dartmouth-ruzicka/ # Contains Dartmouth Ruzika font files (.ttf)  
│           ├── DartmouthRuzicka-Regular.ttf  
│           ├── DartmouthRuzicka-Italic.ttf  
│           ├── DartmouthRuzicka-Bold.ttf  
│           └── DartmouthRuzicka-BoldItalic.ttf  
├── stylesheets/           # Directory for custom CSS files  
[cite_start]│   └── extra.css          # Your custom CSS, referenced in mkdocs.yml  
└── javascripts/           # Directory for custom JavaScript files  
[cite_start]└── extra.js           # Your custom JS (e.g., scroll-to-top), referenced in mkdocs.yml  
└── overrides/             # Optional: For theme template overrides (e.g., main.html for custom footer HTML)  
│   ├── partials/  
└── footer.html          # Example override file
```

### 4. Customization

1.  **Edit `mkdocs.yml`**:
    * Update `site_name`, `site_url`, `site_author`, `site_description` with your specific details.
    * Customize the `nav` section to define your website's navigation structure. Remove or add pages as needed (e.g., if you're a student, you might remove 'Research' or 'Teaching' if not applicable).
    * Update the `social` links in the `extra` section with your profiles (e.g., Google Scholar, GitHub, LinkedIn).
    * Ensure `logo` and `favicon` paths are correct if you change them.

2.  **Edit `extra.css`**:
    This file contains all the Dartmouth-specific styling. It is extensively commented for easy understanding. You generally won't need to modify this unless you want to tweak Dartmouth's specific color shades or minor layout adjustments. The CSS variables at the top make color changes very easy.

3.  **Edit `extra.js`**:
    This file is currently set up to handle the scroll-to-top button. If you have other custom JavaScript needs, add them here.

4.  **Create your Content (`.md` files)**:
    Start writing your content in Markdown files within the `docs/` directory. Refer to the provided template `.md` files (such as `index.md`, `about.md`, `research.md`, etc.) for examples of how to use the custom features.

### 5. Running Your Website

#### Local Development (Preview)

```bash
mkdocs serve
```

Open your web browser and go to http://127.0.0.1:8000 (or the address shown in your terminal). The page will automatically reload when you save changes to your Markdown or configuration files.

#### Building for Deployment

When you're ready to deploy your website, build the static files:

```bash
mkdocs build
```

This command generates a ```site/``` directory containing all your HTML, CSS, JavaScript, and asset files. This ```site/``` directory is what you will upload to your web server (e.g., Dartmouth's AFS space for web hosting).

## Using Custom Features in Your Markdown

This template includes custom CSS classes and specific Markdown patterns to implement enhanced layouts and styles.

### 1. Hero Introduction Block

Use an admonition with the ```hero-intro``` class for a prominent, visually engaging section on your home page:

```bash
!!! hero-intro
    <div class="hero-text">
        # Welcome to My Academic Website!
        <p>I am a **[Your Title/Role, e.g., Assistant Professor, PhD Candidate, Undergraduate Researcher]** at Dartmouth College, passionate about **[Your Field of Study/Research Area]**.</p>
        <p>This website serves as a comprehensive resource showcasing my academic journey, research endeavors, publications, and projects.</p>
        <p>Feel free to explore the different sections to learn more about my work and interests.</p>
    </div>
    <div class="hero-image">
        <img src="assets/images/your_profile_picture.jpg" alt="[Your Name] Profile Picture">
    </div>
```

- The ```hero-text``` div should contain your main introduction and description.
- The ```hero-image``` div should contain your profile image or a relevant banner image. Update the ```src``` to your image path (e.g., ```assets/images/your_profile_picture.jpg```).

### 2. Content Cards

Use the ```card-grid``` wrapper and ```card``` structure for flexible content display (e.g., highlighting publications, personal projects, news, or team members).

```bash
<div class="card-grid">
    <div class="card">
        <img src="assets/images/placeholder_research.jpg" class="card-img" alt="Research Overview">
        <div class="card-body">
            <span class="card-label">My Work</span>
            <h3 class="card-title"><a href="research.md">My Current Research</a></h3>
            <p>Explore my contributions to [mention a specific area], from theoretical models to practical applications. (Adjust or remove if 'Research' page is not used).</p>
        </div>
    </div>
    <div class="card">
        <img src="assets/images/placeholder_publication.jpg" class="card-img" alt="Publication Thumbnail">
        <div class="card-body">
            <span class="card-label">Scholarship</span>
            <h3 class="card-title"><a href="publications/">Latest Publications</a></h3>
            <p>Access a comprehensive list of my peer-reviewed articles, conference papers, and preprints. (Adjust or remove if 'Publications' section is not used).</p>
        </div>
    </div>
    <div class="card">
        <img src="assets/images/placeholder_teaching.jpg" class="card-img" alt="Teaching Overview">
        <div class="card-body">
            <span class="card-label">Academics</span>
            <h3 class="card-title"><a href="teaching.md">Courses & Pedagogy</a></h3>
            <p>Details about the courses I teach and my approach to education. (Adjust or remove if 'Teaching' page is not used).</p>
        </div>
    </div>
</div>
```

- ```card-grid```: Wraps all your individual cards to create the grid layout.
- ```card```: Each individual card item.
- ```card-img```: Optional, for an image at the top of the card. Update src to your desired image.
- ```card-body```: Contains the text content of the card.
- ```card-label```: Small, uppercase text label (e.g., "MY WORK", "SCHOLARSHIP").
- ```card-title```: Main title of the card, usually a link.
- ```p```: Paragraph text for the card description.

#### Specific Card Types (```research-card```, ```news-card```)

While ```card``` is general, the template includes specific styles for ```research-card``` and ```news-card``` if you prefer to use them as simple blocks, particularly good for lists without images.

``` bash
### Highlights

<div class="card research-card">
    <a href="research.md"><strong>My Thesis Research: [Brief Title]</strong></a>
    <p>Developing novel approaches for [specific area]. Published in *[Journal Name]*, [Year].</p>
</div>

<div class="card news-card">
    <strong><a href="[https://dartmouth.edu/news/article-link](https://dartmouth.edu/news/article-link)" target="_blank">Featured in Dartmouth News: [Article Title]</a></strong>
    <p>Read about my involvement in the [project/event name] initiative at Dartmouth.</p>
</div>
```

### 3. Cover Gallery (Optional)

(Typically for researchers/academics) To display a gallery of journal/book covers:

#### Journal Covers (Example)

A selection of journal covers where my work (or work I've contributed to) has been featured.

``` bash
<div class="cover-gallery-wrapper">
    <div class="cover-gallery">
        <div class="cover-item">
            <a href="[https://example.com/cover-paper1.pdf](https://example.com/cover-paper1.pdf)" target="_blank">
                <img src="assets/images/placeholder_cover1.jpg" alt="Journal Cover 1">
            </a>
            <p class="journal-name">Example Journal Title</p>
            <p>Vol. XX, No. Y, [Year]</p>
            <p>Our work on [brief topic].</p>
        </div>
        <div class="cover-item">
            <a href="[https://example.com/cover-paper2.pdf](https://example.com/cover-paper2.pdf)" target="_blank">
                <img src="assets/images/placeholder_cover2.jpg" alt="Journal Cover 2">
            </a>
            <p class="journal-name">Another Journal Title</p>
            <p>Vol. AA, Issue BB, [Year]</p>
            <p>Featured research: [brief topic].</p>
        </div>
        </div>
</div>
```

- ```cover-gallery-wrapper```: Provides a background and padding for the gallery.
- ```cover-gallery```: The grid container for individual covers.
- ```cover-item```: Each individual cover, containing an image link and text.
- ```journal-name```: Specific class for the journal/book title for custom styling.

### 4. Research Project Sections (Optional)

(Typically for faculty/researchers with distinct projects) For detailed project descriptions, with images floating left or right.

``` bash
# My Research Projects (Example)

My research program at Dartmouth College focuses on [your main research theme]. We leverage [key methodologies, e.g., computational modeling, advanced experimental techniques, theoretical frameworks] to investigate [main problems or questions].

## Current Research Projects

### Project A: [Engaging Project Title]

<div class="project-section">
    <div class="project-figure float-right">
        <img src="assets/images/placeholder_projectA.jpg" alt="Image related to Project A">
        <p class="project-caption">Figure 1.1: [Brief caption for Project A image].</p>
    </div>
    <p>This project delves into [specific topic within Project A]. We are exploring [key aspects or questions]. Our recent work on this topic involves [mention a specific method or discovery].</p>
    <p>The long-term goal of this project is to [explain the broader impact or future direction]. We anticipate these findings will [explain anticipated outcomes, e.g., inform new therapeutic strategies, enhance our understanding of X, or lead to to development of Y].</p>

    <div class="admonition project-summary">
        <p><strong>Summary:</strong> Investigating [concise summary of project].</p>
        <p><strong>Funding:</strong> [Grant Agency (if applicable)], [Grant ID (if applicable)]</p>
        <p><strong>Keywords:</strong> #TopicA, #MethodB, #ApplicationC</p>
        <p><a href="publications/placeholder-paper-A.md">Related Publication: [Link to Paper Title]</a></p>
    </div>
</div>

<div style="clear: both;"></div> ### Project B: [Another Project Title]

<div class="project-section">
    <div class="project-figure float-left">
        <img src="assets/images/placeholder_projectB.jpg" alt="Image related to Project B">
        <p class="project-caption">Figure 2.1: [Brief caption for Project B image].</p>
    </div>
    <p>In this project, we are developing [new approach or technology] to address [problem]. Our approach combines [method 1] with [method 2] to gain novel insights into [area of study].</p>
    <p>We are particularly excited about [a specific challenge or discovery within this project]. Collaborations with [collaborator/institution] are a key component of this work.</p>

    <div class="admonition project-summary">
        <p><strong>Summary:</strong> Developing [concise summary of project].</p>
        <p><strong>Collaborators:</strong> Prof. [Collaborator Name], [Institution]</p>
        <p><strong>Keywords:</strong> #TopicD, #MethodE, #ChallengeF</p>
        <p><a href="[https://github.com/your-github/projectB-code](https://github.com/your-github/projectB-code)" target="_blank">View Project Code on GitHub</a></p>
    </div>
</div>

<div style="clear: both;"></div>

## Research Opportunities (Optional)

(If you are a P.I. looking for team members) I am always looking for motivated undergraduate and graduate students interested in [your field]. If you are passionate about [your field] and eager to contribute to cutting-edge research, please visit the contact page or email me directly for more information on how to apply.
```

### 5. Admonitions

Standard Materials for MkDocs admonitions (```!!! note```, ```!!! warning```, ```!!! info```) are styled with Dartmouth colors.

```bash
!!! info "Important Note"
    This is an informational box with Dartmouth branding colors.
    It's great for drawing attention to specific details or important announcements.

!!! tip "Helpful Tip"
    Remember to replace all placeholder text with your actual content and images!

!!! warning "Caution!"
    Be mindful of [specific caution or disclaimer].
 ```

### 6. Image Alignment

You can use the ```attr_list``` extension to align images within your text flow:

```bash
![Image Description](assets/images/your_image.jpg){ align=right }

This is some text that will wrap around the image. You can use `align=right` to float the image to the right, or `align=left` to float it to the left. This allows for flexible content layouts.

![Another Image](assets/images/another_image.jpg){ align=left }

This text will wrap around the image floated to the left. For images you want centered, use `align=center`.

![Centered Image](assets/images/centered_image.jpg){ align=center }

This image will be displayed as a block element and centered on the page.
```

### 7. Custom Footer (```overrides/partials/footer.html```)

his template includes a custom Dartmouth-branded footer that replaces the default MkDocs-Material footer. This is achieved by overriding a theme template.

Location: ```overrides/partials/footer.html```

#### How it Works:

- Materials for MkDocs allows you to inject custom HTML into specific parts of its templates using the ```custom_dir``` feature (set to ```overrides``` in ```mkdocs.yml```).
- In this setup, a ```main.html``` file within ```overrides``` (or another appropriate override file) would typically include a line to pull in ```partials/footer.html```.
  - **Note:** Your provided ```footer.html``` snippet seems to be a self-contained file intended to be included by a parent template. Ensure your ```overrides/main.html``` (or ```overrides/base.html``` if overriding the entire base layout) has a line like {```% include "partials/footer.html" %```} in the desired location for the footer.

#### Configuration Steps:

##### 1. Dartmouth Logo:
```src="{{ base_url }}/assets/images/dartmouth/d-pine-logo.png"```: This path points to the Dartmouth "D-Pine" logo. Ensure this image file exists in your ```docs/assets/images/dartmouth/``` directory. If you prefer a different logo, update the ```src``` path accordingly.

##### 2. Department/School Links:

The ```footer-text``` div contains example links to "Dartmouth," "Department of X," and "Department Y."

**Action:** Update these ```<a>``` tags with the correct names and URLs for your specific department, school, or any other relevant Dartmouth affiliations.
- ```<div><a href="https://x.dartmouth.edu/" target="_blank">Department of X</a></div>```
- ```<div><a href="https://school.dartmouth.edu/y/" target="_blank">Department Y</a></div>```
- Remove any lines that are not applicable to your affiliations.

##### 3. Social Media & Contact Links:

The ```footer-links``` section uses Font Awesome icons (```<i>``` tags with ```fas``` or ```fab``` classes) for various contact and social profiles.

***Action:***
- ***Email:*** ```mailto:youremail@dartmouth.edu```
  - Change ```youremail@dartmouth.edu``` to your actual Dartmouth email address.
- ***Google Scholar:*** https://scholar.google.com/  
  - Replace this with your specific Google Scholar profile URL. The icon ```fas fa-graduation-cap``` is used.
- ***GitHub:*** https://github.com/  
  - Replace this with your specific GitHub profile ```URL```. The icon ```fab fa-github``` is used.
- **Curriculum Vitae (CV):** {{ base_url }}/assets/files/cv.pdf  
  - Update the path to your CV PDF file. Ensure ```cv.pdf``` is placed in ```docs/assets/files/```. The icon ```fas fa-file-alt``` is used.
- **Add/Remove Links:*** You can add more social links (e.g., LinkedIn, Twitter) by duplicating an ```<a>``` tag, changing the ```href```, ```title```, and the Font Awesome ```<i>``` class (e.g., ```fab fa-linkedin```, ```fab fa-twitter```). Remove any links that you don't use.

##### 4. Your Name:

```<div class="footer-name">YOUR NAME</div>```  
    - Replace ```"YOUR NAME"``` with your full name.

#### Important Considerations:

- **Font Awesome Integration:** The ```footer.html``` file includes ```link``` tags for Font Awesome 6 and Material Icons in the ```extrahead block```. These ensure the icons display correctly.
- ```overrides/main.html```: For this ```footer.html``` to be effective, your ```overrides/main.html``` file (or whatever base template you are overriding) needs to explicitly include it. A typical ```main.html``` that integrates this footer might look something like this (simplified):

```bash 
{# overrides/main.html #}
{% extends "base.html" %}

{# Other blocks from base.html might go here, e.g., for content, header #}

{% block content %}
  {{ super() }} {# Renders the main Markdown content #}
{% endblock %}

{% block footer %}
  {% include "partials/footer.html" %}
{% endblock %}

{# If footer.html has its own extrahead block, it might need to be hoisted #}
{% block extrahead %}
  {{ super() }} {# Keeps anything from parent extrahead #}
  <link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet">
  <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css" rel="stylesheet">
{% endblock %}
```

Confirm that your ```main.html``` (or equivalent) includes ```footer.html``` in the appropriate ```{% block footer %}``` or similar section. If you don't have an ```overrides/main.html``` yet, you'll need to create one to inject this custom footer.
