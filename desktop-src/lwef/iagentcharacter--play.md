---
title: IAgentCharacter Play
description: IAgentCharacter Play
ms.assetid: a0158693-ff62-4da4-8b68-402e8d5b1c2a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 320572322d7a28b52693c80eb918ebf78fcb50083e012e35c65df3a7bffdf0a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976399"
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


 

 




