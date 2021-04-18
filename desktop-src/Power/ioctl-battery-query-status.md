---
description: Récupère l’état actuel de la batterie.
ms.assetid: 7a7bf429-9b2c-4faf-9f27-fb5fd8dd18df
title: IOCTL_BATTERY_QUERY_STATUS le code de contrôle (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_BATTERY_QUERY_STATUS
api_type:
- HeaderDef
api_location:
- Poclass.h
- BatClass.h
ms.openlocfilehash: e2de9d3ab48aec13a9a5c1957a5f98aefbe6a09f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519111"
---
# <a name="ioctl_battery_query_status-control-code"></a><span data-ttu-id="30fea-103">\_Code de \_ contrôle d' \_ État de la requête IOCTL</span><span class="sxs-lookup"><span data-stu-id="30fea-103">IOCTL\_BATTERY\_QUERY\_STATUS control code</span></span>

<span data-ttu-id="30fea-104">Récupère l’état actuel de la batterie.</span><span class="sxs-lookup"><span data-stu-id="30fea-104">Retrieves the current status of the battery.</span></span>

<span data-ttu-id="30fea-105">Pour effectuer cette opération, appelez la fonction [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="30fea-105">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,           // handle to battery
  IOCTL_BATTERY_QUERY_STATUS, // dwIoControlCode
  (LPVOID) lpInBuffer,        // input buffer
  (DWORD) nInBufferSize,      // size of input buffer
  (LPVOID) lpOutBuffer,       // output buffer
  (DWORD) nOutBufferSize,     // size of output buffer
  (LPDWORD) lpBytesReturned,  // number of bytes returned
  (LPOVERLAPPED) lpOverlapped // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="30fea-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="30fea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30fea-107">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="30fea-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="30fea-108">Handle de la batterie à partir de laquelle les informations doivent être retournées.</span><span class="sxs-lookup"><span data-stu-id="30fea-108">A handle to the battery from which information is to be returned.</span></span> <span data-ttu-id="30fea-109">Pour récupérer un handle d’appareil, appelez la fonction [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="30fea-109">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="30fea-110">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="30fea-110">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="30fea-111">Code de contrôle de l’opération.</span><span class="sxs-lookup"><span data-stu-id="30fea-111">The control code for the operation.</span></span> <span data-ttu-id="30fea-112">Cette valeur identifie l’opération spécifique à effectuer et le type d’appareil sur lequel l’exécuter.</span><span class="sxs-lookup"><span data-stu-id="30fea-112">This value identifies the specific operation to be performed and the type of device on which to perform it.</span></span> <span data-ttu-id="30fea-113">Utilisez l’état de la **\_ requête de batterie \_ \_ IOCTL** pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="30fea-113">Use **IOCTL\_BATTERY\_QUERY\_STATUS** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="30fea-114">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="30fea-114">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="30fea-115">Pointeur vers une structure [**d' \_ \_ État d’attente**](battery-wait-status-str.md) de la batterie.</span><span class="sxs-lookup"><span data-stu-id="30fea-115">A pointer to a [**BATTERY\_WAIT\_STATUS**](battery-wait-status-str.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="30fea-116">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="30fea-116">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="30fea-117">Taille de la mémoire tampon d’entrée, en octets.</span><span class="sxs-lookup"><span data-stu-id="30fea-117">The size of the input buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="30fea-118">*lpOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="30fea-118">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="30fea-119">Pointeur vers une structure [**d' \_ État**](battery-status-str.md) de la batterie.</span><span class="sxs-lookup"><span data-stu-id="30fea-119">A pointer to a [**BATTERY\_STATUS**](battery-status-str.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="30fea-120">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="30fea-120">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="30fea-121">Taille de la mémoire tampon de sortie en octets.</span><span class="sxs-lookup"><span data-stu-id="30fea-121">The size of the output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="30fea-122">*lpBytesReturned*</span><span class="sxs-lookup"><span data-stu-id="30fea-122">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="30fea-123">Pointeur vers une variable qui reçoit la taille des données retournées dans la mémoire tampon *lpOutBuffer* , en octets.</span><span class="sxs-lookup"><span data-stu-id="30fea-123">A pointer to a variable that receives the size of the data returned in the *lpOutBuffer* buffer, in bytes.</span></span>

<span data-ttu-id="30fea-124">Si la mémoire tampon de sortie est trop petite pour retourner des données, alors l’appel échoue, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne l’erreur de code d’erreur **\_ \_ mémoire tampon insuffisante** et le nombre d’octets retourné est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="30fea-124">If the output buffer is too small to return any data then the call fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code **ERROR\_INSUFFICIENT\_BUFFER**, and the returned byte count is zero.</span></span>

<span data-ttu-id="30fea-125">Si *lpOverlapped* a la **valeur null** (e/s nonoverlapped), *lpBytesReturned* ne peut pas avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="30fea-125">If *lpOverlapped* is **NULL** (nonoverlapped I/O), *lpBytesReturned* cannot be **NULL**.</span></span>

<span data-ttu-id="30fea-126">Si *lpOverlapped* n’a pas la **valeur null** (e/s avec chevauchement), *LpBytesReturned* peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="30fea-126">If *lpOverlapped* is not **NULL** (overlapped I/O), *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="30fea-127">S’il s’agit d’une opération avec chevauchement, vous pouvez récupérer le nombre d’octets retournés en appelant la fonction [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) .</span><span class="sxs-lookup"><span data-stu-id="30fea-127">If this is an overlapped operation, you can retrieve the number of bytes returned by calling the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="30fea-128">Si *hDevice* est associé à un port de terminaison d’e/s, vous pouvez récupérer le nombre d’octets renvoyés en appelant la fonction [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="30fea-128">If *hDevice* is associated with an I/O completion port, you can get the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="30fea-129">*lpOverlapped*</span><span class="sxs-lookup"><span data-stu-id="30fea-129">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="30fea-130">Pointeur vers une structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="30fea-130">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="30fea-131">Si *hDevice* a été ouvert avec l’indicateur de **fichier avec indicateur de \_ \_ chevauchement** , *LPOVERLAPPED* doit pointer vers une structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) valide.</span><span class="sxs-lookup"><span data-stu-id="30fea-131">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span> <span data-ttu-id="30fea-132">Dans ce cas, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) est exécuté comme une opération Overlapped (asynchrone).</span><span class="sxs-lookup"><span data-stu-id="30fea-132">In this case, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="30fea-133">Si l’appareil a été ouvert avec l’indicateur de **fichier avec \_ indicateur de \_ chevauchement** et que *lpOverlapped* a la **valeur null**, la fonction échoue de façon imprévisible.</span><span class="sxs-lookup"><span data-stu-id="30fea-133">If the device was opened with the **FILE\_FLAG\_OVERLAPPED** flag and *lpOverlapped* is **NULL**, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="30fea-134">Si *hDevice* a été ouvert sans que l’indicateur de fichier n’ait été spécifié, *lpOverlapped* est ignoré et la fonction [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) ne retourne pas tant que l’opération n’est pas terminée, soit jusqu’à ce qu’une erreur se produise. **\_ \_**</span><span class="sxs-lookup"><span data-stu-id="30fea-134">If *hDevice* was opened without specifying the **FILE\_FLAG\_OVERLAPPED** flag, *lpOverlapped* is ignored and the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function does not return until the operation has been completed, or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30fea-135">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="30fea-135">Return value</span></span>

<span data-ttu-id="30fea-136">Si l’opération se termine correctement, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="30fea-136">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="30fea-137">Si l’opération échoue ou est en attente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="30fea-137">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="30fea-138">Pour obtenir des informations détaillées sur l’erreur, appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="30fea-138">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="30fea-139">Remarques</span><span class="sxs-lookup"><span data-stu-id="30fea-139">Remarks</span></span>

<span data-ttu-id="30fea-140">Cette IOCTL de batterie récupère l’état de la batterie au moment où l’opération est retournée.</span><span class="sxs-lookup"><span data-stu-id="30fea-140">This battery IOCTL retrieves the status of the battery at the time the operation returns.</span></span> <span data-ttu-id="30fea-141">La structure du paramètre d’entrée, l' [**\_ \_ État d’attente**](battery-wait-status-str.md)de la batterie, indique quand l’état de la batterie doit être traité et retourné.</span><span class="sxs-lookup"><span data-stu-id="30fea-141">The input parameter structure, [**BATTERY\_WAIT\_STATUS**](battery-wait-status-str.md), indicates when the battery status is to be processed and returned.</span></span>

<span data-ttu-id="30fea-142">Les demandes d’état de la batterie peuvent être pour un retour immédiat ou peuvent être définies pour attendre une condition particulière avant de se terminer.</span><span class="sxs-lookup"><span data-stu-id="30fea-142">Requests for battery status can be for immediate return or can be set to wait for a particular condition before completing.</span></span> <span data-ttu-id="30fea-143">Par exemple, une demande d’informations sur la batterie peut être effectuée, qui attend que la capacité de la batterie atteigne un point spécifié ou que l’état de la batterie change.</span><span class="sxs-lookup"><span data-stu-id="30fea-143">For example, a request for battery information can be made that waits until the battery capacity reaches a specified point or the battery state changes.</span></span>

<span data-ttu-id="30fea-144">Toutes les demandes d’informations sur la batterie se terminent avec l’état **fichier d’erreur \_ \_ \_ introuvable** chaque fois que l’élément **BatteryTag** de la demande ne correspond pas à celui de la balise de batterie actuelle.</span><span class="sxs-lookup"><span data-stu-id="30fea-144">All requests for battery information will complete with the status of **ERROR\_FILE\_NOT\_FOUND** whenever the **BatteryTag** element of the request does not match that of the current battery tag.</span></span> <span data-ttu-id="30fea-145">(Pour plus d’informations, consultez [balises de batterie](battery-information.md) .) Cela permet de s’assurer que les informations sur la batterie retournée correspondent à celles de la batterie demandée.</span><span class="sxs-lookup"><span data-stu-id="30fea-145">(See [Battery Tags](battery-information.md) for more information.) This is used to ensure that the returned battery information matches that of the requested battery.</span></span>

<span data-ttu-id="30fea-146">Pour connaître les implications des e/s avec chevauchement sur cette opération, consultez la section Notes de la rubrique [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) .</span><span class="sxs-lookup"><span data-stu-id="30fea-146">For the implications of overlapped I/O on this operation, see the Remarks section of the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) topic.</span></span>

## <a name="examples"></a><span data-ttu-id="30fea-147">Exemples</span><span class="sxs-lookup"><span data-stu-id="30fea-147">Examples</span></span>

<span data-ttu-id="30fea-148">Pour obtenir un exemple, consultez [énumération des unités de batterie](enumerating-battery-devices.md).</span><span class="sxs-lookup"><span data-stu-id="30fea-148">For an example, see [Enumerating Battery Devices](enumerating-battery-devices.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="30fea-149">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="30fea-149">Requirements</span></span>



| <span data-ttu-id="30fea-150">Condition requise</span><span class="sxs-lookup"><span data-stu-id="30fea-150">Requirement</span></span> | <span data-ttu-id="30fea-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="30fea-151">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30fea-152">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30fea-152">Minimum supported client</span></span><br/> | <span data-ttu-id="30fea-153">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="30fea-153">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="30fea-154">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30fea-154">Minimum supported server</span></span><br/> | <span data-ttu-id="30fea-155">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="30fea-155">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="30fea-156">En-tête</span><span class="sxs-lookup"><span data-stu-id="30fea-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="30fea-157"><dt>Poclass. h ; </dt> <dt>BatClass. h sur Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 et Windows XP</dt></span><span class="sxs-lookup"><span data-stu-id="30fea-157"><dt>Poclass.h; </dt> <dt>BatClass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30fea-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30fea-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30fea-159">Informations sur la batterie</span><span class="sxs-lookup"><span data-stu-id="30fea-159">Battery Information</span></span>](battery-information.md)
</dt> <dt>

[<span data-ttu-id="30fea-160">Codes de contrôle de gestion de l’alimentation</span><span class="sxs-lookup"><span data-stu-id="30fea-160">Power Management Control Codes</span></span>](power-management-control-codes.md)
</dt> <dt>

[<span data-ttu-id="30fea-161">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="30fea-161">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="30fea-162">**État de la batterie \_**</span><span class="sxs-lookup"><span data-stu-id="30fea-162">**BATTERY\_STATUS**</span></span>](battery-status-str.md)
</dt> <dt>

[<span data-ttu-id="30fea-163">**\_État d’attente de la batterie \_**</span><span class="sxs-lookup"><span data-stu-id="30fea-163">**BATTERY\_WAIT\_STATUS**</span></span>](battery-wait-status-str.md)
</dt> <dt>

[<span data-ttu-id="30fea-164">**\_ \_ informations sur les requêtes de batterie IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="30fea-164">**IOCTL\_BATTERY\_QUERY\_INFORMATION**</span></span>](ioctl-battery-query-information.md)
</dt> <dt>

[<span data-ttu-id="30fea-165">**\_ \_ balise de requête de batterie IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="30fea-165">**IOCTL\_BATTERY\_QUERY\_TAG**</span></span>](ioctl-battery-query-tag.md)
</dt> <dt>

[<span data-ttu-id="30fea-166">**\_ \_ informations sur le jeu de batteries IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="30fea-166">**IOCTL\_BATTERY\_SET\_INFORMATION**</span></span>](ioctl-battery-set-information.md)
</dt> </dl>

 

