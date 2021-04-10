---
title: Fonction RtmDeleteRoute (RTM. h)
description: La fonction RtmDeleteRoute supprime une entrée d’itinéraire.
ms.assetid: a98026e9-40f5-42e9-943c-dfc561feef6d
keywords:
- RtmDeleteRoute fonction RAS
topic_type:
- apiref
api_name:
- RtmDeleteRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 310364bdb6e6ba7daf285316fcaaf16884e53929
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942354"
---
# <a name="rtmdeleteroute-function"></a><span data-ttu-id="b5f1d-104">RtmDeleteRoute fonction)</span><span class="sxs-lookup"><span data-stu-id="b5f1d-104">RtmDeleteRoute function</span></span>

<span data-ttu-id="b5f1d-105">\[Cette API a été remplacée par l’API du [Gestionnaire de table de routage version 2](about-routing-table-manager-version-2.md) et n’est pas disponible au-delà de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b5f1d-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="b5f1d-106">Les applications doivent utiliser l’API du gestionnaire de table de routage version 2.\]</span><span class="sxs-lookup"><span data-stu-id="b5f1d-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="b5f1d-107">La fonction **RtmDeleteRoute** supprime une entrée d’itinéraire.</span><span class="sxs-lookup"><span data-stu-id="b5f1d-107">The **RtmDeleteRoute** function deletes a route entry.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5f1d-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b5f1d-108">Syntax</span></span>


```C++
DWORD RtmDeleteRoute(
  _In_  HANDLE ClientHandle,
  _In_  PVOID  Route,
  _Out_ DWORD  Flags,
  _Out_ PVOID  CurBestRoute
);
```



## <a name="parameters"></a><span data-ttu-id="b5f1d-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b5f1d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5f1d-110">*ClientHandle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b5f1d-110">*ClientHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5f1d-111">Handle qui identifie le client et, par conséquent, le protocole de routage de l’itinéraire ajouté ou mis à jour.</span><span class="sxs-lookup"><span data-stu-id="b5f1d-111">Handle that identifies the client and therefore the routing protocol of the added or updated route.</span></span> <span data-ttu-id="b5f1d-112">Obtenez ce handle en appelant [**RtmRegisterClient**](rtmregisterclient.md).</span><span class="sxs-lookup"><span data-stu-id="b5f1d-112">Obtain this handle by calling [**RtmRegisterClient**](rtmregisterclient.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5f1d-113">*Itinéraire* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b5f1d-113">*Route* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5f1d-114">Pointeur vers une structure spécifique à la famille de protocoles qui spécifie l’itinéraire nouveau ou mis à jour.</span><span class="sxs-lookup"><span data-stu-id="b5f1d-114">Pointer to a protocol-family-specific structure that specifies the new or updated route.</span></span> <span data-ttu-id="b5f1d-115">Les champs suivants sont utilisés par le gestionnaire de tables de routage pour mettre à jour la table de routage :</span><span class="sxs-lookup"><span data-stu-id="b5f1d-115">The following fields are used by the routing table manager to update the routing table:</span></span>



| <span data-ttu-id="b5f1d-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5f1d-116">Value</span></span>                                                                                                                                                                                                         | <span data-ttu-id="b5f1d-117">Signification</span><span class="sxs-lookup"><span data-stu-id="b5f1d-117">Meaning</span></span>                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span id="RR_Network"></span><span id="rr_network"></span><span id="RR_NETWORK"></span><dl> <span data-ttu-id="b5f1d-118"><dt>**Réseau de RR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b5f1d-118"><dt>**RR\_Network**</dt></span></span> </dl>                             | <span data-ttu-id="b5f1d-119">Spécifie le numéro de réseau de destination.</span><span class="sxs-lookup"><span data-stu-id="b5f1d-119">Specifies the destination network number.</span></span> <br/>                                 |
| <span id="RR_InterfaceID"></span><span id="rr_interfaceid"></span><span id="RR_INTERFACEID"></span><dl> <span data-ttu-id="b5f1d-120"><dt>**RR \_ InterfaceId**</dt></span><span class="sxs-lookup"><span data-stu-id="b5f1d-120"><dt>**RR\_InterfaceID**</dt></span></span> </dl>             | <span data-ttu-id="b5f1d-121">Spécifie l’index de l’interface par le biais duquel l’itinéraire a été reçu.</span><span class="sxs-lookup"><span data-stu-id="b5f1d-121">Specifies the index of the interface through which the route was received.</span></span><br/> |
| <span id="RR_NextHopAddress"></span><span id="rr_nexthopaddress"></span><span id="RR_NEXTHOPADDRESS"></span><dl> <span data-ttu-id="b5f1d-122"><dt>**\_NEXTHOPADDRESS RR**</dt></span><span class="sxs-lookup"><span data-stu-id="b5f1d-122"><dt>**RR\_NextHopAddress**</dt></span></span> </dl> | <span data-ttu-id="b5f1d-123">Spécifie l’adresse réseau du routeur de tronçon suivant.</span><span class="sxs-lookup"><span data-stu-id="b5f1d-123">Specifies the network address of the next-hop router.</span></span><br/>                      |



 

</dd> <dt>

<span data-ttu-id="b5f1d-124">*Indicateurs* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b5f1d-124">*Flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5f1d-125">Pointeur vers un jeu d’indicateurs qui indiquent le type du message de modification et les informations qui ont été placées dans les mémoires tampons fournies.</span><span class="sxs-lookup"><span data-stu-id="b5f1d-125">Pointer to a set of flags that indicate the type of the change message, and what information was placed in the provided buffers.</span></span> <span data-ttu-id="b5f1d-126">Ce paramètre est l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="b5f1d-126">This parameter is one of the following values.</span></span>



| <span data-ttu-id="b5f1d-127">Indicateurs</span><span class="sxs-lookup"><span data-stu-id="b5f1d-127">Flags</span></span>                                                                                                                                                                      | <span data-ttu-id="b5f1d-128">Signification</span><span class="sxs-lookup"><span data-stu-id="b5f1d-128">Meaning</span></span>                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_NO_CHANGE"></span><span id="rtm_no_change"></span><dl> <span data-ttu-id="b5f1d-129"><dt>**RTM- \_ aucune \_ modification**</dt></span><span class="sxs-lookup"><span data-stu-id="b5f1d-129"><dt>**RTM\_NO\_CHANGE**</dt></span></span> </dl>             | <span data-ttu-id="b5f1d-130">La suppression de l’itinéraire n’a pas affecté le meilleur itinéraire vers un réseau de destination.</span><span class="sxs-lookup"><span data-stu-id="b5f1d-130">Deleting the route did not affect the best route to any destination network.</span></span> <span data-ttu-id="b5f1d-131">En d’autres termes, une autre entrée représente un itinéraire vers le même réseau de destination et a une métrique inférieure.</span><span class="sxs-lookup"><span data-stu-id="b5f1d-131">In other words, another entry represents a route to the same destination network and has a lower metric.</span></span><br/> |
| <span id="RTM_ROUTE_DELETED"></span><span id="rtm_route_deleted"></span><dl> <span data-ttu-id="b5f1d-132"><dt>**\_itinéraire RTM \_ supprimé**</dt></span><span class="sxs-lookup"><span data-stu-id="b5f1d-132"><dt>**RTM\_ROUTE\_DELETED**</dt></span></span> </dl> | <span data-ttu-id="b5f1d-133">L’itinéraire supprimé était le seul itinéraire disponible pour un réseau de destination particulier.</span><span class="sxs-lookup"><span data-stu-id="b5f1d-133">The route deleted was the only route available for a particular destination network.</span></span><br/>                                                                                                  |
| <span id="RTM_ROUTE_CHANGED"></span><span id="rtm_route_changed"></span><dl> <span data-ttu-id="b5f1d-134"><dt>**\_itinéraire RTM \_ modifié**</dt></span><span class="sxs-lookup"><span data-stu-id="b5f1d-134"><dt>**RTM\_ROUTE\_CHANGED**</dt></span></span> </dl> | <span data-ttu-id="b5f1d-135">Après la suppression de cet itinéraire, un autre itinéraire est devenu le meilleur itinéraire vers un réseau de destination particulier.</span><span class="sxs-lookup"><span data-stu-id="b5f1d-135">After this route was deleted, another route became the best route to a particular destination network.</span></span> <span data-ttu-id="b5f1d-136">*CurBestRoute* pointe vers les informations pour le nouveau meilleur itinéraire.</span><span class="sxs-lookup"><span data-stu-id="b5f1d-136">*CurBestRoute* points to the information for the new best route.</span></span><br/>               |



 

</dd> <dt>

<span data-ttu-id="b5f1d-137">*CurBestRoute* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b5f1d-137">*CurBestRoute* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5f1d-138">Pointeur vers une structure qui reçoit les informations de meilleure route actuelles, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="b5f1d-138">Pointer to a structure that receives the current best-route information, if any.</span></span> <span data-ttu-id="b5f1d-139">Le type de la structure est spécifique à la famille de protocoles, par exemple, IP ou IPX.</span><span class="sxs-lookup"><span data-stu-id="b5f1d-139">The type of the structure is specific to the protocol family, for example, IP or IPX.</span></span>

<span data-ttu-id="b5f1d-140">Ce paramètre est facultatif.</span><span class="sxs-lookup"><span data-stu-id="b5f1d-140">This parameter is optional.</span></span> <span data-ttu-id="b5f1d-141">Si l’appelant spécifie la **valeur null** pour ce paramètre, les informations de meilleure route actuelles ne sont pas retournées.</span><span class="sxs-lookup"><span data-stu-id="b5f1d-141">If the caller specifies **NULL** for this parameter, the current best-route information is not returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5f1d-142">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b5f1d-142">Return value</span></span>

<span data-ttu-id="b5f1d-143">Si la fonction est réussie, la valeur de retour n’est **pas une \_ erreur**.</span><span class="sxs-lookup"><span data-stu-id="b5f1d-143">If the function succeeds, the return value is **NO\_ERROR**.</span></span>

<span data-ttu-id="b5f1d-144">Si la fonction échoue, la valeur de retour est l’un des codes d’erreur suivants.</span><span class="sxs-lookup"><span data-stu-id="b5f1d-144">If the function fails, the return value is one of the following error codes.</span></span>



| <span data-ttu-id="b5f1d-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5f1d-145">Value</span></span>                                                                                                       | <span data-ttu-id="b5f1d-146">Description</span><span class="sxs-lookup"><span data-stu-id="b5f1d-146">Description</span></span>                                                                                            |
|-------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b5f1d-147"><dt>**HANDLE d’erreur \_ non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b5f1d-147"><dt>**ERROR\_INVALID\_HANDLE**</dt></span></span> </dl>       | <span data-ttu-id="b5f1d-148">Le paramètre de handle du client n’est pas un handle valide.</span><span class="sxs-lookup"><span data-stu-id="b5f1d-148">The client handle parameter is not a valid handle.</span></span><br/>                                          |
| <dl> <span data-ttu-id="b5f1d-149"><dt>**paramètre d’erreur \_ non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b5f1d-149"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="b5f1d-150">La structure d’itinéraire vers laquelle pointe le paramètre d' *itinéraire* contient une valeur de membre.</span><span class="sxs-lookup"><span data-stu-id="b5f1d-150">The route structure pointed to by the *Route* parameter contains a member value.</span></span><br/>            |
| <dl> <span data-ttu-id="b5f1d-151"><dt>**ERREUR \_ aucun \_ itinéraire de ce type \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b5f1d-151"><dt>**ERROR\_NO\_SUCH\_ROUTE**</dt></span></span> </dl>       | <span data-ttu-id="b5f1d-152">Il n’existe aucune entrée dans la table de routage qui correspond aux paramètres de l’itinéraire spécifié.</span><span class="sxs-lookup"><span data-stu-id="b5f1d-152">There are no entries in the routing table that match the parameters of the specified route.</span></span><br/> |
| <dl> <span data-ttu-id="b5f1d-153"><dt>**ERREUR \_ aucune \_ \_ ressource système**</dt></span><span class="sxs-lookup"><span data-stu-id="b5f1d-153"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="b5f1d-154">Les ressources sont insuffisantes pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="b5f1d-154">There are insufficient resources to perform the operation.</span></span> <br/>                                 |



 

## <a name="remarks"></a><span data-ttu-id="b5f1d-155">Notes</span><span class="sxs-lookup"><span data-stu-id="b5f1d-155">Remarks</span></span>

<span data-ttu-id="b5f1d-156">La fonction génère un message de modification d’itinéraire si le meilleur itinéraire vers un réseau de destination a été modifié à la suite de la suppression.</span><span class="sxs-lookup"><span data-stu-id="b5f1d-156">The function generates a route-change message if the best route to a destination network has changed as the result of the deletion.</span></span> <span data-ttu-id="b5f1d-157">Toutefois, le message de modification d’itinéraire n’est pas envoyé au client qui effectue cet appel.</span><span class="sxs-lookup"><span data-stu-id="b5f1d-157">However, the route-change message is not sent to the client that makes this call.</span></span> <span data-ttu-id="b5f1d-158">Au lieu de cela, les informations pertinentes sont retournées par cette fonction directement à ce client.</span><span class="sxs-lookup"><span data-stu-id="b5f1d-158">Instead, relevant information is returned by this function directly to that client.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5f1d-159">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b5f1d-159">Requirements</span></span>



| <span data-ttu-id="b5f1d-160">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b5f1d-160">Requirement</span></span> | <span data-ttu-id="b5f1d-161">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5f1d-161">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b5f1d-162">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5f1d-162">Minimum supported client</span></span><br/> | <span data-ttu-id="b5f1d-163">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5f1d-163">None supported</span></span><br/>                                                          |
| <span data-ttu-id="b5f1d-164">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5f1d-164">Minimum supported server</span></span><br/> | <span data-ttu-id="b5f1d-165">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b5f1d-165">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b5f1d-166">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="b5f1d-166">End of server support</span></span><br/>    | <span data-ttu-id="b5f1d-167">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b5f1d-167">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="b5f1d-168">En-tête</span><span class="sxs-lookup"><span data-stu-id="b5f1d-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5f1d-169"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5f1d-169"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="b5f1d-170">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b5f1d-170">Library</span></span><br/>                  | <dl> <span data-ttu-id="b5f1d-171"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b5f1d-171"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="b5f1d-172">DLL</span><span class="sxs-lookup"><span data-stu-id="b5f1d-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5f1d-173"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5f1d-173"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5f1d-174">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5f1d-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5f1d-175">Référence de la version 1 du gestionnaire de tables de routage</span><span class="sxs-lookup"><span data-stu-id="b5f1d-175">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="b5f1d-176">Fonctions de la version 1 du gestionnaire de table de routage</span><span class="sxs-lookup"><span data-stu-id="b5f1d-176">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="b5f1d-177">**RtmAddRoute**</span><span class="sxs-lookup"><span data-stu-id="b5f1d-177">**RtmAddRoute**</span></span>](rtmaddroute.md)
</dt> <dt>

[<span data-ttu-id="b5f1d-178">**RtmDequeueRouteChangeMessage**</span><span class="sxs-lookup"><span data-stu-id="b5f1d-178">**RtmDequeueRouteChangeMessage**</span></span>](rtmdequeueroutechangemessage.md)
</dt> </dl>

 

 





