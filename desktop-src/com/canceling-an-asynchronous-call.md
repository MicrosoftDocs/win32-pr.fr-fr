---
title: Annulation d’un appel asynchrone
description: Un client peut annuler un appel asynchrone en cours si l’objet d’appel implémente l’interface ICancelMethodCalls.
ms.assetid: 30a162f2-ce16-4ee6-8002-59216ac0e59a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 775b187f1abd3fca43ba907d92f6eabd926e4608
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104102424"
---
# <a name="canceling-an-asynchronous-call"></a><span data-ttu-id="a157c-103">Annulation d’un appel asynchrone</span><span class="sxs-lookup"><span data-stu-id="a157c-103">Canceling an Asynchronous Call</span></span>

<span data-ttu-id="a157c-104">Un client peut annuler un appel asynchrone en cours si l’objet d’appel implémente l’interface [**ICancelMethodCalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls) .</span><span class="sxs-lookup"><span data-stu-id="a157c-104">A client can cancel an asynchronous call that is in progress if the call object implements the [**ICancelMethodCalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls) interface.</span></span> <span data-ttu-id="a157c-105">Pour les objets qui utilisent le marshaling standard, **ICancelMethodCalls** est toujours disponible pour les appels marshalés.</span><span class="sxs-lookup"><span data-stu-id="a157c-105">For objects that use standard marshaling, **ICancelMethodCalls** is always available for marshaled calls.</span></span> <span data-ttu-id="a157c-106">Pour les objets qui utilisent le marshaling personnalisé ou pour les appels aux objets serveur au sein du même cloisonnement, cette fonctionnalité est disponible uniquement si l’objet d’appel implémente **ICancelMethodCalls**.</span><span class="sxs-lookup"><span data-stu-id="a157c-106">For objects that use custom marshaling or for calls to server objects within the same apartment, this functionality is available only if the call object implements **ICancelMethodCalls**.</span></span>

<span data-ttu-id="a157c-107">Le client peut annuler l’appel à tout moment, à partir de lorsque la méthode Begin \_ est appelée jusqu’à ce que la méthode Finish soit \_ retournée.</span><span class="sxs-lookup"><span data-stu-id="a157c-107">The client can cancel the call at any time, from when the Begin\_ method is called until the Finish\_ method returns.</span></span> <span data-ttu-id="a157c-108">Si le client annule l’appel avant d’appeler la \_ méthode Finish, il doit appeler la \_ méthode Finish pour nettoyer l’état de l’objet d’appel.</span><span class="sxs-lookup"><span data-stu-id="a157c-108">If the client cancels the call before calling the Finish\_ method, it must call the Finish\_ method to clean up the state of the call object.</span></span> <span data-ttu-id="a157c-109">Tant que le client n’a pas effectué cette opération, tous les appels à toute \_ méthode Begin sur l’objet Call renverront l' \_ appel E RPC E \_ \_ en attente.</span><span class="sxs-lookup"><span data-stu-id="a157c-109">Until the client has done so, any calls to any Begin\_ method on the call object will return RPC\_E\_CALL\_PENDING.</span></span>

<span data-ttu-id="a157c-110">**Pour annuler un appel asynchrone**</span><span class="sxs-lookup"><span data-stu-id="a157c-110">**To cancel an asynchronous call**</span></span>

1.  <span data-ttu-id="a157c-111">Interrogez l’objet d’appel pour [**ICancelMethodCalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls).</span><span class="sxs-lookup"><span data-stu-id="a157c-111">Query the call object for [**ICancelMethodCalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls).</span></span>

2.  <span data-ttu-id="a157c-112">Appelez [**ICancelMethodCalls :: Cancel**](/windows/win32/api/objidlbase/nf-objidlbase-icancelmethodcalls-cancel), puis appelez [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) pour libérer le pointeur obtenu par l’appel [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="a157c-112">Call [**ICancelMethodCalls::Cancel**](/windows/win32/api/objidlbase/nf-objidlbase-icancelmethodcalls-cancel), and then call [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) to release the pointer obtained by the [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) call in step 1.</span></span>

3.  <span data-ttu-id="a157c-113">Si le client n’a pas encore appelé la \_ méthode Finish, appelez-le maintenant.</span><span class="sxs-lookup"><span data-stu-id="a157c-113">If the client has not called the Finish\_ method already, call it now.</span></span>

<span data-ttu-id="a157c-114">Il n’y a aucune garantie que le serveur n’a pas réellement arrêté l’exécution de l’appel.</span><span class="sxs-lookup"><span data-stu-id="a157c-114">There is no guarantee that the server actually stopped execution of the call.</span></span> <span data-ttu-id="a157c-115">Si le travail supplémentaire du client dépend de l’état du serveur dont l’appel peut ou non avoir changé, le client doit déterminer cet état avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="a157c-115">If the client's further work depends on some server state that the call may or may not have changed, the client should determine that state before proceeding.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a157c-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a157c-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a157c-117">Exécution d’un appel asynchrone</span><span class="sxs-lookup"><span data-stu-id="a157c-117">Making an Asynchronous Call</span></span>](making-an-asynchronous-call.md)
</dt> </dl>

 

 