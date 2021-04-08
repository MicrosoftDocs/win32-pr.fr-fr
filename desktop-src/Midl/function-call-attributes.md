---
title: Attributs d’appel de fonction
description: Les programmes peuvent utiliser ces attributs sur des fonctions individuelles au sein de l’interface et affectent uniquement cette fonction.
ms.assetid: c54dbcd9-46c9-4755-b4a8-0f78068920b7
keywords:
- IDL MIDL, attributs, appel de fonction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4d53407abf464d7b201c49d9cb2b1d3f3625b9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675589"
---
# <a name="function-call-attributes"></a><span data-ttu-id="71bd3-104">Attributs d’appel de fonction</span><span class="sxs-lookup"><span data-stu-id="71bd3-104">Function Call Attributes</span></span>

<span data-ttu-id="71bd3-105">Les programmes peuvent utiliser ces attributs sur des fonctions individuelles au sein de l’interface et affectent uniquement cette fonction.</span><span class="sxs-lookup"><span data-stu-id="71bd3-105">Programs can use these attributes on individual functions within the interface, and affect only that function.</span></span>



| <span data-ttu-id="71bd3-106">Attribut</span><span class="sxs-lookup"><span data-stu-id="71bd3-106">Attribute</span></span>                        | <span data-ttu-id="71bd3-107">Utilisation</span><span class="sxs-lookup"><span data-stu-id="71bd3-107">Usage</span></span>                                                                                                                                                                                                                                                      |
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="71bd3-108">**Message**</span><span class="sxs-lookup"><span data-stu-id="71bd3-108">**message**</span></span>](message.md)       | <span data-ttu-id="71bd3-109">L’appel de procédure distante doit être traité comme un message asynchrone du client au serveur.</span><span class="sxs-lookup"><span data-stu-id="71bd3-109">The remote procedure call is to be treated as an asynchronous message from the client to the server.</span></span> <span data-ttu-id="71bd3-110">Le client effectue l’appel et le retourne immédiatement, tandis que l’appel réel est géré par le transport de mise en file d’attente de messages ([**ncadg \_ MQ**](ncadg-mq.md)).</span><span class="sxs-lookup"><span data-stu-id="71bd3-110">The client makes the call and returns immediately, while the actual call is handled by the message-queuing transport ([**ncadg\_mq**](ncadg-mq.md)).</span></span> |
| [<span data-ttu-id="71bd3-111">**environ**</span><span class="sxs-lookup"><span data-stu-id="71bd3-111">**maybe**</span></span>](maybe.md)           | <span data-ttu-id="71bd3-112">Le client qui effectue cet appel de procédure distante n’attend aucune réponse indiquant la remise ou l’achèvement de l’appel.</span><span class="sxs-lookup"><span data-stu-id="71bd3-112">The client making this remote procedure call does not expect any response indicating delivery or completion of the call.</span></span> <span data-ttu-id="71bd3-113">Cela diffère des opérations de [**message**](message.md) quand aucune réponse n’est attendue, mais que la remise est garantie.</span><span class="sxs-lookup"><span data-stu-id="71bd3-113">This is in contrast to [**message**](message.md) operations where no response is expected but the delivery is guaranteed.</span></span>        |
| [<span data-ttu-id="71bd3-114">**diffusion**</span><span class="sxs-lookup"><span data-stu-id="71bd3-114">**broadcast**</span></span>](broadcast.md)   | <span data-ttu-id="71bd3-115">L’appel de procédure distante doit être envoyé à tous les serveurs sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="71bd3-115">The remote procedure call is to be sent to all of the servers on the network.</span></span> <span data-ttu-id="71bd3-116">Le client accepte le premier retour, les réponses suivantes provenant d’autres serveurs sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="71bd3-116">The client accepts the first return, subsequent replies from other servers are discarded.</span></span>                                                                                    |
| [<span data-ttu-id="71bd3-117">**idempotent**</span><span class="sxs-lookup"><span data-stu-id="71bd3-117">**idempotent**</span></span>](idempotent.md) | <span data-ttu-id="71bd3-118">L’appel ne change pas d’État et retourne les mêmes informations chaque fois qu’il est appelé avec les mêmes paramètres d’entrée.</span><span class="sxs-lookup"><span data-stu-id="71bd3-118">The call does not change state and returns the same information each time it is called with the same input parameters.</span></span>                                                                                                                                     |
| [<span data-ttu-id="71bd3-119">**rappel**</span><span class="sxs-lookup"><span data-stu-id="71bd3-119">**callback**</span></span>](callback.md)     | <span data-ttu-id="71bd3-120">Désigne une fonction qui réside dans l’application cliente, que le serveur peut appeler pour obtenir des informations à partir du client.</span><span class="sxs-lookup"><span data-stu-id="71bd3-120">Designates a function that resides in the client application, which the server can call to obtain information from the client.</span></span>                                                                                                                             |
| [<span data-ttu-id="71bd3-121">**appeler \_ en tant que**</span><span class="sxs-lookup"><span data-stu-id="71bd3-121">**call\_as**</span></span>](call-as.md)      | <span data-ttu-id="71bd3-122">Mappe une fonction qui n’est pas accessible à distance à un appel de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="71bd3-122">Maps a nonremotable function to a remote procedure call.</span></span>                                                                                                                                                                                                   |
| [<span data-ttu-id="71bd3-123">**localisé**</span><span class="sxs-lookup"><span data-stu-id="71bd3-123">**local**</span></span>](local.md)           | <span data-ttu-id="71bd3-124">Désigne une procédure locale pour laquelle MIDL ne génère pas de code stub.</span><span class="sxs-lookup"><span data-stu-id="71bd3-124">Designates a local procedure for which MIDL does not generate stub code.</span></span>                                                                                                                                                                                   |



 

<span data-ttu-id="71bd3-125">Sur les interfaces qui ne sont pas des [**objets**](object.md) , vous pouvez également appliquer l’attribut de [**\_ handle de contexte**](context-handle.md) à une fonction pour spécifier les caractéristiques de la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="71bd3-125">On non-[**object**](object.md) interfaces, you can also apply the [**context\_handle**](context-handle.md) attribute to a function to specify characteristics of the return value.</span></span>

 

 




