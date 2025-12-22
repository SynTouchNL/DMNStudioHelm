
# Publishing chart
TODO: Move to pipeline (Something like https://gist.github.com/joaomlneto/b3970c9f022f231c2bbf644a780ebe12)
For now:
```
helm package .
helm repo index .
git commit ....
```

# Using chart:
helm repo add dmnstudio 'https://raw.githubusercontent.com/SynTouchNL/DMNStudioHelm/main'
helm repo update
helm search repo dmnstudio/dmnstudio


