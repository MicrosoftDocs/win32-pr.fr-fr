---
title: IAgentNotifySink déplacer
description: IAgentNotifySink déplacer
ms.assetid: d1809fdb-df4b-4884-b9e8-2877a814dc9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16f32df3058a5b5c8e0a4e02a98f9a97afdbff56f349a63fceb5d70a9001391
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105171"
---
# <a name="iagentnotifysinkmove"></a>IAgentNotifySink :: Move

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT Move(
   long dwCharID,  // character ID
   long x,         // x-coordinate of new location
   long y,         // y-coordinate of new location
   long dwCause    // cause of move state
);                          
```

Avertit une application cliente lorsque le caractère a été déplacé.

-   Pas de valeur de retour.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Identificateur du caractère qui a été déplacé.

</dd> <dt>

<span id="x"></span><span id="X"></span>*x*
</dt> <dd>

Coordonnée x de la nouvelle position, en pixels, par rapport à l’origine de l’écran (en haut à gauche). L’emplacement d’un caractère est basé sur l’angle supérieur gauche de son cadre d’animation.

</dd> <dt>

<span id="y"></span><span id="Y"></span>*y*
</dt> <dd>

Coordonnée y de la nouvelle position, en pixels, par rapport à l’origine de l’écran (en haut à gauche). L’emplacement d’un caractère est basé sur l’angle supérieur gauche de son cadre d’animation.

</dd> <dt>

<span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*
</dt> <dd>

Cause du déplacement du caractère. Le paramètre peut être l’un des suivants :



| Valeur                                                          | Description                                                                          |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------|
| **const unsigned short** **NeverMoved = 0 ;**<br/>        | Le caractère n’a pas été déplacé.                                                        |
| **const unsigned short** **UserMoved = 1 ;**<br/>         | L’utilisateur a fait glisser le caractère.                                                          |
| **const unsigned short** **ProgramMoved = 2 ;**<br/>      | Votre application a déplacé le caractère.                                                |
| **const unsigned short** **OtherProgramMoved = 3 ;**<br/> | Une autre application a déplacé le caractère.                                             |
| **const non signé Short** **SystemMoved = 4**<br/>        | Le serveur a déplacé le caractère pour le garder à l’écran après une modification de la résolution de l’écran. |



 

</dd> </dl>

Cet événement est envoyé à tous les clients du caractère.

## <a name="see-also"></a>Voir aussi

[**IAgentCharacter :: GetMoveCause**](iagentcharacter--getmovecause.md), [ **IAgentCharacter :: MoveTo**](iagentcharacter--moveto.md)


 

 





