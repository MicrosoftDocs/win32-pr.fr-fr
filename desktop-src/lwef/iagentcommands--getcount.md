---
title: IAgentCommands GetCount
description: IAgentCommands GetCount
ms.assetid: 17140eda-17b0-49c2-8d50-5a38a553191a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 810f9fc268bc13558e4e51a3b64dd6f5b1d54caa5a055d9c90b6a8d11c48b3c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118749823"
---
# <a name="iagentcommandsgetcount"></a>IAgentCommands :: GetCount

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetCount(
   long * pdwCount  // address of count of commands
);                    
```

Récupère le nombre d’objets de [**commande**](/windows/desktop/lwef/the-command-object) dans une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) .

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="pdwCount"></span><span id="pdwcount"></span><span id="PDWCOUNT"></span>*pdwCount*
</dt> <dd>

Adresse d’une variable qui reçoit le nombre de [**commandes**](/windows/desktop/lwef/the-command-object) dans une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> </dl>

*pdwCount* comprend uniquement le nombre de [**commandes**](/windows/desktop/lwef/the-command-object) que vous définissez dans votre collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) . Le serveur ou d’autres entrées du client ne sont pas inclus.

 

 