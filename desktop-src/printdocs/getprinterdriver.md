---
description: La fonction GetPrinterDriver récupère les données du pilote pour l’imprimante spécifiée. Si le pilote n’est pas installé sur l’ordinateur local, GetPrinterDriver l’installe.
ms.assetid: 93f859b4-1005-4359-8029-9536d6eeb7e7
title: GetPrinterDriver, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDriver
- GetPrinterDriverA
- GetPrinterDriverW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: a67a77a8167bf207231d2f3f6f063ed7636e201f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531747"
---
# <a name="getprinterdriver-function"></a><span data-ttu-id="ef03a-104">GetPrinterDriver fonction)</span><span class="sxs-lookup"><span data-stu-id="ef03a-104">GetPrinterDriver function</span></span>

<span data-ttu-id="ef03a-105">La fonction **GetPrinterDriver** récupère les données du pilote pour l’imprimante spécifiée.</span><span class="sxs-lookup"><span data-stu-id="ef03a-105">The **GetPrinterDriver** function retrieves driver data for the specified printer.</span></span> <span data-ttu-id="ef03a-106">Si le pilote n’est pas installé sur l’ordinateur local, **GetPrinterDriver** l’installe.</span><span class="sxs-lookup"><span data-stu-id="ef03a-106">If the driver is not installed on the local computer, **GetPrinterDriver** installs it.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef03a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ef03a-107">Syntax</span></span>


```C++
BOOL GetPrinterDriver(
  _In_  HANDLE  hPrinter,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pDriverInfo,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="ef03a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ef03a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef03a-109">*hPrinter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ef03a-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef03a-110">Handle vers l’imprimante pour laquelle les données du pilote doivent être récupérées.</span><span class="sxs-lookup"><span data-stu-id="ef03a-110">A handle to the printer for which the driver data should be retrieved.</span></span> <span data-ttu-id="ef03a-111">Utilisez la fonction [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="ef03a-111">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="ef03a-112">*pEnvironment* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ef03a-112">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef03a-113">Pointeur vers une chaîne se terminant par un caractère null qui spécifie l’environnement (par exemple, Windows x86, Windows IA64 ou Windows x64).</span><span class="sxs-lookup"><span data-stu-id="ef03a-113">A pointer to a null-terminated string that specifies the environment (for example, Windows x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="ef03a-114">Si ce paramètre a la **valeur null**, l’environnement actuel de l’application appelante et de l’ordinateur client (pas du serveur d’impression et de l’application de destination) est utilisé.</span><span class="sxs-lookup"><span data-stu-id="ef03a-114">If this parameter is **NULL**, the current environment of the calling application and client machine (not of the destination application and print server) is used.</span></span>

</dd> <dt>

<span data-ttu-id="ef03a-115">De *niveau* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ef03a-115">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef03a-116">Structure du pilote d’imprimante renvoyée dans la mémoire tampon *pDriverInfo* .</span><span class="sxs-lookup"><span data-stu-id="ef03a-116">The printer driver structure returned in the *pDriverInfo* buffer.</span></span> <span data-ttu-id="ef03a-117">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="ef03a-117">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="ef03a-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef03a-118">Value</span></span>                                                                                                | <span data-ttu-id="ef03a-119">Signification</span><span class="sxs-lookup"><span data-stu-id="ef03a-119">Meaning</span></span>                                             |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="ef03a-120"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="ef03a-120"><dt>**1**</dt></span></span> </dl> | [<span data-ttu-id="ef03a-121">**\_Informations sur le pilote \_ 1**</span><span class="sxs-lookup"><span data-stu-id="ef03a-121">**DRIVER\_INFO\_1**</span></span>](driver-info-1.md)<br/> |
| <span id="2"></span><dl> <span data-ttu-id="ef03a-122"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="ef03a-122"><dt>**2**</dt></span></span> </dl> | [<span data-ttu-id="ef03a-123">**\_Informations sur le pilote \_ 2**</span><span class="sxs-lookup"><span data-stu-id="ef03a-123">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)<br/> |
| <span id="3"></span><dl> <span data-ttu-id="ef03a-124"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="ef03a-124"><dt>**3**</dt></span></span> </dl> | [<span data-ttu-id="ef03a-125">**\_Informations sur le pilote \_ 3**</span><span class="sxs-lookup"><span data-stu-id="ef03a-125">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)<br/> |
| <span id="4"></span><dl> <span data-ttu-id="ef03a-126"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="ef03a-126"><dt>**4**</dt></span></span> </dl> | [<span data-ttu-id="ef03a-127">**\_Informations sur le pilote \_ 4**</span><span class="sxs-lookup"><span data-stu-id="ef03a-127">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)<br/> |
| <span id="5"></span><dl> <span data-ttu-id="ef03a-128"><dt>**5**</dt></span><span class="sxs-lookup"><span data-stu-id="ef03a-128"><dt>**5**</dt></span></span> </dl> | [<span data-ttu-id="ef03a-129">**\_Informations sur le pilote \_ 5**</span><span class="sxs-lookup"><span data-stu-id="ef03a-129">**DRIVER\_INFO\_5**</span></span>](driver-info-5.md)<br/> |
| <span id="6"></span><dl> <span data-ttu-id="ef03a-130"><dt>**6**</dt></span><span class="sxs-lookup"><span data-stu-id="ef03a-130"><dt>**6**</dt></span></span> </dl> | [<span data-ttu-id="ef03a-131">**\_Informations sur le pilote \_ 6**</span><span class="sxs-lookup"><span data-stu-id="ef03a-131">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)<br/> |
| <span id="8"></span><dl> <span data-ttu-id="ef03a-132"><dt>**8**</dt></span><span class="sxs-lookup"><span data-stu-id="ef03a-132"><dt>**8**</dt></span></span> </dl> | [<span data-ttu-id="ef03a-133">**\_Informations sur le pilote \_ 8**</span><span class="sxs-lookup"><span data-stu-id="ef03a-133">**DRIVER\_INFO\_8**</span></span>](driver-info-8.md)<br/> |



 

</dd> <dt>

<span data-ttu-id="ef03a-134">*pDriverInfo* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ef03a-134">*pDriverInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef03a-135">Pointeur vers une mémoire tampon qui reçoit une structure contenant des informations sur le pilote, comme spécifié par le niveau.</span><span class="sxs-lookup"><span data-stu-id="ef03a-135">A pointer to a buffer that receives a structure containing information about the driver, as specified by Level.</span></span> <span data-ttu-id="ef03a-136">La mémoire tampon doit être suffisamment grande pour stocker les chaînes pointées par les membres de la structure.</span><span class="sxs-lookup"><span data-stu-id="ef03a-136">The buffer must be large enough to store the strings pointed to by the structure members.</span></span>

<span data-ttu-id="ef03a-137">Pour déterminer la taille de mémoire tampon requise, appelez **GetPrinterDriver** avec *cbBuf* défini à zéro.</span><span class="sxs-lookup"><span data-stu-id="ef03a-137">To determine the required buffer size, call **GetPrinterDriver** with *cbBuf* set to zero.</span></span> <span data-ttu-id="ef03a-138">**GetPrinterDriver** échoue, [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne une \_ erreur \_ de mémoire tampon insuffisante et le paramètre *pcbNeeded* retourne la taille, en octets, de la mémoire tampon nécessaire pour contenir le tableau de structures et leurs données.</span><span class="sxs-lookup"><span data-stu-id="ef03a-138">**GetPrinterDriver** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

</dd> <dt>

<span data-ttu-id="ef03a-139">*cbBuf* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ef03a-139">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef03a-140">Taille, en octets, du tableau auquel *pDriverInfo* pointe.</span><span class="sxs-lookup"><span data-stu-id="ef03a-140">The size, in bytes, of the array at which *pDriverInfo* points.</span></span>

</dd> <dt>

<span data-ttu-id="ef03a-141">*pcbNeeded* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ef03a-141">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef03a-142">Pointeur vers une valeur qui reçoit le nombre d’octets copiés si la fonction est réussie ou le nombre d’octets requis si *cbBuf* est trop petit.</span><span class="sxs-lookup"><span data-stu-id="ef03a-142">A pointer to a value that receives the number of bytes copied if the function succeeds or the number of bytes required if *cbBuf* is too small.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef03a-143">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ef03a-143">Return value</span></span>

<span data-ttu-id="ef03a-144">Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="ef03a-144">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="ef03a-145">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="ef03a-145">If the function fails, the return value is zero.</span></span>

<span data-ttu-id="ef03a-146">Pour un pilote inexistant, la fonction retourne l’erreur \_ \_ pilote d’imprimante inconnu \_ .</span><span class="sxs-lookup"><span data-stu-id="ef03a-146">For a non-existent driver, the function returns ERROR\_UNKNOWN\_PRINTER\_DRIVER.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef03a-147">Notes</span><span class="sxs-lookup"><span data-stu-id="ef03a-147">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ef03a-148">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="ef03a-148">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="ef03a-149">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="ef03a-149">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="ef03a-150">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="ef03a-150">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="ef03a-151">Les structures informations sur le pilote [**\_ \_ 2**](driver-info-2.md), informations sur le pilote [**\_ \_ 3**](driver-info-3.md), informations sur le pilote [**\_ \_ 4**](driver-info-4.md), [**\_ informations sur le pilote \_ 5**](driver-info-5.md)et [**\_ informations sur le pilote \_ 6**](driver-info-6.md) contiennent le nom de fichier, le chemin d’accès complet et le nom de fichier du pilote d’imprimante dans le membre **pDriverPath** .</span><span class="sxs-lookup"><span data-stu-id="ef03a-151">The [**DRIVER\_INFO\_2**](driver-info-2.md), [**DRIVER\_INFO\_3**](driver-info-3.md), [**DRIVER\_INFO\_4**](driver-info-4.md), [**DRIVER\_INFO\_5**](driver-info-5.md), and [**DRIVER\_INFO\_6**](driver-info-6.md) structures contain the file name or the full path and file name of the printer driver in the **pDriverPath** member.</span></span> <span data-ttu-id="ef03a-152">Une application peut utiliser le chemin d’accès et le nom de fichier pour charger un pilote d’imprimante en appelant la fonction [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et en spécifiant le chemin d’accès et le nom de fichier comme argument unique.</span><span class="sxs-lookup"><span data-stu-id="ef03a-152">An application can use the path and file name to load a printer driver by calling the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) function and supplying the path and file name as the single argument.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef03a-153">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ef03a-153">Requirements</span></span>



| <span data-ttu-id="ef03a-154">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ef03a-154">Requirement</span></span> | <span data-ttu-id="ef03a-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef03a-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef03a-156">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef03a-156">Minimum supported client</span></span><br/> | <span data-ttu-id="ef03a-157">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ef03a-157">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ef03a-158">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef03a-158">Minimum supported server</span></span><br/> | <span data-ttu-id="ef03a-159">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ef03a-159">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ef03a-160">En-tête</span><span class="sxs-lookup"><span data-stu-id="ef03a-160">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef03a-161"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ef03a-161"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="ef03a-162">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ef03a-162">Library</span></span><br/>                  | <dl> <span data-ttu-id="ef03a-163"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ef03a-163"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="ef03a-164">DLL</span><span class="sxs-lookup"><span data-stu-id="ef03a-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef03a-165"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="ef03a-165"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="ef03a-166">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="ef03a-166">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ef03a-167">**GetPrinterDriverW** (Unicode) et **GetPrinterDriverA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ef03a-167">**GetPrinterDriverW** (Unicode) and **GetPrinterDriverA** (ANSI)</span></span><br/>                               |



## <a name="see-also"></a><span data-ttu-id="ef03a-168">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef03a-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef03a-169">Impression</span><span class="sxs-lookup"><span data-stu-id="ef03a-169">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="ef03a-170">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="ef03a-170">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="ef03a-171">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="ef03a-171">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="ef03a-172">**\_Informations sur le pilote \_ 1**</span><span class="sxs-lookup"><span data-stu-id="ef03a-172">**DRIVER\_INFO\_1**</span></span>](driver-info-1.md)
</dt> <dt>

[<span data-ttu-id="ef03a-173">**\_Informations sur le pilote \_ 2**</span><span class="sxs-lookup"><span data-stu-id="ef03a-173">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)
</dt> <dt>

[<span data-ttu-id="ef03a-174">**\_Informations sur le pilote \_ 3**</span><span class="sxs-lookup"><span data-stu-id="ef03a-174">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)
</dt> <dt>

[<span data-ttu-id="ef03a-175">**\_Informations sur le pilote \_ 4**</span><span class="sxs-lookup"><span data-stu-id="ef03a-175">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)
</dt> <dt>

[<span data-ttu-id="ef03a-176">**\_Informations sur le pilote \_ 5**</span><span class="sxs-lookup"><span data-stu-id="ef03a-176">**DRIVER\_INFO\_5**</span></span>](driver-info-5.md)
</dt> <dt>

[<span data-ttu-id="ef03a-177">**\_Informations sur le pilote \_ 6**</span><span class="sxs-lookup"><span data-stu-id="ef03a-177">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)
</dt> <dt>

[<span data-ttu-id="ef03a-178">**EnumPrinterDrivers**</span><span class="sxs-lookup"><span data-stu-id="ef03a-178">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="ef03a-179">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="ef03a-179">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

