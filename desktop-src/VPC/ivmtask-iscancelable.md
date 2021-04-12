---
title: IVMTask IsCancelable, propriété (VPCCOMInterfaces. h)
description: Détermine si la tâche peut être annulée.
ms.assetid: abb8a29a-7f5b-45ba-ae79-d422dfb2f39d
keywords:
- IsCancelable propriété Virtual PC
- IsCancelable, propriété Virtual PC, IVMTask, interface
- IVMTask interface Virtual PC, propriété IsCancelable
topic_type:
- apiref
api_name:
- IVMTask.IsCancelable
- IVMTask.get_IsCancelable
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bcd06db3fc338277d7551233b0d609ceae03f35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105667"
---
# <a name="ivmtaskiscancelable-property"></a><span data-ttu-id="04905-106">IVMTask :: IsCancelable, propriété</span><span class="sxs-lookup"><span data-stu-id="04905-106">IVMTask::IsCancelable property</span></span>

<span data-ttu-id="04905-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="04905-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="04905-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="04905-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="04905-109">Détermine si la tâche peut être annulée.</span><span class="sxs-lookup"><span data-stu-id="04905-109">Determines whether the task can be canceled.</span></span>

<span data-ttu-id="04905-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="04905-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="04905-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="04905-111">Syntax</span></span>


```C++
HRESULT get_IsCancelable(
  [out, retval] VARIANT_BOOL *isCancelable
);
```



## <a name="property-value"></a><span data-ttu-id="04905-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="04905-112">Property value</span></span>

<span data-ttu-id="04905-113">**True** si la tâche peut être annulée avant l’achèvement et **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="04905-113">**TRUE** if the task can be canceled before completion and **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="04905-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="04905-114">Error codes</span></span>



| <span data-ttu-id="04905-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="04905-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="04905-116">Signification</span><span class="sxs-lookup"><span data-stu-id="04905-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="04905-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="04905-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="04905-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="04905-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="04905-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="04905-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="04905-120">La valeur du paramètre est **null**.</span><span class="sxs-lookup"><span data-stu-id="04905-120">The parameter value is **NULL**.</span></span><br/>  |
| <dl> <span data-ttu-id="04905-121"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="04905-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="04905-122">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="04905-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="04905-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="04905-123">Requirements</span></span>



| <span data-ttu-id="04905-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="04905-124">Requirement</span></span> | <span data-ttu-id="04905-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="04905-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="04905-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="04905-126">Minimum supported client</span></span><br/> | <span data-ttu-id="04905-127">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="04905-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="04905-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="04905-128">Minimum supported server</span></span><br/> | <span data-ttu-id="04905-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="04905-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="04905-130">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="04905-130">End of client support</span></span><br/>    | <span data-ttu-id="04905-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="04905-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="04905-132">Produit</span><span class="sxs-lookup"><span data-stu-id="04905-132">Product</span></span><br/>                  | <span data-ttu-id="04905-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="04905-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="04905-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="04905-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="04905-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="04905-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="04905-136">IID</span><span class="sxs-lookup"><span data-stu-id="04905-136">IID</span></span><br/>                      | <span data-ttu-id="04905-137">IID \_ IVMTask est défini en tant que ab72b222-6e9c-48ae-aa54-85e3e635767c</span><span class="sxs-lookup"><span data-stu-id="04905-137">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="04905-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="04905-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04905-139">**IVMTask**</span><span class="sxs-lookup"><span data-stu-id="04905-139">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

