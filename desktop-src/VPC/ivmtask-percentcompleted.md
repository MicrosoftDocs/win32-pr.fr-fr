---
title: IVMTask PercentCompleted, propriété (VPCCOMInterfaces. h)
description: Récupère le pourcentage d’achèvement de la tâche.
ms.assetid: 23ba9696-06ed-44ec-a1ec-ef3bf9122c6f
keywords:
- PercentCompleted propriété Virtual PC
- PercentCompleted, propriété Virtual PC, IVMTask, interface
- IVMTask interface Virtual PC, propriété PercentCompleted
topic_type:
- apiref
api_name:
- IVMTask.PercentCompleted
- IVMTask.get_PercentCompleted
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa820adbbde2fc68632da27a9b146bd0e8f40143
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743093"
---
# <a name="ivmtaskpercentcompleted-property"></a><span data-ttu-id="584ff-106">IVMTask ::P propriété ercentCompleted</span><span class="sxs-lookup"><span data-stu-id="584ff-106">IVMTask::PercentCompleted property</span></span>

<span data-ttu-id="584ff-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="584ff-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="584ff-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="584ff-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="584ff-109">Récupère le pourcentage d’achèvement de la tâche.</span><span class="sxs-lookup"><span data-stu-id="584ff-109">Retrieves the completion percentage of the task.</span></span>

<span data-ttu-id="584ff-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="584ff-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="584ff-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="584ff-111">Syntax</span></span>


```C++
HRESULT get_PercentCompleted(
  [out, retval] long *percentCompleted
);
```



## <a name="property-value"></a><span data-ttu-id="584ff-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="584ff-112">Property value</span></span>

<span data-ttu-id="584ff-113">Pourcentage d’achèvement actuel.</span><span class="sxs-lookup"><span data-stu-id="584ff-113">The current completion percentage.</span></span> <span data-ttu-id="584ff-114">La valeur est un nombre compris entre 0 et 100.</span><span class="sxs-lookup"><span data-stu-id="584ff-114">The value is a number between 0 and 100.</span></span>

## <a name="error-codes"></a><span data-ttu-id="584ff-115">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="584ff-115">Error codes</span></span>



| <span data-ttu-id="584ff-116">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="584ff-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="584ff-117">Signification</span><span class="sxs-lookup"><span data-stu-id="584ff-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="584ff-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="584ff-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="584ff-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="584ff-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="584ff-120"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="584ff-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="584ff-121">La valeur du paramètre est **null**.</span><span class="sxs-lookup"><span data-stu-id="584ff-121">The parameter value is **NULL**.</span></span><br/>  |
| <dl> <span data-ttu-id="584ff-122"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="584ff-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="584ff-123">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="584ff-123">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="584ff-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="584ff-124">Requirements</span></span>



| <span data-ttu-id="584ff-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="584ff-125">Requirement</span></span> | <span data-ttu-id="584ff-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="584ff-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="584ff-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="584ff-127">Minimum supported client</span></span><br/> | <span data-ttu-id="584ff-128">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="584ff-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="584ff-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="584ff-129">Minimum supported server</span></span><br/> | <span data-ttu-id="584ff-130">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="584ff-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="584ff-131">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="584ff-131">End of client support</span></span><br/>    | <span data-ttu-id="584ff-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="584ff-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="584ff-133">Produit</span><span class="sxs-lookup"><span data-stu-id="584ff-133">Product</span></span><br/>                  | <span data-ttu-id="584ff-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="584ff-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="584ff-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="584ff-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="584ff-136"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="584ff-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="584ff-137">IID</span><span class="sxs-lookup"><span data-stu-id="584ff-137">IID</span></span><br/>                      | <span data-ttu-id="584ff-138">IID \_ IVMTask est défini en tant que ab72b222-6e9c-48ae-aa54-85e3e635767c</span><span class="sxs-lookup"><span data-stu-id="584ff-138">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="584ff-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="584ff-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="584ff-140">**IVMTask**</span><span class="sxs-lookup"><span data-stu-id="584ff-140">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

