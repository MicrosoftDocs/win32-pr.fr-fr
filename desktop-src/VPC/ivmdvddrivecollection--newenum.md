---
title: IVMDVDDriveCollection _NewEnum, propriété (VPCCOMInterfaces. h)
description: Récupère un énumérateur pour la collection de CD/DVD.
ms.assetid: e911628b-2a92-41e5-9271-556a297d747d
keywords:
- _NewEnum de la propriété Virtual PC
- _NewEnum propriété Virtual PC, interface IVMDVDDriveCollection
- IVMDVDDriveCollection interface Virtual PC, propriété _NewEnum
topic_type:
- apiref
api_name:
- IVMDVDDriveCollection._NewEnum
- IVMDVDDriveCollection.get__NewEnum
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dfd0de3aaf6b25808d1afa591b0c2099599e6bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942080"
---
# <a name="ivmdvddrivecollection_newenum-property"></a><span data-ttu-id="984c4-106">IVMDVDDriveCollection :: \_ NewEnum, propriété</span><span class="sxs-lookup"><span data-stu-id="984c4-106">IVMDVDDriveCollection::\_NewEnum property</span></span>

<span data-ttu-id="984c4-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="984c4-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="984c4-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="984c4-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="984c4-109">Récupère un énumérateur pour la collection de CD/DVD.</span><span class="sxs-lookup"><span data-stu-id="984c4-109">Retrieves an enumerator for the CD/DVD collection.</span></span>

<span data-ttu-id="984c4-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="984c4-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="984c4-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="984c4-111">Syntax</span></span>


```C++
HRESULT get__NewEnum(
  [out, retval] IUnknown **enumerator
);
```



## <a name="property-value"></a><span data-ttu-id="984c4-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="984c4-112">Property value</span></span>

<span data-ttu-id="984c4-113">Énumérateur [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) .</span><span class="sxs-lookup"><span data-stu-id="984c4-113">The [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) enumerator.</span></span>

## <a name="error-codes"></a><span data-ttu-id="984c4-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="984c4-114">Error codes</span></span>



| <span data-ttu-id="984c4-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="984c4-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="984c4-116">Signification</span><span class="sxs-lookup"><span data-stu-id="984c4-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="984c4-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="984c4-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="984c4-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="984c4-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="984c4-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="984c4-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="984c4-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="984c4-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="984c4-121"><dt>E \_ ÉCHEC</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="984c4-121"><dt>E\_FAIL</dt> <dt>0x80004005</dt></span></span> </dl>            | <span data-ttu-id="984c4-122">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="984c4-122">An unexpected error has occurred.</span></span><br/> |
| <dl> <span data-ttu-id="984c4-123"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="984c4-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="984c4-124">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="984c4-124">An unexpected error occurred.</span></span><br/>     |



## <a name="requirements"></a><span data-ttu-id="984c4-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="984c4-125">Requirements</span></span>



| <span data-ttu-id="984c4-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="984c4-126">Requirement</span></span> | <span data-ttu-id="984c4-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="984c4-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="984c4-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="984c4-128">Minimum supported client</span></span><br/> | <span data-ttu-id="984c4-129">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="984c4-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="984c4-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="984c4-130">Minimum supported server</span></span><br/> | <span data-ttu-id="984c4-131">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="984c4-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="984c4-132">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="984c4-132">End of client support</span></span><br/>    | <span data-ttu-id="984c4-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="984c4-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="984c4-134">Produit</span><span class="sxs-lookup"><span data-stu-id="984c4-134">Product</span></span><br/>                  | <span data-ttu-id="984c4-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="984c4-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="984c4-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="984c4-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="984c4-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="984c4-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="984c4-138">IID</span><span class="sxs-lookup"><span data-stu-id="984c4-138">IID</span></span><br/>                      | <span data-ttu-id="984c4-139">IID \_ IVMDVDDriveCollection est défini en tant que bc86e297-e55f-4742-9614-ad11d3131f68</span><span class="sxs-lookup"><span data-stu-id="984c4-139">IID\_IVMDVDDriveCollection is defined as bc86e297-e55f-4742-9614-ad11d3131f68</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="984c4-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="984c4-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="984c4-141">**IVMDVDDriveCollection**</span><span class="sxs-lookup"><span data-stu-id="984c4-141">**IVMDVDDriveCollection**</span></span>](ivmdvddrivecollection.md)
</dt> </dl>

 

