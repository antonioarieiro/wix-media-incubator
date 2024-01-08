# Wix Media PHP SDK

O Wix Media PHP SDK é uma interface de programação de aplicativos (API) que facilita o armazenamento, serviço, upload e gerenciamento de arquivos de imagem, oferecendo uma integração eficiente com a Wix Media Platform.

## Funcionalidades Básicas

- Armazenamento, serviço, upload e gerenciamento eficiente de arquivos de imagem.

## Componentes Adicionais

- **Serviços de Imagem**: APIs REST para manipulação on-the-fly de imagens hospedadas na Wix Media Platform.
- **SDKs**: Conjunto de bibliotecas para o lado do cliente e do servidor.

## Configuração e Uso

### Instalação

Instale o pacote `wixmedia-PHP` adicionando-o ao caminho de inclusão do seu projeto. Para usuários do Git, clone o repositório usando:

git clone git@github.com:wix/wixmedia-php.git


### Exemplo de Uso

#### Upload de Arquivos

```php
require($sdk_wix_midea_dir.'WixClient.php');

$client = new WixClient('YOUR_API_KEY', 'YOUR_API_SECRET');

if ($image = $client->uploadImage('test.jpg')) {
    echo "The image was successfully uploaded!\n";
    echo $image->getId();
} else {
    echo "An error occurred...\n";
    // Error handling
}
