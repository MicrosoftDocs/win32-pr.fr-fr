---
title: Fonction RtmEnumerateGetNextRoute (RTM. h)
description: La fonction RtmEnumerateGetNextRoute retourne l’entrée Next-route dans l’énumération démarrée par un appel à RtmCreateEnumerationHandle.
ms.assetid: fff6fb58-8a37-49f0-abc5-354b5bc340f8
keywords:
- RtmEnumerateGetNextRoute fonction RAS
topic_type:
- apiref
api_name:
- RtmEnumerateGetNextRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e74cc5aa15c1014056075e876efca296556066d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106530809"
---
# <a name="rtmenumerategetnextroute-function"></a><span data-ttu-id="f2b1b-104">RtmEnumerateGetNextRoute fonction)</span><span class="sxs-lookup"><span data-stu-id="f2b1b-104">RtmEnumerateGetNextRoute function</span></span>

<span data-ttu-id="f2b1b-105">\[Cette API a été remplacée par l’API du [Gestionnaire de table de routage version 2](about-routing-table-manager-version-2.md) et n’est pas disponible au-delà de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f2b1b-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="f2b1b-106">Les applications doivent utiliser l’API du gestionnaire de table de routage version 2.\]</span><span class="sxs-lookup"><span data-stu-id="f2b1b-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="f2b1b-107">La fonction **RtmEnumerateGetNextRoute** retourne l’entrée Next-route dans l’énumération démarrée par un appel à [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).</span><span class="sxs-lookup"><span data-stu-id="f2b1b-107">The **RtmEnumerateGetNextRoute** function returns the next-route entry in the enumeration started by a call to [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f2b1b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f2b1b-108">Syntax</span></span>


```C++
DWORD RtmEnumerateGetNextRoute(
  _In_  HANDLE EnumerationHandle,
  _Out_ PVOID  Route
);
```



## <a name="parameters"></a><span data-ttu-id="f2b1b-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f2b1b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2b1b-110">*EnumerationHandle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f2b1b-110">*EnumerationHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2b1b-111">Handle qui identifie l’énumération et spécifie sa portée.</span><span class="sxs-lookup"><span data-stu-id="f2b1b-111">Handle that identifies the enumeration and specifies its scope.</span></span> <span data-ttu-id="f2b1b-112">Obtenez ce handle en appelant [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).</span><span class="sxs-lookup"><span data-stu-id="f2b1b-112">Obtain this handle by calling [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).</span></span>

</dd> <dt>

<span data-ttu-id="f2b1b-113">*Itinéraire* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f2b1b-113">*Route* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f2b1b-114">Pointeur vers une structure de route spécifique à la famille de protocoles ( [**\_ \_ itinéraire IP RTM**](rtm-ip-route.md) ou [**\_ \_ itinéraire IPX RTM**](rtm-ipx-route.md)).</span><span class="sxs-lookup"><span data-stu-id="f2b1b-114">Pointer to a protocol-family-specific route structure ( [**RTM\_IP\_ROUTE**](rtm-ip-route.md) or [**RTM\_IPX\_ROUTE**](rtm-ipx-route.md)).</span></span> <span data-ttu-id="f2b1b-115">Cette structure recevra l’itinéraire suivant dans l’énumération.</span><span class="sxs-lookup"><span data-stu-id="f2b1b-115">This structure will receive the next route in the enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2b1b-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f2b1b-116">Return value</span></span>

<span data-ttu-id="f2b1b-117">Si la fonction est réussie, la valeur de retour n’est pas une \_ erreur.</span><span class="sxs-lookup"><span data-stu-id="f2b1b-117">If the function succeeds, the return value is NO\_ERROR.</span></span>

<span data-ttu-id="f2b1b-118">Si la fonction échoue, la valeur de retour est l’un des codes d’erreur suivants.</span><span class="sxs-lookup"><span data-stu-id="f2b1b-118">If the function fails, the return value is one of the following error codes.</span></span>



| <span data-ttu-id="f2b1b-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="f2b1b-119">Value</span></span>                                                                                                       | <span data-ttu-id="f2b1b-120">Description</span><span class="sxs-lookup"><span data-stu-id="f2b1b-120">Description</span></span>                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f2b1b-121"><dt>**HANDLE d’erreur \_ non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f2b1b-121"><dt>**ERROR\_INVALID\_HANDLE**</dt></span></span> </dl>       | <span data-ttu-id="f2b1b-122">Le paramètre *EnumerationHandle* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="f2b1b-122">The *EnumerationHandle* parameter is not valid.</span></span><br/>              |
| <dl> <span data-ttu-id="f2b1b-123"><dt>**ERREUR \_ \_ plus aucun \_ itinéraire**</dt></span><span class="sxs-lookup"><span data-stu-id="f2b1b-123"><dt>**ERROR\_NO\_MORE\_ROUTES**</dt></span></span> </dl>      | <span data-ttu-id="f2b1b-124">Il n’y a plus d’itinéraires dans l’énumération.</span><span class="sxs-lookup"><span data-stu-id="f2b1b-124">There are no more routes in the enumeration.</span></span><br/>                 |
| <dl> <span data-ttu-id="f2b1b-125"><dt>**ERREUR \_ aucune \_ \_ ressource système**</dt></span><span class="sxs-lookup"><span data-stu-id="f2b1b-125"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="f2b1b-126">Les ressources sont insuffisantes pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="f2b1b-126">There are insufficient resources to carry out the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f2b1b-127">Notes</span><span class="sxs-lookup"><span data-stu-id="f2b1b-127">Remarks</span></span>

<span data-ttu-id="f2b1b-128">Bien que les itinéraires ne soient pas retournés dans un ordre particulier, chaque itinéraire de l’énumération n’est retourné qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="f2b1b-128">Although routes are not returned in any particular order, each route in the enumeration is returned only once.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2b1b-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f2b1b-129">Requirements</span></span>



| <span data-ttu-id="f2b1b-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f2b1b-130">Requirement</span></span> | <span data-ttu-id="f2b1b-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="f2b1b-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f2b1b-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2b1b-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f2b1b-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2b1b-133">None supported</span></span><br/>                                                          |
| <span data-ttu-id="f2b1b-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2b1b-134">Minimum supported server</span></span><br/> | <span data-ttu-id="f2b1b-135">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f2b1b-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f2b1b-136">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="f2b1b-136">End of server support</span></span><br/>    | <span data-ttu-id="f2b1b-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f2b1b-137">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="f2b1b-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="f2b1b-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2b1b-139"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2b1b-139"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="f2b1b-140">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f2b1b-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="f2b1b-141"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f2b1b-141"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="f2b1b-142">DLL</span><span class="sxs-lookup"><span data-stu-id="f2b1b-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2b1b-143"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2b1b-143"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2b1b-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2b1b-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2b1b-145">Référence de la version 1 du gestionnaire de tables de routage</span><span class="sxs-lookup"><span data-stu-id="f2b1b-145">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="f2b1b-146">Fonctions de la version 1 du gestionnaire de table de routage</span><span class="sxs-lookup"><span data-stu-id="f2b1b-146">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="f2b1b-147">**\_itinéraire IP \_ RTM**</span><span class="sxs-lookup"><span data-stu-id="f2b1b-147">**RTM\_IP\_ROUTE**</span></span>](rtm-ip-route.md)
</dt> <dt>

[<span data-ttu-id="f2b1b-148">**\_itinéraire IPX \_ RTM**</span><span class="sxs-lookup"><span data-stu-id="f2b1b-148">**RTM\_IPX\_ROUTE**</span></span>](rtm-ipx-route.md)
</dt> <dt>

[<span data-ttu-id="f2b1b-149">**RtmCloseEnumerationHandle**</span><span class="sxs-lookup"><span data-stu-id="f2b1b-149">**RtmCloseEnumerationHandle**</span></span>](rtmcloseenumerationhandle.md)
</dt> <dt>

[<span data-ttu-id="f2b1b-150">**RtmCreateEnumerationHandle**</span><span class="sxs-lookup"><span data-stu-id="f2b1b-150">**RtmCreateEnumerationHandle**</span></span>](rtmcreateenumerationhandle.md)
</dt> </dl>

 

 





