---
title: Méthode IVMVirtualPC RemoveConfigurationValue (VPCCOMInterfaces. h)
description: Supprime la valeur du paramètre de configuration spécifié.
ms.assetid: 07bafa5e-bf62-45bf-af4e-a66050f5afad
keywords:
- Méthode RemoveConfigurationValue Virtual PC
- Méthode RemoveConfigurationValue Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface Virtual PC, méthode RemoveConfigurationValue
topic_type:
- apiref
api_name:
- IVMVirtualPC.RemoveConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73821657ed7983e2d92fc379c3222f343763b3ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844053"
---
# <a name="ivmvirtualpcremoveconfigurationvalue-method"></a><span data-ttu-id="7da28-106">IVMVirtualPC :: RemoveConfigurationValue, méthode</span><span class="sxs-lookup"><span data-stu-id="7da28-106">IVMVirtualPC::RemoveConfigurationValue method</span></span>

<span data-ttu-id="7da28-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7da28-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7da28-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7da28-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7da28-109">Supprime la valeur du paramètre de configuration spécifié.</span><span class="sxs-lookup"><span data-stu-id="7da28-109">Removes the value of the specified configuration setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="7da28-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7da28-110">Syntax</span></span>


```C++
HRESULT RemoveConfigurationValue(
  [in] BSTR preferenceKey
);
```



## <a name="parameters"></a><span data-ttu-id="7da28-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7da28-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7da28-112">*preferenceKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7da28-112">*preferenceKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7da28-113">Clé utilisée pour identifier la préférence, telle qu’elle est stockée dans le fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="7da28-113">The key used to identify the preference, as stored in the configuration file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7da28-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7da28-114">Return value</span></span>

<span data-ttu-id="7da28-115">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="7da28-115">This method can return one of these values.</span></span>



| <span data-ttu-id="7da28-116">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="7da28-116">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="7da28-117">Description</span><span class="sxs-lookup"><span data-stu-id="7da28-117">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7da28-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7da28-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="7da28-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="7da28-119">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="7da28-120"><dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="7da28-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="7da28-121">Le paramètre *preferenceKey* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="7da28-121">The *preferenceKey* parameter is **NULL**.</span></span><br/>                                           |
| <dl> <span data-ttu-id="7da28-122"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="7da28-122"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                             | <span data-ttu-id="7da28-123">Le paramètre *preferenceKey* n’est pas valide ou est une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="7da28-123">The *preferenceKey* parameter is not valid or is an empty string.</span></span><br/>                    |
| <dl> <span data-ttu-id="7da28-124"><dt>**Ordinateur virtuel \_ E \_ Préférences \_ \_ introuvables**</dt> <dt>0xA0040300</dt></span><span class="sxs-lookup"><span data-stu-id="7da28-124"><dt>**VM\_E\_PREF\_NOT\_FOUND**</dt> <dt>0xA0040300</dt></span></span> </dl>                   | <span data-ttu-id="7da28-125">La préférence est introuvable.</span><span class="sxs-lookup"><span data-stu-id="7da28-125">The preference was not found.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="7da28-126"><dt>**Ordinateur virtuel \_ \_Virtualisation matérielle E \_ \_ désactivée**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="7da28-126"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="7da28-127">Le processeur ne prend pas en charge les extensions avez (Hardware Accelerated Virtualization).</span><span class="sxs-lookup"><span data-stu-id="7da28-127">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |
| <dl> <span data-ttu-id="7da28-128"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="7da28-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="7da28-129">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="7da28-129">An unexpected error has occurred.</span></span><br/>                                                    |



 

## <a name="remarks"></a><span data-ttu-id="7da28-130">Notes</span><span class="sxs-lookup"><span data-stu-id="7da28-130">Remarks</span></span>

<span data-ttu-id="7da28-131">Cette méthode fournit un accès de bas niveau à toute valeur de préférence pour l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="7da28-131">This method provides low-level access to any preference value for the current user.</span></span> <span data-ttu-id="7da28-132">Il peut être utilisé pour supprimer des valeurs de préférence pour les clés définies par le client.</span><span class="sxs-lookup"><span data-stu-id="7da28-132">It can be used to remove preference values for customer-defined keys.</span></span>

## <a name="requirements"></a><span data-ttu-id="7da28-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7da28-133">Requirements</span></span>



| <span data-ttu-id="7da28-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7da28-134">Requirement</span></span> | <span data-ttu-id="7da28-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="7da28-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7da28-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7da28-136">Minimum supported client</span></span><br/> | <span data-ttu-id="7da28-137">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7da28-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7da28-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7da28-138">Minimum supported server</span></span><br/> | <span data-ttu-id="7da28-139">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7da28-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7da28-140">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="7da28-140">End of client support</span></span><br/>    | <span data-ttu-id="7da28-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7da28-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7da28-142">Produit</span><span class="sxs-lookup"><span data-stu-id="7da28-142">Product</span></span><br/>                  | <span data-ttu-id="7da28-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7da28-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7da28-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="7da28-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="7da28-145"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="7da28-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="7da28-146">IID</span><span class="sxs-lookup"><span data-stu-id="7da28-146">IID</span></span><br/>                      | <span data-ttu-id="7da28-147">IID \_ IVMVirtualPC est défini en tant que 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="7da28-147">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="7da28-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7da28-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7da28-149">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="7da28-149">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

