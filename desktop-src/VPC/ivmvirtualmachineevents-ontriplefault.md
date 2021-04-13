---
title: Méthode IVMVirtualMachineEvents OnTripleFault (VPCCOMInterfaces. h)
description: Reçoit une notification indiquant qu’un ordinateur virtuel a une erreur triple.
ms.assetid: a17b1a05-3058-48ba-a196-7e9563f3e1c0
keywords:
- Méthode OnTripleFault Virtual PC
- Méthode OnTripleFault Virtual PC, interface IVMVirtualMachineEvents
- IVMVirtualMachineEvents interface Virtual PC, méthode OnTripleFault
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnTripleFault
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48d635b9009ecadecb7aed4a921a9c609ef69505
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509098"
---
# <a name="ivmvirtualmachineeventsontriplefault-method"></a><span data-ttu-id="d425e-106">IVMVirtualMachineEvents :: OnTripleFault, méthode</span><span class="sxs-lookup"><span data-stu-id="d425e-106">IVMVirtualMachineEvents::OnTripleFault method</span></span>

<span data-ttu-id="d425e-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d425e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d425e-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d425e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d425e-109">Reçoit une notification indiquant qu’un ordinateur virtuel a une erreur triple.</span><span class="sxs-lookup"><span data-stu-id="d425e-109">Receives notification that a virtual machine has triple-faulted.</span></span>

## <a name="syntax"></a><span data-ttu-id="d425e-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d425e-110">Syntax</span></span>


```C++
HRESULT OnTripleFault();
```



## <a name="parameters"></a><span data-ttu-id="d425e-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d425e-111">Parameters</span></span>

<span data-ttu-id="d425e-112">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="d425e-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d425e-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d425e-113">Return value</span></span>

<span data-ttu-id="d425e-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d425e-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d425e-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d425e-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d425e-116">Notes</span><span class="sxs-lookup"><span data-stu-id="d425e-116">Remarks</span></span>

<span data-ttu-id="d425e-117">Cette méthode est appelée lorsqu’un ordinateur virtuel a une erreur triple.</span><span class="sxs-lookup"><span data-stu-id="d425e-117">This method is called when a virtual machine has triple-faulted.</span></span> <span data-ttu-id="d425e-118">Le programme client doit implémenter cette méthode d’interface pour recevoir la notification de l' \_ événement vmVirtualMachineEvent TripleFault provenant de [**IVMVirtualMachine**](ivmvirtualmachine.md).</span><span class="sxs-lookup"><span data-stu-id="d425e-118">The client program must implement this interface method to receive notification of the vmVirtualMachineEvent\_TripleFault event originating from [**IVMVirtualMachine**](ivmvirtualmachine.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d425e-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d425e-119">Requirements</span></span>



| <span data-ttu-id="d425e-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d425e-120">Requirement</span></span> | <span data-ttu-id="d425e-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="d425e-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d425e-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d425e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d425e-123">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d425e-123">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d425e-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d425e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d425e-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d425e-125">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d425e-126">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="d425e-126">End of client support</span></span><br/>    | <span data-ttu-id="d425e-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d425e-127">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d425e-128">Produit</span><span class="sxs-lookup"><span data-stu-id="d425e-128">Product</span></span><br/>                  | <span data-ttu-id="d425e-129">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d425e-129">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d425e-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="d425e-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="d425e-131"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d425e-131"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d425e-132">IID</span><span class="sxs-lookup"><span data-stu-id="d425e-132">IID</span></span><br/>                      | <span data-ttu-id="d425e-133">DIID \_ IVMVirtualMachineEvents est défini comme 9d84f560-bb67-4961-BD12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="d425e-133">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="d425e-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d425e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d425e-135">**IVMVirtualMachineEvents**</span><span class="sxs-lookup"><span data-stu-id="d425e-135">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

