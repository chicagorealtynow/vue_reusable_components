# Vue Reusable Components

A collection of reusable Vue.js components commonly used in portfolio and business websites.

## Components

### Layout Components
- **NavBar** - A responsive navigation bar component
- **Footer** - A customizable footer component
- **BackToTop** - A button component that scrolls the page back to top

### Section Components
- **HeroSection** - A hero/banner section for the main landing area
- **AboutSection** - A section for displaying company/personal information
- **ServicesSection** - A section to showcase services offered
- **ExperienceAndSkills** - A component to display professional experience and skills
- **LatestProjSection** - A portfolio section for showing recent projects
- **TestimonialsSection** - A section for displaying client testimonials
- **ContactSection** - A contact form section with validation

### Utility Components
- **loadingSpinner** - A loading animation component for async operations

## Installation

```bash
# Clone the repository
git clone https://github.com/[username]/vue_reusable_components

# Install dependencies
npm install
```

## Usage

Import the components you need in your Vue.js project:

```javascript
import NavBar from './components/NavBar.vue'
import HeroSection from './components/HeroSection.vue'
// ... import other components as needed

export default {
  components: {
    NavBar,
    HeroSection,
    // ... register other components
  }
}
```

## Features

- Fully responsive components
- Customizable through props
- Built with Vue.js best practices
- Easy to integrate into existing projects
- Modern and clean design
- Reusable across different projects

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is open source and available under the [MIT License](LICENSE).
