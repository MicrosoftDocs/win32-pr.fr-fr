---
description: Erreurs de composants en file d’attente
ms.assetid: 29a1bf52-7252-4f8a-bdb7-61b152fb907e
title: Erreurs de composants en file d’attente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 422ea9c7ff77f2d69633d6db8b8d48c63fabc071
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514122"
---
# <a name="queued-components-errors"></a><span data-ttu-id="063c8-103">Erreurs de composants en file d’attente</span><span class="sxs-lookup"><span data-stu-id="063c8-103">Queued Components Errors</span></span>

<span data-ttu-id="063c8-104">Lorsqu’un appel à un composant en file d’attente échoue, soit parce qu’il n’a pas pu être transmis au serveur (échec côté client), soit parce qu’il n’a pas pu s’exécuter lorsqu’il est arrivé (échec côté serveur), le message d' [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) correspondant est appelé *message incohérent*.</span><span class="sxs-lookup"><span data-stu-id="063c8-104">When a call to a queued component fails, either because it could not be transmitted to the server (a client-side failure) or because it failed to execute when it arrived (a server-side failure), the corresponding [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) message is called a *poison message*.</span></span>

<span data-ttu-id="063c8-105">Le service COM+ Queued Components gère les messages incohérents à l’aide d’une série de files d’attente de nouvelles tentatives.</span><span class="sxs-lookup"><span data-stu-id="063c8-105">The COM+ queued components service handles poison messages by using a series of retry queues.</span></span> <span data-ttu-id="063c8-106">Après plusieurs tentatives, le message est déplacé vers une file d’attente Rest finale.</span><span class="sxs-lookup"><span data-stu-id="063c8-106">After several retries, the message is moved to a final resting queue.</span></span> <span data-ttu-id="063c8-107">Les messages restent dans la file d’attente Rest jusqu’à ce qu’ils soient déplacés manuellement à l’aide de l’utilitaire de déplacement de messages des composants en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="063c8-107">Messages stay in the resting queue until they are moved manually by using the queued components message mover utility.</span></span> <span data-ttu-id="063c8-108">Pour plus d’informations sur l’utilisation du Data Mover, consultez [gestion des erreurs](handling-errors-in-queued-components.md).</span><span class="sxs-lookup"><span data-stu-id="063c8-108">For more information about using the message mover, see [Handling Errors](handling-errors-in-queued-components.md).</span></span>

<span data-ttu-id="063c8-109">Vous trouverez des descriptions détaillées de la séquence d’événements qui se produit pour différents types d’erreurs dans les rubriques décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="063c8-109">Detailed descriptions of the sequence of events that occurs for various sorts of errors can be found in the topics described in the following table.</span></span>



| <span data-ttu-id="063c8-110">Rubrique</span><span class="sxs-lookup"><span data-stu-id="063c8-110">Topic</span></span>                                                                             | <span data-ttu-id="063c8-111">Description</span><span class="sxs-lookup"><span data-stu-id="063c8-111">Description</span></span>                                                                                                             |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="063c8-112">Erreurs côté serveur</span><span class="sxs-lookup"><span data-stu-id="063c8-112">Server-Side Errors</span></span>](server-side-errors.md)<br/>                           | <span data-ttu-id="063c8-113">Décrit en détail la réponse du service COM+ Queued Components à une défaillance côté serveur.</span><span class="sxs-lookup"><span data-stu-id="063c8-113">Describes in detail the response of the COM+ queued components service to a server-side failure.</span></span><br/>             |
| [<span data-ttu-id="063c8-114">Erreurs côté client</span><span class="sxs-lookup"><span data-stu-id="063c8-114">Client-Side Errors</span></span>](client-side-errors.md)<br/>                           | <span data-ttu-id="063c8-115">Décrit en détail la réponse du service COM+ Queued Components à une défaillance côté client.</span><span class="sxs-lookup"><span data-stu-id="063c8-115">Describes in detail the response of the COM+ queued components service to a client-side failure.</span></span><br/>             |
| [<span data-ttu-id="063c8-116">Échecs de Client-Side persistant</span><span class="sxs-lookup"><span data-stu-id="063c8-116">Persistent Client-Side Failures</span></span>](persistent-client-side-failures.md)<br/> | <span data-ttu-id="063c8-117">Décrit dans les détails la réponse du service des composants en file d’attente COM+ aux défaillances répétées côté client.</span><span class="sxs-lookup"><span data-stu-id="063c8-117">Describes in the detail the response of the COM+ queued components service to repeated client-side failures.</span></span><br/> |



 

 

 




