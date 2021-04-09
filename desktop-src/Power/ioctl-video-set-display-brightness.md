---
description: Définit les niveaux de rétroéclairage AC et DC actuels.
ms.assetid: baa77811-046d-4a07-b3df-2a31fba2d9a7
title: IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS le code de contrôle (Ntddvdeo. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS
api_type:
- HeaderDef
api_location:
- Ntddvdeo.h
ms.openlocfilehash: a0c679f352012eea66b80335bc3ad1547501dd92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951990"
---
# <a name="ioctl_video_set_display_brightness-control-code"></a><span data-ttu-id="a087f-103">\_Code de \_ contrôle de luminosité d' \_ affichage du jeu vidéo IOCTL \_</span><span class="sxs-lookup"><span data-stu-id="a087f-103">IOCTL\_VIDEO\_SET\_DISPLAY\_BRIGHTNESS control code</span></span>

<span data-ttu-id="a087f-104">Définit les niveaux de rétroéclairage AC et DC actuels.</span><span class="sxs-lookup"><span data-stu-id="a087f-104">Sets the current AC and DC backlight levels.</span></span>

<span data-ttu-id="a087f-105">Pour effectuer cette opération, appelez la fonction [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="a087f-105">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,            // handle to device
  IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS, // dwIoControlCode
  (LPVOID) lpInBuffer,         // input buffer
  (DWORD) nInBufferSize,       // size of the input buffer
  NULL,                        // lpOutBuffer
  0,                           // nOutBufferSize 
  (LPDWORD) lpBytesReturned,   // number of bytes returned
  (LPOVERLAPPED) lpOverlapped  // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="a087f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a087f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a087f-107">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="a087f-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="a087f-108">Handle de \\ \\ . \\ Appareil LCD.</span><span class="sxs-lookup"><span data-stu-id="a087f-108">A handle to the \\\\.\\LCD device.</span></span> <span data-ttu-id="a087f-109">Pour récupérer un handle d’appareil, appelez la fonction [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="a087f-109">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="a087f-110">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="a087f-110">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="a087f-111">Code de contrôle de l’opération.</span><span class="sxs-lookup"><span data-stu-id="a087f-111">The control code for the operation.</span></span> <span data-ttu-id="a087f-112">Cette valeur identifie l’opération spécifique à effectuer et le type d’appareil sur lequel l’exécuter.</span><span class="sxs-lookup"><span data-stu-id="a087f-112">This value identifies the specific operation to be performed and the type of device on which to perform it.</span></span> <span data-ttu-id="a087f-113">Utilisez la luminosité de l' **\_ affichage du jeu de vidéos \_ \_ \_ IOCTL** pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="a087f-113">Use **IOCTL\_VIDEO\_SET\_DISPLAY\_BRIGHTNESS** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="a087f-114">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="a087f-114">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="a087f-115">Pointeur vers une structure [**de \_ luminosité d’affichage**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a087f-115">A pointer to a [**DISPLAY\_BRIGHTNESS**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a087f-116">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="a087f-116">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="a087f-117">Taille de la mémoire tampon vers laquelle pointe *lpOutBuffer*, en octets.</span><span class="sxs-lookup"><span data-stu-id="a087f-117">The size of the buffer pointed to by *lpOutBuffer*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="a087f-118">*lpOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="a087f-118">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="a087f-119">Non utilisé avec cette opération ; Affectez la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="a087f-119">Not used with this operation; set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a087f-120">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="a087f-120">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="a087f-121">Non utilisé avec cette opération ; défini à zéro.</span><span class="sxs-lookup"><span data-stu-id="a087f-121">Not used with this operation; set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="a087f-122">*lpBytesReturned*</span><span class="sxs-lookup"><span data-stu-id="a087f-122">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="a087f-123">Pointeur vers une variable qui reçoit le nombre réel d’octets retournés par la fonction dans la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="a087f-123">A pointer to a variable that receives the actual count of bytes returned by the function in the output buffer.</span></span>

<span data-ttu-id="a087f-124">Si *lpOverlapped* a la **valeur null** (e/s nonoverlapped), *lpBytesReturned* est utilisé en interne et ne peut pas avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="a087f-124">If *lpOverlapped* is **NULL** (nonoverlapped I/O), *lpBytesReturned* is used internally and cannot be **NULL**.</span></span>

<span data-ttu-id="a087f-125">Si *lpOverlapped* n’a pas la **valeur null** (e/s avec chevauchement), *LpBytesReturned* peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="a087f-125">If *lpOverlapped* is not **NULL** (overlapped I/O), *lpBytesReturned* can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a087f-126">*lpOverlapped*</span><span class="sxs-lookup"><span data-stu-id="a087f-126">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="a087f-127">Pointeur vers une structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="a087f-127">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="a087f-128">Si *hDevice* a été ouvert avec l’indicateur de fichier avec \_ indicateur de \_ chevauchement, *lpOverlapped* doit pointer vers une structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) valide.</span><span class="sxs-lookup"><span data-stu-id="a087f-128">If *hDevice* was opened with the FILE\_FLAG\_OVERLAPPED flag, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span> <span data-ttu-id="a087f-129">Dans ce cas, l’opération est exécutée en tant qu’opération Overlapped (asynchrone).</span><span class="sxs-lookup"><span data-stu-id="a087f-129">In this case, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="a087f-130">Si l’appareil a été ouvert avec l’indicateur de fichier avec \_ indicateur \_ de chevauchement et que *LpOverlapped* a la **valeur null**, la fonction échoue de façon imprévisible.</span><span class="sxs-lookup"><span data-stu-id="a087f-130">If the device was opened with the FILE\_FLAG\_OVERLAPPED flag and *lpOverlapped* is **NULL**, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="a087f-131">Si *hDevice* a été ouvert sans que l’indicateur de fichier n’ait été spécifié \_ \_ , *lpOverlapped* est ignoré et [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) ne retourne pas tant que l’opération n’est pas terminée, ou jusqu’à ce qu’une erreur se produise.</span><span class="sxs-lookup"><span data-stu-id="a087f-131">If *hDevice* was opened without specifying the FILE\_FLAG\_OVERLAPPED flag, *lpOverlapped* is ignored and [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) does not return until the operation has been completed, or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a087f-132">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a087f-132">Return value</span></span>

<span data-ttu-id="a087f-133">Si l’opération se termine correctement, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="a087f-133">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="a087f-134">Si l’opération échoue ou est en attente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="a087f-134">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="a087f-135">Pour obtenir des informations détaillées sur l’erreur, appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="a087f-135">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="a087f-136">Remarques</span><span class="sxs-lookup"><span data-stu-id="a087f-136">Remarks</span></span>

<span data-ttu-id="a087f-137">Les valeurs spécifiées dans les membres **ucACBrightness** et **ucDCBrightness** de la structure de [**\_ luminosité d’affichage**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) doivent avoir été retournées par la luminosité de la [**\_ requête vidéo IOCTL \_ \_ prise en charge \_**](ioctl-video-query-supported-brightness.md).</span><span class="sxs-lookup"><span data-stu-id="a087f-137">The values specified in the **ucACBrightness** and **ucDCBrightness** members of the [**DISPLAY\_BRIGHTNESS**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) structure must have been previously returned by [**IOCTL\_VIDEO\_QUERY\_SUPPORTED\_BRIGHTNESS**](ioctl-video-query-supported-brightness.md).</span></span> <span data-ttu-id="a087f-138">Par exemple, si les valeurs prises en charge sont 10, 20, 30, 40, 50, 60, 70, 80, 90 et 100, l’utilisation d’une valeur de 33 serait une erreur.</span><span class="sxs-lookup"><span data-stu-id="a087f-138">For example, if the supported values are 10, 20, 30, 40, 50, 60, 70, 80, 90, and 100, then using a value of 33 would be an error.</span></span>

<span data-ttu-id="a087f-139">Le fichier d’en-tête utilisé pour créer des applications qui incluent cette fonctionnalité, Ntddvdeo. h, est inclus dans le kit de développement de pilotes (DDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="a087f-139">The header file used to build applications that include this functionality, Ntddvdeo.h, is included in the Microsoft Windows Driver Development Kit (DDK).</span></span> <span data-ttu-id="a087f-140">Pour plus d’informations sur l’obtention du DDK, consultez [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513) .</span><span class="sxs-lookup"><span data-stu-id="a087f-140">For information on obtaining the DDK, see [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513).</span></span>

<span data-ttu-id="a087f-141">Vous pouvez également définir ce code de contrôle comme suit :</span><span class="sxs-lookup"><span data-stu-id="a087f-141">Alternatively, you can define this control code as follows:</span></span>

``` syntax
#define IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS \
  CTL_CODE(FILE_DEVICE_VIDEO, 0x127, METHOD_BUFFERED, FILE_ANY_ACCESS)
```

## <a name="requirements"></a><span data-ttu-id="a087f-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a087f-142">Requirements</span></span>



| <span data-ttu-id="a087f-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a087f-143">Requirement</span></span> | <span data-ttu-id="a087f-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="a087f-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a087f-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a087f-145">Minimum supported client</span></span><br/> | <span data-ttu-id="a087f-146">Windows Vista, Windows XP avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a087f-146">Windows Vista, Windows XP with SP1 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="a087f-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a087f-147">Minimum supported server</span></span><br/> | <span data-ttu-id="a087f-148">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a087f-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a087f-149">En-tête</span><span class="sxs-lookup"><span data-stu-id="a087f-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="a087f-150"><dt>Ntddvdeo. h</dt></span><span class="sxs-lookup"><span data-stu-id="a087f-150"><dt>Ntddvdeo.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a087f-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a087f-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a087f-152">Interface de contrôle de rétroéclairage</span><span class="sxs-lookup"><span data-stu-id="a087f-152">Backlight Control Interface</span></span>](backlight-control-interface.md)
</dt> <dt>

[<span data-ttu-id="a087f-153">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="a087f-153">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

<span data-ttu-id="a087f-154">[**luminosité de l’affichage \_**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a087f-154">[**DISPLAY\_BRIGHTNESS**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="a087f-155">**luminosité de l' \_ \_ affichage des requêtes vidéo \_ IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="a087f-155">**IOCTL\_VIDEO\_QUERY\_DISPLAY\_BRIGHTNESS**</span></span>](ioctl-video-query-display-brightness.md)
</dt> <dt>

[<span data-ttu-id="a087f-156">**\_ \_ \_ luminosité prise en charge des requêtes de vidéo IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="a087f-156">**IOCTL\_VIDEO\_QUERY\_SUPPORTED\_BRIGHTNESS**</span></span>](ioctl-video-query-supported-brightness.md)
</dt> </dl>

 

