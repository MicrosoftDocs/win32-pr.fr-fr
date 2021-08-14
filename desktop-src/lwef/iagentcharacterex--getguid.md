---
title: IAgentCharacterEx GetGUID
description: IAgentCharacterEx GetGUID
ms.assetid: 25fb2531-a81c-4add-8134-77b1cd57cfe3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e43a98617b1e2d25a25167ad5b95462eeb462f40f5a353b5a5ec45ffb3a9cca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477967"
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

 

 




