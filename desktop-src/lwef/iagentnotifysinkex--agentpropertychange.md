---
title: IAgentNotifySinkEx AgentPropertyChange
description: IAgentNotifySinkEx AgentPropertyChange
ms.assetid: 8293cd77-320a-4b57-b3d8-52bc450d6aa0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7d7a0737428d20b297d83ac92c3ce6957dac0390c719c17b96a00983a0a57af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961489"
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


 

 




