---
title: IAgentCharacter SetIdleOn
description: IAgentCharacter SetIdleOn
ms.assetid: 397d223a-0970-4535-ad46-2923df6b9975
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98db30c9c440ed0564b98977d33e15e390cf57d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380438"
---
# <a name="iagentcharactersetidleon"></a>IAgentCharacter::SetIdleOn

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT SetIdleOn(
   long bOn  // idle processing flag
);
```

Définit le traitement d’inactivité automatique d’un caractère.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="bOn"></span><span id="bon"></span><span id="BON"></span>*Ble*
</dt> <dd>

Indicateur de traitement inactif. Si ce paramètre a la **valeur true**, l’agent Microsoft lit automatiquement les animations d’état **ralenti** .

</dd> </dl>

Le serveur définit automatiquement un délai d’attente après la dernière animation d’un caractère. Lorsque l’intervalle de ce minuteur est terminé, le serveur commence les États de **ralenti** pour un caractère, en lisant ses animations de **ralenti** associées à intervalles réguliers. Si vous souhaitez gérer vous-même les animations d’état **ralenti** , affectez la valeur **false** à la propriété. Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.

## <a name="see-also"></a>Voir aussi

[**IAgentCharacter::GetIdleOn**](iagentcharacter--getidleon.md)


 

 




