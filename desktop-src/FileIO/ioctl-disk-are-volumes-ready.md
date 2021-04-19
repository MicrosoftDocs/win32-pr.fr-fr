---
description: Attend que tous les volumes du disque spécifié soient prêts à être utilisés.
ms.assetid: 6cf619bb-7ff5-485e-b533-0f7f6503c6e0
title: IOCTL_DISK_ARE_VOLUMES_READY le code de contrôle (NTDDDISK. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_DISK_ARE_VOLUMES_READY
api_type:
- HeaderDef
api_location:
- ntdddisk.h
ms.openlocfilehash: dc4457af2ce6e7759ef879900803504933a09978
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541978"
---
# <a name="ioctl_disk_are_volumes_ready-control-code"></a><span data-ttu-id="54735-103">\_Le disque IOCTL \_ est un code de \_ \_ contrôle prêt pour les volumes</span><span class="sxs-lookup"><span data-stu-id="54735-103">IOCTL\_DISK\_ARE\_VOLUMES\_READY control code</span></span>

<span data-ttu-id="54735-104">Attend que tous les volumes du disque spécifié soient prêts à être utilisés.</span><span class="sxs-lookup"><span data-stu-id="54735-104">Waits for all volumes on the specified disk to be ready for use.</span></span>

<span data-ttu-id="54735-105">Pour effectuer cette opération, appelez la fonction [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="54735-105">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL 
WINAPI 
DeviceIoControl( (HANDLE)       hDevice,         // handle to device 
                 IOCTL_DISK_ARE_VOLUMES_READY,   // dwIoControlCode
                 (LPVOID)       NULL,            // lpInBuffer 
                 (DWORD)        0,               // nInBufferSize 
                 (LPVOID)       NULL,            // lpOutBuffer 
                 (DWORD)        0,               // nOutBufferSize
                 (LPDWORD)      lpBytesReturned, // number of bytes returned
                 (LPOVERLAPPED) lpOverlapped );  // OVERLAPPED structure
```



## <a name="parameters"></a><span data-ttu-id="54735-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="54735-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54735-107">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="54735-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="54735-108">Handle sur le disque.</span><span class="sxs-lookup"><span data-stu-id="54735-108">A handle to the disk.</span></span>

<span data-ttu-id="54735-109">Pour récupérer un handle d’appareil, appelez la fonction [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="54735-109">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="54735-110">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="54735-110">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="54735-111">Code de contrôle de l’opération.</span><span class="sxs-lookup"><span data-stu-id="54735-111">The control code for the operation.</span></span>

<span data-ttu-id="54735-112">Utilisez **le \_ disque IOCTL \_ les \_ volumes sont \_ prêts** pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="54735-112">Use **IOCTL\_DISK\_ARE\_VOLUMES\_READY** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="54735-113">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="54735-113">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="54735-114">Non utilisé avec cette opération.</span><span class="sxs-lookup"><span data-stu-id="54735-114">Not used with this operation.</span></span> <span data-ttu-id="54735-115">Affectez la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="54735-115">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="54735-116">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="54735-116">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="54735-117">Taille de la mémoire tampon d’entrée, en octets.</span><span class="sxs-lookup"><span data-stu-id="54735-117">The size of the input buffer, in bytes.</span></span> <span data-ttu-id="54735-118">Défini sur 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="54735-118">Set to 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="54735-119">*lpOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="54735-119">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="54735-120">Non utilisé avec cette opération.</span><span class="sxs-lookup"><span data-stu-id="54735-120">Not used with this operation.</span></span> <span data-ttu-id="54735-121">Affectez la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="54735-121">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="54735-122">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="54735-122">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="54735-123">Non utilisé avec cette opération.</span><span class="sxs-lookup"><span data-stu-id="54735-123">Not used with this operation.</span></span> <span data-ttu-id="54735-124">Défini sur 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="54735-124">Set to 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="54735-125">*lpBytesReturned*</span><span class="sxs-lookup"><span data-stu-id="54735-125">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="54735-126">Non utilisé avec cette opération.</span><span class="sxs-lookup"><span data-stu-id="54735-126">Not used with this operation.</span></span> <span data-ttu-id="54735-127">Affectez la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="54735-127">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="54735-128">*lpOverlapped*</span><span class="sxs-lookup"><span data-stu-id="54735-128">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="54735-129">Pointeur vers une structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="54735-129">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="54735-130">Si *hDevice* a été ouvert sans spécifier d' **indicateur de fichier avec \_ \_ chevauchement**, *lpOverlapped* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="54735-130">If *hDevice* was opened without specifying **FILE\_FLAG\_OVERLAPPED**, *lpOverlapped* is ignored.</span></span>

<span data-ttu-id="54735-131">Si *hDevice* a été ouvert avec l’indicateur de fichier avec l' **indicateur de \_ \_ chevauchement** , l’opération est exécutée en tant qu’opération Overlapped (asynchrone).</span><span class="sxs-lookup"><span data-stu-id="54735-131">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="54735-132">Dans ce cas, *lpOverlapped* doit pointer vers une structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) valide qui contient un handle vers un objet d’événement.</span><span class="sxs-lookup"><span data-stu-id="54735-132">In this case, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure that contains a handle to an event object.</span></span> <span data-ttu-id="54735-133">Dans le cas contraire, la fonction échoue de façon imprévisible.</span><span class="sxs-lookup"><span data-stu-id="54735-133">Otherwise, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="54735-134">Pour les opérations avec chevauchement, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne immédiatement, et l’objet d’événement est signalé lorsque l’opération est terminée.</span><span class="sxs-lookup"><span data-stu-id="54735-134">For overlapped operations, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns immediately, and the event object is signaled when the operation has been completed.</span></span> <span data-ttu-id="54735-135">Sinon, la fonction ne retourne pas jusqu’à ce que l’opération soit terminée ou qu’une erreur se produise.</span><span class="sxs-lookup"><span data-stu-id="54735-135">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54735-136">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="54735-136">Return value</span></span>

<span data-ttu-id="54735-137">Si l’opération se termine correctement, ce qui indique que tous les volumes sur le disque sont prêts à être utilisés, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="54735-137">If the operation completes successfully, indicating that all volumes on the disk are ready for use, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="54735-138">Si l’opération échoue ou est en attente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="54735-138">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="54735-139">Pour obtenir des informations détaillées sur l’erreur, appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="54735-139">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="54735-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="54735-140">Requirements</span></span>



| <span data-ttu-id="54735-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="54735-141">Requirement</span></span> | <span data-ttu-id="54735-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="54735-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="54735-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="54735-143">Minimum supported client</span></span><br/> | <span data-ttu-id="54735-144">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="54735-144">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="54735-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="54735-145">Minimum supported server</span></span><br/> | <span data-ttu-id="54735-146">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="54735-146">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="54735-147">En-tête</span><span class="sxs-lookup"><span data-stu-id="54735-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="54735-148"><dt>NTDDDISK. h</dt></span><span class="sxs-lookup"><span data-stu-id="54735-148"><dt>Ntdddisk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54735-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54735-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54735-150">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="54735-150">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="54735-151">Codes de contrôle de gestion des disques</span><span class="sxs-lookup"><span data-stu-id="54735-151">Disk Management Control Codes</span></span>](disk-management-control-codes.md)
</dt> </dl>

 

