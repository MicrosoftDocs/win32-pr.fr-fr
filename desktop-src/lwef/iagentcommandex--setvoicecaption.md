---
title: IAgentCommandEx SetVoiceCaption
description: IAgentCommandEx SetVoiceCaption
ms.assetid: 672fdc13-25d3-4ced-b295-2b687767c17f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe76edb17c2b099db5e16e2b6160703c6b11e8a9f52bcbc24a9ca4bfcb7077c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477212"
---
# <a name="iagentcommandexsetvoicecaption"></a>IAgentCommandEx::SetVoiceCaption

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT SetVoiceCaption(
   BSTR bszVoiceCaption  // voice caption text
);
```

Définit le texte [**VoiceCaption**](voicecaption-property.md) affiché pour une [**commande**](/windows/desktop/lwef/the-command-object).

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszVoiceCaption*
</dt> <dd>

BSTR qui spécifie le texte de la propriété [**VoiceCaption**](voicecaption-property.md) pour une [**commande**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

Si vous définissez un objet de [**commande**](/windows/desktop/lwef/the-command-object) dans une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) et que vous définissez sa propriété [**Voice**](voice-property.md) , vous définissez en général également sa propriété [**VoiceCaption**](voicecaption-property.md) . Ce texte s’affiche dans la fenêtre commandes vocales lorsque votre application cliente est entrée active. Si cette propriété n’est pas définie, le paramètre de la propriété [**Caption**](caption-property.md) détermine le texte affiché. Lorsque ni la propriété **VoiceCaption** ni la propriété n’est définie, la commande n’apparaît pas dans la fenêtre commandes vocales.

[**Caption**](caption-property.md)

## <a name="see-also"></a>Voir aussi

[**IAgentCommand :: GetCaption**](iagentcommand--getcaption.md), [**IAgentCommand :: SetEnabled**](iagentcommand--setenabled.md), [**IAgentCommand :: setVisible**](iagentcommand--setvisible.md), [**IAgentCommand :: SetVoice**](iagentcommand--setvoice.md), [**IAgentCommandsEx :: Addex**](iagentcommandsex--addex.md), [**IAgentCommandsEx :: InsertEx**](iagentcommandsex--insertex.md), [**IAgentCommands :: Add**](iagentcommands--add.md), [**IAgentCommands :: Insert**](iagentcommands--insert.md)


 

 