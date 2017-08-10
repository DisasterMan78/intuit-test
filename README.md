License applies ONLY to code, not assets. Assets are property of Intuit.

#Installation

Install Node from [https://nodejs.org/en/](https://nodejs.org/en/)

Via SSH

`$ git checkout git@github.com:DisasterMan78/intuit-test.git`

Via HTTPS

`$ git checkout https://github.com/DisasterMan78/intuit-test.git`

Then
`$ cd intuit-test`

Install dependencies

`$ npm install`

Start server

`$ node server/`

View page

[http://localhost:3000/](http://localhost:3000/)

Build SASS
`$ gulp sass`

Watch for changes and build
`$ gulp sass:watch`

#Notes

Assumptions have been made about the grid. While not pixel-perfect accurate to the designs, the layout obeys sensible rules. Ordinarily discussion with the designers would help obviate this issue.

Grid is made with [http://gridle.org/](http://gridle.org/) The solution is a little heavy handed for the needs of the test. Far more CSS has been generated for the grid than is needed. Gridle was chosen as a quick solution, not the best. Also, the website has a Balrog on it, so that clinches it.

Grid system uses floats over flexbox for maximum compatibility.

Responsive styling is mobile first.

Max content width is 1200px.

Desktop breakpoint starts at 900 pixels to ensure menu does not overlap with logo.

Mobile menu is controlled with a hidden checkbox, using the `input +label` 'hack'. Animation is handled with CSS transitions. No Javascript is used at all.

Fonts are installed locally. CORS restrictions prevents loading font files from intuit.com.

Page has been built and tested with Chrome. Modern browsers are targeted, but old browser should be well supported.