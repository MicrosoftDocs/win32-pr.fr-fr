---
title: IVMHostInfo ProcessorManufacturerString, propriété (VPCCOMInterfaces. h)
description: Récupère le fabricant du processeur hôte.
ms.assetid: b7f4a03a-184c-4996-8102-994bf7f37e50
keywords:
- ProcessorManufacturerString propriété Virtual PC
- ProcessorManufacturerString, propriété Virtual PC, IVMHostInfo, interface
- IVMHostInfo interface Virtual PC, propriété ProcessorManufacturerString
topic_type:
- apiref
api_name:
- IVMHostInfo.ProcessorManufacturerString
- IVMHostInfo.get_ProcessorManufacturerString
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 029e64f0a13d84bea118498726893620e058ac83
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032304"
---
# <a name="ivmhostinfoprocessormanufacturerstring-property"></a><span data-ttu-id="7be28-106">IVMHostInfo ::P propriété rocessorManufacturerString</span><span class="sxs-lookup"><span data-stu-id="7be28-106">IVMHostInfo::ProcessorManufacturerString property</span></span>

<span data-ttu-id="7be28-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7be28-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7be28-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7be28-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7be28-109">Récupère le fabricant du processeur hôte.</span><span class="sxs-lookup"><span data-stu-id="7be28-109">Retrieves the manufacturer of the host processor.</span></span>

<span data-ttu-id="7be28-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="7be28-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7be28-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7be28-111">Syntax</span></span>


```C++
HRESULT get_ProcessorManufacturerString(
  [out, retval] BSTR *processorManufacturerString
);
```



## <a name="property-value"></a><span data-ttu-id="7be28-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="7be28-112">Property value</span></span>

<span data-ttu-id="7be28-113">Le fabricant.</span><span class="sxs-lookup"><span data-stu-id="7be28-113">The manufacturer.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7be28-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="7be28-114">Error codes</span></span>



| <span data-ttu-id="7be28-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="7be28-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="7be28-116">Signification</span><span class="sxs-lookup"><span data-stu-id="7be28-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="7be28-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7be28-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="7be28-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="7be28-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="7be28-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="7be28-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="7be28-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="7be28-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="7be28-121"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="7be28-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="7be28-122">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="7be28-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="7be28-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7be28-123">Requirements</span></span>



| <span data-ttu-id="7be28-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7be28-124">Requirement</span></span> | <span data-ttu-id="7be28-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="7be28-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7be28-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7be28-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7be28-127">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7be28-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7be28-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7be28-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7be28-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7be28-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7be28-130">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="7be28-130">End of client support</span></span><br/>    | <span data-ttu-id="7be28-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7be28-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7be28-132">Produit</span><span class="sxs-lookup"><span data-stu-id="7be28-132">Product</span></span><br/>                  | <span data-ttu-id="7be28-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7be28-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7be28-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="7be28-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="7be28-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="7be28-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="7be28-136">IID</span><span class="sxs-lookup"><span data-stu-id="7be28-136">IID</span></span><br/>                      | <span data-ttu-id="7be28-137">IID \_ IVMHostInfo est défini en tant que 5b5cf343-05ad-453B-BE99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="7be28-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="7be28-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7be28-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7be28-139">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="7be28-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

