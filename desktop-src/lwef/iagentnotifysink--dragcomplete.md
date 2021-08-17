---
title: IAgentNotifySink DragComplete
description: IAgentNotifySink DragComplete
ms.assetid: b2d9b9c2-709e-4988-aa92-f129e3836fc7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b63c24abd41f0509293ba2fafeb055f195a4d13ad354662e8d32d0fb1715e1fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477027"
---
# <a name="iagentnotifysinkdragcomplete"></a>IAgentNotifySink ::D ragComplete

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT DragComplete(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x-coordinate of mouse pointer
   long y          // y-coordinate of mouse pointer
);                          
```

Avertit une application cliente lorsque l’utilisateur arrête de faire glisser un caractère.

-   Pas de valeur de retour.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Identificateur du caractère déplacé.

</dd> <dt>

<span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*
</dt> <dd>

Paramètre qui indique le bouton de la souris et l’état de la touche de modification. Le paramètre peut retourner n’importe quelle combinaison des éléments suivants :



| Valeur  | Description      |
|--------|------------------|
| 0x0001 | Bouton gauche      |
| 0x0010 | Bouton central    |
| 0x0002 | Bouton droit     |
| 0x0004 | Touche Maj enfoncée   |
| 0x0008 | Touche CTRL enfoncée |
| 0x0020 | Touche Alt enfoncée     |



 

</dd> <dt>

<span id="x"></span><span id="X"></span>*x*
</dt> <dd>

Coordonnée x du pointeur de la souris en pixels, par rapport à l’origine de l’écran (en haut à gauche).

</dd> <dt>

<span id="y"></span><span id="Y"></span>*y*
</dt> <dd>

Coordonnée y du pointeur de la souris en pixels, par rapport à l’origine de l’écran (en haut à gauche).

</dd> </dl>

 

 




