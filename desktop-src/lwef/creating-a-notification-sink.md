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
# <a name="creating-a-notification-sink"></a><span data-ttu-id="73fa3-103">Création d’un récepteur de notification</span><span class="sxs-lookup"><span data-stu-id="73fa3-103">Creating a Notification Sink</span></span>

<span data-ttu-id="73fa3-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="73fa3-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="73fa3-105">Pour être averti des événements par Microsoft Agent, vous devez implémenter l’interface [**IAgentNotifySink**](events.md)ou [**IAgentNotifySinkEx**](iagentnotifysinkex.md) , puis créer et inscrire un objet de ce type suivant les conventions com :</span><span class="sxs-lookup"><span data-stu-id="73fa3-105">To be notified of events by Microsoft Agent, you must implement either the [**IAgentNotifySink**](events.md)or the [**IAgentNotifySinkEx**](iagentnotifysinkex.md) interface, and create and register an object of that type following COM conventions:</span></span>


```
// Create a notification sink

pSinkEx = new AgentNotifySinkEx;

pSinkEx->AddRef();

// And register it with Microsoft Agent

hRes = pAgentEx->Register((IUnknown *)pSinkEx, &lNotifySinkID);
```



<span data-ttu-id="73fa3-106">N’oubliez pas d’annuler l’inscription de votre récepteur de notification lorsque votre application s’arrête et libère les interfaces de Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="73fa3-106">Remember to unregister your notification sink when your application shuts down and releases Microsoft Agent's interfaces.</span></span>

 

 




