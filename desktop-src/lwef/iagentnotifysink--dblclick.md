---
title: IAgentNotifySink DblClick
description: IAgentNotifySink DblClick
ms.assetid: 7e86cc9b-8bc3-405e-9bbf-764cec9c3130
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9ec7372d524027588dae5a0a3aafaf07146556e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379946"
---
# <a name="iagentnotifysinkdblclick"></a>IAgentNotifySink ::D blClick

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT DblClick(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x coordinate of mouse pointer
   long y          // y coordinate of mouse pointer
);                          
```

Avertit une application cliente lorsque l’utilisateur double-clique sur un caractère.

-   Pas de valeur de retour.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Identificateur du caractère double-cliqué.

</dd> <dt>

<span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*
</dt> <dd>

Paramètre qui indique le bouton de la souris et l’état de la touche de modification. Le paramètre peut retourner n’importe quelle combinaison des éléments suivants :



|        |                                                |
|--------|------------------------------------------------|
| 0x0001 | Bouton gauche                                    |
| 0x0010 | Bouton central                                  |
| 0x0002 | Bouton droit                                   |
| 0x0004 | Touche Maj enfoncée                                 |
| 0x0008 | Touche CTRL enfoncée                               |
| 0x0020 | Touche Alt enfoncée                                   |
| 0x1000 | Un événement s’est produit sur l’icône de la barre des tâches du caractère |



 

</dd> <dt>

<span id="x"></span><span id="X"></span>*x*
</dt> <dd>

Coordonnée x du pointeur de la souris en pixels, par rapport à l’origine de l’écran (en haut à gauche).

</dd> <dt>

<span id="y"></span><span id="Y"></span>*y*
</dt> <dd>

Coordonnée y du pointeur de la souris en pixels, par rapport à l’origine de l’écran (en haut à gauche).

</dd> </dl>

Cet événement est envoyé au client d’entrée-actif du caractère. Si aucun des clients du caractère n’est en entrée-actif, le serveur notifie le client actif du caractère. Si le caractère est visible, le serveur rend également ce client en entrée-actif et envoie [**IAgentNotifySink :: ActivateInputState**](iagentnotifysink--activateinputstate.md). Si le caractère est masqué, le caractère s’affiche également automatiquement.

 

 




