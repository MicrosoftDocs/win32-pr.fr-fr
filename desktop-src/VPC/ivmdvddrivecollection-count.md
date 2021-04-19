---
title: Propriété Count IVMDVDDriveCollection (VPCCOMInterfaces. h)
description: Récupère le nombre de lecteurs de CD et de DVD dans ce regroupement.
ms.assetid: 22e39c42-1f98-4680-a97e-0d329dc608e2
keywords:
- Propriété Count Virtual PC
- Propriété Count Virtual PC, IVMDVDDriveCollection, interface
- IVMDVDDriveCollection interface Virtual PC, propriété Count
topic_type:
- apiref
api_name:
- IVMDVDDriveCollection.Count
- IVMDVDDriveCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e9ea713810348c0bd78c7de307600fc6ac9adc0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510332"
---
# <a name="ivmdvddrivecollectioncount-property"></a><span data-ttu-id="a6878-106">IVMDVDDriveCollection :: Count, propriété</span><span class="sxs-lookup"><span data-stu-id="a6878-106">IVMDVDDriveCollection::Count property</span></span>

<span data-ttu-id="a6878-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a6878-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a6878-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a6878-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a6878-109">Récupère le nombre de lecteurs de CD et de DVD dans ce regroupement.</span><span class="sxs-lookup"><span data-stu-id="a6878-109">Retrieves the number of CD and DVD drives in this collection.</span></span>

<span data-ttu-id="a6878-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="a6878-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6878-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a6878-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="a6878-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="a6878-112">Property value</span></span>

<span data-ttu-id="a6878-113">Nombre de lecteurs de CD et DVD.</span><span class="sxs-lookup"><span data-stu-id="a6878-113">The number of CD and DVD drives.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a6878-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="a6878-114">Error codes</span></span>



| <span data-ttu-id="a6878-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="a6878-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="a6878-116">Signification</span><span class="sxs-lookup"><span data-stu-id="a6878-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="a6878-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a6878-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="a6878-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="a6878-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="a6878-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="a6878-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="a6878-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="a6878-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="a6878-121"><dt>E \_ ÉCHEC</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="a6878-121"><dt>E\_FAIL</dt> <dt>0x80004005</dt></span></span> </dl>            | <span data-ttu-id="a6878-122">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="a6878-122">An unexpected error has occurred.</span></span><br/> |
| <dl> <span data-ttu-id="a6878-123"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="a6878-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="a6878-124">La configuration est inconnue.</span><span class="sxs-lookup"><span data-stu-id="a6878-124">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="a6878-125"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="a6878-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="a6878-126">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="a6878-126">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="a6878-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a6878-127">Requirements</span></span>



| <span data-ttu-id="a6878-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a6878-128">Requirement</span></span> | <span data-ttu-id="a6878-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="a6878-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6878-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a6878-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a6878-131">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a6878-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a6878-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a6878-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a6878-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a6878-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a6878-134">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="a6878-134">End of client support</span></span><br/>    | <span data-ttu-id="a6878-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a6878-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a6878-136">Produit</span><span class="sxs-lookup"><span data-stu-id="a6878-136">Product</span></span><br/>                  | <span data-ttu-id="a6878-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a6878-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a6878-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="a6878-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6878-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6878-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a6878-140">IID</span><span class="sxs-lookup"><span data-stu-id="a6878-140">IID</span></span><br/>                      | <span data-ttu-id="a6878-141">IID \_ IVMDVDDriveCollection est défini en tant que bc86e297-e55f-4742-9614-ad11d3131f68</span><span class="sxs-lookup"><span data-stu-id="a6878-141">IID\_IVMDVDDriveCollection is defined as bc86e297-e55f-4742-9614-ad11d3131f68</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="a6878-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a6878-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6878-143">**IVMDVDDriveCollection**</span><span class="sxs-lookup"><span data-stu-id="a6878-143">**IVMDVDDriveCollection**</span></span>](ivmdvddrivecollection.md)
</dt> </dl>

 

