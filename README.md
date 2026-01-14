### Governance Archaeology Data Exploration

Dataset from [Governance Archaeology - Communities](https://airtable.com/appLmSaCALVZHYVLh/tbl4nk4lMDVFLwOTB/viwPIcevsTL6gADQS?blocks=hide)

### Setup

#### Fresh setup
- Clone repo
  ```zsh
  git clone https://github.com/metagov/governance-archaeology.git
  ```
- Check Python version: Python 3.13.5
  ```zsh
  python3 --version
  ```
- Python virtual environment:
  ```zsh
  python3 -m venv .venv
  source .venv/bin/activate
  ```
- Install requirements
  ```zsh
  pip install --upgrade pip setuptools wheel;
  pip install jupyter ipykernel;
  pip install -r requirements.txt
  ```
- Install kernel
  ```zsh
  python -m ipykernel install --user \
    --name governance-archaeology \
    --display-name "Governance Archaeology";
  ```
- Launch notebook:
  ```zsh
  jupyter notebook
  ```
  
#### New data:
- Download `Communities-Grid-view.csv`, `Institutions-Grid-view.csv` from Airtable, move into `data/` folder
- Update DATA_VERSION as needed 
- If needed, create a `{DATA_VERSION}_fig` folder with subfolders:
```zsh
# Replace {DATA_VERSION} e.g. DATA_VERSION=v5
export DATA_VERSION={DATA_VERSION}
```
```zsh
mkdir $DATA_VERSION"-fig"
mkdir $DATA_VERSION"-fig/fig-correlations/"
mkdir $DATA_VERSION"-fig/fig-correlations-no-eu/"
mkdir $DATA_VERSION"-fig/fig-communities"
mkdir $DATA_VERSION"-fig/fig-cgis/"
mkdir $DATA_VERSION"-fig/fig-cgis-no-eu/"
mkdir "csv/"$DATA_VERSION
```

#### Development
- Activate virtual environment
  ```zsh
  source .venv/bin/activate;
  jupyter notebook
  ```
- Check that the "Governance Archaeology" kernel is selected
