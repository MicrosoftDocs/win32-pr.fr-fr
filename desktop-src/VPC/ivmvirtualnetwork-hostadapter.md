---
title: IVMVirtualNetwork HostAdapter, propriété (VPCCOMInterfaces. h)
description: Nom de l’adaptateur auquel le réseau virtuel est connecté.
ms.assetid: 7ee074d2-13ba-42db-84db-ecfd22576a9a
keywords:
- HostAdapter propriété Virtual PC
- HostAdapter, propriété Virtual PC, IVMVirtualNetwork, interface
- IVMVirtualNetwork interface Virtual PC, propriété HostAdapter
topic_type:
- apiref
api_name:
- IVMVirtualNetwork.HostAdapter
- IVMVirtualNetwork.get_HostAdapter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0485303c2328a85c70779f16652121729546f3ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033117"
---
# <a name="ivmvirtualnetworkhostadapter-property"></a><span data-ttu-id="7e102-106">IVMVirtualNetwork :: HostAdapter, propriété</span><span class="sxs-lookup"><span data-stu-id="7e102-106">IVMVirtualNetwork::HostAdapter property</span></span>

<span data-ttu-id="7e102-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7e102-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7e102-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7e102-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7e102-109">Récupère le nom de l’adaptateur auquel le réseau virtuel est connecté.</span><span class="sxs-lookup"><span data-stu-id="7e102-109">Retrieves the name of the adapter to which the virtual network is connected.</span></span>

<span data-ttu-id="7e102-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="7e102-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e102-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7e102-111">Syntax</span></span>


```C++
HRESULT get_HostAdapter(
  [out, retval] BSTR *hostAdapter
);
```



## <a name="property-value"></a><span data-ttu-id="7e102-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="7e102-112">Property value</span></span>

<span data-ttu-id="7e102-113">Nom de la carte hôte à laquelle le réseau virtuel est connecté.</span><span class="sxs-lookup"><span data-stu-id="7e102-113">The name of the host adapter to which the virtual network is connected.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7e102-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="7e102-114">Error codes</span></span>



| <span data-ttu-id="7e102-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="7e102-115">Name/value</span></span>                                                                                                                                                            | <span data-ttu-id="7e102-116">Signification</span><span class="sxs-lookup"><span data-stu-id="7e102-116">Meaning</span></span>                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7e102-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7e102-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                               | <span data-ttu-id="7e102-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="7e102-118">The operation was successful.</span></span><br/>                                                                                                                              |
| <dl> <span data-ttu-id="7e102-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="7e102-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                 | <span data-ttu-id="7e102-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="7e102-120">The parameter is **NULL**.</span></span><br/>                                                                                                                                 |
| <dl> <span data-ttu-id="7e102-121"><dt>Ordinateur virtuel \_ \_Adaptateur E \_ \_ introuvable</dt> <dt>0xA0040700</dt></span><span class="sxs-lookup"><span data-stu-id="7e102-121"><dt>VM\_E\_ADAPTER\_NOT\_FOUND</dt> <dt>0xA0040700</dt></span></span> </dl> | <span data-ttu-id="7e102-122">La carte Ethernet hôte à laquelle ce réseau virtuel était connecté n’est plus disponible.</span><span class="sxs-lookup"><span data-stu-id="7e102-122">The host Ethernet adapter to which this virtual network was connected is no longer available.</span></span> <span data-ttu-id="7e102-123">La carte Ethernet hôte a peut-être été supprimée ou désactivée.</span><span class="sxs-lookup"><span data-stu-id="7e102-123">The host Ethernet adapter may have been removed or disabled.</span></span><br/> |
| <dl> <span data-ttu-id="7e102-124"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="7e102-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>         | <span data-ttu-id="7e102-125">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="7e102-125">An unexpected error has occurred.</span></span><br/>                                                                                                                          |



## <a name="remarks"></a><span data-ttu-id="7e102-126">Notes</span><span class="sxs-lookup"><span data-stu-id="7e102-126">Remarks</span></span>

<span data-ttu-id="7e102-127">La carte réseau virtuelle permet à un réseau virtuel de communiquer avec des réseaux externes.</span><span class="sxs-lookup"><span data-stu-id="7e102-127">The virtual network adapter allows a virtual network to talk to external networks.</span></span> <span data-ttu-id="7e102-128">Il y a généralement une carte par carte Ethernet installée sur l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="7e102-128">There is normally one adapter per Ethernet adapter installed in the host machine.</span></span> <span data-ttu-id="7e102-129">Par exemple, supposons qu’un ordinateur hôte contenait un adaptateur étiqueté « 10/100 ENET ».</span><span class="sxs-lookup"><span data-stu-id="7e102-129">For example, let's say a host machine had an adapter labeled "10/100 ENET".</span></span> <span data-ttu-id="7e102-130">Pour connecter une carte réseau virtuelle au réseau attaché à « 10/100 ENET », définissez la propriété réseau **Hostadapter** du réseau virtuel sur « 10/100 ENET » et connectez la carte réseau virtuelle à ce réseau virtuel.</span><span class="sxs-lookup"><span data-stu-id="7e102-130">To connect a virtual NIC to the network attached to "10/100 ENET", set the virtual network's Network **HostAdapter** property to "10/100 ENET" and connect the virtual NIC to this virtual network.</span></span>

<span data-ttu-id="7e102-131">Si la propriété **Hostadapter** est définie sur une chaîne vide (""), la carte réseau virtuelle est connectée au réseau « réseau interne » ou au réseau « réseau partagé ».</span><span class="sxs-lookup"><span data-stu-id="7e102-131">If the **HostAdapter** property is set to an empty string (""), the virtual NIC adapter is connected to the "Internal Network" or "Shared Networking (NAT)" network.</span></span> <span data-ttu-id="7e102-132">Les cartes réseau virtuelles connectées au réseau « réseau interne » n’ont pas accès aux réseaux externes sur l’hôte système.</span><span class="sxs-lookup"><span data-stu-id="7e102-132">Virtual NICs attached to the "Internal Network" network will have no access to external networks on the system host.</span></span> <span data-ttu-id="7e102-133">Toutefois, les cartes réseau virtuelles attachées à ce réseau virtuel peuvent toujours communiquer entre elles.</span><span class="sxs-lookup"><span data-stu-id="7e102-133">However, the virtual NICs attached to this virtual network are still able to communicate with each other.</span></span>

<span data-ttu-id="7e102-134">La liste complète des adaptateurs est accessible par le biais de la propriété [**IVMHostInfo :: NetworkAdapters**](ivmhostinfo-networkadapters.md) .</span><span class="sxs-lookup"><span data-stu-id="7e102-134">The complete list of adapters can be accessed through the [**IVMHostInfo::NetworkAdapters**](ivmhostinfo-networkadapters.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e102-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7e102-135">Requirements</span></span>



| <span data-ttu-id="7e102-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7e102-136">Requirement</span></span> | <span data-ttu-id="7e102-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="7e102-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e102-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e102-138">Minimum supported client</span></span><br/> | <span data-ttu-id="7e102-139">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7e102-139">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7e102-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e102-140">Minimum supported server</span></span><br/> | <span data-ttu-id="7e102-141">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e102-141">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7e102-142">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="7e102-142">End of client support</span></span><br/>    | <span data-ttu-id="7e102-143">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7e102-143">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7e102-144">Produit</span><span class="sxs-lookup"><span data-stu-id="7e102-144">Product</span></span><br/>                  | <span data-ttu-id="7e102-145">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7e102-145">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7e102-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="7e102-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e102-147"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e102-147"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="7e102-148">IID</span><span class="sxs-lookup"><span data-stu-id="7e102-148">IID</span></span><br/>                      | <span data-ttu-id="7e102-149">IID \_ IVMVirtualNetwork est défini en tant que 431cb7a1-2469-4563-b94e-38b987adca63</span><span class="sxs-lookup"><span data-stu-id="7e102-149">IID\_IVMVirtualNetwork is defined as 431cb7a1-2469-4563-b94e-38b987adca63</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="7e102-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7e102-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e102-151">**IVMVirtualNetwork**</span><span class="sxs-lookup"><span data-stu-id="7e102-151">**IVMVirtualNetwork**</span></span>](ivmvirtualnetwork.md)
</dt> </dl>

 

