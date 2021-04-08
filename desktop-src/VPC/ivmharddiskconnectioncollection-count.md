---
title: Propriété Count IVMHardDiskConnectionCollection (VPCCOMInterfaces. h)
description: Récupère le nombre de connexions de disque dur dans cette collection.
ms.assetid: 913c1bb7-0237-4f11-9873-7b42a94004f8
keywords:
- Propriété Count Virtual PC
- Propriété Count Virtual PC, IVMHardDiskConnectionCollection, interface
- IVMHardDiskConnectionCollection interface Virtual PC, propriété Count
topic_type:
- apiref
api_name:
- IVMHardDiskConnectionCollection.Count
- IVMHardDiskConnectionCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f34bbf4d07d7c5967ccfc38e16a743105de8e69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741756"
---
# <a name="ivmharddiskconnectioncollectioncount-property"></a><span data-ttu-id="f3b62-106">IVMHardDiskConnectionCollection :: Count, propriété</span><span class="sxs-lookup"><span data-stu-id="f3b62-106">IVMHardDiskConnectionCollection::Count property</span></span>

<span data-ttu-id="f3b62-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f3b62-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f3b62-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f3b62-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f3b62-109">Récupère le nombre de connexions de disque dur dans cette collection.</span><span class="sxs-lookup"><span data-stu-id="f3b62-109">Retrieves the number of hard disk connections in this collection.</span></span>

<span data-ttu-id="f3b62-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="f3b62-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3b62-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f3b62-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="f3b62-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="f3b62-112">Property value</span></span>

<span data-ttu-id="f3b62-113">Nombre de connexions de disque dur.</span><span class="sxs-lookup"><span data-stu-id="f3b62-113">The number of hard disk connections.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f3b62-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="f3b62-114">Error codes</span></span>



| <span data-ttu-id="f3b62-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="f3b62-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="f3b62-116">Signification</span><span class="sxs-lookup"><span data-stu-id="f3b62-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="f3b62-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f3b62-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="f3b62-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="f3b62-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="f3b62-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="f3b62-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="f3b62-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="f3b62-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="f3b62-121"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="f3b62-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="f3b62-122">La configuration est inconnue.</span><span class="sxs-lookup"><span data-stu-id="f3b62-122">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="f3b62-123"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="f3b62-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="f3b62-124">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="f3b62-124">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="f3b62-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f3b62-125">Requirements</span></span>



| <span data-ttu-id="f3b62-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f3b62-126">Requirement</span></span> | <span data-ttu-id="f3b62-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3b62-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3b62-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f3b62-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f3b62-129">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f3b62-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                         |
| <span data-ttu-id="f3b62-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f3b62-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f3b62-131">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="f3b62-131">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="f3b62-132">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="f3b62-132">End of client support</span></span><br/>    | <span data-ttu-id="f3b62-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f3b62-133">Windows 7</span></span><br/>                                                                               |
| <span data-ttu-id="f3b62-134">Produit</span><span class="sxs-lookup"><span data-stu-id="f3b62-134">Product</span></span><br/>                  | <span data-ttu-id="f3b62-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f3b62-135">Windows Virtual PC</span></span><br/>                                                                      |
| <span data-ttu-id="f3b62-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="f3b62-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3b62-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3b62-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>      |
| <span data-ttu-id="f3b62-138">IID</span><span class="sxs-lookup"><span data-stu-id="f3b62-138">IID</span></span><br/>                      | <span data-ttu-id="f3b62-139">IID \_ IVMHardDiskconnectionCollection est défini en tant que b9f2caf4-0aeb-4085-B105-ceddb90dbf62</span><span class="sxs-lookup"><span data-stu-id="f3b62-139">IID\_IVMHardDiskconnectionCollection is defined as b9f2caf4-0aeb-4085-b105-ceddb90dbf62</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f3b62-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3b62-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3b62-141">**IVMHardDiskConnectionCollection**</span><span class="sxs-lookup"><span data-stu-id="f3b62-141">**IVMHardDiskConnectionCollection**</span></span>](ivmharddiskconnectioncollection.md)
</dt> </dl>

 

