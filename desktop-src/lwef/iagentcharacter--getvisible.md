---
title: IAgentCharacter GetVisible
description: IAgentCharacter GetVisible
ms.assetid: 6e8e3a68-a7bb-4afb-a753-836fe82a0b24
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c812c7765bed791532db00c8f2e9cfd68cc771575e7a70fd27d45adef00bdb2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118478359"
---
# <a name="iagentcharactergetvisible"></a>IAgentCharacter::GetVisible

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of variable for character Visible setting
);
```

Détermine si le cadre d’animation du caractère est actuellement visible.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*
</dt> <dd>

Adresse d’une variable qui reçoit la **valeur true** si le frame du caractère est visible et **false** s’il est masqué.

</dd> </dl>

Vous pouvez utiliser cette méthode pour déterminer si le frame du caractère est actuellement visible. Pour rendre un caractère visible, utilisez la méthode [**Show**](/windows/desktop/lwef/iagentcharacter--show) . Pour masquer un caractère, utilisez la méthode [**Hide**](/windows/desktop/lwef/iagentcharacter--hide) .

 

 