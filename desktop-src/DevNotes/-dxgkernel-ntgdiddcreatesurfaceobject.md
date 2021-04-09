---
description: Crée un objet surface en mode noyau qui représente l’objet surface en mode utilisateur référencé par puSurfaceLocal.
ms.assetid: 1b2886a8-279b-4bec-9fb8-b88a68ded25b
title: NtGdiDdCreateSurfaceObject, fonction (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateSurfaceObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 5aef9a70897f5a8a46f9c966242d8842c54f9946
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033603"
---
# <a name="ntgdiddcreatesurfaceobject-function"></a><span data-ttu-id="930ca-103">NtGdiDdCreateSurfaceObject fonction)</span><span class="sxs-lookup"><span data-stu-id="930ca-103">NtGdiDdCreateSurfaceObject function</span></span>

<span data-ttu-id="930ca-104">\[Cette fonction est sujette à modification avec chaque révision du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="930ca-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="930ca-105">Utilisez plutôt Microsoft DirectDraw et Microsoft Direct3DAPIs ; Ces API isolent les applications de ces modifications du système d’exploitation et masquent de nombreuses autres difficultés liées à l’interaction directe avec les pilotes d’affichage.\]</span><span class="sxs-lookup"><span data-stu-id="930ca-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="930ca-106">Crée un objet surface en mode noyau qui représente l’objet surface en mode utilisateur référencé par *puSurfaceLocal*.</span><span class="sxs-lookup"><span data-stu-id="930ca-106">Creates a kernel-mode surface object that represents the user-mode surface object referenced by *puSurfaceLocal*.</span></span>

## <a name="syntax"></a><span data-ttu-id="930ca-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="930ca-107">Syntax</span></span>


```C++
HANDLE APIENTRY NtGdiDdCreateSurfaceObject(
  _In_ HANDLE             hDirectDrawLocal,
  _In_ HANDLE             hSurface,
  _In_ PDD_SURFACE_LOCAL  puSurfaceLocal,
  _In_ PDD_SURFACE_MORE   puSurfaceMore,
  _In_ PDD_SURFACE_GLOBAL puSurfaceGlobal,
  _In_ BOOL               bComplete
);
```



## <a name="parameters"></a><span data-ttu-id="930ca-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="930ca-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="930ca-109">*hDirectDrawLocal* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="930ca-109">*hDirectDrawLocal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="930ca-110">Handle vers l’objet DirectDraw en mode noyau.</span><span class="sxs-lookup"><span data-stu-id="930ca-110">Handle to the kernel-mode DirectDraw object.</span></span>

</dd> <dt>

<span data-ttu-id="930ca-111">*hSurface* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="930ca-111">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="930ca-112">Handle précédent à la même surface.</span><span class="sxs-lookup"><span data-stu-id="930ca-112">Previous handle to the same surface.</span></span> <span data-ttu-id="930ca-113">Utilisé si la surface est recréée après un basculement de mode.</span><span class="sxs-lookup"><span data-stu-id="930ca-113">Used if the surface is being re-created after a mode switch.</span></span>

</dd> <dt>

<span data-ttu-id="930ca-114">*puSurfaceLocal* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="930ca-114">*puSurfaceLocal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="930ca-115">Pointeur vers la structure de [**\_ surface \_ locale DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) qui représente l’objet de surface de mode utilisateur DirectDraw avec lequel associer la mémoire allouée.</span><span class="sxs-lookup"><span data-stu-id="930ca-115">Pointer to the [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that represents the DirectDraw user-mode surface object with which to associate the allocated memory.</span></span> <span data-ttu-id="930ca-116">Pour plus d’informations, consultez la documentation du DDK.</span><span class="sxs-lookup"><span data-stu-id="930ca-116">See the DDK documentation for details.</span></span>

</dd> <dt>

<span data-ttu-id="930ca-117">*puSurfaceMore* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="930ca-117">*puSurfaceMore* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="930ca-118">Pointeur vers la structure de [**\_ \_ plus de surface DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) qui contient des données locales supplémentaires pour chaque objet surface individuel.</span><span class="sxs-lookup"><span data-stu-id="930ca-118">Pointer to the [**DD\_SURFACE\_MORE**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) structure that contains additional local data for each individual surface object.</span></span> <span data-ttu-id="930ca-119">Pour plus d’informations, consultez la documentation du DDK.</span><span class="sxs-lookup"><span data-stu-id="930ca-119">See the DDK documentation for details.</span></span>

</dd> <dt>

<span data-ttu-id="930ca-120">*puSurfaceGlobal* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="930ca-120">*puSurfaceGlobal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="930ca-121">Pointeur vers la [**structure \_ \_ globale de la surface DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) qui contient les données de surface partagées globalement avec plusieurs surfaces.</span><span class="sxs-lookup"><span data-stu-id="930ca-121">Pointer to the [**DD\_SURFACE\_GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) structure that contains surface data shared globally with multiple surfaces.</span></span> <span data-ttu-id="930ca-122">Pour plus d’informations, consultez la documentation du DDK.</span><span class="sxs-lookup"><span data-stu-id="930ca-122">See the DDK documentation for details.</span></span>

</dd> <dt>

<span data-ttu-id="930ca-123">*bComplete* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="930ca-123">*bComplete* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="930ca-124">Indicateur de fin de l’objet en mode noyau.</span><span class="sxs-lookup"><span data-stu-id="930ca-124">Kernel-mode object completion flag.</span></span> <span data-ttu-id="930ca-125">Il peut s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="930ca-125">Can be one of the following values.</span></span>

<dt>



 <span data-ttu-id="930ca-126">:</span><span class="sxs-lookup"><span data-stu-id="930ca-126">(TRUE)</span></span>


</dt> <dd>

<span data-ttu-id="930ca-127">Terminez tout le traitement concernant la représentation en mode noyau.</span><span class="sxs-lookup"><span data-stu-id="930ca-127">Complete all processing concerning the kernel-mode representation.</span></span>

</dd> <dt>



 <span data-ttu-id="930ca-128">FAUSSES</span><span class="sxs-lookup"><span data-stu-id="930ca-128">(FALSE)</span></span>


</dt> <dd>

<span data-ttu-id="930ca-129">Créez l’objet, mais ne configurez pas de données internes telles que le pointeur de mémoire.</span><span class="sxs-lookup"><span data-stu-id="930ca-129">Create the object, but do not set up internal data such as the memory pointer.</span></span> <span data-ttu-id="930ca-130">Les objets créés à l’aide de la **valeur false** peuvent être joints à l’aide de [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md) et sont terminés par un appel à [**NtGdiDdCreateSurface**](-dxgkernel-ntgdiddcreatesurface.md).</span><span class="sxs-lookup"><span data-stu-id="930ca-130">Objects created using **FALSE** can be attached using [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md) and are completed by a call to [**NtGdiDdCreateSurface**](-dxgkernel-ntgdiddcreatesurface.md).</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="930ca-131">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="930ca-131">Return value</span></span>

<span data-ttu-id="930ca-132">En cas de réussite, cette fonction retourne un handle vers la représentation sous forme de surface en mode noyau. Sinon, elle retourne la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="930ca-132">If successful, this function returns a handle to the kernel-mode surface representation; otherwise it returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="930ca-133">Notes</span><span class="sxs-lookup"><span data-stu-id="930ca-133">Remarks</span></span>

<span data-ttu-id="930ca-134">Il est recommandé aux applications d’utiliser les API DirectDraw et [Direct3D](../direct3d10/d3d10-graphics-reference.md) pour créer et gérer des objets d’appareils graphiques.</span><span class="sxs-lookup"><span data-stu-id="930ca-134">Applications are advised to use the DirectDraw and [Direct3D](../direct3d10/d3d10-graphics-reference.md) APIs to create and manage graphics device objects.</span></span> <span data-ttu-id="930ca-135">Ces constructions résument le processus de création d’appareils de façon simplifiée et indépendante du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="930ca-135">These constructs abstract the device creation process in a simplified and operating-system-independent way.</span></span>

## <a name="requirements"></a><span data-ttu-id="930ca-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="930ca-136">Requirements</span></span>



| <span data-ttu-id="930ca-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="930ca-137">Requirement</span></span> | <span data-ttu-id="930ca-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="930ca-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="930ca-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="930ca-139">Minimum supported client</span></span><br/> | <span data-ttu-id="930ca-140">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="930ca-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="930ca-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="930ca-141">Minimum supported server</span></span><br/> | <span data-ttu-id="930ca-142">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="930ca-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="930ca-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="930ca-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="930ca-144"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="930ca-144"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="930ca-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="930ca-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="930ca-146">Prise en charge des clients de bas niveau</span><span class="sxs-lookup"><span data-stu-id="930ca-146">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="930ca-147">**DdCreateSurfaceObject**</span><span class="sxs-lookup"><span data-stu-id="930ca-147">**DdCreateSurfaceObject**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddcreatesurfaceobject)
</dt> <dt>

[<span data-ttu-id="930ca-148">**NtGdiDdDeleteSurfaceObject**</span><span class="sxs-lookup"><span data-stu-id="930ca-148">**NtGdiDdDeleteSurfaceObject**</span></span>](-dxgkernel-ntgdidddeletesurfaceobject.md)
</dt> <dt>

[<span data-ttu-id="930ca-149">**NtGdiDdAttachSurface**</span><span class="sxs-lookup"><span data-stu-id="930ca-149">**NtGdiDdAttachSurface**</span></span>](-dxgkernel-ntgdiddattachsurface.md)
</dt> <dt>

[<span data-ttu-id="930ca-150">**NtGdiDdCreateSurface**</span><span class="sxs-lookup"><span data-stu-id="930ca-150">**NtGdiDdCreateSurface**</span></span>](-dxgkernel-ntgdiddcreatesurface.md)
</dt> </dl>

 

 
