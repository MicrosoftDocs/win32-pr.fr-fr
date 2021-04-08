---
description: La fonction GetPrinterDataEx récupère les données de configuration pour l’imprimante ou le serveur d’impression spécifié.
ms.assetid: 5d9183a7-97cc-46de-848e-e37ce51396eb
title: GetPrinterDataEx, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDataEx
- GetPrinterDataExA
- GetPrinterDataExW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: bdadf2e1259445ca5285e5b12bc906140a137cf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759663"
---
# <a name="getprinterdataex-function"></a><span data-ttu-id="46065-103">GetPrinterDataEx fonction)</span><span class="sxs-lookup"><span data-stu-id="46065-103">GetPrinterDataEx function</span></span>

<span data-ttu-id="46065-104">La fonction **GetPrinterDataEx** récupère les données de configuration pour l’imprimante ou le serveur d’impression spécifié.</span><span class="sxs-lookup"><span data-stu-id="46065-104">The **GetPrinterDataEx** function retrieves configuration data for the specified printer or print server.</span></span> <span data-ttu-id="46065-105">**GetPrinterDataEx** peut récupérer des valeurs stockées par la fonction [**SetPrinterData**](setprinterdata.md) .</span><span class="sxs-lookup"><span data-stu-id="46065-105">**GetPrinterDataEx** can retrieve values that the [**SetPrinterData**](setprinterdata.md) function stored.</span></span> <span data-ttu-id="46065-106">En outre, **GetPrinterDataEx** peut récupérer des valeurs que la fonction [**SetPrinterDataEx**](setprinterdataex.md) stockée sous une clé spécifiée.</span><span class="sxs-lookup"><span data-stu-id="46065-106">In addition, **GetPrinterDataEx** can retrieve values that the [**SetPrinterDataEx**](setprinterdataex.md) function stored under a specified key.</span></span>

## <a name="syntax"></a><span data-ttu-id="46065-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="46065-107">Syntax</span></span>


```C++
DWORD GetPrinterDataEx(
  _In_  HANDLE  hPrinter,
  _In_  LPCTSTR pKeyName,
  _In_  LPCTSTR pValueName,
  _Out_ LPDWORD pType,
  _Out_ LPBYTE  pData,
  _In_  DWORD   nSize,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="46065-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="46065-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46065-109">*hPrinter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="46065-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46065-110">Handle vers l’imprimante ou le serveur d’impression pour lequel la fonction récupère les données de configuration.</span><span class="sxs-lookup"><span data-stu-id="46065-110">A handle to the printer or print server for which the function retrieves configuration data.</span></span> <span data-ttu-id="46065-111">Utilisez la fonction [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md)ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="46065-111">Use the [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md), or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="46065-112">*pKeyName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="46065-112">*pKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46065-113">Pointeur vers une chaîne se terminant par un caractère null qui spécifie la clé contenant la valeur à récupérer.</span><span class="sxs-lookup"><span data-stu-id="46065-113">A pointer to a null-terminated string that specifies the key containing the value to be retrieved.</span></span> <span data-ttu-id="46065-114">Utilisez la barre oblique inverse ( \\ ) comme séparateur pour spécifier un chemin d’accès qui a une ou plusieurs sous-clés.</span><span class="sxs-lookup"><span data-stu-id="46065-114">Use the backslash ( \\ ) character as a delimiter to specify a path that has one or more subkeys.</span></span>

<span data-ttu-id="46065-115">Si *hPrinter* est un handle d’imprimante et que *PKeyName* a la **valeur null** ou est une chaîne vide, **GetPrinterDataEx** retourne un **paramètre d’erreur \_ \_ non valide**.</span><span class="sxs-lookup"><span data-stu-id="46065-115">If *hPrinter* is a handle to a printer and *pKeyName* is **NULL** or an empty string, **GetPrinterDataEx** returns **ERROR\_INVALID\_PARAMETER**.</span></span>

<span data-ttu-id="46065-116">Si *hPrinter* est un handle vers un serveur d’impression, *pKeyName* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="46065-116">If *hPrinter* is a handle to a print server, *pKeyName* is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="46065-117">*pValueName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="46065-117">*pValueName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46065-118">Pointeur vers une chaîne terminée par le caractère null qui identifie les données à récupérer.</span><span class="sxs-lookup"><span data-stu-id="46065-118">A pointer to a null-terminated string that identifies the data to retrieve.</span></span>

<span data-ttu-id="46065-119">Pour les imprimantes, cette chaîne spécifie le nom d’une valeur sous la clé *pKeyName* .</span><span class="sxs-lookup"><span data-stu-id="46065-119">For printers, this string specifies the name of a value under the *pKeyName* key.</span></span>

<span data-ttu-id="46065-120">Pour les serveurs d’impression, cette chaîne est l’une des chaînes prédéfinies énumérées dans la section Notes suivante.</span><span class="sxs-lookup"><span data-stu-id="46065-120">For print servers, this string is one of the predefined strings listed in the following Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="46065-121">*PTYPE* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="46065-121">*pType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46065-122">Pointeur vers une variable qui reçoit le type de données stockées dans la valeur.</span><span class="sxs-lookup"><span data-stu-id="46065-122">A pointer to a variable that receives the type of data stored in the value.</span></span> <span data-ttu-id="46065-123">La fonction retourne le type spécifié dans l’appel [**SetPrinterDataEx**](setprinterdataex.md) lorsque les données ont été stockées.</span><span class="sxs-lookup"><span data-stu-id="46065-123">The function returns the type specified in the [**SetPrinterDataEx**](setprinterdataex.md) call when the data was stored.</span></span> <span data-ttu-id="46065-124">Ce paramètre peut avoir la **valeur null** si vous n’avez pas besoin des informations.</span><span class="sxs-lookup"><span data-stu-id="46065-124">This parameter can be **NULL** if you don't need the information.</span></span> <span data-ttu-id="46065-125">**GetPrinterDataEx** transmet *PTYPE* en tant que paramètre *lpdwType* d’un appel de fonction [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) .</span><span class="sxs-lookup"><span data-stu-id="46065-125">**GetPrinterDataEx** passes *pType* on as the *lpdwType* parameter of a [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) function call.</span></span>

</dd> <dt>

<span data-ttu-id="46065-126">*pData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="46065-126">*pData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46065-127">Pointeur vers une mémoire tampon qui reçoit les données de configuration.</span><span class="sxs-lookup"><span data-stu-id="46065-127">A pointer to a buffer that receives the configuration data.</span></span>

</dd> <dt>

<span data-ttu-id="46065-128">*nSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="46065-128">*nSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46065-129">Taille, en octets, de la mémoire tampon vers laquelle pointe *pData*.</span><span class="sxs-lookup"><span data-stu-id="46065-129">The size, in bytes, of the buffer pointed to by *pData*.</span></span>

</dd> <dt>

<span data-ttu-id="46065-130">*pcbNeeded* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="46065-130">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46065-131">Pointeur vers une variable qui reçoit la taille, en octets, des données de configuration.</span><span class="sxs-lookup"><span data-stu-id="46065-131">A pointer to a variable that receives the size, in bytes, of the configuration data.</span></span> <span data-ttu-id="46065-132">Si la taille de la mémoire tampon spécifiée par *nSize* est trop petite, la fonction retourne l' **erreur \_ plus de \_ données** et *pcbNeeded* indique la taille de mémoire tampon requise.</span><span class="sxs-lookup"><span data-stu-id="46065-132">If the buffer size specified by *nSize* is too small, the function returns **ERROR\_MORE\_DATA**, and *pcbNeeded* indicates the required buffer size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46065-133">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="46065-133">Return value</span></span>

<span data-ttu-id="46065-134">Si la fonction réussit, la valeur de retour est une **erreur de \_ réussite**.</span><span class="sxs-lookup"><span data-stu-id="46065-134">If the function succeeds, the return value is **ERROR\_SUCCESS**.</span></span>

<span data-ttu-id="46065-135">Si la fonction échoue, la valeur de retour est une valeur d’erreur.</span><span class="sxs-lookup"><span data-stu-id="46065-135">If the function fails, the return value is an error value.</span></span>

## <a name="remarks"></a><span data-ttu-id="46065-136">Notes</span><span class="sxs-lookup"><span data-stu-id="46065-136">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="46065-137">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="46065-137">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="46065-138">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="46065-138">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="46065-139">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="46065-139">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="46065-140">**GetPrinterDataEx** récupère les données de configuration de l’imprimante qui ont été définies par les fonctions [**SetPrinterDataEx**](setprinterdataex.md) et [**SetPrinterData**](setprinterdata.md) .</span><span class="sxs-lookup"><span data-stu-id="46065-140">**GetPrinterDataEx** retrieves printer-configuration data that was set by the [**SetPrinterDataEx**](setprinterdataex.md) and [**SetPrinterData**](setprinterdata.md) functions.</span></span>

<span data-ttu-id="46065-141">L’appel de **GetPrinterDataEx** avec le paramètre *pKeyName* défini sur « PrinterDriverData » équivaut à appeler la fonction [**GetPrinterData**](getprinterdata.md) .</span><span class="sxs-lookup"><span data-stu-id="46065-141">Calling **GetPrinterDataEx** with the *pKeyName* parameter set to "PrinterDriverData" is equivalent to calling the [**GetPrinterData**](getprinterdata.md) function.</span></span>

<span data-ttu-id="46065-142">Si *hPrinter* est un handle vers un serveur d’impression, *pValueName* peut spécifier l’une des valeurs prédéfinies suivantes.</span><span class="sxs-lookup"><span data-stu-id="46065-142">If *hPrinter* is a handle to a print server, *pValueName* can specify one of the following predefined values.</span></span>



| <span data-ttu-id="46065-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="46065-143">Value</span></span>                                                               | <span data-ttu-id="46065-144">Commentaires</span><span class="sxs-lookup"><span data-stu-id="46065-144">Comments</span></span>                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46065-145">**SPLREG \_ autoriser l' \_ utilisateur \_ MANAGEFORMS**</span><span class="sxs-lookup"><span data-stu-id="46065-145">**SPLREG\_ALLOW\_USER\_MANAGEFORMS**</span></span>                                | <span data-ttu-id="46065-146">Windows XP avec Service Pack 2 (SP2) et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="46065-146">Windows XP with Service Pack 2 (SP2) and later</span></span><br/> <span data-ttu-id="46065-147">Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="46065-147">Windows Server 2003 with Service Pack 1 (SP1) and later</span></span><br/>                                                                                                    |
| <span data-ttu-id="46065-148">**\_architecture SPLREG**</span><span class="sxs-lookup"><span data-stu-id="46065-148">**SPLREG\_ARCHITECTURE**</span></span>                                            |                                                                                                                                                                                                                                 |
| <span data-ttu-id="46065-149">**\_signal sonore SPLREG \_ activé**</span><span class="sxs-lookup"><span data-stu-id="46065-149">**SPLREG\_BEEP\_ENABLED**</span></span>                                           |                                                                                                                                                                                                                                 |
| <span data-ttu-id="46065-150">**SPLREG \_ \_ Répertoire de spoule par défaut \_**</span><span class="sxs-lookup"><span data-stu-id="46065-150">**SPLREG\_DEFAULT\_SPOOL\_DIRECTORY**</span></span>                               |                                                                                                                                                                                                                                 |
| <span data-ttu-id="46065-151">**nom de l' \_ ordinateur DNS SPLREG \_ \_**</span><span class="sxs-lookup"><span data-stu-id="46065-151">**SPLREG\_DNS\_MACHINE\_NAME**</span></span>                                      |                                                                                                                                                                                                                                 |
| <span data-ttu-id="46065-152">**SPLREG \_ DS \_ présent**</span><span class="sxs-lookup"><span data-stu-id="46065-152">**SPLREG\_DS\_PRESENT**</span></span>                                             | <span data-ttu-id="46065-153">En cas de retour réussi, *pData* contient 0x0001 si l’ordinateur se trouve sur un domaine DS, sinon, 0.</span><span class="sxs-lookup"><span data-stu-id="46065-153">On successful return, *pData* contains 0x0001 if the machine is on a DS domain, 0 otherwise.</span></span><br/>                                                                                                                         |
| <span data-ttu-id="46065-154">**SPLREG \_ DS \_ présent \_ pour l' \_ utilisateur**</span><span class="sxs-lookup"><span data-stu-id="46065-154">**SPLREG\_DS\_PRESENT\_FOR\_USER**</span></span>                                  | <span data-ttu-id="46065-155">En cas de retour réussi, *pData* contient 0x0001 si l’utilisateur a ouvert une session sur un domaine DS, sinon, 0.</span><span class="sxs-lookup"><span data-stu-id="46065-155">On successful return, *pData* contains 0x0001 if the user is logged onto a DS domain, 0 otherwise.</span></span><br/>                                                                                                                   |
| <span data-ttu-id="46065-156">**\_Journal des événements SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="46065-156">**SPLREG\_EVENT\_LOG**</span></span>                                              |                                                                                                                                                                                                                                 |
| <span data-ttu-id="46065-157">**\_version principale de SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="46065-157">**SPLREG\_MAJOR\_VERSION**</span></span>                                          |                                                                                                                                                                                                                                 |
| <span data-ttu-id="46065-158">**\_version mineure SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="46065-158">**SPLREG\_MINOR\_VERSION**</span></span>                                          |                                                                                                                                                                                                                                 |
| <span data-ttu-id="46065-159">**\_fenêtre SPLREG NET \_**</span><span class="sxs-lookup"><span data-stu-id="46065-159">**SPLREG\_NET\_POPUP**</span></span>                                              | <span data-ttu-id="46065-160">Non pris en charge dans Windows Server 2003 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="46065-160">Not supported in Windows Server 2003 and later</span></span><br/>                                                                                                                                                                       |
| <span data-ttu-id="46065-161">**SPLREG \_ NET \_ Popup \_ à l' \_ ordinateur**</span><span class="sxs-lookup"><span data-stu-id="46065-161">**SPLREG\_NET\_POPUP\_TO\_COMPUTER**</span></span>                                | <span data-ttu-id="46065-162">En cas de retour réussi, *pData* contient 1 si les notifications de travaux doivent être envoyées à l’ordinateur client, ou 0 si les notifications de travail doivent être envoyées à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="46065-162">On successful return, *pData* contains 1 if job notifications should be sent to the client computer, or 0 if job notifications are to be sent to the user.</span></span><br/> <span data-ttu-id="46065-163">Non pris en charge dans Windows Server 2003 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="46065-163">Not supported in Windows Server 2003 and later</span></span><br/> |
| <span data-ttu-id="46065-164">**\_version du système d’exploitation SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="46065-164">**SPLREG\_OS\_VERSION**</span></span>                                             | <span data-ttu-id="46065-165">Windows XP et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="46065-165">Windows XP and later</span></span><br/>                                                                                                                                                                                                 |
| <span data-ttu-id="46065-166">**SPLREG \_ se \_ VERSIONEX**</span><span class="sxs-lookup"><span data-stu-id="46065-166">**SPLREG\_OS\_VERSIONEX**</span></span>                                           |                                                                                                                                                                                                                                 |
| <span data-ttu-id="46065-167">**\_ \_ \_ \_ valeur par défaut de la priorité du thread du port SPLREG**</span><span class="sxs-lookup"><span data-stu-id="46065-167">**SPLREG\_PORT\_THREAD\_PRIORITY\_DEFAULT**</span></span>                         |                                                                                                                                                                                                                                 |
| <span data-ttu-id="46065-168">**\_priorité de \_ thread de port SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="46065-168">**SPLREG\_PORT\_THREAD\_PRIORITY**</span></span>                                  |                                                                                                                                                                                                                                 |
| <span data-ttu-id="46065-169">**\_ \_ \_ groupes d’isolation du pilote d’impression SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="46065-169">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_GROUPS**</span></span>                        | <span data-ttu-id="46065-170">Windows 7 et ultérieur</span><span class="sxs-lookup"><span data-stu-id="46065-170">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="46065-171">**\_ \_ \_ temps d’isolement du pilote d’impression SPLREG \_ avant le \_ \_ recyclage**</span><span class="sxs-lookup"><span data-stu-id="46065-171">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_TIME\_BEFORE\_RECYCLE**</span></span>         | <span data-ttu-id="46065-172">Windows 7 et ultérieur</span><span class="sxs-lookup"><span data-stu-id="46065-172">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="46065-173">**\_isolement du \_ pilote d’impression SPLREG \_ \_ nombre maximal d' \_ objets \_ avant le \_ recyclage**</span><span class="sxs-lookup"><span data-stu-id="46065-173">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_MAX\_OBJECTS\_BEFORE\_RECYCLE**</span></span> | <span data-ttu-id="46065-174">Windows 7 et ultérieur</span><span class="sxs-lookup"><span data-stu-id="46065-174">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="46065-175">**\_ \_ \_ \_ délai d’inactivité d’isolation du pilote d’impression \_ SPLREG**</span><span class="sxs-lookup"><span data-stu-id="46065-175">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_IDLE\_TIMEOUT**</span></span>                 | <span data-ttu-id="46065-176">Windows 7 et ultérieur</span><span class="sxs-lookup"><span data-stu-id="46065-176">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="46065-177">**\_ \_ \_ stratégie d’exécution de \_ l' \_ isolation du pilote d’impression SPLREG**</span><span class="sxs-lookup"><span data-stu-id="46065-177">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_EXECUTION\_POLICY**</span></span>             | <span data-ttu-id="46065-178">Windows 7 et ultérieur</span><span class="sxs-lookup"><span data-stu-id="46065-178">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="46065-179">**\_stratégie de \_ \_ remplacement d’isolation du pilote d’impression \_ SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="46065-179">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_OVERRIDE\_POLICY**</span></span>              | <span data-ttu-id="46065-180">Windows 7 et ultérieur</span><span class="sxs-lookup"><span data-stu-id="46065-180">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="46065-181">**\_télécopie à distance SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="46065-181">**SPLREG\_REMOTE\_FAX**</span></span>                                             | <span data-ttu-id="46065-182">En cas de retour réussi, *pData* contient 0x0001 si le service de télécopie prend en charge les clients distants, sinon 0.</span><span class="sxs-lookup"><span data-stu-id="46065-182">On successful return, *pData* contains 0x0001 if the FAX service supports remote clients, 0 otherwise.</span></span><br/>                                                                                                               |
| <span data-ttu-id="46065-183">**\_ \_ fenêtre contextuelle SPLREG Retry**</span><span class="sxs-lookup"><span data-stu-id="46065-183">**SPLREG\_RETRY\_POPUP**</span></span>                                            | <span data-ttu-id="46065-184">En cas de retour réussi, *pData* contient 1 si le serveur est configuré pour réessayer les fenêtres contextuelles pour tous les travaux, ou 0 si le serveur ne réessaye pas les fenêtres publicitaires pour tous les travaux.</span><span class="sxs-lookup"><span data-stu-id="46065-184">On successful return, *pData* contains 1 if server is set to retry pop-up windows for all jobs, or 0 if server does not retry pop-up windows for all jobs.</span></span><br/> <span data-ttu-id="46065-185">Non pris en charge dans Windows Server 2003 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="46065-185">Not supported in Windows Server 2003 and later</span></span><br/> |
| <span data-ttu-id="46065-186">**\_ \_ priorité de threads du planificateur SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="46065-186">**SPLREG\_SCHEDULER\_THREAD\_PRIORITY**</span></span>                             |                                                                                                                                                                                                                                 |
| <span data-ttu-id="46065-187">**\_priorité de thread du planificateur SPLREG \_ \_ \_ par défaut**</span><span class="sxs-lookup"><span data-stu-id="46065-187">**SPLREG\_SCHEDULER\_THREAD\_PRIORITY\_DEFAULT**</span></span>                    |                                                                                                                                                                                                                                 |
| <span data-ttu-id="46065-188">**SPLREG \_ WEBSHAREMGMT**</span><span class="sxs-lookup"><span data-stu-id="46065-188">**SPLREG\_WEBSHAREMGMT**</span></span>                                            | <span data-ttu-id="46065-189">Windows Server 2003 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="46065-189">Windows Server 2003 and later</span></span><br/>                                                                                                                                                                                        |



 

<span data-ttu-id="46065-190">Les valeurs suivantes de *pValueName* indiquent le comportement d’impression du pool lorsqu’une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="46065-190">The following values of *pValueName* indicate the pool printing behavior when an error occurs.</span></span>



| <span data-ttu-id="46065-191">Valeur</span><span class="sxs-lookup"><span data-stu-id="46065-191">Value</span></span>                                       | <span data-ttu-id="46065-192">Commentaires</span><span class="sxs-lookup"><span data-stu-id="46065-192">Comments</span></span>                                                                                                                                                                                              |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46065-193">**\_ \_ erreur de redémarrage du travail SPLREG \_ sur le \_ pool \_**</span><span class="sxs-lookup"><span data-stu-id="46065-193">**SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR**</span></span>   | <span data-ttu-id="46065-194">La valeur de *pData* indique la durée, en secondes, à laquelle un travail est redémarré sur un autre port après qu’une erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="46065-194">The value of *pData* indicates the time, in seconds, when a job is restarted on another port after an error occurs.</span></span> <span data-ttu-id="46065-195">Ce paramètre est utilisé avec **la \_ tâche de redémarrage SPLREG \_ \_ sur le \_ pool \_ activée**.</span><span class="sxs-lookup"><span data-stu-id="46065-195">This setting is used with **SPLREG\_RESTART\_JOB\_ON\_POOL\_ENABLED**.</span></span><br/> |
| <span data-ttu-id="46065-196">**\_tâche de redémarrage SPLREG \_ \_ sur le \_ pool \_ activée**</span><span class="sxs-lookup"><span data-stu-id="46065-196">**SPLREG\_RESTART\_JOB\_ON\_POOL\_ENABLED**</span></span> | <span data-ttu-id="46065-197">Une valeur différente de zéro dans *pData* indique **que \_ \_ le travail de redémarrage SPLREG sur l' \_ \_ \_ erreur de pool** est activé.</span><span class="sxs-lookup"><span data-stu-id="46065-197">A nonzero value in *pData* indicates that **SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR** is enabled.</span></span><br/>                                                                                            |



 

<span data-ttu-id="46065-198">L’heure spécifiée dans **l' \_ erreur de redémarrage du \_ travail SPLREG \_ sur le \_ pool \_** est une heure minimale.</span><span class="sxs-lookup"><span data-stu-id="46065-198">The time specified in **SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR** is a minimum time.</span></span> <span data-ttu-id="46065-199">L’heure réelle peut être plus longue, en fonction des paramètres de moniteur de port suivants, qui sont des valeurs de Registre sous cette clé de Registre :</span><span class="sxs-lookup"><span data-stu-id="46065-199">The actual time can be longer, depending on the following port monitor settings, which are registry values under this registry key:</span></span>

<span data-ttu-id="46065-200">**HKLM \\ System \\ CurrentControlSet \\ Control \\ moniteurs d’impression \\ \\ <  > \\ ports nomdumoniteur**</span><span class="sxs-lookup"><span data-stu-id="46065-200">**HKLM\\SYSTEM\\CurrentControlSet\\Control\\Print\\Monitors\\<*MonitorName*>\\Ports**</span></span>

<span data-ttu-id="46065-201">Appelez la fonction [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) pour interroger ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="46065-201">Call the [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) function to query these values.</span></span>



| <span data-ttu-id="46065-202">Paramètre du moniteur de port</span><span class="sxs-lookup"><span data-stu-id="46065-202">Port monitor setting</span></span>     | <span data-ttu-id="46065-203">Type de données</span><span class="sxs-lookup"><span data-stu-id="46065-203">Data type</span></span>      | <span data-ttu-id="46065-204">Signification</span><span class="sxs-lookup"><span data-stu-id="46065-204">Meaning</span></span>                                                                                                        |
|--------------------------|----------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46065-205">**StatusUpdateEnabled**</span><span class="sxs-lookup"><span data-stu-id="46065-205">**StatusUpdateEnabled**</span></span>  | <span data-ttu-id="46065-206">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="46065-206">**REG\_DWORD**</span></span> | <span data-ttu-id="46065-207">Si la valeur est différente de zéro, active le moniteur de port pour mettre à jour le spouleur avec l’état du port.</span><span class="sxs-lookup"><span data-stu-id="46065-207">If a nonzero value, enables the port monitor to update the spooler with the port status.</span></span><br/>            |
| <span data-ttu-id="46065-208">**StatusUpdateInterval**</span><span class="sxs-lookup"><span data-stu-id="46065-208">**StatusUpdateInterval**</span></span> | <span data-ttu-id="46065-209">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="46065-209">**REG\_DWORD**</span></span> | <span data-ttu-id="46065-210">Spécifie l’intervalle, en minutes, au cours duquel le moniteur de port met à jour le spouleur avec l’état du port.</span><span class="sxs-lookup"><span data-stu-id="46065-210">Specifies the interval, in minutes, when the port monitor updates the spooler with the port status.</span></span><br/> |



 

<span data-ttu-id="46065-211">Si *pKeyName* est l’une des clés du service d’annuaire prédéfini (voir [**SetPrinter**](setprinter.md)) et *pValueName* contient une virgule (', '), la partie de *pValueName* avant la virgule est le nom de la valeur et la partie de *pValueName* à droite de la virgule est l’OID de propriété DS.</span><span class="sxs-lookup"><span data-stu-id="46065-211">If *pKeyName* is one of the predefined Directory Service (DS) keys (see [**SetPrinter**](setprinter.md)) and *pValueName* contains a comma (','), then the portion of *pValueName* before the comma is the value name and the portion of *pValueName* to the right of the comma is the DS Property OID.</span></span> <span data-ttu-id="46065-212">Une sous-clé appelée OID est créée et une nouvelle valeur composée du nom de la valeur et de l’OID est entrée sous la clé OID.</span><span class="sxs-lookup"><span data-stu-id="46065-212">A subkey called OID is created and a new value that consists of the value name and OID is entered under the OID key.</span></span> <span data-ttu-id="46065-213">[**SetPrinterDataEx**](setprinterdataex.md) ajoute également le nom de la valeur et les données sous la clé DS.</span><span class="sxs-lookup"><span data-stu-id="46065-213">[**SetPrinterDataEx**](setprinterdataex.md) also adds the value name and data under the DS key.</span></span>

<span data-ttu-id="46065-214">Dans Windows 7 et les versions ultérieures de Windows, les travaux d’impression qui sont envoyés à un serveur d’impression sont rendus sur le client par défaut.</span><span class="sxs-lookup"><span data-stu-id="46065-214">In Windows 7 and later versions of Windows, print jobs that are sent to a print server are rendered on the client by default.</span></span> <span data-ttu-id="46065-215">La configuration du rendu côté client pour une imprimante peut être lue en définissant *pKeyName* sur « PrinterDriverData » et *pValueName* sur la valeur de paramètre dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="46065-215">The configuration of client-side rendering for a printer can be read by setting *pKeyName* to "PrinterDriverData" and *pValueName* to the setting value in the following table.</span></span>



| <span data-ttu-id="46065-216">Paramètre</span><span class="sxs-lookup"><span data-stu-id="46065-216">Setting</span></span>                      | <span data-ttu-id="46065-217">Type de données</span><span class="sxs-lookup"><span data-stu-id="46065-217">Data type</span></span>      | <span data-ttu-id="46065-218">Description</span><span class="sxs-lookup"><span data-stu-id="46065-218">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46065-219">**EMFDespoolingSetting**</span><span class="sxs-lookup"><span data-stu-id="46065-219">**EMFDespoolingSetting**</span></span>     | <span data-ttu-id="46065-220">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="46065-220">**REG\_DWORD**</span></span> | <span data-ttu-id="46065-221">La valeur 0, ou si cette valeur n’est pas présente dans le registre, active le rendu par défaut côté client des travaux d’impression.</span><span class="sxs-lookup"><span data-stu-id="46065-221">A value of 0, or if this value is not present in the registry, enables the default client-side rendering of print jobs.</span></span><br/> <span data-ttu-id="46065-222">La valeur 1 désactive le rendu côté client des travaux d’impression.</span><span class="sxs-lookup"><span data-stu-id="46065-222">A value of 1 disables client-side rendering of print jobs.</span></span><br/>                                                                                                                                                                                                          |
| <span data-ttu-id="46065-223">**ForceClientSideRendering**</span><span class="sxs-lookup"><span data-stu-id="46065-223">**ForceClientSideRendering**</span></span> | <span data-ttu-id="46065-224">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="46065-224">**REG\_DWORD**</span></span> | <span data-ttu-id="46065-225">La valeur 0, ou si cette valeur n’est pas présente dans le registre, entraîne le rendu des travaux d’impression sur le client.</span><span class="sxs-lookup"><span data-stu-id="46065-225">A value of 0, or if this value is not present in the registry, will cause the print jobs to be rendered on the client.</span></span> <span data-ttu-id="46065-226">Si un travail d’impression ne peut pas être rendu sur le client, il sera rendu sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="46065-226">If a print job cannot be rendered on the client, it will be rendered on the server.</span></span> <span data-ttu-id="46065-227">Si un travail d’impression ne peut pas être rendu sur le serveur, il échoue.</span><span class="sxs-lookup"><span data-stu-id="46065-227">If a print job cannot be rendered on the server, it will fail.</span></span><br/> <span data-ttu-id="46065-228">La valeur 1 affiche les travaux d’impression sur le client.</span><span class="sxs-lookup"><span data-stu-id="46065-228">A value of 1 will render print jobs on the client.</span></span> <span data-ttu-id="46065-229">Si un travail d’impression ne peut pas être rendu sur le client, l’opération échoue.</span><span class="sxs-lookup"><span data-stu-id="46065-229">If a print job cannot be rendered on the client, it will fail.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="46065-230">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="46065-230">Requirements</span></span>



| <span data-ttu-id="46065-231">Condition requise</span><span class="sxs-lookup"><span data-stu-id="46065-231">Requirement</span></span> | <span data-ttu-id="46065-232">Valeur</span><span class="sxs-lookup"><span data-stu-id="46065-232">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46065-233">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="46065-233">Minimum supported client</span></span><br/> | <span data-ttu-id="46065-234">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="46065-234">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="46065-235">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="46065-235">Minimum supported server</span></span><br/> | <span data-ttu-id="46065-236">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="46065-236">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="46065-237">En-tête</span><span class="sxs-lookup"><span data-stu-id="46065-237">Header</span></span><br/>                   | <dl> <span data-ttu-id="46065-238"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="46065-238"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="46065-239">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="46065-239">Library</span></span><br/>                  | <dl> <span data-ttu-id="46065-240"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="46065-240"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="46065-241">DLL</span><span class="sxs-lookup"><span data-stu-id="46065-241">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46065-242"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="46065-242"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="46065-243">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="46065-243">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="46065-244">**GetPrinterDataExW** (Unicode) et **GetPrinterDataExA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="46065-244">**GetPrinterDataExW** (Unicode) and **GetPrinterDataExA** (ANSI)</span></span><br/>                               |



## <a name="see-also"></a><span data-ttu-id="46065-245">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="46065-245">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46065-246">Impression</span><span class="sxs-lookup"><span data-stu-id="46065-246">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="46065-247">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="46065-247">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="46065-248">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="46065-248">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="46065-249">**SetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="46065-249">**SetPrinterDataEx**</span></span>](setprinterdataex.md)
</dt> </dl>

 

