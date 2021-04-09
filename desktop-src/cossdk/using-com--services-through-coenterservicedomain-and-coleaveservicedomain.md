---
description: Utilisation des services COM+ via CoEnterServiceDomain et CoLeaveServiceDomain
ms.assetid: 763fb01e-5daf-4e9b-8ef1-9ae79c0a84cc
title: Utilisation des services COM+ via CoEnterServiceDomain et CoLeaveServiceDomain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36d87931628e177374dd07b40e9917a56c168a81
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111018"
---
# <a name="using-com-services-through-coenterservicedomain-and-coleaveservicedomain"></a><span data-ttu-id="3491b-103">Utilisation des services COM+ via CoEnterServiceDomain et CoLeaveServiceDomain</span><span class="sxs-lookup"><span data-stu-id="3491b-103">Using COM+ Services Through CoEnterServiceDomain and CoLeaveServiceDomain</span></span>

<span data-ttu-id="3491b-104">[**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) et [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain) sont utilisés ensemble pour entourer une zone de code qui s’exécute dans son propre contexte et peut utiliser des services com+ sans nécessiter de composants com+.</span><span class="sxs-lookup"><span data-stu-id="3491b-104">[**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) and [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain) are used together to surround an area of code that runs in its own context and can use COM+ services without the need for COM+ components.</span></span> <span data-ttu-id="3491b-105">Les services COM+ utilisés dans ce contexte sont configurés via l’objet [**CServiceConfig**](cserviceconfig.md) qui est transmis à **CoEnterServiceDomain**.</span><span class="sxs-lookup"><span data-stu-id="3491b-105">The COM+ services that are used in this context are configured through the [**CServiceConfig**](cserviceconfig.md) object that is passed in to **CoEnterServiceDomain**.</span></span> <span data-ttu-id="3491b-106">Le code entouré par **CoEnterServiceDomain** et **CoLeaveServiceDomain** se comporte comme s’il s’agissait d’une méthode appelée sur un objet créé dans ce contexte.</span><span class="sxs-lookup"><span data-stu-id="3491b-106">The code that is surrounded by **CoEnterServiceDomain** and **CoLeaveServiceDomain** behaves as though it were a method that is called on an object created within this context.</span></span>

<span data-ttu-id="3491b-107">Une application de script peut utiliser cette paire de fonctions pour fournir une prise en charge au moment de l’exécution des services COM+ sans composants.</span><span class="sxs-lookup"><span data-stu-id="3491b-107">A scripting application can use this pair of functions to provide run-time support of COM+ services without components.</span></span> <span data-ttu-id="3491b-108">Par exemple, une application de script peut être développée pour fournir des balises qui permettent aux créateurs de script d’entrer et de laisser un domaine de service au sein du script.</span><span class="sxs-lookup"><span data-stu-id="3491b-108">For example, a scripting application can be developed to provide tags that allow the script writers to enter and leave a service domain within the script.</span></span> <span data-ttu-id="3491b-109">Lorsque le moteur de script traite le script et rencontre les balises, il peut appeler [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) avec un objet [**CServiceConfig**](cserviceconfig.md) préconfiguré, exécuter le code nécessaire, puis appeler [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain).</span><span class="sxs-lookup"><span data-stu-id="3491b-109">When the scripting engine processes the script and encounters the tags, it can call [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) with a preconfigured [**CServiceConfig**](cserviceconfig.md) object, run the necessary code, and then call [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain).</span></span>

## <a name="component-services-administrative-tool"></a><span data-ttu-id="3491b-110">Outil d’administration Services de composants</span><span class="sxs-lookup"><span data-stu-id="3491b-110">Component Services Administrative Tool</span></span>

<span data-ttu-id="3491b-111">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="3491b-111">Does not apply.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="3491b-112">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="3491b-112">Visual Basic</span></span>

<span data-ttu-id="3491b-113">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="3491b-113">Does not apply.</span></span>

## <a name="cc"></a><span data-ttu-id="3491b-114">C/C++</span><span class="sxs-lookup"><span data-stu-id="3491b-114">C/C++</span></span>

<span data-ttu-id="3491b-115">Le fragment de code suivant illustre l’utilisation des services COM+ entre les appels à [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) et [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain).</span><span class="sxs-lookup"><span data-stu-id="3491b-115">The following code fragment illustrates how to use COM+ services between calls to [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) and [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain).</span></span> <span data-ttu-id="3491b-116">La gestion des erreurs est omise par souci de concision.</span><span class="sxs-lookup"><span data-stu-id="3491b-116">Error handling is omitted for brevity.</span></span> <span data-ttu-id="3491b-117">Ce fragment de code utilise l’objet [**CServiceConfig**](cserviceconfig.md) qui a été créé et configuré dans [Configuration des services com+ avec CServiceConfig](configuring-com--services-with-cserviceconfig.md).</span><span class="sxs-lookup"><span data-stu-id="3491b-117">This code fragment uses the [**CServiceConfig**](cserviceconfig.md) object that was created and configured in [Configuring COM+ Services with CServiceConfig](configuring-com--services-with-cserviceconfig.md).</span></span>


```C++
// A CServiceConfig object was created as follows:
// hr = CoCreateInstance(CLSID_CServiceConfig, NULL, CLSCTX_INPROC_SERVER, 
//   IID_IUnknown, (void**)&pUnknownCSC);

// Enter the Service Domain.
HRESULT hr = CoEnterServiceDomain(pUnknownCSC);
if (FAILED(hr)) throw(hr);

// Do the work that uses COM+ services here.
//DoMyWork();

// Leave the Service Domain.
CoLeaveServiceDomain(NULL);
```



## <a name="related-topics"></a><span data-ttu-id="3491b-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3491b-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3491b-119">**CoEnterServiceDomain**</span><span class="sxs-lookup"><span data-stu-id="3491b-119">**CoEnterServiceDomain**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain)
</dt> <dt>

[<span data-ttu-id="3491b-120">**CoLeaveServiceDomain**</span><span class="sxs-lookup"><span data-stu-id="3491b-120">**CoLeaveServiceDomain**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain)
</dt> <dt>

[<span data-ttu-id="3491b-121">Configuration des services COM+ avec CServiceConfig</span><span class="sxs-lookup"><span data-stu-id="3491b-121">Configuring COM+ Services with CServiceConfig</span></span>](configuring-com--services-with-cserviceconfig.md)
</dt> <dt>

[<span data-ttu-id="3491b-122">**CServiceConfig**</span><span class="sxs-lookup"><span data-stu-id="3491b-122">**CServiceConfig**</span></span>](cserviceconfig.md)
</dt> <dt>

[<span data-ttu-id="3491b-123">Utilisation des services COM+ via CoCreateActivity</span><span class="sxs-lookup"><span data-stu-id="3491b-123">Using COM+ Services Through CoCreateActivity</span></span>](using-com--services-through-cocreateactivity.md)
</dt> </dl>

 

 



