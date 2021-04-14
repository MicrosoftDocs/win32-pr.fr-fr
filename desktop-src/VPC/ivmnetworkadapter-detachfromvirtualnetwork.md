---
title: Méthode IVMNetworkAdapter DetachFromVirtualNetwork (VPCCOMInterfaces. h)
description: Détache l’interface réseau de son réseau virtuel.
ms.assetid: f1a00ea2-2b79-4b5c-a4bd-3cab66deb0d0
keywords:
- Méthode DetachFromVirtualNetwork Virtual PC
- Méthode DetachFromVirtualNetwork Virtual PC, interface IVMNetworkAdapter
- IVMNetworkAdapter interface Virtual PC, méthode DetachFromVirtualNetwork
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.DetachFromVirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d90d5046844764fe9e9eb6552fe1a04b6140201b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384804"
---
# <a name="ivmnetworkadapterdetachfromvirtualnetwork-method"></a><span data-ttu-id="73d3d-106">IVMNetworkAdapter ::D méthode etachFromVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="73d3d-106">IVMNetworkAdapter::DetachFromVirtualNetwork method</span></span>

<span data-ttu-id="73d3d-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="73d3d-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="73d3d-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="73d3d-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="73d3d-109">Détache l’interface réseau de son réseau virtuel.</span><span class="sxs-lookup"><span data-stu-id="73d3d-109">Detaches the network interface from its virtual network.</span></span>

## <a name="syntax"></a><span data-ttu-id="73d3d-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="73d3d-110">Syntax</span></span>


```C++
HRESULT DetachFromVirtualNetwork();
```



## <a name="parameters"></a><span data-ttu-id="73d3d-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="73d3d-111">Parameters</span></span>

<span data-ttu-id="73d3d-112">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="73d3d-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="73d3d-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="73d3d-113">Return value</span></span>

<span data-ttu-id="73d3d-114">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="73d3d-114">This method can return one of these values.</span></span>



| <span data-ttu-id="73d3d-115">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="73d3d-115">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="73d3d-116">Description</span><span class="sxs-lookup"><span data-stu-id="73d3d-116">Description</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="73d3d-117"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="73d3d-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="73d3d-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="73d3d-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="73d3d-119"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="73d3d-119"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="73d3d-120">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="73d3d-120">An unexpected error has occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="73d3d-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="73d3d-121">Requirements</span></span>



| <span data-ttu-id="73d3d-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="73d3d-122">Requirement</span></span> | <span data-ttu-id="73d3d-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="73d3d-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="73d3d-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="73d3d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="73d3d-125">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="73d3d-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="73d3d-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="73d3d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="73d3d-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="73d3d-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="73d3d-128">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="73d3d-128">End of client support</span></span><br/>    | <span data-ttu-id="73d3d-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="73d3d-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="73d3d-130">Produit</span><span class="sxs-lookup"><span data-stu-id="73d3d-130">Product</span></span><br/>                  | <span data-ttu-id="73d3d-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="73d3d-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="73d3d-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="73d3d-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="73d3d-133"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="73d3d-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="73d3d-134">IID</span><span class="sxs-lookup"><span data-stu-id="73d3d-134">IID</span></span><br/>                      | <span data-ttu-id="73d3d-135">IID \_ IVMNetworkAdapter est défini en tant que e32e4165-22b8-4DC0-8d57-850171ae207a</span><span class="sxs-lookup"><span data-stu-id="73d3d-135">IID\_IVMNetworkAdapter is defined as e32e4165-22b8-4dc0-8d57-850171ae207a</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="73d3d-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="73d3d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73d3d-137">**IVMNetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="73d3d-137">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> </dl>

 

