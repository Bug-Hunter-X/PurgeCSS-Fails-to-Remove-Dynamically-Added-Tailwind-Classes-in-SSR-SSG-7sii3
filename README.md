# PurgeCSS and Dynamically Added Tailwind Classes
This repository demonstrates a common issue with PurgeCSS in Tailwind CSS when using server-side rendering (SSR) or static site generation (SSG) frameworks. Dynamically added classes may not be purged, leading to bloated CSS output.

## Problem
When using frameworks like Next.js or Nuxt.js, Tailwind's PurgeCSS may not identify all classes used if those classes are added to the DOM dynamically after the initial render. This results in unused CSS classes being included in the final build, increasing its size.

## Solution
To resolve this, we need to ensure that PurgeCSS can correctly identify all classes used, even those added dynamically.  Several strategies can be used, including adjusting PurgeCSS configurations or using different techniques for adding classes dynamically, like using a pre-defined set of classes and applying those within an existing dynamic structure.