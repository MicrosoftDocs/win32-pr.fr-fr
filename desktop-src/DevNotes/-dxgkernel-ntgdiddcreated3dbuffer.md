---
description: Utilisé pour créer une commande de niveau pilote ou une mémoire tampon de vertex de la description spécifiée.
ms.assetid: c65403a1-5686-4c7d-80a4-6e49417c11eb
title: NtGdiDdCreateD3DBuffer, fonction (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateD3DBuffer
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 2d402a70822fba094d22c82b8767ee3298b86374
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950437"
---
# <a name="ntgdiddcreated3dbuffer-function"></a><span data-ttu-id="3f04f-103">NtGdiDdCreateD3DBuffer fonction)</span><span class="sxs-lookup"><span data-stu-id="3f04f-103">NtGdiDdCreateD3DBuffer function</span></span>

<span data-ttu-id="3f04f-104">\[Cette fonction est sujette à modification avec chaque révision du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="3f04f-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="3f04f-105">Utilisez plutôt Microsoft DirectDraw et Microsoft Direct3DAPIs ; Ces API isolent les applications de ces modifications du système d’exploitation et masquent de nombreuses autres difficultés liées à l’interaction directe avec les pilotes d’affichage.\]</span><span class="sxs-lookup"><span data-stu-id="3f04f-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="3f04f-106">Utilisé pour créer une commande de niveau pilote ou une mémoire tampon de vertex de la description spécifiée.</span><span class="sxs-lookup"><span data-stu-id="3f04f-106">Used to create a driver-level command or vertex buffer of the specified description.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f04f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3f04f-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdCreateD3DBuffer(
  _In_    HANDLE               hDirectDraw,
  _Inout_ HANDLE               *hSurface,
  _Inout_ DDSURFACEDESC        *puSurfaceDescription,
  _Inout_ DD_SURFACE_GLOBAL    *puSurfaceGlobalData,
  _Inout_ DD_SURFACE_LOCAL     *puSurfaceLocalData,
  _Inout_ DD_SURFACE_MORE      *puSurfaceMoreData,
  _Inout_ DD_CREATESURFACEDATA *puCreateSurfaceData,
  _Inout_ HANDLE               *puhSurface
);
```



## <a name="parameters"></a><span data-ttu-id="3f04f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3f04f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f04f-109">*hDirectDraw* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3f04f-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f04f-110">Handle vers la [**structure \_ \_ globale d’JJ DIRECTDRAW**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) représentant le pilote.</span><span class="sxs-lookup"><span data-stu-id="3f04f-110">Handle to the [**DD\_DIRECTDRAW\_GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) structure representing the driver.</span></span>

</dd> <dt>

<span data-ttu-id="3f04f-111">*hSurface* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="3f04f-111">*hSurface* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f04f-112">Pointeur vers un tableau de handles de surface.</span><span class="sxs-lookup"><span data-stu-id="3f04f-112">Pointer to an array of surface handles.</span></span> <span data-ttu-id="3f04f-113">L’appelant peut définir ces handles aux valeurs de handle précédentes si les surfaces sont recréées après un changement de mode.</span><span class="sxs-lookup"><span data-stu-id="3f04f-113">The caller can set these handles to the previous handle values if the surfaces are being re-created after a mode switch.</span></span> <span data-ttu-id="3f04f-114">Ce processus est appelé « restauration » dans la documentation de DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="3f04f-114">This process is called "restoring" in the DirectDraw documentation.</span></span>

</dd> <dt>

<span data-ttu-id="3f04f-115">*puSurfaceDescription* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="3f04f-115">*puSurfaceDescription* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f04f-116">Pointeur vers une structure [**DDSURFACEDESC**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) décrivant la surface ou la mémoire tampon que le pilote doit créer.</span><span class="sxs-lookup"><span data-stu-id="3f04f-116">Pointer to a [**DDSURFACEDESC**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) structure describing the surface or buffer that the driver should create.</span></span>

</dd> <dt>

<span data-ttu-id="3f04f-117">*puSurfaceGlobalData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="3f04f-117">*puSurfaceGlobalData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f04f-118">Pointeur vers une [**structure \_ \_ globale de surface DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) qui contient des données de surface partagées globalement avec plusieurs surfaces.</span><span class="sxs-lookup"><span data-stu-id="3f04f-118">Pointer to a [**DD\_SURFACE\_GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) structure containing surface data that is shared globally with multiple surfaces.</span></span>

</dd> <dt>

<span data-ttu-id="3f04f-119">*puSurfaceLocalData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="3f04f-119">*puSurfaceLocalData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f04f-120">Pointeur désignant une liste de structures [**\_ \_ locales de surface DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) décrivant les objets surface créés par le pilote.</span><span class="sxs-lookup"><span data-stu-id="3f04f-120">Pointer to a list of [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structures describing the surface objects created by the driver.</span></span> <span data-ttu-id="3f04f-121">Il n’y a généralement qu’une seule entrée dans ce tableau.</span><span class="sxs-lookup"><span data-stu-id="3f04f-121">There is usually only one entry in this array.</span></span>

</dd> <dt>

<span data-ttu-id="3f04f-122">*puSurfaceMoreData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="3f04f-122">*puSurfaceMoreData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f04f-123">Pointeur vers une structure de [**\_ \_ plus grande surface DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) qui contient des données de surface locales supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="3f04f-123">Pointer to a [**DD\_SURFACE\_MORE**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) structure that contains additional local surface data.</span></span>

</dd> <dt>

<span data-ttu-id="3f04f-124">*puCreateSurfaceData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="3f04f-124">*puCreateSurfaceData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f04f-125">Pointeur vers une [**structure \_ CREATESURFACEDATA DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfacedata) qui contient les informations requises pour créer la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="3f04f-125">Pointer to a [**DD\_CREATESURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfacedata) structure that contains the information required to create the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="3f04f-126">*puhSurface* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="3f04f-126">*puhSurface* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f04f-127">Est utilisé par l’API DirectDraw et ne doit pas être renseigné par le pilote.</span><span class="sxs-lookup"><span data-stu-id="3f04f-127">Is used by the DirectDraw  API and should not be filled in by the driver.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f04f-128">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3f04f-128">Return value</span></span>

<span data-ttu-id="3f04f-129">**NtGdiDdCreateD3DBuffer** retourne l’un des codes de rappel suivants.</span><span class="sxs-lookup"><span data-stu-id="3f04f-129">**NtGdiDdCreateD3DBuffer** returns one of the following callback codes.</span></span>



| <span data-ttu-id="3f04f-130">Code de retour</span><span class="sxs-lookup"><span data-stu-id="3f04f-130">Return code</span></span>                                                                                              | <span data-ttu-id="3f04f-131">Description</span><span class="sxs-lookup"><span data-stu-id="3f04f-131">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3f04f-132"><dt>**\_pilote DDHAL \_ géré**</dt></span><span class="sxs-lookup"><span data-stu-id="3f04f-132"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="3f04f-133">Le pilote a effectué l’opération et a retourné un code de retour valide pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="3f04f-133">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="3f04f-134">Si ce code est JJ \_ OK, DirectDraw ou Direct3D continue avec la fonction.</span><span class="sxs-lookup"><span data-stu-id="3f04f-134">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="3f04f-135">Dans le cas contraire, DirectDraw ou Direct3D retourne le code d’erreur fourni par le pilote et abandonne la fonction.</span><span class="sxs-lookup"><span data-stu-id="3f04f-135">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="3f04f-136"><dt>**DDHAL de \_ pilote \_ NOTHANDLED**</dt></span><span class="sxs-lookup"><span data-stu-id="3f04f-136"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="3f04f-137">Le pilote n’a pas de commentaire sur l’opération demandée.</span><span class="sxs-lookup"><span data-stu-id="3f04f-137">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="3f04f-138">Si le pilote doit avoir implémenté un rappel particulier, DirectDraw ou Direct3D signale une condition d’erreur.</span><span class="sxs-lookup"><span data-stu-id="3f04f-138">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="3f04f-139">Dans le cas contraire, DirectDraw ou Direct3D gère l’opération comme si le rappel de pilote n’avait pas été défini par l’exécution de l’implémentation de DirectDraw ou de l’implémentation indépendante du périphérique Direct3D.</span><span class="sxs-lookup"><span data-stu-id="3f04f-139">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3f04f-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3f04f-140">Requirements</span></span>



| <span data-ttu-id="3f04f-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3f04f-141">Requirement</span></span> | <span data-ttu-id="3f04f-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="3f04f-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3f04f-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3f04f-143">Minimum supported client</span></span><br/> | <span data-ttu-id="3f04f-144">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3f04f-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="3f04f-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3f04f-145">Minimum supported server</span></span><br/> | <span data-ttu-id="3f04f-146">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3f04f-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3f04f-147">En-tête</span><span class="sxs-lookup"><span data-stu-id="3f04f-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f04f-148"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f04f-148"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f04f-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f04f-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f04f-150">Prise en charge des clients de bas niveau</span><span class="sxs-lookup"><span data-stu-id="3f04f-150">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
