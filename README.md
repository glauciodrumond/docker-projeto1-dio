# DEVOPS EXPERIENCE CARREFOUR - DIO
## Docker Projeto 1

Neste projeto foi utilizado o Docker Compose para executar uma aplicação HTML em um Container Apache.

Para realizar o projeto usei uma EC2 instance AWS

### Passo a passo

1. Criar um diretório root [nome do projeto]
2. Acessar este diretório
3.  Criar arquivo *compose.yml*

```yaml
version: "3.9"
service:
	apache:
		image: httpd:latest
		container_name: gd_apache_app
		ports:
		- "80:80"
		volumes:
		- .website:/usr/local/apache2/htdocs
```

1. Criar novo diretório dentro do diretório do projeto com o nome dado ao volumes no arquivo yml **[website]**
2. Acessar diretório website
3. Criar arquivo index.html

```html
<html>
	<head>
		<h1> MEU PROJETO DOCKER!!!</h1>
    <h2> BY GLAUCIO DRUMOND</h2>
	</head>
	<body>
		<div class="header">
			<div class="container">
				<h1> Criando um container de uma aplicacao WEB</h1>
				<div>Cloud DevOps Experience - Banco Carrefour - DIO</div>
			</div>
		</div>	
	</body>
</html>
```

1. Voltar ao diretório do projeto
2. Instalar o docker compose

```bash
apt-get install -y docker-compose
```

1. Gerar o arquivo

```bash
docker-compose up -d
```

![Screen Shot 2022-11-09 at 4.45.21 PM.png](Docker%20Projeto%201%2012f53fc3e50e40d69a49c41b842ad73c/Screen_Shot_2022-11-09_at_4.45.21_PM.png)

### Resultado

![Screen Shot 2022-11-09 at 5.11.07 PM.png](Docker%20Projeto%201%2012f53fc3e50e40d69a49c41b842ad73c/Screen_Shot_2022-11-09_at_5.11.07_PM.png)
