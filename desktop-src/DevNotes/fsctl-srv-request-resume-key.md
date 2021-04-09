---
description: Le code de contrôle de la \_ \_ clé de reprise de la demande FSCTL SRV \_ \_ est utilisé pour récupérer une référence de fichier opaque à utiliser avec le \_ Code de contrôle IOCTL COPYCHUNK.
ms.assetid: a6e0d253-5beb-4de8-8c40-d004f5794d47
title: Code de contrôle FSCTL_SRV_REQUEST_RESUME_KEY
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FSCTL_SRV_REQUEST_RESUME_KEY
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8f11b70f7b4bfd05cbd5f7c29323f1dca00083a4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860661"
---
# <a name="fsctl_srv_request_resume_key-control-code"></a><span data-ttu-id="3739c-103">Code de contrôle de la clé de reprise de la \_ demande FSCTL SRV \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="3739c-103">FSCTL\_SRV\_REQUEST\_RESUME\_KEY control code</span></span>

<span data-ttu-id="3739c-104">Le code de contrôle de la clé de reprise de la **\_ \_ demande \_ \_ FSCTL SRV** est utilisé pour récupérer une référence de fichier opaque à utiliser avec le code de contrôle [**IOCTL \_ COPYCHUNK**](ioctl-copychunk.md) .</span><span class="sxs-lookup"><span data-stu-id="3739c-104">The **FSCTL\_SRV\_REQUEST\_RESUME\_KEY** control code is used to retrieve an opaque file reference for use with the [**IOCTL\_COPYCHUNK**](ioctl-copychunk.md) control code.</span></span>

<span data-ttu-id="3739c-105">Pour effectuer cette opération, appelez la fonction [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="3739c-105">To perform this operation, call the [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  FSCTL_SRV_REQUEST_RESUME_KEY, // dwIoControlCode
  NULL,                         // lpInBuffer
  0,                            // nInBufferSize
  (LPVOID) lpOutBuffer,         // output buffer
  (DWORD) nOutBufferSize,       // size of output buffer
  (LPDWORD) lpBytesReturned,    // number of bytes returned
  (LPOVERLAPPED) lpOverlapped   // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="3739c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3739c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3739c-107">*hDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3739c-107">*hDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3739c-108">Handle du fichier pour lequel la clé du fichier source doit être demandée.</span><span class="sxs-lookup"><span data-stu-id="3739c-108">A handle to the file for which the source file key is to be requested.</span></span> <span data-ttu-id="3739c-109">Pour obtenir ce descripteur, appelez la fonction [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="3739c-109">To obtain this handle, call the [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="3739c-110">*dwIoControlCode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3739c-110">*dwIoControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3739c-111">Code de contrôle de l’opération.</span><span class="sxs-lookup"><span data-stu-id="3739c-111">The control code for the operation.</span></span> <span data-ttu-id="3739c-112">Utilisez **la \_ \_ clé de \_ reprise \_ de la demande FSCTL SRV** pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="3739c-112">Use **FSCTL\_SRV\_REQUEST\_RESUME\_KEY** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="3739c-113">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="3739c-113">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="3739c-114">Non utilisé avec cette opération ; Affectez la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="3739c-114">Not used with this operation; set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="3739c-115">*nInBufferSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3739c-115">*nInBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3739c-116">Non utilisé avec cette opération ; défini à zéro.</span><span class="sxs-lookup"><span data-stu-id="3739c-116">Not used with this operation; set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="3739c-117">*lpOutBuffer* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3739c-117">*lpOutBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3739c-118">Pointeur vers la mémoire tampon de sortie, une structure de **\_ clé de \_ reprise \_ de demande SRV** .</span><span class="sxs-lookup"><span data-stu-id="3739c-118">A pointer to the output buffer, a **SRV\_REQUEST\_RESUME\_KEY** structure.</span></span> <span data-ttu-id="3739c-119">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="3739c-119">For more information, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="3739c-120">*nOutBufferSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3739c-120">*nOutBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3739c-121">Taille de la mémoire tampon de sortie en octets.</span><span class="sxs-lookup"><span data-stu-id="3739c-121">The size of the output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="3739c-122">*lpBytesReturned* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3739c-122">*lpBytesReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3739c-123">Pointeur vers une variable qui reçoit la taille des données stockées dans la mémoire tampon de sortie, en octets.</span><span class="sxs-lookup"><span data-stu-id="3739c-123">A pointer to a variable that receives the size of the data stored in the output buffer, in bytes.</span></span>

<span data-ttu-id="3739c-124">Si la mémoire tampon de sortie est trop petite, l’appel échoue, la fonction [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne l' **erreur \_ \_ mémoire tampon insuffisante** et *lpBytesReturned* est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="3739c-124">If the output buffer is too small, the call fails, the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns **ERROR\_INSUFFICIENT\_BUFFER**, and *lpBytesReturned* is zero.</span></span>

<span data-ttu-id="3739c-125">Si le paramètre *lpOverlapped* a la **valeur null**, *lpBytesReturned* ne peut pas avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="3739c-125">If the *lpOverlapped* parameter is **NULL**, *lpBytesReturned* cannot be **NULL**.</span></span> <span data-ttu-id="3739c-126">Même lorsqu’une opération ne retourne aucune donnée de sortie et que le paramètre *lpOutBuffer* a la **valeur null**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) utilise *lpBytesReturned*.</span><span class="sxs-lookup"><span data-stu-id="3739c-126">Even when an operation returns no output data and the *lpOutBuffer* parameter is **NULL**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) makes use of *lpBytesReturned*.</span></span> <span data-ttu-id="3739c-127">Après une telle opération, la valeur de *lpBytesReturned* est sans signification.</span><span class="sxs-lookup"><span data-stu-id="3739c-127">After such an operation, the value of *lpBytesReturned* is meaningless.</span></span>

<span data-ttu-id="3739c-128">Si *lpOverlapped* n’a pas la **valeur null**, *LpBytesReturned* peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="3739c-128">If *lpOverlapped* is not **NULL**, *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="3739c-129">Si *lpOverlapped* n’a pas la **valeur null** et que l’opération retourne des données, *lpBytesReturned* n’a aucun sens tant que l’opération avec chevauchement n’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="3739c-129">If *lpOverlapped* is not **NULL** and the operation returns data, *lpBytesReturned* is meaningless until the overlapped operation has completed.</span></span> <span data-ttu-id="3739c-130">Pour récupérer le nombre d’octets retournés, appelez la fonction [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) .</span><span class="sxs-lookup"><span data-stu-id="3739c-130">To retrieve the number of bytes returned, call the [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="3739c-131">Si le paramètre *hDevice* est associé à un port de terminaison d’e/s, vous pouvez récupérer le nombre d’octets renvoyés en appelant la fonction [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="3739c-131">If the *hDevice* parameter is associated with an I/O completion port, you can retrieve the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="3739c-132">*lpOverlapped* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3739c-132">*lpOverlapped* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3739c-133">Pointeur vers une structure [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="3739c-133">A pointer to an [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="3739c-134">Si le paramètre *hDevice* a été ouvert sans spécifier d' **indicateur de fichier avec \_ \_ chevauchement**, *lpOverlapped* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="3739c-134">If the *hDevice* parameter was opened without specifying **FILE\_FLAG\_OVERLAPPED**, *lpOverlapped* is ignored.</span></span>

<span data-ttu-id="3739c-135">Si *hDevice* a été ouvert avec l’indicateur de fichier avec l' **indicateur de \_ \_ chevauchement** , l’opération est exécutée en tant qu’opération Overlapped (asynchrone).</span><span class="sxs-lookup"><span data-stu-id="3739c-135">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="3739c-136">Dans ce cas, *lpOverlapped* doit pointer vers une structure [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) valide qui contient un handle vers un objet d’événement.</span><span class="sxs-lookup"><span data-stu-id="3739c-136">In this case, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure that contains a handle to an event object.</span></span> <span data-ttu-id="3739c-137">Dans le cas contraire, la fonction échoue de façon imprévisible.</span><span class="sxs-lookup"><span data-stu-id="3739c-137">Otherwise, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="3739c-138">Pour les opérations avec chevauchement, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne immédiatement, et l’objet d’événement est signalé lorsque l’opération est terminée.</span><span class="sxs-lookup"><span data-stu-id="3739c-138">For overlapped operations, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns immediately, and the event object is signaled when the operation has been completed.</span></span> <span data-ttu-id="3739c-139">Sinon, la fonction ne retourne pas jusqu’à ce que l’opération soit terminée ou jusqu’à ce qu’une erreur se produise.</span><span class="sxs-lookup"><span data-stu-id="3739c-139">Otherwise, the function does not return until the operation has been completed or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3739c-140">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3739c-140">Return value</span></span>

<span data-ttu-id="3739c-141">Si l’opération se termine correctement, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="3739c-141">If the operation completes successfully, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="3739c-142">Si l’opération échoue ou est en attente, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="3739c-142">If the operation fails or is pending, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="3739c-143">Pour obtenir des informations détaillées sur l’erreur, appelez [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="3739c-143">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="3739c-144">Remarques</span><span class="sxs-lookup"><span data-stu-id="3739c-144">Remarks</span></span>

<span data-ttu-id="3739c-145">Ce code de contrôle n’a aucun fichier d’en-tête associé.</span><span class="sxs-lookup"><span data-stu-id="3739c-145">This control code has no associated header file.</span></span> <span data-ttu-id="3739c-146">Vous devez définir le code de contrôle et les structures de données comme suit.</span><span class="sxs-lookup"><span data-stu-id="3739c-146">You must define the control code and data structures as follows.</span></span>

``` syntax
#define FSCTL_SRV_REQUEST_RESUME_KEY CTL_CODE(FILE_DEVICE_NETWORK_FILE_SYSTEM, 30, METHOD_BUFFERED, FILE_ANY_ACCESS)

typedef struct _SRV_RESUME_KEY {
    UINT64 ResumeKey;
    UINT64 Timestamp;
    UINT64 Pid;
} SRV_RESUME_KEY, *PSRV_RESUME_KEY;

typedef struct _SRV_REQUEST_RESUME_KEY {
    SRV_RESUME_KEY Key;
    ULONG  ContextLength;
    BYTE   Context[1];
} SRV_REQUEST_RESUME_KEY, *PSRV_REQUEST_RESUME_KEY;
```

<span data-ttu-id="3739c-147">Ces membres peuvent être décrits comme suit.</span><span class="sxs-lookup"><span data-stu-id="3739c-147">These members can be described as follows.</span></span>



| <span data-ttu-id="3739c-148">Membre</span><span class="sxs-lookup"><span data-stu-id="3739c-148">Member</span></span>                                                                                                                       | <span data-ttu-id="3739c-149">Description</span><span class="sxs-lookup"><span data-stu-id="3739c-149">Description</span></span>                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3739c-150"><span id="ResumeKey"></span><span id="resumekey"></span><span id="RESUMEKEY"></span>**ResumeKey**</span><span class="sxs-lookup"><span data-stu-id="3739c-150"><span id="ResumeKey"></span><span id="resumekey"></span><span id="RESUMEKEY"></span>**ResumeKey**</span></span><br/>                 | <span data-ttu-id="3739c-151">Valeur opaque qui identifie le fichier source sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="3739c-151">An opaque value that identifies the source file to the server.</span></span><br/>                                                                                                   |
| <span data-ttu-id="3739c-152"><span id="Timestamp"></span><span id="timestamp"></span><span id="TIMESTAMP"></span>**Confirmé**</span><span class="sxs-lookup"><span data-stu-id="3739c-152"><span id="Timestamp"></span><span id="timestamp"></span><span id="TIMESTAMP"></span>**Timestamp**</span></span><br/>                 | <span data-ttu-id="3739c-153">Valeur opaque qui identifie l’heure à laquelle le fichier a été ouvert.</span><span class="sxs-lookup"><span data-stu-id="3739c-153">An opaque value that identifies the time when the file was opened.</span></span><br/>                                                                                               |
| <span data-ttu-id="3739c-154"><span id="Pid"></span><span id="pid"></span><span id="PID"></span>**ELECTRIQUE**</span><span class="sxs-lookup"><span data-stu-id="3739c-154"><span id="Pid"></span><span id="pid"></span><span id="PID"></span>**Pid**</span></span><br/>                                         | <span data-ttu-id="3739c-155">Valeur opaque qui identifie le processus qui a ouvert le fichier.</span><span class="sxs-lookup"><span data-stu-id="3739c-155">An opaque value that identifies the process that opened the file.</span></span><br/>                                                                                                |
| <span data-ttu-id="3739c-156"><span id="Key"></span><span id="key"></span><span id="KEY"></span>**Essentiel**</span><span class="sxs-lookup"><span data-stu-id="3739c-156"><span id="Key"></span><span id="key"></span><span id="KEY"></span>**Key**</span></span><br/>                                         | <span data-ttu-id="3739c-157">Structure **de \_ \_ clé de reprise SRV** .</span><span class="sxs-lookup"><span data-stu-id="3739c-157">A **SRV\_RESUME\_KEY** structure.</span></span> <span data-ttu-id="3739c-158">Pour effectuer une opération de copie côté serveur, utilisez cette structure avec le code de contrôle [**IOCTL \_ COPYCHUNK**](ioctl-copychunk.md) .</span><span class="sxs-lookup"><span data-stu-id="3739c-158">To perform a server-side copy operation, use this structure with the [**IOCTL\_COPYCHUNK**](ioctl-copychunk.md) control code.</span></span><br/> |
| <span data-ttu-id="3739c-159"><span id="ContextLength"></span><span id="contextlength"></span><span id="CONTEXTLENGTH"></span>**ContextLength**</span><span class="sxs-lookup"><span data-stu-id="3739c-159"><span id="ContextLength"></span><span id="contextlength"></span><span id="CONTEXTLENGTH"></span>**ContextLength**</span></span><br/> | <span data-ttu-id="3739c-160">Ce membre est réservé à l’usage du système ; n’utilisez pas.</span><span class="sxs-lookup"><span data-stu-id="3739c-160">This member is reserved for system use; do not use.</span></span><br/>                                                                                                              |
| <span data-ttu-id="3739c-161"><span id="Context"></span><span id="context"></span><span id="CONTEXT"></span>**Contexte**</span><span class="sxs-lookup"><span data-stu-id="3739c-161"><span id="Context"></span><span id="context"></span><span id="CONTEXT"></span>**Context**</span></span><br/>                         | <span data-ttu-id="3739c-162">Ce membre est réservé à l’usage du système ; n’utilisez pas.</span><span class="sxs-lookup"><span data-stu-id="3739c-162">This member is reserved for system use; do not use.</span></span><br/>                                                                                                              |



 

## <a name="see-also"></a><span data-ttu-id="3739c-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3739c-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3739c-164">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="3739c-164">**DeviceIoControl**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="3739c-165">**\_COPYCHUNK IOCTL**</span><span class="sxs-lookup"><span data-stu-id="3739c-165">**IOCTL\_COPYCHUNK**</span></span>](ioctl-copychunk.md)
</dt> </dl>

 

 
