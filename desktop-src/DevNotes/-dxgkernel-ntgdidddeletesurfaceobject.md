---
description: NtGdiDdDeleteSurfaceObject supprime un objet surface en mode noyau précédemment créé.
ms.assetid: 95ce6c73-7e41-4ac3-b849-9b8f53aa3ac3
title: NtGdiDdDeleteSurfaceObject, fonction (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdDeleteSurfaceObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 03988b842aacc29915287490508eb9e9d057e907
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517392"
---
# <a name="ntgdidddeletesurfaceobject-function"></a><span data-ttu-id="86fc9-103">NtGdiDdDeleteSurfaceObject fonction)</span><span class="sxs-lookup"><span data-stu-id="86fc9-103">NtGdiDdDeleteSurfaceObject function</span></span>

<span data-ttu-id="86fc9-104">\[Cette fonction est sujette à modification avec chaque révision du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="86fc9-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="86fc9-105">Utilisez plutôt Microsoft DirectDraw et Microsoft Direct3DAPIs ; Ces API isolent les applications de ces modifications du système d’exploitation et masquent de nombreuses autres difficultés liées à l’interaction directe avec les pilotes d’affichage.\]</span><span class="sxs-lookup"><span data-stu-id="86fc9-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="86fc9-106">**NtGdiDdDeleteSurfaceObject** supprime un objet surface en mode noyau précédemment créé.</span><span class="sxs-lookup"><span data-stu-id="86fc9-106">**NtGdiDdDeleteSurfaceObject** deletes a previously created kernel-mode surface object.</span></span>

## <a name="syntax"></a><span data-ttu-id="86fc9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="86fc9-107">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiDdDeleteSurfaceObject(
  _In_ HANDLE hSurface
);
```



## <a name="parameters"></a><span data-ttu-id="86fc9-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="86fc9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86fc9-109">*hSurface* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="86fc9-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86fc9-110">Handle vers l’objet surface en mode noyau précédemment créé.</span><span class="sxs-lookup"><span data-stu-id="86fc9-110">Handle to the previously created kernel-mode surface object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86fc9-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="86fc9-111">Return value</span></span>

<span data-ttu-id="86fc9-112">En cas de réussite, cette fonction retourne la **valeur true**; Sinon, elle retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="86fc9-112">If successful, this function returns **TRUE**; otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="86fc9-113">Notes</span><span class="sxs-lookup"><span data-stu-id="86fc9-113">Remarks</span></span>

<span data-ttu-id="86fc9-114">Il est recommandé aux applications d’utiliser les API DirectDraw et [Direct3D](../direct3d10/d3d10-graphics-reference.md) pour créer et gérer des objets d’appareils graphiques.</span><span class="sxs-lookup"><span data-stu-id="86fc9-114">Applications are advised to use the DirectDraw and [Direct3D](../direct3d10/d3d10-graphics-reference.md) APIs to create and manage graphics device objects.</span></span> <span data-ttu-id="86fc9-115">Ces constructions résument le processus de création d’appareils de façon simplifiée et indépendante du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="86fc9-115">These constructs abstract the device creation process in a simplified and operating-system-independent way.</span></span>

## <a name="requirements"></a><span data-ttu-id="86fc9-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="86fc9-116">Requirements</span></span>



| <span data-ttu-id="86fc9-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="86fc9-117">Requirement</span></span> | <span data-ttu-id="86fc9-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="86fc9-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="86fc9-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="86fc9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="86fc9-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="86fc9-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="86fc9-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="86fc9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="86fc9-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="86fc9-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="86fc9-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="86fc9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="86fc9-124"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="86fc9-124"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86fc9-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="86fc9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86fc9-126">Prise en charge des clients de bas niveau</span><span class="sxs-lookup"><span data-stu-id="86fc9-126">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="86fc9-127">**DdDeleteSurfaceObject**</span><span class="sxs-lookup"><span data-stu-id="86fc9-127">**DdDeleteSurfaceObject**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-dddeletesurfaceobject)
</dt> <dt>

[<span data-ttu-id="86fc9-128">**NtGdiDdCreateSurfaceObject**</span><span class="sxs-lookup"><span data-stu-id="86fc9-128">**NtGdiDdCreateSurfaceObject**</span></span>](-dxgkernel-ntgdiddcreatesurfaceobject.md)
</dt> </dl>

 

 
