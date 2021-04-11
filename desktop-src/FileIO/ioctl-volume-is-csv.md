---
description: Détermine si un volume est un volume partagé de cluster.
ms.assetid: 6B09B519-1E2F-4757-AAD5-1E4C81023E14
title: IOCTL_VOLUME_IS_CSV le code de contrôle (Ntddvol. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_VOLUME_IS_CSV
api_type:
- HeaderDef
api_location:
- Ntddvol.h
ms.openlocfilehash: 8121e1b89c88ad05a2c2be8537d7170bfabfc412
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320393"
---
# <a name="ioctl_volume_is_csv-control-code"></a><span data-ttu-id="28c89-103">\_Le volume IOCTL \_ est \_ le code de contrôle CSV</span><span class="sxs-lookup"><span data-stu-id="28c89-103">IOCTL\_VOLUME\_IS\_CSV control code</span></span>

<span data-ttu-id="28c89-104">Détermine si un volume est un volume partagé de cluster.</span><span class="sxs-lookup"><span data-stu-id="28c89-104">Determines whether a volume is a CSV volume.</span></span>

<span data-ttu-id="28c89-105">Pour effectuer cette opération, appelez la fonction [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="28c89-105">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL 
WINAPI 
DeviceIoControl( (HANDLE) hDevice,              // handle to device
                 IOCTL_VOLUME_IS_CSV,           // dwIoControlCode
                 NULL,                          // input buffer
                 0,                             // size of input buffer
                 (LPVOID) lpOutBuffer,          // lpOutBuffer
                 (DWORD) nOutBufferSize,        // nOutBufferSize
                 (LPDWORD) lpBytesReturned,     // number of bytes returned
                 (LPOVERLAPPED) lpOverlapped ); // OVERLAPPED structure
```



## <a name="parameters"></a><span data-ttu-id="28c89-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="28c89-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28c89-107">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="28c89-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="28c89-108">Handle vers le volume.</span><span class="sxs-lookup"><span data-stu-id="28c89-108">A handle to the volume.</span></span> <span data-ttu-id="28c89-109">Pour récupérer un handle de volume, appelez la fonction [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="28c89-109">To retrieve a volume handle, call the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function.</span></span> <span data-ttu-id="28c89-110">Seuls les administrateurs peuvent ouvrir des descripteurs de volume.</span><span class="sxs-lookup"><span data-stu-id="28c89-110">Only administrators can open volume handles.</span></span>

</dd> <dt>

<span data-ttu-id="28c89-111">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="28c89-111">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="28c89-112">Code de contrôle de l’opération.</span><span class="sxs-lookup"><span data-stu-id="28c89-112">The control code for the operation.</span></span> <span data-ttu-id="28c89-113">L’utilisation du **\_ volume IOCTL \_ est \_ CSV** pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="28c89-113">Use **IOCTL\_VOLUME\_IS\_CSV** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="28c89-114">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="28c89-114">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="28c89-115">Non utilisé avec cette opération ; Affectez la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="28c89-115">Not used with this operation; set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="28c89-116">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="28c89-116">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="28c89-117">Non utilisé avec cette opération ; a la valeur zéro (0).</span><span class="sxs-lookup"><span data-stu-id="28c89-117">Not used with this operation; set to zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="28c89-118">*lpOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="28c89-118">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="28c89-119">Pointeur vers **true** si le volume est un volume partagé de cluster (CSV); dans le cas contraire, l’appel de fonction échoue.</span><span class="sxs-lookup"><span data-stu-id="28c89-119">A pointer to **TRUE** if the volume is a CSV volume; otherwise, the function call fails.</span></span>

</dd> <dt>

<span data-ttu-id="28c89-120">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="28c89-120">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="28c89-121">Taille de la mémoire tampon de sortie en octets.</span><span class="sxs-lookup"><span data-stu-id="28c89-121">The size of the output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="28c89-122">*lpBytesReturned*</span><span class="sxs-lookup"><span data-stu-id="28c89-122">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="28c89-123">Pointeur vers une variable qui reçoit la taille des données stockées dans la mémoire tampon de sortie, en octets.</span><span class="sxs-lookup"><span data-stu-id="28c89-123">A pointer to a variable that receives the size of the data stored in the output buffer, in bytes.</span></span>

<span data-ttu-id="28c89-124">Si *lpOverlapped* a la **valeur null**, *lpBytesReturned* ne peut pas avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="28c89-124">If *lpOverlapped* is **NULL**, *lpBytesReturned* cannot be **NULL**.</span></span> <span data-ttu-id="28c89-125">Même lorsqu’une opération ne retourne aucune donnée de sortie et que *lpOutBuffer* a la **valeur null**, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) utilise *lpBytesReturned*.</span><span class="sxs-lookup"><span data-stu-id="28c89-125">Even when an operation returns no output data and *lpOutBuffer* is **NULL**, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) makes use of *lpBytesReturned*.</span></span> <span data-ttu-id="28c89-126">Après une telle opération, la valeur de *lpBytesReturned* est sans signification.</span><span class="sxs-lookup"><span data-stu-id="28c89-126">After such an operation, the value of *lpBytesReturned* is meaningless.</span></span>

<span data-ttu-id="28c89-127">Si *lpOverlapped* n’a pas la **valeur null**, *LpBytesReturned* peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="28c89-127">If *lpOverlapped* is not **NULL**, *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="28c89-128">Si ce paramètre n’est pas **null** et que l’opération retourne des données, *lpBytesReturned* n’a pas de sens tant que l’opération avec chevauchement n’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="28c89-128">If this parameter is not **NULL** and the operation returns data, *lpBytesReturned* is meaningless until the overlapped operation has completed.</span></span> <span data-ttu-id="28c89-129">Pour récupérer le nombre d’octets retournés, appelez [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult).</span><span class="sxs-lookup"><span data-stu-id="28c89-129">To retrieve the number of bytes returned, call [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult).</span></span> <span data-ttu-id="28c89-130">Si *hDevice* est associé à un port de terminaison d’e/s, vous pouvez récupérer le nombre d’octets retournés en appelant [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus).</span><span class="sxs-lookup"><span data-stu-id="28c89-130">If *hDevice* is associated with an I/O completion port, you can retrieve the number of bytes returned by calling [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus).</span></span>

</dd> <dt>

<span data-ttu-id="28c89-131">*lpOverlapped*</span><span class="sxs-lookup"><span data-stu-id="28c89-131">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="28c89-132">Pointeur vers une structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="28c89-132">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="28c89-133">Si *hDevice* a été ouvert sans spécifier d' **indicateur de fichier avec \_ \_ chevauchement**, *lpOverlapped* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="28c89-133">If *hDevice* was opened without specifying **FILE\_FLAG\_OVERLAPPED**, *lpOverlapped* is ignored.</span></span>

<span data-ttu-id="28c89-134">Si *hDevice* a été ouvert avec l’indicateur de fichier avec l' **indicateur de \_ \_ chevauchement** , l’opération est exécutée en tant qu’opération Overlapped (asynchrone).</span><span class="sxs-lookup"><span data-stu-id="28c89-134">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="28c89-135">Dans ce cas, *lpOverlapped* doit pointer vers une structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) valide qui contient un handle vers un objet d’événement.</span><span class="sxs-lookup"><span data-stu-id="28c89-135">In this case, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure that contains a handle to an event object.</span></span> <span data-ttu-id="28c89-136">Dans le cas contraire, la fonction échoue de façon imprévisible.</span><span class="sxs-lookup"><span data-stu-id="28c89-136">Otherwise, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="28c89-137">Pour les opérations avec chevauchement, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne immédiatement, et l’objet d’événement est signalé lorsque l’opération est terminée.</span><span class="sxs-lookup"><span data-stu-id="28c89-137">For overlapped operations, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns immediately, and the event object is signaled when the operation has been completed.</span></span> <span data-ttu-id="28c89-138">Sinon, la fonction ne retourne pas jusqu’à ce que l’opération soit terminée ou qu’une erreur se produise.</span><span class="sxs-lookup"><span data-stu-id="28c89-138">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28c89-139">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="28c89-139">Return value</span></span>

<span data-ttu-id="28c89-140">Si l’opération se termine correctement, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="28c89-140">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="28c89-141">Si l’opération échoue ou est en attente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne la valeur zéro (0).</span><span class="sxs-lookup"><span data-stu-id="28c89-141">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero (0).</span></span> <span data-ttu-id="28c89-142">Pour obtenir des informations détaillées sur l’erreur, appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="28c89-142">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="28c89-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="28c89-143">Requirements</span></span>



| <span data-ttu-id="28c89-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="28c89-144">Requirement</span></span> | <span data-ttu-id="28c89-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="28c89-145">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="28c89-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="28c89-146">Minimum supported client</span></span><br/> | <span data-ttu-id="28c89-147">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="28c89-147">None supported</span></span><br/>                                                            |
| <span data-ttu-id="28c89-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="28c89-148">Minimum supported server</span></span><br/> | <span data-ttu-id="28c89-149">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="28c89-149">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="28c89-150">En-tête</span><span class="sxs-lookup"><span data-stu-id="28c89-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="28c89-151"><dt>Ntddvol. h</dt></span><span class="sxs-lookup"><span data-stu-id="28c89-151"><dt>Ntddvol.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28c89-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="28c89-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28c89-153">**CreateFile**</span><span class="sxs-lookup"><span data-stu-id="28c89-153">**CreateFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[<span data-ttu-id="28c89-154">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="28c89-154">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="28c89-155">Codes de contrôle de gestion des volumes</span><span class="sxs-lookup"><span data-stu-id="28c89-155">Volume Management Control Codes</span></span>](volume-management-control-codes.md)
</dt> </dl>

 

