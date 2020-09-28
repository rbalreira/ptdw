# Projeto Temático em Desenvolvimento Web
Projeto no âmbito do [Módulo Temático em Desenvolvimento Web](https://www.ua.pt/pt/uc/5156) da licenciatura em [Tecnologias da Informação](https://www.ua.pt/pt/curso/63) da [Universidade de Aveiro - Escola Superior de Tecnologia e Gestão de Águeda](https://www.ua.pt/pt/estga).

## Objetivo
Aplicação Web com o principal objetivo de possibilitar a introdução de valores a fim de calibrar os equipamentos. Os parâmetros a serem medidos pelos equipamentos são o batimento cardíaco (BC) e eletromiografia (EMG), pelo que serão estes os dados para a sua calibração. Desta forma, o utilizador insere os valores máximos e mínimos em ambos os critérios e caso o equipamento registe um valor que não esteja dentro da gama, este envia um alerta para a aplicação. Assim, podem-se indicar dois tipos de alerta: chamada – EMG, emergência – BC. A plataforma monitoriza os valores registados dos equipamentos, o que possibilita a análise dos dados em tempo real.

## Tecnologias
- [Microsoft Project](https://www.microsoft.com/pt-pt/microsoft-365/project/project-management-software)
- UML
- [Git](https://git-scm.com/)
- [Laravel](https://laravel.com/)
- HTML
- CSS
- JavaScript
- [jQuery](https://jquery.com/)
- PHP
- [Bootstrap](https://getbootstrap.com/)
- [PostgreSQL](https://www.postgresql.org/)

## Instalação
1. Criar uma base de dados no PostgreSQL, usando a linha de comandos ou um GUI ([pgAdmin](https://www.pgadmin.org/), [DBeaver](https://dbeaver.io/)...)
2. Alterar o role "[postgres]" do ficheiro de backup [database.sql](database.sql) para o role usado na base de dados criada no ponto anterior
3. Importar o ficheiro de backup da base de dados [database.sql](database.sql) para a base de dados criada no ponto 1.
4. Abrir a aplicação na framework Laravel
5. Alterar as credenciais de acesso do ficheiro [.env](app/.env) que faz conexão à base de dados
5. Executar os seguintes comandos:
```
composer install
php artisan key:generate
chmod -R ug+rwx storage bootstrap/cache
chown -R www-data:www-data vendor/
chmod -R 775 ./
chmod -R 777 storage/
chmod -R 777 bootstrap/
php artisan db:seed
php artisan serve
```

## Documentação
- [Relatório](report.pdf)
- [Enunciado](outline.pdf)

## Autores
- Diogo Santos
- Jorge Godinho
- Pedro Quinta
- Ricardo Balreira
- Tiago Silva
