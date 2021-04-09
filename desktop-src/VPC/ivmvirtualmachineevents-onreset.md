---
title: IVMVirtualMachineEvents OnReset, méthode (VPCCOMInterfaces. h)
description: Reçoit une notification indiquant qu’un ordinateur virtuel a été réinitialisé.
ms.assetid: 10a66aea-9a8f-4663-8eb6-cc35f361e43f
keywords:
- OnReset, méthode Virtual PC
- OnReset, méthode Virtual PC, interface IVMVirtualMachineEvents
- IVMVirtualMachineEvents interface Virtual PC, OnReset, méthode
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnReset
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6345d0e925777fbecf42247b3e3064b9f993c7c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941627"
---
# <a name="ivmvirtualmachineeventsonreset-method"></a><span data-ttu-id="2b7e2-106">IVMVirtualMachineEvents :: OnReset, méthode</span><span class="sxs-lookup"><span data-stu-id="2b7e2-106">IVMVirtualMachineEvents::OnReset method</span></span>

<span data-ttu-id="2b7e2-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2b7e2-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2b7e2-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2b7e2-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2b7e2-109">Reçoit une notification indiquant qu’un ordinateur virtuel a été réinitialisé.</span><span class="sxs-lookup"><span data-stu-id="2b7e2-109">Receives notification that a virtual machine has been reset.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b7e2-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2b7e2-110">Syntax</span></span>


```C++
HRESULT OnReset();
```



## <a name="parameters"></a><span data-ttu-id="2b7e2-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2b7e2-111">Parameters</span></span>

<span data-ttu-id="2b7e2-112">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="2b7e2-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2b7e2-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2b7e2-113">Return value</span></span>

<span data-ttu-id="2b7e2-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="2b7e2-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2b7e2-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2b7e2-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b7e2-116">Notes</span><span class="sxs-lookup"><span data-stu-id="2b7e2-116">Remarks</span></span>

<span data-ttu-id="2b7e2-117">Cette méthode est appelée lorsque l’ordinateur virtuel a été réinitialisé.</span><span class="sxs-lookup"><span data-stu-id="2b7e2-117">This method is called when the virtual machine has been reset.</span></span> <span data-ttu-id="2b7e2-118">Le programme client doit implémenter cette méthode d’interface pour recevoir la notification de l' \_ événement de réinitialisation vmVirtualMachineEvent provenant de [**IVMVirtualMachine**](ivmvirtualmachine.md).</span><span class="sxs-lookup"><span data-stu-id="2b7e2-118">The client program must implement this interface method to receive notification of the vmVirtualMachineEvent\_Reset event originating from [**IVMVirtualMachine**](ivmvirtualmachine.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2b7e2-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2b7e2-119">Requirements</span></span>



| <span data-ttu-id="2b7e2-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2b7e2-120">Requirement</span></span> | <span data-ttu-id="2b7e2-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="2b7e2-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b7e2-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2b7e2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2b7e2-123">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2b7e2-123">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2b7e2-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2b7e2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2b7e2-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="2b7e2-125">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2b7e2-126">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="2b7e2-126">End of client support</span></span><br/>    | <span data-ttu-id="2b7e2-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2b7e2-127">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2b7e2-128">Produit</span><span class="sxs-lookup"><span data-stu-id="2b7e2-128">Product</span></span><br/>                  | <span data-ttu-id="2b7e2-129">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2b7e2-129">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2b7e2-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="2b7e2-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b7e2-131"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b7e2-131"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="2b7e2-132">IID</span><span class="sxs-lookup"><span data-stu-id="2b7e2-132">IID</span></span><br/>                      | <span data-ttu-id="2b7e2-133">DIID \_ IVMVirtualMachineEvents est défini comme 9d84f560-bb67-4961-BD12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="2b7e2-133">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="2b7e2-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2b7e2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b7e2-135">**IVMVirtualMachineEvents**</span><span class="sxs-lookup"><span data-stu-id="2b7e2-135">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

