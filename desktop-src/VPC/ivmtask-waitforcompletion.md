---
title: Méthode IVMTask WaitForCompletion (VPCCOMInterfaces. h)
description: Attend que la tâche soit terminée ou que l’intervalle de délai d’attente spécifié soit écoulé.
ms.assetid: 28718c54-4411-4c69-89de-35ea6a8d074c
keywords:
- Méthode WaitForCompletion Virtual PC
- Méthode WaitForCompletion Virtual PC, interface IVMTask
- IVMTask interface Virtual PC, méthode WaitForCompletion
topic_type:
- apiref
api_name:
- IVMTask.WaitForCompletion
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 950cc19bad2a0f5804f994fe9279cec649d7c2f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510765"
---
# <a name="ivmtaskwaitforcompletion-method"></a><span data-ttu-id="9c362-106">IVMTask :: WaitForCompletion, méthode</span><span class="sxs-lookup"><span data-stu-id="9c362-106">IVMTask::WaitForCompletion method</span></span>

<span data-ttu-id="9c362-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="9c362-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="9c362-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="9c362-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="9c362-109">Attend que la tâche soit terminée ou que l’intervalle de délai d’attente spécifié soit écoulé.</span><span class="sxs-lookup"><span data-stu-id="9c362-109">Waits for the task to complete or for the specified time-out interval to elapse.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c362-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9c362-110">Syntax</span></span>


```C++
HRESULT WaitForCompletion(
  [in] long timeout
);
```



## <a name="parameters"></a><span data-ttu-id="9c362-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9c362-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c362-112">*délai d’expiration* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9c362-112">*timeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c362-113">Durée, en millisecondes, pendant laquelle cette méthode attendra la fin de l’exécution de la tâche avant de retourner le contrôle à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="9c362-113">The time, in milliseconds, that this method will wait for task completion before returning control to the caller.</span></span> <span data-ttu-id="9c362-114">Une valeur de-1 spécifie que la méthode attendra jusqu’à ce que la tâche se termine sans dépasser le délai d’attente. Les autres valeurs valides de délai d’attente sont comprises entre 0 et 4 millions millisecondes.</span><span class="sxs-lookup"><span data-stu-id="9c362-114">A value of -1 specifies that method will wait until the task completes without timing out. Other valid timeout values range from 0 to 4,000,000 milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c362-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9c362-115">Return value</span></span>

<span data-ttu-id="9c362-116">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="9c362-116">This method can return one of these values.</span></span>



| <span data-ttu-id="9c362-117">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="9c362-117">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="9c362-118">Description</span><span class="sxs-lookup"><span data-stu-id="9c362-118">Description</span></span>                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="9c362-119"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9c362-119"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="9c362-120">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="9c362-120">The operation was successful.</span></span><br/>         |
| <dl> <span data-ttu-id="9c362-121"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="9c362-121"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="9c362-122">Le paramètre de *délai d’attente* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="9c362-122">The *timeout* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="9c362-123"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="9c362-123"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="9c362-124">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="9c362-124">An unexpected error has occurred.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="9c362-125">Notes</span><span class="sxs-lookup"><span data-stu-id="9c362-125">Remarks</span></span>

<span data-ttu-id="9c362-126">La méthode **WaitForCompletion** met le thread d’exécution actuel en veille jusqu’à ce qu’il retourne.</span><span class="sxs-lookup"><span data-stu-id="9c362-126">The **WaitForCompletion** method puts the current execution thread to sleep until it returns.</span></span> <span data-ttu-id="9c362-127">La spécification d’une attente infinie (timeout =-1) n’est pas recommandée, à moins qu’il soit absolument essentiel que la tâche se termine dans n’importe quelle circonstance.</span><span class="sxs-lookup"><span data-stu-id="9c362-127">Specifying an infinite wait (timeout = -1) is not recommended unless it is absolutely critical that the task completes under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c362-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9c362-128">Requirements</span></span>



| <span data-ttu-id="9c362-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9c362-129">Requirement</span></span> | <span data-ttu-id="9c362-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="9c362-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c362-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9c362-131">Minimum supported client</span></span><br/> | <span data-ttu-id="9c362-132">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9c362-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9c362-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9c362-133">Minimum supported server</span></span><br/> | <span data-ttu-id="9c362-134">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="9c362-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="9c362-135">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="9c362-135">End of client support</span></span><br/>    | <span data-ttu-id="9c362-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9c362-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="9c362-137">Produit</span><span class="sxs-lookup"><span data-stu-id="9c362-137">Product</span></span><br/>                  | <span data-ttu-id="9c362-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="9c362-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="9c362-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="9c362-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c362-140"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c362-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="9c362-141">IID</span><span class="sxs-lookup"><span data-stu-id="9c362-141">IID</span></span><br/>                      | <span data-ttu-id="9c362-142">IID \_ IVMTask est défini en tant que ab72b222-6e9c-48ae-aa54-85e3e635767c</span><span class="sxs-lookup"><span data-stu-id="9c362-142">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="9c362-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9c362-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c362-144">**IVMTask**</span><span class="sxs-lookup"><span data-stu-id="9c362-144">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

