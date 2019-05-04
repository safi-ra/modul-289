# Template Sprache

Viele CMS bieten eine Template Sprache, die dir das Arbeiten vereinfacht.

Template Sprachen machen es möglich, einfache Logik in ein Template einzuführen. Zudem verhindern sie übliche Sicherheitslücken wie XSS-Attacken. 

## Twig

October CMS verwendet [Twig](https://twig.symfony.com/) als Template Sprache.

### Partials einbinden

Um ein Partial einzubinden verwende folgende Syntax:

```twig
{% partial 'mein-partial' %}
```

Dieser Code lädt das Partial aus `themes/dein-theme/partials/mein-partial.htm`.


### Content einbinden

Um ein Partial einzubinden verwende folgende Syntax:

```twig
{% content 'mein-inhalt' %}
```

Dieser Code lädt den Inhalt aus `themes/dein-theme/content/mein-inhalt.htm`.


### Asset einbinden

Um ein Asset einzubinden verwende folgende Syntax:

```twig
<link rel="stylesheet" href="{{ 'assets/main.css' | theme }}">

<script src="{{ 'assets/main.js' | theme }}"></script>

<img src="{{ 'assets/logo.png' | theme }}">
```