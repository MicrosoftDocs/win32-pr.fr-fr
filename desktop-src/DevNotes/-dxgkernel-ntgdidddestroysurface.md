---
description: Détruit un objet surface Microsoft DirectDraw précédemment alloué en mode noyau.
ms.assetid: 65419fce-9e82-4621-9906-832144888a3b
title: NtGdiDdDestroySurface, fonction (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdDestroySurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 54799aa90007370439b2be8c8cf8c1f584360a5d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033679"
---
# <a name="ntgdidddestroysurface-function"></a><span data-ttu-id="fe470-103">NtGdiDdDestroySurface fonction)</span><span class="sxs-lookup"><span data-stu-id="fe470-103">NtGdiDdDestroySurface function</span></span>

<span data-ttu-id="fe470-104">\[Cette fonction est sujette à modification avec chaque révision du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="fe470-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="fe470-105">Utilisez à la place DirectDraw et Microsoft Direct3DAPIs ; Ces API isolent les applications de ces modifications du système d’exploitation et masquent de nombreuses autres difficultés liées à l’interaction directe avec les pilotes d’affichage.\]</span><span class="sxs-lookup"><span data-stu-id="fe470-105">Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="fe470-106">Détruit un objet surface Microsoft DirectDraw précédemment alloué en mode noyau.</span><span class="sxs-lookup"><span data-stu-id="fe470-106">Destroys a previously allocated kernel-mode Microsoft DirectDraw surface object.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe470-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fe470-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdDestroySurface(
  _In_ HANDLE hSurface,
  _In_ BOOL   bRealDestroy
);
```



## <a name="parameters"></a><span data-ttu-id="fe470-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fe470-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe470-109">*hSurface* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fe470-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe470-110">Handle vers l’objet surface en mode noyau précédemment alloué.</span><span class="sxs-lookup"><span data-stu-id="fe470-110">Handle to previously allocated kernel-mode surface object.</span></span>

</dd> <dt>

<span data-ttu-id="fe470-111">*bRealDestroy* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fe470-111">*bRealDestroy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe470-112">Spécifie comment détruire l’aire.</span><span class="sxs-lookup"><span data-stu-id="fe470-112">Specifies how to destroy the surface.</span></span> <span data-ttu-id="fe470-113">Il peut s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="fe470-113">Can be one of the following values.</span></span>

<dt>



 <span data-ttu-id="fe470-114">:</span><span class="sxs-lookup"><span data-stu-id="fe470-114">(TRUE)</span></span>


</dt> <dd>

<span data-ttu-id="fe470-115">Détruisez la surface et la mémoire vidéo libre.</span><span class="sxs-lookup"><span data-stu-id="fe470-115">Destroy the surface and free video memory.</span></span>

</dd> <dt>



 <span data-ttu-id="fe470-116">FAUSSES</span><span class="sxs-lookup"><span data-stu-id="fe470-116">(FALSE)</span></span>


</dt> <dd>

<span data-ttu-id="fe470-117">Libérez de la mémoire vidéo tout en laissant la surface dans un État non initialisé.</span><span class="sxs-lookup"><span data-stu-id="fe470-117">Free the video memory but leave the surface in an uninitialized state.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe470-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fe470-118">Return value</span></span>

<span data-ttu-id="fe470-119">**NtGdiDdDestroySurface** retourne l’un des codes de rappel suivants.</span><span class="sxs-lookup"><span data-stu-id="fe470-119">**NtGdiDdDestroySurface** returns one of the following callback codes.</span></span>



| <span data-ttu-id="fe470-120">Code de retour</span><span class="sxs-lookup"><span data-stu-id="fe470-120">Return code</span></span>                                                                                              | <span data-ttu-id="fe470-121">Description</span><span class="sxs-lookup"><span data-stu-id="fe470-121">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fe470-122"><dt>**\_pilote DDHAL \_ géré**</dt></span><span class="sxs-lookup"><span data-stu-id="fe470-122"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="fe470-123">Le pilote a effectué l’opération et a retourné un code de retour valide pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="fe470-123">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="fe470-124">Si ce code est JJ \_ OK, DirectDraw ou Direct3D continue avec la fonction.</span><span class="sxs-lookup"><span data-stu-id="fe470-124">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="fe470-125">Dans le cas contraire, DirectDraw ou Direct3D retourne le code d’erreur fourni par le pilote et abandonne la fonction.</span><span class="sxs-lookup"><span data-stu-id="fe470-125">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="fe470-126"><dt>**DDHAL de \_ pilote \_ NOTHANDLED**</dt></span><span class="sxs-lookup"><span data-stu-id="fe470-126"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="fe470-127">Le pilote n’a pas de commentaire sur l’opération demandée.</span><span class="sxs-lookup"><span data-stu-id="fe470-127">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="fe470-128">Si le pilote doit avoir implémenté un rappel particulier, DirectDraw ou Direct3D signale une condition d’erreur.</span><span class="sxs-lookup"><span data-stu-id="fe470-128">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="fe470-129">Dans le cas contraire, DirectDraw ou Direct3D gère l’opération comme si le rappel de pilote n’avait pas été défini par l’exécution de l’implémentation de DirectDraw ou de l’implémentation indépendante du périphérique Direct3D.</span><span class="sxs-lookup"><span data-stu-id="fe470-129">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fe470-130">Notes</span><span class="sxs-lookup"><span data-stu-id="fe470-130">Remarks</span></span>

<span data-ttu-id="fe470-131">Il est recommandé que les applications utilisent les API DirectDraw et Direct3D pour créer et détruire des surfaces au lieu de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="fe470-131">It is recommended that applications use the DirectDraw and Direct3D APIs to create and destroy surfaces instead of this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe470-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fe470-132">Requirements</span></span>



| <span data-ttu-id="fe470-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fe470-133">Requirement</span></span> | <span data-ttu-id="fe470-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="fe470-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fe470-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fe470-135">Minimum supported client</span></span><br/> | <span data-ttu-id="fe470-136">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fe470-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="fe470-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fe470-137">Minimum supported server</span></span><br/> | <span data-ttu-id="fe470-138">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fe470-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="fe470-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="fe470-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe470-140"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe470-140"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe470-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fe470-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe470-142">Prise en charge des clients de bas niveau</span><span class="sxs-lookup"><span data-stu-id="fe470-142">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




