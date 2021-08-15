---
title: IAgentNotifySinkEx ListeningState
description: IAgentNotifySinkEx ListeningState
ms.assetid: e303b299-0dd0-419a-87a9-1490fe6cf54a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21d3926741f83f66ab6133874ec47783976c0ddb6d3fbd2ee91c6e584813147a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117692605"
---
# <a name="iagentnotifysinkexlisteningstate"></a>IAgentNotifySinkEx::ListeningState

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT ListeningState(
   long dwCharacterID,  // character ID
   long bListening,     // listening mode state
   long dwCause         // cause  
);
```

Avertit une application cliente lorsque le mode d’écoute change.

-   Pas de valeur de retour.

<dl> <dt>

<span id="dwCharacterID"></span><span id="dwcharacterid"></span><span id="DWCHARACTERID"></span>*dwCharacterID*
</dt> <dd>

Caractère pour lequel l’état d’écoute a changé.

</dd> <dt>

<span id="bListening"></span><span id="blistening"></span><span id="BLISTENING"></span>*bListening*
</dt> <dd>

État du mode d’écoute. **True** indique que le mode d’écoute a démarré ; **False**, ce mode d’écoute est terminé.

</dd> <dt>

<span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*
</dt> <dd>

La cause de l’événement, qui peut être l’une des valeurs suivantes.



| Valeur                                                                             | Description                                                                    |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| **const unsigned long** **LSCOMPLETE \_ cause \_ PROGRAMDISABLED = 1 ;**<br/>    | Le mode d’écoute a été désactivé par le code de programme.                                 |
| **const unsigned long** **LSCOMPLETE \_ cause \_ PROGRAMTIMEDOUT = 2 ;**<br/>    | Le mode d’écoute (activé par code de programme) a expiré.                          |
| **const unsigned long** **LSCOMPLETE \_ cause \_ USERTIMEDOUT = 3 ;**<br/>       | Le mode d’écoute (activé par la clé d’écoute) a expiré.                     |
| **const unsigned long** **LSCOMPLETE \_ cause \_ USERRELEASEDKEY = 4 ;**<br/>    | Le mode d’écoute a été désactivé, car l’utilisateur a relâché la clé d’écoute.     |
| **const unsigned long** **LSCOMPLETE \_ cause \_ USERUTTERANCEENDED = 5 ;**<br/> | Le mode d’écoute a été désactivé, car l’utilisateur a terminé de parler.              |
| **const unsigned long** **LSCOMPLETE \_ cause \_ CLIENTDEACTIVATED = 6 ;**<br/>  | Le mode d’écoute a été désactivé, car le client actif d’entrée a été désactivé. |
| **const unsigned long** **LSCOMPLETE \_ cause \_ DEFAULTCHARCHANGE = 7**<br/>   | Le mode d’écoute a été désactivé car le caractère par défaut a été modifié.       |
| **const unsigned long** **LSCOMPLETE \_ cause \_ USERDISABLED = 8**<br/>        | Le mode d’écoute a été désactivé, car l’utilisateur a désactivé l’entrée vocale.          |



 

</dd> </dl>

Cet événement est envoyé à tous les clients lorsque le mode d’écoute commence après que l’utilisateur appuie sur la touche d’écoute ou à la fin de son délai d’attente, ou lorsque le client d’entrée-actif appelle la méthode [**IAgentCharacterEx :: Listen**](iagentcharacterex--listen.md) avec **true** ou **false**.

L’événement retourne des valeurs aux clients pour lesquels ce caractère est actuellement chargé. Tous les autres clients reçoivent un caractère null (chaîne vide).

## <a name="see-also"></a>Voir aussi

[**IAgentCharacterEx :: Listen**](iagentcharacterex--listen.md)


 

 





