---
description: Marque toutes les opérations d’e/s en attente pour le handle de fichier spécifié. La fonction annule uniquement les opérations d’e/s dans le processus actuel, quel que soit le thread qui a créé l’opération d’e/s.
ms.assetid: a2ce13b8-7da6-4848-848d-901d9667c2e3
title: CancelIoEx, fonction (IoAPI. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CancelIoEx
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-0.dll
- KernelBase.dll
- MinKernelBase.dll
- API-MS-Win-Core-io-l1-1-1.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: 3de44762ad9a230a9d8cc410c4ba3ae7c2d9964e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524181"
---
# <a name="cancelioex-function"></a><span data-ttu-id="972aa-104">CancelIoEx fonction)</span><span class="sxs-lookup"><span data-stu-id="972aa-104">CancelIoEx function</span></span>

<span data-ttu-id="972aa-105">Marque toutes les opérations d’e/s en attente pour le handle de fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="972aa-105">Marks any outstanding I/O operations for the specified file handle.</span></span> <span data-ttu-id="972aa-106">La fonction annule uniquement les opérations d’e/s dans le processus actuel, quel que soit le thread qui a créé l’opération d’e/s.</span><span class="sxs-lookup"><span data-stu-id="972aa-106">The function only cancels I/O operations in the current process, regardless of which thread created the I/O operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="972aa-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="972aa-107">Syntax</span></span>


```C++
BOOL WINAPI CancelIoEx(
  _In_     HANDLE       hFile,
  _In_opt_ LPOVERLAPPED lpOverlapped
);
```



## <a name="parameters"></a><span data-ttu-id="972aa-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="972aa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="972aa-109">*hFile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="972aa-109">*hFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="972aa-110">Handle du fichier.</span><span class="sxs-lookup"><span data-stu-id="972aa-110">A handle to the file.</span></span>

</dd> <dt>

<span data-ttu-id="972aa-111">*lpOverlapped* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="972aa-111">*lpOverlapped* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="972aa-112">Pointeur vers une structure de données avec [**chevauchement**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) qui contient les données utilisées pour les e/s asynchrones.</span><span class="sxs-lookup"><span data-stu-id="972aa-112">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) data structure that contains the data used for asynchronous I/O.</span></span>

<span data-ttu-id="972aa-113">Si ce paramètre a la **valeur null**, toutes les demandes d’e/s pour le paramètre *hFile* sont annulées.</span><span class="sxs-lookup"><span data-stu-id="972aa-113">If this parameter is **NULL**, all I/O requests for the *hFile* parameter are canceled.</span></span>

<span data-ttu-id="972aa-114">Si ce paramètre n’est pas **null**, seules les demandes d’e/s spécifiques qui ont été émises pour le fichier avec la structure OVERLAPPED *lpOverlapped* spécifiée sont marquées comme annulées, ce qui signifie que vous pouvez annuler une ou plusieurs requêtes, tandis que la fonction [**CancelIo**](cancelio.md) annule toutes les demandes en suspens sur un descripteur de fichier.</span><span class="sxs-lookup"><span data-stu-id="972aa-114">If this parameter is not **NULL**, only those specific I/O requests that were issued for the file with the specified *lpOverlapped* overlapped structure are marked as canceled, meaning that you can cancel one or more requests, while the [**CancelIo**](cancelio.md) function cancels all outstanding requests on a file handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="972aa-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="972aa-115">Return value</span></span>

<span data-ttu-id="972aa-116">Si la fonction réussit, la valeur de retour est différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="972aa-116">If the function succeeds, the return value is nonzero.</span></span> <span data-ttu-id="972aa-117">L’opération d’annulation pour toutes les opérations d’e/s en attente émises par le processus appelant pour le handle de fichier spécifié a été correctement demandée.</span><span class="sxs-lookup"><span data-stu-id="972aa-117">The cancel operation for all pending I/O operations issued by the calling process for the specified file handle was successfully requested.</span></span> <span data-ttu-id="972aa-118">L’application ne doit pas libérer ou réutiliser la structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) associée aux opérations d’e/s annulées tant qu’elles n’ont pas été terminées.</span><span class="sxs-lookup"><span data-stu-id="972aa-118">The application must not free or reuse the [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure associated with the canceled I/O operations until they have completed.</span></span> <span data-ttu-id="972aa-119">Le thread peut utiliser la fonction [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) pour déterminer à quel moment les opérations d’e/s ont elles-mêmes été effectuées.</span><span class="sxs-lookup"><span data-stu-id="972aa-119">The thread can use the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function to determine when the I/O operations themselves have been completed.</span></span>

<span data-ttu-id="972aa-120">Si la fonction échoue, la valeur de retour est 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="972aa-120">If the function fails, the return value is 0 (zero).</span></span> <span data-ttu-id="972aa-121">Pour afficher les informations d’erreur étendues, appelez la fonction [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="972aa-121">To get extended error information, call the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

<span data-ttu-id="972aa-122">Si cette fonction ne peut pas trouver de demande d’annulation, la valeur de retour est 0 (zéro), et [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne l' **erreur \_ \_ introuvable**.</span><span class="sxs-lookup"><span data-stu-id="972aa-122">If this function cannot find a request to cancel, the return value is 0 (zero), and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns **ERROR\_NOT\_FOUND**.</span></span>

## <a name="remarks"></a><span data-ttu-id="972aa-123">Notes</span><span class="sxs-lookup"><span data-stu-id="972aa-123">Remarks</span></span>

<span data-ttu-id="972aa-124">La fonction **CancelIoEx** vous permet d’annuler des requêtes dans des threads autres que le thread appelant.</span><span class="sxs-lookup"><span data-stu-id="972aa-124">The **CancelIoEx** function allows you to cancel requests in threads other than the calling thread.</span></span> <span data-ttu-id="972aa-125">La fonction [**CancelIo**](cancelio.md) annule uniquement les demandes dans le thread qui a appelé la fonction **CancelIo** .</span><span class="sxs-lookup"><span data-stu-id="972aa-125">The [**CancelIo**](cancelio.md) function only cancels requests in the same thread that called the **CancelIo** function.</span></span> <span data-ttu-id="972aa-126">**CancelIoEx** annule uniquement les e/s en suspens sur le handle, mais ne modifie pas l’état du descripteur. Cela signifie que vous ne pouvez pas compter sur l’état du handle, car vous ne pouvez pas savoir si l’opération a été effectuée avec succès ou a été annulée.</span><span class="sxs-lookup"><span data-stu-id="972aa-126">**CancelIoEx** cancels only outstanding I/O on the handle, it does not change the state of the handle; this means that you cannot rely on the state of the handle because you cannot know whether the operation was completed successfully or canceled.</span></span>

<span data-ttu-id="972aa-127">Si des opérations d’e/s en attente sont en cours pour le handle de fichier spécifié, la fonction **CancelIoEx** les marque pour l’annulation.</span><span class="sxs-lookup"><span data-stu-id="972aa-127">If there are any pending I/O operations in progress for the specified file handle, the **CancelIoEx** function marks them for cancellation.</span></span> <span data-ttu-id="972aa-128">La plupart des types d’opérations peuvent être annulés immédiatement ; d’autres opérations peuvent continuer à se terminer avant qu’elles ne soient réellement annulées et que l’appelant soit notifié.</span><span class="sxs-lookup"><span data-stu-id="972aa-128">Most types of operations can be canceled immediately; other operations can continue toward completion before they are actually canceled and the caller is notified.</span></span> <span data-ttu-id="972aa-129">La fonction **CancelIoEx** n’attend pas que toutes les opérations annulées soient terminées.</span><span class="sxs-lookup"><span data-stu-id="972aa-129">The **CancelIoEx** function does not wait for all canceled operations to complete.</span></span>

<span data-ttu-id="972aa-130">Si le descripteur de fichier est associé à un port de terminaison, un paquet de terminaison d’e/s n’est pas mis en file d’attente vers le port si une opération synchrone est correctement annulée.</span><span class="sxs-lookup"><span data-stu-id="972aa-130">If the file handle is associated with a completion port, an I/O completion packet is not queued to the port if a synchronous operation is successfully canceled.</span></span> <span data-ttu-id="972aa-131">Pour les opérations asynchrones toujours en attente, l’opération d’annulation met en file d’attente un paquet de terminaison d’e/s.</span><span class="sxs-lookup"><span data-stu-id="972aa-131">For asynchronous operations still pending, the cancel operation will queue an I/O completion packet.</span></span>

<span data-ttu-id="972aa-132">L’opération qui est annulée se termine avec l’un des trois États suivants : vous devez vérifier l’état d’achèvement pour déterminer l’état d’achèvement.</span><span class="sxs-lookup"><span data-stu-id="972aa-132">The operation being canceled is completed with one of three statuses; you must check the completion status to determine the completion state.</span></span> <span data-ttu-id="972aa-133">Les trois États sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="972aa-133">The three statuses are:</span></span>

-   <span data-ttu-id="972aa-134">L’opération s’est terminée normalement.</span><span class="sxs-lookup"><span data-stu-id="972aa-134">The operation completed normally.</span></span> <span data-ttu-id="972aa-135">Cela peut se produire même si l’opération a été annulée, car la demande d’annulation n’a peut-être pas été envoyée dans le temps pour annuler l’opération.</span><span class="sxs-lookup"><span data-stu-id="972aa-135">This can occur even if the operation was canceled, because the cancel request might not have been submitted in time to cancel the operation.</span></span>
-   <span data-ttu-id="972aa-136">L'opération a été annulée.</span><span class="sxs-lookup"><span data-stu-id="972aa-136">The operation was canceled.</span></span> <span data-ttu-id="972aa-137">La fonction [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne une erreur indiquant que l’opération a été **\_ \_ abandonnée**.</span><span class="sxs-lookup"><span data-stu-id="972aa-137">The [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns **ERROR\_OPERATION\_ABORTED**.</span></span>
-   <span data-ttu-id="972aa-138">L’opération a échoué avec une autre erreur.</span><span class="sxs-lookup"><span data-stu-id="972aa-138">The operation failed with another error.</span></span> <span data-ttu-id="972aa-139">La fonction [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne le code d’erreur approprié.</span><span class="sxs-lookup"><span data-stu-id="972aa-139">The [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns the relevant error code.</span></span>

<span data-ttu-id="972aa-140">Dans Windows 8 et Windows Server 2012, cette fonction est prise en charge par les technologies suivantes.</span><span class="sxs-lookup"><span data-stu-id="972aa-140">In Windows 8 and Windows Server 2012, this function is supported by the following technologies.</span></span>



| <span data-ttu-id="972aa-141">Technology</span><span class="sxs-lookup"><span data-stu-id="972aa-141">Technology</span></span>                                           | <span data-ttu-id="972aa-142">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="972aa-142">Supported</span></span>      |
|------------------------------------------------------|----------------|
| <span data-ttu-id="972aa-143">Protocole SMB (Server Message Block) 3,0</span><span class="sxs-lookup"><span data-stu-id="972aa-143">Server Message Block (SMB) 3.0 protocol</span></span><br/>   | <span data-ttu-id="972aa-144">Oui</span><span class="sxs-lookup"><span data-stu-id="972aa-144">Yes</span></span><br/> |
| <span data-ttu-id="972aa-145">Basculement transparent SMB 3,0 (TFO)</span><span class="sxs-lookup"><span data-stu-id="972aa-145">SMB 3.0 Transparent Failover (TFO)</span></span><br/>        | <span data-ttu-id="972aa-146">Oui</span><span class="sxs-lookup"><span data-stu-id="972aa-146">Yes</span></span><br/> |
| <span data-ttu-id="972aa-147">SMB 3,0 avec des partages de fichiers avec montée en puissance parallèle (SO)</span><span class="sxs-lookup"><span data-stu-id="972aa-147">SMB 3.0 with Scale-out File Shares (SO)</span></span><br/>   | <span data-ttu-id="972aa-148">Oui</span><span class="sxs-lookup"><span data-stu-id="972aa-148">Yes</span></span><br/> |
| <span data-ttu-id="972aa-149">Système de fichiers Volume partagé de cluster (CsvFS)</span><span class="sxs-lookup"><span data-stu-id="972aa-149">Cluster Shared Volume File System (CsvFS)</span></span><br/> | <span data-ttu-id="972aa-150">Oui</span><span class="sxs-lookup"><span data-stu-id="972aa-150">Yes</span></span><br/> |
| <span data-ttu-id="972aa-151">Système de fichiers résilient (ReFS)</span><span class="sxs-lookup"><span data-stu-id="972aa-151">Resilient File System (ReFS)</span></span><br/>              | <span data-ttu-id="972aa-152">Oui</span><span class="sxs-lookup"><span data-stu-id="972aa-152">Yes</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="972aa-153">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="972aa-153">Requirements</span></span>



| <span data-ttu-id="972aa-154">Condition requise</span><span class="sxs-lookup"><span data-stu-id="972aa-154">Requirement</span></span> | <span data-ttu-id="972aa-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="972aa-155">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="972aa-156">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="972aa-156">Minimum supported client</span></span><br/> | <span data-ttu-id="972aa-157">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="972aa-157">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                                   |
| <span data-ttu-id="972aa-158">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="972aa-158">Minimum supported server</span></span><br/> | <span data-ttu-id="972aa-159">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="972aa-159">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                             |
| <span data-ttu-id="972aa-160">En-tête</span><span class="sxs-lookup"><span data-stu-id="972aa-160">Header</span></span><br/>                   | <dl> <span data-ttu-id="972aa-161"><dt>IoAPI. h (inclure Windows. h); </dt> <dt>WinBase. h sur Windows server 2008 R2, Windows 7, Windows server 2008 et Windows Vista (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="972aa-161"><dt>IoAPI.h (include Windows.h); </dt> <dt>WinBase.h on Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="972aa-162">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="972aa-162">Library</span></span><br/>                  | <dl> <span data-ttu-id="972aa-163"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="972aa-163"><dt>Kernel32.lib</dt></span></span> </dl>                                                                                                                                                                                 |
| <span data-ttu-id="972aa-164">DLL</span><span class="sxs-lookup"><span data-stu-id="972aa-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="972aa-165"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="972aa-165"><dt>Kernel32.dll</dt></span></span> </dl>                                                                                                                                                                                 |



## <a name="see-also"></a><span data-ttu-id="972aa-166">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="972aa-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="972aa-167">**CancelIo**</span><span class="sxs-lookup"><span data-stu-id="972aa-167">**CancelIo**</span></span>](cancelio.md)
</dt> <dt>

[<span data-ttu-id="972aa-168">**CancelSynchronousIo**</span><span class="sxs-lookup"><span data-stu-id="972aa-168">**CancelSynchronousIo**</span></span>](cancelsynchronousio-func.md)
</dt> <dt>

[<span data-ttu-id="972aa-169">Annulation d’opérations d’e/s en attente</span><span class="sxs-lookup"><span data-stu-id="972aa-169">Canceling Pending I/O Operations</span></span>](canceling-pending-i-o-operations.md)
</dt> <dt>

[<span data-ttu-id="972aa-170">Fonctions de gestion de fichiers</span><span class="sxs-lookup"><span data-stu-id="972aa-170">File Management Functions</span></span>](file-management-functions.md)
</dt> <dt>

[<span data-ttu-id="972aa-171">E/s synchrones et asynchrones</span><span class="sxs-lookup"><span data-stu-id="972aa-171">Synchronous and Asynchronous I/O</span></span>](synchronous-and-asynchronous-i-o.md)
</dt> </dl>

 

