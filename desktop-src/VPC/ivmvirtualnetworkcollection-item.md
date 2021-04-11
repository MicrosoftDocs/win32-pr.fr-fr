---
title: IVMVirtualNetworkCollection, propriété d’élément (VPCCOMInterfaces. h)
description: Objet IVMVirtualNetwork qui correspond à l’index spécifié.
ms.assetid: 1c6a3449-f76a-4216-8840-0fb9fb133e67
keywords:
- Propriété de l’élément Virtual PC
- Propriété d’élément Virtual PC, interface IVMVirtualNetworkCollection
- IVMVirtualNetworkCollection interface Virtual PC, propriété Item
topic_type:
- apiref
api_name:
- IVMVirtualNetworkCollection.Item
- IVMVirtualNetworkCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac5a7648db4708fbc1b445029419ee794809abcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032952"
---
# <a name="ivmvirtualnetworkcollectionitem-property"></a><span data-ttu-id="100fb-106">IVMVirtualNetworkCollection :: Item, propriété</span><span class="sxs-lookup"><span data-stu-id="100fb-106">IVMVirtualNetworkCollection::Item property</span></span>

<span data-ttu-id="100fb-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="100fb-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="100fb-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="100fb-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="100fb-109">Récupère l’objet [**IVMVirtualNetwork**](ivmvirtualnetwork.md) qui correspond à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="100fb-109">Retrieves the [**IVMVirtualNetwork**](ivmvirtualnetwork.md) object that corresponds to the specified index.</span></span>

<span data-ttu-id="100fb-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="100fb-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="100fb-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="100fb-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long              index,
  [out, retval] IVMVirtualNetwork **virtualNetwork
);
```



## <a name="property-value"></a><span data-ttu-id="100fb-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="100fb-112">Property value</span></span>

<span data-ttu-id="100fb-113">Objet [**IVMVirtualNetwork**](ivmvirtualnetwork.md) .</span><span class="sxs-lookup"><span data-stu-id="100fb-113">The [**IVMVirtualNetwork**](ivmvirtualnetwork.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="100fb-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="100fb-114">Error codes</span></span>



| <span data-ttu-id="100fb-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="100fb-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="100fb-116">Signification</span><span class="sxs-lookup"><span data-stu-id="100fb-116">Meaning</span></span>                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="100fb-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="100fb-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="100fb-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="100fb-118">The operation was successful.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="100fb-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="100fb-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="100fb-120">Le paramètre *virtualNetwork* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="100fb-120">The *virtualNetwork* parameter is **NULL**.</span></span><br/>                                        |
| <dl> <span data-ttu-id="100fb-121"><dt>DISP \_ \_BADINDEX</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="100fb-121"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="100fb-122">L’index de l’élément demandé ne correspond pas à un élément de cette collection.</span><span class="sxs-lookup"><span data-stu-id="100fb-122">The index of the requested item does not correspond to an item in this collection.</span></span><br/> |
| <dl> <span data-ttu-id="100fb-123"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="100fb-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="100fb-124">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="100fb-124">An unexpected error has occurred.</span></span><br/>                                                  |



## <a name="requirements"></a><span data-ttu-id="100fb-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="100fb-125">Requirements</span></span>



| <span data-ttu-id="100fb-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="100fb-126">Requirement</span></span> | <span data-ttu-id="100fb-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="100fb-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="100fb-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="100fb-128">Minimum supported client</span></span><br/> | <span data-ttu-id="100fb-129">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="100fb-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="100fb-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="100fb-130">Minimum supported server</span></span><br/> | <span data-ttu-id="100fb-131">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="100fb-131">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="100fb-132">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="100fb-132">End of client support</span></span><br/>    | <span data-ttu-id="100fb-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="100fb-133">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="100fb-134">Produit</span><span class="sxs-lookup"><span data-stu-id="100fb-134">Product</span></span><br/>                  | <span data-ttu-id="100fb-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="100fb-135">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="100fb-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="100fb-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="100fb-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="100fb-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="100fb-138">IID</span><span class="sxs-lookup"><span data-stu-id="100fb-138">IID</span></span><br/>                      | <span data-ttu-id="100fb-139">IID \_ IVMVirtualNetworkCollection est défini en tant que 8ed680be-4242-4B2A-A21C-1982d8b0f675</span><span class="sxs-lookup"><span data-stu-id="100fb-139">IID\_IVMVirtualNetworkCollection is defined as 8ed680be-4242-4b2a-a21c-1982d8b0f675</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="100fb-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="100fb-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="100fb-141">**IVMVirtualNetwork**</span><span class="sxs-lookup"><span data-stu-id="100fb-141">**IVMVirtualNetwork**</span></span>](ivmvirtualnetwork.md)
</dt> <dt>

[<span data-ttu-id="100fb-142">**IVMVirtualNetworkCollection**</span><span class="sxs-lookup"><span data-stu-id="100fb-142">**IVMVirtualNetworkCollection**</span></span>](ivmvirtualnetworkcollection.md)
</dt> </dl>

 

