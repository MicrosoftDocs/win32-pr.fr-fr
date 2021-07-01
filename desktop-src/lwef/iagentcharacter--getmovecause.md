---
title: IAgentCharacter GetMoveCause
description: IAgentCharacter GetMoveCause
ms.assetid: 36cdd3bc-65b6-469f-9344-93403c1d24e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be943cf3b25b789838215f0209b16e67d5b50659
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119683"
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



| Value                                                               | Description                                                                                     |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------|
| **const unsigned short** **NeverMoved = 0 ;**<br/>        | Le caractère n’a pas été déplacé.                                                        |
| **const unsigned short** **UserMoved = 1 ;**<br/>         | L’utilisateur a fait glisser le caractère.                                                          |
| **const unsigned short** **ProgramMoved = 2 ;**<br/>      | Votre application a déplacé le caractère.                                                |
| **const unsigned short** **OtherProgramMoved = 3 ;**<br/> | Une autre application a déplacé le caractère.                                             |
| **const non signé Short** **SystemMoved = 4**<br/>        | Le serveur a déplacé le caractère pour le garder à l’écran après une modification de la résolution de l’écran. |



 

</dd> </dl>

## <a name="see-also"></a>Voir aussi

[**IAgentNotifySink :: Move**](iagentnotifysink--move.md)


 

 





