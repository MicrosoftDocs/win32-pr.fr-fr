---
title: Interface IVMVirtualNetwork (VPCCOMInterfaces. h)
description: Définit un réseau virtuel.
ms.assetid: 1ddafc33-05d4-45fb-924d-9830288aa240
keywords:
- Virtual PC de l’interface IVMVirtualNetwork
- IVMVirtualNetwork interface Virtual PC, Description
topic_type:
- apiref
api_name:
- IVMVirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06fb7c759059034874890f1dba7f7e2d1280ea8a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512203"
---
# <a name="ivmvirtualnetwork-interface"></a><span data-ttu-id="258ea-105">Interface IVMVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="258ea-105">IVMVirtualNetwork interface</span></span>

<span data-ttu-id="258ea-106">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="258ea-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="258ea-107">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="258ea-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="258ea-108">Définit un réseau virtuel.</span><span class="sxs-lookup"><span data-stu-id="258ea-108">Defines a virtual network.</span></span> <span data-ttu-id="258ea-109">Les objets **IVMVirtualNetwork** sont retournés à partir de la méthode [**IVMVirtualPC**](ivmvirtualpc.md) [**FindVirtualNetwork**](ivmvirtualpc-findvirtualnetwork.md).</span><span class="sxs-lookup"><span data-stu-id="258ea-109">**IVMVirtualNetwork** objects are returned from [**IVMVirtualPC**](ivmvirtualpc.md) method [**FindVirtualNetwork**](ivmvirtualpc-findvirtualnetwork.md).</span></span> <span data-ttu-id="258ea-110">Vous pouvez également récupérer un objet **IVMVirtualNetwork** à partir de l’objet [**IVMVirtualNetworkCollection**](ivmvirtualnetworkcollection.md) retourné à partir de la propriété [**IVMVirtualPC :: VirtualNetworks**](ivmvirtualpc-virtualnetworks.md) .</span><span class="sxs-lookup"><span data-stu-id="258ea-110">You can also retrieve an **IVMVirtualNetwork** object from the [**IVMVirtualNetworkCollection**](ivmvirtualnetworkcollection.md) object returned from the [**IVMVirtualPC::VirtualNetworks**](ivmvirtualpc-virtualnetworks.md) property.</span></span>

<span data-ttu-id="258ea-111">Un réseau virtuel se compose d’un commutateur virtuel qui effectue tout le routage interne et plusieurs connexions « connectées » au commutateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="258ea-111">A virtual network consists of a virtual switch, which performs all internal routing, and several connections that are "plugged in" to the virtual switch.</span></span> <span data-ttu-id="258ea-112">Ces connexions peuvent être une connexion d’hôte externe réelle, un « réseau interne » ou une mise en réseau partagée (NAT).</span><span class="sxs-lookup"><span data-stu-id="258ea-112">These connections can be a real external host connection, an "internal network" or shared networking (NAT).</span></span>

## <a name="members"></a><span data-ttu-id="258ea-113">Membres</span><span class="sxs-lookup"><span data-stu-id="258ea-113">Members</span></span>

<span data-ttu-id="258ea-114">L’interface **IVMVirtualNetwork** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="258ea-114">The **IVMVirtualNetwork** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="258ea-115">**IVMVirtualNetwork** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="258ea-115">**IVMVirtualNetwork** also has these types of members:</span></span>

-   [<span data-ttu-id="258ea-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="258ea-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="258ea-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="258ea-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="258ea-118">Méthodes</span><span class="sxs-lookup"><span data-stu-id="258ea-118">Methods</span></span>

<span data-ttu-id="258ea-119">L’interface **IVMVirtualNetwork** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="258ea-119">The **IVMVirtualNetwork** interface has these methods.</span></span>



| <span data-ttu-id="258ea-120">Méthode</span><span class="sxs-lookup"><span data-stu-id="258ea-120">Method</span></span>                                | <span data-ttu-id="258ea-121">Description</span><span class="sxs-lookup"><span data-stu-id="258ea-121">Description</span></span>                                                          |
|:--------------------------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="258ea-122">**\_IDENTIFI**</span><span class="sxs-lookup"><span data-stu-id="258ea-122">**\_ID**</span></span>](ivmvirtualnetwork--id.md) | <span data-ttu-id="258ea-123">Récupère l’identificateur interne du réseau virtuel.</span><span class="sxs-lookup"><span data-stu-id="258ea-123">Retrieves the internal identifier of the virtual network.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="258ea-124">Propriétés</span><span class="sxs-lookup"><span data-stu-id="258ea-124">Properties</span></span>

<span data-ttu-id="258ea-125">L’interface **IVMVirtualNetwork** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="258ea-125">The **IVMVirtualNetwork** interface has these properties.</span></span>



| <span data-ttu-id="258ea-126">Propriété</span><span class="sxs-lookup"><span data-stu-id="258ea-126">Property</span></span>                                                                | <span data-ttu-id="258ea-127">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="258ea-127">Access type</span></span>          | <span data-ttu-id="258ea-128">Description</span><span class="sxs-lookup"><span data-stu-id="258ea-128">Description</span></span>                                                                    |
|:------------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="258ea-129">**HostAdapter**</span><span class="sxs-lookup"><span data-stu-id="258ea-129">**HostAdapter**</span></span>](ivmvirtualnetwork-hostadapter.md)<br/>         | <span data-ttu-id="258ea-130">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="258ea-130">Read-only</span></span><br/> | <span data-ttu-id="258ea-131">Nom de l’adaptateur auquel le réseau virtuel est connecté.</span><span class="sxs-lookup"><span data-stu-id="258ea-131">The name of the adapter to which the virtual network is connected.</span></span><br/>  |
| <span data-ttu-id="258ea-132">[**MediaType**](/previous-versions/windows/desktop/legacy/dd796707(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="258ea-132">[**MediaType**](/previous-versions/windows/desktop/legacy/dd796707(v=vs.85))</span></span><br/>             | <span data-ttu-id="258ea-133">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="258ea-133">Read-only</span></span><br/> | <span data-ttu-id="258ea-134">Détermine si l’instance de réseau virtuel est sans fil ou non.</span><span class="sxs-lookup"><span data-stu-id="258ea-134">Determines whether the virtual network instance is wireless or not.</span></span><br/> |
| [<span data-ttu-id="258ea-135">**Nom**</span><span class="sxs-lookup"><span data-stu-id="258ea-135">**Name**</span></span>](ivmvirtualnetwork-name.md)<br/>                       | <span data-ttu-id="258ea-136">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="258ea-136">Read-only</span></span><br/> | <span data-ttu-id="258ea-137">Nom unique de l’instance de réseau virtuel.</span><span class="sxs-lookup"><span data-stu-id="258ea-137">The unique name of the virtual network instance.</span></span><br/>                    |
| [<span data-ttu-id="258ea-138">**NetworkAdapters**</span><span class="sxs-lookup"><span data-stu-id="258ea-138">**NetworkAdapters**</span></span>](ivmvirtualnetwork-networkadapters.md)<br/> | <span data-ttu-id="258ea-139">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="258ea-139">Read-only</span></span><br/> | <span data-ttu-id="258ea-140">Collection énumérable de cartes réseau attachées au réseau virtuel.</span><span class="sxs-lookup"><span data-stu-id="258ea-140">An enumerable collection of NICs attached to the virtual network.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="258ea-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="258ea-141">Requirements</span></span>



| <span data-ttu-id="258ea-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="258ea-142">Requirement</span></span> | <span data-ttu-id="258ea-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="258ea-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="258ea-144">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="258ea-144">Minimum supported client</span></span><br/> | <span data-ttu-id="258ea-145">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="258ea-145">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="258ea-146">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="258ea-146">Minimum supported server</span></span><br/> | <span data-ttu-id="258ea-147">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="258ea-147">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="258ea-148">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="258ea-148">End of client support</span></span><br/>    | <span data-ttu-id="258ea-149">Windows 7</span><span class="sxs-lookup"><span data-stu-id="258ea-149">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="258ea-150">Produit</span><span class="sxs-lookup"><span data-stu-id="258ea-150">Product</span></span><br/>                  | <span data-ttu-id="258ea-151">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="258ea-151">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="258ea-152">En-tête</span><span class="sxs-lookup"><span data-stu-id="258ea-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="258ea-153"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="258ea-153"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="258ea-154">IID</span><span class="sxs-lookup"><span data-stu-id="258ea-154">IID</span></span><br/>                      | <span data-ttu-id="258ea-155">IID \_ IVMVirtualNetwork est défini en tant que 431cb7a1-2469-4563-b94e-38b987adca63</span><span class="sxs-lookup"><span data-stu-id="258ea-155">IID\_IVMVirtualNetwork is defined as 431cb7a1-2469-4563-b94e-38b987adca63</span></span><br/>          |



 

