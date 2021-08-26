---
title: IAgentBalloon GetVisible
description: IAgentBalloon GetVisible
ms.assetid: 328af211-4ea4-482c-8487-42c8e4cd66b0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 939026026e18e550ca18838977f00a8878db9039595d9eadd0b30b88235a0248
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962319"
---
# <a name="iagentballoongetvisible"></a>IAgentBalloon::GetVisible

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of variable for word balloon
);                   // Visible setting
```

Détermine si la bulle de texte est visible ou masquée.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*
</dt> <dd>

Adresse d’une variable qui reçoit la **valeur true** si le mot-bulle est visible et **false** s’il est masqué.

</dd> </dl>

## <a name="see-also"></a>Voir aussi

[**IAgentBalloon :: SetVisible**](iagentballoon--setvisible.md)


 

 




