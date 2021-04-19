---
description: Spécifie et configure les services qui doivent être actifs dans le domaine de service entré lors de l’appel de CoCreateActivity ou CoEnterServiceDomain.
ms.assetid: f546ded4-255e-4565-b588-f36175902778
title: CServiceConfig, classe (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CServiceConfig
api_type:
- COM
ms.openlocfilehash: e0b48b05be4afa1d42dbc8a16c4b596a08aba859
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515352"
---
# <a name="cserviceconfig-class"></a><span data-ttu-id="9d14c-103">CServiceConfig, classe</span><span class="sxs-lookup"><span data-stu-id="9d14c-103">CServiceConfig class</span></span>

<span data-ttu-id="9d14c-104">Spécifie et configure les services qui doivent être actifs dans le domaine de service entré lors de l’appel de [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) ou [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain).</span><span class="sxs-lookup"><span data-stu-id="9d14c-104">Specifies and configures the services that are to be active in the service domain entered when calling either [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) or [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain).</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="9d14c-105">Quand implémenter</span><span class="sxs-lookup"><span data-stu-id="9d14c-105">When to implement</span></span>

<span data-ttu-id="9d14c-106">Cette classe est implémentée par COM+.</span><span class="sxs-lookup"><span data-stu-id="9d14c-106">This class is implemented by COM+.</span></span>



| <span data-ttu-id="9d14c-107">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9d14c-107">Requirement</span></span> | <span data-ttu-id="9d14c-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="9d14c-108">Value</span></span> |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d14c-109">CLSID</span><span class="sxs-lookup"><span data-stu-id="9d14c-109">CLSID</span></span>      | <span data-ttu-id="9d14c-110">CLSID \_ CServiceConfig</span><span class="sxs-lookup"><span data-stu-id="9d14c-110">CLSID\_CServiceConfig</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="9d14c-111">ProgID</span><span class="sxs-lookup"><span data-stu-id="9d14c-111">ProgID</span></span>     | <span data-ttu-id="9d14c-112">L "COMSVCS. CServiceConfig"</span><span class="sxs-lookup"><span data-stu-id="9d14c-112">L"COMSVCS.CServiceConfig"</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="9d14c-113">Interfaces</span><span class="sxs-lookup"><span data-stu-id="9d14c-113">Interfaces</span></span> | [<span data-ttu-id="9d14c-114">**IServiceComTIIntrinsicsConfig**</span><span class="sxs-lookup"><span data-stu-id="9d14c-114">**IServiceComTIIntrinsicsConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicecomtiintrinsicsconfig)<br/> [<span data-ttu-id="9d14c-115">**IServiceIISIntrinsicsConfig**</span><span class="sxs-lookup"><span data-stu-id="9d14c-115">**IServiceIISIntrinsicsConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceiisintrinsicsconfig)<br/> [<span data-ttu-id="9d14c-116">**IServiceInheritanceConfig**</span><span class="sxs-lookup"><span data-stu-id="9d14c-116">**IServiceInheritanceConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceinheritanceconfig)<br/> [<span data-ttu-id="9d14c-117">**IServicePartitionConfig**</span><span class="sxs-lookup"><span data-stu-id="9d14c-117">**IServicePartitionConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicepartitionconfig)<br/> [<span data-ttu-id="9d14c-118">**IServiceSxSConfig**</span><span class="sxs-lookup"><span data-stu-id="9d14c-118">**IServiceSxSConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicesxsconfig)<br/> [<span data-ttu-id="9d14c-119">**IServiceSynchronizationConfig**</span><span class="sxs-lookup"><span data-stu-id="9d14c-119">**IServiceSynchronizationConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicesynchronizationconfig)<br/> [<span data-ttu-id="9d14c-120">**IServiceThreadPoolConfig**</span><span class="sxs-lookup"><span data-stu-id="9d14c-120">**IServiceThreadPoolConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicethreadpoolconfig)<br/> [<span data-ttu-id="9d14c-121">**IServiceTrackerConfig**</span><span class="sxs-lookup"><span data-stu-id="9d14c-121">**IServiceTrackerConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicetrackerconfig)<br/> [<span data-ttu-id="9d14c-122">**IServiceTransactionConfig**</span><span class="sxs-lookup"><span data-stu-id="9d14c-122">**IServiceTransactionConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicetransactionconfig)<br/> |



 

## <a name="when-to-use"></a><span data-ttu-id="9d14c-123">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="9d14c-123">When to use</span></span>

<span data-ttu-id="9d14c-124">Utilisez cette classe pour configurer les services que vous souhaitez utiliser.</span><span class="sxs-lookup"><span data-stu-id="9d14c-124">Use this class to configure the services that you want to use.</span></span> <span data-ttu-id="9d14c-125">[**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) et [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) vous permettent d’utiliser les services configurés par cette classe sans avoir à lier ces services à un composant avant de les utiliser.</span><span class="sxs-lookup"><span data-stu-id="9d14c-125">[**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) and [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) enable you to use the services configured by this class without needing to tie those services to a component before using them.</span></span>

<span data-ttu-id="9d14c-126">Cette classe n’a pas été conçue pour être utilisée dans Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="9d14c-126">This class was not designed to be used in Visual Basic.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d14c-127">Notes</span><span class="sxs-lookup"><span data-stu-id="9d14c-127">Remarks</span></span>

<span data-ttu-id="9d14c-128">Pour créer cet objet, appelez [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="9d14c-128">To create this object, call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

<span data-ttu-id="9d14c-129">Les objets instanciés à partir de la classe **CServiceConfig** agrègent le marshaleur libre de threads afin qu’ils puissent être stockés par les runtimes système et réutilisés dans différents cloisonnements.</span><span class="sxs-lookup"><span data-stu-id="9d14c-129">Objects instantiated from the **CServiceConfig** class aggregate the free-threaded marshaler so that they can be stored by system runtimes and reused in different apartments.</span></span>

<span data-ttu-id="9d14c-130">Pour configurer un service individuel, appelez [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour l’interface associée au service, puis appelez les méthodes sur cette interface pour établir la configuration appropriée.</span><span class="sxs-lookup"><span data-stu-id="9d14c-130">To configure an individual service, call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) for the interface associated with the service and then call methods on that interface to establish the appropriate configuration.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d14c-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9d14c-131">Requirements</span></span>



| <span data-ttu-id="9d14c-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9d14c-132">Requirement</span></span> | <span data-ttu-id="9d14c-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="9d14c-133">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9d14c-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d14c-134">Minimum supported client</span></span><br/> | <span data-ttu-id="9d14c-135">Windows XP avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9d14c-135">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9d14c-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d14c-136">Minimum supported server</span></span><br/> | <span data-ttu-id="9d14c-137">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9d14c-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9d14c-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="9d14c-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d14c-139"><dt>ComSvcs. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d14c-139"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d14c-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d14c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d14c-141">**CoCreateActivity**</span><span class="sxs-lookup"><span data-stu-id="9d14c-141">**CoCreateActivity**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity)
</dt> <dt>

[<span data-ttu-id="9d14c-142">**CoCreateFreeThreadedMarshaler**</span><span class="sxs-lookup"><span data-stu-id="9d14c-142">**CoCreateFreeThreadedMarshaler**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler)
</dt> <dt>

[<span data-ttu-id="9d14c-143">**CoEnterServiceDomain**</span><span class="sxs-lookup"><span data-stu-id="9d14c-143">**CoEnterServiceDomain**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain)
</dt> <dt>

[<span data-ttu-id="9d14c-144">**CoLeaveServiceDomain**</span><span class="sxs-lookup"><span data-stu-id="9d14c-144">**CoLeaveServiceDomain**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain)
</dt> <dt>

[<span data-ttu-id="9d14c-145">Services COM+ sans composants</span><span class="sxs-lookup"><span data-stu-id="9d14c-145">COM+ Services Without Components</span></span>](com--services-without-components.md)
</dt> </dl>

 

