---
title: Méthode IVMGuestOS SetParameter (VPCCOMInterfaces. h)
description: Définit un paramètre nommé dans le système d’exploitation invité.
ms.assetid: ed6ade61-19dc-44ac-9e86-29fffe80e874
keywords:
- Méthode SetParameter Virtual PC
- Méthode SetParameter Virtual PC, interface IVMGuestOS
- IVMGuestOS interface Virtual PC, méthode SetParameter
topic_type:
- apiref
api_name:
- IVMGuestOS.SetParameter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80dd2290578ef55d56e4c194e27102a1075d7a10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508654"
---
# <a name="ivmguestossetparameter-method"></a><span data-ttu-id="a2fbf-106">IVMGuestOS :: SetParameter, méthode</span><span class="sxs-lookup"><span data-stu-id="a2fbf-106">IVMGuestOS::SetParameter method</span></span>

<span data-ttu-id="a2fbf-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a2fbf-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a2fbf-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a2fbf-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a2fbf-109">Définit un paramètre nommé dans le système d’exploitation invité.</span><span class="sxs-lookup"><span data-stu-id="a2fbf-109">Sets a named parameter within the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2fbf-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a2fbf-110">Syntax</span></span>


```C++
HRESULT SetParameter(
  [in] BSTR inParameterName,
  [in] BSTR inParameterValue
);
```



## <a name="parameters"></a><span data-ttu-id="a2fbf-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a2fbf-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2fbf-112">*inParameterName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a2fbf-112">*inParameterName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2fbf-113">Nom du paramètre.</span><span class="sxs-lookup"><span data-stu-id="a2fbf-113">The parameter name.</span></span> <span data-ttu-id="a2fbf-114">Sa longueur doit être comprise entre 1 et 255 caractères et ne peut pas contenir de barre oblique inverse ( \) caractère.</span><span class="sxs-lookup"><span data-stu-id="a2fbf-114">It must be between 1 and 255 characters in length and cannot contain a backslash (\) character.</span></span>

</dd> <dt>

<span data-ttu-id="a2fbf-115">*inParameterValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a2fbf-115">*inParameterValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2fbf-116">Valeur du paramètre.</span><span class="sxs-lookup"><span data-stu-id="a2fbf-116">The parameter value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2fbf-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a2fbf-117">Return value</span></span>

<span data-ttu-id="a2fbf-118">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="a2fbf-118">This method can return one of these values.</span></span>



| <span data-ttu-id="a2fbf-119">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="a2fbf-119">Return code/value</span></span>                                                                                                                                                                    | <span data-ttu-id="a2fbf-120">Description</span><span class="sxs-lookup"><span data-stu-id="a2fbf-120">Description</span></span>                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="a2fbf-121"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a2fbf-121"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="a2fbf-122">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="a2fbf-122">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="a2fbf-123"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="a2fbf-123"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                         | <span data-ttu-id="a2fbf-124">Un paramètre n’est pas valide ou n’est pas spécifié.</span><span class="sxs-lookup"><span data-stu-id="a2fbf-124">A parameter is not valid or not specified.</span></span><br/>           |
| <dl> <span data-ttu-id="a2fbf-125"><dt>**Ordinateur virtuel \_ E \_ a \_ expiré**</dt> <dt>0xA0040202</dt></span><span class="sxs-lookup"><span data-stu-id="a2fbf-125"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                     | <span data-ttu-id="a2fbf-126">L’opération ne s’est pas terminée en temps opportun.</span><span class="sxs-lookup"><span data-stu-id="a2fbf-126">The operation did not complete in a timely manner.</span></span><br/>   |
| <dl> <span data-ttu-id="a2fbf-127"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="a2fbf-127"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="a2fbf-128">L’ordinateur virtuel n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="a2fbf-128">The virtual machine (VM) is not running.</span></span><br/>             |
| <dl> <span data-ttu-id="a2fbf-129"><dt>**Ordinateur virtuel \_ 0xA00400507 \_ en \_ pause de la machine virtuelle E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="a2fbf-129"><dt>**VM\_E\_VM\_PAUSED**</dt> <dt>0xA00400507</dt></span></span> </dl>                    | <span data-ttu-id="a2fbf-130">La machine virtuelle est suspendue.</span><span class="sxs-lookup"><span data-stu-id="a2fbf-130">The VM is paused.</span></span><br/>                                    |
| <dl> <span data-ttu-id="a2fbf-131"><dt>**Ordinateur virtuel \_ La \_ fonctionnalité d’ajouts E \_ \_ n’est pas disponible \_**</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="a2fbf-131"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="a2fbf-132">Les composants d’intégration ne sont pas installés sur cette machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="a2fbf-132">Integration components are not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="a2fbf-133"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="a2fbf-133"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="a2fbf-134">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="a2fbf-134">An unexpected error has occurred.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="a2fbf-135">Notes</span><span class="sxs-lookup"><span data-stu-id="a2fbf-135">Remarks</span></span>

<span data-ttu-id="a2fbf-136">La machine virtuelle doit être en cours d’exécution et les composants d’intégration doivent être installés lorsque cette méthode est appelée.</span><span class="sxs-lookup"><span data-stu-id="a2fbf-136">The VM must be running and integration components must be installed when this method is invoked.</span></span> <span data-ttu-id="a2fbf-137">Cette méthode est uniquement prise en charge pour les systèmes d’exploitation invités basés sur Windows.</span><span class="sxs-lookup"><span data-stu-id="a2fbf-137">This method is only supported for Windows-based guest operating systems.</span></span>

<span data-ttu-id="a2fbf-138">Avec les composants d’intégration installés, la clé suivante est automatiquement ajoutée au registre du système d’exploitation invité :</span><span class="sxs-lookup"><span data-stu-id="a2fbf-138">With integration components installed, the following key is automatically added to the guest operating system's registry:</span></span>

<span data-ttu-id="a2fbf-139">**HKEY \_ local \_ machine \\ Software logiciel \\ Microsoft \\ Virtual \\ machine \\ paramètres invité**</span><span class="sxs-lookup"><span data-stu-id="a2fbf-139">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Virtual Machine\\Guest\\Parameters**</span></span>

<span data-ttu-id="a2fbf-140">Lorsque le système d’exploitation invité démarre, les valeurs de chaîne de Registre suivantes sont renseignées dans la clé des **paramètres** :</span><span class="sxs-lookup"><span data-stu-id="a2fbf-140">When the guest operating system starts, the following registry string values are populated in the **Parameters** key:</span></span>

-   <span data-ttu-id="a2fbf-141">**HostName**</span><span class="sxs-lookup"><span data-stu-id="a2fbf-141">**HostName**</span></span>
-   <span data-ttu-id="a2fbf-142">**PhysicalHostName**</span><span class="sxs-lookup"><span data-stu-id="a2fbf-142">**PhysicalHostName**</span></span>
-   <span data-ttu-id="a2fbf-143">**PhysicalHostNameFullyQualified**</span><span class="sxs-lookup"><span data-stu-id="a2fbf-143">**PhysicalHostNameFullyQualified**</span></span>
-   <span data-ttu-id="a2fbf-144">**VirtualMachineName**</span><span class="sxs-lookup"><span data-stu-id="a2fbf-144">**VirtualMachineName**</span></span>

## <a name="requirements"></a><span data-ttu-id="a2fbf-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a2fbf-145">Requirements</span></span>



| <span data-ttu-id="a2fbf-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a2fbf-146">Requirement</span></span> | <span data-ttu-id="a2fbf-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="a2fbf-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2fbf-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a2fbf-148">Minimum supported client</span></span><br/> | <span data-ttu-id="a2fbf-149">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a2fbf-149">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a2fbf-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a2fbf-150">Minimum supported server</span></span><br/> | <span data-ttu-id="a2fbf-151">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a2fbf-151">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a2fbf-152">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="a2fbf-152">End of client support</span></span><br/>    | <span data-ttu-id="a2fbf-153">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a2fbf-153">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a2fbf-154">Produit</span><span class="sxs-lookup"><span data-stu-id="a2fbf-154">Product</span></span><br/>                  | <span data-ttu-id="a2fbf-155">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a2fbf-155">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a2fbf-156">En-tête</span><span class="sxs-lookup"><span data-stu-id="a2fbf-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2fbf-157"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2fbf-157"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a2fbf-158">IID</span><span class="sxs-lookup"><span data-stu-id="a2fbf-158">IID</span></span><br/>                      | <span data-ttu-id="a2fbf-159">IID \_ IVMGuestOS est défini en tant que 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="a2fbf-159">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="a2fbf-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a2fbf-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2fbf-161">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="a2fbf-161">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

