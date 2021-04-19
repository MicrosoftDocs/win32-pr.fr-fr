---
description: Le code de contrôle de mise en \_ \_ \_ mémoire tampon locale d’IOCTL LMR désactive \_ la mise en cache en mémoire côté client locale des données lors de la lecture ou de l’écriture de données dans un fichier distant. Il s’agit d’un code de contrôle défini en interne qui n’est pas disponible dans un en-tête public.
ms.assetid: a464671b-253c-4f35-84a2-2619cb15b009
title: Code de contrôle IOCTL_LMR_DISABLE_LOCAL_BUFFERING
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
ms.openlocfilehash: 0d596402c489caee972e1305f2a32881312fd3e0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106532069"
---
# <a name="ioctl_lmr_disable_local_buffering-control-code"></a><span data-ttu-id="cd63b-104">\_LMR IOCTL \_ désactiver \_ \_ le code de contrôle de mise en mémoire tampon locale</span><span class="sxs-lookup"><span data-stu-id="cd63b-104">IOCTL\_LMR\_DISABLE\_LOCAL\_BUFFERING control code</span></span>

<span data-ttu-id="cd63b-105">Le code de contrôle de mise en **\_ \_ \_ \_ mémoire tampon locale d’IOCTL LMR** désactive la mise en cache en mémoire côté client locale des données lors de la lecture ou de l’écriture de données dans un fichier distant.</span><span class="sxs-lookup"><span data-stu-id="cd63b-105">The **IOCTL\_LMR\_DISABLE\_LOCAL\_BUFFERING** control code disables local client-side in-memory caching of data when reading data from or writing data to a remote file.</span></span> <span data-ttu-id="cd63b-106">Il s’agit d’un code de contrôle défini en interne qui n’est pas disponible dans un en-tête public.</span><span class="sxs-lookup"><span data-stu-id="cd63b-106">This is an internally-defined control code not available in a public header.</span></span>

<span data-ttu-id="cd63b-107">Pour effectuer cette opération, appelez la fonction [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="cd63b-107">To perform this operation, call the [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  IOCTL_LMR_DISABLE_LOCAL_BUFFERING, // dwIoControlCode
  (LPVOID) NULL,                // lpInBuffer
  (DWORD) 0,                    // nInBufferSize
  (LPVOID) NULL,                // lpOutBuffer
  (DWORD) 0,                    // nOutBufferSize
  (LPDWORD) lpBytesReturned,    // number of bytes returned
  (LPOVERLAPPED) lpOverlapped   // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="cd63b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cd63b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd63b-109">*hDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cd63b-109">*hDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd63b-110">Handle du fichier distant.</span><span class="sxs-lookup"><span data-stu-id="cd63b-110">A handle to the remote file.</span></span> <span data-ttu-id="cd63b-111">Pour obtenir ce descripteur, appelez la fonction [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="cd63b-111">To obtain this handle, call the [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="cd63b-112">*dwIoControlCode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cd63b-112">*dwIoControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd63b-113">Code de contrôle de l’opération.</span><span class="sxs-lookup"><span data-stu-id="cd63b-113">The control code for the operation.</span></span> <span data-ttu-id="cd63b-114">Utilisez la valeur 0x140390 pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="cd63b-114">Use the value 0x140390 for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="cd63b-115">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="cd63b-115">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="cd63b-116">Non utilisé, doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="cd63b-116">Not used, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="cd63b-117">*nInBufferSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cd63b-117">*nInBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd63b-118">Taille de la mémoire tampon d’entrée, en octets.</span><span class="sxs-lookup"><span data-stu-id="cd63b-118">The size of the input buffer, in bytes.</span></span> <span data-ttu-id="cd63b-119">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="cd63b-119">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="cd63b-120">*lpOutBuffer* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="cd63b-120">*lpOutBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd63b-121">Non utilisé, doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="cd63b-121">Not used, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="cd63b-122">*nOutBufferSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cd63b-122">*nOutBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd63b-123">Taille de la mémoire tampon de sortie en octets.</span><span class="sxs-lookup"><span data-stu-id="cd63b-123">The size of the output buffer, in bytes.</span></span> <span data-ttu-id="cd63b-124">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="cd63b-124">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="cd63b-125">*lpBytesReturned* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="cd63b-125">*lpBytesReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd63b-126">Pointeur vers une variable qui reçoit la taille des données stockées dans la mémoire tampon de sortie, en octets.</span><span class="sxs-lookup"><span data-stu-id="cd63b-126">A pointer to a variable that receives the size of the data stored in the output buffer, in bytes.</span></span>

<span data-ttu-id="cd63b-127">Si la mémoire tampon de sortie est trop petite, l’appel échoue, la fonction [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne l' **erreur \_ \_ mémoire tampon insuffisante** et *lpBytesReturned* est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="cd63b-127">If the output buffer is too small, then the call fails, the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns **ERROR\_INSUFFICIENT\_BUFFER**, and *lpBytesReturned* is zero.</span></span>

<span data-ttu-id="cd63b-128">Si le paramètre *lpOverlapped* a la **valeur null**, *lpBytesReturned* ne peut pas avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="cd63b-128">If the *lpOverlapped* parameter is **NULL**, *lpBytesReturned* cannot be **NULL**.</span></span> <span data-ttu-id="cd63b-129">Même lorsqu’une opération ne retourne aucune donnée de sortie et que le paramètre *lpOutBuffer* a la **valeur null**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) utilise *lpBytesReturned*.</span><span class="sxs-lookup"><span data-stu-id="cd63b-129">Even when an operation returns no output data and the *lpOutBuffer* parameter is **NULL**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) makes use of *lpBytesReturned*.</span></span> <span data-ttu-id="cd63b-130">Après une telle opération, la valeur de *lpBytesReturned* est sans signification.</span><span class="sxs-lookup"><span data-stu-id="cd63b-130">After such an operation, the value of *lpBytesReturned* is meaningless.</span></span>

<span data-ttu-id="cd63b-131">Si *lpOverlapped* n’a pas la **valeur null**, *LpBytesReturned* peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="cd63b-131">If *lpOverlapped* is not **NULL**, *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="cd63b-132">Si *lpOverlapped* n’a pas la **valeur null** et que l’opération retourne des données, *lpBytesReturned* n’a aucun sens tant que l’opération avec chevauchement n’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="cd63b-132">If *lpOverlapped* is not **NULL** and the operation returns data, *lpBytesReturned* is meaningless until the overlapped operation has completed.</span></span> <span data-ttu-id="cd63b-133">Pour récupérer le nombre d’octets retournés, appelez la fonction [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) .</span><span class="sxs-lookup"><span data-stu-id="cd63b-133">To retrieve the number of bytes returned, call the [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="cd63b-134">Si le paramètre *hDevice* est associé à un port de terminaison d’e/s, vous pouvez récupérer le nombre d’octets renvoyés en appelant la fonction [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="cd63b-134">If the *hDevice* parameter is associated with an I/O completion port, you can retrieve the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="cd63b-135">*lpOverlapped* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cd63b-135">*lpOverlapped* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd63b-136">Pointeur vers une structure [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="cd63b-136">A pointer to an [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="cd63b-137">Si le paramètre *hDevice* a été ouvert sans spécifier d' **indicateur de fichier avec \_ \_ chevauchement**, *lpOverlapped* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="cd63b-137">If the *hDevice* parameter was opened without specifying **FILE\_FLAG\_OVERLAPPED**, *lpOverlapped* is ignored.</span></span>

<span data-ttu-id="cd63b-138">Si *hDevice* a été ouvert avec l’indicateur de fichier avec l' **indicateur de \_ \_ chevauchement** , l’opération est exécutée en tant qu’opération Overlapped (asynchrone).</span><span class="sxs-lookup"><span data-stu-id="cd63b-138">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="cd63b-139">Dans ce cas, *lpOverlapped* doit pointer vers une structure [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) valide qui contient un handle vers un objet d’événement.</span><span class="sxs-lookup"><span data-stu-id="cd63b-139">In this case, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure that contains a handle to an event object.</span></span> <span data-ttu-id="cd63b-140">Dans le cas contraire, la fonction échoue de façon imprévisible.</span><span class="sxs-lookup"><span data-stu-id="cd63b-140">Otherwise, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="cd63b-141">Pour les opérations avec chevauchement, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne immédiatement, et l’objet d’événement est signalé lorsque l’opération est terminée.</span><span class="sxs-lookup"><span data-stu-id="cd63b-141">For overlapped operations, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns immediately, and the event object is signaled when the operation has been completed.</span></span> <span data-ttu-id="cd63b-142">Sinon, la fonction ne retourne pas jusqu’à ce que l’opération soit terminée ou jusqu’à ce qu’une erreur se produise.</span><span class="sxs-lookup"><span data-stu-id="cd63b-142">Otherwise, the function does not return until the operation has been completed or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd63b-143">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cd63b-143">Return value</span></span>

<span data-ttu-id="cd63b-144">Si l’opération se termine correctement, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="cd63b-144">If the operation completes successfully, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="cd63b-145">Si l’opération échoue ou est en attente, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="cd63b-145">If the operation fails or is pending, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="cd63b-146">Pour obtenir des informations détaillées sur l’erreur, appelez [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="cd63b-146">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="cd63b-147">Remarques</span><span class="sxs-lookup"><span data-stu-id="cd63b-147">Remarks</span></span>

<span data-ttu-id="cd63b-148">Le code de contrôle de **\_ mise en \_ \_ \_ mémoire tampon locale d’IOCTL LMR** est défini en interne par le système en tant que 0x140390 et non dans un fichier d’en-tête public.</span><span class="sxs-lookup"><span data-stu-id="cd63b-148">The **IOCTL\_LMR\_DISABLE\_LOCAL\_BUFFERING** control code is defined internally by the system as 0x140390 and not in a public header file.</span></span> <span data-ttu-id="cd63b-149">Il est utilisé par les applications à usage spécifique pour désactiver la mise en cache en mémoire côté client locale des données lors de la lecture ou de l’écriture de données dans un fichier distant.</span><span class="sxs-lookup"><span data-stu-id="cd63b-149">It is used by special-purpose applications to disable local client-side in-memory caching of data when reading data from or writing data to a remote file.</span></span> <span data-ttu-id="cd63b-150">Une fois la mise en mémoire tampon locale désactivée, le paramètre reste en vigueur jusqu’à la fermeture de tous les descripteurs ouverts du fichier et le redirecteur nettoie ses structures de données internes.</span><span class="sxs-lookup"><span data-stu-id="cd63b-150">After local buffering is disabled, the setting remains in effect until all open handles to the file are closed and the redirector cleans up its internal data structures.</span></span>

<span data-ttu-id="cd63b-151">Les applications à usage général ne doivent pas utiliser les **\_ LMR IOCTL \_ désactivent la \_ mise en \_ mémoire tampon locale**, car cela peut entraîner un trafic réseau excessif et une perte de performances.</span><span class="sxs-lookup"><span data-stu-id="cd63b-151">General-purpose applications should not use **IOCTL\_LMR\_DISABLE\_LOCAL\_BUFFERING**, because it can result in excessive network traffic and associated loss of performance.</span></span> <span data-ttu-id="cd63b-152">Le code de contrôle de **\_ mise en \_ \_ \_ mémoire tampon locale d’IOCTL LMR** doit être utilisé uniquement dans les applications spécialisées qui déplacent de grandes quantités de données sur le réseau tout en tentant d’optimiser l’utilisation de la bande passante réseau.</span><span class="sxs-lookup"><span data-stu-id="cd63b-152">The **IOCTL\_LMR\_DISABLE\_LOCAL\_BUFFERING** control code should be used only in specialized applications moving large amounts of data over the network while attempting to maximize use of network bandwidth.</span></span> <span data-ttu-id="cd63b-153">Par exemple, les fonctions [**CopyFile**](/windows/win32/api/winbase/nf-winbase-copyfile) et [**CopyFileEx**](/windows/win32/api/winbase/nf-winbase-copyfileexa) utilisent **les \_ LMR IOCTL \_ désactivent la \_ mise en \_ mémoire tampon locale** pour améliorer les performances de copie de fichiers volumineux.</span><span class="sxs-lookup"><span data-stu-id="cd63b-153">For example, the [**CopyFile**](/windows/win32/api/winbase/nf-winbase-copyfile) and [**CopyFileEx**](/windows/win32/api/winbase/nf-winbase-copyfileexa) functions use **IOCTL\_LMR\_DISABLE\_LOCAL\_BUFFERING** to improve large file copy performance.</span></span>

<span data-ttu-id="cd63b-154">**IOCTL \_ La \_ désactivation de la \_ \_ mise en mémoire tampon locale LMR** n’est pas implémentée par les systèmes de fichiers locaux et échoue avec la fonction erreur erreur **\_ non valide \_**.</span><span class="sxs-lookup"><span data-stu-id="cd63b-154">**IOCTL\_LMR\_DISABLE\_LOCAL\_BUFFERING** is not implemented by local file systems and will fail with the error **ERROR\_INVALID\_FUNCTION**.</span></span> <span data-ttu-id="cd63b-155">L’émission du code de contrôle de **\_ mise en \_ \_ \_ mémoire tampon locale d’IOCTL LMR** sur les handles de répertoires distants échouera avec l’erreur erreur **\_ non \_ prise en charge**.</span><span class="sxs-lookup"><span data-stu-id="cd63b-155">Issuing the **IOCTL\_LMR\_DISABLE\_LOCAL\_BUFFERING** control code on remote directory handles will fail with the error **ERROR\_NOT\_SUPPORTED**.</span></span>

## <a name="see-also"></a><span data-ttu-id="cd63b-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cd63b-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd63b-157">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="cd63b-157">**DeviceIoControl**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> </dl>

 

 
