---
title: Propriété Description de IVMTask (VPCCOMInterfaces. h)
description: Récupère une description de la tâche.
ms.assetid: f1d5c7a2-b29e-4a8d-9cbd-263c168ec658
keywords:
- Propriété Description Virtual PC
- Propriété de description Virtual PC, interface IVMTask
- IVMTask interface Virtual PC, propriété Description
topic_type:
- apiref
api_name:
- IVMTask.Description
- IVMTask.get_Description
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62123174a61aa9b1c58ec36be69774e10e75de59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106536298"
---
# <a name="ivmtaskdescription-property"></a><span data-ttu-id="9cc98-106">IVMTask ::D propriété escription</span><span class="sxs-lookup"><span data-stu-id="9cc98-106">IVMTask::Description property</span></span>

<span data-ttu-id="9cc98-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="9cc98-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="9cc98-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="9cc98-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="9cc98-109">Récupère une description de la tâche.</span><span class="sxs-lookup"><span data-stu-id="9cc98-109">Retrieves a description of the task.</span></span>

<span data-ttu-id="9cc98-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="9cc98-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cc98-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9cc98-111">Syntax</span></span>


```C++
HRESULT get_Description(
  [out, retval] BSTR *description
);
```



## <a name="property-value"></a><span data-ttu-id="9cc98-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="9cc98-112">Property value</span></span>

<span data-ttu-id="9cc98-113">Description de la tâche, telle que définie par Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="9cc98-113">The description of the task, as set by Virtual PC.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9cc98-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="9cc98-114">Error codes</span></span>



| <span data-ttu-id="9cc98-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="9cc98-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="9cc98-116">Signification</span><span class="sxs-lookup"><span data-stu-id="9cc98-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="9cc98-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9cc98-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="9cc98-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="9cc98-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="9cc98-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="9cc98-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="9cc98-120">La valeur du paramètre est **null**.</span><span class="sxs-lookup"><span data-stu-id="9cc98-120">The parameter value is **NULL**.</span></span><br/>  |
| <dl> <span data-ttu-id="9cc98-121"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="9cc98-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="9cc98-122">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="9cc98-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="9cc98-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9cc98-123">Requirements</span></span>



| <span data-ttu-id="9cc98-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9cc98-124">Requirement</span></span> | <span data-ttu-id="9cc98-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="9cc98-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9cc98-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9cc98-126">Minimum supported client</span></span><br/> | <span data-ttu-id="9cc98-127">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9cc98-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9cc98-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9cc98-128">Minimum supported server</span></span><br/> | <span data-ttu-id="9cc98-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="9cc98-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="9cc98-130">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="9cc98-130">End of client support</span></span><br/>    | <span data-ttu-id="9cc98-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9cc98-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="9cc98-132">Produit</span><span class="sxs-lookup"><span data-stu-id="9cc98-132">Product</span></span><br/>                  | <span data-ttu-id="9cc98-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="9cc98-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="9cc98-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="9cc98-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="9cc98-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="9cc98-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="9cc98-136">IID</span><span class="sxs-lookup"><span data-stu-id="9cc98-136">IID</span></span><br/>                      | <span data-ttu-id="9cc98-137">IID \_ IVMTask est défini en tant que ab72b222-6e9c-48ae-aa54-85e3e635767c</span><span class="sxs-lookup"><span data-stu-id="9cc98-137">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="9cc98-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9cc98-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cc98-139">**IVMTask**</span><span class="sxs-lookup"><span data-stu-id="9cc98-139">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

