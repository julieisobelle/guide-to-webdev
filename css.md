# Oversikt i CSS

* [CSS-struktur](#CSS-struktur)
* [Selektorer](#Selektorer)
* [Farger og tekst](#Farger-og-tekst)
* [Layout med Flex](#Layout-med-Flex)
* [Responsivt design](#Responsivt-design)
* [Overganger og animasjoner](#Overganger-og-animasjoner)
* [Pseudoklasser og pseudeoelementer](#Pseudoklasser-og-pseudeoelementer)
* [Kommentarer i CSS](#Kommentarer-i-css)

## CSS-struktur

En CSS-fil kan enten være:

* Ekstern (kobles til HTML med `<link>`)
* Intern (skrevet i `<style>` i `<head>`)
* Inline (skrevet direkte i `style`-attributt på et element)

Eksempel på ekstern bruk:

```html
<link rel="stylesheet" href="stil.css">
```

## Selektorer

Selektorer brukes for å velge HTML-elementer som skal styles.

* `element`: Velger alle elementer av denne typen. F.eks. `p`, `h1`, `ul`
* `.klasse`: Velger elementer med en spesifikk klasse
* `#id`: Velger element med spesifikk ID
* Kombinasjoner: `div p`, `ul li`, `a:hover`, `section > h2`

Eksempel:

```css
p {
  color: black;
}
.navbar {
  background-color: lightgray;
}
#logo {
  width: 200px;
}
```

## Farger og tekst

Brukes for å style skrift og bakgrunner.

* `color`: Tekstfarge
* `background-color`: Bakgrunnsfarge
* `font-family`: Skrifttype
* `font-size`: Skriftstørrelse
* `text-align`: Justering av tekst (venstre, høyre, midt)

Eksempel:

```css
h1 {
  color: navy;
  font-family: Arial, sans-serif;
  text-align: center;
}
```

## Layout med Flex

`display: flex` brukes for å lage fleksible og responsive layouts.

* `flex-direction`: Retning på elementene (`row`, `column`)
* `justify-content`: Horisontal justering (f.eks. `flex-start`, `center`, `flex-end`, `space-around`, `space-between`, `space-evenly`)
* `align-items`: Vertikal justering (f.eks. `flex-start`, `center`, `flex-end`)

Eksempel:

```css
.container {
  display: flex;
  justify-content: center;
  align-items: center;
}
```

## Responsivt design

Tilpasning av utseende til ulike skjermstørrelser:

* `@media`: Medieforespørsler for tilpasning
* `max-width` / `min-width`: Betingelser for stilendringer

Eksempel:

```css
@media (max-width: 600px) {
  body {
    font-size: 14px;
  }
}
```

## Overganger og animasjoner

Gir visuelle effekter når stil endres:

* `transition`: Tidsstyrt endring av egenskaper
* `transform`: Endrer form, rotasjon, størrelse
* `animation`: Definerer bevegelse over tid

Eksempel:

```css
button {
  transition: background-color 0.3s;
}
button:hover {
  background-color: lightblue;
}
```

## Pseudoklasser og pseudeoelementer

* **Pseudoklasser** velger elementer i en bestemt tilstand:

  * `:hover`, `:focus`, `:first-child`, `:nth-child(n)`

* **Pseudeoelementer** påvirker deler av et element:

  * `::before`, `::after`, `::first-line`, `::placeholder`

Eksempel:

```css
a:hover {
  text-decoration: underline;
}
.card::before {
  content: "★ ";
  color: gold;
}
```

## Kommentarer i CSS

Kommentarer skrives slik:

```css
/* Dette er en kommentar */
```
