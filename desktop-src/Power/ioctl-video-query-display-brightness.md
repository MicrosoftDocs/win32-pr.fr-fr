---
description: Récupère les niveaux de rétroéclairage AC et DC actuels et l’état d’alimentation actuel.
ms.assetid: c7b7c302-6e92-46a7-b9a6-e3f2a3e44d1b
title: IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS le code de contrôle (Ntddvdeo. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS
api_type:
- HeaderDef
api_location:
- Ntddvdeo.h
ms.openlocfilehash: 547501a28492aecfe06f63f95b0e007fc80d3d02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519896"
---
# <a name="ioctl_video_query_display_brightness-control-code"></a><span data-ttu-id="787e8-103">Code de contrôle de luminosité de l' \_ \_ affichage des requêtes vidéo \_ IOCTL \_</span><span class="sxs-lookup"><span data-stu-id="787e8-103">IOCTL\_VIDEO\_QUERY\_DISPLAY\_BRIGHTNESS control code</span></span>

<span data-ttu-id="787e8-104">\[Ce code de contrôle peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="787e8-104">\[This control code is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="787e8-105">La prise en charge de ce code de contrôle a été supprimée dans Windows Server 2008 et Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="787e8-105">Support for this control code was removed in Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="787e8-106">Utilisez la classe [**WmiMonitorBrightness**](/windows/desktop/WmiCoreProv/wmimonitorbrightness) à la place.\]</span><span class="sxs-lookup"><span data-stu-id="787e8-106">Use the [**WmiMonitorBrightness**](/windows/desktop/WmiCoreProv/wmimonitorbrightness) class instead.\]</span></span>

<span data-ttu-id="787e8-107">Récupère les niveaux de rétroéclairage AC et DC actuels et l’état d’alimentation actuel.</span><span class="sxs-lookup"><span data-stu-id="787e8-107">Retrieves the current AC and DC backlight levels and the current power state.</span></span>

<span data-ttu-id="787e8-108">Pour effectuer cette opération, appelez la fonction [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="787e8-108">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,                // handle to device
  IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS,  // dwIoControlCode
  NULL,                            // lpInBuffer
  0,                               // nInBufferSize
  (LPVOID) lpOutBuffer,            // output buffer
  (DWORD) nOutBufferSize,          // size of output buffer
  (LPDWORD) lpBytesReturned,       // number of bytes returned
  (LPOVERLAPPED) lpOverlapped      // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="787e8-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="787e8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="787e8-110">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="787e8-110">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="787e8-111">Handle de \\ \\ . \\ Appareil LCD.</span><span class="sxs-lookup"><span data-stu-id="787e8-111">A handle to the \\\\.\\LCD device.</span></span> <span data-ttu-id="787e8-112">Pour récupérer un handle d’appareil, appelez la fonction [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="787e8-112">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="787e8-113">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="787e8-113">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="787e8-114">Code de contrôle de l’opération.</span><span class="sxs-lookup"><span data-stu-id="787e8-114">The control code for the operation.</span></span> <span data-ttu-id="787e8-115">Cette valeur identifie l’opération spécifique à effectuer et le type d’appareil sur lequel l’exécuter.</span><span class="sxs-lookup"><span data-stu-id="787e8-115">This value identifies the specific operation to be performed and the type of device on which to perform it.</span></span> <span data-ttu-id="787e8-116">Utilisez la luminosité de l' **\_ \_ \_ affichage \_ des requêtes vidéo IOCTL** pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="787e8-116">Use **IOCTL\_VIDEO\_QUERY\_DISPLAY\_BRIGHTNESS** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="787e8-117">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="787e8-117">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="787e8-118">Non utilisé avec cette opération ; Affectez la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="787e8-118">Not used with this operation; set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="787e8-119">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="787e8-119">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="787e8-120">Non utilisé avec cette opération ; défini à zéro.</span><span class="sxs-lookup"><span data-stu-id="787e8-120">Not used with this operation; set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="787e8-121">*lpOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="787e8-121">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="787e8-122">Pointeur vers une mémoire tampon qui reçoit une structure [**de \_ luminosité**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="787e8-122">A pointer to a buffer that will receive a [**DISPLAY\_BRIGHTNESS**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) structure.</span></span>

</dd> <dt>

<span data-ttu-id="787e8-123">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="787e8-123">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="787e8-124">Taille de la mémoire tampon de sortie en octets.</span><span class="sxs-lookup"><span data-stu-id="787e8-124">The size of the output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="787e8-125">*lpBytesReturned*</span><span class="sxs-lookup"><span data-stu-id="787e8-125">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="787e8-126">Pointeur vers une variable qui reçoit la taille, en octets, des données de sortie retournées.</span><span class="sxs-lookup"><span data-stu-id="787e8-126">A pointer to a variable that receives the size, in bytes, of output data returned.</span></span>

<span data-ttu-id="787e8-127">Si la mémoire tampon de sortie est trop petite pour retourner des données, l’appel échoue, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne l’erreur de code d’erreur \_ mémoire tampon insuffisante \_ et le nombre d’octets retournés est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="787e8-127">If the output buffer is too small to return any data, then the call fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code ERROR\_INSUFFICIENT\_BUFFER, and the returned byte count is zero.</span></span>

<span data-ttu-id="787e8-128">Si la mémoire tampon de sortie est trop petite pour contenir toutes les données mais peut contenir des entrées, le système d’exploitation retourne autant d’éléments que vous le souhaitez, l’appel échoue, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne le code d’erreur \_ plus de \_ données, et *lpBytesReturned* indique la quantité de données retournées.</span><span class="sxs-lookup"><span data-stu-id="787e8-128">If the output buffer is too small to hold all of the data but can hold some entries, then the operating system returns as much as fits, the call fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code ERROR\_MORE\_DATA, and *lpBytesReturned* indicates the amount of data returned.</span></span> <span data-ttu-id="787e8-129">Votre application doit à nouveau appeler [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) avec la même opération, en spécifiant un nouveau point de départ.</span><span class="sxs-lookup"><span data-stu-id="787e8-129">Your application should call [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) again with the same operation, specifying a new starting point.</span></span>

<span data-ttu-id="787e8-130">Si *lpOverlapped* a la **valeur null** (e/s nonoverlapped), *lpBytesReturned* ne peut pas avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="787e8-130">If *lpOverlapped* is **NULL** (nonoverlapped I/O), *lpBytesReturned* cannot be **NULL**.</span></span>

<span data-ttu-id="787e8-131">Si *lpOverlapped* n’a pas la **valeur null** (e/s avec chevauchement), *LpBytesReturned* peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="787e8-131">If *lpOverlapped* is not **NULL** (overlapped I/O), *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="787e8-132">S’il s’agit d’une opération avec chevauchement, vous pouvez récupérer le nombre d’octets retournés en appelant la fonction [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) .</span><span class="sxs-lookup"><span data-stu-id="787e8-132">If this is an overlapped operation, you can retrieve the number of bytes returned by calling the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="787e8-133">Si *hDevice* est associé à un port de terminaison d’e/s, vous pouvez récupérer le nombre d’octets renvoyés en appelant la fonction [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="787e8-133">If *hDevice* is associated with an I/O completion port, you can get the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="787e8-134">*lpOverlapped*</span><span class="sxs-lookup"><span data-stu-id="787e8-134">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="787e8-135">Pointeur vers une structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="787e8-135">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="787e8-136">Si *hDevice* a été ouvert avec l’indicateur de fichier avec \_ indicateur de \_ chevauchement, *lpOverlapped* doit pointer vers une structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) valide.</span><span class="sxs-lookup"><span data-stu-id="787e8-136">If *hDevice* was opened with the FILE\_FLAG\_OVERLAPPED flag, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span> <span data-ttu-id="787e8-137">Dans ce cas, l’opération est exécutée en tant qu’opération Overlapped (asynchrone).</span><span class="sxs-lookup"><span data-stu-id="787e8-137">In this case, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="787e8-138">Si l’appareil a été ouvert avec l’indicateur de fichier avec \_ indicateur \_ de chevauchement et que *LpOverlapped* a la **valeur null**, la fonction échoue de façon imprévisible.</span><span class="sxs-lookup"><span data-stu-id="787e8-138">If the device was opened with the FILE\_FLAG\_OVERLAPPED flag and *lpOverlapped* is **NULL**, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="787e8-139">Si *hDevice* a été ouvert sans que l’indicateur de fichier n’ait été spécifié \_ \_ , *lpOverlapped* est ignoré et [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) ne retourne pas tant que l’opération n’est pas terminée, ou jusqu’à ce qu’une erreur se produise.</span><span class="sxs-lookup"><span data-stu-id="787e8-139">If *hDevice* was opened without specifying the FILE\_FLAG\_OVERLAPPED flag, *lpOverlapped* is ignored and [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) does not return until the operation has been completed, or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="787e8-140">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="787e8-140">Return value</span></span>

<span data-ttu-id="787e8-141">Si l’opération se termine correctement, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="787e8-141">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="787e8-142">Si l’opération échoue ou est en attente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="787e8-142">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="787e8-143">Pour obtenir des informations détaillées sur l’erreur, appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="787e8-143">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="787e8-144">Remarques</span><span class="sxs-lookup"><span data-stu-id="787e8-144">Remarks</span></span>

<span data-ttu-id="787e8-145">Le fichier d’en-tête utilisé pour créer des applications qui incluent cette fonctionnalité, Ntddvdeo. h, est inclus dans le kit de développement de pilotes (DDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="787e8-145">The header file used to build applications that include this functionality, Ntddvdeo.h, is included in the Microsoft Windows Driver Development Kit (DDK).</span></span> <span data-ttu-id="787e8-146">Pour plus d’informations sur l’obtention du DDK, consultez [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513) .</span><span class="sxs-lookup"><span data-stu-id="787e8-146">For information on obtaining the DDK, see [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513).</span></span>

<span data-ttu-id="787e8-147">Vous pouvez également définir ce code de contrôle comme suit :</span><span class="sxs-lookup"><span data-stu-id="787e8-147">Alternatively, you can define this control code as follows:</span></span>

``` syntax
#define IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS \
  CTL_CODE(FILE_DEVICE_VIDEO, 0x126, METHOD_BUFFERED, FILE_ANY_ACCESS)
```

## <a name="requirements"></a><span data-ttu-id="787e8-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="787e8-148">Requirements</span></span>



| <span data-ttu-id="787e8-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="787e8-149">Requirement</span></span> | <span data-ttu-id="787e8-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="787e8-150">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="787e8-151">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="787e8-151">Minimum supported client</span></span><br/> | <span data-ttu-id="787e8-152">Windows XP avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="787e8-152">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="787e8-153">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="787e8-153">Minimum supported server</span></span><br/> | <span data-ttu-id="787e8-154">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="787e8-154">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="787e8-155">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="787e8-155">End of client support</span></span><br/>    | <span data-ttu-id="787e8-156">Windows XP SP2</span><span class="sxs-lookup"><span data-stu-id="787e8-156">Windows XP with SP2</span></span><br/>                                                        |
| <span data-ttu-id="787e8-157">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="787e8-157">End of server support</span></span><br/>    | <span data-ttu-id="787e8-158">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="787e8-158">Windows Server 2003 R2</span></span><br/>                                                     |
| <span data-ttu-id="787e8-159">En-tête</span><span class="sxs-lookup"><span data-stu-id="787e8-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="787e8-160"><dt>Ntddvdeo. h</dt></span><span class="sxs-lookup"><span data-stu-id="787e8-160"><dt>Ntddvdeo.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="787e8-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="787e8-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="787e8-162">Interface de contrôle de rétroéclairage</span><span class="sxs-lookup"><span data-stu-id="787e8-162">Backlight Control Interface</span></span>](backlight-control-interface.md)
</dt> <dt>

[<span data-ttu-id="787e8-163">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="787e8-163">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

<span data-ttu-id="787e8-164">[**luminosité de l’affichage \_**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="787e8-164">[**DISPLAY\_BRIGHTNESS**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="787e8-165">**luminosité de l’affichage du jeu de \_ vidéos IOCTL \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="787e8-165">**IOCTL\_VIDEO\_SET\_DISPLAY\_BRIGHTNESS**</span></span>](ioctl-video-set-display-brightness.md)
</dt> </dl>

 

