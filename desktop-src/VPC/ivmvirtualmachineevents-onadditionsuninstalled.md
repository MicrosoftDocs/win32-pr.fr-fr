---
title: Méthode IVMVirtualMachineEvents OnAdditionsUninstalled (VPCCOMInterfaces. h)
description: Reçoit une notification indiquant que les composants d’intégration sont désinstallés sur une machine virtuelle.
ms.assetid: bbbc01b6-adb1-491e-a5b0-ff463dca7dfd
keywords:
- Méthode OnAdditionsUninstalled Virtual PC
- Méthode OnAdditionsUninstalled Virtual PC, interface IVMVirtualMachineEvents
- IVMVirtualMachineEvents interface Virtual PC, méthode OnAdditionsUninstalled
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnAdditionsUninstalled
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 514a88249ad34d51965df75feab6f129bd9fa5a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102800"
---
# <a name="ivmvirtualmachineeventsonadditionsuninstalled-method"></a><span data-ttu-id="9a8a7-106">IVMVirtualMachineEvents :: OnAdditionsUninstalled, méthode</span><span class="sxs-lookup"><span data-stu-id="9a8a7-106">IVMVirtualMachineEvents::OnAdditionsUninstalled method</span></span>

<span data-ttu-id="9a8a7-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="9a8a7-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="9a8a7-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="9a8a7-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="9a8a7-109">Reçoit une notification indiquant que les composants d’intégration sont désinstallés sur une machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="9a8a7-109">Receives notification that integration components are uninstalled in a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a8a7-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9a8a7-110">Syntax</span></span>


```C++
HRESULT OnAdditionsUninstalled();
```



## <a name="parameters"></a><span data-ttu-id="9a8a7-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9a8a7-111">Parameters</span></span>

<span data-ttu-id="9a8a7-112">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="9a8a7-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9a8a7-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9a8a7-113">Return value</span></span>

<span data-ttu-id="9a8a7-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9a8a7-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9a8a7-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9a8a7-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a8a7-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9a8a7-116">Requirements</span></span>



| <span data-ttu-id="9a8a7-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9a8a7-117">Requirement</span></span> | <span data-ttu-id="9a8a7-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a8a7-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a8a7-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9a8a7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9a8a7-120">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9a8a7-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9a8a7-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9a8a7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9a8a7-122">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="9a8a7-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="9a8a7-123">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="9a8a7-123">End of client support</span></span><br/>    | <span data-ttu-id="9a8a7-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9a8a7-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="9a8a7-125">Produit</span><span class="sxs-lookup"><span data-stu-id="9a8a7-125">Product</span></span><br/>                  | <span data-ttu-id="9a8a7-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="9a8a7-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="9a8a7-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="9a8a7-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a8a7-128"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a8a7-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="9a8a7-129">IID</span><span class="sxs-lookup"><span data-stu-id="9a8a7-129">IID</span></span><br/>                      | <span data-ttu-id="9a8a7-130">DIID \_ IVMVirtualMachineEvents est défini comme 9d84f560-bb67-4961-BD12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="9a8a7-130">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="9a8a7-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a8a7-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a8a7-132">**IVMVirtualMachineEvents**</span><span class="sxs-lookup"><span data-stu-id="9a8a7-132">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

