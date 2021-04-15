---
title: Fonction RtmIsRoute (RTM. h)
description: La fonction RtmIsRoute détermine s’il existe un ou plusieurs itinéraires vers un réseau de destination spécifié. Si c’est le cas, la fonction retourne des informations pour le meilleur itinéraire vers ce réseau.
ms.assetid: f9939790-d0a6-487e-9674-a01d436dc962
keywords:
- RtmIsRoute fonction RAS
topic_type:
- apiref
api_name:
- RtmIsRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e64621732f2f7a35223421e5f0fc86a309d332c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466311"
---
# <a name="rtmisroute-function"></a><span data-ttu-id="05b06-105">RtmIsRoute fonction)</span><span class="sxs-lookup"><span data-stu-id="05b06-105">RtmIsRoute function</span></span>

<span data-ttu-id="05b06-106">\[Cette API a été remplacée par l’API du [Gestionnaire de table de routage version 2](about-routing-table-manager-version-2.md) et n’est pas disponible au-delà de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="05b06-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="05b06-107">Les applications doivent utiliser l’API du gestionnaire de table de routage version 2.\]</span><span class="sxs-lookup"><span data-stu-id="05b06-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="05b06-108">La fonction **RtmIsRoute** détermine s’il existe un ou plusieurs itinéraires vers un réseau de destination spécifié.</span><span class="sxs-lookup"><span data-stu-id="05b06-108">The **RtmIsRoute** function determines if one or more routes to a specified destination network exist.</span></span> <span data-ttu-id="05b06-109">Si c’est le cas, la fonction retourne des informations pour le meilleur itinéraire vers ce réseau.</span><span class="sxs-lookup"><span data-stu-id="05b06-109">If so, the function returns information for the best route to that network.</span></span>

## <a name="syntax"></a><span data-ttu-id="05b06-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="05b06-110">Syntax</span></span>


```C++
BOOL RtmIsRoute(
  _In_  DWORD ProtocolFamily,
  _In_  PVOID Network,
  _Out_ PVOID BestRoute
);
```



## <a name="parameters"></a><span data-ttu-id="05b06-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="05b06-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05b06-112">*ProtocolFamily* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="05b06-112">*ProtocolFamily* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05b06-113">Spécifie le type de structure de données vers lequel pointe le paramètre *réseau* , par exemple, réseau [**IP \_**](ip-network.md), [**\_ réseau IPX**](ipx-network.md).</span><span class="sxs-lookup"><span data-stu-id="05b06-113">Specifies the type of data structure pointed to by the *Network* parameter, for example, [**IP\_NETWORK**](ip-network.md), [**IPX\_NETWORK**](ipx-network.md).</span></span>

</dd> <dt>

<span data-ttu-id="05b06-114">*Réseau* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="05b06-114">*Network* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05b06-115">Pointeur vers une structure qui spécifie les données de numéro de réseau spécifiques à la famille de protocoles.</span><span class="sxs-lookup"><span data-stu-id="05b06-115">Pointer to a structure that specifies protocol-family-specific network number data.</span></span> <span data-ttu-id="05b06-116">Ces données identifient le réseau pour lequel l’appelant recherche des informations de routage.</span><span class="sxs-lookup"><span data-stu-id="05b06-116">This data identifies the network for which the caller seeks route information.</span></span>

</dd> <dt>

<span data-ttu-id="05b06-117">*BestRoute* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="05b06-117">*BestRoute* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="05b06-118">Pointeur vers une structure spécifique à la famille de protocoles qui reçoit les meilleures informations d’itinéraire actuelles, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="05b06-118">Pointer to a protocol-family-specific structure that receives the current best route information, if any.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05b06-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="05b06-119">Return value</span></span>

<span data-ttu-id="05b06-120">La valeur de retour est l’un des codes suivants.</span><span class="sxs-lookup"><span data-stu-id="05b06-120">The return value is one of the following codes.</span></span>



| <span data-ttu-id="05b06-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="05b06-121">Value</span></span>                                                                                                       | <span data-ttu-id="05b06-122">Description</span><span class="sxs-lookup"><span data-stu-id="05b06-122">Description</span></span>                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="05b06-123"><dt>**:**</dt></span><span class="sxs-lookup"><span data-stu-id="05b06-123"><dt>**TRUE**</dt></span></span> </dl>                         | <span data-ttu-id="05b06-124">Au moins un itinéraire vers le réseau spécifié existe.</span><span class="sxs-lookup"><span data-stu-id="05b06-124">At least one route to the specified network exists.</span></span> <span data-ttu-id="05b06-125">Le meilleur itinéraire est retourné dans la structure vers laquelle pointe le paramètre *BestRoute* .</span><span class="sxs-lookup"><span data-stu-id="05b06-125">The best route is returned in the structure pointed to by the *BestRoute* parameter.</span></span><br/>      |
| <dl> <span data-ttu-id="05b06-126"><dt>**FAUSSES**</dt></span><span class="sxs-lookup"><span data-stu-id="05b06-126"><dt>**FALSE**</dt></span></span> </dl>                        | <span data-ttu-id="05b06-127">Il n’y a pas d’itinéraire vers le réseau spécifié, ou l’opération a échoué.</span><span class="sxs-lookup"><span data-stu-id="05b06-127">There is no route to the specified network, or the operation failed.</span></span> <span data-ttu-id="05b06-128">Appelez [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) pour obtenir plus d’informations :</span><span class="sxs-lookup"><span data-stu-id="05b06-128">Call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) to obtain more information:</span></span><br/> |
| <dl> <span data-ttu-id="05b06-129"><dt>**AUCUNE \_ erreur**</dt></span><span class="sxs-lookup"><span data-stu-id="05b06-129"><dt>**NO\_ERROR**</dt></span></span> </dl>                    | <span data-ttu-id="05b06-130">L’opération a réussi, mais il n’y a pas d’itinéraire vers le réseau spécifié.</span><span class="sxs-lookup"><span data-stu-id="05b06-130">The operation succeeded, but there is no route to the specified network.</span></span><br/>                                                                      |
| <dl> <span data-ttu-id="05b06-131"><dt>**paramètre d’erreur \_ non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="05b06-131"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="05b06-132">La valeur du paramètre *ProtocolFamily* ne correspond à aucune famille de protocoles installée.</span><span class="sxs-lookup"><span data-stu-id="05b06-132">The value of the *ProtocolFamily* parameter does not correspond to any installed protocol family.</span></span><br/>                                             |
| <dl> <span data-ttu-id="05b06-133"><dt>**ERREUR \_ aucune \_ \_ ressource système**</dt></span><span class="sxs-lookup"><span data-stu-id="05b06-133"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="05b06-134">Les ressources sont insuffisantes pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="05b06-134">There are insufficient resources to carry out the operation.</span></span><br/>                                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="05b06-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="05b06-135">Requirements</span></span>



| <span data-ttu-id="05b06-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="05b06-136">Requirement</span></span> | <span data-ttu-id="05b06-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="05b06-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="05b06-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05b06-138">Minimum supported client</span></span><br/> | <span data-ttu-id="05b06-139">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="05b06-139">None supported</span></span><br/>                                                          |
| <span data-ttu-id="05b06-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05b06-140">Minimum supported server</span></span><br/> | <span data-ttu-id="05b06-141">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="05b06-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="05b06-142">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="05b06-142">End of server support</span></span><br/>    | <span data-ttu-id="05b06-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="05b06-143">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="05b06-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="05b06-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="05b06-145"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="05b06-145"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="05b06-146">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="05b06-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="05b06-147"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="05b06-147"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="05b06-148">DLL</span><span class="sxs-lookup"><span data-stu-id="05b06-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05b06-149"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05b06-149"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05b06-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="05b06-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05b06-151">Référence de la version 1 du gestionnaire de tables de routage</span><span class="sxs-lookup"><span data-stu-id="05b06-151">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="05b06-152">Fonctions de la version 1 du gestionnaire de table de routage</span><span class="sxs-lookup"><span data-stu-id="05b06-152">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="05b06-153">**GetLastError**</span><span class="sxs-lookup"><span data-stu-id="05b06-153">**GetLastError**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[<span data-ttu-id="05b06-154">**\_réseau IP**</span><span class="sxs-lookup"><span data-stu-id="05b06-154">**IP\_NETWORK**</span></span>](ip-network.md)
</dt> <dt>

[<span data-ttu-id="05b06-155">**\_réseau IPX**</span><span class="sxs-lookup"><span data-stu-id="05b06-155">**IPX\_NETWORK**</span></span>](ipx-network.md)
</dt> <dt>

[<span data-ttu-id="05b06-156">Identificateurs de famille de protocole RTMv1</span><span class="sxs-lookup"><span data-stu-id="05b06-156">RTMv1 Protocol Family Identifiers</span></span>](routing-table-manager-version-1-protocol-family-identifiers.md)
</dt> </dl>

 

