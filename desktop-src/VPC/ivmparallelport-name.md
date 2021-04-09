---
title: Propriété IVMParallelPort Name (VPCCOMInterfaces. h)
description: Nom du port parallèle.
ms.assetid: 254df134-2b48-4a81-8229-0f5fbacf2e1c
keywords:
- Propriété de nom Virtual PC
- Propriété de nom Virtual PC, interface IVMParallelPort
- IVMParallelPort interface Virtual PC, propriété Name
topic_type:
- apiref
api_name:
- IVMParallelPort.Name
- IVMParallelPort.get_Name
- IVMParallelPort.put_Name
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42f89638504b7e0fd8814ea8b429ee70f43c6c67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102804"
---
# <a name="ivmparallelportname-property"></a><span data-ttu-id="abf65-106">IVMParallelPort :: Name, propriété</span><span class="sxs-lookup"><span data-stu-id="abf65-106">IVMParallelPort::Name property</span></span>

<span data-ttu-id="abf65-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="abf65-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="abf65-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="abf65-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="abf65-109">Récupère et définit le nom du port parallèle.</span><span class="sxs-lookup"><span data-stu-id="abf65-109">Retrieves and sets the name of the parallel port.</span></span>

<span data-ttu-id="abf65-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="abf65-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="abf65-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="abf65-111">Syntax</span></span>


```C++
HRESULT put_Name(
  [in]          BSTR portName
);

HRESULT get_Name(
  [out, retval] BSTR *portName
);
```



## <a name="property-value"></a><span data-ttu-id="abf65-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="abf65-112">Property value</span></span>

<span data-ttu-id="abf65-113">Définit le nom du port parallèle (par exemple, « LPT1 »).</span><span class="sxs-lookup"><span data-stu-id="abf65-113">Sets the name of the parallel port (for example, "LPT1").</span></span>

## <a name="error-codes"></a><span data-ttu-id="abf65-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="abf65-114">Error codes</span></span>



| <span data-ttu-id="abf65-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="abf65-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="abf65-116">Signification</span><span class="sxs-lookup"><span data-stu-id="abf65-116">Meaning</span></span>                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="abf65-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="abf65-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="abf65-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="abf65-118">The operation was successful.</span></span><br/>                              |
| <dl> <span data-ttu-id="abf65-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="abf65-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="abf65-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="abf65-120">The parameter is **NULL**.</span></span><br/>                                 |
| <dl> <span data-ttu-id="abf65-121"><dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="abf65-121"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="abf65-122">Le paramètre fait référence à un port parallèle qui n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="abf65-122">The parameter refers to a parallel port that is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="abf65-123"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="abf65-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="abf65-124">La configuration de cet ordinateur virtuel n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="abf65-124">The configuration for this virtual machine is not valid.</span></span><br/>   |
| <dl> <span data-ttu-id="abf65-125"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="abf65-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="abf65-126">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="abf65-126">An unexpected error has occurred.</span></span><br/>                          |



## <a name="requirements"></a><span data-ttu-id="abf65-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="abf65-127">Requirements</span></span>



| <span data-ttu-id="abf65-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="abf65-128">Requirement</span></span> | <span data-ttu-id="abf65-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="abf65-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="abf65-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="abf65-130">Minimum supported client</span></span><br/> | <span data-ttu-id="abf65-131">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="abf65-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="abf65-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="abf65-132">Minimum supported server</span></span><br/> | <span data-ttu-id="abf65-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="abf65-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="abf65-134">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="abf65-134">End of client support</span></span><br/>    | <span data-ttu-id="abf65-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="abf65-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="abf65-136">Produit</span><span class="sxs-lookup"><span data-stu-id="abf65-136">Product</span></span><br/>                  | <span data-ttu-id="abf65-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="abf65-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="abf65-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="abf65-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="abf65-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="abf65-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="abf65-140">IID</span><span class="sxs-lookup"><span data-stu-id="abf65-140">IID</span></span><br/>                      | <span data-ttu-id="abf65-141">IID \_ IVMParallelPort est défini en tant que 097beecb-0a02-474F-abd6-298b22293fc6</span><span class="sxs-lookup"><span data-stu-id="abf65-141">IID\_IVMParallelPort is defined as 097beecb-0a02-474f-abd6-298b22293fc6</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="abf65-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="abf65-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abf65-143">**IVMParallelPort**</span><span class="sxs-lookup"><span data-stu-id="abf65-143">**IVMParallelPort**</span></span>](ivmparallelport.md)
</dt> </dl>

 

