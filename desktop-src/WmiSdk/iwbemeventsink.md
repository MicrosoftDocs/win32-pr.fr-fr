---
description: Lance la communication avec un fournisseur d’événements à l’aide d’un ensemble restreint de requêtes.
ms.assetid: dd076dd0-ed39-47a2-86fb-a595baf3f464
ms.tgt_platform: multiple
title: Interface IWbemEventSink (wbemprov. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemEventSink
api_type:
- COM
api_location:
- Wbemsvc.dll
ms.openlocfilehash: 22a3a15920d26f482cedfa3a596fd439ea70c2f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527233"
---
# <a name="iwbemeventsink-interface"></a><span data-ttu-id="ee3bc-103">Interface IWbemEventSink</span><span class="sxs-lookup"><span data-stu-id="ee3bc-103">IWbemEventSink interface</span></span>

<span data-ttu-id="ee3bc-104">L’interface **IWbemEventSink** initie la communication avec un fournisseur d’événements à l’aide d’un ensemble restreint de requêtes.</span><span class="sxs-lookup"><span data-stu-id="ee3bc-104">The **IWbemEventSink** interface initiates communication with an event provider using a restricted set of queries.</span></span> <span data-ttu-id="ee3bc-105">Cette interface étend [**IWbemObjectSink**](iwbemobjectsink.md), en fournissant de nouvelles méthodes pour la sécurité et les performances.</span><span class="sxs-lookup"><span data-stu-id="ee3bc-105">This interface extends [**IWbemObjectSink**](iwbemobjectsink.md), providing new methods dealing with security and performance.</span></span> <span data-ttu-id="ee3bc-106">Pour plus d’informations sur l’utilisation de cette interface, consultez [écriture d’un fournisseur d’événements](writing-an-event-provider.md) et [sécurisation des événements WMI](securing-wmi-events.md).</span><span class="sxs-lookup"><span data-stu-id="ee3bc-106">For more information about using this interface, see [Writing an Event Provider](writing-an-event-provider.md) and [Securing WMI Events](securing-wmi-events.md).</span></span>

## <a name="members"></a><span data-ttu-id="ee3bc-107">Membres</span><span class="sxs-lookup"><span data-stu-id="ee3bc-107">Members</span></span>

<span data-ttu-id="ee3bc-108">L’interface **IWbemEventSink** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ee3bc-108">The **IWbemEventSink** interface has these types of members:</span></span>

-   [<span data-ttu-id="ee3bc-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ee3bc-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ee3bc-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ee3bc-110">Methods</span></span>

<span data-ttu-id="ee3bc-111">L’interface **IWbemEventSink** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="ee3bc-111">The **IWbemEventSink** interface has these methods.</span></span>



| <span data-ttu-id="ee3bc-112">Méthode</span><span class="sxs-lookup"><span data-stu-id="ee3bc-112">Method</span></span>                                                                | <span data-ttu-id="ee3bc-113">Description</span><span class="sxs-lookup"><span data-stu-id="ee3bc-113">Description</span></span>                                                           |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="ee3bc-114">**GetRestrictedSink**</span><span class="sxs-lookup"><span data-stu-id="ee3bc-114">**GetRestrictedSink**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-getrestrictedsink)         | <span data-ttu-id="ee3bc-115">Appelée par le consommateur pour configurer des requêtes d’événement restreintes.</span><span class="sxs-lookup"><span data-stu-id="ee3bc-115">Called by the consumer to set up restricted event queries.</span></span><br/> |
| [<span data-ttu-id="ee3bc-116">**IsActive**</span><span class="sxs-lookup"><span data-stu-id="ee3bc-116">**IsActive**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-isactive)                           | <span data-ttu-id="ee3bc-117">Vérifie l’état du récepteur d’événements.</span><span class="sxs-lookup"><span data-stu-id="ee3bc-117">Checks status of event sink.</span></span><br/>                               |
| [<span data-ttu-id="ee3bc-118">**SetBatchingParameters**</span><span class="sxs-lookup"><span data-stu-id="ee3bc-118">**SetBatchingParameters**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setbatchingparameters) | <span data-ttu-id="ee3bc-119">Appelé par le consommateur pour définir les paramètres de traitement par lot.</span><span class="sxs-lookup"><span data-stu-id="ee3bc-119">Called by the consumer to set batching parameters.</span></span><br/>         |
| [<span data-ttu-id="ee3bc-120">**SetSinkSecurity**</span><span class="sxs-lookup"><span data-stu-id="ee3bc-120">**SetSinkSecurity**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity)             | <span data-ttu-id="ee3bc-121">Utilisé pour mettre à jour le descripteur de sécurité sur un récepteur d’événements.</span><span class="sxs-lookup"><span data-stu-id="ee3bc-121">Used to update the security descriptor on an event sink.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="ee3bc-122">Notes</span><span class="sxs-lookup"><span data-stu-id="ee3bc-122">Remarks</span></span>

<span data-ttu-id="ee3bc-123">Lors de l’implémentation d’un récepteur d’abonnement aux événements ([**IWbemObjectSink**](iwbemobjectsink.md) ou **IWbemEventSink**), n’appelez pas WMI à partir des méthodes sur l’objet récepteur.</span><span class="sxs-lookup"><span data-stu-id="ee3bc-123">When implementing an event subscription sink ([**IWbemObjectSink**](iwbemobjectsink.md) or **IWbemEventSink**), do not call into WMI from within the methods on the sink object.</span></span> <span data-ttu-id="ee3bc-124">Par exemple, l’appel de [**IWbemServices :: CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) pour annuler le récepteur dans une implémentation de [**IWbemEventSink :: SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity) peut interférer avec l’État WMI.</span><span class="sxs-lookup"><span data-stu-id="ee3bc-124">For example, calling [**IWbemServices::CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) to cancel the sink from within an implementation of [**IWbemEventSink::SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity) can interfere with the WMI state.</span></span> <span data-ttu-id="ee3bc-125">Pour annuler un abonnement à un événement, définissez un indicateur et appelez **IWbemServices :: CancelAsyncCall** à partir d’un autre thread ou objet.</span><span class="sxs-lookup"><span data-stu-id="ee3bc-125">To cancel an event subscription, set a flag and call **IWbemServices::CancelAsyncCall** from another thread or object.</span></span> <span data-ttu-id="ee3bc-126">Pour les implémentations qui ne sont pas liées à un récepteur d’événements, telles que les récupérations d’objets, d’enum et de requêtes, vous pouvez rappeler dans WMI.</span><span class="sxs-lookup"><span data-stu-id="ee3bc-126">For implementations that are not related to an event sink, such as object, enum, and query retrievals, you can call back into WMI.</span></span>

<span data-ttu-id="ee3bc-127">Les implémentations de récepteur doivent traiter la notification d’événement dans un délai de 100 ms car le thread WMI qui remet la notification d’événement ne peut pas effectuer d’autres tâches tant que le traitement de l’objet récepteur n’est pas terminé.</span><span class="sxs-lookup"><span data-stu-id="ee3bc-127">Sink implementations should process the event notification within 100 MSEC because the WMI thread that delivers the event notification cannot do other work until the sink object has completed processing.</span></span> <span data-ttu-id="ee3bc-128">Si la notification nécessite une grande quantité de traitement, le récepteur peut utiliser une file d’attente interne pour qu’un autre thread gère le traitement.</span><span class="sxs-lookup"><span data-stu-id="ee3bc-128">If the notification requires a large amount of processing, the sink can use an internal queue for another thread to handle the processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee3bc-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ee3bc-129">Requirements</span></span>



| <span data-ttu-id="ee3bc-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ee3bc-130">Requirement</span></span> | <span data-ttu-id="ee3bc-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee3bc-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee3bc-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ee3bc-132">Minimum supported client</span></span><br/> | <span data-ttu-id="ee3bc-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ee3bc-133">Windows Vista</span></span><br/>                                                                                  |
| <span data-ttu-id="ee3bc-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ee3bc-134">Minimum supported server</span></span><br/> | <span data-ttu-id="ee3bc-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ee3bc-135">Windows Server 2008</span></span><br/>                                                                            |
| <span data-ttu-id="ee3bc-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="ee3bc-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee3bc-137"><dt>Wbemprov. h (inclure Wbemidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ee3bc-137"><dt>Wbemprov.h (include Wbemidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="ee3bc-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ee3bc-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="ee3bc-139"><dt>Wbemuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ee3bc-139"><dt>Wbemuuid.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="ee3bc-140">DLL</span><span class="sxs-lookup"><span data-stu-id="ee3bc-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee3bc-141"><dt>Wbemsvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee3bc-141"><dt>Wbemsvc.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="ee3bc-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee3bc-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee3bc-143">API COM pour WMI</span><span class="sxs-lookup"><span data-stu-id="ee3bc-143">COM API for WMI</span></span>](com-api-for-wmi.md)
</dt> </dl>

 

 




