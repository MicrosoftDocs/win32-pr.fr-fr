---
title: Fonction RtmGetNextRoute (RTM. h)
description: La fonction RtmGetNextRoute retourne l’itinéraire suivant à partir du sous-ensemble spécifié d’itinéraires dans la table.
ms.assetid: 0f413276-2ace-4216-a1a0-1b3061bacc4a
keywords:
- RtmGetNextRoute fonction RAS
topic_type:
- apiref
api_name:
- RtmGetNextRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da8592855e0c30cef2ed43b7818badd336bc2ab6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508782"
---
# <a name="rtmgetnextroute-function"></a><span data-ttu-id="d6f0b-104">RtmGetNextRoute fonction)</span><span class="sxs-lookup"><span data-stu-id="d6f0b-104">RtmGetNextRoute function</span></span>

<span data-ttu-id="d6f0b-105">\[Cette API a été remplacée par l’API du [Gestionnaire de table de routage version 2](about-routing-table-manager-version-2.md) et n’est pas disponible au-delà de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d6f0b-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="d6f0b-106">Les applications doivent utiliser l’API du gestionnaire de table de routage version 2.\]</span><span class="sxs-lookup"><span data-stu-id="d6f0b-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="d6f0b-107">La fonction **RtmGetNextRoute** retourne l’itinéraire suivant à partir du sous-ensemble spécifié d’itinéraires dans la table.</span><span class="sxs-lookup"><span data-stu-id="d6f0b-107">The **RtmGetNextRoute** function returns the next route from the specified subset of routes in the table.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6f0b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d6f0b-108">Syntax</span></span>


```C++
DWORD RtmGetNextRoute(
  _In_    DWORD ProtocolFamily,
  _In_    DWORD EnumerationFlags,
  _Inout_ PVOID Route
);
```



## <a name="parameters"></a><span data-ttu-id="d6f0b-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d6f0b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6f0b-110">*ProtocolFamily* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d6f0b-110">*ProtocolFamily* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6f0b-111">Spécifie la famille de protocoles d’itinéraires à récupérer, par exemple, IP ou IPX.</span><span class="sxs-lookup"><span data-stu-id="d6f0b-111">Specifies the protocol family of routes to retrieve, for example, IP or IPX.</span></span>

</dd> <dt>

<span data-ttu-id="d6f0b-112">*EnumerationFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d6f0b-112">*EnumerationFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6f0b-113">Spécifie les itinéraires qui doivent être énumérés.</span><span class="sxs-lookup"><span data-stu-id="d6f0b-113">Specifies which routes should be enumerated.</span></span> <span data-ttu-id="d6f0b-114">Ce paramètre limite l’ensemble des itinéraires supprimés à un sous-ensemble défini par les indicateurs suivants et les valeurs des membres correspondants de la structure vers laquelle pointe le paramètre *CriteriaRoute* .</span><span class="sxs-lookup"><span data-stu-id="d6f0b-114">This parameter limits the set of deleted routes to a subset defined by the following flags and the values in the corresponding members of the structure pointed to by the *CriteriaRoute* parameter.</span></span> <span data-ttu-id="d6f0b-115">Les indicateurs sont les mêmes que ceux utilisés dans [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).</span><span class="sxs-lookup"><span data-stu-id="d6f0b-115">The flags are the same as those used in [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).</span></span>

</dd> <dt>

<span data-ttu-id="d6f0b-116">*Itinéraire* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d6f0b-116">*Route* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d6f0b-117">En entrée, l' *itinéraire* pointe vers une structure spécifique à la famille de protocoles ( [**\_ \_ itinéraire IP RTM**](rtm-ip-route.md) ou [**\_ \_ itinéraire IPX RTM**](rtm-ipx-route.md)).</span><span class="sxs-lookup"><span data-stu-id="d6f0b-117">On input, *Route* points to a protocol-family-specific structure ( [**RTM\_IP\_ROUTE**](rtm-ip-route.md) or [**RTM\_IPX\_ROUTE**](rtm-ipx-route.md)).</span></span>

<span data-ttu-id="d6f0b-118">La fonction appelante fournit des valeurs de membre pour cette structure.</span><span class="sxs-lookup"><span data-stu-id="d6f0b-118">The calling function provides member values for this structure.</span></span> <span data-ttu-id="d6f0b-119">Ces valeurs, conjointement avec le paramètre *EnumerationFlags* , spécifient le jeu à partir duquel les itinéraires doivent être retournés.</span><span class="sxs-lookup"><span data-stu-id="d6f0b-119">These values, in conjunction with the *EnumerationFlags* parameter, specify the set from which to return routes.</span></span>

<span data-ttu-id="d6f0b-120">Lors de la sortie, l' *itinéraire* pointe vers une structure qui reçoit le premier itinéraire correspondant aux critères spécifiés.</span><span class="sxs-lookup"><span data-stu-id="d6f0b-120">On output, *Route* points to a structure that receives the first route that matched the specified criteria.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6f0b-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d6f0b-121">Return value</span></span>

<span data-ttu-id="d6f0b-122">Si la fonction est réussie, la valeur de retour n’est **pas une \_ erreur**.</span><span class="sxs-lookup"><span data-stu-id="d6f0b-122">If the function succeeds, the return value is **NO\_ERROR**.</span></span>

<span data-ttu-id="d6f0b-123">Si la fonction échoue, la valeur de retour est l’un des codes d’erreur suivants.</span><span class="sxs-lookup"><span data-stu-id="d6f0b-123">If the function fails, the return value is one of the following error codes.</span></span>



| <span data-ttu-id="d6f0b-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="d6f0b-124">Value</span></span>                                                                                                       | <span data-ttu-id="d6f0b-125">Description</span><span class="sxs-lookup"><span data-stu-id="d6f0b-125">Description</span></span>                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d6f0b-126"><dt>**paramètre d’erreur \_ non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d6f0b-126"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="d6f0b-127">L’un des paramètres n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="d6f0b-127">One of the parameters is invalid.</span></span><br/>                            |
| <dl> <span data-ttu-id="d6f0b-128"><dt>**ERREUR \_ aucun \_ itinéraire**</dt></span><span class="sxs-lookup"><span data-stu-id="d6f0b-128"><dt>**ERROR\_NO\_ROUTES**</dt></span></span> </dl>            | <span data-ttu-id="d6f0b-129">Aucun itinéraire ne correspond aux critères spécifiés.</span><span class="sxs-lookup"><span data-stu-id="d6f0b-129">There are no routes that match the specified criteria.</span></span><br/>       |
| <dl> <span data-ttu-id="d6f0b-130"><dt>**ERREUR \_ aucune \_ \_ ressource système**</dt></span><span class="sxs-lookup"><span data-stu-id="d6f0b-130"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="d6f0b-131">Les ressources sont insuffisantes pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="d6f0b-131">There are insufficient resources to carry out the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d6f0b-132">Notes</span><span class="sxs-lookup"><span data-stu-id="d6f0b-132">Remarks</span></span>

<span data-ttu-id="d6f0b-133">Les itinéraires sont retournés dans l’ordre suivant :</span><span class="sxs-lookup"><span data-stu-id="d6f0b-133">The routes are returned in the following order:</span></span>

1.  <span data-ttu-id="d6f0b-134">Numéro de réseau</span><span class="sxs-lookup"><span data-stu-id="d6f0b-134">Network number</span></span>
2.  <span data-ttu-id="d6f0b-135">Protocole de routage</span><span class="sxs-lookup"><span data-stu-id="d6f0b-135">Routing protocol</span></span>
3.  <span data-ttu-id="d6f0b-136">Identificateur d’interface</span><span class="sxs-lookup"><span data-stu-id="d6f0b-136">Interface identifier</span></span>
4.  <span data-ttu-id="d6f0b-137">Adresse du tronçon suivant</span><span class="sxs-lookup"><span data-stu-id="d6f0b-137">Next-hop address</span></span>

<span data-ttu-id="d6f0b-138">Cette fonction est moins efficace que les fonctions de handle d’énumération correspondantes.</span><span class="sxs-lookup"><span data-stu-id="d6f0b-138">This function is less efficient than the corresponding enumeration handle functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6f0b-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d6f0b-139">Requirements</span></span>



| <span data-ttu-id="d6f0b-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d6f0b-140">Requirement</span></span> | <span data-ttu-id="d6f0b-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="d6f0b-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d6f0b-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6f0b-142">Minimum supported client</span></span><br/> | <span data-ttu-id="d6f0b-143">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6f0b-143">None supported</span></span><br/>                                                          |
| <span data-ttu-id="d6f0b-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6f0b-144">Minimum supported server</span></span><br/> | <span data-ttu-id="d6f0b-145">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d6f0b-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d6f0b-146">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="d6f0b-146">End of server support</span></span><br/>    | <span data-ttu-id="d6f0b-147">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d6f0b-147">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="d6f0b-148">En-tête</span><span class="sxs-lookup"><span data-stu-id="d6f0b-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6f0b-149"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6f0b-149"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="d6f0b-150">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d6f0b-150">Library</span></span><br/>                  | <dl> <span data-ttu-id="d6f0b-151"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d6f0b-151"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="d6f0b-152">DLL</span><span class="sxs-lookup"><span data-stu-id="d6f0b-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6f0b-153"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6f0b-153"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6f0b-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6f0b-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6f0b-155">Référence de la version 1 du gestionnaire de tables de routage</span><span class="sxs-lookup"><span data-stu-id="d6f0b-155">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="d6f0b-156">Fonctions de la version 1 du gestionnaire de table de routage</span><span class="sxs-lookup"><span data-stu-id="d6f0b-156">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="d6f0b-157">**RtmCloseEnumerationHandle**</span><span class="sxs-lookup"><span data-stu-id="d6f0b-157">**RtmCloseEnumerationHandle**</span></span>](rtmcloseenumerationhandle.md)
</dt> <dt>

[<span data-ttu-id="d6f0b-158">**RtmCreateEnumerationHandle**</span><span class="sxs-lookup"><span data-stu-id="d6f0b-158">**RtmCreateEnumerationHandle**</span></span>](rtmcreateenumerationhandle.md)
</dt> <dt>

[<span data-ttu-id="d6f0b-159">**RtmEnumerateGetNextRoute**</span><span class="sxs-lookup"><span data-stu-id="d6f0b-159">**RtmEnumerateGetNextRoute**</span></span>](rtmenumerategetnextroute.md)
</dt> <dt>

[<span data-ttu-id="d6f0b-160">**RtmGetFirstRoute**</span><span class="sxs-lookup"><span data-stu-id="d6f0b-160">**RtmGetFirstRoute**</span></span>](rtmgetfirstroute.md)
</dt> </dl>

 

 





