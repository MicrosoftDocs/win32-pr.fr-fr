---
description: Définit la position d’une superposition.
ms.assetid: dd495118-9ceb-4100-a7ec-794659bb4461
title: NtGdiDdSetOverlayPosition, fonction (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdSetOverlayPosition
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 73882e20fd7065d208835c2005d102b1312e8ce1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033601"
---
# <a name="ntgdiddsetoverlayposition-function"></a><span data-ttu-id="1f6bd-103">NtGdiDdSetOverlayPosition fonction)</span><span class="sxs-lookup"><span data-stu-id="1f6bd-103">NtGdiDdSetOverlayPosition function</span></span>

<span data-ttu-id="1f6bd-104">\[Cette fonction est sujette à modification avec chaque révision du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="1f6bd-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="1f6bd-105">Utilisez plutôt Microsoft DirectDraw et Microsoft Direct3DAPIs ; Ces API isolent les applications de ces modifications du système d’exploitation et masquent de nombreuses autres difficultés liées à l’interaction directe avec les pilotes d’affichage.\]</span><span class="sxs-lookup"><span data-stu-id="1f6bd-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="1f6bd-106">Définit la position d’une superposition.</span><span class="sxs-lookup"><span data-stu-id="1f6bd-106">Sets the position for an overlay.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f6bd-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1f6bd-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdSetOverlayPosition(
  _In_    HANDLE                     hSurfaceSource,
  _In_    HANDLE                     hSurfaceDestination,
  _Inout_ PDD_SETOVERLAYPOSITIONDATA puSetOverlayPositionData
);
```



## <a name="parameters"></a><span data-ttu-id="1f6bd-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1f6bd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f6bd-109">*hSurfaceSource* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1f6bd-109">*hSurfaceSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f6bd-110">Handle vers une structure de [**\_ surface \_ locale DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) qui représente la surface de superposition DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="1f6bd-110">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that represents the DirectDraw overlay surface.</span></span>

</dd> <dt>

<span data-ttu-id="1f6bd-111">*hSurfaceDestination* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1f6bd-111">*hSurfaceDestination* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f6bd-112">Pointeur désignant une structure [**\_ \_ locale de surface DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) représentant la surface qui est superposée.</span><span class="sxs-lookup"><span data-stu-id="1f6bd-112">Pointer to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure representing the surface that is being overlaid.</span></span>

</dd> <dt>

<span data-ttu-id="1f6bd-113">*puSetOverlayPositionData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1f6bd-113">*puSetOverlayPositionData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f6bd-114">Pointeur vers une [**structure \_ SETOVERLAYPOSITIONDATA DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_setoverlaypositiondata) qui contient les informations requises pour définir la position de la superposition.</span><span class="sxs-lookup"><span data-stu-id="1f6bd-114">Pointer to a [**DD\_SETOVERLAYPOSITIONDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_setoverlaypositiondata) structure that contains the information required to set the overlay position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f6bd-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1f6bd-115">Return value</span></span>

<span data-ttu-id="1f6bd-116">**NtGdiDdSetOverlayPosition** retourne l’un des codes de rappel suivants.</span><span class="sxs-lookup"><span data-stu-id="1f6bd-116">**NtGdiDdSetOverlayPosition** returns one of the following callback codes.</span></span>



| <span data-ttu-id="1f6bd-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="1f6bd-117">Return code</span></span>                                                                                              | <span data-ttu-id="1f6bd-118">Description</span><span class="sxs-lookup"><span data-stu-id="1f6bd-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1f6bd-119"><dt>**\_pilote DDHAL \_ géré**</dt></span><span class="sxs-lookup"><span data-stu-id="1f6bd-119"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="1f6bd-120">Le pilote a effectué l’opération et a retourné un code de retour valide pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="1f6bd-120">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="1f6bd-121">Si ce code est JJ \_ OK, DirectDraw ou Direct3D continue avec la fonction.</span><span class="sxs-lookup"><span data-stu-id="1f6bd-121">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="1f6bd-122">Dans le cas contraire, DirectDraw ou Direct3D retourne le code d’erreur fourni par le pilote et abandonne la fonction.</span><span class="sxs-lookup"><span data-stu-id="1f6bd-122">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="1f6bd-123"><dt>**DDHAL de \_ pilote \_ NOTHANDLED**</dt></span><span class="sxs-lookup"><span data-stu-id="1f6bd-123"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="1f6bd-124">Le pilote n’a pas de commentaire sur l’opération demandée.</span><span class="sxs-lookup"><span data-stu-id="1f6bd-124">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="1f6bd-125">Si le pilote doit avoir implémenté un rappel particulier, DirectDraw ou Direct3D signale une condition d’erreur.</span><span class="sxs-lookup"><span data-stu-id="1f6bd-125">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="1f6bd-126">Dans le cas contraire, DirectDraw ou Direct3D gère l’opération comme si le rappel de pilote n’avait pas été défini par l’exécution de l’implémentation de DirectDraw ou de l’implémentation indépendante du périphérique Direct3D.</span><span class="sxs-lookup"><span data-stu-id="1f6bd-126">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1f6bd-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1f6bd-127">Requirements</span></span>



| <span data-ttu-id="1f6bd-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1f6bd-128">Requirement</span></span> | <span data-ttu-id="1f6bd-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="1f6bd-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1f6bd-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1f6bd-130">Minimum supported client</span></span><br/> | <span data-ttu-id="1f6bd-131">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1f6bd-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="1f6bd-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1f6bd-132">Minimum supported server</span></span><br/> | <span data-ttu-id="1f6bd-133">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1f6bd-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1f6bd-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="1f6bd-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f6bd-135"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f6bd-135"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f6bd-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f6bd-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f6bd-137">Prise en charge des clients de bas niveau</span><span class="sxs-lookup"><span data-stu-id="1f6bd-137">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
