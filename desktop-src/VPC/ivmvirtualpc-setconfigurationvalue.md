---
title: Méthode IVMVirtualPC SetConfigurationValue (VPCCOMInterfaces. h)
description: Définit la valeur du paramètre de configuration spécifié.
ms.assetid: 7760b81e-734d-4970-8875-f2d310ff6c5c
keywords:
- Méthode SetConfigurationValue Virtual PC
- Méthode SetConfigurationValue Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface Virtual PC, méthode SetConfigurationValue
topic_type:
- apiref
api_name:
- IVMVirtualPC.SetConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecb8ff3bb68829e944461cedb1c86904c7150593
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509034"
---
# <a name="ivmvirtualpcsetconfigurationvalue-method"></a><span data-ttu-id="74791-106">IVMVirtualPC :: SetConfigurationValue, méthode</span><span class="sxs-lookup"><span data-stu-id="74791-106">IVMVirtualPC::SetConfigurationValue method</span></span>

<span data-ttu-id="74791-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="74791-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="74791-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="74791-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="74791-109">Définit la valeur du paramètre de configuration spécifié.</span><span class="sxs-lookup"><span data-stu-id="74791-109">Sets the value of the specified configuration setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="74791-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="74791-110">Syntax</span></span>


```C++
HRESULT SetConfigurationValue(
  [in] BSTR    preferenceKey,
  [in] VARIANT preferenceValue
);
```



## <a name="parameters"></a><span data-ttu-id="74791-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="74791-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74791-112">*preferenceKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="74791-112">*preferenceKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74791-113">Clé utilisée pour identifier la préférence, telle qu’elle est stockée dans le fichier de configuration par utilisateur (Options.xml dans « % LocalAppData% \\ Microsoft \\ Windows Virtual PC »).</span><span class="sxs-lookup"><span data-stu-id="74791-113">The key used to identify the preference, as stored in the per-user configuration file (Options.xml in "%LocalAppData%\\Microsoft\\Windows Virtual PC").</span></span>

> [!IMPORTANT]
> <span data-ttu-id="74791-114">Les modifications doivent être apportées à Options.xml uniquement à l’aide de la méthode **SetConfigurationValue** .</span><span class="sxs-lookup"><span data-stu-id="74791-114">Changes should be made to Options.xml only using the **SetConfigurationValue** method.</span></span> <span data-ttu-id="74791-115">La modification de Options.xml à l’aide d’une autre méthode n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="74791-115">Changing Options.xml using any other method is not supported.</span></span>

 

</dd> <dt>

<span data-ttu-id="74791-116">*preferenceValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="74791-116">*preferenceValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74791-117">Valeur de préférence.</span><span class="sxs-lookup"><span data-stu-id="74791-117">The preference value.</span></span> <span data-ttu-id="74791-118">Cette valeur peut être l’un des types de **variantes** suivants : VT **\_ tableau** VT \| **\_ UI1** (octets bruts), **VT \_ BSTR** (chaîne), **VT \_ UI4** (entier) ou **VT \_ bool** (booléen).</span><span class="sxs-lookup"><span data-stu-id="74791-118">This value may be one of the following **VARIANT** types: **VT\_ARRAY**\|**VT\_UI1** (raw bytes), **VT\_BSTR** (string), **VT\_UI4** (integer), or **VT\_BOOL** (Boolean).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74791-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="74791-119">Return value</span></span>

<span data-ttu-id="74791-120">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="74791-120">This method can return one of these values.</span></span>



| <span data-ttu-id="74791-121">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="74791-121">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="74791-122">Description</span><span class="sxs-lookup"><span data-stu-id="74791-122">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="74791-123"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="74791-123"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="74791-124">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="74791-124">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="74791-125"><dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="74791-125"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="74791-126">Le paramètre *preferenceKey* ou *PreferenceValue* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="74791-126">The *preferenceKey* or *preferenceValue* parameter is **NULL**.</span></span><br/>                      |
| <dl> <span data-ttu-id="74791-127"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="74791-127"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                             | <span data-ttu-id="74791-128">Le paramètre *preferenceKey* n’est pas valide ou est une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="74791-128">The *preferenceKey* parameter is not valid or is an empty string.</span></span><br/>                    |
| <dl> <span data-ttu-id="74791-129"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="74791-129"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="74791-130">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="74791-130">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="74791-131"><dt>**E \_ ACCESSDENIED**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="74791-131"><dt>**E\_ACCESSDENIED**</dt> <dt>0x80070005</dt></span></span> </dl>                           | <span data-ttu-id="74791-132">L’utilisateur actuel ne dispose pas d’un accès suffisant au fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="74791-132">The current user has insufficient access to the configuration file.</span></span><br/>                  |
| <dl> <span data-ttu-id="74791-133"><dt>**Ordinateur virtuel \_ \_Virtualisation matérielle E \_ \_ désactivée**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="74791-133"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="74791-134">Le processeur ne prend pas en charge les extensions avez (Hardware Accelerated Virtualization).</span><span class="sxs-lookup"><span data-stu-id="74791-134">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="74791-135">Notes</span><span class="sxs-lookup"><span data-stu-id="74791-135">Remarks</span></span>

<span data-ttu-id="74791-136">Les valeurs suivantes sont prises en charge pour le paramètre *preferenceKey* .</span><span class="sxs-lookup"><span data-stu-id="74791-136">The following values are supported for the *preferenceKey* parameter.</span></span>



| <span data-ttu-id="74791-137">valeur *preferenceKey*</span><span class="sxs-lookup"><span data-stu-id="74791-137">*preferenceKey* value</span></span>      | <span data-ttu-id="74791-138">Description</span><span class="sxs-lookup"><span data-stu-id="74791-138">Description</span></span>                                                                                                                                                                           | <span data-ttu-id="74791-139">Type de données</span><span class="sxs-lookup"><span data-stu-id="74791-139">Data type</span></span>            | <span data-ttu-id="74791-140">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="74791-140">Default value</span></span>   |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|-----------------|
| <span data-ttu-id="74791-141">« \_ délai d’inactivité »</span><span class="sxs-lookup"><span data-stu-id="74791-141">"idle\_timeout"</span></span><br/> | <span data-ttu-id="74791-142">Nombre de secondes pendant lesquelles vpc.exe doit attendre avant de quitter s’il n’y a pas de machines virtuelles ou d’applications actives utilisant les [interfaces de PC virtuels Windows](virtual-pc-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="74791-142">Number of seconds that vpc.exe should wait before exiting if there are no active VMs or applications using the [Windows Virtual PC Interfaces](virtual-pc-interfaces.md).</span></span><br/> | <span data-ttu-id="74791-143">entière</span><span class="sxs-lookup"><span data-stu-id="74791-143">"integer"</span></span><br/> | <span data-ttu-id="74791-144">"30"</span><span class="sxs-lookup"><span data-stu-id="74791-144">"30"</span></span><br/> |



 

<span data-ttu-id="74791-145">Cette méthode fournit un accès de bas niveau à toute valeur de configuration.</span><span class="sxs-lookup"><span data-stu-id="74791-145">This method provides low-level access to any configuration value.</span></span> <span data-ttu-id="74791-146">Il peut être utilisé pour définir des valeurs de configuration pour les clés définies par le client.</span><span class="sxs-lookup"><span data-stu-id="74791-146">It can be used to set configuration values for customer-defined keys.</span></span> <span data-ttu-id="74791-147">Soyez prudent si vous utilisez cette méthode pour définir les valeurs de configuration du système, car aucune vérification des erreurs n’est effectuée sur la valeur de configuration.</span><span class="sxs-lookup"><span data-stu-id="74791-147">Be careful if you use this method to set system configuration values, because no error checking is performed on the configuration value.</span></span> <span data-ttu-id="74791-148">En outre, certaines valeurs de configuration ne peuvent pas être modifiées tant qu’un ordinateur virtuel est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="74791-148">Also, some configuration values cannot be changed while a virtual machine is running.</span></span>

<span data-ttu-id="74791-149">Les clés de configuration se trouvent dans le fichier « Options.xml » de l’ordinateur virtuel au format XML.</span><span class="sxs-lookup"><span data-stu-id="74791-149">Configuration keys are located in the virtual machine's "Options.xml" file in XML format.</span></span> <span data-ttu-id="74791-150">Les clés sont stockées de manière hiérarchique comme les clés de Registre dans Windows.</span><span class="sxs-lookup"><span data-stu-id="74791-150">The keys are stored in a hierarchical manner similar to the registry keys in Windows.</span></span> <span data-ttu-id="74791-151">Pour spécifier une sous-clé spécifique, un « chemin d’accès de clé » est construit, qui spécifie les différentes clés dans un format délimité par des barres obliques.</span><span class="sxs-lookup"><span data-stu-id="74791-151">To specify a specific subkey, a "key path" is constructed which specifies the various keys in a slash mark delimited format.</span></span>

<span data-ttu-id="74791-152">Par exemple, pour définir la valeur de la clé « délai d’inactivité \_ » située dans l’arborescence de clé suivante :</span><span class="sxs-lookup"><span data-stu-id="74791-152">For example, to set the value of the "idle\_timeout" key located in the following key tree:</span></span>

``` syntax
<preferences>
  <idle_timeout type="integer">60</idle_timeout>
```

<span data-ttu-id="74791-153">La chaîne de chemin d’accès *preferenceKey* est spécifiée comme suit :</span><span class="sxs-lookup"><span data-stu-id="74791-153">The *preferenceKey* path string would be specified as follows:</span></span>

``` syntax
"idle_timeout"
```

<span data-ttu-id="74791-154">Si l’une des clés de l’arborescence souhaitée a une valeur d’attribut « ID », l’attribut et sa valeur sont incorporés dans la chaîne de chemin d’accès *preferenceKey* immédiatement après la clé de configuration associée en utilisant le format entre crochets suivant : « \[ @id = »*\_ valeur d’ID*« \] ».</span><span class="sxs-lookup"><span data-stu-id="74791-154">If any of the keys in the desired tree have an "id" attribute value, the attribute and its value is embedded in the *preferenceKey* path string immediately after its associated configuration key using the following bracketed format: "\[@id="*id\_value*"\]".</span></span>

<span data-ttu-id="74791-155">Par exemple, pour définir la valeur de la clé « Golf » située dans l’arborescence de clé suivante :</span><span class="sxs-lookup"><span data-stu-id="74791-155">For example, to set the value of the "golf" key located in the following key tree:</span></span>

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

<span data-ttu-id="74791-156">La chaîne de chemin d’accès *preferenceKey* est spécifiée comme suit :</span><span class="sxs-lookup"><span data-stu-id="74791-156">The *preferenceKey* path string would be specified as follows:</span></span>

``` syntax
"alpha/bravo/charlie/delta[@id=1]/echo[@id=0]/foxtrot/golf"
```

## <a name="requirements"></a><span data-ttu-id="74791-157">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="74791-157">Requirements</span></span>



| <span data-ttu-id="74791-158">Condition requise</span><span class="sxs-lookup"><span data-stu-id="74791-158">Requirement</span></span> | <span data-ttu-id="74791-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="74791-159">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="74791-160">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="74791-160">Minimum supported client</span></span><br/> | <span data-ttu-id="74791-161">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="74791-161">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="74791-162">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="74791-162">Minimum supported server</span></span><br/> | <span data-ttu-id="74791-163">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="74791-163">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="74791-164">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="74791-164">End of client support</span></span><br/>    | <span data-ttu-id="74791-165">Windows 7</span><span class="sxs-lookup"><span data-stu-id="74791-165">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="74791-166">Produit</span><span class="sxs-lookup"><span data-stu-id="74791-166">Product</span></span><br/>                  | <span data-ttu-id="74791-167">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="74791-167">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="74791-168">En-tête</span><span class="sxs-lookup"><span data-stu-id="74791-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="74791-169"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="74791-169"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="74791-170">IID</span><span class="sxs-lookup"><span data-stu-id="74791-170">IID</span></span><br/>                      | <span data-ttu-id="74791-171">IID \_ IVMVirtualPC est défini en tant que 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="74791-171">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="74791-172">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="74791-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74791-173">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="74791-173">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> <dt>

[<span data-ttu-id="74791-174">**IVMVirtualMachine::SetConfigurationValue**</span><span class="sxs-lookup"><span data-stu-id="74791-174">**IVMVirtualMachine::SetConfigurationValue**</span></span>](ivmvirtualmachine-setconfigurationvalue.md)
</dt> </dl>

 

