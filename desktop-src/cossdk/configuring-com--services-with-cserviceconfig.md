---
description: Configuration des services COM+ avec CServiceConfig
ms.assetid: c44743a8-8b91-4e2a-9ba4-4cb6ae787999
title: Configuration des services COM+ avec CServiceConfig
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc8bbc6c3131347f450340863db70fd9b3999730
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748052"
---
# <a name="configuring-com-services-with-cserviceconfig"></a><span data-ttu-id="66482-103">Configuration des services COM+ avec CServiceConfig</span><span class="sxs-lookup"><span data-stu-id="66482-103">Configuring COM+ Services with CServiceConfig</span></span>

<span data-ttu-id="66482-104">La classe [**CServiceConfig**](cserviceconfig.md) est utilisée pour configurer les services com+ qui peuvent être utilisés sans composants.</span><span class="sxs-lookup"><span data-stu-id="66482-104">The [**CServiceConfig**](cserviceconfig.md) class is used to configure the COM+ services that can be used without components.</span></span> <span data-ttu-id="66482-105">Il agrège le marshaleur libre de threads, afin qu’il puisse être utilisé dans différents cloisonnements.</span><span class="sxs-lookup"><span data-stu-id="66482-105">It aggregates the free-threaded marshaler, so it can be used in different apartments.</span></span> <span data-ttu-id="66482-106">Pour configurer un service individuel, vous devez appeler [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour l’interface associée au service, puis appeler des méthodes sur cette interface pour établir la configuration appropriée.</span><span class="sxs-lookup"><span data-stu-id="66482-106">To configure an individual service, you must call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) for the interface associated with the service and then call methods on that interface to establish the appropriate configuration.</span></span> <span data-ttu-id="66482-107">Le tableau suivant décrit les interfaces qui sont implémentées par le biais de la classe **CServiceConfig** .</span><span class="sxs-lookup"><span data-stu-id="66482-107">The following table describes the interfaces that are implemented through the **CServiceConfig** class.</span></span>



| <span data-ttu-id="66482-108">Interface</span><span class="sxs-lookup"><span data-stu-id="66482-108">Interface</span></span>                                                                         | <span data-ttu-id="66482-109">Description</span><span class="sxs-lookup"><span data-stu-id="66482-109">Description</span></span>                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="66482-110">**IServiceInheritanceConfig**</span><span class="sxs-lookup"><span data-stu-id="66482-110">**IServiceInheritanceConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceinheritanceconfig)<br/>         | <span data-ttu-id="66482-111">Interface par défaut de la classe.</span><span class="sxs-lookup"><span data-stu-id="66482-111">The default interface for the class.</span></span> <span data-ttu-id="66482-112">Elle est utilisée pour initialiser rapidement un grand nombre des services COM+.</span><span class="sxs-lookup"><span data-stu-id="66482-112">It is used to quickly initialize many of the COM+ services.</span></span><br/>                                                                                              |
| [<span data-ttu-id="66482-113">**IServiceComTIIntrinsicsConfig**</span><span class="sxs-lookup"><span data-stu-id="66482-113">**IServiceComTIIntrinsicsConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicecomtiintrinsicsconfig)<br/> | <span data-ttu-id="66482-114">Utilisé pour configurer les informations intrinsèques de l’COM Transaction Integrator (COMTI).</span><span class="sxs-lookup"><span data-stu-id="66482-114">Used to configure the COM Transaction Integrator (COMTI) intrinsics information.</span></span> <span data-ttu-id="66482-115">COMTI permet aux développeurs d’intégrer des programmes de transaction basés sur des macroordinateurs à des applications basées sur des composants.</span><span class="sxs-lookup"><span data-stu-id="66482-115">COMTI allows developers to integrate mainframe-based transaction programs with component-based applications.</span></span><br/> |
| [<span data-ttu-id="66482-116">**IServiceIISIntrinsicsConfig**</span><span class="sxs-lookup"><span data-stu-id="66482-116">**IServiceIISIntrinsicsConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceiisintrinsicsconfig)<br/>     | <span data-ttu-id="66482-117">Utilisé pour configurer les informations intrinsèques du Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="66482-117">Used to configure the Internet Information Services (IIS) intrinsics information.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="66482-118">**IServicePartitionConfig**</span><span class="sxs-lookup"><span data-stu-id="66482-118">**IServicePartitionConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicepartitionconfig)<br/>             | <span data-ttu-id="66482-119">Utilisé pour configurer le mode d’utilisation des partitions COM+ avec les services.</span><span class="sxs-lookup"><span data-stu-id="66482-119">Used to configure how COM+ partitions are used with the services.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="66482-120">**IServiceSxSConfig**</span><span class="sxs-lookup"><span data-stu-id="66482-120">**IServiceSxSConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicesxsconfig)<br/>                         | <span data-ttu-id="66482-121">Utilisé pour configurer des assemblys côte à côte.</span><span class="sxs-lookup"><span data-stu-id="66482-121">Used to configure side-by-side assemblies.</span></span><br/>                                                                                                                                                    |
| [<span data-ttu-id="66482-122">**IServiceSynchronizationConfig**</span><span class="sxs-lookup"><span data-stu-id="66482-122">**IServiceSynchronizationConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicesynchronizationconfig)<br/> | <span data-ttu-id="66482-123">Utilisé pour configurer les services de synchronisation COM+.</span><span class="sxs-lookup"><span data-stu-id="66482-123">Used to configure COM+ synchronization services.</span></span><br/>                                                                                                                                              |
| [<span data-ttu-id="66482-124">**IServiceThreadPoolConfig**</span><span class="sxs-lookup"><span data-stu-id="66482-124">**IServiceThreadPoolConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicethreadpoolconfig)<br/>           | <span data-ttu-id="66482-125">Utilisé pour configurer le pool de threads pour le service COM+.</span><span class="sxs-lookup"><span data-stu-id="66482-125">Used to configure the thread pool for the COM+ service.</span></span> <span data-ttu-id="66482-126">Le pool de threads ne peut être configuré que lors de l’utilisation de la fonction [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) .</span><span class="sxs-lookup"><span data-stu-id="66482-126">The thread pool can be configured only when using the [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) function.</span></span><br/>                          |
| [<span data-ttu-id="66482-127">**IServiceTrackerConfig**</span><span class="sxs-lookup"><span data-stu-id="66482-127">**IServiceTrackerConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicetrackerconfig)<br/>                 | <span data-ttu-id="66482-128">Utilisé pour configurer la propriété tracker.</span><span class="sxs-lookup"><span data-stu-id="66482-128">Used to configure the Tracker property.</span></span> <span data-ttu-id="66482-129">Tracker est un mécanisme de création de rapports utilisé par le code de surveillance pour surveiller le code en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="66482-129">Tracker is a reporting mechanism used by monitoring code to watch which code is running when.</span></span><br/>                                                         |
| [<span data-ttu-id="66482-130">**IServiceTransactionConfig**</span><span class="sxs-lookup"><span data-stu-id="66482-130">**IServiceTransactionConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicetransactionconfig)<br/>         | <span data-ttu-id="66482-131">Utilisé pour configurer le service de transactions COM+.</span><span class="sxs-lookup"><span data-stu-id="66482-131">Used to configure the COM+ transaction service.</span></span><br/>                                                                                                                                               |



 

## <a name="component-services-administrative-tool"></a><span data-ttu-id="66482-132">Outil d’administration Services de composants</span><span class="sxs-lookup"><span data-stu-id="66482-132">Component Services Administrative Tool</span></span>

<span data-ttu-id="66482-133">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="66482-133">Does not apply.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="66482-134">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="66482-134">Visual Basic</span></span>

<span data-ttu-id="66482-135">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="66482-135">Does not apply.</span></span>

## <a name="cc"></a><span data-ttu-id="66482-136">C/C++</span><span class="sxs-lookup"><span data-stu-id="66482-136">C/C++</span></span>

<span data-ttu-id="66482-137">Le fragment de code suivant illustre la création et la configuration d’un objet [**CServiceConfig**](cserviceconfig.md) pour utiliser des transactions com+.</span><span class="sxs-lookup"><span data-stu-id="66482-137">The following code fragment illustrates how to create and configure a [**CServiceConfig**](cserviceconfig.md) object to use COM+ transactions.</span></span>


```C++
// Create a CServiceConfig object.
HRESULT hr = CoCreateInstance(CLSID_CServiceConfig, NULL, CLSCTX_INPROC_SERVER, 
  IID_IUnknown, (void**)&pUnknownCSC);
if (FAILED(hr)) throw(hr);

// Query for the IServiceInheritanceConfig interface.
hr = pUnknownCSC->QueryInterface(IID_IServiceInheritanceConfig, 
  (void**)&pInheritanceConfig);
if (FAILED(hr)) throw(hr);

// Inherit the current context before using transactions.
hr = pInheritanceConfig->ContainingContextTreatment(CSC_Inherit);
if (FAILED(hr)) throw(hr);

// Query for the IServiceTransactionConfig interface.
hr = pUnknownCSC->QueryInterface(IID_IServiceTransactionConfig, 
  (void**)&pTransactionConfig);
if (FAILED(hr)) throw(hr);

// Configure transactions to always create a new one.
hr = pTransactionConfig->ConfigureTransaction(CSC_NewTransaction);
if (FAILED(hr)) throw(hr);

// Set the isolation level of the transactions to ReadCommitted.
hr = pTransactionConfig->IsolationLevel( 
  COMAdminTxIsolationLevelReadCommitted);
if (FAILED(hr)) throw(hr);

// Set the transaction time-out to 1 minute.
hr = pTransactionConfig->TransactionTimeout(60);
if (FAILED(hr)) throw(hr);

```



## <a name="related-topics"></a><span data-ttu-id="66482-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="66482-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66482-139">**CServiceConfig**</span><span class="sxs-lookup"><span data-stu-id="66482-139">**CServiceConfig**</span></span>](cserviceconfig.md)
</dt> <dt>

[<span data-ttu-id="66482-140">Utilisation des services COM+ via CoCreateActivity</span><span class="sxs-lookup"><span data-stu-id="66482-140">Using COM+ Services Through CoCreateActivity</span></span>](using-com--services-through-cocreateactivity.md)
</dt> <dt>

[<span data-ttu-id="66482-141">Utilisation des services COM+ via CoEnterServiceDomain et CoLeaveServiceDomain</span><span class="sxs-lookup"><span data-stu-id="66482-141">Using COM+ Services Through CoEnterServiceDomain and CoLeaveServiceDomain</span></span>](using-com--services-through-coenterservicedomain-and-coleaveservicedomain.md)
</dt> </dl>

 

