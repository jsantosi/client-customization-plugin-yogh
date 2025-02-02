# Client Customization Plugin-YOGH 🚀

Este é um plugin WordPress customizado criado para a Yogh - Especialista em WordPress.

## Descrição

Este plugin tinha o objetivo de inserir uma mensagem no final de todo o conteúdo do site (posts e páginas).

✔️ A tarefa consistiu em modificar o plugin para que a mensagem seja exibida apenas no final dos posts (artigos) e não mais nas páginas.

### 🗂️ Este repositório contém:

*   **`client-customization.php`**: O código fonte do plugin WordPress corrigido, com a mensagem aparecendo apenas nos posts.
*   **`documentation/technical.md`**: Documentação técnica com todos os detalhes da implementação, tempo gasto e referências.
*   **`documentation/non-technical.md`**: A documentação não-técnica, explicando o problema e a solução em uma linguagem acessível para o cliente.
*   **`README.md`**: Este arquivo, com informações sobre o repositório e como utilizá-lo.

## Código original

O código original do plugin, antes da correção, era o seguinte:
```php
<?php
/**
 * Plugin Name:     Client Customization
 * Plugin URI:https://www.yogh.com.br/
 * Description:     Plugins with Project Customization
 * Author:          Yogh Soluções
 * Author URI:      https://www.yogh.com.br/
 * Text Domain:     client-customization
 * Domain Path:     /languages
 * Version:         0.1.0
 *
 * @package         Client_Customization
 */

// If this file is called directly, abort.
if ( ! defined( 'ABSPATH' ) ) {
die( 'not allowed' );
}

add_filter('the_content', function ( $content ) {

$message = '<p><b>This content is created by: ' . get_bloginfo( 'name' ) . ' (' . get_bloginfo( 'url' ) . ')</b></p>';
return $content . $message;

}, 10 );
```

## ⚙️ Uso 

1.  Baixe o plugin do [repositório](https://link_do_seu_repositorio).
2.  Instale o plugin em seu WordPress.
3.  Verifique se a mensagem aparece apenas nos posts e não nas páginas.
