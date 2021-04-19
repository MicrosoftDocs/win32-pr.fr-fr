---
description: Attache deux représentations de surface en mode noyau.
ms.assetid: f1b1859f-8b62-4385-9e8a-296086446fe7
title: NtGdiDdAttachSurface, fonction (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdAttachSurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: a3d099e7b3a3106e0e1e4285b37d2ea205baf3d5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106545768"
---
# <a name="ntgdiddattachsurface-function"></a><span data-ttu-id="088ce-103">NtGdiDdAttachSurface fonction)</span><span class="sxs-lookup"><span data-stu-id="088ce-103">NtGdiDdAttachSurface function</span></span>

<span data-ttu-id="088ce-104">\[Cette fonction est sujette à modification avec chaque révision du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="088ce-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="088ce-105">Utilisez plutôt Microsoft DirectDraw et Microsoft Direct3DAPIs ; Ces API isolent les applications de ces modifications du système d’exploitation et masquent de nombreuses autres difficultés liées à l’interaction directe avec les pilotes d’affichage.\]</span><span class="sxs-lookup"><span data-stu-id="088ce-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="088ce-106">Attache deux représentations de surface en mode noyau.</span><span class="sxs-lookup"><span data-stu-id="088ce-106">Attaches two kernel-mode surface representations.</span></span>

## <a name="syntax"></a><span data-ttu-id="088ce-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="088ce-107">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiDdAttachSurface(
  _In_ HANDLE hSurfaceFrom,
  _In_ HANDLE hSurfaceTo
);
```



## <a name="parameters"></a><span data-ttu-id="088ce-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="088ce-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="088ce-109">*hSurfaceFrom* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="088ce-109">*hSurfaceFrom* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="088ce-110">Handle vers l’objet surface en mode noyau qui sera le point de départ de la nouvelle pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="088ce-110">Handle to kernel-mode surface object that will be the start point of the new attachment.</span></span>

</dd> <dt>

<span data-ttu-id="088ce-111">*hSurfaceTo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="088ce-111">*hSurfaceTo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="088ce-112">Handle vers l’objet surface en mode noyau qui sera le point de terminaison de la nouvelle pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="088ce-112">Handle to kernel-mode surface object that will be the end point of the new attachment.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="088ce-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="088ce-113">Return value</span></span>

<span data-ttu-id="088ce-114">**NtGdiDdAttachSurface** retourne l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="088ce-114">**NtGdiDdAttachSurface** returns one of the following:</span></span>



| <span data-ttu-id="088ce-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="088ce-115">Return code</span></span>                                                                          | <span data-ttu-id="088ce-116">Description</span><span class="sxs-lookup"><span data-stu-id="088ce-116">Description</span></span>                             |
|--------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="088ce-117"><dt>**:**</dt></span><span class="sxs-lookup"><span data-stu-id="088ce-117"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="088ce-118">L’appel de fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="088ce-118">The function call succeeded.</span></span><br/> |
| <dl> <span data-ttu-id="088ce-119"><dt>**FAUSSES**</dt></span><span class="sxs-lookup"><span data-stu-id="088ce-119"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="088ce-120">L’appel de fonction a échoué.</span><span class="sxs-lookup"><span data-stu-id="088ce-120">The function call failed.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="088ce-121">Notes</span><span class="sxs-lookup"><span data-stu-id="088ce-121">Remarks</span></span>

<span data-ttu-id="088ce-122">Pour obtenir une description complète des pièces jointes, consultez le kit de développement logiciel (SDK) et le kit de développement de pilotes (DDK) DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="088ce-122">See the DirectDraw  software development kit (SDK) and Driver Development Kit (DDK) for a full description of surface attachments.</span></span>

> [!Note]  
> <span data-ttu-id="088ce-123">Comme pour les autres pièces jointes de surface, la pièce jointe résultante est unidirectionnelle.</span><span class="sxs-lookup"><span data-stu-id="088ce-123">As with other surface attachments, the resulting attachment is one-way.</span></span> <span data-ttu-id="088ce-124">Une fois cette fonction appelée, *hSurfaceTo* n’est pas attaché à *hSurfaceFrom*.</span><span class="sxs-lookup"><span data-stu-id="088ce-124">After this function is called, *hSurfaceTo* will not be attached to *hSurfaceFrom*.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="088ce-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="088ce-125">Requirements</span></span>



| <span data-ttu-id="088ce-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="088ce-126">Requirement</span></span> | <span data-ttu-id="088ce-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="088ce-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="088ce-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="088ce-128">Minimum supported client</span></span><br/> | <span data-ttu-id="088ce-129">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="088ce-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="088ce-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="088ce-130">Minimum supported server</span></span><br/> | <span data-ttu-id="088ce-131">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="088ce-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="088ce-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="088ce-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="088ce-133"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="088ce-133"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="088ce-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="088ce-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="088ce-135">Prise en charge des clients de bas niveau</span><span class="sxs-lookup"><span data-stu-id="088ce-135">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




