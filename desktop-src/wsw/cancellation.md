---
title: Annulation
description: La plupart des opérations dans WWSAPI peuvent être annulées pendant l’exécution.
ms.assetid: d73d76e1-bd78-40ce-9f92-e282b6b127ce
keywords:
- Annulation des services Web pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e979455e898922dfb7c81381c1f1aafd455274
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104316848"
---
# <a name="cancellation"></a><span data-ttu-id="7cb04-106">Annulation</span><span class="sxs-lookup"><span data-stu-id="7cb04-106">Cancellation</span></span>

<span data-ttu-id="7cb04-107">La plupart des opérations dans WWSAPI peuvent être annulées pendant l’exécution.</span><span class="sxs-lookup"><span data-stu-id="7cb04-107">Most of operations in the WWSAPI can be canceled during execution.</span></span>

<span data-ttu-id="7cb04-108">La fonction que vous utilisez pour annuler une opération dépend de l’objet affecté.</span><span class="sxs-lookup"><span data-stu-id="7cb04-108">Which function you use to cancel an operation depends on the object affected.</span></span>

| <span data-ttu-id="7cb04-109">Fonction</span><span class="sxs-lookup"><span data-stu-id="7cb04-109">Function</span></span>                                           | <span data-ttu-id="7cb04-110">Description</span><span class="sxs-lookup"><span data-stu-id="7cb04-110">Description</span></span>                                                                                                            |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7cb04-111">**WsAbortChannel**</span><span class="sxs-lookup"><span data-stu-id="7cb04-111">**WsAbortChannel**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel)           | <span data-ttu-id="7cb04-112">Annule toutes les entrées et sorties en attente sur un canal spécifié et définit l’état du canal sur WS \_ Channel \_ State \_ Faulted.</span><span class="sxs-lookup"><span data-stu-id="7cb04-112">Cancels all pending input and output on a specified channel and sets the channel state to WS\_CHANNEL\_STATE\_FAULTED.</span></span> |
| [<span data-ttu-id="7cb04-113">**WsAbortListener**</span><span class="sxs-lookup"><span data-stu-id="7cb04-113">**WsAbortListener**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener)         | <span data-ttu-id="7cb04-114">Annule toutes les entrées et sorties en attente sur un écouteur spécifié.</span><span class="sxs-lookup"><span data-stu-id="7cb04-114">Cancels all pending input and output on a specified listener.</span></span>                                                          |
| [<span data-ttu-id="7cb04-115">**WsAbortServiceProxy**</span><span class="sxs-lookup"><span data-stu-id="7cb04-115">**WsAbortServiceProxy**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabortserviceproxy) | <span data-ttu-id="7cb04-116">Annule toutes les entrées et sorties en attente sur un proxy de service spécifié.</span><span class="sxs-lookup"><span data-stu-id="7cb04-116">Cancels all pending input and output on a specified service proxy.</span></span>                                                     |
| [<span data-ttu-id="7cb04-117">**WsAbortServiceHost**</span><span class="sxs-lookup"><span data-stu-id="7cb04-117">**WsAbortServiceHost**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabortservicehost)   | <span data-ttu-id="7cb04-118">Interrompt et interrompt les opérations en cours sur l’hôte de service.</span><span class="sxs-lookup"><span data-stu-id="7cb04-118">Interrupts and discontinues current operations on the service host.</span></span>                                                    |
| [<span data-ttu-id="7cb04-119">**WsAbandonCall**</span><span class="sxs-lookup"><span data-stu-id="7cb04-119">**WsAbandonCall**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)             | <span data-ttu-id="7cb04-120">Abandonne un appel, un appel spécifié sur un proxy de service spécifié.</span><span class="sxs-lookup"><span data-stu-id="7cb04-120">Abandons a call, a specified call on a specified service proxy.</span></span>                                                        |



 

<span data-ttu-id="7cb04-121">Pour plus d’informations sur les annulations qui affectent les [opérations de service côté serveur](server-side-service-operations.md) et les rappels de modèle de service, consultez [appel d’annulation](call-cancellation.md).</span><span class="sxs-lookup"><span data-stu-id="7cb04-121">For information on cancellations that affect [server side service operations](server-side-service-operations.md) and service-model callbacks, see [Call Cancellation](call-cancellation.md).</span></span>


 

 




