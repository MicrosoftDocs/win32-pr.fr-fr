---
title: IVMNetworkAdapterCollection, propriété d’élément (VPCCOMInterfaces. h)
description: Objet IVMNetworkAdapter qui correspond à l’index spécifié.
ms.assetid: 3de76e24-3315-473f-870b-074be8bcfe70
keywords:
- Propriété de l’élément Virtual PC
- Propriété d’élément Virtual PC, interface IVMNetworkAdapterCollection
- IVMNetworkAdapterCollection interface Virtual PC, propriété Item
topic_type:
- apiref
api_name:
- IVMNetworkAdapterCollection.Item
- IVMNetworkAdapterCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63d2f7ee389938a44c6608241fb3fb2d48ec1bca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942777"
---
# <a name="ivmnetworkadaptercollectionitem-property"></a><span data-ttu-id="a9dc9-106">IVMNetworkAdapterCollection :: Item, propriété</span><span class="sxs-lookup"><span data-stu-id="a9dc9-106">IVMNetworkAdapterCollection::Item property</span></span>

<span data-ttu-id="a9dc9-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a9dc9-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a9dc9-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a9dc9-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a9dc9-109">Récupère l’objet [**IVMNetworkAdapter**](ivmnetworkadapter.md) qui correspond à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="a9dc9-109">Retrieves the [**IVMNetworkAdapter**](ivmnetworkadapter.md) object that corresponds to the specified index.</span></span>

<span data-ttu-id="a9dc9-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="a9dc9-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9dc9-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a9dc9-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long              index,
  [out, retval] IVMNetworkAdapter **networkInterface
);
```



## <a name="property-value"></a><span data-ttu-id="a9dc9-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="a9dc9-112">Property value</span></span>

<span data-ttu-id="a9dc9-113">Objet [**IVMNetworkAdapter**](ivmnetworkadapter.md) .</span><span class="sxs-lookup"><span data-stu-id="a9dc9-113">The [**IVMNetworkAdapter**](ivmnetworkadapter.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a9dc9-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="a9dc9-114">Error codes</span></span>



| <span data-ttu-id="a9dc9-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="a9dc9-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="a9dc9-116">Signification</span><span class="sxs-lookup"><span data-stu-id="a9dc9-116">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a9dc9-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a9dc9-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="a9dc9-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="a9dc9-118">The operation was successful.</span></span> <br/>                                                      |
| <dl> <span data-ttu-id="a9dc9-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="a9dc9-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="a9dc9-120">Le paramètre *l’interface réseau* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="a9dc9-120">The *networkInterface* parameter is **NULL**.</span></span> <br/>                                      |
| <dl> <span data-ttu-id="a9dc9-121"><dt>DISP \_ \_BADINDEX</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="a9dc9-121"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="a9dc9-122">L’index de l’élément demandé ne correspond pas à un élément de cette collection.</span><span class="sxs-lookup"><span data-stu-id="a9dc9-122">The index of the requested item does not correspond to an item in this collection.</span></span> <br/> |
| <dl> <span data-ttu-id="a9dc9-123"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="a9dc9-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="a9dc9-124">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="a9dc9-124">An unexpected error has occurred.</span></span><br/>                                                   |



## <a name="requirements"></a><span data-ttu-id="a9dc9-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a9dc9-125">Requirements</span></span>



| <span data-ttu-id="a9dc9-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a9dc9-126">Requirement</span></span> | <span data-ttu-id="a9dc9-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="a9dc9-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9dc9-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9dc9-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a9dc9-129">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a9dc9-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a9dc9-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9dc9-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a9dc9-131">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9dc9-131">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="a9dc9-132">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="a9dc9-132">End of client support</span></span><br/>    | <span data-ttu-id="a9dc9-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a9dc9-133">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="a9dc9-134">Produit</span><span class="sxs-lookup"><span data-stu-id="a9dc9-134">Product</span></span><br/>                  | <span data-ttu-id="a9dc9-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a9dc9-135">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="a9dc9-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="a9dc9-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9dc9-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9dc9-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="a9dc9-138">IID</span><span class="sxs-lookup"><span data-stu-id="a9dc9-138">IID</span></span><br/>                      | <span data-ttu-id="a9dc9-139">IID \_ IVMNetworkAdapterCollection est défini en tant que ebaeafe9-EBCD-47cf-866e-ad87d735e479</span><span class="sxs-lookup"><span data-stu-id="a9dc9-139">IID\_IVMNetworkAdapterCollection is defined as ebaeafe9-ebcd-47cf-866e-ad87d735e479</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a9dc9-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a9dc9-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9dc9-141">**IVMNetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="a9dc9-141">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> <dt>

[<span data-ttu-id="a9dc9-142">**IVMNetworkAdapterCollection**</span><span class="sxs-lookup"><span data-stu-id="a9dc9-142">**IVMNetworkAdapterCollection**</span></span>](ivmnetworkadaptercollection.md)
</dt> </dl>

 

