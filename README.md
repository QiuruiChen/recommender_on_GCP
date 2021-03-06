# Build multitask recommenders on GCP

## Data Structure:
- user model(query model): using features: `userId` and `organization` 
- article model(candidate model): `contentId`
- mutlitask recommender: 
    - framework: tensorflow-recommender
    - predicting:
        1. predict time spend on pages
        2. predict article wachtes
    
### File Strcture:
- [serving](serving): CI/CD; kubflow; ai-platform; bigquery; tensorflow-recommenders
  
  <img src="assets/img.png" width="50%">
- [application](application): serving model predicting API with google app engine
  
    <img src="assets/img_1.png" width="40%">

- [streaming](streaming): dataflow; bigquery;
  
  <img src="assets/img_2.png" width="50%">
  
### Global environment:
Change below environment variables into your version:
- model name: `tfrs`
- model version: `mf`
- project name: `buddie-270710`
- region: `west-europe4`

### Source:
Modified from [here](https://github.com/GoogleCloudPlatform/training-data-analyst/tree/master/courses/machine_learning/deepdive2/building_production_ml_systems)