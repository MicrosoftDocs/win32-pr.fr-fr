---
title: IAgentCharacter Play
description: IAgentCharacter Play
ms.assetid: a0158693-ff62-4da4-8b68-402e8d5b1c2a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 996929271156254377f08b9fc41da3932aee9da4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029898"
---
# <a name="iagentcharacterplay"></a>IAgentCharacter ::P

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT Play(
   BSTR bszAnimation,  // name of an animation
   long * pdwReqID     // address of request ID
);
```

Lit l’animation spécifiée.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi. Lorsque la fonction retourne, *pdwReqID* contient l’ID de la demande.

<dl> <dt>

<span id="bszAnimation"></span><span id="bszanimation"></span><span id="BSZANIMATION"></span>*bszAnimation*
</dt> <dd>

Nom d’une animation.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Adresse d’une variable qui reçoit l’ID de demande **IAgentCharacter ::P** .

</dd> </dl>

Le nom d’une animation est défini lorsque le caractère est compilé à l’aide de l’éditeur de caractères Microsoft Agent. Avant de lire l’animation spécifiée, le serveur tente de lire l’animation de **retour** pour l’animation précédente (le cas échéant).

Lorsque les données d’animation d’un caractère sont stockées sur l’ordinateur local de l’utilisateur, vous pouvez utiliser la méthode **IAgentCharacter ::P** et spécifier le nom de l’animation. Lorsque vous utilisez le protocole HTTP pour accéder aux données d’animation, utilisez la méthode [**Prepare**](iagentcharacter--prepare.md) pour garantir la disponibilité de l’animation avant d’appeler cette méthode.

## <a name="see-also"></a>Voir aussi

[**IAgentCharacter ::P la même parenthèse**](iagentcharacter--prepare.md)


 

 




