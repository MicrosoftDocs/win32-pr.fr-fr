---
title: Méthode IVMVirtualMachine SetConfigurationValue (VPCCOMInterfaces. h)
description: Définit la valeur du paramètre de configuration spécifié pour cette machine virtuelle.
ms.assetid: 43c3ac88-2e25-4c9e-a2ac-fcae5add62c5
keywords:
- Méthode SetConfigurationValue Virtual PC
- Méthode SetConfigurationValue Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC, méthode SetConfigurationValue
topic_type:
- apiref
api_name:
- IVMVirtualMachine.SetConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1ebafd53a2eb82ea1869b5522d0258ece67d110
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106543630"
---
# <a name="ivmvirtualmachinesetconfigurationvalue-method"></a><span data-ttu-id="12f58-106">IVMVirtualMachine :: SetConfigurationValue, méthode</span><span class="sxs-lookup"><span data-stu-id="12f58-106">IVMVirtualMachine::SetConfigurationValue method</span></span>

<span data-ttu-id="12f58-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="12f58-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="12f58-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="12f58-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="12f58-109">Définit la valeur du paramètre de configuration spécifié pour cette machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="12f58-109">Sets the value of the specified configuration setting for this virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="12f58-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="12f58-110">Syntax</span></span>


```C++
HRESULT SetConfigurationValue(
  [in] BSTR    configurationKey,
  [in] VARIANT configurationValue
);
```



## <a name="parameters"></a><span data-ttu-id="12f58-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="12f58-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12f58-112">*configurationKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="12f58-112">*configurationKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12f58-113">Clé utilisée pour identifier la valeur de configuration telle qu’elle est stockée dans le \* fichier « . vmc ».</span><span class="sxs-lookup"><span data-stu-id="12f58-113">The key used to identify the configuration value as stored in the "\*.vmc" file.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="12f58-114">Les modifications doivent être apportées à " \* . VMC" uniquement à l’aide de la méthode **SetConfigurationValue** .</span><span class="sxs-lookup"><span data-stu-id="12f58-114">Changes should be made to "\*.vmc" only using the **SetConfigurationValue** method.</span></span> <span data-ttu-id="12f58-115">La modification \* de « . VMC » à l’aide d’une autre méthode n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="12f58-115">Changing "\*.vmc" using any other method is not supported.</span></span>

 

</dd> <dt>

<span data-ttu-id="12f58-116">*configurationValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="12f58-116">*configurationValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12f58-117">Valeur de configuration.</span><span class="sxs-lookup"><span data-stu-id="12f58-117">The configuration value.</span></span> <span data-ttu-id="12f58-118">Cette valeur peut être l’un des types de **variantes** suivants : VT **\_ Array** \| **VT \_ UI1** (RAW bytes), **VT \_ BSTR** (String), **VT \_ UI4** (Integer) ou **VT \_ bool** (Boolean).</span><span class="sxs-lookup"><span data-stu-id="12f58-118">This value cay be one of the following **VARIANT** types: **VT\_ARRAY**\|**VT\_UI1** (raw bytes), **VT\_BSTR** (string), **VT\_UI4** (integer), or **VT\_BOOL** (Boolean).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12f58-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="12f58-119">Return value</span></span>

<span data-ttu-id="12f58-120">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="12f58-120">This method can return one of these values.</span></span>



| <span data-ttu-id="12f58-121">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="12f58-121">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="12f58-122">Description</span><span class="sxs-lookup"><span data-stu-id="12f58-122">Description</span></span>                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="12f58-123"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="12f58-123"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="12f58-124">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="12f58-124">The operation was successful.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="12f58-125"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="12f58-125"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="12f58-126">Le paramètre *configurationKey* est **null** ou vide, ou le paramètre *configurationValue* n’est pas un type Variant valide.</span><span class="sxs-lookup"><span data-stu-id="12f58-126">The *configurationKey* parameter is **NULL** or empty or the *configurationValue* parameter is not a valid variant type.</span></span><br/> |
| <dl> <span data-ttu-id="12f58-127"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="12f58-127"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="12f58-128">La configuration est inconnue.</span><span class="sxs-lookup"><span data-stu-id="12f58-128">The configuration is unknown.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="12f58-129"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="12f58-129"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="12f58-130">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="12f58-130">An unexpected error has occurred.</span></span><br/>                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="12f58-131">Notes</span><span class="sxs-lookup"><span data-stu-id="12f58-131">Remarks</span></span>

<span data-ttu-id="12f58-132">Les valeurs suivantes sont prises en charge pour le paramètre *configurationKey* .</span><span class="sxs-lookup"><span data-stu-id="12f58-132">The following values are supported for the *configurationKey* parameter.</span></span>



| <span data-ttu-id="12f58-133">valeur *configurationKey*</span><span class="sxs-lookup"><span data-stu-id="12f58-133">*configurationKey* value</span></span>                                     | <span data-ttu-id="12f58-134">Description</span><span class="sxs-lookup"><span data-stu-id="12f58-134">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | <span data-ttu-id="12f58-135">Type de données</span><span class="sxs-lookup"><span data-stu-id="12f58-135">Data type</span></span>            | <span data-ttu-id="12f58-136">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="12f58-136">Default value</span></span>     |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|-------------------|
| <span data-ttu-id="12f58-137">« matériel/BIOS/ \_ synchronisation de l’heure \_ au \_ démarrage »</span><span class="sxs-lookup"><span data-stu-id="12f58-137">"hardware/bios/time\_sync\_at\_boot"</span></span><br/>              | <span data-ttu-id="12f58-138">« true » si l’horloge CMOS de la machine virtuelle doit être synchronisée avec l’horloge de l’hôte au démarrage ; « false » dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="12f58-138">"true" if the VM CMOS clock is to be synchronized with the host clock at boot; "false" otherwise.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         | <span data-ttu-id="12f58-139">expression</span><span class="sxs-lookup"><span data-stu-id="12f58-139">"boolean"</span></span><br/> | <span data-ttu-id="12f58-140">"true"</span><span class="sxs-lookup"><span data-stu-id="12f58-140">"true"</span></span><br/> |
| <span data-ttu-id="12f58-141">« intégration/synchronisation de l’heure de l’hôte/de Microsoft/ \_ \_ activée »</span><span class="sxs-lookup"><span data-stu-id="12f58-141">"integration/microsoft/host\_time\_sync/enabled""</span></span><br/> | <span data-ttu-id="12f58-142">« true » si la synchronisation de l’heure de l’hôte est activée dans les composants d’intégration ; « false » dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="12f58-142">"true" if host time synchronization is enabled in the integration components; "false" otherwise.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | <span data-ttu-id="12f58-143">expression</span><span class="sxs-lookup"><span data-stu-id="12f58-143">"boolean"</span></span><br/> | <span data-ttu-id="12f58-144">"true"</span><span class="sxs-lookup"><span data-stu-id="12f58-144">"true"</span></span><br/> |
| <span data-ttu-id="12f58-145">« options d’interface utilisateur \_ /publication de l' \_ application automatique \_ »</span><span class="sxs-lookup"><span data-stu-id="12f58-145">"ui\_options/auto\_app\_publish"</span></span><br/>                  | <span data-ttu-id="12f58-146">« true » si la publication automatique des applications est activée dans les composants d’intégration ; « false » dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="12f58-146">"true" if automatic publishing of applications is enabled in the integration components; "false" otherwise.</span></span> <span data-ttu-id="12f58-147">Cela est également appelé applications virtuelles.</span><span class="sxs-lookup"><span data-stu-id="12f58-147">This is also called virtual applications.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="12f58-148">expression</span><span class="sxs-lookup"><span data-stu-id="12f58-148">"boolean"</span></span><br/> | <span data-ttu-id="12f58-149">"true"</span><span class="sxs-lookup"><span data-stu-id="12f58-149">"true"</span></span><br/> |
| <span data-ttu-id="12f58-150">« \_ options d’interface utilisateur/secondes \_ à \_ Enregistrer »</span><span class="sxs-lookup"><span data-stu-id="12f58-150">"ui\_options/seconds\_to\_save"</span></span><br/>                   | <span data-ttu-id="12f58-151">Nombre de secondes d’attente avant l’enregistrement de la machine virtuelle après la fermeture de toutes les applications.</span><span class="sxs-lookup"><span data-stu-id="12f58-151">Number of seconds to wait before saving the VM after all applications are closed.</span></span> <span data-ttu-id="12f58-152">Toutefois, les valeurs inférieures à 20 et supérieures à 4 294 968 ont des significations particulières.</span><span class="sxs-lookup"><span data-stu-id="12f58-152">However, values below 20 and more than 4,294,968 have special meanings.</span></span> <span data-ttu-id="12f58-153">Pour plus d’informations, consultez la liste suivante</span><span class="sxs-lookup"><span data-stu-id="12f58-153">For details, see the following list</span></span><br/> <dl> <span data-ttu-id="12f58-154"><dt><span id="0"></span>0</dt></span><span class="sxs-lookup"><span data-stu-id="12f58-154"><dt><span id="0"></span>0</dt></span></span> <dd> <span data-ttu-id="12f58-155">N’enregistrez jamais la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="12f58-155">Never save the VM.</span></span><br/> </dd> <span data-ttu-id="12f58-156"><dt><span id="120"></span>1 20</dt></span><span class="sxs-lookup"><span data-stu-id="12f58-156"><dt><span id="120"></span>1 20</dt></span></span> <dd> <span data-ttu-id="12f58-157">Patientez 20 secondes avant d’enregistrer la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="12f58-157">Wait 20 seconds before saving the VM.</span></span><br/> </dd> <span data-ttu-id="12f58-158"><dt><span id="214_294_967"></span>21 4 294 967</dt></span><span class="sxs-lookup"><span data-stu-id="12f58-158"><dt><span id="214_294_967"></span>21 4,294,967</dt></span></span> <dd> <span data-ttu-id="12f58-159">Patientez le nombre de secondes spécifié avant d’enregistrer la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="12f58-159">Wait the specified number of seconds before saving the VM.</span></span><br/> </dd> <span data-ttu-id="12f58-160"><dt><span id="4_294_9684_294_967_295"></span>4 294 968 4 294 967 295</dt></span><span class="sxs-lookup"><span data-stu-id="12f58-160"><dt><span id="4_294_9684_294_967_295"></span>4,294,968 4,294,967,295</dt></span></span> <dd> <span data-ttu-id="12f58-161">Attendez 4 294 968 secondes avant d’enregistrer la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="12f58-161">Wait 4,294,968 seconds before saving the VM.</span></span><br/> </dd> </dl> | <span data-ttu-id="12f58-162">entière</span><span class="sxs-lookup"><span data-stu-id="12f58-162">"integer"</span></span><br/> | <span data-ttu-id="12f58-163">300</span><span class="sxs-lookup"><span data-stu-id="12f58-163">300</span></span><br/>    |



 

<span data-ttu-id="12f58-164">Cette méthode fournit un accès de bas niveau à toute valeur de configuration.</span><span class="sxs-lookup"><span data-stu-id="12f58-164">This method provides low-level access to any configuration value.</span></span> <span data-ttu-id="12f58-165">Il peut être utilisé pour définir des valeurs de configuration pour les clés définies par le client.</span><span class="sxs-lookup"><span data-stu-id="12f58-165">It can be used to set configuration values for customer-defined keys.</span></span> <span data-ttu-id="12f58-166">Soyez prudent si vous utilisez cette méthode pour définir les valeurs de configuration du système, car aucune vérification des erreurs n’est effectuée sur la valeur de configuration.</span><span class="sxs-lookup"><span data-stu-id="12f58-166">Be careful if you use this method to set system configuration values, because no error checking is performed on the configuration value.</span></span> <span data-ttu-id="12f58-167">En outre, certaines valeurs de configuration ne peuvent pas être modifiées pendant l’exécution de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="12f58-167">Also, some configuration values cannot be changed while the virtual machine is running.</span></span>

<span data-ttu-id="12f58-168">Les clés de configuration se trouvent dans le fichier « \* . vmc » de l’ordinateur virtuel au format XML.</span><span class="sxs-lookup"><span data-stu-id="12f58-168">Configuration keys are located in the virtual machine's "\*.vmc" file in XML format.</span></span> <span data-ttu-id="12f58-169">Les clés sont stockées de manière hiérarchique comme les clés de Registre dans Windows.</span><span class="sxs-lookup"><span data-stu-id="12f58-169">The keys are stored in a hierarchical manner similar to the registry keys in Windows.</span></span> <span data-ttu-id="12f58-170">Pour spécifier une sous-clé spécifique, un « chemin d’accès de clé » est construit, qui spécifie les différentes clés dans un format délimité par des barres obliques.</span><span class="sxs-lookup"><span data-stu-id="12f58-170">To specify a specific subkey, a "key path" is constructed which specifies the various keys in a slash mark delimited format.</span></span>

<span data-ttu-id="12f58-171">Par exemple, pour définir la valeur de la clé « RAM \_ Size » située dans l’arborescence de clé suivante :</span><span class="sxs-lookup"><span data-stu-id="12f58-171">For example, to set the value of the "ram\_size" key located in the following key tree:</span></span>

``` syntax
<preferences>
  <hardware>
    <bios>
      <time_sync_at_boot type="boolean">true</time_sync_at_boot>
```

<span data-ttu-id="12f58-172">La chaîne de chemin d’accès *configurationKey* est spécifiée comme suit :</span><span class="sxs-lookup"><span data-stu-id="12f58-172">The *configurationKey* path string would be specified as follows:</span></span>

``` syntax
"hardware/memory/ram_size"
```

<span data-ttu-id="12f58-173">Si l’une des clés de l’arborescence souhaitée a une valeur d’attribut « ID », l’attribut et sa valeur sont incorporés dans la chaîne de chemin d’accès *configurationKey* immédiatement après la clé de configuration associée en utilisant le format entre crochets suivant : « \[ @id = »*\_ valeur d’ID*« \] ».</span><span class="sxs-lookup"><span data-stu-id="12f58-173">If any of the keys in the desired tree have an "id" attribute value, the attribute and its value is embedded in the *configurationKey* path string immediately after its associated configuration key using the following bracketed format: "\[@id="*id\_value*"\]".</span></span>

<span data-ttu-id="12f58-174">Par exemple, pour définir la valeur de la clé « Golf » située dans l’arborescence de clé suivante :</span><span class="sxs-lookup"><span data-stu-id="12f58-174">For example, to set the value of the "golf" key located in the following key tree:</span></span>

``` syntax
<preferences>
  <alpha>
    <bravo>
      <charlie>
        <delta id="1">
          <echo id="0">
            <foxtrot>
              <golf type="string">D</golf>
```

<span data-ttu-id="12f58-175">La chaîne de chemin d’accès *configurationKey* est spécifiée comme suit :</span><span class="sxs-lookup"><span data-stu-id="12f58-175">The *configurationKey* path string would be specified as follows:</span></span>

``` syntax
"alpha/bravo/charlie/delta[@id=1]/echo[@id=0]/foxtrot/golf"
```

## <a name="requirements"></a><span data-ttu-id="12f58-176">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="12f58-176">Requirements</span></span>



| <span data-ttu-id="12f58-177">Condition requise</span><span class="sxs-lookup"><span data-stu-id="12f58-177">Requirement</span></span> | <span data-ttu-id="12f58-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="12f58-178">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="12f58-179">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="12f58-179">Minimum supported client</span></span><br/> | <span data-ttu-id="12f58-180">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="12f58-180">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="12f58-181">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="12f58-181">Minimum supported server</span></span><br/> | <span data-ttu-id="12f58-182">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="12f58-182">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="12f58-183">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="12f58-183">End of client support</span></span><br/>    | <span data-ttu-id="12f58-184">Windows 7</span><span class="sxs-lookup"><span data-stu-id="12f58-184">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="12f58-185">Produit</span><span class="sxs-lookup"><span data-stu-id="12f58-185">Product</span></span><br/>                  | <span data-ttu-id="12f58-186">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="12f58-186">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="12f58-187">En-tête</span><span class="sxs-lookup"><span data-stu-id="12f58-187">Header</span></span><br/>                   | <dl> <span data-ttu-id="12f58-188"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="12f58-188"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="12f58-189">IID</span><span class="sxs-lookup"><span data-stu-id="12f58-189">IID</span></span><br/>                      | <span data-ttu-id="12f58-190">IID \_ IVMVirtualMachine est défini en tant que f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="12f58-190">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="12f58-191">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="12f58-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12f58-192">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="12f58-192">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> <dt>

[<span data-ttu-id="12f58-193">**IVMVirtualPC::SetConfigurationValue**</span><span class="sxs-lookup"><span data-stu-id="12f58-193">**IVMVirtualPC::SetConfigurationValue**</span></span>](ivmvirtualpc-setconfigurationvalue.md)
</dt> </dl>

 

