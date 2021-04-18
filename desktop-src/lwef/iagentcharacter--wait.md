---
title: IAgentCharacter Wait
description: IAgentCharacter Wait
ms.assetid: 4edb9a47-9385-49da-83ff-144780853ae7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d54ac2de03c78c220803a774537230938a00a776
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310746"
---
# <a name="iagentcharacterwait"></a>IAgentCharacter :: wait

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT Wait(
   long dwReqID,    // request ID
   long * pdwReqID  // address of request ID
);
```

Contient la file d’attente d’animation du caractère à l’animation (demande) spécifiée jusqu’à ce qu’une autre demande d’un autre caractère se termine.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*
</dt> <dd>

ID de la demande à attendre.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Adresse d’une variable qui reçoit l’ID de demande d' **attente** .

</dd> </dl>

Utilisez cette méthode uniquement lorsque vous prenez en charge plusieurs caractères (simultanés) et que vous souhaitez séquencer leur interaction. (Pour un caractère unique, chaque demande d’animation est lue de manière séquentielle, à l’issue de la requête précédente.) Si vous avez deux caractères et que vous souhaitez que la demande d’animation d’un caractère soit attendue jusqu’à la fin de l’animation de l’autre caractère, définissez la méthode d' **attente** sur l’ID de demande d’animation de l’autre caractère.

 

 




