---
title: Interface IVMVirtualNetworkCollection (VPCCOMInterfaces. h)
description: Définit une collection d’objets IVMVirtualNetwork. Pour obtenir un objet IVMVirtualNetworkCollection, utilisez la propriété VirtualNetworks IVMVirtualPC.
ms.assetid: 3d595bc3-1a8d-4e09-a809-944d4dcdc675
keywords:
- Virtual PC de l’interface IVMVirtualNetworkCollection
- IVMVirtualNetworkCollection interface Virtual PC, Description
topic_type:
- apiref
api_name:
- IVMVirtualNetworkCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76935fd4a67983847e211d8aa53f4a616bed9d4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743084"
---
# <a name="ivmvirtualnetworkcollection-interface"></a><span data-ttu-id="c8853-106">Interface IVMVirtualNetworkCollection</span><span class="sxs-lookup"><span data-stu-id="c8853-106">IVMVirtualNetworkCollection interface</span></span>

<span data-ttu-id="c8853-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c8853-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c8853-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c8853-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c8853-109">Définit une collection d’objets [**IVMVirtualNetwork**](ivmvirtualnetwork.md) .</span><span class="sxs-lookup"><span data-stu-id="c8853-109">Defines a collection of [**IVMVirtualNetwork**](ivmvirtualnetwork.md) objects.</span></span> <span data-ttu-id="c8853-110">Pour obtenir un objet **IVMVirtualNetworkCollection** , utilisez la propriété [**IVMVirtualPC :: VirtualNetworks**](ivmvirtualpc-virtualnetworks.md) .</span><span class="sxs-lookup"><span data-stu-id="c8853-110">To obtain an **IVMVirtualNetworkCollection** object, use the [**IVMVirtualPC::VirtualNetworks**](ivmvirtualpc-virtualnetworks.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="c8853-111">Membres</span><span class="sxs-lookup"><span data-stu-id="c8853-111">Members</span></span>

<span data-ttu-id="c8853-112">L’interface **IVMVirtualNetworkCollection** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="c8853-112">The **IVMVirtualNetworkCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="c8853-113">**IVMVirtualNetworkCollection** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c8853-113">**IVMVirtualNetworkCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="c8853-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c8853-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c8853-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c8853-115">Properties</span></span>

<span data-ttu-id="c8853-116">L’interface **IVMVirtualNetworkCollection** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="c8853-116">The **IVMVirtualNetworkCollection** interface has these properties.</span></span>



| <span data-ttu-id="c8853-117">Propriété</span><span class="sxs-lookup"><span data-stu-id="c8853-117">Property</span></span>                                                             | <span data-ttu-id="c8853-118">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="c8853-118">Access type</span></span>          | <span data-ttu-id="c8853-119">Description</span><span class="sxs-lookup"><span data-stu-id="c8853-119">Description</span></span>                                                                                                   |
|:---------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c8853-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="c8853-120">**\_NewEnum**</span></span>](ivmvirtualnetworkcollection--newenum.md)<br/> | <span data-ttu-id="c8853-121">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c8853-121">Read-only</span></span><br/> | <span data-ttu-id="c8853-122">Énumérateur de la collection.</span><span class="sxs-lookup"><span data-stu-id="c8853-122">An enumerator for the collection.</span></span><br/>                                                                  |
| [<span data-ttu-id="c8853-123">**Saut**</span><span class="sxs-lookup"><span data-stu-id="c8853-123">**Count**</span></span>](ivmvirtualnetworkcollection-count.md)<br/>        | <span data-ttu-id="c8853-124">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c8853-124">Read-only</span></span><br/> | <span data-ttu-id="c8853-125">Nombre de réseaux virtuels dans ce regroupement.</span><span class="sxs-lookup"><span data-stu-id="c8853-125">The number of virtual networks in this collection.</span></span><br/>                                                 |
| [<span data-ttu-id="c8853-126">**Élément**</span><span class="sxs-lookup"><span data-stu-id="c8853-126">**Item**</span></span>](ivmvirtualnetworkcollection-item.md)<br/>          | <span data-ttu-id="c8853-127">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c8853-127">Read-only</span></span><br/> | <span data-ttu-id="c8853-128">Objet [**IVMVirtualNetwork**](ivmvirtualnetwork.md) qui correspond à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="c8853-128">The [**IVMVirtualNetwork**](ivmvirtualnetwork.md) object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c8853-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c8853-129">Requirements</span></span>



| <span data-ttu-id="c8853-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c8853-130">Requirement</span></span> | <span data-ttu-id="c8853-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="c8853-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8853-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c8853-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c8853-133">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c8853-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c8853-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c8853-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c8853-135">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c8853-135">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="c8853-136">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="c8853-136">End of client support</span></span><br/>    | <span data-ttu-id="c8853-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c8853-137">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="c8853-138">Produit</span><span class="sxs-lookup"><span data-stu-id="c8853-138">Product</span></span><br/>                  | <span data-ttu-id="c8853-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c8853-139">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="c8853-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="c8853-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8853-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8853-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="c8853-142">IID</span><span class="sxs-lookup"><span data-stu-id="c8853-142">IID</span></span><br/>                      | <span data-ttu-id="c8853-143">IID \_ IVMVirtualNetworkCollection est défini en tant que 8ed680be-4242-4B2A-A21C-1982d8b0f675</span><span class="sxs-lookup"><span data-stu-id="c8853-143">IID\_IVMVirtualNetworkCollection is defined as 8ed680be-4242-4b2a-a21c-1982d8b0f675</span></span><br/> |



 

