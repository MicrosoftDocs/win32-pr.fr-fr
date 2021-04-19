---
title: IAgentPropertySheet GetPosition
description: IAgentPropertySheet GetPosition
ms.assetid: 5d3de366-e48a-4643-81c5-ac4808671763
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ff4dcac994901824d7dc37868d7fcfc3f39cefd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510828"
---
# <a name="iagentpropertysheetgetposition"></a>IAgentPropertySheet :: GetPosition

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetPosition(
   long * plLeft,  // address of variable for left edge of property sheet
   long * plTop    // address of variable for top edge of property sheet
);
```

Récupère la position de la fenêtre de la feuille de propriétés de l’agent Microsoft.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plLeft*
</dt> <dd>

Adresse d’une variable qui reçoit les coordonnées d’écran du bord gauche de la feuille de propriétés, en pixels, par rapport à l’origine de l’écran (en haut à gauche).

</dd> <dt>

<span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*plTop*
</dt> <dd>

Adresse d’une variable qui reçoit les coordonnées d’écran du bord supérieur de la feuille de propriétés, en pixels, par rapport à l’origine de l’écran (en haut à gauche).

</dd> </dl>

## <a name="see-also"></a>Voir aussi

[**IAgentPropertySheet :: est à obtenir**](iagentpropertysheet--getsize.md)


 

 




