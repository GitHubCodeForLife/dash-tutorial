This folder intended to divide the views into different files.

1. Components

- Using bootstrap or html, dcc
  from dash import dcc, html
  import dash_bootstrap_components as dbc
- Naming convention:
  - [Dash]\_[ComponenentName]
- CSS, Java Script: write your own CSS and JavaScript in assets folder.

2. Callbacks
   Ideas: start from extract function

- Allow to callbacks from other files.

```
from dash import Input, Output

class Demo:
    def __init__(self, app):
        self.app = app

        @app.callback(
            Output(component_id='my-output', component_property='children'),
            Input(component_id='my-input', component_property='value')
        )
        def update_output_div(input_value):
            return f'Output: {input_value}'
```
