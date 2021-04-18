---
title: Méthode IVMGuestOS IsUserLoggedOn (VPCCOMInterfaces. h)
description: Détermine si la session demandée est présente.
ms.assetid: 28035e30-023a-4ec2-88ef-43fe22f6d14e
keywords:
- Méthode IsUserLoggedOn Virtual PC
- Méthode IsUserLoggedOn Virtual PC, interface IVMGuestOS
- IVMGuestOS interface Virtual PC, méthode IsUserLoggedOn
topic_type:
- apiref
api_name:
- IVMGuestOS.IsUserLoggedOn
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4eeb0482d7d3ac45b67a863948526b57d6c6e412
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106527155"
---
# <a name="ivmguestosisuserloggedon-method"></a><span data-ttu-id="e5216-106">IVMGuestOS :: IsUserLoggedOn, méthode</span><span class="sxs-lookup"><span data-stu-id="e5216-106">IVMGuestOS::IsUserLoggedOn method</span></span>

<span data-ttu-id="e5216-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e5216-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e5216-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e5216-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e5216-109">Détermine si la session demandée est présente.</span><span class="sxs-lookup"><span data-stu-id="e5216-109">Determines whether the requested session is present.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5216-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e5216-110">Syntax</span></span>


```C++
HRESULT IsUserLoggedOn(
  [in]          long         inRailSession,
  [out, retval] VARIANT_BOOL *outSessionPresent
);
```



## <a name="parameters"></a><span data-ttu-id="e5216-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e5216-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5216-112">*inRailSession* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e5216-112">*inRailSession* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5216-113">Définissez la valeur 0 pour une session de rail ou 1 pour une session RDP.</span><span class="sxs-lookup"><span data-stu-id="e5216-113">Set to 0 for a Rail session or 1 for an RDP session.</span></span>

</dd> <dt>

<span data-ttu-id="e5216-114">*outSessionPresent* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="e5216-114">*outSessionPresent* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="e5216-115">A la valeur **Variant \_ true** si la session est présente **et \_ false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="e5216-115">Set to **VARIANT\_TRUE** if the session is present and **VARIANT\_FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5216-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e5216-116">Return value</span></span>

<span data-ttu-id="e5216-117">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="e5216-117">This method can return one of these values.</span></span>



| <span data-ttu-id="e5216-118">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="e5216-118">Return code/value</span></span>                                                                                                                                                                       | <span data-ttu-id="e5216-119">Description</span><span class="sxs-lookup"><span data-stu-id="e5216-119">Description</span></span>                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e5216-120"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e5216-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                             | <span data-ttu-id="e5216-121">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="e5216-121">The operation was successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="e5216-122"><dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="e5216-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                               | <span data-ttu-id="e5216-123">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="e5216-123">The parameter is **NULL**.</span></span><br/>                                      |
| <dl> <span data-ttu-id="e5216-124"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="e5216-124"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                            | <span data-ttu-id="e5216-125">Le paramètre *outSessionPresent* n’est pas valide ou a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="e5216-125">The *outSessionPresent* parameter is not valid or is **NULL**.</span></span><br/>  |
| <dl> <span data-ttu-id="e5216-126"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="e5216-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                       | <span data-ttu-id="e5216-127">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="e5216-127">An unexpected error has occurred.</span></span><br/>                               |
| <dl> <span data-ttu-id="e5216-128">Valeur <dt>**HRESULT \_ À partir de \_ Win32 (erreur \_ OUTOFMEMORY)**</dt> <dt>0x8007000E</dt></span><span class="sxs-lookup"><span data-stu-id="e5216-128"><dt>**HRESULT\_FROM\_WIN32(ERROR\_OUTOFMEMORY)**</dt> <dt>0x8007000e</dt></span></span> </dl> | <span data-ttu-id="e5216-129">La mémoire disponible est insuffisante pour effectuer cette requête.</span><span class="sxs-lookup"><span data-stu-id="e5216-129">There is not enough memory available to complete this request.</span></span><br/>  |
| <dl> <span data-ttu-id="e5216-130"><dt>**Ordinateur virtuel \_ E \_ a \_ expiré**</dt> <dt>0xA0040202</dt></span><span class="sxs-lookup"><span data-stu-id="e5216-130"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                        | <span data-ttu-id="e5216-131">L’opération ne s’est pas terminée en temps opportun.</span><span class="sxs-lookup"><span data-stu-id="e5216-131">The operation did not complete in a timely manner.</span></span><br/>              |
| <dl> <span data-ttu-id="e5216-132"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="e5216-132"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                  | <span data-ttu-id="e5216-133">L’ordinateur virtuel (VM) doit être en cours d’exécution pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="e5216-133">The virtual machine (VM) must be running for this operation.</span></span><br/>    |
| <dl> <span data-ttu-id="e5216-134"><dt>**Ordinateur virtuel \_ La \_ fonctionnalité d’ajouts E \_ \_ n’est pas disponible \_**</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="e5216-134"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl>    | <span data-ttu-id="e5216-135">La fonctionnalité composants d’intégration n’est pas installée sur cette machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="e5216-135">The integration components feature is not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="e5216-136"><dt>**Ordinateur virtuel \_ 0xA00400507 \_ en \_ pause de la machine virtuelle E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="e5216-136"><dt>**VM\_E\_VM\_PAUSED**</dt> <dt>0xA00400507</dt></span></span> </dl>                       | <span data-ttu-id="e5216-137">La machine virtuelle est suspendue.</span><span class="sxs-lookup"><span data-stu-id="e5216-137">The VM is paused.</span></span><br/>                                               |



 

## <a name="requirements"></a><span data-ttu-id="e5216-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e5216-138">Requirements</span></span>



| <span data-ttu-id="e5216-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e5216-139">Requirement</span></span> | <span data-ttu-id="e5216-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="e5216-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5216-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e5216-141">Minimum supported client</span></span><br/> | <span data-ttu-id="e5216-142">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e5216-142">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e5216-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e5216-143">Minimum supported server</span></span><br/> | <span data-ttu-id="e5216-144">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e5216-144">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e5216-145">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="e5216-145">End of client support</span></span><br/>    | <span data-ttu-id="e5216-146">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e5216-146">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e5216-147">Produit</span><span class="sxs-lookup"><span data-stu-id="e5216-147">Product</span></span><br/>                  | <span data-ttu-id="e5216-148">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e5216-148">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e5216-149">En-tête</span><span class="sxs-lookup"><span data-stu-id="e5216-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5216-150"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5216-150"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e5216-151">IID</span><span class="sxs-lookup"><span data-stu-id="e5216-151">IID</span></span><br/>                      | <span data-ttu-id="e5216-152">IID \_ IVMGuestOS est défini en tant que 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="e5216-152">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="e5216-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e5216-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5216-154">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="e5216-154">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

