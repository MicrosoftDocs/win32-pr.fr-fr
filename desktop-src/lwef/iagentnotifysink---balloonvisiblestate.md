---
title: IAgentNotifySink BalloonVisibleState
description: IAgentNotifySink BalloonVisibleState
ms.assetid: 240e049c-7167-41b7-b092-95ed2a83aad3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2dd63d8eef3a7f1a70af81e13506a7e92ad84f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511228"
---
# <a name="iagentnotifysinkballoonvisiblestate"></a>IAgentNotifySink::BalloonVisibleState

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT BalloonVisibleState(
   long dwCharID,  // character ID
   long bVisible   // visibility flag
);                          
```

Avertit une application cliente lorsque l’état de visibilité de la bulle de texte du caractère change.

-   Pas de valeur de retour.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Identificateur du caractère dont l’état de visibilité de l’info-bulle du mot a changé.

</dd> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*
</dt> <dd>

Indicateur de visibilité. Cette valeur booléenne est **true** lorsque la bulle de texte du caractère devient visible ; et **false** lorsqu’il devient masqué.

</dd> </dl>

Cet événement est envoyé à tous les clients du caractère.

 

 




