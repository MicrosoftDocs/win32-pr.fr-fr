---
title: IVMMouse VerticalPosition, propriété (VPCCOMInterfaces. h)
description: Coordonnée y absolue de la souris.
ms.assetid: 02fd3677-95d8-44b4-b398-d3ec62e5d9f0
keywords:
- Propriété VerticalPosition Virtual PC
- Propriété VerticalPosition Virtual PC, interface IVMMouse
- IVMMouse interface Virtual PC, VerticalPosition, propriété
topic_type:
- apiref
api_name:
- IVMMouse.VerticalPosition
- IVMMouse.get_VerticalPosition
- IVMMouse.put_VerticalPosition
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64712f557a3fcd59181e8ce65d835b630da68e48
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942778"
---
# <a name="ivmmouseverticalposition-property"></a><span data-ttu-id="7f841-106">IVMMouse :: VerticalPosition, propriété</span><span class="sxs-lookup"><span data-stu-id="7f841-106">IVMMouse::VerticalPosition property</span></span>

<span data-ttu-id="7f841-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7f841-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7f841-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7f841-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7f841-109">Récupère la coordonnée y absolue de la souris.</span><span class="sxs-lookup"><span data-stu-id="7f841-109">Retrieves the absolute y-coordinate of the mouse.</span></span>

<span data-ttu-id="7f841-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="7f841-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f841-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7f841-111">Syntax</span></span>


```C++
HRESULT put_VerticalPosition(
  [in]          long position
);

HRESULT get_VerticalPosition(
  [out, retval] long *position
);
```



## <a name="property-value"></a><span data-ttu-id="7f841-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="7f841-112">Property value</span></span>

<span data-ttu-id="7f841-113">Coordonnée y indiquant la nouvelle position de la souris.</span><span class="sxs-lookup"><span data-stu-id="7f841-113">The y-coordinate indicating the new position of the mouse.</span></span> <span data-ttu-id="7f841-114">Lorsque vous utilisez des coordonnées absolues, cette valeur spécifie la nouvelle coordonnée y de la souris.</span><span class="sxs-lookup"><span data-stu-id="7f841-114">When using absolute coordinates, this value specifies the new y-coordinate of the mouse.</span></span> <span data-ttu-id="7f841-115">Lorsque vous utilisez des coordonnées relatives, cette valeur spécifie le nombre de pixels que la souris doit déplacer sur l’axe y.</span><span class="sxs-lookup"><span data-stu-id="7f841-115">When using relative coordinates, this value specifies the number of pixels the mouse should be moved in the y direction.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7f841-116">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="7f841-116">Error codes</span></span>



| <span data-ttu-id="7f841-117">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="7f841-117">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="7f841-118">Signification</span><span class="sxs-lookup"><span data-stu-id="7f841-118">Meaning</span></span>                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7f841-119"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7f841-119"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="7f841-120">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="7f841-120">The operation was successful.</span></span><br/>                                                                                                                |
| <dl> <span data-ttu-id="7f841-121"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="7f841-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="7f841-122">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="7f841-122">The parameter is **NULL**.</span></span><br/>                                                                                                                   |
| <dl> <span data-ttu-id="7f841-123"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="7f841-123"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="7f841-124">L’ordinateur virtuel auquel ce périphérique de souris est attaché n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="7f841-124">The virtual machine to which this mouse device is attached is not currently running.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="7f841-125"><dt>Ordinateur virtuel \_ La \_ fonctionnalité d’ajouts E \_ \_ n’est pas disponible \_ </dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="7f841-125"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="7f841-126">Les composants d’intégration doivent être installés pour récupérer la position de la souris ou définir la position de la souris lors de l’utilisation de coordonnées absolues.</span><span class="sxs-lookup"><span data-stu-id="7f841-126">Integration components must be installed to retrieve the mouse position, or to set the mouse position when using absolute coordinates.</span></span><br/>       |
| <dl> <span data-ttu-id="7f841-127"><dt>Ordinateur virtuel \_ E \_ utilisant \_ des \_ coordonnées relatives</dt> <dt>0xA0040802</dt></span><span class="sxs-lookup"><span data-stu-id="7f841-127"><dt>VM\_E\_USING\_RELATIVE\_COORDINATES</dt> <dt>0xA0040802</dt></span></span> </dl>   | <span data-ttu-id="7f841-128">Le périphérique souris est actuellement configuré pour utiliser des coordonnées de souris relatives.</span><span class="sxs-lookup"><span data-stu-id="7f841-128">The mouse device is currently set to use relative mouse coordinates.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="7f841-129"><dt>Ordinateur virtuel \_ E \_ souris \_ non \_ active</dt> <dt>0xA0040800</dt></span><span class="sxs-lookup"><span data-stu-id="7f841-129"><dt>VM\_E\_MOUSE\_NOT\_ACTIVE</dt> <dt>0xA0040800</dt></span></span> </dl>             | <span data-ttu-id="7f841-130">Les coordonnées absolues ne peuvent pas être récupérées si le périphérique de la souris n’est pas sous tension ou s’il n’est pas actuellement actif sur l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="7f841-130">The absolute coordinates cannot be retrieved if the mouse device is not powered up, or if it is not currently active in the virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="7f841-131"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="7f841-131"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="7f841-132">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="7f841-132">An unexpected error has occurred.</span></span><br/>                                                                                                            |



## <a name="remarks"></a><span data-ttu-id="7f841-133">Notes</span><span class="sxs-lookup"><span data-stu-id="7f841-133">Remarks</span></span>

<span data-ttu-id="7f841-134">Impossible de récupérer cette propriété lors de l’utilisation de coordonnées relatives.</span><span class="sxs-lookup"><span data-stu-id="7f841-134">This property cannot be retrieved when using relative coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f841-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7f841-135">Requirements</span></span>



| <span data-ttu-id="7f841-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7f841-136">Requirement</span></span> | <span data-ttu-id="7f841-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="7f841-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f841-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7f841-138">Minimum supported client</span></span><br/> | <span data-ttu-id="7f841-139">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7f841-139">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7f841-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7f841-140">Minimum supported server</span></span><br/> | <span data-ttu-id="7f841-141">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7f841-141">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7f841-142">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="7f841-142">End of client support</span></span><br/>    | <span data-ttu-id="7f841-143">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7f841-143">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7f841-144">Produit</span><span class="sxs-lookup"><span data-stu-id="7f841-144">Product</span></span><br/>                  | <span data-ttu-id="7f841-145">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7f841-145">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7f841-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="7f841-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f841-147"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f841-147"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="7f841-148">IID</span><span class="sxs-lookup"><span data-stu-id="7f841-148">IID</span></span><br/>                      | <span data-ttu-id="7f841-149">IID \_ IVMmouse est défini en tant que ac903f6d-6346-4f29-8875-5d511a13895e</span><span class="sxs-lookup"><span data-stu-id="7f841-149">IID\_IVMmouse is defined as ac903f6d-6346-4f29-8875-5d511a13895e</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="7f841-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f841-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f841-151">**IVMMouse**</span><span class="sxs-lookup"><span data-stu-id="7f841-151">**IVMMouse**</span></span>](ivmmouse.md)
</dt> </dl>

 

