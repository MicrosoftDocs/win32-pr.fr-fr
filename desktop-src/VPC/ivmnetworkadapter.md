---
title: Interface IVMNetworkAdapter (VPCCOMInterfaces. h)
description: Sert d’interface à une carte d’interface réseau virtuelle.
ms.assetid: df050706-09be-47d1-9ae1-1eb0e1836d64
keywords:
- Virtual PC de l’interface IVMNetworkAdapter
- IVMNetworkAdapter interface Virtual PC, Description
topic_type:
- apiref
api_name:
- IVMNetworkAdapter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74a0ccf722715896743129b6666609bd8a88df3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384748"
---
# <a name="ivmnetworkadapter-interface"></a><span data-ttu-id="3d17e-105">Interface IVMNetworkAdapter</span><span class="sxs-lookup"><span data-stu-id="3d17e-105">IVMNetworkAdapter interface</span></span>

<span data-ttu-id="3d17e-106">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3d17e-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3d17e-107">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3d17e-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3d17e-108">Sert d’interface à une carte d’interface réseau (NIC) virtuelle.</span><span class="sxs-lookup"><span data-stu-id="3d17e-108">Serves as the interface to a virtual network interface card (NIC).</span></span> <span data-ttu-id="3d17e-109">Il permet de configurer la façon dont une machine virtuelle est en réseau.</span><span class="sxs-lookup"><span data-stu-id="3d17e-109">It is used to set up how a virtual machine is networked.</span></span> <span data-ttu-id="3d17e-110">Les cartes d’interface réseau peuvent être ajoutées et supprimées à l’aide de [**IVMVirtualMachine :: AddNetworkAdapter**](ivmvirtualmachine-addnetworkadapter.md) et [**IVMVirtualMachine :: RemoveNetworkAdapter**](ivmvirtualmachine-removenetworkadapter.md).</span><span class="sxs-lookup"><span data-stu-id="3d17e-110">Network interface cards can be added and removed by using [**IVMVirtualMachine::AddNetworkAdapter**](ivmvirtualmachine-addnetworkadapter.md) and [**IVMVirtualMachine::RemoveNetworkAdapter**](ivmvirtualmachine-removenetworkadapter.md).</span></span> <span data-ttu-id="3d17e-111">Vous pouvez également récupérer un objet **IVMNetworkAdapter** à partir de la collection [**IVMNetworkAdapterCollection**](ivmnetworkadaptercollection.md) retournée par les propriétés [**IVMVirtualMachine :: NetworkAdapters**](ivmvirtualmachine-networkadapters.md) ou [**IVMVirtualNetwork :: NetworkAdapters**](ivmvirtualnetwork-networkadapters.md) .</span><span class="sxs-lookup"><span data-stu-id="3d17e-111">You can also retrieve an **IVMNetworkAdapter** object from the [**IVMNetworkAdapterCollection**](ivmnetworkadaptercollection.md) collection returned from the [**IVMVirtualMachine::NetworkAdapters**](ivmvirtualmachine-networkadapters.md) or [**IVMVirtualNetwork::NetworkAdapters**](ivmvirtualnetwork-networkadapters.md) properties.</span></span>

## <a name="members"></a><span data-ttu-id="3d17e-112">Membres</span><span class="sxs-lookup"><span data-stu-id="3d17e-112">Members</span></span>

<span data-ttu-id="3d17e-113">L’interface **IVMNetworkAdapter** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="3d17e-113">The **IVMNetworkAdapter** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="3d17e-114">**IVMNetworkAdapter** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="3d17e-114">**IVMNetworkAdapter** also has these types of members:</span></span>

-   [<span data-ttu-id="3d17e-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="3d17e-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="3d17e-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3d17e-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3d17e-117">Méthodes</span><span class="sxs-lookup"><span data-stu-id="3d17e-117">Methods</span></span>

<span data-ttu-id="3d17e-118">L’interface **IVMNetworkAdapter** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="3d17e-118">The **IVMNetworkAdapter** interface has these methods.</span></span>



| <span data-ttu-id="3d17e-119">Méthode</span><span class="sxs-lookup"><span data-stu-id="3d17e-119">Method</span></span>                                                                         | <span data-ttu-id="3d17e-120">Description</span><span class="sxs-lookup"><span data-stu-id="3d17e-120">Description</span></span>                                                                 |
|:-------------------------------------------------------------------------------|:----------------------------------------------------------------------------|
| [<span data-ttu-id="3d17e-121">**\_IDENTIFI**</span><span class="sxs-lookup"><span data-stu-id="3d17e-121">**\_ID**</span></span>](ivmnetworkadapter--id.md)                                          | <span data-ttu-id="3d17e-122">Récupère l’identificateur interne de cette interface réseau.</span><span class="sxs-lookup"><span data-stu-id="3d17e-122">Retrieves the internal identifier of this network interface.</span></span><br/>     |
| [<span data-ttu-id="3d17e-123">**AttachToVirtualNetwork**</span><span class="sxs-lookup"><span data-stu-id="3d17e-123">**AttachToVirtualNetwork**</span></span>](ivmnetworkadapter-attachtovirtualnetwork.md)     | <span data-ttu-id="3d17e-124">Attache l’interface réseau au réseau virtuel spécifié.</span><span class="sxs-lookup"><span data-stu-id="3d17e-124">Attaches the network interface to the specified virtual network.</span></span><br/> |
| [<span data-ttu-id="3d17e-125">**DetachFromVirtualNetwork**</span><span class="sxs-lookup"><span data-stu-id="3d17e-125">**DetachFromVirtualNetwork**</span></span>](ivmnetworkadapter-detachfromvirtualnetwork.md) | <span data-ttu-id="3d17e-126">Détache l’interface réseau de son réseau virtuel.</span><span class="sxs-lookup"><span data-stu-id="3d17e-126">Detaches the network interface from its virtual network.</span></span><br/>         |



 

### <a name="properties"></a><span data-ttu-id="3d17e-127">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3d17e-127">Properties</span></span>

<span data-ttu-id="3d17e-128">L’interface **IVMNetworkAdapter** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="3d17e-128">The **IVMNetworkAdapter** interface has these properties.</span></span>



| <span data-ttu-id="3d17e-129">Propriété</span><span class="sxs-lookup"><span data-stu-id="3d17e-129">Property</span></span>                                                                                  | <span data-ttu-id="3d17e-130">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="3d17e-130">Access type</span></span>           | <span data-ttu-id="3d17e-131">Description</span><span class="sxs-lookup"><span data-stu-id="3d17e-131">Description</span></span>                                                                 |
|:------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------|
| [<span data-ttu-id="3d17e-132">**EthernetAddress**</span><span class="sxs-lookup"><span data-stu-id="3d17e-132">**EthernetAddress**</span></span>](ivmnetworkadapter-ethernetaddress.md)<br/>                   | <span data-ttu-id="3d17e-133">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3d17e-133">Read/write</span></span><br/> | <span data-ttu-id="3d17e-134">Adresse Ethernet (MAC) de l’interface réseau.</span><span class="sxs-lookup"><span data-stu-id="3d17e-134">The Ethernet (MAC) address of the network interface.</span></span><br/>             |
| [<span data-ttu-id="3d17e-135">**IsEthernetAddressDynamic**</span><span class="sxs-lookup"><span data-stu-id="3d17e-135">**IsEthernetAddressDynamic**</span></span>](ivmnetworkadapter-isethernetaddressdynamic.md)<br/> | <span data-ttu-id="3d17e-136">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3d17e-136">Read/write</span></span><br/> | <span data-ttu-id="3d17e-137">Indique si l’adresse Ethernet est générée dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="3d17e-137">Indicates whether the Ethernet address is dynamically generated.</span></span><br/> |
| [<span data-ttu-id="3d17e-138">**VirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="3d17e-138">**VirtualMachine**</span></span>](ivmnetworkadapter-virtualmachine.md)<br/>                     | <span data-ttu-id="3d17e-139">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3d17e-139">Read-only</span></span><br/>  | <span data-ttu-id="3d17e-140">Ordinateur virtuel associé à cette interface réseau.</span><span class="sxs-lookup"><span data-stu-id="3d17e-140">The virtual machine associated with this network interface.</span></span><br/>      |
| [<span data-ttu-id="3d17e-141">**VirtualNetwork**</span><span class="sxs-lookup"><span data-stu-id="3d17e-141">**VirtualNetwork**</span></span>](ivmnetworkadapter-virtualnetwork.md)<br/>                     | <span data-ttu-id="3d17e-142">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3d17e-142">Read-only</span></span><br/>  | <span data-ttu-id="3d17e-143">Réseau virtuel auquel l’interface réseau est attachée.</span><span class="sxs-lookup"><span data-stu-id="3d17e-143">The virtual network to which the network interface is attached.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="3d17e-144">Notes</span><span class="sxs-lookup"><span data-stu-id="3d17e-144">Remarks</span></span>

<span data-ttu-id="3d17e-145">L’adresse Ethernet par défaut pour une interface réseau est « 00-00-00-00-00-00 », qui est considérée comme une adresse Ethernet non valide par la plupart des systèmes d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="3d17e-145">The default Ethernet address for a network interface is "00-00-00-00-00-00", which is considered an invalid Ethernet address by most operating systems.</span></span> <span data-ttu-id="3d17e-146">Si [**IsEthernetAddressDynamic**](ivmnetworkadapter-isethernetaddressdynamic.md) a la valeur **false**, [**EthernetAddress**](ivmnetworkadapter-ethernetaddress.md) doit être initialisé avec une adresse réseau Ethernet valide.</span><span class="sxs-lookup"><span data-stu-id="3d17e-146">If [**IsEthernetAddressDynamic**](ivmnetworkadapter-isethernetaddressdynamic.md) is set to **FALSE**, [**EthernetAddress**](ivmnetworkadapter-ethernetaddress.md) must be initialized with a valid Ethernet network address.</span></span>

<span data-ttu-id="3d17e-147">Les procédures suivantes expliquent comment utiliser l’interface **IVMNetworkAdapter** .</span><span class="sxs-lookup"><span data-stu-id="3d17e-147">The following procedures explain how to use the **IVMNetworkAdapter** interface.</span></span>

<span data-ttu-id="3d17e-148">**Pour attacher une carte réseau virtuelle à une carte réseau d’ordinateur hôte**</span><span class="sxs-lookup"><span data-stu-id="3d17e-148">**To attach a virtual NIC to a host NIC**</span></span>

-   <span data-ttu-id="3d17e-149">Les cartes réseau virtuelles (invitées) ne sont pas directement attachées à une carte réseau d’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="3d17e-149">Virtual (guest) NICs are not attached directly to a host NIC.</span></span> <span data-ttu-id="3d17e-150">Au lieu de cela, la carte d’interface réseau virtuelle est attachée à un réseau virtuel associé à une carte réseau d’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="3d17e-150">Instead, the virtual NIC is attached to a virtual network that is attached to a host NIC.</span></span> <span data-ttu-id="3d17e-151">Pour plus d’informations sur la configuration des réseaux virtuels, consultez [**IVMVirtualNetwork**](ivmvirtualnetwork.md).</span><span class="sxs-lookup"><span data-stu-id="3d17e-151">For more information about configuring virtual networks, see [**IVMVirtualNetwork**](ivmvirtualnetwork.md).</span></span> <span data-ttu-id="3d17e-152">Pour attacher la carte réseau virtuelle à un réseau virtuel, utilisez la méthode [**AttachToVirtualNetwork**](ivmnetworkadapter-attachtovirtualnetwork.md) .</span><span class="sxs-lookup"><span data-stu-id="3d17e-152">To attach the virtual NIC to a virtual network, use the [**AttachToVirtualNetwork**](ivmnetworkadapter-attachtovirtualnetwork.md) method.</span></span>

<span data-ttu-id="3d17e-153">**Pour déconnecter une carte réseau virtuelle du réseau virtuel**</span><span class="sxs-lookup"><span data-stu-id="3d17e-153">**To disconnect a virtual NIC from the virtual network**</span></span>

-   <span data-ttu-id="3d17e-154">La méthode [**DetachFromVirtualNetwork**](ivmnetworkadapter-detachfromvirtualnetwork.md) détachera la carte réseau virtuelle du réseau virtuel.</span><span class="sxs-lookup"><span data-stu-id="3d17e-154">The [**DetachFromVirtualNetwork**](ivmnetworkadapter-detachfromvirtualnetwork.md) method will detach the virtual NIC from the virtual network.</span></span> <span data-ttu-id="3d17e-155">Après l’appel de cette fonction, la propriété [**virtualnetwork**](ivmnetworkadapter-virtualnetwork.md) retourne un ID de réseau virtuel qui n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="3d17e-155">After this function is called, the [**VirtualNetwork**](ivmnetworkadapter-virtualnetwork.md) property will return a virtual network ID that is not valid.</span></span>

<span data-ttu-id="3d17e-156">**Pour supprimer une carte réseau virtuelle d’un ordinateur virtuel si vous avez l’objet de carte réseau virtuelle**</span><span class="sxs-lookup"><span data-stu-id="3d17e-156">**To remove a virtual NIC from a virtual machine if you have the virtual NIC object**</span></span>

1.  <span data-ttu-id="3d17e-157">Récupérez l’ordinateur virtuel associé à la carte réseau virtuelle à l’aide de la propriété [**VirtualMachine**](ivmnetworkadapter-virtualmachine.md) .</span><span class="sxs-lookup"><span data-stu-id="3d17e-157">Get the virtual machine associated with the virtual NIC by using the [**VirtualMachine**](ivmnetworkadapter-virtualmachine.md) property.</span></span>
2.  <span data-ttu-id="3d17e-158">Utilisez l’objet en cours en tant que paramètre de la méthode [**IVMVirtualMachine :: RemoveNetworkAdapter**](ivmvirtualmachine-removenetworkadapter.md) .</span><span class="sxs-lookup"><span data-stu-id="3d17e-158">Use the current object as a parameter to the [**IVMVirtualMachine::RemoveNetworkAdapter**](ivmvirtualmachine-removenetworkadapter.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d17e-159">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3d17e-159">Requirements</span></span>



| <span data-ttu-id="3d17e-160">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3d17e-160">Requirement</span></span> | <span data-ttu-id="3d17e-161">Valeur</span><span class="sxs-lookup"><span data-stu-id="3d17e-161">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d17e-162">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3d17e-162">Minimum supported client</span></span><br/> | <span data-ttu-id="3d17e-163">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3d17e-163">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3d17e-164">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3d17e-164">Minimum supported server</span></span><br/> | <span data-ttu-id="3d17e-165">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="3d17e-165">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3d17e-166">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="3d17e-166">End of client support</span></span><br/>    | <span data-ttu-id="3d17e-167">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3d17e-167">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3d17e-168">Produit</span><span class="sxs-lookup"><span data-stu-id="3d17e-168">Product</span></span><br/>                  | <span data-ttu-id="3d17e-169">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3d17e-169">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3d17e-170">En-tête</span><span class="sxs-lookup"><span data-stu-id="3d17e-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d17e-171"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d17e-171"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3d17e-172">IID</span><span class="sxs-lookup"><span data-stu-id="3d17e-172">IID</span></span><br/>                      | <span data-ttu-id="3d17e-173">IID \_ IVMNetworkAdapter est défini en tant que e32e4165-22b8-4DC0-8d57-850171ae207a</span><span class="sxs-lookup"><span data-stu-id="3d17e-173">IID\_IVMNetworkAdapter is defined as e32e4165-22b8-4dc0-8d57-850171ae207a</span></span><br/>          |



 

