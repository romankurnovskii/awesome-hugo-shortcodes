## notebook

Embed a Jupyter notebook into a Hugo page.

## Path

{theme}/layouts/shortcodes/notebook.html

## Requirements

To generate notebook to `html` need [nbconvert](https://nbconvert.readthedocs.io/en/latest/).

```python
pip install nbconvert
```

## Parameters

- **notebook_name** (mandatory) - Name of the Jupyter notebook (without the .html extension).
- **iframe_height** - Height of the iframe in pixels. Adjust this value to display the entire notebook without cropping or enabling scrolling. Defaults to the height of the iframe if not provided.

## Usage

To use this shortcode, provide the name of your Jupyter notebook and, optionally, the desired height of the iframe:

```sh
# save in root static folder in dir jupyter
jupyter nbconvert --to html static/jupyter/my_notebook.ipynb
```

```markdown
{{< notebook my_notebook >}}
{{< notebook my_notebook 600 >}}
{{< notebook my_notebook 1200 >}}
```

```sh
jupyter nbconvert --to html static/my_notebook.ipynb
```

```markdown
{{< notebook "jupyter/my_notebook" >}}
{{< notebook "jupyter/my_notebook" 1200 >}}
```
