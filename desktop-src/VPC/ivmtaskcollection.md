---
title: Interface IVMTaskCollection (VPCCOMInterfaces. h)
description: Définit la collection d’objets Task. Pour obtenir un objet IVMTaskCollection, utilisez la propriété tâches IVMVirtualPC.
ms.assetid: 5cfc543c-81a1-49d2-93a9-9b1db1cb5070
keywords:
- Virtual PC de l’interface IVMTaskCollection
- IVMTaskCollection interface Virtual PC, Description
topic_type:
- apiref
api_name:
- IVMTaskCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43ff7a4b12b936f2b5c72a73818eca0f927eef12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385043"
---
# <a name="ivmtaskcollection-interface"></a><span data-ttu-id="d3508-106">Interface IVMTaskCollection</span><span class="sxs-lookup"><span data-stu-id="d3508-106">IVMTaskCollection interface</span></span>

<span data-ttu-id="d3508-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d3508-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d3508-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d3508-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d3508-109">Définit la collection d’objets Task.</span><span class="sxs-lookup"><span data-stu-id="d3508-109">Defines the collection of task objects.</span></span> <span data-ttu-id="d3508-110">Pour obtenir un objet **IVMTaskCollection** , utilisez la propriété [**IVMVirtualPC :: Tasks**](ivmvirtualpc-tasks.md) .</span><span class="sxs-lookup"><span data-stu-id="d3508-110">To obtain an **IVMTaskCollection** object, use the [**IVMVirtualPC::Tasks**](ivmvirtualpc-tasks.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="d3508-111">Membres</span><span class="sxs-lookup"><span data-stu-id="d3508-111">Members</span></span>

<span data-ttu-id="d3508-112">L’interface **IVMTaskCollection** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="d3508-112">The **IVMTaskCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="d3508-113">**IVMTaskCollection** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d3508-113">**IVMTaskCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="d3508-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d3508-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d3508-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d3508-115">Properties</span></span>

<span data-ttu-id="d3508-116">L’interface **IVMTaskCollection** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="d3508-116">The **IVMTaskCollection** interface has these properties.</span></span>



| <span data-ttu-id="d3508-117">Propriété</span><span class="sxs-lookup"><span data-stu-id="d3508-117">Property</span></span>                                                   | <span data-ttu-id="d3508-118">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="d3508-118">Access type</span></span>          | <span data-ttu-id="d3508-119">Description</span><span class="sxs-lookup"><span data-stu-id="d3508-119">Description</span></span>                                                         |
|:-----------------------------------------------------------|:---------------------|:--------------------------------------------------------------------|
| [<span data-ttu-id="d3508-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="d3508-120">**\_NewEnum**</span></span>](ivmtaskcollection--newenum.md)<br/> | <span data-ttu-id="d3508-121">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d3508-121">Read-only</span></span><br/> | <span data-ttu-id="d3508-122">Énumérateur de la collection.</span><span class="sxs-lookup"><span data-stu-id="d3508-122">An enumerator for the collection.</span></span><br/>                        |
| [<span data-ttu-id="d3508-123">**Saut**</span><span class="sxs-lookup"><span data-stu-id="d3508-123">**Count**</span></span>](ivmtaskcollection-count.md)<br/>        | <span data-ttu-id="d3508-124">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d3508-124">Read-only</span></span><br/> | <span data-ttu-id="d3508-125">Nombre de tâches de cette collection.</span><span class="sxs-lookup"><span data-stu-id="d3508-125">The number of tasks in this collection.</span></span><br/>                  |
| [<span data-ttu-id="d3508-126">**Élément**</span><span class="sxs-lookup"><span data-stu-id="d3508-126">**Item**</span></span>](ivmtaskcollection-item.md)<br/>          | <span data-ttu-id="d3508-127">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d3508-127">Read-only</span></span><br/> | <span data-ttu-id="d3508-128">Objet de tâche qui correspond à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="d3508-128">The task object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d3508-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d3508-129">Requirements</span></span>



| <span data-ttu-id="d3508-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d3508-130">Requirement</span></span> | <span data-ttu-id="d3508-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="d3508-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3508-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d3508-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d3508-133">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d3508-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d3508-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d3508-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d3508-135">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d3508-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d3508-136">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="d3508-136">End of client support</span></span><br/>    | <span data-ttu-id="d3508-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d3508-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d3508-138">Produit</span><span class="sxs-lookup"><span data-stu-id="d3508-138">Product</span></span><br/>                  | <span data-ttu-id="d3508-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d3508-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d3508-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="d3508-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3508-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3508-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d3508-142">IID</span><span class="sxs-lookup"><span data-stu-id="d3508-142">IID</span></span><br/>                      | <span data-ttu-id="d3508-143">IID \_ IVMTaskCollection est défini en tant que 5c4387c8-0e8b-4B97-8058-84679adf4c40</span><span class="sxs-lookup"><span data-stu-id="d3508-143">IID\_IVMTaskCollection is defined as 5c4387c8-0e8b-4b97-8058-84679adf4c40</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="d3508-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d3508-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3508-145">**IVMTask**</span><span class="sxs-lookup"><span data-stu-id="d3508-145">**IVMTask**</span></span>](ivmtask.md)
</dt> <dt>

[<span data-ttu-id="d3508-146">**IVMVirtualPC :: Tasks**</span><span class="sxs-lookup"><span data-stu-id="d3508-146">**IVMVirtualPC::Tasks**</span></span>](ivmvirtualpc-tasks.md)
</dt> </dl>

 

