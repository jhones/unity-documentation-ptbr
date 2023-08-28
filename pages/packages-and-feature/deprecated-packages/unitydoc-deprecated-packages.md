---
title: Pacotes Obsoletos
category: Pacotes e Conjuntos de Recursos
order: 18
permalink: pacotes-obsoletos.html
---

Pacotes que atingem o fim de sua vida útil não são mais suportados nos Editores Unity onde são rotulados como obsoletos. Você não deve usar pacotes obsoletos, pois eles podem estar não funcionais ou inseguros para uso.

Existem dois rótulos de obsolescência para distinguir duas variantes:

| Variante de Obsolescência | Rótulo | Descrição |
|-------|--------|--------|
| Obsolescência no Ciclo de Vida de Pacotes da Unity | ![](https://jhones.github.io/unity-documentation-ptbr/assets/libdoc/img/iconDeprecated-yellow.png) | Este rótulo identifica um pacote que não está mais em desenvolvimento para essa versão do Unity Editor. A Unity não oferecerá mais suporte para pacotes que atingirem este estado. |
| Obsolescência de Versão do Pacote | ![](https://jhones.github.io/unity-documentation-ptbr/assets/libdoc/img/iconDeprecated-red.png) | Este rótulo identifica uma versão específica do pacote que está obsoleta. A Unity normalmente aplica essa designação quando descobrem um problema crítico em uma versão específica de um pacote que ainda não atingiu o fim de sua vida útil. Autores de pacotes personalizados também podem aplicar essa designação com base em seu próprio processo de obsolescência. |

Se o seu projeto possui pacotes obsoletos de qualquer uma das variantes, o Editor exibe a seguinte mensagem quando você abre o seu projeto:

![Caixa de Diálogo para Pacotes Obsoletos](https://jhones.github.io/unity-documentation-ptbr/assets/libdoc/img/upm-ui-deprecated.png)

Se você abrir o Gerenciador de Pacotes quando esta mensagem for exibida, a janela do Gerenciador de Pacotes será carregada com o pacote obsoleto exibido. Neste ponto, você pode:

* Remover um pacote que atingiu a obsolescência no ciclo de vida. Embora você possa ser capaz de instalar uma versão diferente do pacote, o estado de obsolescência ainda se aplica. Considere encontrar outro pacote para usar no lugar deste pacote obsoleto.
* Remover um pacote cuja versão específica está obsoleta. Procure outra versão do mesmo pacote que seja compatível com o seu Editor, mas que não seja obsoleta.

## Recursos adicionais

[Estados e ciclo de vida dos pacotes]()