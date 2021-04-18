---
description: Annule toutes les opérations d’entrée et de sortie (e/s) en attente émises par le thread appelant pour le fichier spécifié.
ms.assetid: b28162dc-0da8-41c6-9901-29381d2d72c4
title: CancelIo, fonction (IoAPI. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CancelIo
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-1.dll
- KernelBase.dll
- MinKernelBase.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: adb1ab95b30b31670a6ff5a4cc0e0205943f7683
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533845"
---
# <a name="cancelio-function"></a><span data-ttu-id="d6d91-103">CancelIo fonction)</span><span class="sxs-lookup"><span data-stu-id="d6d91-103">CancelIo function</span></span>

<span data-ttu-id="d6d91-104">Annule toutes les opérations d’entrée et de sortie (e/s) en attente émises par le thread appelant pour le fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="d6d91-104">Cancels all pending input and output (I/O) operations that are issued by the calling thread for the specified file.</span></span> <span data-ttu-id="d6d91-105">La fonction n’annule pas les opérations d’e/s émises par d’autres threads pour un handle de fichier.</span><span class="sxs-lookup"><span data-stu-id="d6d91-105">The function does not cancel I/O operations that other threads issue for a file handle.</span></span>

<span data-ttu-id="d6d91-106">Pour annuler les opérations d’e/s d’un autre thread, utilisez la fonction [**CancelIoEx**](cancelioex-func.md) .</span><span class="sxs-lookup"><span data-stu-id="d6d91-106">To cancel I/O operations from another thread, use the [**CancelIoEx**](cancelioex-func.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6d91-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d6d91-107">Syntax</span></span>


```C++
BOOL WINAPI CancelIo(
  _In_ HANDLE hFile
);
```



## <a name="parameters"></a><span data-ttu-id="d6d91-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d6d91-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6d91-109">*hFile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d6d91-109">*hFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6d91-110">Handle du fichier.</span><span class="sxs-lookup"><span data-stu-id="d6d91-110">A handle to the file.</span></span>

<span data-ttu-id="d6d91-111">La fonction annule toutes les opérations d’e/s en attente pour ce descripteur de fichier.</span><span class="sxs-lookup"><span data-stu-id="d6d91-111">The function cancels all pending I/O operations for this file handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6d91-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d6d91-112">Return value</span></span>

<span data-ttu-id="d6d91-113">Si la fonction réussit, la valeur de retour est différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="d6d91-113">If the function succeeds, the return value is nonzero.</span></span> <span data-ttu-id="d6d91-114">L’opération d’annulation pour toutes les opérations d’e/s en attente émises par le thread appelant pour le handle de fichier spécifié a été correctement demandée.</span><span class="sxs-lookup"><span data-stu-id="d6d91-114">The cancel operation for all pending I/O operations issued by the calling thread for the specified file handle was successfully requested.</span></span> <span data-ttu-id="d6d91-115">Le thread peut utiliser la fonction [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) pour déterminer à quel moment les opérations d’e/s ont elles-mêmes été effectuées.</span><span class="sxs-lookup"><span data-stu-id="d6d91-115">The thread can use the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function to determine when the I/O operations themselves have been completed.</span></span>

<span data-ttu-id="d6d91-116">Si la fonction échoue, la valeur de retour est zéro (0).</span><span class="sxs-lookup"><span data-stu-id="d6d91-116">If the function fails, the return value is zero (0).</span></span> <span data-ttu-id="d6d91-117">Pour afficher les informations d’erreur étendues, appelez la fonction [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="d6d91-117">To get extended error information, call the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6d91-118">Notes</span><span class="sxs-lookup"><span data-stu-id="d6d91-118">Remarks</span></span>

<span data-ttu-id="d6d91-119">Si des opérations d’e/s en cours sont en cours pour le handle de fichier spécifié et qu’elles sont émises par le thread appelant, la fonction **CancelIo** les annule.</span><span class="sxs-lookup"><span data-stu-id="d6d91-119">If there are any pending I/O operations in progress for the specified file handle, and they are issued by the calling thread, the **CancelIo** function cancels them.</span></span> <span data-ttu-id="d6d91-120">**CancelIo** annule uniquement les e/s en suspens sur le handle, mais ne modifie pas l’état du descripteur. Cela signifie que vous ne pouvez pas compter sur l’état du handle, car vous ne pouvez pas savoir si l’opération a été effectuée avec succès ou a été annulée.</span><span class="sxs-lookup"><span data-stu-id="d6d91-120">**CancelIo** cancels only outstanding I/O on the handle, it does not change the state of the handle; this means that you cannot rely on the state of the handle because you cannot know whether the operation was completed successfully or canceled.</span></span>

<span data-ttu-id="d6d91-121">Les opérations d’e/s doivent être émises en tant qu’e/s avec chevauchement.</span><span class="sxs-lookup"><span data-stu-id="d6d91-121">The I/O operations must be issued as overlapped I/O.</span></span> <span data-ttu-id="d6d91-122">Si ce n’est pas le cas, les opérations d’e/s ne retournent pas pour permettre au thread d’appeler la fonction **CancelIo** .</span><span class="sxs-lookup"><span data-stu-id="d6d91-122">If they are not, the I/O operations do not return to allow the thread to call the **CancelIo** function.</span></span> <span data-ttu-id="d6d91-123">L’appel de la fonction **CancelIo** avec un descripteur de fichier qui n’est pas ouvert avec l' **indicateur de fichier \_ \_ OVERLAPPED** n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="d6d91-123">Calling the **CancelIo** function with a file handle that is not opened with **FILE\_FLAG\_OVERLAPPED** does nothing.</span></span>

<span data-ttu-id="d6d91-124">Toutes les opérations d’e/s qui sont annulées avec l’erreur erreur d’erreur ont été **\_ \_ annulées**, et toutes les notifications de fin d’exécution des opérations d’e/s se produisent normalement.</span><span class="sxs-lookup"><span data-stu-id="d6d91-124">All I/O operations that are canceled complete with the error **ERROR\_OPERATION\_ABORTED**, and all completion notifications for the I/O operations occur normally.</span></span>

<span data-ttu-id="d6d91-125">Dans Windows 8 et Windows Server 2012, cette fonction est prise en charge par les technologies suivantes.</span><span class="sxs-lookup"><span data-stu-id="d6d91-125">In Windows 8 and Windows Server 2012, this function is supported by the following technologies.</span></span>



| <span data-ttu-id="d6d91-126">Technology</span><span class="sxs-lookup"><span data-stu-id="d6d91-126">Technology</span></span>                                           | <span data-ttu-id="d6d91-127">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6d91-127">Supported</span></span>      |
|------------------------------------------------------|----------------|
| <span data-ttu-id="d6d91-128">Protocole SMB (Server Message Block) 3,0</span><span class="sxs-lookup"><span data-stu-id="d6d91-128">Server Message Block (SMB) 3.0 protocol</span></span><br/>   | <span data-ttu-id="d6d91-129">Oui</span><span class="sxs-lookup"><span data-stu-id="d6d91-129">Yes</span></span><br/> |
| <span data-ttu-id="d6d91-130">Basculement transparent SMB 3,0 (TFO)</span><span class="sxs-lookup"><span data-stu-id="d6d91-130">SMB 3.0 Transparent Failover (TFO)</span></span><br/>        | <span data-ttu-id="d6d91-131">Oui</span><span class="sxs-lookup"><span data-stu-id="d6d91-131">Yes</span></span><br/> |
| <span data-ttu-id="d6d91-132">SMB 3,0 avec des partages de fichiers avec montée en puissance parallèle (SO)</span><span class="sxs-lookup"><span data-stu-id="d6d91-132">SMB 3.0 with Scale-out File Shares (SO)</span></span><br/>   | <span data-ttu-id="d6d91-133">Oui</span><span class="sxs-lookup"><span data-stu-id="d6d91-133">Yes</span></span><br/> |
| <span data-ttu-id="d6d91-134">Système de fichiers Volume partagé de cluster (CsvFS)</span><span class="sxs-lookup"><span data-stu-id="d6d91-134">Cluster Shared Volume File System (CsvFS)</span></span><br/> | <span data-ttu-id="d6d91-135">Oui</span><span class="sxs-lookup"><span data-stu-id="d6d91-135">Yes</span></span><br/> |
| <span data-ttu-id="d6d91-136">Système de fichiers résilient (ReFS)</span><span class="sxs-lookup"><span data-stu-id="d6d91-136">Resilient File System (ReFS)</span></span><br/>              | <span data-ttu-id="d6d91-137">Oui</span><span class="sxs-lookup"><span data-stu-id="d6d91-137">Yes</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d6d91-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d6d91-138">Requirements</span></span>



| <span data-ttu-id="d6d91-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d6d91-139">Requirement</span></span> | <span data-ttu-id="d6d91-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="d6d91-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6d91-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6d91-141">Minimum supported client</span></span><br/> | <span data-ttu-id="d6d91-142">Applications de bureau Windows XP- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="d6d91-142">Windows XP \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="d6d91-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6d91-143">Minimum supported server</span></span><br/> | <span data-ttu-id="d6d91-144">Applications de bureau Windows Server 2003 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="d6d91-144">Windows Server 2003 \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                                                              |
| <span data-ttu-id="d6d91-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="d6d91-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6d91-146"><dt>IoAPI. h (inclure Windows. h); </dt> <dt>WinBase. h sur Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 et Windows XP (incluant Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d6d91-146"><dt>IoAPI.h (include Windows.h); </dt> <dt>WinBase.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="d6d91-147">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d6d91-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="d6d91-148"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="d6d91-148"><dt>Kernel32.lib</dt></span></span> </dl>                                                                                                                                                                                                                  |
| <span data-ttu-id="d6d91-149">DLL</span><span class="sxs-lookup"><span data-stu-id="d6d91-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6d91-150"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6d91-150"><dt>Kernel32.dll</dt></span></span> </dl>                                                                                                                                                                                                                  |



## <a name="see-also"></a><span data-ttu-id="d6d91-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6d91-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6d91-152">**CancelIoEx**</span><span class="sxs-lookup"><span data-stu-id="d6d91-152">**CancelIoEx**</span></span>](cancelioex-func.md)
</dt> <dt>

[<span data-ttu-id="d6d91-153">**CancelSynchronousIo**</span><span class="sxs-lookup"><span data-stu-id="d6d91-153">**CancelSynchronousIo**</span></span>](cancelsynchronousio-func.md)
</dt> <dt>

[<span data-ttu-id="d6d91-154">**CreateFile**</span><span class="sxs-lookup"><span data-stu-id="d6d91-154">**CreateFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[<span data-ttu-id="d6d91-155">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="d6d91-155">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="d6d91-156">Fonctions de gestion de fichiers</span><span class="sxs-lookup"><span data-stu-id="d6d91-156">File Management Functions</span></span>](file-management-functions.md)
</dt> <dt>

[<span data-ttu-id="d6d91-157">**LockFileEx**</span><span class="sxs-lookup"><span data-stu-id="d6d91-157">**LockFileEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex)
</dt> <dt>

[<span data-ttu-id="d6d91-158">**ReadDirectoryChangesW**</span><span class="sxs-lookup"><span data-stu-id="d6d91-158">**ReadDirectoryChangesW**</span></span>](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)
</dt> <dt>

[<span data-ttu-id="d6d91-159">**ReadFile**</span><span class="sxs-lookup"><span data-stu-id="d6d91-159">**ReadFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-readfile)
</dt> <dt>

[<span data-ttu-id="d6d91-160">**ReadFileEx**</span><span class="sxs-lookup"><span data-stu-id="d6d91-160">**ReadFileEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-readfileex)
</dt> <dt>

[<span data-ttu-id="d6d91-161">E/s synchrones et asynchrones</span><span class="sxs-lookup"><span data-stu-id="d6d91-161">Synchronous and Asynchronous I/O</span></span>](synchronous-and-asynchronous-i-o.md)
</dt> <dt>

[<span data-ttu-id="d6d91-162">**WriteFile**</span><span class="sxs-lookup"><span data-stu-id="d6d91-162">**WriteFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-writefile)
</dt> <dt>

[<span data-ttu-id="d6d91-163">**WriteFileEx**</span><span class="sxs-lookup"><span data-stu-id="d6d91-163">**WriteFileEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-writefileex)
</dt> </dl>

 

