# Social Media Icon Animator

## Description
Provides standardized animations for social media icons with accessibility and performance in mind.

## Prompt
When asked about social media icon animations, suggest solutions that:
- Use React-compatible CSS or library animations
- Include hover and focus states for accessibility
- Maintain performance with hardware acceleration
- Consider reduced motion preferences
- Include smooth transitions

## Example
```jsx
const SocialIcon = ({ url, icon }) => {
  return (
    <a 
      href={url}
      className="social-icon"
      aria-label={`Visit my ${icon} profile`}
    >
      <i className={`fab fa-${icon}`} />
    </a>
  );
};

/* CSS */
.social-icon {
  transition: transform 0.2s ease;
  will-change: transform;
}

.social-icon:hover,
.social-icon:focus {
  transform: scale(1.1);
}

@media (prefers-reduced-motion: reduce) {
  .social-icon {
    transition: none;
  }
}