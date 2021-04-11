---
title: IVMTask méthode Cancel (VPCCOMInterfaces. h)
description: Annule la tâche.
ms.assetid: 29107942-334c-452a-b787-6e0cb7380f90
keywords:
- Annuler la méthode Virtual PC
- Méthode Cancel Virtual PC, interface IVMTask
- IVMTask interface Virtual PC, méthode Cancel
topic_type:
- apiref
api_name:
- IVMTask.Cancel
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 931b7229f3c81166f4610e873c23eca979c8897b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317470"
---
# <a name="ivmtaskcancel-method"></a><span data-ttu-id="8b561-106">IVMTask :: Cancel, méthode</span><span class="sxs-lookup"><span data-stu-id="8b561-106">IVMTask::Cancel method</span></span>

<span data-ttu-id="8b561-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8b561-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8b561-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="8b561-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8b561-109">Annule la tâche.</span><span class="sxs-lookup"><span data-stu-id="8b561-109">Cancels the task.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b561-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8b561-110">Syntax</span></span>


```C++
HRESULT Cancel();
```



## <a name="parameters"></a><span data-ttu-id="8b561-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8b561-111">Parameters</span></span>

<span data-ttu-id="8b561-112">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="8b561-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8b561-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8b561-113">Return value</span></span>

<span data-ttu-id="8b561-114">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="8b561-114">This method can return one of these values.</span></span>



| <span data-ttu-id="8b561-115">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="8b561-115">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="8b561-116">Description</span><span class="sxs-lookup"><span data-stu-id="8b561-116">Description</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="8b561-117"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8b561-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="8b561-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="8b561-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="8b561-119"><dt>**E \_ ÉCHEC**</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="8b561-119"><dt>**E\_FAIL**</dt> <dt>0x80004005</dt></span></span> </dl>            | <span data-ttu-id="8b561-120">La tâche ne peut pas être annulée.</span><span class="sxs-lookup"><span data-stu-id="8b561-120">The task cannot be canceled.</span></span><br/>      |
| <dl> <span data-ttu-id="8b561-121"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="8b561-121"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="8b561-122">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="8b561-122">An unexpected error has occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8b561-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8b561-123">Requirements</span></span>



| <span data-ttu-id="8b561-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8b561-124">Requirement</span></span> | <span data-ttu-id="8b561-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="8b561-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b561-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8b561-126">Minimum supported client</span></span><br/> | <span data-ttu-id="8b561-127">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8b561-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8b561-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8b561-128">Minimum supported server</span></span><br/> | <span data-ttu-id="8b561-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="8b561-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="8b561-130">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="8b561-130">End of client support</span></span><br/>    | <span data-ttu-id="8b561-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8b561-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8b561-132">Produit</span><span class="sxs-lookup"><span data-stu-id="8b561-132">Product</span></span><br/>                  | <span data-ttu-id="8b561-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8b561-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="8b561-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="8b561-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b561-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b561-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="8b561-136">IID</span><span class="sxs-lookup"><span data-stu-id="8b561-136">IID</span></span><br/>                      | <span data-ttu-id="8b561-137">IID \_ IVMTask est défini en tant que ab72b222-6e9c-48ae-aa54-85e3e635767c</span><span class="sxs-lookup"><span data-stu-id="8b561-137">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="8b561-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b561-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b561-139">**IVMTask**</span><span class="sxs-lookup"><span data-stu-id="8b561-139">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

