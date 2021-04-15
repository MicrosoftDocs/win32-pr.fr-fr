---
title: Méthode IVMVirtualPC CreateVirtualMachine (VPCCOMInterfaces. h)
description: Crée une nouvelle configuration d’ordinateur virtuel et récupère l’objet ordinateur virtuel.
ms.assetid: 35f7364f-debd-4b9c-8240-23c0512eb004
keywords:
- Méthode CreateVirtualMachine Virtual PC
- Méthode CreateVirtualMachine Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface Virtual PC, méthode CreateVirtualMachine
topic_type:
- apiref
api_name:
- IVMVirtualPC.CreateVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 494d5166271e6c4086b8dfee12deb61e32ae8a18
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466266"
---
# <a name="ivmvirtualpccreatevirtualmachine-method"></a><span data-ttu-id="f5c78-106">IVMVirtualPC :: CreateVirtualMachine, méthode</span><span class="sxs-lookup"><span data-stu-id="f5c78-106">IVMVirtualPC::CreateVirtualMachine method</span></span>

<span data-ttu-id="f5c78-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f5c78-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f5c78-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f5c78-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f5c78-109">Crée une nouvelle configuration d’ordinateur virtuel et récupère l’objet ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="f5c78-109">Creates a new virtual machine configuration and retrieves the virtual machine object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5c78-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f5c78-110">Syntax</span></span>


```C++
HRESULT CreateVirtualMachine(
  [in]          BSTR              configurationName,
  [in]          BSTR              configurationPath,
  [out, retval] IVMVirtualMachine **virtualMachine
);
```



## <a name="parameters"></a><span data-ttu-id="f5c78-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f5c78-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5c78-112">*ConfigurationName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f5c78-112">*configurationName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5c78-113">Nom de la machine virtuelle à créer.</span><span class="sxs-lookup"><span data-stu-id="f5c78-113">The name of the virtual machine to be created.</span></span> <span data-ttu-id="f5c78-114">La longueur du nom ne peut pas dépasser 80 caractères et la longueur combinée du nom et du chemin d’accès aux fichiers VMC et VMCX ne peut pas dépasser les caractères de **\_ chemin d’accès maximal** (260).</span><span class="sxs-lookup"><span data-stu-id="f5c78-114">The length of the name cannot exceed 80 characters and the combined length of the name and path to VMC and VMCX files cannot exceed **MAX\_PATH** (260) characters.</span></span> <span data-ttu-id="f5c78-115">Les extensions de nom de fichier. vmc et. vmcx seront ajoutées à la fin du nom de l’ordinateur virtuel lors de la création des fichiers de configuration.</span><span class="sxs-lookup"><span data-stu-id="f5c78-115">The file name extensions .vmc and .vmcx will be appended to the end of the virtual machine name when the configuration files are created.</span></span> <span data-ttu-id="f5c78-116">Si ce paramètre a la **valeur null** ou est une chaîne vide, le paramètre *ConfigurationPath* doit spécifier le chemin d’accès complet au fichier VMC.</span><span class="sxs-lookup"><span data-stu-id="f5c78-116">If this parameter is **NULL** or an empty string, the *configurationPath* parameter must specify the full path to the VMC file.</span></span>

</dd> <dt>

<span data-ttu-id="f5c78-117">*ConfigurationPath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f5c78-117">*configurationPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5c78-118">Chemin d’accès au dossier qui contiendra le fichier VMC.</span><span class="sxs-lookup"><span data-stu-id="f5c78-118">The path to the folder that will contain the VMC file.</span></span> <span data-ttu-id="f5c78-119">Ce dossier sera créé s’il n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="f5c78-119">This folder will be created if it does not exist.</span></span> <span data-ttu-id="f5c78-120">Si *ConfigurationName* a la **valeur null** ou est une chaîne vide, le chemin d’accès complet du nouveau fichier de configuration doit être spécifié.</span><span class="sxs-lookup"><span data-stu-id="f5c78-120">If *configurationName* is **NULL** or an empty string, this must specify the full path of the new configuration file.</span></span>

</dd> <dt>

<span data-ttu-id="f5c78-121">*VirtualMachine* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="f5c78-121">*virtualMachine* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="f5c78-122">Pointeur vers un nouvel objet [**IVMVirtualMachine**](ivmvirtualmachine.md) qui représente cet ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="f5c78-122">A pointer to a new [**IVMVirtualMachine**](ivmvirtualmachine.md) object that represents this virtual machine.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5c78-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f5c78-123">Return value</span></span>

<span data-ttu-id="f5c78-124">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="f5c78-124">This method can return one of these values.</span></span>



| <span data-ttu-id="f5c78-125">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="f5c78-125">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="f5c78-126">Description</span><span class="sxs-lookup"><span data-stu-id="f5c78-126">Description</span></span>                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f5c78-127"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f5c78-127"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="f5c78-128">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="f5c78-128">The operation was successful.</span></span><br/>                                                                                                                                                                       |
| <dl> <span data-ttu-id="f5c78-129"><dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="f5c78-129"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="f5c78-130">Le paramètre *ConfigurationName* ou *ConfigurationPath* n’est pas valide, ou le paramètre *VirtualMachine* est **null**.</span><span class="sxs-lookup"><span data-stu-id="f5c78-130">The *configurationName* or *configurationPath* parameter is not valid, or the *virtualMachine* parameter is **NULL**.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="f5c78-131">Valeur <dt>**HRESULT \_ À partir de \_ Win32 ( \_ chemin d’erreur \_ \_ introuvable)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="f5c78-131"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="f5c78-132">Le système ne trouve pas le chemin d’accès spécifié par le paramètre *ConfigurationPath* .</span><span class="sxs-lookup"><span data-stu-id="f5c78-132">The system cannot find the path specified by the *configurationPath* parameter.</span></span><br/>                                                                                                                     |
| <dl> <span data-ttu-id="f5c78-133">Valeur <dt>**HRESULT \_ À partir de \_ Win32 (erreur \_ \_ nom non valide)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="f5c78-133"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="f5c78-134">Le paramètre *ConfigurationPath* contient un caractère non valide (l’un des « \* ?: <>/ \| »).</span><span class="sxs-lookup"><span data-stu-id="f5c78-134">The *configurationPath* parameter contains an invalid character (one of "\*?:<>/\|"").</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="f5c78-135">Valeur <dt>**HRESULT \_ FROM \_ Win32 (erreur \_ de \_ nom de chemin incorrect)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="f5c78-135"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="f5c78-136">Le paramètre *ConfigurationPath* spécifie un chemin d’accès vide ou relatif.</span><span class="sxs-lookup"><span data-stu-id="f5c78-136">The *configurationPath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="f5c78-137">Un chemin d’accès absolu est requis.</span><span class="sxs-lookup"><span data-stu-id="f5c78-137">An absolute path is required.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="f5c78-138">Valeur <dt>**HRESULT \_ À partir de \_ Win32 \_ ( \_ dépassement de mémoire tampon d’erreur)**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="f5c78-138"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="f5c78-139">Le chemin d’accès spécifié par les paramètres *ConfigurationName* et *ConfigurationPath* génère un chemin d’accès trop long.</span><span class="sxs-lookup"><span data-stu-id="f5c78-139">The path specified by the *configurationName* and *configurationPath* parameters results in a path that is too long.</span></span> <span data-ttu-id="f5c78-140">La longueur totale du chemin d’accès doit être inférieure à la longueur **maximale \_** (260) caractères.</span><span class="sxs-lookup"><span data-stu-id="f5c78-140">The total length of the path must be less than **MAX\_PATH** (260) characters.</span></span><br/> |
| <dl> <span data-ttu-id="f5c78-141">Valeur <dt>**HRESULT \_ À partir de \_ Win32 (l’erreur \_ \_ existe déjà)**</dt> <dt>0x800700b7</dt></span><span class="sxs-lookup"><span data-stu-id="f5c78-141"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ALREADY\_EXISTS)**</dt> <dt>0x800700b7</dt></span></span> </dl>  | <span data-ttu-id="f5c78-142">Un fichier de configuration portant ce nom existe déjà à cet emplacement.</span><span class="sxs-lookup"><span data-stu-id="f5c78-142">A configuration file with this name already exists at this location.</span></span><br/>                                                                                                                                |
| <dl> <span data-ttu-id="f5c78-143"><dt>**Ordinateur virtuel \_ E \_ config \_ sans \_ nom**</dt> <dt>0xA0040400</dt></span><span class="sxs-lookup"><span data-stu-id="f5c78-143"><dt>**VM\_E\_CONFIG\_NO\_NAME**</dt> <dt>0xA0040400</dt></span></span> </dl>                       | <span data-ttu-id="f5c78-144">Le paramètre *ConfigurationName* est vide.</span><span class="sxs-lookup"><span data-stu-id="f5c78-144">The *configurationName* parameter is empty.</span></span><br/>                                                                                                                                                         |
| <dl> <span data-ttu-id="f5c78-145"><dt>**Ordinateur virtuel \_ Nom de la \_ configuration E \_ \_ trop \_ long**</dt> <dt>0xA0040401</dt></span><span class="sxs-lookup"><span data-stu-id="f5c78-145"><dt>**VM\_E\_CONFIG\_NAME\_TOO\_LONG**</dt> <dt>0xA0040401</dt></span></span> </dl>                | <span data-ttu-id="f5c78-146">La longueur du paramètre *ConfigurationName* dépasse 80 caractères.</span><span class="sxs-lookup"><span data-stu-id="f5c78-146">The *configurationName* parameter exceeds 80 characters in length.</span></span><br/>                                                                                                                                  |
| <dl> <span data-ttu-id="f5c78-147"><dt>**Ordinateur virtuel \_ Nom de la configuration E 0xA0040402 \_ \_ \_ \_ char non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="f5c78-147"><dt>**VM\_E\_CONFIG\_NAME\_INVALID\_CHAR**</dt> <dt>0xA0040402</dt></span></span> </dl>            | <span data-ttu-id="f5c78-148">Le paramètre *ConfigurationName* contient un caractère non valide (l’un des « \* ?: <>/ \| \\ »).</span><span class="sxs-lookup"><span data-stu-id="f5c78-148">The *configurationName* parameter contains an invalid character (one of "\*?:<>/\|\\"").</span></span><br/>                                                                                                      |
| <dl> <span data-ttu-id="f5c78-149"><dt>**Ordinateur virtuel \_ \_ \_ \_ Nom en double de la configuration E**</dt> <dt>0xA0040403</dt></span><span class="sxs-lookup"><span data-stu-id="f5c78-149"><dt>**VM\_E\_CONFIG\_DUPLICATE\_NAME**</dt> <dt>0xA0040403</dt></span></span> </dl>                | <span data-ttu-id="f5c78-150">Il existe déjà un ordinateur virtuel portant ce nom.</span><span class="sxs-lookup"><span data-stu-id="f5c78-150">There is already a virtual machine with this name.</span></span><br/>                                                                                                                                                  |
| <dl> <span data-ttu-id="f5c78-151"><dt>**Ordinateur virtuel \_ \_Virtualisation matérielle E \_ \_ désactivée**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="f5c78-151"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="f5c78-152">Le processeur ne prend pas en charge les extensions avez (Hardware Accelerated Virtualization).</span><span class="sxs-lookup"><span data-stu-id="f5c78-152">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                                                                                                |
| <dl> <span data-ttu-id="f5c78-153"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="f5c78-153"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="f5c78-154">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="f5c78-154">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="f5c78-155">Notes</span><span class="sxs-lookup"><span data-stu-id="f5c78-155">Remarks</span></span>

<span data-ttu-id="f5c78-156">Les noms de machine virtuelle ne respectent pas la casse, par exemple, « MyVM » et « MyVM » font référence à la même machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="f5c78-156">Virtual machine names are case-insensitive, for example, "MyVM" and "myvm" refer to the same virtual machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5c78-157">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f5c78-157">Requirements</span></span>



| <span data-ttu-id="f5c78-158">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f5c78-158">Requirement</span></span> | <span data-ttu-id="f5c78-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="f5c78-159">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5c78-160">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f5c78-160">Minimum supported client</span></span><br/> | <span data-ttu-id="f5c78-161">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f5c78-161">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f5c78-162">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f5c78-162">Minimum supported server</span></span><br/> | <span data-ttu-id="f5c78-163">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="f5c78-163">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f5c78-164">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="f5c78-164">End of client support</span></span><br/>    | <span data-ttu-id="f5c78-165">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f5c78-165">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f5c78-166">Produit</span><span class="sxs-lookup"><span data-stu-id="f5c78-166">Product</span></span><br/>                  | <span data-ttu-id="f5c78-167">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f5c78-167">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f5c78-168">En-tête</span><span class="sxs-lookup"><span data-stu-id="f5c78-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5c78-169"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5c78-169"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f5c78-170">IID</span><span class="sxs-lookup"><span data-stu-id="f5c78-170">IID</span></span><br/>                      | <span data-ttu-id="f5c78-171">IID \_ IVMVirtualPC est défini en tant que 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="f5c78-171">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="f5c78-172">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5c78-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5c78-173">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="f5c78-173">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

