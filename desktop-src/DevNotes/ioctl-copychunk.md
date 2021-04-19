---
description: Le \_ Code de contrôle IOCTL COPYCHUNK initie une copie côté serveur d’une plage de données, également appelée un segment.
ms.assetid: 36f68840-bd5c-4cfc-a8ad-0cfbbdc5a2a9
title: Code de contrôle IOCTL_COPYCHUNK
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COPY_CHUNK
api_type:
- NA
api_location: ''
ms.openlocfilehash: c425fc53563e6dfc16d2040fb575f47f0f8fdf35
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515765"
---
# <a name="ioctl_copychunk-control-code"></a><span data-ttu-id="82887-103">\_Code de contrôle COPYCHUNK IOCTL</span><span class="sxs-lookup"><span data-stu-id="82887-103">IOCTL\_COPYCHUNK control code</span></span>

<span data-ttu-id="82887-104">Le code de contrôle **IOCTL \_ COPYCHUNK** initie une copie côté serveur d’une plage de données, également appelée un segment.</span><span class="sxs-lookup"><span data-stu-id="82887-104">The **IOCTL\_COPYCHUNK** control code initiates a server-side copy of a range of data, also called a chunk.</span></span>

<span data-ttu-id="82887-105">Pour effectuer cette opération, appelez la fonction [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="82887-105">To perform this operation, call the [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  IOCTL_COPYCHUNK,              // dwIoControlCode
  (LPVOID) lpInBuffer,          // input buffer
  (DWORD) nInBufferSize,        // size of input buffer
  (LPVOID) lpOutBuffer,         // output buffer
  (DWORD) nOutBufferSize,       // size of output buffer
  (LPDWORD) lpBytesReturned,    // number of bytes returned
  (LPOVERLAPPED) lpOverlapped   // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="82887-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="82887-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82887-107">*hDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="82887-107">*hDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82887-108">Handle du fichier qui est la cible de l’opération de copie côté serveur.</span><span class="sxs-lookup"><span data-stu-id="82887-108">A handle to the file that is the target of the server-side copy operation.</span></span> <span data-ttu-id="82887-109">Pour obtenir ce descripteur, appelez la fonction [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="82887-109">To obtain this handle, call the [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="82887-110">*dwIoControlCode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="82887-110">*dwIoControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82887-111">Code de contrôle de l’opération.</span><span class="sxs-lookup"><span data-stu-id="82887-111">The control code for the operation.</span></span> <span data-ttu-id="82887-112">Utilisez **IOCTL \_ COPYCHUNK** pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="82887-112">Use **IOCTL\_COPYCHUNK** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="82887-113">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="82887-113">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="82887-114">Pointeur vers la mémoire tampon d’entrée, une structure de **\_ \_ copie COPYCHUNK SRV** .</span><span class="sxs-lookup"><span data-stu-id="82887-114">A pointer to the input buffer, a **SRV\_COPYCHUNK\_COPY** structure.</span></span> <span data-ttu-id="82887-115">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="82887-115">For more information, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="82887-116">*nInBufferSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="82887-116">*nInBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82887-117">Taille de la mémoire tampon d’entrée, en octets.</span><span class="sxs-lookup"><span data-stu-id="82887-117">The size of the input buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="82887-118">*lpOutBuffer* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="82887-118">*lpOutBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="82887-119">Pointeur vers la mémoire tampon de sortie, une structure de **\_ \_ réponse SRV COPYCHUNK** .</span><span class="sxs-lookup"><span data-stu-id="82887-119">A pointer to the output buffer, a **SRV\_COPYCHUNK\_RESPONSE** structure.</span></span> <span data-ttu-id="82887-120">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="82887-120">For more information, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="82887-121">*nOutBufferSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="82887-121">*nOutBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82887-122">Taille de la mémoire tampon de sortie en octets.</span><span class="sxs-lookup"><span data-stu-id="82887-122">The size of the output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="82887-123">*lpBytesReturned* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="82887-123">*lpBytesReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="82887-124">Pointeur vers une variable qui reçoit la taille des données stockées dans la mémoire tampon de sortie, en octets.</span><span class="sxs-lookup"><span data-stu-id="82887-124">A pointer to a variable that receives the size of the data stored in the output buffer, in bytes.</span></span>

<span data-ttu-id="82887-125">Si la mémoire tampon de sortie est trop petite, l’appel échoue, la fonction [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne l' **erreur \_ \_ mémoire tampon insuffisante** et *lpBytesReturned* est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="82887-125">If the output buffer is too small, the call fails, the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns **ERROR\_INSUFFICIENT\_BUFFER**, and *lpBytesReturned* is zero.</span></span>

<span data-ttu-id="82887-126">Si le paramètre *lpOverlapped* a la **valeur null**, *lpBytesReturned* ne peut pas avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="82887-126">If the *lpOverlapped* parameter is **NULL**, *lpBytesReturned* cannot be **NULL**.</span></span> <span data-ttu-id="82887-127">Même lorsqu’une opération ne retourne aucune donnée de sortie et que le paramètre *lpOutBuffer* a la **valeur null**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) utilise *lpBytesReturned*.</span><span class="sxs-lookup"><span data-stu-id="82887-127">Even when an operation returns no output data and the *lpOutBuffer* parameter is **NULL**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) makes use of *lpBytesReturned*.</span></span> <span data-ttu-id="82887-128">Après une telle opération, la valeur de *lpBytesReturned* est sans signification.</span><span class="sxs-lookup"><span data-stu-id="82887-128">After such an operation, the value of *lpBytesReturned* is meaningless.</span></span>

<span data-ttu-id="82887-129">Si *lpOverlapped* n’a pas la **valeur null**, *LpBytesReturned* peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="82887-129">If *lpOverlapped* is not **NULL**, *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="82887-130">Si *lpOverlapped* n’a pas la **valeur null** et que l’opération retourne des données, *lpBytesReturned* n’a aucun sens tant que l’opération avec chevauchement n’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="82887-130">If *lpOverlapped* is not **NULL** and the operation returns data, *lpBytesReturned* is meaningless until the overlapped operation has completed.</span></span> <span data-ttu-id="82887-131">Pour récupérer le nombre d’octets retournés, appelez la fonction [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) .</span><span class="sxs-lookup"><span data-stu-id="82887-131">To retrieve the number of bytes returned, call the [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="82887-132">Si le paramètre *hDevice* est associé à un port de terminaison d’e/s, vous pouvez récupérer le nombre d’octets renvoyés en appelant la fonction [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="82887-132">If the *hDevice* parameter is associated with an I/O completion port, you can retrieve the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="82887-133">*lpOverlapped* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="82887-133">*lpOverlapped* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82887-134">Pointeur vers une structure [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="82887-134">A pointer to an [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="82887-135">Si le paramètre *hDevice* a été ouvert sans spécifier d' **indicateur de fichier avec \_ \_ chevauchement**, *lpOverlapped* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="82887-135">If the *hDevice* parameter was opened without specifying **FILE\_FLAG\_OVERLAPPED**, *lpOverlapped* is ignored.</span></span>

<span data-ttu-id="82887-136">Si *hDevice* a été ouvert avec l’indicateur de fichier avec l' **indicateur de \_ \_ chevauchement** , l’opération est exécutée en tant qu’opération Overlapped (asynchrone).</span><span class="sxs-lookup"><span data-stu-id="82887-136">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="82887-137">Dans ce cas, *lpOverlapped* doit pointer vers une structure [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) valide qui contient un handle vers un objet d’événement.</span><span class="sxs-lookup"><span data-stu-id="82887-137">In this case, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure that contains a handle to an event object.</span></span> <span data-ttu-id="82887-138">Dans le cas contraire, la fonction échoue de façon imprévisible.</span><span class="sxs-lookup"><span data-stu-id="82887-138">Otherwise, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="82887-139">Pour les opérations avec chevauchement, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne immédiatement, et l’objet d’événement est signalé lorsque l’opération est terminée.</span><span class="sxs-lookup"><span data-stu-id="82887-139">For overlapped operations, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns immediately, and the event object is signaled when the operation has been completed.</span></span> <span data-ttu-id="82887-140">Sinon, la fonction ne retourne pas jusqu’à ce que l’opération soit terminée ou jusqu’à ce qu’une erreur se produise.</span><span class="sxs-lookup"><span data-stu-id="82887-140">Otherwise, the function does not return until the operation has been completed or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82887-141">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="82887-141">Return value</span></span>

<span data-ttu-id="82887-142">Si l’opération se termine correctement, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="82887-142">If the operation completes successfully, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="82887-143">Si l’opération échoue ou est en attente, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="82887-143">If the operation fails or is pending, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="82887-144">Pour obtenir des informations détaillées sur l’erreur, appelez [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="82887-144">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="82887-145">Remarques</span><span class="sxs-lookup"><span data-stu-id="82887-145">Remarks</span></span>

<span data-ttu-id="82887-146">Ce code de contrôle n’a aucun fichier d’en-tête associé.</span><span class="sxs-lookup"><span data-stu-id="82887-146">This control code has no associated header file.</span></span> <span data-ttu-id="82887-147">Vous devez définir le code de contrôle et les structures de données comme suit.</span><span class="sxs-lookup"><span data-stu-id="82887-147">You must define the control code and data structures as follows.</span></span>

``` syntax
#define IOCTL_COPYCHUNK CTL_CODE(FILE_DEVICE_NETWORK_FILE_SYSTEM, 262, METHOD_BUFFERED,  FILE_READ_ACCESS)

typedef struct _SRV_COPYCHUNK {
    LARGE_INTEGER SourceOffset;
    LARGE_INTEGER DestinationOffset;
    ULONG  Length;
} SRV_COPYCHUNK, *PSRV_COPYCHUNK;

typedef struct _SRV_COPYCHUNK_COPY {
    SRV_RESUME_KEY SourceFile;
    ULONG          ChunkCount;
    ULONG          Reserved;
    SRV_COPYCHUNK  Chunk[1];    // Array
} SRV_COPYCHUNK_COPY, *PSRV_COPYCHUNK_COPY;

typedef struct _SRV_COPYCHUNK_RESPONSE {
    ULONG          ChunksWritten;
    ULONG          ChunkBytesWritten;
    ULONG          TotalBytesWritten;
} SRV_COPYCHUNK_RESPONSE, *PSRV_COPYCHUNK_RESPONSE;
```

<span data-ttu-id="82887-148">Ces membres peuvent être décrits comme suit.</span><span class="sxs-lookup"><span data-stu-id="82887-148">These members can be described as follows.</span></span>



| <span data-ttu-id="82887-149">Membre</span><span class="sxs-lookup"><span data-stu-id="82887-149">Member</span></span>                                                                                                                                       | <span data-ttu-id="82887-150">Description</span><span class="sxs-lookup"><span data-stu-id="82887-150">Description</span></span>                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82887-151"><span id="SourceOffset"></span><span id="sourceoffset"></span><span id="SOURCEOFFSET"></span>**SourceOffset**</span><span class="sxs-lookup"><span data-stu-id="82887-151"><span id="SourceOffset"></span><span id="sourceoffset"></span><span id="SOURCEOFFSET"></span>**SourceOffset**</span></span><br/>                     | <span data-ttu-id="82887-152">Offset, en octets, entre le début du fichier source et le segment à copier.</span><span class="sxs-lookup"><span data-stu-id="82887-152">The offset, in bytes, from the beginning of the source file to the chunk to be copied.</span></span><br/>                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="82887-153"><span id="DestinationOffset"></span><span id="destinationoffset"></span><span id="DESTINATIONOFFSET"></span>**DestinationOffset**</span><span class="sxs-lookup"><span data-stu-id="82887-153"><span id="DestinationOffset"></span><span id="destinationoffset"></span><span id="DESTINATIONOFFSET"></span>**DestinationOffset**</span></span><br/> | <span data-ttu-id="82887-154">Offset, en octets, entre le début du fichier cible et l’emplacement où le segment doit être copié.</span><span class="sxs-lookup"><span data-stu-id="82887-154">The offset, in bytes, from the beginning of the target file to the location where the chunk is to be copied.</span></span><br/>                                                                                                                                                                                                                                               |
| <span data-ttu-id="82887-155"><span id="Length"></span><span id="length"></span><span id="LENGTH"></span>**Base**</span><span class="sxs-lookup"><span data-stu-id="82887-155"><span id="Length"></span><span id="length"></span><span id="LENGTH"></span>**Length**</span></span><br/>                                             | <span data-ttu-id="82887-156">Nombre d’octets de données dans le bloc à copier.</span><span class="sxs-lookup"><span data-stu-id="82887-156">The number of bytes of data in the chunk to be copied.</span></span> <span data-ttu-id="82887-157">Doit être supérieur à zéro et inférieur ou égal à 1 Mo.</span><span class="sxs-lookup"><span data-stu-id="82887-157">Must be greater than zero and less than or equal to 1 MB.</span></span> <span data-ttu-id="82887-158">**Longueur** \* **ChunkCount** doit être inférieur ou égal à 16 Mo.</span><span class="sxs-lookup"><span data-stu-id="82887-158">**Length** \* **ChunkCount** must be less than or equal to 16 MB.</span></span><br/>                                                                                                                                                                         |
| <span data-ttu-id="82887-159"><span id="SourceFile"></span><span id="sourcefile"></span><span id="SOURCEFILE"></span>**SourceFile**</span><span class="sxs-lookup"><span data-stu-id="82887-159"><span id="SourceFile"></span><span id="sourcefile"></span><span id="SOURCEFILE"></span>**SourceFile**</span></span><br/>                             | <span data-ttu-id="82887-160">Clé qui représente le fichier source avec les données à copier.</span><span class="sxs-lookup"><span data-stu-id="82887-160">A key that represents the source file with the data to be copied.</span></span> <span data-ttu-id="82887-161">Cette clé est obtenue via [**la \_ \_ clé de \_ reprise \_ de la demande FSCTL SRV**](fsctl-srv-request-resume-key.md).</span><span class="sxs-lookup"><span data-stu-id="82887-161">This key is obtained through [**FSCTL\_SRV\_REQUEST\_RESUME\_KEY**](fsctl-srv-request-resume-key.md).</span></span><br/>                                                                                                                                                                                   |
| <span data-ttu-id="82887-162"><span id="ChunkCount"></span><span id="chunkcount"></span><span id="CHUNKCOUNT"></span>**ChunkCount**</span><span class="sxs-lookup"><span data-stu-id="82887-162"><span id="ChunkCount"></span><span id="chunkcount"></span><span id="CHUNKCOUNT"></span>**ChunkCount**</span></span><br/>                             | <span data-ttu-id="82887-163">Nombre de segments à copier.</span><span class="sxs-lookup"><span data-stu-id="82887-163">The number of chunks to be copied.</span></span> <span data-ttu-id="82887-164">Doit être supérieur à zéro et inférieur ou égal à 256.</span><span class="sxs-lookup"><span data-stu-id="82887-164">Must be greater than zero and less than or equal to 256.</span></span><br/>                                                                                                                                                                                                                                                                |
| <span data-ttu-id="82887-165"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Réservé**</span><span class="sxs-lookup"><span data-stu-id="82887-165"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserved**</span></span><br/>                                     | <span data-ttu-id="82887-166">Ce membre est réservé à l’usage du système ; n’utilisez pas.</span><span class="sxs-lookup"><span data-stu-id="82887-166">This member is reserved for system use; do not use.</span></span><br/>                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="82887-167"><span id="Chunk"></span><span id="chunk"></span><span id="CHUNK"></span>**Transfert**</span><span class="sxs-lookup"><span data-stu-id="82887-167"><span id="Chunk"></span><span id="chunk"></span><span id="CHUNK"></span>**Chunk**</span></span><br/>                                                 | <span data-ttu-id="82887-168">Tableau de structures **ChunkCount** **SRV \_ COPYCHUNK** , un pour chaque segment à copier.</span><span class="sxs-lookup"><span data-stu-id="82887-168">An array of **ChunkCount** **SRV\_COPYCHUNK** structures, one for each chunk to be copied.</span></span> <span data-ttu-id="82887-169">La longueur, en octets, de ce tableau doit être **ChunkCount** \* sizeof (**SRV \_ COPYCHUNK**).</span><span class="sxs-lookup"><span data-stu-id="82887-169">The length, in bytes, of this array must be **ChunkCount** \* sizeof(**SRV\_COPYCHUNK**).</span></span><br/>                                                                                                                                                                       |
| <span data-ttu-id="82887-170"><span id="ChunksWritten"></span><span id="chunkswritten"></span><span id="CHUNKSWRITTEN"></span>**ChunksWritten**</span><span class="sxs-lookup"><span data-stu-id="82887-170"><span id="ChunksWritten"></span><span id="chunkswritten"></span><span id="CHUNKSWRITTEN"></span>**ChunksWritten**</span></span><br/>                 | <span data-ttu-id="82887-171">Si l’opération a échoué avec un **paramètre d’erreur \_ non valide \_**, cette valeur indique le nombre maximal de segments que le serveur acceptera dans une seule requête, qui est 256.</span><span class="sxs-lookup"><span data-stu-id="82887-171">If the operation failed with **ERROR\_INVALID\_PARAMETER**, this value indicates the maximum number of chunks the server will accept in a single request, which is 256.</span></span> <span data-ttu-id="82887-172">Sinon, cette valeur indique le nombre de segments qui ont été écrits avec succès.</span><span class="sxs-lookup"><span data-stu-id="82887-172">Otherwise, this value indicates the number of chunks that were successfully written.</span></span><br/>                                                                                               |
| <span data-ttu-id="82887-173"><span id="ChunkBytesWritten"></span><span id="chunkbyteswritten"></span><span id="CHUNKBYTESWRITTEN"></span>**ChunkBytesWritten**</span><span class="sxs-lookup"><span data-stu-id="82887-173"><span id="ChunkBytesWritten"></span><span id="chunkbyteswritten"></span><span id="CHUNKBYTESWRITTEN"></span>**ChunkBytesWritten**</span></span><br/> | <span data-ttu-id="82887-174">Si l’opération a échoué avec un **paramètre d’erreur \_ non valide \_**, cette valeur indique le nombre maximal d’octets que le serveur autorisera à écrire en un seul segment, soit 1 Mo.</span><span class="sxs-lookup"><span data-stu-id="82887-174">If the operation failed with **ERROR\_INVALID\_PARAMETER**, this value indicates the maximum number of bytes the server will allow to be written in a single chunk, which is 1 MB.</span></span> <span data-ttu-id="82887-175">Sinon, cette valeur indique le nombre d’octets qui ont été correctement écrits dans le dernier segment qui n’a pas été traité avec succès (si une écriture partielle s’est produite).</span><span class="sxs-lookup"><span data-stu-id="82887-175">Otherwise, this value indicates the number of bytes that were successfully written in the last chunk that was not successfully processed (if a partial write occurred).</span></span><br/> |
| <span data-ttu-id="82887-176"><span id="TotalBytesWritten"></span><span id="totalbyteswritten"></span><span id="TOTALBYTESWRITTEN"></span>**TotalBytesWritten**</span><span class="sxs-lookup"><span data-stu-id="82887-176"><span id="TotalBytesWritten"></span><span id="totalbyteswritten"></span><span id="TOTALBYTESWRITTEN"></span>**TotalBytesWritten**</span></span><br/> | <span data-ttu-id="82887-177">Si l’opération a échoué avec un **paramètre d’erreur \_ non valide \_**, cette valeur indique le nombre maximal d’octets que le serveur doit copier dans une seule requête, qui est de 16 Mo.</span><span class="sxs-lookup"><span data-stu-id="82887-177">If the operation failed with **ERROR\_INVALID\_PARAMETER**, this value indicates the maximum number of bytes the server will copy in a single request, which is 16 MB.</span></span> <span data-ttu-id="82887-178">Sinon, cette valeur indique le nombre d’octets qui ont été écrits avec succès.</span><span class="sxs-lookup"><span data-stu-id="82887-178">Otherwise, this value indicates the number of bytes that were successfully written.</span></span><br/>                                                                                                 |



 

## <a name="see-also"></a><span data-ttu-id="82887-179">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="82887-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82887-180">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="82887-180">**DeviceIoControl**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="82887-181">**clé de reprise de la \_ demande FSCTL SRV \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="82887-181">**FSCTL\_SRV\_REQUEST\_RESUME\_KEY**</span></span>](fsctl-srv-request-resume-key.md)
</dt> </dl>

 

 
