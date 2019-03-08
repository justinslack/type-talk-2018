# fonts on the web

I work at a company called NML where I head up the design and front-end team.

---

# Hand lettering bible

Not going to go to the history of type as we will be here all weekend. Let's start here.

any idea what we are looking at?

---

# Gutenberg bible

This one?

---

# Gutenberg bible

Moveable type

# Black letter

Guttenberg's type

Punches

---

# Pierre Haultin

This one. huguenot bible
Kenneth Ormand

---

# Modernism

Modernism - early 20th century

Bauhaus - skipped a few centuries. Jan Tchisold's new typography

Art nouveau, Swiss style - helvetica, expressive typography
Herb Lubalin

---

# First web site

Show web site and responsiveness

Point out that it's just text

Images would come in 1993

---

# Type on the scree

Core fonts for the Web

Andalé Mono,
Arial,
Arial Black,
Comic Sans MS,
Courier New,
Georgia,
Impact,
Times New Roman,
Trebuchet MS,
Verdana
Webdings,
all of them in TrueType font format

---

# Font wars

Apple first to offer varying width fonts. Previously, most computer systems were limited to using monospaced fonts, as on a typewriter, requiring, for example, j and m to be the same width.

Postcript allowed printing from the screen for the first time. Everyone was paying royalties to adobe. In 1990 Adobe published Type 1 which allowed matching between what you saw on the screen and what was printed for the first time

True Type was born as a rival but never properly adopted.

OpenType allowed fonts to use either TrueType or Type 1 formats, and let a single font file work on both Mac and Windows, making documents much easier to share.

---

# Why open type?

we may use woff on the web but woff is invariably derived from open type

Much fewer files for a font family

---

# Netscape

Bitstream TrueDoc(TM)
.pfr font requires an active-x control to run in IE
Manual refresh required after activating active-x
Netscape 6 = open source no more proprietary fonts

---

# IE

Show link from web archive

Everyone hates on IE but it was the first browser to have full CSS support

---

IE 2

Microsoft Typography
.eot is proprietary and requires a browser plugin to render in Netscape

impasse!

Ridiculous solutions - SIFR - Scalable Inman Flash Replacement

Cufon - js

---

# @font-face

major problem with adopting font-face was licensing concerns

2008 - safari and ie
2010 - chrome, firefox and opera

---

# woff

uses a compressed version of the same table- based sfnt structure used by TrueType, OpenType, and Open Font Format, but adds metadata and private-use data structures, including predefined fields allowing foundries and vendors to provide license information if desired.

---

# Bullet proof syntax

Bullet proof font-face devised by Paul Irish - Mostly for IE6, 7, 8 but also older iOS. 2009

Don't need it any more

---

# woff - current syntax

Font data is compressed. Sites using WOFF will use less bandwidth and will load faster than if they used equivalent uncompressed TrueType or OpenType files.
Many font vendors that are unwilling to license their TrueType or OpenType format fonts for use on the web will license WOFF format fonts.
Both proprietary and free-software browser vendors support the WOFF format.

---

# Open type features

OpenType features allow fonts to behave smartly

---

# ligatures

Common/standard ligatures (the liga feature) exist to resolve spacing problems in a sequence of glyphs (for example, when an ‘f’ crashes into the dot of an ‘i’) by replacing the glyphs with a single glyph — a more elegant combination of the letterforms.

some browsers enable ligatures by default - safari, chrome and firefox

contextual and discretionary

---

# enable open type

The CSS3 Specification defines two ways of accessing OpenType features in CSS: high-level and low-level properties.

High-level properties are independent of font format and have semantic, human-readable names. The specification recommends authors to use these properties whenever possible – but not all browsers support them yet.

The low-level property font-feature-settings is specific to OpenType fonts. It offers an easy way to access OpenType features directly using standard 4-letter tags. This property is supported by the latest versions of all major browsers.

---

# ligatures 2

Ligatures they are not essential in most cases. In some cases they actually make type more difficult to read.

The real point is for you to look at the faces you’re using and see if they really need ligatures, or if, in fact, they are actually getting in the way of readability for the sake of “aesthetic” (which is in the eye of the beholder) fineness.

Problem is we have to switch them off

---

# Performance matters

Web fonts are great

Open type features are great - they give personality to our type, make data easier to read.

But they come at a cost and that cost is performance

---

# foit

FOIT or Flash of invisible text

The font hasn't downloaded yet and the browser is blocking the rendering of all text.

---

# FOIT

Flash of unstyled text

The font hasn't downloaded yet and the browser is showing a fallback.

---

# Download even less

To mitigate the file size of WOFF files, most @font-face generators and font services and subset fonts. Subsetting removes any characters that are deemed (or assumed) to be unnecessary, regardless of what the type designer originally intended.

While subsetting is often worthwhile, or even necessary, it also imposes many limitations that aren’t immediately obvious:

In practice, however, browser inconsistencies are not the first problem encountered. Often, those ligatures, alternate glyphs, and other versatile design considerations, are being subset out of the font file before you can ever use them with CSS.

Requires strict maintenance/control of your CSS

Typically requires you to hard code which web fonts you want to load on the page. This can mean that you end up loading more web font content than a page needs.

Could be License restrictions

---

# data uri

It puts a large Data URI in the critical path. Remember that CSS blocks rendering. The goal here is to avoid a Flash of Invisible Text (FOIT) and minimize our Flash of Unstyled Text (FOUT). It obviously isn’t a good tradeoff to delay the entire page render to avoid FOIT and FOUT. Since 42% of web sites load more than 40KB of web font page weight, many sites would need to put 40KB of Data URIs in their critical path, far exceeding the recommended 14KB window for critical content.

If you embed a Data URI, you’ll probably embed the WOFF format to give you ubiquity (better browser support)

Could inline a subset then asynchronously load the rest (js dependent?)

Ability to cache fonts suffers. This approach worsens with repeat views because the Data URI is tightly coupled to the markup and will not be cached

If you have multiple web fonts, making them all Data URIs forces them to be loaded sequentially (bad) instead of in parallel (good).

---

# font-display

It always feels weird to me to be reliant on JavaScript to fix what is a CSS-driven problem. i.e. go to step 3 (parse JS, execute) to fix a problem at step 2 (parse CSS, paint). Being reliant on JS is a CON for the strategies that use JS?

---

# font-display

Font block period
If the font face is not loaded, any element attempting to use it must render an invisible fallback font face. If the font face successfully loads during this period, it is used normally.

Font swap period
If the font face is not loaded, any element attempting to use it must render a fallback font face. If the font face successfully loads during this period, it is used normally.

Font failure period
If the font face is not loaded, the user agent treats it as a failed load causing normal font fallback

---

# font-display properties

auto
The font display strategy is defined by the user agent.

block
Gives the font face a short block period and an infinite swap period.

swap
Gives the font face an extremely small block period and an infinite swap period.

fallback
Gives the font face an extremely small block period and a short swap period.

optional
Gives the font face an extremely small block period and no swap period.

---

# font display diagram

Monica Dinculescu (google)

---

# Variable fonts

In 2016, an important development in typography was jointly announced by representatives from Adobe, Microsoft, Apple, and Google.

Version 1.8 of the OpenType font format introduced variable fonts.

A variable font is a collection of master styles, with one central 'default' master (usually the Regular font style) and multiple registered “axes” which tie the central master to the other masters. For example, the Weight axis might connect a Light style master to the default style and through to the Bold style master

---

# variable fonts CSS slide 3

If the browser supports variable fonts, SourceSansVariable.woff2 and SourceSansVariable-italic.woff2 will be downloaded and used. If not, SourceSans.woff2, SourceSans-bold.woff2 and SourceSans-italic.woff2 will be downloaded instead.

---

# variable fonts css properties

wght - Weight is controlled by the CSS font-weight property. The value can be anything from 1 to 999. This will allow for a more granular level of control.
wdth - Width is controlled by the CSS font-stretch property. It can take a keyword or a percentage value.
opsz - Optical sizing can be turned on or off using the new font-optical-sizing property. (slightly differing visual representations to optimize viewing at different sizes, or not
ital - Italicization is achieved by setting the CSS font-style property to italic
slnt- Slant is controlled by setting the CSS font-style property set to oblique

---




