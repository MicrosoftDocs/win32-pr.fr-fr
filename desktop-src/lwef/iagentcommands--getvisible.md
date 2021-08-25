---
title: IAgentCommands GetVisible
description: IAgentCommands GetVisible
ms.assetid: 229a02c8-f0a1-4ee5-9bae-961b63792038
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8d63ef62a0e57539d633d595901c6cfde1a252ac9ef369f9f56bc3ddaaeea0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961909"
---
# <a name="iagentcommandsgetvisible"></a>IAgentCommands::GetVisible

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of Visible setting for Commands collection
);
```

Récupère la valeur de la propriété [**visible**](visible-property.md) pour une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) .

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*
</dt> <dd>

Adresse d’une variable qui reçoit la valeur de la propriété [**visible**](visible-property.md) pour une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> </dl>

## <a name="see-also"></a>Voir aussi

[**IAgentCommands :: setVisible**](iagentcommands--setvisible.md), [ **IAgentCommands :: SetCaption**](iagentcommands--setcaption.md)


 

 