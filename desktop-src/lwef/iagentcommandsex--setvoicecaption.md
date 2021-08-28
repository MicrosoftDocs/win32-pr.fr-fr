---
title: IAgentCommandsEx SetVoiceCaption
description: IAgentCommandsEx SetVoiceCaption
ms.assetid: f13c9ca5-70c9-42d0-b53c-45dc8980a24c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85de69b4b594f93adfb0ff554819243c94986420a79c35e8d7a64a3c2eaccb6f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119716139"
---
# <a name="iagentcommandsexsetvoicecaption"></a>IAgentCommandsEx::SetVoiceCaption

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT SetVoiceCaption(
   BSTR bszVoiceCaption  // voice caption text
);
```

Définit le texte [**VoiceCaption**](voicecaption-property.md) affiché pour l’objet de [**commande**](/windows/desktop/lwef/the-command-object) .

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszVoiceCaption*
</dt> <dd>

BSTR qui spécifie le texte de la propriété [**VoiceCaption**](voicecaption-property.md) pour une [**commande**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

Si vous définissez un objet de [**commande**](/windows/desktop/lwef/the-command-object) dans une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) et que vous définissez sa propriété [**Voice**](voice-property.md) , vous définissez en général également sa propriété [**VoiceCaption**](voicecaption-property.md) . Ce texte s’affiche dans la fenêtre commandes vocales lorsque votre application cliente est en entrée-active et que le caractère est visible. Si cette propriété n’est pas définie, le paramètre de la propriété [**Caption**](caption-property.md) détermine le texte affiché. Lorsque ni la propriété **VoiceCaption** ni **Caption** n’est définie, la commande n’apparaît pas dans la fenêtre commandes vocales.

## <a name="see-also"></a>Voir aussi

[**IAgentCommandsEx::GetVoiceCaption**](iagentcommandsex--getvoicecaption.md)


 

 