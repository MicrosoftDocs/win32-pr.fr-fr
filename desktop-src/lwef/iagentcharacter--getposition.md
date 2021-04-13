---
title: IAgentCharacter GetPosition
description: IAgentCharacter GetPosition
ms.assetid: 79343337-2700-48cb-a09d-1a356ea560e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40cdff0d6876fc7257e05014f3d9ba695db5d168
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311599"
---
# <a name="iagentcharactergetposition"></a>IAgentCharacter :: GetPosition

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetPosition(
   long * plLeft,  // address of variable for left edge of character 
   long * plTop    // address of variable for top edge of character 
);
```

Récupère la position du frame d’animation du caractère.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plLeft*
</dt> <dd>

Adresse d’une variable qui reçoit la coordonnée d’écran du bord gauche du cadre d’animation de caractères, en pixels, par rapport à l’origine de l’écran (en haut à gauche).

</dd> <dt>

<span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*plTop*
</dt> <dd>

Adresse d’une variable qui reçoit la coordonnée d’écran du bord supérieur du cadre d’animation de caractères, en pixels, par rapport à l’origine de l’écran (en haut à gauche).

</dd> </dl>

Même si le caractère apparaît dans une fenêtre de zone de forme irrégulière, l’emplacement du caractère est basé sur son cadre d’animation rectangulaire.

## <a name="see-also"></a>Voir aussi

[**IAgentCharacter :: SetPosition**](iagentcharacter--setposition.md), [ **IAgentCharacter ::** de](iagentcharacter--getsize.md)


 

 




