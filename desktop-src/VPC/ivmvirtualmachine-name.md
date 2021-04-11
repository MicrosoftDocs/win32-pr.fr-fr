---
title: Propriété IVMVirtualMachine Name (VPCCOMInterfaces. h)
description: Nom de la configuration de la machine virtuelle.
ms.assetid: 90acedbf-4159-48a3-a9e9-6f1ee00dab8b
keywords:
- Propriété de nom Virtual PC
- Propriété de nom Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC, propriété Name
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Name
- IVMVirtualMachine.get_Name
- IVMVirtualMachine.put_Name
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c163173a778d8103922fd8c8948ab5156f512ed0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104101"
---
# <a name="ivmvirtualmachinename-property"></a><span data-ttu-id="e70ff-106">IVMVirtualMachine :: Name, propriété</span><span class="sxs-lookup"><span data-stu-id="e70ff-106">IVMVirtualMachine::Name property</span></span>

<span data-ttu-id="e70ff-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e70ff-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e70ff-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e70ff-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e70ff-109">Récupère et définit le nom de la configuration de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="e70ff-109">Retrieves and sets the name of the virtual machine configuration.</span></span>

<span data-ttu-id="e70ff-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="e70ff-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e70ff-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e70ff-111">Syntax</span></span>


```C++
HRESULT put_Name(
  [in]          BSTR virtualMachineName
);

HRESULT get_Name(
  [out, retval] BSTR *virtualMachineName
);
```



## <a name="property-value"></a><span data-ttu-id="e70ff-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="e70ff-112">Property value</span></span>

<span data-ttu-id="e70ff-113">Spécifie le nom de la configuration de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="e70ff-113">Specifies the name of the virtual machine configuration.</span></span> <span data-ttu-id="e70ff-114">La longueur du nom ne peut pas dépasser 80 caractères et la longueur totale du chemin d’accès complet qui comprend le fichier de configuration du nom de l’ordinateur virtuel ne peut pas dépasser le **\_ chemin d’accès maximal** (260) caractères.</span><span class="sxs-lookup"><span data-stu-id="e70ff-114">The length of the name cannot be more than 80 characters and the total length of the fully qualified path that includes the virtual machine name configuration file cannot be more than **MAX\_PATH** (260) characters.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e70ff-115">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="e70ff-115">Error codes</span></span>



| <span data-ttu-id="e70ff-116">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="e70ff-116">Name/value</span></span>                                                                                                                                                                    | <span data-ttu-id="e70ff-117">Signification</span><span class="sxs-lookup"><span data-stu-id="e70ff-117">Meaning</span></span>                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e70ff-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e70ff-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                       | <span data-ttu-id="e70ff-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="e70ff-119">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="e70ff-120"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="e70ff-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                         | <span data-ttu-id="e70ff-121">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="e70ff-121">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="e70ff-122"><dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="e70ff-122"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>                      | <span data-ttu-id="e70ff-123">Le paramètre n’est pas valide ou est une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="e70ff-123">The parameter is not valid or is an empty string.</span></span><br/>                                    |
| <dl> <span data-ttu-id="e70ff-124"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="e70ff-124"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>                 | <span data-ttu-id="e70ff-125">La configuration est inconnue.</span><span class="sxs-lookup"><span data-stu-id="e70ff-125">The configuration is unknown.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="e70ff-126"><dt>Ordinateur virtuel \_ E/r 0xA0040302 \_ \_ \_ active VM</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="e70ff-126"><dt>VM\_E\_PREF\_VM\_ACTIVE</dt> <dt>0xA0040302</dt></span></span> </dl>            | <span data-ttu-id="e70ff-127">L’ordinateur virtuel est en cours d’exécution ou enregistré.</span><span class="sxs-lookup"><span data-stu-id="e70ff-127">The virtual machine is running or saved.</span></span><br/>                                             |
| <dl> <span data-ttu-id="e70ff-128"><dt>Ordinateur virtuel \_ E \_ config \_ sans \_ nom</dt> <dt>0xA0040400</dt></span><span class="sxs-lookup"><span data-stu-id="e70ff-128"><dt>VM\_E\_CONFIG\_NO\_NAME</dt> <dt>0xA0040400</dt></span></span> </dl>            | <span data-ttu-id="e70ff-129">Le paramètre *virtualMachineName* est vide.</span><span class="sxs-lookup"><span data-stu-id="e70ff-129">The *virtualMachineName* parameter is empty.</span></span><br/>                                         |
| <dl> <span data-ttu-id="e70ff-130"><dt>Ordinateur virtuel \_ Nom de la \_ configuration E \_ \_ trop \_ long</dt> <dt>0xA00400401</dt></span><span class="sxs-lookup"><span data-stu-id="e70ff-130"><dt>VM\_E\_CONFIG\_NAME\_TOO\_LONG</dt> <dt>0xA00400401</dt></span></span> </dl>    | <span data-ttu-id="e70ff-131">Le paramètre contient trop de caractères.</span><span class="sxs-lookup"><span data-stu-id="e70ff-131">The parameter contains too many characters.</span></span><br/>                                          |
| <dl> <span data-ttu-id="e70ff-132"><dt>Ordinateur virtuel \_ Nom de la configuration E 0xA0040402 \_ \_ \_ \_ char non valide</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="e70ff-132"><dt>VM\_E\_CONFIG\_NAME\_INVALID\_CHAR</dt> <dt>0xA0040402</dt></span></span> </dl> | <span data-ttu-id="e70ff-133">Le paramètre contient l’un des caractères non valides suivants : « \* ?: <>/ \| \\ ».</span><span class="sxs-lookup"><span data-stu-id="e70ff-133">The parameter contains one of the following invalid characters "\*?:<>/\|\\"".</span></span><br/> |
| <dl> <span data-ttu-id="e70ff-134"><dt>Ordinateur virtuel \_ \_ \_ \_ Nom en double de la configuration E</dt> <dt>0xA0040403</dt></span><span class="sxs-lookup"><span data-stu-id="e70ff-134"><dt>VM\_E\_CONFIG\_DUPLICATE\_NAME</dt> <dt>0xA0040403</dt></span></span> </dl>     | <span data-ttu-id="e70ff-135">Le nom spécifié existe déjà en tant que nom d’un autre ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="e70ff-135">The specified name already exists as the name of another virtual machine.</span></span><br/>            |
| <dl> <span data-ttu-id="e70ff-136"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="e70ff-136"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                 | <span data-ttu-id="e70ff-137">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="e70ff-137">An unexpected error has occurred.</span></span><br/>                                                    |



## <a name="remarks"></a><span data-ttu-id="e70ff-138">Notes</span><span class="sxs-lookup"><span data-stu-id="e70ff-138">Remarks</span></span>

<span data-ttu-id="e70ff-139">Les noms de machine virtuelle ne respectent pas la casse, par exemple « MyVM » et « MyVM » font référence à la même machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="e70ff-139">Virtual machine names are case-insensitive, e.g. "MyVM" and "myvm" refer to the same virtual machine.</span></span> <span data-ttu-id="e70ff-140">Il s’agit de la propriété par défaut pour [**IVMVirtualMachine**](ivmvirtualmachine.md).</span><span class="sxs-lookup"><span data-stu-id="e70ff-140">This is the default property for [**IVMVirtualMachine**](ivmvirtualmachine.md).</span></span>

<span data-ttu-id="e70ff-141">Si VPC.exe est en cours d’exécution et que la machine virtuelle est enregistrée, la définition de la propriété **Name** échouera.</span><span class="sxs-lookup"><span data-stu-id="e70ff-141">If VPC.exe is running and the VM is saved then setting the **Name** property will not succeed.</span></span> <span data-ttu-id="e70ff-142">Si VPC.exe n’est pas en cours d’exécution et que la machine virtuelle est enregistrée, la définition de la propriété **Name** est réussie lors du prochain démarrage de VPC.exe.</span><span class="sxs-lookup"><span data-stu-id="e70ff-142">If VPC.exe is not running and the VM is saved then setting the **Name** property will succeed when VPC.exe is next started.</span></span>

## <a name="requirements"></a><span data-ttu-id="e70ff-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e70ff-143">Requirements</span></span>



| <span data-ttu-id="e70ff-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e70ff-144">Requirement</span></span> | <span data-ttu-id="e70ff-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="e70ff-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e70ff-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e70ff-146">Minimum supported client</span></span><br/> | <span data-ttu-id="e70ff-147">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e70ff-147">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e70ff-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e70ff-148">Minimum supported server</span></span><br/> | <span data-ttu-id="e70ff-149">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e70ff-149">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e70ff-150">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="e70ff-150">End of client support</span></span><br/>    | <span data-ttu-id="e70ff-151">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e70ff-151">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e70ff-152">Produit</span><span class="sxs-lookup"><span data-stu-id="e70ff-152">Product</span></span><br/>                  | <span data-ttu-id="e70ff-153">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e70ff-153">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e70ff-154">En-tête</span><span class="sxs-lookup"><span data-stu-id="e70ff-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="e70ff-155"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="e70ff-155"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e70ff-156">IID</span><span class="sxs-lookup"><span data-stu-id="e70ff-156">IID</span></span><br/>                      | <span data-ttu-id="e70ff-157">IID \_ IVMVirtualMachine est défini en tant que f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="e70ff-157">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="e70ff-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e70ff-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e70ff-159">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="e70ff-159">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

