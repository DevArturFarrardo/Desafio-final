# Usar uma imagem base oficial do Python
FROM python:3.9-slim

# Evitar criação de .pyc e garantir logs “flushados”
ENV PYTHONDONTWRITEBYTECODE=1 \
    PYTHONUNBUFFERED=1

# Definir o diretório de trabalho
WORKDIR /app

# Copiar e instalar dependências
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Copiar os arquivos da API para o container
COPY . .

# Expor a porta 1313
EXPOSE 1313

# Comando para rodar a aplicação
CMD ["python", "app.py"]