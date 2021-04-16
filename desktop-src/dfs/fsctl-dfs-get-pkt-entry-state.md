---
title: FSCTL_DFS_GET_PKT_ENTRY_STATE, code de contrôle (LmDfs.h)
description: Le code de contrôle FSCTL_DFS_GET_PKT_ENTRY_STATE peut obtenir les mêmes informations que la fonction NetDfsGetClientInfo, mais peut fournir de meilleures performances dans certaines configurations avec des latences élevées aux serveurs DFS.
ms.assetid: d4eec104-128b-43b5-9fae-08ab0b977dec
topic_type:
- apiref
api_name:
- FSCTL_DFS_GET_PKT_ENTRY_STATE
api_location:
- LmDfs.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a57fb448934908ebc1530e95a298715324aaee6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524031"
---
# <a name="fsctl_dfs_get_pkt_entry_state-control-code"></a><span data-ttu-id="ba0eb-103">Code de contrôle FSCTL_DFS_GET_PKT_ENTRY_STATE</span><span class="sxs-lookup"><span data-stu-id="ba0eb-103">FSCTL_DFS_GET_PKT_ENTRY_STATE control code</span></span>

<span data-ttu-id="ba0eb-104">Le code de contrôle **FSCTL_DFS_GET_PKT_ENTRY_STATE** peut obtenir les mêmes informations que la fonction [**NetDfsGetClientInfo**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo) , mais peut fournir de meilleures performances dans certaines configurations avec des latences élevées aux serveurs DFS.</span><span class="sxs-lookup"><span data-stu-id="ba0eb-104">The **FSCTL_DFS_GET_PKT_ENTRY_STATE** control code can get the same information as the [**NetDfsGetClientInfo**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo) function but can provide better performance in some configurations with high latencies to the DFS servers.</span></span> <span data-ttu-id="ba0eb-105">Il n’est pas recommandé d’utiliser le code de contrôle **FSCTL_DFS_GET_PKT_ENTRY_STATE** , sauf s’il existe des problèmes de performances.</span><span class="sxs-lookup"><span data-stu-id="ba0eb-105">It is not recommended to use the **FSCTL_DFS_GET_PKT_ENTRY_STATE** control code unless there are performance issues.</span></span>

<span data-ttu-id="ba0eb-106">Pour effectuer cette opération, appelez la fonction [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="ba0eb-106">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>

```C++
BOOL 
   WINAPI 
   DeviceIoControl( (HANDLE)       hDevice,            // handle to device
                    (DWORD)        FSCTL_DFS_GET_PKT_ENTRY_STATE, // dwIoControlCode(LPDWORD)      lpInBuffer,         // input buffer
                    (DWORD)        nInBufferSize,      // size of input buffer
                    (LPDWORD)      lpOutBuffer,        // output buffer
                    (DWORD)        nOutBufferSize,     // size of output buffer
                    (LPDWORD)      lpBytesReturned,    // number of bytes returned
                    (LPOVERLAPPED) lpOverlapped );     // OVERLAPPED structure
```

## <a name="parameters"></a><span data-ttu-id="ba0eb-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ba0eb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba0eb-108">*hDevice* [in]</span><span class="sxs-lookup"><span data-stu-id="ba0eb-108">*hDevice* [in]</span></span>
</dt> <dd>

<span data-ttu-id="ba0eb-109">Handle de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ba0eb-109">A handle to the device.</span></span> <span data-ttu-id="ba0eb-110">Pour obtenir un descripteur d’appareil, appelez la fonction [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="ba0eb-110">To obtain a device handle, call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="ba0eb-111">*dwIoControlCode* [in]</span><span class="sxs-lookup"><span data-stu-id="ba0eb-111">*dwIoControlCode* [in]</span></span>
</dt> <dd>

<span data-ttu-id="ba0eb-112">Code de contrôle de l’opération.</span><span class="sxs-lookup"><span data-stu-id="ba0eb-112">The control code for the operation.</span></span> <span data-ttu-id="ba0eb-113">Utilisez **FSCTL_DFS_GET_PKT_ENTRY_STATE** pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="ba0eb-113">Use **FSCTL_DFS_GET_PKT_ENTRY_STATE** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="ba0eb-114">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="ba0eb-114">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="ba0eb-115">Adresse d’une structure [**DFS_GET_PKT_ENTRY_STATE_ARG**](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg) et des chaînes Unicode 1-3 qui suivent.</span><span class="sxs-lookup"><span data-stu-id="ba0eb-115">Address of a [**DFS_GET_PKT_ENTRY_STATE_ARG**](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg) structure and the 1-3 Unicode strings that follow.</span></span>

</dd> <dt>

<span data-ttu-id="ba0eb-116">*nInBufferSize* [in]</span><span class="sxs-lookup"><span data-stu-id="ba0eb-116">*nInBufferSize* [in]</span></span>
</dt> <dd>

<span data-ttu-id="ba0eb-117">Taille, en octets, de la mémoire tampon vers laquelle pointe le paramètre *lpInBuffer* .</span><span class="sxs-lookup"><span data-stu-id="ba0eb-117">Size, in bytes, of the buffer pointed to by the *lpInBuffer* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ba0eb-118">*lpOutBuffer* [out]</span><span class="sxs-lookup"><span data-stu-id="ba0eb-118">*lpOutBuffer* [out]</span></span>
</dt> <dd>

<span data-ttu-id="ba0eb-119">Adresse d’une **structure \# DFS_INFO_** et toute chaîne et structure vers laquelle pointe la **structure \# DFS_INFO_** .</span><span class="sxs-lookup"><span data-stu-id="ba0eb-119">Address of a **DFS_INFO_\#** structure and any strings and structures pointed to by the **DFS_INFO_\#** structure.</span></span> <span data-ttu-id="ba0eb-120">La structure spécifique retournée dépend du membre de **niveau** de la structure [**DFS_GET_PKT_ENTRY_STATE_ARG**](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg) passée dans la mémoire tampon d’entrée.</span><span class="sxs-lookup"><span data-stu-id="ba0eb-120">The specific structure returned depends on the **Level** member in the [**DFS_GET_PKT_ENTRY_STATE_ARG**](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg) structure passed in the input buffer.</span></span>

</dd> <dt>

<span data-ttu-id="ba0eb-121">*nOutBufferSize* [in]</span><span class="sxs-lookup"><span data-stu-id="ba0eb-121">*nOutBufferSize* [in]</span></span>
</dt> <dd>

<span data-ttu-id="ba0eb-122">Taille, en octets, de la mémoire tampon vers laquelle pointe le paramètre *lpOutBuffer* .</span><span class="sxs-lookup"><span data-stu-id="ba0eb-122">Size, in bytes, of the buffer pointed to by the *lpOutBuffer* parameter.</span></span> <span data-ttu-id="ba0eb-123">En raison des chaînes et des structures référencées par la **structure \# DFS_INFO_** retournée qui se trouvent également dans la mémoire tampon de sortie, cette mémoire tampon doit être plus grande que la structure **DFS_INFO_ \#** spécifiée.</span><span class="sxs-lookup"><span data-stu-id="ba0eb-123">Due to the strings and structures referenced by the returned **DFS_INFO_\#** structure that are also in the output buffer, this buffer should be larger than the **DFS_INFO_\#** structure specified.</span></span>

</dd> <dt>

<span data-ttu-id="ba0eb-124">*lpBytesReturned* [out]</span><span class="sxs-lookup"><span data-stu-id="ba0eb-124">*lpBytesReturned* [out]</span></span>
</dt> <dd>

<span data-ttu-id="ba0eb-125">Pointeur vers une variable qui reçoit la taille des données stockées dans la mémoire tampon de sortie, en octets.</span><span class="sxs-lookup"><span data-stu-id="ba0eb-125">A pointer to a variable that receives the size of the data stored in the output buffer, in bytes.</span></span>

<span data-ttu-id="ba0eb-126">Si la mémoire tampon de sortie est trop petite, mais au moins suffisamment grande pour contenir une **valeur DWORD**, l’appel échoue, [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne **ERROR_MORE_DATA**, et le premier **DWORD** de la mémoire tampon de sortie contient la taille requise.</span><span class="sxs-lookup"><span data-stu-id="ba0eb-126">If the output buffer is too small, but at least large enough to hold a **DWORD**, the call fails, [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns **ERROR_MORE_DATA**, and the first **DWORD** of the output buffer contains the size that would have been required.</span></span> <span data-ttu-id="ba0eb-127">Si la mémoire tampon de sortie ne peut pas contenir de **valeur DWORD** , l’appel échoue avec **ERROR_INSUFFICIENT_BUFFER**, et *lpBytesReturned* est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="ba0eb-127">If the output buffer cannot hold a **DWORD** then the call fails with **ERROR_INSUFFICIENT_BUFFER**, and *lpBytesReturned* is zero.</span></span>

<span data-ttu-id="ba0eb-128">Si *lpOverlapped* a la **valeur null**, *lpBytesReturned* ne peut pas avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="ba0eb-128">If *lpOverlapped* is **NULL**, *lpBytesReturned* cannot be **NULL**.</span></span> <span data-ttu-id="ba0eb-129">Même lorsqu’une opération ne retourne aucune donnée de sortie et que *lpOutBuffer* a la **valeur null**, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) utilise *lpBytesReturned*.</span><span class="sxs-lookup"><span data-stu-id="ba0eb-129">Even when an operation returns no output data and *lpOutBuffer* is **NULL**, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) makes use of *lpBytesReturned*.</span></span> <span data-ttu-id="ba0eb-130">Après une telle opération, la valeur de *lpBytesReturned* est sans signification.</span><span class="sxs-lookup"><span data-stu-id="ba0eb-130">After such an operation, the value of *lpBytesReturned* is meaningless.</span></span>

<span data-ttu-id="ba0eb-131">Si *lpOverlapped* n’a pas la **valeur null**, *LpBytesReturned* peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="ba0eb-131">If *lpOverlapped* is not **NULL**, *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="ba0eb-132">Si ce paramètre n’est pas **null** et que l’opération retourne des données, *lpBytesReturned* n’a pas de sens tant que l’opération avec chevauchement n’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="ba0eb-132">If this parameter is not **NULL** and the operation returns data, *lpBytesReturned* is meaningless until the overlapped operation has completed.</span></span> <span data-ttu-id="ba0eb-133">Pour récupérer le nombre d’octets retournés, appelez [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult).</span><span class="sxs-lookup"><span data-stu-id="ba0eb-133">To retrieve the number of bytes returned, call [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult).</span></span> <span data-ttu-id="ba0eb-134">Si le paramètre *hDevice* est associé à un port de terminaison d’e/s, vous pouvez récupérer le nombre d’octets renvoyés en appelant [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus).</span><span class="sxs-lookup"><span data-stu-id="ba0eb-134">If the *hDevice* parameter is associated with an I/O completion port, you can retrieve the number of bytes returned by calling [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus).</span></span>

</dd> <dt>

<span data-ttu-id="ba0eb-135">*lpOverlapped* [in]</span><span class="sxs-lookup"><span data-stu-id="ba0eb-135">*lpOverlapped* [in]</span></span>
</dt> <dd>

<span data-ttu-id="ba0eb-136">Pointeur vers une structure [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="ba0eb-136">A pointer to an [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="ba0eb-137">Si *hDevice* a été ouvert sans spécifier **FILE_FLAG_OVERLAPPED**, *lpOverlapped* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="ba0eb-137">If *hDevice* was opened without specifying **FILE_FLAG_OVERLAPPED**, *lpOverlapped* is ignored.</span></span>

<span data-ttu-id="ba0eb-138">Si *hDevice* a été ouvert avec l’indicateur **FILE_FLAG_OVERLAPPED** , l’opération est exécutée en tant qu’opération Overlapped (asynchrone).</span><span class="sxs-lookup"><span data-stu-id="ba0eb-138">If *hDevice* was opened with the **FILE_FLAG_OVERLAPPED** flag, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="ba0eb-139">Dans ce cas, *lpOverlapped* doit pointer vers une structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) valide qui contient un handle vers un objet d’événement.</span><span class="sxs-lookup"><span data-stu-id="ba0eb-139">In this case, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure that contains a handle to an event object.</span></span> <span data-ttu-id="ba0eb-140">Dans le cas contraire, la fonction échoue de façon imprévisible.</span><span class="sxs-lookup"><span data-stu-id="ba0eb-140">Otherwise, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="ba0eb-141">Pour les opérations avec chevauchement, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne immédiatement, et l’objet d’événement est signalé lorsque l’opération est terminée.</span><span class="sxs-lookup"><span data-stu-id="ba0eb-141">For overlapped operations, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns immediately, and the event object is signaled when the operation has been completed.</span></span> <span data-ttu-id="ba0eb-142">Sinon, la fonction ne retourne pas jusqu’à ce que l’opération soit terminée ou qu’une erreur se produise.</span><span class="sxs-lookup"><span data-stu-id="ba0eb-142">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba0eb-143">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ba0eb-143">Return value</span></span>

<span data-ttu-id="ba0eb-144">Si l’opération se termine correctement, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="ba0eb-144">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="ba0eb-145">Si l’opération échoue ou est en attente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="ba0eb-145">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="ba0eb-146">Pour obtenir des informations détaillées sur l’erreur, appelez [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="ba0eb-146">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="ba0eb-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ba0eb-147">Requirements</span></span>

| <span data-ttu-id="ba0eb-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ba0eb-148">Requirement</span></span> | <span data-ttu-id="ba0eb-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="ba0eb-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba0eb-150">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ba0eb-150">Minimum supported client</span></span><br/> | <span data-ttu-id="ba0eb-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ba0eb-151">Windows Vista</span></span><br/>                                                                             |
| <span data-ttu-id="ba0eb-152">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ba0eb-152">Minimum supported server</span></span><br/> | <span data-ttu-id="ba0eb-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ba0eb-153">Windows Server 2008</span></span><br/>                                                                       |
| <span data-ttu-id="ba0eb-154">En-tête</span><span class="sxs-lookup"><span data-stu-id="ba0eb-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba0eb-155"><dt>LmDfs. h (inclure LmDfs. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ba0eb-155"><dt>LmDfs.h (include LmDfs.h)</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="ba0eb-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ba0eb-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba0eb-157">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="ba0eb-157">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="ba0eb-158">**NetDfsGetClientInfo**</span><span class="sxs-lookup"><span data-stu-id="ba0eb-158">**NetDfsGetClientInfo**</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo)
</dt> </dl>
