---
description: Interroge l’État blit de la surface spécifiée.
ms.assetid: 0221bdc6-2146-4f4d-afb5-d1f701446d5e
title: NtGdiDdGetBltStatus, fonction (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetBltStatus
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 381de7f8c360f222a004786834fa36e92f1220d9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514530"
---
# <a name="ntgdiddgetbltstatus-function"></a><span data-ttu-id="e20ff-103">NtGdiDdGetBltStatus fonction)</span><span class="sxs-lookup"><span data-stu-id="e20ff-103">NtGdiDdGetBltStatus function</span></span>

<span data-ttu-id="e20ff-104">\[Cette fonction est sujette à modification avec chaque révision du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="e20ff-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="e20ff-105">Utilisez plutôt Microsoft DirectDraw et Microsoft Direct3DAPIs ; Ces API isolent les applications de ces modifications du système d’exploitation et masquent de nombreuses autres difficultés liées à l’interaction directe avec les pilotes d’affichage.\]</span><span class="sxs-lookup"><span data-stu-id="e20ff-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="e20ff-106">Interroge l’État blit de la surface spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e20ff-106">Queries the blit status of the specified surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="e20ff-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e20ff-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdGetBltStatus(
  _In_    HANDLE               hSurface,
  _Inout_ PDD_GETBLTSTATUSDATA puGetBltStatusData
);
```



## <a name="parameters"></a><span data-ttu-id="e20ff-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e20ff-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e20ff-109">*hSurface* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e20ff-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e20ff-110">Handle vers une [structure \_ \_ locale de surface DD](https://msdn.microsoft.com/library/ms793861.aspx) représentant la surface dont l’état de Blit est interrogé.</span><span class="sxs-lookup"><span data-stu-id="e20ff-110">Handle to a [DD\_SURFACE\_LOCAL](https://msdn.microsoft.com/library/ms793861.aspx) structure representing the surface whose blit status is being queried.</span></span>

</dd> <dt>

<span data-ttu-id="e20ff-111">*puGetBltStatusData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e20ff-111">*puGetBltStatusData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e20ff-112">Pointeur vers une [structure \_ GETBLTSTATUSDATA DD](https://msdn.microsoft.com/library/ms794243.aspx) qui contient les informations requises pour exécuter la requête d’État blit.</span><span class="sxs-lookup"><span data-stu-id="e20ff-112">Pointer to a [DD\_GETBLTSTATUSDATA](https://msdn.microsoft.com/library/ms794243.aspx) structure that contains the information required to perform the blit status query.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e20ff-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e20ff-113">Return value</span></span>

<span data-ttu-id="e20ff-114">**NtGdiDdGetBltStatus** retourne l’un des codes de rappel suivants.</span><span class="sxs-lookup"><span data-stu-id="e20ff-114">**NtGdiDdGetBltStatus** returns one of the following callback codes.</span></span>



| <span data-ttu-id="e20ff-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="e20ff-115">Return code</span></span>                                                                                              | <span data-ttu-id="e20ff-116">Description</span><span class="sxs-lookup"><span data-stu-id="e20ff-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e20ff-117"><dt>**\_pilote DDHAL \_ géré**</dt></span><span class="sxs-lookup"><span data-stu-id="e20ff-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="e20ff-118">Le pilote a effectué l’opération et a retourné un code de retour valide pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="e20ff-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="e20ff-119">Si ce code est JJ \_ OK, DirectDraw ou Direct3D continue avec la fonction.</span><span class="sxs-lookup"><span data-stu-id="e20ff-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="e20ff-120">Dans le cas contraire, DirectDraw ou Direct3D retourne le code d’erreur fourni par le pilote et abandonne la fonction.</span><span class="sxs-lookup"><span data-stu-id="e20ff-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="e20ff-121"><dt>**DDHAL de \_ pilote \_ NOTHANDLED**</dt></span><span class="sxs-lookup"><span data-stu-id="e20ff-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="e20ff-122">Le pilote n’a pas de commentaire sur l’opération demandée.</span><span class="sxs-lookup"><span data-stu-id="e20ff-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="e20ff-123">Si le pilote doit avoir implémenté un rappel particulier, DirectDraw ou Direct3D signale une condition d’erreur.</span><span class="sxs-lookup"><span data-stu-id="e20ff-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="e20ff-124">Dans le cas contraire, DirectDraw ou Direct3D gère l’opération comme si le rappel de pilote n’avait pas été défini par l’exécution de l’implémentation de DirectDraw ou de l’implémentation indépendante du périphérique Direct3D.</span><span class="sxs-lookup"><span data-stu-id="e20ff-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e20ff-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e20ff-125">Requirements</span></span>



| <span data-ttu-id="e20ff-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e20ff-126">Requirement</span></span> | <span data-ttu-id="e20ff-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="e20ff-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e20ff-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e20ff-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e20ff-129">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e20ff-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="e20ff-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e20ff-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e20ff-131">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e20ff-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e20ff-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="e20ff-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="e20ff-133"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e20ff-133"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e20ff-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e20ff-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e20ff-135">Prise en charge des clients de bas niveau</span><span class="sxs-lookup"><span data-stu-id="e20ff-135">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




