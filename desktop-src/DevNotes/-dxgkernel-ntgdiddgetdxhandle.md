---
description: Retourne le handle de l’API Microsoft DirectX en mode noyau à utiliser dans les appels suivants aux points d’entrée en mode noyau qui contrôlent le mécanisme de l’API DirectX.
ms.assetid: c95cb188-305f-4b60-be55-0511b57f0597
title: NtGdiDdGetDxHandle, fonction (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetDxHandle
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: f1b304216c518765be73d9f3a3e63d39ec4b37fb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512895"
---
# <a name="ntgdiddgetdxhandle-function"></a><span data-ttu-id="7cb17-103">NtGdiDdGetDxHandle fonction)</span><span class="sxs-lookup"><span data-stu-id="7cb17-103">NtGdiDdGetDxHandle function</span></span>

<span data-ttu-id="7cb17-104">\[Cette fonction est sujette à modification avec chaque révision du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="7cb17-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="7cb17-105">Utilisez plutôt Microsoft DirectDraw et Microsoft Direct3DAPIs ; Ces API isolent les applications de ces modifications du système d’exploitation et masquent de nombreuses autres difficultés liées à l’interaction directe avec les pilotes d’affichage.\]</span><span class="sxs-lookup"><span data-stu-id="7cb17-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="7cb17-106">Retourne le handle de l’API Microsoft DirectX en mode noyau à utiliser dans les appels suivants aux points d’entrée en mode noyau qui contrôlent le mécanisme de l’API DirectX.</span><span class="sxs-lookup"><span data-stu-id="7cb17-106">Returns the kernel-mode Microsoft DirectX  API handle to use in subsequent calls to the kernel-mode entry points that control the DirectX  API mechanism.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cb17-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7cb17-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdGetDxHandle(
  _In_ HANDLE hDirectDraw,
  _In_ HANDLE hSurface,
  _In_ BOOL   bRelease
);
```



## <a name="parameters"></a><span data-ttu-id="7cb17-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7cb17-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cb17-109">*hDirectDraw* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7cb17-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cb17-110">Handle de l’objet DirectDraw propriétaire de l’aire.</span><span class="sxs-lookup"><span data-stu-id="7cb17-110">Handle to DirectDraw object owning the surface.</span></span> <span data-ttu-id="7cb17-111">Ce paramètre est facultatif et peut avoir la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="7cb17-111">This parameter is optional and may be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7cb17-112">*hSurface* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7cb17-112">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cb17-113">Handle vers la surface pour laquelle retourner un handle d’API DirectX en mode noyau.</span><span class="sxs-lookup"><span data-stu-id="7cb17-113">Handle to surface for which to return a kernel-mode DirectX API handle.</span></span> <span data-ttu-id="7cb17-114">Ce paramètre est facultatif et peut avoir la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="7cb17-114">This parameter is optional and may be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7cb17-115">*bRelease* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7cb17-115">*bRelease* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cb17-116">Affectez la valeur **true** si l’interface du mode noyau de l’API DirectX doit être libérée.</span><span class="sxs-lookup"><span data-stu-id="7cb17-116">Set to **TRUE** if the DirectX API kernel mode interface should be released.</span></span> <span data-ttu-id="7cb17-117">Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="7cb17-117">Otherwise, **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7cb17-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7cb17-118">Return value</span></span>

<span data-ttu-id="7cb17-119">Handle d’API DirectX utilisé dans les points d’entrée de noyau orientés API DirectX suivants.</span><span class="sxs-lookup"><span data-stu-id="7cb17-119">A DirectX API handle used in subsequent DirectX API-oriented kernel entry points.</span></span>

## <a name="remarks"></a><span data-ttu-id="7cb17-120">Notes</span><span class="sxs-lookup"><span data-stu-id="7cb17-120">Remarks</span></span>

<span data-ttu-id="7cb17-121">Si *hDirectDraw* et *hSurface* sont tous les deux spécifiés, *hSurface* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="7cb17-121">If both *hDirectDraw* and *hSurface* are specified, *hSurface* is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="7cb17-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7cb17-122">Requirements</span></span>



| <span data-ttu-id="7cb17-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7cb17-123">Requirement</span></span> | <span data-ttu-id="7cb17-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="7cb17-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7cb17-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7cb17-125">Minimum supported client</span></span><br/> | <span data-ttu-id="7cb17-126">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7cb17-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="7cb17-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7cb17-127">Minimum supported server</span></span><br/> | <span data-ttu-id="7cb17-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7cb17-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7cb17-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="7cb17-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="7cb17-130"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="7cb17-130"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7cb17-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7cb17-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cb17-132">Prise en charge des clients de bas niveau</span><span class="sxs-lookup"><span data-stu-id="7cb17-132">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




