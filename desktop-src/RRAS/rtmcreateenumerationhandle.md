---
title: Fonction RtmCreateEnumerationHandle (RTM. h)
description: La fonction RtmCreateEnumerationHandle retourne un handle à utiliser avec RtmEnumerateGetNextRoute pour analyser tous les itinéraires, ou un sous-ensemble d’itinéraires, connus du gestionnaire de tables de routage.
ms.assetid: 73e3ac7d-498a-4d89-a6b5-17aaf4b17ec2
keywords:
- RtmCreateEnumerationHandle fonction RAS
topic_type:
- apiref
api_name:
- RtmCreateEnumerationHandle
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14086639db299038139e0e7d02eb12bb892042bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103116"
---
# <a name="rtmcreateenumerationhandle-function"></a><span data-ttu-id="9251f-104">RtmCreateEnumerationHandle fonction)</span><span class="sxs-lookup"><span data-stu-id="9251f-104">RtmCreateEnumerationHandle function</span></span>

<span data-ttu-id="9251f-105">\[Cette API a été remplacée par l’API du [Gestionnaire de table de routage version 2](about-routing-table-manager-version-2.md) et n’est pas disponible au-delà de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="9251f-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="9251f-106">Les applications doivent utiliser l’API du gestionnaire de table de routage version 2.\]</span><span class="sxs-lookup"><span data-stu-id="9251f-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="9251f-107">La fonction **RtmCreateEnumerationHandle** retourne un handle à utiliser avec [**RtmEnumerateGetNextRoute**](rtmenumerategetnextroute.md) pour analyser tous les itinéraires, ou un sous-ensemble d’itinéraires, connus du gestionnaire de tables de routage.</span><span class="sxs-lookup"><span data-stu-id="9251f-107">The **RtmCreateEnumerationHandle** function returns a handle to use with [**RtmEnumerateGetNextRoute**](rtmenumerategetnextroute.md) to scan through all routes, or a subset of routes, known to the routing table manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="9251f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9251f-108">Syntax</span></span>


```C++
HANDLE RtmCreateEnumerationHandle(
  _In_ DWORD ProtocolFamily,
  _In_ DWORD EnumerationFlags,
  _In_ PVOID CriteriaRoute
);
```



## <a name="parameters"></a><span data-ttu-id="9251f-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9251f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9251f-110">*ProtocolFamily* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9251f-110">*ProtocolFamily* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9251f-111">Spécifie la famille de protocoles des itinéraires à énumérer.</span><span class="sxs-lookup"><span data-stu-id="9251f-111">Specifies the protocol family of the routes to enumerate.</span></span>

</dd> <dt>

<span data-ttu-id="9251f-112">*EnumerationFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9251f-112">*EnumerationFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9251f-113">Spécifie les itinéraires qui doivent être énumérés.</span><span class="sxs-lookup"><span data-stu-id="9251f-113">Specifies which routes should be enumerated.</span></span> <span data-ttu-id="9251f-114">Ce paramètre limite l’ensemble des itinéraires retournés par l’API d’énumération à un sous-ensemble défini par les indicateurs suivants et les valeurs des membres correspondants de la structure vers laquelle pointe le paramètre *CriteriaRoute* .</span><span class="sxs-lookup"><span data-stu-id="9251f-114">This parameter limits the set of routes returned by the enumeration API to a subset defined by the following flags and the values in the corresponding members of the structure pointed to by the *CriteriaRoute* parameter.</span></span> <span data-ttu-id="9251f-115">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="9251f-115">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="9251f-116">EnumerationFlags</span><span class="sxs-lookup"><span data-stu-id="9251f-116">EnumerationFlags</span></span>                                                                                                                                                                              | <span data-ttu-id="9251f-117">Signification</span><span class="sxs-lookup"><span data-stu-id="9251f-117">Meaning</span></span>                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_ONLY_THIS_NETWORK"></span><span id="rtm_only_this_network"></span><dl> <span data-ttu-id="9251f-118"><dt>**RTM \_ uniquement \_ ce \_ réseau**</dt></span><span class="sxs-lookup"><span data-stu-id="9251f-118"><dt>**RTM\_ONLY\_THIS\_NETWORK**</dt></span></span> </dl>       | <span data-ttu-id="9251f-119">Énumérer uniquement les itinéraires qui ont le même numéro de réseau que le \_ membre de réseau RR de la structure vers laquelle pointe CriteriaRoute.</span><span class="sxs-lookup"><span data-stu-id="9251f-119">Enumerate only those routes that have the same network number as the RR\_Network member of the structure pointed to by CriteriaRoute.</span></span><br/>                        |
| <span id="RTM_ONLY_THIS_INTERFACE"></span><span id="rtm_only_this_interface"></span><dl> <span data-ttu-id="9251f-120"><dt>**RTM \_ uniquement \_ cette \_ interface**</dt></span><span class="sxs-lookup"><span data-stu-id="9251f-120"><dt>**RTM\_ONLY\_THIS\_INTERFACE**</dt></span></span> </dl> | <span data-ttu-id="9251f-121">Énumère uniquement les itinéraires obtenus par le biais de l’interface spécifiée par le \_ champ de RR InterfaceId de la structure vers laquelle pointe CriteriaRoute.</span><span class="sxs-lookup"><span data-stu-id="9251f-121">Enumerate only those routes that were obtained through the interface specified by the RR\_InterfaceID field of the structure pointed to by CriteriaRoute.</span></span><br/>    |
| <span id="RTM_ONLY_THIS_PROTOCOL"></span><span id="rtm_only_this_protocol"></span><dl> <span data-ttu-id="9251f-122"><dt>**RTM \_ uniquement \_ ce \_ protocole**</dt></span><span class="sxs-lookup"><span data-stu-id="9251f-122"><dt>**RTM\_ONLY\_THIS\_PROTOCOL**</dt></span></span> </dl>    | <span data-ttu-id="9251f-123">Énumère uniquement les itinéraires qui ont été ajoutés par le protocole de routage spécifié par le \_ champ ROUTINGPROTOCOL RR de la structure vers laquelle pointe CriteriaRoute.</span><span class="sxs-lookup"><span data-stu-id="9251f-123">Enumerate only those routes that were added by the routing protocol specified by the RR\_RoutingProtocol field of the structure pointed to by CriteriaRoute.</span></span><br/> |
| <span id="RTM_ONLY_BEST_ROUTES"></span><span id="rtm_only_best_routes"></span><dl> <span data-ttu-id="9251f-124"><dt>**les \_ \_ meilleurs \_ itinéraires RTM**</dt></span><span class="sxs-lookup"><span data-stu-id="9251f-124"><dt>**RTM\_ONLY\_BEST\_ROUTES**</dt></span></span> </dl>          | <span data-ttu-id="9251f-125">Énumérer uniquement les meilleurs itinéraires à chacun des réseaux de l’ensemble.</span><span class="sxs-lookup"><span data-stu-id="9251f-125">Enumerate only the best routes to each of the networks in the set.</span></span><br/>                                                                                           |



 

</dd> <dt>

<span data-ttu-id="9251f-126">*CriteriaRoute* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9251f-126">*CriteriaRoute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9251f-127">Pointeur vers une structure de route spécifique à la famille de protocoles ([**\_ \_ itinéraire IP RTM**](rtm-ip-route.md) ou [**\_ \_ itinéraire IPX RTM**](rtm-ipx-route.md)).</span><span class="sxs-lookup"><span data-stu-id="9251f-127">Pointer to a protocol-family-specific route structure ([**RTM\_IP\_ROUTE**](rtm-ip-route.md) or [**RTM\_IPX\_ROUTE**](rtm-ipx-route.md)).</span></span> <span data-ttu-id="9251f-128">Les valeurs de membre de cette structure correspondent aux indicateurs spécifiés par le paramètre *EnumerationFlags* .</span><span class="sxs-lookup"><span data-stu-id="9251f-128">The member values in this structure correspond to the flags specified by the *EnumerationFlags* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9251f-129">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9251f-129">Return value</span></span>

<span data-ttu-id="9251f-130">Si la fonction est réussie, la valeur de retour est un **handle** à utiliser avec les appels d’énumération suivants.</span><span class="sxs-lookup"><span data-stu-id="9251f-130">If the function succeeds, the return value is a **HANDLE** to use with subsequent enumeration calls.</span></span>

<span data-ttu-id="9251f-131">Si la fonction échoue ou qu’il n’existe aucun itinéraire avec les critères spécifiés, la valeur de retour est **null**.</span><span class="sxs-lookup"><span data-stu-id="9251f-131">If the function fails, or no routes exist with the specified criteria, the return value is **NULL**.</span></span> <span data-ttu-id="9251f-132">Appelez [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) pour obtenir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="9251f-132">Call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) to obtain more information.</span></span>



| <span data-ttu-id="9251f-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="9251f-133">Value</span></span>                                                                                                       | <span data-ttu-id="9251f-134">Description</span><span class="sxs-lookup"><span data-stu-id="9251f-134">Description</span></span>                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9251f-135"><dt>**ERREUR \_ aucun \_ itinéraire**</dt></span><span class="sxs-lookup"><span data-stu-id="9251f-135"><dt>**ERROR\_NO\_ROUTES**</dt></span></span> </dl>            | <span data-ttu-id="9251f-136">Aucun itinéraire n’a les critères spécifiés.</span><span class="sxs-lookup"><span data-stu-id="9251f-136">There are no routes that have the specified criteria.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="9251f-137"><dt>**paramètre d’erreur \_ non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9251f-137"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="9251f-138">Un ou plusieurs des paramètres d’entrée ne sont pas valides (par exemple, famille de protocole inconnue, indicateurs d’énumération non valides).</span><span class="sxs-lookup"><span data-stu-id="9251f-138">One or more of the input parameters is invalid (for example, unknown protocol family, invalid enumeration flags).</span></span><br/> |
| <dl> <span data-ttu-id="9251f-139"><dt>**ERREUR \_ aucune \_ \_ ressource système**</dt></span><span class="sxs-lookup"><span data-stu-id="9251f-139"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="9251f-140">Les ressources sont insuffisantes pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="9251f-140">There are insufficient resources to carry out the operation.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="9251f-141"><dt>**ERREUR \_ de \_ mémoire insuffisante \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9251f-141"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl>   | <span data-ttu-id="9251f-142">La mémoire est insuffisante pour allouer le descripteur.</span><span class="sxs-lookup"><span data-stu-id="9251f-142">There is insufficient memory to allocate the handle.</span></span><br/>                                                              |



 

## <a name="requirements"></a><span data-ttu-id="9251f-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9251f-143">Requirements</span></span>



| <span data-ttu-id="9251f-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9251f-144">Requirement</span></span> | <span data-ttu-id="9251f-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="9251f-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9251f-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9251f-146">Minimum supported client</span></span><br/> | <span data-ttu-id="9251f-147">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="9251f-147">None supported</span></span><br/>                                                          |
| <span data-ttu-id="9251f-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9251f-148">Minimum supported server</span></span><br/> | <span data-ttu-id="9251f-149">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9251f-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9251f-150">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="9251f-150">End of server support</span></span><br/>    | <span data-ttu-id="9251f-151">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9251f-151">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="9251f-152">En-tête</span><span class="sxs-lookup"><span data-stu-id="9251f-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="9251f-153"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="9251f-153"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="9251f-154">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9251f-154">Library</span></span><br/>                  | <dl> <span data-ttu-id="9251f-155"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9251f-155"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="9251f-156">DLL</span><span class="sxs-lookup"><span data-stu-id="9251f-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9251f-157"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9251f-157"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9251f-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9251f-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9251f-159">Référence de la version 1 du gestionnaire de tables de routage</span><span class="sxs-lookup"><span data-stu-id="9251f-159">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="9251f-160">Fonctions de la version 1 du gestionnaire de table de routage</span><span class="sxs-lookup"><span data-stu-id="9251f-160">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="9251f-161">**GetLastError**</span><span class="sxs-lookup"><span data-stu-id="9251f-161">**GetLastError**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[<span data-ttu-id="9251f-162">**\_itinéraire IP \_ RTM**</span><span class="sxs-lookup"><span data-stu-id="9251f-162">**RTM\_IP\_ROUTE**</span></span>](rtm-ip-route.md)
</dt> <dt>

[<span data-ttu-id="9251f-163">**\_itinéraire IPX \_ RTM**</span><span class="sxs-lookup"><span data-stu-id="9251f-163">**RTM\_IPX\_ROUTE**</span></span>](rtm-ipx-route.md)
</dt> <dt>

[<span data-ttu-id="9251f-164">**RtmCloseEnumerationHandle**</span><span class="sxs-lookup"><span data-stu-id="9251f-164">**RtmCloseEnumerationHandle**</span></span>](rtmcloseenumerationhandle.md)
</dt> <dt>

[<span data-ttu-id="9251f-165">**RtmEnumerateGetNextRoute**</span><span class="sxs-lookup"><span data-stu-id="9251f-165">**RtmEnumerateGetNextRoute**</span></span>](rtmenumerategetnextroute.md)
</dt> </dl>

 

