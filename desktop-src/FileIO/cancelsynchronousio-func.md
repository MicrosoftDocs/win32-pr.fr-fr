---
description: Marque les opérations d’e/s synchrones en attente qui sont émises par le thread spécifié comme annulées.
ms.assetid: f362c8b2-2193-443e-bb69-78f8b4147117
title: CancelSynchronousIo, fonction (IoAPI. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CancelSynchronousIo
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-1.dll
- KernelBase.dll
- MinKernelBase.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: 3e0c1596603ef7c0d13362c2608cc59b88d366fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530004"
---
# <a name="cancelsynchronousio-function"></a><span data-ttu-id="6f641-103">CancelSynchronousIo fonction)</span><span class="sxs-lookup"><span data-stu-id="6f641-103">CancelSynchronousIo function</span></span>

<span data-ttu-id="6f641-104">Marque les opérations d’e/s synchrones en attente qui sont émises par le thread spécifié comme annulées.</span><span class="sxs-lookup"><span data-stu-id="6f641-104">Marks pending synchronous I/O operations that are issued by the specified thread as canceled.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f641-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6f641-105">Syntax</span></span>


```C++
BOOL WINAPI CancelSynchronousIo(
  _In_ HANDLE hThread
);
```



## <a name="parameters"></a><span data-ttu-id="6f641-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6f641-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f641-107">*hThread* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6f641-107">*hThread* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f641-108">Handle du thread.</span><span class="sxs-lookup"><span data-stu-id="6f641-108">A handle to the thread.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f641-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6f641-109">Return value</span></span>

<span data-ttu-id="6f641-110">Si la fonction réussit, la valeur de retour est différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="6f641-110">If the function succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="6f641-111">Si la fonction échoue, la valeur de retour est 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="6f641-111">If the function fails, the return value is 0 (zero).</span></span> <span data-ttu-id="6f641-112">Pour afficher les informations d’erreur étendues, appelez la fonction [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="6f641-112">To get extended error information, call the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

<span data-ttu-id="6f641-113">Si cette fonction ne peut pas trouver de demande d’annulation, la valeur de retour est 0 (zéro), et [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne l' **erreur \_ \_ introuvable**.</span><span class="sxs-lookup"><span data-stu-id="6f641-113">If this function cannot find a request to cancel, the return value is 0 (zero), and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns **ERROR\_NOT\_FOUND**.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f641-114">Notes</span><span class="sxs-lookup"><span data-stu-id="6f641-114">Remarks</span></span>

<span data-ttu-id="6f641-115">L’appelant doit disposer du droit d’accès de [ \_ terminaison du thread](/windows/desktop/ProcThread/thread-security-and-access-rights) .</span><span class="sxs-lookup"><span data-stu-id="6f641-115">The caller must have the [THREAD\_TERMINATE](/windows/desktop/ProcThread/thread-security-and-access-rights) access right.</span></span>

<span data-ttu-id="6f641-116">Si des opérations d’e/s en attente sont en cours pour le thread spécifié, la fonction **CancelSynchronousIo** les marque pour l’annulation.</span><span class="sxs-lookup"><span data-stu-id="6f641-116">If there are any pending I/O operations in progress for the specified thread, the **CancelSynchronousIo** function marks them for cancellation.</span></span> <span data-ttu-id="6f641-117">La plupart des types d’opérations peuvent être annulés immédiatement ; d’autres opérations peuvent continuer à se terminer avant qu’elles ne soient réellement annulées et que l’appelant soit notifié.</span><span class="sxs-lookup"><span data-stu-id="6f641-117">Most types of operations can be canceled immediately; other operations can continue toward completion before they are actually canceled and the caller is notified.</span></span> <span data-ttu-id="6f641-118">La fonction **CancelSynchronousIo** n’attend pas que toutes les opérations annulées soient terminées.</span><span class="sxs-lookup"><span data-stu-id="6f641-118">The **CancelSynchronousIo** function does not wait for all canceled operations to complete.</span></span> <span data-ttu-id="6f641-119">Pour plus d’informations, consultez [instructions d’achèvement/annulation d’e/s](https://www.microsoft.com/whdc/driver/kernel/iocancel.mspx).</span><span class="sxs-lookup"><span data-stu-id="6f641-119">For more information, see [I/O Completion/Cancellation Guidelines](https://www.microsoft.com/whdc/driver/kernel/iocancel.mspx).</span></span>

<span data-ttu-id="6f641-120">L’opération qui est annulée se termine avec l’un des trois États suivants : vous devez vérifier l’état d’achèvement pour déterminer l’état d’achèvement.</span><span class="sxs-lookup"><span data-stu-id="6f641-120">The operation being canceled is completed with one of three statuses; you must check the completion status to determine the completion state.</span></span> <span data-ttu-id="6f641-121">Les trois États sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="6f641-121">The three statuses are:</span></span>

-   <span data-ttu-id="6f641-122">**L’opération s’est terminée normalement.**</span><span class="sxs-lookup"><span data-stu-id="6f641-122">**The operation completed normally.**</span></span> <span data-ttu-id="6f641-123">Cela peut se produire même si l’opération a été annulée, car la demande d’annulation n’a peut-être pas été envoyée dans le temps pour annuler l’opération.</span><span class="sxs-lookup"><span data-stu-id="6f641-123">This can occur even if the operation was canceled, because the cancel request might not have been submitted in time to cancel the operation.</span></span>
-   <span data-ttu-id="6f641-124">**L'opération a été annulée.**</span><span class="sxs-lookup"><span data-stu-id="6f641-124">**The operation was canceled.**</span></span> <span data-ttu-id="6f641-125">La fonction [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne une erreur indiquant que l’opération a été **\_ \_ abandonnée**.</span><span class="sxs-lookup"><span data-stu-id="6f641-125">The [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns **ERROR\_OPERATION\_ABORTED**.</span></span>
-   <span data-ttu-id="6f641-126">**L’opération a échoué avec une autre erreur.**</span><span class="sxs-lookup"><span data-stu-id="6f641-126">**The operation failed with another error.**</span></span> <span data-ttu-id="6f641-127">La fonction [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne le code d’erreur approprié.</span><span class="sxs-lookup"><span data-stu-id="6f641-127">The [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns the relevant error code.</span></span>

<span data-ttu-id="6f641-128">Dans Windows 8 et Windows Server 2012, cette fonction est prise en charge par les technologies suivantes.</span><span class="sxs-lookup"><span data-stu-id="6f641-128">In Windows 8 and Windows Server 2012, this function is supported by the following technologies.</span></span>



| <span data-ttu-id="6f641-129">Technology</span><span class="sxs-lookup"><span data-stu-id="6f641-129">Technology</span></span>                                           | <span data-ttu-id="6f641-130">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="6f641-130">Supported</span></span>      |
|------------------------------------------------------|----------------|
| <span data-ttu-id="6f641-131">Protocole SMB (Server Message Block) 3,0</span><span class="sxs-lookup"><span data-stu-id="6f641-131">Server Message Block (SMB) 3.0 protocol</span></span><br/>   | <span data-ttu-id="6f641-132">Oui</span><span class="sxs-lookup"><span data-stu-id="6f641-132">Yes</span></span><br/> |
| <span data-ttu-id="6f641-133">Basculement transparent SMB 3,0 (TFO)</span><span class="sxs-lookup"><span data-stu-id="6f641-133">SMB 3.0 Transparent Failover (TFO)</span></span><br/>        | <span data-ttu-id="6f641-134">Oui</span><span class="sxs-lookup"><span data-stu-id="6f641-134">Yes</span></span><br/> |
| <span data-ttu-id="6f641-135">SMB 3,0 avec des partages de fichiers avec montée en puissance parallèle (SO)</span><span class="sxs-lookup"><span data-stu-id="6f641-135">SMB 3.0 with Scale-out File Shares (SO)</span></span><br/>   | <span data-ttu-id="6f641-136">Oui</span><span class="sxs-lookup"><span data-stu-id="6f641-136">Yes</span></span><br/> |
| <span data-ttu-id="6f641-137">Système de fichiers Volume partagé de cluster (CsvFS)</span><span class="sxs-lookup"><span data-stu-id="6f641-137">Cluster Shared Volume File System (CsvFS)</span></span><br/> | <span data-ttu-id="6f641-138">Oui</span><span class="sxs-lookup"><span data-stu-id="6f641-138">Yes</span></span><br/> |
| <span data-ttu-id="6f641-139">Système de fichiers résilient (ReFS)</span><span class="sxs-lookup"><span data-stu-id="6f641-139">Resilient File System (ReFS)</span></span><br/>              | <span data-ttu-id="6f641-140">Oui</span><span class="sxs-lookup"><span data-stu-id="6f641-140">Yes</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6f641-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6f641-141">Requirements</span></span>



| <span data-ttu-id="6f641-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6f641-142">Requirement</span></span> | <span data-ttu-id="6f641-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="6f641-143">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f641-144">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6f641-144">Minimum supported client</span></span><br/> | <span data-ttu-id="6f641-145">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6f641-145">Windows Vista \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                          |
| <span data-ttu-id="6f641-146">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6f641-146">Minimum supported server</span></span><br/> | <span data-ttu-id="6f641-147">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6f641-147">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                    |
| <span data-ttu-id="6f641-148">En-tête</span><span class="sxs-lookup"><span data-stu-id="6f641-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f641-149"><dt>IoAPI. h (inclure Windows. h); </dt> <dt>WinBase. h sur Windows server 2008 R2, Windows 7, Windows server 2008 et Windows Vista (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6f641-149"><dt>IoAPI.h (include Windows.h); </dt> <dt>WinBase.h on Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="6f641-150">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6f641-150">Library</span></span><br/>                  | <dl> <span data-ttu-id="6f641-151"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="6f641-151"><dt>Kernel32.lib</dt></span></span> </dl>                                                                                                                                                                                 |
| <span data-ttu-id="6f641-152">DLL</span><span class="sxs-lookup"><span data-stu-id="6f641-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f641-153"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f641-153"><dt>Kernel32.dll</dt></span></span> </dl>                                                                                                                                                                                 |



## <a name="see-also"></a><span data-ttu-id="6f641-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6f641-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f641-155">**CancelIo**</span><span class="sxs-lookup"><span data-stu-id="6f641-155">**CancelIo**</span></span>](cancelio.md)
</dt> <dt>

[<span data-ttu-id="6f641-156">**CancelIoEx**</span><span class="sxs-lookup"><span data-stu-id="6f641-156">**CancelIoEx**</span></span>](cancelioex-func.md)
</dt> <dt>

[<span data-ttu-id="6f641-157">Fonctions de gestion de fichiers</span><span class="sxs-lookup"><span data-stu-id="6f641-157">File Management Functions</span></span>](file-management-functions.md)
</dt> <dt>

[<span data-ttu-id="6f641-158">E/s synchrones et asynchrones</span><span class="sxs-lookup"><span data-stu-id="6f641-158">Synchronous and Asynchronous I/O</span></span>](synchronous-and-asynchronous-i-o.md)
</dt> </dl>

 

