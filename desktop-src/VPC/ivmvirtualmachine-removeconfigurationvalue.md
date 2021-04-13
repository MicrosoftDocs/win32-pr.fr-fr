---
title: Méthode IVMVirtualMachine RemoveConfigurationValue (VPCCOMInterfaces. h)
description: Supprime la valeur du paramètre de configuration spécifié pour cet ordinateur virtuel.
ms.assetid: 2d75a667-9656-4d4c-bafe-f3f8be3763f5
keywords:
- Méthode RemoveConfigurationValue Virtual PC
- Méthode RemoveConfigurationValue Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC, méthode RemoveConfigurationValue
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RemoveConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 683cad2c7cce34822f6f5607ea2676902284baf0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466154"
---
# <a name="ivmvirtualmachineremoveconfigurationvalue-method"></a><span data-ttu-id="fd898-106">IVMVirtualMachine :: RemoveConfigurationValue, méthode</span><span class="sxs-lookup"><span data-stu-id="fd898-106">IVMVirtualMachine::RemoveConfigurationValue method</span></span>

<span data-ttu-id="fd898-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="fd898-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="fd898-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="fd898-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="fd898-109">Supprime la valeur du paramètre de configuration spécifié pour cet ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="fd898-109">Removes the value of the specified configuration setting for this virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd898-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fd898-110">Syntax</span></span>


```C++
HRESULT RemoveConfigurationValue(
  [in] BSTR configurationKey
);
```



## <a name="parameters"></a><span data-ttu-id="fd898-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fd898-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd898-112">*configurationKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fd898-112">*configurationKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd898-113">Clé utilisée pour identifier la valeur de configuration telle qu’elle est stockée dans le \* fichier « . vmc ».</span><span class="sxs-lookup"><span data-stu-id="fd898-113">The key used to identify the configuration value as stored in the "\*.vmc" file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd898-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fd898-114">Return value</span></span>

<span data-ttu-id="fd898-115">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="fd898-115">This method can return one of these values.</span></span>



| <span data-ttu-id="fd898-116">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="fd898-116">Return code/value</span></span>                                                                                                                                                      | <span data-ttu-id="fd898-117">Description</span><span class="sxs-lookup"><span data-stu-id="fd898-117">Description</span></span>                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="fd898-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="fd898-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="fd898-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="fd898-119">The operation was successful.</span></span><br/>       |
| <dl> <span data-ttu-id="fd898-120"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="fd898-120"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>           | <span data-ttu-id="fd898-121">Le paramètre a la **valeur null** ou est vide.</span><span class="sxs-lookup"><span data-stu-id="fd898-121">The parameter is **NULL** or empty.</span></span><br/> |
| <dl> <span data-ttu-id="fd898-122"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="fd898-122"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="fd898-123">La configuration est inconnue.</span><span class="sxs-lookup"><span data-stu-id="fd898-123">The configuration is unknown.</span></span><br/>       |
| <dl> <span data-ttu-id="fd898-124"><dt>**Ordinateur virtuel \_ E \_ Préférences \_ \_ introuvables**</dt> <dt>0xA0040300</dt></span><span class="sxs-lookup"><span data-stu-id="fd898-124"><dt>**VM\_E\_PREF\_NOT\_FOUND**</dt> <dt>0xA0040300</dt></span></span> </dl> | <span data-ttu-id="fd898-125">La préférence est introuvable.</span><span class="sxs-lookup"><span data-stu-id="fd898-125">The preference was not found.</span></span><br/>       |
| <dl> <span data-ttu-id="fd898-126"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="fd898-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="fd898-127">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="fd898-127">An unexpected error has occurred.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="fd898-128">Notes</span><span class="sxs-lookup"><span data-stu-id="fd898-128">Remarks</span></span>

<span data-ttu-id="fd898-129">Cette méthode fournit un accès de bas niveau à toute valeur de configuration.</span><span class="sxs-lookup"><span data-stu-id="fd898-129">This method provides low-level access to any configuration value.</span></span> <span data-ttu-id="fd898-130">Il peut être utilisé pour supprimer des valeurs de configuration pour les clés définies par le client.</span><span class="sxs-lookup"><span data-stu-id="fd898-130">It can be used to remove configuration values for customer-defined keys.</span></span> <span data-ttu-id="fd898-131">Soyez prudent si vous utilisez cette méthode pour supprimer les valeurs de configuration système, car certaines valeurs ne peuvent pas être modifiées pendant l’exécution de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="fd898-131">Be careful if you use this method to remove system configuration values, since some values cannot be changed while the virtual machine is running.</span></span>

<span data-ttu-id="fd898-132">Les clés de configuration se trouvent dans le fichier « \* . vmc » de l’ordinateur virtuel au format XML.</span><span class="sxs-lookup"><span data-stu-id="fd898-132">Configuration keys are located in the virtual machine's "\*.vmc" file in XML format.</span></span> <span data-ttu-id="fd898-133">Les clés sont stockées de manière hiérarchique comme les clés de Registre dans Windows.</span><span class="sxs-lookup"><span data-stu-id="fd898-133">The keys are stored in a hierarchical manner similar to the registry keys in Windows.</span></span> <span data-ttu-id="fd898-134">Pour spécifier une sous-clé spécifique, un « chemin d’accès de clé » est construit, qui spécifie les différentes clés dans un format délimité par des barres obliques.</span><span class="sxs-lookup"><span data-stu-id="fd898-134">To specify a specific subkey, a "key path" is constructed which specifies the various keys in a slash mark delimited format.</span></span>

<span data-ttu-id="fd898-135">Par exemple, pour supprimer la valeur de la clé « RAM \_ Size » située dans l’arborescence de clé suivante :</span><span class="sxs-lookup"><span data-stu-id="fd898-135">For example, to remove the value of the "ram\_size" key located in the following key tree:</span></span>

``` syntax
<hardware>
    <memory>
        <ram_size type="integer">128</ram_size>
```

<span data-ttu-id="fd898-136">La chaîne de chemin d’accès *configurationKey* est spécifiée comme suit :</span><span class="sxs-lookup"><span data-stu-id="fd898-136">The *configurationKey* path string would be specified as follows:</span></span>

``` syntax
"hardware/memory/ram_size"
```

<span data-ttu-id="fd898-137">Si l’une des clés de l’arborescence souhaitée a une valeur d’attribut « ID », l’attribut et sa valeur sont incorporés dans la chaîne de chemin d’accès *configurationKey* immédiatement après la clé de configuration associée en utilisant le format entre crochets suivant : « \[ @id = »*\_ valeur d’ID*« \] ».</span><span class="sxs-lookup"><span data-stu-id="fd898-137">If any of the keys in the desired tree have an "id" attribute value, the attribute and its value is embedded in the *configurationKey* path string immediately after its associated configuration key using the following bracketed format: "\[@id="*id\_value*"\]".</span></span>

<span data-ttu-id="fd898-138">Par exemple, pour supprimer la valeur de la clé « Absolute » située dans l’arborescence de clé suivante :</span><span class="sxs-lookup"><span data-stu-id="fd898-138">For example, to remove the value of the "absolute" key located in the following key tree:</span></span>

``` syntax
<hardware>
    <pci_bus>
        <ide_adapter>
            <ide_controller id="1">
                <location id="0">
                    <pathname>
                        <absolute type="string">D</absolute>
```

<span data-ttu-id="fd898-139">La chaîne de chemin d’accès *configurationKey* est spécifiée comme suit :</span><span class="sxs-lookup"><span data-stu-id="fd898-139">The *configurationKey* path string would be specified as follows:</span></span>

``` syntax
"hardware/pci_bus/ide_adapter/ide_controller[@id=1]/location[@id=0]/pathname/absolute"
```

## <a name="requirements"></a><span data-ttu-id="fd898-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fd898-140">Requirements</span></span>



| <span data-ttu-id="fd898-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fd898-141">Requirement</span></span> | <span data-ttu-id="fd898-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd898-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd898-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd898-143">Minimum supported client</span></span><br/> | <span data-ttu-id="fd898-144">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fd898-144">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fd898-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd898-145">Minimum supported server</span></span><br/> | <span data-ttu-id="fd898-146">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd898-146">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="fd898-147">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="fd898-147">End of client support</span></span><br/>    | <span data-ttu-id="fd898-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fd898-148">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="fd898-149">Produit</span><span class="sxs-lookup"><span data-stu-id="fd898-149">Product</span></span><br/>                  | <span data-ttu-id="fd898-150">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="fd898-150">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="fd898-151">En-tête</span><span class="sxs-lookup"><span data-stu-id="fd898-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd898-152"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd898-152"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="fd898-153">IID</span><span class="sxs-lookup"><span data-stu-id="fd898-153">IID</span></span><br/>                      | <span data-ttu-id="fd898-154">IID \_ IVMVirtualMachine est défini en tant que f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="fd898-154">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="fd898-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd898-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd898-156">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="fd898-156">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

