---
title: Pacotes Experimentais
category: Pacotes e Conjuntos de Recursos
order: 16
permalink: pacotes-experimentais.html
---

Pacotes experimentais são novos pacotes ou modificações experimentais feitas em pacotes maduros. A Unity não oferece suporte a pacotes experimentais porque eles estão nas fases iniciais de desenvolvimento.

Observação: Antes da versão do Unity Editor 2021.1, o Gerenciador de Pacotes usava o estado 'Visualização' para descrever pacotes que eram experimentais ou arriscados, mas de outra forma maduros. O Gerenciador de Pacotes usava o estado 'Visualização' para descrever pacotes que ainda não haviam sido completamente validados como seguros para uso em produção. A partir de 2021.1, o estado 'Visualização' não existe mais, e os pacotes podem ser 'Experimentais' ou 'De Pré-lançamento'. Isso proporciona uma distinção mais clara entre pacotes que são maduros, mas arriscados para uso, e pacotes que estão quase completamente maduros.

Pacotes experimentais podem passar por muitas mudanças antes de estarem prontos para o lançamento em uma versão específica da Unity. Em algum momento no futuro, eles podem atender aos requisitos de verificação, mas também podem ser descontinuados. Como não há garantia de suporte futuro, você não deve usar pacotes experimentais em produção.

Pacotes no estado experimental geralmente não aparecem no contexto do Registro da Unity no Gerenciador de Pacotes, embora estejam no servidor oficial de registro de pacotes da Unity. Esses pacotes não são visíveis na janela do Gerenciador de Pacotes porque:

* São muito arriscados para uso em produção. Alguns desses pacotes exigem muito treinamento e expertise e são recomendados apenas em circunstâncias específicas.
* Eles fornecem funcionalidade compartilhada ou adicional a pacotes existentes. Você não deve usá-los por conta própria, pois são apenas pacotes de 'suporte'.

Pacotes experimentais que não são visíveis ainda podem aparecer na janela do Gerenciador de Pacotes se você já os instalou em seu projeto ou os instalou como dependências de pacotes suportados. No entanto, eles são ocultados para que você não os descubra por acidente e os use sem perceber os riscos. Se eles aparecerem no Editor, eles sempre são marcados com o rótulo ![](https://jhones.github.io/unity-documentation-ptbr/assets/libdoc/img/iconExperimental.png) e o seguinte menu aparece como um aviso no Editor:

![O menu 'Pacotes Experimentais em Uso' aparece como um aviso na barra de ferramentas](https://jhones.github.io/unity-documentation-ptbr/assets/libdoc/img/upm-lifecycle.png)

Você pode abrir o menu **Pacotes Experimentais em Uso** e selecionar **Ignorar** se você não desejar ver este aviso para este projeto. Você também pode abrir o menu e selecionar 'Mostrar Pacotes Experimentais' para abrir o Gerenciador de Pacotes com uma lista filtrada dos pacotes experimentais em seu projeto.

Para ver uma lista de pacotes estáveis verificados para este lançamento, consulte Pacotes lançados.

Para obter mais informações sobre os estados de pacotes, consulte Estados e ciclo de vida dos pacotes.
