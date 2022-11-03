# SEAMOS UNO Donaciones

Aplicación web para de donaciones y sorteo para el sitio web seamos.com.ar

- [Argentina.gob.ar](https://www.argentina.gob.ar/salud/coronavirus-COVID-19) - Información, recomendaciones del Ministerio de Salud de la Nación y medidas de prevención.

- [who.int](https://www.who.int/es/emergencies/diseases/novel-coronavirus-2019) - En este sitio web se puede encontrar información y orientaciones de la OMS acerca del actual brote de enfermedad por coronavirus (COVID-19) que fue notificado por primera vez en Wuhan (China) el 31 de diciembre de 2019. En esta página figura información actualizada diariamente.

## Configuración Inicial

Estas instrucciones le permitirán obtener una copia del proyecto funcionando en su máquina local para desarrollo y testeo. Vea las notas de publicación para conocer como realizar su despliegue en un sistema productivo.

### Prerequisitos

Para ejecución local:

- npm o yarn
- node.js
- MongoDB

### Instalación para entorno DEV

- Clonar este repositorio y ejecutar npm

```zsh
npm -i
```

- Configurar variables de entorno, manualmente usando `SET` o generando un `.env` en la carpeta raiz del proyecto

```zsh
covid19_secret=
```

- Configurar el nombre de la base local en `config/development.json`

```json
{
  "host": "localhost",
  "dbName": "NOMBRE_DB"
}
```

- Iniciar MonboDB

```zsh
mongod
```

- Iniciar la aplicación

```zsh
npm run dev
```

- Testear conexión ejecutando únicamente el backend server

```zsh
npm run server
```

- Debe obtener un log similar al siguiente

```zsh
[DB] Connected to LOCAL MongoDB... db-test
```

- Si desea utilizar una instancia remota de mongo, debe dejar **vacio** el campo `dbName` de `config/development.json` y completar las siguientes variables de entorno

```zsh
covid19_secret=
DB_USER=
DB_PASS=
DB_HOST=
DB_NAME=
```

- Al iniciar nuevamente el backend server con `npm run server` obtendrá un output similar al siguiente

```zsh
[DB] Connected to REMOTE MongoDB... test-hospitales
```

- Una vez chequeada la conexión a la base de datos puede iniciar la aplicación

```zsh
npm run dev
```

## Running the tests

Explain how to run the automated tests for this system

### Break down into end to end tests

Explain what these tests test and why

```
Give an example
```

### And coding style tests

Explain what these tests test and why

```
Give an example
```

## Deployment

Add additional notes about how to deploy this on a live system

```zsh
covid19_secret=
DB_USER=
DB_PASS=
DB_HOST=
DB_NAME=
```

## Built With

- [Dropwizard](http://www.dropwizard.io/1.0.2/docs/) - The web framework used
- [Maven](https://maven.apache.org/) - Dependency Management
- [ROME](https://rometools.github.io/rome/) - Used to generate RSS Feeds

## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags).

## Authors

- **Billie Thompson** - _Initial work_ - [PurpleBooth](https://github.com/PurpleBooth)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

- Hat tip to anyone whose code was used
- Inspiration
- etc

##

"bcrypt": "^4.0.1",
# seamosuno
