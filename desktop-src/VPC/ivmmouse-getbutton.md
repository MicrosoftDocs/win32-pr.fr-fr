---
title: Méthode IVMMouse GetButton (VPCCOMInterfaces. h)
description: Récupère l’état actuel du bouton de la souris spécifié.
ms.assetid: eb534f88-387d-42fb-bfc3-bca17685021e
keywords:
- Méthode GetButton Virtual PC
- Méthode GetButton Virtual PC, interface IVMMouse
- IVMMouse interface Virtual PC, méthode GetButton
topic_type:
- apiref
api_name:
- IVMMouse.GetButton
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab73929a1fc9dfaa3942ed49f8a449343a594eec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743460"
---
# <a name="ivmmousegetbutton-method"></a><span data-ttu-id="6d4fe-106">IVMMouse :: GetButton, méthode</span><span class="sxs-lookup"><span data-stu-id="6d4fe-106">IVMMouse::GetButton method</span></span>

<span data-ttu-id="6d4fe-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6d4fe-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="6d4fe-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="6d4fe-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="6d4fe-109">Récupère l’état actuel (vers le haut ou vers le haut) du bouton spécifié de la souris.</span><span class="sxs-lookup"><span data-stu-id="6d4fe-109">Retrieves the current state (up or down) of the specified mouse button.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d4fe-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6d4fe-110">Syntax</span></span>


```C++
HRESULT GetButton(
  [in]          VMMouseButton buttonIndex,
  [out, retval] VARIANT_BOOL  *isDown
);
```



## <a name="parameters"></a><span data-ttu-id="6d4fe-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6d4fe-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d4fe-112">*buttonIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6d4fe-112">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d4fe-113">Index du bouton dont l’État est demandé.</span><span class="sxs-lookup"><span data-stu-id="6d4fe-113">The index of the button whose state is being requested.</span></span> <span data-ttu-id="6d4fe-114">Pour obtenir la liste des valeurs, consultez [**VMMouseButton**](vmmousebutton.md).</span><span class="sxs-lookup"><span data-stu-id="6d4fe-114">For a list of values, see [**VMMouseButton**](vmmousebutton.md).</span></span>

</dd> <dt>

<span data-ttu-id="6d4fe-115">*isDown* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="6d4fe-115">*isDown* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="6d4fe-116">État du bouton indiqué.</span><span class="sxs-lookup"><span data-stu-id="6d4fe-116">The state of the indicated button.</span></span> <span data-ttu-id="6d4fe-117">**True** si le bouton est actuellement enfoncé sur l’ordinateur virtuel ; sinon, **false** .</span><span class="sxs-lookup"><span data-stu-id="6d4fe-117">**TRUE** if the button is currently down in the virtual machine, **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d4fe-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6d4fe-118">Return value</span></span>

<span data-ttu-id="6d4fe-119">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="6d4fe-119">This method can return one of these values.</span></span>



| <span data-ttu-id="6d4fe-120">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="6d4fe-120">Return code/value</span></span>                                                                                                                                                        | <span data-ttu-id="6d4fe-121">Description</span><span class="sxs-lookup"><span data-stu-id="6d4fe-121">Description</span></span>                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6d4fe-122"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6d4fe-122"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                              | <span data-ttu-id="6d4fe-123">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="6d4fe-123">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="6d4fe-124"><dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="6d4fe-124"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                | <span data-ttu-id="6d4fe-125">Le paramètre *isDown* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="6d4fe-125">The *isDown* parameter is **NULL**.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="6d4fe-126"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="6d4fe-126"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>             | <span data-ttu-id="6d4fe-127">Le paramètre *buttonIndex* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="6d4fe-127">The *buttonIndex* parameter is not valid.</span></span><br/>                                            |
| <dl> <span data-ttu-id="6d4fe-128"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="6d4fe-128"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>   | <span data-ttu-id="6d4fe-129">L’ordinateur virtuel auquel ce périphérique de souris est attaché n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="6d4fe-129">The virtual machine to which this mouse device is attached is not currently running.</span></span><br/> |
| <dl> <span data-ttu-id="6d4fe-130"><dt>**Ordinateur virtuel \_ E \_ souris \_ non \_ active**</dt> <dt>0xA0040800</dt></span><span class="sxs-lookup"><span data-stu-id="6d4fe-130"><dt>**VM\_E\_MOUSE\_NOT\_ACTIVE**</dt> <dt>0xA0040800</dt></span></span> </dl> | <span data-ttu-id="6d4fe-131">Le périphérique souris n’a pas été mis sous tension.</span><span class="sxs-lookup"><span data-stu-id="6d4fe-131">The mouse device has not been powered up.</span></span><br/>                                            |
| <dl> <span data-ttu-id="6d4fe-132"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="6d4fe-132"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>        | <span data-ttu-id="6d4fe-133">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="6d4fe-133">An unexpected error has occurred.</span></span><br/>                                                    |



 

## <a name="requirements"></a><span data-ttu-id="6d4fe-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6d4fe-134">Requirements</span></span>



| <span data-ttu-id="6d4fe-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6d4fe-135">Requirement</span></span> | <span data-ttu-id="6d4fe-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="6d4fe-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d4fe-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d4fe-137">Minimum supported client</span></span><br/> | <span data-ttu-id="6d4fe-138">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6d4fe-138">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6d4fe-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d4fe-139">Minimum supported server</span></span><br/> | <span data-ttu-id="6d4fe-140">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d4fe-140">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="6d4fe-141">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="6d4fe-141">End of client support</span></span><br/>    | <span data-ttu-id="6d4fe-142">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6d4fe-142">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="6d4fe-143">Produit</span><span class="sxs-lookup"><span data-stu-id="6d4fe-143">Product</span></span><br/>                  | <span data-ttu-id="6d4fe-144">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="6d4fe-144">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="6d4fe-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="6d4fe-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d4fe-146"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d4fe-146"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="6d4fe-147">IID</span><span class="sxs-lookup"><span data-stu-id="6d4fe-147">IID</span></span><br/>                      | <span data-ttu-id="6d4fe-148">IID \_ IVMmouse est défini en tant que ac903f6d-6346-4f29-8875-5d511a13895e</span><span class="sxs-lookup"><span data-stu-id="6d4fe-148">IID\_IVMmouse is defined as ac903f6d-6346-4f29-8875-5d511a13895e</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="6d4fe-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6d4fe-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d4fe-150">**IVMMouse**</span><span class="sxs-lookup"><span data-stu-id="6d4fe-150">**IVMMouse**</span></span>](ivmmouse.md)
</dt> </dl>

 

