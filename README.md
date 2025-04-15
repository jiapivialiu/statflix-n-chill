# Statflix & Chill

_“Low-energy? Low motivation? But still wanna feel a tiny bit productive as a stats student or researcher? This is for you.”_

Welcome to **Statflix & Chill** – your cozy corner of the internet where statistics and data science students can relax, recharge, and still learn *just a little bit*. This is a curated menu of fun, light, and creative activities that are **kinda stats-related**, **very low-effort**, and **totally guilt-free**.

---

## 🍿 What You’ll Find Here

- ☕ **Tiny LaTeX tasks** – like drawing a neural network with TikZ.
- ✍️ **Light learning prompts** – like exploring a new R package with just one plot.
- 🎨 **Creative projects** – like visualizing a dataset aesthetically.
- 🧪 **Play with tools** – try Quarto, RShiny, or Jupyter extensions just for fun.
- 🎧 **Watchables** – short vids or talks that feel more like entertainment.
- 🧘 **No-pressure ideas** – a space where it's OK to do “just one little thing.”

---

## 🧠 For Who?

- Stats / data science students and researchers
- People recovering from burnout / mid-semester slump
- Folks who love the field but not the pressure
- You, when you're thinking:  
  _“I could do *something*... but not, like, too much.”_

---

## 🧃How to Use

Pick a random idea. Do it. Or don’t. This repo is chill.  
Contributions welcome, especially if they’re fun, nerdy, or semi-productive in a cozy way 🧡

---

## What You Can Do?

### Idea 1: ☁️ Set Up a GitHub Repo with Daily Commits (for ✨Consistency Vibes✨)

**Why**: Make your contribution graph green daily, with zero effort!

**How**:
1. Create a new GitHub repo and name it `your-id-daily-checkin`.
2. Follow a prebuilt GitHub Action to auto-commit daily.
3. Sit back and enjoy your growing green graph.
4. Starter Kit:
  - 💚 [How to keep your GitHub contribution graph green](https://github.com/ryo-ma/github-profile-trophy/pull/29#issuecomment-1025371000)
  - Or just fork this ready-to-go repo: [`actions-js/push`](https://github.com/actions-js/push)

### Idea 2: ✒️ Use LaTeX to Draw a Neural Network

**Why**: It’s visual, satisfying, and kinda meditative.

**How**:
1. Open Overleaf or Quarto.
2. Use TikZ to sketch a tiny neural net (3-layer is enough).
3. Add colors if you’re feeling ✨extra✨.
4. Starter Kits:
  - 🧠 [LaTeX Neural Network with TikZ Example](https://tikz.net/neural_networks/)

### Idea 3: 📘 Add an Observable JavaScript Plot Inside a Quarto Document

**What**: Use a reactive JS cell in Quarto to show a cool plot.

**How**:
1. Install Quarto
2. Create a .qmd file
3. Add a JS cell using observable and paste this:

```{ojs}
import {Plot} from "@observablehq/plot"
Plot.plot({
  marks: [
    Plot.dotY([10, 20, 30, 40], {x: (d, i) => i})
  ]
})
```

📎 Guide: [Observable + Quarto](https://quarto.org/docs/interactive/ojs/index.html)

### Idea 4: 🎨 Make a Beautiful Table in R using `gt`

**What**: Turn a boring CSV into a slick, publish-ready table.

**How**:
```r
library(gt)
iris %>%
  head() %>%
  gt() %>%
  tab_header(title = "🌸 Pretty Table of Iris")
```

📎 Guide: [Get Started with GT](https://gt.rstudio.com/articles/gt.html)

### Idea 5: 📊 Animate a Plot in Python Using Plotly

**What**: Build a simple animated scatter plot.

**How**:

```python
import plotly.express as px
df = px.data.gapminder()
fig = px.scatter(df, x="gdpPercap", y="lifeExp", animation_frame="year",
                 size="pop", color="continent", log_x=True)
fig.show()
```

📎 More ideas: [Plotly Express Examples](https://plotly.com/python/plotly-express/)

### Idea 6: 🔍 Animate a Plot in R Using gganimate

**Why**: Small win, satisfying output.

**Ideas**:

1. Try `tidyverse`-style figure with Animation in R using `gganimate`.
2. Recreate a cool plot you’ve seen in an example.
3. Keep it aesthetic — add themes, minimal labels, nice color palettes.
4. Challenge:
  - Reimplement the animated figure [here](https://gganimate.com/index.html) on a dataset of your choice.

### Idea 7: ✨ Create an RShiny App that Does One Simple Thing

**What**: A slider that changes the mean of a histogram.

**How**:

```R
library(shiny)
ui <- fluidPage(
  sliderInput("mean", "Choose mean:", min = 0, max = 10, value = 5),
  plotOutput("hist")
)
server <- function(input, output) {
  output$hist <- renderPlot({
    hist(rnorm(100, mean = input$mean), main = paste("Mean:", input$mean))
  })
}
shinyApp(ui, server)
```

📎 Copy-paste into: [RStudio Cloud](https://posit.cloud)

### Idea 8: 📝 Build Your First Blog Post Using Quarto

**What**: A one-post site, hosted via GitHub Pages.

**How**:

```bash
quarto create-project blog
cd blog
quarto preview
```

📎 Full Guide: [Blogging with Quarto](https://quarto.org/docs/blog/)
🧁 Bonus challenge: Add [Callout blocks](https://quarto.org/docs/authoring/callouts.html) for fun side notes.

### Idea 9: 🪩 Copy Someone's GitHub Profile You Like (Then Personalize It)

**What**: Make your profile page feel like you.

**How**:
1. Create your GitHub repository that shares the same name as your User ID.
2. Or generate your profile using an [auto-generator](https://github.com/rahuldkjain/github-profile-readme-generator).
3. Paste into README.md of a repo named exactly like your GitHub username
4. 🎨 Add icons from SimpleIcons or shields from [Shields.io](https://shields.io).


### Idea 10: 🎮 Play With an AI Model on HuggingFace — No Code Needed

**What**: Try a model like text classification or voice cloning.

**How**:
1. Go to [Hugging Face Spaces](https://huggingface.co/spaces).
2. Search: "text summarizer", "GPT-2", or "dreambooth".
3. Click around. Try entering your own text.


### Idea 11: `leaflet` in R for maps

Optional Challenge:
  * Plot your city using [Basemaps](https://rstudio.github.io/leaflet/articles/basemaps.html).

### Idea 12: Git Basics: Understanding merge vs rebase

**What**: Learn the difference between git merge and git rebase so you can manage branches with confidence.

**How**:
1. Understand the Purpose: Both are used to combine changes from one branch into another, but they handle history differently..
2. `git merge` — Combine with history.
3. `git rebase` — Linearize history.
4. Know When to Use.
    - Use merge if...
      - You’re working with a team.
      - You want to preserve the full history.
      - Avoid rewriting commits.
    - Use rebase if...
  	  - You're cleaning up local history.
      - You want a simple, linear history.
      - Comfortable handling conflicts.

Suggested reading: [Merging vs. rebasing](https://www.atlassian.com/git/tutorials/merging-vs-rebasing)

✅ Bonus Tip: Never rebase shared branches (like `main`) that others might be using!


***More fun is coming soon!***

**Want to contribute some fun ideas? Fork this repository and create a Pull Request to it!**
