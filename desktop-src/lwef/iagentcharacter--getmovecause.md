---
title: IAgentCharacter GetMoveCause
description: IAgentCharacter GetMoveCause
ms.assetid: 36cdd3bc-65b6-469f-9344-93403c1d24e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 612fcbfd4470d17e2365373458a8ded899a8180a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380446"
---
# <a name="iagentcharactergetmovecause"></a>IAgentCharacter::GetMoveCause

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetMoveCause(
   long * pdwCause  // address of variable for cause of character move
);
```

Récupère la cause du dernier déplacement du caractère.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*pdwCause*
</dt> <dd>

Adresse d’une variable qui reçoit la cause du dernier déplacement du caractère et sera l’une des suivantes :



|                                                                |                                                                                      |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------|
| **const unsigned short** **NeverMoved = 0 ;**<br/>        | Le caractère n’a pas été déplacé.                                                        |
| **const unsigned short** **UserMoved = 1 ;**<br/>         | L’utilisateur a fait glisser le caractère.                                                          |
| **const unsigned short** **ProgramMoved = 2 ;**<br/>      | Votre application a déplacé le caractère.                                                |
| **const unsigned short** **OtherProgramMoved = 3 ;**<br/> | Une autre application a déplacé le caractère.                                             |
| **const non signé Short** **SystemMoved = 4**<br/>        | Le serveur a déplacé le caractère pour le garder à l’écran après une modification de la résolution de l’écran. |



 

</dd> </dl>

## <a name="see-also"></a>Voir aussi

[**IAgentNotifySink :: Move**](iagentnotifysink--move.md)


 

 





