---
description: Crée un contexte de périphérique (DC) pour la surface spécifiée.
ms.assetid: c2eaaed6-db19-4dab-ac12-6b4e7eeb58e4
title: NtGdiDdGetDC, fonction (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetDC
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 4f930334f0712107d5651a22b35d6917c7977011
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110670"
---
# <a name="ntgdiddgetdc-function"></a><span data-ttu-id="54824-103">NtGdiDdGetDC fonction)</span><span class="sxs-lookup"><span data-stu-id="54824-103">NtGdiDdGetDC function</span></span>

<span data-ttu-id="54824-104">\[Cette fonction est sujette à modification avec chaque révision du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="54824-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="54824-105">Utilisez plutôt Microsoft DirectDraw et Microsoft Direct3DAPIs ; Ces API isolent les applications de ces modifications du système d’exploitation et masquent de nombreuses autres difficultés liées à l’interaction directe avec les pilotes d’affichage.\]</span><span class="sxs-lookup"><span data-stu-id="54824-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="54824-106">Crée un contexte de périphérique (DC) pour la surface spécifiée.</span><span class="sxs-lookup"><span data-stu-id="54824-106">Creates a device context (DC) for the specified surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="54824-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="54824-107">Syntax</span></span>


```C++
HDC APIENTRY NtGdiDdGetDC(
  _In_ HANDLE       hSurface,
  _In_ PALETTEENTRY *puColorTable
);
```



## <a name="parameters"></a><span data-ttu-id="54824-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="54824-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54824-109">*hSurface* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="54824-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54824-110">Handle vers une surface DirectDraw en mode noyau précédemment retournée par [**NtGdiDdCreateSurface**](-dxgkernel-ntgdiddcreatesurface.md) ou [**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md).</span><span class="sxs-lookup"><span data-stu-id="54824-110">Handle to a kernel-mode DirectDraw surface previously returned by [**NtGdiDdCreateSurface**](-dxgkernel-ntgdiddcreatesurface.md) or [**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="54824-111">*puColorTable* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="54824-111">*puColorTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54824-112">Pointeur vers une table de couleurs de remplacement pour le contrôleur de périphérique retourné.</span><span class="sxs-lookup"><span data-stu-id="54824-112">Pointer to an override color table for the returned DC.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54824-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="54824-113">Return value</span></span>

<span data-ttu-id="54824-114">En cas de réussite, cette fonction retourne un **HDC** valide ; Sinon, elle retourne la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="54824-114">If successful, this function returns a valid **HDC**; otherwise it returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="54824-115">Notes</span><span class="sxs-lookup"><span data-stu-id="54824-115">Remarks</span></span>

<span data-ttu-id="54824-116">Un seul contrôleur de périphérique est autorisé par surface à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="54824-116">Only one DC is allowed per surface at any given time.</span></span> <span data-ttu-id="54824-117">Les appels suivants à **NtGdiDdGetDC** échouent tant que le DC précédent n’est pas libéré.</span><span class="sxs-lookup"><span data-stu-id="54824-117">Subsequent calls to **NtGdiDdGetDC** will fail until the previous DC is released.</span></span>

<span data-ttu-id="54824-118">Il est recommandé aux applications d’appeler [IDirectDrawSurface7 :: GetDC](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-getdc) à la place, ce qui fournit les mêmes fonctionnalités d’une manière indépendante du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="54824-118">Applications are advised to call [IDirectDrawSurface7::GetDC](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-getdc) instead, which provides the same functionality in a manner independent of the operating system.</span></span>

## <a name="requirements"></a><span data-ttu-id="54824-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="54824-119">Requirements</span></span>



| <span data-ttu-id="54824-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="54824-120">Requirement</span></span> | <span data-ttu-id="54824-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="54824-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="54824-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="54824-122">Minimum supported client</span></span><br/> | <span data-ttu-id="54824-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="54824-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="54824-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="54824-124">Minimum supported server</span></span><br/> | <span data-ttu-id="54824-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="54824-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="54824-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="54824-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="54824-127"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="54824-127"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54824-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54824-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54824-129">Prise en charge des clients de bas niveau</span><span class="sxs-lookup"><span data-stu-id="54824-129">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="54824-130">**DdGetDC**</span><span class="sxs-lookup"><span data-stu-id="54824-130">**DdGetDC**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddgetdc)
</dt> </dl>

 

 
