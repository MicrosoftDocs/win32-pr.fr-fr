---
description: Récupère la balise actuelle des piles.
ms.assetid: 0bbe59ba-e037-47ce-a54a-6500ea7c9bc5
title: IOCTL_BATTERY_QUERY_TAG le code de contrôle (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_BATTERY_QUERY_TAG
api_type:
- HeaderDef
api_location:
- Poclass.h
- BatClass.h
ms.openlocfilehash: 1d8435e62c4f061ac13b3e18e5bcd64afcb399c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517079"
---
# <a name="ioctl_battery_query_tag-control-code"></a><span data-ttu-id="0697f-103">\_Code de \_ contrôle de balise de requête de batterie IOCTL \_</span><span class="sxs-lookup"><span data-stu-id="0697f-103">IOCTL\_BATTERY\_QUERY\_TAG control code</span></span>

<span data-ttu-id="0697f-104">Récupère la balise actuelle de la batterie.</span><span class="sxs-lookup"><span data-stu-id="0697f-104">Retrieves the battery's current tag.</span></span>

<span data-ttu-id="0697f-105">Pour effectuer cette opération, appelez la fonction [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="0697f-105">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,            // handle to battery
  IOCTL_BATTERY_QUERY_TAG,     // dwIoControlCode
  (LPVOID) lpInBuffer,         // input buffer
  (DWORD) nInBufferSize,       // size of input buffer
  (LPVOID) lpOutBuffer,        // output buffer
  (DWORD) nOutBufferSize,      // size of output buffer
  (LPDWORD) lpBytesReturned,   // number of bytes returned
  (LPOVERLAPPED) lpOverlapped);// OVERLAPPED structure
```



## <a name="parameters"></a><span data-ttu-id="0697f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0697f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0697f-107">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="0697f-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="0697f-108">Handle de la batterie à partir de laquelle la balise doit être récupérée.</span><span class="sxs-lookup"><span data-stu-id="0697f-108">A handle to the battery from which the tag is to be retrieved.</span></span> <span data-ttu-id="0697f-109">Pour récupérer un handle d’appareil, appelez la fonction [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="0697f-109">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="0697f-110">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="0697f-110">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="0697f-111">Code de contrôle de l’opération.</span><span class="sxs-lookup"><span data-stu-id="0697f-111">The control code for the operation.</span></span> <span data-ttu-id="0697f-112">Cette valeur identifie l’opération spécifique à effectuer et le type d’appareil sur lequel l’exécuter.</span><span class="sxs-lookup"><span data-stu-id="0697f-112">This value identifies the specific operation to be performed and the type of device on which to perform it.</span></span> <span data-ttu-id="0697f-113">Utilisez **la \_ \_ \_ balise de requête de batterie IOCTL** pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="0697f-113">Use **IOCTL\_BATTERY\_QUERY\_TAG** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="0697f-114">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="0697f-114">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="0697f-115">Pointeur vers une mémoire tampon d’entrée **ULong** .</span><span class="sxs-lookup"><span data-stu-id="0697f-115">A pointer to a **ULONG** input buffer.</span></span> <span data-ttu-id="0697f-116">La valeur indique le nombre de millisecondes à attendre s’il n’y a aucune batterie.</span><span class="sxs-lookup"><span data-stu-id="0697f-116">The value indicates the number of milliseconds to wait if there is no battery.</span></span> <span data-ttu-id="0697f-117">La valeur-1 indique que la demande attend indéfiniment (ou jusqu’à ce qu’elle soit annulée par un autre événement).</span><span class="sxs-lookup"><span data-stu-id="0697f-117">A value of -1 indicates the request will wait indefinitely (or until canceled by some other event).</span></span>

</dd> <dt>

<span data-ttu-id="0697f-118">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="0697f-118">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="0697f-119">Taille de la mémoire tampon d’entrée, en octets.</span><span class="sxs-lookup"><span data-stu-id="0697f-119">The size of the input buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="0697f-120">*lpOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="0697f-120">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="0697f-121">Pointeur vers une mémoire tampon de sortie **ULong** .</span><span class="sxs-lookup"><span data-stu-id="0697f-121">A pointer to a **ULONG** output buffer.</span></span> <span data-ttu-id="0697f-122">En cas de réussite, cette mémoire tampon contient la balise de batterie actuelle, qui peut être toute valeur à l’exception de la \_ balise de batterie \_ non valide.</span><span class="sxs-lookup"><span data-stu-id="0697f-122">On success this buffer contains the current battery tag, which can be any value except BATTERY\_TAG\_INVALID.</span></span> <span data-ttu-id="0697f-123">En cas d’échec, si [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne le fichier d’erreur de code d’erreur **\_ \_ \_ introuvable**, cette mémoire tampon contient la **balise de batterie de valeur \_ \_ non valide**.</span><span class="sxs-lookup"><span data-stu-id="0697f-123">On failure, if [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code **ERROR\_FILE\_NOT\_FOUND**, this buffer contains the value **BATTERY\_TAG\_INVALID**.</span></span>

</dd> <dt>

<span data-ttu-id="0697f-124">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="0697f-124">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="0697f-125">Taille de la mémoire tampon de sortie en octets.</span><span class="sxs-lookup"><span data-stu-id="0697f-125">The size of the output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="0697f-126">*lpBytesReturned*</span><span class="sxs-lookup"><span data-stu-id="0697f-126">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="0697f-127">Pointeur vers une variable qui reçoit la taille des données stockées dans la mémoire tampon *lpOutBuffer* , en octets.</span><span class="sxs-lookup"><span data-stu-id="0697f-127">A pointer to a variable that receives the size of the data stored in the *lpOutBuffer* buffer, in bytes.</span></span>

<span data-ttu-id="0697f-128">Si la mémoire tampon de sortie est trop petite pour retourner des données, alors l’appel échoue, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne l’erreur de code d’erreur **\_ \_ mémoire tampon insuffisante** et le nombre d’octets retourné est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="0697f-128">If the output buffer is too small to return any data then the call fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code **ERROR\_INSUFFICIENT\_BUFFER**, and the returned byte count is zero.</span></span>

<span data-ttu-id="0697f-129">Si *lpOverlapped* a la **valeur null** (e/s nonoverlapped), *lpBytesReturned* ne peut pas avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="0697f-129">If *lpOverlapped* is **NULL** (nonoverlapped I/O), *lpBytesReturned* cannot be **NULL**.</span></span>

<span data-ttu-id="0697f-130">Si *lpOverlapped* n’a pas la **valeur null** (e/s avec chevauchement), *LpBytesReturned* peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="0697f-130">If *lpOverlapped* is not **NULL** (overlapped I/O), *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="0697f-131">S’il s’agit d’une opération avec chevauchement, vous pouvez récupérer le nombre d’octets retournés en appelant la fonction [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) .</span><span class="sxs-lookup"><span data-stu-id="0697f-131">If this is an overlapped operation, you can retrieve the number of bytes returned by calling the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="0697f-132">Si *hDevice* est associé à un port de terminaison d’e/s, vous pouvez récupérer le nombre d’octets renvoyés en appelant la fonction [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="0697f-132">If *hDevice* is associated with an I/O completion port, you can get the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="0697f-133">*lpOverlapped*</span><span class="sxs-lookup"><span data-stu-id="0697f-133">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="0697f-134">Pointeur vers une structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="0697f-134">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="0697f-135">Si *hDevice* a été ouvert avec l’indicateur de **fichier avec indicateur de \_ \_ chevauchement** , *LPOVERLAPPED* doit pointer vers une structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) valide.</span><span class="sxs-lookup"><span data-stu-id="0697f-135">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span> <span data-ttu-id="0697f-136">Dans ce cas, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) est exécuté comme une opération Overlapped (asynchrone).</span><span class="sxs-lookup"><span data-stu-id="0697f-136">In this case, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="0697f-137">Si l’appareil a été ouvert avec l’indicateur de **fichier avec \_ indicateur de \_ chevauchement** et que *lpOverlapped* a la **valeur null**, la fonction échoue de façon imprévisible.</span><span class="sxs-lookup"><span data-stu-id="0697f-137">If the device was opened with the **FILE\_FLAG\_OVERLAPPED** flag and *lpOverlapped* is **NULL**, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="0697f-138">Si *hDevice* a été ouvert sans que l’indicateur de fichier n’ait été spécifié, *lpOverlapped* est ignoré et la fonction [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) ne retourne pas tant que l’opération n’est pas terminée, soit jusqu’à ce qu’une erreur se produise. **\_ \_**</span><span class="sxs-lookup"><span data-stu-id="0697f-138">If *hDevice* was opened without specifying the **FILE\_FLAG\_OVERLAPPED** flag, *lpOverlapped* is ignored and the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function does not return until the operation has been completed, or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0697f-139">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0697f-139">Return value</span></span>

<span data-ttu-id="0697f-140">Si l’opération se termine correctement, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="0697f-140">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="0697f-141">Si l’opération échoue ou est en attente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="0697f-141">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="0697f-142">Pour obtenir des informations détaillées sur l’erreur, appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="0697f-142">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="0697f-143">Remarques</span><span class="sxs-lookup"><span data-stu-id="0697f-143">Remarks</span></span>

<span data-ttu-id="0697f-144">Cette IOCTL de batterie récupère la balise actuelle de la batterie.</span><span class="sxs-lookup"><span data-stu-id="0697f-144">This battery IOCTL retrieves the battery's current tag.</span></span> <span data-ttu-id="0697f-145">La balise de batterie est une valeur différente de zéro unique qui change lorsque la batterie physique est réinsérée, remplacée ou subit des modifications caractéristiques.</span><span class="sxs-lookup"><span data-stu-id="0697f-145">The battery tag is a unique nonzero value that changes when the physical battery is reinserted, replaced, or undergoes any characteristic changes.</span></span> <span data-ttu-id="0697f-146">Consultez la section balises de batterie dans la rubrique vue d’ensemble des informations sur la batterie pour plus d' [informations](battery-information.md) sur la modification d’une balise de batterie, sur la façon de détecter la modification et sur la manière dont une application doit se poursuivre après une modification de la balise de batterie.</span><span class="sxs-lookup"><span data-stu-id="0697f-146">See the Battery Tags section in the [Battery Information](battery-information.md) overview topic for more detail on when a battery tag changes, how to detect the change, and how an application should proceed after a battery tag change.</span></span> <span data-ttu-id="0697f-147">Lorsqu’une batterie n’est pas présente, cette demande attend l’heure indiquée et, si aucune batterie n’est présente, elle retourne le fichier d' **erreur \_ \_ \_ introuvable** et définit la balise de batterie sur la **\_ balise de batterie \_ non valide**.</span><span class="sxs-lookup"><span data-stu-id="0697f-147">When a battery is not present, this request will wait the indicated time, and if there is still no battery present, then it will return **ERROR\_FILE\_NOT\_FOUND** and set the battery tag to **BATTERY\_TAG\_INVALID**.</span></span> <span data-ttu-id="0697f-148">(Pour plus d’informations, consultez les informations relatives à la batterie.)</span><span class="sxs-lookup"><span data-stu-id="0697f-148">(See Battery Information for more information.)</span></span>

<span data-ttu-id="0697f-149">Toutes les demandes d’autres informations sur la batterie requièrent que l’appelant fournisse la balise de batterie correspondante.</span><span class="sxs-lookup"><span data-stu-id="0697f-149">All requests for other battery information require the caller to supply the matching battery tag.</span></span> <span data-ttu-id="0697f-150">Cela garantit que l’appelant reçoit des informations pour la même batterie pour chaque demande et s’assure que l’appelant est conscient des modifications de la batterie sans interrogation constante.</span><span class="sxs-lookup"><span data-stu-id="0697f-150">This ensures that the caller is receiving information for the same battery for every request and ensures that the caller is aware of battery changes without constant polling.</span></span>

<span data-ttu-id="0697f-151">Pour connaître les implications des e/s avec chevauchement sur cette opération, consultez la section Notes de la rubrique [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) .</span><span class="sxs-lookup"><span data-stu-id="0697f-151">For the implications of overlapped I/O on this operation, see the Remarks section of the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) topic.</span></span>

## <a name="examples"></a><span data-ttu-id="0697f-152">Exemples</span><span class="sxs-lookup"><span data-stu-id="0697f-152">Examples</span></span>

<span data-ttu-id="0697f-153">Pour obtenir un exemple, consultez [énumération des unités de batterie](enumerating-battery-devices.md).</span><span class="sxs-lookup"><span data-stu-id="0697f-153">For an example, see [Enumerating Battery Devices](enumerating-battery-devices.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0697f-154">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0697f-154">Requirements</span></span>



| <span data-ttu-id="0697f-155">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0697f-155">Requirement</span></span> | <span data-ttu-id="0697f-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="0697f-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0697f-157">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0697f-157">Minimum supported client</span></span><br/> | <span data-ttu-id="0697f-158">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0697f-158">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="0697f-159">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0697f-159">Minimum supported server</span></span><br/> | <span data-ttu-id="0697f-160">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0697f-160">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="0697f-161">En-tête</span><span class="sxs-lookup"><span data-stu-id="0697f-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="0697f-162"><dt>Poclass. h ; </dt> <dt>BatClass. h sur Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 et Windows XP</dt></span><span class="sxs-lookup"><span data-stu-id="0697f-162"><dt>Poclass.h; </dt> <dt>BatClass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0697f-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0697f-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0697f-164">Informations sur la batterie</span><span class="sxs-lookup"><span data-stu-id="0697f-164">Battery Information</span></span>](battery-information.md)
</dt> <dt>

[<span data-ttu-id="0697f-165">Codes de contrôle de gestion de l’alimentation</span><span class="sxs-lookup"><span data-stu-id="0697f-165">Power Management Control Codes</span></span>](power-management-control-codes.md)
</dt> <dt>

[<span data-ttu-id="0697f-166">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="0697f-166">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="0697f-167">**\_ \_ informations sur les requêtes de batterie IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="0697f-167">**IOCTL\_BATTERY\_QUERY\_INFORMATION**</span></span>](ioctl-battery-query-information.md)
</dt> <dt>

[<span data-ttu-id="0697f-168">**État de la \_ requête de batterie IOCTL \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0697f-168">**IOCTL\_BATTERY\_QUERY\_STATUS**</span></span>](ioctl-battery-query-status.md)
</dt> <dt>

[<span data-ttu-id="0697f-169">**\_ \_ informations sur le jeu de batteries IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="0697f-169">**IOCTL\_BATTERY\_SET\_INFORMATION**</span></span>](ioctl-battery-set-information.md)
</dt> </dl>

 

