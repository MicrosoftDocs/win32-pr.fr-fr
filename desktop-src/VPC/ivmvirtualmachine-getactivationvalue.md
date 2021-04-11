---
title: Méthode IVMVirtualMachine GetActivationValue (VPCCOMInterfaces. h)
description: Récupère la valeur du paramètre d’activation spécifié pour cet ordinateur virtuel.
ms.assetid: 9a6f138f-6a8a-4cdf-8fb3-83d541d88fba
keywords:
- Méthode GetActivationValue Virtual PC
- Méthode GetActivationValue Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC, méthode GetActivationValue
topic_type:
- apiref
api_name:
- IVMVirtualMachine.GetActivationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e87b51e34feb654fa9c5ab00ed7906268cdc9ec3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317102"
---
# <a name="ivmvirtualmachinegetactivationvalue-method"></a><span data-ttu-id="fd9b2-106">IVMVirtualMachine :: GetActivationValue, méthode</span><span class="sxs-lookup"><span data-stu-id="fd9b2-106">IVMVirtualMachine::GetActivationValue method</span></span>

<span data-ttu-id="fd9b2-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="fd9b2-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="fd9b2-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="fd9b2-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="fd9b2-109">Récupère la valeur du paramètre d’activation spécifié pour cet ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="fd9b2-109">Retrieves the value of the specified activation setting for this virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd9b2-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fd9b2-110">Syntax</span></span>


```C++
HRESULT GetActivationValue(
  [in]          BSTR    activationKey,
  [out, retval] VARIANT *activationValue
);
```



## <a name="parameters"></a><span data-ttu-id="fd9b2-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fd9b2-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd9b2-112">*clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fd9b2-112">*activationKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd9b2-113">Clé utilisée pour identifier la valeur d’activation telle qu’elle est stockée dans le \* fichier « . vmc ».</span><span class="sxs-lookup"><span data-stu-id="fd9b2-113">The key used to identify the activation value as stored in the "\*.vmc" file.</span></span>

</dd> <dt>

<span data-ttu-id="fd9b2-114">*activationValue* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="fd9b2-114">*activationValue* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="fd9b2-115">Valeur d’activation.</span><span class="sxs-lookup"><span data-stu-id="fd9b2-115">The activation value.</span></span> <span data-ttu-id="fd9b2-116">Cette valeur peut être l’un des types de **variantes** suivants : VT **\_ tableau** VT \| **\_ UI1** (octets bruts), **VT \_ BSTR** (chaîne), **VT \_ I4** (entier) ou **VT \_ bool** (booléen).</span><span class="sxs-lookup"><span data-stu-id="fd9b2-116">This value can be one of the following **VARIANT** types: **VT\_ARRAY** \| **VT\_UI1** (raw bytes), **VT\_BSTR** (string), **VT\_I4** (integer), or **VT\_BOOL** (Boolean).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd9b2-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fd9b2-117">Return value</span></span>

<span data-ttu-id="fd9b2-118">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="fd9b2-118">This method can return one of these values.</span></span>



| <span data-ttu-id="fd9b2-119">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="fd9b2-119">Return code/value</span></span>                                                                                                                                                      | <span data-ttu-id="fd9b2-120">Description</span><span class="sxs-lookup"><span data-stu-id="fd9b2-120">Description</span></span>                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fd9b2-121"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="fd9b2-121"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="fd9b2-122">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="fd9b2-122">The operation was successful.</span></span><br/>                                                |
| <dl> <span data-ttu-id="fd9b2-123"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="fd9b2-123"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>           | <span data-ttu-id="fd9b2-124">Le paramètre *clé* est **null** ou vide.</span><span class="sxs-lookup"><span data-stu-id="fd9b2-124">The *activationKey* parameter is **NULL** or empty.</span></span><br/>                          |
| <dl> <span data-ttu-id="fd9b2-125"><dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="fd9b2-125"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="fd9b2-126">Le paramètre *activationValue* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="fd9b2-126">The *activationValue* parameter is **NULL**.</span></span><br/>                                 |
| <dl> <span data-ttu-id="fd9b2-127"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="fd9b2-127"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="fd9b2-128">La configuration est inconnue.</span><span class="sxs-lookup"><span data-stu-id="fd9b2-128">The configuration is unknown.</span></span><br/>                                                |
| <dl> <span data-ttu-id="fd9b2-129"><dt>**Ordinateur virtuel \_ E \_ Préférences \_ \_ introuvables**</dt> <dt>0xA0040300</dt></span><span class="sxs-lookup"><span data-stu-id="fd9b2-129"><dt>**VM\_E\_PREF\_NOT\_FOUND**</dt> <dt>0xA0040300</dt></span></span> </dl> | <span data-ttu-id="fd9b2-130">La préférence est introuvable, ou cette configuration n’a pas d’activation valide.</span><span class="sxs-lookup"><span data-stu-id="fd9b2-130">The preference was not found, or this configuration has no valid activation.</span></span><br/> |
| <dl> <span data-ttu-id="fd9b2-131"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="fd9b2-131"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="fd9b2-132">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="fd9b2-132">An unexpected error has occurred.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="fd9b2-133">Notes</span><span class="sxs-lookup"><span data-stu-id="fd9b2-133">Remarks</span></span>

<span data-ttu-id="fd9b2-134">Cette méthode fournit un accès de bas niveau à toute valeur d’activation.</span><span class="sxs-lookup"><span data-stu-id="fd9b2-134">This method provides low-level access to any activation value.</span></span> <span data-ttu-id="fd9b2-135">Il peut être utilisé pour définir des valeurs d’activation pour les clés définies par le client.</span><span class="sxs-lookup"><span data-stu-id="fd9b2-135">It can be used to set activation values for customer-defined keys.</span></span> <span data-ttu-id="fd9b2-136">Lorsqu’un ordinateur virtuel est démarré, une copie de ses valeurs de configuration est créée, qui devient son ensemble de valeurs d’activation.</span><span class="sxs-lookup"><span data-stu-id="fd9b2-136">When a virtual machine is started, a copy is made of its configuration values, which becomes its set of activation values.</span></span> <span data-ttu-id="fd9b2-137">Les valeurs d’activation sont conservées jusqu’à ce que la machine virtuelle soit arrêtée ou redémarrée.</span><span class="sxs-lookup"><span data-stu-id="fd9b2-137">Activation values are maintained until the virtual machine is shut down or restarted.</span></span> <span data-ttu-id="fd9b2-138">Notez que Windows Virtual PC peut uniquement utiliser la configuration pour stocker des valeurs pour certaines clés, autrement dit, la valeur d’activation peut ne jamais être utilisée.</span><span class="sxs-lookup"><span data-stu-id="fd9b2-138">Note that Windows Virtual PC may only use the configuration to store values for certain keys, that is, the activation value may never be used.</span></span>

<span data-ttu-id="fd9b2-139">Les clés d’activation sont stockées en interne de manière hiérarchique, de la même façon que les clés de Registre dans Windows.</span><span class="sxs-lookup"><span data-stu-id="fd9b2-139">Activation keys are stored internally in a hierarchical manner similar to the registry keys in Windows.</span></span> <span data-ttu-id="fd9b2-140">Pour spécifier une sous-clé spécifique, un « chemin d’accès de clé » est construit, qui spécifie les différentes clés dans un format délimité par des barres obliques.</span><span class="sxs-lookup"><span data-stu-id="fd9b2-140">To specify a specific subkey, a "key path" is constructed which specifies the various keys in a slash mark delimited format.</span></span>

<span data-ttu-id="fd9b2-141">Par exemple, pour lire la valeur de la clé « \_ action par défaut » située dans l’arborescence de clé suivante :</span><span class="sxs-lookup"><span data-stu-id="fd9b2-141">For example, to read the value of the "default\_action" key located in the following key tree:</span></span>

``` syntax
<settings>
    <undo_drives>
        <default_action type="integer">1</default_action>
```

<span data-ttu-id="fd9b2-142">La chaîne de chemin d’accès *clé* est spécifiée comme suit :</span><span class="sxs-lookup"><span data-stu-id="fd9b2-142">The *activationKey* path string would be specified as follows:</span></span>

``` syntax
"settings/undo_drives/default_action"
```

## <a name="requirements"></a><span data-ttu-id="fd9b2-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fd9b2-143">Requirements</span></span>



| <span data-ttu-id="fd9b2-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fd9b2-144">Requirement</span></span> | <span data-ttu-id="fd9b2-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd9b2-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd9b2-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd9b2-146">Minimum supported client</span></span><br/> | <span data-ttu-id="fd9b2-147">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fd9b2-147">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fd9b2-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd9b2-148">Minimum supported server</span></span><br/> | <span data-ttu-id="fd9b2-149">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd9b2-149">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="fd9b2-150">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="fd9b2-150">End of client support</span></span><br/>    | <span data-ttu-id="fd9b2-151">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fd9b2-151">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="fd9b2-152">Produit</span><span class="sxs-lookup"><span data-stu-id="fd9b2-152">Product</span></span><br/>                  | <span data-ttu-id="fd9b2-153">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="fd9b2-153">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="fd9b2-154">En-tête</span><span class="sxs-lookup"><span data-stu-id="fd9b2-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd9b2-155"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd9b2-155"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="fd9b2-156">IID</span><span class="sxs-lookup"><span data-stu-id="fd9b2-156">IID</span></span><br/>                      | <span data-ttu-id="fd9b2-157">IID \_ IVMVirtualMachine est défini en tant que f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="fd9b2-157">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="fd9b2-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd9b2-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd9b2-159">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="fd9b2-159">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

