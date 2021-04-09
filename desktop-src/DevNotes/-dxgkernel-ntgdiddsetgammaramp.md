---
description: Définit la rampe gamma de l’appareil.
ms.assetid: 92ea0247-6eec-4c5f-9ea7-65f6b97dde1e
title: NtGdiDdSetGammaRamp, fonction (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdSetGammaRamp
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 0c5efba67eedbd6e70f1e0682f42c1855948cecd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110122"
---
# <a name="ntgdiddsetgammaramp-function"></a><span data-ttu-id="70233-103">NtGdiDdSetGammaRamp fonction)</span><span class="sxs-lookup"><span data-stu-id="70233-103">NtGdiDdSetGammaRamp function</span></span>

<span data-ttu-id="70233-104">\[Cette fonction est sujette à modification avec chaque révision du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="70233-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="70233-105">Utilisez plutôt Microsoft DirectDraw et Microsoft Direct3DAPIs ; Ces API isolent les applications de ces modifications du système d’exploitation et masquent de nombreuses autres difficultés liées à l’interaction directe avec les pilotes d’affichage.\]</span><span class="sxs-lookup"><span data-stu-id="70233-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="70233-106">Définit la rampe gamma de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="70233-106">Sets the gamma ramp for the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="70233-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="70233-107">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiDdSetGammaRamp(
  _In_ HANDLE hDirectDraw,
  _In_ HDC    hdc,
  _In_ LPVOID lpGammaRamp
);
```



## <a name="parameters"></a><span data-ttu-id="70233-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="70233-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70233-109">*hDirectDraw* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="70233-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70233-110">Handle de l’objet de pilote en mode noyau pour lequel la rampe doit être définie.</span><span class="sxs-lookup"><span data-stu-id="70233-110">Handle to the kernel-mode driver object for which the ramp is to be set.</span></span>

</dd> <dt>

<span data-ttu-id="70233-111">*HDC* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="70233-111">*hdc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70233-112">Réservé.</span><span class="sxs-lookup"><span data-stu-id="70233-112">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="70233-113">*lpGammaRamp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="70233-113">*lpGammaRamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70233-114">Pointeur vers un tableau de structures **DDGAMMARAMP** .</span><span class="sxs-lookup"><span data-stu-id="70233-114">Pointer to an array of **DDGAMMARAMP** structures.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70233-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="70233-115">Return value</span></span>

<span data-ttu-id="70233-116">La valeur de retour est **true** si la fonction réussit.</span><span class="sxs-lookup"><span data-stu-id="70233-116">The return value is **TRUE** if the function is successful.</span></span> <span data-ttu-id="70233-117">Dans le cas contraire, la **valeur est null**.</span><span class="sxs-lookup"><span data-stu-id="70233-117">Otherwise, it is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="70233-118">Notes</span><span class="sxs-lookup"><span data-stu-id="70233-118">Remarks</span></span>

<span data-ttu-id="70233-119">Il est recommandé que les applications utilisent plutôt les méthodes **IDirectDrawGammaControl :: SetGammaRamp** ou [**IDirect3DDevice9 :: SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp) , car ces méthodes offrent les mêmes fonctionnalités indépendamment du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="70233-119">It is recommended that applications use the **IDirectDrawGammaControl::SetGammaRamp** or [**IDirect3DDevice9::SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp) methods instead because these methods offer the same functionality independent of the operating system.</span></span>

## <a name="requirements"></a><span data-ttu-id="70233-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="70233-120">Requirements</span></span>



| <span data-ttu-id="70233-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="70233-121">Requirement</span></span> | <span data-ttu-id="70233-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="70233-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="70233-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="70233-123">Minimum supported client</span></span><br/> | <span data-ttu-id="70233-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="70233-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="70233-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="70233-125">Minimum supported server</span></span><br/> | <span data-ttu-id="70233-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="70233-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="70233-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="70233-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="70233-128"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="70233-128"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70233-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="70233-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70233-130">Prise en charge des clients de bas niveau</span><span class="sxs-lookup"><span data-stu-id="70233-130">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
