---
description: Récupère la surface partagée DirectX qui stocke une fenêtre donnée. Cette surface peut être écrite pour mettre à jour le contenu de la fenêtre.
ms.assetid: 500CF5B4-0D56-4201-91F4-7333E45DACEE
title: DwmDxGetWindowSharedSurface fonction)
ms.topic: reference
ms.date: 11/27/2018
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Dwmapi.dll
api_name:
- DwmDxGetWindowSharedSurface
ms.openlocfilehash: 15e7829383ce23e5bc06bb61ab9c0c224ab18182
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517754"
---
# <a name="dwmdxgetwindowsharedsurface-function"></a><span data-ttu-id="fe361-104">DwmDxGetWindowSharedSurface fonction)</span><span class="sxs-lookup"><span data-stu-id="fe361-104">DwmDxGetWindowSharedSurface function</span></span>

<span data-ttu-id="fe361-105">Récupère la surface partagée DirectX qui stocke une fenêtre donnée.</span><span class="sxs-lookup"><span data-stu-id="fe361-105">Retrieves the DirectX shared surface backing a given window.</span></span> <span data-ttu-id="fe361-106">Cette surface peut être écrite pour mettre à jour le contenu de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="fe361-106">This surface can be written to in order to update the contents of the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe361-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fe361-107">Syntax</span></span>

```C++
HRESULT WINAPI DwmDxGetWindowSharedSurface(
  _In_     HWND        hwnd,
  _In_     LUID        luidAdapter,
  _In_opt_ HMONITOR    hmonitorAssociation,
  _In_     DWORD       dwFlags,
  _Inout_  DXGI_FORMAT *pfmtWindow,
  _Out_    HANDLE      *phDxSurface,
  _Out_    UINT64      *puiUpdateId
);
```

## <a name="parameters"></a><span data-ttu-id="fe361-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fe361-108">Parameters</span></span>

`hwnd`

<span data-ttu-id="fe361-109">[**HWND**](/windows/desktop/winprog/windows-data-types) spécifiant la fenêtre à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="fe361-109">An [**HWND**](/windows/desktop/winprog/windows-data-types) specifying the window to be updated.</span></span>

`luidAdapter`

<span data-ttu-id="fe361-110">[**LUID**](/previous-versions/bb401655(v%3dmsdn.10)) de l’adaptateur dans lequel la surface doit être localisée.</span><span class="sxs-lookup"><span data-stu-id="fe361-110">The [**LUID**](/previous-versions/bb401655(v%3dmsdn.10)) of the adapter where the surface should be located.</span></span>

`hmonitorAssociation`

<span data-ttu-id="fe361-111">Réservé.</span><span class="sxs-lookup"><span data-stu-id="fe361-111">Reserved.</span></span>

`dwFlags`

<span data-ttu-id="fe361-112">Ce paramètre peut avoir l’une des valeurs suivantes, ou une combinaison au niveau du bit ou une combinaison de plusieurs valeurs, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="fe361-112">This parameter can be one of the following values, or a bitwise OR combination of multiple values where appropriate.</span></span>

| <span data-ttu-id="fe361-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="fe361-113">Value</span></span> | <span data-ttu-id="fe361-114">Signification</span><span class="sxs-lookup"><span data-stu-id="fe361-114">Meaning</span></span> |
|-|-|
| <span id="DWM_REDIRECTION_FLAG_WAIT"></span><span id="dwm_redirection_flag_wait"></span><dl> <span data-ttu-id="fe361-115"><dt>**DWM \_ Attente de l' \_ indicateur \_ de redirection**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="fe361-115"><dt>**DWM\_REDIRECTION\_FLAG\_WAIT**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="fe361-116">Provoque le blocage de la fonction jusqu’à ce qu’une synchronisation verticale (VSync) soit passée depuis la dernière fois que la fonction a été appelée avec succès.</span><span class="sxs-lookup"><span data-stu-id="fe361-116">Causes the function to block until a vertical synchronization (VSync) has passed since the last time the function was called successfully.</span></span> |
| <span id="DWM_REDIRECTION_FLAG_SUPPORT_PRESENT_TO_GDI_SURFACE"></span><span id="dwm_redirection_flag_support_present_to_gdi_surface"></span><dl> <span data-ttu-id="fe361-117"><dt>**DWM \_ \_ \_ Prise en charge des indicateurs \_ de redirection présents \_ dans \_ GDI \_ surface**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="fe361-117"><dt>**DWM\_REDIRECTION\_FLAG\_SUPPORT\_PRESENT\_TO\_GDI\_SURFACE**</dt> <dt>0x10</dt></span></span> </dl> | <span data-ttu-id="fe361-118">Indique que l’application appelante peut présenter à une surface partagée GDI.</span><span class="sxs-lookup"><span data-stu-id="fe361-118">Indicates that the calling application is capable of presenting to a GDI shared surface.</span></span> |

`pfmtWindow`

<span data-ttu-id="fe361-119">En entrée, le format souhaité de la surface.</span><span class="sxs-lookup"><span data-stu-id="fe361-119">On input, the desired format of the surface.</span></span> <span data-ttu-id="fe361-120">Lors de la sortie, le format réel de la surface retournée.</span><span class="sxs-lookup"><span data-stu-id="fe361-120">On output, the actual format of the returned surface.</span></span>

`phDxSurface`

<span data-ttu-id="fe361-121">À la sortie, handle partagé vers la surface.</span><span class="sxs-lookup"><span data-stu-id="fe361-121">On output, the shared handle to the surface.</span></span>

`puiUpdateId`

<span data-ttu-id="fe361-122">À la sortie, ID de la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="fe361-122">On output, the ID of the update.</span></span>

## <a name="return-value"></a><span data-ttu-id="fe361-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fe361-123">Return value</span></span>

<span data-ttu-id="fe361-124">Cette fonction peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="fe361-124">This function can return one of these values.</span></span>

| <span data-ttu-id="fe361-125">Code de retour</span><span class="sxs-lookup"><span data-stu-id="fe361-125">Return code</span></span> | <span data-ttu-id="fe361-126">Description</span><span class="sxs-lookup"><span data-stu-id="fe361-126">Description</span></span> |
|-|-|
| <span data-ttu-id="fe361-127">**\_OK**</span><span class="sxs-lookup"><span data-stu-id="fe361-127">**S\_OK**</span></span> | <span data-ttu-id="fe361-128">L’appel a réussi, et vous devez mettre à jour la surface, en veillant à transmettre l’ID de mise à jour à [D3DKMTRender](/windows-hardware/drivers/ddi/content/d3dkmthk/nf-d3dkmthk-d3dkmtrender) (dans le membre **PresentHistoryToken** de la structure de **\_ rendu D3DKMT** lorsque la mise à jour est envoyée, puis [**DwmDxUpdateWindowSharedSurface**](dwmdxupdatewindowsharedsurface.md) doit être appelé avec le même ID de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="fe361-128">The call succeeded, and you should update the surface, being sure to pass the update ID to [D3DKMTRender](/windows-hardware/drivers/ddi/content/d3dkmthk/nf-d3dkmthk-d3dkmtrender) (in the **PresentHistoryToken** member of the **D3DKMT\_RENDER** structure when the update is submitted, and then [**DwmDxUpdateWindowSharedSurface**](dwmdxupdatewindowsharedsurface.md) should be called with the same update ID.</span></span> <span data-ttu-id="fe361-129">Notez que **DwmDxUpdateWindowSharedSurface** doit être appelé, que la surface ait ou non été réellement mise à jour.</span><span class="sxs-lookup"><span data-stu-id="fe361-129">Note that **DwmDxUpdateWindowSharedSurface** should be called regardless of whether the surface was actually updated or not.</span></span> |
| <span data-ttu-id="fe361-130">**\_ \_ \_ la surface de redirection GDI du DWM S \_**</span><span class="sxs-lookup"><span data-stu-id="fe361-130">**DWM\_S\_GDI\_REDIRECTION\_SURFACE**</span></span> | <span data-ttu-id="fe361-131">L’appel a réussi, et vous devez mettre à jour la surface en appelant [D3DKMTPresent](/windows-hardware/drivers/ddi/content/d3dkmthk/nf-d3dkmthk-d3dkmtpresent)et en définissant le **modèle** du membre **PRESENTHISTORYTOKEN** sur **D3DKMT \_ PM \_ Redirigé \_**, et en fournissant l’ID de mise à jour dans le membre **BLT** de l’Union.</span><span class="sxs-lookup"><span data-stu-id="fe361-131">The call succeeded, and you should update the surface by calling [D3DKMTPresent](/windows-hardware/drivers/ddi/content/d3dkmthk/nf-d3dkmthk-d3dkmtpresent), and setting **PresentHistoryToken** member's **Model** to **D3DKMT\_PM\_REDIRECTED\_BLT**, and providing the update ID in the **Blt** member of the union.</span></span> <span data-ttu-id="fe361-132">Cette valeur est retournée uniquement si la **\_ \_ \_ prise en charge de l’indicateur de redirection DWM \_ présente \_ à la \_ \_ surface GDI** a été spécifiée dans *dwFlags*.</span><span class="sxs-lookup"><span data-stu-id="fe361-132">This value is only returned if **DWM\_REDIRECTION\_FLAG\_SUPPORT\_PRESENT\_TO\_GDI\_SURFACE** was specified in *dwFlags*.</span></span> |
| <span data-ttu-id="fe361-133">**\_adaptateur DWM \_ E \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="fe361-133">**DWM\_E\_ADAPTER\_NOT\_FOUND**</span></span> | <span data-ttu-id="fe361-134">La valeur de *luidAdapter* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="fe361-134">The value of *luidAdapter* is not valid.</span></span> |
| <span data-ttu-id="fe361-135">**DWM \_ E \_ COMPOSITIONDISABLED**</span><span class="sxs-lookup"><span data-stu-id="fe361-135">**DWM\_E\_COMPOSITIONDISABLED**</span></span> | <span data-ttu-id="fe361-136">DWM n’est pas activé actuellement, et l’application doit présenter une autre méthode.</span><span class="sxs-lookup"><span data-stu-id="fe361-136">DWM is not currently enabled, and the application will need to present another way.</span></span> |

## <a name="remarks"></a><span data-ttu-id="fe361-137">Notes</span><span class="sxs-lookup"><span data-stu-id="fe361-137">Remarks</span></span>

<span data-ttu-id="fe361-138">Cette API est destinée à l’implémentation d’un pilote ou d’un Runtime Graphics.</span><span class="sxs-lookup"><span data-stu-id="fe361-138">This API is intended for implementing a graphics driver or runtime.</span></span> <span data-ttu-id="fe361-139">Une application ne peut pas appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="fe361-139">An application may not call this method.</span></span> <span data-ttu-id="fe361-140">Cette documentation n’est valide que pour Windows 7, et il n’est pas garanti que cette API existe et qu’elle se comporte de manière similaire sur d’autres versions de Windows.</span><span class="sxs-lookup"><span data-stu-id="fe361-140">This documentation is only valid for Windows 7, and this API is not guaranteed to exist nor behave in a similar manner on other versions of Windows.</span></span> <span data-ttu-id="fe361-141">Cette fonction n’est pas présente dans un en-tête ou une bibliothèque de liens statiques, et elle se trouve à l’ordinal 100 dans dwmapi.dll.</span><span class="sxs-lookup"><span data-stu-id="fe361-141">This function is not present in any header or static-link library, and it is located at ordinal 100 in dwmapi.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe361-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fe361-142">Requirements</span></span>

| <span data-ttu-id="fe361-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fe361-143">Requirement</span></span> | <span data-ttu-id="fe361-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="fe361-144">Value</span></span> |
|-|-|
| <span data-ttu-id="fe361-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fe361-145">Minimum supported client</span></span> | <span data-ttu-id="fe361-146">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fe361-146">Windows 7 \[desktop apps only\]</span></span> |
| <span data-ttu-id="fe361-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fe361-147">Minimum supported server</span></span> | <span data-ttu-id="fe361-148">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="fe361-148">None supported</span></span> |
| <span data-ttu-id="fe361-149">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="fe361-149">End of client support</span></span> | <span data-ttu-id="fe361-150">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fe361-150">Windows 7</span></span> |
| <span data-ttu-id="fe361-151">En-tête</span><span class="sxs-lookup"><span data-stu-id="fe361-151">Header</span></span> | <span data-ttu-id="fe361-152">N/A</span><span class="sxs-lookup"><span data-stu-id="fe361-152">N/A</span></span> |
| <span data-ttu-id="fe361-153">DLL</span><span class="sxs-lookup"><span data-stu-id="fe361-153">DLL</span></span> | <span data-ttu-id="fe361-154">Dwmapi.dll</span><span class="sxs-lookup"><span data-stu-id="fe361-154">Dwmapi.dll</span></span> |
