---
description: Attache une surface à une autre surface.
ms.assetid: c4ef9e96-c498-4175-a2cd-22e0f88fd86e
title: NtGdiDdAddAttachedSurface, fonction (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdAddAttachedSurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: d6e87d3a077c1381eeaa306e594daec0f5b855d1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860810"
---
# <a name="ntgdiddaddattachedsurface-function"></a><span data-ttu-id="1b6fe-103">NtGdiDdAddAttachedSurface fonction)</span><span class="sxs-lookup"><span data-stu-id="1b6fe-103">NtGdiDdAddAttachedSurface function</span></span>

<span data-ttu-id="1b6fe-104">\[Cette fonction est sujette à modification avec chaque révision du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="1b6fe-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="1b6fe-105">Utilisez plutôt Microsoft DirectDraw et Microsoft Direct3DAPIs ; Ces API isolent les applications de ces modifications du système d’exploitation et masquent de nombreuses autres difficultés liées à l’interaction directe avec les pilotes d’affichage.\]</span><span class="sxs-lookup"><span data-stu-id="1b6fe-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="1b6fe-106">Attache une surface à une autre surface.</span><span class="sxs-lookup"><span data-stu-id="1b6fe-106">Attaches a surface to another surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b6fe-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1b6fe-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdAddAttachedSurface(
  _In_    HANDLE                     hSurface,
  _In_    HANDLE                     hSurfaceAttached,
  _Inout_ PDD_ADDATTACHEDSURFACEDATA puAddAttachedSurfaceData
);
```



## <a name="parameters"></a><span data-ttu-id="1b6fe-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1b6fe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b6fe-109">*hSurface* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1b6fe-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b6fe-110">Handle vers une structure de [**\_ surface \_ locale DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) qui représente la surface à laquelle une autre surface est attachée.</span><span class="sxs-lookup"><span data-stu-id="1b6fe-110">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that represents the surface to which another surface is being attached.</span></span>

</dd> <dt>

<span data-ttu-id="1b6fe-111">*hSurfaceAttached* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1b6fe-111">*hSurfaceAttached* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b6fe-112">Handle vers une structure de [**\_ surface \_ locale DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) qui représente la surface à attacher.</span><span class="sxs-lookup"><span data-stu-id="1b6fe-112">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that represents the surface to be attached.</span></span>

</dd> <dt>

<span data-ttu-id="1b6fe-113">*puAddAttachedSurfaceData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1b6fe-113">*puAddAttachedSurfaceData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b6fe-114">Pointeur vers une [**structure \_ ADDATTACHEDSURFACEDATA DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_addattachedsurfacedata) qui contient les informations requises pour que le pilote exécute la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="1b6fe-114">Pointer to a [**DD\_ADDATTACHEDSURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_addattachedsurfacedata) structure that contains information required for the driver to perform the attachment.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b6fe-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1b6fe-115">Return value</span></span>

<span data-ttu-id="1b6fe-116">**NtGdiDdAddAttachedSurface** retourne l’un des codes de rappel suivants.</span><span class="sxs-lookup"><span data-stu-id="1b6fe-116">**NtGdiDdAddAttachedSurface** returns one of the following callback codes.</span></span>



| <span data-ttu-id="1b6fe-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="1b6fe-117">Return code</span></span>                                                                                              | <span data-ttu-id="1b6fe-118">Description</span><span class="sxs-lookup"><span data-stu-id="1b6fe-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1b6fe-119"><dt>**\_pilote DDHAL \_ géré**</dt></span><span class="sxs-lookup"><span data-stu-id="1b6fe-119"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="1b6fe-120">Le pilote a effectué l’opération et a retourné un code de retour valide pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="1b6fe-120">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="1b6fe-121">Si ce code est JJ \_ OK, DirectDraw ou Direct3D continue avec la fonction.</span><span class="sxs-lookup"><span data-stu-id="1b6fe-121">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="1b6fe-122">Dans le cas contraire, DirectDraw ou Direct3D retourne le code d’erreur fourni par le pilote et abandonne la fonction.</span><span class="sxs-lookup"><span data-stu-id="1b6fe-122">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="1b6fe-123"><dt>**DDHAL de \_ pilote \_ NOTHANDLED**</dt></span><span class="sxs-lookup"><span data-stu-id="1b6fe-123"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="1b6fe-124">Le pilote n’a pas de commentaire sur l’opération demandée.</span><span class="sxs-lookup"><span data-stu-id="1b6fe-124">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="1b6fe-125">Si le pilote doit avoir implémenté un rappel particulier, DirectDraw ou Direct3D signale une condition d’erreur.</span><span class="sxs-lookup"><span data-stu-id="1b6fe-125">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="1b6fe-126">Dans le cas contraire, DirectDraw ou Direct3D gère l’opération comme si le rappel de pilote n’avait pas été défini par l’exécution de l’implémentation de DirectDraw ou de l’implémentation indépendante du périphérique Direct3D.</span><span class="sxs-lookup"><span data-stu-id="1b6fe-126">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1b6fe-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1b6fe-127">Requirements</span></span>



| <span data-ttu-id="1b6fe-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1b6fe-128">Requirement</span></span> | <span data-ttu-id="1b6fe-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="1b6fe-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1b6fe-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b6fe-130">Minimum supported client</span></span><br/> | <span data-ttu-id="1b6fe-131">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1b6fe-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="1b6fe-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b6fe-132">Minimum supported server</span></span><br/> | <span data-ttu-id="1b6fe-133">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1b6fe-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1b6fe-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="1b6fe-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b6fe-135"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b6fe-135"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b6fe-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b6fe-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b6fe-137">Prise en charge des clients de bas niveau</span><span class="sxs-lookup"><span data-stu-id="1b6fe-137">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
