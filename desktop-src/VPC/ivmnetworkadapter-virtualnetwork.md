---
title: IVMNetworkAdapter VirtualNetwork, propriété (VPCCOMInterfaces. h)
description: Récupère le réseau virtuel auquel l’interface réseau est attachée.
ms.assetid: 7f52fd86-5f83-41d8-ba48-7db65e9c357c
keywords:
- VirtualNetwork propriété Virtual PC
- VirtualNetwork, propriété Virtual PC, IVMNetworkAdapter, interface
- IVMNetworkAdapter interface Virtual PC, propriété VirtualNetwork
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.VirtualNetwork
- IVMNetworkAdapter.get_VirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b932ef553d3952fbc69edba3416ac20049984810
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032298"
---
# <a name="ivmnetworkadaptervirtualnetwork-property"></a><span data-ttu-id="4896e-106">IVMNetworkAdapter :: VirtualNetwork, propriété</span><span class="sxs-lookup"><span data-stu-id="4896e-106">IVMNetworkAdapter::VirtualNetwork property</span></span>

<span data-ttu-id="4896e-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4896e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4896e-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4896e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4896e-109">Récupère le réseau virtuel auquel l’interface réseau est attachée.</span><span class="sxs-lookup"><span data-stu-id="4896e-109">Retrieves the virtual network to which the network interface is attached.</span></span>

<span data-ttu-id="4896e-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="4896e-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4896e-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4896e-111">Syntax</span></span>


```C++
HRESULT get_VirtualNetwork(
  [out, retval] IVMVirtualNetwork **virtualNetwork
);
```



## <a name="property-value"></a><span data-ttu-id="4896e-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="4896e-112">Property value</span></span>

<span data-ttu-id="4896e-113">Interface [**IVMVirtualNetwork**](ivmvirtualnetwork.md) qui représente le réseau virtuel auquel cette interface réseau virtuelle est attachée.</span><span class="sxs-lookup"><span data-stu-id="4896e-113">An [**IVMVirtualNetwork**](ivmvirtualnetwork.md) interface that represents the virtual network to which this virtual network interface is attached.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4896e-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="4896e-114">Error codes</span></span>



| <span data-ttu-id="4896e-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="4896e-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="4896e-116">Signification</span><span class="sxs-lookup"><span data-stu-id="4896e-116">Meaning</span></span>                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4896e-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4896e-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="4896e-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="4896e-118">The operation was successful.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="4896e-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="4896e-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="4896e-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="4896e-120">The parameter is **NULL**.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="4896e-121"><dt>S \_ FALSe</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="4896e-121"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                                       | <span data-ttu-id="4896e-122">Cette interface réseau est déconnectée et n’est pas connectée à un réseau virtuel.</span><span class="sxs-lookup"><span data-stu-id="4896e-122">This network interface is unplugged and is not connected to a virtual network.</span></span><br/> |
| <dl> <span data-ttu-id="4896e-123"><dt>Ordinateur virtuel \_ E \_ \_ ID de \_ réseau \_ virtuel non valide</dt> <dt>0xA00400702</dt></span><span class="sxs-lookup"><span data-stu-id="4896e-123"><dt>VM\_E\_INVALID\_VIRTUAL\_NETWORK\_ID</dt> <dt>0xA00400702</dt></span></span> </dl> | <span data-ttu-id="4896e-124">Cette interface est connectée à un réseau virtuel avec un ID non valide.</span><span class="sxs-lookup"><span data-stu-id="4896e-124">This interface is connected to a virtual network with an invalid ID.</span></span><br/>           |
| <dl> <span data-ttu-id="4896e-125"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="4896e-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="4896e-126">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="4896e-126">An unexpected error has occurred.</span></span><br/>                                              |



## <a name="requirements"></a><span data-ttu-id="4896e-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4896e-127">Requirements</span></span>



| <span data-ttu-id="4896e-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4896e-128">Requirement</span></span> | <span data-ttu-id="4896e-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="4896e-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4896e-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4896e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="4896e-131">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4896e-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4896e-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4896e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="4896e-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="4896e-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4896e-134">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="4896e-134">End of client support</span></span><br/>    | <span data-ttu-id="4896e-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4896e-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4896e-136">Produit</span><span class="sxs-lookup"><span data-stu-id="4896e-136">Product</span></span><br/>                  | <span data-ttu-id="4896e-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4896e-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4896e-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="4896e-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="4896e-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="4896e-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4896e-140">IID</span><span class="sxs-lookup"><span data-stu-id="4896e-140">IID</span></span><br/>                      | <span data-ttu-id="4896e-141">IID \_ IVMNetworkAdapter est défini en tant que e32e4165-22b8-4DC0-8d57-850171ae207a</span><span class="sxs-lookup"><span data-stu-id="4896e-141">IID\_IVMNetworkAdapter is defined as e32e4165-22b8-4dc0-8d57-850171ae207a</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="4896e-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4896e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4896e-143">**IVMNetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="4896e-143">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> </dl>

 

