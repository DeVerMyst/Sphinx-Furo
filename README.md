uv add --dev furo
uv add myst_parser
uv add sphinxcontrib-bibtex

mkdir docs
uv run sphinx-quickstart
cd ..

uv run sphinx-build -b html docs/source public

conf.py
# docs/source/conf.py

html_theme = "furo"

# Optionnel : Personnaliser la couleur ou le logo pour Furo
html_theme_options = {
    "light_css_variables": {
        "color-brand-primary": "#7C4DFF",
        "color-brand-content": "#7C4DFF",
    },
}