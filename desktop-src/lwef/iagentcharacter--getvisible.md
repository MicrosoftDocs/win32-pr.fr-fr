---
title: IAgentCharacter GetVisible
description: IAgentCharacter GetVisible
ms.assetid: 6e8e3a68-a7bb-4afb-a753-836fe82a0b24
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0593b9b3a193b9d5910888b81b4ecba90469b1e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101485"
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

 

 