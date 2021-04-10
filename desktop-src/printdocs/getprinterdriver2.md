---
description: La fonction GetPrinterDriver2 récupère les données du pilote pour l’imprimante spécifiée. Si le pilote n’est pas installé sur l’ordinateur local, GetPrinterDriver2 l’installe et affiche l’interface utilisateur dans la fenêtre spécifiée.
ms.assetid: 0d482d28-7668-4734-ba71-5b355c18ddec
title: GetPrinterDriver2, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDriver2
- GetPrinterDriver2W
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: b0a9d2bfe7827a2c0e3db9fff9e8249b73bf5102
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210474"
---
# <a name="getprinterdriver2-function"></a><span data-ttu-id="19e4a-104">GetPrinterDriver2 fonction)</span><span class="sxs-lookup"><span data-stu-id="19e4a-104">GetPrinterDriver2 function</span></span>

<span data-ttu-id="19e4a-105">La fonction **GetPrinterDriver2** récupère les données du pilote pour l’imprimante spécifiée.</span><span class="sxs-lookup"><span data-stu-id="19e4a-105">The **GetPrinterDriver2** function retrieves driver data for the specified printer.</span></span> <span data-ttu-id="19e4a-106">Si le pilote n’est pas installé sur l’ordinateur local, **GetPrinterDriver2** l’installe et affiche l’interface utilisateur dans la fenêtre spécifiée.</span><span class="sxs-lookup"><span data-stu-id="19e4a-106">If the driver is not installed on the local computer, **GetPrinterDriver2** installs it and displays any user interface to the specified window.</span></span>

## <a name="syntax"></a><span data-ttu-id="19e4a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="19e4a-107">Syntax</span></span>


```C++
BOOL GetPrinterDriver2(
  _In_opt_ HWND    hWnd,
  _In_     HANDLE  hPrinter,
  _In_opt_ LPTSTR  pEnvironment,
  _In_     DWORD   Level,
  _Out_    LPBYTE  pDriverInfo,
  _In_     DWORD   cbBuf,
  _Out_    LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="19e4a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="19e4a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19e4a-109">*HWND* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="19e4a-109">*hWnd* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="19e4a-110">Handle de la fenêtre qui sera utilisée comme fenêtre parente d’une interface utilisateur, telle qu’une boîte de dialogue, que le pilote affiche au cours de l’installation.</span><span class="sxs-lookup"><span data-stu-id="19e4a-110">A handle of the window that will be used as the parent window of any user interface, such as a dialog box, that the driver displays during installation.</span></span> <span data-ttu-id="19e4a-111">Si la valeur de ce paramètre est **null**, l’interface utilisateur du pilote est toujours affichée à l’utilisateur lors de l’installation, mais elle n’a pas de fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="19e4a-111">If the value of this parameter is **NULL**, the driver's user interface will still be displayed to the user during installation, but it will not have a parent window.</span></span>

</dd> <dt>

<span data-ttu-id="19e4a-112">*hPrinter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="19e4a-112">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19e4a-113">Handle vers l’imprimante pour laquelle les données du pilote doivent être récupérées.</span><span class="sxs-lookup"><span data-stu-id="19e4a-113">A handle to the printer for which the driver data should be retrieved.</span></span> <span data-ttu-id="19e4a-114">Utilisez la fonction [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="19e4a-114">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="19e4a-115">*pEnvironment* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="19e4a-115">*pEnvironment* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="19e4a-116">Pointeur vers une chaîne se terminant par un caractère null qui spécifie l’environnement (par exemple, Windows x86, Windows IA64 ou Windows x64).</span><span class="sxs-lookup"><span data-stu-id="19e4a-116">A pointer to a null-terminated string that specifies the environment (for example, Windows x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="19e4a-117">Si ce paramètre a la **valeur null**, l’environnement actuel de l’application appelante et de l’ordinateur client (pas du serveur d’impression et de l’application de destination) est utilisé.</span><span class="sxs-lookup"><span data-stu-id="19e4a-117">If this parameter is **NULL**, the current environment of the calling application and client machine (not of the destination application and print server) is used.</span></span>

</dd> <dt>

<span data-ttu-id="19e4a-118">De *niveau* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="19e4a-118">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19e4a-119">Structure du pilote d’imprimante renvoyée dans la mémoire tampon *pDriverInfo* .</span><span class="sxs-lookup"><span data-stu-id="19e4a-119">The printer driver structure returned in the *pDriverInfo* buffer.</span></span> <span data-ttu-id="19e4a-120">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="19e4a-120">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="19e4a-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="19e4a-121">Value</span></span>                                                                                                | <span data-ttu-id="19e4a-122">Signification</span><span class="sxs-lookup"><span data-stu-id="19e4a-122">Meaning</span></span>                                             |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="19e4a-123"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="19e4a-123"><dt>**1**</dt></span></span> </dl> | [<span data-ttu-id="19e4a-124">**\_Informations sur le pilote \_ 1**</span><span class="sxs-lookup"><span data-stu-id="19e4a-124">**DRIVER\_INFO\_1**</span></span>](driver-info-1.md)<br/> |
| <span id="2"></span><dl> <span data-ttu-id="19e4a-125"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="19e4a-125"><dt>**2**</dt></span></span> </dl> | [<span data-ttu-id="19e4a-126">**\_Informations sur le pilote \_ 2**</span><span class="sxs-lookup"><span data-stu-id="19e4a-126">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)<br/> |
| <span id="3"></span><dl> <span data-ttu-id="19e4a-127"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="19e4a-127"><dt>**3**</dt></span></span> </dl> | [<span data-ttu-id="19e4a-128">**\_Informations sur le pilote \_ 3**</span><span class="sxs-lookup"><span data-stu-id="19e4a-128">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)<br/> |
| <span id="4"></span><dl> <span data-ttu-id="19e4a-129"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="19e4a-129"><dt>**4**</dt></span></span> </dl> | [<span data-ttu-id="19e4a-130">**\_Informations sur le pilote \_ 4**</span><span class="sxs-lookup"><span data-stu-id="19e4a-130">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)<br/> |
| <span id="5"></span><dl> <span data-ttu-id="19e4a-131"><dt>**5**</dt></span><span class="sxs-lookup"><span data-stu-id="19e4a-131"><dt>**5**</dt></span></span> </dl> | [<span data-ttu-id="19e4a-132">**\_Informations sur le pilote \_ 5**</span><span class="sxs-lookup"><span data-stu-id="19e4a-132">**DRIVER\_INFO\_5**</span></span>](driver-info-5.md)<br/> |
| <span id="6"></span><dl> <span data-ttu-id="19e4a-133"><dt>**6**</dt></span><span class="sxs-lookup"><span data-stu-id="19e4a-133"><dt>**6**</dt></span></span> </dl> | [<span data-ttu-id="19e4a-134">**\_Informations sur le pilote \_ 6**</span><span class="sxs-lookup"><span data-stu-id="19e4a-134">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)<br/> |
| <span id="8"></span><dl> <span data-ttu-id="19e4a-135"><dt>**8**</dt></span><span class="sxs-lookup"><span data-stu-id="19e4a-135"><dt>**8**</dt></span></span> </dl> | [<span data-ttu-id="19e4a-136">**\_Informations sur le pilote \_ 8**</span><span class="sxs-lookup"><span data-stu-id="19e4a-136">**DRIVER\_INFO\_8**</span></span>](driver-info-8.md)<br/> |



 

</dd> <dt>

<span data-ttu-id="19e4a-137">*pDriverInfo* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="19e4a-137">*pDriverInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="19e4a-138">Pointeur vers une mémoire tampon qui reçoit une structure contenant des informations sur le pilote, comme spécifié par le *niveau*.</span><span class="sxs-lookup"><span data-stu-id="19e4a-138">A pointer to a buffer that receives a structure containing information about the driver, as specified by *Level*.</span></span> <span data-ttu-id="19e4a-139">La mémoire tampon doit être suffisamment grande pour stocker les chaînes pointées par les membres de la structure.</span><span class="sxs-lookup"><span data-stu-id="19e4a-139">The buffer must be large enough to store the strings pointed to by the structure members.</span></span>

<span data-ttu-id="19e4a-140">Pour déterminer la taille de mémoire tampon requise, appelez **GetPrinterDriver2** avec *cbBuf* défini à zéro.</span><span class="sxs-lookup"><span data-stu-id="19e4a-140">To determine the required buffer size, call **GetPrinterDriver2** with *cbBuf* set to zero.</span></span> <span data-ttu-id="19e4a-141">**GetPrinterDriver2** échoue, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne une **erreur de \_ \_ mémoire tampon insuffisante** et le paramètre *pcbNeeded* retourne la taille, en octets, de la mémoire tampon nécessaire pour contenir le tableau de structures et leurs données.</span><span class="sxs-lookup"><span data-stu-id="19e4a-141">**GetPrinterDriver2** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns **ERROR\_INSUFFICIENT\_BUFFER**, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

</dd> <dt>

<span data-ttu-id="19e4a-142">*cbBuf* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="19e4a-142">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19e4a-143">Taille, en octets, du tableau auquel *pDriverInfo* pointe.</span><span class="sxs-lookup"><span data-stu-id="19e4a-143">The size, in bytes, of the array at which *pDriverInfo* points.</span></span>

</dd> <dt>

<span data-ttu-id="19e4a-144">*pcbNeeded* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="19e4a-144">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="19e4a-145">Pointeur vers une valeur qui reçoit le nombre d’octets copiés si la fonction est réussie ou le nombre d’octets requis si *cbBuf* est trop petit.</span><span class="sxs-lookup"><span data-stu-id="19e4a-145">A pointer to a value that receives the number of bytes copied if the function succeeds or the number of bytes required if *cbBuf* is too small.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19e4a-146">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="19e4a-146">Return value</span></span>

<span data-ttu-id="19e4a-147">Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="19e4a-147">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="19e4a-148">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="19e4a-148">If the function fails, the return value is zero.</span></span> <span data-ttu-id="19e4a-149">Pour obtenir l’état de retour, appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="19e4a-149">To get the return status, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="19e4a-150">Notes</span><span class="sxs-lookup"><span data-stu-id="19e4a-150">Remarks</span></span>

<span data-ttu-id="19e4a-151">Les informations relatives aux pilotes [**\_ \_ 2**](driver-info-2.md), informations sur le pilote [**\_ \_ 3**](driver-info-3.md), informations sur le pilote [**\_ \_ 4**](driver-info-4.md), informations sur le pilote [**\_ \_ 5**](driver-info-5.md), [**\_ informations sur le pilote \_ 6**](driver-info-6.md)et structures [**\_ informations sur le pilote \_ 8**](driver-info-8.md) contiennent le nom du fichier, le chemin d’accès complet et le nom du pilote d’imprimante dans le membre **pDriverPath** .</span><span class="sxs-lookup"><span data-stu-id="19e4a-151">The [**DRIVER\_INFO\_2**](driver-info-2.md), [**DRIVER\_INFO\_3**](driver-info-3.md), [**DRIVER\_INFO\_4**](driver-info-4.md), [**DRIVER\_INFO\_5**](driver-info-5.md), [**DRIVER\_INFO\_6**](driver-info-6.md), and [**DRIVER\_INFO\_8**](driver-info-8.md) structures contain the file name or the full path and file name of the printer driver in the **pDriverPath** member.</span></span> <span data-ttu-id="19e4a-152">Une application peut utiliser le chemin d’accès et le nom de fichier pour charger un pilote d’imprimante en appelant la fonction [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et en spécifiant le chemin d’accès et le nom de fichier comme argument unique.</span><span class="sxs-lookup"><span data-stu-id="19e4a-152">An application can use the path and file name to load a printer driver by calling the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) function and supplying the path and file name as the single argument.</span></span>

<span data-ttu-id="19e4a-153">La version ANSI de cette fonction, **GetPrinterDriver2A** n’est pas prise en charge et retourne une **erreur \_ non \_ prise en charge**.</span><span class="sxs-lookup"><span data-stu-id="19e4a-153">The ANSI version of this function, **GetPrinterDriver2A** is not supported and returns **ERROR\_NOT\_SUPPORTED**.</span></span>

## <a name="requirements"></a><span data-ttu-id="19e4a-154">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="19e4a-154">Requirements</span></span>



| <span data-ttu-id="19e4a-155">Condition requise</span><span class="sxs-lookup"><span data-stu-id="19e4a-155">Requirement</span></span> | <span data-ttu-id="19e4a-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="19e4a-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19e4a-157">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="19e4a-157">Minimum supported client</span></span><br/> | <span data-ttu-id="19e4a-158">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="19e4a-158">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="19e4a-159">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="19e4a-159">Minimum supported server</span></span><br/> | <span data-ttu-id="19e4a-160">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="19e4a-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="19e4a-161">En-tête</span><span class="sxs-lookup"><span data-stu-id="19e4a-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="19e4a-162"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="19e4a-162"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="19e4a-163">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="19e4a-163">Library</span></span><br/>                  | <dl> <span data-ttu-id="19e4a-164"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="19e4a-164"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="19e4a-165">DLL</span><span class="sxs-lookup"><span data-stu-id="19e4a-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19e4a-166"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="19e4a-166"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="19e4a-167">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="19e4a-167">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="19e4a-168">**GetPrinterDriver2W** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="19e4a-168">**GetPrinterDriver2W** (Unicode)</span></span><br/>                                                               |



## <a name="see-also"></a><span data-ttu-id="19e4a-169">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="19e4a-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19e4a-170">Impression</span><span class="sxs-lookup"><span data-stu-id="19e4a-170">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="19e4a-171">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="19e4a-171">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="19e4a-172">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="19e4a-172">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="19e4a-173">**\_Informations sur le pilote \_ 1**</span><span class="sxs-lookup"><span data-stu-id="19e4a-173">**DRIVER\_INFO\_1**</span></span>](driver-info-1.md)
</dt> <dt>

[<span data-ttu-id="19e4a-174">**\_Informations sur le pilote \_ 2**</span><span class="sxs-lookup"><span data-stu-id="19e4a-174">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)
</dt> <dt>

[<span data-ttu-id="19e4a-175">**\_Informations sur le pilote \_ 3**</span><span class="sxs-lookup"><span data-stu-id="19e4a-175">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)
</dt> <dt>

[<span data-ttu-id="19e4a-176">**\_Informations sur le pilote \_ 4**</span><span class="sxs-lookup"><span data-stu-id="19e4a-176">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)
</dt> <dt>

[<span data-ttu-id="19e4a-177">**\_Informations sur le pilote \_ 5**</span><span class="sxs-lookup"><span data-stu-id="19e4a-177">**DRIVER\_INFO\_5**</span></span>](driver-info-5.md)
</dt> <dt>

[<span data-ttu-id="19e4a-178">**\_Informations sur le pilote \_ 6**</span><span class="sxs-lookup"><span data-stu-id="19e4a-178">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)
</dt> <dt>

[<span data-ttu-id="19e4a-179">**EnumPrinterDrivers**</span><span class="sxs-lookup"><span data-stu-id="19e4a-179">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="19e4a-180">**GetPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="19e4a-180">**GetPrinterDriver**</span></span>](getprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="19e4a-181">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="19e4a-181">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

