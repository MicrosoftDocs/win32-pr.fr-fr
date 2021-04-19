---
title: IVMFloppyDriveCollection _NewEnum, propriété (VPCCOMInterfaces. h)
description: Récupère un énumérateur pour la collection. | IVMFloppyDriveCollection _NewEnum, propriété (VPCCOMInterfaces. h)
ms.assetid: 06de9560-cba9-4c64-907e-83e77781cafc
keywords:
- _NewEnum de la propriété Virtual PC
- _NewEnum propriété Virtual PC, interface IVMFloppyDriveCollection
- IVMFloppyDriveCollection interface Virtual PC, propriété _NewEnum
topic_type:
- apiref
api_name:
- IVMFloppyDriveCollection._NewEnum
- IVMFloppyDriveCollection.get__NewEnum
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7db9960ca627b66442e583c6e6bc8fdc89d8d878
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106538284"
---
# <a name="ivmfloppydrivecollection_newenum-property"></a><span data-ttu-id="4612a-107">IVMFloppyDriveCollection :: \_ NewEnum, propriété</span><span class="sxs-lookup"><span data-stu-id="4612a-107">IVMFloppyDriveCollection::\_NewEnum property</span></span>

<span data-ttu-id="4612a-108">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4612a-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4612a-109">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4612a-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4612a-110">Récupère un énumérateur pour la collection.</span><span class="sxs-lookup"><span data-stu-id="4612a-110">Retrieves an enumerator for the collection.</span></span>

<span data-ttu-id="4612a-111">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="4612a-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4612a-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4612a-112">Syntax</span></span>


```C++
HRESULT get__NewEnum(
  [out, retval] IUnknown **enumerator
);
```



## <a name="property-value"></a><span data-ttu-id="4612a-113">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="4612a-113">Property value</span></span>

<span data-ttu-id="4612a-114">Énumérateur [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) .</span><span class="sxs-lookup"><span data-stu-id="4612a-114">The [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) enumerator.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4612a-115">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="4612a-115">Error codes</span></span>



| <span data-ttu-id="4612a-116">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="4612a-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="4612a-117">Signification</span><span class="sxs-lookup"><span data-stu-id="4612a-117">Meaning</span></span>                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="4612a-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4612a-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="4612a-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="4612a-119">The operation was successful.</span></span><br/> |
| <dl> <span data-ttu-id="4612a-120"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="4612a-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="4612a-121">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="4612a-121">The parameter is **NULL**.</span></span><br/>    |
| <dl> <span data-ttu-id="4612a-122"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="4612a-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="4612a-123">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="4612a-123">An unexpected error occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="4612a-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4612a-124">Requirements</span></span>



| <span data-ttu-id="4612a-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4612a-125">Requirement</span></span> | <span data-ttu-id="4612a-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="4612a-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4612a-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4612a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="4612a-128">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4612a-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4612a-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4612a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="4612a-130">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="4612a-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4612a-131">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="4612a-131">End of client support</span></span><br/>    | <span data-ttu-id="4612a-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4612a-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4612a-133">Produit</span><span class="sxs-lookup"><span data-stu-id="4612a-133">Product</span></span><br/>                  | <span data-ttu-id="4612a-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4612a-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4612a-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="4612a-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="4612a-136"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="4612a-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4612a-137">IID</span><span class="sxs-lookup"><span data-stu-id="4612a-137">IID</span></span><br/>                      | <span data-ttu-id="4612a-138">IID \_ IVMFloppyDriveCollection est défini en tant que 8ba70a25-F698-4EE5-85ce-3cc93a925516</span><span class="sxs-lookup"><span data-stu-id="4612a-138">IID\_IVMFloppyDriveCollection is defined as 8ba70a25-f698-4ee5-85ce-3cc93a925516</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="4612a-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4612a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4612a-140">**IVMFloppyDriveCollection**</span><span class="sxs-lookup"><span data-stu-id="4612a-140">**IVMFloppyDriveCollection**</span></span>](ivmfloppydrivecollection.md)
</dt> </dl>

 

