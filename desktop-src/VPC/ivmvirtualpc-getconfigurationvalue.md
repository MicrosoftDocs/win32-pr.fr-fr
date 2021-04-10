---
title: Méthode IVMVirtualPC GetConfigurationValue (VPCCOMInterfaces. h)
description: Récupère la valeur du paramètre de configuration spécifié.
ms.assetid: 4598b57c-9942-4b40-97b5-41ad9ec74bfa
keywords:
- Méthode GetConfigurationValue Virtual PC
- Méthode GetConfigurationValue Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface Virtual PC, méthode GetConfigurationValue
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11851e2dc2e51c0dc5eed876fc755655ed488554
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105199"
---
# <a name="ivmvirtualpcgetconfigurationvalue-method"></a><span data-ttu-id="46441-106">IVMVirtualPC :: GetConfigurationValue, méthode</span><span class="sxs-lookup"><span data-stu-id="46441-106">IVMVirtualPC::GetConfigurationValue method</span></span>

<span data-ttu-id="46441-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="46441-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="46441-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="46441-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="46441-109">Récupère la valeur du paramètre de configuration spécifié.</span><span class="sxs-lookup"><span data-stu-id="46441-109">Retrieves the value of the specified configuration setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="46441-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="46441-110">Syntax</span></span>


```C++
HRESULT GetConfigurationValue(
  [in]          BSTR    preferenceKey,
  [out, retval] VARIANT *preferenceValue
);
```



## <a name="parameters"></a><span data-ttu-id="46441-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="46441-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46441-112">*preferenceKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="46441-112">*preferenceKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46441-113">Clé utilisée pour identifier la préférence, telle qu’elle est stockée dans le fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="46441-113">The key used to identify the preference, as stored in the configuration file.</span></span>

</dd> <dt>

<span data-ttu-id="46441-114">*preferenceValue* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="46441-114">*preferenceValue* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="46441-115">Valeur de préférence.</span><span class="sxs-lookup"><span data-stu-id="46441-115">The preference value.</span></span> <span data-ttu-id="46441-116">Ce paramètre peut être l’un des types de **variantes** suivants : VT **\_ Array** \| **VT \_ UI1** (RAW bytes), **VT \_ BSTR** (String), **VT \_ I4** (Integer) ou **VT \_ bool** (Boolean).</span><span class="sxs-lookup"><span data-stu-id="46441-116">This parameter may be one of the following **VARIANT** types: **VT\_ARRAY**\|**VT\_UI1** (raw bytes), **VT\_BSTR** (string), **VT\_I4** (integer), or **VT\_BOOL** (Boolean).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46441-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="46441-117">Return value</span></span>

<span data-ttu-id="46441-118">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="46441-118">This method can return one of these values.</span></span>



| <span data-ttu-id="46441-119">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="46441-119">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="46441-120">Description</span><span class="sxs-lookup"><span data-stu-id="46441-120">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="46441-121"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="46441-121"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="46441-122">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="46441-122">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="46441-123"><dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="46441-123"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="46441-124">Le paramètre *preferenceKey* ou *PreferenceValue* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="46441-124">The *preferenceKey* or *preferenceValue* parameter is **NULL**.</span></span><br/>                      |
| <dl> <span data-ttu-id="46441-125"><dt>**Ordinateur virtuel \_ E \_ Préférences \_ \_ introuvables**</dt> <dt>0xa0040300</dt></span><span class="sxs-lookup"><span data-stu-id="46441-125"><dt>**VM\_E\_PREF\_NOT\_FOUND**</dt> <dt>0xa0040300</dt></span></span> </dl>                   | <span data-ttu-id="46441-126">La préférence est introuvable.</span><span class="sxs-lookup"><span data-stu-id="46441-126">The preference was not found.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="46441-127"><dt>**Ordinateur virtuel \_ \_Virtualisation matérielle E \_ \_ désactivée**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="46441-127"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="46441-128">Le processeur ne prend pas en charge les extensions avez (Hardware Accelerated Virtualization).</span><span class="sxs-lookup"><span data-stu-id="46441-128">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |
| <dl> <span data-ttu-id="46441-129"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="46441-129"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="46441-130">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="46441-130">An unexpected error has occurred.</span></span><br/>                                                    |



 

## <a name="remarks"></a><span data-ttu-id="46441-131">Notes</span><span class="sxs-lookup"><span data-stu-id="46441-131">Remarks</span></span>

<span data-ttu-id="46441-132">Cette méthode fournit un accès de bas niveau à toute valeur de préférence pour l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="46441-132">This method provides low-level access to any preference value for the current user.</span></span> <span data-ttu-id="46441-133">Il peut être utilisé pour récupérer les valeurs de préférence pour les clés définies par le client.</span><span class="sxs-lookup"><span data-stu-id="46441-133">It can be used to retrieve preference values for customer-defined keys.</span></span>

## <a name="requirements"></a><span data-ttu-id="46441-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="46441-134">Requirements</span></span>



| <span data-ttu-id="46441-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="46441-135">Requirement</span></span> | <span data-ttu-id="46441-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="46441-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="46441-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="46441-137">Minimum supported client</span></span><br/> | <span data-ttu-id="46441-138">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="46441-138">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="46441-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="46441-139">Minimum supported server</span></span><br/> | <span data-ttu-id="46441-140">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="46441-140">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="46441-141">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="46441-141">End of client support</span></span><br/>    | <span data-ttu-id="46441-142">Windows 7</span><span class="sxs-lookup"><span data-stu-id="46441-142">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="46441-143">Produit</span><span class="sxs-lookup"><span data-stu-id="46441-143">Product</span></span><br/>                  | <span data-ttu-id="46441-144">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="46441-144">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="46441-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="46441-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="46441-146"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="46441-146"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="46441-147">IID</span><span class="sxs-lookup"><span data-stu-id="46441-147">IID</span></span><br/>                      | <span data-ttu-id="46441-148">IID \_ IVMVirtualPC est défini en tant que 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="46441-148">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="46441-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="46441-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46441-150">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="46441-150">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

