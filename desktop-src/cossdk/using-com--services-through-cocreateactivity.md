---
description: La fonction CoCreateActivity est utilisée pour soumettre le travail en traitement par lots au système COM+. Il permet aux applications basées sur des scripts de prendre en charge une configuration de service COM+ à l’ensemble de l’application.
ms.assetid: af734507-516c-43f1-9c5e-c77cde1b8008
title: Utilisation des services COM+ via CoCreateActivity
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5b3296756b91d0f8ea29b1d67c11c78c431cfcd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515376"
---
# <a name="using-com-services-through-cocreateactivity"></a><span data-ttu-id="0a999-104">Utilisation des services COM+ via CoCreateActivity</span><span class="sxs-lookup"><span data-stu-id="0a999-104">Using COM+ Services Through CoCreateActivity</span></span>

<span data-ttu-id="0a999-105">La fonction [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) est utilisée pour soumettre le travail en traitement par lots au système com+.</span><span class="sxs-lookup"><span data-stu-id="0a999-105">The [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) function is used to submit batch work to the COM+ system.</span></span> <span data-ttu-id="0a999-106">Il permet aux applications basées sur des scripts de prendre en charge une configuration de service COM+ à l’ensemble de l’application.</span><span class="sxs-lookup"><span data-stu-id="0a999-106">It allows script-based applications to support an application-wide COM+ service configuration.</span></span>

<span data-ttu-id="0a999-107">Les services COM+ souhaités sont configurés via un objet [**CServiceConfig**](cserviceconfig.md) qui est transmis à la fonction.</span><span class="sxs-lookup"><span data-stu-id="0a999-107">The desired COM+ services are configured through a [**CServiceConfig**](cserviceconfig.md) object that is passed in to the function.</span></span> <span data-ttu-id="0a999-108">La fonction crée un objet d’activité et retourne l’interface [**IServiceActivity**](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceactivity) de cet objet.</span><span class="sxs-lookup"><span data-stu-id="0a999-108">The function creates an activity object and returns the [**IServiceActivity**](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceactivity) interface of that object.</span></span> <span data-ttu-id="0a999-109">Le travail en traitement par lots peut être envoyé de manière synchrone ou asynchrone, à l’aide des méthodes [**SynchronousCall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iserviceactivity-synchronouscall) ou [**AsynchronousCall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iserviceactivity-asynchronouscall) de **IServiceActivity**, respectivement.</span><span class="sxs-lookup"><span data-stu-id="0a999-109">The batch work can be submitted either synchronously or asynchronously, by using the [**SynchronousCall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iserviceactivity-synchronouscall) or [**AsynchronousCall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iserviceactivity-asynchronouscall) methods of **IServiceActivity**, respectively.</span></span> <span data-ttu-id="0a999-110">Un pointeur vers une interface [**IServiceCall**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicecall) est passé à chacune de ces méthodes, et le travail en traitement par lots est implémenté par le développeur dans la méthode [**OnCall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iservicecall-oncall) de l’interface **IServiceCall** .</span><span class="sxs-lookup"><span data-stu-id="0a999-110">A pointer to an [**IServiceCall**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicecall) interface is passed in to each of these methods, and the batch work is implemented by the developer in the [**OnCall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iservicecall-oncall) method of the **IServiceCall** interface.</span></span>

## <a name="component-services-administrative-tool"></a><span data-ttu-id="0a999-111">Outil d’administration Services de composants</span><span class="sxs-lookup"><span data-stu-id="0a999-111">Component Services Administrative Tool</span></span>

<span data-ttu-id="0a999-112">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="0a999-112">Does not apply.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="0a999-113">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="0a999-113">Visual Basic</span></span>

<span data-ttu-id="0a999-114">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="0a999-114">Does not apply.</span></span>

## <a name="cc"></a><span data-ttu-id="0a999-115">C/C++</span><span class="sxs-lookup"><span data-stu-id="0a999-115">C/C++</span></span>

<span data-ttu-id="0a999-116">Le fragment de code suivant illustre l’utilisation des services COM+ par le biais de [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity).</span><span class="sxs-lookup"><span data-stu-id="0a999-116">The following code fragment illustrates how to use COM+ services through [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity).</span></span> <span data-ttu-id="0a999-117">La gestion des erreurs est omise par souci de concision.</span><span class="sxs-lookup"><span data-stu-id="0a999-117">Error handling is omitted for brevity.</span></span> <span data-ttu-id="0a999-118">Ce fragment de code utilise l’objet [**CServiceConfig**](cserviceconfig.md) qui a été créé et configuré dans [Configuration des services com+ avec CServiceConfig](configuring-com--services-with-cserviceconfig.md).</span><span class="sxs-lookup"><span data-stu-id="0a999-118">This code fragment uses the [**CServiceConfig**](cserviceconfig.md) object that was created and configured in [Configuring COM+ Services with CServiceConfig](configuring-com--services-with-cserviceconfig.md).</span></span>


```C++
// A CServiceConfig object was created as follows:
// hr = CoCreateInstance(CLSID_CServiceConfig, NULL, CLSCTX_INPROC_SERVER,
//   IID_IUnknown, (void**)&pUnknownCSC);

// Create the activity for our services.
HRESULT hr = CoCreateActivity(pUnknownCSC, IID_IServiceActivity, (void**)&pActivity);
if (FAILED(hr)) throw(hr);

// Do the batch work synchronously.
// The batch work is implemented in pServiceCall->OnCall().
hr = pActivity->SynchronousCall(pServiceCall);
if (FAILED(hr)) throw(hr);

```



## <a name="related-topics"></a><span data-ttu-id="0a999-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0a999-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a999-120">**CoCreateActivity**</span><span class="sxs-lookup"><span data-stu-id="0a999-120">**CoCreateActivity**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity)
</dt> <dt>

[<span data-ttu-id="0a999-121">Configuration des services COM+ avec CServiceConfig</span><span class="sxs-lookup"><span data-stu-id="0a999-121">Configuring COM+ Services with CServiceConfig</span></span>](configuring-com--services-with-cserviceconfig.md)
</dt> <dt>

[<span data-ttu-id="0a999-122">**CServiceConfig**</span><span class="sxs-lookup"><span data-stu-id="0a999-122">**CServiceConfig**</span></span>](cserviceconfig.md)
</dt> <dt>

[<span data-ttu-id="0a999-123">Utilisation des services COM+ via CoEnterServiceDomain et CoLeaveServiceDomain</span><span class="sxs-lookup"><span data-stu-id="0a999-123">Using COM+ Services Through CoEnterServiceDomain and CoLeaveServiceDomain</span></span>](using-com--services-through-coenterservicedomain-and-coleaveservicedomain.md)
</dt> </dl>

 

 



