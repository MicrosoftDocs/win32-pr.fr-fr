---
title: IAgentNotifySink déplacer
description: IAgentNotifySink déplacer
ms.assetid: d1809fdb-df4b-4884-b9e8-2877a814dc9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52563ff3838348b7bf8e6a2bcdfdf20a51c79723
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292307"
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


 

 





