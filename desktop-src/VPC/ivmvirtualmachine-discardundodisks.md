---
title: Méthode IVMVirtualMachine DiscardUndoDisks (VPCCOMInterfaces. h)
description: Ignore les disques d’annulations virtuelles.
ms.assetid: 5c3a4b3f-ea58-498c-b7cf-54f028fa061c
keywords:
- Méthode DiscardUndoDisks Virtual PC
- Méthode DiscardUndoDisks Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC, méthode DiscardUndoDisks
topic_type:
- apiref
api_name:
- IVMVirtualMachine.DiscardUndoDisks
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d548b69a6cfebc383a0233f01ef19ad14d051474
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465526"
---
# <a name="ivmvirtualmachinediscardundodisks-method"></a><span data-ttu-id="40b42-106">IVMVirtualMachine ::D méthode iscardUndoDisks</span><span class="sxs-lookup"><span data-stu-id="40b42-106">IVMVirtualMachine::DiscardUndoDisks method</span></span>

<span data-ttu-id="40b42-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="40b42-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="40b42-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="40b42-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="40b42-109">Ignore les disques d’annulations virtuelles.</span><span class="sxs-lookup"><span data-stu-id="40b42-109">Discards the virtual undo disks.</span></span>

## <a name="syntax"></a><span data-ttu-id="40b42-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="40b42-110">Syntax</span></span>


```C++
HRESULT DiscardUndoDisks();
```



## <a name="parameters"></a><span data-ttu-id="40b42-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="40b42-111">Parameters</span></span>

<span data-ttu-id="40b42-112">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="40b42-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="40b42-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="40b42-113">Return value</span></span>

<span data-ttu-id="40b42-114">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="40b42-114">This method can return one of these values.</span></span>



| <span data-ttu-id="40b42-115">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="40b42-115">Return code/value</span></span>                                                                                                                                                            | <span data-ttu-id="40b42-116">Description</span><span class="sxs-lookup"><span data-stu-id="40b42-116">Description</span></span>                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="40b42-117"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="40b42-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="40b42-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="40b42-118">The operation was successful.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="40b42-119"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="40b42-119"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="40b42-120">La configuration est inconnue.</span><span class="sxs-lookup"><span data-stu-id="40b42-120">The configuration is unknown.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="40b42-121"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_ en cours d’exécution \_ ou \_**</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="40b42-121"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="40b42-122">Les disques d’annulations virtuelles ne peuvent pas être supprimés pendant que l’ordinateur virtuel est en cours d’exécution ou dans un état enregistré.</span><span class="sxs-lookup"><span data-stu-id="40b42-122">The virtual undo disks cannot be discarded while the virtual machine is running or in a saved state.</span></span><br/> |
| <dl> <span data-ttu-id="40b42-123"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="40b42-123"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="40b42-124">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="40b42-124">An unexpected error has occurred.</span></span><br/>                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="40b42-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="40b42-125">Requirements</span></span>



| <span data-ttu-id="40b42-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="40b42-126">Requirement</span></span> | <span data-ttu-id="40b42-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="40b42-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="40b42-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="40b42-128">Minimum supported client</span></span><br/> | <span data-ttu-id="40b42-129">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="40b42-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="40b42-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="40b42-130">Minimum supported server</span></span><br/> | <span data-ttu-id="40b42-131">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="40b42-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="40b42-132">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="40b42-132">End of client support</span></span><br/>    | <span data-ttu-id="40b42-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="40b42-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="40b42-134">Produit</span><span class="sxs-lookup"><span data-stu-id="40b42-134">Product</span></span><br/>                  | <span data-ttu-id="40b42-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="40b42-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="40b42-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="40b42-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="40b42-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="40b42-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="40b42-138">IID</span><span class="sxs-lookup"><span data-stu-id="40b42-138">IID</span></span><br/>                      | <span data-ttu-id="40b42-139">IID \_ IVMVirtualMachine est défini en tant que f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="40b42-139">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="40b42-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="40b42-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40b42-141">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="40b42-141">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

