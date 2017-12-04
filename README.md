# gcp

Sign Up for the Free Trial and Create a Project
```
#https://codelabs.developers.google.com/codelabs/cpb100-free-trial/
#https://console.developers.google.com/freetrial
```
Start Compute Engine instance
```
# https://codelabs.developers.google.com/codelabs/cpb100-compute-engine/
```
Create SSH Key 
```
#https://cloud.google.com/compute/docs/instances/adding-removing-ssh-keys
ssh-keygen -t rsa -f ~/.ssh/[KEY_FILENAME] -C [USERNAME]
```
Connect using SSH key
```
ssh -i [PATH_TO_PRIVATE_KEY] [USERNAME]@[EXTERNAL_IP_ADDRESS]
```
Clone and process data
```
git clone https://github.com/GoogleCloudPlatform/training-data-analyst
cd training-data-analyst/CPB100/lab2b
less ingest.sh
bash ingest.sh
head earthquakes.csv
# check out for addinional information https://github.com/GoogleCloudPlatform/datalab-samples/blob/master/basemap/earthquakes.ipynb
less bash install_missing.sh
bash bash install_missing.sh
python transform.py
ls -l
gsutil cp earthquakes.* gs://<YOUR-BUCKET>/
# share for public
```

```
