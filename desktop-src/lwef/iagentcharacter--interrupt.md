---
title: Interruption IAgentCharacter
description: Interruption IAgentCharacter
ms.assetid: ae05d317-e2d9-4d11-a6df-f9b25e43467a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17c9f19f716b15a48ec3cdb064aa4c0fdbbd1774
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940854"
---
# <a name="iagentcharacterinterrupt"></a>IAgentCharacter :: Interrupt

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT Interrupt(
   long dwReqID,    // request ID to interrupt
   long * pdwReqID  // address of request ID
);
```

Interrompt l’animation (demande) spécifiée d’un autre caractère.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi. Lorsque la fonction retourne, *pdwReqID* contient l’ID de la demande.

<dl> <dt>

<span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*
</dt> <dd>

ID de la demande à interrompre.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Adresse d’une variable qui reçoit l’ID de demande d' **interruption** .

</dd> </dl>

Si vous chargez plusieurs caractères, vous pouvez utiliser cette méthode pour synchroniser les animations entre les caractères. Par exemple, si un autre caractère se trouve dans une animation de bouclage, cette méthode arrête l’animation de bouclage et démarre l’animation suivante dans la file d’attente du caractère.

L' **interruption** interrompt l’animation existante, mais n’efface pas la file d’attente d’animation du caractère. Il démarre l’animation suivante dans la file d’attente du caractère. Pour arrêter et vider la file d’attente d’un caractère, utilisez la méthode [**Stop**](/windows/desktop/lwef/iagentcharacter--stop) .

Vous ne pouvez pas utiliser cette méthode pour avoir une interruption de caractère proprement dite car le serveur Microsoft agent met en file d’attente la méthode d' **interruption** dans la file d’attente d’animation du caractère. Par conséquent, vous ne pouvez utiliser l' **interruption** que pour arrêter l’animation d’un autre caractère que vous avez chargé.

 

 