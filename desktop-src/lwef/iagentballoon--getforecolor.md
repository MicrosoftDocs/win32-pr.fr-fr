---
title: IAgentBalloon GetForeColor
description: IAgentBalloon GetForeColor
ms.assetid: b06ad924-66b6-42a6-8c97-5bc4c46f6e2d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b7a251471b0281661b087dbfb9b141c54ff9dc7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511640"
---
# <a name="iagentballoongetforecolor"></a>IAgentBalloon::GetForeColor

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetForeColor(
   long * plFGColor // address of variable for foreground color displayed
);                  // in word balloon
```

Récupère la valeur de la couleur de premier plan affichée dans une bulle de mot.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="plFGColor"></span><span id="plfgcolor"></span><span id="PLFGCOLOR"></span>*plFGColor*
</dt> <dd>

Adresse d’une variable qui reçoit le paramètre de couleur pour le premier plan de l’info-bulle.

</dd> </dl>

La couleur de premier plan utilisée dans une bulle de mot de caractères est définie dans l’éditeur de caractères Microsoft Agent. Elle ne peut pas être modifiée par une application. Toutefois, l’utilisateur peut remplacer la couleur de premier plan des bulles de mot pour tous les caractères par le biais de la feuille de propriétés de l’agent Microsoft.

## <a name="see-also"></a>Voir aussi

[**IAgentBalloon::GetBackColor**](iagentballoon--getbackcolor.md)


 

 




