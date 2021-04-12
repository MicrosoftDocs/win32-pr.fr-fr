---
title: IVMTaskCollection, propriété d’élément (VPCCOMInterfaces. h)
description: Récupère l’objet de tâche qui correspond à l’index spécifié.
ms.assetid: e4738b7a-12d6-4aed-992d-2f70c5cdd4d0
keywords:
- Propriété de l’élément Virtual PC
- Propriété d’élément Virtual PC, interface IVMTaskCollection
- IVMTaskCollection interface Virtual PC, propriété Item
topic_type:
- apiref
api_name:
- IVMTaskCollection.Item
- IVMTaskCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f445280834383ee594fbb53a3390c91b1928f4ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508981"
---
# <a name="ivmtaskcollectionitem-property"></a><span data-ttu-id="fb62f-106">IVMTaskCollection :: Item, propriété</span><span class="sxs-lookup"><span data-stu-id="fb62f-106">IVMTaskCollection::Item property</span></span>

<span data-ttu-id="fb62f-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="fb62f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="fb62f-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="fb62f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="fb62f-109">Récupère l’objet de tâche qui correspond à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="fb62f-109">Retrieves the task object that corresponds to the specified index.</span></span>

<span data-ttu-id="fb62f-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="fb62f-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb62f-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fb62f-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long    index,
  [out, retval] IVMTask **task
);
```



## <a name="property-value"></a><span data-ttu-id="fb62f-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="fb62f-112">Property value</span></span>

<span data-ttu-id="fb62f-113">Objet [**IVMTask**](ivmtask.md) .</span><span class="sxs-lookup"><span data-stu-id="fb62f-113">The [**IVMTask**](ivmtask.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fb62f-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="fb62f-114">Error codes</span></span>



| <span data-ttu-id="fb62f-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="fb62f-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="fb62f-116">Signification</span><span class="sxs-lookup"><span data-stu-id="fb62f-116">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fb62f-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="fb62f-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="fb62f-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="fb62f-118">The operation was successful.</span></span> <br/>                                                      |
| <dl> <span data-ttu-id="fb62f-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="fb62f-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="fb62f-120">Le paramètre de *tâche* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="fb62f-120">The *task* parameter is **NULL**.</span></span> <br/>                                                  |
| <dl> <span data-ttu-id="fb62f-121"><dt>DISP \_ \_BADINDEX</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="fb62f-121"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="fb62f-122">L’index de l’élément demandé ne correspond pas à un élément de cette collection.</span><span class="sxs-lookup"><span data-stu-id="fb62f-122">The index of the requested item does not correspond to an item in this collection.</span></span> <br/> |
| <dl> <span data-ttu-id="fb62f-123"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="fb62f-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="fb62f-124">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="fb62f-124">An unexpected error has occurred.</span></span><br/>                                                   |



## <a name="requirements"></a><span data-ttu-id="fb62f-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fb62f-125">Requirements</span></span>



| <span data-ttu-id="fb62f-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fb62f-126">Requirement</span></span> | <span data-ttu-id="fb62f-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="fb62f-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb62f-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fb62f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="fb62f-129">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fb62f-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fb62f-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fb62f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="fb62f-131">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="fb62f-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="fb62f-132">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="fb62f-132">End of client support</span></span><br/>    | <span data-ttu-id="fb62f-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fb62f-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="fb62f-134">Produit</span><span class="sxs-lookup"><span data-stu-id="fb62f-134">Product</span></span><br/>                  | <span data-ttu-id="fb62f-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="fb62f-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="fb62f-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="fb62f-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb62f-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb62f-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="fb62f-138">IID</span><span class="sxs-lookup"><span data-stu-id="fb62f-138">IID</span></span><br/>                      | <span data-ttu-id="fb62f-139">IID \_ IVMTaskCollection est défini en tant que 5c4387c8-0e8b-4B97-8058-84679adf4c40</span><span class="sxs-lookup"><span data-stu-id="fb62f-139">IID\_IVMTaskCollection is defined as 5c4387c8-0e8b-4b97-8058-84679adf4c40</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="fb62f-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fb62f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb62f-141">**IVMTask**</span><span class="sxs-lookup"><span data-stu-id="fb62f-141">**IVMTask**</span></span>](ivmtask.md)
</dt> <dt>

[<span data-ttu-id="fb62f-142">**IVMTaskCollection**</span><span class="sxs-lookup"><span data-stu-id="fb62f-142">**IVMTaskCollection**</span></span>](ivmtaskcollection.md)
</dt> </dl>

 

