# GOVUK Prototype kit table card plugin

This plugin transforms standard table rows into vertically stacked cards on smaller viewports, ensuring better usability on mobile devices while maintaining full accessibility. The table will function as a typical table when read by a screen reader, preserving the correct semantics.

## Features

- **Responsive design**: Automatically [switches between a traditional table layout and card layout](#example-output) based on the viewport width.
- **Accessible**: Maintains [table semantics for screen readers](#accessibility), ensuring tabular data remains accessible.
- **Customisable**: Supports custom captions, headers, and row content.

## Installation

To install the plugin, add it to your project using NPM:

```bash
npm install govuk-table-card-plugin
```

## Usage

Here’s an example of how to use the govukTableCard component in your project:
```nunjucks
{{ govukTableCard({
  caption: {
    text: 'Project deadlines',
    classes: 'govuk-table__caption--l'
  },
  headers: [
    {
      name: 'Deadline'
    },
    {
      name: 'Project name'
    },
    {
      name: 'Days left',
      numeric: true
    }
  ],
  rows: [
    ['10th November 2024', 'Website redesign', '30'],
    ['20th November 2024', 'Marketing campaign', '40'],
    ['5th December 2024', 'New product launch', '55'],
    ['15th December 2024', 'Internal audit', '65'],
    ['1st January 2025', 'Annual report', '82'],
    ['15th January 2025', 'Team onboarding', '96'],
    ['1st February 2025', 'System upgrade', '113'],
    ['15th February 2025', 'Customer feedback review', '127'],
    ['1st March 2025', 'New service rollout', '141'],
    ['15th March 2025', 'Quarterly budget review', '155']
  ]
}) }}
```

### Parameters

* caption: Defines the table caption. Includes:
  * text: The content of the caption.
  * classes: Optional CSS classes to apply to the caption.
* headers: An array of objects defining the table headers. Each object can include:
  * name: The header title.
  * numeric: Optional, true for numeric data columns.
* rows: A 2D array defining the rows of the table, with each inner array representing a single row.

### Example output

![Example of table responding toe viewport width](./table-card.gif?raw=true)


### Accessibility

The component ensures that all table semantics are preserved for screen readers, meaning that users relying on assistive technologies will have a seamless experience regardless of the viewport size.

![Example of voiceover output](./screenreader-compatible.gif?raw=true)

## Updating

To update, go to `http://localhost:3000/manage-prototype/plugins-installed` and hit the update button.

