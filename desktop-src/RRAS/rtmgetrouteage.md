---
title: Fonction RtmGetRouteAge (RTM. h)
description: La fonction RtmGetRouteAge retourne l’âge d’un itinéraire. L’âge est le temps, en secondes, depuis sa création ou sa dernière mise à jour.
ms.assetid: 93052412-227f-4c9e-978b-3ec4bde4a256
keywords:
- RtmGetRouteAge fonction RAS
topic_type:
- apiref
api_name:
- RtmGetRouteAge
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a484bb5684fde974ce5fa704c0d0cca38c320851
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742181"
---
# <a name="rtmgetrouteage-function"></a><span data-ttu-id="40783-105">RtmGetRouteAge fonction)</span><span class="sxs-lookup"><span data-stu-id="40783-105">RtmGetRouteAge function</span></span>

<span data-ttu-id="40783-106">\[Cette API a été remplacée par l’API du [Gestionnaire de table de routage version 2](about-routing-table-manager-version-2.md) et n’est pas disponible au-delà de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="40783-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="40783-107">Les applications doivent utiliser l’API du gestionnaire de table de routage version 2.\]</span><span class="sxs-lookup"><span data-stu-id="40783-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="40783-108">La fonction **RtmGetRouteAge** retourne l’âge d’un itinéraire.</span><span class="sxs-lookup"><span data-stu-id="40783-108">The **RtmGetRouteAge** function returns the age of a route.</span></span> <span data-ttu-id="40783-109">L’âge est le temps, en secondes, depuis sa création ou sa dernière mise à jour.</span><span class="sxs-lookup"><span data-stu-id="40783-109">The age is the time, in seconds, since it was created or last updated.</span></span>

## <a name="syntax"></a><span data-ttu-id="40783-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="40783-110">Syntax</span></span>


```C++
ULONG RtmGetRouteAge(
  _In_ PVOID Route
);
```



## <a name="parameters"></a><span data-ttu-id="40783-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="40783-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40783-112">*Itinéraire* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="40783-112">*Route* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40783-113">Pointeur vers une structure spécifique à la famille de protocoles qui spécifie les données de routage récemment obtenues à partir du gestionnaire de tables de routage.</span><span class="sxs-lookup"><span data-stu-id="40783-113">Pointer to a protocol-family-specific structure that specifies route data recently obtained from the routing table manager.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40783-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="40783-114">Return value</span></span>

<span data-ttu-id="40783-115">La valeur de retour est l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="40783-115">The return value is one of the following values.</span></span>



| <span data-ttu-id="40783-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="40783-116">Value</span></span>                                                                                   | <span data-ttu-id="40783-117">Description</span><span class="sxs-lookup"><span data-stu-id="40783-117">Description</span></span>                                                                                                                                                  |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="40783-118"><dt>**Routage**</dt></span><span class="sxs-lookup"><span data-stu-id="40783-118"><dt>**RouteAge**</dt></span></span> </dl> | <span data-ttu-id="40783-119">Durée en secondes depuis la création ou la dernière mise à jour d’un itinéraire.</span><span class="sxs-lookup"><span data-stu-id="40783-119">The time in seconds since a route was created or last updated.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="40783-120"><dt>**LIMITES**</dt></span><span class="sxs-lookup"><span data-stu-id="40783-120"><dt>**INFINITE**</dt></span></span> </dl> | <span data-ttu-id="40783-121">Le contenu de la structure de routage n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="40783-121">The content of the route structure is invalid.</span></span> <span data-ttu-id="40783-122">Dans ce cas, un appel à [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne un \_ paramètre d’erreur non valide \_ .</span><span class="sxs-lookup"><span data-stu-id="40783-122">In this case, a call to [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INVALID\_PARAMETER.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="40783-123">Notes</span><span class="sxs-lookup"><span data-stu-id="40783-123">Remarks</span></span>

<span data-ttu-id="40783-124">L’âge de l’itinéraire est calculé à partir du \_ membre d’horodatage de RR de la structure vers laquelle pointe le paramètre d' *itinéraire* .</span><span class="sxs-lookup"><span data-stu-id="40783-124">The route age is computed from the RR\_TimeStamp member of the structure that is pointed to by the *Route* parameter.</span></span> <span data-ttu-id="40783-125">Le gestionnaire de tables de routage définit la valeur de ce membre lorsqu’un itinéraire est ajouté ou mis à jour.</span><span class="sxs-lookup"><span data-stu-id="40783-125">The routing table manager sets the value of this member when a route is added or updated.</span></span>

## <a name="requirements"></a><span data-ttu-id="40783-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="40783-126">Requirements</span></span>



| <span data-ttu-id="40783-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="40783-127">Requirement</span></span> | <span data-ttu-id="40783-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="40783-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="40783-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="40783-129">Minimum supported client</span></span><br/> | <span data-ttu-id="40783-130">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="40783-130">None supported</span></span><br/>                                                          |
| <span data-ttu-id="40783-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="40783-131">Minimum supported server</span></span><br/> | <span data-ttu-id="40783-132">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="40783-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="40783-133">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="40783-133">End of server support</span></span><br/>    | <span data-ttu-id="40783-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="40783-134">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="40783-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="40783-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="40783-136"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="40783-136"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="40783-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="40783-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="40783-138"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="40783-138"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="40783-139">DLL</span><span class="sxs-lookup"><span data-stu-id="40783-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40783-140"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40783-140"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40783-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="40783-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40783-142">Référence de la version 1 du gestionnaire de tables de routage \_</span><span class="sxs-lookup"><span data-stu-id="40783-142">Routing Table Manager Version\_1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="40783-143">Fonctions de la version 1 du gestionnaire de table de routage</span><span class="sxs-lookup"><span data-stu-id="40783-143">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="40783-144">**GetLastError**</span><span class="sxs-lookup"><span data-stu-id="40783-144">**GetLastError**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[<span data-ttu-id="40783-145">**\_itinéraire IP \_ RTM**</span><span class="sxs-lookup"><span data-stu-id="40783-145">**RTM\_IP\_ROUTE**</span></span>](rtm-ip-route.md)
</dt> <dt>

[<span data-ttu-id="40783-146">**\_itinéraire IPX \_ RTM**</span><span class="sxs-lookup"><span data-stu-id="40783-146">**RTM\_IPX\_ROUTE**</span></span>](rtm-ipx-route.md)
</dt> </dl>

 

