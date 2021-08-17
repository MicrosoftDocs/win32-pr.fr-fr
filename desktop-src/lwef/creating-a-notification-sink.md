---
title: Création d’un récepteur de notification
description: Création d’un récepteur de notification
ms.assetid: 6a3cc771-1fef-4b79-baa1-c8d050e36d92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2acf76d77e69df41b7fbd3fb83fbd232dfdfd03682d39681e1f2a4fa9f2d19ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118480091"
---
# <a name="creating-a-notification-sink"></a>Création d’un récepteur de notification

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

Pour être averti des événements par Microsoft Agent, vous devez implémenter l’interface [**IAgentNotifySink**](events.md)ou [**IAgentNotifySinkEx**](iagentnotifysinkex.md) , puis créer et inscrire un objet de ce type suivant les conventions com :


```
// Create a notification sink

pSinkEx = new AgentNotifySinkEx;

pSinkEx->AddRef();

// And register it with Microsoft Agent

hRes = pAgentEx->Register((IUnknown *)pSinkEx, &lNotifySinkID);
```



N’oubliez pas d’annuler l’inscription de votre récepteur de notification lorsque votre application s’arrête et libère les interfaces de Microsoft Agent.

 

 




