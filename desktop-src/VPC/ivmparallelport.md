---
title: Interface IVMParallelPort (VPCCOMInterfaces. h)
description: Définit un port parallèle à l’intérieur d’une machine virtuelle.
ms.assetid: da8daf16-5d22-49be-8fe9-72d5018c0622
keywords:
- Virtual PC de l’interface IVMParallelPort
- IVMParallelPort interface Virtual PC, Description
topic_type:
- apiref
api_name:
- IVMParallelPort
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71b76b23f48e728104a3826afa80a8f272cd7e66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512204"
---
# <a name="ivmparallelport-interface"></a><span data-ttu-id="b885a-105">Interface IVMParallelPort</span><span class="sxs-lookup"><span data-stu-id="b885a-105">IVMParallelPort interface</span></span>

<span data-ttu-id="b885a-106">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b885a-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b885a-107">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b885a-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b885a-108">Définit un port parallèle à l’intérieur d’une machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="b885a-108">Defines a parallel port inside a virtual machine.</span></span> <span data-ttu-id="b885a-109">Cette interface vous permet de configurer des ports parallèles à l’intérieur d’une machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="b885a-109">This interface allows you to configure parallel ports inside a virtual machine.</span></span> <span data-ttu-id="b885a-110">Vous pouvez récupérer un objet **IVMParallelPort** à partir de l’objet [**IVMParallelPortCollection**](ivmparallelportcollection.md) retourné à partir de la propriété [**IVMVirtualMachine ::P arallelports**](ivmvirtualmachine-parallelports.md) .</span><span class="sxs-lookup"><span data-stu-id="b885a-110">You can retrieve an **IVMParallelPort** object from the [**IVMParallelPortCollection**](ivmparallelportcollection.md) object returned from the [**IVMVirtualMachine::ParallelPorts**](ivmvirtualmachine-parallelports.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="b885a-111">Membres</span><span class="sxs-lookup"><span data-stu-id="b885a-111">Members</span></span>

<span data-ttu-id="b885a-112">L’interface **IVMParallelPort** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="b885a-112">The **IVMParallelPort** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="b885a-113">**IVMParallelPort** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b885a-113">**IVMParallelPort** also has these types of members:</span></span>

-   [<span data-ttu-id="b885a-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b885a-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="b885a-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b885a-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b885a-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b885a-116">Methods</span></span>

<span data-ttu-id="b885a-117">L’interface **IVMParallelPort** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="b885a-117">The **IVMParallelPort** interface has these methods.</span></span>



| <span data-ttu-id="b885a-118">Méthode</span><span class="sxs-lookup"><span data-stu-id="b885a-118">Method</span></span>                              | <span data-ttu-id="b885a-119">Description</span><span class="sxs-lookup"><span data-stu-id="b885a-119">Description</span></span>                                                        |
|:------------------------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="b885a-120">**\_IDENTIFI**</span><span class="sxs-lookup"><span data-stu-id="b885a-120">**\_ID**</span></span>](ivmparallelport--id.md) | <span data-ttu-id="b885a-121">Récupère l’identificateur interne du port parallèle.</span><span class="sxs-lookup"><span data-stu-id="b885a-121">Retrieves the internal identifier of the parallel port.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b885a-122">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b885a-122">Properties</span></span>

<span data-ttu-id="b885a-123">L’interface **IVMParallelPort** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="b885a-123">The **IVMParallelPort** interface has these properties.</span></span>



| <span data-ttu-id="b885a-124">Propriété</span><span class="sxs-lookup"><span data-stu-id="b885a-124">Property</span></span>                                        | <span data-ttu-id="b885a-125">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="b885a-125">Access type</span></span>           | <span data-ttu-id="b885a-126">Description</span><span class="sxs-lookup"><span data-stu-id="b885a-126">Description</span></span>                               |
|:------------------------------------------------|:----------------------|:------------------------------------------|
| [<span data-ttu-id="b885a-127">**Nom**</span><span class="sxs-lookup"><span data-stu-id="b885a-127">**Name**</span></span>](ivmparallelport-name.md)<br/> | <span data-ttu-id="b885a-128">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b885a-128">Read/write</span></span><br/> | <span data-ttu-id="b885a-129">Nom du port parallèle.</span><span class="sxs-lookup"><span data-stu-id="b885a-129">The name of the parallel port.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b885a-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b885a-130">Requirements</span></span>



| <span data-ttu-id="b885a-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b885a-131">Requirement</span></span> | <span data-ttu-id="b885a-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="b885a-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b885a-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b885a-133">Minimum supported client</span></span><br/> | <span data-ttu-id="b885a-134">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b885a-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b885a-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b885a-135">Minimum supported server</span></span><br/> | <span data-ttu-id="b885a-136">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b885a-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b885a-137">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="b885a-137">End of client support</span></span><br/>    | <span data-ttu-id="b885a-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b885a-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b885a-139">Produit</span><span class="sxs-lookup"><span data-stu-id="b885a-139">Product</span></span><br/>                  | <span data-ttu-id="b885a-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b885a-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b885a-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="b885a-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="b885a-142"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b885a-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b885a-143">IID</span><span class="sxs-lookup"><span data-stu-id="b885a-143">IID</span></span><br/>                      | <span data-ttu-id="b885a-144">IID \_ IVMParallelPort est défini en tant que 097beecb-0a02-474F-abd6-298b22293fc6</span><span class="sxs-lookup"><span data-stu-id="b885a-144">IID\_IVMParallelPort is defined as 097beecb-0a02-474f-abd6-298b22293fc6</span></span><br/>            |



 

