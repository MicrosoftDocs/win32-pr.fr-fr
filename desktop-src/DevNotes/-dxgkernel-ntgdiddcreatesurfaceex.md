---
description: Crée une surface Microsoft Direct3D à partir d’une surface Microsoft DirectDraw et associe une valeur de handle demandée à celle-ci.
ms.assetid: 7b1ce714-a56e-4508-8160-af8c1748c5f7
title: NtGdiDdCreateSurfaceEx, fonction (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateSurfaceEx
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 8aad613762773e466fb83eadf689b7703a8c4198
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110127"
---
# <a name="ntgdiddcreatesurfaceex-function"></a><span data-ttu-id="7fab1-103">NtGdiDdCreateSurfaceEx fonction)</span><span class="sxs-lookup"><span data-stu-id="7fab1-103">NtGdiDdCreateSurfaceEx function</span></span>

<span data-ttu-id="7fab1-104">\[Cette fonction est sujette à modification avec chaque révision du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="7fab1-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="7fab1-105">Utilisez à la place DirectDraw et Direct3DAPIs. Ces API isolent les applications de ces modifications du système d’exploitation et masquent de nombreuses autres difficultés liées à l’interaction directe avec les pilotes d’affichage.\]</span><span class="sxs-lookup"><span data-stu-id="7fab1-105">Instead, use the DirectDraw and Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="7fab1-106">Crée une surface Microsoft Direct3D à partir d’une surface Microsoft DirectDraw et associe une valeur de handle demandée à celle-ci.</span><span class="sxs-lookup"><span data-stu-id="7fab1-106">Creates a Microsoft Direct3D surface from a Microsoft DirectDraw surface and associates a requested handle value to it.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fab1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7fab1-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdCreateSurfaceEx(
  _In_ HANDLE hDirectDraw,
  _In_ HANDLE hSurface,
  _In_ DWORD  dwSurfaceHandle
);
```



## <a name="parameters"></a><span data-ttu-id="7fab1-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7fab1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fab1-109">*hDirectDraw* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7fab1-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fab1-110">Handle vers l’objet DirectDraw créé par l’application.</span><span class="sxs-lookup"><span data-stu-id="7fab1-110">Handle to the DirectDraw object created by the application.</span></span>

</dd> <dt>

<span data-ttu-id="7fab1-111">*hSurface* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7fab1-111">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fab1-112">Handle vers la surface DirectDraw à créer pour Direct3D.</span><span class="sxs-lookup"><span data-stu-id="7fab1-112">Handle to the DirectDraw surface to be created for Direct3D.</span></span> <span data-ttu-id="7fab1-113">Ces descripteurs sont uniques au sein de chaque structure [**\_ \_ locale DD DIRECTDRAW**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_local) .</span><span class="sxs-lookup"><span data-stu-id="7fab1-113">These handles are unique within each different [**DD\_DIRECTDRAW\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_local) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7fab1-114">*dwSurfaceHandle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7fab1-114">*dwSurfaceHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fab1-115">Handle vers une [**structure \_ CREATESURFACEEXDATA DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfaceexdata) qui contient les informations requises pour que le pilote crée la surface.</span><span class="sxs-lookup"><span data-stu-id="7fab1-115">Handle to a [**DD\_CREATESURFACEEXDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfaceexdata) structure that contains the information required for the driver to create the surface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fab1-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7fab1-116">Return value</span></span>

<span data-ttu-id="7fab1-117">**NtGdiDdCreateSurfaceEx** retourne l’un des codes de rappel suivants.</span><span class="sxs-lookup"><span data-stu-id="7fab1-117">**NtGdiDdCreateSurfaceEx** returns one of the following callback codes.</span></span>



| <span data-ttu-id="7fab1-118">Code de retour</span><span class="sxs-lookup"><span data-stu-id="7fab1-118">Return code</span></span>                                                                                              | <span data-ttu-id="7fab1-119">Description</span><span class="sxs-lookup"><span data-stu-id="7fab1-119">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7fab1-120"><dt>**\_pilote DDHAL \_ géré**</dt></span><span class="sxs-lookup"><span data-stu-id="7fab1-120"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="7fab1-121">Le pilote a effectué l’opération et a retourné un code de retour valide pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="7fab1-121">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="7fab1-122">Si ce code est JJ \_ OK, DirectDraw ou Direct3D continue avec la fonction.</span><span class="sxs-lookup"><span data-stu-id="7fab1-122">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="7fab1-123">Dans le cas contraire, DirectDraw ou Direct3D retourne le code d’erreur fourni par le pilote et abandonne la fonction.</span><span class="sxs-lookup"><span data-stu-id="7fab1-123">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="7fab1-124"><dt>**DDHAL de \_ pilote \_ NOTHANDLED**</dt></span><span class="sxs-lookup"><span data-stu-id="7fab1-124"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="7fab1-125">Le pilote n’a pas de commentaire sur l’opération demandée.</span><span class="sxs-lookup"><span data-stu-id="7fab1-125">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="7fab1-126">Si le pilote doit avoir implémenté un rappel particulier, DirectDraw ou Direct3D signale une condition d’erreur.</span><span class="sxs-lookup"><span data-stu-id="7fab1-126">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="7fab1-127">Dans le cas contraire, DirectDraw ou Direct3D gère l’opération comme si le rappel de pilote n’avait pas été défini par l’exécution de l’implémentation de DirectDraw ou de l’implémentation indépendante du périphérique Direct3D.</span><span class="sxs-lookup"><span data-stu-id="7fab1-127">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7fab1-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7fab1-128">Requirements</span></span>



| <span data-ttu-id="7fab1-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7fab1-129">Requirement</span></span> | <span data-ttu-id="7fab1-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="7fab1-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7fab1-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7fab1-131">Minimum supported client</span></span><br/> | <span data-ttu-id="7fab1-132">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7fab1-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="7fab1-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7fab1-133">Minimum supported server</span></span><br/> | <span data-ttu-id="7fab1-134">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7fab1-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7fab1-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="7fab1-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="7fab1-136"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="7fab1-136"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fab1-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7fab1-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fab1-138">Prise en charge des clients de bas niveau</span><span class="sxs-lookup"><span data-stu-id="7fab1-138">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
