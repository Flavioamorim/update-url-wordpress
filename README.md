# update-url-wordpress
simple update for urls wordpress

Este procedimento é utilizando na maioria das vezes quando vamos publicar um site local para o servidor online.

1. Faça backup do banco de dados MySQL do servidor atual.

2. Importe os dados do banco de dos para o novo Servidor.

3. Rode a consulta SQL para fazer a alteração dos links.

## Use example
```
UPDATE wp_options SET option_value = replace(option_value, “http://enderecoatual“, “http://novoendereco“) WHERE option_name = “home” OR option_name = “siteurl”;

UPDATE wp_posts SET guid = replace(guid, “http://enderecoatual“,“http://novoendereco“);

UPDATE wp_posts SET post_content = replace(post_content,“http://enderecoatual“,”http://novoendereco“);

Observação: acesse a área administrativa do wordpress, vá em permalinks e verifique se a as URLs já foram alteradas corretamente.
```
