---
description: Implémentation d’un distributeur de ressources COM+
ms.assetid: 083c5962-f55a-435a-964e-fdc868f9bd3d
title: Implémentation d’un distributeur de ressources COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a81e189f3bfc5025bc949ef6e5bc82bf9408c339
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111434"
---
# <a name="implementing-a-com-resource-dispenser"></a><span data-ttu-id="820e4-103">Implémentation d’un distributeur de ressources COM+</span><span class="sxs-lookup"><span data-stu-id="820e4-103">Implementing a COM+ Resource Dispenser</span></span>

<span data-ttu-id="820e4-104">Les étapes suivantes décrivent une procédure générale pour l’implémentation d’un distributeur de ressources COM+ :</span><span class="sxs-lookup"><span data-stu-id="820e4-104">The following steps outline a general procedure for implementing a COM+ resource dispenser:</span></span>

1.  <span data-ttu-id="820e4-105">Choisissez un format de **RESTYPID** qui catégorise les différences entre les ressources.</span><span class="sxs-lookup"><span data-stu-id="820e4-105">Decide on **RESTYPID** format that categorizes how your resources differ from each other.</span></span>

2.  <span data-ttu-id="820e4-106">Utilisez respectivement le fichier d’en-tête et la bibliothèque mtxdm. h et mtxdm. lib.</span><span class="sxs-lookup"><span data-stu-id="820e4-106">Use the Mtxdm.h and Mtxdm.lib header file and library, respectively.</span></span>

3.  <span data-ttu-id="820e4-107">Générez une DLL qui implémente l’interface [**IDispenserDriver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver) et l’API que vous souhaitez exposer aux applications.</span><span class="sxs-lookup"><span data-stu-id="820e4-107">Build a DLL that implements the [**IDispenserDriver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver) interface and the API you want to expose to applications.</span></span>

4.  <span data-ttu-id="820e4-108">Dans le démarrage ([*DllMain*](/windows/desktop/Dlls/dllmain) ou premier appel à l’API du distributeur), appelez la fonction [**GetDispenserManager**](/windows/desktop/api/MtxDM/nf-mtxdm-getdispensermanager) .</span><span class="sxs-lookup"><span data-stu-id="820e4-108">In the startup ([*DllMain*](/windows/desktop/Dlls/dllmain) or first call to the dispenser API), call the [**GetDispenserManager**](/windows/desktop/api/MtxDM/nf-mtxdm-getdispensermanager) function.</span></span> <span data-ttu-id="820e4-109">Cela retourne un pointeur vers l’interface [**IDispenserManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispensermanager) du gestionnaire du distributeur.</span><span class="sxs-lookup"><span data-stu-id="820e4-109">This returns a pointer to the dispenser manager's [**IDispenserManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispensermanager) interface.</span></span>

5.  <span data-ttu-id="820e4-110">Appelez [**IDispenserManager :: RegisterDispenser**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispensermanager-registerdispenser), en passant un pointeur vers votre implémentation de [**IDispenserDriver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver).</span><span class="sxs-lookup"><span data-stu-id="820e4-110">Call [**IDispenserManager::RegisterDispenser**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispensermanager-registerdispenser), passing a pointer to your implementation of [**IDispenserDriver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver).</span></span> <span data-ttu-id="820e4-111">Le gestionnaire de distribution crée alors un conteneur (gestionnaire de regroupement) pour votre distributeur de ressources, puis retourne le pointeur à votre interface [**IHolder**](/windows/desktop/api/ComSvcs/nn-comsvcs-iholder) .</span><span class="sxs-lookup"><span data-stu-id="820e4-111">This causes the dispenser manager to create a holder (pooling manager) for your resource dispenser and then return the pointer to your [**IHolder**](/windows/desktop/api/ComSvcs/nn-comsvcs-iholder) interface.</span></span>

6.  <span data-ttu-id="820e4-112">Stockez ce pointeur pour pouvoir appeler [**IHolder :: AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) et [**IHolder :: FreeResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-freeresource).</span><span class="sxs-lookup"><span data-stu-id="820e4-112">Store this pointer so that you can call [**IHolder::AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) and [**IHolder::FreeResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-freeresource).</span></span>

7.  <span data-ttu-id="820e4-113">Vous pouvez maintenant (en réponse aux appels à votre API) effectuer des appels à [**AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) et [**FreeResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-freeresource).</span><span class="sxs-lookup"><span data-stu-id="820e4-113">You can now (in response to calls to your API) make calls to [**AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) and [**FreeResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-freeresource).</span></span> <span data-ttu-id="820e4-114">**AllocResource** répond initialement en rappelant à votre méthode [**CreateResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-createresource) , mais les appels **AllocResource** ultérieurs sont desservis à partir du pool de ressources en augmentation.</span><span class="sxs-lookup"><span data-stu-id="820e4-114">**AllocResource** initially responds by calling back to your [**CreateResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-createresource) method, but later **AllocResource** calls are serviced from the growing pool of resources.</span></span>

## <a name="related-topics"></a><span data-ttu-id="820e4-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="820e4-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="820e4-116">Concepts du distributeur de ressources COM+</span><span class="sxs-lookup"><span data-stu-id="820e4-116">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> <dt>

[<span data-ttu-id="820e4-117">Interfaces du distributeur de ressources COM+</span><span class="sxs-lookup"><span data-stu-id="820e4-117">COM+ Resource Dispenser Interfaces</span></span>](com--resource-dispenser-interfaces.md)
</dt> </dl>

 

 
