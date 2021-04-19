---
title: Fonction RtmAddRoute (RTM. h)
description: La fonction RtmAddRoute ajoute une entrée de routage ou met à jour une entrée d’itinéraire existante.
ms.assetid: 09a9b57d-f10b-40b7-a3c1-2e0613f29431
keywords:
- RtmAddRoute fonction RAS
topic_type:
- apiref
api_name:
- RtmAddRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0c3ee68c9b026fc37457819777e69d2be7984e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510982"
---
# <a name="rtmaddroute-function"></a><span data-ttu-id="685be-104">RtmAddRoute fonction)</span><span class="sxs-lookup"><span data-stu-id="685be-104">RtmAddRoute function</span></span>

<span data-ttu-id="685be-105">\[Cette API a été remplacée par l’API du [Gestionnaire de table de routage version 2](about-routing-table-manager-version-2.md) et n’est pas disponible au-delà de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="685be-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="685be-106">Les applications doivent utiliser l’API du gestionnaire de table de routage version 2.\]</span><span class="sxs-lookup"><span data-stu-id="685be-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="685be-107">La fonction **RtmAddRoute** ajoute une entrée de routage ou met à jour une entrée d’itinéraire existante.</span><span class="sxs-lookup"><span data-stu-id="685be-107">The **RtmAddRoute** function adds a route entry or updates an existing route entry.</span></span>

## <a name="syntax"></a><span data-ttu-id="685be-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="685be-108">Syntax</span></span>


```C++
DWORD RtmAddRoute(
  _In_  HANDLE ClientHandle,
  _In_  PVOID  Route,
  _In_  DWORD  TimeToLive,
  _Out_ DWORD  Flags,
  _Out_ PVOID  CurBestRoute,
  _Out_ PVOID  PrevBestRoute
);
```



## <a name="parameters"></a><span data-ttu-id="685be-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="685be-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="685be-110">*ClientHandle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="685be-110">*ClientHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="685be-111">Handle qui identifie le client et, par conséquent, le protocole de routage, qui a ajouté ou mis à jour l’itinéraire.</span><span class="sxs-lookup"><span data-stu-id="685be-111">Handle that identifies the client, and therefore the routing protocol, that added or updated the route.</span></span> <span data-ttu-id="685be-112">Obtenez ce handle en appelant [**RtmRegisterClient**](rtmregisterclient.md).</span><span class="sxs-lookup"><span data-stu-id="685be-112">Obtain this handle by calling [**RtmRegisterClient**](rtmregisterclient.md).</span></span>

</dd> <dt>

<span data-ttu-id="685be-113">*Itinéraire* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="685be-113">*Route* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="685be-114">Pointeur vers une structure spécifique à la famille de protocoles qui spécifie l’itinéraire nouveau ou mis à jour.</span><span class="sxs-lookup"><span data-stu-id="685be-114">Pointer to a protocol-family-specific structure that specifies the new or updated route.</span></span> <span data-ttu-id="685be-115">Les champs suivants sont utilisés par le gestionnaire de tables de routage pour mettre à jour la table de routage :</span><span class="sxs-lookup"><span data-stu-id="685be-115">The following fields are used by the routing table manager to update the routing table:</span></span>



| <span data-ttu-id="685be-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="685be-116">Value</span></span>                                                                                                                                                                                                                                 | <span data-ttu-id="685be-117">Signification</span><span class="sxs-lookup"><span data-stu-id="685be-117">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RR_Network"></span><span id="rr_network"></span><span id="RR_NETWORK"></span><dl> <span data-ttu-id="685be-118"><dt>**Réseau de RR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="685be-118"><dt>**RR\_Network**</dt></span></span> </dl>                                                     | <span data-ttu-id="685be-119">Spécifie le numéro de réseau de destination.</span><span class="sxs-lookup"><span data-stu-id="685be-119">Specifies the destination network number.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                      |
| <span id="RR_InterfaceID"></span><span id="rr_interfaceid"></span><span id="RR_INTERFACEID"></span><dl> <span data-ttu-id="685be-120"><dt>**RR \_ InterfaceId**</dt></span><span class="sxs-lookup"><span data-stu-id="685be-120"><dt>**RR\_InterfaceID**</dt></span></span> </dl>                                     | <span data-ttu-id="685be-121">Spécifie l’index de l’interface par le biais duquel l’itinéraire a été reçu.</span><span class="sxs-lookup"><span data-stu-id="685be-121">Specifies the index of the interface through which the route was received.</span></span><br/>                                                                                                                                                                                                                                                                                                                     |
| <span id="RR_NextHopAddress"></span><span id="rr_nexthopaddress"></span><span id="RR_NEXTHOPADDRESS"></span><dl> <span data-ttu-id="685be-122"><dt>**\_NEXTHOPADDRESS RR**</dt></span><span class="sxs-lookup"><span data-stu-id="685be-122"><dt>**RR\_NextHopAddress**</dt></span></span> </dl>                         | <span data-ttu-id="685be-123">Spécifie l’adresse du routeur de tronçon suivant.</span><span class="sxs-lookup"><span data-stu-id="685be-123">Specifies the address of the next-hop router.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                  |
| <span id="RR_FamilySpecificData"></span><span id="rr_familyspecificdata"></span><span id="RR_FAMILYSPECIFICDATA"></span><dl> <span data-ttu-id="685be-124"><dt>**\_FAMILYSPECIFICDATA RR**</dt></span><span class="sxs-lookup"><span data-stu-id="685be-124"><dt>**RR\_FamilySpecificData**</dt></span></span> </dl>         | <span data-ttu-id="685be-125">Spécifie les données qui sont spécifiques à la famille de protocoles.</span><span class="sxs-lookup"><span data-stu-id="685be-125">Specifies data that is specific to the protocol family.</span></span> <span data-ttu-id="685be-126">Bien que les données soient transparentes pour le gestionnaire de tables de routage, elles sont prises en compte lors de la comparaison des itinéraires pour déterminer si les informations de routage ont changé.</span><span class="sxs-lookup"><span data-stu-id="685be-126">Although the data is transparent to the routing table manager, it is considered when comparing routes to determine if route information has changed.</span></span> <span data-ttu-id="685be-127">Les données sont également utilisées pour définir des valeurs de métrique qui sont indépendantes du protocole de routage.</span><span class="sxs-lookup"><span data-stu-id="685be-127">The data is also used to set metric values that are independent of the routing protocol.</span></span> <span data-ttu-id="685be-128">Par conséquent, ces données sont utilisées pour déterminer le meilleur itinéraire pour le réseau de destination.</span><span class="sxs-lookup"><span data-stu-id="685be-128">Consequently, this data is used to determine the best route for the destination network.</span></span><br/> |
| <span id="RR_ProtocolSpecificData"></span><span id="rr_protocolspecificdata"></span><span id="RR_PROTOCOLSPECIFICDATA"></span><dl> <span data-ttu-id="685be-129"><dt>**\_PROTOCOLSPECIFICDATA RR**</dt></span><span class="sxs-lookup"><span data-stu-id="685be-129"><dt>**RR\_ProtocolSpecificData**</dt></span></span> </dl> | <span data-ttu-id="685be-130">Spécifie des données qui sont spécifiques au protocole de routage qui a fourni l’itinéraire.</span><span class="sxs-lookup"><span data-stu-id="685be-130">Specifies data which is specific to the routing protocol that supplied the route.</span></span><br/>                                                                                                                                                                                                                                                                                                              |
| <span id="RR_TimeStamp"></span><span id="rr_timestamp"></span><span id="RR_TIMESTAMP"></span><dl> <span data-ttu-id="685be-131"><dt>**Horodateur du RR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="685be-131"><dt>**RR\_TimeStamp**</dt></span></span> </dl>                                             | <span data-ttu-id="685be-132">Spécifie l’heure système actuelle.</span><span class="sxs-lookup"><span data-stu-id="685be-132">Specifies the current system time.</span></span> <span data-ttu-id="685be-133">Ce champ est défini par le gestionnaire de tables de routage.</span><span class="sxs-lookup"><span data-stu-id="685be-133">This field is set by the routing table manager.</span></span><br/>                                                                                                                                                                                                                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="685be-134">*TimeToLive* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="685be-134">*TimeToLive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="685be-135">Spécifie le nombre de secondes pendant lesquelles l’itinéraire spécifié doit être conservé dans la table de routage.</span><span class="sxs-lookup"><span data-stu-id="685be-135">Specifies the number of seconds the specified route should be kept in the routing table.</span></span> <span data-ttu-id="685be-136">Si ce paramètre est défini sur Infinite, l’itinéraire est conservé jusqu’à ce qu’il soit explicitement supprimé.</span><span class="sxs-lookup"><span data-stu-id="685be-136">If this parameter is set to INFINITE, the route is kept until it is explicitly deleted.</span></span> <span data-ttu-id="685be-137">La limite actuelle pour *TimeToLive* est 2147483 s (24 + jours).</span><span class="sxs-lookup"><span data-stu-id="685be-137">The current limit for *TimeToLive* is 2147483 sec (24+ days).</span></span>

</dd> <dt>

<span data-ttu-id="685be-138">*Indicateurs* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="685be-138">*Flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="685be-139">Pointeur vers une variable **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="685be-139">Pointer to a **DWORD** variable.</span></span> <span data-ttu-id="685be-140">La valeur de cette variable est définie par le gestionnaire de tables de routage.</span><span class="sxs-lookup"><span data-stu-id="685be-140">The value of this variable is set by the routing table manager.</span></span> <span data-ttu-id="685be-141">La valeur indique le type de la modification et les informations qui ont été retournées dans les mémoires tampons fournies.</span><span class="sxs-lookup"><span data-stu-id="685be-141">The value indicates the type of the change, and what information was returned in the provided buffers.</span></span> <span data-ttu-id="685be-142">Ce paramètre est l’un des éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="685be-142">This parameter is one of the following.</span></span>



| <span data-ttu-id="685be-143">Indicateurs</span><span class="sxs-lookup"><span data-stu-id="685be-143">Flags</span></span>                                                                                                                                                                      | <span data-ttu-id="685be-144">Signification</span><span class="sxs-lookup"><span data-stu-id="685be-144">Meaning</span></span>                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_NO_CHANGE"></span><span id="rtm_no_change"></span><dl> <span data-ttu-id="685be-145"><dt>**RTM- \_ aucune \_ modification**</dt></span><span class="sxs-lookup"><span data-stu-id="685be-145"><dt>**RTM\_NO\_CHANGE**</dt></span></span> </dl>             | <span data-ttu-id="685be-146">L’ajout ou la mise à jour n’a modifié aucun des paramètres d’itinéraire significatifs, ou l’entrée de route affectée n’est pas la meilleure route parmi les entrées pour le réseau de destination.</span><span class="sxs-lookup"><span data-stu-id="685be-146">The addition or update either did not change any of the significant route parameters, or the route entry affected is not the best route among the entries for the destination network.</span></span><br/>                                                                                                          |
| <span id="RTM_ROUTE_ADDED"></span><span id="rtm_route_added"></span><dl> <span data-ttu-id="685be-147"><dt>**\_itinéraire RTM \_ ajouté**</dt></span><span class="sxs-lookup"><span data-stu-id="685be-147"><dt>**RTM\_ROUTE\_ADDED**</dt></span></span> </dl>       | <span data-ttu-id="685be-148">L’itinéraire a été ajouté pour le réseau de destination.</span><span class="sxs-lookup"><span data-stu-id="685be-148">The route was added for the destination network.</span></span> <span data-ttu-id="685be-149">Le paramètre *CurBestRoute* pointe vers les informations de l’itinéraire ajouté.</span><span class="sxs-lookup"><span data-stu-id="685be-149">The *CurBestRoute* parameter points to the information for the added route.</span></span><br/>                                                                                                                                                                    |
| <span id="RTM_ROUTE_CHANGED"></span><span id="rtm_route_changed"></span><dl> <span data-ttu-id="685be-150"><dt>**\_itinéraire RTM \_ modifié**</dt></span><span class="sxs-lookup"><span data-stu-id="685be-150"><dt>**RTM\_ROUTE\_CHANGED**</dt></span></span> </dl> | <span data-ttu-id="685be-151">Au moins un des paramètres significatifs a été modifié pour le meilleur itinéraire vers le réseau de destination.</span><span class="sxs-lookup"><span data-stu-id="685be-151">At least one of the significant parameters was changed for the best route to the destination network.</span></span> <span data-ttu-id="685be-152">Les paramètres significatifs sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="685be-152">The significant parameters are:</span></span> <br/> <span data-ttu-id="685be-153">Identificateur de protocole</span><span class="sxs-lookup"><span data-stu-id="685be-153">Protocol identifier</span></span><br/> <span data-ttu-id="685be-154">Index d’interface</span><span class="sxs-lookup"><span data-stu-id="685be-154">Interface index</span></span><br/> <span data-ttu-id="685be-155">Adresse du tronçon suivant</span><span class="sxs-lookup"><span data-stu-id="685be-155">Next-hop address</span></span><br/> <span data-ttu-id="685be-156">Données spécifiques à la famille de protocoles (y compris les métriques d’itinéraires)</span><span class="sxs-lookup"><span data-stu-id="685be-156">Protocol-family-specific data (including route metrics)</span></span><br/> |



 

<span data-ttu-id="685be-157">Le paramètre *PrevBestRoute* pointe vers les informations d’itinéraire telles qu’elles étaient avant la modification.</span><span class="sxs-lookup"><span data-stu-id="685be-157">The *PrevBestRoute* parameter points to the route information as it was before the change.</span></span> <span data-ttu-id="685be-158">Le paramètre *CurBestRoute* pointe vers les informations d’itinéraire actuelles (c’est-à-dire après modification).</span><span class="sxs-lookup"><span data-stu-id="685be-158">The *CurBestRoute* parameter points to the current (that is, after-change) route information.</span></span>

</dd> <dt>

<span data-ttu-id="685be-159">*CurBestRoute* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="685be-159">*CurBestRoute* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="685be-160">Pointeur vers une structure qui reçoit les informations de meilleure route actuelles, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="685be-160">Pointer to a structure that receives the current best-route information, if any.</span></span> <span data-ttu-id="685be-161">Le type de la structure est spécifique à la famille de protocoles, par exemple, IP ou IPX.</span><span class="sxs-lookup"><span data-stu-id="685be-161">The type of the structure is specific to the protocol family, for example, IP or IPX.</span></span>

<span data-ttu-id="685be-162">Ce paramètre est facultatif.</span><span class="sxs-lookup"><span data-stu-id="685be-162">This parameter is optional.</span></span> <span data-ttu-id="685be-163">Si l’appelant spécifie la **valeur null** pour ce paramètre, les informations de meilleure route actuelles ne sont pas retournées.</span><span class="sxs-lookup"><span data-stu-id="685be-163">If the caller specifies **NULL** for this parameter, the current best-route information is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="685be-164">*PrevBestRoute* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="685be-164">*PrevBestRoute* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="685be-165">Pointeur vers une structure qui reçoit les informations de meilleur itinéraire précédentes, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="685be-165">Pointer to a structure that receives the previous best-route information, if any.</span></span> <span data-ttu-id="685be-166">Le type de la structure est spécifique à la famille de protocoles, par exemple, IP ou IPX.</span><span class="sxs-lookup"><span data-stu-id="685be-166">The type of the structure is specific to the protocol family, for example, IP or IPX.</span></span>

<span data-ttu-id="685be-167">Ce paramètre est facultatif.</span><span class="sxs-lookup"><span data-stu-id="685be-167">This parameter is optional.</span></span> <span data-ttu-id="685be-168">Si l’appelant spécifie **null** pour ce paramètre, les informations sur le meilleur itinéraire précédent ne sont pas retournées.</span><span class="sxs-lookup"><span data-stu-id="685be-168">If the caller specifies **NULL** for this parameter the previous best-route information is not returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="685be-169">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="685be-169">Return value</span></span>

<span data-ttu-id="685be-170">La valeur de retour est l’un des codes suivants.</span><span class="sxs-lookup"><span data-stu-id="685be-170">The return value is one of the following codes.</span></span>



| <span data-ttu-id="685be-171">Valeur</span><span class="sxs-lookup"><span data-stu-id="685be-171">Value</span></span>                                                                                                       | <span data-ttu-id="685be-172">Description</span><span class="sxs-lookup"><span data-stu-id="685be-172">Description</span></span>                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="685be-173"><dt>**AUCUNE \_ erreur**</dt></span><span class="sxs-lookup"><span data-stu-id="685be-173"><dt>**NO\_ERROR**</dt></span></span> </dl>                    | <span data-ttu-id="685be-174">L’itinéraire a été ajouté ou mis à jour avec succès.</span><span class="sxs-lookup"><span data-stu-id="685be-174">The route was added or updated successfully.</span></span><br/>                 |
| <dl> <span data-ttu-id="685be-175"><dt>**HANDLE d’erreur \_ non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="685be-175"><dt>**ERROR\_INVALID\_HANDLE**</dt></span></span> </dl>       | <span data-ttu-id="685be-176">Le paramètre de handle du client n’est pas un handle valide.</span><span class="sxs-lookup"><span data-stu-id="685be-176">The client handle parameter is not a valid handle.</span></span><br/>           |
| <dl> <span data-ttu-id="685be-177"><dt>**paramètre d’erreur \_ non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="685be-177"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="685be-178">La structure de l’itinéraire contient un paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="685be-178">The route structure contains an invalid parameter.</span></span><br/>           |
| <dl> <span data-ttu-id="685be-179"><dt>**ERREUR \_ aucune \_ \_ ressource système**</dt></span><span class="sxs-lookup"><span data-stu-id="685be-179"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="685be-180">Les ressources sont insuffisantes pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="685be-180">There are insufficient resources to carry out the operation.</span></span><br/> |
| <dl> <span data-ttu-id="685be-181"><dt>**ERREUR \_ de \_ mémoire insuffisante \_**</dt></span><span class="sxs-lookup"><span data-stu-id="685be-181"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl>   | <span data-ttu-id="685be-182">La mémoire est insuffisante pour allouer l’entrée d’itinéraire.</span><span class="sxs-lookup"><span data-stu-id="685be-182">There is insufficient memory to allocate the route entry.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="685be-183">Notes</span><span class="sxs-lookup"><span data-stu-id="685be-183">Remarks</span></span>

<span data-ttu-id="685be-184">La fonction génère un message de modification de l’itinéraire si le meilleur itinéraire vers un réseau de destination a été modifié à la suite de cette opération.</span><span class="sxs-lookup"><span data-stu-id="685be-184">The function generates a route-change message if the best route to a destination network has changed as the result of this operation.</span></span> <span data-ttu-id="685be-185">Toutefois, le message de modification d’itinéraire n’est pas envoyé au client qui effectue cet appel.</span><span class="sxs-lookup"><span data-stu-id="685be-185">However, the route-change message is not sent to the client that makes this call.</span></span> <span data-ttu-id="685be-186">Au lieu de cela, les informations pertinentes sont retournées par cette fonction directement à ce client via les paramètres *Flags*, *CurBestRoute* et *PrevBestRoute* .</span><span class="sxs-lookup"><span data-stu-id="685be-186">Instead, relevant information is returned by this function directly to that client through the *Flags*, *CurBestRoute*, and *PrevBestRoute* parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="685be-187">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="685be-187">Requirements</span></span>



| <span data-ttu-id="685be-188">Condition requise</span><span class="sxs-lookup"><span data-stu-id="685be-188">Requirement</span></span> | <span data-ttu-id="685be-189">Valeur</span><span class="sxs-lookup"><span data-stu-id="685be-189">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="685be-190">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="685be-190">Minimum supported client</span></span><br/> | <span data-ttu-id="685be-191">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="685be-191">None supported</span></span><br/>                                                          |
| <span data-ttu-id="685be-192">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="685be-192">Minimum supported server</span></span><br/> | <span data-ttu-id="685be-193">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="685be-193">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="685be-194">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="685be-194">End of server support</span></span><br/>    | <span data-ttu-id="685be-195">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="685be-195">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="685be-196">En-tête</span><span class="sxs-lookup"><span data-stu-id="685be-196">Header</span></span><br/>                   | <dl> <span data-ttu-id="685be-197"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="685be-197"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="685be-198">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="685be-198">Library</span></span><br/>                  | <dl> <span data-ttu-id="685be-199"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="685be-199"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="685be-200">DLL</span><span class="sxs-lookup"><span data-stu-id="685be-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="685be-201"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="685be-201"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="685be-202">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="685be-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="685be-203">Référence de la version 1 du gestionnaire de tables de routage</span><span class="sxs-lookup"><span data-stu-id="685be-203">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="685be-204">Fonctions de la version 1 du gestionnaire de table de routage</span><span class="sxs-lookup"><span data-stu-id="685be-204">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="685be-205">**RtmDeleteRoute**</span><span class="sxs-lookup"><span data-stu-id="685be-205">**RtmDeleteRoute**</span></span>](rtmdeleteroute.md)
</dt> <dt>

[<span data-ttu-id="685be-206">**RtmDequeueRouteChangeMessage**</span><span class="sxs-lookup"><span data-stu-id="685be-206">**RtmDequeueRouteChangeMessage**</span></span>](rtmdequeueroutechangemessage.md)
</dt> </dl>

 

 





