---
title: IAgentCharacterEx GetGUID
description: IAgentCharacterEx GetGUID
ms.assetid: 25fb2531-a81c-4add-8134-77b1cd57cfe3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c9e0e14d0931774bf6ab5e1c8599bbebaadd0ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940167"
---
# <a name="iagentcharacterexgetguid"></a>IAgentCharacterEx :: GetGUID

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetGUID(
   BSTR * pbszGUID  // address of character's ID
);
```

Récupère l’ID unique du caractère.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="pbszGUID"></span><span id="pbszguid"></span><span id="PBSZGUID"></span>*pbszGUID*
</dt> <dd>

Adresse d’un BSTR qui reçoit l’ID du caractère.

</dd> </dl>

La propriété retourne une représentation sous forme de chaîne du GUID (mis en forme à l’aide d’accolades et de tirets) que le serveur utilise pour identifier le caractère de manière unique. Un identificateur de caractère est défini lorsqu’il est compilé avec l’éditeur de caractères Microsoft Agent. la propriété est en lecture seule.

 

 




