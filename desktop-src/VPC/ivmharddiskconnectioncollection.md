---
title: Interface IVMHardDiskConnectionCollection (VPCCOMInterfaces. h)
description: Définit la collection de connexions de disque dur au sein de la machine virtuelle. Pour obtenir un objet IVMHardDiskConnectionCollection, utilisez la propriété HardDiskConnections IVMVirtualMachine.
ms.assetid: 3440318c-45f4-4d24-9609-dbe5ca59b005
keywords:
- Virtual PC de l’interface IVMHardDiskConnectionCollection
- IVMHardDiskConnectionCollection interface Virtual PC, Description
topic_type:
- apiref
api_name:
- IVMHardDiskConnectionCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbde67f226c5b2d8cb86a8764c6dd61c24c2a468
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464186"
---
# <a name="ivmharddiskconnectioncollection-interface"></a><span data-ttu-id="18943-106">Interface IVMHardDiskConnectionCollection</span><span class="sxs-lookup"><span data-stu-id="18943-106">IVMHardDiskConnectionCollection interface</span></span>

<span data-ttu-id="18943-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="18943-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="18943-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="18943-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="18943-109">Définit la collection de connexions de disque dur au sein de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="18943-109">Defines the collection of hard disk connections within the virtual machine.</span></span> <span data-ttu-id="18943-110">Pour obtenir un objet **IVMHardDiskConnectionCollection** , utilisez la propriété [**IVMVirtualMachine :: HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md) .</span><span class="sxs-lookup"><span data-stu-id="18943-110">To obtain an **IVMHardDiskConnectionCollection** object, use the [**IVMVirtualMachine::HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="18943-111">Membres</span><span class="sxs-lookup"><span data-stu-id="18943-111">Members</span></span>

<span data-ttu-id="18943-112">L’interface **IVMHardDiskConnectionCollection** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="18943-112">The **IVMHardDiskConnectionCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="18943-113">**IVMHardDiskConnectionCollection** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="18943-113">**IVMHardDiskConnectionCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="18943-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="18943-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="18943-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="18943-115">Properties</span></span>

<span data-ttu-id="18943-116">L’interface **IVMHardDiskConnectionCollection** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="18943-116">The **IVMHardDiskConnectionCollection** interface has these properties.</span></span>



| <span data-ttu-id="18943-117">Propriété</span><span class="sxs-lookup"><span data-stu-id="18943-117">Property</span></span>                                                                 | <span data-ttu-id="18943-118">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="18943-118">Access type</span></span>          | <span data-ttu-id="18943-119">Description</span><span class="sxs-lookup"><span data-stu-id="18943-119">Description</span></span>                                                                         |
|:-------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------|
| [<span data-ttu-id="18943-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="18943-120">**\_NewEnum**</span></span>](ivmharddiskconnectioncollection--newenum.md)<br/> | <span data-ttu-id="18943-121">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18943-121">Read-only</span></span><br/> | <span data-ttu-id="18943-122">Énumérateur de la collection.</span><span class="sxs-lookup"><span data-stu-id="18943-122">An enumerator for the collection.</span></span><br/>                                        |
| [<span data-ttu-id="18943-123">**Saut**</span><span class="sxs-lookup"><span data-stu-id="18943-123">**Count**</span></span>](ivmharddiskconnectioncollection-count.md)<br/>        | <span data-ttu-id="18943-124">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18943-124">Read-only</span></span><br/> | <span data-ttu-id="18943-125">Nombre de connexions de disque dur dans ce regroupement.</span><span class="sxs-lookup"><span data-stu-id="18943-125">The number of hard disk connections in this collection.</span></span><br/>                  |
| [<span data-ttu-id="18943-126">**Élément**</span><span class="sxs-lookup"><span data-stu-id="18943-126">**Item**</span></span>](ivmharddiskconnectioncollection-item.md)<br/>          | <span data-ttu-id="18943-127">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18943-127">Read-only</span></span><br/> | <span data-ttu-id="18943-128">Objet de connexion de disque dur qui correspond à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="18943-128">The hard disk connection object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="18943-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="18943-129">Requirements</span></span>



| <span data-ttu-id="18943-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="18943-130">Requirement</span></span> | <span data-ttu-id="18943-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="18943-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18943-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18943-132">Minimum supported client</span></span><br/> | <span data-ttu-id="18943-133">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="18943-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                         |
| <span data-ttu-id="18943-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18943-134">Minimum supported server</span></span><br/> | <span data-ttu-id="18943-135">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="18943-135">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="18943-136">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="18943-136">End of client support</span></span><br/>    | <span data-ttu-id="18943-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="18943-137">Windows 7</span></span><br/>                                                                               |
| <span data-ttu-id="18943-138">Produit</span><span class="sxs-lookup"><span data-stu-id="18943-138">Product</span></span><br/>                  | <span data-ttu-id="18943-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="18943-139">Windows Virtual PC</span></span><br/>                                                                      |
| <span data-ttu-id="18943-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="18943-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="18943-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="18943-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>      |
| <span data-ttu-id="18943-142">IID</span><span class="sxs-lookup"><span data-stu-id="18943-142">IID</span></span><br/>                      | <span data-ttu-id="18943-143">IID \_ IVMHardDiskconnectionCollection est défini en tant que b9f2caf4-0aeb-4085-B105-ceddb90dbf62</span><span class="sxs-lookup"><span data-stu-id="18943-143">IID\_IVMHardDiskconnectionCollection is defined as b9f2caf4-0aeb-4085-b105-ceddb90dbf62</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="18943-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18943-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18943-145">**IVMHardDiskConnection**</span><span class="sxs-lookup"><span data-stu-id="18943-145">**IVMHardDiskConnection**</span></span>](ivmharddiskconnection.md)
</dt> <dt>

[<span data-ttu-id="18943-146">**IVMVirtualMachine::HardDiskConnections**</span><span class="sxs-lookup"><span data-stu-id="18943-146">**IVMVirtualMachine::HardDiskConnections**</span></span>](ivmvirtualmachine-harddiskconnections.md)
</dt> </dl>

 

