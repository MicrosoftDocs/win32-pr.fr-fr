---
title: Fonction RtmRegisterClient (RTM. h)
description: La fonction RtmRegisterClient inscrit un client en tant que gestionnaire du protocole spécifié. Il établit un mécanisme de notification de changement d’itinéraire pour le client et définit des options de protocole.
ms.assetid: 70426601-695d-47ed-b71a-1df3fb8ddf10
keywords:
- RtmRegisterClient fonction RAS
topic_type:
- apiref
api_name:
- RtmRegisterClient
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 564f47e68fd6cdce3d5437fe184bac1ed74d8322
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743109"
---
# <a name="rtmregisterclient-function"></a><span data-ttu-id="42e05-105">RtmRegisterClient fonction)</span><span class="sxs-lookup"><span data-stu-id="42e05-105">RtmRegisterClient function</span></span>

<span data-ttu-id="42e05-106">\[Cette API a été remplacée par l’API du [Gestionnaire de table de routage version 2](about-routing-table-manager-version-2.md) et n’est pas disponible au-delà de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="42e05-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="42e05-107">Les applications doivent utiliser l’API du gestionnaire de table de routage version 2.\]</span><span class="sxs-lookup"><span data-stu-id="42e05-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="42e05-108">La fonction **RtmRegisterClient** inscrit un client en tant que gestionnaire du protocole spécifié.</span><span class="sxs-lookup"><span data-stu-id="42e05-108">The **RtmRegisterClient** function registers a client as a handler of the specified protocol.</span></span> <span data-ttu-id="42e05-109">Il établit un mécanisme de notification de changement d’itinéraire pour le client et définit des options de protocole.</span><span class="sxs-lookup"><span data-stu-id="42e05-109">It establishes a route change notification mechanism for the client, and sets protocol options.</span></span>

## <a name="syntax"></a><span data-ttu-id="42e05-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="42e05-110">Syntax</span></span>


```C++
HANDLE RtmRegisterClient(
  _In_ DWORD  ProtocolFamily,
  _In_ DWORD  RoutingProtocol,
  _In_ HANDLE ChangeEvent,
  _In_ DWORD  Flags
);
```



## <a name="parameters"></a><span data-ttu-id="42e05-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="42e05-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42e05-112">*ProtocolFamily* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="42e05-112">*ProtocolFamily* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42e05-113">Spécifie la famille de protocoles du protocole de routage à inscrire.</span><span class="sxs-lookup"><span data-stu-id="42e05-113">Specifies the protocol family of the routing protocol to register.</span></span>

</dd> <dt>

<span data-ttu-id="42e05-114">*RoutingProtocol* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="42e05-114">*RoutingProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42e05-115">Spécifie l’identificateur de protocole de routage, identique à celui utilisé lors de l’inscription auprès du gestionnaire de routage.</span><span class="sxs-lookup"><span data-stu-id="42e05-115">Specifies the routing protocol identifier, the same as that used when registering with the router manager.</span></span> <span data-ttu-id="42e05-116">Consultez [**RegisterProtocol**](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol).</span><span class="sxs-lookup"><span data-stu-id="42e05-116">See [**RegisterProtocol**](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol).</span></span>

</dd> <dt>

<span data-ttu-id="42e05-117">*ChangeEvent* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="42e05-117">*ChangeEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42e05-118">Spécifie qu’un itinéraire optimal vers un réseau de la table a changé.</span><span class="sxs-lookup"><span data-stu-id="42e05-118">Specifies that a best route to a network in the table has changed.</span></span> <span data-ttu-id="42e05-119">Le gestionnaire de table de routage signale cet événement après une modification du meilleur itinéraire vers un réseau de la table.</span><span class="sxs-lookup"><span data-stu-id="42e05-119">The routing table manager signals this event after a change to the best route to any network in the table.</span></span> <span data-ttu-id="42e05-120">Pour plus d’informations sur la notification de modification de route, consultez [**RtmDequeueRouteChangeMessage**](rtmdequeueroutechangemessage.md) .</span><span class="sxs-lookup"><span data-stu-id="42e05-120">See [**RtmDequeueRouteChangeMessage**](rtmdequeueroutechangemessage.md) for more information about route-change notification.</span></span>

<span data-ttu-id="42e05-121">Ce paramètre est facultatif.</span><span class="sxs-lookup"><span data-stu-id="42e05-121">This parameter is optional.</span></span> <span data-ttu-id="42e05-122">Si l’appelant spécifie la **valeur null** pour ce paramètre, le gestionnaire de tables de routage ne notifie pas le client des modifications dans le meilleur état d’itinéraire.</span><span class="sxs-lookup"><span data-stu-id="42e05-122">If the caller specifies **NULL** for this parameter, the routing table manager does not notify the client of changes in best route status.</span></span>

</dd> <dt>

<span data-ttu-id="42e05-123">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="42e05-123">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42e05-124">Spécifie diverses options pour le traitement spécial du protocole de routage.</span><span class="sxs-lookup"><span data-stu-id="42e05-124">Specifies miscellaneous options for special handling of the routing protocol.</span></span> <span data-ttu-id="42e05-125">La valeur suivante est actuellement prise en charge.</span><span class="sxs-lookup"><span data-stu-id="42e05-125">The following value is currently supported.</span></span>



| <span data-ttu-id="42e05-126">Indicateurs</span><span class="sxs-lookup"><span data-stu-id="42e05-126">Flags</span></span>                                                                                                                                                                                               | <span data-ttu-id="42e05-127">Signification</span><span class="sxs-lookup"><span data-stu-id="42e05-127">Meaning</span></span>                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_PROTOCOL_SINGLE_ROUTE"></span><span id="rtm_protocol_single_route"></span><dl> <span data-ttu-id="42e05-128"><dt>**\_ \_ itinéraire unique du protocole RTM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="42e05-128"><dt>**RTM\_PROTOCOL\_SINGLE\_ROUTE**</dt></span></span> </dl> | <span data-ttu-id="42e05-129">Le gestionnaire de tables de routage conserve un seul itinéraire par réseau de destination pour le protocole de routage.</span><span class="sxs-lookup"><span data-stu-id="42e05-129">The routing table manager keeps only one route per destination network for the routing protocol.</span></span> <span data-ttu-id="42e05-130">En d’autres termes, le gestionnaire de tables de routage remplace les entrées d’itinéraire qui ont les mêmes numéros de réseau de destination au lieu d’en ajouter de nouveaux.</span><span class="sxs-lookup"><span data-stu-id="42e05-130">In other words, the routing table manager replaces route entries that have the same destination network numbers instead of adding new ones.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42e05-131">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="42e05-131">Return value</span></span>

<span data-ttu-id="42e05-132">En cas de retour réussi, valeur de **handle** qui identifie le client lors des appels suivants au gestionnaire de tables de routage.</span><span class="sxs-lookup"><span data-stu-id="42e05-132">On successful return, a **HANDLE** value that identifies the client in subsequent calls to the routing table manager.</span></span>

<span data-ttu-id="42e05-133">Un descripteur **null** indique que le gestionnaire de table de routage n’a pas pu inscrire le client.</span><span class="sxs-lookup"><span data-stu-id="42e05-133">A **NULL** handle indicates that the routing table manager was unable to register the client.</span></span> <span data-ttu-id="42e05-134">Appelez [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) pour obtenir la raison de l’échec.</span><span class="sxs-lookup"><span data-stu-id="42e05-134">Call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) to obtain the reason for the failure.</span></span>



| <span data-ttu-id="42e05-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="42e05-135">Value</span></span>                                                                                                         | <span data-ttu-id="42e05-136">Description</span><span class="sxs-lookup"><span data-stu-id="42e05-136">Description</span></span>                                                                                     |
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="42e05-137"><dt>**le \_ client d’erreur \_ \_ existe déjà**</dt></span><span class="sxs-lookup"><span data-stu-id="42e05-137"><dt>**ERROR\_CLIENT\_ALREADY\_EXISTS**</dt></span></span> </dl> | <span data-ttu-id="42e05-138">Un autre client s’est déjà inscrit pour gérer le protocole spécifié.</span><span class="sxs-lookup"><span data-stu-id="42e05-138">Another client has already registered to handle the specified protocol.</span></span><br/>              |
| <dl> <span data-ttu-id="42e05-139"><dt>**paramètre d’erreur \_ non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="42e05-139"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>      | <span data-ttu-id="42e05-140">La famille de protocoles spécifiée n’est pas prise en charge ou le paramètre *Flags* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="42e05-140">The specified protocol family is not supported, or the *Flags* parameter is invalid.</span></span><br/> |
| <dl> <span data-ttu-id="42e05-141"><dt>**ERREUR \_ aucune \_ \_ ressource système**</dt></span><span class="sxs-lookup"><span data-stu-id="42e05-141"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl>   | <span data-ttu-id="42e05-142">Ressources insuffisantes pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="42e05-142">Insufficient resources to carry out the operation.</span></span><br/>                                   |
| <dl> <span data-ttu-id="42e05-143"><dt>**ERREUR \_ de \_ mémoire insuffisante \_**</dt></span><span class="sxs-lookup"><span data-stu-id="42e05-143"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl>     | <span data-ttu-id="42e05-144">Mémoire insuffisante pour allouer des structures de données pour le client.</span><span class="sxs-lookup"><span data-stu-id="42e05-144">Insufficient memory to allocate data structures for the client.</span></span><br/>                      |



 

## <a name="requirements"></a><span data-ttu-id="42e05-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="42e05-145">Requirements</span></span>



| <span data-ttu-id="42e05-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="42e05-146">Requirement</span></span> | <span data-ttu-id="42e05-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="42e05-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="42e05-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="42e05-148">Minimum supported client</span></span><br/> | <span data-ttu-id="42e05-149">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="42e05-149">None supported</span></span><br/>                                                          |
| <span data-ttu-id="42e05-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="42e05-150">Minimum supported server</span></span><br/> | <span data-ttu-id="42e05-151">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="42e05-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="42e05-152">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="42e05-152">End of server support</span></span><br/>    | <span data-ttu-id="42e05-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="42e05-153">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="42e05-154">En-tête</span><span class="sxs-lookup"><span data-stu-id="42e05-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="42e05-155"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="42e05-155"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="42e05-156">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="42e05-156">Library</span></span><br/>                  | <dl> <span data-ttu-id="42e05-157"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="42e05-157"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="42e05-158">DLL</span><span class="sxs-lookup"><span data-stu-id="42e05-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42e05-159"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42e05-159"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42e05-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="42e05-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42e05-161">Référence de la version 1 du gestionnaire de tables de routage</span><span class="sxs-lookup"><span data-stu-id="42e05-161">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="42e05-162">Fonctions de la version 1 du gestionnaire de table de routage</span><span class="sxs-lookup"><span data-stu-id="42e05-162">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="42e05-163">**GetLastError**</span><span class="sxs-lookup"><span data-stu-id="42e05-163">**GetLastError**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[<span data-ttu-id="42e05-164">**RegisterProtocol**</span><span class="sxs-lookup"><span data-stu-id="42e05-164">**RegisterProtocol**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol)
</dt> <dt>

[<span data-ttu-id="42e05-165">Identificateurs de famille de protocole RTMv1</span><span class="sxs-lookup"><span data-stu-id="42e05-165">RTMv1 Protocol Family Identifiers</span></span>](routing-table-manager-version-1-protocol-family-identifiers.md)
</dt> <dt>

[<span data-ttu-id="42e05-166">**RtmDequeueRouteChangeMessage**</span><span class="sxs-lookup"><span data-stu-id="42e05-166">**RtmDequeueRouteChangeMessage**</span></span>](rtmdequeueroutechangemessage.md)
</dt> <dt>

[<span data-ttu-id="42e05-167">**RtmDeregisterClient**</span><span class="sxs-lookup"><span data-stu-id="42e05-167">**RtmDeregisterClient**</span></span>](rtmderegisterclient.md)
</dt> </dl>

 

