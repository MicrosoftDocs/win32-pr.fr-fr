---
title: Fonction RtmGetFirstRoute (RTM. h)
description: La fonction RtmGetFirstRoute retourne le premier itinéraire du sous-ensemble spécifié d’itinéraires dans la table.
ms.assetid: f2071b50-4b06-432f-8dbf-45696f8a5cb1
keywords:
- RtmGetFirstRoute fonction RAS
topic_type:
- apiref
api_name:
- RtmGetFirstRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32e98a5deb0f925fbf3b27c21302060bbe4869b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104386"
---
# <a name="rtmgetfirstroute-function"></a><span data-ttu-id="95e2e-104">RtmGetFirstRoute fonction)</span><span class="sxs-lookup"><span data-stu-id="95e2e-104">RtmGetFirstRoute function</span></span>

<span data-ttu-id="95e2e-105">\[Cette API a été remplacée par l’API du [Gestionnaire de table de routage version 2](about-routing-table-manager-version-2.md) et n’est pas disponible au-delà de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="95e2e-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="95e2e-106">Les applications doivent utiliser l’API du gestionnaire de table de routage version 2.\]</span><span class="sxs-lookup"><span data-stu-id="95e2e-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="95e2e-107">La fonction **RtmGetFirstRoute** retourne le premier itinéraire du sous-ensemble spécifié d’itinéraires dans la table.</span><span class="sxs-lookup"><span data-stu-id="95e2e-107">The **RtmGetFirstRoute** function returns the first route from the specified subset of routes in the table.</span></span>

## <a name="syntax"></a><span data-ttu-id="95e2e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="95e2e-108">Syntax</span></span>


```C++
DWORD RtmGetFirstRoute(
  _In_    DWORD ProtocolFamily,
  _In_    DWORD EnumerationFlags,
  _Inout_ PVOID Route
);
```



## <a name="parameters"></a><span data-ttu-id="95e2e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="95e2e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95e2e-110">*ProtocolFamily* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="95e2e-110">*ProtocolFamily* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95e2e-111">Spécifie la famille de protocoles d’itinéraires à récupérer, par exemple, IP ou IPX.</span><span class="sxs-lookup"><span data-stu-id="95e2e-111">Specifies the protocol family of routes to retrieve, for example, IP or IPX.</span></span>

</dd> <dt>

<span data-ttu-id="95e2e-112">*EnumerationFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="95e2e-112">*EnumerationFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95e2e-113">Spécifie que limite le jeu d’itinéraires supprimés à un sous-ensemble défini par ces indicateurs et les valeurs des membres correspondants de la structure vers laquelle pointe le paramètre *CriteriaRoute* .</span><span class="sxs-lookup"><span data-stu-id="95e2e-113">Specifies the limits the set of deleted routes to a subset defined by these flags and the values in the corresponding members of the structure pointed to by the *CriteriaRoute* parameter.</span></span> <span data-ttu-id="95e2e-114">Les indicateurs sont les mêmes que ceux utilisés dans [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).</span><span class="sxs-lookup"><span data-stu-id="95e2e-114">The flags are the same as those used in [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).</span></span>

</dd> <dt>

<span data-ttu-id="95e2e-115">*Itinéraire* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="95e2e-115">*Route* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="95e2e-116">En entrée, l' *itinéraire* pointe vers une structure spécifique à la famille de protocoles ( [**\_ \_ itinéraire IP RTM**](rtm-ip-route.md) ou [**\_ \_ itinéraire IPX RTM**](rtm-ipx-route.md)).</span><span class="sxs-lookup"><span data-stu-id="95e2e-116">On input, *Route* points to a protocol-family-specific structure ( [**RTM\_IP\_ROUTE**](rtm-ip-route.md) or [**RTM\_IPX\_ROUTE**](rtm-ipx-route.md)).</span></span>

<span data-ttu-id="95e2e-117">La fonction appelante fournit des valeurs de membre pour cette structure.</span><span class="sxs-lookup"><span data-stu-id="95e2e-117">The calling function provides member values for this structure.</span></span> <span data-ttu-id="95e2e-118">Ces valeurs, conjointement avec le paramètre *EnumerationFlags* , spécifient le jeu à partir duquel les itinéraires doivent être retournés.</span><span class="sxs-lookup"><span data-stu-id="95e2e-118">These values, in conjunction with the *EnumerationFlags* parameter, specify the set from which to return routes.</span></span>

<span data-ttu-id="95e2e-119">Sortie de sortie, *itinéraire* pointe vers le premier itinéraire correspondant aux critères spécifiés.</span><span class="sxs-lookup"><span data-stu-id="95e2e-119">Out output, *Route* points to the first route that matched the specified criteria.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95e2e-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="95e2e-120">Return value</span></span>

<span data-ttu-id="95e2e-121">Si la fonction est réussie, la valeur de retour n’est pas une \_ erreur.</span><span class="sxs-lookup"><span data-stu-id="95e2e-121">If the function succeeds, the return value is NO\_ERROR.</span></span>

<span data-ttu-id="95e2e-122">Si la fonction échoue, la valeur de retour est l’un des codes d’erreur suivants.</span><span class="sxs-lookup"><span data-stu-id="95e2e-122">If the function fails, the return value is one of the following error codes.</span></span>



| <span data-ttu-id="95e2e-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="95e2e-123">Value</span></span>                                                                                                       | <span data-ttu-id="95e2e-124">Description</span><span class="sxs-lookup"><span data-stu-id="95e2e-124">Description</span></span>                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="95e2e-125"><dt>**paramètre d’erreur \_ non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="95e2e-125"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="95e2e-126">L’un des paramètres n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="95e2e-126">One of the parameters is invalid.</span></span><br/>                            |
| <dl> <span data-ttu-id="95e2e-127"><dt>**ERREUR \_ aucun \_ itinéraire**</dt></span><span class="sxs-lookup"><span data-stu-id="95e2e-127"><dt>**ERROR\_NO\_ROUTES**</dt></span></span> </dl>            | <span data-ttu-id="95e2e-128">Aucun itinéraire ne correspond aux critères spécifiés.</span><span class="sxs-lookup"><span data-stu-id="95e2e-128">There are no routes that match the specified criteria.</span></span><br/>       |
| <dl> <span data-ttu-id="95e2e-129"><dt>**ERREUR \_ aucune \_ \_ ressource système**</dt></span><span class="sxs-lookup"><span data-stu-id="95e2e-129"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="95e2e-130">Les ressources sont insuffisantes pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="95e2e-130">There are insufficient resources to carry out the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="95e2e-131">Notes</span><span class="sxs-lookup"><span data-stu-id="95e2e-131">Remarks</span></span>

<span data-ttu-id="95e2e-132">Les itinéraires sont retournés dans l’ordre suivant :</span><span class="sxs-lookup"><span data-stu-id="95e2e-132">The routes are returned in the following order:</span></span>

1.  <span data-ttu-id="95e2e-133">Numéro de réseau</span><span class="sxs-lookup"><span data-stu-id="95e2e-133">Network number</span></span>
2.  <span data-ttu-id="95e2e-134">Protocole de routage</span><span class="sxs-lookup"><span data-stu-id="95e2e-134">Routing protocol</span></span>
3.  <span data-ttu-id="95e2e-135">Identificateur d’interface</span><span class="sxs-lookup"><span data-stu-id="95e2e-135">Interface identifier</span></span>
4.  <span data-ttu-id="95e2e-136">Adresse du tronçon suivant</span><span class="sxs-lookup"><span data-stu-id="95e2e-136">Next-hop address</span></span>

<span data-ttu-id="95e2e-137">Cette fonction est moins efficace que la fonction de handle d’énumération correspondante, [**RtmEnumerateGetNextRoute**](rtmenumerategetnextroute.md).</span><span class="sxs-lookup"><span data-stu-id="95e2e-137">This function is less efficient than the corresponding enumeration handle function, [**RtmEnumerateGetNextRoute**](rtmenumerategetnextroute.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="95e2e-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="95e2e-138">Requirements</span></span>



| <span data-ttu-id="95e2e-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="95e2e-139">Requirement</span></span> | <span data-ttu-id="95e2e-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="95e2e-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="95e2e-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="95e2e-141">Minimum supported client</span></span><br/> | <span data-ttu-id="95e2e-142">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="95e2e-142">None supported</span></span><br/>                                                          |
| <span data-ttu-id="95e2e-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="95e2e-143">Minimum supported server</span></span><br/> | <span data-ttu-id="95e2e-144">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="95e2e-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="95e2e-145">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="95e2e-145">End of server support</span></span><br/>    | <span data-ttu-id="95e2e-146">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="95e2e-146">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="95e2e-147">En-tête</span><span class="sxs-lookup"><span data-stu-id="95e2e-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="95e2e-148"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="95e2e-148"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="95e2e-149">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="95e2e-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="95e2e-150"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="95e2e-150"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="95e2e-151">DLL</span><span class="sxs-lookup"><span data-stu-id="95e2e-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95e2e-152"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95e2e-152"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95e2e-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="95e2e-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95e2e-154">Référence de la version 1 du gestionnaire de tables de routage</span><span class="sxs-lookup"><span data-stu-id="95e2e-154">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="95e2e-155">Fonctions de la version 1 du gestionnaire de table de routage</span><span class="sxs-lookup"><span data-stu-id="95e2e-155">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="95e2e-156">**RtmCloseEnumerationHandle**</span><span class="sxs-lookup"><span data-stu-id="95e2e-156">**RtmCloseEnumerationHandle**</span></span>](rtmcloseenumerationhandle.md)
</dt> <dt>

[<span data-ttu-id="95e2e-157">**RtmCreateEnumerationHandle**</span><span class="sxs-lookup"><span data-stu-id="95e2e-157">**RtmCreateEnumerationHandle**</span></span>](rtmcreateenumerationhandle.md)
</dt> <dt>

[<span data-ttu-id="95e2e-158">**RtmEnumerateGetNextRoute**</span><span class="sxs-lookup"><span data-stu-id="95e2e-158">**RtmEnumerateGetNextRoute**</span></span>](rtmenumerategetnextroute.md)
</dt> <dt>

[<span data-ttu-id="95e2e-159">**RtmGetNextRoute**</span><span class="sxs-lookup"><span data-stu-id="95e2e-159">**RtmGetNextRoute**</span></span>](rtmgetnextroute.md)
</dt> </dl>

 

 





