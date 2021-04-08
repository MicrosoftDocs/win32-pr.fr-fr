---
title: Fonction RtmGetNetworkCount (RTM. h)
description: La fonction RtmGetNetworkCount récupère le nombre de réseaux sur lesquels le gestionnaire de tables de routage a des itinéraires.
ms.assetid: d0c04b8d-a6c4-44bf-a3f2-de822d635131
keywords:
- RtmGetNetworkCount fonction RAS
topic_type:
- apiref
api_name:
- RtmGetNetworkCount
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eab4babd1e9d98071b2fbe6ab30c9b92d4a23f0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741412"
---
# <a name="rtmgetnetworkcount-function"></a><span data-ttu-id="4d03c-104">RtmGetNetworkCount fonction)</span><span class="sxs-lookup"><span data-stu-id="4d03c-104">RtmGetNetworkCount function</span></span>

<span data-ttu-id="4d03c-105">\[Cette API a été remplacée par l’API du [Gestionnaire de table de routage version 2](about-routing-table-manager-version-2.md) et n’est pas disponible au-delà de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="4d03c-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="4d03c-106">Les applications doivent utiliser l’API du gestionnaire de table de routage version 2.\]</span><span class="sxs-lookup"><span data-stu-id="4d03c-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="4d03c-107">La fonction **RtmGetNetworkCount** récupère le nombre de réseaux sur lesquels le gestionnaire de tables de routage a des itinéraires.</span><span class="sxs-lookup"><span data-stu-id="4d03c-107">The **RtmGetNetworkCount** function retrieves the number of networks to which the routing table manager has routes.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d03c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4d03c-108">Syntax</span></span>


```C++
ULONG RtmGetNetworkCount(
  _In_ DWORD ProtocolFamily
);
```



## <a name="parameters"></a><span data-ttu-id="4d03c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4d03c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d03c-110">*ProtocolFamily* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4d03c-110">*ProtocolFamily* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d03c-111">Spécifie le type de réseau pour obtenir des informations sur l’itinéraire, par exemple, IP ou IPX.</span><span class="sxs-lookup"><span data-stu-id="4d03c-111">Specifies for which type of network to obtain route information, for example, IP or IPX.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d03c-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4d03c-112">Return value</span></span>

<span data-ttu-id="4d03c-113">Si la fonction s’exécute correctement, la valeur de retour est le nombre de réseaux, le nombre de réseaux connus des protocoles de routage de la famille de protocoles spécifiée.</span><span class="sxs-lookup"><span data-stu-id="4d03c-113">If the function succeeds, the return value is the network count, the number of networks known to the routing protocols of the specified protocol family.</span></span>

<span data-ttu-id="4d03c-114">Si la valeur de retour est égale à zéro, aucun itinéraire n’est disponible ou l’opération a échoué.</span><span class="sxs-lookup"><span data-stu-id="4d03c-114">If the return value is zero, either no routes are available, or the operation failed.</span></span> <span data-ttu-id="4d03c-115">Appelez [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) pour obtenir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="4d03c-115">Call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) to obtain more information.</span></span>



| <span data-ttu-id="4d03c-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="4d03c-116">Value</span></span>                                                                                                    | <span data-ttu-id="4d03c-117">Description</span><span class="sxs-lookup"><span data-stu-id="4d03c-117">Description</span></span>                                                                                                  |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4d03c-118"><dt>**AUCUNE \_ erreur**</dt></span><span class="sxs-lookup"><span data-stu-id="4d03c-118"><dt>**NO\_ERROR**</dt></span></span> </dl>                 | <span data-ttu-id="4d03c-119">L’opération a réussi, mais aucun itinéraire n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="4d03c-119">The operation succeeded, but no routes are available.</span></span><br/>                                             |
| <dl> <span data-ttu-id="4d03c-120"><dt>**paramètre d’erreur \_ non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4d03c-120"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="4d03c-121">La valeur du paramètre *ProtocolFamily* ne correspond à aucune famille de protocoles installée.</span><span class="sxs-lookup"><span data-stu-id="4d03c-121">The value of the *ProtocolFamily* parameter does not correspond to any installed protocol family.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4d03c-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4d03c-122">Requirements</span></span>



| <span data-ttu-id="4d03c-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4d03c-123">Requirement</span></span> | <span data-ttu-id="4d03c-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="4d03c-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4d03c-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4d03c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4d03c-126">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="4d03c-126">None supported</span></span><br/>                                                          |
| <span data-ttu-id="4d03c-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4d03c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4d03c-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4d03c-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4d03c-129">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="4d03c-129">End of server support</span></span><br/>    | <span data-ttu-id="4d03c-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4d03c-130">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="4d03c-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="4d03c-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d03c-132"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d03c-132"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="4d03c-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4d03c-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="4d03c-134"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4d03c-134"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="4d03c-135">DLL</span><span class="sxs-lookup"><span data-stu-id="4d03c-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d03c-136"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d03c-136"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d03c-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4d03c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d03c-138">Référence de la version 1 du gestionnaire de tables de routage</span><span class="sxs-lookup"><span data-stu-id="4d03c-138">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="4d03c-139">Fonctions de la version 1 du gestionnaire de table de routage</span><span class="sxs-lookup"><span data-stu-id="4d03c-139">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="4d03c-140">**GetLastError**</span><span class="sxs-lookup"><span data-stu-id="4d03c-140">**GetLastError**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[<span data-ttu-id="4d03c-141">Identificateurs de famille de protocole RTMv1</span><span class="sxs-lookup"><span data-stu-id="4d03c-141">RTMv1 Protocol Family Identifiers</span></span>](routing-table-manager-version-1-protocol-family-identifiers.md)
</dt> </dl>

 

