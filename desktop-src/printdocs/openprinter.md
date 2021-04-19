---
description: La fonction OpenPrinter récupère un handle vers l’imprimante ou le serveur d’impression spécifié ou d’autres types de handles dans le sous-système d’impression.
ms.assetid: 96763220-d851-46f0-8be8-403f3356edb9
title: OpenPrinter, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OpenPrinter
- OpenPrinterA
- OpenPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-0.dll
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 02cd6f6b5d56eec525bd00e2feef50f4d5f07734
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531981"
---
# <a name="openprinter-function"></a><span data-ttu-id="d7712-103">OpenPrinter fonction)</span><span class="sxs-lookup"><span data-stu-id="d7712-103">OpenPrinter function</span></span>

<span data-ttu-id="d7712-104">La fonction **OpenPrinter** récupère un handle vers l’imprimante ou le serveur d’impression spécifié ou d’autres types de handles dans le sous-système d’impression.</span><span class="sxs-lookup"><span data-stu-id="d7712-104">The **OpenPrinter** function retrieves a handle to the specified printer or print server or other types of handles in the print subsystem.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7712-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d7712-105">Syntax</span></span>


```C++
BOOL OpenPrinter(
  _In_  LPTSTR             pPrinterName,
  _Out_ LPHANDLE           phPrinter,
  _In_  LPPRINTER_DEFAULTS pDefault
);
```



## <a name="parameters"></a><span data-ttu-id="d7712-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d7712-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7712-107">*pPrinterName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d7712-107">*pPrinterName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7712-108">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom de l’imprimante ou du serveur d’impression, de l’objet Printer, du XcvMonitor ou du XcvPort.</span><span class="sxs-lookup"><span data-stu-id="d7712-108">A pointer to a null-terminated string that specifies the name of the printer or print server, the printer object, the XcvMonitor, or the XcvPort.</span></span>

<span data-ttu-id="d7712-109">Pour un objet Printer, utilisez : nom_imprimante, Job xxxx.</span><span class="sxs-lookup"><span data-stu-id="d7712-109">For a printer object use: PrinterName, Job xxxx.</span></span> <span data-ttu-id="d7712-110">Pour un XcvMonitor, utilisez : ServerName, XcvMonitor Nomdumoniteur.</span><span class="sxs-lookup"><span data-stu-id="d7712-110">For an XcvMonitor, use: ServerName, XcvMonitor MonitorName.</span></span> <span data-ttu-id="d7712-111">Pour un XcvPort, utilisez : ServerName, XcvPort PortName.</span><span class="sxs-lookup"><span data-stu-id="d7712-111">For an XcvPort, use: ServerName, XcvPort PortName.</span></span>

<span data-ttu-id="d7712-112">Si la **valeur est null**, le serveur d’impression local est activé.</span><span class="sxs-lookup"><span data-stu-id="d7712-112">If **NULL**, it indicates the local printer server.</span></span>

</dd> <dt>

<span data-ttu-id="d7712-113">*phPrinter* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d7712-113">*phPrinter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7712-114">Pointeur vers une variable qui reçoit un handle (non thread-safe) vers l’imprimante ou l’objet serveur d’impression ouvert.</span><span class="sxs-lookup"><span data-stu-id="d7712-114">A pointer to a variable that receives a handle (not thread safe) to the open printer or print server object.</span></span>

<span data-ttu-id="d7712-115">Le paramètre *phPrinter* peut retourner un handle XCV à utiliser avec la fonction XcvData.</span><span class="sxs-lookup"><span data-stu-id="d7712-115">The *phPrinter* parameter can return an Xcv handle for use with the XcvData function.</span></span> <span data-ttu-id="d7712-116">Pour plus d’informations sur XcvData, consultez le DDK.</span><span class="sxs-lookup"><span data-stu-id="d7712-116">For more information about XcvData, see the DDK.</span></span>

</dd> <dt>

<span data-ttu-id="d7712-117">*pDefault* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d7712-117">*pDefault* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7712-118">Pointeur vers une structure d' [**imprimante \_ par défaut**](printer-defaults.md) .</span><span class="sxs-lookup"><span data-stu-id="d7712-118">A pointer to a [**PRINTER\_DEFAULTS**](printer-defaults.md) structure.</span></span> <span data-ttu-id="d7712-119">Cette valeur peut être **null**.</span><span class="sxs-lookup"><span data-stu-id="d7712-119">This value can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7712-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d7712-120">Return value</span></span>

<span data-ttu-id="d7712-121">Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="d7712-121">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="d7712-122">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="d7712-122">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7712-123">Notes</span><span class="sxs-lookup"><span data-stu-id="d7712-123">Remarks</span></span>

<span data-ttu-id="d7712-124">N’appelez pas cette méthode dans [**DllMain**](/windows/desktop/Dlls/dllmain).</span><span class="sxs-lookup"><span data-stu-id="d7712-124">Do not call this method in [**DllMain**](/windows/desktop/Dlls/dllmain).</span></span>

> [!Note]  
> <span data-ttu-id="d7712-125">Un handle obtenu pour une imprimante distante par un appel à **OpenPrinter** pour une imprimante distante accède à l’imprimante via un cache local dans le service spouleur d’impression.</span><span class="sxs-lookup"><span data-stu-id="d7712-125">A handle obtained for a remote printer by a call to **OpenPrinter** for a remote printer accesses the printer through a local cache in the print spooler service.</span></span> <span data-ttu-id="d7712-126">Ce cache n’est pas précis en temps réel.</span><span class="sxs-lookup"><span data-stu-id="d7712-126">This cache isn't real-time accurate.</span></span> <span data-ttu-id="d7712-127">Pour obtenir des données précises, remplacez l’appel de OpenPrinter par [**OpenPrinter2**](openprinter2.md) par POptions. dwFlags défini sur Printer \_ option \_ no \_ cache.</span><span class="sxs-lookup"><span data-stu-id="d7712-127">To obtain accurate data, replace the OpenPrinter call with [**OpenPrinter2**](openprinter2.md) with pOptions.dwFlags set to PRINTER\_OPTION\_NO\_CACHE.</span></span> <span data-ttu-id="d7712-128">Notez que seul OpenPrinter2W est fonctionnel.</span><span class="sxs-lookup"><span data-stu-id="d7712-128">Note that only OpenPrinter2W is functional.</span></span> <span data-ttu-id="d7712-129">La fonction retourne un handle d’imprimante qui utilise d’autres appels d’API d’impression et contourne le cache local.</span><span class="sxs-lookup"><span data-stu-id="d7712-129">The function returns a printer handle that uses other Printing API calls and bypasses the local cache.</span></span> <span data-ttu-id="d7712-130">Cette méthode bloque tout en attendant la communication réseau avec l’imprimante distante, il est donc possible qu’elle ne soit pas renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="d7712-130">This method blocks while waiting for network communication with the remote printer, so it might not return immediately.</span></span> <span data-ttu-id="d7712-131">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="d7712-131">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="d7712-132">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut rendre l’application sans réponse.</span><span class="sxs-lookup"><span data-stu-id="d7712-132">Calling this function from a thread that manages user interface interaction might make the application appear unresponsive.</span></span>

 

> [!Note]  
> <span data-ttu-id="d7712-133">Un handle obtenu par un appel à **OpenPrinter** pour une imprimante distante accède à l’imprimante via un cache local dans le service spouleur d’impression.</span><span class="sxs-lookup"><span data-stu-id="d7712-133">A handle obtained by a call to **OpenPrinter** for a remote printer will access the printer through a local cache in the print spooler service.</span></span> <span data-ttu-id="d7712-134">Ce cache est, de par sa conception, non précis en temps réel.</span><span class="sxs-lookup"><span data-stu-id="d7712-134">This cache is, by design, not real time accurate.</span></span> <span data-ttu-id="d7712-135">Si vous devez obtenir des données précises, remplacez l’appel de **OpenPrinter** par [**OpenPrinter2**](openprinter2.md) par *POptions. dwFlags* défini [**sur \_ Printer option \_ no \_ cache**](printer-options.md).</span><span class="sxs-lookup"><span data-stu-id="d7712-135">If you need to obtain accurate data, replace the **OpenPrinter** call with [**OpenPrinter2**](openprinter2.md) with *pOptions.dwFlags* set to [**PRINTER\_OPTION\_NO\_CACHE**](printer-options.md).</span></span> <span data-ttu-id="d7712-136">Notez que seul **OpenPrinter2W** est fonctionnel.</span><span class="sxs-lookup"><span data-stu-id="d7712-136">Note that only **OpenPrinter2W** is functional.</span></span> <span data-ttu-id="d7712-137">En procédant ainsi, la fonction retourne un handle d’imprimante qui effectue d’autres appels d’API d’impression pour contourner le cache local.</span><span class="sxs-lookup"><span data-stu-id="d7712-137">Doing so the function returns a printer handle that makes other Printing API calls to bypass the local cache.</span></span> <span data-ttu-id="d7712-138">Notez que cette approche sera bloquée en attendant la communication réseau aller-retour à l’imprimante distante, de sorte qu’elle risque de ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="d7712-138">Note that this approach will block while waiting for the round-trip network communication to the remote printer, so it may not return immediately.</span></span> <span data-ttu-id="d7712-139">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et l’implémentation du pilote d’imprimante, facteurs difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="d7712-139">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation - factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="d7712-140">Par conséquent, l’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="d7712-140">Therefore calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="d7712-141">Le handle pointé par *phPrinter* n’est pas thread-safe.</span><span class="sxs-lookup"><span data-stu-id="d7712-141">The handle pointed to by *phPrinter* is not thread safe.</span></span> <span data-ttu-id="d7712-142">Si les appelants doivent l’utiliser simultanément sur plusieurs threads, ils doivent fournir un accès de synchronisation personnalisé au handle d’imprimante à l’aide des [fonctions de synchronisation](/windows/desktop/Sync/synchronization-functions).</span><span class="sxs-lookup"><span data-stu-id="d7712-142">If callers need to use it concurrently on multiple threads, they must provide custom synchronization access to the printer handle using the [Synchronization Functions](/windows/desktop/Sync/synchronization-functions).</span></span> <span data-ttu-id="d7712-143">Pour éviter d’écrire du code personnalisé, l’application peut ouvrir un handle d’imprimante sur chaque thread, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="d7712-143">To avoid writing custom code the application can open a printer handle on each thread, as needed.</span></span>

<span data-ttu-id="d7712-144">Le paramètre *pDefault* vous permet de spécifier les valeurs du type de données et du mode de l’appareil utilisées pour l’impression des documents soumis par la fonction [**StartDocPrinter**](startdocprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="d7712-144">The *pDefault* parameter enables you to specify the data type and device mode values that are used for printing documents submitted by the [**StartDocPrinter**](startdocprinter.md) function.</span></span> <span data-ttu-id="d7712-145">Toutefois, vous pouvez remplacer ces valeurs à l’aide de la fonction [**SetJob**](setjob.md) après le démarrage d’un document.</span><span class="sxs-lookup"><span data-stu-id="d7712-145">However, you can override these values by using the [**SetJob**](setjob.md) function after a document has been started.</span></span>

<span data-ttu-id="d7712-146">Les paramètres [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) définis dans la [**structure \_ par défaut**](printer-defaults.md) de l’imprimante du paramètre *pDefault* ne sont pas utilisés lorsque la valeur du membre *pDatatype* de la structure [**\_ infos doc \_ 1**](doc-info-1.md) qui a été transmise dans le paramètre *pDocInfo* de l’appel [**StartDocPrinter**](startdocprinter.md) est « RAW ».</span><span class="sxs-lookup"><span data-stu-id="d7712-146">The [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) settings defined in the [**PRINTER\_DEFAULTS**](printer-defaults.md) structure of the *pDefault* parameter are not used when the value of the *pDatatype* member of the [**DOC\_INFO\_1**](doc-info-1.md) structure that was passed in the *pDocInfo* parameter of the [**StartDocPrinter**](startdocprinter.md) call is "RAW".</span></span> <span data-ttu-id="d7712-147">Lorsqu’un document de niveau supérieur (par exemple, un fichier Adobe PDF ou Microsoft Word) ou d’autres données d’imprimante (par exemple, PCL, PS ou HPGL) est envoyé directement à une imprimante avec *pDatatype* défini sur « RAW », le document doit décrire entièrement les paramètres du travail d’impression de style **DEVMODE** dans la langue comprise par le matériel.</span><span class="sxs-lookup"><span data-stu-id="d7712-147">When a high-level document (such as an Adobe PDF or Microsoft Word file) or other printer data (such PCL, PS, or HPGL) is sent directly to a printer with *pDatatype* set to "RAW", the document must fully describe the **DEVMODE**-style print job settings in the language understood by the hardware.</span></span>

<span data-ttu-id="d7712-148">Vous pouvez appeler la fonction **OpenPrinter** pour ouvrir un handle sur un serveur d’impression ou pour déterminer les droits d’accès d’un client à un serveur d’impression.</span><span class="sxs-lookup"><span data-stu-id="d7712-148">You can call the **OpenPrinter** function to open a handle to a print server or to determine the access rights that a client has to a print server.</span></span> <span data-ttu-id="d7712-149">Pour ce faire, spécifiez le nom du serveur d’impression dans le paramètre *pPrinterName* , définissez les membres **pDatatype** et **pDevMode** de la structure [**\_ par défaut**](printer-defaults.md) de l’imprimante sur la valeur **null**, puis définissez le membre **desiredAccess** de manière à spécifier une valeur de masque d’accès au serveur, par exemple \_ tous les \_ accès serveur.</span><span class="sxs-lookup"><span data-stu-id="d7712-149">To do so, specify the name of the print server in the *pPrinterName* parameter, set the **pDatatype** and **pDevMode** members of the [**PRINTER\_DEFAULTS**](printer-defaults.md) structure to **NULL**, and set the **DesiredAccess** member to specify a server access mask value such as SERVER\_ALL\_ACCESS.</span></span> <span data-ttu-id="d7712-150">Lorsque vous avez terminé avec le descripteur, transmettez-le à la fonction [**ClosePrinter**](closeprinter.md) pour le fermer.</span><span class="sxs-lookup"><span data-stu-id="d7712-150">When you finish with the handle, pass it to the [**ClosePrinter**](closeprinter.md) function to close it.</span></span>

<span data-ttu-id="d7712-151">Utilisez le membre **desiredAccess** de la [**structure \_ par défaut**](printer-defaults.md) de l’imprimante pour spécifier les droits d’accès dont vous avez besoin pour l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="d7712-151">Use the **DesiredAccess** member of the [**PRINTER\_DEFAULTS**](printer-defaults.md) structure to specify the access rights that you need to the printer.</span></span> <span data-ttu-id="d7712-152">Les droits d’accès peuvent être l’un des suivants :</span><span class="sxs-lookup"><span data-stu-id="d7712-152">The access rights can be one of the following.</span></span> <span data-ttu-id="d7712-153">(Si *pDefault* a la **valeur null**, les droits d’accès sont Printer \_ utilisation de l’accès \_ .)</span><span class="sxs-lookup"><span data-stu-id="d7712-153">(If *pDefault* is **NULL**, then the access rights are PRINTER\_ACCESS\_USE.)</span></span>



| <span data-ttu-id="d7712-154">Valeur d’accès souhaitée</span><span class="sxs-lookup"><span data-stu-id="d7712-154">Desired Access value</span></span>                        | <span data-ttu-id="d7712-155">Signification</span><span class="sxs-lookup"><span data-stu-id="d7712-155">Meaning</span></span>                                                                                                                                                                                      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7712-156">\_administration de l’accès aux imprimantes \_</span><span class="sxs-lookup"><span data-stu-id="d7712-156">PRINTER\_ACCESS\_ADMINISTER</span></span>                 | <span data-ttu-id="d7712-157">Pour effectuer des tâches d’administration, telles que celles fournies par [**SetPrinter**](setprinter.md).</span><span class="sxs-lookup"><span data-stu-id="d7712-157">To perform administrative tasks, such as those provided by [**SetPrinter**](setprinter.md).</span></span>                                                                                                 |
| <span data-ttu-id="d7712-158">\_utilisation de l’accès à l’imprimante \_</span><span class="sxs-lookup"><span data-stu-id="d7712-158">PRINTER\_ACCESS\_USE</span></span>                        | <span data-ttu-id="d7712-159">Pour effectuer des opérations d’impression de base.</span><span class="sxs-lookup"><span data-stu-id="d7712-159">To perform basic printing operations.</span></span>                                                                                                                                                        |
| <span data-ttu-id="d7712-160">\_tout \_ accès imprimante</span><span class="sxs-lookup"><span data-stu-id="d7712-160">PRINTER\_ALL\_ACCESS</span></span>                        | <span data-ttu-id="d7712-161">Pour effectuer toutes les tâches d’administration et les opérations d’impression de base, à l’exception de la synchronisation (consultez [droits d’accès standard](/windows/desktop/SecAuthZ/standard-access-rights).</span><span class="sxs-lookup"><span data-stu-id="d7712-161">To perform all administrative tasks and basic printing operations except for SYNCHRONIZE (see [Standard Access Rights](/windows/desktop/SecAuthZ/standard-access-rights).</span></span>                                     |
| <span data-ttu-id="d7712-162">\_gestion de l’accès à l’imprimante \_ \_ limitée</span><span class="sxs-lookup"><span data-stu-id="d7712-162">PRINTER\_ACCESS\_MANAGE\_LIMITED</span></span>            | <span data-ttu-id="d7712-163">Pour effectuer des tâches d’administration, telles que celles fournies par [**SetPrinter**](setprinter.md) et [**SetPrinterData**](setprinterdata.md).</span><span class="sxs-lookup"><span data-stu-id="d7712-163">To perform administrative tasks, such as those provided by [**SetPrinter**](setprinter.md) and [**SetPrinterData**](setprinterdata.md).</span></span> <span data-ttu-id="d7712-164">Cette valeur est disponible à partir de Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="d7712-164">This value is available starting from Windows 8.1.</span></span> |
| <span data-ttu-id="d7712-165">valeurs de sécurité génériques, telles que WRITE \_ DAC</span><span class="sxs-lookup"><span data-stu-id="d7712-165">generic security values, such as WRITE\_DAC</span></span> | <span data-ttu-id="d7712-166">Pour autoriser des droits d’accès de contrôle spécifiques.</span><span class="sxs-lookup"><span data-stu-id="d7712-166">To allow specific control access rights.</span></span> <span data-ttu-id="d7712-167">Consultez [droits d’accès standard](/windows/desktop/SecAuthZ/standard-access-rights).</span><span class="sxs-lookup"><span data-stu-id="d7712-167">See [Standard Access Rights](/windows/desktop/SecAuthZ/standard-access-rights).</span></span>                                                                                      |



 

<span data-ttu-id="d7712-168">Si un utilisateur n’est pas autorisé à ouvrir l’imprimante ou le serveur d’impression spécifié avec l’accès souhaité, l’appel **OpenPrinter** échoue avec une valeur de retour égale à zéro et [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne la valeur erreur \_ accès \_ refusé.</span><span class="sxs-lookup"><span data-stu-id="d7712-168">If a user does not have permission to open a specified printer or print server with the desired access, the **OpenPrinter** call will fail with a return value of zero and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) will return the value ERROR\_ACCESS\_DENIED.</span></span>

## <a name="examples"></a><span data-ttu-id="d7712-169">Exemples</span><span class="sxs-lookup"><span data-stu-id="d7712-169">Examples</span></span>

<span data-ttu-id="d7712-170">Pour obtenir un exemple de programme qui utilise cette fonction, consultez [Comment : imprimer à l’aide de l’API d’impression GDI](how-to--print-using-the-gdi-print-api.md).</span><span class="sxs-lookup"><span data-stu-id="d7712-170">For a sample program that uses this function, see [How To: Print Using the GDI Print API](how-to--print-using-the-gdi-print-api.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d7712-171">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d7712-171">Requirements</span></span>



| <span data-ttu-id="d7712-172">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d7712-172">Requirement</span></span> | <span data-ttu-id="d7712-173">Valeur</span><span class="sxs-lookup"><span data-stu-id="d7712-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7712-174">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7712-174">Minimum supported client</span></span><br/> | <span data-ttu-id="d7712-175">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d7712-175">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d7712-176">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7712-176">Minimum supported server</span></span><br/> | <span data-ttu-id="d7712-177">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d7712-177">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d7712-178">En-tête</span><span class="sxs-lookup"><span data-stu-id="d7712-178">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7712-179"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d7712-179"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="d7712-180">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d7712-180">Library</span></span><br/>                  | <dl> <span data-ttu-id="d7712-181"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d7712-181"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="d7712-182">DLL</span><span class="sxs-lookup"><span data-stu-id="d7712-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7712-183"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="d7712-183"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="d7712-184">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="d7712-184">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d7712-185">**OpenPrinterW** (Unicode) et **OpenPrinterA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d7712-185">**OpenPrinterW** (Unicode) and **OpenPrinterA** (ANSI)</span></span><br/>                                         |



## <a name="see-also"></a><span data-ttu-id="d7712-186">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7712-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7712-187">Impression</span><span class="sxs-lookup"><span data-stu-id="d7712-187">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="d7712-188">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="d7712-188">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="d7712-189">**WritePrinter**</span><span class="sxs-lookup"><span data-stu-id="d7712-189">**WritePrinter**</span></span>](writeprinter.md)
</dt> <dt>

[<span data-ttu-id="d7712-190">**ClosePrinter**</span><span class="sxs-lookup"><span data-stu-id="d7712-190">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="d7712-191">**\_valeurs par défaut de l’imprimante**</span><span class="sxs-lookup"><span data-stu-id="d7712-191">**PRINTER\_DEFAULTS**</span></span>](printer-defaults.md)
</dt> <dt>

[<span data-ttu-id="d7712-192">**SetJob**</span><span class="sxs-lookup"><span data-stu-id="d7712-192">**SetJob**</span></span>](setjob.md)
</dt> <dt>

[<span data-ttu-id="d7712-193">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="d7712-193">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="d7712-194">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="d7712-194">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> </dl>

 

