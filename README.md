# PIN 1 - Consigna

Objetivos:
Instalar docker
Lanzar un contenedor custom de Jenkins
Correr un pipeline con ciertas customizaciones
Crear una imagen y enviarla a nuestro registry propio
Scanear la imagen

## Instalando Docker, Custom Jenkins, Pipelines, Registry propio

### Instalando Docker last version en Ubuntu Server 24.04.1

```bash
# Add Docker's official GPG key:
sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

# Add the repository to Apt sources:
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
```

```bash
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```

### Jenkinks custom del repositorio de mundose

```bash
docker.io/mguazzardo/pipe-seg
```

### Estructura de Archivos para Docker Compose

/PIN1
│
├── docker-compose.yml
├── Dockerfile
├── index.js
├── Jenkinsfile.seg
├── package.json
├── package-lock.json
└── README.md
