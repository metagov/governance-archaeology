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
  Optional: Install kernel
  ```zsh
  python -m ipykernel install --user \
    --name governance-archaeology \
    --display-name "Governance Archaeology";
  ```
- Launch notebook:
  ```zsh
  jupyter lab
  ```
  
#### New data:
- Download `Communities-Grid-view.csv`, `Institutions-Grid-view.csv` from Airtable, move into `data/` folder
- Update DATA_VERSION as needed 

#### Development
- Activate virtual environment
  ```zsh
  source .venv/bin/activate;
  jupyter lab
  ```
