---
title: Criando Pacotes Personalizados
category: Pacotes e Conjuntos de Recursos
order: 21
permalink: criando-pacotes-personalizados.html
---

* 
{:toc}

# Pacotes Personalizados

O Gerenciador de Pacotes da Unity é o sistema oficial de gerenciamento de pacotes para a Unity. Ele realiza o seguinte:

* Permite que a Unity distribua novos recursos e atualize recursos existentes de forma rápida e fácil.
* Fornece uma plataforma para os usuários descobrirem e compartilharem componentes reutilizáveis.
* Promove a Unity como uma plataforma extensível e aberta.

Você pode usar o Gerenciador de Pacotes para definir as dependências do projeto, resolver as dependências dos pacotes, baixar pacotes, adicionar pacotes e integrar conteúdo em seus projetos.

Para informações gerais sobre o que é um pacote e como o Gerenciador de Pacotes da Unity funciona, consulte a documentação sobre [Pacotes]().

## Visão Geral

Os pacotes podem conter o seguinte:

* Scripts em C#
* Assemblies
* Plug-ins nativos
* Modelos, Texturas, animações, clipes de áudio e outros ativos.

**Observação**: O Gerenciador de Pacotes não oferece suporte a ativos de streaming em pacotes. Use o pacote [Addressables]() em vez disso.

Cada pacote também contém um arquivo [Manifesto de Pacote]() que inclui informações como o nome do pacote, sua versão, uma lista de suas dependências e a URL para seu repositório.

## Procedimento

Para criar um novo pacote:

1. Crie uma estrutura vazia para o pacote usando um destes métodos:

    * [Configure um pacote incorporado]().
    * [Configure um pacote local]().

2. Certifique-se de que o layout da sua estrutura de pastas segue a [convenção de layout de pacotes]() da Unity. Por exemplo, se você tiver bibliotecas de Editor e em tempo de execução, certifique-se de armazená-las nas pastas `Editor` e `Runtime`.

3. Se o seu pacote incluir código, certifique-se de que o layout do pacote que você criou contenha os arquivos de definição de montagem necessários. Para obter informações sobre como criar e definir arquivos de definição de montagem, consulte [Definição de montagem e pacotes](). Para informações adicionais, consulte [Definições de Montagem]().

    **Observação**: Se a **janela do console** relatar um aviso após adicionar um arquivo de definição de montagem, salve o seu projeto, feche-o e depois o reabra.

4. Adicione suas ferramentas, bibliotecas e todos os ativos necessários para o seu pacote.

5. Adicione [testes]() ao seu pacote. Os testes são essenciais para garantir que o pacote funcione conforme o esperado em diferentes cenários:

    * Escreva todos os seus Testes de Editor em `Tests/Editor`.
    * Escreva todos os seus Testes de Modo de Reprodução em `Tests/Runtime`.

6. Se você tiver amostras para o seu pacote, adicione-as à [subpasta apropriada de amostras.]()

    **Observação**: Os pacotes podem conter apenas amostras, mas você também pode incluir amostras como parte de um pacote de ferramentas ou modelo usando o mesmo layout e estrutura JSON.

7. Você pode atualizar o arquivo `CHANGELOG.md` toda vez que publicar uma nova versão. Cada novo recurso ou correção de bug deve ter um rastreamento neste arquivo. Para mais detalhes sobre o formato de changelog escolhido, consulte a documentação [Keep a Changelog](). Esta etapa é opcional para pacotes que você não compartilha, mas é altamente recomendada para pacotes compartilhados, para que os usuários saibam qual versão melhor atende às suas necessidades.

    **Dica**: Você pode fornecer um link para uma página web externa onde hospeda o changelog deste pacote, definindo a propriedade [changelogUrl]() no arquivo manifesto `package.json` do seu pacote.

8. Você pode [incluir licenças e avisos de terceiros]() nos arquivos `LICENSE.md` e `THIRD PARTY NOTICES.md`. Esta etapa é opcional para pacotes que você não compartilha, mas é altamente recomendada para pacotes compartilhados, para que seus usuários não utilizem inadequadamente seus pacotes ou violem licenças de terceiros.
    **Dica**: Você pode fornecer um link para uma página web externa onde hospeda as licenças e avisos de terceiros deste pacote, definindo a propriedade [licensesUrl]() no arquivo manifesto `package.json` do seu pacote.

9. Documente o seu pacote.
    **Dica**: Você pode fornecer um link para uma página web externa onde hospeda a documentação deste pacote, definindo a propriedade [documentationUrl]() no arquivo manifesto `package.json` do seu pacote.

10. Compartilhe o seu pacote.

## Criando um Novo Pacote Incorporado

Siga estas instruções se deseja criar um pacote personalizado [dentro da pasta do seu projeto]().

**Observação**: Essas instruções fazem parte do procedimento maior para a [criação de pacotes personalizados]().

1. Abra o Unity Hub e crie um projeto vazio em seu computador. Você também pode usar um projeto existente em seu computador e [incorporar o pacote em seu projeto]() ou [instalar o pacote a partir de uma pasta local](). No entanto, começar com um novo projeto torna o conteúdo do pacote menos propenso a erros.

2. Usando o gerenciador de arquivos do seu computador (por exemplo, o Windows File Explorer ou o macOS Finder), navegue até a pasta do seu projeto e localize o subdiretório `Packages`.

3. Crie um novo subdiretório para o seu pacote dentro da pasta `Packages` usando um nome que corresponda ao [nome do pacote]() e siga as [convenções de nomenclatura](). Por exemplo, se o nome do seu pacote for `com.example.mypackage`, crie um subdiretório chamado `com.example.mypackage`.

    **Observação**: Isso é particularmente importante se o seu pacote contiver ativos, porque o [AssetDatabase procura um caminho de ativo]() que corresponda a `Packages/<nome-do-seu-pacote>/Assets`, independentemente do nome real da pasta.

4. Abra o seu editor de texto preferido e crie um arquivo JSON chamado `package.json` na raiz da pasta do pacote.

5. Preencha todos os [campos obrigatórios e recomendados]() no arquivo `package.json`. Você pode usar o [exemplo de manifesto de pacote]() como referência.

Quando você reabrir o Unity, o novo pacote aparecerá na janela do [Gerenciador de Pacotes e na janela do Projeto](), onde você pode visualizar e modificar o conteúdo do pacote. Se você selecionar o arquivo `package.json` na janela do Projeto, também poderá modificar seus valores JSON diretamente no **Inspector**.

Volte ao [procedimento principal]() para concluir a criação do seu pacote.  

## Criando um Novo Pacote Local

Siga estas instruções se deseja criar um pacote personalizado fora da pasta do seu projeto.

**Observação**: Essas instruções fazem parte do procedimento maior para a [criação de pacotes personalizados]().

1. Usando o gerenciador de arquivos do seu computador (por exemplo, o Windows File Explorer ou o macOS Finder), crie uma pasta para o seu pacote. Você também pode usar um local existente se já tiver criado algum conteúdo para o seu pacote.

2. Abra o seu editor de texto preferido e crie um arquivo JSON chamado `package.json` na raiz da pasta do pacote.

3. Preencha todos os [campos obrigatórios e recomendados]() no arquivo `package.json`, garantindo que a propriedade `name` siga as [convenções de nomenclatura](). Você pode usar o [exemplo de manifesto de pacote]() como referência.

4. No Unity, crie um novo projeto ou abra um projeto existente.

5. Abra a janela do [Gerenciador de Pacotes]() e siga as instruções para [instalar um pacote local](), usando o arquivo `package.json` que você acabou de criar.

O novo pacote aparece na janela do Gerenciador de Pacotes e na janela do Projeto, onde você pode visualizar e modificar o conteúdo do pacote. Se você selecionar o arquivo `package.json` na janela do Projeto, também poderá modificar seus valores JSON diretamente na janela do Inspector.

Volte ao [procedimento principal]() para concluir a criação do seu pacote.