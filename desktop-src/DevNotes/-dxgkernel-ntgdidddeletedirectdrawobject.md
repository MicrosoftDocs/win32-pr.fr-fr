---
description: Détruit un objet appareil Microsoft DirectDraw en mode noyau créé précédemment.
ms.assetid: 0b2e1bae-8291-4fe4-9528-980680906e0a
title: NtGdiDdDeleteDirectDrawObject, fonction (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdDeleteDirectDrawObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 9ac10798f83fe7e1a07a0803dd29cfa9cd8b1c98
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110126"
---
# <a name="ntgdidddeletedirectdrawobject-function"></a><span data-ttu-id="5d713-103">NtGdiDdDeleteDirectDrawObject fonction)</span><span class="sxs-lookup"><span data-stu-id="5d713-103">NtGdiDdDeleteDirectDrawObject function</span></span>

<span data-ttu-id="5d713-104">\[Cette fonction est sujette à modification avec chaque révision du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="5d713-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="5d713-105">Utilisez à la place DirectDraw et Microsoft Direct3DAPIs ; Ces API isolent les applications de ces modifications du système d’exploitation et masquent de nombreuses autres difficultés liées à l’interaction directe avec les pilotes d’affichage.\]</span><span class="sxs-lookup"><span data-stu-id="5d713-105">Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="5d713-106">Détruit un objet appareil Microsoft DirectDraw en mode noyau créé précédemment.</span><span class="sxs-lookup"><span data-stu-id="5d713-106">Destroys a previously created kernel-mode Microsoft DirectDraw device object.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d713-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5d713-107">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiDdDeleteDirectDrawObject(
   HANDLE hDirectDrawLocal
);
```



## <a name="parameters"></a><span data-ttu-id="5d713-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5d713-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d713-109">*hDirectDrawLocal*</span><span class="sxs-lookup"><span data-stu-id="5d713-109">*hDirectDrawLocal*</span></span> 
</dt> <dd>

<span data-ttu-id="5d713-110">Handle vers l’objet appareil DirectDraw en mode noyau.</span><span class="sxs-lookup"><span data-stu-id="5d713-110">Handle to the kernel-mode DirectDraw device object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d713-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5d713-111">Return value</span></span>

<span data-ttu-id="5d713-112">En cas de réussite, cette fonction retourne la **valeur true**; Sinon, elle retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="5d713-112">If successful, this function returns **TRUE**; otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d713-113">Notes</span><span class="sxs-lookup"><span data-stu-id="5d713-113">Remarks</span></span>

<span data-ttu-id="5d713-114">Il est recommandé aux applications d’utiliser les API DirectDraw et [Direct3D](../direct3d10/d3d10-graphics-reference.md) pour créer et gérer des objets d’appareils graphiques.</span><span class="sxs-lookup"><span data-stu-id="5d713-114">Applications are advised to use the DirectDraw and [Direct3D](../direct3d10/d3d10-graphics-reference.md) APIs to create and manage graphics device objects.</span></span> <span data-ttu-id="5d713-115">Ces constructions résument le processus de création d’appareils de façon simplifiée et indépendante du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="5d713-115">These constructs abstract the device creation process in a simplified and operating-system-independent way.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d713-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5d713-116">Requirements</span></span>



| <span data-ttu-id="5d713-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5d713-117">Requirement</span></span> | <span data-ttu-id="5d713-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d713-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5d713-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5d713-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5d713-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5d713-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="5d713-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5d713-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5d713-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5d713-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5d713-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="5d713-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d713-124"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d713-124"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d713-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d713-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d713-126">Prise en charge des clients de bas niveau</span><span class="sxs-lookup"><span data-stu-id="5d713-126">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="5d713-127">**NtGdiDdCreateDirectDrawObject**</span><span class="sxs-lookup"><span data-stu-id="5d713-127">**NtGdiDdCreateDirectDrawObject**</span></span>](-dxgkernel-ntgdiddcreatedirectdrawobject.md)
</dt> <dt>

[<span data-ttu-id="5d713-128">**DdDeleteDirectDrawObject**</span><span class="sxs-lookup"><span data-stu-id="5d713-128">**DdDeleteDirectDrawObject**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-dddeletedirectdrawobject)
</dt> </dl>

 

 
