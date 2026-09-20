# Testing Evidence

## What I tested
I tested all four pages but primarily focused on the index page is it is the only one with photos other than the logo.
I tested them in the Chrome browser through DevTools and Lighthouse 13.4.1.
The website scored 89 for performance, 100 for accessibility, 100 for best practices, 91 for SEO, and 0 for CLS.

## Assets
| File | Dimensions | Format | Size | Source / License |
| --- | --- | --- | --- | --- |
| C1.svg | vector | SVG | 3.6 KB | Unsplash, Mar Sono, Unsplash License |
| C2-400w.jpg | 400 × 187 | JPEG q80 | 29.1 KB | Unsplash, Erika Fletcher, Unsplash License |
| C2-800w.jpg | 800 × 374 | JPEG q80 | 105.4 KB | Unsplash, Erika Fletcher, Unsplash License |
| C2-1200w.jpg | 1200 × 560 | JPEG q80 | 225.8 KB | Unsplash, Erika Fletcher, Unsplash License |
| C7-400w.jpg | 400 × 265 | JPEG q80 | 24.2 KB | Unsplash, Taylor Flowe, Unsplash License |
| C7-800w.jpg | 800 × 530 | JPEG q80 | 71.2 KB | Unsplash, Taylor Flowe, Unsplash License |
| C7-1200w.jpg | 1200 × 795 | JPEG q80 | 145.1 KB | Unsplash, Taylor Flowe, Unsplash License |
| Noto Serif | — | WOFF2 via Google Fonts | external | SIL Open Font License |
| Roboto | — | WOFF2 via Google Fonts | external | SIL Open Font License |

A browser load is 53 to 371 KB. The biggest difference to loading was the resizing of images. The original school and class images were 2760 x 5910 and 3022 x 4563 which took longer to load.
There are no audio, video, or embeds. I removed the YouTube video as it was for a previous assignment and not a part of my original capstone plan.

## Responsive widths
The website passed all resize tests

| Width | Layout behavior | Result |
| --- | --- | --- |
| 320 px | Single column; nav wraps to left-aligned list; hero h1 stays centered over image | Pass |
| 480 px | Same single-column layout; program cards full width | Pass |
| 768 px | Below the 48rem breakpoint, so header stacks logo above nav | Pass |
| 1024 px | Program grid splits to multiple columns; feature grid goes two-up | Pass |
| 1440 px | Wrapper caps at 75rem and centers; no over-stretch | Pass |

Both photos use srcset and sizes, allowing the browser to pick the best sized image per the space available on the page. 
The hero image is sized with sizes="(min-width: 77rem) 75rem, 100vw", because it fills the wrapper, which caps at 75rem.
The classroom image is sized with sizes="(min-width: 56rem) 50vw, 100vw", because it is half width when the feature grid splits.

## 200% Zoom
I zoomed to 200% at 1280px and went through all the pages. There is no horizontal scrolling anywhere. All elements readjust to fit within the screen (text reflows, nav wraps, images shrink). All my sizes are in rem which is what makes this work.

## Slow network
I tested the webpage in Lighthouse using a slow network and these were the results

| Metric | Result | Rating |
| --- | --- | --- |
| First Contentful Paint | 0.7 s | Good |
| Largest Contentful Paint | 0.9 s | Good |
| Total Blocking Time | 40 ms | Good |

Images and fonts did take a second to load in, but nothing moved or readjusted on the page. Text appeared right away as the fallbacks, Georgia and Arial. There is no invisible text thankfully due to display=swap and the fallbacks fonts that are not significantly different in size.

## Alt Text
I changed my alt text to more accurately describe the images. As I turned the logo into a link, I changed the alt to describe the purpose of the logo as a link rather than describe what the logo looks like.

| Image | Purpose | Alt text used |
| --- | --- | --- |
| C1.svg (logo) | Functional, it's wrapped in a link to the home page | "Advanced American Academy - Home" |
| C2 (campus) | Informative, shows the building | "Advanced American Academy campus, a glass and red brick building with a stairway and red path leading to the entrance" |
| C7 (classroom) | Informative, shows a class in session | "Students working at desks in an Advanced American Academy classroom, viewed from behind a student" |


##
