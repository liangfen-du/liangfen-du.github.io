# AGENTS.md

This file contains guidelines and commands for agentic coding agents working in this Academic Pages Jekyll repository.

## Project Overview

This is an Academic Pages website - a Jekyll-based static site generator designed for academic and professional portfolio websites. It's built on the Minimal Mistakes theme and optimized for GitHub Pages deployment.

**Key Characteristics:**
- Static site generator using Jekyll (Ruby-based)
- Content-driven architecture using YAML data files and Markdown
- Mobile-first responsive design
- Academic-focused with publications, teaching, talks, and portfolio support

## Development Commands

### Local Development
```bash
# Start local development server with live reload
bundle exec jekyll serve -l -H localhost

# Alternative: Docker-based development
docker compose up
```

### Build Commands
```bash
# Build JavaScript (minify and concatenate)
npm run build:js
# or
npm run uglify

# Watch JavaScript files for changes and rebuild automatically
npm run watch:js

# Build the entire Jekyll site
bundle exec jekyll build
```

### Testing
**No testing framework is currently configured.** This is a gap in the codebase that should be addressed.

## Code Style Guidelines

### JavaScript
- Use jQuery for DOM manipulation and event handling
- Traditional function declarations over arrow functions
- 4-space indentation
- Descriptive variable names (e.g., `scssLarge`, `didResize`, `bumpIt`)
- JSDoc-style comments for major sections
- Minimal error handling (jQuery's error-implicit approach)

### SCSS/CSS
- Component-based organization with clear section comments
- Mobile-first responsive design using breakpoints
- BEM-like class naming convention (`team-member`, `activity-item`, `banner-container`)
- Consistent use of SCSS variables and mixins
- Import dependencies in logical order

### Front Matter (YAML)
- Consistent field ordering: layout, title, permalink, author_profile
- Use Jekyll's default liquid template syntax
- Include proper YAML validation

### File Naming
- **Assets**: kebab-case (e.g., `main.css`, `custom.js`)
- **Data files**: snake_case (e.g., `team.yml`, `research_projects.yml`)
- **Classes**: kebab-case for CSS, camelCase for JavaScript
- **IDs**: kebab-case

## Architecture Patterns

### Data-Driven Content
- Use YAML files in `_data/` directory for structured content
- Liquid templates iterate over data for dynamic rendering
- Collections for publications, teaching, talks, and portfolio items

### File Organization
```
_layouts/     # HTML page templates
_includes/    # Reusable template partials
_sass/        # Stylesheets organized by function
_pages/       # Static page content
assets/       # CSS, JS, fonts, and images
_data/        # YAML data files
```

### Import Patterns
- SCSS: Use `@import` with clear dependency ordering
- JavaScript: Files concatenated via npm script
- Font Awesome: Import via SCSS modules

## Dependencies and Frameworks

### Core
- **Jekyll**: Ruby-based static site generator
- **Academic Pages theme**: Forked from Minimal Mistakes

### JavaScript
- jQuery 3.7.1
- fitvids (responsive video embedding)
- magnific-popup (lightbox functionality)
- jquery-smooth-scroll

### Jekyll Plugins
- jekyll-feed, jekyll-sitemap, jekyll-redirect-from
- jemoji, jekyll-gist, jekyll-paginate

### SCSS Frameworks
- Susy grid system (responsive layouts)
- Breakpoint SCSS mixin (media queries)
- Font Awesome (icons)
- Magnific Popup (lightbox styles)

## Content Guidelines

### Academic Publications
- Use structured YAML data for publications
- Support author highlighting and metadata
- Include DOI, journal, and publication information

### Team Members
- Profile structure with education and contact info
- Consistent image naming and sizing
- Role-based organization

### Research Projects
- Project descriptions with status and funding info
- Associated publications and team members
- Timeline and milestone tracking

## Deployment

### Primary (GitHub Pages)
- Automatic deployment on push to main branch
- Jekyll configuration in `_config.yml`

### Alternative (Vercel)
- Vercel configuration present
- Can be used for preview deployments

### Docker Support
- Container-based development and deployment
- Use `docker compose up` for local development

## Code Quality Improvements Needed

### Testing
- Set up a testing framework (Jest for JavaScript, RSpec for Ruby/Jekyll)
- Write unit tests for JavaScript functions
- Add integration tests for Jekyll builds

### Linting and Formatting
- Configure ESLint for JavaScript
- Add StyleLint for SCSS
- Implement Prettier for consistent formatting
- Add pre-commit hooks for code quality

### Error Handling
- Implement proper error handling in JavaScript
- Add validation for YAML data files
- Include fallbacks for missing data

## Common Tasks

### Adding New Team Members
1. Update `_data/team.yml`
2. Add team member photo to `assets/images/team/`
3. Follow existing naming conventions

### Adding Publications
1. Update `_data/publications.yml`
2. Include all required metadata fields
3. Link to associated team members

### Modifying Styles
1. Edit SCSS files in `_sass/`
2. Use existing variable system
3. Test responsive behavior at all breakpoints

### JavaScript Changes
1. Edit files in `assets/js/`
2. Run `npm run build:js` to rebuild minified version
3. Test jQuery compatibility

## Important Notes

- This is a static site - no server-side processing
- All content changes require Jekyll rebuild
- GitHub Pages handles deployment automatically
- Docker provides consistent development environment
- No current testing setup - this should be prioritized