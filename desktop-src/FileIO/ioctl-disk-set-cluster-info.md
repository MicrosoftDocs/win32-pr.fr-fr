---
description: Définit les informations de cluster sur un disque.
ms.assetid: AB2243D9-4913-4412-87E0-2C8DB8AB10B8
title: IOCTL_DISK_SET_CLUSTER_INFO le code de contrôle (NTDDDISK. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_DISK_SET_CLUSTER_INFO
api_type:
- HeaderDef
api_location:
- Ntdddisk.h
ms.openlocfilehash: 4ba0994dd1c9030e84c22e24b1eb4583eba7e3d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545091"
---
# <a name="ioctl_disk_set_cluster_info-control-code"></a><span data-ttu-id="a9dd6-103">\_Code de \_ contrôle d' \_ informations de cluster IOCTL Disk Set \_</span><span class="sxs-lookup"><span data-stu-id="a9dd6-103">IOCTL\_DISK\_SET\_CLUSTER\_INFO control code</span></span>

<span data-ttu-id="a9dd6-104">Définit les informations de cluster sur un disque.</span><span class="sxs-lookup"><span data-stu-id="a9dd6-104">Sets the cluster information on a disk.</span></span>

<span data-ttu-id="a9dd6-105">Pour effectuer cette opération, appelez la fonction [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="a9dd6-105">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL 
WINAPI 
DeviceIoControl( (HANDLE)       hDevice,         // handle to device 
                 IOCTL_DISK_SET_CLUSTER_INFO,    // dwIoControlCode
                 (LPVOID)       NULL,            // lpInBuffer 
                 (DWORD)        0,               // nInBufferSize 
                 (LPVOID)       lpOutBuffer,     // output buffer:GET_DISK_ATTRIBUTES
                 (DWORD)        nOutBufferSize,  // size of output buffer
                 (LPDWORD)      lpBytesReturned, // number of bytes returned
                 (LPOVERLAPPED) lpOverlapped );  // OVERLAPPED structure
```



## <a name="parameters"></a><span data-ttu-id="a9dd6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a9dd6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9dd6-107">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="a9dd6-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="a9dd6-108">Handle sur le disque.</span><span class="sxs-lookup"><span data-stu-id="a9dd6-108">A handle to the disk.</span></span>

<span data-ttu-id="a9dd6-109">Pour récupérer un handle d’appareil, appelez la fonction [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="a9dd6-109">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="a9dd6-110">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="a9dd6-110">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="a9dd6-111">Code de contrôle de l’opération.</span><span class="sxs-lookup"><span data-stu-id="a9dd6-111">The control code for the operation.</span></span>

<span data-ttu-id="a9dd6-112">Utilisez **les \_ \_ informations du \_ cluster \_ d’ensemble de disques IOCTL** pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="a9dd6-112">Use **IOCTL\_DISK\_SET\_CLUSTER\_INFO** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="a9dd6-113">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="a9dd6-113">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="a9dd6-114">Pointeur vers une structure de données d' [**\_ \_ informations de cluster de disque**](disk-cluster-info.md) qui contient des informations de cluster pour le disque.</span><span class="sxs-lookup"><span data-stu-id="a9dd6-114">A pointer to a [**DISK\_CLUSTER\_INFO**](disk-cluster-info.md) data structure that contains cluster information for the disk.</span></span>

</dd> <dt>

<span data-ttu-id="a9dd6-115">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="a9dd6-115">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="a9dd6-116">Taille de la mémoire tampon d’entrée, en octets.</span><span class="sxs-lookup"><span data-stu-id="a9dd6-116">The size of the input buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="a9dd6-117">*lpOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="a9dd6-117">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="a9dd6-118">Non utilisé avec cette opération.</span><span class="sxs-lookup"><span data-stu-id="a9dd6-118">Not used with this operation.</span></span> <span data-ttu-id="a9dd6-119">Affectez la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="a9dd6-119">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a9dd6-120">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="a9dd6-120">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="a9dd6-121">Taille de la mémoire tampon de sortie en octets.</span><span class="sxs-lookup"><span data-stu-id="a9dd6-121">The size of the output buffer, in bytes.</span></span> <span data-ttu-id="a9dd6-122">Défini sur 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="a9dd6-122">Set to 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="a9dd6-123">*lpBytesReturned*</span><span class="sxs-lookup"><span data-stu-id="a9dd6-123">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="a9dd6-124">Non utilisé avec cette opération.</span><span class="sxs-lookup"><span data-stu-id="a9dd6-124">Not used with this operation.</span></span> <span data-ttu-id="a9dd6-125">Affectez la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="a9dd6-125">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a9dd6-126">*lpOverlapped*</span><span class="sxs-lookup"><span data-stu-id="a9dd6-126">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="a9dd6-127">Pointeur vers une structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="a9dd6-127">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="a9dd6-128">Si *hDevice* a été ouvert sans spécifier d' **indicateur de fichier avec \_ \_ chevauchement**, *lpOverlapped* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="a9dd6-128">If *hDevice* was opened without specifying **FILE\_FLAG\_OVERLAPPED**, *lpOverlapped* is ignored.</span></span>

<span data-ttu-id="a9dd6-129">Si *hDevice* a été ouvert avec l’indicateur de fichier avec l' **indicateur de \_ \_ chevauchement** , l’opération est exécutée en tant qu’opération Overlapped (asynchrone).</span><span class="sxs-lookup"><span data-stu-id="a9dd6-129">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="a9dd6-130">Dans ce cas, *lpOverlapped* doit pointer vers une structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) valide qui contient un handle vers un objet d’événement.</span><span class="sxs-lookup"><span data-stu-id="a9dd6-130">In this case, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure that contains a handle to an event object.</span></span> <span data-ttu-id="a9dd6-131">Dans le cas contraire, la fonction échoue de façon imprévisible.</span><span class="sxs-lookup"><span data-stu-id="a9dd6-131">Otherwise, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="a9dd6-132">Pour les opérations avec chevauchement, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne immédiatement, et l’objet d’événement est signalé lorsque l’opération est terminée.</span><span class="sxs-lookup"><span data-stu-id="a9dd6-132">For overlapped operations, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns immediately, and the event object is signaled when the operation has been completed.</span></span> <span data-ttu-id="a9dd6-133">Sinon, la fonction ne retourne pas jusqu’à ce que l’opération soit terminée ou qu’une erreur se produise.</span><span class="sxs-lookup"><span data-stu-id="a9dd6-133">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9dd6-134">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a9dd6-134">Return value</span></span>

<span data-ttu-id="a9dd6-135">Si l’opération se termine correctement, ce qui indique que tous les volumes sur le disque sont prêts à être utilisés, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="a9dd6-135">If the operation completes successfully, indicating that all volumes on the disk are ready for use, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="a9dd6-136">Si l’opération échoue ou est en attente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="a9dd6-136">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="a9dd6-137">Pour obtenir des informations détaillées sur l’erreur, appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="a9dd6-137">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="a9dd6-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a9dd6-138">Requirements</span></span>



| <span data-ttu-id="a9dd6-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a9dd6-139">Requirement</span></span> | <span data-ttu-id="a9dd6-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="a9dd6-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a9dd6-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9dd6-141">Minimum supported client</span></span><br/> | <span data-ttu-id="a9dd6-142">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9dd6-142">None supported</span></span><br/>                                                             |
| <span data-ttu-id="a9dd6-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9dd6-143">Minimum supported server</span></span><br/> | <span data-ttu-id="a9dd6-144">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a9dd6-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a9dd6-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="a9dd6-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9dd6-146"><dt>NTDDDISK. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9dd6-146"><dt>Ntdddisk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9dd6-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a9dd6-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9dd6-148">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="a9dd6-148">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="a9dd6-149">Codes de contrôle de gestion des disques</span><span class="sxs-lookup"><span data-stu-id="a9dd6-149">Disk Management Control Codes</span></span>](disk-management-control-codes.md)
</dt> <dt>

[<span data-ttu-id="a9dd6-150">**\_informations sur le cluster de disque \_**</span><span class="sxs-lookup"><span data-stu-id="a9dd6-150">**DISK\_CLUSTER\_INFO**</span></span>](disk-cluster-info.md)
</dt> <dt>

[<span data-ttu-id="a9dd6-151">**\_informations de \_ cluster d’extraction de disque IOCTL \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a9dd6-151">**IOCTL\_DISK\_GET\_CLUSTER\_INFO**</span></span>](ioctl-disk-get-cluster-info.md)
</dt> </dl>

 

