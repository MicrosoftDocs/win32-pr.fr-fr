---
title: Méthode IVMVirtualMachine GetConfigurationValue (VPCCOMInterfaces. h)
description: Récupère la valeur du paramètre de configuration spécifié pour cet ordinateur virtuel.
ms.assetid: fd3c509e-8a40-4828-b866-6bd2cb455ab2
keywords:
- Méthode GetConfigurationValue Virtual PC
- Méthode GetConfigurationValue Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC, méthode GetConfigurationValue
topic_type:
- apiref
api_name:
- IVMVirtualMachine.GetConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e98e37bd4bd5ec4ba9843ae2fdb33874a4303f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384799"
---
# <a name="ivmvirtualmachinegetconfigurationvalue-method"></a><span data-ttu-id="3c045-106">IVMVirtualMachine :: GetConfigurationValue, méthode</span><span class="sxs-lookup"><span data-stu-id="3c045-106">IVMVirtualMachine::GetConfigurationValue method</span></span>

<span data-ttu-id="3c045-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3c045-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3c045-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3c045-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3c045-109">Récupère la valeur du paramètre de configuration spécifié pour cet ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="3c045-109">Retrieves the value of the specified configuration setting for this virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c045-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3c045-110">Syntax</span></span>


```C++
HRESULT GetConfigurationValue(
  [in]          BSTR    configurationKey,
  [out, retval] VARIANT *configurationValue
);
```



## <a name="parameters"></a><span data-ttu-id="3c045-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3c045-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c045-112">*configurationKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3c045-112">*configurationKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c045-113">Clé utilisée pour identifier la valeur de configuration telle qu’elle est stockée dans le \* fichier « . vmc ».</span><span class="sxs-lookup"><span data-stu-id="3c045-113">The key used to identify the configuration value as stored in the "\*.vmc" file.</span></span>

</dd> <dt>

<span data-ttu-id="3c045-114">*configurationValue* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="3c045-114">*configurationValue* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="3c045-115">Valeur de configuration.</span><span class="sxs-lookup"><span data-stu-id="3c045-115">The configuration value.</span></span> <span data-ttu-id="3c045-116">Cette valeur peut être l’un des types de **variantes** suivants : VT **\_ tableau** VT \| **\_ UI1** (octets bruts), **VT \_ BSTR** (chaîne), **VT \_ I4** (entier) ou **VT \_ bool** (booléen).</span><span class="sxs-lookup"><span data-stu-id="3c045-116">This value can be one of the following **VARIANT** types: **VT\_ARRAY**\|**VT\_UI1** (raw bytes), **VT\_BSTR** (string), **VT\_I4** (integer), or **VT\_BOOL** (Boolean).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c045-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3c045-117">Return value</span></span>

<span data-ttu-id="3c045-118">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="3c045-118">This method can return one of these values.</span></span>



| <span data-ttu-id="3c045-119">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="3c045-119">Return code/value</span></span>                                                                                                                                                      | <span data-ttu-id="3c045-120">Description</span><span class="sxs-lookup"><span data-stu-id="3c045-120">Description</span></span>                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <span data-ttu-id="3c045-121"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3c045-121"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="3c045-122">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="3c045-122">The operation was successful.</span></span><br/>                          |
| <dl> <span data-ttu-id="3c045-123"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="3c045-123"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>           | <span data-ttu-id="3c045-124">Le paramètre *configurationKey* est **null** ou vide.</span><span class="sxs-lookup"><span data-stu-id="3c045-124">The *configurationKey* parameter is **NULL** or empty.</span></span><br/> |
| <dl> <span data-ttu-id="3c045-125"><dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="3c045-125"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="3c045-126">Le paramètre *configurationValue* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="3c045-126">The *configurationValue* parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="3c045-127"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="3c045-127"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="3c045-128">La configuration est inconnue.</span><span class="sxs-lookup"><span data-stu-id="3c045-128">The configuration is unknown.</span></span><br/>                          |
| <dl> <span data-ttu-id="3c045-129"><dt>**Ordinateur virtuel \_ E \_ Préférences \_ \_ introuvables**</dt> <dt>0xA0040300</dt></span><span class="sxs-lookup"><span data-stu-id="3c045-129"><dt>**VM\_E\_PREF\_NOT\_FOUND**</dt> <dt>0xA0040300</dt></span></span> </dl> | <span data-ttu-id="3c045-130">La préférence est introuvable.</span><span class="sxs-lookup"><span data-stu-id="3c045-130">The preference was not found.</span></span><br/>                          |
| <dl> <span data-ttu-id="3c045-131"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="3c045-131"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="3c045-132">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="3c045-132">An unexpected error has occurred.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="3c045-133">Notes</span><span class="sxs-lookup"><span data-stu-id="3c045-133">Remarks</span></span>

<span data-ttu-id="3c045-134">Cette méthode fournit un accès de bas niveau à toute valeur de configuration.</span><span class="sxs-lookup"><span data-stu-id="3c045-134">This method provides low-level access to any configuration value.</span></span> <span data-ttu-id="3c045-135">Il peut être utilisé pour lire les valeurs de configuration des clés définies par le client.</span><span class="sxs-lookup"><span data-stu-id="3c045-135">It can be used to read configuration values for customer-defined keys.</span></span>

<span data-ttu-id="3c045-136">Les clés de configuration se trouvent dans le fichier « \* . vmc » de l’ordinateur virtuel au format XML.</span><span class="sxs-lookup"><span data-stu-id="3c045-136">Configuration keys are located in the virtual machine's "\*.vmc" file in XML format.</span></span> <span data-ttu-id="3c045-137">Les clés sont stockées de manière hiérarchique comme les clés de Registre dans Windows.</span><span class="sxs-lookup"><span data-stu-id="3c045-137">The keys are stored in a hierarchical manner similar to the registry keys in Windows.</span></span> <span data-ttu-id="3c045-138">Pour spécifier une sous-clé spécifique, un « chemin d’accès de clé » est construit, qui spécifie les différentes clés dans un format délimité par des barres obliques.</span><span class="sxs-lookup"><span data-stu-id="3c045-138">To specify a specific subkey, a "key path" is constructed which specifies the various keys in a slash mark delimited format.</span></span>

<span data-ttu-id="3c045-139">Par exemple, pour lire la valeur de la clé « RAM \_ Size » située dans l’arborescence de clé suivante :</span><span class="sxs-lookup"><span data-stu-id="3c045-139">For example, to read the value of the "ram\_size" key located in the following key tree:</span></span>

``` syntax
<hardware>
    <memory>
        <ram_size type="integer">128</ram_size>
```

<span data-ttu-id="3c045-140">La chaîne de chemin d’accès *configurationKey* est spécifiée comme suit :</span><span class="sxs-lookup"><span data-stu-id="3c045-140">The *configurationKey* path string would be specified as follows:</span></span>

``` syntax
"hardware/memory/ram_size"
```

<span data-ttu-id="3c045-141">Si l’une des clés de l’arborescence souhaitée a une valeur d’attribut « ID », l’attribut et sa valeur sont incorporés dans la chaîne de chemin d’accès *configurationKey* immédiatement après la clé de configuration associée en utilisant le format entre crochets suivant : « \[ @id = »*\_ valeur d’ID*« \] ».</span><span class="sxs-lookup"><span data-stu-id="3c045-141">If any of the keys in the desired tree have an "id" attribute value, the attribute and its value is embedded in the *configurationKey* path string immediately after its associated configuration key using the following bracketed format: "\[@id="*id\_value*"\]".</span></span>

<span data-ttu-id="3c045-142">Par exemple, pour lire la valeur de la clé « Absolute » située dans l’arborescence de clé suivante :</span><span class="sxs-lookup"><span data-stu-id="3c045-142">For example, to read the value of the "absolute" key located in the following key tree:</span></span>

``` syntax
<hardware>
    <pci_bus>
        <ide_adapter>
            <ide_controller id="1">
                <location id="0">
                    <pathname>
                        <absolute type="string">D</absolute>
```

<span data-ttu-id="3c045-143">La chaîne de chemin d’accès *configurationKey* est spécifiée comme suit :</span><span class="sxs-lookup"><span data-stu-id="3c045-143">The *configurationKey* path string would be specified as follows:</span></span>

``` syntax
"hardware/pci_bus/ide_adapter/ide_controller[@id=1]/location[@id=0]/pathname/absolute"
```

## <a name="requirements"></a><span data-ttu-id="3c045-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3c045-144">Requirements</span></span>



| <span data-ttu-id="3c045-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3c045-145">Requirement</span></span> | <span data-ttu-id="3c045-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="3c045-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c045-147">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c045-147">Minimum supported client</span></span><br/> | <span data-ttu-id="3c045-148">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3c045-148">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3c045-149">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c045-149">Minimum supported server</span></span><br/> | <span data-ttu-id="3c045-150">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c045-150">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3c045-151">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="3c045-151">End of client support</span></span><br/>    | <span data-ttu-id="3c045-152">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3c045-152">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3c045-153">Produit</span><span class="sxs-lookup"><span data-stu-id="3c045-153">Product</span></span><br/>                  | <span data-ttu-id="3c045-154">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3c045-154">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3c045-155">En-tête</span><span class="sxs-lookup"><span data-stu-id="3c045-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c045-156"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c045-156"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3c045-157">IID</span><span class="sxs-lookup"><span data-stu-id="3c045-157">IID</span></span><br/>                      | <span data-ttu-id="3c045-158">IID \_ IVMVirtualMachine est défini en tant que f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="3c045-158">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="3c045-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c045-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c045-160">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="3c045-160">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

