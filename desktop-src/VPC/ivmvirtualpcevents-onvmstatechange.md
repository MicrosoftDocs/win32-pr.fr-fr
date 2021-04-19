---
title: Méthode IVMVirtualPCEvents OnVMStateChange (VPCCOMInterfaces. h)
description: Reçoit une notification indiquant que l’état d’une machine virtuelle a changé. | Méthode IVMVirtualPCEvents OnVMStateChange (VPCCOMInterfaces. h)
ms.assetid: a79afe14-9b7d-4528-ad38-e9b5ad068561
keywords:
- Méthode OnVMStateChange Virtual PC
- Méthode OnVMStateChange Virtual PC, interface IVMVirtualPCEvents
- IVMVirtualPCEvents interface Virtual PC, méthode OnVMStateChange
topic_type:
- apiref
api_name:
- IVMVirtualPCEvents.OnVMStateChange
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2d0a8bd9a362c558c307fb4719c95a9ba8cbf4a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106538291"
---
# <a name="ivmvirtualpceventsonvmstatechange-method"></a><span data-ttu-id="32e13-107">IVMVirtualPCEvents :: OnVMStateChange, méthode</span><span class="sxs-lookup"><span data-stu-id="32e13-107">IVMVirtualPCEvents::OnVMStateChange method</span></span>

<span data-ttu-id="32e13-108">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="32e13-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="32e13-109">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="32e13-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="32e13-110">Reçoit une notification indiquant que l’état d’une machine virtuelle a changé.</span><span class="sxs-lookup"><span data-stu-id="32e13-110">Receives notification that a virtual machine's state has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="32e13-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="32e13-111">Syntax</span></span>


```C++
HRESULT OnVMStateChange(
  [in] BSTR      virtualMachineConfig,
  [in] VMVMState virtualMachineState
);
```



## <a name="parameters"></a><span data-ttu-id="32e13-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="32e13-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32e13-113">*virtualMachineConfig* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="32e13-113">*virtualMachineConfig* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32e13-114">Nom de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="32e13-114">The name of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="32e13-115">*virtualMachineState* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="32e13-115">*virtualMachineState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32e13-116">Nouvel état de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="32e13-116">The new state of the virtual machine.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32e13-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="32e13-117">Return value</span></span>

<span data-ttu-id="32e13-118">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="32e13-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="32e13-119">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="32e13-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="32e13-120">Notes</span><span class="sxs-lookup"><span data-stu-id="32e13-120">Remarks</span></span>

<span data-ttu-id="32e13-121">Le programme client doit implémenter cette méthode d’interface pour recevoir la notification de l’événement **vmVirtualPCEvent \_ VMStateChanged** provenant de [**IVMVirtualPC**](ivmvirtualpc.md).</span><span class="sxs-lookup"><span data-stu-id="32e13-121">The client program must implement this interface method to receive notification of the **vmVirtualPCEvent\_VMStateChanged** event originating from [**IVMVirtualPC**](ivmvirtualpc.md).</span></span> <span data-ttu-id="32e13-122">Pour surveiller un ordinateur virtuel spécifique, utilisez la méthode [**IVMVirtualMachineEvents :: OnStateChange**](ivmvirtualmachineevents-onstatechange.md) .</span><span class="sxs-lookup"><span data-stu-id="32e13-122">To monitor a specific virtual machine, use the [**IVMVirtualMachineEvents::OnStateChange**](ivmvirtualmachineevents-onstatechange.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="32e13-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="32e13-123">Requirements</span></span>



| <span data-ttu-id="32e13-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="32e13-124">Requirement</span></span> | <span data-ttu-id="32e13-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="32e13-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="32e13-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="32e13-126">Minimum supported client</span></span><br/> | <span data-ttu-id="32e13-127">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="32e13-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="32e13-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="32e13-128">Minimum supported server</span></span><br/> | <span data-ttu-id="32e13-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="32e13-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="32e13-130">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="32e13-130">End of client support</span></span><br/>    | <span data-ttu-id="32e13-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="32e13-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="32e13-132">Produit</span><span class="sxs-lookup"><span data-stu-id="32e13-132">Product</span></span><br/>                  | <span data-ttu-id="32e13-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="32e13-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="32e13-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="32e13-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="32e13-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="32e13-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="32e13-136">IID</span><span class="sxs-lookup"><span data-stu-id="32e13-136">IID</span></span><br/>                      | <span data-ttu-id="32e13-137">DIID \_ IVMVirtualPCEvents est défini comme efed1ef1-3c09-41f7-a9c2-7e29fa286c9d</span><span class="sxs-lookup"><span data-stu-id="32e13-137">DIID\_IVMVirtualPCEvents is defined as efed1ef1-3c09-41f7-a9c2-7e29fa286c9d</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="32e13-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="32e13-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32e13-139">**IVMVirtualPCEvents**</span><span class="sxs-lookup"><span data-stu-id="32e13-139">**IVMVirtualPCEvents**</span></span>](ivmvirtualpcevents.md)
</dt> </dl>

 

