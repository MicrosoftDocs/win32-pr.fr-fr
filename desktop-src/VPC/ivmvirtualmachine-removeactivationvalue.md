---
title: Méthode IVMVirtualMachine RemoveActivationValue (VPCCOMInterfaces. h)
description: Supprime la valeur du paramètre d’activation spécifié pour cet ordinateur virtuel.
ms.assetid: 8e9b9d95-aec9-4b73-afc3-cd0d7300f40f
keywords:
- Méthode RemoveActivationValue Virtual PC
- Méthode RemoveActivationValue Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC, méthode RemoveActivationValue
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RemoveActivationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b0461b27e43066f32c25663e3b38dab9b3b71b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032953"
---
# <a name="ivmvirtualmachineremoveactivationvalue-method"></a><span data-ttu-id="f4746-106">IVMVirtualMachine :: RemoveActivationValue, méthode</span><span class="sxs-lookup"><span data-stu-id="f4746-106">IVMVirtualMachine::RemoveActivationValue method</span></span>

<span data-ttu-id="f4746-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f4746-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f4746-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f4746-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f4746-109">Supprime la valeur du paramètre d’activation spécifié pour cet ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="f4746-109">Removes the value of the specified activation setting for this virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4746-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f4746-110">Syntax</span></span>


```C++
HRESULT RemoveActivationValue(
  [in] BSTR activationKey
);
```



## <a name="parameters"></a><span data-ttu-id="f4746-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f4746-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4746-112">*clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f4746-112">*activationKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4746-113">Clé utilisée pour identifier la valeur d’activation telle qu’elle est stockée dans le \* fichier « . vmc ».</span><span class="sxs-lookup"><span data-stu-id="f4746-113">The key used to identify the activation value as stored in the "\*.vmc" file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4746-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f4746-114">Return value</span></span>

<span data-ttu-id="f4746-115">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="f4746-115">This method can return one of these values.</span></span>



| <span data-ttu-id="f4746-116">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="f4746-116">Return code/value</span></span>                                                                                                                                                      | <span data-ttu-id="f4746-117">Description</span><span class="sxs-lookup"><span data-stu-id="f4746-117">Description</span></span>                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f4746-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f4746-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="f4746-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="f4746-119">The operation was successful.</span></span><br/>                                                |
| <dl> <span data-ttu-id="f4746-120"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="f4746-120"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>           | <span data-ttu-id="f4746-121">Le paramètre a la **valeur null** ou est vide.</span><span class="sxs-lookup"><span data-stu-id="f4746-121">The parameter is **NULL** or empty.</span></span><br/>                                          |
| <dl> <span data-ttu-id="f4746-122"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="f4746-122"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="f4746-123">La configuration est inconnue.</span><span class="sxs-lookup"><span data-stu-id="f4746-123">The configuration is unknown.</span></span><br/>                                                |
| <dl> <span data-ttu-id="f4746-124"><dt>**Ordinateur virtuel \_ E \_ Préférences \_ \_ introuvables**</dt> <dt>0xA0040300</dt></span><span class="sxs-lookup"><span data-stu-id="f4746-124"><dt>**VM\_E\_PREF\_NOT\_FOUND**</dt> <dt>0xA0040300</dt></span></span> </dl> | <span data-ttu-id="f4746-125">La préférence est introuvable, ou cette configuration n’a pas d’activation valide.</span><span class="sxs-lookup"><span data-stu-id="f4746-125">The preference was not found, or this configuration has no valid activation.</span></span><br/> |
| <dl> <span data-ttu-id="f4746-126"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="f4746-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="f4746-127">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="f4746-127">An unexpected error has occurred.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="f4746-128">Notes</span><span class="sxs-lookup"><span data-stu-id="f4746-128">Remarks</span></span>

<span data-ttu-id="f4746-129">Cette méthode fournit un accès de bas niveau à toute valeur d’activation.</span><span class="sxs-lookup"><span data-stu-id="f4746-129">This method provides low-level access to any activation value.</span></span> <span data-ttu-id="f4746-130">Il peut être utilisé pour supprimer des valeurs d’activation pour les clés définies par le client.</span><span class="sxs-lookup"><span data-stu-id="f4746-130">It can be used to remove activation values for customer-defined keys.</span></span> <span data-ttu-id="f4746-131">Soyez prudent si vous utilisez cette méthode pour supprimer les valeurs d’activation du système, car certaines valeurs ne peuvent pas être modifiées pendant l’exécution de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="f4746-131">Be careful if you use this method to remove system activation values, since some values cannot be changed while the virtual machine is running.</span></span> <span data-ttu-id="f4746-132">Lorsqu’un ordinateur virtuel est démarré, une copie de ses valeurs de configuration est créée, qui devient son ensemble de valeurs d’activation.</span><span class="sxs-lookup"><span data-stu-id="f4746-132">When a virtual machine is started, a copy is made of its configuration values, which becomes its set of activation values.</span></span> <span data-ttu-id="f4746-133">Les valeurs d’activation sont conservées jusqu’à ce que la machine virtuelle soit arrêtée ou redémarrée.</span><span class="sxs-lookup"><span data-stu-id="f4746-133">Activation values are maintained until the virtual machine is shut down or restarted.</span></span> <span data-ttu-id="f4746-134">Notez que Windows Virtual PC peut uniquement utiliser la configuration pour stocker des valeurs pour certaines clés, autrement dit, la valeur d’activation peut ne jamais être utilisée.</span><span class="sxs-lookup"><span data-stu-id="f4746-134">Note that Windows Virtual PC may only use the configuration to store values for certain keys, that is, the activation value may never be used.</span></span>

> [!Note]  
> <span data-ttu-id="f4746-135">La session de l’ordinateur virtuel doit être en cours d’exécution pour que toutes les valeurs d’activation puissent être modifiées.</span><span class="sxs-lookup"><span data-stu-id="f4746-135">The virtual machine session must be running before any activation values can be changed.</span></span>

 

<span data-ttu-id="f4746-136">Les clés d’activation sont stockées en interne de manière hiérarchique, de la même façon que les clés de Registre dans Windows.</span><span class="sxs-lookup"><span data-stu-id="f4746-136">Activation keys are stored internally in a hierarchical manner similar to the registry keys in Windows.</span></span> <span data-ttu-id="f4746-137">Pour spécifier une sous-clé spécifique, un « chemin d’accès de clé » est construit, qui spécifie les différentes clés dans un format délimité par des barres obliques.</span><span class="sxs-lookup"><span data-stu-id="f4746-137">To specify a specific subkey, a "key path" is constructed which specifies the various keys in a slash mark delimited format.</span></span>

<span data-ttu-id="f4746-138">Par exemple, pour supprimer la valeur de la clé « \_ action par défaut » située dans l’arborescence de clé suivante :</span><span class="sxs-lookup"><span data-stu-id="f4746-138">For example, to remove the value of the "default\_action" key located in the following key tree:</span></span>

``` syntax
<settings>
    <undo_drives>
        <default_action type="integer">1</default_action>
```

<span data-ttu-id="f4746-139">La chaîne de chemin d’accès *clé* est spécifiée comme suit :</span><span class="sxs-lookup"><span data-stu-id="f4746-139">The *activationKey* path string would be specified as follows:</span></span>

``` syntax
"settings/undo_drives/default_action"
```

## <a name="requirements"></a><span data-ttu-id="f4746-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f4746-140">Requirements</span></span>



| <span data-ttu-id="f4746-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f4746-141">Requirement</span></span> | <span data-ttu-id="f4746-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4746-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4746-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f4746-143">Minimum supported client</span></span><br/> | <span data-ttu-id="f4746-144">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f4746-144">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f4746-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f4746-145">Minimum supported server</span></span><br/> | <span data-ttu-id="f4746-146">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="f4746-146">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f4746-147">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="f4746-147">End of client support</span></span><br/>    | <span data-ttu-id="f4746-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f4746-148">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f4746-149">Produit</span><span class="sxs-lookup"><span data-stu-id="f4746-149">Product</span></span><br/>                  | <span data-ttu-id="f4746-150">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f4746-150">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f4746-151">En-tête</span><span class="sxs-lookup"><span data-stu-id="f4746-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4746-152"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4746-152"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f4746-153">IID</span><span class="sxs-lookup"><span data-stu-id="f4746-153">IID</span></span><br/>                      | <span data-ttu-id="f4746-154">IID \_ IVMVirtualMachine est défini en tant que f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="f4746-154">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="f4746-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4746-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4746-156">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="f4746-156">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

