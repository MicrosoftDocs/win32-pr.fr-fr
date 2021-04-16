---
title: IAgentCharacter HasOtherClients
description: IAgentCharacter HasOtherClients
ms.assetid: ee74fa9b-2842-43ac-8493-bc69b480581e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32380e31e63278f4181cfd854ecaada1775a4fd5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507467"
---
# <a name="iagentcharacterhasotherclients"></a>IAgentCharacter::HasOtherClients

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT HasOtherClients(
   long * plNumOtherClients  // address of variable for number of clients 
);                           // for character 
```

Récupère les pour savoir si un caractère a d’autres clients.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="plNumOtherClients"></span><span id="plnumotherclients"></span><span id="PLNUMOTHERCLIENTS"></span>*plNumOtherClients*
</dt> <dd>

Adresse d’une variable qui reçoit le nombre d’autres clients connectés pour le caractère (nombre total de clients moins votre client).

</dd> </dl>

 

 




