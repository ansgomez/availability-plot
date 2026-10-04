# availability-plot

> **Status:** experimental / superseded. This was a short-lived attempt (March 2022)
> to deploy an interactive availability plot as a Voila notebook on Heroku. Heroku's
> free tier no longer exists, and the Plotly Dash version in
> [availability-graph](https://github.com/ansgomez/availability-graph) is the
> maintained variant.

`availability.ipynb` plots the availability of a two-state repairable system,
A(t) = mu/(lambda+mu) + lambda/(lambda+mu) * exp(-(lambda+mu) t), with interactive
sliders for mu and lambda (matplotlib + ipywidgets).

## Run locally

```bash
python -m venv .venv && . .venv/bin/activate
pip install numpy matplotlib ipywidgets ipympl voila
voila availability.ipynb
```

Note: `requirements.txt` still lists unused packages left over from the Heroku
experiments (SQLAlchemy, WTForms, Flask-Babel, celery, ...).
