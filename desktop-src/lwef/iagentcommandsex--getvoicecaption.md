---
title: IAgentCommandsEx GetVoiceCaption
description: IAgentCommandsEx GetVoiceCaption
ms.assetid: 0e505295-386a-421f-a43c-6da03c8a2b6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3a757e1c841afd62b9b6ae13f1ef34178f133ca
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106543047"
---
# <a name="iagentcommandsexgetvoicecaption"></a>IAgentCommandsEx::GetVoiceCaption

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetVoiceCaption(
   BSTR * pbszVoiceCaption  // address of command's voice caption
);
```

Récupère le [**VoiceCaption**](voicecaption-property.md) pour un objet [**Command**](/windows/desktop/lwef/the-command-object) .

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="pbszVoiceCaption"></span><span id="pbszvoicecaption"></span><span id="PBSZVOICECAPTION"></span>*pbszVoiceCaption*
</dt> <dd>

Adresse d’un BSTR qui reçoit la valeur du texte de [**légende**](caption-property.md) affiché pour une [**commande**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

Le texte retourné est celui défini pour l’objet de [**commande**](/windows/desktop/lwef/the-command-object) et apparaît dans la fenêtre commandes vocales lorsque votre application cliente est active en entrée.

Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.

## <a name="see-also"></a>Voir aussi

[**IAgentCommandsEx::SetVoiceCaption**](iagentcommandsex--setvoicecaption.md)


 

 