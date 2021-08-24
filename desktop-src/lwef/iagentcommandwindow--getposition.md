---
title: IAgentCommandWindow GetPosition
description: IAgentCommandWindow GetPosition
ms.assetid: d85a7a2c-f0ea-4612-aa73-2e44c49e4e18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52571311a87ee0846dcaf515912762069fe3025a25c5a2589770ee9738bb2de7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119716099"
---
# <a name="iagentcommandwindowgetposition"></a>IAgentCommandWindow :: GetPosition

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetPosition(
   long * plLeft,  // address of variable for left edge of Voice Commands Window
   long * plTop    // address of variable for top edge of Voice Commands Window
);
```

Récupère la position de la fenêtre commandes vocales.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plLeft*
</dt> <dd>

Adresse d’une variable qui reçoit la coordonnée d’écran du bord gauche de la fenêtre commandes vocales, en pixels, par rapport à l’origine de l’écran (en haut à gauche).

</dd> <dt>

<span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*plTop*
</dt> <dd>

Adresse d’une variable qui reçoit la coordonnée d’écran du bord supérieur de la fenêtre commandes vocales, en pixels, par rapport à l’origine de l’écran (en haut à gauche).

</dd> </dl>

## <a name="see-also"></a>Voir aussi

[**IAgentCommandWindow :: est à obtenir**](iagentcommandwindow--getsize.md)


 

 




