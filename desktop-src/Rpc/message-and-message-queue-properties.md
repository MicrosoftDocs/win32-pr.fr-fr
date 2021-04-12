---
title: Propriétés des messages et des files d’attente de messages
description: Un message contient des propriétés qui spécifient une étiquette, un corps de message et un certain nombre d’options.
ms.assetid: d0c9126e-a2c6-4d70-b87a-154a570899fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0139a588b52f1de1de43d8ec50aebdaf57b995ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310517"
---
# <a name="message-and-message-queue-properties"></a><span data-ttu-id="1bce9-103">Propriétés des messages et des files d’attente de messages</span><span class="sxs-lookup"><span data-stu-id="1bce9-103">Message and Message Queue Properties</span></span>

<span data-ttu-id="1bce9-104">Un message contient des propriétés qui spécifient une étiquette, un corps de message et un certain nombre d’options.</span><span class="sxs-lookup"><span data-stu-id="1bce9-104">A message has properties, which specify a label, a message body, and a number of options.</span></span> <span data-ttu-id="1bce9-105">Les options de propriété de message peuvent inclure la qualité de service, la priorité, la journalisation, les niveaux de confidentialité et d’authentification, ainsi que la durée de vie du message.</span><span class="sxs-lookup"><span data-stu-id="1bce9-105">Message property options can include quality of service, priority, journaling, privacy and authentication levels, and the lifetime of the message.</span></span> <span data-ttu-id="1bce9-106">Dans les applications de mise en file d’attente de messages conventionnels (non RPC), vous spécifiez ces propriétés en appelant les fonctions de l’API MSMQ ou les méthodes de l’objet COM, qui sont décrites dans la documentation du kit de développement logiciel (SDK) MSMQ.</span><span class="sxs-lookup"><span data-stu-id="1bce9-106">In conventional (non-RPC) message-queuing applications, you specify these properties by calling the MSMQ API functions or COM object methods, which are described in the MSMQ SDK documentation.</span></span> <span data-ttu-id="1bce9-107">Les applications clientes RPC peuvent définir certaines propriétés pour les appels de procédure distante en appelant [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) et [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span><span class="sxs-lookup"><span data-stu-id="1bce9-107">RPC client applications can set certain properties for remote procedure calls by calling [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) and [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span></span> <span data-ttu-id="1bce9-108">Une fois définis, les propriétés restent en vigueur pour chaque message jusqu’à ce que l’application cliente les réinitialise.</span><span class="sxs-lookup"><span data-stu-id="1bce9-108">Once set, the properties remain in effect for each message until the client application resets them.</span></span>

<span data-ttu-id="1bce9-109">Une file d’attente de messages a son propre ensemble de propriétés, à l’exception de celles des messages.</span><span class="sxs-lookup"><span data-stu-id="1bce9-109">A message queue has its own set of properties, apart from those of the messages.</span></span> <span data-ttu-id="1bce9-110">Ces propriétés identifient de façon unique une file d’attente et définissent la classe de service fournie par la file d’attente, les niveaux de confidentialité et d’authentification requis pour les messages de cette file d’attente, et si les messages doivent faire partie d’une transaction distribuée.</span><span class="sxs-lookup"><span data-stu-id="1bce9-110">These properties uniquely identify a queue and define the class of service that the queue provides, the privacy and authentication levels required for messages in this queue, and whether the messages are to be part of a distributed transaction.</span></span> <span data-ttu-id="1bce9-111">Comme avec les propriétés de message, vous spécifiez les propriétés d’une file d’attente de messages en appelant les fonctions de l’API MSMQ ou les méthodes de l’objet COM, qui sont décrites dans la documentation MSMQ.</span><span class="sxs-lookup"><span data-stu-id="1bce9-111">As with message properties, you specify the properties of a message queue by calling the MSMQ API functions or COM object methods, which are described in the MSMQ documentation.</span></span> <span data-ttu-id="1bce9-112">Toutefois, une application serveur RPC peut spécifier des propriétés de sa propre file d’attente de réception lorsqu’elle appelle [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) pour établir la liaison.</span><span class="sxs-lookup"><span data-stu-id="1bce9-112">However, an RPC server application can specify properties of its own receive queue when it calls [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) to establish the binding.</span></span>

 

 




