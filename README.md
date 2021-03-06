# uit-bodo-ml-workshop

Sample code for a workshop on simple ML on health data for students at UiT Bodø.
I'm live coding the workshop, but have to have my notes somewhere. The
`tidyverse`, `tidymodels` and `plumber` are just awesome pieces of software.

# Workshop in brief (live-coding this part)

- Set up a workspace on [rstudio.cloud](http://rstudio.cloud)
- Download the [Pima Indians Diabetes Database dataset](https://www.kaggle.com/uciml/pima-indians-diabetes-database)
  from Kaggle. You'll get something like [data/diabetes.csv](data/diabetes.csv).
- Create some sort of model. Take a look at [analysis.R](analysis.R) for a
  logistic regression model, aka peak ML.
- Create a [plumber](https://www.rplumber.io/) API for your model, and run it!
  See [diabetes-prediction/diabetes-prediction.R](/diabetes-prediction/plumber.R)
- Dockerize it with `docker build -t api .` and `docker run -p 8000:8000 -t api`, 
  and open [http://localhost:8000](http://localhost:8000).  
- Over-engineer and deploy to Azure Kubernetes with `kubectl apply -f azure-diabetes-predictor.yaml`
- Write an app? Maybe with [Svelte](https://svelte.dev/) since I haven't done
  that before. See [svelte-app/](svelte-app) for more on that.
