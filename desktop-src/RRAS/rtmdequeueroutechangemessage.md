---
title: Fonction RtmDequeueRouteChangeMessage (RTM. h)
description: La fonction RtmDequeueRouteChangeMessage retourne le prochain message de modification de l’itinéraire dans la file d’attente associée au client spécifié.
ms.assetid: 44f2116a-3c8d-4ac6-896e-b12930b218a5
keywords:
- RtmDequeueRouteChangeMessage fonction RAS
topic_type:
- apiref
api_name:
- RtmDequeueRouteChangeMessage
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 448df230742b03f82294de102bf14b50fefa035c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104389"
---
# <a name="rtmdequeueroutechangemessage-function"></a><span data-ttu-id="fea9a-104">RtmDequeueRouteChangeMessage fonction)</span><span class="sxs-lookup"><span data-stu-id="fea9a-104">RtmDequeueRouteChangeMessage function</span></span>

<span data-ttu-id="fea9a-105">\[Cette API a été remplacée par l’API du [Gestionnaire de table de routage version 2](about-routing-table-manager-version-2.md) et n’est pas disponible au-delà de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="fea9a-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="fea9a-106">Les applications doivent utiliser l’API du gestionnaire de table de routage version 2.\]</span><span class="sxs-lookup"><span data-stu-id="fea9a-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="fea9a-107">La fonction **RtmDequeueRouteChangeMessage** retourne le prochain message de modification de l’itinéraire dans la file d’attente associée au client spécifié.</span><span class="sxs-lookup"><span data-stu-id="fea9a-107">The **RtmDequeueRouteChangeMessage** function returns the next route-change message in the queue associated with the specified client.</span></span>

## <a name="syntax"></a><span data-ttu-id="fea9a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fea9a-108">Syntax</span></span>


```C++
DWORD RtmDequeueRouteChangeMessage(
  _In_  HANDLE ClientHandle,
  _Out_ DWORD  Flags,
  _Out_ PVOID  CurBestRoute,
  _Out_ PVOID  PrevBestRoute
);
```



## <a name="parameters"></a><span data-ttu-id="fea9a-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fea9a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fea9a-110">*ClientHandle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fea9a-110">*ClientHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fea9a-111">Handle qui identifie le client pour lequel l’opération est effectuée.</span><span class="sxs-lookup"><span data-stu-id="fea9a-111">Handle that identifies the client for which the operation is performed.</span></span> <span data-ttu-id="fea9a-112">Obtenez ce handle en appelant [**RtmRegisterClient**](rtmregisterclient.md).</span><span class="sxs-lookup"><span data-stu-id="fea9a-112">Obtain this handle by calling [**RtmRegisterClient**](rtmregisterclient.md).</span></span>

</dd> <dt>

<span data-ttu-id="fea9a-113">*Indicateurs* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="fea9a-113">*Flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fea9a-114">Pointeur vers une variable **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="fea9a-114">Pointer to a **DWORD** variable.</span></span> <span data-ttu-id="fea9a-115">La valeur de cette variable est définie par le gestionnaire de tables de routage.</span><span class="sxs-lookup"><span data-stu-id="fea9a-115">The value of this variable is set by the routing table manager.</span></span> <span data-ttu-id="fea9a-116">La valeur spécifie le type du message de modification et les informations qui ont été retournées dans les mémoires tampons fournies.</span><span class="sxs-lookup"><span data-stu-id="fea9a-116">The value specifies the type of the change message, and what information was returned in the provided buffers.</span></span> <span data-ttu-id="fea9a-117">Ce paramètre est l’un des éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="fea9a-117">This parameter is one of the following.</span></span>



| <span data-ttu-id="fea9a-118">Indicateurs</span><span class="sxs-lookup"><span data-stu-id="fea9a-118">Flags</span></span>                                                                                                                                                                      | <span data-ttu-id="fea9a-119">Signification</span><span class="sxs-lookup"><span data-stu-id="fea9a-119">Meaning</span></span>                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_ROUTE_ADDED"></span><span id="rtm_route_added"></span><dl> <span data-ttu-id="fea9a-120"><dt>**\_itinéraire RTM \_ ajouté**</dt></span><span class="sxs-lookup"><span data-stu-id="fea9a-120"><dt>**RTM\_ROUTE\_ADDED**</dt></span></span> </dl>       | <span data-ttu-id="fea9a-121">Le premier itinéraire a été ajouté pour un réseau de destination particulier.</span><span class="sxs-lookup"><span data-stu-id="fea9a-121">The first route was added for a particular destination network.</span></span> <span data-ttu-id="fea9a-122">Le paramètre *CurBestRoute* pointe vers les informations de l’itinéraire ajouté.</span><span class="sxs-lookup"><span data-stu-id="fea9a-122">The *CurBestRoute* parameter points to the information for the added route.</span></span><br/>                                                                                                                                                            |
| <span id="RTM_ROUTE_DELETED"></span><span id="rtm_route_deleted"></span><dl> <span data-ttu-id="fea9a-123"><dt>**\_itinéraire RTM \_ supprimé**</dt></span><span class="sxs-lookup"><span data-stu-id="fea9a-123"><dt>**RTM\_ROUTE\_DELETED**</dt></span></span> </dl> | <span data-ttu-id="fea9a-124">Le seul itinéraire disponible pour un réseau de destination particulier a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="fea9a-124">The only route available for a particular destination network was deleted.</span></span> <span data-ttu-id="fea9a-125">Le paramètre *PrevBestRoute* pointe vers les informations de l’itinéraire supprimé.</span><span class="sxs-lookup"><span data-stu-id="fea9a-125">The *PrevBestRoute* parameter points to the information for the deleted route.</span></span><br/>                                                                                                                                              |
| <span id="RTM_ROUTE_CHANGED"></span><span id="rtm_route_changed"></span><dl> <span data-ttu-id="fea9a-126"><dt>**\_itinéraire RTM \_ modifié**</dt></span><span class="sxs-lookup"><span data-stu-id="fea9a-126"><dt>**RTM\_ROUTE\_CHANGED**</dt></span></span> </dl> | <span data-ttu-id="fea9a-127">Au moins un des paramètres significatifs a été modifié pour un itinéraire optimal vers un réseau de destination particulier.</span><span class="sxs-lookup"><span data-stu-id="fea9a-127">At least one of the significant parameters was changed for a best route to a particular destination network.</span></span> <span data-ttu-id="fea9a-128">Les paramètres significatifs sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="fea9a-128">The significant parameters are:</span></span> <br/> <span data-ttu-id="fea9a-129">Identificateur de protocole</span><span class="sxs-lookup"><span data-stu-id="fea9a-129">Protocol identifier</span></span><br/> <span data-ttu-id="fea9a-130">Index d’interface</span><span class="sxs-lookup"><span data-stu-id="fea9a-130">Interface index</span></span><br/> <span data-ttu-id="fea9a-131">Adresse du tronçon suivant</span><span class="sxs-lookup"><span data-stu-id="fea9a-131">Next-hop address</span></span><br/> <span data-ttu-id="fea9a-132">Données spécifiques à la famille de protocoles (y compris les métriques d’itinéraires)</span><span class="sxs-lookup"><span data-stu-id="fea9a-132">Protocol-family-specific data (including route metrics)</span></span><br/> |



 

<span data-ttu-id="fea9a-133">Le paramètre *PrevBestRoute* pointe vers les informations d’itinéraire telles qu’elles étaient avant la modification.</span><span class="sxs-lookup"><span data-stu-id="fea9a-133">The *PrevBestRoute* parameter points to the route information as it was before the change.</span></span> <span data-ttu-id="fea9a-134">Le paramètre *CurBestRoute* pointe vers les informations d’itinéraire actuelles (autrement dit, après modification).</span><span class="sxs-lookup"><span data-stu-id="fea9a-134">The *CurBestRoute* parameter points to current (that is, after-change) route information.</span></span>

</dd> <dt>

<span data-ttu-id="fea9a-135">*CurBestRoute* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="fea9a-135">*CurBestRoute* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fea9a-136">Pointeur vers une structure qui reçoit les informations de meilleure route actuelles (le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="fea9a-136">Pointer to a structure that receives the current best-route information (if any).</span></span> <span data-ttu-id="fea9a-137">Le type de la structure est spécifique à la famille de protocoles, par exemple, IP ou IPX.</span><span class="sxs-lookup"><span data-stu-id="fea9a-137">The type of the structure is specific to the protocol family, for example, IP or IPX.</span></span>

<span data-ttu-id="fea9a-138">Ce paramètre est facultatif.</span><span class="sxs-lookup"><span data-stu-id="fea9a-138">This parameter is optional.</span></span> <span data-ttu-id="fea9a-139">Si l’appelant spécifie la **valeur null** pour ce paramètre, les informations de meilleure route actuelles ne sont pas retournées.</span><span class="sxs-lookup"><span data-stu-id="fea9a-139">If the caller specifies **NULL** for this parameter, the current best-route information is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="fea9a-140">*PrevBestRoute* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="fea9a-140">*PrevBestRoute* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fea9a-141">Pointeur vers une structure qui reçoit les informations de meilleur itinéraire précédentes, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="fea9a-141">Pointer to a structure that receives the previous best-route information, if any.</span></span> <span data-ttu-id="fea9a-142">Le type de la structure est spécifique à la famille de protocoles, par exemple, IP ou IPX.</span><span class="sxs-lookup"><span data-stu-id="fea9a-142">The type of the structure is specific to the protocol family, for example, IP or IPX.</span></span>

<span data-ttu-id="fea9a-143">Ce paramètre est facultatif.</span><span class="sxs-lookup"><span data-stu-id="fea9a-143">This parameter is optional.</span></span> <span data-ttu-id="fea9a-144">Si l’appelant spécifie **null** pour ce paramètre, les informations sur le meilleur itinéraire précédent ne sont pas retournées.</span><span class="sxs-lookup"><span data-stu-id="fea9a-144">If the caller specifies **NULL** for this parameter, the previous best-route information is not returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fea9a-145">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fea9a-145">Return value</span></span>

<span data-ttu-id="fea9a-146">La valeur de retour est l’un des codes suivants.</span><span class="sxs-lookup"><span data-stu-id="fea9a-146">The return value is one of the following codes.</span></span>



| <span data-ttu-id="fea9a-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="fea9a-147">Value</span></span>                                                                                                       | <span data-ttu-id="fea9a-148">Description</span><span class="sxs-lookup"><span data-stu-id="fea9a-148">Description</span></span>                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fea9a-149"><dt>**AUCUNE \_ erreur**</dt></span><span class="sxs-lookup"><span data-stu-id="fea9a-149"><dt>**NO\_ERROR**</dt></span></span> </dl>                    | <span data-ttu-id="fea9a-150">Ce message était le dernier message de la file d’attente du client.</span><span class="sxs-lookup"><span data-stu-id="fea9a-150">This message was the last message in the client's queue.</span></span> <span data-ttu-id="fea9a-151">L’objet d’événement est réinitialisé.</span><span class="sxs-lookup"><span data-stu-id="fea9a-151">The event object is reset.</span></span><br/>                                                                                                                                               |
| <dl> <span data-ttu-id="fea9a-152"><dt>**HANDLE d’erreur \_ non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fea9a-152"><dt>**ERROR\_INVALID\_HANDLE**</dt></span></span> </dl>       | <span data-ttu-id="fea9a-153">Le paramètre *ClientHandle* n’est pas un handle valide, ou à l’inscription, le client n’a pas fourni d’objet d’événement pour la notification de modification de message (voir [**RtmRegisterClient**](rtmregisterclient.md)).</span><span class="sxs-lookup"><span data-stu-id="fea9a-153">The *ClientHandle* parameter is not a valid handle, or at registration the client did not provide an event object for change message notification (see [**RtmRegisterClient**](rtmregisterclient.md)).</span></span><br/>                           |
| <dl> <span data-ttu-id="fea9a-154"><dt>**MESSAGES d’erreur \_ supplémentaires \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fea9a-154"><dt>**ERROR\_MORE\_MESSAGES**</dt></span></span> </dl>        | <span data-ttu-id="fea9a-155">La file d’attente du client contient des messages supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="fea9a-155">The client's queue contains additional messages.</span></span> <span data-ttu-id="fea9a-156">Le client doit appeler **RtmDequeueRouteChangeMessage** à nouveau dès que possible pour permettre au gestionnaire de tables de routage de libérer les ressources associées aux messages en attente.</span><span class="sxs-lookup"><span data-stu-id="fea9a-156">The client should call **RtmDequeueRouteChangeMessage** again as soon as possible to allow the routing table manager to free the resources associated with the pending messages.</span></span><br/> |
| <dl> <span data-ttu-id="fea9a-157"><dt>**ERREUR \_ aucun \_ message**</dt></span><span class="sxs-lookup"><span data-stu-id="fea9a-157"><dt>**ERROR\_NO\_MESSAGES**</dt></span></span> </dl>          | <span data-ttu-id="fea9a-158">La file d’attente du client ne contient aucun message. l’appel n’a pas été sollicité.</span><span class="sxs-lookup"><span data-stu-id="fea9a-158">The client's queue contains no messages; the call was unsolicited.</span></span> <span data-ttu-id="fea9a-159">L’événement est réinitialisé.</span><span class="sxs-lookup"><span data-stu-id="fea9a-159">The event is reset.</span></span><br/>                                                                                                                                            |
| <dl> <span data-ttu-id="fea9a-160"><dt>**ERREUR \_ aucune \_ \_ ressource système**</dt></span><span class="sxs-lookup"><span data-stu-id="fea9a-160"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="fea9a-161">Les ressources sont insuffisantes pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="fea9a-161">There are insufficient resources to carry out the operation.</span></span><br/>                                                                                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="fea9a-162">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fea9a-162">Requirements</span></span>



| <span data-ttu-id="fea9a-163">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fea9a-163">Requirement</span></span> | <span data-ttu-id="fea9a-164">Valeur</span><span class="sxs-lookup"><span data-stu-id="fea9a-164">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fea9a-165">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fea9a-165">Minimum supported client</span></span><br/> | <span data-ttu-id="fea9a-166">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="fea9a-166">None supported</span></span><br/>                                                          |
| <span data-ttu-id="fea9a-167">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fea9a-167">Minimum supported server</span></span><br/> | <span data-ttu-id="fea9a-168">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fea9a-168">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="fea9a-169">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="fea9a-169">End of server support</span></span><br/>    | <span data-ttu-id="fea9a-170">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fea9a-170">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="fea9a-171">En-tête</span><span class="sxs-lookup"><span data-stu-id="fea9a-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="fea9a-172"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="fea9a-172"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="fea9a-173">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fea9a-173">Library</span></span><br/>                  | <dl> <span data-ttu-id="fea9a-174"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fea9a-174"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="fea9a-175">DLL</span><span class="sxs-lookup"><span data-stu-id="fea9a-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fea9a-176"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fea9a-176"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fea9a-177">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fea9a-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fea9a-178">Référence de la version 1 du gestionnaire de tables de routage</span><span class="sxs-lookup"><span data-stu-id="fea9a-178">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="fea9a-179">Fonctions de la version 1 du gestionnaire de table de routage</span><span class="sxs-lookup"><span data-stu-id="fea9a-179">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="fea9a-180">**RtmRegisterClient**</span><span class="sxs-lookup"><span data-stu-id="fea9a-180">**RtmRegisterClient**</span></span>](rtmregisterclient.md)
</dt> </dl>

 

 





