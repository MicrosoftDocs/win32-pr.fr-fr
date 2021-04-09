---
description: Interroge une représentation en mode noyau précédemment créée d’un objet Microsoft DirectDraw pour ses fonctionnalités.
ms.assetid: ec07c7ef-4c57-4ed9-849b-f30692cc3181
title: NtGdiDdQueryDirectDrawObject, fonction (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdQueryDirectDrawObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 557854f70f4f1a55022b16d1bfe045efbc017a13
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861474"
---
# <a name="ntgdiddquerydirectdrawobject-function"></a><span data-ttu-id="76abf-103">NtGdiDdQueryDirectDrawObject fonction)</span><span class="sxs-lookup"><span data-stu-id="76abf-103">NtGdiDdQueryDirectDrawObject function</span></span>

<span data-ttu-id="76abf-104">\[Cette fonction est sujette à modification avec chaque révision du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="76abf-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="76abf-105">Utilisez à la place DirectDraw et Microsoft Direct3DAPIs ; Ces API isolent les applications de ces modifications du système d’exploitation et masquent de nombreuses autres difficultés liées à l’interaction directe avec les pilotes d’affichage.\]</span><span class="sxs-lookup"><span data-stu-id="76abf-105">Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="76abf-106">Interroge une représentation en mode noyau précédemment créée d’un objet Microsoft DirectDraw pour ses fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="76abf-106">Queries a previously created kernel-mode representation of a Microsoft DirectDraw object for its capabilities.</span></span>

## <a name="syntax"></a><span data-ttu-id="76abf-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="76abf-107">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiDdQueryDirectDrawObject(
  _In_  HANDLE                      hDirectDrawLocal,
  _Out_ DD_HALINFO                  *pHalInfo,
        DWORD                       *pCallBackFlags,
  _Out_ LPD3DNTHAL_CALLBACKS        puD3dCallbacks,
  _Out_ LPD3DNTHAL_GLOBALDRIVERDATA puD3dDriverData,
  _Out_ PDD_D3DBUFCALLBACKS         puD3dBufferCallbacks,
  _Out_ LPDDSURFACEDESC             puD3dTextureFormats,
  _Out_ DWORD                       *puNumHeaps,
  _Out_ VIDEOMEMORY                 *puvmList,
  _Out_ DWORD                       *puNumFourCC,
  _Out_ DWORD                       *puFourCC
);
```



## <a name="parameters"></a><span data-ttu-id="76abf-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="76abf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76abf-109">*hDirectDrawLocal* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="76abf-109">*hDirectDrawLocal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76abf-110">Handle vers l’appareil DirectDraw en mode noyau précédemment créé.</span><span class="sxs-lookup"><span data-stu-id="76abf-110">Handle to the previously-created kernel-mode DirectDraw device.</span></span>

</dd> <dt>

<span data-ttu-id="76abf-111">*pHalInfo* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="76abf-111">*pHalInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="76abf-112">Pointeur vers une [**structure \_ HALINFO DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo) qui sera remplie avec les fonctionnalités de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="76abf-112">Pointer to a [**DD\_HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo) structure that will be filled with the device's capabilities.</span></span> <span data-ttu-id="76abf-113">Pour plus d’informations, consultez la documentation du DDK.</span><span class="sxs-lookup"><span data-stu-id="76abf-113">See DDK documentation for details.</span></span>

</dd> <dt>

<span data-ttu-id="76abf-114">*pCallBackFlags*</span><span class="sxs-lookup"><span data-stu-id="76abf-114">*pCallBackFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="76abf-115">Pointeur vers une mémoire tampon fournie par l’appelant qui stocke des indicateurs de rappel signalés par un pilote.</span><span class="sxs-lookup"><span data-stu-id="76abf-115">Pointer to a caller-provided buffer that stores driver-reported callback flags.</span></span> <span data-ttu-id="76abf-116">La mémoire tampon doit être d’une taille de 3 \* sizeof (DWORD) et stocke les indicateurs de rappel dans l’ordre suivant : pCallBackFlags \[ 0 \] pour les indicateurs dans les [**\_ rappels DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_callbacks), PCallBackFlags \[ 1 \] pour les indicateurs dans [**DD \_ SURFACECALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surfacecallbacks)et pCallBackFlags \[ 2 \] pour les indicateurs dans [**DD \_ PALETTECALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_palettecallbacks).</span><span class="sxs-lookup"><span data-stu-id="76abf-116">The buffer should be of size 3\*sizeof(DWORD) and stores callback flags in the following order: pCallBackFlags\[0\] for flags in [**DD\_CALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_callbacks), pCallBackFlags\[1\] for flags in [**DD\_SURFACECALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surfacecallbacks), and pCallBackFlags\[2\] for flags in [**DD\_PALETTECALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_palettecallbacks).</span></span> <span data-ttu-id="76abf-117">Pour plus d’informations, consultez la documentation du DDK.</span><span class="sxs-lookup"><span data-stu-id="76abf-117">See DDK documentation for details.</span></span>

</dd> <dt>

<span data-ttu-id="76abf-118">*puD3dCallbacks* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="76abf-118">*puD3dCallbacks* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="76abf-119">Pointeur vers un tableau de pointeurs de rappel Direct3D.</span><span class="sxs-lookup"><span data-stu-id="76abf-119">Pointer to a table of Direct3D callback pointers.</span></span> <span data-ttu-id="76abf-120">La table est remplie avec des pointeurs vers des fonctions dans Gdi32.dll qui imitent un pilote d’affichage Direct3D.</span><span class="sxs-lookup"><span data-stu-id="76abf-120">The table is filled with pointers to functions within Gdi32.dll that imitate a Direct3D display driver.</span></span> <span data-ttu-id="76abf-121">Cette table de rappel est identique à la \_ structure D3DHAL D3DCALLBACKS décrite dans la documentation du DDK.</span><span class="sxs-lookup"><span data-stu-id="76abf-121">This callback table is identical to the D3DHAL\_D3DCALLBACKS structure discussed in the DDK documentation.</span></span>

</dd> <dt>

<span data-ttu-id="76abf-122">*puD3dDriverData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="76abf-122">*puD3dDriverData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="76abf-123">Pointeur vers [**D3DHAL \_ GLOBALDRIVERDATA**](/windows-hardware/drivers/ddi/d3dhal/ns-d3dhal-_d3dhal_globaldriverdata) Data, comme décrit dans la documentation du DDK.</span><span class="sxs-lookup"><span data-stu-id="76abf-123">Pointer to [**D3DHAL\_GLOBALDRIVERDATA**](/windows-hardware/drivers/ddi/d3dhal/ns-d3dhal-_d3dhal_globaldriverdata) data, as described in the DDK documentation.</span></span>

</dd> <dt>

<span data-ttu-id="76abf-124">*puD3dBufferCallbacks* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="76abf-124">*puD3dBufferCallbacks* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="76abf-125">Pointeur vers un tableau de pointeurs de rappel.</span><span class="sxs-lookup"><span data-stu-id="76abf-125">Pointer to a table of callback pointers.</span></span> <span data-ttu-id="76abf-126">La table est remplie avec des pointeurs vers des fonctions dans Gdi32.dll qui imitent un pilote d’affichage Direct3D.</span><span class="sxs-lookup"><span data-stu-id="76abf-126">The table is filled with pointers to functions within Gdi32.dll that imitate a Direct3D display driver.</span></span> <span data-ttu-id="76abf-127">Cette table de rappel est identique à la \_ structure DDHAL DDEXEBUFCALLBACKS, qui est mappée à la structure [**DD de \_ D3DBUFCALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_d3dbufcallbacks) décrite dans la documentation du DDK, sauf que les membres XxxD3DBuffer dans **DD \_ D3DBUFCALLBACKS** sont remplacés par XxxExecuteBuffer dans DDHAL \_ DDEXEBUFCALLBACKS.</span><span class="sxs-lookup"><span data-stu-id="76abf-127">This callback table is identical to the DDHAL\_DDEXEBUFCALLBACKS structure, which maps to the [**DD\_D3DBUFCALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_d3dbufcallbacks) structure discussed in the DDK documentation, except that members XxxD3DBuffer in **DD\_D3DBUFCALLBACKS** are replaced with XxxExecuteBuffer in DDHAL\_DDEXEBUFCALLBACKS.</span></span>

</dd> <dt>

<span data-ttu-id="76abf-128">*puD3dTextureFormats* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="76abf-128">*puD3dTextureFormats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="76abf-129">Pointeur vers un tableau de structures [**DDSURFACEDESC**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) qui définissent le jeu de formats de texture autorisés.</span><span class="sxs-lookup"><span data-stu-id="76abf-129">Pointer to an array of [**DDSURFACEDESC**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) structures that define the set of permissible texture formats.</span></span>

</dd> <dt>

<span data-ttu-id="76abf-130">*puNumHeaps* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="76abf-130">*puNumHeaps* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="76abf-131">Pointeur vers le membre **dwNumHeaps** de [**DD \_ HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo).**vmiData**.</span><span class="sxs-lookup"><span data-stu-id="76abf-131">Pointer to the **dwNumHeaps** member of [**DD\_HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo).**vmiData**.</span></span> <span data-ttu-id="76abf-132">Le membre **dwNumHeaps** spécifie le nombre de segments de mémoire dans *puvmList*.</span><span class="sxs-lookup"><span data-stu-id="76abf-132">The **dwNumHeaps** member specifies the number of memory heaps in *puvmList*.</span></span> <span data-ttu-id="76abf-133">Pour plus d’informations, consultez la documentation du DDK.</span><span class="sxs-lookup"><span data-stu-id="76abf-133">See DDK documentation for details.</span></span>

</dd> <dt>

<span data-ttu-id="76abf-134">*puvmList* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="76abf-134">*puvmList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="76abf-135">Pointeur vers une liste de descripteurs de tas de mémoire vidéo.</span><span class="sxs-lookup"><span data-stu-id="76abf-135">Pointer to a list of video memory heap descriptors.</span></span> <span data-ttu-id="76abf-136">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="76abf-136">Can be **NULL**.</span></span> <span data-ttu-id="76abf-137">Ce paramètre n’est pas utilisé, car la gestion de la mémoire vidéo est gérée entièrement en mode noyau.</span><span class="sxs-lookup"><span data-stu-id="76abf-137">This parameter is not used because video memory management is handled entirely within kernel mode.</span></span>

</dd> <dt>

<span data-ttu-id="76abf-138">*puNumFourCC* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="76abf-138">*puNumFourCC* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="76abf-139">Pointeur vers le membre **puNumFourCCCodes** de [**DD \_ HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo).**ddCaps**.</span><span class="sxs-lookup"><span data-stu-id="76abf-139">Pointer to the **puNumFourCCCodes** member of [**DD\_HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo).**ddCaps**.</span></span> <span data-ttu-id="76abf-140">Le membre **puNumFourCCCodes** spécifie le nombre de codes [à quatre caractères (FourCC)](../directshow/fourcc-codes.md) pris en charge par le pilote.</span><span class="sxs-lookup"><span data-stu-id="76abf-140">The **puNumFourCCCodes** member specifies the number of [Four-Character Codes (FOURCC)](../directshow/fourcc-codes.md) codes that the driver supports.</span></span> <span data-ttu-id="76abf-141">Pour plus d’informations, consultez la documentation du DDK.</span><span class="sxs-lookup"><span data-stu-id="76abf-141">See DDK documentation for details.</span></span>

</dd> <dt>

<span data-ttu-id="76abf-142">*puFourCC* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="76abf-142">*puFourCC* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="76abf-143">Pointeur désignant une liste de formats de surface de [codes à quatre caractères (FourCC)](../directshow/fourcc-codes.md) pris en charge.</span><span class="sxs-lookup"><span data-stu-id="76abf-143">Pointer to a list of supported [Four-Character Codes (FOURCC)](../directshow/fourcc-codes.md) surface formats.</span></span> <span data-ttu-id="76abf-144">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="76abf-144">Can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76abf-145">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="76abf-145">Return value</span></span>

<span data-ttu-id="76abf-146">En cas de réussite, cette fonction retourne la **valeur true**; Sinon, elle retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="76abf-146">If successful, this function returns **TRUE**; otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="76abf-147">Notes</span><span class="sxs-lookup"><span data-stu-id="76abf-147">Remarks</span></span>

<span data-ttu-id="76abf-148">Un appel à cette fonction est conçu pour être effectué dans un processus en deux étapes.</span><span class="sxs-lookup"><span data-stu-id="76abf-148">A call to this function is designed to be made in a two-step process.</span></span> <span data-ttu-id="76abf-149">Dans la première étape, *puFourCC*, *puvmList* et *PuD3dTextureFormats* doivent avoir la **valeur null**, et [**DdQueryDirectDrawObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddquerydirectdrawobject) remplira le [**\_ HALINFO DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo).**ddCaps**. **dwNumFourCCCodes**, **DD \_ HALINFO**.**vmiData**. **dwNumHeaps** et [**D3DHAL \_ GLOBALDRIVERDATA**](/windows-hardware/drivers/ddi/d3dhal/ns-d3dhal-_d3dhal_globaldriverdata).**dwNumTextureFormats** avec le nombre d’entrées qui doivent être retournées.</span><span class="sxs-lookup"><span data-stu-id="76abf-149">In the first step, *puFourCC*, *puvmList* and *puD3dTextureFormats* should be **NULL**, and [**DdQueryDirectDrawObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddquerydirectdrawobject) will fill in [**DD\_HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo).**ddCaps**.**dwNumFourCCCodes**, **DD\_HALINFO**.**vmiData**.**dwNumHeaps**, and [**D3DHAL\_GLOBALDRIVERDATA**](/windows-hardware/drivers/ddi/d3dhal/ns-d3dhal-_d3dhal_globaldriverdata).**dwNumTextureFormats** with the number of entries that are to be returned.</span></span> <span data-ttu-id="76abf-150">Dans le deuxième appel, l’appelant doit allouer des tableaux de la taille indiquée et passer ces pointeurs au lieu de valeurs **null** dans les paramètres *puFourCC*, *puvmList* et *puD3dTextureFormats* .</span><span class="sxs-lookup"><span data-stu-id="76abf-150">In the second call, the caller should allocate arrays of the indicated size and pass those pointers instead of **NULL** values in the *puFourCC*, *puvmList* and *puD3dTextureFormats* parameters.</span></span> <span data-ttu-id="76abf-151">Les tableaux sont ensuite remplis avec les données appropriées.</span><span class="sxs-lookup"><span data-stu-id="76abf-151">The arrays will then be populated with appropriate data.</span></span>

<span data-ttu-id="76abf-152">Il est recommandé aux applications d’utiliser les API DirectDraw et [Direct3D](../direct3d10/d3d10-graphics-reference.md) pour créer et gérer des objets d’appareils graphiques.</span><span class="sxs-lookup"><span data-stu-id="76abf-152">Applications are advised to use the DirectDraw and [Direct3D](../direct3d10/d3d10-graphics-reference.md) APIs to create and manage graphics device objects.</span></span> <span data-ttu-id="76abf-153">Ces constructions résument le processus de création d’appareils de façon simplifiée et indépendante du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="76abf-153">These constructs abstract the device creation process in a simplified and operating-system-independent way.</span></span>

## <a name="requirements"></a><span data-ttu-id="76abf-154">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="76abf-154">Requirements</span></span>



| <span data-ttu-id="76abf-155">Condition requise</span><span class="sxs-lookup"><span data-stu-id="76abf-155">Requirement</span></span> | <span data-ttu-id="76abf-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="76abf-156">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="76abf-157">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="76abf-157">Minimum supported client</span></span><br/> | <span data-ttu-id="76abf-158">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="76abf-158">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="76abf-159">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="76abf-159">Minimum supported server</span></span><br/> | <span data-ttu-id="76abf-160">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="76abf-160">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="76abf-161">En-tête</span><span class="sxs-lookup"><span data-stu-id="76abf-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="76abf-162"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="76abf-162"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76abf-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="76abf-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76abf-164">Prise en charge des clients de bas niveau</span><span class="sxs-lookup"><span data-stu-id="76abf-164">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="76abf-165">**DdQueryDirectDrawObject**</span><span class="sxs-lookup"><span data-stu-id="76abf-165">**DdQueryDirectDrawObject**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddquerydirectdrawobject)
</dt> <dt>

[<span data-ttu-id="76abf-166">**NtGdiDdCreateDirectDrawObject**</span><span class="sxs-lookup"><span data-stu-id="76abf-166">**NtGdiDdCreateDirectDrawObject**</span></span>](-dxgkernel-ntgdiddcreatedirectdrawobject.md)
</dt> </dl>

 

 
