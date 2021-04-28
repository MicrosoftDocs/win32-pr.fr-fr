---
description: NtGdiDdCreateSurface fonction-attache une surface à une autre surface.
ms.assetid: 4fd757c7-9e32-4737-b666-3226f6cf29fa
title: NtGdiDdCreateSurface, fonction (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateSurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: bf8e13cff80ddea4e102c045c174565e7e835274
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085777"
---
# <a name="ntgdiddcreatesurface-function"></a><span data-ttu-id="0e943-103">NtGdiDdCreateSurface fonction)</span><span class="sxs-lookup"><span data-stu-id="0e943-103">NtGdiDdCreateSurface function</span></span>

<span data-ttu-id="0e943-104">\[Cette fonction est sujette à modification avec chaque révision du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="0e943-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="0e943-105">Utilisez plutôt Microsoft DirectDraw et Microsoft Direct3DAPIs ; Ces API isolent les applications de ces modifications du système d’exploitation et masquent de nombreuses autres difficultés liées à l’interaction directe avec les pilotes d’affichage.\]</span><span class="sxs-lookup"><span data-stu-id="0e943-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="0e943-106">Attache une surface à une autre surface.</span><span class="sxs-lookup"><span data-stu-id="0e943-106">Attaches a surface to another surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e943-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0e943-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdCreateSurface(
  _In_    HANDLE               hDirectDraw,
  _In_    HANDLE               *hSurface,
  _Inout_ DDSURFACEDESC        *puSurfaceDescription,
  _Inout_ DD_SURFACE_GLOBAL    *puSurfaceGlobalData,
  _Inout_ DD_SURFACE_LOCAL     *puSurfaceLocalData,
  _Inout_ DD_SURFACE_MORE      *puSurfaceMoreData,
  _Inout_ DD_CREATESURFACEDATA *puCreateSurfaceData,
  _Out_   HANDLE               *puhSurface
);
```



## <a name="parameters"></a><span data-ttu-id="0e943-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0e943-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e943-109">*hDirectDraw* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0e943-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e943-110">Handle vers la [**structure \_ \_ globale d’JJ DIRECTDRAW**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) représentant le pilote.</span><span class="sxs-lookup"><span data-stu-id="0e943-110">Handle to the [**DD\_DIRECTDRAW\_GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) structure representing the driver.</span></span>

</dd> <dt>

<span data-ttu-id="0e943-111">*hSurface* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0e943-111">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e943-112">Handle précédent à la même surface.</span><span class="sxs-lookup"><span data-stu-id="0e943-112">Previous handle to the same surface.</span></span> <span data-ttu-id="0e943-113">Utilisé si la surface est recréée après un basculement de mode.</span><span class="sxs-lookup"><span data-stu-id="0e943-113">Used if the surface is being re-created after a mode switch.</span></span>

</dd> <dt>

<span data-ttu-id="0e943-114">*puSurfaceDescription* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="0e943-114">*puSurfaceDescription* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0e943-115">Pointeur vers la structure [**DDSURFACEDESC**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) décrivant la surface ou la mémoire tampon que le pilote doit créer.</span><span class="sxs-lookup"><span data-stu-id="0e943-115">Pointer to the [**DDSURFACEDESC**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) structure describing the surface or buffer that the driver should create.</span></span>

</dd> <dt>

<span data-ttu-id="0e943-116">*puSurfaceGlobalData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="0e943-116">*puSurfaceGlobalData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0e943-117">Pointeur vers la [**structure \_ \_ globale de la surface DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) qui contient des données de surface partagées globalement avec plusieurs surfaces.</span><span class="sxs-lookup"><span data-stu-id="0e943-117">Pointer to the [**DD\_SURFACE\_GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) structure containing surface data that is shared globally with multiple surfaces.</span></span>

</dd> <dt>

<span data-ttu-id="0e943-118">*puSurfaceLocalData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="0e943-118">*puSurfaceLocalData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0e943-119">Pointeur désignant une liste de structures [**\_ \_ locales de surface DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) décrivant les objets surface créés par le pilote.</span><span class="sxs-lookup"><span data-stu-id="0e943-119">Pointer to a list of [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structures describing the surface objects created by the driver.</span></span>

</dd> <dt>

<span data-ttu-id="0e943-120">*puSurfaceMoreData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="0e943-120">*puSurfaceMoreData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0e943-121">Pointeur vers une structure de [**\_ \_ plus grande surface DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) qui contient des données de surface locales supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="0e943-121">Pointer to a [**DD\_SURFACE\_MORE**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) structure that contains additional local surface data.</span></span>

</dd> <dt>

<span data-ttu-id="0e943-122">*puCreateSurfaceData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="0e943-122">*puCreateSurfaceData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0e943-123">Pointeur vers une [**structure \_ CREATESURFACEDATA DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfacedata) qui contient les informations requises pour créer une surface.</span><span class="sxs-lookup"><span data-stu-id="0e943-123">Pointer to a [**DD\_CREATESURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfacedata) structure that contains the information required to create a surface.</span></span>

</dd> <dt>

<span data-ttu-id="0e943-124">*puhSurface* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0e943-124">*puhSurface* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0e943-125">Est utilisé par l’API DirectDraw et ne doit pas être renseigné par le pilote.</span><span class="sxs-lookup"><span data-stu-id="0e943-125">Is used by the DirectDraw  API and should not be filled in by the driver.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e943-126">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0e943-126">Return value</span></span>

<span data-ttu-id="0e943-127">**NtGdiDdCreateSurface** retourne l’un des codes de rappel suivants.</span><span class="sxs-lookup"><span data-stu-id="0e943-127">**NtGdiDdCreateSurface** returns one of the following callback codes.</span></span>



| <span data-ttu-id="0e943-128">Code de retour</span><span class="sxs-lookup"><span data-stu-id="0e943-128">Return code</span></span>                                                                                              | <span data-ttu-id="0e943-129">Description</span><span class="sxs-lookup"><span data-stu-id="0e943-129">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0e943-130"><dt>**\_pilote DDHAL \_ géré**</dt></span><span class="sxs-lookup"><span data-stu-id="0e943-130"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="0e943-131">Le pilote a effectué l’opération et a retourné un code de retour valide pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="0e943-131">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="0e943-132">Si ce code est JJ \_ OK, DirectDraw ou Direct3D continue avec la fonction.</span><span class="sxs-lookup"><span data-stu-id="0e943-132">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="0e943-133">Dans le cas contraire, DirectDraw ou Direct3D retourne le code d’erreur fourni par le pilote et abandonne la fonction.</span><span class="sxs-lookup"><span data-stu-id="0e943-133">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="0e943-134"><dt>**DDHAL de \_ pilote \_ NOTHANDLED**</dt></span><span class="sxs-lookup"><span data-stu-id="0e943-134"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="0e943-135">Le pilote n’a pas de commentaire sur l’opération demandée.</span><span class="sxs-lookup"><span data-stu-id="0e943-135">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="0e943-136">Si le pilote doit avoir implémenté un rappel particulier, DirectDraw ou Direct3D signale une condition d’erreur.</span><span class="sxs-lookup"><span data-stu-id="0e943-136">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="0e943-137">Dans le cas contraire, DirectDraw ou Direct3D gère l’opération comme si le rappel de pilote n’avait pas été défini par l’exécution de l’implémentation de DirectDraw ou de l’implémentation indépendante du périphérique Direct3D.</span><span class="sxs-lookup"><span data-stu-id="0e943-137">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0e943-138">Notes </span><span class="sxs-lookup"><span data-stu-id="0e943-138">Remarks</span></span>

<span data-ttu-id="0e943-139">Il est recommandé que votre application appelle [IDirectDraw7 :: CreateSurface](/windows/win32/api/ddraw/nf-ddraw-idirectdraw7-createsurface) au lieu d’utiliser cette fonction.</span><span class="sxs-lookup"><span data-stu-id="0e943-139">It is recommended that your application call [IDirectDraw7::CreateSurface](/windows/win32/api/ddraw/nf-ddraw-idirectdraw7-createsurface) instead of using this function.</span></span>

<span data-ttu-id="0e943-140">Lors de la création d’une chaîne de surfaces attachées, telle qu’une chaîne de permutation ou une chaîne ou des mipmaps, [**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md) doit être appelé pour chaque surface en premier.</span><span class="sxs-lookup"><span data-stu-id="0e943-140">When creating a chain of attached surfaces, such as a swap chain or chain or mipmaps, [**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md) should be called for each surface first.</span></span> <span data-ttu-id="0e943-141">Appelez ensuite [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md) pour les attacher.</span><span class="sxs-lookup"><span data-stu-id="0e943-141">Then call [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md) to attach them.</span></span> <span data-ttu-id="0e943-142">Enfin, appelez **NtGdiDdCreateSurface** pour la première surface de la chaîne uniquement.</span><span class="sxs-lookup"><span data-stu-id="0e943-142">Finally, call **NtGdiDdCreateSurface** for the first surface in the chain only.</span></span> <span data-ttu-id="0e943-143">Dans ce cas, *hSurface* serait le handle retourné par **NtGdiDdCreateSurfaceObject** pour la première surface de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="0e943-143">In this case, *hSurface* would be the handle returned by **NtGdiDdCreateSurfaceObject** for the first surface in the chain.</span></span>

<span data-ttu-id="0e943-144">**NtGdiDdCreateSurface** doit être appelé uniquement pour créer des surfaces dans la mémoire vidéo locale et non locale.</span><span class="sxs-lookup"><span data-stu-id="0e943-144">**NtGdiDdCreateSurface** should only be called to create surfaces in local and non-local video memory.</span></span> <span data-ttu-id="0e943-145">Il ne doit jamais être appelé pour créer des surfaces de mémoire système.</span><span class="sxs-lookup"><span data-stu-id="0e943-145">It should never be called to create system memory surfaces.</span></span> <span data-ttu-id="0e943-146">Pour créer des surfaces de mémoire système, utilisez [**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md) à la place.</span><span class="sxs-lookup"><span data-stu-id="0e943-146">To create system memory surfaces, use [**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md) instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e943-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e943-147">Requirements</span></span>



| <span data-ttu-id="0e943-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e943-148">Requirement</span></span> | <span data-ttu-id="0e943-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e943-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0e943-150">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e943-150">Minimum supported client</span></span><br/> | <span data-ttu-id="0e943-151">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0e943-151">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="0e943-152">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e943-152">Minimum supported server</span></span><br/> | <span data-ttu-id="0e943-153">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0e943-153">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0e943-154">En-tête</span><span class="sxs-lookup"><span data-stu-id="0e943-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e943-155"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e943-155"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e943-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e943-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e943-157">Prise en charge des clients de bas niveau</span><span class="sxs-lookup"><span data-stu-id="0e943-157">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
