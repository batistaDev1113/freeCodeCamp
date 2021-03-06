---
id: 5efada803cbd2bbdab94e332
title: Part 28
challengeType: 0
isHidden: true
---

## Description
<section id='description'>

Inside the `figure` element you just added, nest an `img` element with a `src` attribute set to `https://bit.ly/fcc-cats`.

</section>

## Tests
<section id='tests'>

```yml
tests:
  - text: 'Your second `figure` element should have an opening tag. Opening tags have this syntax: `<elementName>`.'
    testString: assert( document.querySelectorAll('figure').length === 2 );
  - text: Your second `figure` element should have a closing tag. Closing tags have a `/` just after the `<` character.
    testString: assert( code.match(/<\/figure>/g).length === 2 );
  - text: There should be a second `figure` element right above the second `section` element's closing tag. You have them in the wrong order.
    testString: assert( $('main > section')[1].lastElementChild.nodeName === 'FIGURE' );
  - text: You should have a third `img` element nested in the `figure` element.
    testString: const catsImg = document.querySelectorAll('figure > img')[1]; assert( catsImg && catsImg.getAttribute('src').toLowerCase() === 'https://bit.ly/fcc-cats');
  - text: The third image should have an `src` attribute set to `https://bit.ly/fcc-cats`.
    testString: |
      const catsImg = document.querySelectorAll('figure > img')[1];
      assert( catsImg && catsImg.getAttribute('src').toLowerCase() === 'https://bit.ly/fcc-cats');
  - text: Although you have set the new image's `src` to the correct URL, it is recommended to always surround the value of an attribute with quotation marks.
    testString: assert( !/\<img\s+.+\s+src\s*=\s*https:\/\/bit\.ly\/fcc-cats/.test(code) );

```

</section>

## Challenge Seed
<section id='challengeSeed'>
<div id='html-seed'>

```html
<html>
  <body>
    <h1>CatPhotoApp</h1>
    <main>
      <section>
        <h2>Cat Photos</h2>
        <!-- TODO: Add link to cat photos -->
        <p>Click here to view more <a target="_blank" href="https://freecatphotoapp.com">cat photos</a>.</p>
        <a href="https://freecatphotoapp.com"><img src="https://bit.ly/fcc-relaxing-cat" alt="A cute orange cat lying on its back."></a>
      </section>
      <section>
        <h2>Cat Lists</h2>
        <h3>Things cats love:</h3>
        <ul>
          <li>cat nip</li>
          <li>laser pointers</li>
          <li>lasagna</li>
        </ul>
        <figure>
          <img src="https://bit.ly/fcc-lasagna" alt="A slice of lasagna on a plate.">
          <figcaption>Cats <em>love</em> lasagna.</figcaption>  
        </figure>
        <h3>Top 3 things cats hate:</h3>
        <ol>
          <li>flea treatment</li>
          <li>thunder</li>
          <li>other cats</li>
        </ol>
        --fcc-editable-region--
        <figure>
        </figure>
        --fcc-editable-region--
      </section>
    </main>
  </body>
</html>
```

</div>
</section>
