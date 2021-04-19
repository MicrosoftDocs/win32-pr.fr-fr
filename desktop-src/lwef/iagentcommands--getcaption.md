---
title: IAgentCommands GetCaption
description: IAgentCommands GetCaption
ms.assetid: bbaaaa20-c8c2-41af-a6fc-cf8849daa399
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f886413ae6bfbfe104306d7280d8c66b08bf311a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106509026"
---
# <a name="iagentcommandsgetcaption"></a>IAgentCommands::GetCaption

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetCaption(
   BSTR * pbszCaption  // address of Caption text for Commands collection
);
```

Récupère la [**légende**](caption-property.md) pour une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) .

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="pbszCaption"></span><span id="pbszcaption"></span><span id="PBSZCAPTION"></span>*pbszCaption*
</dt> <dd>

Adresse d’un BSTR qui reçoit la valeur du paramètre de texte de [**légende**](caption-property.md) affiché pour une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> </dl>

## <a name="see-also"></a>Voir aussi

[**IAgentCommands :: SetCaption**](iagentcommands--setcaption.md), [**IAgentCommands :: getVisible**](iagentcommands--getvisible.md), [**IAgentCommands :: GetVoice**](iagentcommands--getvoice.md)


 

 