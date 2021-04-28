---
description: NtGdiDdAddAttachedSurface fonction-attache une surface à une autre surface.
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
ms.openlocfilehash: dacaa07a586a88c808d8da07b8233002e8ae5055
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085787"
---
# <a name="ntgdiddaddattachedsurface-function"></a><span data-ttu-id="caed9-103">NtGdiDdAddAttachedSurface fonction)</span><span class="sxs-lookup"><span data-stu-id="caed9-103">NtGdiDdAddAttachedSurface function</span></span>

<span data-ttu-id="caed9-104">\[Cette fonction est sujette à modification avec chaque révision du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="caed9-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="caed9-105">Utilisez plutôt Microsoft DirectDraw et Microsoft Direct3DAPIs ; Ces API isolent les applications de ces modifications du système d’exploitation et masquent de nombreuses autres difficultés liées à l’interaction directe avec les pilotes d’affichage.\]</span><span class="sxs-lookup"><span data-stu-id="caed9-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="caed9-106">Attache une surface à une autre surface.</span><span class="sxs-lookup"><span data-stu-id="caed9-106">Attaches a surface to another surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="caed9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="caed9-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdAddAttachedSurface(
  _In_    HANDLE                     hSurface,
  _In_    HANDLE                     hSurfaceAttached,
  _Inout_ PDD_ADDATTACHEDSURFACEDATA puAddAttachedSurfaceData
);
```



## <a name="parameters"></a><span data-ttu-id="caed9-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="caed9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="caed9-109">*hSurface* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="caed9-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="caed9-110">Handle vers une structure de [**\_ surface \_ locale DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) qui représente la surface à laquelle une autre surface est attachée.</span><span class="sxs-lookup"><span data-stu-id="caed9-110">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that represents the surface to which another surface is being attached.</span></span>

</dd> <dt>

<span data-ttu-id="caed9-111">*hSurfaceAttached* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="caed9-111">*hSurfaceAttached* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="caed9-112">Handle vers une structure de [**\_ surface \_ locale DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) qui représente la surface à attacher.</span><span class="sxs-lookup"><span data-stu-id="caed9-112">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that represents the surface to be attached.</span></span>

</dd> <dt>

<span data-ttu-id="caed9-113">*puAddAttachedSurfaceData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="caed9-113">*puAddAttachedSurfaceData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="caed9-114">Pointeur vers une [**structure \_ ADDATTACHEDSURFACEDATA DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_addattachedsurfacedata) qui contient les informations requises pour que le pilote exécute la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="caed9-114">Pointer to a [**DD\_ADDATTACHEDSURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_addattachedsurfacedata) structure that contains information required for the driver to perform the attachment.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="caed9-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="caed9-115">Return value</span></span>

<span data-ttu-id="caed9-116">**NtGdiDdAddAttachedSurface** retourne l’un des codes de rappel suivants.</span><span class="sxs-lookup"><span data-stu-id="caed9-116">**NtGdiDdAddAttachedSurface** returns one of the following callback codes.</span></span>



| <span data-ttu-id="caed9-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="caed9-117">Return code</span></span>                                                                                              | <span data-ttu-id="caed9-118">Description</span><span class="sxs-lookup"><span data-stu-id="caed9-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="caed9-119"><dt>**\_pilote DDHAL \_ géré**</dt></span><span class="sxs-lookup"><span data-stu-id="caed9-119"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="caed9-120">Le pilote a effectué l’opération et a retourné un code de retour valide pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="caed9-120">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="caed9-121">Si ce code est JJ \_ OK, DirectDraw ou Direct3D continue avec la fonction.</span><span class="sxs-lookup"><span data-stu-id="caed9-121">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="caed9-122">Dans le cas contraire, DirectDraw ou Direct3D retourne le code d’erreur fourni par le pilote et abandonne la fonction.</span><span class="sxs-lookup"><span data-stu-id="caed9-122">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="caed9-123"><dt>**DDHAL de \_ pilote \_ NOTHANDLED**</dt></span><span class="sxs-lookup"><span data-stu-id="caed9-123"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="caed9-124">Le pilote n’a pas de commentaire sur l’opération demandée.</span><span class="sxs-lookup"><span data-stu-id="caed9-124">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="caed9-125">Si le pilote doit avoir implémenté un rappel particulier, DirectDraw ou Direct3D signale une condition d’erreur.</span><span class="sxs-lookup"><span data-stu-id="caed9-125">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="caed9-126">Dans le cas contraire, DirectDraw ou Direct3D gère l’opération comme si le rappel de pilote n’avait pas été défini par l’exécution de l’implémentation de DirectDraw ou de l’implémentation indépendante du périphérique Direct3D.</span><span class="sxs-lookup"><span data-stu-id="caed9-126">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="caed9-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="caed9-127">Requirements</span></span>



| <span data-ttu-id="caed9-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="caed9-128">Requirement</span></span> | <span data-ttu-id="caed9-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="caed9-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="caed9-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="caed9-130">Minimum supported client</span></span><br/> | <span data-ttu-id="caed9-131">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="caed9-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="caed9-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="caed9-132">Minimum supported server</span></span><br/> | <span data-ttu-id="caed9-133">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="caed9-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="caed9-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="caed9-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="caed9-135"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="caed9-135"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="caed9-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="caed9-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="caed9-137">Prise en charge des clients de bas niveau</span><span class="sxs-lookup"><span data-stu-id="caed9-137">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
