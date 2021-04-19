---
title: Annulation des appels de méthode
description: Avec l’introduction d’applications distribuées et basées sur le Web, certains appels de méthode peuvent prendre beaucoup de temps à retourner.
ms.assetid: 18228ff1-8c1c-430a-ae5f-0e9a56b0fe3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2e2a78f042e528036135df4865e8a454cd687da
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "106509474"
---
# <a name="canceling-method-calls"></a><span data-ttu-id="d91e4-103">Annulation des appels de méthode</span><span class="sxs-lookup"><span data-stu-id="d91e4-103">Canceling Method Calls</span></span>

<span data-ttu-id="d91e4-104">Avec l’introduction d’applications distribuées et basées sur le Web, certains appels de méthode peuvent prendre beaucoup de temps à retourner.</span><span class="sxs-lookup"><span data-stu-id="d91e4-104">With the introduction of distributed and Web-based applications, some method calls can take an unacceptably long time to return.</span></span> <span data-ttu-id="d91e4-105">La latence de la connexion réseau peut être élevée, l’ordinateur serveur peut servir de nombreux clients ou le composant serveur peut transmettre une grande quantité de données, par exemple un fichier multimédia.</span><span class="sxs-lookup"><span data-stu-id="d91e4-105">The latency of the network connection may be high, the server machine may be serving many clients, or the server component may be passing a large amount of data, such as a multimedia file.</span></span> <span data-ttu-id="d91e4-106">Les utilisateurs doivent être en mesure d’annuler une demande qui prend trop de temps et l’application doit être en mesure de gérer les demandes d’annulation et de poursuivre son autre travail.</span><span class="sxs-lookup"><span data-stu-id="d91e4-106">Users should be able to cancel a request that is taking too long, and the application should be able to handle cancellation requests and continue with its other work.</span></span> <span data-ttu-id="d91e4-107">Dans COM, vous pouvez utiliser l’interface [**IMessageFilter**](/windows/desktop/api/ObjIdl/nn-objidl-imessagefilter) pour annuler un appel en attente qui provient d’un cloisonnement à thread unique.</span><span class="sxs-lookup"><span data-stu-id="d91e4-107">In COM, you can use the [**IMessageFilter**](/windows/desktop/api/ObjIdl/nn-objidl-imessagefilter) interface to cancel a pending call that originates from a single-threaded apartment.</span></span>

<span data-ttu-id="d91e4-108">Lorsqu’un appel est marshalé, le proxy crée un objet Cancel, qui implémente l’interface [**ICancelMethodCalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls) .</span><span class="sxs-lookup"><span data-stu-id="d91e4-108">When a call is marshaled, the proxy creates a cancel object, which implements the [**ICancelMethodCalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls) interface.</span></span> <span data-ttu-id="d91e4-109">L’objet Cancel est associé à l’appel et au thread sur lequel l’appel est en attente.</span><span class="sxs-lookup"><span data-stu-id="d91e4-109">The cancel object is associated with both the call and the thread on which the call is pending.</span></span>

<span data-ttu-id="d91e4-110">Pour annuler l’appel en attente, le client passe une demande d’annulation via l’objet Cancel, qui gère les détails de la notification à l’objet serveur que l’appel a été annulé.</span><span class="sxs-lookup"><span data-stu-id="d91e4-110">To cancel the pending call, the client passes a cancellation request through the cancel object, which handles the details of notifying the server object that the call has been canceled.</span></span> <span data-ttu-id="d91e4-111">Si la méthode appelée n’a pas été retournée, l’objet serveur, lors de la détection de la demande d’annulation, nettoie toutes les ressources de programme qu’il a allouées et notifie son client, en retournant une valeur **HRESULT** appropriée, qu’il a annulé l’exécution de l’appel.</span><span class="sxs-lookup"><span data-stu-id="d91e4-111">If the called method has not returned, the server object, on detecting the cancellation request, cleans up any program resources it has allocated and notifies its client, by returning an appropriate **HRESULT** value, that it canceled execution of the call.</span></span> <span data-ttu-id="d91e4-112">Si la méthode appelée a déjà été retournée, l’objet Cancel avertit le client.</span><span class="sxs-lookup"><span data-stu-id="d91e4-112">If the called method has already returned, the cancel object notifies the client.</span></span> <span data-ttu-id="d91e4-113">Dans les deux cas, le thread client est débloqué et peut continuer le traitement.</span><span class="sxs-lookup"><span data-stu-id="d91e4-113">In either case, the client thread is unblocked and can continue processing.</span></span>

<span data-ttu-id="d91e4-114">La manière dont l’objet serveur répond à une demande d’annulation est à la discrétion de l’implémenteur de serveur, mais le thread appelant sur le client est toujours débloqué et ignore les résultats que le serveur tente de lui passer.</span><span class="sxs-lookup"><span data-stu-id="d91e4-114">How the server object responds to a cancellation request is at the discretion of the server implementer, but the calling thread on the client will always be unblocked and will ignore whatever results the server tries to pass to it.</span></span> <span data-ttu-id="d91e4-115">Les objets Cancel permettent de demander l’annulation d’une méthode en cours d’exécution, mais il n’existe aucune garantie que l’objet serveur arrête le traitement de l’appel.</span><span class="sxs-lookup"><span data-stu-id="d91e4-115">Cancel objects provide a means to request that a currently running method be canceled, but there is no guarantee that the server object will stop processing the call.</span></span> <span data-ttu-id="d91e4-116">Par exemple, l’appel peut avoir déjà été retourné, ou l’objet serveur peut ne pas prendre en charge les objets Cancel.</span><span class="sxs-lookup"><span data-stu-id="d91e4-116">For example, the call may have already returned, or the server object may not support cancel objects.</span></span>

<span data-ttu-id="d91e4-117">COM fournit automatiquement une implémentation standard d’objets CANCEL pour les objets client et les interfaces qui utilisent le marshaling standard.</span><span class="sxs-lookup"><span data-stu-id="d91e4-117">COM automatically provides a standard implementation of cancel objects for client objects and interfaces that use standard marshaling.</span></span> <span data-ttu-id="d91e4-118">Pour les objets et les interfaces qui utilisent le marshaling personnalisé, vous devez implémenter votre propre objet d’annulation.</span><span class="sxs-lookup"><span data-stu-id="d91e4-118">For objects and interfaces that use custom marshaling, you will need to implement your own cancel object.</span></span>

<span data-ttu-id="d91e4-119">À ce stade, les objets Cancel gèrent uniquement les appels synchrones.</span><span class="sxs-lookup"><span data-stu-id="d91e4-119">At this time, cancel objects handle only synchronous calls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d91e4-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d91e4-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d91e4-121">Annulation d’un appel asynchrone</span><span class="sxs-lookup"><span data-stu-id="d91e4-121">Canceling an Asynchronous Call</span></span>](canceling-an-asynchronous-call.md)
</dt> <dt>

[<span data-ttu-id="d91e4-122">**CoGetCancelObject**</span><span class="sxs-lookup"><span data-stu-id="d91e4-122">**CoGetCancelObject**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcancelobject)
</dt> <dt>

[<span data-ttu-id="d91e4-123">**CoSetCancelObject**</span><span class="sxs-lookup"><span data-stu-id="d91e4-123">**CoSetCancelObject**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cosetcancelobject)
</dt> <dt>

[<span data-ttu-id="d91e4-124">**CoTestCancel**</span><span class="sxs-lookup"><span data-stu-id="d91e4-124">**CoTestCancel**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotestcancel)
</dt> </dl>

 

 