---
title: Méthode IVMVirtualMachineEvents OnDiskOutOfSpace (VPCCOMInterfaces. h)
description: Reçoit une notification indiquant qu’un disque requis pour une machine virtuelle ne dispose pas de suffisamment d’espace libre.
ms.assetid: 1c431904-fffd-4513-8670-b9723f53edf1
keywords:
- Méthode OnDiskOutOfSpace Virtual PC
- Méthode OnDiskOutOfSpace Virtual PC, interface IVMVirtualMachineEvents
- IVMVirtualMachineEvents interface Virtual PC, méthode OnDiskOutOfSpace
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnDiskOutOfSpace
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ac2d5f45068dc8cd7341d0a599b2da4e5c7655a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843034"
---
# <a name="ivmvirtualmachineeventsondiskoutofspace-method"></a><span data-ttu-id="53331-106">IVMVirtualMachineEvents :: OnDiskOutOfSpace, méthode</span><span class="sxs-lookup"><span data-stu-id="53331-106">IVMVirtualMachineEvents::OnDiskOutOfSpace method</span></span>

<span data-ttu-id="53331-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="53331-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="53331-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="53331-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="53331-109">Reçoit une notification indiquant qu’un disque requis pour un ordinateur virtuel ne dispose pas de suffisamment d’espace libre.</span><span class="sxs-lookup"><span data-stu-id="53331-109">Receives notification that a disk required for a virtual machine (VM) is low on free space.</span></span> <span data-ttu-id="53331-110">Si l’espace libre descend en dessous de 100 Mo, cet événement est reçu en tant qu’avertissement et si l’espace libre descend en dessous de 20 Mo, cet événement est de nouveau reçu en tant qu’erreur et la machine virtuelle est suspendue.</span><span class="sxs-lookup"><span data-stu-id="53331-110">If free space drops below 100 MB this event is received as a warning and if free space drops below 20 MB this event is received again as an error and the VM will be paused.</span></span>

## <a name="syntax"></a><span data-ttu-id="53331-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="53331-111">Syntax</span></span>


```C++
HRESULT OnDiskOutOfSpace(
  [in] VARIANT_BOOL criticallyLow
);
```



## <a name="parameters"></a><span data-ttu-id="53331-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="53331-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53331-113">*criticallyLow* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="53331-113">*criticallyLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53331-114">Affectez la valeur **Variant \_ true** si le disque dispose de moins de 20 Mo de libre et la **\_ valeur false** si l’espace libre est supérieur à 20 Mo mais inférieur à 100 Mo.</span><span class="sxs-lookup"><span data-stu-id="53331-114">Set to **VARIANT\_TRUE** if the disk has less than 20 MB free and to **VARIANT\_FALSE** if the free space is more than 20 MB but less than 100 MB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53331-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="53331-115">Return value</span></span>

<span data-ttu-id="53331-116">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="53331-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="53331-117">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="53331-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="53331-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="53331-118">Requirements</span></span>



| <span data-ttu-id="53331-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="53331-119">Requirement</span></span> | <span data-ttu-id="53331-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="53331-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="53331-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53331-121">Minimum supported client</span></span><br/> | <span data-ttu-id="53331-122">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="53331-122">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="53331-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53331-123">Minimum supported server</span></span><br/> | <span data-ttu-id="53331-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="53331-124">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="53331-125">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="53331-125">End of client support</span></span><br/>    | <span data-ttu-id="53331-126">Windows 7</span><span class="sxs-lookup"><span data-stu-id="53331-126">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="53331-127">Produit</span><span class="sxs-lookup"><span data-stu-id="53331-127">Product</span></span><br/>                  | <span data-ttu-id="53331-128">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="53331-128">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="53331-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="53331-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="53331-130"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="53331-130"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="53331-131">IID</span><span class="sxs-lookup"><span data-stu-id="53331-131">IID</span></span><br/>                      | <span data-ttu-id="53331-132">DIID \_ IVMVirtualMachineEvents est défini comme 9d84f560-bb67-4961-BD12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="53331-132">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="53331-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53331-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53331-134">**IVMVirtualMachineEvents**</span><span class="sxs-lookup"><span data-stu-id="53331-134">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

