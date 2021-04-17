---
title: IAgentCharacter GetVisibilityCause
description: IAgentCharacter GetVisibilityCause
ms.assetid: 46f681de-1c99-4f90-a3fe-aae04bb75339
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6013385144b82b79a0f17ae6443b094a9d9c8a4c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380442"
---
# <a name="iagentcharactergetvisibilitycause"></a>IAgentCharacter::GetVisibilityCause

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetVisibilityCause(
   long * pdwCause  // address of variable for cause of character visible state
);
```

Récupère la cause de l’état visible du caractère.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*pdwCause*
</dt> <dd>

Adresse d’une variable qui reçoit la cause de la modification de l’état de la dernière visibilité du caractère et sera l’une des suivantes :



| Valeur                                                                   | Description                                                                                 |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| **const unsigned short** **NeverShown = 0 ;**<br/>                 | Le caractère n’a pas été affiché.                                                               |
| **const unsigned short** **UserHid = 1 ;**<br/>                    | Utilisateur a masqué le caractère dans le menu contextuel de l’icône de barre des tâches du caractère ou à l’aide d’une entrée vocale. |
| **const unsigned short** **UserShowed = 2 ;**<br/>                 | L’utilisateur a affiché le caractère.                                                                  |
| **const unsigned short** **ProgramHid = 3 ;**<br/>                 | Votre application a masqué le caractère.                                                         |
| **const unsigned short** **ProgramShowed = 4 ;**<br/>              | Votre application a affiché le caractère.                                                      |
| **const unsigned short** **OtherProgramHid = 5 ;**<br/>            | Une autre application a masqué le caractère.                                                      |
| **const unsigned short** **OtherProgramShowed = 6 ;**<br/>         | Une autre application a montré le caractère.                                                   |
| **const non signé Short** **UserHidViaCharacterMenu = 7**<br/>     | Utilisateur a masqué le caractère dans le menu contextuel du caractère.                                    |
| **const non signed Short** **UserHidViaTaskbarIcon = UserHid**<br/> | Utilisateur a masqué le caractère dans le menu contextuel de l’icône de barre des tâches du caractère ou à l’aide d’une entrée vocale. |



 

</dd> </dl>

## <a name="see-also"></a>Voir aussi

[**IAgentNotifySink::VisibleState**](iagentnotifysink--visiblestate.md)


 

 





