---
title: IAgentCommands GetVoice
description: IAgentCommands GetVoice
ms.assetid: ef8983bc-c70c-48c7-9c5f-1dae61028d90
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b1915512c89611267df3788e5dcaa84fb0874a4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381956"
---
# <a name="iagentcommandsgetvoice"></a>IAgentCommands::GetVoice

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetVoice(
   BSTR * pbszVoice  // address of Voice setting for Commands collection
);
```

Récupère la valeur de la propriété [**Voice**](voice-property.md) pour une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) .

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="pbszVoice"></span><span id="pbszvoice"></span><span id="PBSZVOICE"></span>*pbszVoice*
</dt> <dd>

Adresse d’un BSTR qui reçoit la valeur du paramètre de texte [**vocal**](voice-property.md) pour une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> </dl>

## <a name="see-also"></a>Voir aussi

[**IAgentCommands :: SetVoice**](iagentcommands--setvoice.md), [**IAgentCommands :: GetCaption**](iagentcommands--getcaption.md), [**IAgentCommands :: getVisible**](iagentcommands--getvisible.md)


 

 