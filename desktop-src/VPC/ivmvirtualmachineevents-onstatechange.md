---
title: Méthode IVMVirtualMachineEvents OnStateChange (VPCCOMInterfaces. h)
description: Reçoit une notification indiquant que l’état d’une machine virtuelle a changé. | Méthode IVMVirtualMachineEvents OnStateChange (VPCCOMInterfaces. h)
ms.assetid: 1737bb5e-078d-4ebe-9558-de083aae1baa
keywords:
- Méthode OnStateChange Virtual PC
- Méthode OnStateChange Virtual PC, interface IVMVirtualMachineEvents
- IVMVirtualMachineEvents interface Virtual PC, méthode OnStateChange
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnStateChange
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7da112d8f6211882953056afef0219b9efdf9843
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322505"
---
# <a name="ivmvirtualmachineeventsonstatechange-method"></a><span data-ttu-id="7e30a-107">IVMVirtualMachineEvents :: OnStateChange, méthode</span><span class="sxs-lookup"><span data-stu-id="7e30a-107">IVMVirtualMachineEvents::OnStateChange method</span></span>

<span data-ttu-id="7e30a-108">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7e30a-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7e30a-109">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7e30a-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7e30a-110">Reçoit une notification indiquant que l’état d’une machine virtuelle a changé.</span><span class="sxs-lookup"><span data-stu-id="7e30a-110">Receives notification that a virtual machine's state has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e30a-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7e30a-111">Syntax</span></span>


```C++
HRESULT OnStateChange(
  [in] VMVMState virtualMachineState
);
```



## <a name="parameters"></a><span data-ttu-id="7e30a-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7e30a-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e30a-113">*virtualMachineState* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7e30a-113">*virtualMachineState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e30a-114">Nouvel état de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="7e30a-114">The new state of the virtual machine.</span></span> <span data-ttu-id="7e30a-115">Pour obtenir la liste des valeurs, consultez [**VMVMState**](vmvmstate.md).</span><span class="sxs-lookup"><span data-stu-id="7e30a-115">For a list of values, see [**VMVMState**](vmvmstate.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e30a-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7e30a-116">Return value</span></span>

<span data-ttu-id="7e30a-117">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="7e30a-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7e30a-118">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7e30a-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e30a-119">Notes</span><span class="sxs-lookup"><span data-stu-id="7e30a-119">Remarks</span></span>

<span data-ttu-id="7e30a-120">Cette méthode est appelée lorsque l’état de cet ordinateur virtuel change.</span><span class="sxs-lookup"><span data-stu-id="7e30a-120">This method is called when the state for this virtual machine changes.</span></span> <span data-ttu-id="7e30a-121">Le programme client doit implémenter cette méthode d’interface pour recevoir la notification de l' \_ événement vmVirtualMachineEvent StateChanged provenant de [**IVMVirtualMachine**](ivmvirtualmachine.md).</span><span class="sxs-lookup"><span data-stu-id="7e30a-121">The client program must implement this interface method to receive notification of the vmVirtualMachineEvent\_StateChanged event originating from [**IVMVirtualMachine**](ivmvirtualmachine.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7e30a-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7e30a-122">Requirements</span></span>



| <span data-ttu-id="7e30a-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7e30a-123">Requirement</span></span> | <span data-ttu-id="7e30a-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="7e30a-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e30a-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e30a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="7e30a-126">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7e30a-126">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7e30a-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e30a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="7e30a-128">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e30a-128">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7e30a-129">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="7e30a-129">End of client support</span></span><br/>    | <span data-ttu-id="7e30a-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7e30a-130">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7e30a-131">Produit</span><span class="sxs-lookup"><span data-stu-id="7e30a-131">Product</span></span><br/>                  | <span data-ttu-id="7e30a-132">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7e30a-132">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7e30a-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="7e30a-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e30a-134"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e30a-134"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="7e30a-135">IID</span><span class="sxs-lookup"><span data-stu-id="7e30a-135">IID</span></span><br/>                      | <span data-ttu-id="7e30a-136">DIID \_ IVMVirtualMachineEvents est défini comme 9d84f560-bb67-4961-BD12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="7e30a-136">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="7e30a-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7e30a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e30a-138">**IVMVirtualMachineEvents**</span><span class="sxs-lookup"><span data-stu-id="7e30a-138">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

