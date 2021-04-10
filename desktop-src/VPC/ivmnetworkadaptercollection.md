---
title: Interface IVMNetworkAdapterCollection (VPCCOMInterfaces. h)
description: Définit une collection de cartes d’interface réseau virtuelles. Pour obtenir un objet IVMNetworkAdapterCollection, utilisez les propriétés IVMVirtualMachine NetworkAdapters, IVMVirtualNetwork NetworkAdapters et IVMVirtualPC UnconnectedNetworkAdapters.
ms.assetid: cfb03a7c-a568-488c-9284-798b7e21027a
keywords:
- Virtual PC de l’interface IVMNetworkAdapterCollection
- IVMNetworkAdapterCollection interface Virtual PC, Description
topic_type:
- apiref
api_name:
- IVMNetworkAdapterCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8005b88cb873f00708829672cdeb6563b606d42b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032958"
---
# <a name="ivmnetworkadaptercollection-interface"></a><span data-ttu-id="92963-106">Interface IVMNetworkAdapterCollection</span><span class="sxs-lookup"><span data-stu-id="92963-106">IVMNetworkAdapterCollection interface</span></span>

<span data-ttu-id="92963-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="92963-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="92963-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="92963-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="92963-109">Définit une collection de cartes d’interface réseau virtuelles.</span><span class="sxs-lookup"><span data-stu-id="92963-109">Defines a collection of virtual network interface cards.</span></span> <span data-ttu-id="92963-110">Pour obtenir un objet IVMNetworkAdapterCollection, utilisez les propriétés [**IVMVirtualMachine :: NetworkAdapters**](ivmvirtualmachine-networkadapters.md), [**IVMVirtualNetwork :: NetworkAdapters**](ivmvirtualnetwork-networkadapters.md)et [**IVMVirtualPC :: UnconnectedNetworkAdapters**](ivmvirtualpc-unconnectednetworkadapters.md) .</span><span class="sxs-lookup"><span data-stu-id="92963-110">To obtain an IVMNetworkAdapterCollection object, use the [**IVMVirtualMachine::NetworkAdapters**](ivmvirtualmachine-networkadapters.md), [**IVMVirtualNetwork::NetworkAdapters**](ivmvirtualnetwork-networkadapters.md), and [**IVMVirtualPC::UnconnectedNetworkAdapters**](ivmvirtualpc-unconnectednetworkadapters.md) properties.</span></span>

## <a name="members"></a><span data-ttu-id="92963-111">Membres</span><span class="sxs-lookup"><span data-stu-id="92963-111">Members</span></span>

<span data-ttu-id="92963-112">L’interface **IVMNetworkAdapterCollection** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="92963-112">The **IVMNetworkAdapterCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="92963-113">**IVMNetworkAdapterCollection** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="92963-113">**IVMNetworkAdapterCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="92963-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="92963-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="92963-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="92963-115">Properties</span></span>

<span data-ttu-id="92963-116">L’interface **IVMNetworkAdapterCollection** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="92963-116">The **IVMNetworkAdapterCollection** interface has these properties.</span></span>



| <span data-ttu-id="92963-117">Propriété</span><span class="sxs-lookup"><span data-stu-id="92963-117">Property</span></span>                                                             | <span data-ttu-id="92963-118">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="92963-118">Access type</span></span>          | <span data-ttu-id="92963-119">Description</span><span class="sxs-lookup"><span data-stu-id="92963-119">Description</span></span>                                                                                                   |
|:---------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="92963-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="92963-120">**\_NewEnum**</span></span>](ivmnetworkadaptercollection--newenum.md)<br/> | <span data-ttu-id="92963-121">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92963-121">Read-only</span></span><br/> | <span data-ttu-id="92963-122">Énumérateur de la collection.</span><span class="sxs-lookup"><span data-stu-id="92963-122">An enumerator for the collection.</span></span><br/>                                                                  |
| [<span data-ttu-id="92963-123">**Saut**</span><span class="sxs-lookup"><span data-stu-id="92963-123">**Count**</span></span>](ivmnetworkadaptercollection-count.md)<br/>        | <span data-ttu-id="92963-124">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92963-124">Read-only</span></span><br/> | <span data-ttu-id="92963-125">Nombre d’interfaces réseau de cette collection.</span><span class="sxs-lookup"><span data-stu-id="92963-125">The number of network interfaces in this collection.</span></span><br/>                                               |
| [<span data-ttu-id="92963-126">**Élément**</span><span class="sxs-lookup"><span data-stu-id="92963-126">**Item**</span></span>](ivmnetworkadaptercollection-item.md)<br/>          | <span data-ttu-id="92963-127">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92963-127">Read-only</span></span><br/> | <span data-ttu-id="92963-128">Objet [**IVMNetworkAdapter**](ivmnetworkadapter.md) qui correspond à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="92963-128">The [**IVMNetworkAdapter**](ivmnetworkadapter.md) object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="92963-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="92963-129">Requirements</span></span>



| <span data-ttu-id="92963-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="92963-130">Requirement</span></span> | <span data-ttu-id="92963-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="92963-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92963-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="92963-132">Minimum supported client</span></span><br/> | <span data-ttu-id="92963-133">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="92963-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="92963-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="92963-134">Minimum supported server</span></span><br/> | <span data-ttu-id="92963-135">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="92963-135">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="92963-136">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="92963-136">End of client support</span></span><br/>    | <span data-ttu-id="92963-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="92963-137">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="92963-138">Produit</span><span class="sxs-lookup"><span data-stu-id="92963-138">Product</span></span><br/>                  | <span data-ttu-id="92963-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="92963-139">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="92963-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="92963-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="92963-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="92963-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="92963-142">IID</span><span class="sxs-lookup"><span data-stu-id="92963-142">IID</span></span><br/>                      | <span data-ttu-id="92963-143">IID \_ IVMNetworkAdapterCollection est défini en tant que ebaeafe9-EBCD-47cf-866e-ad87d735e479</span><span class="sxs-lookup"><span data-stu-id="92963-143">IID\_IVMNetworkAdapterCollection is defined as ebaeafe9-ebcd-47cf-866e-ad87d735e479</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="92963-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92963-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92963-145">**IVMNetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="92963-145">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> <dt>

[<span data-ttu-id="92963-146">**IVMVirtualMachine::NetworkAdapters**</span><span class="sxs-lookup"><span data-stu-id="92963-146">**IVMVirtualMachine::NetworkAdapters**</span></span>](ivmvirtualmachine-networkadapters.md)
</dt> <dt>

[<span data-ttu-id="92963-147">**IVMVirtualNetwork::NetworkAdapters**</span><span class="sxs-lookup"><span data-stu-id="92963-147">**IVMVirtualNetwork::NetworkAdapters**</span></span>](ivmvirtualnetwork-networkadapters.md)
</dt> <dt>

[<span data-ttu-id="92963-148">**IVMVirtualPC::UnconnectedNetworkAdapters**</span><span class="sxs-lookup"><span data-stu-id="92963-148">**IVMVirtualPC::UnconnectedNetworkAdapters**</span></span>](ivmvirtualpc-unconnectednetworkadapters.md)
</dt> </dl>

 

