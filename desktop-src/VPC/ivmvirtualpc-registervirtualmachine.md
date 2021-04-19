---
title: Méthode IVMVirtualPC RegisterVirtualMachine (VPCCOMInterfaces. h)
description: Inscrit une configuration d’ordinateur virtuel existante et récupère l’objet ordinateur virtuel.
ms.assetid: d3b13f1b-7537-4e3f-9bcc-98a6fe855f78
keywords:
- Méthode RegisterVirtualMachine Virtual PC
- Méthode RegisterVirtualMachine Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface Virtual PC, méthode RegisterVirtualMachine
topic_type:
- apiref
api_name:
- IVMVirtualPC.RegisterVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72cc1e27a657eaad70aeec81c0216d1e707fa36b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511589"
---
# <a name="ivmvirtualpcregistervirtualmachine-method"></a><span data-ttu-id="adac3-106">IVMVirtualPC :: RegisterVirtualMachine, méthode</span><span class="sxs-lookup"><span data-stu-id="adac3-106">IVMVirtualPC::RegisterVirtualMachine method</span></span>

<span data-ttu-id="adac3-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="adac3-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="adac3-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="adac3-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="adac3-109">Inscrit une configuration d’ordinateur virtuel existante et récupère l’objet ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="adac3-109">Registers an existing virtual machine configuration and retrieves the virtual machine object.</span></span>

## <a name="syntax"></a><span data-ttu-id="adac3-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="adac3-110">Syntax</span></span>


```C++
HRESULT RegisterVirtualMachine(
  [in]          BSTR              configurationName,
  [in]          BSTR              configurationPath,
  [out, retval] IVMVirtualMachine **virtualMachine
);
```



## <a name="parameters"></a><span data-ttu-id="adac3-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="adac3-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="adac3-112">*ConfigurationName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="adac3-112">*configurationName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adac3-113">Nom de la machine virtuelle à inscrire.</span><span class="sxs-lookup"><span data-stu-id="adac3-113">The name of the virtual machine to be registered.</span></span> <span data-ttu-id="adac3-114">La longueur du nom ne peut pas dépasser 80 caractères et la longueur combinée du nom et du chemin d’accès ne peut pas dépasser le **\_ chemin d’accès maximal** (260) caractères.</span><span class="sxs-lookup"><span data-stu-id="adac3-114">The length of the name cannot exceed 80 characters and the combined length of the name and path cannot exceed **MAX\_PATH** (260) characters.</span></span> <span data-ttu-id="adac3-115">Le nom spécifié peut contenir l’extension. vmc.</span><span class="sxs-lookup"><span data-stu-id="adac3-115">The specified name may contain the .vmc extension.</span></span> <span data-ttu-id="adac3-116">Si ce paramètre a la **valeur null** ou est une chaîne vide, le paramètre *ConfigurationPath* doit spécifier le chemin d’accès complet au fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="adac3-116">If this parameter is **NULL** or an empty string, the *configurationPath* parameter must specify the full path to the configuration file.</span></span>

</dd> <dt>

<span data-ttu-id="adac3-117">*ConfigurationPath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="adac3-117">*configurationPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adac3-118">Chemin d’accès au dossier qui contient le fichier de configuration existant.</span><span class="sxs-lookup"><span data-stu-id="adac3-118">The path to the folder that contains the existing configuration file.</span></span> <span data-ttu-id="adac3-119">Si le paramètre *ConfigurationName* a la **valeur null** ou est une chaîne vide, il doit spécifier le chemin d’accès complet au fichier de configuration existant.</span><span class="sxs-lookup"><span data-stu-id="adac3-119">If the *configurationName* parameter is **NULL** or an empty string, this must specify the full path to the existing configuration file.</span></span>

</dd> <dt>

<span data-ttu-id="adac3-120">*VirtualMachine* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="adac3-120">*virtualMachine* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="adac3-121">Pointeur vers un nouvel objet [**IVMVirtualMachine**](ivmvirtualmachine.md) qui représente cet ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="adac3-121">A pointer to a new [**IVMVirtualMachine**](ivmvirtualmachine.md) object that represents this virtual machine.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="adac3-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="adac3-122">Return value</span></span>

<span data-ttu-id="adac3-123">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="adac3-123">This method can return one of these values.</span></span>



| <span data-ttu-id="adac3-124">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="adac3-124">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="adac3-125">Description</span><span class="sxs-lookup"><span data-stu-id="adac3-125">Description</span></span>                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="adac3-126"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="adac3-126"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="adac3-127">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="adac3-127">The operation was successful.</span></span><br/>                                                                                                                                                                          |
| <dl> <span data-ttu-id="adac3-128"><dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="adac3-128"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="adac3-129">Le paramètre *ConfigurationName* ou *ConfigurationPath* n’est pas valide, ou *VirtualMachine* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="adac3-129">The *configurationName* or *configurationPath* parameter is invalid, or *virtualMachine* is **NULL**.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="adac3-130">Valeur <dt>**HRESULT \_ À partir de \_ Win32 ( \_ chemin d’erreur \_ \_ introuvable)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="adac3-130"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="adac3-131">Le système ne trouve pas le chemin d’accès spécifié par les paramètres *ConfigurationName* et *ConfigurationPath* .</span><span class="sxs-lookup"><span data-stu-id="adac3-131">The system cannot find the path specified by the *configurationName* and *configurationPath* parameters.</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="adac3-132">Valeur <dt>**HRESULT \_ FROM \_ Win32 ( \_ fichier d' \_ erreur \_ introuvable)**</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="adac3-132"><dt>**HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)**</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="adac3-133">Le système ne peut pas trouver le fichier spécifié par les paramètres *ConfigurationName* et *ConfigurationPath* .</span><span class="sxs-lookup"><span data-stu-id="adac3-133">The system cannot find the file specified by the *configurationName* and *configurationPath* parameters.</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="adac3-134">Valeur <dt>**HRESULT \_ À partir de \_ Win32 (erreur \_ \_ nom non valide)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="adac3-134"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="adac3-135">Le paramètre *ConfigurationPath* contient un caractère non valide (l’un des « \* ?: <>/ \| »).</span><span class="sxs-lookup"><span data-stu-id="adac3-135">The *configurationPath* parameter contains an invalid character (one of "\*?:<>/\|"").</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="adac3-136">Valeur <dt>**HRESULT \_ FROM \_ Win32 (erreur \_ de \_ nom de chemin incorrect)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="adac3-136"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="adac3-137">Le paramètre *ConfigurationPath* spécifie un chemin d’accès vide ou relatif.</span><span class="sxs-lookup"><span data-stu-id="adac3-137">The parameter *configurationPath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="adac3-138">Un chemin d’accès absolu est requis.</span><span class="sxs-lookup"><span data-stu-id="adac3-138">An absolute path is required.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="adac3-139">Valeur <dt>**HRESULT \_ À partir de \_ Win32 \_ ( \_ dépassement de mémoire tampon d’erreur)**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="adac3-139"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="adac3-140">Le chemin d’accès spécifié par les paramètres *ConfigurationName* et *ConfigurationPath* génère un chemin d’accès trop long.</span><span class="sxs-lookup"><span data-stu-id="adac3-140">The path specified by the *configurationName* and *configurationPath* parameters results in a path that is too long.</span></span> <span data-ttu-id="adac3-141">La longueur combinée du chemin d’accès doit être inférieure à la longueur **maximale \_** (260) caractères.</span><span class="sxs-lookup"><span data-stu-id="adac3-141">The combined length of the path must be less than **MAX\_PATH** (260) characters.</span></span><br/> |
| <dl> <span data-ttu-id="adac3-142">Valeur <dt>**HRESULT \_ À partir de \_ Win32 (l’erreur \_ \_ existe déjà)**</dt> <dt>0x800700b7</dt></span><span class="sxs-lookup"><span data-stu-id="adac3-142"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ALREADY\_EXISTS)**</dt> <dt>0x800700b7</dt></span></span> </dl>  | <span data-ttu-id="adac3-143">Un fichier de configuration portant ce nom existe déjà à cet emplacement.</span><span class="sxs-lookup"><span data-stu-id="adac3-143">A configuration file with this name already exists at this location.</span></span><br/>                                                                                                                                   |
| <dl> <span data-ttu-id="adac3-144"><dt>**Ordinateur virtuel \_ Nom de la \_ configuration E \_ \_ trop \_ long**</dt> <dt>0xA0040401</dt></span><span class="sxs-lookup"><span data-stu-id="adac3-144"><dt>**VM\_E\_CONFIG\_NAME\_TOO\_LONG**</dt> <dt>0xA0040401</dt></span></span> </dl>                | <span data-ttu-id="adac3-145">La longueur du paramètre *ConfigurationName* dépasse 80 caractères.</span><span class="sxs-lookup"><span data-stu-id="adac3-145">The *configurationName* parameter exceeds 80 characters in length.</span></span><br/>                                                                                                                                     |
| <dl> <span data-ttu-id="adac3-146"><dt>**Ordinateur virtuel \_ Nom de la configuration E 0xA0040402 \_ \_ \_ \_ char non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="adac3-146"><dt>**VM\_E\_CONFIG\_NAME\_INVALID\_CHAR**</dt> <dt>0xA0040402</dt></span></span> </dl>            | <span data-ttu-id="adac3-147">Le paramètre *ConfigurationName* contient un caractère non valide (l’un des « \* ?: <>/ \| \\ »).</span><span class="sxs-lookup"><span data-stu-id="adac3-147">The *configurationName* parameter contains an invalid character (one of "\*?:<>/\|\\"").</span></span><br/>                                                                                                         |
| <dl> <span data-ttu-id="adac3-148"><dt>**Ordinateur virtuel \_ \_ \_ \_ Nom en double de la configuration E**</dt> <dt>0xA0040403</dt></span><span class="sxs-lookup"><span data-stu-id="adac3-148"><dt>**VM\_E\_CONFIG\_DUPLICATE\_NAME**</dt> <dt>0xA0040403</dt></span></span> </dl>                | <span data-ttu-id="adac3-149">Il existe déjà un ordinateur virtuel portant ce nom.</span><span class="sxs-lookup"><span data-stu-id="adac3-149">There is already a virtual machine with this name.</span></span><br/>                                                                                                                                                     |
| <dl> <span data-ttu-id="adac3-150"><dt>**Ordinateur virtuel \_ \_Virtualisation matérielle E \_ \_ désactivée**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="adac3-150"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="adac3-151">Le processeur ne prend pas en charge les extensions avez (Hardware Accelerated Virtualization).</span><span class="sxs-lookup"><span data-stu-id="adac3-151">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                                                                                                   |
| <dl> <span data-ttu-id="adac3-152"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="adac3-152"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="adac3-153">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="adac3-153">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="adac3-154">Notes</span><span class="sxs-lookup"><span data-stu-id="adac3-154">Remarks</span></span>

<span data-ttu-id="adac3-155">Les noms de machine virtuelle ne respectent pas la casse, par exemple, « MyVM » et « MyVM » font référence à la même machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="adac3-155">Virtual machine names are case-insensitive, for example, "MyVM" and "myvm" refer to the same virtual machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="adac3-156">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="adac3-156">Requirements</span></span>



| <span data-ttu-id="adac3-157">Condition requise</span><span class="sxs-lookup"><span data-stu-id="adac3-157">Requirement</span></span> | <span data-ttu-id="adac3-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="adac3-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="adac3-159">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="adac3-159">Minimum supported client</span></span><br/> | <span data-ttu-id="adac3-160">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="adac3-160">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="adac3-161">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="adac3-161">Minimum supported server</span></span><br/> | <span data-ttu-id="adac3-162">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="adac3-162">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="adac3-163">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="adac3-163">End of client support</span></span><br/>    | <span data-ttu-id="adac3-164">Windows 7</span><span class="sxs-lookup"><span data-stu-id="adac3-164">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="adac3-165">Produit</span><span class="sxs-lookup"><span data-stu-id="adac3-165">Product</span></span><br/>                  | <span data-ttu-id="adac3-166">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="adac3-166">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="adac3-167">En-tête</span><span class="sxs-lookup"><span data-stu-id="adac3-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="adac3-168"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="adac3-168"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="adac3-169">IID</span><span class="sxs-lookup"><span data-stu-id="adac3-169">IID</span></span><br/>                      | <span data-ttu-id="adac3-170">IID \_ IVMVirtualPC est défini en tant que 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="adac3-170">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="adac3-171">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="adac3-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adac3-172">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="adac3-172">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

