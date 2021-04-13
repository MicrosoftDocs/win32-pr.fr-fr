---
title: Méthode IVMVirtualMachine SetActivationValue (VPCCOMInterfaces. h)
description: Définit la valeur du paramètre d’activation spécifié pour cet ordinateur virtuel.
ms.assetid: 6d664a80-1777-42ca-8454-df84c64ab505
keywords:
- Méthode SetActivationValue Virtual PC
- Méthode SetActivationValue Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC, méthode SetActivationValue
topic_type:
- apiref
api_name:
- IVMVirtualMachine.SetActivationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c7cb48b5691a9ca99a0fca5b696d8b545a40e46
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466386"
---
# <a name="ivmvirtualmachinesetactivationvalue-method"></a><span data-ttu-id="64f2e-106">IVMVirtualMachine :: SetActivationValue, méthode</span><span class="sxs-lookup"><span data-stu-id="64f2e-106">IVMVirtualMachine::SetActivationValue method</span></span>

<span data-ttu-id="64f2e-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="64f2e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="64f2e-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="64f2e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="64f2e-109">Définit la valeur du paramètre d’activation spécifié pour cet ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="64f2e-109">Sets the value of the specified activation setting for this virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="64f2e-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="64f2e-110">Syntax</span></span>


```C++
HRESULT SetActivationValue(
  [in] BSTR    activationKey,
  [in] VARIANT activationValue
);
```



## <a name="parameters"></a><span data-ttu-id="64f2e-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="64f2e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64f2e-112">*clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="64f2e-112">*activationKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64f2e-113">Clé utilisée pour identifier la valeur d’activation telle qu’elle est stockée dans le \* fichier « . vmc ».</span><span class="sxs-lookup"><span data-stu-id="64f2e-113">The key used to identify the activation value as stored in the "\*.vmc" file.</span></span>

</dd> <dt>

<span data-ttu-id="64f2e-114">*activationValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="64f2e-114">*activationValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64f2e-115">Valeur d’activation.</span><span class="sxs-lookup"><span data-stu-id="64f2e-115">The activation value.</span></span> <span data-ttu-id="64f2e-116">Cette valeur peut être l’un des types de **variantes** suivants : VT **\_ tableau** VT \| **\_ UI1** (octets bruts), **VT \_ BSTR** (chaîne), **VT \_ UI4** (entier) ou **VT \_ bool** (booléen).</span><span class="sxs-lookup"><span data-stu-id="64f2e-116">This value can be one of the following **VARIANT** types: **VT\_ARRAY**\|**VT\_UI1** (raw bytes), **VT\_BSTR** (string), **VT\_UI4** (integer), or **VT\_BOOL** (Boolean).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64f2e-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="64f2e-117">Return value</span></span>

<span data-ttu-id="64f2e-118">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="64f2e-118">This method can return one of these values.</span></span>



| <span data-ttu-id="64f2e-119">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="64f2e-119">Return code/value</span></span>                                                                                                                                                      | <span data-ttu-id="64f2e-120">Description</span><span class="sxs-lookup"><span data-stu-id="64f2e-120">Description</span></span>                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="64f2e-121"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="64f2e-121"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="64f2e-122">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="64f2e-122">The operation was successful.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="64f2e-123"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="64f2e-123"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>           | <span data-ttu-id="64f2e-124">Le paramètre *clé* est **null** ou vide, ou le paramètre *activationValue* n’est pas un type Variant valide.</span><span class="sxs-lookup"><span data-stu-id="64f2e-124">The *activationKey* parameter is **NULL** or empty, or the *activationValue* parameter is not a valid variant type.</span></span><br/> |
| <dl> <span data-ttu-id="64f2e-125"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="64f2e-125"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="64f2e-126">La configuration est inconnue.</span><span class="sxs-lookup"><span data-stu-id="64f2e-126">The configuration is unknown.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="64f2e-127"><dt>**Ordinateur virtuel \_ E \_ Préférences \_ \_ introuvables**</dt> <dt>0xA0040300</dt></span><span class="sxs-lookup"><span data-stu-id="64f2e-127"><dt>**VM\_E\_PREF\_NOT\_FOUND**</dt> <dt>0xA0040300</dt></span></span> </dl> | <span data-ttu-id="64f2e-128">La configuration n’a pas d’activation valide.</span><span class="sxs-lookup"><span data-stu-id="64f2e-128">The configuration has no valid activation.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="64f2e-129"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="64f2e-129"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="64f2e-130">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="64f2e-130">An unexpected error has occurred.</span></span><br/>                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="64f2e-131">Notes</span><span class="sxs-lookup"><span data-stu-id="64f2e-131">Remarks</span></span>

<span data-ttu-id="64f2e-132">Cette méthode fournit un accès de bas niveau à toute valeur d’activation.</span><span class="sxs-lookup"><span data-stu-id="64f2e-132">This method provides low-level access to any activation value.</span></span> <span data-ttu-id="64f2e-133">Il peut être utilisé pour définir des valeurs d’activation pour les clés définies par le client.</span><span class="sxs-lookup"><span data-stu-id="64f2e-133">It can be used to set activation values for customer-defined keys.</span></span> <span data-ttu-id="64f2e-134">Soyez prudent si vous utilisez cette méthode pour définir les valeurs d’activation du système, car aucune vérification des erreurs n’est effectuée sur la valeur d’activation.</span><span class="sxs-lookup"><span data-stu-id="64f2e-134">Be careful if you use this method to set system activation values, since no error checking is performed on the activation value.</span></span> <span data-ttu-id="64f2e-135">En outre, certaines valeurs d’activation ne peuvent pas être modifiées pendant l’exécution de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="64f2e-135">Also, some activation values cannot be changed while the virtual machine is running.</span></span> <span data-ttu-id="64f2e-136">Lorsqu’un ordinateur virtuel est démarré, une copie de ses valeurs de configuration est créée, qui devient son ensemble de valeurs d’activation.</span><span class="sxs-lookup"><span data-stu-id="64f2e-136">When a virtual machine is started, a copy is made of its configuration values, which becomes its set of activation values.</span></span> <span data-ttu-id="64f2e-137">Les valeurs d’activation sont conservées jusqu’à ce que la machine virtuelle soit arrêtée ou redémarrée.</span><span class="sxs-lookup"><span data-stu-id="64f2e-137">Activation values are maintained until the virtual machine is shut down or restarted.</span></span> <span data-ttu-id="64f2e-138">Notez que Windows Virtual PC peut uniquement utiliser la configuration pour stocker des valeurs pour certaines clés, autrement dit, la valeur d’activation peut ne jamais être utilisée.</span><span class="sxs-lookup"><span data-stu-id="64f2e-138">Note that Windows Virtual PC may only use the configuration to store values for certain keys, that is, the activation value may never be used.</span></span>

> [!Note]  
> <span data-ttu-id="64f2e-139">La session de l’ordinateur virtuel doit être en cours d’exécution pour que toutes les valeurs d’activation puissent être modifiées.</span><span class="sxs-lookup"><span data-stu-id="64f2e-139">The virtual machine session must be running before any activation values can be changed.</span></span>

 

<span data-ttu-id="64f2e-140">Les clés d’activation sont stockées en interne de manière hiérarchique, de la même façon que les clés de Registre dans Windows.</span><span class="sxs-lookup"><span data-stu-id="64f2e-140">Activation keys are stored internally in a hierarchical manner similar to the registry keys in Windows.</span></span> <span data-ttu-id="64f2e-141">Pour spécifier une sous-clé spécifique, un « chemin d’accès de clé » est construit, qui spécifie les différentes clés dans un format délimité par des barres obliques.</span><span class="sxs-lookup"><span data-stu-id="64f2e-141">To specify a specific subkey, a "key path" is constructed which specifies the various keys in a slash mark delimited format.</span></span>

<span data-ttu-id="64f2e-142">Par exemple, pour définir la valeur de la clé « \_ action par défaut » située dans l’arborescence de clé suivante :</span><span class="sxs-lookup"><span data-stu-id="64f2e-142">For example, to set the value of the "default\_action" key located in the following key tree:</span></span>

``` syntax
<settings>
    <undo_drives>
        <default_action type="integer">1</default_action>
```

<span data-ttu-id="64f2e-143">La chaîne de chemin d’accès *clé* est spécifiée comme suit :</span><span class="sxs-lookup"><span data-stu-id="64f2e-143">The *activationKey* path string would be specified as follows:</span></span>

``` syntax
"settings/undo_drives/default_action"
```

## <a name="requirements"></a><span data-ttu-id="64f2e-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="64f2e-144">Requirements</span></span>



| <span data-ttu-id="64f2e-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="64f2e-145">Requirement</span></span> | <span data-ttu-id="64f2e-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="64f2e-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="64f2e-147">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="64f2e-147">Minimum supported client</span></span><br/> | <span data-ttu-id="64f2e-148">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="64f2e-148">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="64f2e-149">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="64f2e-149">Minimum supported server</span></span><br/> | <span data-ttu-id="64f2e-150">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="64f2e-150">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="64f2e-151">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="64f2e-151">End of client support</span></span><br/>    | <span data-ttu-id="64f2e-152">Windows 7</span><span class="sxs-lookup"><span data-stu-id="64f2e-152">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="64f2e-153">Produit</span><span class="sxs-lookup"><span data-stu-id="64f2e-153">Product</span></span><br/>                  | <span data-ttu-id="64f2e-154">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="64f2e-154">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="64f2e-155">En-tête</span><span class="sxs-lookup"><span data-stu-id="64f2e-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="64f2e-156"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="64f2e-156"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="64f2e-157">IID</span><span class="sxs-lookup"><span data-stu-id="64f2e-157">IID</span></span><br/>                      | <span data-ttu-id="64f2e-158">IID \_ IVMVirtualMachine est défini en tant que f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="64f2e-158">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="64f2e-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64f2e-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64f2e-160">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="64f2e-160">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

