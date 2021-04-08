---
title: Propriété ID IVMTask (VPCCOMInterfaces. h)
description: Récupère un identificateur unique pour cette tâche.
ms.assetid: 56a63b94-139b-4445-aef6-1b988e548b4b
keywords:
- Propriété d’ID Virtual PC
- Propriété d’ID Virtual PC, interface IVMTask
- IVMTask interface Virtual PC, propriété ID
topic_type:
- apiref
api_name:
- IVMTask.ID
- IVMTask.get_ID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 821650fcec725a43d86e539bd7f6cc9e7a6e2677
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844145"
---
# <a name="ivmtaskid-property"></a><span data-ttu-id="84737-106">IVMTask :: ID, propriété</span><span class="sxs-lookup"><span data-stu-id="84737-106">IVMTask::ID property</span></span>

<span data-ttu-id="84737-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="84737-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="84737-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="84737-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="84737-109">Récupère un identificateur unique pour cette tâche.</span><span class="sxs-lookup"><span data-stu-id="84737-109">Retrieves a unique identifier for this task.</span></span>

<span data-ttu-id="84737-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="84737-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="84737-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="84737-111">Syntax</span></span>


```C++
HRESULT get_ID(
  [out, retval] long *ID
);
```



## <a name="property-value"></a><span data-ttu-id="84737-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="84737-112">Property value</span></span>

<span data-ttu-id="84737-113">Identificateur unique.</span><span class="sxs-lookup"><span data-stu-id="84737-113">The unique identifier.</span></span>

## <a name="error-codes"></a><span data-ttu-id="84737-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="84737-114">Error codes</span></span>



| <span data-ttu-id="84737-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="84737-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="84737-116">Signification</span><span class="sxs-lookup"><span data-stu-id="84737-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="84737-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="84737-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="84737-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="84737-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="84737-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="84737-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="84737-120">La valeur du paramètre est **null**.</span><span class="sxs-lookup"><span data-stu-id="84737-120">The parameter value is **NULL**.</span></span><br/>  |
| <dl> <span data-ttu-id="84737-121"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="84737-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="84737-122">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="84737-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="84737-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="84737-123">Requirements</span></span>



| <span data-ttu-id="84737-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="84737-124">Requirement</span></span> | <span data-ttu-id="84737-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="84737-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="84737-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84737-126">Minimum supported client</span></span><br/> | <span data-ttu-id="84737-127">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="84737-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="84737-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84737-128">Minimum supported server</span></span><br/> | <span data-ttu-id="84737-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="84737-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="84737-130">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="84737-130">End of client support</span></span><br/>    | <span data-ttu-id="84737-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="84737-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="84737-132">Produit</span><span class="sxs-lookup"><span data-stu-id="84737-132">Product</span></span><br/>                  | <span data-ttu-id="84737-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="84737-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="84737-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="84737-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="84737-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="84737-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="84737-136">IID</span><span class="sxs-lookup"><span data-stu-id="84737-136">IID</span></span><br/>                      | <span data-ttu-id="84737-137">IID \_ IVMTask est défini en tant que ab72b222-6e9c-48ae-aa54-85e3e635767c</span><span class="sxs-lookup"><span data-stu-id="84737-137">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="84737-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="84737-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84737-139">**IVMTask**</span><span class="sxs-lookup"><span data-stu-id="84737-139">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

