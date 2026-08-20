# Google Search Clone

This project is a recreation of Google's Search, Image Search, and Advanced Search pages.

It was created as part of CS50's Web Programming with Python and JavaScript, Project 0: Search.

## Description

The goal of this project is to recreate the Google Search interface using HTML and CSS, without using JavaScript.

The website includes three different search pages:

- Google Search
- Google Image Search
- Google Advanced Search

The forms send GET requests to Google's existing search server using the parameters expected by Google.

## Features

### Google Search

The main page allows users to enter a search query and perform a normal Google search.

The search form sends the query to:

```
https://www.google.com/search
```

The search input uses:

```html
<input type="text" name="q">
```

The `name="q"` attribute is important because Google uses the `q` parameter for the search query.

For example, if the user searches for:

```
minecraft
```

the browser sends a request similar to:

```
https://www.google.com/search?q=minecraft
```

The page also includes an **I'm Feeling Lucky** button.

### Google Image Search

The Image Search page allows users to search for images through Google's existing search system.

The form sends the user's search query together with the parameter required by Google to display image results.

For example:

```
q=minecraft
udm=2
```

The `q` parameter contains the search query, while the additional parameter tells Google to display image results.

### Google Advanced Search

The Advanced Search page provides several search options that correspond to Google's advanced search parameters.

The available fields are:

| Field | Parameter |
|---|---|
| All these words | `as_q` |
| This exact word or phrase | `as_epq` |
| Any of these words | `as_oq` |
| None of these words | `as_eq` |

These parameters are sent to Google's search server when the form is submitted.

## Technologies

This project was built using:

- HTML5
- CSS3

No JavaScript is used.

## Project Structure

```
search/
│
├── README.md
├── index.html
├── images.html
├── advanced.html
└── styles.css
```

## Files

### `index.html`

Contains the main Google Search page.

It includes:

- Google Search
- I'm Feeling Lucky
- A link to Image Search
- A link to Advanced Search

### `images.html`

Contains the Google Image Search page.

It includes:

- An image search form
- A link back to the main search page

### `advanced.html`

Contains the Google Advanced Search page.

It includes:

- All these words
- This exact word or phrase
- Any of these words
- None of these words
- A link back to the main search page

### `styles.css`

Contains the CSS used to style all three pages.

## How It Works

The project uses HTML forms to send GET requests to Google's search server.

A basic form looks like this:

```html
<form action="https://www.google.com/search">
    <input type="text" name="q">
    <input type="submit" value="Google Search">
</form>
```

When the user enters:

```
minecraft
```

the browser creates a URL similar to:

```
https://www.google.com/search?q=minecraft
```

The browser then sends the request to Google.

### Hidden Inputs

Some search pages require additional parameters.

These can be sent using hidden inputs:

```html
<input type="hidden" name="udm" value="2">
```

The user cannot see this input on the page, but the browser still includes it when submitting the form.

This allows the project to send additional parameters required by Google without requiring the user to enter them manually.

## What I Learned

Through this project, I learned:

- How HTML forms work.
- How the `action` attribute determines where form data is sent.
- How GET requests work with HTML forms.
- How input `name` attributes become URL parameters.
- How `input type="hidden"` can send fixed parameters.
- How to inspect HTTP requests using browser developer tools.
- How to analyze URL query parameters.
- How to recreate an existing web interface using HTML and CSS.
- How to organize a small web project.
- How to use Git and GitHub to manage a project.

## Testing

The search forms can be tested by entering different queries and checking whether they correctly redirect to Google's:

- Normal Search
- Image Search
- Advanced Search
- I'm Feeling Lucky functionality

The browser's developer tools can also be used to inspect the requests generated when submitting each form.

## Course

This project was created for:

**CS50's Web Programming with Python and JavaScript**
Project 0: Search

Course website: https://cs50.harvard.edu/web/

Project specification: https://cs50.harvard.edu/web/projects/0/search/

## Author

Héctor Mula Águeda
