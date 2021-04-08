---
description: La fonction SetPrinterData définit les données de configuration d’une imprimante ou d’un serveur d’impression.
ms.assetid: 16072de9-98fb-4ada-8216-180b64cf44c8
title: SetPrinterData, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetPrinterData
- SetPrinterDataA
- SetPrinterDataW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 36af84fe665d68fd7996a0b81fbbf291314cc69e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864750"
---
# <a name="setprinterdata-function"></a><span data-ttu-id="46ef1-103">SetPrinterData fonction)</span><span class="sxs-lookup"><span data-stu-id="46ef1-103">SetPrinterData function</span></span>

<span data-ttu-id="46ef1-104">La fonction **SetPrinterData** définit les données de configuration d’une imprimante ou d’un serveur d’impression.</span><span class="sxs-lookup"><span data-stu-id="46ef1-104">The **SetPrinterData** function sets the configuration data for a printer or print server.</span></span>

<span data-ttu-id="46ef1-105">Pour spécifier la clé de Registre dans laquelle stocker les données, appelez la fonction [**SetPrinterDataEx**](setprinterdataex.md) .</span><span class="sxs-lookup"><span data-stu-id="46ef1-105">To specify the registry key under which to store the data, call the [**SetPrinterDataEx**](setprinterdataex.md) function.</span></span> <span data-ttu-id="46ef1-106">L’appel de **SetPrinterData** équivaut à appeler la fonction **SetPrinterDataEx** avec le paramètre *pKeyName* défini sur « PrinterDriverData ».</span><span class="sxs-lookup"><span data-stu-id="46ef1-106">Calling **SetPrinterData** is equivalent to calling the **SetPrinterDataEx** function with the *pKeyName* parameter set to "PrinterDriverData".</span></span>

## <a name="syntax"></a><span data-ttu-id="46ef1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="46ef1-107">Syntax</span></span>


```C++
DWORD SetPrinterData(
  _In_ HANDLE hPrinter,
  _In_ LPTSTR pValueName,
  _In_ DWORD  Type,
  _In_ LPBYTE pData,
  _In_ DWORD  cbData
);
```



## <a name="parameters"></a><span data-ttu-id="46ef1-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="46ef1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46ef1-109">*hPrinter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="46ef1-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46ef1-110">Handle vers l’imprimante ou le serveur d’impression pour lequel la fonction définit les données de configuration.</span><span class="sxs-lookup"><span data-stu-id="46ef1-110">A handle to the printer or print server for which the function sets configuration data.</span></span> <span data-ttu-id="46ef1-111">Utilisez la fonction [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md)ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="46ef1-111">Use the [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md), or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="46ef1-112">*pValueName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="46ef1-112">*pValueName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46ef1-113">Pointeur vers une chaîne terminée par le caractère null qui identifie les données à définir.</span><span class="sxs-lookup"><span data-stu-id="46ef1-113">A pointer to a null-terminated string that identifies the data to set.</span></span>

<span data-ttu-id="46ef1-114">Pour les imprimantes, cette chaîne correspond au nom d’une valeur de Registre sous la clé « PrinterDriverData » de l’imprimante dans le registre.</span><span class="sxs-lookup"><span data-stu-id="46ef1-114">For printers, this string is the name of a registry value under the printer's "PrinterDriverData" key in the registry.</span></span>

<span data-ttu-id="46ef1-115">Pour les serveurs d’impression, cette chaîne est l’une des chaînes prédéfinies énumérées dans la section Notes suivante.</span><span class="sxs-lookup"><span data-stu-id="46ef1-115">For print servers, this string is one of the predefined strings listed in the following Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="46ef1-116">*Type* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="46ef1-116">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46ef1-117">Code qui indique le type de données vers lequel pointe le paramètre *pData* .</span><span class="sxs-lookup"><span data-stu-id="46ef1-117">A code that indicates the type of data that the *pData* parameter points to.</span></span> <span data-ttu-id="46ef1-118">Pour obtenir la liste des codes de type possibles, consultez [types de valeurs de Registre](/windows/desktop/SysInfo/registry-value-types).</span><span class="sxs-lookup"><span data-stu-id="46ef1-118">For a list of the possible type codes, see [Registry Value Types](/windows/desktop/SysInfo/registry-value-types).</span></span>

</dd> <dt>

<span data-ttu-id="46ef1-119">*pData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="46ef1-119">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46ef1-120">Pointeur vers un tableau d’octets qui contient les données de configuration de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="46ef1-120">A pointer to an array of bytes that contains the printer configuration data.</span></span>

</dd> <dt>

<span data-ttu-id="46ef1-121">*cbData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="46ef1-121">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46ef1-122">Taille, en octets, du tableau.</span><span class="sxs-lookup"><span data-stu-id="46ef1-122">The size, in bytes, of the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46ef1-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="46ef1-123">Return value</span></span>

<span data-ttu-id="46ef1-124">Si la fonction réussit, la valeur de retour est une **erreur de \_ réussite**.</span><span class="sxs-lookup"><span data-stu-id="46ef1-124">If the function succeeds, the return value is **ERROR\_SUCCESS**.</span></span>

<span data-ttu-id="46ef1-125">Si la fonction échoue, la valeur de retour est une valeur d’erreur.</span><span class="sxs-lookup"><span data-stu-id="46ef1-125">If the function fails, the return value is an error value.</span></span>

## <a name="remarks"></a><span data-ttu-id="46ef1-126">Notes</span><span class="sxs-lookup"><span data-stu-id="46ef1-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="46ef1-127">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="46ef1-127">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="46ef1-128">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="46ef1-128">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="46ef1-129">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="46ef1-129">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="46ef1-130">Pour récupérer les données de configuration existantes d’une imprimante, appelez la fonction [**GetPrinterDataEx**](getprinterdataex.md) ou [**GetPrinterData**](getprinterdata.md) .</span><span class="sxs-lookup"><span data-stu-id="46ef1-130">To retrieve existing configuration data for a printer, call the [**GetPrinterDataEx**](getprinterdataex.md) or [**GetPrinterData**](getprinterdata.md) function.</span></span>

<span data-ttu-id="46ef1-131">Si *hPrinter* est un handle vers un serveur d’impression, *pValueName* peut spécifier l’une des valeurs prédéfinies suivantes.</span><span class="sxs-lookup"><span data-stu-id="46ef1-131">If *hPrinter* is a handle to a print server, *pValueName* can specify one of the following predefined values.</span></span>



| <span data-ttu-id="46ef1-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="46ef1-132">Value</span></span>                                                               | <span data-ttu-id="46ef1-133">Commentaires</span><span class="sxs-lookup"><span data-stu-id="46ef1-133">Comments</span></span>                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46ef1-134">**SPLREG \_ autoriser l' \_ utilisateur \_ MANAGEFORMS**</span><span class="sxs-lookup"><span data-stu-id="46ef1-134">**SPLREG\_ALLOW\_USER\_MANAGEFORMS**</span></span>                                | <span data-ttu-id="46ef1-135">Windows XP avec Service Pack 2 (SP2) et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="46ef1-135">Windows XP with Service Pack 2 (SP2) and later</span></span><br/> <span data-ttu-id="46ef1-136">Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="46ef1-136">Windows Server 2003 with Service Pack 1 (SP1) and later</span></span><br/>                                                                                                    |
| <span data-ttu-id="46ef1-137">**\_signal sonore SPLREG \_ activé**</span><span class="sxs-lookup"><span data-stu-id="46ef1-137">**SPLREG\_BEEP\_ENABLED**</span></span>                                           |                                                                                                                                                                                                                                 |
| <span data-ttu-id="46ef1-138">**SPLREG \_ \_ Répertoire de spoule par défaut \_**</span><span class="sxs-lookup"><span data-stu-id="46ef1-138">**SPLREG\_DEFAULT\_SPOOL\_DIRECTORY**</span></span>                               |                                                                                                                                                                                                                                 |
| <span data-ttu-id="46ef1-139">**\_Journal des événements SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="46ef1-139">**SPLREG\_EVENT\_LOG**</span></span>                                              |                                                                                                                                                                                                                                 |
| <span data-ttu-id="46ef1-140">**\_fenêtre SPLREG NET \_**</span><span class="sxs-lookup"><span data-stu-id="46ef1-140">**SPLREG\_NET\_POPUP**</span></span>                                              | <span data-ttu-id="46ef1-141">Non pris en charge dans Windows Server 2003 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="46ef1-141">Not supported in Windows Server 2003 and later</span></span><br/>                                                                                                                                                                       |
| <span data-ttu-id="46ef1-142">**\_ \_ \_ \_ valeur par défaut de la priorité du thread du port SPLREG**</span><span class="sxs-lookup"><span data-stu-id="46ef1-142">**SPLREG\_PORT\_THREAD\_PRIORITY\_DEFAULT**</span></span>                         |                                                                                                                                                                                                                                 |
| <span data-ttu-id="46ef1-143">**\_priorité de \_ thread de port SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="46ef1-143">**SPLREG\_PORT\_THREAD\_PRIORITY**</span></span>                                  |                                                                                                                                                                                                                                 |
| <span data-ttu-id="46ef1-144">**\_ \_ \_ groupes d’isolation du pilote d’impression SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="46ef1-144">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_GROUPS**</span></span>                        | <span data-ttu-id="46ef1-145">Windows 7 et ultérieur</span><span class="sxs-lookup"><span data-stu-id="46ef1-145">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="46ef1-146">**\_ \_ \_ temps d’isolement du pilote d’impression SPLREG \_ avant le \_ \_ recyclage**</span><span class="sxs-lookup"><span data-stu-id="46ef1-146">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_TIME\_BEFORE\_RECYCLE**</span></span>         | <span data-ttu-id="46ef1-147">Windows 7 et ultérieur</span><span class="sxs-lookup"><span data-stu-id="46ef1-147">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="46ef1-148">**\_isolement du \_ pilote d’impression SPLREG \_ \_ nombre maximal d' \_ objets \_ avant le \_ recyclage**</span><span class="sxs-lookup"><span data-stu-id="46ef1-148">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_MAX\_OBJECTS\_BEFORE\_RECYCLE**</span></span> | <span data-ttu-id="46ef1-149">Windows 7 et ultérieur</span><span class="sxs-lookup"><span data-stu-id="46ef1-149">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="46ef1-150">**\_ \_ \_ \_ délai d’inactivité d’isolation du pilote d’impression \_ SPLREG**</span><span class="sxs-lookup"><span data-stu-id="46ef1-150">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_IDLE\_TIMEOUT**</span></span>                 | <span data-ttu-id="46ef1-151">Windows 7 et ultérieur</span><span class="sxs-lookup"><span data-stu-id="46ef1-151">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="46ef1-152">**\_ \_ \_ stratégie d’exécution de \_ l' \_ isolation du pilote d’impression SPLREG**</span><span class="sxs-lookup"><span data-stu-id="46ef1-152">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_EXECUTION\_POLICY**</span></span>             | <span data-ttu-id="46ef1-153">Windows 7 et ultérieur</span><span class="sxs-lookup"><span data-stu-id="46ef1-153">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="46ef1-154">**\_stratégie de \_ \_ remplacement d’isolation du pilote d’impression \_ SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="46ef1-154">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_OVERRIDE\_POLICY**</span></span>              | <span data-ttu-id="46ef1-155">Windows 7 et ultérieur</span><span class="sxs-lookup"><span data-stu-id="46ef1-155">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="46ef1-156">**\_ \_ fenêtre contextuelle SPLREG Retry**</span><span class="sxs-lookup"><span data-stu-id="46ef1-156">**SPLREG\_RETRY\_POPUP**</span></span>                                            | <span data-ttu-id="46ef1-157">En cas de retour réussi, *pData* contient 1 si le serveur est configuré pour réessayer les fenêtres contextuelles pour tous les travaux, ou 0 si le serveur ne réessaye pas les fenêtres publicitaires pour tous les travaux.</span><span class="sxs-lookup"><span data-stu-id="46ef1-157">On successful return, *pData* contains 1 if server is set to retry pop-up windows for all jobs, or 0 if server does not retry pop-up windows for all jobs.</span></span><br/> <span data-ttu-id="46ef1-158">Non pris en charge dans Windows Server 2003 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="46ef1-158">Not supported in Windows Server 2003 and later</span></span><br/> |
| <span data-ttu-id="46ef1-159">**\_ \_ priorité de threads du planificateur SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="46ef1-159">**SPLREG\_SCHEDULER\_THREAD\_PRIORITY**</span></span>                             |                                                                                                                                                                                                                                 |
| <span data-ttu-id="46ef1-160">**\_priorité de thread du planificateur SPLREG \_ \_ \_ par défaut**</span><span class="sxs-lookup"><span data-stu-id="46ef1-160">**SPLREG\_SCHEDULER\_THREAD\_PRIORITY\_DEFAULT**</span></span>                    |                                                                                                                                                                                                                                 |
| <span data-ttu-id="46ef1-161">**SPLREG \_ WEBSHAREMGMT**</span><span class="sxs-lookup"><span data-stu-id="46ef1-161">**SPLREG\_WEBSHAREMGMT**</span></span>                                            | <span data-ttu-id="46ef1-162">Windows Server 2003 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="46ef1-162">Windows Server 2003 and later</span></span><br/>                                                                                                                                                                                        |



 

<span data-ttu-id="46ef1-163">Les valeurs suivantes de *pValueName* déterminent le comportement d’impression du pool lorsqu’une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="46ef1-163">The following values of *pValueName* determine the pool printing behavior when an error occurs.</span></span>



| <span data-ttu-id="46ef1-164">Valeur</span><span class="sxs-lookup"><span data-stu-id="46ef1-164">Value</span></span>                                       | <span data-ttu-id="46ef1-165">Commentaires</span><span class="sxs-lookup"><span data-stu-id="46ef1-165">Comments</span></span>                                                                                                                                                                                              |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46ef1-166">**\_ \_ erreur de redémarrage du travail SPLREG \_ sur le \_ pool \_**</span><span class="sxs-lookup"><span data-stu-id="46ef1-166">**SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR**</span></span>   | <span data-ttu-id="46ef1-167">La valeur de *pData* indique la durée, en secondes, à laquelle un travail est redémarré sur un autre port après qu’une erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="46ef1-167">The value of *pData* indicates the time, in seconds, when a job is restarted on another port after an error occurs.</span></span> <span data-ttu-id="46ef1-168">Ce paramètre est utilisé avec **la \_ tâche de redémarrage SPLREG \_ \_ sur le \_ pool \_ activée**.</span><span class="sxs-lookup"><span data-stu-id="46ef1-168">This setting is used with **SPLREG\_RESTART\_JOB\_ON\_POOL\_ENABLED**.</span></span><br/> |
| <span data-ttu-id="46ef1-169">**\_tâche de redémarrage SPLREG \_ \_ sur le \_ pool \_ activée**</span><span class="sxs-lookup"><span data-stu-id="46ef1-169">**SPLREG\_RESTART\_JOB\_ON\_POOL\_ENABLED**</span></span> | <span data-ttu-id="46ef1-170">Une valeur différente de zéro dans *pData* indique **que \_ \_ le travail de redémarrage SPLREG sur l' \_ \_ \_ erreur de pool** est activé.</span><span class="sxs-lookup"><span data-stu-id="46ef1-170">A nonzero value in *pData* indicates that **SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR** is enabled.</span></span><br/>                                                                                            |



 

<span data-ttu-id="46ef1-171">L’heure spécifiée dans **l' \_ erreur de redémarrage du \_ travail SPLREG \_ sur le \_ pool \_** est une heure minimale.</span><span class="sxs-lookup"><span data-stu-id="46ef1-171">The time specified in **SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR** is a minimum time.</span></span> <span data-ttu-id="46ef1-172">L’heure réelle peut être plus longue, en fonction des paramètres de moniteur de port suivants, qui sont des valeurs de Registre sous cette clé de Registre :</span><span class="sxs-lookup"><span data-stu-id="46ef1-172">The actual time can be longer, depending on the following port monitor settings, which are registry values under this registry key:</span></span>

<span data-ttu-id="46ef1-173">**HKLM \\ System \\ CurrentControlSet \\ Control \\ moniteurs d’impression \\ \\ <  > \\ ports nomdumoniteur**</span><span class="sxs-lookup"><span data-stu-id="46ef1-173">**HKLM\\SYSTEM\\CurrentControlSet\\Control\\Print\\Monitors\\<*MonitorName*>\\Ports**</span></span>

<span data-ttu-id="46ef1-174">Appelez la fonction [**RegSetValueEx**](/windows/win32/api/winreg/nf-winreg-regsetvaluea) pour définir ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="46ef1-174">Call the [**RegSetValueEx**](/windows/win32/api/winreg/nf-winreg-regsetvaluea) function to set these values.</span></span>



| <span data-ttu-id="46ef1-175">Paramètre du moniteur de port</span><span class="sxs-lookup"><span data-stu-id="46ef1-175">Port monitor setting</span></span>     | <span data-ttu-id="46ef1-176">Type de données</span><span class="sxs-lookup"><span data-stu-id="46ef1-176">Data type</span></span>      | <span data-ttu-id="46ef1-177">Signification</span><span class="sxs-lookup"><span data-stu-id="46ef1-177">Meaning</span></span>                                                                                                        |
|--------------------------|----------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46ef1-178">**StatusUpdateEnabled**</span><span class="sxs-lookup"><span data-stu-id="46ef1-178">**StatusUpdateEnabled**</span></span>  | <span data-ttu-id="46ef1-179">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="46ef1-179">**REG\_DWORD**</span></span> | <span data-ttu-id="46ef1-180">Si la valeur est différente de zéro, active le moniteur de port pour mettre à jour le spouleur avec l’état du port.</span><span class="sxs-lookup"><span data-stu-id="46ef1-180">If a nonzero value, enables the port monitor to update the spooler with the port status.</span></span><br/>            |
| <span data-ttu-id="46ef1-181">**StatusUpdateInterval**</span><span class="sxs-lookup"><span data-stu-id="46ef1-181">**StatusUpdateInterval**</span></span> | <span data-ttu-id="46ef1-182">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="46ef1-182">**REG\_DWORD**</span></span> | <span data-ttu-id="46ef1-183">Spécifie l’intervalle, en minutes, au cours duquel le moniteur de port met à jour le spouleur avec l’état du port.</span><span class="sxs-lookup"><span data-stu-id="46ef1-183">Specifies the interval, in minutes, when the port monitor updates the spooler with the port status.</span></span><br/> |



 

<span data-ttu-id="46ef1-184">Dans Windows 7 et les versions ultérieures de Windows, les travaux d’impression qui sont envoyés à un serveur d’impression sont rendus sur le client par défaut.</span><span class="sxs-lookup"><span data-stu-id="46ef1-184">In Windows 7 and later versions of Windows, print jobs that are sent to a print server are rendered on the client by default.</span></span> <span data-ttu-id="46ef1-185">Le rendu côté client d’un travail d’impression peut être configuré pour chaque imprimante en définissant les valeurs suivantes dans *pValueName*.</span><span class="sxs-lookup"><span data-stu-id="46ef1-185">Client-side rendering of a print jobs can be configured for each printer by setting the following values in *pValueName*.</span></span>



| <span data-ttu-id="46ef1-186">Paramètre</span><span class="sxs-lookup"><span data-stu-id="46ef1-186">Setting</span></span>                      | <span data-ttu-id="46ef1-187">Type de données</span><span class="sxs-lookup"><span data-stu-id="46ef1-187">Data type</span></span>      | <span data-ttu-id="46ef1-188">Description</span><span class="sxs-lookup"><span data-stu-id="46ef1-188">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46ef1-189">**EMFDespoolingSetting**</span><span class="sxs-lookup"><span data-stu-id="46ef1-189">**EMFDespoolingSetting**</span></span>     | <span data-ttu-id="46ef1-190">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="46ef1-190">**REG\_DWORD**</span></span> | <span data-ttu-id="46ef1-191">La valeur 0, ou si cette valeur n’est pas présente dans le registre, active le rendu par défaut côté client des travaux d’impression.</span><span class="sxs-lookup"><span data-stu-id="46ef1-191">A value of 0, or if this value is not present in the registry, enables the default client-side rendering of print jobs.</span></span><br/> <span data-ttu-id="46ef1-192">La valeur 1 désactive le rendu côté client des travaux d’impression.</span><span class="sxs-lookup"><span data-stu-id="46ef1-192">A value of 1 disables client-side rendering of print jobs.</span></span><br/>                                                                                                                                                                                                      |
| <span data-ttu-id="46ef1-193">**ForceClientSideRendering**</span><span class="sxs-lookup"><span data-stu-id="46ef1-193">**ForceClientSideRendering**</span></span> | <span data-ttu-id="46ef1-194">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="46ef1-194">**REG\_DWORD**</span></span> | <span data-ttu-id="46ef1-195">La valeur 0, ou si cette valeur n’est pas présente dans le registre, entraîne le rendu des travaux d’impression sur le client.</span><span class="sxs-lookup"><span data-stu-id="46ef1-195">A value of 0, or if this value is not present in the registry, causes the print jobs to be rendered on the client.</span></span> <span data-ttu-id="46ef1-196">Si un travail d’impression ne peut pas être rendu sur le client, il sera rendu sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="46ef1-196">If a print job cannot be rendered on the client, it will be rendered on the server.</span></span> <span data-ttu-id="46ef1-197">Si un travail d’impression ne peut pas être rendu sur le serveur, il échoue.</span><span class="sxs-lookup"><span data-stu-id="46ef1-197">If a print job cannot be rendered on the server, it will fail.</span></span><br/> <span data-ttu-id="46ef1-198">La valeur 1 affiche les travaux d’impression sur le client.</span><span class="sxs-lookup"><span data-stu-id="46ef1-198">A value of 1 will render print jobs on the client.</span></span> <span data-ttu-id="46ef1-199">Si un travail d’impression ne peut pas être rendu sur le client, l’opération échoue.</span><span class="sxs-lookup"><span data-stu-id="46ef1-199">If a print job cannot be rendered on the client, it will fail.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="46ef1-200">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="46ef1-200">Requirements</span></span>



| <span data-ttu-id="46ef1-201">Condition requise</span><span class="sxs-lookup"><span data-stu-id="46ef1-201">Requirement</span></span> | <span data-ttu-id="46ef1-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="46ef1-202">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46ef1-203">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="46ef1-203">Minimum supported client</span></span><br/> | <span data-ttu-id="46ef1-204">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="46ef1-204">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="46ef1-205">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="46ef1-205">Minimum supported server</span></span><br/> | <span data-ttu-id="46ef1-206">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="46ef1-206">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="46ef1-207">En-tête</span><span class="sxs-lookup"><span data-stu-id="46ef1-207">Header</span></span><br/>                   | <dl> <span data-ttu-id="46ef1-208"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="46ef1-208"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="46ef1-209">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="46ef1-209">Library</span></span><br/>                  | <dl> <span data-ttu-id="46ef1-210"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="46ef1-210"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="46ef1-211">DLL</span><span class="sxs-lookup"><span data-stu-id="46ef1-211">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46ef1-212"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="46ef1-212"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="46ef1-213">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="46ef1-213">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="46ef1-214">**SetPrinterDataW** (Unicode) et **SetPrinterDataA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="46ef1-214">**SetPrinterDataW** (Unicode) and **SetPrinterDataA** (ANSI)</span></span><br/>                                   |



## <a name="see-also"></a><span data-ttu-id="46ef1-215">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="46ef1-215">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46ef1-216">Impression</span><span class="sxs-lookup"><span data-stu-id="46ef1-216">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="46ef1-217">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="46ef1-217">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="46ef1-218">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="46ef1-218">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="46ef1-219">**GetPrinterData**</span><span class="sxs-lookup"><span data-stu-id="46ef1-219">**GetPrinterData**</span></span>](getprinterdata.md)
</dt> <dt>

[<span data-ttu-id="46ef1-220">**GetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="46ef1-220">**GetPrinterDataEx**</span></span>](getprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="46ef1-221">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="46ef1-221">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="46ef1-222">**SetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="46ef1-222">**SetPrinterDataEx**</span></span>](setprinterdataex.md)
</dt> </dl>

 

