---
title: Création d’un récepteur de notification
description: Création d’un récepteur de notification
ms.assetid: 6a3cc771-1fef-4b79-baa1-c8d050e36d92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 481cdd754e545ef87e3c0dc44324d46e48baf044
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380355"
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

 

 




