---
title: Méthode IVMVirtualPC FindVirtualMachine (VPCCOMInterfaces. h)
description: Récupère un objet ordinateur virtuel qui correspond à la configuration demandée.
ms.assetid: 1c73d6f7-5662-485e-a864-e8e48197f8e4
keywords:
- Méthode FindVirtualMachine Virtual PC
- Méthode FindVirtualMachine Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface Virtual PC, méthode FindVirtualMachine
topic_type:
- apiref
api_name:
- IVMVirtualPC.FindVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc5e5702738e16fa7b4f4a263264b0574966d1fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105202"
---
# <a name="ivmvirtualpcfindvirtualmachine-method"></a><span data-ttu-id="4cae3-106">IVMVirtualPC :: FindVirtualMachine, méthode</span><span class="sxs-lookup"><span data-stu-id="4cae3-106">IVMVirtualPC::FindVirtualMachine method</span></span>

<span data-ttu-id="4cae3-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4cae3-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4cae3-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4cae3-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4cae3-109">Récupère un objet ordinateur virtuel qui correspond à la configuration demandée.</span><span class="sxs-lookup"><span data-stu-id="4cae3-109">Retrieves a virtual machine object that matches the requested configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cae3-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4cae3-110">Syntax</span></span>


```C++
HRESULT FindVirtualMachine(
  [in]          BSTR              configurationName,
  [out, retval] IVMVirtualMachine **virtualMachine
);
```



## <a name="parameters"></a><span data-ttu-id="4cae3-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4cae3-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cae3-112">*ConfigurationName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4cae3-112">*configurationName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cae3-113">Nom de l’ordinateur virtuel à trouver.</span><span class="sxs-lookup"><span data-stu-id="4cae3-113">The name of the virtual machine to be found.</span></span>

</dd> <dt>

<span data-ttu-id="4cae3-114">*VirtualMachine* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="4cae3-114">*virtualMachine* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="4cae3-115">Pointeur vers un nouvel objet [**IVMVirtualMachine**](ivmvirtualmachine.md) qui représente cet ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="4cae3-115">A pointer to a new [**IVMVirtualMachine**](ivmvirtualmachine.md) object that represents this virtual machine.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cae3-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4cae3-116">Return value</span></span>

<span data-ttu-id="4cae3-117">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="4cae3-117">This method can return one of these values.</span></span>



| <span data-ttu-id="4cae3-118">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="4cae3-118">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="4cae3-119">Description</span><span class="sxs-lookup"><span data-stu-id="4cae3-119">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4cae3-120"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4cae3-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="4cae3-121">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="4cae3-121">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="4cae3-122"><dt>**S \_ FALSe**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="4cae3-122"><dt>**S\_FALSE**</dt> <dt>1</dt></span></span> </dl>                                           | <span data-ttu-id="4cae3-123">La configuration spécifiée est introuvable.</span><span class="sxs-lookup"><span data-stu-id="4cae3-123">The specified configuration could not be found.</span></span><br/>                                      |
| <dl> <span data-ttu-id="4cae3-124"><dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="4cae3-124"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="4cae3-125">Le paramètre *ConfigurationName* n’est pas valide, ou *VirtualMachine* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="4cae3-125">The *configurationName* parameter is invalid, or *virtualMachine* is **NULL**.</span></span><br/>       |
| <dl> <span data-ttu-id="4cae3-126"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="4cae3-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="4cae3-127">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="4cae3-127">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="4cae3-128"><dt>**Ordinateur virtuel \_ \_Virtualisation matérielle E \_ \_ désactivée**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="4cae3-128"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="4cae3-129">Le processeur ne prend pas en charge les extensions avez (Hardware Accelerated Virtualization).</span><span class="sxs-lookup"><span data-stu-id="4cae3-129">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4cae3-130">Notes</span><span class="sxs-lookup"><span data-stu-id="4cae3-130">Remarks</span></span>

<span data-ttu-id="4cae3-131">Les noms de machine virtuelle ne respectent pas la casse, par exemple, « MyVM » et « MyVM » font référence à la même machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="4cae3-131">Virtual machine names are case-insensitive, for example, "MyVM" and "myvm" refer to the same virtual machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cae3-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4cae3-132">Requirements</span></span>



| <span data-ttu-id="4cae3-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4cae3-133">Requirement</span></span> | <span data-ttu-id="4cae3-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="4cae3-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cae3-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4cae3-135">Minimum supported client</span></span><br/> | <span data-ttu-id="4cae3-136">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4cae3-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4cae3-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4cae3-137">Minimum supported server</span></span><br/> | <span data-ttu-id="4cae3-138">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="4cae3-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4cae3-139">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="4cae3-139">End of client support</span></span><br/>    | <span data-ttu-id="4cae3-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4cae3-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4cae3-141">Produit</span><span class="sxs-lookup"><span data-stu-id="4cae3-141">Product</span></span><br/>                  | <span data-ttu-id="4cae3-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4cae3-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4cae3-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="4cae3-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="4cae3-144"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="4cae3-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4cae3-145">IID</span><span class="sxs-lookup"><span data-stu-id="4cae3-145">IID</span></span><br/>                      | <span data-ttu-id="4cae3-146">IID \_ IVMVirtualPC est défini en tant que 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="4cae3-146">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="4cae3-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4cae3-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cae3-148">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="4cae3-148">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

