# Image Optimization Guide for Peak Season Services

## Current Image Audit

### Existing Images
- `public/images/placeholder-hero.svg` - Used as hero image and Open Graph image

### Images Needed for Full Optimization

#### 1. Hero Images (High Priority)
**Recommended Sizes: 1200x600px minimum**

- `hero-christmas-lights-denton.jpg` - Main hero image for homepage
- `hero-flower-mound-lights.jpg` - Flower Mound location page
- `hero-lewisville-lights.jpg` - Lewisville location page  
- `hero-corinth-lights.jpg` - Corinth location page
- `hero-faq-support.jpg` - FAQ page hero

**Alt Text Examples:**
- "Professional Christmas light installation on Denton TX home with festive holiday display"
- "Beautiful holiday lighting installation on Flower Mound luxury home"
- "Festive Christmas lights illuminating Lewisville residential property"

#### 2. Service Images (High Priority)
**Recommended Sizes: 800x600px**

- `residential-christmas-lights-installation.jpg`
- `commercial-holiday-lighting-display.jpg`
- `permanent-holiday-lighting-system.jpg`
- `roofline-christmas-light-installation.jpg`
- `tree-wrapping-holiday-lights.jpg`
- `landscape-christmas-lighting.jpg`

**Alt Text Examples:**
- "Professional technician installing Christmas lights on residential roofline in Denton TX"
- "Commercial building with professional holiday lighting display"
- "Permanent LED holiday lighting system on luxury home"

#### 3. Before/After Images (Medium Priority)
**Recommended Sizes: 600x400px**

- `before-after-denton-home-1.jpg`
- `before-after-flower-mound-display.jpg`
- `before-after-commercial-property.jpg`

**Alt Text Examples:**
- "Before and after Christmas light installation on Denton home showing dramatic transformation"

#### 4. Team/Process Images (Medium Priority)
**Recommended Sizes: 800x600px**

- `peak-season-team-installing-lights.jpg`
- `professional-christmas-light-design-consultation.jpg`
- `safety-equipment-ladder-installation.jpg`
- `commercial-grade-led-christmas-lights.jpg`

**Alt Text Examples:**
- "Peak Season Services team professionally installing Christmas lights with safety equipment"
- "Christmas light design consultation with Denton homeowner"

#### 5. Local Area Images (Medium Priority)
**Recommended Sizes: 600x400px**

- `denton-square-holiday-lights.jpg`
- `unt-campus-area-christmas-display.jpg`
- `lake-lewisville-waterfront-holiday-lights.jpg`
- `flower-mound-luxury-home-christmas.jpg`

**Alt Text Examples:**
- "Denton Square decorated with festive holiday lighting for Christmas season"
- "UNT campus area home with professional Christmas light installation"

#### 6. Blog Images (Medium Priority)
**Recommended Sizes: 600x400px**

- `christmas-light-safety-ladder-installation.jpg`
- `led-vs-traditional-christmas-lights-comparison.jpg`
- `weatherproofing-christmas-lights-north-texas.jpg`
- `maintenance-christmas-light-repair.jpg`

#### 7. Social Media Images (Low Priority)
**Recommended Sizes: 1200x630px (Open Graph)**

- `og-peak-season-services-logo.jpg`
- `og-denton-christmas-lights.jpg`
- `og-holiday-lighting-tips.jpg`

## Image Optimization Best Practices

### File Formats
- **WebP**: Modern format, 25-50% smaller than JPEG
- **JPEG**: For photos with many colors
- **PNG**: For images with transparency or simple graphics
- **SVG**: For logos and simple graphics (already have for placeholder)

### Image Compression
- Target file sizes:
  - Hero images: Under 150KB
  - Service images: Under 100KB
  - Other images: Under 75KB

### Responsive Images
Implement multiple sizes for different screen sizes:
```html
<img 
  src="/images/hero-denton-lights-800.webp"
  srcset="/images/hero-denton-lights-400.webp 400w,
          /images/hero-denton-lights-800.webp 800w,
          /images/hero-denton-lights-1200.webp 1200w"
  sizes="(max-width: 768px) 400px,
         (max-width: 1024px) 800px,
         1200px"
  alt="Professional Christmas light installation on beautiful Denton TX home"
  loading="lazy"
>
```

### Alt Text Guidelines
- Describe what's in the image specifically
- Include relevant keywords naturally
- Mention location when relevant (Denton, Flower Mound, etc.)
- Keep under 125 characters when possible
- Don't start with "Image of" or "Picture of"

### Lazy Loading Implementation
- Add `loading="lazy"` to all images except above-the-fold hero images
- Use `loading="eager"` for critical hero images

## Implementation Priority

### Phase 1 (Immediate - Week 1)
1. Replace placeholder hero image with professional Christmas lights photo
2. Add proper alt text to existing images
3. Implement lazy loading on non-critical images
4. Create optimized Open Graph images

### Phase 2 (Week 2-3)
1. Add service-specific images to each page
2. Create before/after showcase galleries
3. Add team/process photos for credibility

### Phase 3 (Week 4+)
1. Local area specific images
2. Seasonal blog post images
3. Social media optimized images

## SEO Impact

### Image SEO Benefits
- Proper alt text improves accessibility and SEO
- File names with keywords boost search rankings
- Faster loading improves user experience and Core Web Vitals
- Local images help with local SEO

### Recommended File Naming Convention
- Use descriptive, keyword-rich names
- Include location when relevant
- Use hyphens to separate words
- Examples:
  - `christmas-lights-installation-denton-tx.jpg`
  - `holiday-lighting-flower-mound-home.jpg`
  - `commercial-christmas-display-lewisville.jpg`

## Technical Implementation

### Astro Image Optimization
Consider using Astro's built-in image optimization:
```astro
---
import { Image } from 'astro:assets';
import heroImage from '../images/hero-denton-lights.jpg';
---

<Image 
  src={heroImage} 
  alt="Professional Christmas light installation Denton TX"
  width={1200}
  height={600}
  loading="eager"
  format="webp"
/>
```

### Performance Monitoring
- Monitor Core Web Vitals after image updates
- Use tools like Google PageSpeed Insights
- Track image loading performance in Google Analytics

## Content Creation Guidelines

### Photography Requirements
When commissioning or taking photos:

1. **Technical Requirements:**
   - Minimum resolution: 1920x1080
   - Good lighting (preferably evening for Christmas lights)
   - Sharp focus, professional quality
   - Show actual installations, not stock photos

2. **Content Requirements:**
   - Feature real Denton-area homes when possible
   - Show diverse property types and styles
   - Include safety equipment and professional appearance
   - Capture seasonal/weather-appropriate conditions

3. **Legal Requirements:**
   - Obtain proper releases for private properties
   - Ensure photos are original or properly licensed
   - Maintain consistent branding/quality

## Measuring Success

### Metrics to Track
- Page load speed improvements
- Image engagement in Google Search Console
- Reduced bounce rates on image-heavy pages
- Increased time on page
- Better rankings for image searches

### Tools for Monitoring
- Google PageSpeed Insights
- GTmetrix
- Google Search Console (Image tab)
- Google Analytics (Page Speed reports)

### Expected Improvements
- 20-30% faster page load times
- 15-25% improvement in Core Web Vitals scores
- 10-20% increase in image search traffic
- Better user engagement metrics