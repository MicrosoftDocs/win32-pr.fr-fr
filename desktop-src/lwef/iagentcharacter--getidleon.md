---
title: IAgentCharacter GetIdleOn
description: IAgentCharacter GetIdleOn
ms.assetid: e5371326-33d0-4ecc-bda7-28f36f46ddeb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fdaf3ea460a76549112741ac77f83e10ec37cd9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675929"
---
# <a name="iagentcharactergetidleon"></a>IAgentCharacter::GetIdleOn

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetIdleOn(
   long * pbOn  // address of idle processing flag
);
```

Indique l’état de traitement automatique de l’inactivité d’un caractère.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="pbOn"></span><span id="pbon"></span><span id="PBON"></span>*pbOn*
</dt> <dd>

Adresse d’une variable qui reçoit la **valeur true** si le serveur Microsoft Agent lit automatiquement les animations d’état de **ralenti** pour un caractère et **false** dans le cas contraire.

</dd> </dl>

## <a name="see-also"></a>Voir aussi

[**IAgentCharacter::SetIdleOn**](iagentcharacter--setidleon.md)


 

 




