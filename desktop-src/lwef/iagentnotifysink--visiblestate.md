---
title: IAgentNotifySink VisibleState
description: IAgentNotifySink VisibleState
ms.assetid: b0346296-74e9-448f-aa6d-a9fb1e645f05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4ba168fa538cf176de57a8638d7603fd5bc6e990a1b83837ba603b3a62c4236
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961509"
---
# <a name="iagentnotifysinkvisiblestate"></a>IAgentNotifySink::VisibleState

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT VisibleState(
   long dwCharID,  // character ID
   long bVisible,  // visibility flag
   long dwCause,   // cause of visible state
);                          
```

Avertit une application cliente lorsque l’état de visibilité du caractère change.

-   Pas de valeur de retour.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Identificateur du caractère dont l’état de visibilité est modifié.

</dd> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*
</dt> <dd>

Indicateur de visibilité. Cette valeur booléenne est **true** lorsque le caractère devient visible et **false** lorsque le caractère devient masqué.

</dd> <dt>

<span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*
</dt> <dd>

Cause de la dernière modification de l’état de visibilité du caractère. Le paramètre peut être l’un des suivants :



| Valeur                                                                   | Description                                                                                 |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| **const unsigned short** **NeverShown = 0 ;**<br/>                 | Le caractère n’a pas été affiché.                                                               |
| **const unsigned short** **UserHid = 1 ;**<br/>                    | Utilisateur a masqué le caractère avec le menu contextuel de l’icône de barre des tâches du caractère ou avec une entrée vocale. |
| **const unsigned short** **UserShowed = 2 ;**<br/>                 | L’utilisateur a affiché le caractère.                                                                  |
| **const unsigned short** **ProgramHid = 3 ;**<br/>                 | Votre application a masqué le caractère.                                                         |
| **const unsigned short** **ProgramShowed = 4 ;**<br/>              | Votre application a affiché le caractère.                                                      |
| **const unsigned short** **OtherProgramHid = 5 ;**<br/>            | Une autre application a masqué le caractère.                                                      |
| **const unsigned short** **OtherProgramShowed = 6 ;**<br/>         | Une autre application a montré le caractère.                                                   |
| **const non signé Short** **UserHidViaCharacterMenu = 7**<br/>     | Utilisateur a masqué le caractère dans le menu contextuel du caractère.                                    |
| **const non signed Short** **UserHidViaTaskbarIcon = UserHid**<br/> | Utilisateur a masqué le caractère dans le menu contextuel de l’icône de barre des tâches du caractère ou à l’aide d’une entrée vocale. |



 

</dd> </dl>

## <a name="see-also"></a>Voir aussi

[**IAgentCharacter :: getVisible**](iagentcharacter--getvisible.md), [ **IAgentCharacter :: GetVisibilityCause**](iagentcharacter--getvisibilitycause.md)


 

 





