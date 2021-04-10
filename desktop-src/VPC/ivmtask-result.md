---
title: Propriété Result de IVMTask (VPCCOMInterfaces. h)
description: Récupère le résultat de la tâche.
ms.assetid: 640279ef-94b8-4e8f-88f3-a97cec54c121
keywords:
- Propriété de résultat Virtual PC
- Propriété de résultat Virtual PC, interface IVMTask
- IVMTask interface Virtual PC, propriété Result
topic_type:
- apiref
api_name:
- IVMTask.Result
- IVMTask.get_Result
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f4dc36d1529633a850bc10e5c89e8c07147aea8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942505"
---
# <a name="ivmtaskresult-property"></a><span data-ttu-id="e2006-106">IVMTask :: result, propriété</span><span class="sxs-lookup"><span data-stu-id="e2006-106">IVMTask::Result property</span></span>

<span data-ttu-id="e2006-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e2006-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e2006-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e2006-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e2006-109">Récupère le résultat de la tâche.</span><span class="sxs-lookup"><span data-stu-id="e2006-109">Retrieves the result of the task.</span></span>

<span data-ttu-id="e2006-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="e2006-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2006-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e2006-111">Syntax</span></span>


```C++
HRESULT get_Result(
  [out, retval] VMTaskResult *result
);
```



## <a name="property-value"></a><span data-ttu-id="e2006-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="e2006-112">Property value</span></span>

<span data-ttu-id="e2006-113">Résultat de la tâche.</span><span class="sxs-lookup"><span data-stu-id="e2006-113">The result of the task.</span></span> <span data-ttu-id="e2006-114">Pour obtenir la liste des valeurs, consultez [**VMTaskResult**](vmtaskresult.md).</span><span class="sxs-lookup"><span data-stu-id="e2006-114">For a list of values, see [**VMTaskResult**](vmtaskresult.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="e2006-115">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="e2006-115">Error codes</span></span>



| <span data-ttu-id="e2006-116">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="e2006-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="e2006-117">Signification</span><span class="sxs-lookup"><span data-stu-id="e2006-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="e2006-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e2006-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="e2006-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="e2006-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="e2006-120"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="e2006-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="e2006-121">La valeur du paramètre est **null**.</span><span class="sxs-lookup"><span data-stu-id="e2006-121">The parameter value is **NULL**.</span></span><br/>  |
| <dl> <span data-ttu-id="e2006-122"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="e2006-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="e2006-123">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="e2006-123">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="e2006-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e2006-124">Requirements</span></span>



| <span data-ttu-id="e2006-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e2006-125">Requirement</span></span> | <span data-ttu-id="e2006-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="e2006-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2006-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e2006-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e2006-128">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e2006-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e2006-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e2006-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e2006-130">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e2006-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e2006-131">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="e2006-131">End of client support</span></span><br/>    | <span data-ttu-id="e2006-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e2006-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e2006-133">Produit</span><span class="sxs-lookup"><span data-stu-id="e2006-133">Product</span></span><br/>                  | <span data-ttu-id="e2006-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e2006-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e2006-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="e2006-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2006-136"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2006-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e2006-137">IID</span><span class="sxs-lookup"><span data-stu-id="e2006-137">IID</span></span><br/>                      | <span data-ttu-id="e2006-138">IID \_ IVMTask est défini en tant que ab72b222-6e9c-48ae-aa54-85e3e635767c</span><span class="sxs-lookup"><span data-stu-id="e2006-138">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="e2006-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2006-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2006-140">**IVMTask**</span><span class="sxs-lookup"><span data-stu-id="e2006-140">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

