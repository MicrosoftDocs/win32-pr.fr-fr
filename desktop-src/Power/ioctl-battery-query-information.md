---
description: Récupère diverses informations pour la batterie.
ms.assetid: 4cc89b89-ab33-47c2-8327-9627cbd1595e
title: IOCTL_BATTERY_QUERY_INFORMATION le code de contrôle (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_BATTERY_QUERY_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- BatClass.h
ms.openlocfilehash: ee4010e055686c0df2987c34b48b133975b434ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951991"
---
# <a name="ioctl_battery_query_information-control-code"></a><span data-ttu-id="26bc7-103">\_Code de \_ contrôle des \_ informations sur les requêtes de batterie IOCTL</span><span class="sxs-lookup"><span data-stu-id="26bc7-103">IOCTL\_BATTERY\_QUERY\_INFORMATION control code</span></span>

<span data-ttu-id="26bc7-104">Récupère diverses informations pour la batterie.</span><span class="sxs-lookup"><span data-stu-id="26bc7-104">Retrieves a variety of information for the battery.</span></span>

<span data-ttu-id="26bc7-105">Pour effectuer cette opération, appelez la fonction [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="26bc7-105">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,                // handle to battery
  IOCTL_BATTERY_QUERY_INFORMATION, // dwIoControlCode
  (LPVOID) lpInBuffer,             // input buffer
  (DWORD) nInBufferSize,           // size of input buffer
  (LPVOID) lpOutBuffer,            // output buffer
  (DWORD) nOutBufferSize,          // size of output buffer
  (LPDWORD) lpBytesReturned,       // number of bytes returned
  (LPOVERLAPPED) lpOverlapped      // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="26bc7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="26bc7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26bc7-107">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="26bc7-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="26bc7-108">Handle vers la batterie sur laquelle les informations doivent être retournées.</span><span class="sxs-lookup"><span data-stu-id="26bc7-108">A handle to the battery on which information is to be returned.</span></span> <span data-ttu-id="26bc7-109">Pour récupérer un handle d’appareil, appelez la fonction [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="26bc7-109">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="26bc7-110">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="26bc7-110">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="26bc7-111">Code de contrôle de l’opération.</span><span class="sxs-lookup"><span data-stu-id="26bc7-111">The control code for the operation.</span></span> <span data-ttu-id="26bc7-112">Cette valeur identifie l’opération spécifique à effectuer et le type d’appareil sur lequel l’exécuter.</span><span class="sxs-lookup"><span data-stu-id="26bc7-112">This value identifies the specific operation to be performed and the type of device on which to perform it.</span></span> <span data-ttu-id="26bc7-113">Utilisez **les \_ \_ \_ informations de requête de batterie IOCTL** pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="26bc7-113">Use **IOCTL\_BATTERY\_QUERY\_INFORMATION** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="26bc7-114">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="26bc7-114">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="26bc7-115">Pointeur vers une structure [**d' \_ \_ informations de requête de batterie**](battery-query-information-str.md) .</span><span class="sxs-lookup"><span data-stu-id="26bc7-115">A pointer to a [**BATTERY\_QUERY\_INFORMATION**](battery-query-information-str.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="26bc7-116">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="26bc7-116">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="26bc7-117">Taille de la mémoire tampon d’entrée, en octets.</span><span class="sxs-lookup"><span data-stu-id="26bc7-117">The size of the input buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="26bc7-118">*lpOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="26bc7-118">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="26bc7-119">Pointeur vers la mémoire tampon de retour.</span><span class="sxs-lookup"><span data-stu-id="26bc7-119">A pointer to the return buffer.</span></span> <span data-ttu-id="26bc7-120">Le type de données (et, par conséquent, la taille) de la mémoire tampon de retour dépend des informations demandées dans le membre du niveau d’informations de la requête de batterie de la structure d' [**\_ \_ informations sur les requêtes**](battery-query-information-str.md) de la batterie d’entrée. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="26bc7-120">The data type (and, therefore, size) of the return buffer depends on the information requested in the **BATTERY\_QUERY\_INFORMATION\_LEVEL** member of the input [**BATTERY\_QUERY\_INFORMATION**](battery-query-information-str.md) structure.</span></span>

<span data-ttu-id="26bc7-121">Le tableau suivant présente les données retournées par un niveau d’information donné.</span><span class="sxs-lookup"><span data-stu-id="26bc7-121">The following table shows the data returned by a given information level.</span></span>



| <span data-ttu-id="26bc7-122">Niveau d’information</span><span class="sxs-lookup"><span data-stu-id="26bc7-122">Information level</span></span>                 | <span data-ttu-id="26bc7-123">Données retournées</span><span class="sxs-lookup"><span data-stu-id="26bc7-123">Data returned</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26bc7-124">**BatteryDeviceName**</span><span class="sxs-lookup"><span data-stu-id="26bc7-124">**BatteryDeviceName**</span></span>             | <span data-ttu-id="26bc7-125">Chaîne Unicode terminée par le caractère **null** qui spécifie le nom de la batterie.</span><span class="sxs-lookup"><span data-stu-id="26bc7-125">**Null**-terminated Unicode string that specifies the battery's name.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="26bc7-126">**BatteryEstimatedTime**</span><span class="sxs-lookup"><span data-stu-id="26bc7-126">**BatteryEstimatedTime**</span></span>          | <span data-ttu-id="26bc7-127">**ULong** qui spécifie la durée d’exécution estimée de la batterie, en secondes.</span><span class="sxs-lookup"><span data-stu-id="26bc7-127">A **ULONG** that specifies estimated battery run time, in seconds.</span></span> <span data-ttu-id="26bc7-128">Si le taux de drainage fourni dans le membre **AtRate** de la structure d' [**\_ \_ informations sur les requêtes**](battery-query-information-str.md) de la batterie est égal à zéro, ce calcul est basé sur le taux de drainage actuel.</span><span class="sxs-lookup"><span data-stu-id="26bc7-128">If the rate of drain provided in the **AtRate** member of the [**BATTERY\_QUERY\_INFORMATION**](battery-query-information-str.md) structure is zero, this calculation is based on the present rate of drain.</span></span> <span data-ttu-id="26bc7-129">Si **AtRate** est différent de zéro, l’heure retournée correspond à la durée d’exécution attendue pour le taux donné.</span><span class="sxs-lookup"><span data-stu-id="26bc7-129">If **AtRate** is nonzero, the time returned is the expected run time for the given rate.</span></span> <span data-ttu-id="26bc7-130">Si la durée estimée est inconnue (par exemple, si la batterie n’est pas en charge et que **AtRate** est égal à zéro), une **durée de batterie \_ inconnue \_** est retournée.</span><span class="sxs-lookup"><span data-stu-id="26bc7-130">If the estimated time is unknown (for example, the battery is not discharging and **AtRate** is zero), **BATTERY\_UNKNOWN\_TIME** is returned.</span></span> <span data-ttu-id="26bc7-131">Notez que cette valeur n’est pas très précise sur certains systèmes de batterie.</span><span class="sxs-lookup"><span data-stu-id="26bc7-131">Note that this value is not very accurate on some battery systems.</span></span> <span data-ttu-id="26bc7-132">La valeur peut varier considérablement en fonction de l’utilisation actuelle de l’alimentation, ce qui peut être affecté par l’activité du disque et d’autres facteurs.</span><span class="sxs-lookup"><span data-stu-id="26bc7-132">The value may vary widely depending on present power usage, which could be affected by disk activity and other factors.</span></span> <span data-ttu-id="26bc7-133">Il n’existe aucun mécanisme de notification pour les modifications de cette valeur.</span><span class="sxs-lookup"><span data-stu-id="26bc7-133">There is no notification mechanism for changes in this value.</span></span> |
| <span data-ttu-id="26bc7-134">**BatteryGranularityInformation**</span><span class="sxs-lookup"><span data-stu-id="26bc7-134">**BatteryGranularityInformation**</span></span> | <span data-ttu-id="26bc7-135">Tableau de longueur variable de la [**batterie \_ signalant \_**](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale) les structures d’échelle qui contient la granularité des rapports pour la capacité de la batterie qui est retournée par l’état de la [**\_ \_ requête \_ de batterie IOCTL**](ioctl-battery-query-status.md).</span><span class="sxs-lookup"><span data-stu-id="26bc7-135">A variable-length array of [**BATTERY\_REPORTING\_SCALE**](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale) structures that contains the reporting granularity for the battery capacity that is returned from [**IOCTL\_BATTERY\_QUERY\_STATUS**](ioctl-battery-query-status.md).</span></span> <span data-ttu-id="26bc7-136">Plusieurs entrées sont retournées lorsque la granularité dépend de la capacité actuelle de la batterie.</span><span class="sxs-lookup"><span data-stu-id="26bc7-136">Multiple entries are returned when the granularity depends on the present capacity of the battery.</span></span> <span data-ttu-id="26bc7-137">Consultez Mise à l' **\_ \_ échelle des rapports de batterie** pour l’interprétation du tableau d’entrées.</span><span class="sxs-lookup"><span data-stu-id="26bc7-137">See **BATTERY\_REPORTING\_SCALE** for the interpretation of the array of entries.</span></span> <span data-ttu-id="26bc7-138">Le nombre d’entrées est indiqué par la taille de la mémoire tampon retournée et peut être calculé comme suit : (*lpBytesReturned* /sizeof (**\_ \_ Scale Reporting Scale**)).</span><span class="sxs-lookup"><span data-stu-id="26bc7-138">The number of entries is indicated by the size of the buffer returned, and can be calculated as (*lpBytesReturned* / sizeof (**BATTERY\_REPORTING\_SCALE**)).</span></span> <span data-ttu-id="26bc7-139">Le nombre maximal d’entrées qui sera retourné est de quatre.</span><span class="sxs-lookup"><span data-stu-id="26bc7-139">The maximum number of entries that will be returned is four.</span></span>                                                                                                |
| <span data-ttu-id="26bc7-140">**BatteryInformation**</span><span class="sxs-lookup"><span data-stu-id="26bc7-140">**BatteryInformation**</span></span>            | <span data-ttu-id="26bc7-141">Structure [**d' \_ informations sur la batterie**](battery-information-str.md) .</span><span class="sxs-lookup"><span data-stu-id="26bc7-141">A [**BATTERY\_INFORMATION**](battery-information-str.md) structure.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="26bc7-142">**BatteryManufactureDate**</span><span class="sxs-lookup"><span data-stu-id="26bc7-142">**BatteryManufactureDate**</span></span>        | <span data-ttu-id="26bc7-143">Structure [**de \_ \_ Date**](battery-manufacture-date-str.md) de la fabrication d’une batterie.</span><span class="sxs-lookup"><span data-stu-id="26bc7-143">A [**BATTERY\_MANUFACTURE\_DATE**](battery-manufacture-date-str.md) structure.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="26bc7-144">**BatteryManufactureName**</span><span class="sxs-lookup"><span data-stu-id="26bc7-144">**BatteryManufactureName**</span></span>        | <span data-ttu-id="26bc7-145">Chaîne Unicode terminée par le caractère **null** qui contient le nom du fabricant de la batterie.</span><span class="sxs-lookup"><span data-stu-id="26bc7-145">**Null**-terminated Unicode string that contains the name of the manufacturer of the battery.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="26bc7-146">**BatterySerialNumber**</span><span class="sxs-lookup"><span data-stu-id="26bc7-146">**BatterySerialNumber**</span></span>           | <span data-ttu-id="26bc7-147">Chaîne Unicode terminée par le caractère **null** qui contient le numéro de série de la batterie.</span><span class="sxs-lookup"><span data-stu-id="26bc7-147">**Null**-terminated Unicode string that contains the battery's serial number.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="26bc7-148">**BatteryTemperature**</span><span class="sxs-lookup"><span data-stu-id="26bc7-148">**BatteryTemperature**</span></span>            | <span data-ttu-id="26bc7-149">**ULong** qui contient la température actuelle de la batterie, en dixièmes de degré Kelvin.</span><span class="sxs-lookup"><span data-stu-id="26bc7-149">A **ULONG** that contains the battery's current temperature, in 10ths of a degree Kelvin.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="26bc7-150">**BatteryUniqueID**</span><span class="sxs-lookup"><span data-stu-id="26bc7-150">**BatteryUniqueID**</span></span>               | <span data-ttu-id="26bc7-151">Chaîne Unicode terminée par le caractère **null** qui identifie de façon unique la batterie.</span><span class="sxs-lookup"><span data-stu-id="26bc7-151">**Null**-terminated Unicode string that uniquely identifies the battery.</span></span> <span data-ttu-id="26bc7-152">Cette valeur peut être utilisée pour effectuer le suivi d’une batterie spécifique.</span><span class="sxs-lookup"><span data-stu-id="26bc7-152">This value can be used to track a specific battery.</span></span> <span data-ttu-id="26bc7-153">Dans le cas de batteries intelligentes, cet ID correspond à la concaténation du nom du fabricant, du nom de l’appareil, de la date de fabrication et d’une représentation imprimable du numéro de série.</span><span class="sxs-lookup"><span data-stu-id="26bc7-153">In the case of smart batteries, this ID will be the concatenation of the manufacturer's name, device name, date of manufacture, and a printable representation of the serial number.</span></span> <span data-ttu-id="26bc7-154">Cette valeur n’est pas destinée à être affichée à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="26bc7-154">This value is not intended to be displayed to the user.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                              |



 

</dd> <dt>

<span data-ttu-id="26bc7-155">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="26bc7-155">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="26bc7-156">Taille de la mémoire tampon de sortie en octets.</span><span class="sxs-lookup"><span data-stu-id="26bc7-156">The size of the output buffer, in bytes.</span></span> <span data-ttu-id="26bc7-157">En fonction du niveau d’information des données demandées, il peut s’agir d’une mémoire tampon de taille variable.</span><span class="sxs-lookup"><span data-stu-id="26bc7-157">Depending on the information level of data requested, this may be a variably sized buffer.</span></span>

</dd> <dt>

<span data-ttu-id="26bc7-158">*lpBytesReturned*</span><span class="sxs-lookup"><span data-stu-id="26bc7-158">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="26bc7-159">Pointeur vers une variable qui reçoit la taille des données retournées dans la mémoire tampon *lpOutBuffer* , en octets.</span><span class="sxs-lookup"><span data-stu-id="26bc7-159">A pointer to a variable that receives the size of the data returned in the *lpOutBuffer* buffer, in bytes.</span></span>

<span data-ttu-id="26bc7-160">Si la mémoire tampon de sortie est trop petite pour retourner des données, alors l’appel échoue, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne l’erreur de code d’erreur **\_ \_ mémoire tampon insuffisante** et le nombre d’octets retourné est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="26bc7-160">If the output buffer is too small to return any data then the call fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code **ERROR\_INSUFFICIENT\_BUFFER**, and the returned byte count is zero.</span></span>

<span data-ttu-id="26bc7-161">Si *lpOverlapped* a la **valeur null** (e/s nonoverlapped), *lpBytesReturned* ne peut pas avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="26bc7-161">If *lpOverlapped* is **NULL** (nonoverlapped I/O), *lpBytesReturned* cannot be **NULL**.</span></span>

<span data-ttu-id="26bc7-162">Si *lpOverlapped* n’a pas la **valeur null** (e/s avec chevauchement), *LpBytesReturned* peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="26bc7-162">If *lpOverlapped* is not **NULL** (overlapped I/O), *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="26bc7-163">S’il s’agit d’une opération avec chevauchement, vous pouvez récupérer le nombre d’octets retournés en appelant la fonction [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) .</span><span class="sxs-lookup"><span data-stu-id="26bc7-163">If this is an overlapped operation, you can retrieve the number of bytes returned by calling the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="26bc7-164">Si *hDevice* est associé à un port de terminaison d’e/s, vous pouvez récupérer le nombre d’octets renvoyés en appelant la fonction [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="26bc7-164">If *hDevice* is associated with an I/O completion port, you can get the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="26bc7-165">*lpOverlapped*</span><span class="sxs-lookup"><span data-stu-id="26bc7-165">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="26bc7-166">Pointeur vers une structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="26bc7-166">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="26bc7-167">Si *hDevice* a été ouvert avec l’indicateur de **fichier avec indicateur de \_ \_ chevauchement** , *LPOVERLAPPED* doit pointer vers une structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) valide.</span><span class="sxs-lookup"><span data-stu-id="26bc7-167">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span> <span data-ttu-id="26bc7-168">Dans ce cas, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) est exécuté comme une opération Overlapped (asynchrone).</span><span class="sxs-lookup"><span data-stu-id="26bc7-168">In this case, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="26bc7-169">Si l’appareil a été ouvert avec l’indicateur de **fichier avec \_ indicateur de \_ chevauchement** et que *lpOverlapped* a la **valeur null**, la fonction échoue de façon imprévisible.</span><span class="sxs-lookup"><span data-stu-id="26bc7-169">If the device was opened with the **FILE\_FLAG\_OVERLAPPED** flag and *lpOverlapped* is **NULL**, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="26bc7-170">Si *hDevice* a été ouvert sans que l’indicateur de fichier n’ait été spécifié, *lpOverlapped* est ignoré et la fonction [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) ne retourne pas tant que l’opération n’est pas terminée, soit jusqu’à ce qu’une erreur se produise. **\_ \_**</span><span class="sxs-lookup"><span data-stu-id="26bc7-170">If *hDevice* was opened without specifying the **FILE\_FLAG\_OVERLAPPED** flag, *lpOverlapped* is ignored and the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function does not return until the operation has been completed, or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26bc7-171">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="26bc7-171">Return value</span></span>

<span data-ttu-id="26bc7-172">Si l’opération se termine correctement, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="26bc7-172">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="26bc7-173">Si l’opération échoue ou est en attente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="26bc7-173">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="26bc7-174">Pour obtenir des informations détaillées sur l’erreur, appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="26bc7-174">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

<span data-ttu-id="26bc7-175">Certaines informations sur les batteries sont facultatives ou n’ont pas de sens pour certaines batteries.</span><span class="sxs-lookup"><span data-stu-id="26bc7-175">Some information about batteries is optional or may be meaningless for some batteries.</span></span> <span data-ttu-id="26bc7-176">Si le type de données particulier demandé n’est pas disponible pour la batterie actuelle, **la \_ \_ fonction d’erreur non valide** est retournée.</span><span class="sxs-lookup"><span data-stu-id="26bc7-176">If the particular type of data requested is not available for the current battery, then **ERROR\_INVALID\_FUNCTION** is returned.</span></span>

<span data-ttu-id="26bc7-177">Toutes les demandes d’informations sur la batterie se terminent avec l’état **fichier d’erreur \_ \_ \_ introuvable** chaque fois que l’élément **BatteryTag** de la demande ne correspond pas à celui de la balise de batterie actuelle.</span><span class="sxs-lookup"><span data-stu-id="26bc7-177">All requests for battery information will complete with the status of **ERROR\_FILE\_NOT\_FOUND** whenever the **BatteryTag** element of the request does not match that of the current battery tag.</span></span> <span data-ttu-id="26bc7-178">Cela permet de s’assurer que les informations sur la batterie retournée correspondent à celles de la batterie demandée.</span><span class="sxs-lookup"><span data-stu-id="26bc7-178">This ensures that the returned battery information matches that of the requested battery.</span></span> <span data-ttu-id="26bc7-179">(Pour plus d’informations, consultez [balises de batterie](battery-information.md) .)</span><span class="sxs-lookup"><span data-stu-id="26bc7-179">(See [Battery Tags](battery-information.md) for more information.)</span></span>

## <a name="remarks"></a><span data-ttu-id="26bc7-180">Notes</span><span class="sxs-lookup"><span data-stu-id="26bc7-180">Remarks</span></span>

<span data-ttu-id="26bc7-181">Cette IOCTL de batterie récupère diverses informations pour la batterie.</span><span class="sxs-lookup"><span data-stu-id="26bc7-181">This battery IOCTL retrieves a variety of information for the battery.</span></span> <span data-ttu-id="26bc7-182">La structure des paramètres d’entrée, les [**\_ \_ informations sur les requêtes**](battery-query-information-str.md)de la batterie, indiquent le type d’informations à retourner et le moment où les informations sur la batterie doivent être retournées.</span><span class="sxs-lookup"><span data-stu-id="26bc7-182">The input parameter structure, [**BATTERY\_QUERY\_INFORMATION**](battery-query-information-str.md), indicates the type of information to be returned and when the battery information should be returned.</span></span> <span data-ttu-id="26bc7-183">Le type de données et le contenu de la mémoire tampon de sortie varient en fonction des données demandées.</span><span class="sxs-lookup"><span data-stu-id="26bc7-183">The data type and contents of the output buffer vary based on the data requested.</span></span>

<span data-ttu-id="26bc7-184">Pour connaître les implications des e/s avec chevauchement sur cette opération, consultez la section Notes de la rubrique [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) .</span><span class="sxs-lookup"><span data-stu-id="26bc7-184">For the implications of overlapped I/O on this operation, see the Remarks section of the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) topic.</span></span>

## <a name="examples"></a><span data-ttu-id="26bc7-185">Exemples</span><span class="sxs-lookup"><span data-stu-id="26bc7-185">Examples</span></span>

<span data-ttu-id="26bc7-186">Pour obtenir un exemple, consultez [énumération des unités de batterie](enumerating-battery-devices.md).</span><span class="sxs-lookup"><span data-stu-id="26bc7-186">For an example, see [Enumerating Battery Devices](enumerating-battery-devices.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="26bc7-187">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="26bc7-187">Requirements</span></span>



| <span data-ttu-id="26bc7-188">Condition requise</span><span class="sxs-lookup"><span data-stu-id="26bc7-188">Requirement</span></span> | <span data-ttu-id="26bc7-189">Valeur</span><span class="sxs-lookup"><span data-stu-id="26bc7-189">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26bc7-190">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26bc7-190">Minimum supported client</span></span><br/> | <span data-ttu-id="26bc7-191">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="26bc7-191">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="26bc7-192">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26bc7-192">Minimum supported server</span></span><br/> | <span data-ttu-id="26bc7-193">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="26bc7-193">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="26bc7-194">En-tête</span><span class="sxs-lookup"><span data-stu-id="26bc7-194">Header</span></span><br/>                   | <dl> <span data-ttu-id="26bc7-195"><dt>Poclass. h ; </dt> <dt>BatClass. h sur Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 et Windows XP</dt></span><span class="sxs-lookup"><span data-stu-id="26bc7-195"><dt>Poclass.h; </dt> <dt>BatClass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26bc7-196">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26bc7-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26bc7-197">Informations sur la batterie</span><span class="sxs-lookup"><span data-stu-id="26bc7-197">Battery Information</span></span>](battery-information.md)
</dt> <dt>

[<span data-ttu-id="26bc7-198">Codes de contrôle de gestion de l’alimentation</span><span class="sxs-lookup"><span data-stu-id="26bc7-198">Power Management Control Codes</span></span>](power-management-control-codes.md)
</dt> <dt>

[<span data-ttu-id="26bc7-199">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="26bc7-199">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="26bc7-200">**\_informations sur la requête de batterie \_**</span><span class="sxs-lookup"><span data-stu-id="26bc7-200">**BATTERY\_QUERY\_INFORMATION**</span></span>](battery-query-information-str.md)
</dt> <dt>

[<span data-ttu-id="26bc7-201">**mise à l’échelle de la batterie \_ \_**</span><span class="sxs-lookup"><span data-stu-id="26bc7-201">**BATTERY\_REPORTING\_SCALE**</span></span>](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale)
</dt> <dt>

[<span data-ttu-id="26bc7-202">**État de la \_ requête de batterie IOCTL \_ \_**</span><span class="sxs-lookup"><span data-stu-id="26bc7-202">**IOCTL\_BATTERY\_QUERY\_STATUS**</span></span>](ioctl-battery-query-status.md)
</dt> <dt>

[<span data-ttu-id="26bc7-203">**\_ \_ balise de requête de batterie IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="26bc7-203">**IOCTL\_BATTERY\_QUERY\_TAG**</span></span>](ioctl-battery-query-tag.md)
</dt> <dt>

[<span data-ttu-id="26bc7-204">**\_ \_ informations sur le jeu de batteries IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="26bc7-204">**IOCTL\_BATTERY\_SET\_INFORMATION**</span></span>](ioctl-battery-set-information.md)
</dt> </dl>

 

