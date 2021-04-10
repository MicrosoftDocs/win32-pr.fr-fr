---
title: IVMNetworkAdapter VirtualMachine, propriété (VPCCOMInterfaces. h)
description: Récupère l’ordinateur virtuel associé à cette interface réseau.
ms.assetid: a3519041-0081-44e7-aa76-760d59ca8587
keywords:
- VirtualMachine propriété Virtual PC
- VirtualMachine, propriété Virtual PC, IVMNetworkAdapter, interface
- IVMNetworkAdapter interface Virtual PC, propriété VirtualMachine
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.VirtualMachine
- IVMNetworkAdapter.get_VirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea50e43bdcffcd16f668ef596a0f9db9d9bccfe2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032299"
---
# <a name="ivmnetworkadaptervirtualmachine-property"></a><span data-ttu-id="06bbf-106">IVMNetworkAdapter :: VirtualMachine, propriété</span><span class="sxs-lookup"><span data-stu-id="06bbf-106">IVMNetworkAdapter::VirtualMachine property</span></span>

<span data-ttu-id="06bbf-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="06bbf-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="06bbf-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="06bbf-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="06bbf-109">Récupère l’ordinateur virtuel associé à cette interface réseau.</span><span class="sxs-lookup"><span data-stu-id="06bbf-109">Retrieves the virtual machine associated with this network interface.</span></span>

<span data-ttu-id="06bbf-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="06bbf-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="06bbf-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="06bbf-111">Syntax</span></span>


```C++
HRESULT get_VirtualMachine(
  [out, retval] IVMVirtualMachine **virtualMachine
);
```



## <a name="property-value"></a><span data-ttu-id="06bbf-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="06bbf-112">Property value</span></span>

<span data-ttu-id="06bbf-113">Interface [**IVMVirtualMachine**](ivmvirtualmachine.md) qui représente l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="06bbf-113">An [**IVMVirtualMachine**](ivmvirtualmachine.md) interface that represents the virtual machine.</span></span>

## <a name="error-codes"></a><span data-ttu-id="06bbf-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="06bbf-114">Error codes</span></span>



| <span data-ttu-id="06bbf-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="06bbf-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="06bbf-116">Signification</span><span class="sxs-lookup"><span data-stu-id="06bbf-116">Meaning</span></span>                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="06bbf-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="06bbf-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="06bbf-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="06bbf-118">The operation was successful.</span></span><br/>        |
| <dl> <span data-ttu-id="06bbf-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="06bbf-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="06bbf-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="06bbf-120">The parameter is **NULL**.</span></span><br/>           |
| <dl> <span data-ttu-id="06bbf-121"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="06bbf-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="06bbf-122">L’ordinateur virtuel est introuvable.</span><span class="sxs-lookup"><span data-stu-id="06bbf-122">The virtual machine cannot be found.</span></span><br/> |
| <dl> <span data-ttu-id="06bbf-123"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="06bbf-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="06bbf-124">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="06bbf-124">An unexpected error has occurred.</span></span><br/>    |



## <a name="requirements"></a><span data-ttu-id="06bbf-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="06bbf-125">Requirements</span></span>



| <span data-ttu-id="06bbf-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="06bbf-126">Requirement</span></span> | <span data-ttu-id="06bbf-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="06bbf-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="06bbf-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="06bbf-128">Minimum supported client</span></span><br/> | <span data-ttu-id="06bbf-129">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="06bbf-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="06bbf-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="06bbf-130">Minimum supported server</span></span><br/> | <span data-ttu-id="06bbf-131">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="06bbf-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="06bbf-132">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="06bbf-132">End of client support</span></span><br/>    | <span data-ttu-id="06bbf-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="06bbf-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="06bbf-134">Produit</span><span class="sxs-lookup"><span data-stu-id="06bbf-134">Product</span></span><br/>                  | <span data-ttu-id="06bbf-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="06bbf-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="06bbf-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="06bbf-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="06bbf-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="06bbf-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="06bbf-138">IID</span><span class="sxs-lookup"><span data-stu-id="06bbf-138">IID</span></span><br/>                      | <span data-ttu-id="06bbf-139">IID \_ IVMNetworkAdapter est défini en tant que e32e4165-22b8-4DC0-8d57-850171ae207a</span><span class="sxs-lookup"><span data-stu-id="06bbf-139">IID\_IVMNetworkAdapter is defined as e32e4165-22b8-4dc0-8d57-850171ae207a</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="06bbf-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="06bbf-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06bbf-141">**IVMNetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="06bbf-141">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> </dl>

 

