---
title: IAgentCharacter arrêter
description: IAgentCharacter arrêter
ms.assetid: 3064bb3e-37a6-4022-bffb-130735736889
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 297f187b7045b1da5773643f2765160c71fbca0d4eb7c6ec12c4032e2f1d5806
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114779"
---
# <a name="iagentcharacterstop"></a>IAgentCharacter :: Stop

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT Stop(
   long dwReqID  // request ID
);
```

Arrête l’animation spécifiée (requête) et la supprime de la file d’attente d’animation du caractère.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*
</dt> <dd>

ID de la demande à arrêter.

</dd> </dl>

L' **arrêt** peut également être utilisé pour arrêter les appels [**Prepare**](iagentcharacter--prepare.md) en attente.

## <a name="see-also"></a>Voir aussi

[**IAgentCharacter ::P reparenthèse**](iagentcharacter--prepare.md), [ **IAgentCharacter :: stopAll**](iagentcharacter--stopall.md)


 

 




