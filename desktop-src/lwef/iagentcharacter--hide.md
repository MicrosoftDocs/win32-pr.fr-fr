---
title: IAgentCharacter masquer
description: IAgentCharacter masquer
ms.assetid: a8128fe8-9a3b-41a3-bfe3-82ace1baff6f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bcd0ef91eb4d2738f19fb594ac1ab186efaec6e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031163"
---
# <a name="iagentcharacterhide"></a>IAgentCharacter :: Hide

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT Hide(
   long bFast,      // play Hiding state animation flag
   long * pdwReqID  // address of request ID
);
```

Masque le caractère.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi. Lorsque la fonction retourne, *pdwReqID* contient l’ID de la demande.

<dl> <dt>

<span id="bFast"></span><span id="bfast"></span><span id="BFAST"></span>*bFast*
</dt> <dd>

**Masquage** de l’indicateur d’animation d’État. Si ce paramètre a la **valeur true**, l’animation de **masquage** ne s’exécute pas avant que le cadre de caractère soit masqué ; Si la **valeur est false**, l’animation est lue.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Adresse d’une variable qui reçoit l’ID de la demande de **masquage** .

</dd> </dl>

Le serveur met en file d’attente l’animation associée à la méthode **Hide** dans la file d’attente du caractère. Cela vous permet de l’utiliser pour masquer le caractère après une séquence d’autres animations. Vous pouvez exécuter l’action immédiatement à l’aide de la méthode [**Stop**](iagentcharacter--stop.md) avant d’appeler la méthode **Hide** .

Lorsque vous utilisez le protocole HTTP pour accéder aux données de caractères et d’animation, utilisez la méthode [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) pour garantir la disponibilité de l’animation de l’état de **masquage** avant d’appeler cette méthode.

Le masquage d’un caractère peut également entraîner le déclenchement de l’événement [**IAgentNotifySink :: ActivateInputState**](iagentnotifysink--activateinputstate.md) d’un autre caractère visible.

Les caractères masqués ne peuvent pas accéder au canal audio. Le serveur renvoie un état d’échec dans l’événement [**RequestComplete**](iagentnotifysink--requestcomplete.md) si vous générez une demande d’animation et que le caractère est masqué.

## <a name="see-also"></a>Voir aussi

[**IAgentCharacter :: Show**](iagentcharacter--show.md)


 

 