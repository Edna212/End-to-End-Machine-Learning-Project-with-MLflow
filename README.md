# End-to-End Machine Learning Project with MLFlow

## Workflows

1. Update `config.yaml`
2. Update `schema.yaml`
3. Update `params.yaml`
4. Update the entity
5. Update the configuration manager in `src/config`
6. Update the components
7. Update the pipeline
8. Update `main.py`
9. Update `app.py`

---

## How to Run Locally

### Step 1: Clone the repository

```bash
git clone https://github.com/Edna212/End-to-End-Machine-Learning-Project-with-MLflow
cd End-to-End-Machine-Learning-Project-with-MLflow
```

### Step 2: Create and activate conda environment

```bash
conda create -n mlproj python=3.10 -y
conda activate mlproj
```

### Step 3: Install dependencies

```bash
pip install -r requirements.txt
```

### Step 4: Run the app

```bash
python app.py
```

Open your browser at:

```
http://localhost:8080
```

---

## Run with Docker (Recommended)

1. **Build Docker image:**

```bash
docker build -t ml-app .
```

2. **Run Docker container:**

```bash
docker run -d -p 5000:8080 ml-app
```

* `5000` → local machine port
* `8080` → container port inside Docker

3. **Open the app in browser:**

```
http://localhost:5000
```

4. **Optional Docker commands:**

```bash
docker ps                    # check running containers
docker logs <container_id>   # view container logs
docker stop <container_id>   # stop container
```

---

## MLflow

[MLflow Documentation](https://mlflow.org/docs/latest/index.html)

### Run MLflow UI locally

```bash
mlflow ui
```

### DagsHub Integration

Set environment variables:

```bash
export MLFLOW_TRACKING_URI=https://dagshub.com/Edna212/End-to-end-Machine-Learning-Project-with-MLflow.mlflow
export MLFLOW_TRACKING_USERNAME=Edna212
export MLFLOW_TRACKING_PASSWORD=f547b1e7a51efb2449d21d646343d75ebca1aa26
```

Then run:

```bash
python script.py
```

---

✅ Now your project can run **locally** or via **Docker**, making it fully reproducible and portfolio-ready.
