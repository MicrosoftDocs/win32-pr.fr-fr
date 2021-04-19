---
description: La fonction GetPrinterData récupère les données de configuration pour l’imprimante ou le serveur d’impression spécifié.
ms.assetid: b5a44b27-a4aa-4e58-9a64-05be87d12ab5
title: GetPrinterData, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterData
- GetPrinterDataA
- GetPrinterDataW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: cb18936d6d3c1d82f4a52a874883cdcdfaae4815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518789"
---
# <a name="getprinterdata-function"></a><span data-ttu-id="6a51e-103">GetPrinterData fonction)</span><span class="sxs-lookup"><span data-stu-id="6a51e-103">GetPrinterData function</span></span>

<span data-ttu-id="6a51e-104">La fonction **GetPrinterData** récupère les données de configuration pour l’imprimante ou le serveur d’impression spécifié.</span><span class="sxs-lookup"><span data-stu-id="6a51e-104">The **GetPrinterData** function retrieves configuration data for the specified printer or print server.</span></span>

<span data-ttu-id="6a51e-105">Dans Windows 2000 et les versions ultérieures de Windows, l’appel de **GetPrinterData** équivaut à appeler [**GetPrinterDataEx**](/windows/desktop/printdocs/getprinterdataex) avec le paramètre *pKeyName* défini sur « PrinterDriverData ».</span><span class="sxs-lookup"><span data-stu-id="6a51e-105">In Windows 2000 and later versions of Windows, calling **GetPrinterData** is equivalent to calling [**GetPrinterDataEx**](/windows/desktop/printdocs/getprinterdataex) with the *pKeyName* parameter set to "PrinterDriverData".</span></span>

## <a name="syntax"></a><span data-ttu-id="6a51e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6a51e-106">Syntax</span></span>


```C++
DWORD GetPrinterData(
  _In_  HANDLE  hPrinter,
  _In_  LPTSTR  pValueName,
  _Out_ LPDWORD pType,
  _Out_ LPBYTE  pData,
  _In_  DWORD   nSize,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="6a51e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6a51e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a51e-108">*hPrinter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6a51e-108">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a51e-109">Handle vers l’imprimante ou le serveur d’impression pour lequel la fonction récupère les données de configuration.</span><span class="sxs-lookup"><span data-stu-id="6a51e-109">A handle to the printer or print server for which the function retrieves configuration data.</span></span> <span data-ttu-id="6a51e-110">Utilisez la fonction [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md)ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="6a51e-110">Use the [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md), or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="6a51e-111">*pValueName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6a51e-111">*pValueName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a51e-112">Pointeur vers une chaîne terminée par le caractère null qui identifie les données à récupérer.</span><span class="sxs-lookup"><span data-stu-id="6a51e-112">A pointer to a null-terminated string that identifies the data to retrieve.</span></span>

<span data-ttu-id="6a51e-113">Pour les imprimantes, cette chaîne correspond au nom d’une valeur de Registre sous la clé « PrinterDriverData » de l’imprimante dans le registre.</span><span class="sxs-lookup"><span data-stu-id="6a51e-113">For printers, this string is the name of a registry value under the printer's "PrinterDriverData" key in the registry.</span></span>

<span data-ttu-id="6a51e-114">Pour les serveurs d’impression, cette chaîne est l’une des chaînes prédéfinies énumérées dans la section Notes suivante.</span><span class="sxs-lookup"><span data-stu-id="6a51e-114">For print servers, this string is one of the predefined strings listed in the following Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="6a51e-115">*PTYPE* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6a51e-115">*pType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a51e-116">Pointeur vers une variable qui reçoit une valeur qui indique le type de données extraites dans *pData*.</span><span class="sxs-lookup"><span data-stu-id="6a51e-116">A pointer to a variable that receives a value that indicates the type of data retrieved in *pData*.</span></span> <span data-ttu-id="6a51e-117">La fonction retourne le type spécifié dans l’appel [**SetPrinterData**](setprinterdata.md) ou [**SetPrinterDataEx**](setprinterdataex.md) qui a stocké les données.</span><span class="sxs-lookup"><span data-stu-id="6a51e-117">The function returns the type specified in the [**SetPrinterData**](setprinterdata.md) or [**SetPrinterDataEx**](setprinterdataex.md) call that stored the data.</span></span> <span data-ttu-id="6a51e-118">Affectez la valeur **null** à ce paramètre si vous n’avez pas besoin du type de données.</span><span class="sxs-lookup"><span data-stu-id="6a51e-118">Set this parameter to **NULL** if you don't need the data type.</span></span>

</dd> <dt>

<span data-ttu-id="6a51e-119">*pData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6a51e-119">*pData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a51e-120">Pointeur vers une mémoire tampon qui reçoit les données de configuration.</span><span class="sxs-lookup"><span data-stu-id="6a51e-120">A pointer to a buffer that receives the configuration data.</span></span>

</dd> <dt>

<span data-ttu-id="6a51e-121">*nSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6a51e-121">*nSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a51e-122">Taille, en octets, de la mémoire tampon vers laquelle *pData* pointe.</span><span class="sxs-lookup"><span data-stu-id="6a51e-122">The size, in bytes, of the buffer that *pData* points to.</span></span>

</dd> <dt>

<span data-ttu-id="6a51e-123">*pcbNeeded* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6a51e-123">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a51e-124">Pointeur vers une variable qui reçoit la taille, en octets, des données de configuration.</span><span class="sxs-lookup"><span data-stu-id="6a51e-124">A pointer to a variable that receives the size, in bytes, of the configuration data.</span></span> <span data-ttu-id="6a51e-125">Si la taille de la mémoire tampon spécifiée par *nSize* est trop petite, la fonction retourne l' **erreur \_ plus de \_ données** et *pcbNeeded* indique la taille de mémoire tampon requise.</span><span class="sxs-lookup"><span data-stu-id="6a51e-125">If the buffer size specified by *nSize* is too small, the function returns **ERROR\_MORE\_DATA**, and *pcbNeeded* indicates the required buffer size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a51e-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6a51e-126">Return value</span></span>

<span data-ttu-id="6a51e-127">Si la fonction réussit, la valeur de retour est une **erreur de \_ réussite**.</span><span class="sxs-lookup"><span data-stu-id="6a51e-127">If the function succeeds, the return value is **ERROR\_SUCCESS**.</span></span> <span data-ttu-id="6a51e-128">Si la fonction échoue, la valeur de retour est une valeur d’erreur.</span><span class="sxs-lookup"><span data-stu-id="6a51e-128">If the function fails, the return value is an error value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a51e-129">Notes</span><span class="sxs-lookup"><span data-stu-id="6a51e-129">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6a51e-130">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="6a51e-130">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="6a51e-131">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="6a51e-131">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="6a51e-132">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="6a51e-132">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="6a51e-133">**GetPrinterData** récupère les données de configuration d’imprimante qui ont été définies par la fonction [**SetPrinterDataEx**](setprinterdataex.md) ou [**SetPrinterData**](setprinterdata.md) .</span><span class="sxs-lookup"><span data-stu-id="6a51e-133">**GetPrinterData** retrieves printer configuration data that was set by the [**SetPrinterDataEx**](setprinterdataex.md) or [**SetPrinterData**](setprinterdata.md) function.</span></span>

<span data-ttu-id="6a51e-134">**GetPrinterData** peut déclencher un appel Windows à [**GetPrinterDataFromPort**](/previous-versions//ff550506(v=vs.85)), qui peut écrire dans le registre.</span><span class="sxs-lookup"><span data-stu-id="6a51e-134">**GetPrinterData** might trigger a Windows call to [**GetPrinterDataFromPort**](/previous-versions//ff550506(v=vs.85)), which might write to the registry.</span></span> <span data-ttu-id="6a51e-135">Si c’est le cas, des effets secondaires peuvent se produire, tels que le déclenchement d’une mise à jour ou d’une mise à niveau de l’ID d’événement 20 dans le client, si l’imprimante est partagée sur un réseau.</span><span class="sxs-lookup"><span data-stu-id="6a51e-135">If it does, side effects can occur, such as triggering an update or upgrade printer event ID 20 in the client, if the printer is shared in a network.</span></span>

<span data-ttu-id="6a51e-136">Si *hPrinter* est un handle vers un serveur d’impression, *pValueName* peut spécifier l’une des valeurs prédéfinies suivantes.</span><span class="sxs-lookup"><span data-stu-id="6a51e-136">If *hPrinter* is a handle to a print server, *pValueName* can specify one of the following predefined values.</span></span>



| <span data-ttu-id="6a51e-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="6a51e-137">Value</span></span>                                                               | <span data-ttu-id="6a51e-138">Commentaires</span><span class="sxs-lookup"><span data-stu-id="6a51e-138">Comments</span></span>                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a51e-139">**SPLREG \_ autoriser l' \_ utilisateur \_ MANAGEFORMS**</span><span class="sxs-lookup"><span data-stu-id="6a51e-139">**SPLREG\_ALLOW\_USER\_MANAGEFORMS**</span></span>                                | <span data-ttu-id="6a51e-140">Windows XP avec Service Pack 2 (SP2) et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="6a51e-140">Windows XP with Service Pack 2 (SP2) and later</span></span><br/> <span data-ttu-id="6a51e-141">Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="6a51e-141">Windows Server 2003 with Service Pack 1 (SP1) and later</span></span><br/>                                                                                                    |
| <span data-ttu-id="6a51e-142">**\_architecture SPLREG**</span><span class="sxs-lookup"><span data-stu-id="6a51e-142">**SPLREG\_ARCHITECTURE**</span></span>                                            |                                                                                                                                                                                                                                 |
| <span data-ttu-id="6a51e-143">**\_signal sonore SPLREG \_ activé**</span><span class="sxs-lookup"><span data-stu-id="6a51e-143">**SPLREG\_BEEP\_ENABLED**</span></span>                                           |                                                                                                                                                                                                                                 |
| <span data-ttu-id="6a51e-144">**SPLREG \_ \_ Répertoire de spoule par défaut \_**</span><span class="sxs-lookup"><span data-stu-id="6a51e-144">**SPLREG\_DEFAULT\_SPOOL\_DIRECTORY**</span></span>                               |                                                                                                                                                                                                                                 |
| <span data-ttu-id="6a51e-145">**nom de l' \_ ordinateur DNS SPLREG \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6a51e-145">**SPLREG\_DNS\_MACHINE\_NAME**</span></span>                                      |                                                                                                                                                                                                                                 |
| <span data-ttu-id="6a51e-146">**SPLREG \_ DS \_ présent**</span><span class="sxs-lookup"><span data-stu-id="6a51e-146">**SPLREG\_DS\_PRESENT**</span></span>                                             | <span data-ttu-id="6a51e-147">En cas de retour réussi, *pData* contient 0x0001 si l’ordinateur se trouve sur un domaine DS, sinon, 0.</span><span class="sxs-lookup"><span data-stu-id="6a51e-147">On successful return, *pData* contains 0x0001 if the machine is on a DS domain, 0 otherwise.</span></span><br/>                                                                                                                         |
| <span data-ttu-id="6a51e-148">**SPLREG \_ DS \_ présent \_ pour l' \_ utilisateur**</span><span class="sxs-lookup"><span data-stu-id="6a51e-148">**SPLREG\_DS\_PRESENT\_FOR\_USER**</span></span>                                  | <span data-ttu-id="6a51e-149">En cas de retour réussi, *pData* contient 0x0001 si l’utilisateur a ouvert une session sur un domaine DS, sinon, 0.</span><span class="sxs-lookup"><span data-stu-id="6a51e-149">On successful return, *pData* contains 0x0001 if the user is logged onto a DS domain, 0 otherwise.</span></span><br/>                                                                                                                   |
| <span data-ttu-id="6a51e-150">**\_Journal des événements SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="6a51e-150">**SPLREG\_EVENT\_LOG**</span></span>                                              |                                                                                                                                                                                                                                 |
| <span data-ttu-id="6a51e-151">**\_version principale de SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="6a51e-151">**SPLREG\_MAJOR\_VERSION**</span></span>                                          |                                                                                                                                                                                                                                 |
| <span data-ttu-id="6a51e-152">**\_version mineure SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="6a51e-152">**SPLREG\_MINOR\_VERSION**</span></span>                                          |                                                                                                                                                                                                                                 |
| <span data-ttu-id="6a51e-153">**\_fenêtre SPLREG NET \_**</span><span class="sxs-lookup"><span data-stu-id="6a51e-153">**SPLREG\_NET\_POPUP**</span></span>                                              | <span data-ttu-id="6a51e-154">Non pris en charge dans Windows Server 2003 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="6a51e-154">Not supported in Windows Server 2003 and later</span></span><br/>                                                                                                                                                                       |
| <span data-ttu-id="6a51e-155">**SPLREG \_ NET \_ Popup \_ à l' \_ ordinateur**</span><span class="sxs-lookup"><span data-stu-id="6a51e-155">**SPLREG\_NET\_POPUP\_TO\_COMPUTER**</span></span>                                | <span data-ttu-id="6a51e-156">En cas de retour réussi, *pData* contient 1 si les notifications de travaux doivent être envoyées à l’ordinateur client, ou 0 si les notifications de travail doivent être envoyées à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6a51e-156">On successful return, *pData* contains 1 if job notifications should be sent to the client computer, or 0 if job notifications are to be sent to the user.</span></span><br/> <span data-ttu-id="6a51e-157">Non pris en charge dans Windows Server 2003 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="6a51e-157">Not supported in Windows Server 2003 and later</span></span><br/> |
| <span data-ttu-id="6a51e-158">**\_version du système d’exploitation SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="6a51e-158">**SPLREG\_OS\_VERSION**</span></span>                                             | <span data-ttu-id="6a51e-159">Windows XP et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="6a51e-159">Windows XP and later</span></span><br/>                                                                                                                                                                                                 |
| <span data-ttu-id="6a51e-160">**SPLREG \_ se \_ VERSIONEX**</span><span class="sxs-lookup"><span data-stu-id="6a51e-160">**SPLREG\_OS\_VERSIONEX**</span></span>                                           |                                                                                                                                                                                                                                 |
| <span data-ttu-id="6a51e-161">**\_ \_ \_ \_ valeur par défaut de la priorité du thread du port SPLREG**</span><span class="sxs-lookup"><span data-stu-id="6a51e-161">**SPLREG\_PORT\_THREAD\_PRIORITY\_DEFAULT**</span></span>                         |                                                                                                                                                                                                                                 |
| <span data-ttu-id="6a51e-162">**\_priorité de \_ thread de port SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="6a51e-162">**SPLREG\_PORT\_THREAD\_PRIORITY**</span></span>                                  |                                                                                                                                                                                                                                 |
| <span data-ttu-id="6a51e-163">**\_ \_ \_ groupes d’isolation du pilote d’impression SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="6a51e-163">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_GROUPS**</span></span>                        | <span data-ttu-id="6a51e-164">Windows 7 et ultérieur</span><span class="sxs-lookup"><span data-stu-id="6a51e-164">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="6a51e-165">**\_ \_ \_ temps d’isolement du pilote d’impression SPLREG \_ avant le \_ \_ recyclage**</span><span class="sxs-lookup"><span data-stu-id="6a51e-165">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_TIME\_BEFORE\_RECYCLE**</span></span>         | <span data-ttu-id="6a51e-166">Windows 7 et ultérieur</span><span class="sxs-lookup"><span data-stu-id="6a51e-166">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="6a51e-167">**\_isolement du \_ pilote d’impression SPLREG \_ \_ nombre maximal d' \_ objets \_ avant le \_ recyclage**</span><span class="sxs-lookup"><span data-stu-id="6a51e-167">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_MAX\_OBJECTS\_BEFORE\_RECYCLE**</span></span> | <span data-ttu-id="6a51e-168">Windows 7 et ultérieur</span><span class="sxs-lookup"><span data-stu-id="6a51e-168">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="6a51e-169">**\_ \_ \_ \_ délai d’inactivité d’isolation du pilote d’impression \_ SPLREG**</span><span class="sxs-lookup"><span data-stu-id="6a51e-169">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_IDLE\_TIMEOUT**</span></span>                 | <span data-ttu-id="6a51e-170">Windows 7 et ultérieur</span><span class="sxs-lookup"><span data-stu-id="6a51e-170">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="6a51e-171">**\_ \_ \_ stratégie d’exécution de \_ l' \_ isolation du pilote d’impression SPLREG**</span><span class="sxs-lookup"><span data-stu-id="6a51e-171">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_EXECUTION\_POLICY**</span></span>             | <span data-ttu-id="6a51e-172">Windows 7 et ultérieur</span><span class="sxs-lookup"><span data-stu-id="6a51e-172">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="6a51e-173">**\_stratégie de \_ \_ remplacement d’isolation du pilote d’impression \_ SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="6a51e-173">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_OVERRIDE\_POLICY**</span></span>              | <span data-ttu-id="6a51e-174">Windows 7 et ultérieur</span><span class="sxs-lookup"><span data-stu-id="6a51e-174">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="6a51e-175">**\_télécopie à distance SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="6a51e-175">**SPLREG\_REMOTE\_FAX**</span></span>                                             | <span data-ttu-id="6a51e-176">En cas de retour réussi, *pData* contient 0x0001 si le service de télécopie prend en charge les clients distants, sinon 0.</span><span class="sxs-lookup"><span data-stu-id="6a51e-176">On successful return, *pData* contains 0x0001 if the FAX service supports remote clients, 0 otherwise.</span></span><br/>                                                                                                               |
| <span data-ttu-id="6a51e-177">**\_ \_ fenêtre contextuelle SPLREG Retry**</span><span class="sxs-lookup"><span data-stu-id="6a51e-177">**SPLREG\_RETRY\_POPUP**</span></span>                                            | <span data-ttu-id="6a51e-178">En cas de retour réussi, *pData* contient 1 si le serveur est configuré pour réessayer les fenêtres contextuelles pour tous les travaux, ou 0 si le serveur ne réessaye pas les fenêtres publicitaires pour tous les travaux.</span><span class="sxs-lookup"><span data-stu-id="6a51e-178">On successful return, *pData* contains 1 if server is set to retry pop-up windows for all jobs, or 0 if server does not retry pop-up windows for all jobs.</span></span><br/> <span data-ttu-id="6a51e-179">Non pris en charge dans Windows Server 2003 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="6a51e-179">Not supported in Windows Server 2003 and later</span></span><br/> |
| <span data-ttu-id="6a51e-180">**\_ \_ priorité de threads du planificateur SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="6a51e-180">**SPLREG\_SCHEDULER\_THREAD\_PRIORITY**</span></span>                             |                                                                                                                                                                                                                                 |
| <span data-ttu-id="6a51e-181">**\_priorité de thread du planificateur SPLREG \_ \_ \_ par défaut**</span><span class="sxs-lookup"><span data-stu-id="6a51e-181">**SPLREG\_SCHEDULER\_THREAD\_PRIORITY\_DEFAULT**</span></span>                    |                                                                                                                                                                                                                                 |
| <span data-ttu-id="6a51e-182">**SPLREG \_ WEBSHAREMGMT**</span><span class="sxs-lookup"><span data-stu-id="6a51e-182">**SPLREG\_WEBSHAREMGMT**</span></span>                                            | <span data-ttu-id="6a51e-183">Windows Server 2003 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="6a51e-183">Windows Server 2003 and later</span></span><br/>                                                                                                                                                                                        |



 

<span data-ttu-id="6a51e-184">Les valeurs suivantes de *pValueName* indiquent le comportement d’impression du pool lorsqu’une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="6a51e-184">The following values of *pValueName* indicate the pool printing behavior when an error occurs.</span></span>



| <span data-ttu-id="6a51e-185">Valeur</span><span class="sxs-lookup"><span data-stu-id="6a51e-185">Value</span></span>                                       | <span data-ttu-id="6a51e-186">Commentaires</span><span class="sxs-lookup"><span data-stu-id="6a51e-186">Comments</span></span>                                                                                                                                                                                              |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a51e-187">**\_ \_ erreur de redémarrage du travail SPLREG \_ sur le \_ pool \_**</span><span class="sxs-lookup"><span data-stu-id="6a51e-187">**SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR**</span></span>   | <span data-ttu-id="6a51e-188">La valeur de *pData* indique la durée, en secondes, à laquelle un travail est redémarré sur un autre port après qu’une erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="6a51e-188">The value of *pData* indicates the time, in seconds, when a job is restarted on another port after an error occurs.</span></span> <span data-ttu-id="6a51e-189">Ce paramètre est utilisé avec **la \_ tâche de redémarrage SPLREG \_ \_ sur le \_ pool \_ activée**.</span><span class="sxs-lookup"><span data-stu-id="6a51e-189">This setting is used with **SPLREG\_RESTART\_JOB\_ON\_POOL\_ENABLED**.</span></span><br/> |
| <span data-ttu-id="6a51e-190">**\_tâche de redémarrage SPLREG \_ \_ sur le \_ pool \_ activée**</span><span class="sxs-lookup"><span data-stu-id="6a51e-190">**SPLREG\_RESTART\_JOB\_ON\_POOL\_ENABLED**</span></span> | <span data-ttu-id="6a51e-191">Une valeur différente de zéro dans *pData* indique **que \_ \_ le travail de redémarrage SPLREG sur l' \_ \_ \_ erreur de pool** est activé.</span><span class="sxs-lookup"><span data-stu-id="6a51e-191">A nonzero value in *pData* indicates that **SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR** is enabled.</span></span><br/>                                                                                            |



 

<span data-ttu-id="6a51e-192">L’heure spécifiée dans **l' \_ erreur de redémarrage du \_ travail SPLREG \_ sur le \_ pool \_** est une heure minimale.</span><span class="sxs-lookup"><span data-stu-id="6a51e-192">The time specified in **SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR** is a minimum time.</span></span> <span data-ttu-id="6a51e-193">L’heure réelle peut être plus longue, en fonction des paramètres de moniteur de port suivants, qui sont des valeurs de Registre sous cette clé de Registre :</span><span class="sxs-lookup"><span data-stu-id="6a51e-193">The actual time can be longer, depending on the following port monitor settings, which are registry values under this registry key:</span></span>

<span data-ttu-id="6a51e-194">**HKLM \\ System \\ CurrentControlSet \\ Control \\ moniteurs d’impression \\ \\ <  > \\ ports nomdumoniteur**</span><span class="sxs-lookup"><span data-stu-id="6a51e-194">**HKLM\\SYSTEM\\CurrentControlSet\\Control\\Print\\Monitors\\<*MonitorName*>\\Ports**</span></span>

<span data-ttu-id="6a51e-195">Appelez la fonction [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) pour interroger ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="6a51e-195">Call the [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) function to query these values.</span></span>



| <span data-ttu-id="6a51e-196">Paramètre du moniteur de port</span><span class="sxs-lookup"><span data-stu-id="6a51e-196">Port monitor setting</span></span>     | <span data-ttu-id="6a51e-197">Type de données</span><span class="sxs-lookup"><span data-stu-id="6a51e-197">Data type</span></span>      | <span data-ttu-id="6a51e-198">Signification</span><span class="sxs-lookup"><span data-stu-id="6a51e-198">Meaning</span></span>                                                                                                        |
|--------------------------|----------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a51e-199">**StatusUpdateEnabled**</span><span class="sxs-lookup"><span data-stu-id="6a51e-199">**StatusUpdateEnabled**</span></span>  | <span data-ttu-id="6a51e-200">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="6a51e-200">**REG\_DWORD**</span></span> | <span data-ttu-id="6a51e-201">Si la valeur est différente de zéro, active le moniteur de port pour mettre à jour le spouleur avec l’état du port.</span><span class="sxs-lookup"><span data-stu-id="6a51e-201">If a nonzero value, enables the port monitor to update the spooler with the port status.</span></span><br/>            |
| <span data-ttu-id="6a51e-202">**StatusUpdateInterval**</span><span class="sxs-lookup"><span data-stu-id="6a51e-202">**StatusUpdateInterval**</span></span> | <span data-ttu-id="6a51e-203">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="6a51e-203">**REG\_DWORD**</span></span> | <span data-ttu-id="6a51e-204">Spécifie l’intervalle, en minutes, au cours duquel le moniteur de port met à jour le spouleur avec l’état du port.</span><span class="sxs-lookup"><span data-stu-id="6a51e-204">Specifies the interval, in minutes, when the port monitor updates the spooler with the port status.</span></span><br/> |



 

<span data-ttu-id="6a51e-205">Dans Windows 7 et les versions ultérieures de Windows, les travaux d’impression qui sont envoyés à un serveur d’impression sont rendus sur le client par défaut.</span><span class="sxs-lookup"><span data-stu-id="6a51e-205">In Windows 7 and later versions of Windows, print jobs that are sent to a print server are rendered on the client by default.</span></span> <span data-ttu-id="6a51e-206">Les valeurs suivantes configurent le rendu côté client d’un travail d’impression et peuvent être lues si vous définissez les valeurs suivantes dans *pValueName*.</span><span class="sxs-lookup"><span data-stu-id="6a51e-206">The following values configure client-side rendering of a print jobs and can be read if you set the following values in *pValueName*.</span></span>



| <span data-ttu-id="6a51e-207">Paramètre</span><span class="sxs-lookup"><span data-stu-id="6a51e-207">Setting</span></span>                      | <span data-ttu-id="6a51e-208">Type de données</span><span class="sxs-lookup"><span data-stu-id="6a51e-208">Data type</span></span>      | <span data-ttu-id="6a51e-209">Description</span><span class="sxs-lookup"><span data-stu-id="6a51e-209">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a51e-210">**EMFDespoolingSetting**</span><span class="sxs-lookup"><span data-stu-id="6a51e-210">**EMFDespoolingSetting**</span></span>     | <span data-ttu-id="6a51e-211">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="6a51e-211">**REG\_DWORD**</span></span> | <span data-ttu-id="6a51e-212">La valeur 0, ou si cette valeur n’est pas présente dans le registre, active le rendu par défaut côté client des travaux d’impression.</span><span class="sxs-lookup"><span data-stu-id="6a51e-212">A value of 0, or if this value is not present in the registry, enables the default client-side rendering of print jobs.</span></span><br/> <span data-ttu-id="6a51e-213">La valeur 1 désactive le rendu côté client des travaux d’impression.</span><span class="sxs-lookup"><span data-stu-id="6a51e-213">A value of 1 disables client-side rendering of print jobs.</span></span><br/>                                                                                                                                                                                                          |
| <span data-ttu-id="6a51e-214">**ForceClientSideRendering**</span><span class="sxs-lookup"><span data-stu-id="6a51e-214">**ForceClientSideRendering**</span></span> | <span data-ttu-id="6a51e-215">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="6a51e-215">**REG\_DWORD**</span></span> | <span data-ttu-id="6a51e-216">La valeur 0, ou si cette valeur n’est pas présente dans le registre, entraîne le rendu des travaux d’impression sur le client.</span><span class="sxs-lookup"><span data-stu-id="6a51e-216">A value of 0, or if this value is not present in the registry, will cause the print jobs to be rendered on the client.</span></span> <span data-ttu-id="6a51e-217">Si un travail d’impression ne peut pas être rendu sur le client, il sera rendu sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="6a51e-217">If a print job cannot be rendered on the client, it will be rendered on the server.</span></span> <span data-ttu-id="6a51e-218">Si un travail d’impression ne peut pas être rendu sur le serveur, il échoue.</span><span class="sxs-lookup"><span data-stu-id="6a51e-218">If a print job cannot be rendered on the server, it will fail.</span></span><br/> <span data-ttu-id="6a51e-219">La valeur 1 affiche les travaux d’impression sur le client.</span><span class="sxs-lookup"><span data-stu-id="6a51e-219">A value of 1 will render print jobs on the client.</span></span> <span data-ttu-id="6a51e-220">Si un travail d’impression ne peut pas être rendu sur le client, l’opération échoue.</span><span class="sxs-lookup"><span data-stu-id="6a51e-220">If a print job cannot be rendered on the client, it will fail.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6a51e-221">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6a51e-221">Requirements</span></span>



| <span data-ttu-id="6a51e-222">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6a51e-222">Requirement</span></span> | <span data-ttu-id="6a51e-223">Valeur</span><span class="sxs-lookup"><span data-stu-id="6a51e-223">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a51e-224">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a51e-224">Minimum supported client</span></span><br/> | <span data-ttu-id="6a51e-225">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6a51e-225">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6a51e-226">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a51e-226">Minimum supported server</span></span><br/> | <span data-ttu-id="6a51e-227">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6a51e-227">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6a51e-228">En-tête</span><span class="sxs-lookup"><span data-stu-id="6a51e-228">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a51e-229"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6a51e-229"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="6a51e-230">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6a51e-230">Library</span></span><br/>                  | <dl> <span data-ttu-id="6a51e-231"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6a51e-231"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="6a51e-232">DLL</span><span class="sxs-lookup"><span data-stu-id="6a51e-232">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a51e-233"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="6a51e-233"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="6a51e-234">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="6a51e-234">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="6a51e-235">**GetPrinterDataW** (Unicode) et **GetPrinterDataA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="6a51e-235">**GetPrinterDataW** (Unicode) and **GetPrinterDataA** (ANSI)</span></span><br/>                                   |



## <a name="see-also"></a><span data-ttu-id="6a51e-236">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a51e-236">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a51e-237">Impression</span><span class="sxs-lookup"><span data-stu-id="6a51e-237">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="6a51e-238">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="6a51e-238">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="6a51e-239">**GetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="6a51e-239">**GetPrinterDataEx**</span></span>](getprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="6a51e-240">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="6a51e-240">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="6a51e-241">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="6a51e-241">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="6a51e-242">**SetPrinterData**</span><span class="sxs-lookup"><span data-stu-id="6a51e-242">**SetPrinterData**</span></span>](setprinterdata.md)
</dt> <dt>

[<span data-ttu-id="6a51e-243">**SetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="6a51e-243">**SetPrinterDataEx**</span></span>](setprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="6a51e-244">**PRINTPROCESSOR \_ Cap \_ 1**</span><span class="sxs-lookup"><span data-stu-id="6a51e-244">**PRINTPROCESSOR\_CAPS\_1**</span></span>](printprocessor-caps-1.md)
</dt> </dl>

 

