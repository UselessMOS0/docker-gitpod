FROM nikolaik/python-nodejs
#Definisce la working directory del container
WORKDIR /app 

#Copia requirements.txt e installa le dipendenze
COPY requirements.txt ./
RUN npm install -g nodemon
RUN pip install --no-cache-dir -r requirements.txt

#Copia tutta la cartella server
COPY . .

#Espone la porta 5000
EXPOSE 5000

#Avvia il server python
CMD [ "nodemon", "--exec", "python3", "./app.py" ]