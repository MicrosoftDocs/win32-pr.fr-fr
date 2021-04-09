---
description: Récupère un handle vers l’imprimante, le serveur d’impression ou d’autres types de handles spécifiés dans le sous-système d’impression, tout en définissant certaines options d’imprimante.
ms.assetid: e2370ae4-4475-4ccc-a6f9-3d33d1370054
title: OpenPrinter2, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OpenPrinter2
- OpenPrinter2A
- OpenPrinter2W
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 46788d7ad810ef623cd77793a72ab6c046b73590
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865869"
---
# <a name="openprinter2-function"></a><span data-ttu-id="6065e-103">OpenPrinter2 fonction)</span><span class="sxs-lookup"><span data-stu-id="6065e-103">OpenPrinter2 function</span></span>

<span data-ttu-id="6065e-104">Récupère un handle vers l’imprimante, le serveur d’impression ou d’autres types de handles spécifiés dans le sous-système d’impression, tout en définissant certaines options d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="6065e-104">Retrieves a handle to the specified printer, print server, or other types of handles in the print subsystem, while setting some of the printer options.</span></span>

## <a name="syntax"></a><span data-ttu-id="6065e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6065e-105">Syntax</span></span>


```C++
BOOL OpenPrinter2(
  _In_  LPCTSTR            pPrinterName,
  _Out_ LPHANDLE           phPrinter,
  _In_  LPPRINTER_DEFAULTS pDefault,
  _In_  PPRINTER_OPTIONS   pOptions
);
```



## <a name="parameters"></a><span data-ttu-id="6065e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6065e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6065e-107">*pPrinterName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6065e-107">*pPrinterName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6065e-108">Pointeur vers une chaîne constante se terminant par un caractère null qui spécifie le nom de l’imprimante ou du serveur d’impression, l’objet Printer, XcvMonitor ou XcvPort.</span><span class="sxs-lookup"><span data-stu-id="6065e-108">A pointer to a constant null-terminated string that specifies the name of the printer or print server, the printer object, the XcvMonitor, or the XcvPort.</span></span>

<span data-ttu-id="6065e-109">Pour un objet Printer, utilisez : nom_imprimante, Job xxxx.</span><span class="sxs-lookup"><span data-stu-id="6065e-109">For a printer object, use: PrinterName,Job xxxx.</span></span> <span data-ttu-id="6065e-110">Pour un XcvMonitor, utilisez : ServerName, XcvMonitor Nomdumoniteur.</span><span class="sxs-lookup"><span data-stu-id="6065e-110">For an XcvMonitor, use: ServerName,XcvMonitor MonitorName.</span></span> <span data-ttu-id="6065e-111">Pour un XcvPort, utilisez : ServerName, XcvPort PortName.</span><span class="sxs-lookup"><span data-stu-id="6065e-111">For an XcvPort, use: ServerName,XcvPort PortName.</span></span>

<span data-ttu-id="6065e-112">**Windows Vista :** Si la **valeur est null**, le serveur d’impression local est activé.</span><span class="sxs-lookup"><span data-stu-id="6065e-112">**Windows Vista:** If **NULL**, it indicates the local print server.</span></span>

</dd> <dt>

<span data-ttu-id="6065e-113">*phPrinter* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6065e-113">*phPrinter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6065e-114">Pointeur vers une variable qui reçoit un handle vers l’imprimante ouverte ou l’objet serveur d’impression.</span><span class="sxs-lookup"><span data-stu-id="6065e-114">A pointer to a variable that receives a handle to the open printer or print server object.</span></span>

</dd> <dt>

<span data-ttu-id="6065e-115">*pDefault* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6065e-115">*pDefault* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6065e-116">Pointeur vers une structure d' [**imprimante \_ par défaut**](printer-defaults.md) .</span><span class="sxs-lookup"><span data-stu-id="6065e-116">A pointer to a [**PRINTER\_DEFAULTS**](printer-defaults.md) structure.</span></span> <span data-ttu-id="6065e-117">Cette valeur peut être **null**.</span><span class="sxs-lookup"><span data-stu-id="6065e-117">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6065e-118">*pOptions* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6065e-118">*pOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6065e-119">Pointeur vers une structure [**d' \_ options d’imprimante**](printer-options.md) .</span><span class="sxs-lookup"><span data-stu-id="6065e-119">A pointer to a [**PRINTER\_OPTIONS**](printer-options.md) structure.</span></span> <span data-ttu-id="6065e-120">Cette valeur peut être **null**.</span><span class="sxs-lookup"><span data-stu-id="6065e-120">This value can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6065e-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6065e-121">Return value</span></span>

<span data-ttu-id="6065e-122">Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="6065e-122">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="6065e-123">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="6065e-123">If the function fails, the return value is zero.</span></span> <span data-ttu-id="6065e-124">Pour obtenir des informations d’erreur étendues, appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="6065e-124">For extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="6065e-125">Notes</span><span class="sxs-lookup"><span data-stu-id="6065e-125">Remarks</span></span>

<span data-ttu-id="6065e-126">N’appelez pas cette méthode dans [**DllMain**](/windows/desktop/Dlls/dllmain).</span><span class="sxs-lookup"><span data-stu-id="6065e-126">Do not call this method in [**DllMain**](/windows/desktop/Dlls/dllmain).</span></span>

> [!Note]  
> <span data-ttu-id="6065e-127">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="6065e-127">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="6065e-128">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="6065e-128">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="6065e-129">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="6065e-129">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="6065e-130">La version ANSI de cette fonction n’est pas implémentée et retourne une erreur \_ non \_ prise en charge.</span><span class="sxs-lookup"><span data-stu-id="6065e-130">The ANSI version of this function is not implemented and returns ERROR\_NOT\_SUPPORTED.</span></span>

<span data-ttu-id="6065e-131">Le paramètre *pDefault* vous permet de spécifier les valeurs du type de données et du mode de l’appareil utilisées pour l’impression des documents soumis par la fonction [**StartDocPrinter**](startdocprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="6065e-131">The *pDefault* parameter enables you to specify the data type and device mode values that are used for printing documents submitted by the [**StartDocPrinter**](startdocprinter.md) function.</span></span> <span data-ttu-id="6065e-132">Toutefois, vous pouvez remplacer ces valeurs à l’aide de la fonction [**SetJob**](setjob.md) après le démarrage d’un document.</span><span class="sxs-lookup"><span data-stu-id="6065e-132">However, you can override these values by using the [**SetJob**](setjob.md) function after a document has been started.</span></span>

<span data-ttu-id="6065e-133">Vous pouvez appeler la fonction **OpenPrinter2** pour ouvrir un handle sur un serveur d’impression ou pour déterminer les droits d’accès client à un serveur d’impression.</span><span class="sxs-lookup"><span data-stu-id="6065e-133">You can call the **OpenPrinter2** function to open a handle to a print server or to determine client access rights to a print server.</span></span> <span data-ttu-id="6065e-134">Pour ce faire, spécifiez le nom du serveur d’impression dans le paramètre *pPrinterName* , définissez les membres **pDatatype** et **pDevMode** de la structure [**\_ par défaut**](printer-defaults.md) de l’imprimante sur la valeur **null**, puis définissez le membre **desiredAccess** de manière à spécifier une valeur de masque d’accès au serveur, par exemple \_ tous les \_ accès serveur.</span><span class="sxs-lookup"><span data-stu-id="6065e-134">To do this, specify the name of the print server in the *pPrinterName* parameter, set the **pDatatype** and **pDevMode** members of the [**PRINTER\_DEFAULTS**](printer-defaults.md) structure to **NULL**, and set the **DesiredAccess** member to specify a server access mask value such as SERVER\_ALL\_ACCESS.</span></span> <span data-ttu-id="6065e-135">Lorsque vous avez terminé avec le descripteur, transmettez-le à la fonction [**ClosePrinter**](closeprinter.md) pour le fermer.</span><span class="sxs-lookup"><span data-stu-id="6065e-135">When you are finished with the handle, pass it to the [**ClosePrinter**](closeprinter.md) function to close it.</span></span>

<span data-ttu-id="6065e-136">Utilisez le membre **desiredAccess** de la [**structure \_ par défaut**](printer-defaults.md) de l’imprimante pour spécifier les droits d’accès nécessaires.</span><span class="sxs-lookup"><span data-stu-id="6065e-136">Use the **DesiredAccess** member of the [**PRINTER\_DEFAULTS**](printer-defaults.md) structure to specify the necessary access rights.</span></span> <span data-ttu-id="6065e-137">Les droits d’accès peuvent être l’un des suivants :</span><span class="sxs-lookup"><span data-stu-id="6065e-137">The access rights can be one of the following.</span></span>



| <span data-ttu-id="6065e-138">Valeur d’accès souhaitée</span><span class="sxs-lookup"><span data-stu-id="6065e-138">Desired Access value</span></span>                        | <span data-ttu-id="6065e-139">Signification</span><span class="sxs-lookup"><span data-stu-id="6065e-139">Meaning</span></span>                                                                                                                                                                                      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6065e-140">\_administration de l’accès aux imprimantes \_</span><span class="sxs-lookup"><span data-stu-id="6065e-140">PRINTER\_ACCESS\_ADMINISTER</span></span>                 | <span data-ttu-id="6065e-141">Pour effectuer des tâches d’administration, telles que celles fournies par [**SetPrinter**](setprinter.md).</span><span class="sxs-lookup"><span data-stu-id="6065e-141">To perform administrative tasks, such as those provided by [**SetPrinter**](setprinter.md).</span></span>                                                                                                 |
| <span data-ttu-id="6065e-142">\_utilisation de l’accès à l’imprimante \_</span><span class="sxs-lookup"><span data-stu-id="6065e-142">PRINTER\_ACCESS\_USE</span></span>                        | <span data-ttu-id="6065e-143">Pour effectuer des opérations d’impression de base.</span><span class="sxs-lookup"><span data-stu-id="6065e-143">To perform basic printing operations.</span></span>                                                                                                                                                        |
| <span data-ttu-id="6065e-144">\_tout \_ accès imprimante</span><span class="sxs-lookup"><span data-stu-id="6065e-144">PRINTER\_ALL\_ACCESS</span></span>                        | <span data-ttu-id="6065e-145">Pour effectuer toutes les tâches d’administration et les opérations d’impression de base, à l’exception de SYNCHRONISEr.</span><span class="sxs-lookup"><span data-stu-id="6065e-145">To perform all administrative tasks and basic printing operations except SYNCHRONIZE.</span></span> <span data-ttu-id="6065e-146">Consultez [droits d’accès standard](/windows/desktop/SecAuthZ/standard-access-rights).</span><span class="sxs-lookup"><span data-stu-id="6065e-146">See [Standard Access Rights](/windows/desktop/SecAuthZ/standard-access-rights).</span></span>                                         |
| <span data-ttu-id="6065e-147">\_gestion de l’accès à l’imprimante \_ \_ limitée</span><span class="sxs-lookup"><span data-stu-id="6065e-147">PRINTER\_ACCESS\_MANAGE\_LIMITED</span></span>            | <span data-ttu-id="6065e-148">Pour effectuer des tâches d’administration, telles que celles fournies par [**SetPrinter**](setprinter.md) et [**SetPrinterData**](setprinterdata.md).</span><span class="sxs-lookup"><span data-stu-id="6065e-148">To perform administrative tasks, such as those provided by [**SetPrinter**](setprinter.md) and [**SetPrinterData**](setprinterdata.md).</span></span> <span data-ttu-id="6065e-149">Cette valeur est disponible à partir de Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="6065e-149">This value is available starting from Windows 8.1.</span></span> |
| <span data-ttu-id="6065e-150">valeurs de sécurité génériques, telles que WRITE \_ DAC</span><span class="sxs-lookup"><span data-stu-id="6065e-150">generic security values, such as WRITE\_DAC</span></span> | <span data-ttu-id="6065e-151">Pour autoriser des droits d’accès de contrôle spécifiques.</span><span class="sxs-lookup"><span data-stu-id="6065e-151">To allow specific control access rights.</span></span> <span data-ttu-id="6065e-152">Consultez [droits d’accès standard](/windows/desktop/SecAuthZ/standard-access-rights).</span><span class="sxs-lookup"><span data-stu-id="6065e-152">See [Standard Access Rights](/windows/desktop/SecAuthZ/standard-access-rights).</span></span>                                                                                      |



 

<span data-ttu-id="6065e-153">Si un utilisateur n’a pas l’autorisation d’ouvrir une imprimante ou un serveur d’impression spécifié avec l’accès souhaité, l’appel **OpenPrinter2** échoue et [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne la valeur erreur \_ accès \_ refusé.</span><span class="sxs-lookup"><span data-stu-id="6065e-153">If a user does not have permission to open a specified printer or print server with the desired access, the **OpenPrinter2** call will fail, and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) will return the value ERROR\_ACCESS\_DENIED.</span></span>

<span data-ttu-id="6065e-154">Quand *pPrinterName* est une imprimante locale, **OpenPrinter2** ignore toutes les valeurs de l' **dwFlags** que la structure des [**\_ options**](printer-options.md) de l’imprimante a référencées à l’aide de *pOptions*, à l’exception de l’option Printer \_ modification du \_ client \_ .</span><span class="sxs-lookup"><span data-stu-id="6065e-154">When *pPrinterName* is a local printer, then **OpenPrinter2** ignores all values of the **dwFlags** that the [**PRINTER\_OPTIONS**](printer-options.md) structure pointed to using *pOptions*, except PRINTER\_OPTION\_CLIENT\_CHANGE.</span></span> <span data-ttu-id="6065e-155">Si ce dernier est passé, **OpenPrinter2** retourne l’erreur \_ accès \_ refusé.</span><span class="sxs-lookup"><span data-stu-id="6065e-155">If the latter is passed, then **OpenPrinter2** will return ERROR\_ACCESS\_DENIED.</span></span> <span data-ttu-id="6065e-156">En conséquence, lors de l’ouverture d’une imprimante locale, **OpenPrinter2** n’offre aucun avantage sur [**OpenPrinter**](openprinter.md).</span><span class="sxs-lookup"><span data-stu-id="6065e-156">Accordingly, when opening a local printer, **OpenPrinter2** provides no advantage over [**OpenPrinter**](openprinter.md).</span></span>

<span data-ttu-id="6065e-157">**Windows Vista :** Les données d’imprimante retournées par **OpenPrinter2** sont extraites d’un cache local, sauf si l' **option d’imprimante aucun indicateur de \_ \_ \_ cache** n’est définie dans le champ **dwFlags** de la structure d' [**\_ options d’imprimante**](printer-options.md) référencée par *pOptions*.</span><span class="sxs-lookup"><span data-stu-id="6065e-157">**Windows Vista:** The printer data returned by **OpenPrinter2** is retrieved from a local cache unless the **PRINTER\_OPTION\_NO\_CACHE** flag is set in the **dwFlags** field of the [**PRINTER\_OPTIONS**](printer-options.md) structure referenced by *pOptions*.</span></span>

## <a name="examples"></a><span data-ttu-id="6065e-158">Exemples</span><span class="sxs-lookup"><span data-stu-id="6065e-158">Examples</span></span>

<span data-ttu-id="6065e-159">Dans cet exemple, **OpenPrinter2** échoue lorsque la \_ gestion de l’accès à \_ \_ l’imprimante limitée est transmise à la structure [**\_ par défaut**](printer-defaults.md) de l’imprimante et que l’utilisateur ne dispose pas de l’autorisation appropriée.</span><span class="sxs-lookup"><span data-stu-id="6065e-159">In this example, **OpenPrinter2** fails when PRINTER\_ACCESS\_MANAGE\_LIMITED is passed to the [**PRINTER\_DEFAULTS**](printer-defaults.md) structure, and the user does not have the appropriate permission.</span></span>


```C++
// Specify the limited management permission.
PRINTER_DEFAULTS defaults = {};
defaults.DesiredAccess = PRINTER_ACCESS_MANAGE_LIMITED;

// Open a printer to which the user has no administrative rights.
HANDLE printer = nullptr;
assert(!OpenPrinter2(L QueueWithNoAdminRights , // Queue name
                     &printer,                  // Printer handle
                     &defaults,                 // Printer defaults
                     nullptr));                 // Printer options

assert(GetLastError() == ERROR_ACCESS_DENIED);

if (printer)
{
    ClosePrinter(printer);
}
```



<span data-ttu-id="6065e-160">Pour obtenir un exemple de programme qui montre comment utiliser cette fonction, consultez [Comment : imprimer à l’aide de l’API d’impression GDI](how-to--print-using-the-gdi-print-api.md).</span><span class="sxs-lookup"><span data-stu-id="6065e-160">For a sample program that shows how to use this function, see [How To: Print Using the GDI Print API](how-to--print-using-the-gdi-print-api.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6065e-161">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6065e-161">Requirements</span></span>



| <span data-ttu-id="6065e-162">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6065e-162">Requirement</span></span> | <span data-ttu-id="6065e-163">Valeur</span><span class="sxs-lookup"><span data-stu-id="6065e-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6065e-164">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6065e-164">Minimum supported client</span></span><br/> | <span data-ttu-id="6065e-165">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6065e-165">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="6065e-166">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6065e-166">Minimum supported server</span></span><br/> | <span data-ttu-id="6065e-167">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6065e-167">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6065e-168">En-tête</span><span class="sxs-lookup"><span data-stu-id="6065e-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="6065e-169"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6065e-169"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="6065e-170">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6065e-170">Library</span></span><br/>                  | <dl> <span data-ttu-id="6065e-171"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6065e-171"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="6065e-172">DLL</span><span class="sxs-lookup"><span data-stu-id="6065e-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6065e-173"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6065e-173"><dt>Spoolss.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="6065e-174">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="6065e-174">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="6065e-175">**OpenPrinter2W** (Unicode) et **OpenPrinter2A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="6065e-175">**OpenPrinter2W** (Unicode) and **OpenPrinter2A** (ANSI)</span></span><br/>                                       |



## <a name="see-also"></a><span data-ttu-id="6065e-176">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6065e-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6065e-177">Impression</span><span class="sxs-lookup"><span data-stu-id="6065e-177">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="6065e-178">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="6065e-178">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="6065e-179">**ClosePrinter**</span><span class="sxs-lookup"><span data-stu-id="6065e-179">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="6065e-180">**\_valeurs par défaut de l’imprimante**</span><span class="sxs-lookup"><span data-stu-id="6065e-180">**PRINTER\_DEFAULTS**</span></span>](printer-defaults.md)
</dt> <dt>

[<span data-ttu-id="6065e-181">**OPTIONS de l’imprimante \_**</span><span class="sxs-lookup"><span data-stu-id="6065e-181">**PRINTER\_OPTIONS**</span></span>](printer-options.md)
</dt> <dt>

[<span data-ttu-id="6065e-182">**SetJob**</span><span class="sxs-lookup"><span data-stu-id="6065e-182">**SetJob**</span></span>](setjob.md)
</dt> <dt>

[<span data-ttu-id="6065e-183">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="6065e-183">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="6065e-184">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="6065e-184">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="6065e-185">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="6065e-185">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

