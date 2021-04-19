---
description: Récupère les niveaux de rétroéclairage pris en charge.
ms.assetid: b4c1ee3f-af75-477e-b7ed-53be905374d7
title: IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS le code de contrôle (Ntddvdeo. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS
api_type:
- HeaderDef
api_location:
- Ntddvdeo.h
ms.openlocfilehash: a5618ec29fd47ba690106b5f826e6fb145eac208
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524650"
---
# <a name="ioctl_video_query_supported_brightness-control-code"></a><span data-ttu-id="c5142-103">\_Code de \_ contrôle de \_ luminosité pris en charge \_ pour la requête de vidéo IOCTL</span><span class="sxs-lookup"><span data-stu-id="c5142-103">IOCTL\_VIDEO\_QUERY\_SUPPORTED\_BRIGHTNESS control code</span></span>

<span data-ttu-id="c5142-104">Récupère les niveaux de rétroéclairage pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c5142-104">Retrieves the supported backlight levels.</span></span>

<span data-ttu-id="c5142-105">Pour effectuer cette opération, appelez la fonction [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="c5142-105">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,                // handle to device
  IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS,  // dwIoControlCode
  NULL,                            // lpInBuffer
  0,                               // nInBufferSize
  (LPVOID) lpOutBuffer,            // output buffer
  (DWORD) nOutBufferSize,          // size of output buffer
  (LPDWORD) lpBytesReturned,       // number of bytes returned
  (LPOVERLAPPED) lpOverlapped      // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="c5142-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c5142-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5142-107">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="c5142-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="c5142-108">Handle de \\ \\ . \\ Appareil LCD.</span><span class="sxs-lookup"><span data-stu-id="c5142-108">A handle to the \\\\.\\LCD device.</span></span> <span data-ttu-id="c5142-109">Pour récupérer un handle d’appareil, appelez la fonction [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="c5142-109">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="c5142-110">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="c5142-110">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="c5142-111">Code de contrôle de l’opération.</span><span class="sxs-lookup"><span data-stu-id="c5142-111">The control code for the operation.</span></span> <span data-ttu-id="c5142-112">Cette valeur identifie l’opération spécifique à effectuer et le type d’appareil sur lequel l’exécuter.</span><span class="sxs-lookup"><span data-stu-id="c5142-112">This value identifies the specific operation to be performed and the type of device on which to perform it.</span></span> <span data-ttu-id="c5142-113">Utilisez la luminosité de la **\_ requête de vidéo IOCTL \_ \_ prise en charge \_** pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="c5142-113">Use **IOCTL\_VIDEO\_QUERY\_SUPPORTED\_BRIGHTNESS** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="c5142-114">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="c5142-114">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="c5142-115">Non utilisé avec cette opération ; Affectez la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="c5142-115">Not used with this operation; set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c5142-116">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="c5142-116">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="c5142-117">Non utilisé avec cette opération ; défini à zéro.</span><span class="sxs-lookup"><span data-stu-id="c5142-117">Not used with this operation; set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="c5142-118">*lpOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="c5142-118">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="c5142-119">Pointeur vers une mémoire tampon qui reçoit un tableau des niveaux d’alimentation disponibles.</span><span class="sxs-lookup"><span data-stu-id="c5142-119">A pointer to a buffer that receives an array of the available power levels.</span></span> <span data-ttu-id="c5142-120">Cette mémoire tampon doit avoir une longueur de 256 octets.</span><span class="sxs-lookup"><span data-stu-id="c5142-120">This buffer should be 256 bytes long.</span></span>

</dd> <dt>

<span data-ttu-id="c5142-121">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="c5142-121">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="c5142-122">Taille de la mémoire tampon de sortie en octets.</span><span class="sxs-lookup"><span data-stu-id="c5142-122">The size of the output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="c5142-123">*lpBytesReturned*</span><span class="sxs-lookup"><span data-stu-id="c5142-123">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="c5142-124">Pointeur vers une variable qui reçoit la taille, en octets, des données de sortie retournées.</span><span class="sxs-lookup"><span data-stu-id="c5142-124">A pointer to a variable that receives the size, in bytes, of output data returned.</span></span>

<span data-ttu-id="c5142-125">Si la mémoire tampon de sortie est trop petite pour retourner des données, l’appel échoue, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne l’erreur de code d’erreur \_ mémoire tampon insuffisante \_ et le nombre d’octets retournés est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="c5142-125">If the output buffer is too small to return any data, then the call fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code ERROR\_INSUFFICIENT\_BUFFER, and the returned byte count is zero.</span></span>

<span data-ttu-id="c5142-126">Si la mémoire tampon de sortie est trop petite pour contenir toutes les données mais peut contenir des entrées, le système d’exploitation retourne autant d’éléments que vous le souhaitez, l’appel échoue, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne le code d’erreur \_ plus de \_ données, et *lpBytesReturned* indique la quantité de données retournées.</span><span class="sxs-lookup"><span data-stu-id="c5142-126">If the output buffer is too small to hold all of the data but can hold some entries, then the operating system returns as much as fits, the call fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code ERROR\_MORE\_DATA, and *lpBytesReturned* indicates the amount of data returned.</span></span> <span data-ttu-id="c5142-127">Votre application doit à nouveau appeler [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) avec la même opération, en spécifiant un nouveau point de départ.</span><span class="sxs-lookup"><span data-stu-id="c5142-127">Your application should call [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) again with the same operation, specifying a new starting point.</span></span>

<span data-ttu-id="c5142-128">Si *lpOverlapped* a la **valeur null** (e/s nonoverlapped), *lpBytesReturned* ne peut pas avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="c5142-128">If *lpOverlapped* is **NULL** (nonoverlapped I/O), *lpBytesReturned* cannot be **NULL**.</span></span>

<span data-ttu-id="c5142-129">Si *lpOverlapped* n’a pas la **valeur null** (e/s avec chevauchement), *LpBytesReturned* peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="c5142-129">If *lpOverlapped* is not **NULL** (overlapped I/O), *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="c5142-130">S’il s’agit d’une opération avec chevauchement, vous pouvez récupérer le nombre d’octets retournés en appelant la fonction [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) .</span><span class="sxs-lookup"><span data-stu-id="c5142-130">If this is an overlapped operation, you can retrieve the number of bytes returned by calling the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="c5142-131">Si *hDevice* est associé à un port de terminaison d’e/s, vous pouvez récupérer le nombre d’octets renvoyés en appelant la fonction [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="c5142-131">If *hDevice* is associated with an I/O completion port, you can get the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="c5142-132">*lpOverlapped*</span><span class="sxs-lookup"><span data-stu-id="c5142-132">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="c5142-133">Pointeur vers une structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="c5142-133">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="c5142-134">Si *hDevice* a été ouvert avec l’indicateur de fichier avec \_ indicateur de \_ chevauchement, *lpOverlapped* doit pointer vers une structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) valide.</span><span class="sxs-lookup"><span data-stu-id="c5142-134">If *hDevice* was opened with the FILE\_FLAG\_OVERLAPPED flag, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span> <span data-ttu-id="c5142-135">Dans ce cas, l’opération est exécutée en tant qu’opération Overlapped (asynchrone).</span><span class="sxs-lookup"><span data-stu-id="c5142-135">In this case, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="c5142-136">Si l’appareil a été ouvert avec l’indicateur de fichier avec \_ indicateur \_ de chevauchement et que *LpOverlapped* a la **valeur null**, la fonction échoue de façon imprévisible.</span><span class="sxs-lookup"><span data-stu-id="c5142-136">If the device was opened with the FILE\_FLAG\_OVERLAPPED flag and *lpOverlapped* is **NULL**, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="c5142-137">Si *hDevice* a été ouvert sans que l’indicateur de fichier n’ait été spécifié \_ \_ , *lpOverlapped* est ignoré et [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) ne retourne pas tant que l’opération n’est pas terminée, ou jusqu’à ce qu’une erreur se produise.</span><span class="sxs-lookup"><span data-stu-id="c5142-137">If *hDevice* was opened without specifying the FILE\_FLAG\_OVERLAPPED flag, *lpOverlapped* is ignored and [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) does not return until the operation has been completed, or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5142-138">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c5142-138">Return value</span></span>

<span data-ttu-id="c5142-139">Si l’opération se termine correctement, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="c5142-139">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="c5142-140">Si l’opération échoue ou est en attente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="c5142-140">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="c5142-141">Pour obtenir des informations détaillées sur l’erreur, appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="c5142-141">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="c5142-142">Remarques</span><span class="sxs-lookup"><span data-stu-id="c5142-142">Remarks</span></span>

<span data-ttu-id="c5142-143">Chaque élément du tableau *lpOutBuffer* est d’une longueur d’un octet.</span><span class="sxs-lookup"><span data-stu-id="c5142-143">Each element in the *lpOutBuffer* array is one byte in length.</span></span> <span data-ttu-id="c5142-144">Par conséquent, lors du retour, le paramètre *lpBytesReturned* indique le nombre de niveaux pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c5142-144">Therefore, upon return, the *lpBytesReturned* parameter indicates the number of supported levels.</span></span> <span data-ttu-id="c5142-145">Chaque niveau est une valeur comprise entre 0 et 100.</span><span class="sxs-lookup"><span data-stu-id="c5142-145">Each level is a value from 0 to 100.</span></span> <span data-ttu-id="c5142-146">Plus la valeur est grande, plus le rétroéclairage est clair.</span><span class="sxs-lookup"><span data-stu-id="c5142-146">The larger the value, the brighter the backlight.</span></span> <span data-ttu-id="c5142-147">Tous les niveaux sont pris en charge, que la source d’alimentation soit AC ou DC.</span><span class="sxs-lookup"><span data-stu-id="c5142-147">All levels are supported whether the power source is AC or DC.</span></span>

<span data-ttu-id="c5142-148">Le fichier d’en-tête utilisé pour créer des applications qui incluent cette fonctionnalité, Ntddvdeo. h, est inclus dans le kit de développement de pilotes (DDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="c5142-148">The header file used to build applications that include this functionality, Ntddvdeo.h, is included in the Microsoft Windows Driver Development Kit (DDK).</span></span> <span data-ttu-id="c5142-149">Pour plus d’informations sur l’obtention du DDK, consultez [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513) .</span><span class="sxs-lookup"><span data-stu-id="c5142-149">For information on obtaining the DDK, see [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513).</span></span>

<span data-ttu-id="c5142-150">Vous pouvez également définir ce code de contrôle comme suit :</span><span class="sxs-lookup"><span data-stu-id="c5142-150">Alternatively, you can define this control code as follows:</span></span>

``` syntax
#define IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS \
  CTL_CODE(FILE_DEVICE_VIDEO, 0x125, METHOD_BUFFERED, FILE_ANY_ACCESS)
```

## <a name="requirements"></a><span data-ttu-id="c5142-151">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c5142-151">Requirements</span></span>



| <span data-ttu-id="c5142-152">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c5142-152">Requirement</span></span> | <span data-ttu-id="c5142-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5142-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c5142-154">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c5142-154">Minimum supported client</span></span><br/> | <span data-ttu-id="c5142-155">Windows Vista, Windows XP avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c5142-155">Windows Vista, Windows XP with SP1 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="c5142-156">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c5142-156">Minimum supported server</span></span><br/> | <span data-ttu-id="c5142-157">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c5142-157">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c5142-158">En-tête</span><span class="sxs-lookup"><span data-stu-id="c5142-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5142-159"><dt>Ntddvdeo. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5142-159"><dt>Ntddvdeo.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5142-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5142-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5142-161">Interface de contrôle de rétroéclairage</span><span class="sxs-lookup"><span data-stu-id="c5142-161">Backlight Control Interface</span></span>](backlight-control-interface.md)
</dt> <dt>

[<span data-ttu-id="c5142-162">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="c5142-162">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> </dl>

 

