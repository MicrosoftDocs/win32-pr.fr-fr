---
description: La fonction GetPrinter récupère des informations sur une imprimante spécifiée.
ms.assetid: f162edbb-83ee-40c3-8710-9c867301d652
title: GetPrinter, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinter
- GetPrinterA
- GetPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-0.dll
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: e99b3574762b84b830845da8149b0406664b6da7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523420"
---
# <a name="getprinter-function"></a><span data-ttu-id="c4c07-103">GetPrinter fonction)</span><span class="sxs-lookup"><span data-stu-id="c4c07-103">GetPrinter function</span></span>

<span data-ttu-id="c4c07-104">La fonction **GetPrinter** récupère des informations sur une imprimante spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c4c07-104">The **GetPrinter** function retrieves information about a specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4c07-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c4c07-105">Syntax</span></span>


```C++
BOOL GetPrinter(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPrinter,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="c4c07-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c4c07-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4c07-107">*hPrinter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c4c07-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4c07-108">Handle vers l’imprimante pour laquelle la fonction récupère des informations.</span><span class="sxs-lookup"><span data-stu-id="c4c07-108">A handle to the printer for which the function retrieves information.</span></span> <span data-ttu-id="c4c07-109">Utilisez la fonction [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="c4c07-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="c4c07-110">De *niveau* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c4c07-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4c07-111">Niveau ou type de structure que la fonction stocke dans la mémoire tampon vers laquelle pointe *pPrinter*.</span><span class="sxs-lookup"><span data-stu-id="c4c07-111">The level or type of structure that the function stores into the buffer pointed to by *pPrinter*.</span></span>

<span data-ttu-id="c4c07-112">Cette valeur peut être 1, 2, 3, 4, 5, 6, 7, 8 ou 9.</span><span class="sxs-lookup"><span data-stu-id="c4c07-112">This value can be 1, 2, 3, 4, 5, 6, 7, 8 or 9.</span></span>

</dd> <dt>

<span data-ttu-id="c4c07-113">*pPrinter* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c4c07-113">*pPrinter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c4c07-114">Pointeur vers une mémoire tampon qui reçoit une structure contenant des informations sur l’imprimante spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c4c07-114">A pointer to a buffer that receives a structure containing information about the specified printer.</span></span> <span data-ttu-id="c4c07-115">La mémoire tampon doit être suffisamment grande pour recevoir la structure et toutes les chaînes ou autres données auxquelles les membres de la structure pointent.</span><span class="sxs-lookup"><span data-stu-id="c4c07-115">The buffer must be large enough to receive the structure and any strings or other data to which the structure members point.</span></span> <span data-ttu-id="c4c07-116">Si la mémoire tampon est trop petite, le paramètre *pcbNeeded* retourne la taille de mémoire tampon requise.</span><span class="sxs-lookup"><span data-stu-id="c4c07-116">If the buffer is too small, the *pcbNeeded* parameter returns the required buffer size.</span></span>

<span data-ttu-id="c4c07-117">Le type de structure est déterminé par la valeur de *Level*.</span><span class="sxs-lookup"><span data-stu-id="c4c07-117">The type of structure is determined by the value of *Level*.</span></span>



| <span data-ttu-id="c4c07-118">Level</span><span class="sxs-lookup"><span data-stu-id="c4c07-118">Level</span></span>                                                                                                | <span data-ttu-id="c4c07-119">Structure</span><span class="sxs-lookup"><span data-stu-id="c4c07-119">Structure</span></span>                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="c4c07-120"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="c4c07-120"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="c4c07-121">Une structure d’informations d' [**imprimante \_ \_ 1**](printer-info-1.md) contenant des informations générales sur l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="c4c07-121">A [**PRINTER\_INFO\_1**](printer-info-1.md) structure containing general printer information.</span></span><br/>                                                                                                        |
| <span id="2"></span><dl> <span data-ttu-id="c4c07-122"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="c4c07-122"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="c4c07-123">Structure de l' [**imprimante \_ info \_ 2**](printer-info-2.md) contenant des informations détaillées sur l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="c4c07-123">A [**PRINTER\_INFO\_2**](printer-info-2.md) structure containing detailed information about the printer.</span></span><br/>                                                                                             |
| <span id="3"></span><dl> <span data-ttu-id="c4c07-124"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="c4c07-124"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="c4c07-125">Une structure [**Printer \_ info \_ 3**](printer-info-3.md) contenant les informations de sécurité de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="c4c07-125">A [**PRINTER\_INFO\_3**](printer-info-3.md) structure containing the printer's security information.</span></span><br/>                                                                                                 |
| <span id="4"></span><dl> <span data-ttu-id="c4c07-126"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="c4c07-126"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="c4c07-127">Une structure [**Printer \_ info \_ 4**](printer-info-4.md) contenant des informations d’imprimante minimales, y compris le nom de l’imprimante, le nom du serveur et si l’imprimante est distante ou locale.</span><span class="sxs-lookup"><span data-stu-id="c4c07-127">A [**PRINTER\_INFO\_4**](printer-info-4.md) structure containing minimal printer information, including the name of the printer, the name of the server, and whether the printer is remote or local.</span></span><br/> |
| <span id="5"></span><dl> <span data-ttu-id="c4c07-128"><dt>**5**</dt></span><span class="sxs-lookup"><span data-stu-id="c4c07-128"><dt>**5**</dt></span></span> </dl> | <span data-ttu-id="c4c07-129">Une structure [**Printer \_ info \_ 5**](printer-info-5.md) contenant des informations sur l’imprimante, telles que des attributs d’imprimante et des paramètres de délai d’attente.</span><span class="sxs-lookup"><span data-stu-id="c4c07-129">A [**PRINTER\_INFO\_5**](printer-info-5.md) structure containing printer information such as printer attributes and time-out settings.</span></span><br/>                                                               |
| <span id="6"></span><dl> <span data-ttu-id="c4c07-130"><dt>**6**</dt></span><span class="sxs-lookup"><span data-stu-id="c4c07-130"><dt>**6**</dt></span></span> </dl> | <span data-ttu-id="c4c07-131">Une structure [**Printer \_ info \_ 6**](printer-info-6.md) spécifiant la valeur d’état d’une imprimante.</span><span class="sxs-lookup"><span data-stu-id="c4c07-131">A [**PRINTER\_INFO\_6**](printer-info-6.md) structure specifying the status value of a printer.</span></span><br/>                                                                                                      |
| <span id="7"></span><dl> <span data-ttu-id="c4c07-132"><dt>**7**</dt></span><span class="sxs-lookup"><span data-stu-id="c4c07-132"><dt>**7**</dt></span></span> </dl> | <span data-ttu-id="c4c07-133">Une structure d' [**informations d’imprimante \_ \_ 7**](printer-info-7.md) qui indique si l’imprimante est publiée dans le service d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="c4c07-133">A [**PRINTER\_INFO\_7**](printer-info-7.md) structure that indicates whether the printer is published in the directory service.</span></span><br/>                                                                      |
| <span id="8"></span><dl> <span data-ttu-id="c4c07-134"><dt>**8**</dt></span><span class="sxs-lookup"><span data-stu-id="c4c07-134"><dt>**8**</dt></span></span> </dl> | <span data-ttu-id="c4c07-135">Structure [**d' \_ informations \_ d’imprimante 8**](printer-info-8.md) spécifiant les paramètres d’imprimante par défaut globaux.</span><span class="sxs-lookup"><span data-stu-id="c4c07-135">A [**PRINTER\_INFO\_8**](printer-info-8.md) structure specifying the global default printer settings.</span></span><br/>                                                                                                |
| <span id="9"></span><dl> <span data-ttu-id="c4c07-136"><dt>**9**</dt></span><span class="sxs-lookup"><span data-stu-id="c4c07-136"><dt>**9**</dt></span></span> </dl> | <span data-ttu-id="c4c07-137">Une structure d' [**informations d’imprimante \_ \_ 9**](printer-info-9.md) spécifiant les paramètres d’imprimante par défaut par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c4c07-137">A [**PRINTER\_INFO\_9**](printer-info-9.md) structure specifying the per-user default printer settings.</span></span><br/>                                                                                              |



 

</dd> <dt>

<span data-ttu-id="c4c07-138">*cbBuf* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c4c07-138">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4c07-139">Taille, en octets, de la mémoire tampon vers laquelle pointe *pPrinter*.</span><span class="sxs-lookup"><span data-stu-id="c4c07-139">The size, in bytes, of the buffer pointed to by *pPrinter*.</span></span>

</dd> <dt>

<span data-ttu-id="c4c07-140">*pcbNeeded* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c4c07-140">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c4c07-141">Pointeur vers une variable dont la fonction définit la taille, en octets, des informations sur l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="c4c07-141">A pointer to a variable that the function sets to the size, in bytes, of the printer information.</span></span> <span data-ttu-id="c4c07-142">Si la valeur de *cbBuf* est inférieure à cette valeur, **GetPrinter** échoue et la valeur représente la taille de mémoire tampon requise.</span><span class="sxs-lookup"><span data-stu-id="c4c07-142">If *cbBuf* is smaller than this value, **GetPrinter** fails, and the value represents the required buffer size.</span></span> <span data-ttu-id="c4c07-143">Si *cbBuf* est supérieur ou égal à cette valeur, **GetPrinter** suit et la valeur représente le nombre d’octets stockés dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="c4c07-143">If *cbBuf* is equal to or greater than this value, **GetPrinter** succeeds, and the value represents the number of bytes stored in the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4c07-144">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c4c07-144">Return value</span></span>

<span data-ttu-id="c4c07-145">Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="c4c07-145">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="c4c07-146">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="c4c07-146">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4c07-147">Notes</span><span class="sxs-lookup"><span data-stu-id="c4c07-147">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c4c07-148">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="c4c07-148">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="c4c07-149">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="c4c07-149">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="c4c07-150">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="c4c07-150">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="c4c07-151">Le membre **pDevMode** des structures Printer info [**\_ \_ 2**](printer-info-2.md), [**Printer \_ info \_ 8**](printer-info-8.md)et [**Printer \_ info \_ 9**](printer-info-9.md) peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="c4c07-151">The **pDevMode** member in the [**PRINTER\_INFO\_2**](printer-info-2.md), [**PRINTER\_INFO\_8**](printer-info-8.md), and [**PRINTER\_INFO\_9**](printer-info-9.md) structures can be **NULL**.</span></span> <span data-ttu-id="c4c07-152">Dans ce cas, l’imprimante est inutilisable jusqu’à ce que le pilote soit réinstallé avec succès.</span><span class="sxs-lookup"><span data-stu-id="c4c07-152">When this happens, the printer is unusable until the driver is reinstalled successfully.</span></span>

<span data-ttu-id="c4c07-153">Pour les structures [**Printer \_ info \_ 2**](printer-info-2.md) et [**Printer \_ info \_ 3**](printer-info-3.md) qui contiennent un pointeur vers un descripteur de sécurité, la fonction récupère uniquement les composants du descripteur de sécurité que l’appelant est autorisé à lire.</span><span class="sxs-lookup"><span data-stu-id="c4c07-153">For the [**PRINTER\_INFO\_2**](printer-info-2.md) and [**PRINTER\_INFO\_3**](printer-info-3.md) structures that contain a pointer to a security descriptor, the function retrieves only those components of the security descriptor that the caller has permission to read.</span></span> <span data-ttu-id="c4c07-154">Pour récupérer des composants de descripteur de sécurité particuliers, vous devez spécifier les droits d’accès nécessaires lorsque vous appelez la fonction [**OpenPrinter**](openprinter.md) pour récupérer un handle vers l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="c4c07-154">To retrieve particular security descriptor components, you must specify the necessary access rights when you call the [**OpenPrinter**](openprinter.md) function to retrieve a handle to the printer.</span></span> <span data-ttu-id="c4c07-155">Le tableau suivant présente les droits d’accès requis pour lire les différents composants du descripteur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="c4c07-155">The following table shows the access rights required to read the various security descriptor components.</span></span>



| <span data-ttu-id="c4c07-156">Droit d'accès</span><span class="sxs-lookup"><span data-stu-id="c4c07-156">Access Right</span></span>                        | <span data-ttu-id="c4c07-157">Composant descripteur de sécurité</span><span class="sxs-lookup"><span data-stu-id="c4c07-157">Security Descriptor Component</span></span>                                                                 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4c07-158">LIRE \_ le contrôle</span><span class="sxs-lookup"><span data-stu-id="c4c07-158">READ\_CONTROL</span></span><br/>            | <span data-ttu-id="c4c07-159">Propriétaire</span><span class="sxs-lookup"><span data-stu-id="c4c07-159">Owner</span></span><br/> <span data-ttu-id="c4c07-160">Groupe principal</span><span class="sxs-lookup"><span data-stu-id="c4c07-160">Primary group</span></span><br/> <span data-ttu-id="c4c07-161">Liste de contrôle d’accès discrétionnaire (DACL)</span><span class="sxs-lookup"><span data-stu-id="c4c07-161">Discretionary access-control list (DACL)</span></span><br/> |
| <span data-ttu-id="c4c07-162">ACCÉDER à la \_ sécurité du système \_</span><span class="sxs-lookup"><span data-stu-id="c4c07-162">ACCESS\_SYSTEM\_SECURITY</span></span><br/> | <span data-ttu-id="c4c07-163">Liste de contrôle d’accès système (SACL)</span><span class="sxs-lookup"><span data-stu-id="c4c07-163">System access-control list (SACL)</span></span><br/>                                                  |



 

<span data-ttu-id="c4c07-164">Si vous spécifiez le niveau 7, le membre **dwAction** de [**Printer \_ info \_ 7**](printer-info-7.md) retourne l’une des valeurs suivantes pour indiquer si l’imprimante est publiée dans le service d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="c4c07-164">If you specify level 7, the **dwAction** member of [**PRINTER\_INFO\_7**](printer-info-7.md) returns one of the following values to indicate whether the printer is published in the directory service.</span></span>



| <span data-ttu-id="c4c07-165">valeur dwAction</span><span class="sxs-lookup"><span data-stu-id="c4c07-165">dwAction value</span></span>     | <span data-ttu-id="c4c07-166">Signification</span><span class="sxs-lookup"><span data-stu-id="c4c07-166">Meaning</span></span>                                                                                                                                                                                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4c07-167">\_publication DSPRINT</span><span class="sxs-lookup"><span data-stu-id="c4c07-167">DSPRINT\_PUBLISH</span></span>   | <span data-ttu-id="c4c07-168">L’imprimante est publiée.</span><span class="sxs-lookup"><span data-stu-id="c4c07-168">The printer is published.</span></span> <span data-ttu-id="c4c07-169">Le membre **pszObjectGUID** contient le GUID de l’objet file d’attente à l’impression des services d’annuaire associé à l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="c4c07-169">The **pszObjectGUID** member contains the GUID of the directory services print queue object associated with the printer.</span></span>                                                                                                       |
| <span data-ttu-id="c4c07-170">DSPRINT \_ annuler la publication</span><span class="sxs-lookup"><span data-stu-id="c4c07-170">DSPRINT\_UNPUBLISH</span></span> | <span data-ttu-id="c4c07-171">L’imprimante n’est pas publiée.</span><span class="sxs-lookup"><span data-stu-id="c4c07-171">The printer is not published.</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="c4c07-172">DSPRINT \_ en attente</span><span class="sxs-lookup"><span data-stu-id="c4c07-172">DSPRINT\_PENDING</span></span>   | <span data-ttu-id="c4c07-173">Indique que le système tente d’effectuer une opération de publication ou d’annulation de publication.</span><span class="sxs-lookup"><span data-stu-id="c4c07-173">Indicates that the system is attempting to complete a publish or unpublish operation.</span></span> <span data-ttu-id="c4c07-174">Si un appel [**SetPrinter**](setprinter.md) ne parvient pas à publier ou à annuler la publication d’une imprimante, le système effectue d’autres tentatives pour terminer l’opération en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="c4c07-174">If a [**SetPrinter**](setprinter.md) call fails to publish or unpublish a printer, the system makes further attempts to complete the operation in the background.</span></span> |



 

<span data-ttu-id="c4c07-175">À compter de Windows Vista, les données d’imprimante retournées par **GetPrinter** sont récupérées à partir d’un cache local lorsque *hPrinter* fait référence à une imprimante hébergée par un serveur d’impression et qu’il y a au moins une connexion ouverte au serveur d’impression.</span><span class="sxs-lookup"><span data-stu-id="c4c07-175">Starting with Windows Vista, the printer data returned by **GetPrinter** is retrieved from a local cache when *hPrinter* refers to a printer hosted by a print server and there is at least one open connection to the print server.</span></span> <span data-ttu-id="c4c07-176">Dans toutes les autres configurations, les données de l’imprimante sont interrogées à partir du serveur d’impression.</span><span class="sxs-lookup"><span data-stu-id="c4c07-176">In all other configurations, the printer data is queried from the print server.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4c07-177">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c4c07-177">Requirements</span></span>



| <span data-ttu-id="c4c07-178">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c4c07-178">Requirement</span></span> | <span data-ttu-id="c4c07-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4c07-179">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4c07-180">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4c07-180">Minimum supported client</span></span><br/> | <span data-ttu-id="c4c07-181">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c4c07-181">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c4c07-182">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4c07-182">Minimum supported server</span></span><br/> | <span data-ttu-id="c4c07-183">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c4c07-183">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c4c07-184">En-tête</span><span class="sxs-lookup"><span data-stu-id="c4c07-184">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4c07-185"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c4c07-185"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="c4c07-186">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c4c07-186">Library</span></span><br/>                  | <dl> <span data-ttu-id="c4c07-187"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c4c07-187"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="c4c07-188">DLL</span><span class="sxs-lookup"><span data-stu-id="c4c07-188">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4c07-189"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="c4c07-189"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="c4c07-190">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="c4c07-190">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c4c07-191">**GetPrinterW** (Unicode) et **GetPrinterA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="c4c07-191">**GetPrinterW** (Unicode) and **GetPrinterA** (ANSI)</span></span><br/>                                           |



## <a name="see-also"></a><span data-ttu-id="c4c07-192">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4c07-192">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4c07-193">Impression</span><span class="sxs-lookup"><span data-stu-id="c4c07-193">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="c4c07-194">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="c4c07-194">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="c4c07-195">**AbortPrinter**</span><span class="sxs-lookup"><span data-stu-id="c4c07-195">**AbortPrinter**</span></span>](abortprinter.md)
</dt> <dt>

[<span data-ttu-id="c4c07-196">**AddPrinter**</span><span class="sxs-lookup"><span data-stu-id="c4c07-196">**AddPrinter**</span></span>](addprinter.md)
</dt> <dt>

[<span data-ttu-id="c4c07-197">**ClosePrinter**</span><span class="sxs-lookup"><span data-stu-id="c4c07-197">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="c4c07-198">**DeletePrinter**</span><span class="sxs-lookup"><span data-stu-id="c4c07-198">**DeletePrinter**</span></span>](deleteprinter.md)
</dt> <dt>

[<span data-ttu-id="c4c07-199">**EnumPrinters**</span><span class="sxs-lookup"><span data-stu-id="c4c07-199">**EnumPrinters**</span></span>](enumprinters.md)
</dt> <dt>

[<span data-ttu-id="c4c07-200">**\_Infos sur l’imprimante \_ 1**</span><span class="sxs-lookup"><span data-stu-id="c4c07-200">**PRINTER\_INFO\_1**</span></span>](printer-info-1.md)
</dt> <dt>

[<span data-ttu-id="c4c07-201">**\_Infos sur l’imprimante \_ 2**</span><span class="sxs-lookup"><span data-stu-id="c4c07-201">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="c4c07-202">**\_Infos sur l’imprimante \_ 3**</span><span class="sxs-lookup"><span data-stu-id="c4c07-202">**PRINTER\_INFO\_3**</span></span>](printer-info-3.md)
</dt> <dt>

[<span data-ttu-id="c4c07-203">**\_Infos sur l’imprimante \_ 4**</span><span class="sxs-lookup"><span data-stu-id="c4c07-203">**PRINTER\_INFO\_4**</span></span>](printer-info-4.md)
</dt> <dt>

[<span data-ttu-id="c4c07-204">**\_Infos sur l’imprimante \_ 5**</span><span class="sxs-lookup"><span data-stu-id="c4c07-204">**PRINTER\_INFO\_5**</span></span>](printer-info-5.md)
</dt> <dt>

[<span data-ttu-id="c4c07-205">**\_Infos sur l’imprimante \_ 7**</span><span class="sxs-lookup"><span data-stu-id="c4c07-205">**PRINTER\_INFO\_7**</span></span>](printer-info-7.md)
</dt> <dt>

[<span data-ttu-id="c4c07-206">**\_Infos sur l’imprimante \_ 8**</span><span class="sxs-lookup"><span data-stu-id="c4c07-206">**PRINTER\_INFO\_8**</span></span>](printer-info-8.md)
</dt> <dt>

[<span data-ttu-id="c4c07-207">**\_Infos sur l’imprimante \_ 9**</span><span class="sxs-lookup"><span data-stu-id="c4c07-207">**PRINTER\_INFO\_9**</span></span>](printer-info-9.md)
</dt> <dt>

[<span data-ttu-id="c4c07-208">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="c4c07-208">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="c4c07-209">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="c4c07-209">**SetPrinter**</span></span>](setprinter.md)
</dt> </dl>

 

 




