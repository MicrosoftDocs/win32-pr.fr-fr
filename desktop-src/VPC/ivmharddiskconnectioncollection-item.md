---
title: IVMHardDiskConnectionCollection, propriété d’élément (VPCCOMInterfaces. h)
description: Récupère l’objet de connexion de disque dur qui correspond à l’index spécifié.
ms.assetid: 24e158fb-b026-4619-9d0d-a59cd782894f
keywords:
- Propriété de l’élément Virtual PC
- Propriété d’élément Virtual PC, interface IVMHardDiskConnectionCollection
- IVMHardDiskConnectionCollection interface Virtual PC, propriété Item
topic_type:
- apiref
api_name:
- IVMHardDiskConnectionCollection.Item
- IVMHardDiskConnectionCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5558e70cfcf18f67c14e52160737b851fa9ea2c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106541162"
---
# <a name="ivmharddiskconnectioncollectionitem-property"></a><span data-ttu-id="24b4a-106">IVMHardDiskConnectionCollection :: Item, propriété</span><span class="sxs-lookup"><span data-stu-id="24b4a-106">IVMHardDiskConnectionCollection::Item property</span></span>

<span data-ttu-id="24b4a-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="24b4a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="24b4a-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="24b4a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="24b4a-109">Récupère l’objet de connexion de disque dur qui correspond à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="24b4a-109">Retrieves the hard disk connection object that corresponds to the specified index.</span></span>

<span data-ttu-id="24b4a-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="24b4a-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="24b4a-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="24b4a-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long                  index,
  [out, retval] IVMHardDiskConnection **hardDiskConnection
);
```



## <a name="property-value"></a><span data-ttu-id="24b4a-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="24b4a-112">Property value</span></span>

<span data-ttu-id="24b4a-113">Objet [**IVMHardDiskConnection**](ivmharddiskconnection.md) .</span><span class="sxs-lookup"><span data-stu-id="24b4a-113">The [**IVMHardDiskConnection**](ivmharddiskconnection.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="24b4a-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="24b4a-114">Error codes</span></span>



| <span data-ttu-id="24b4a-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="24b4a-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="24b4a-116">Signification</span><span class="sxs-lookup"><span data-stu-id="24b4a-116">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="24b4a-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="24b4a-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="24b4a-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="24b4a-118">The operation was successful.</span></span> <br/>                                                      |
| <dl> <span data-ttu-id="24b4a-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="24b4a-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="24b4a-120">Le paramètre *hardDiskConnection* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="24b4a-120">The *hardDiskConnection* parameter is **NULL**.</span></span> <br/>                                    |
| <dl> <span data-ttu-id="24b4a-121"><dt>DISP \_ \_BADINDEX</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="24b4a-121"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="24b4a-122">L’index de l’élément demandé ne correspond pas à un élément de cette collection.</span><span class="sxs-lookup"><span data-stu-id="24b4a-122">The index of the requested item does not correspond to an item in this collection.</span></span> <br/> |
| <dl> <span data-ttu-id="24b4a-123"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="24b4a-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="24b4a-124">La configuration est inconnue.</span><span class="sxs-lookup"><span data-stu-id="24b4a-124">The configuration is unknown.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="24b4a-125"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="24b4a-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="24b4a-126">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="24b4a-126">An unexpected error has occurred.</span></span><br/>                                                   |



## <a name="requirements"></a><span data-ttu-id="24b4a-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="24b4a-127">Requirements</span></span>



| <span data-ttu-id="24b4a-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="24b4a-128">Requirement</span></span> | <span data-ttu-id="24b4a-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="24b4a-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24b4a-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="24b4a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="24b4a-131">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="24b4a-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                         |
| <span data-ttu-id="24b4a-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="24b4a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="24b4a-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="24b4a-133">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="24b4a-134">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="24b4a-134">End of client support</span></span><br/>    | <span data-ttu-id="24b4a-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="24b4a-135">Windows 7</span></span><br/>                                                                               |
| <span data-ttu-id="24b4a-136">Produit</span><span class="sxs-lookup"><span data-stu-id="24b4a-136">Product</span></span><br/>                  | <span data-ttu-id="24b4a-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="24b4a-137">Windows Virtual PC</span></span><br/>                                                                      |
| <span data-ttu-id="24b4a-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="24b4a-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="24b4a-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="24b4a-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>      |
| <span data-ttu-id="24b4a-140">IID</span><span class="sxs-lookup"><span data-stu-id="24b4a-140">IID</span></span><br/>                      | <span data-ttu-id="24b4a-141">IID \_ IVMHardDiskconnectionCollection est défini en tant que b9f2caf4-0aeb-4085-B105-ceddb90dbf62</span><span class="sxs-lookup"><span data-stu-id="24b4a-141">IID\_IVMHardDiskconnectionCollection is defined as b9f2caf4-0aeb-4085-b105-ceddb90dbf62</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="24b4a-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="24b4a-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24b4a-143">**IVMHardDiskConnection**</span><span class="sxs-lookup"><span data-stu-id="24b4a-143">**IVMHardDiskConnection**</span></span>](ivmharddiskconnection.md)
</dt> <dt>

[<span data-ttu-id="24b4a-144">**IVMHardDiskConnectionCollection**</span><span class="sxs-lookup"><span data-stu-id="24b4a-144">**IVMHardDiskConnectionCollection**</span></span>](ivmharddiskconnectioncollection.md)
</dt> </dl>

 

