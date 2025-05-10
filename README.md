
# Android APK Builder com Docker

Este repositório contém um **Dockerfile** para automatizar a construção de um APK Android usando Docker. O objetivo é gerar o APK de maneira rápida utilizando a imagem base do Docker.

## Como rodar

### 1. Construir a Imagem Docker

Para construir a imagem Docker, use o seguinte comando:

```bash  
docker build -t android-apk-builder .
```

Isso criará uma imagem chamada `android-apk-builder` com base no `Dockerfile` presente neste repositório.

### 2. Rodar o Container e Gerar o APK
```bash  
docker run --rm -v "${PWD}:/output" android-apk-builder cp /app.apk /output/
```

### 3. Localização do APK Gerado
Após a execução bem-sucedida do comando, você encontrará o APK  `app.apk` pronto para ser usado ou instalado em um dispositivo Android.