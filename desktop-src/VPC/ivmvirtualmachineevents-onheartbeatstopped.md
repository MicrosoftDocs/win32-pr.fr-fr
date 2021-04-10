---
title: Méthode IVMVirtualMachineEvents OnHeartbeatStopped (VPCCOMInterfaces. h)
description: Reçoit une notification indiquant que la pulsation d’une machine virtuelle s’est arrêtée.
ms.assetid: 58fc81a8-747c-47f9-98ec-38482694f533
keywords:
- Méthode OnHeartbeatStopped Virtual PC
- Méthode OnHeartbeatStopped Virtual PC, interface IVMVirtualMachineEvents
- IVMVirtualMachineEvents interface Virtual PC, méthode OnHeartbeatStopped
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnHeartbeatStopped
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ade783d2d182439d5c500dcc114c74c8278ba6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942611"
---
# <a name="ivmvirtualmachineeventsonheartbeatstopped-method"></a><span data-ttu-id="bebf7-106">IVMVirtualMachineEvents :: OnHeartbeatStopped, méthode</span><span class="sxs-lookup"><span data-stu-id="bebf7-106">IVMVirtualMachineEvents::OnHeartbeatStopped method</span></span>

<span data-ttu-id="bebf7-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="bebf7-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="bebf7-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="bebf7-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="bebf7-109">Reçoit une notification indiquant que la pulsation d’une machine virtuelle s’est arrêtée.</span><span class="sxs-lookup"><span data-stu-id="bebf7-109">Receives notification that a virtual machine's heartbeat has stopped.</span></span>

## <a name="syntax"></a><span data-ttu-id="bebf7-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bebf7-110">Syntax</span></span>


```C++
HRESULT OnHeartbeatStopped();
```



## <a name="parameters"></a><span data-ttu-id="bebf7-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bebf7-111">Parameters</span></span>

<span data-ttu-id="bebf7-112">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="bebf7-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bebf7-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bebf7-113">Return value</span></span>

<span data-ttu-id="bebf7-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="bebf7-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bebf7-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bebf7-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bebf7-116">Notes</span><span class="sxs-lookup"><span data-stu-id="bebf7-116">Remarks</span></span>

<span data-ttu-id="bebf7-117">Cette méthode est appelée lorsque le système d’exploitation invité de cet ordinateur virtuel s’est arrêté brutalement.</span><span class="sxs-lookup"><span data-stu-id="bebf7-117">This method is called when the guest operating system for this virtual machine has stopped abruptly.</span></span> <span data-ttu-id="bebf7-118">Le programme client doit implémenter cette méthode d’interface pour recevoir la notification de l' \_ événement vmVirtualMachineEvent HeartbeatStopped provenant de [**IVMVirtualMachine**](ivmvirtualmachine.md).</span><span class="sxs-lookup"><span data-stu-id="bebf7-118">The client program must implement this interface method to receive notification of the vmVirtualMachineEvent\_HeartbeatStopped event originating from [**IVMVirtualMachine**](ivmvirtualmachine.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bebf7-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bebf7-119">Requirements</span></span>



| <span data-ttu-id="bebf7-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bebf7-120">Requirement</span></span> | <span data-ttu-id="bebf7-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="bebf7-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bebf7-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bebf7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bebf7-123">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bebf7-123">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bebf7-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bebf7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bebf7-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="bebf7-125">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="bebf7-126">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="bebf7-126">End of client support</span></span><br/>    | <span data-ttu-id="bebf7-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bebf7-127">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="bebf7-128">Produit</span><span class="sxs-lookup"><span data-stu-id="bebf7-128">Product</span></span><br/>                  | <span data-ttu-id="bebf7-129">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="bebf7-129">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="bebf7-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="bebf7-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="bebf7-131"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="bebf7-131"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="bebf7-132">IID</span><span class="sxs-lookup"><span data-stu-id="bebf7-132">IID</span></span><br/>                      | <span data-ttu-id="bebf7-133">DIID \_ IVMVirtualMachineEvents est défini comme 9d84f560-bb67-4961-BD12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="bebf7-133">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="bebf7-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bebf7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bebf7-135">**IVMVirtualMachineEvents**</span><span class="sxs-lookup"><span data-stu-id="bebf7-135">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

