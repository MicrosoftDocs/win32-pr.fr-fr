---
description: Provoque l’échange de la mémoire de surface associée aux surfaces cibles et actuelles.
ms.assetid: 2c557393-079e-48e5-b3a6-1157265d88e3
title: NtGdiDdFlip, fonction (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdFlip
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 1fd2d6f84f602fd07cc29a0efeae28209cb970a5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861097"
---
# <a name="ntgdiddflip-function"></a><span data-ttu-id="ef99a-103">NtGdiDdFlip fonction)</span><span class="sxs-lookup"><span data-stu-id="ef99a-103">NtGdiDdFlip function</span></span>

<span data-ttu-id="ef99a-104">\[Cette fonction est sujette à modification avec chaque révision du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="ef99a-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="ef99a-105">Utilisez plutôt Microsoft DirectDraw et Microsoft Direct3DAPIs ; Ces API isolent les applications de ces modifications du système d’exploitation et masquent de nombreuses autres difficultés liées à l’interaction directe avec les pilotes d’affichage.\]</span><span class="sxs-lookup"><span data-stu-id="ef99a-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="ef99a-106">Provoque l’échange de la mémoire de surface associée aux surfaces cibles et actuelles.</span><span class="sxs-lookup"><span data-stu-id="ef99a-106">Causes the surface memory associated with the target and current surfaces to be interchanged.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef99a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ef99a-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdFlip(
  _In_    HANDLE       hSurfaceCurrent,
  _In_    HANDLE       hSurfaceTarget,
  _In_    HANDLE       hSurfaceCurrentLeft,
  _In_    HANDLE       hSurfaceTargetLeft,
  _Inout_ PDD_FLIPDATA puFlipData
);
```



## <a name="parameters"></a><span data-ttu-id="ef99a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ef99a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef99a-109">*hSurfaceCurrent* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ef99a-109">*hSurfaceCurrent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef99a-110">Handle de la [structure \_ \_ locale de la surface DD](https://msdn.microsoft.com/library/ms793861.aspx) décrivant l’aire actuelle.</span><span class="sxs-lookup"><span data-stu-id="ef99a-110">Handle to the [DD\_SURFACE\_LOCAL](https://msdn.microsoft.com/library/ms793861.aspx) structure describing the current surface.</span></span>

</dd> <dt>

<span data-ttu-id="ef99a-111">*hSurfaceTarget* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ef99a-111">*hSurfaceTarget* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef99a-112">Handle de la [structure \_ \_ locale de la surface DD](https://msdn.microsoft.com/library/ms793861.aspx) décrivant la surface cible ; autrement dit, la surface vers laquelle le pilote doit retourner.</span><span class="sxs-lookup"><span data-stu-id="ef99a-112">Handle to the [DD\_SURFACE\_LOCAL](https://msdn.microsoft.com/library/ms793861.aspx) structure describing the target surface; that is, the surface to which the driver should flip.</span></span>

</dd> <dt>

<span data-ttu-id="ef99a-113">*hSurfaceCurrentLeft* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ef99a-113">*hSurfaceCurrentLeft* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef99a-114">Handle de la [structure \_ \_ locale de la surface DD](https://msdn.microsoft.com/library/ms793861.aspx) décrivant la surface gauche actuelle.</span><span class="sxs-lookup"><span data-stu-id="ef99a-114">Handle to the [DD\_SURFACE\_LOCAL](https://msdn.microsoft.com/library/ms793861.aspx) structure describing the current left surface.</span></span>

</dd> <dt>

<span data-ttu-id="ef99a-115">*hSurfaceTargetLeft* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ef99a-115">*hSurfaceTargetLeft* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef99a-116">Handle de la [structure \_ \_ locale de la surface DD](https://msdn.microsoft.com/library/ms793861.aspx) décrivant la surface cible gauche à retourner.</span><span class="sxs-lookup"><span data-stu-id="ef99a-116">Handle to the [DD\_SURFACE\_LOCAL](https://msdn.microsoft.com/library/ms793861.aspx) structure describing the left target surface to flip to.</span></span>

</dd> <dt>

<span data-ttu-id="ef99a-117">*puFlipData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ef99a-117">*puFlipData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef99a-118">Pointeur vers une [structure \_ FLIPDATA DD](https://msdn.microsoft.com/library/ms794213.aspx) qui contient les informations requises pour effectuer le retournement.</span><span class="sxs-lookup"><span data-stu-id="ef99a-118">Pointer to a [DD\_FLIPDATA](https://msdn.microsoft.com/library/ms794213.aspx) structure that contains the information required to perform the flip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef99a-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ef99a-119">Return value</span></span>

<span data-ttu-id="ef99a-120">**NtGdiDdFlip** retourne l’un des codes de rappel suivants.</span><span class="sxs-lookup"><span data-stu-id="ef99a-120">**NtGdiDdFlip** returns one of the following callback codes.</span></span>



| <span data-ttu-id="ef99a-121">Code de retour</span><span class="sxs-lookup"><span data-stu-id="ef99a-121">Return code</span></span>                                                                                              | <span data-ttu-id="ef99a-122">Description</span><span class="sxs-lookup"><span data-stu-id="ef99a-122">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ef99a-123"><dt>**\_pilote DDHAL \_ géré**</dt></span><span class="sxs-lookup"><span data-stu-id="ef99a-123"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="ef99a-124">Le pilote a effectué l’opération et a retourné un code de retour valide pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="ef99a-124">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="ef99a-125">Si ce code est JJ \_ OK, DirectDraw ou Direct3D continue avec la fonction.</span><span class="sxs-lookup"><span data-stu-id="ef99a-125">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="ef99a-126">Dans le cas contraire, DirectDraw ou Direct3D retourne le code d’erreur fourni par le pilote et abandonne la fonction.</span><span class="sxs-lookup"><span data-stu-id="ef99a-126">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="ef99a-127"><dt>**DDHAL de \_ pilote \_ NOTHANDLED**</dt></span><span class="sxs-lookup"><span data-stu-id="ef99a-127"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="ef99a-128">Le pilote n’a pas de commentaire sur l’opération demandée.</span><span class="sxs-lookup"><span data-stu-id="ef99a-128">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="ef99a-129">Si le pilote doit avoir implémenté un rappel particulier, DirectDraw ou Direct3D signale une condition d’erreur.</span><span class="sxs-lookup"><span data-stu-id="ef99a-129">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="ef99a-130">Dans le cas contraire, DirectDraw ou Direct3D gère l’opération comme si le rappel de pilote n’avait pas été défini par l’exécution de l’implémentation de DirectDraw ou de l’implémentation indépendante du périphérique Direct3D.</span><span class="sxs-lookup"><span data-stu-id="ef99a-130">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ef99a-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ef99a-131">Requirements</span></span>



| <span data-ttu-id="ef99a-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ef99a-132">Requirement</span></span> | <span data-ttu-id="ef99a-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef99a-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ef99a-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef99a-134">Minimum supported client</span></span><br/> | <span data-ttu-id="ef99a-135">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ef99a-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="ef99a-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef99a-136">Minimum supported server</span></span><br/> | <span data-ttu-id="ef99a-137">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ef99a-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ef99a-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="ef99a-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef99a-139"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef99a-139"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef99a-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef99a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef99a-141">Prise en charge des clients de bas niveau</span><span class="sxs-lookup"><span data-stu-id="ef99a-141">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




