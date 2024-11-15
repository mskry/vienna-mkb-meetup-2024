# <span style="background-image: linear-gradient(to bottom, #ed2939 0%, #ed2939 33%, #ffffff 33%, #ffffff 67%, #ed2939 67%, #ed2939 100%); -webkit-background-clip: text; background-clip: text; color: transparent;">Imported Slides</span>

You can split your slides.md into multiple files and organize them as you want using the `src` attribute.

#### `slides.md`

```markdown
# Page 1

Page 2 from main entry.

---

## src: ./subpage.md
```

<br>

#### `subpage.md`

```markdown
# Page 2

Page 2 from another file.
```

[Learn more](https://sli.dev/guide/syntax.html#importing-slides)
