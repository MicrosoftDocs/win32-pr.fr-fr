---
title: Propriété IVMHostInfo OperatingSystem (VPCCOMInterfaces. h)
description: Récupère le système d’exploitation en cours d’exécution sur l’ordinateur.
ms.assetid: 1164bb7d-cdce-4649-86d6-22e3ea7bad98
keywords:
- Propriété OperatingSystem Virtual PC
- Propriété OperatingSystem Virtual PC, interface IVMHostInfo
- IVMHostInfo interface Virtual PC, OperatingSystem, propriété
topic_type:
- apiref
api_name:
- IVMHostInfo.OperatingSystem
- IVMHostInfo.get_OperatingSystem
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55af1d0cfdc2abaa01fe78c08509c2448b4d8cc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106529073"
---
# <a name="ivmhostinfooperatingsystem-property"></a><span data-ttu-id="3f672-106">IVMHostInfo :: OperatingSystem, propriété</span><span class="sxs-lookup"><span data-stu-id="3f672-106">IVMHostInfo::OperatingSystem property</span></span>

<span data-ttu-id="3f672-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3f672-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3f672-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3f672-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3f672-109">Récupère le système d’exploitation en cours d’exécution sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="3f672-109">Retrieves the operating system running on the machine.</span></span>

<span data-ttu-id="3f672-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3f672-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f672-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3f672-111">Syntax</span></span>


```C++
HRESULT get_OperatingSystem(
  [out, retval] BSTR *operatingSystem
);
```



## <a name="property-value"></a><span data-ttu-id="3f672-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="3f672-112">Property value</span></span>

<span data-ttu-id="3f672-113">Nom du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="3f672-113">The name of the operating system.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3f672-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="3f672-114">Error codes</span></span>



| <span data-ttu-id="3f672-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="3f672-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="3f672-116">Signification</span><span class="sxs-lookup"><span data-stu-id="3f672-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="3f672-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3f672-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="3f672-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="3f672-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="3f672-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="3f672-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="3f672-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="3f672-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="3f672-121"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="3f672-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="3f672-122">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="3f672-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="3f672-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3f672-123">Requirements</span></span>



| <span data-ttu-id="3f672-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3f672-124">Requirement</span></span> | <span data-ttu-id="3f672-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="3f672-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f672-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3f672-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3f672-127">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3f672-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3f672-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3f672-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3f672-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="3f672-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3f672-130">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="3f672-130">End of client support</span></span><br/>    | <span data-ttu-id="3f672-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3f672-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3f672-132">Produit</span><span class="sxs-lookup"><span data-stu-id="3f672-132">Product</span></span><br/>                  | <span data-ttu-id="3f672-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3f672-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3f672-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="3f672-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f672-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f672-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3f672-136">IID</span><span class="sxs-lookup"><span data-stu-id="3f672-136">IID</span></span><br/>                      | <span data-ttu-id="3f672-137">IID \_ IVMHostInfo est défini en tant que 5b5cf343-05ad-453B-BE99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="3f672-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="3f672-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f672-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f672-139">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="3f672-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

