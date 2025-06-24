## Testing-ChromaDB

## Introduction:

ChromaDB is a modern database specially built to help applications understand and store AI-generated knowledge, like text, images, or documents — so that we can search them efficiently using meanings, not just keywords.
 
## what is ChromaDB?

ChromaDB is an open-source vector database designed to store and retrieve information using embeddings — numerical representations of data created by AI models.

#### Stores embeddings (vectors) of:

- Text

- Documents

- Code

- Images (indirectly)

- Provides semantic search: search based on meaning/similarity.

### Installation process of ChromaDB ?

#### Prerequisites:

1.EC2-Instance with Docker install in it.
2.Instance type : t3.small and 2GB of memory  
3.Ubuntu OS (latest version )
4.Installing Python3 

### Step1 : Installing Docker

Installing Docker on an EC2 Ubuntu VM involves a series of steps. Here's a simplified guide to get Docker installed:

### Update Your System:

Before installing Docker, update the package database with the command:
```
sudo apt-get update
```
Install the necessary packages that allow apt to use a repository over HTTPS:
```
sudo apt-get install apt-transport-https ca-certificates curl gnupg lsb-release
```
### Add Docker’s Official GPG Key:
Next, add the GPG key for the official Docker repository to your system:
```
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
```
### Add Docker Repository:

#### Add the Docker repository to APT sources:
```
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```
### Update the Package Database with Docker Packages:

Update the package database with the Docker packages from the newly added repo:
```
sudo apt-get update
```
### Install Docker CE:

Now you can install Docker:
```
sudo apt-get install docker-ce docker-ce-cli containerd.io
```
#### Verify Installation:

Check the Docker version to ensure the installation was successful:
```
docker --version
```
### Now pull the docker image from the docker rigistry 
Pull and Run Docker Image

```
docker pull chromadb/chroma
```
### Now run the container

```
docker run -d -p 8000:8000 chromadb/chroma
```












 
