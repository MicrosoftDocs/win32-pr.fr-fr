---
title: IAgentNotifySinkEx AgentPropertyChange
description: IAgentNotifySinkEx AgentPropertyChange
ms.assetid: 8293cd77-320a-4b57-b3d8-52bc450d6aa0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e27fe9e2318af0642c2df680af3a279ab57253d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939975"
---
# <a name="iagentnotifysinkexagentpropertychange"></a>IAgentNotifySinkEx::AgentPropertyChange

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT AgentPropertyChange(
);
```

Avertit une application cliente lorsque l’utilisateur modifie un paramètre de propriété de l’agent Microsoft.

-   Pas de valeur de retour.

Lorsque l’utilisateur modifie un paramètre de propriété de l’agent Microsoft dans la feuille de propriétés de l’agent Microsoft, le serveur envoie cet événement à tous les clients, sauf si le serveur est actuellement suspendu.

## <a name="see-also"></a>Voir aussi

[**IAgentNotifySinkEx ::D efaultCharacterChange**](iagentnotifysinkex--defaultcharacterchange.md)


 

 




