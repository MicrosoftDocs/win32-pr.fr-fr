---
title: Méthode IVMVirtualMachine DiscardSavedState (VPCCOMInterfaces. h)
description: Ignore toutes les informations d’état enregistrées pour un ordinateur virtuel enregistré.
ms.assetid: 546d6ea9-bfa3-487d-a333-399986bdf9a1
keywords:
- Méthode DiscardSavedState Virtual PC
- Méthode DiscardSavedState Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC, méthode DiscardSavedState
topic_type:
- apiref
api_name:
- IVMVirtualMachine.DiscardSavedState
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ce5c9cc0b07af2cc8c995d0c368d7747fa1475a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032989"
---
# <a name="ivmvirtualmachinediscardsavedstate-method"></a><span data-ttu-id="cf092-106">IVMVirtualMachine ::D méthode iscardSavedState</span><span class="sxs-lookup"><span data-stu-id="cf092-106">IVMVirtualMachine::DiscardSavedState method</span></span>

<span data-ttu-id="cf092-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="cf092-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="cf092-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="cf092-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="cf092-109">Ignore toutes les informations d’état enregistrées pour un ordinateur virtuel enregistré.</span><span class="sxs-lookup"><span data-stu-id="cf092-109">Discards any saved state information for a saved virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf092-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cf092-110">Syntax</span></span>


```C++
HRESULT DiscardSavedState();
```



## <a name="parameters"></a><span data-ttu-id="cf092-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cf092-111">Parameters</span></span>

<span data-ttu-id="cf092-112">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="cf092-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cf092-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cf092-113">Return value</span></span>

<span data-ttu-id="cf092-114">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="cf092-114">This method can return one of these values.</span></span>



| <span data-ttu-id="cf092-115">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="cf092-115">Return code/value</span></span>                                                                                                                                                           | <span data-ttu-id="cf092-116">Description</span><span class="sxs-lookup"><span data-stu-id="cf092-116">Description</span></span>                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cf092-117"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="cf092-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                 | <span data-ttu-id="cf092-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="cf092-118">The operation was successful.</span></span><br/>                               |
| <dl> <span data-ttu-id="cf092-119"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="cf092-119"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>           | <span data-ttu-id="cf092-120">La configuration est inconnue.</span><span class="sxs-lookup"><span data-stu-id="cf092-120">The configuration is unknown.</span></span><br/>                               |
| <dl> <span data-ttu-id="cf092-121"><dt>**Ordinateur virtuel \_ \_Machine virtuelle E \_ exécutant**</dt> <dt>0xA0040500</dt></span><span class="sxs-lookup"><span data-stu-id="cf092-121"><dt>**VM\_E\_VM\_RUNNING**</dt> <dt>0xA0040500</dt></span></span> </dl>           | <span data-ttu-id="cf092-122">La machine virtuelle est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="cf092-122">The virtual machine is running.</span></span><br/>                             |
| <dl> <span data-ttu-id="cf092-123"><dt>**Ordinateur virtuel \_ E \_ VM \_ sans \_ \_ état enregistré**</dt> <dt>0xA00400501</dt></span><span class="sxs-lookup"><span data-stu-id="cf092-123"><dt>**VM\_E\_VM\_NO\_SAVED\_STATE**</dt> <dt>0xA00400501</dt></span></span> </dl> | <span data-ttu-id="cf092-124">L’ordinateur virtuel n’est pas en cours d’exécution, mais il n’a pas d’état enregistré.</span><span class="sxs-lookup"><span data-stu-id="cf092-124">The virtual machine is not running, but has no saved state.</span></span><br/> |
| <dl> <span data-ttu-id="cf092-125"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="cf092-125"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>           | <span data-ttu-id="cf092-126">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="cf092-126">An unexpected error has occurred.</span></span><br/>                           |



 

## <a name="requirements"></a><span data-ttu-id="cf092-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cf092-127">Requirements</span></span>



| <span data-ttu-id="cf092-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cf092-128">Requirement</span></span> | <span data-ttu-id="cf092-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="cf092-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf092-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cf092-130">Minimum supported client</span></span><br/> | <span data-ttu-id="cf092-131">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cf092-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cf092-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cf092-132">Minimum supported server</span></span><br/> | <span data-ttu-id="cf092-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="cf092-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="cf092-134">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="cf092-134">End of client support</span></span><br/>    | <span data-ttu-id="cf092-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="cf092-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="cf092-136">Produit</span><span class="sxs-lookup"><span data-stu-id="cf092-136">Product</span></span><br/>                  | <span data-ttu-id="cf092-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="cf092-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="cf092-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="cf092-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf092-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf092-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="cf092-140">IID</span><span class="sxs-lookup"><span data-stu-id="cf092-140">IID</span></span><br/>                      | <span data-ttu-id="cf092-141">IID \_ IVMVirtualMachine est défini en tant que f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="cf092-141">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="cf092-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cf092-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf092-143">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="cf092-143">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

