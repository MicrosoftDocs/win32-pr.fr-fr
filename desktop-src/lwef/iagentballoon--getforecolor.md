---
title: IAgentBalloon GetForeColor
description: IAgentBalloon GetForeColor
ms.assetid: b06ad924-66b6-42a6-8c97-5bc4c46f6e2d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fabd35a43cba0485bbda1fae20b116316dec90832e42920d010b27586e972c5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962329"
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


 

 




