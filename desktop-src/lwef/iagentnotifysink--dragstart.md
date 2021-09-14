---
title: IAgentNotifySink DragStart
description: IAgentNotifySink DragStart
ms.assetid: b3905b99-69e4-4046-aab9-2322618935aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f33ae89f9e24c6c7b0ec69fba1a98b3a64a18620
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127295447"
---
# <a name="iagentnotifysinkdragstart"></a>IAgentNotifySink ::D ragStart

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT DragStart(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x-coordinate of mouse pointer
   long y          // y-coordinate of mouse pointer
);                          
```

Avertit une application cliente lorsque l’utilisateur commence à faire glisser un caractère.

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

 

 




