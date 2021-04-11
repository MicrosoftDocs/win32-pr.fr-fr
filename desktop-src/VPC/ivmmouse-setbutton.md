---
title: Méthode IVMMouse SetButton (VPCCOMInterfaces. h)
description: Définit l’état actuel (vers le haut ou vers le haut) du bouton spécifié de la souris.
ms.assetid: 52b24472-68d6-4a42-8ae5-b1434a6d67f3
keywords:
- Méthode SetButton Virtual PC
- Méthode SetButton Virtual PC, interface IVMMouse
- IVMMouse interface Virtual PC, méthode SetButton
topic_type:
- apiref
api_name:
- IVMMouse.SetButton
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2d30ae131ac33eeff339b98511fd2da60a1e606
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105676"
---
# <a name="ivmmousesetbutton-method"></a><span data-ttu-id="b0751-106">IVMMouse :: SetButton, méthode</span><span class="sxs-lookup"><span data-stu-id="b0751-106">IVMMouse::SetButton method</span></span>

<span data-ttu-id="b0751-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b0751-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b0751-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b0751-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b0751-109">Définit l’état actuel (vers le haut ou vers le haut) du bouton spécifié de la souris.</span><span class="sxs-lookup"><span data-stu-id="b0751-109">Sets the current state (up or down) of the specified mouse button.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0751-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b0751-110">Syntax</span></span>


```C++
HRESULT SetButton(
  [in] VMMouseButton buttonIndex,
  [in] VARIANT_BOOL  down
);
```



## <a name="parameters"></a><span data-ttu-id="b0751-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b0751-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0751-112">*buttonIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b0751-112">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0751-113">Index du bouton.</span><span class="sxs-lookup"><span data-stu-id="b0751-113">The button index.</span></span> <span data-ttu-id="b0751-114">Pour obtenir la liste des valeurs, consultez [**VMMouseButton**](vmmousebutton.md).</span><span class="sxs-lookup"><span data-stu-id="b0751-114">For a list of values, see [**VMMouseButton**](vmmousebutton.md).</span></span>

</dd> <dt>

<span data-ttu-id="b0751-115">*vers le* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b0751-115">*down* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0751-116">Nouvel État du bouton.</span><span class="sxs-lookup"><span data-stu-id="b0751-116">The new button state.</span></span> <span data-ttu-id="b0751-117">Utilisez **true** si l’état du bouton doit être défini sur inactif et **false** s’il doit être défini sur up.</span><span class="sxs-lookup"><span data-stu-id="b0751-117">Use **TRUE** if the button state is to be set to down, and **FALSE** if it is to be set to up.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0751-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b0751-118">Return value</span></span>

<span data-ttu-id="b0751-119">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="b0751-119">This method can return one of these values.</span></span>



| <span data-ttu-id="b0751-120">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="b0751-120">Return code/value</span></span>                                                                                                                                                        | <span data-ttu-id="b0751-121">Description</span><span class="sxs-lookup"><span data-stu-id="b0751-121">Description</span></span>                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b0751-122"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b0751-122"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                              | <span data-ttu-id="b0751-123">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="b0751-123">The operation was successful.</span></span><br/>                                                                                                          |
| <dl> <span data-ttu-id="b0751-124"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="b0751-124"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>             | <span data-ttu-id="b0751-125">Le paramètre *buttonIndex* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="b0751-125">The *buttonIndex* parameter is not valid.</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="b0751-126"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="b0751-126"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>   | <span data-ttu-id="b0751-127">L’ordinateur virtuel auquel ce périphérique de souris est attaché n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="b0751-127">The virtual machine to which this mouse device is attached is not currently running.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="b0751-128"><dt>**Ordinateur virtuel \_ E \_ souris \_ non \_ active**</dt> <dt>0xA0040800</dt></span><span class="sxs-lookup"><span data-stu-id="b0751-128"><dt>**VM\_E\_MOUSE\_NOT\_ACTIVE**</dt> <dt>0xA0040800</dt></span></span> </dl> | <span data-ttu-id="b0751-129">L’opération n’a pas pu aboutir car le périphérique de la souris n’est pas sous tension ou n’est pas actuellement actif sur la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="b0751-129">The operation could not be completed because the mouse device is not powered up, or it is not currently active in the virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="b0751-130"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="b0751-130"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>        | <span data-ttu-id="b0751-131">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="b0751-131">An unexpected error has occurred.</span></span><br/>                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="b0751-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b0751-132">Requirements</span></span>



| <span data-ttu-id="b0751-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b0751-133">Requirement</span></span> | <span data-ttu-id="b0751-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="b0751-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0751-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b0751-135">Minimum supported client</span></span><br/> | <span data-ttu-id="b0751-136">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b0751-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b0751-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b0751-137">Minimum supported server</span></span><br/> | <span data-ttu-id="b0751-138">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b0751-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b0751-139">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="b0751-139">End of client support</span></span><br/>    | <span data-ttu-id="b0751-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b0751-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b0751-141">Produit</span><span class="sxs-lookup"><span data-stu-id="b0751-141">Product</span></span><br/>                  | <span data-ttu-id="b0751-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b0751-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b0751-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="b0751-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0751-144"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0751-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b0751-145">IID</span><span class="sxs-lookup"><span data-stu-id="b0751-145">IID</span></span><br/>                      | <span data-ttu-id="b0751-146">IID \_ IVMmouse est défini en tant que ac903f6d-6346-4f29-8875-5d511a13895e</span><span class="sxs-lookup"><span data-stu-id="b0751-146">IID\_IVMmouse is defined as ac903f6d-6346-4f29-8875-5d511a13895e</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="b0751-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b0751-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0751-148">**IVMMouse**</span><span class="sxs-lookup"><span data-stu-id="b0751-148">**IVMMouse**</span></span>](ivmmouse.md)
</dt> </dl>

 

