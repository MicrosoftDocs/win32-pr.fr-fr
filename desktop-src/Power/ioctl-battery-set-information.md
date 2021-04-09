---
description: Définit différentes informations sur la batterie.
ms.assetid: b827983d-5fb8-43f2-b732-541d16b3eb7b
title: IOCTL_BATTERY_SET_INFORMATION le code de contrôle (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_BATTERY_SET_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: f540037486f16e920b3346620ff934b279652e7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865081"
---
# <a name="ioctl_battery_set_information-control-code"></a><span data-ttu-id="92a6b-103">\_Code de \_ contrôle des informations du jeu de batteries IOCTL \_</span><span class="sxs-lookup"><span data-stu-id="92a6b-103">IOCTL\_BATTERY\_SET\_INFORMATION control code</span></span>

<span data-ttu-id="92a6b-104">Définit différentes informations sur la batterie.</span><span class="sxs-lookup"><span data-stu-id="92a6b-104">Sets various battery information.</span></span> <span data-ttu-id="92a6b-105">La structure des paramètres d’entrée, les [**\_ \_ informations sur le jeu de batteries**](battery-set-information-str.md), indiquent les informations d’état de la batterie à définir.</span><span class="sxs-lookup"><span data-stu-id="92a6b-105">The input parameter structure, [**BATTERY\_SET\_INFORMATION**](battery-set-information-str.md), indicates which battery status information is to be set.</span></span>

<span data-ttu-id="92a6b-106">Pour effectuer cette opération, appelez la fonction [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="92a6b-106">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,              // handle to battery
  IOCTL_BATTERY_SET_INFORMATION, // dwIoControlCode
  (LPVOID) lpInBuffer,           // input buffer
  (DWORD) nInBufferSize,         // size of input buffer
  NULL,                          // lpOutBuffer
  0,                             // nOutBufferSize
  (LPDWORD) lpBytesReturned,     // number of bytes returned
  (LPOVERLAPPED) lpOverlapped    // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="92a6b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="92a6b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92a6b-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="92a6b-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="92a6b-109">Handle vers la batterie sur laquelle les informations doivent être définies.</span><span class="sxs-lookup"><span data-stu-id="92a6b-109">A handle to the battery on which the information is to be set.</span></span> <span data-ttu-id="92a6b-110">Pour récupérer un handle d’appareil, appelez la fonction [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="92a6b-110">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="92a6b-111">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="92a6b-111">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="92a6b-112">Code de contrôle de l’opération.</span><span class="sxs-lookup"><span data-stu-id="92a6b-112">The control code for the operation.</span></span> <span data-ttu-id="92a6b-113">Cette valeur identifie l’opération spécifique à effectuer et le type d’appareil sur lequel l’exécuter.</span><span class="sxs-lookup"><span data-stu-id="92a6b-113">This value identifies the specific operation to be performed and the type of device on which to perform it.</span></span> <span data-ttu-id="92a6b-114">Utilisez **les \_ \_ \_ informations du jeu de piles IOCTL** pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="92a6b-114">Use **IOCTL\_BATTERY\_SET\_INFORMATION** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="92a6b-115">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="92a6b-115">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="92a6b-116">Pointeur vers une structure [**d' \_ \_ informations d’ensemble de batteries**](battery-set-information-str.md) .</span><span class="sxs-lookup"><span data-stu-id="92a6b-116">A pointer to a [**BATTERY\_SET\_INFORMATION**](battery-set-information-str.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="92a6b-117">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="92a6b-117">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="92a6b-118">Taille de la mémoire tampon d’entrée, en octets.</span><span class="sxs-lookup"><span data-stu-id="92a6b-118">The size of the input buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="92a6b-119">*lpOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="92a6b-119">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="92a6b-120">Non utilisé avec cette opération ; Affectez la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="92a6b-120">Not used with this operation; set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="92a6b-121">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="92a6b-121">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="92a6b-122">Non utilisé avec cette opération ; défini à zéro.</span><span class="sxs-lookup"><span data-stu-id="92a6b-122">Not used with this operation; set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="92a6b-123">*lpBytesReturned*</span><span class="sxs-lookup"><span data-stu-id="92a6b-123">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="92a6b-124">Pointeur vers une variable qui reçoit la taille des données retournées dans la mémoire tampon *lpOutBuffer* , en octets.</span><span class="sxs-lookup"><span data-stu-id="92a6b-124">A pointer to a variable that receives the size of data returned in the *lpOutBuffer* buffer, in bytes.</span></span>

<span data-ttu-id="92a6b-125">Si la mémoire tampon de sortie est trop petite pour retourner des données, l’appel échoue, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne l’erreur de code d’erreur \_ mémoire tampon insuffisante \_ et le nombre d’octets retournés est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="92a6b-125">If the output buffer is too small to return any data, then the call fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code ERROR\_INSUFFICIENT\_BUFFER, and the returned byte count is zero.</span></span>

<span data-ttu-id="92a6b-126">Si *lpOverlapped* a la **valeur null** (e/s nonoverlapped), *lpBytesReturned* ne peut pas avoir la **valeur null**, même si *lpOutBuffer* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="92a6b-126">If *lpOverlapped* is **NULL** (nonoverlapped I/O), *lpBytesReturned* cannot be **NULL**, even if *lpOutBuffer* is **NULL**.</span></span>

<span data-ttu-id="92a6b-127">Si *lpOverlapped* n’a pas la **valeur null** (e/s avec chevauchement), *LpBytesReturned* peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="92a6b-127">If *lpOverlapped* is not **NULL** (overlapped I/O), *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="92a6b-128">S’il s’agit d’une opération avec chevauchement, vous pouvez récupérer le nombre d’octets retournés en appelant la fonction [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) .</span><span class="sxs-lookup"><span data-stu-id="92a6b-128">If this is an overlapped operation, you can retrieve the number of bytes returned by calling the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="92a6b-129">Si *hDevice* est associé à un port de terminaison d’e/s, vous pouvez récupérer le nombre d’octets renvoyés en appelant la fonction [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="92a6b-129">If *hDevice* is associated with an I/O completion port, you can get the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="92a6b-130">*lpOverlapped*</span><span class="sxs-lookup"><span data-stu-id="92a6b-130">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="92a6b-131">Pointeur vers une structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="92a6b-131">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="92a6b-132">Si *hDevice* a été ouvert avec l’indicateur de fichier avec \_ indicateur de \_ chevauchement, *lpOverlapped* doit pointer vers une structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) valide.</span><span class="sxs-lookup"><span data-stu-id="92a6b-132">If *hDevice* was opened with the FILE\_FLAG\_OVERLAPPED flag, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span> <span data-ttu-id="92a6b-133">Dans ce cas, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) est exécuté comme une opération Overlapped (asynchrone).</span><span class="sxs-lookup"><span data-stu-id="92a6b-133">In this case, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="92a6b-134">Si l’appareil a été ouvert avec l’indicateur de fichier avec \_ indicateur \_ de chevauchement et que *LpOverlapped* a la **valeur null**, la fonction échoue de façon imprévisible.</span><span class="sxs-lookup"><span data-stu-id="92a6b-134">If the device was opened with the FILE\_FLAG\_OVERLAPPED flag and *lpOverlapped* is **NULL**, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="92a6b-135">Si *hDevice* a été ouvert sans que l’indicateur de fichier n’ait été spécifié \_ \_ , *lpOverlapped* est ignoré et la fonction [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) ne retourne pas tant que l’opération n’est pas terminée, soit jusqu’à ce qu’une erreur se produise.</span><span class="sxs-lookup"><span data-stu-id="92a6b-135">If *hDevice* was opened without specifying the FILE\_FLAG\_OVERLAPPED flag, *lpOverlapped* is ignored and the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function does not return until the operation has been completed, or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92a6b-136">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="92a6b-136">Return value</span></span>

<span data-ttu-id="92a6b-137">Si l’opération se termine correctement, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="92a6b-137">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="92a6b-138">Si l’opération échoue ou est en attente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="92a6b-138">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="92a6b-139">Pour obtenir des informations détaillées sur l’erreur, appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="92a6b-139">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="92a6b-140">Remarques</span><span class="sxs-lookup"><span data-stu-id="92a6b-140">Remarks</span></span>

<span data-ttu-id="92a6b-141">Toutes les demandes de définition des informations sur la batterie se terminent avec l’État fichier d’erreur \_ \_ \_ introuvable si la balise de batterie de la demande ne correspond pas à celle de la balise de batterie actuelle.</span><span class="sxs-lookup"><span data-stu-id="92a6b-141">All requests to set battery information will complete with the status of ERROR\_FILE\_NOT\_FOUND if the battery tag of the request does not match that of the current battery tag.</span></span>

<span data-ttu-id="92a6b-142">Pour connaître les implications des e/s avec chevauchement sur cette opération, consultez la section Notes de la rubrique [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) .</span><span class="sxs-lookup"><span data-stu-id="92a6b-142">For the implications of overlapped I/O on this operation, see the Remarks section of the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) topic.</span></span>

## <a name="requirements"></a><span data-ttu-id="92a6b-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="92a6b-143">Requirements</span></span>



| <span data-ttu-id="92a6b-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="92a6b-144">Requirement</span></span> | <span data-ttu-id="92a6b-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="92a6b-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92a6b-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="92a6b-146">Minimum supported client</span></span><br/> | <span data-ttu-id="92a6b-147">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="92a6b-147">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="92a6b-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="92a6b-148">Minimum supported server</span></span><br/> | <span data-ttu-id="92a6b-149">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="92a6b-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="92a6b-150">En-tête</span><span class="sxs-lookup"><span data-stu-id="92a6b-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="92a6b-151"><dt>Poclass. h ; </dt> <dt>Batclass. h sur Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 et Windows XP</dt></span><span class="sxs-lookup"><span data-stu-id="92a6b-151"><dt>Poclass.h; </dt> <dt>Batclass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92a6b-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92a6b-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92a6b-153">Informations sur la batterie</span><span class="sxs-lookup"><span data-stu-id="92a6b-153">Battery Information</span></span>](battery-information.md)
</dt> <dt>

[<span data-ttu-id="92a6b-154">Codes de contrôle de gestion de l’alimentation</span><span class="sxs-lookup"><span data-stu-id="92a6b-154">Power Management Control Codes</span></span>](power-management-control-codes.md)
</dt> <dt>

[<span data-ttu-id="92a6b-155">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="92a6b-155">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="92a6b-156">**\_informations sur le jeu de batteries \_**</span><span class="sxs-lookup"><span data-stu-id="92a6b-156">**BATTERY\_SET\_INFORMATION**</span></span>](battery-set-information-str.md)
</dt> <dt>

[<span data-ttu-id="92a6b-157">**\_ \_ informations sur les requêtes de batterie IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="92a6b-157">**IOCTL\_BATTERY\_QUERY\_INFORMATION**</span></span>](ioctl-battery-query-information.md)
</dt> <dt>

[<span data-ttu-id="92a6b-158">**État de la \_ requête de batterie IOCTL \_ \_**</span><span class="sxs-lookup"><span data-stu-id="92a6b-158">**IOCTL\_BATTERY\_QUERY\_STATUS**</span></span>](ioctl-battery-query-status.md)
</dt> <dt>

[<span data-ttu-id="92a6b-159">**\_ \_ balise de requête de batterie IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="92a6b-159">**IOCTL\_BATTERY\_QUERY\_TAG**</span></span>](ioctl-battery-query-tag.md)
</dt> </dl>

 

