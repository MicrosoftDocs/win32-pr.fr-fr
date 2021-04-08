---
title: Fonction RtmCloseEnumerationHandle (RTM. h)
description: Le RtmCloseEnumerationHandle met fin à une énumération spécifiée et libère les ressources associées.
ms.assetid: 8daea42f-4304-4749-9894-d37f6ba733da
keywords:
- RtmCloseEnumerationHandle fonction RAS
topic_type:
- apiref
api_name:
- RtmCloseEnumerationHandle
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5adb47d40cb1300305c7ff6f9bb6f1c3c716f0f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033005"
---
# <a name="rtmcloseenumerationhandle-function"></a><span data-ttu-id="60d4b-104">RtmCloseEnumerationHandle fonction)</span><span class="sxs-lookup"><span data-stu-id="60d4b-104">RtmCloseEnumerationHandle function</span></span>

<span data-ttu-id="60d4b-105">\[Cette API a été remplacée par l’API du [Gestionnaire de table de routage version 2](about-routing-table-manager-version-2.md) et n’est pas disponible au-delà de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="60d4b-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="60d4b-106">Les applications doivent utiliser l’API du gestionnaire de table de routage version 2.\]</span><span class="sxs-lookup"><span data-stu-id="60d4b-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="60d4b-107">Le **RtmCloseEnumerationHandle** met fin à une énumération spécifiée et libère les ressources associées.</span><span class="sxs-lookup"><span data-stu-id="60d4b-107">The **RtmCloseEnumerationHandle** terminates a specified enumeration and frees the associated resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="60d4b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="60d4b-108">Syntax</span></span>


```C++
DWORD RtmCloseEnumerationHandle(
  _In_ HANDLE EnumerationHandle
);
```



## <a name="parameters"></a><span data-ttu-id="60d4b-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="60d4b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60d4b-110">*EnumerationHandle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="60d4b-110">*EnumerationHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60d4b-111">Handle de l’énumération à arrêter.</span><span class="sxs-lookup"><span data-stu-id="60d4b-111">Handle to the enumeration to terminate.</span></span> <span data-ttu-id="60d4b-112">Obtenez ce handle en appelant [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).</span><span class="sxs-lookup"><span data-stu-id="60d4b-112">Obtain this handle by calling [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60d4b-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="60d4b-113">Return value</span></span>

<span data-ttu-id="60d4b-114">Si la fonction est réussie, la valeur de retour n’est pas une \_ erreur.</span><span class="sxs-lookup"><span data-stu-id="60d4b-114">If the function succeeds, the return value is NO\_ERROR.</span></span>

<span data-ttu-id="60d4b-115">Si la fonction échoue, la valeur de retour est l’un des codes d’erreur suivants.</span><span class="sxs-lookup"><span data-stu-id="60d4b-115">If the function fails, the return value is one of the following error codes.</span></span>



| <span data-ttu-id="60d4b-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="60d4b-116">Value</span></span>                                                                                                       | <span data-ttu-id="60d4b-117">Description</span><span class="sxs-lookup"><span data-stu-id="60d4b-117">Description</span></span>                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="60d4b-118"><dt>**HANDLE d’erreur \_ non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="60d4b-118"><dt>**ERROR\_INVALID\_HANDLE**</dt></span></span> </dl>       | <span data-ttu-id="60d4b-119">Ce paramètre n'est pas valide.</span><span class="sxs-lookup"><span data-stu-id="60d4b-119">The parameter is not valid.</span></span><br/>                                  |
| <dl> <span data-ttu-id="60d4b-120"><dt>**ERREUR \_ aucune \_ \_ ressource système**</dt></span><span class="sxs-lookup"><span data-stu-id="60d4b-120"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="60d4b-121">Les ressources sont insuffisantes pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="60d4b-121">There are insufficient resources to carry out the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="60d4b-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="60d4b-122">Requirements</span></span>



| <span data-ttu-id="60d4b-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="60d4b-123">Requirement</span></span> | <span data-ttu-id="60d4b-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="60d4b-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="60d4b-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="60d4b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="60d4b-126">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="60d4b-126">None supported</span></span><br/>                                                          |
| <span data-ttu-id="60d4b-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="60d4b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="60d4b-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="60d4b-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="60d4b-129">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="60d4b-129">End of server support</span></span><br/>    | <span data-ttu-id="60d4b-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="60d4b-130">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="60d4b-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="60d4b-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="60d4b-132"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="60d4b-132"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="60d4b-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="60d4b-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="60d4b-134"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="60d4b-134"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="60d4b-135">DLL</span><span class="sxs-lookup"><span data-stu-id="60d4b-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60d4b-136"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60d4b-136"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60d4b-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60d4b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60d4b-138">Référence de la version 1 du gestionnaire de tables de routage</span><span class="sxs-lookup"><span data-stu-id="60d4b-138">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="60d4b-139">Fonctions de la version 1 du gestionnaire de table de routage</span><span class="sxs-lookup"><span data-stu-id="60d4b-139">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="60d4b-140">**RtmCreateEnumerationHandle**</span><span class="sxs-lookup"><span data-stu-id="60d4b-140">**RtmCreateEnumerationHandle**</span></span>](rtmcreateenumerationhandle.md)
</dt> <dt>

[<span data-ttu-id="60d4b-141">**RtmEnumerateGetNextRoute**</span><span class="sxs-lookup"><span data-stu-id="60d4b-141">**RtmEnumerateGetNextRoute**</span></span>](rtmenumerategetnextroute.md)
</dt> </dl>

 

 





