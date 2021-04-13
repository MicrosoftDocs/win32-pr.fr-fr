---
title: Fonction RtmBlockDeleteRoutes (RTM. h)
description: La fonction RtmBlockDeleteRoutes supprime tous les itinéraires dans le sous-ensemble spécifié d’itinéraires dans la table.
ms.assetid: d191883d-da3d-4a91-92e6-4979db96f4a4
keywords:
- RtmBlockDeleteRoutes fonction RAS
topic_type:
- apiref
api_name:
- RtmBlockDeleteRoutes
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a71090371fe8a84698b84b84391e5a782fdc636f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465838"
---
# <a name="rtmblockdeleteroutes-function"></a><span data-ttu-id="20206-104">RtmBlockDeleteRoutes fonction)</span><span class="sxs-lookup"><span data-stu-id="20206-104">RtmBlockDeleteRoutes function</span></span>

<span data-ttu-id="20206-105">\[Cette API a été remplacée par l’API du [Gestionnaire de table de routage version 2](about-routing-table-manager-version-2.md) et n’est pas disponible au-delà de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="20206-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="20206-106">Les applications doivent utiliser l’API du gestionnaire de table de routage version 2.\]</span><span class="sxs-lookup"><span data-stu-id="20206-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="20206-107">La fonction **RtmBlockDeleteRoutes** supprime tous les itinéraires dans le sous-ensemble spécifié d’itinéraires dans la table.</span><span class="sxs-lookup"><span data-stu-id="20206-107">The **RtmBlockDeleteRoutes** function deletes all routes in the specified subset of routes in the table.</span></span>

## <a name="syntax"></a><span data-ttu-id="20206-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="20206-108">Syntax</span></span>


```C++
HANDLE RtmBlockDeleteRoutes(
  _In_ HANDLE ClientHandle,
  _In_ DWORD  EnumerationFlags,
  _In_ PVOID  CriteriaRoute
);
```



## <a name="parameters"></a><span data-ttu-id="20206-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="20206-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20206-110">*ClientHandle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="20206-110">*ClientHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20206-111">Handle qui identifie le client et, par conséquent, le protocole de routage des itinéraires à supprimer.</span><span class="sxs-lookup"><span data-stu-id="20206-111">Handle that identifies the client, and therefore the routing protocol, of the routes to be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="20206-112">*EnumerationFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="20206-112">*EnumerationFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20206-113">Spécifie les itinéraires qui doivent être énumérés.</span><span class="sxs-lookup"><span data-stu-id="20206-113">Specifies which routes should be enumerated.</span></span> <span data-ttu-id="20206-114">Ce paramètre limite l’ensemble des itinéraires supprimés à un sous-ensemble défini par les indicateurs suivants et les valeurs des membres correspondants de la structure vers laquelle pointe le paramètre *CriteriaRoute* .</span><span class="sxs-lookup"><span data-stu-id="20206-114">This parameter limits the set of deleted routes to a subset defined by the following flags and the values in the corresponding members of the structure pointed to by the *CriteriaRoute* parameter.</span></span> <span data-ttu-id="20206-115">Les indicateurs sont les mêmes que ceux utilisés dans [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md) , à ceci près que la version RTM \_ \_ \_ des meilleurs itinéraires est redondante pour **RtmBlockDeleteRoutes**.</span><span class="sxs-lookup"><span data-stu-id="20206-115">The flags are the same as those used in [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md) except that RTM\_ONLY\_BEST\_ROUTES is redundant for **RtmBlockDeleteRoutes**.</span></span> <span data-ttu-id="20206-116">La meilleure désignation de route est ajustée en fonction de la suppression des itinéraires. par conséquent, la fonction supprime tous les itinéraires dans le sous-ensemble.</span><span class="sxs-lookup"><span data-stu-id="20206-116">The best-route designation is adjusted as routes are deleted, so the function eventually deletes all the routes in the subset.</span></span>

</dd> <dt>

<span data-ttu-id="20206-117">*CriteriaRoute* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="20206-117">*CriteriaRoute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20206-118">Pointeur vers une structure de route spécifique à la famille de protocoles ( [**\_ \_ itinéraire IP RTM**](rtm-ip-route.md) ou [**\_ \_ itinéraire IPX RTM**](rtm-ipx-route.md)).</span><span class="sxs-lookup"><span data-stu-id="20206-118">Pointer to a protocol-family-specific route structure ( [**RTM\_IP\_ROUTE**](rtm-ip-route.md) or [**RTM\_IPX\_ROUTE**](rtm-ipx-route.md)).</span></span> <span data-ttu-id="20206-119">Les valeurs de membre de cette structure correspondent aux indicateurs spécifiés par le paramètre *EnumerationFlags* .</span><span class="sxs-lookup"><span data-stu-id="20206-119">The member values in this structure correspond to the flags specified by the *EnumerationFlags* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20206-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="20206-120">Return value</span></span>

<span data-ttu-id="20206-121">Si la fonction est réussie, la valeur de retour n’est pas une \_ erreur.</span><span class="sxs-lookup"><span data-stu-id="20206-121">If the function succeeds, the return value is NO\_ERROR.</span></span>

<span data-ttu-id="20206-122">Si la fonction échoue, la valeur de retour est l’un des codes d’erreur suivants.</span><span class="sxs-lookup"><span data-stu-id="20206-122">If the function fails, the return value is one of the following error codes.</span></span>



| <span data-ttu-id="20206-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="20206-123">Value</span></span>                                                                                                       | <span data-ttu-id="20206-124">Description</span><span class="sxs-lookup"><span data-stu-id="20206-124">Description</span></span>                                                                                                |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="20206-125"><dt>**ERREUR \_ aucun \_ itinéraire**</dt></span><span class="sxs-lookup"><span data-stu-id="20206-125"><dt>**ERROR\_NO\_ROUTES**</dt></span></span> </dl>            | <span data-ttu-id="20206-126">Aucun itinéraire n’a les critères spécifiés.</span><span class="sxs-lookup"><span data-stu-id="20206-126">There are no routes that have the specified criteria.</span></span><br/>                                           |
| <dl> <span data-ttu-id="20206-127"><dt>**HANDLE d’erreur \_ non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="20206-127"><dt>**ERROR\_INVALID\_HANDLE**</dt></span></span> </dl>       | <span data-ttu-id="20206-128">Le paramètre *ClientHandle* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="20206-128">The *ClientHandle* parameter is not valid.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="20206-129"><dt>**paramètre d’erreur \_ non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="20206-129"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="20206-130">Un ou plusieurs des paramètres d’entrée ne sont pas valides, par exemple, les indicateurs d’énumération ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="20206-130">One or more of the input parameters is invalid, for example, the enumeration flags are invalid.</span></span><br/> |
| <dl> <span data-ttu-id="20206-131"><dt>**ERREUR \_ aucune \_ \_ ressource système**</dt></span><span class="sxs-lookup"><span data-stu-id="20206-131"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="20206-132">Les ressources sont insuffisantes pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="20206-132">There are insufficient resources to carry out the operation.</span></span><br/>                                    |
| <dl> <span data-ttu-id="20206-133"><dt>**ERREUR \_ de \_ mémoire insuffisante \_**</dt></span><span class="sxs-lookup"><span data-stu-id="20206-133"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl>   | <span data-ttu-id="20206-134">La mémoire est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="20206-134">There is insufficient memory to carry out the operation.</span></span><br/>                                        |



 

## <a name="remarks"></a><span data-ttu-id="20206-135">Notes</span><span class="sxs-lookup"><span data-stu-id="20206-135">Remarks</span></span>

<span data-ttu-id="20206-136">La fonction génère des messages de notification appropriés à tous les clients inscrits, y compris l’appelant.</span><span class="sxs-lookup"><span data-stu-id="20206-136">The function generates appropriate notification messages to all registered clients including the caller.</span></span>

## <a name="requirements"></a><span data-ttu-id="20206-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="20206-137">Requirements</span></span>



| <span data-ttu-id="20206-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="20206-138">Requirement</span></span> | <span data-ttu-id="20206-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="20206-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="20206-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="20206-140">Minimum supported client</span></span><br/> | <span data-ttu-id="20206-141">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="20206-141">None supported</span></span><br/>                                                          |
| <span data-ttu-id="20206-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="20206-142">Minimum supported server</span></span><br/> | <span data-ttu-id="20206-143">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="20206-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="20206-144">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="20206-144">End of server support</span></span><br/>    | <span data-ttu-id="20206-145">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="20206-145">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="20206-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="20206-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="20206-147"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="20206-147"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="20206-148">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="20206-148">Library</span></span><br/>                  | <dl> <span data-ttu-id="20206-149"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="20206-149"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="20206-150">DLL</span><span class="sxs-lookup"><span data-stu-id="20206-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20206-151"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20206-151"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20206-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20206-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20206-153">Référence de la version 1 du gestionnaire de tables de routage</span><span class="sxs-lookup"><span data-stu-id="20206-153">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="20206-154">Fonctions de la version 1 du gestionnaire de table de routage</span><span class="sxs-lookup"><span data-stu-id="20206-154">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="20206-155">**RtmCreateEnumerationHandle**</span><span class="sxs-lookup"><span data-stu-id="20206-155">**RtmCreateEnumerationHandle**</span></span>](rtmcreateenumerationhandle.md)
</dt> <dt>

[<span data-ttu-id="20206-156">**RtmRegisterClient**</span><span class="sxs-lookup"><span data-stu-id="20206-156">**RtmRegisterClient**</span></span>](rtmregisterclient.md)
</dt> </dl>

 

 





