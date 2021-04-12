---
description: Le \_ Code de contrôle des attributs da obtenir \_ NFS \_ interroge des informations supplémentaires sur un partage NFS.
ms.assetid: BC9E0E19-7D78-4AE7-A3E6-9FD9212B2B83
title: Code de contrôle DA_GET_NFS_ATTRIBUTES
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DA_GET_NFS_ATTRIBUTES
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4427dd48190bd12f7837c4841a98e15f7ddaff5f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523372"
---
# <a name="da_get_nfs_attributes-control-code"></a><span data-ttu-id="b94aa-103">\_Code de \_ contrôle des attributs NFS d’extraction de da \_</span><span class="sxs-lookup"><span data-stu-id="b94aa-103">DA\_GET\_NFS\_ATTRIBUTES control code</span></span>

<span data-ttu-id="b94aa-104">Le code de contrôle des **\_ \_ \_ attributs da obtenir NFS** interroge des informations supplémentaires sur un partage NFS.</span><span class="sxs-lookup"><span data-stu-id="b94aa-104">The **DA\_GET\_NFS\_ATTRIBUTES** control code queries additional information about an NFS share.</span></span>

<span data-ttu-id="b94aa-105">Pour effectuer cette opération, appelez la fonction [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="b94aa-105">To perform this operation, call the [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL 
   WINAPI 
   DeviceIoControl( (HANDLE)       hDevice,               // handle to device
                    (DWORD)        DA_GET_NFS_ATTRIBUTES, // dwIoControlCode
                                   NULL,                  // lpInBuffer
                                   0,                     // nInBufferSize
                    (LPDWORD)      lpOutBuffer,           // output buffer
                    (DWORD)        nOutBufferSize,        // size of output buffer
                    (LPDWORD)      lpBytesReturned,       // number of bytes returned
                    (LPOVERLAPPED) lpOverlapped );        // OVERLAPPED structure
```



## <a name="parameters"></a><span data-ttu-id="b94aa-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b94aa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b94aa-107">*hDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b94aa-107">*hDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b94aa-108">Handle d’un fichier sur le partage NFS.</span><span class="sxs-lookup"><span data-stu-id="b94aa-108">A handle to a file on the NFS share.</span></span> <span data-ttu-id="b94aa-109">Pour obtenir ce descripteur, appelez la fonction [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="b94aa-109">To obtain this handle, call the [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="b94aa-110">*dwIoControlCode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b94aa-110">*dwIoControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b94aa-111">Code de contrôle de l’opération.</span><span class="sxs-lookup"><span data-stu-id="b94aa-111">The control code for the operation.</span></span> <span data-ttu-id="b94aa-112">Utilisez **da \_ obtenir \_ des \_ attributs NFS** pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="b94aa-112">Use **DA\_GET\_NFS\_ATTRIBUTES** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="b94aa-113">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="b94aa-113">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="b94aa-114">Non utilisé avec cette opération ; Affectez la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="b94aa-114">Not used with this operation; set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b94aa-115">*nInBufferSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b94aa-115">*nInBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b94aa-116">Non utilisé avec cette opération ; défini à zéro.</span><span class="sxs-lookup"><span data-stu-id="b94aa-116">Not used with this operation; set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="b94aa-117">*lpOutBuffer* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b94aa-117">*lpOutBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b94aa-118">Pointeur vers la mémoire tampon de sortie, qui contient une structure d' **\_ \_ attributs de fichier NFS** .</span><span class="sxs-lookup"><span data-stu-id="b94aa-118">A pointer to the output buffer, which contains an **NFS\_FILE\_ATTRIBUTES** structure.</span></span> <span data-ttu-id="b94aa-119">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="b94aa-119">For more information, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="b94aa-120">*nOutBufferSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b94aa-120">*nOutBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b94aa-121">Taille de la mémoire tampon de sortie en octets.</span><span class="sxs-lookup"><span data-stu-id="b94aa-121">The size of the output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="b94aa-122">*lpBytesReturned* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b94aa-122">*lpBytesReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b94aa-123">Pointeur vers une variable qui reçoit la taille des données stockées dans la mémoire tampon de sortie, en octets.</span><span class="sxs-lookup"><span data-stu-id="b94aa-123">A pointer to a variable that receives the size of the data stored in the output buffer, in bytes.</span></span>

<span data-ttu-id="b94aa-124">Si la mémoire tampon de sortie est trop petite, l’appel échoue, [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne l' **erreur \_ \_ mémoire tampon insuffisante** et *lpBytesReturned* est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="b94aa-124">If the output buffer is too small, the call fails, [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns **ERROR\_INSUFFICIENT\_BUFFER**, and *lpBytesReturned* is zero.</span></span>

<span data-ttu-id="b94aa-125">Si *lpOverlapped* a la **valeur null**, *lpBytesReturned* ne peut pas avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="b94aa-125">If *lpOverlapped* is **NULL**, *lpBytesReturned* cannot be **NULL**.</span></span> <span data-ttu-id="b94aa-126">Même lorsqu’une opération ne retourne aucune donnée de sortie et que *lpOutBuffer* a la **valeur null**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) utilise *lpBytesReturned*.</span><span class="sxs-lookup"><span data-stu-id="b94aa-126">Even when an operation returns no output data and *lpOutBuffer* is **NULL**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) makes use of *lpBytesReturned*.</span></span> <span data-ttu-id="b94aa-127">Après une telle opération, la valeur de *lpBytesReturned* est sans signification.</span><span class="sxs-lookup"><span data-stu-id="b94aa-127">After such an operation, the value of *lpBytesReturned* is meaningless.</span></span>

<span data-ttu-id="b94aa-128">Si *lpOverlapped* n’a pas la **valeur null**, *LpBytesReturned* peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="b94aa-128">If *lpOverlapped* is not **NULL**, *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="b94aa-129">Si ce paramètre n’est pas **null** et que l’opération retourne des données, *lpBytesReturned* n’a pas de sens tant que l’opération avec chevauchement n’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="b94aa-129">If this parameter is not **NULL** and the operation returns data, *lpBytesReturned* is meaningless until the overlapped operation has completed.</span></span> <span data-ttu-id="b94aa-130">Pour récupérer le nombre d’octets retournés, appelez [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult).</span><span class="sxs-lookup"><span data-stu-id="b94aa-130">To retrieve the number of bytes returned, call [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult).</span></span> <span data-ttu-id="b94aa-131">Si le paramètre *hDevice* est associé à un port de terminaison d’e/s, vous pouvez récupérer le nombre d’octets renvoyés en appelant [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus).</span><span class="sxs-lookup"><span data-stu-id="b94aa-131">If the *hDevice* parameter is associated with an I/O completion port, you can retrieve the number of bytes returned by calling [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus).</span></span>

</dd> <dt>

<span data-ttu-id="b94aa-132">*lpOverlapped* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b94aa-132">*lpOverlapped* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b94aa-133">Pointeur vers une structure [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="b94aa-133">A pointer to an [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="b94aa-134">Si *hDevice* a été ouvert sans spécifier d' **indicateur de fichier avec \_ \_ chevauchement**, *lpOverlapped* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="b94aa-134">If *hDevice* was opened without specifying **FILE\_FLAG\_OVERLAPPED**, *lpOverlapped* is ignored.</span></span>

<span data-ttu-id="b94aa-135">Si *hDevice* a été ouvert avec l’indicateur de fichier avec l' **indicateur de \_ \_ chevauchement** , l’opération est exécutée en tant qu’opération Overlapped (asynchrone).</span><span class="sxs-lookup"><span data-stu-id="b94aa-135">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="b94aa-136">Dans ce cas, *lpOverlapped* doit pointer vers une structure [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) valide qui contient un handle vers un objet d’événement.</span><span class="sxs-lookup"><span data-stu-id="b94aa-136">In this case, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure that contains a handle to an event object.</span></span> <span data-ttu-id="b94aa-137">Dans le cas contraire, la fonction échoue de façon imprévisible.</span><span class="sxs-lookup"><span data-stu-id="b94aa-137">Otherwise, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="b94aa-138">Pour les opérations avec chevauchement, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne immédiatement, et l’objet d’événement est signalé lorsque l’opération est terminée.</span><span class="sxs-lookup"><span data-stu-id="b94aa-138">For overlapped operations, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns immediately, and the event object is signaled when the operation has been completed.</span></span> <span data-ttu-id="b94aa-139">Sinon, la fonction ne retourne pas jusqu’à ce que l’opération soit terminée ou qu’une erreur se produise.</span><span class="sxs-lookup"><span data-stu-id="b94aa-139">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b94aa-140">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b94aa-140">Return value</span></span>

<span data-ttu-id="b94aa-141">Si l’opération se termine correctement, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="b94aa-141">If the operation completes successfully, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="b94aa-142">Si l’opération échoue ou est en attente, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="b94aa-142">If the operation fails or is pending, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="b94aa-143">Pour obtenir des informations détaillées sur l’erreur, appelez [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="b94aa-143">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="b94aa-144">Remarques</span><span class="sxs-lookup"><span data-stu-id="b94aa-144">Remarks</span></span>

<span data-ttu-id="b94aa-145">Ce code de contrôle n’a aucun fichier d’en-tête associé.</span><span class="sxs-lookup"><span data-stu-id="b94aa-145">This control code has no associated header file.</span></span> <span data-ttu-id="b94aa-146">Vous devez définir le code de contrôle et les structures de données comme suit.</span><span class="sxs-lookup"><span data-stu-id="b94aa-146">You must define the control code and data structures as follows.</span></span>

``` syntax
#define DEVICE_DA_RDR 0x80000  
 
#define DA_GET_NFS_ATTRIBUTES CTL_CODE(DEVICE_DA_RDR, 0x804, METHOD_BUFFERED, FILE_ANY_ACCESS)

typedef struct _NFS_SPEC_DATA {  
    ULONG               SpecData1;
    ULONG               SpecData2;
} NFS_SPEC_DATA, *PNFS_SPEC_DATA;

typedef struct _NFS_TIME {
    ULONG        Seconds;
    ULONG        nSeconds;
} NFS_TIME, *PNFS_TIME;

#define NFS_TYPE_REG         1
#define NFS_TYPE_DIR         2
#define NFS_TYPE_BLK         3
#define NFS_TYPE_CHR         4
#define NFS_TYPE_LNK         5
#define NFS_TYPE_SOCK        6
#define NFS_TYPE_FIFO        7

typedef struct _NFS_FILE_ATTRIBUTES {  
    ULONG               FileType;  
    ULONG               Mode;  
    ULONG               NLink;  
    ULONG               Uid;  
    ULONG               Gid;  
    ULONGLONG           Size;  
    ULONGLONG           Used;
    NFS_SPEC_DATA       Rdev;
    ULONGLONG           Fsid;  
    ULONGLONG           FileId;  
    NFS_TIME            AccessTime;  
    NFS_TIME            ModifyTime;  
    NFS_TIME            ChangeTime;  
} NFS_FILE_ATTRIBUTES, *PNFS_FILE_ATTRIBUTES;

typedef struct _DA_FILE_ATTRIBUTES {  
    NFS_FILE_ATTRIBUTES FileAttributes;  
    ULONG               Version;  
} DA_FILE_ATTRIBUTES, *PDA_FILE_ATTRIBUTES;
```

<span data-ttu-id="b94aa-147">Les membres de la structure peuvent être décrits comme suit.</span><span class="sxs-lookup"><span data-stu-id="b94aa-147">The structure members can be described as follows.</span></span>

<dl> <dt>

<span data-ttu-id="b94aa-148"><span id="SpecData1"></span><span id="specdata1"></span><span id="SPECDATA1"></span>**SpecData1**</span><span class="sxs-lookup"><span data-stu-id="b94aa-148"><span id="SpecData1"></span><span id="specdata1"></span><span id="SPECDATA1"></span>**SpecData1**</span></span>
</dt> <dd>

<span data-ttu-id="b94aa-149">Valeur opaque utilisée pour les types de fichiers spéciaux, tels que les fichiers spéciaux de bloc, spéciaux et FIFO.</span><span class="sxs-lookup"><span data-stu-id="b94aa-149">An opaque value that is used for special file types such as block-special, character-special and FIFO files.</span></span>

</dd> <dt>

<span data-ttu-id="b94aa-150"><span id="SpecData2"></span><span id="specdata2"></span><span id="SPECDATA2"></span>**SpecData2**</span><span class="sxs-lookup"><span data-stu-id="b94aa-150"><span id="SpecData2"></span><span id="specdata2"></span><span id="SPECDATA2"></span>**SpecData2**</span></span>
</dt> <dd>

<span data-ttu-id="b94aa-151">Valeur opaque utilisée pour les types de fichiers spéciaux, tels que les fichiers spéciaux de bloc, spéciaux et FIFO.</span><span class="sxs-lookup"><span data-stu-id="b94aa-151">An opaque value that is used for special file types such as block-special, character-special and FIFO files.</span></span>

</dd> <dt>

<span data-ttu-id="b94aa-152"><span id="Seconds"></span><span id="seconds"></span><span id="SECONDS"></span>**Durée**</span><span class="sxs-lookup"><span data-stu-id="b94aa-152"><span id="Seconds"></span><span id="seconds"></span><span id="SECONDS"></span>**Seconds**</span></span>
</dt> <dd>

<span data-ttu-id="b94aa-153">Valeur 64 bits représentant les secondes écoulées depuis le 1er janvier 1970 (UTC).</span><span class="sxs-lookup"><span data-stu-id="b94aa-153">A 64-bit value representing the seconds since January 1, 1970 (UTC).</span></span>

</dd> <dt>

<span data-ttu-id="b94aa-154"><span id="nSeconds"></span><span id="nseconds"></span><span id="NSECONDS"></span>**nSeconds**</span><span class="sxs-lookup"><span data-stu-id="b94aa-154"><span id="nSeconds"></span><span id="nseconds"></span><span id="NSECONDS"></span>**nSeconds**</span></span>
</dt> <dd>

<span data-ttu-id="b94aa-155">Nombre de nanosecondes à ajouter au membre **seconds** .</span><span class="sxs-lookup"><span data-stu-id="b94aa-155">The number of nanoseconds to be added to the **Seconds** member.</span></span>

</dd> <dt>

<span data-ttu-id="b94aa-156"><span id="FileType"></span><span id="filetype"></span><span id="FILETYPE"></span>**FileType**</span><span class="sxs-lookup"><span data-stu-id="b94aa-156"><span id="FileType"></span><span id="filetype"></span><span id="FILETYPE"></span>**FileType**</span></span>
</dt> <dd>

<span data-ttu-id="b94aa-157">Type de fichier NFS du partage.</span><span class="sxs-lookup"><span data-stu-id="b94aa-157">The NFS file type of the share.</span></span>



| <span data-ttu-id="b94aa-158">Type de fichier NFS</span><span class="sxs-lookup"><span data-stu-id="b94aa-158">NFS File Type</span></span>                                                                              | <span data-ttu-id="b94aa-159">Description</span><span class="sxs-lookup"><span data-stu-id="b94aa-159">Description</span></span>                          |
|--------------------------------------------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="b94aa-160"><span id="NFS_TYPE_REG"></span><span id="nfs_type_reg"></span>\_reg de type NFS \_</span><span class="sxs-lookup"><span data-stu-id="b94aa-160"><span id="NFS_TYPE_REG"></span><span id="nfs_type_reg"></span>NFS\_TYPE\_REG</span></span><br/>    | <span data-ttu-id="b94aa-161">Fichier normal.</span><span class="sxs-lookup"><span data-stu-id="b94aa-161">A regular file.</span></span><br/>           |
| <span data-ttu-id="b94aa-162"><span id="NFS_TYPE_DIR"></span><span id="nfs_type_dir"></span>Rép. de \_ type NFS \_</span><span class="sxs-lookup"><span data-stu-id="b94aa-162"><span id="NFS_TYPE_DIR"></span><span id="nfs_type_dir"></span>NFS\_TYPE\_DIR</span></span><br/>    | <span data-ttu-id="b94aa-163">Un répertoire.</span><span class="sxs-lookup"><span data-stu-id="b94aa-163">A directory.</span></span><br/>              |
| <span data-ttu-id="b94aa-164"><span id="NFS_TYPE_BLK"></span><span id="nfs_type_blk"></span>\_BLK de type NFS \_</span><span class="sxs-lookup"><span data-stu-id="b94aa-164"><span id="NFS_TYPE_BLK"></span><span id="nfs_type_blk"></span>NFS\_TYPE\_BLK</span></span><br/>    | <span data-ttu-id="b94aa-165">Fichier spécial de bloc.</span><span class="sxs-lookup"><span data-stu-id="b94aa-165">A block-special file.</span></span><br/>     |
| <span data-ttu-id="b94aa-166"><span id="NFS_TYPE_CHR"></span><span id="nfs_type_chr"></span>TYPE de NFS \_ \_ Chr</span><span class="sxs-lookup"><span data-stu-id="b94aa-166"><span id="NFS_TYPE_CHR"></span><span id="nfs_type_chr"></span>NFS\_TYPE\_CHR</span></span><br/>    | <span data-ttu-id="b94aa-167">Fichier spécial de caractères.</span><span class="sxs-lookup"><span data-stu-id="b94aa-167">A character-special file.</span></span><br/> |
| <span data-ttu-id="b94aa-168"><span id="NFS_TYPE_LNK"></span><span id="nfs_type_lnk"></span>\_type NFS \_ lnk</span><span class="sxs-lookup"><span data-stu-id="b94aa-168"><span id="NFS_TYPE_LNK"></span><span id="nfs_type_lnk"></span>NFS\_TYPE\_LNK</span></span><br/>    | <span data-ttu-id="b94aa-169">Lien symbolique.</span><span class="sxs-lookup"><span data-stu-id="b94aa-169">A symbolic link.</span></span><br/>          |
| <span data-ttu-id="b94aa-170"><span id="NFS_TYPE_SOCK"></span><span id="nfs_type_sock"></span>\_chaussette de type NFS \_</span><span class="sxs-lookup"><span data-stu-id="b94aa-170"><span id="NFS_TYPE_SOCK"></span><span id="nfs_type_sock"></span>NFS\_TYPE\_SOCK</span></span><br/> | <span data-ttu-id="b94aa-171">Socket Windows.</span><span class="sxs-lookup"><span data-stu-id="b94aa-171">A Windows socket.</span></span><br/>         |
| <span data-ttu-id="b94aa-172"><span id="NFS_TYPE_FIFO"></span><span id="nfs_type_fifo"></span>\_type NFS \_ FIFO</span><span class="sxs-lookup"><span data-stu-id="b94aa-172"><span id="NFS_TYPE_FIFO"></span><span id="nfs_type_fifo"></span>NFS\_TYPE\_FIFO</span></span><br/> | <span data-ttu-id="b94aa-173">Fichier FIFO.</span><span class="sxs-lookup"><span data-stu-id="b94aa-173">A FIFO file.</span></span><br/>              |



 

</dd> <dt>

<span data-ttu-id="b94aa-174"><span id="Mode"></span><span id="mode"></span><span id="MODE"></span>**Mode**</span><span class="sxs-lookup"><span data-stu-id="b94aa-174"><span id="Mode"></span><span id="mode"></span><span id="MODE"></span>**Mode**</span></span>
</dt> <dd>

<span data-ttu-id="b94aa-175">Mode de fichier.</span><span class="sxs-lookup"><span data-stu-id="b94aa-175">The file mode.</span></span>

</dd> <dt>

<span data-ttu-id="b94aa-176"><span id="NLink"></span><span id="nlink"></span><span id="NLINK"></span>**NLink**</span><span class="sxs-lookup"><span data-stu-id="b94aa-176"><span id="NLink"></span><span id="nlink"></span><span id="NLINK"></span>**NLink**</span></span>
</dt> <dd>

<span data-ttu-id="b94aa-177">Nombre de liens vers le partage.</span><span class="sxs-lookup"><span data-stu-id="b94aa-177">The number of links to the share.</span></span>

</dd> <dt>

<span data-ttu-id="b94aa-178"><span id="Uid"></span><span id="uid"></span><span id="UID"></span>**Codé**</span><span class="sxs-lookup"><span data-stu-id="b94aa-178"><span id="Uid"></span><span id="uid"></span><span id="UID"></span>**Uid**</span></span>
</dt> <dd>

<span data-ttu-id="b94aa-179">Identificateur d’utilisateur (UID) UNIX.</span><span class="sxs-lookup"><span data-stu-id="b94aa-179">The UNIX user identifier (UID).</span></span>

</dd> <dt>

<span data-ttu-id="b94aa-180"><span id="Gid"></span><span id="gid"></span><span id="GID"></span>**ID**</span><span class="sxs-lookup"><span data-stu-id="b94aa-180"><span id="Gid"></span><span id="gid"></span><span id="GID"></span>**Gid**</span></span>
</dt> <dd>

<span data-ttu-id="b94aa-181">Identificateur du groupe UNIX (GID).</span><span class="sxs-lookup"><span data-stu-id="b94aa-181">The UNIX group identifier (GID).</span></span>

</dd> <dt>

<span data-ttu-id="b94aa-182"><span id="Size"></span><span id="size"></span><span id="SIZE"></span>**Corps**</span><span class="sxs-lookup"><span data-stu-id="b94aa-182"><span id="Size"></span><span id="size"></span><span id="SIZE"></span>**Size**</span></span>
</dt> <dd>

<span data-ttu-id="b94aa-183">Taille du fichier, en octets.</span><span class="sxs-lookup"><span data-stu-id="b94aa-183">The file size, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="b94aa-184"><span id="Used"></span><span id="used"></span><span id="USED"></span>**Servir**</span><span class="sxs-lookup"><span data-stu-id="b94aa-184"><span id="Used"></span><span id="used"></span><span id="USED"></span>**Used**</span></span>
</dt> <dd>

<span data-ttu-id="b94aa-185">Taille de fichier utilisée, en octets.</span><span class="sxs-lookup"><span data-stu-id="b94aa-185">The file size used, in bytes.</span></span> <span data-ttu-id="b94aa-186">Il s’agit de la même taille de fichier.</span><span class="sxs-lookup"><span data-stu-id="b94aa-186">This is the same as the file size.</span></span>

</dd> <dt>

<span data-ttu-id="b94aa-187"><span id="Rdev"></span><span id="rdev"></span><span id="RDEV"></span>**Rdev**</span><span class="sxs-lookup"><span data-stu-id="b94aa-187"><span id="Rdev"></span><span id="rdev"></span><span id="RDEV"></span>**Rdev**</span></span>
</dt> <dd>

<span data-ttu-id="b94aa-188">Identificateur de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="b94aa-188">The device identifier.</span></span>

</dd> <dt>

<span data-ttu-id="b94aa-189"><span id="Fsid"></span><span id="fsid"></span><span id="FSID"></span>**Fsid**</span><span class="sxs-lookup"><span data-stu-id="b94aa-189"><span id="Fsid"></span><span id="fsid"></span><span id="FSID"></span>**Fsid**</span></span>
</dt> <dd>

<span data-ttu-id="b94aa-190">Identificateur du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="b94aa-190">The file system identifier.</span></span>

</dd> <dt>

<span data-ttu-id="b94aa-191"><span id="FileId"></span><span id="fileid"></span><span id="FILEID"></span>**Combinaison**</span><span class="sxs-lookup"><span data-stu-id="b94aa-191"><span id="FileId"></span><span id="fileid"></span><span id="FILEID"></span>**FileId**</span></span>
</dt> <dd>

<span data-ttu-id="b94aa-192">Identificateur de fichier.</span><span class="sxs-lookup"><span data-stu-id="b94aa-192">The file identifier.</span></span>

</dd> <dt>

<span data-ttu-id="b94aa-193"><span id="AccessTime"></span><span id="accesstime"></span><span id="ACCESSTIME"></span>**AccessTime**</span><span class="sxs-lookup"><span data-stu-id="b94aa-193"><span id="AccessTime"></span><span id="accesstime"></span><span id="ACCESSTIME"></span>**AccessTime**</span></span>
</dt> <dd>

<span data-ttu-id="b94aa-194">Heure du dernier accès.</span><span class="sxs-lookup"><span data-stu-id="b94aa-194">The last access time.</span></span>

</dd> <dt>

<span data-ttu-id="b94aa-195"><span id="ModifyTime"></span><span id="modifytime"></span><span id="MODIFYTIME"></span>**ModifyTime**</span><span class="sxs-lookup"><span data-stu-id="b94aa-195"><span id="ModifyTime"></span><span id="modifytime"></span><span id="MODIFYTIME"></span>**ModifyTime**</span></span>
</dt> <dd>

<span data-ttu-id="b94aa-196">Heure de la dernière modification.</span><span class="sxs-lookup"><span data-stu-id="b94aa-196">The last modification time.</span></span>

</dd> <dt>

<span data-ttu-id="b94aa-197"><span id="ChangeTime"></span><span id="changetime"></span><span id="CHANGETIME"></span>**ChangeTime**</span><span class="sxs-lookup"><span data-stu-id="b94aa-197"><span id="ChangeTime"></span><span id="changetime"></span><span id="CHANGETIME"></span>**ChangeTime**</span></span>
</dt> <dd>

<span data-ttu-id="b94aa-198">Heure de la dernière modification.</span><span class="sxs-lookup"><span data-stu-id="b94aa-198">The last change time.</span></span>

</dd> <dt>

<span data-ttu-id="b94aa-199"><span id="FileAttributes"></span><span id="fileattributes"></span><span id="FILEATTRIBUTES"></span>**FileAttributes**</span><span class="sxs-lookup"><span data-stu-id="b94aa-199"><span id="FileAttributes"></span><span id="fileattributes"></span><span id="FILEATTRIBUTES"></span>**FileAttributes**</span></span>
</dt> <dd>

<span data-ttu-id="b94aa-200">Structure **d' \_ \_ attributs de fichier NFS** .</span><span class="sxs-lookup"><span data-stu-id="b94aa-200">An **NFS\_FILE\_ATTRIBUTES** structure.</span></span>

> [!Note]  
> <span data-ttu-id="b94aa-201">Pour obtenir une description plus détaillée des membres de cette structure, consultez la structure **fattr3** dans la spécification du protocole NFS version 3 (telle que définie dans la [norme RFC 1813](https://www.ietf.org/rfc/rfc1813.txt)).</span><span class="sxs-lookup"><span data-stu-id="b94aa-201">For more detailed descriptions of the members of this structure, see the **fattr3** structure in the NFS Version 3 Protocol Specification (as defined in [RFC 1813](https://www.ietf.org/rfc/rfc1813.txt)).</span></span>

 

</dd> <dt>

<span data-ttu-id="b94aa-202"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Version**</span><span class="sxs-lookup"><span data-stu-id="b94aa-202"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Version**</span></span>
</dt> <dd>

<span data-ttu-id="b94aa-203">Spécifie si la connexion sur laquelle le descripteur du partage NFS a été créé se trouve sur le protocole NFS version 2 ou NFS version 3.</span><span class="sxs-lookup"><span data-stu-id="b94aa-203">Specifies whether the connection on which the handle to the NFS share was created is over NFS Version 2 or NFS Version 3 protocol.</span></span>



| <span data-ttu-id="b94aa-204">Valeur</span><span class="sxs-lookup"><span data-stu-id="b94aa-204">Value</span></span>                            | <span data-ttu-id="b94aa-205">Description</span><span class="sxs-lookup"><span data-stu-id="b94aa-205">Description</span></span>              |
|----------------------------------|--------------------------|
| <span data-ttu-id="b94aa-206"><span id="2"></span>2</span><span class="sxs-lookup"><span data-stu-id="b94aa-206"><span id="2"></span>2</span></span><br/> | <span data-ttu-id="b94aa-207">NFS version 2</span><span class="sxs-lookup"><span data-stu-id="b94aa-207">NFS Version 2</span></span><br/> |
| <span data-ttu-id="b94aa-208"><span id="3"></span>1,3</span><span class="sxs-lookup"><span data-stu-id="b94aa-208"><span id="3"></span>3</span></span><br/> | <span data-ttu-id="b94aa-209">NFS version 3</span><span class="sxs-lookup"><span data-stu-id="b94aa-209">NFS Version 3</span></span><br/> |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b94aa-210">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b94aa-210">Requirements</span></span>



| <span data-ttu-id="b94aa-211">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b94aa-211">Requirement</span></span> | <span data-ttu-id="b94aa-212">Valeur</span><span class="sxs-lookup"><span data-stu-id="b94aa-212">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="b94aa-213">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b94aa-213">Minimum supported client</span></span><br/> | <span data-ttu-id="b94aa-214">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b94aa-214">None supported</span></span><br/>         |
| <span data-ttu-id="b94aa-215">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b94aa-215">Minimum supported server</span></span><br/> | <span data-ttu-id="b94aa-216">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b94aa-216">Windows Server 2008</span></span><br/>    |
| <span data-ttu-id="b94aa-217">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="b94aa-217">End of client support</span></span><br/>    | <span data-ttu-id="b94aa-218">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b94aa-218">None supported</span></span><br/>         |
| <span data-ttu-id="b94aa-219">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="b94aa-219">End of server support</span></span><br/>    | <span data-ttu-id="b94aa-220">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b94aa-220">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b94aa-221">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b94aa-221">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b94aa-222">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="b94aa-222">**DeviceIoControl**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> </dl>

 

 
