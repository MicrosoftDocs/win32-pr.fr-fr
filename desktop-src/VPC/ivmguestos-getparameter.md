---
title: IVMGuestOS GetParameter, méthode (VPCCOMInterfaces. h)
description: Récupère un paramètre nommé dans le système d’exploitation invité.
ms.assetid: d4d5acbd-fa19-4eb2-af75-2c94e5f6f7f0
keywords:
- Méthode GetParameter Virtual PC
- Méthode GetParameter Virtual PC, interface IVMGuestOS
- IVMGuestOS interface Virtual PC, GetParameter, méthode
topic_type:
- apiref
api_name:
- IVMGuestOS.GetParameter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0acbdd5a1d633a8c032651d2df16f4d0e26dec70
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509254"
---
# <a name="ivmguestosgetparameter-method"></a><span data-ttu-id="8c3e2-106">IVMGuestOS :: GetParameter, méthode</span><span class="sxs-lookup"><span data-stu-id="8c3e2-106">IVMGuestOS::GetParameter method</span></span>

<span data-ttu-id="8c3e2-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8c3e2-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8c3e2-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="8c3e2-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8c3e2-109">Récupère un paramètre nommé dans le système d’exploitation invité.</span><span class="sxs-lookup"><span data-stu-id="8c3e2-109">Retrieves a named parameter within the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c3e2-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8c3e2-110">Syntax</span></span>


```C++
HRESULT GetParameter(
  [in]          BSTR inParameterName,
  [out, retval] BSTR *outParameterValue
);
```



## <a name="parameters"></a><span data-ttu-id="8c3e2-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8c3e2-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c3e2-112">*inParameterName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8c3e2-112">*inParameterName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c3e2-113">Nom du paramètre.</span><span class="sxs-lookup"><span data-stu-id="8c3e2-113">The parameter name.</span></span> <span data-ttu-id="8c3e2-114">Sa longueur doit être comprise entre 1 et 255 caractères et ne peut pas contenir de barre oblique inverse ( \) caractère.</span><span class="sxs-lookup"><span data-stu-id="8c3e2-114">It must be between 1 and 255 characters in length and cannot contain a backslash (\) character.</span></span>

</dd> <dt>

<span data-ttu-id="8c3e2-115">*outParameterValue* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="8c3e2-115">*outParameterValue* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="8c3e2-116">Valeur du paramètre.</span><span class="sxs-lookup"><span data-stu-id="8c3e2-116">The parameter value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c3e2-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8c3e2-117">Return value</span></span>

<span data-ttu-id="8c3e2-118">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="8c3e2-118">This method can return one of these values.</span></span>



| <span data-ttu-id="8c3e2-119">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="8c3e2-119">Return code/value</span></span>                                                                                                                                                                    | <span data-ttu-id="8c3e2-120">Description</span><span class="sxs-lookup"><span data-stu-id="8c3e2-120">Description</span></span>                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8c3e2-121"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8c3e2-121"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="8c3e2-122">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="8c3e2-122">The operation was successful.</span></span><br/>                                     |
| <dl> <span data-ttu-id="8c3e2-123"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="8c3e2-123"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                         | <span data-ttu-id="8c3e2-124">Un paramètre n’est pas valide ou n’est pas spécifié.</span><span class="sxs-lookup"><span data-stu-id="8c3e2-124">A parameter is not valid or not specified.</span></span><br/>                        |
| <dl> <span data-ttu-id="8c3e2-125"><dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="8c3e2-125"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="8c3e2-126">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="8c3e2-126">The parameter is **NULL**.</span></span><br/>                                        |
| <dl> <span data-ttu-id="8c3e2-127"><dt>**Ordinateur virtuel \_ E \_ a \_ expiré**</dt> <dt>0xA0040202</dt></span><span class="sxs-lookup"><span data-stu-id="8c3e2-127"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                     | <span data-ttu-id="8c3e2-128">L’opération ne s’est pas terminée en temps opportun.</span><span class="sxs-lookup"><span data-stu-id="8c3e2-128">The operation did not complete in a timely manner.</span></span><br/>                |
| <dl> <span data-ttu-id="8c3e2-129"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="8c3e2-129"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="8c3e2-130">L’ordinateur virtuel n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="8c3e2-130">The virtual machine is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="8c3e2-131"><dt>**Ordinateur virtuel \_ 0xA00400507 \_ en \_ pause de la machine virtuelle E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="8c3e2-131"><dt>**VM\_E\_VM\_PAUSED**</dt> <dt>0xA00400507</dt></span></span> </dl>                    | <span data-ttu-id="8c3e2-132">L’ordinateur virtuel est en pause.</span><span class="sxs-lookup"><span data-stu-id="8c3e2-132">The virtual machine is paused.</span></span><br/>                                    |
| <dl> <span data-ttu-id="8c3e2-133"><dt>**Ordinateur virtuel \_ La \_ fonctionnalité d’ajouts E \_ \_ n’est pas disponible \_**</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="8c3e2-133"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="8c3e2-134">Les composants d’intégration ne sont pas installés sur cet ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="8c3e2-134">Integration components are not installed in this virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="8c3e2-135"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="8c3e2-135"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="8c3e2-136">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="8c3e2-136">An unexpected error has occurred.</span></span><br/>                                 |



 

## <a name="remarks"></a><span data-ttu-id="8c3e2-137">Notes</span><span class="sxs-lookup"><span data-stu-id="8c3e2-137">Remarks</span></span>

<span data-ttu-id="8c3e2-138">L’ordinateur virtuel doit être en cours d’exécution et les composants d’intégration doivent être installés lorsque cette méthode est appelée.</span><span class="sxs-lookup"><span data-stu-id="8c3e2-138">The virtual machine must be running and integration components must be installed when this method is invoked.</span></span> <span data-ttu-id="8c3e2-139">Cette méthode est uniquement prise en charge pour les systèmes d’exploitation invités basés sur Windows.</span><span class="sxs-lookup"><span data-stu-id="8c3e2-139">This method is only supported for Windows-based guest operating systems.</span></span>

<span data-ttu-id="8c3e2-140">Avec les composants d’intégration installés, la clé suivante est automatiquement ajoutée au registre du système d’exploitation invité :</span><span class="sxs-lookup"><span data-stu-id="8c3e2-140">With integration components installed, the following key is automatically added to the guest operating system's registry:</span></span>

<span data-ttu-id="8c3e2-141">**HKEY \_ local \_ machine \\ Software logiciel \\ Microsoft \\ Virtual \\ machine \\ paramètres invité**</span><span class="sxs-lookup"><span data-stu-id="8c3e2-141">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Virtual Machine\\Guest\\Parameters**</span></span>

<span data-ttu-id="8c3e2-142">Lorsque le système d’exploitation invité démarre, les valeurs de chaîne de Registre suivantes sont renseignées dans la clé des **paramètres** :</span><span class="sxs-lookup"><span data-stu-id="8c3e2-142">When the guest operating system starts, the following registry string values are populated in the **Parameters** key:</span></span>

-   <span data-ttu-id="8c3e2-143">**HostName**</span><span class="sxs-lookup"><span data-stu-id="8c3e2-143">**HostName**</span></span>
-   <span data-ttu-id="8c3e2-144">**PhysicalHostName**</span><span class="sxs-lookup"><span data-stu-id="8c3e2-144">**PhysicalHostName**</span></span>
-   <span data-ttu-id="8c3e2-145">**PhysicalHostNameFullyQualified**</span><span class="sxs-lookup"><span data-stu-id="8c3e2-145">**PhysicalHostNameFullyQualified**</span></span>
-   <span data-ttu-id="8c3e2-146">**VirtualMachineName**</span><span class="sxs-lookup"><span data-stu-id="8c3e2-146">**VirtualMachineName**</span></span>

## <a name="requirements"></a><span data-ttu-id="8c3e2-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8c3e2-147">Requirements</span></span>



| <span data-ttu-id="8c3e2-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8c3e2-148">Requirement</span></span> | <span data-ttu-id="8c3e2-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="8c3e2-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c3e2-150">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c3e2-150">Minimum supported client</span></span><br/> | <span data-ttu-id="8c3e2-151">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8c3e2-151">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8c3e2-152">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c3e2-152">Minimum supported server</span></span><br/> | <span data-ttu-id="8c3e2-153">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c3e2-153">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="8c3e2-154">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="8c3e2-154">End of client support</span></span><br/>    | <span data-ttu-id="8c3e2-155">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8c3e2-155">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8c3e2-156">Produit</span><span class="sxs-lookup"><span data-stu-id="8c3e2-156">Product</span></span><br/>                  | <span data-ttu-id="8c3e2-157">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8c3e2-157">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="8c3e2-158">En-tête</span><span class="sxs-lookup"><span data-stu-id="8c3e2-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c3e2-159"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c3e2-159"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="8c3e2-160">IID</span><span class="sxs-lookup"><span data-stu-id="8c3e2-160">IID</span></span><br/>                      | <span data-ttu-id="8c3e2-161">IID \_ IVMGuestOS est défini en tant que 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="8c3e2-161">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="8c3e2-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c3e2-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c3e2-163">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="8c3e2-163">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

