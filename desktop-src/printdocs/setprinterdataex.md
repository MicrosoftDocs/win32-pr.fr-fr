---
description: La fonction SetPrinterDataEx définit les données de configuration d’une imprimante ou d’un serveur d’impression. La fonction stocke les données de configuration sous la clé de Registre Printers.
ms.assetid: b7faadfc-1c81-4ddf-8fe5-68f4cc0376f1
title: SetPrinterDataEx, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetPrinterDataEx
- SetPrinterDataExA
- SetPrinterDataExW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 9f384c9c9d6f0d956264b45ec8b52043ad20e897
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210087"
---
# <a name="setprinterdataex-function"></a><span data-ttu-id="66676-104">SetPrinterDataEx fonction)</span><span class="sxs-lookup"><span data-stu-id="66676-104">SetPrinterDataEx function</span></span>

<span data-ttu-id="66676-105">La fonction **SetPrinterDataEx** définit les données de configuration d’une imprimante ou d’un serveur d’impression.</span><span class="sxs-lookup"><span data-stu-id="66676-105">The **SetPrinterDataEx** function sets the configuration data for a printer or print server.</span></span> <span data-ttu-id="66676-106">La fonction stocke les données de configuration sous la clé de registre de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="66676-106">The function stores the configuration data under the printer's registry key.</span></span>

## <a name="syntax"></a><span data-ttu-id="66676-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="66676-107">Syntax</span></span>


```C++
DWORD SetPrinterDataEx(
  _In_ HANDLE  hPrinter,
  _In_ LPCTSTR pKeyName,
  _In_ LPCTSTR pValueName,
  _In_ DWORD   Type,
  _In_ LPBYTE  pData,
  _In_ DWORD   cbData
);
```



## <a name="parameters"></a><span data-ttu-id="66676-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="66676-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66676-109">*hPrinter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="66676-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66676-110">Handle vers l’imprimante ou le serveur d’impression pour lequel la fonction définit les données de configuration.</span><span class="sxs-lookup"><span data-stu-id="66676-110">A handle to the printer or print server for which the function sets configuration data.</span></span> <span data-ttu-id="66676-111">Utilisez la fonction [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md)ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="66676-111">Use the [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md), or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="66676-112">*pKeyName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="66676-112">*pKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66676-113">Pointeur vers une chaîne se terminant par un caractère null qui spécifie la clé contenant la valeur à définir.</span><span class="sxs-lookup"><span data-stu-id="66676-113">A pointer to a null-terminated string that specifies the key containing the value to set.</span></span> <span data-ttu-id="66676-114">Si la clé ou les sous-clés spécifiées n’existent pas, la fonction les crée.</span><span class="sxs-lookup"><span data-stu-id="66676-114">If the specified key or subkeys do not exist, the function creates them.</span></span>

<span data-ttu-id="66676-115">Pour stocker les données de configuration qui peuvent être publiées dans le service d’annuaire (DS), spécifiez l’une des clés de Registre prédéfinies suivantes.</span><span class="sxs-lookup"><span data-stu-id="66676-115">To store configuration data that can be published in the directory service (DS), specify one of the following predefined registry keys.</span></span>



| <span data-ttu-id="66676-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="66676-116">Value</span></span>                                                                                                                                                                      | <span data-ttu-id="66676-117">Signification</span><span class="sxs-lookup"><span data-stu-id="66676-117">Meaning</span></span>                                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="SPLDS_DRIVER_KEY"></span><span id="splds_driver_key"></span><dl> <span data-ttu-id="66676-118"><dt>**SPLDS_DRIVER_KEY**</dt></span><span class="sxs-lookup"><span data-stu-id="66676-118"><dt>**SPLDS_DRIVER_KEY**</dt></span></span> </dl>    | <span data-ttu-id="66676-119">Pilotes d’imprimante Utilisez cette clé pour stocker les propriétés du pilote.</span><span class="sxs-lookup"><span data-stu-id="66676-119">Printer drivers use this key to store driver properties.</span></span><br/>                             |
| <span id="SPLDS_SPOOLER_KEY"></span><span id="splds_spooler_key"></span><dl> <span data-ttu-id="66676-120"><dt>**SPLDS_SPOOLER_KEY**</dt></span><span class="sxs-lookup"><span data-stu-id="66676-120"><dt>**SPLDS_SPOOLER_KEY**</dt></span></span> </dl> | <span data-ttu-id="66676-121">Réservé.</span><span class="sxs-lookup"><span data-stu-id="66676-121">Reserved.</span></span> <span data-ttu-id="66676-122">Utilisé uniquement par le spouleur d’impression pour stocker les propriétés internes du spouleur.</span><span class="sxs-lookup"><span data-stu-id="66676-122">Used only by the print spooler to store internal spooler properties.</span></span><br/>       |
| <span id="SPLDS_USER_KEY"></span><span id="splds_user_key"></span><dl> <span data-ttu-id="66676-123"><dt>**SPLDS_USER_KEY**</dt></span><span class="sxs-lookup"><span data-stu-id="66676-123"><dt>**SPLDS_USER_KEY**</dt></span></span> </dl>          | <span data-ttu-id="66676-124">Les applications utilisent cette clé pour stocker des propriétés d’imprimante telles que des numéros de ressources d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="66676-124">Applications use this key to store printer properties such as printer asset numbers.</span></span><br/> |



 

<span data-ttu-id="66676-125">Les valeurs stockées sous la clé de SPLDS_USER_KEY sont publiées dans le service d’annuaire uniquement s’il existe une propriété correspondante dans le schéma.</span><span class="sxs-lookup"><span data-stu-id="66676-125">Values that are stored under the SPLDS_USER_KEY key are published in the directory service only if there is a corresponding property in the schema.</span></span> <span data-ttu-id="66676-126">Un administrateur de domaine doit créer la propriété si elle n’existe pas déjà.</span><span class="sxs-lookup"><span data-stu-id="66676-126">A domain administrator must create the property if it doesn't already exist.</span></span> <span data-ttu-id="66676-127">Pour publier une propriété définie par l’utilisateur après avoir utilisé **SetPrinterDataEx** pour ajouter ou modifier une valeur, appelez [**SetPrinter**](setprinter.md) avec *Level* = 7 et avec le membre **dwAction** de [**PRINTER_INFO_7**](printer-info-7.md) défini sur **DSPRINT_UPDATE**.</span><span class="sxs-lookup"><span data-stu-id="66676-127">To publish a user-defined property after you use **SetPrinterDataEx** to add or change a value, call [**SetPrinter**](setprinter.md) with *Level* = 7 and with the **dwAction** member of [**PRINTER_INFO_7**](printer-info-7.md) set to **DSPRINT_UPDATE**.</span></span>

<span data-ttu-id="66676-128">Vous pouvez spécifier d’autres clés pour stocker des données de configuration non-DS.</span><span class="sxs-lookup"><span data-stu-id="66676-128">You can specify other keys to store non-DS configuration data.</span></span> <span data-ttu-id="66676-129">Utilisez la barre oblique inverse ( \\ ) comme séparateur pour spécifier un chemin d’accès qui a une ou plusieurs sous-clés.</span><span class="sxs-lookup"><span data-stu-id="66676-129">Use the backslash ( \\ ) character as a delimiter to specify a path that has one or more subkeys.</span></span>

<span data-ttu-id="66676-130">Si *hPrinter* est un handle d’imprimante et que *PKeyName* a la **valeur null** ou est une chaîne vide, **SetPrinterDataEx** retourne **ERROR_INVALID_PARAMETER**.</span><span class="sxs-lookup"><span data-stu-id="66676-130">If *hPrinter* is a handle to a printer and *pKeyName* is **NULL** or an empty string, **SetPrinterDataEx** returns **ERROR_INVALID_PARAMETER**.</span></span>

<span data-ttu-id="66676-131">Si *hPrinter* est un handle vers un serveur d’impression, *pKeyName* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="66676-131">If *hPrinter* is a handle to a print server, *pKeyName* is ignored.</span></span>

<span data-ttu-id="66676-132">N’utilisez pas **SPLDS_SPOOLER_KEY**.</span><span class="sxs-lookup"><span data-stu-id="66676-132">Do not use **SPLDS_SPOOLER_KEY**.</span></span> <span data-ttu-id="66676-133">Pour modifier les propriétés de l’imprimante du spouleur, utilisez [**SetPrinter**](setprinter.md) avec *Level* = 2.</span><span class="sxs-lookup"><span data-stu-id="66676-133">To change the spooler printer properties, use [**SetPrinter**](setprinter.md) with *Level* = 2.</span></span>

</dd> <dt>

<span data-ttu-id="66676-134">*pValueName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="66676-134">*pValueName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66676-135">Pointeur vers une chaîne terminée par le caractère null qui identifie les données à définir.</span><span class="sxs-lookup"><span data-stu-id="66676-135">A pointer to a null-terminated string that identifies the data to set.</span></span>

<span data-ttu-id="66676-136">Pour les imprimantes, cette chaîne spécifie le nom d’une valeur sous la clé *pKeyName* .</span><span class="sxs-lookup"><span data-stu-id="66676-136">For printers, this string specifies the name of a value under the *pKeyName* key.</span></span>

<span data-ttu-id="66676-137">Pour les serveurs d’impression, cette chaîne est l’une des chaînes prédéfinies énumérées dans la section Notes suivante.</span><span class="sxs-lookup"><span data-stu-id="66676-137">For print servers, this string is one of the predefined strings listed in the following Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="66676-138">*Type* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="66676-138">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66676-139">Code indiquant le type de données vers lequel pointe le paramètre *pData* .</span><span class="sxs-lookup"><span data-stu-id="66676-139">A code indicating the type of data pointed to by the *pData* parameter.</span></span> <span data-ttu-id="66676-140">Pour obtenir la liste des codes de type possibles, consultez [types de valeurs de Registre](/windows/desktop/SysInfo/registry-value-types).</span><span class="sxs-lookup"><span data-stu-id="66676-140">For a list of the possible type codes, see [Registry Value Types](/windows/desktop/SysInfo/registry-value-types).</span></span>

<span data-ttu-id="66676-141">Si *pKeyName* spécifie l’une des clés de service d’annuaire prédéfinies, le *Type* doit être **REG_SZ**, **REG_MULTI_SZ**, **REG_DWORD** ou **REG_BINARY**.</span><span class="sxs-lookup"><span data-stu-id="66676-141">If *pKeyName* specifies one of the predefined directory service keys, *Type* must be **REG_SZ**, **REG_MULTI_SZ**, **REG_DWORD**, or **REG_BINARY**.</span></span> <span data-ttu-id="66676-142">Si **REG_BINARY** est utilisé, *cbData* doit être égal à 1 et le service d’annuaire traite les données comme une valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="66676-142">If **REG_BINARY** is used, *cbData* must be equal to 1, and the directory service treats the data as a Boolean value.</span></span>

</dd> <dt>

<span data-ttu-id="66676-143">*pData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="66676-143">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66676-144">Pointeur vers une mémoire tampon qui contient les données de configuration de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="66676-144">A pointer to a buffer that contains the printer configuration data.</span></span>

</dd> <dt>

<span data-ttu-id="66676-145">*cbData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="66676-145">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66676-146">Taille, en octets, du tableau.</span><span class="sxs-lookup"><span data-stu-id="66676-146">The size, in bytes, of the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66676-147">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="66676-147">Return value</span></span>

<span data-ttu-id="66676-148">Si la fonction est réussie, la valeur de retour est **ERROR_SUCCESS**.</span><span class="sxs-lookup"><span data-stu-id="66676-148">If the function succeeds, the return value is **ERROR_SUCCESS**.</span></span>

<span data-ttu-id="66676-149">Si la fonction échoue, la valeur de retour est une valeur d’erreur.</span><span class="sxs-lookup"><span data-stu-id="66676-149">If the function fails, the return value is an error value.</span></span>

## <a name="remarks"></a><span data-ttu-id="66676-150">Notes</span><span class="sxs-lookup"><span data-stu-id="66676-150">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="66676-151">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="66676-151">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="66676-152">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="66676-152">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="66676-153">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="66676-153">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="66676-154">Pour récupérer les données de configuration existantes d’une imprimante ou d’un spouleur d’impression, appelez la fonction [**GetPrinterDataEx**](getprinterdataex.md) .</span><span class="sxs-lookup"><span data-stu-id="66676-154">To retrieve existing configuration data for a printer or print spooler, call the [**GetPrinterDataEx**](getprinterdataex.md) function.</span></span>

<span data-ttu-id="66676-155">L’appel de **SetPrinterDataEx** avec le paramètre *pKeyName* défini sur « PrinterDriverData » équivaut à appeler la fonction [**SetPrinterData**](setprinterdata.md) .</span><span class="sxs-lookup"><span data-stu-id="66676-155">Calling **SetPrinterDataEx** with the *pKeyName* parameter set to "PrinterDriverData" is equivalent to calling the [**SetPrinterData**](setprinterdata.md) function.</span></span>

<span data-ttu-id="66676-156">Si *hPrinter* est un handle vers un serveur d’impression, *pValueName* peut spécifier l’une des valeurs prédéfinies suivantes.</span><span class="sxs-lookup"><span data-stu-id="66676-156">If *hPrinter* is a handle to a print server, *pValueName* can specify one of the following predefined values.</span></span>



| <span data-ttu-id="66676-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="66676-157">Value</span></span>                                                               | <span data-ttu-id="66676-158">Commentaires</span><span class="sxs-lookup"><span data-stu-id="66676-158">Comments</span></span>                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66676-159">**SPLREG_ALLOW_USER_MANAGEFORMS**</span><span class="sxs-lookup"><span data-stu-id="66676-159">**SPLREG_ALLOW_USER_MANAGEFORMS**</span></span>                                | <span data-ttu-id="66676-160">Windows XP avec Service Pack 2 (SP2) et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="66676-160">Windows XP with Service Pack 2 (SP2) and later</span></span><br/> <span data-ttu-id="66676-161">Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="66676-161">Windows Server 2003 with Service Pack 1 (SP1) and later</span></span><br/>                                                                                                    |
| <span data-ttu-id="66676-162">**SPLREG_BEEP_ENABLED**</span><span class="sxs-lookup"><span data-stu-id="66676-162">**SPLREG_BEEP_ENABLED**</span></span>                                           |                                                                                                                                                                                                                                 |
| <span data-ttu-id="66676-163">**SPLREG_DEFAULT_SPOOL_DIRECTORY**</span><span class="sxs-lookup"><span data-stu-id="66676-163">**SPLREG_DEFAULT_SPOOL_DIRECTORY**</span></span>                               |                                                                                                                                                                                                                                 |
| <span data-ttu-id="66676-164">**SPLREG_EVENT_LOG**</span><span class="sxs-lookup"><span data-stu-id="66676-164">**SPLREG_EVENT_LOG**</span></span>                                              |                                                                                                                                                                                                                                 |
| <span data-ttu-id="66676-165">**SPLREG_NET_POPUP**</span><span class="sxs-lookup"><span data-stu-id="66676-165">**SPLREG_NET_POPUP**</span></span>                                              | <span data-ttu-id="66676-166">Non pris en charge dans Windows Server 2003 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="66676-166">Not supported in Windows Server 2003 and later</span></span><br/>                                                                                                                                                                       |
| <span data-ttu-id="66676-167">**SPLREG_PORT_THREAD_PRIORITY_DEFAULT**</span><span class="sxs-lookup"><span data-stu-id="66676-167">**SPLREG_PORT_THREAD_PRIORITY_DEFAULT**</span></span>                         |                                                                                                                                                                                                                                 |
| <span data-ttu-id="66676-168">**SPLREG_PORT_THREAD_PRIORITY**</span><span class="sxs-lookup"><span data-stu-id="66676-168">**SPLREG_PORT_THREAD_PRIORITY**</span></span>                                  |                                                                                                                                                                                                                                 |
| <span data-ttu-id="66676-169">**SPLREG_PRINT_DRIVER_ISOLATION_GROUPS**</span><span class="sxs-lookup"><span data-stu-id="66676-169">**SPLREG_PRINT_DRIVER_ISOLATION_GROUPS**</span></span>                        | <span data-ttu-id="66676-170">Windows 7 et ultérieur</span><span class="sxs-lookup"><span data-stu-id="66676-170">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="66676-171">**SPLREG_PRINT_DRIVER_ISOLATION_TIME_BEFORE_RECYCLE**</span><span class="sxs-lookup"><span data-stu-id="66676-171">**SPLREG_PRINT_DRIVER_ISOLATION_TIME_BEFORE_RECYCLE**</span></span>         | <span data-ttu-id="66676-172">Windows 7 et ultérieur</span><span class="sxs-lookup"><span data-stu-id="66676-172">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="66676-173">**SPLREG_PRINT_DRIVER_ISOLATION_MAX_OBJECTS_BEFORE_RECYCLE**</span><span class="sxs-lookup"><span data-stu-id="66676-173">**SPLREG_PRINT_DRIVER_ISOLATION_MAX_OBJECTS_BEFORE_RECYCLE**</span></span> | <span data-ttu-id="66676-174">Windows 7 et ultérieur</span><span class="sxs-lookup"><span data-stu-id="66676-174">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="66676-175">**SPLREG_PRINT_DRIVER_ISOLATION_IDLE_TIMEOUT**</span><span class="sxs-lookup"><span data-stu-id="66676-175">**SPLREG_PRINT_DRIVER_ISOLATION_IDLE_TIMEOUT**</span></span>                 | <span data-ttu-id="66676-176">Windows 7 et ultérieur</span><span class="sxs-lookup"><span data-stu-id="66676-176">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="66676-177">**SPLREG_PRINT_DRIVER_ISOLATION_EXECUTION_POLICY**</span><span class="sxs-lookup"><span data-stu-id="66676-177">**SPLREG_PRINT_DRIVER_ISOLATION_EXECUTION_POLICY**</span></span>             | <span data-ttu-id="66676-178">Windows 7 et ultérieur</span><span class="sxs-lookup"><span data-stu-id="66676-178">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="66676-179">**SPLREG_PRINT_DRIVER_ISOLATION_OVERRIDE_POLICY**</span><span class="sxs-lookup"><span data-stu-id="66676-179">**SPLREG_PRINT_DRIVER_ISOLATION_OVERRIDE_POLICY**</span></span>              | <span data-ttu-id="66676-180">Windows 7 et ultérieur</span><span class="sxs-lookup"><span data-stu-id="66676-180">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="66676-181">**SPLREG_RETRY_POPUP**</span><span class="sxs-lookup"><span data-stu-id="66676-181">**SPLREG_RETRY_POPUP**</span></span>                                            | <span data-ttu-id="66676-182">En cas de retour réussi, *pData* contient 1 si le serveur est configuré pour réessayer les fenêtres contextuelles pour tous les travaux, ou 0 si le serveur ne réessaye pas les fenêtres publicitaires pour tous les travaux.</span><span class="sxs-lookup"><span data-stu-id="66676-182">On successful return, *pData* contains 1 if server is set to retry pop-up windows for all jobs, or 0 if server does not retry pop-up windows for all jobs.</span></span><br/> <span data-ttu-id="66676-183">Non pris en charge dans Windows Server 2003 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="66676-183">Not supported in Windows Server 2003 and later</span></span><br/> |
| <span data-ttu-id="66676-184">**SPLREG_SCHEDULER_THREAD_PRIORITY**</span><span class="sxs-lookup"><span data-stu-id="66676-184">**SPLREG_SCHEDULER_THREAD_PRIORITY**</span></span>                             |                                                                                                                                                                                                                                 |
| <span data-ttu-id="66676-185">**SPLREG_SCHEDULER_THREAD_PRIORITY_DEFAULT**</span><span class="sxs-lookup"><span data-stu-id="66676-185">**SPLREG_SCHEDULER_THREAD_PRIORITY_DEFAULT**</span></span>                    |                                                                                                                                                                                                                                 |
| <span data-ttu-id="66676-186">**SPLREG_WEBSHAREMGMT**</span><span class="sxs-lookup"><span data-stu-id="66676-186">**SPLREG_WEBSHAREMGMT**</span></span>                                            | <span data-ttu-id="66676-187">Windows Server 2003 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="66676-187">Windows Server 2003 and later</span></span><br/>                                                                                                                                                                                        |



 

<span data-ttu-id="66676-188">Le passage de l’une des valeurs prédéfinies suivantes comme *pValueName* définit le comportement d’impression du pool lorsqu’une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="66676-188">Passing one of the following predefined values as *pValueName* sets the pool printing behavior when an error occurs.</span></span>



| <span data-ttu-id="66676-189">Valeur</span><span class="sxs-lookup"><span data-stu-id="66676-189">Value</span></span>                                       | <span data-ttu-id="66676-190">Commentaires</span><span class="sxs-lookup"><span data-stu-id="66676-190">Comments</span></span>                                                                                                                                                                                              |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66676-191">**SPLREG_RESTART_JOB_ON_POOL_ERROR**</span><span class="sxs-lookup"><span data-stu-id="66676-191">**SPLREG_RESTART_JOB_ON_POOL_ERROR**</span></span>   | <span data-ttu-id="66676-192">La valeur de *pData* indique la durée, en secondes, à laquelle un travail est redémarré sur un autre port après qu’une erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="66676-192">The value of *pData* indicates the time, in seconds, when a job is restarted on another port after an error occurs.</span></span> <span data-ttu-id="66676-193">Ce paramètre est utilisé avec **SPLREG_RESTART_JOB_ON_POOL_ENABLED**.</span><span class="sxs-lookup"><span data-stu-id="66676-193">This setting is used with **SPLREG_RESTART_JOB_ON_POOL_ENABLED**.</span></span><br/> |
| <span data-ttu-id="66676-194">**SPLREG_RESTART_JOB_ON_POOL_ENABLED**</span><span class="sxs-lookup"><span data-stu-id="66676-194">**SPLREG_RESTART_JOB_ON_POOL_ENABLED**</span></span> | <span data-ttu-id="66676-195">Une valeur différente de zéro dans *pData* indique que **SPLREG_RESTART_JOB_ON_POOL_ERROR** est activé.</span><span class="sxs-lookup"><span data-stu-id="66676-195">A nonzero value in *pData* indicates that **SPLREG_RESTART_JOB_ON_POOL_ERROR** is enabled.</span></span><br/>                                                                                            |



 

<span data-ttu-id="66676-196">L’heure spécifiée dans **SPLREG_RESTART_JOB_ON_POOL_ERROR** est une durée minimale.</span><span class="sxs-lookup"><span data-stu-id="66676-196">The time specified in **SPLREG_RESTART_JOB_ON_POOL_ERROR** is a minimum time.</span></span> <span data-ttu-id="66676-197">L’heure réelle peut être plus longue, en fonction des paramètres de moniteur de port suivants, qui sont des valeurs de Registre sous cette clé de Registre :</span><span class="sxs-lookup"><span data-stu-id="66676-197">The actual time can be longer, depending on the following port monitor settings, which are registry values under this registry key:</span></span>

<span data-ttu-id="66676-198">**HKLM \\ System \\ CurrentControlSet \\ Control \\ moniteurs d’impression \\ \\ <  > \\ ports nomdumoniteur**</span><span class="sxs-lookup"><span data-stu-id="66676-198">**HKLM\\SYSTEM\\CurrentControlSet\\Control\\Print\\Monitors\\<*MonitorName*>\\Ports**</span></span>

<span data-ttu-id="66676-199">Appelez la fonction [**RegSetValueEx**](/windows/win32/api/winreg/nf-winreg-regsetvaluea) pour définir ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="66676-199">Call the [**RegSetValueEx**](/windows/win32/api/winreg/nf-winreg-regsetvaluea) function to set these values.</span></span>



| <span data-ttu-id="66676-200">Paramètre du moniteur de port</span><span class="sxs-lookup"><span data-stu-id="66676-200">Port monitor setting</span></span>     | <span data-ttu-id="66676-201">Type de données</span><span class="sxs-lookup"><span data-stu-id="66676-201">Data type</span></span>      | <span data-ttu-id="66676-202">Signification</span><span class="sxs-lookup"><span data-stu-id="66676-202">Meaning</span></span>                                                                                                        |
|--------------------------|----------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66676-203">**StatusUpdateEnabled**</span><span class="sxs-lookup"><span data-stu-id="66676-203">**StatusUpdateEnabled**</span></span>  | <span data-ttu-id="66676-204">**REG_DWORD**</span><span class="sxs-lookup"><span data-stu-id="66676-204">**REG_DWORD**</span></span> | <span data-ttu-id="66676-205">Si la valeur est différente de zéro, active le moniteur de port pour mettre à jour le spouleur avec l’état du port.</span><span class="sxs-lookup"><span data-stu-id="66676-205">If a nonzero value, enables the port monitor to update the spooler with the port status.</span></span><br/>            |
| <span data-ttu-id="66676-206">**StatusUpdateInterval**</span><span class="sxs-lookup"><span data-stu-id="66676-206">**StatusUpdateInterval**</span></span> | <span data-ttu-id="66676-207">**REG_DWORD**</span><span class="sxs-lookup"><span data-stu-id="66676-207">**REG_DWORD**</span></span> | <span data-ttu-id="66676-208">Spécifie l’intervalle, en minutes, au cours duquel le moniteur de port met à jour le spouleur avec l’état du port.</span><span class="sxs-lookup"><span data-stu-id="66676-208">Specifies the interval, in minutes, when the port monitor updates the spooler with the port status.</span></span><br/> |



 

<span data-ttu-id="66676-209">Pour vous assurer que le spouleur redirige les travaux vers la prochaine imprimante disponible dans le pool (lorsque le travail d’impression n’est pas imprimé dans le délai défini), le moniteur de port doit prendre en charge SNMP et les ports réseau du pool doivent être configurés comme « État SNMP activé ».</span><span class="sxs-lookup"><span data-stu-id="66676-209">To ensure that the spooler redirects jobs to the next available printer in the pool (when the print job is not printed within the set time), the port monitor must support SNMP and the network ports in the pool must be configured as "SNMP status enabled."</span></span> <span data-ttu-id="66676-210">Le moniteur de port qui prend en charge SNMP est le moniteur de port TCP/IP standard.</span><span class="sxs-lookup"><span data-stu-id="66676-210">The port monitor that supports SNMP is Standard TCP/IP port monitor.</span></span>

<span data-ttu-id="66676-211">Dans Windows 7 et les versions ultérieures de Windows, les travaux d’impression qui sont envoyés à un serveur d’impression sont rendus sur le client par défaut.</span><span class="sxs-lookup"><span data-stu-id="66676-211">In Windows 7 and later versions of Windows, print jobs that are sent to a print server are rendered on the client by default.</span></span> <span data-ttu-id="66676-212">Le rendu côté client des travaux d’impression peut être configuré en définissant *pKeyName* sur « PrinterDriverData » et *pValueName* sur la valeur de paramètre dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="66676-212">Client-side rendering of print jobs can be configured by setting *pKeyName* to "PrinterDriverData" and *pValueName* to the setting value in the following table.</span></span>



| <span data-ttu-id="66676-213">Paramètre</span><span class="sxs-lookup"><span data-stu-id="66676-213">Setting</span></span>                      | <span data-ttu-id="66676-214">Type de données</span><span class="sxs-lookup"><span data-stu-id="66676-214">Data type</span></span>      | <span data-ttu-id="66676-215">Description</span><span class="sxs-lookup"><span data-stu-id="66676-215">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66676-216">**EMFDespoolingSetting**</span><span class="sxs-lookup"><span data-stu-id="66676-216">**EMFDespoolingSetting**</span></span>     | <span data-ttu-id="66676-217">**REG_DWORD**</span><span class="sxs-lookup"><span data-stu-id="66676-217">**REG_DWORD**</span></span> | <span data-ttu-id="66676-218">La valeur 0, ou si cette valeur n’est pas présente dans le registre, active le rendu par défaut côté client des travaux d’impression.</span><span class="sxs-lookup"><span data-stu-id="66676-218">A value of 0, or if this value is not present in the registry, enables the default client-side rendering of print jobs.</span></span><br/> <span data-ttu-id="66676-219">La valeur 1 désactive le rendu côté client des travaux d’impression.</span><span class="sxs-lookup"><span data-stu-id="66676-219">A value of 1 disables client-side rendering of print jobs.</span></span><br/>                                                                                                                                                                                                          |
| <span data-ttu-id="66676-220">**ForceClientSideRendering**</span><span class="sxs-lookup"><span data-stu-id="66676-220">**ForceClientSideRendering**</span></span> | <span data-ttu-id="66676-221">**REG_DWORD**</span><span class="sxs-lookup"><span data-stu-id="66676-221">**REG_DWORD**</span></span> | <span data-ttu-id="66676-222">La valeur 0, ou si cette valeur n’est pas présente dans le registre, entraîne le rendu des travaux d’impression sur le client.</span><span class="sxs-lookup"><span data-stu-id="66676-222">A value of 0, or if this value is not present in the registry, will cause the print jobs to be rendered on the client.</span></span> <span data-ttu-id="66676-223">Si un travail d’impression ne peut pas être rendu sur le client, il sera rendu sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="66676-223">If a print job cannot be rendered on the client, it will be rendered on the server.</span></span> <span data-ttu-id="66676-224">Si un travail d’impression ne peut pas être rendu sur le serveur, il échoue.</span><span class="sxs-lookup"><span data-stu-id="66676-224">If a print job cannot be rendered on the server, it will fail.</span></span><br/> <span data-ttu-id="66676-225">La valeur 1 affiche les travaux d’impression sur le client.</span><span class="sxs-lookup"><span data-stu-id="66676-225">A value of 1 will render print jobs on the client.</span></span> <span data-ttu-id="66676-226">Si un travail d’impression ne peut pas être rendu sur le client, l’opération échoue.</span><span class="sxs-lookup"><span data-stu-id="66676-226">If a print job cannot be rendered on the client, it will fail.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="66676-227">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="66676-227">Requirements</span></span>



| <span data-ttu-id="66676-228">Condition requise</span><span class="sxs-lookup"><span data-stu-id="66676-228">Requirement</span></span> | <span data-ttu-id="66676-229">Valeur</span><span class="sxs-lookup"><span data-stu-id="66676-229">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66676-230">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66676-230">Minimum supported client</span></span><br/> | <span data-ttu-id="66676-231">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="66676-231">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="66676-232">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66676-232">Minimum supported server</span></span><br/> | <span data-ttu-id="66676-233">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="66676-233">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="66676-234">En-tête</span><span class="sxs-lookup"><span data-stu-id="66676-234">Header</span></span><br/>                   | <dl> <span data-ttu-id="66676-235"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="66676-235"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="66676-236">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="66676-236">Library</span></span><br/>                  | <dl> <span data-ttu-id="66676-237"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="66676-237"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="66676-238">DLL</span><span class="sxs-lookup"><span data-stu-id="66676-238">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66676-239"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="66676-239"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="66676-240">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="66676-240">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="66676-241">**SetPrinterDataExW** (Unicode) et **SetPrinterDataExA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="66676-241">**SetPrinterDataExW** (Unicode) and **SetPrinterDataExA** (ANSI)</span></span><br/>                               |



## <a name="see-also"></a><span data-ttu-id="66676-242">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="66676-242">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66676-243">Impression</span><span class="sxs-lookup"><span data-stu-id="66676-243">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="66676-244">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="66676-244">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="66676-245">**GetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="66676-245">**GetPrinterDataEx**</span></span>](getprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="66676-246">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="66676-246">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="66676-247">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="66676-247">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="66676-248">**PRINTER_INFO_7**</span><span class="sxs-lookup"><span data-stu-id="66676-248">**PRINTER_INFO_7**</span></span>](printer-info-7.md)
</dt> </dl>

 

