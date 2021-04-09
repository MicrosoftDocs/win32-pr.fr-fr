---
description: Supprime une pièce jointe, créée avec NtGdiDdAttachSurface, entre deux objets surface en mode noyau.
ms.assetid: 28037b42-a00c-4063-93ee-5d71761a95d8
title: NtGdiDdUnattachSurface, fonction (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdUnattachSurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 4513020a40c9b704e0b84e1a8b1c582be95db78f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950434"
---
# <a name="ntgdiddunattachsurface-function"></a><span data-ttu-id="f99e2-103">NtGdiDdUnattachSurface fonction)</span><span class="sxs-lookup"><span data-stu-id="f99e2-103">NtGdiDdUnattachSurface function</span></span>

<span data-ttu-id="f99e2-104">\[Cette fonction est sujette à modification avec chaque révision du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="f99e2-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="f99e2-105">Utilisez plutôt Microsoft DirectDraw et Microsoft Direct3DAPIs ; Ces API isolent les applications de ces modifications du système d’exploitation et masquent de nombreuses autres difficultés liées à l’interaction directe avec les pilotes d’affichage.\]</span><span class="sxs-lookup"><span data-stu-id="f99e2-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="f99e2-106">Supprime une pièce jointe, créée avec [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md), entre deux objets surface en mode noyau.</span><span class="sxs-lookup"><span data-stu-id="f99e2-106">Removes an attachment, created with [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md), between two kernel-mode surface objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="f99e2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f99e2-107">Syntax</span></span>


```C++
VOID APIENTRY NtGdiDdUnattachSurface(
  _In_ HANDLE hSurface,
  _In_ HANDLE hSurfaceAttached
);
```



## <a name="parameters"></a><span data-ttu-id="f99e2-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f99e2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f99e2-109">*hSurface* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f99e2-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f99e2-110">Objet surface en mode noyau qui a été passé en tant que paramètre hSurfaceFrom à [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md).</span><span class="sxs-lookup"><span data-stu-id="f99e2-110">The kernel-mode surface object that was passed as the hSurfaceFrom parameter to [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md).</span></span>

</dd> <dt>

<span data-ttu-id="f99e2-111">*hSurfaceAttached* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f99e2-111">*hSurfaceAttached* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f99e2-112">Objet surface en mode noyau qui a été passé en tant que paramètre hSurfaceTo à [ **NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md)</span><span class="sxs-lookup"><span data-stu-id="f99e2-112">The kernel-mode surface object that was passed as the hSurfaceTo parameter to [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f99e2-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f99e2-113">Return value</span></span>

<span data-ttu-id="f99e2-114">**NtGdiDdUnattachSurface** retourne l’un des codes de rappel suivants.</span><span class="sxs-lookup"><span data-stu-id="f99e2-114">**NtGdiDdUnattachSurface** returns one of the following callback codes.</span></span>



| <span data-ttu-id="f99e2-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="f99e2-115">Return code</span></span>                                                                                              | <span data-ttu-id="f99e2-116">Description</span><span class="sxs-lookup"><span data-stu-id="f99e2-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f99e2-117"><dt>**\_pilote DDHAL \_ géré**</dt></span><span class="sxs-lookup"><span data-stu-id="f99e2-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="f99e2-118">Le pilote a effectué l’opération et a retourné un code de retour valide pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="f99e2-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="f99e2-119">Si ce code est JJ \_ OK, DirectDraw ou Direct3D continue avec la fonction.</span><span class="sxs-lookup"><span data-stu-id="f99e2-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="f99e2-120">Dans le cas contraire, DirectDraw ou Direct3D retourne le code d’erreur fourni par le pilote et abandonne la fonction.</span><span class="sxs-lookup"><span data-stu-id="f99e2-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="f99e2-121"><dt>**DDHAL de \_ pilote \_ NOTHANDLED**</dt></span><span class="sxs-lookup"><span data-stu-id="f99e2-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="f99e2-122">Le pilote n’a pas de commentaire sur l’opération demandée.</span><span class="sxs-lookup"><span data-stu-id="f99e2-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="f99e2-123">Si le pilote doit avoir implémenté un rappel particulier, DirectDraw ou Direct3D signale une condition d’erreur.</span><span class="sxs-lookup"><span data-stu-id="f99e2-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="f99e2-124">Dans le cas contraire, DirectDraw ou Direct3D gère l’opération comme si le rappel de pilote n’avait pas été défini par l’exécution de l’implémentation de DirectDraw ou de l’implémentation indépendante du périphérique Direct3D.</span><span class="sxs-lookup"><span data-stu-id="f99e2-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f99e2-125">Notes</span><span class="sxs-lookup"><span data-stu-id="f99e2-125">Remarks</span></span>

<span data-ttu-id="f99e2-126">Il est recommandé que les applications utilisent l’API DirectDraw, qui gère les pièces jointes de surface de manière plus détaillée.</span><span class="sxs-lookup"><span data-stu-id="f99e2-126">It is recommended that applications use the DirectDraw  API, which handles surface attachments in a higher-level manner.</span></span>

<span data-ttu-id="f99e2-127">Il n’est pas nécessaire d’appeler cette fonction, car le noyau détruit automatiquement toutes les pièces jointes lorsque [**NtGdiDdDestroySurface**](-dxgkernel-ntgdidddestroysurface.md) est appelé.</span><span class="sxs-lookup"><span data-stu-id="f99e2-127">It is not necessary to call this function because the kernel will automatically destroy all attachments when [**NtGdiDdDestroySurface**](-dxgkernel-ntgdidddestroysurface.md) is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="f99e2-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f99e2-128">Requirements</span></span>



| <span data-ttu-id="f99e2-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f99e2-129">Requirement</span></span> | <span data-ttu-id="f99e2-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="f99e2-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f99e2-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f99e2-131">Minimum supported client</span></span><br/> | <span data-ttu-id="f99e2-132">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f99e2-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="f99e2-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f99e2-133">Minimum supported server</span></span><br/> | <span data-ttu-id="f99e2-134">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f99e2-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f99e2-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="f99e2-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="f99e2-136"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f99e2-136"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f99e2-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f99e2-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f99e2-138">Prise en charge des clients de bas niveau</span><span class="sxs-lookup"><span data-stu-id="f99e2-138">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




