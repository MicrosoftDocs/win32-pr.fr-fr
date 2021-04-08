---
title: IVMMouse ScrollWheelPosition, propriété (VPCCOMInterfaces. h)
description: Ajuste la coordonnée z de la souris (relative uniquement).
ms.assetid: 52269d0c-a7a8-4dc2-bb27-c891d1e9c293
keywords:
- ScrollWheelPosition propriété Virtual PC
- ScrollWheelPosition, propriété Virtual PC, IVMMouse, interface
- IVMMouse interface Virtual PC, propriété ScrollWheelPosition
topic_type:
- apiref
api_name:
- IVMMouse.ScrollWheelPosition
- IVMMouse.put_ScrollWheelPosition
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e374011dc87ad00d4edef1f33e9787d5a2e6d787
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743453"
---
# <a name="ivmmousescrollwheelposition-property"></a><span data-ttu-id="c2a10-106">IVMMouse :: ScrollWheelPosition, propriété</span><span class="sxs-lookup"><span data-stu-id="c2a10-106">IVMMouse::ScrollWheelPosition property</span></span>

<span data-ttu-id="c2a10-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c2a10-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c2a10-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c2a10-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c2a10-109">Ajuste la coordonnée z de la souris (relative uniquement).</span><span class="sxs-lookup"><span data-stu-id="c2a10-109">Adjusts the z-coordinate of the mouse (relative only).</span></span>

<span data-ttu-id="c2a10-110">Cette propriété est en écriture seule.</span><span class="sxs-lookup"><span data-stu-id="c2a10-110">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2a10-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c2a10-111">Syntax</span></span>


```C++
HRESULT put_ScrollWheelPosition(
  [in] long position
);
```



## <a name="property-value"></a><span data-ttu-id="c2a10-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="c2a10-112">Property value</span></span>

<span data-ttu-id="c2a10-113">Coordonnée z qui indique le nombre de pixels que la souris doit déplacer le long de l’axe z.</span><span class="sxs-lookup"><span data-stu-id="c2a10-113">The z-coordinate indicating the number of pixels the mouse is to be moved along the z-axis.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c2a10-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="c2a10-114">Error codes</span></span>



| <span data-ttu-id="c2a10-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="c2a10-115">Name/value</span></span>                                                                                                                                                                     | <span data-ttu-id="c2a10-116">Signification</span><span class="sxs-lookup"><span data-stu-id="c2a10-116">Meaning</span></span>                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c2a10-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c2a10-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                        | <span data-ttu-id="c2a10-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="c2a10-118">The operation was successful.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="c2a10-119"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="c2a10-119"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>             | <span data-ttu-id="c2a10-120">L’ordinateur virtuel auquel ce périphérique de souris est attaché n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="c2a10-120">The virtual machine to which this mouse device is attached is not currently running.</span></span><br/>         |
| <dl> <span data-ttu-id="c2a10-121"><dt>Ordinateur virtuel \_ E \_ souris \_ non \_ active</dt> <dt>0xA0040800</dt></span><span class="sxs-lookup"><span data-stu-id="c2a10-121"><dt>VM\_E\_MOUSE\_NOT\_ACTIVE</dt> <dt>0xA0040800</dt></span></span> </dl>           | <span data-ttu-id="c2a10-122">Le périphérique de la souris n’a pas été mis sous tension ou n’est pas actuellement actif sur la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="c2a10-122">The mouse device has not been powered up, or is not currently active in the virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="c2a10-123"><dt>Ordinateur virtuel \_ E \_ utilisant \_ des \_ coordonnées absolues</dt> <dt>0xA0040801</dt></span><span class="sxs-lookup"><span data-stu-id="c2a10-123"><dt>VM\_E\_USING\_ABSOLUTE\_COORDINATES</dt> <dt>0xA0040801</dt></span></span> </dl> | <span data-ttu-id="c2a10-124">La position de la roulette de défilement ne peut pas être définie lorsque le périphérique de la souris utilise des coordonnées absolues.</span><span class="sxs-lookup"><span data-stu-id="c2a10-124">The scroll wheel position cannot be set when the mouse device is using absolute coordinates.</span></span><br/> |
| <dl> <span data-ttu-id="c2a10-125"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="c2a10-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                  | <span data-ttu-id="c2a10-126">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="c2a10-126">An unexpected error has occurred.</span></span><br/>                                                            |



## <a name="requirements"></a><span data-ttu-id="c2a10-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c2a10-127">Requirements</span></span>



| <span data-ttu-id="c2a10-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c2a10-128">Requirement</span></span> | <span data-ttu-id="c2a10-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2a10-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2a10-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2a10-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c2a10-131">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c2a10-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c2a10-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2a10-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c2a10-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2a10-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c2a10-134">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="c2a10-134">End of client support</span></span><br/>    | <span data-ttu-id="c2a10-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c2a10-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c2a10-136">Produit</span><span class="sxs-lookup"><span data-stu-id="c2a10-136">Product</span></span><br/>                  | <span data-ttu-id="c2a10-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c2a10-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c2a10-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="c2a10-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2a10-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2a10-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c2a10-140">IID</span><span class="sxs-lookup"><span data-stu-id="c2a10-140">IID</span></span><br/>                      | <span data-ttu-id="c2a10-141">IID \_ IVMmouse est défini en tant que ac903f6d-6346-4f29-8875-5d511a13895e</span><span class="sxs-lookup"><span data-stu-id="c2a10-141">IID\_IVMmouse is defined as ac903f6d-6346-4f29-8875-5d511a13895e</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="c2a10-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c2a10-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2a10-143">**IVMMouse**</span><span class="sxs-lookup"><span data-stu-id="c2a10-143">**IVMMouse**</span></span>](ivmmouse.md)
</dt> </dl>

 

