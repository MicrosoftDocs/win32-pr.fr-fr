---
title: IAgentNotifySink inactif
description: IAgentNotifySink inactif
ms.assetid: 7770a698-31d9-4f3a-9c7e-858c480b640e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b43e060f361499b02bc0a83db697938975c76291
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512687"
---
# <a name="iagentnotifysinkidle"></a>IAgentNotifySink :: Idle

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT Idle(
   long dwCharID,  // character ID
   long bStart     // start flag
);                          
```

Avertit une application cliente lorsque l’état de **ralenti** d’un caractère a changé.

-   Pas de valeur de retour.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Identificateur de la demande qui a démarré.

</dd> <dt>

<span id="bStart"></span><span id="bstart"></span><span id="BSTART"></span>*bDémarrer*
</dt> <dd>

Indicateur de début. Cette valeur booléenne est **true** lorsque le caractère commence le ralenti et **false** lorsqu’il arrête le ralenti.

</dd> </dl>

Cet événement vous permet de suivre le moment où le serveur Microsoft Agent démarre ou arrête le traitement de l’inactivité d’un caractère.

## <a name="see-also"></a>Voir aussi

[**IAgentCharacter :: GetIdleOn**](iagentcharacter--getidleon.md), [ **IAgentCharacter :: SetIdleOn**](iagentcharacter--setidleon.md)


 

 




