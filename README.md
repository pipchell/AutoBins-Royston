##Bins – Royston##

A simple, efficient web tool for viewing upcoming bin collection schedules in Royston. The project focuses on clarity, mobile accessibility, and ease of maintenance while avoiding unnecessary complexity.

Overview

Bins – Royston is a minimal web application that displays upcoming bin collection days for households in the Royston area. The goal is to provide a fast-loading, easy-to-read page that works consistently across devices.

The site is built with plain HTML, CSS, and lightweight JavaScript where necessary. No frameworks or external libraries are used.

Key Features
Clean Layout

Clear containers display the next collection for each bin type. Information is presented without visual clutter.

Mobile-Optimised Scaling

A responsive scaling system enlarges the interface on mobile devices for improved readability. This preserves the desktop layout while enhancing mobile usability.

Flexible Styling

All typography and spacing are controlled through CSS variables, allowing quick edits to:

Text size

Card spacing

Layout width

Color themes

Overall responsiveness

Lightweight Structure

The project runs entirely from one HTML file for easy hosting, quick loading, and simple maintenance.

Easy Maintenance

Bin dates can be updated by editing a single section of the HTML—no databases or APIs required.

Project Structure
/project-root
│
├── index.html   # Main and only file containing layout, styling, and responsive scaling
└── README.md    # Documentation

How Mobile Scaling Works

The project uses proportional zoom via CSS transforms. This keeps the desktop layout intact while enlarging it on mobile:

@media screen and (max-width: 768px) {
    .scale-wrapper {
        transform: scale(1.17);
        transform-origin: top center;
    }
}


Change the value to adjust zoom.

Editing Bin Dates

Update bin schedules directly inside the HTML:

<div class="box green">
    <h2>Green Bin</h2>
    <p>Next collection: Monday</p>
</div>

Adjusting Zoom Level

Modify:

transform: scale(1.17);


Lower values reduce zoom. Higher values increase it.

Adjusting Desktop Width

The max width of the content area is set with:

width: min(100%, 900px);


Change 900px to increase or reduce the desktop container width.

Why This Project Exists

The official bin-collection interface is harder to read quickly, inconsistent across devices, and often cluttered.
This project improves on that by:

Putting all information on one screen

Removing unnecessary navigation

Improving readability at a distance

Using one codebase for all devices

Loading instantly, even on slow connections

The design principle: simple, readable, fast.

Future Improvements

Potential enhancements:

“Put out” toggle using local storage

Push or email notifications

Colorblind-friendly theme option

Automatic date rotation logic

Export to iCalendar (.ics)

All optional features will maintain the minimal approach.

Contributing

If contributing:

Keep the single-file structure

Avoid adding unnecessary dependencies

Preserve readability and simplicity

Verify layout on both mobile and desktop

License

A permissive license such as MIT is recommended.
