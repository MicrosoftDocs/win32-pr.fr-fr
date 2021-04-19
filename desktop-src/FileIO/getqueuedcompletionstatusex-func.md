---
description: Récupère simultanément plusieurs entrées de port de terminaison.
ms.assetid: 3996c02c-562c-4697-a091-e241ad54b239
title: GetQueuedCompletionStatusEx, fonction (IoAPI. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetQueuedCompletionStatusEx
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-0.dll
- KernelBase.dll
- MinKernelBase.dll
- API-MS-Win-Core-io-l1-1-1.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: d45471cc066e6de7cb388036e06e727fe828a532
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521955"
---
# <a name="getqueuedcompletionstatusex-function"></a><span data-ttu-id="5171e-103">GetQueuedCompletionStatusEx fonction)</span><span class="sxs-lookup"><span data-stu-id="5171e-103">GetQueuedCompletionStatusEx function</span></span>

<span data-ttu-id="5171e-104">Récupère simultanément plusieurs entrées de port de terminaison.</span><span class="sxs-lookup"><span data-stu-id="5171e-104">Retrieves multiple completion port entries simultaneously.</span></span> <span data-ttu-id="5171e-105">Elle attend la fin des opérations d’e/s en attente associées au port de terminaison spécifié.</span><span class="sxs-lookup"><span data-stu-id="5171e-105">It waits for pending I/O operations that are associated with the specified completion port to complete.</span></span>

<span data-ttu-id="5171e-106">Pour défiler les paquets de fin d’exécution d’e/s une à la fois, utilisez la fonction [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="5171e-106">To dequeue I/O completion packets one at a time, use the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="5171e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5171e-107">Syntax</span></span>


```C++
BOOL WINAPI GetQueuedCompletionStatusEx(
  _In_  HANDLE             CompletionPort,
  _Out_ LPOVERLAPPED_ENTRY lpCompletionPortEntries,
  _In_  ULONG              ulCount,
  _Out_ PULONG             ulNumEntriesRemoved,
  _In_  DWORD              dwMilliseconds,
  _In_  BOOL               fAlertable
);
```



## <a name="parameters"></a><span data-ttu-id="5171e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5171e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5171e-109">*CompletionPort* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5171e-109">*CompletionPort* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5171e-110">Handle vers le port de terminaison.</span><span class="sxs-lookup"><span data-stu-id="5171e-110">A handle to the completion port.</span></span> <span data-ttu-id="5171e-111">Pour créer un port de terminaison, utilisez la fonction [**CreateIoCompletionPort**](createiocompletionport.md) .</span><span class="sxs-lookup"><span data-stu-id="5171e-111">To create a completion port, use the [**CreateIoCompletionPort**](createiocompletionport.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="5171e-112">*lpCompletionPortEntries* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5171e-112">*lpCompletionPortEntries* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5171e-113">En entrée, pointe vers un tableau pré-alloué de structures d' [**\_ entrée avec chevauchement**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) .</span><span class="sxs-lookup"><span data-stu-id="5171e-113">On input, points to a pre-allocated array of [**OVERLAPPED\_ENTRY**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) structures.</span></span>

<span data-ttu-id="5171e-114">Lors de la sortie, reçoit un tableau de structures d' [**\_ entrée avec chevauchement**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) qui contiennent les entrées.</span><span class="sxs-lookup"><span data-stu-id="5171e-114">On output, receives an array of [**OVERLAPPED\_ENTRY**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) structures that hold the entries.</span></span> <span data-ttu-id="5171e-115">Le nombre d’éléments du tableau est fourni par *ulNumEntriesRemoved*.</span><span class="sxs-lookup"><span data-stu-id="5171e-115">The number of array elements is provided by *ulNumEntriesRemoved*.</span></span>

<span data-ttu-id="5171e-116">Le nombre d’octets transférés au cours de chaque e/s, la clé de saisie semi-automatique qui indique sur quel fichier chaque e/s s’est produite, et l’adresse de la structure OVERLAPPED utilisée dans chaque e/s d’origine sont toutes retournées dans le tableau *lpCompletionPortEntries* .</span><span class="sxs-lookup"><span data-stu-id="5171e-116">The number of bytes transferred during each I/O, the completion key that indicates on which file each I/O occurred, and the overlapped structure address used in each original I/O are all returned in the *lpCompletionPortEntries* array.</span></span>

</dd> <dt>

<span data-ttu-id="5171e-117">*ulCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5171e-117">*ulCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5171e-118">Nombre maximal d’entrées à supprimer.</span><span class="sxs-lookup"><span data-stu-id="5171e-118">The maximum number of entries to remove.</span></span>

</dd> <dt>

<span data-ttu-id="5171e-119">*ulNumEntriesRemoved* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5171e-119">*ulNumEntriesRemoved* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5171e-120">Pointeur vers une variable qui reçoit le nombre d’entrées réellement supprimées.</span><span class="sxs-lookup"><span data-stu-id="5171e-120">A pointer to a variable that receives the number of entries actually removed.</span></span>

</dd> <dt>

<span data-ttu-id="5171e-121">*dwMilliseconds* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5171e-121">*dwMilliseconds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5171e-122">Nombre de millisecondes pendant lesquelles l’appelant est disposé à attendre qu’un paquet d’achèvement apparaisse sur le port de terminaison.</span><span class="sxs-lookup"><span data-stu-id="5171e-122">The number of milliseconds that the caller is willing to wait for a completion packet to appear at the completion port.</span></span> <span data-ttu-id="5171e-123">Si un paquet de saisie semi-automatique n’apparaît pas dans le délai spécifié, la fonction expire et retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="5171e-123">If a completion packet does not appear within the specified time, the function times out and returns **FALSE**.</span></span>

<span data-ttu-id="5171e-124">Si *dwMilliseconds* est **infini** (0xFFFFFFFF), la fonction n’expire jamais. Si *dwMilliseconds* est égal à zéro et qu’il n’y a pas d’opération d’e/s à défiler, la fonction expire immédiatement.</span><span class="sxs-lookup"><span data-stu-id="5171e-124">If *dwMilliseconds* is **INFINITE** (0xFFFFFFFF), the function will never time out. If *dwMilliseconds* is zero and there is no I/O operation to dequeue, the function will time out immediately.</span></span>

</dd> <dt>

<span data-ttu-id="5171e-125">*fAlertable* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5171e-125">*fAlertable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5171e-126">Si ce paramètre a la **valeur false**, la fonction ne retourne pas de valeur tant que le délai d’attente n’est pas écoulé ou qu’une entrée n’a pas été récupérée.</span><span class="sxs-lookup"><span data-stu-id="5171e-126">If this parameter is **FALSE**, the function does not return until the time-out period has elapsed or an entry is retrieved.</span></span>

<span data-ttu-id="5171e-127">Si le paramètre a la **valeur true** et qu’il n’y a pas d’entrées disponibles, la fonction exécute une attente signalable.</span><span class="sxs-lookup"><span data-stu-id="5171e-127">If the parameter is **TRUE** and there are no available entries, the function performs an alertable wait.</span></span> <span data-ttu-id="5171e-128">Le thread retourne lorsque le système met en file d’attente une routine d’exécution d’e/s ou un APC dans le thread et que le thread exécute la fonction.</span><span class="sxs-lookup"><span data-stu-id="5171e-128">The thread returns when the system queues an I/O completion routine or APC to the thread and the thread executes the function.</span></span>

<span data-ttu-id="5171e-129">Une routine de saisie semi-automatique est mise en file d’attente lorsque la fonction [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) ou [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) dans laquelle elle a été spécifiée est terminée, et le thread appelant est le thread qui a initié l’opération.</span><span class="sxs-lookup"><span data-stu-id="5171e-129">A completion routine is queued when the [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) or [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) function in which it was specified has completed, and the calling thread is the thread that initiated the operation.</span></span> <span data-ttu-id="5171e-130">Un APC est mis en file d’attente lorsque vous appelez [**QueueUserAPC**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-queueuserapc).</span><span class="sxs-lookup"><span data-stu-id="5171e-130">An APC is queued when you call [**QueueUserAPC**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-queueuserapc).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5171e-131">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5171e-131">Return value</span></span>

<span data-ttu-id="5171e-132">Retourne une valeur différente de zéro (**true**) en cas de réussite ou zéro (**false**) dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="5171e-132">Returns nonzero (**TRUE**) if successful or zero (**FALSE**) otherwise.</span></span>

<span data-ttu-id="5171e-133">Pour obtenir des informations détaillées sur l’erreur, appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="5171e-133">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="5171e-134">Remarques</span><span class="sxs-lookup"><span data-stu-id="5171e-134">Remarks</span></span>

<span data-ttu-id="5171e-135">Cette fonction associe un thread au port de terminaison spécifié.</span><span class="sxs-lookup"><span data-stu-id="5171e-135">This function associates a thread with the specified completion port.</span></span> <span data-ttu-id="5171e-136">Un thread peut être associé à au plus un port de terminaison.</span><span class="sxs-lookup"><span data-stu-id="5171e-136">A thread can be associated with at most one completion port.</span></span>

<span data-ttu-id="5171e-137">Cette fonction retourne la **valeur true** lorsqu’au moins une e/s en attente est terminée, mais il est possible qu’une ou plusieurs opérations d’e/s aient échoué.</span><span class="sxs-lookup"><span data-stu-id="5171e-137">This function returns **TRUE** when at least one pending I/O is completed, but it is possible that one or more I/O operations failed.</span></span> <span data-ttu-id="5171e-138">Notez qu’il revient à l’utilisateur de cette fonction de vérifier la liste des entrées retournées dans le paramètre *lpCompletionPortEntries* pour déterminer celles qui correspondent à toutes les opérations d’e/s ayant échoué, en examinant l’État contenu dans le membre **lpOverlapped** de chaque [**\_ entrée Overlapped**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry).</span><span class="sxs-lookup"><span data-stu-id="5171e-138">Note that it is up to the user of this function to check the list of returned entries in the *lpCompletionPortEntries* parameter to determine which of them correspond to any possible failed I/O operations by looking at the status contained in the **lpOverlapped** member in each [**OVERLAPPED\_ENTRY**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry).</span></span>

<span data-ttu-id="5171e-139">Cette fonction retourne la **valeur false** lorsqu’aucune opération d’e/s n’a été déplacée dans la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="5171e-139">This function returns **FALSE** when no I/O operation was dequeued.</span></span> <span data-ttu-id="5171e-140">Cela signifie généralement qu’une erreur s’est produite lors du traitement des paramètres de cet appel, ou que le handle *CompletionPort* a été fermé ou qu’il n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="5171e-140">This typically means that an error occurred while processing the parameters to this call, or that the *CompletionPort* handle was closed or is otherwise invalid.</span></span> <span data-ttu-id="5171e-141">La fonction [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) fournit des informations d’erreur étendues.</span><span class="sxs-lookup"><span data-stu-id="5171e-141">The [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function provides extended error information.</span></span>

<span data-ttu-id="5171e-142">Si un appel à [**GetQueuedCompletionStatusEx**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) échoue parce que le descripteur qui lui est associé est fermé, la fonction retourne **false** et [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne une **erreur d' \_ attente abandonnée \_ \_ 0**.</span><span class="sxs-lookup"><span data-stu-id="5171e-142">If a call to [**GetQueuedCompletionStatusEx**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) fails because the handle associated with it is closed, the function returns **FALSE** and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) will return **ERROR\_ABANDONED\_WAIT\_0**.</span></span>

<span data-ttu-id="5171e-143">Les applications serveur peuvent avoir plusieurs threads appelant la fonction **GetQueuedCompletionStatusEx** pour le même port de terminaison.</span><span class="sxs-lookup"><span data-stu-id="5171e-143">Server applications may have several threads calling the **GetQueuedCompletionStatusEx** function for the same completion port.</span></span> <span data-ttu-id="5171e-144">À mesure que les opérations d’e/s se terminent, elles sont mises en file d’attente sur ce port dans l’ordre First-in-First-Out.</span><span class="sxs-lookup"><span data-stu-id="5171e-144">As I/O operations complete, they are queued to this port in first-in-first-out order.</span></span> <span data-ttu-id="5171e-145">Si un thread attend activement cet appel, une ou plusieurs demandes mises en file d’attente terminent l’appel de ce thread uniquement.</span><span class="sxs-lookup"><span data-stu-id="5171e-145">If a thread is actively waiting on this call, one or more queued requests complete the call for that thread only.</span></span>

<span data-ttu-id="5171e-146">Pour plus d’informations sur la théorie, l’utilisation et les fonctions associées du port de terminaison d’e/s, consultez [ports de terminaison d’e/s](i-o-completion-ports.md).</span><span class="sxs-lookup"><span data-stu-id="5171e-146">For more information on I/O completion port theory, usage, and associated functions, see [I/O Completion Ports](i-o-completion-ports.md).</span></span>

<span data-ttu-id="5171e-147">Dans Windows 8 et Windows Server 2012, cette fonction est prise en charge par les technologies suivantes.</span><span class="sxs-lookup"><span data-stu-id="5171e-147">In Windows 8 and Windows Server 2012, this function is supported by the following technologies.</span></span>



| <span data-ttu-id="5171e-148">Technology</span><span class="sxs-lookup"><span data-stu-id="5171e-148">Technology</span></span>                                           | <span data-ttu-id="5171e-149">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="5171e-149">Supported</span></span>      |
|------------------------------------------------------|----------------|
| <span data-ttu-id="5171e-150">Protocole SMB (Server Message Block) 3,0</span><span class="sxs-lookup"><span data-stu-id="5171e-150">Server Message Block (SMB) 3.0 protocol</span></span><br/>   | <span data-ttu-id="5171e-151">Oui</span><span class="sxs-lookup"><span data-stu-id="5171e-151">Yes</span></span><br/> |
| <span data-ttu-id="5171e-152">Basculement transparent SMB 3,0 (TFO)</span><span class="sxs-lookup"><span data-stu-id="5171e-152">SMB 3.0 Transparent Failover (TFO)</span></span><br/>        | <span data-ttu-id="5171e-153">Oui</span><span class="sxs-lookup"><span data-stu-id="5171e-153">Yes</span></span><br/> |
| <span data-ttu-id="5171e-154">SMB 3,0 avec des partages de fichiers avec montée en puissance parallèle (SO)</span><span class="sxs-lookup"><span data-stu-id="5171e-154">SMB 3.0 with Scale-out File Shares (SO)</span></span><br/>   | <span data-ttu-id="5171e-155">Oui</span><span class="sxs-lookup"><span data-stu-id="5171e-155">Yes</span></span><br/> |
| <span data-ttu-id="5171e-156">Système de fichiers Volume partagé de cluster (CsvFS)</span><span class="sxs-lookup"><span data-stu-id="5171e-156">Cluster Shared Volume File System (CsvFS)</span></span><br/> | <span data-ttu-id="5171e-157">Oui</span><span class="sxs-lookup"><span data-stu-id="5171e-157">Yes</span></span><br/> |
| <span data-ttu-id="5171e-158">Système de fichiers résilient (ReFS)</span><span class="sxs-lookup"><span data-stu-id="5171e-158">Resilient File System (ReFS)</span></span><br/>              | <span data-ttu-id="5171e-159">Oui</span><span class="sxs-lookup"><span data-stu-id="5171e-159">Yes</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5171e-160">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5171e-160">Requirements</span></span>



| <span data-ttu-id="5171e-161">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5171e-161">Requirement</span></span> | <span data-ttu-id="5171e-162">Valeur</span><span class="sxs-lookup"><span data-stu-id="5171e-162">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5171e-163">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5171e-163">Minimum supported client</span></span><br/> | <span data-ttu-id="5171e-164">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="5171e-164">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                                   |
| <span data-ttu-id="5171e-165">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5171e-165">Minimum supported server</span></span><br/> | <span data-ttu-id="5171e-166">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="5171e-166">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                             |
| <span data-ttu-id="5171e-167">En-tête</span><span class="sxs-lookup"><span data-stu-id="5171e-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="5171e-168"><dt>IoAPI. h (inclure Windows. h); </dt> <dt>WinBase. h sur Windows server 2008 R2, Windows 7, Windows server 2008 et Windows Vista (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5171e-168"><dt>IoAPI.h (include Windows.h); </dt> <dt>WinBase.h on Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="5171e-169">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5171e-169">Library</span></span><br/>                  | <dl> <span data-ttu-id="5171e-170"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="5171e-170"><dt>Kernel32.lib</dt></span></span> </dl>                                                                                                                                                                                 |
| <span data-ttu-id="5171e-171">DLL</span><span class="sxs-lookup"><span data-stu-id="5171e-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5171e-172"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5171e-172"><dt>Kernel32.dll</dt></span></span> </dl>                                                                                                                                                                                 |



## <a name="see-also"></a><span data-ttu-id="5171e-173">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5171e-173">See also</span></span>

<dl> <dt>

<span data-ttu-id="5171e-174">**Rubriques de présentation**</span><span class="sxs-lookup"><span data-stu-id="5171e-174">**Overview Topics**</span></span>
</dt> <dt>

[<span data-ttu-id="5171e-175">Fonctions de gestion de fichiers</span><span class="sxs-lookup"><span data-stu-id="5171e-175">File Management Functions</span></span>](file-management-functions.md)
</dt> <dt>

[<span data-ttu-id="5171e-176">Ports de terminaison d’e/s</span><span class="sxs-lookup"><span data-stu-id="5171e-176">I/O Completion Ports</span></span>](i-o-completion-ports.md)
</dt> <dt>

[<span data-ttu-id="5171e-177">Utilisation des en-têtes Windows</span><span class="sxs-lookup"><span data-stu-id="5171e-177">Using the Windows Headers</span></span>](/windows/desktop/WinProg/using-the-windows-headers)
</dt> <dt>

<span data-ttu-id="5171e-178">**Fonctions**</span><span class="sxs-lookup"><span data-stu-id="5171e-178">**Functions**</span></span>
</dt> <dt>

[<span data-ttu-id="5171e-179">**ConnectNamedPipe**</span><span class="sxs-lookup"><span data-stu-id="5171e-179">**ConnectNamedPipe**</span></span>](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe)
</dt> <dt>

[<span data-ttu-id="5171e-180">**CreateIoCompletionPort**</span><span class="sxs-lookup"><span data-stu-id="5171e-180">**CreateIoCompletionPort**</span></span>](createiocompletionport.md)
</dt> <dt>

[<span data-ttu-id="5171e-181">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="5171e-181">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="5171e-182">**GetQueuedCompletionStatusEx**</span><span class="sxs-lookup"><span data-stu-id="5171e-182">**GetQueuedCompletionStatusEx**</span></span>](getqueuedcompletionstatusex-func.md)
</dt> <dt>

[<span data-ttu-id="5171e-183">**LockFileEx**</span><span class="sxs-lookup"><span data-stu-id="5171e-183">**LockFileEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex)
</dt> <dt>

[<span data-ttu-id="5171e-184">**ReadFile**</span><span class="sxs-lookup"><span data-stu-id="5171e-184">**ReadFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-readfile)
</dt> <dt>

[<span data-ttu-id="5171e-185">**PostQueuedCompletionStatus**</span><span class="sxs-lookup"><span data-stu-id="5171e-185">**PostQueuedCompletionStatus**</span></span>](postqueuedcompletionstatus.md)
</dt> <dt>

[<span data-ttu-id="5171e-186">**TransactNamedPipe**</span><span class="sxs-lookup"><span data-stu-id="5171e-186">**TransactNamedPipe**</span></span>](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)
</dt> <dt>

[<span data-ttu-id="5171e-187">**WaitCommEvent**</span><span class="sxs-lookup"><span data-stu-id="5171e-187">**WaitCommEvent**</span></span>](/windows/desktop/api/winbase/nf-winbase-waitcommevent)
</dt> <dt>

[<span data-ttu-id="5171e-188">**WriteFile**</span><span class="sxs-lookup"><span data-stu-id="5171e-188">**WriteFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-writefile)
</dt> </dl>

 

