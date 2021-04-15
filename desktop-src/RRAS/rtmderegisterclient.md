---
title: Fonction RtmDeregisterClient (RTM. h)
description: La fonction RtmDeregisterClient annule l’inscription du client et libère les ressources associées au client.
ms.assetid: 5d04f276-86a7-4e63-8266-e93f0d6e5241
keywords:
- RtmDeregisterClient fonction RAS
topic_type:
- apiref
api_name:
- RtmDeregisterClient
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ab1f56d3d65e13c083d8952f500cfba4638ab83
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384636"
---
# <a name="rtmderegisterclient-function"></a><span data-ttu-id="fd6cb-104">RtmDeregisterClient fonction)</span><span class="sxs-lookup"><span data-stu-id="fd6cb-104">RtmDeregisterClient function</span></span>

<span data-ttu-id="fd6cb-105">\[Cette API a été remplacée par l’API du [Gestionnaire de table de routage version 2](about-routing-table-manager-version-2.md) et n’est pas disponible au-delà de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="fd6cb-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="fd6cb-106">Les applications doivent utiliser l’API du gestionnaire de table de routage version 2.\]</span><span class="sxs-lookup"><span data-stu-id="fd6cb-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="fd6cb-107">La fonction **RtmDeregisterClient** annule l’inscription du client et libère les ressources associées au client.</span><span class="sxs-lookup"><span data-stu-id="fd6cb-107">The **RtmDeregisterClient** function deregisters the client, and frees resources associated with the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd6cb-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fd6cb-108">Syntax</span></span>


```C++
DWORD RtmDeregisterClient(
  _In_ HANDLE ClientHandle
);
```



## <a name="parameters"></a><span data-ttu-id="fd6cb-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fd6cb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd6cb-110">*ClientHandle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fd6cb-110">*ClientHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd6cb-111">Handle qui identifie le client dont l’inscription doit être annulée.</span><span class="sxs-lookup"><span data-stu-id="fd6cb-111">Handle that identifies the client to deregister.</span></span> <span data-ttu-id="fd6cb-112">Obtenez ce handle en appelant [**RtmRegisterClient**](rtmregisterclient.md).</span><span class="sxs-lookup"><span data-stu-id="fd6cb-112">Obtain this handle by calling [**RtmRegisterClient**](rtmregisterclient.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd6cb-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fd6cb-113">Return value</span></span>

<span data-ttu-id="fd6cb-114">Si la fonction est réussie, la valeur de retour n’est pas une \_ erreur.</span><span class="sxs-lookup"><span data-stu-id="fd6cb-114">If the function succeeds, the return value is NO\_ERROR.</span></span>

<span data-ttu-id="fd6cb-115">Si la fonction échoue, la valeur de retour est l’un des codes d’erreur suivants.</span><span class="sxs-lookup"><span data-stu-id="fd6cb-115">If the function fails, the return value is one of the following error codes.</span></span>



| <span data-ttu-id="fd6cb-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd6cb-116">Value</span></span>                                                                                                       | <span data-ttu-id="fd6cb-117">Description</span><span class="sxs-lookup"><span data-stu-id="fd6cb-117">Description</span></span>                                                    |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="fd6cb-118"><dt>**HANDLE d’erreur \_ non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fd6cb-118"><dt>**ERROR\_INVALID\_HANDLE**</dt></span></span> </dl>       | <span data-ttu-id="fd6cb-119">Le paramètre *ClientHandle* n’est pas un handle valide.</span><span class="sxs-lookup"><span data-stu-id="fd6cb-119">The *ClientHandle* parameter is not a valid handle.</span></span><br/> |
| <dl> <span data-ttu-id="fd6cb-120"><dt>**ERREUR \_ aucune \_ \_ ressource système**</dt></span><span class="sxs-lookup"><span data-stu-id="fd6cb-120"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="fd6cb-121">Ressources insuffisantes pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="fd6cb-121">Insufficient resources to carry out the operation.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="fd6cb-122">Notes</span><span class="sxs-lookup"><span data-stu-id="fd6cb-122">Remarks</span></span>

<span data-ttu-id="fd6cb-123">Cette fonction supprime tous les itinéraires qui ont été ajoutés par le client.</span><span class="sxs-lookup"><span data-stu-id="fd6cb-123">This function removes all routes that were added by the client.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd6cb-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fd6cb-124">Requirements</span></span>



| <span data-ttu-id="fd6cb-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fd6cb-125">Requirement</span></span> | <span data-ttu-id="fd6cb-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd6cb-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fd6cb-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd6cb-127">Minimum supported client</span></span><br/> | <span data-ttu-id="fd6cb-128">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd6cb-128">None supported</span></span><br/>                                                          |
| <span data-ttu-id="fd6cb-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd6cb-129">Minimum supported server</span></span><br/> | <span data-ttu-id="fd6cb-130">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fd6cb-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="fd6cb-131">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="fd6cb-131">End of server support</span></span><br/>    | <span data-ttu-id="fd6cb-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fd6cb-132">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="fd6cb-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="fd6cb-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd6cb-134"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd6cb-134"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="fd6cb-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fd6cb-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="fd6cb-136"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fd6cb-136"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="fd6cb-137">DLL</span><span class="sxs-lookup"><span data-stu-id="fd6cb-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd6cb-138"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd6cb-138"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd6cb-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd6cb-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd6cb-140">Référence de la version 1 du gestionnaire de tables de routage</span><span class="sxs-lookup"><span data-stu-id="fd6cb-140">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="fd6cb-141">Fonctions de la version 1 du gestionnaire de table de routage</span><span class="sxs-lookup"><span data-stu-id="fd6cb-141">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="fd6cb-142">**RtmRegisterClient**</span><span class="sxs-lookup"><span data-stu-id="fd6cb-142">**RtmRegisterClient**</span></span>](rtmregisterclient.md)
</dt> </dl>

 

 





