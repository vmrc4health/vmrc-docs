# Using the Portal Client

This guide follows instructions for [portal client pre-requisites](portal_client_prereqs.md) and provides instructions to set up and launch portal client

---

## Steps to access portal client repository:
### 1. Get the source code
Get the source code for portal-client v1.5.3 from https://github.com/IGS/portal_client/archive/refs/tags/v1.5.3.tar.gz
### 2. Untar the source code
In your terminal, go to the directory where source code is downloaded and untar the source code
```bash
tar -xf portal_client-1.5.3.tar.gz 
```
### 3. Create a virtual environment
You can provide a path to create an environment in the portal client directory
```bash
cd portal_client-1.5.3
python3 -m venv </path/to/env>     #For example, python3 -m venv env1
```
### 4. Activate the virtual environment
Use the same path that you used in previous command
```bash
source /path/to/env/bin/activate
```
### 5. Install the portal-client into the virtual environment
```bash
pip3 install .
```
This will retrieve and install the dependencies as well.
### 6. Verify
```bash
which portal-client
```

---

## Steps to set VMRC project:
### 1. Ensure correct project id is selected
```bash
gcloud config set project vmrc-462716
```

---

## Steps to launch portal client:
### 1. For users accessing files from Google buckets:
```bash
portal-client --manifest /path/to/my/manifest.tsv \
                --google-project-id vmrc-462716 \
                --endpoint-priority GS,HTTP
```
> **Note:** To disable checksum validation, use option `--disable-validation` along with the previous command. To provide a path to download files, use option `--destination` <path/to/output/directory>.

## You're set
To download a manifest, follow instructions to [browse portal](browse_portal.md)
