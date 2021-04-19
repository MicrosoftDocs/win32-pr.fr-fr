---
description: La fonction SetPrinter définit les données pour une imprimante spécifiée ou définit l’état de l’imprimante spécifiée en interrompant l’impression, en reprenant l’impression ou en effaçant tous les travaux d’impression.
ms.assetid: ade367c5-20d6-4da9-bb52-ce6768cf7537
title: SetPrinter, fonction (WinSpool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetPrinter
- SetPrinterA
- SetPrinterW
api_type:
- DllExport
api_location:
- WinSpool.drv
- Ext-MS-Win-printer-WinSpool-l1-1-0.dll
- Ext-MS-Win-printer-WinSpool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 5f2c58d97315ff108c8f12bd029849993a307025
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536506"
---
# <a name="setprinter-function"></a><span data-ttu-id="53986-103">SetPrinter fonction)</span><span class="sxs-lookup"><span data-stu-id="53986-103">SetPrinter function</span></span>

<span data-ttu-id="53986-104">La fonction **SetPrinter** définit les données pour une imprimante spécifiée ou définit l’état de l’imprimante spécifiée en interrompant l’impression, en reprenant l’impression ou en effaçant tous les travaux d’impression.</span><span class="sxs-lookup"><span data-stu-id="53986-104">The **SetPrinter** function sets the data for a specified printer or sets the state of the specified printer by pausing printing, resuming printing, or clearing all print jobs.</span></span>

## <a name="syntax"></a><span data-ttu-id="53986-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="53986-105">Syntax</span></span>


```C++
BOOL SetPrinter(
  _In_ HANDLE hPrinter,
  _In_ DWORD  Level,
  _In_ LPBYTE pPrinter,
  _In_ DWORD  Command
);
```



## <a name="parameters"></a><span data-ttu-id="53986-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="53986-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53986-107">*hPrinter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="53986-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53986-108">Handle vers l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="53986-108">A handle to the printer.</span></span> <span data-ttu-id="53986-109">Utilisez la fonction [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md)ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="53986-109">Use the [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md), or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="53986-110">De *niveau* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="53986-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53986-111">Type de données que la fonction stocke dans la mémoire tampon vers laquelle pointe *pPrinter*.</span><span class="sxs-lookup"><span data-stu-id="53986-111">The type of data that the function stores into the buffer pointed to by *pPrinter*.</span></span> <span data-ttu-id="53986-112">Si le paramètre de *commande* n’est pas égal à zéro, le paramètre de *niveau* doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="53986-112">If the *Command* parameter is not equal to zero, the *Level* parameter must be zero.</span></span>

<span data-ttu-id="53986-113">Cette valeur peut être 0, 2, 3, 4, 5, 6, 7, 8 ou 9.</span><span class="sxs-lookup"><span data-stu-id="53986-113">This value can be 0, 2, 3, 4, 5, 6, 7, 8, or 9.</span></span>

</dd> <dt>

<span data-ttu-id="53986-114">*pPrinter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="53986-114">*pPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53986-115">Pointeur vers une mémoire tampon qui contient les données à définir pour l’imprimante, ou contenant des informations pour la commande spécifiée par le paramètre de *commande* .</span><span class="sxs-lookup"><span data-stu-id="53986-115">A pointer to a buffer containing data to set for the printer, or containing information for the command specified by the *Command* parameter.</span></span> <span data-ttu-id="53986-116">Le type de données dans la mémoire tampon est déterminé par la valeur de *Level*.</span><span class="sxs-lookup"><span data-stu-id="53986-116">The type of data in the buffer is determined by the value of *Level*.</span></span>



| <span data-ttu-id="53986-117">Level</span><span class="sxs-lookup"><span data-stu-id="53986-117">Level</span></span>                                                                                                | <span data-ttu-id="53986-118">Structure</span><span class="sxs-lookup"><span data-stu-id="53986-118">Structure</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="53986-119"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="53986-119"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="53986-120">Si le paramètre de *commande* est défini sur l' **\_ \_ \_ État du contrôle d’imprimante**, *pPrinter* doit contenir une valeur **DWORD** qui spécifie le nouvel état de l’imprimante à définir.</span><span class="sxs-lookup"><span data-stu-id="53986-120">If the *Command* parameter is **PRINTER\_CONTROL\_SET\_STATUS**, *pPrinter* must contain a **DWORD** value that specifies the new printer status to set.</span></span> <span data-ttu-id="53986-121">Pour obtenir la liste des valeurs d’État possibles, consultez le membre **Status** de la structure [**Printer \_ info \_ 2**](printer-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="53986-121">For a list of the possible status values, see the **Status** member of the [**PRINTER\_INFO\_2**](printer-info-2.md) structure.</span></span> <span data-ttu-id="53986-122">Notez que l’état de l' **imprimante est \_ \_ suspendu** et que la **\_ \_ \_ suppression** de l’état de l’imprimante n’est pas une valeur d’état valide à définir.</span><span class="sxs-lookup"><span data-stu-id="53986-122">Note that **PRINTER\_STATUS\_PAUSED** and **PRINTER\_STATUS\_PENDING\_DELETION** are not valid status values to set.</span></span><br/> <span data-ttu-id="53986-123">Si le *niveau* est 0, mais que le paramètre de *commande* n’est pas l'  État du jeu de contrôle d’imprimante, pPrinter doit avoir la **valeur null**. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="53986-123">If *Level* is 0, but the *Command* parameter is not **PRINTER\_CONTROL\_SET\_STATUS**, *pPrinter* must be **NULL**.</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="53986-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="53986-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="53986-125">Structure de l' [**imprimante \_ info \_ 2**](printer-info-2.md) contenant des informations détaillées sur l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="53986-125">A [**PRINTER\_INFO\_2**](printer-info-2.md) structure containing detailed information about the printer.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="3"></span><dl> <span data-ttu-id="53986-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="53986-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="53986-127">Une structure [**Printer \_ info \_ 3**](printer-info-3.md) contenant les informations de sécurité de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="53986-127">A [**PRINTER\_INFO\_3**](printer-info-3.md) structure containing the printer's security information.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="4"></span><dl> <span data-ttu-id="53986-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="53986-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="53986-129">Une structure [**Printer \_ info \_ 4**](printer-info-4.md) contenant des informations d’imprimante minimales, y compris le nom de l’imprimante, le nom du serveur et si l’imprimante est distante ou locale.</span><span class="sxs-lookup"><span data-stu-id="53986-129">A [**PRINTER\_INFO\_4**](printer-info-4.md) structure containing minimal printer information, including the name of the printer, the name of the server, and whether the printer is remote or local.</span></span><br/>                                                                                                                                                                                                                                                                                                                                         |
| <span id="5"></span><dl> <span data-ttu-id="53986-130"><dt>**5**</dt></span><span class="sxs-lookup"><span data-stu-id="53986-130"><dt>**5**</dt></span></span> </dl> | <span data-ttu-id="53986-131">Une structure [**Printer \_ info \_ 5**](printer-info-5.md) contenant des informations sur l’imprimante, telles que des attributs d’imprimante et des paramètres de délai d’attente.</span><span class="sxs-lookup"><span data-stu-id="53986-131">A [**PRINTER\_INFO\_5**](printer-info-5.md) structure containing printer information such as printer attributes and time-out settings.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="6"></span><dl> <span data-ttu-id="53986-132"><dt>**6**</dt></span><span class="sxs-lookup"><span data-stu-id="53986-132"><dt>**6**</dt></span></span> </dl> | <span data-ttu-id="53986-133">Une structure [**Printer \_ info \_ 6**](printer-info-6.md) spécifiant la valeur d’état d’une imprimante.</span><span class="sxs-lookup"><span data-stu-id="53986-133">A [**PRINTER\_INFO\_6**](printer-info-6.md) structure specifying the status value of a printer.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="7"></span><dl> <span data-ttu-id="53986-134"><dt>**7**</dt></span><span class="sxs-lookup"><span data-stu-id="53986-134"><dt>**7**</dt></span></span> </dl> | <span data-ttu-id="53986-135">Structure de l' [**imprimante \_ info \_ 7**](printer-info-7.md) .</span><span class="sxs-lookup"><span data-stu-id="53986-135">A [**PRINTER\_INFO\_7**](printer-info-7.md) structure.</span></span> <span data-ttu-id="53986-136">Le membre *dwAction* de cette structure indique si **SetPrinter** doit publier, annuler la publication, publier à nouveau ou mettre à jour les données de l’imprimante dans le service d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="53986-136">The *dwAction* member of this structure indicates whether **SetPrinter** should publish, unpublish, re-publish, or update the printer's data in the directory service.</span></span><br/>                                                                                                                                                                                                                                                                                                                |
| <span id="8"></span><dl> <span data-ttu-id="53986-137"><dt>**8**</dt></span><span class="sxs-lookup"><span data-stu-id="53986-137"><dt>**8**</dt></span></span> </dl> | <span data-ttu-id="53986-138">Structure [**d' \_ informations \_ d’imprimante 8**](printer-info-8.md) spécifiant les paramètres d’imprimante par défaut globaux.</span><span class="sxs-lookup"><span data-stu-id="53986-138">A [**PRINTER\_INFO\_8**](printer-info-8.md) structure specifying the global default printer settings.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="9"></span><dl> <span data-ttu-id="53986-139"><dt>**9**</dt></span><span class="sxs-lookup"><span data-stu-id="53986-139"><dt>**9**</dt></span></span> </dl> | <span data-ttu-id="53986-140">Une structure d' [**informations d’imprimante \_ \_ 9**](printer-info-9.md) spécifiant les paramètres d’imprimante par défaut par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="53986-140">A [**PRINTER\_INFO\_9**](printer-info-9.md) structure specifying the per-user default printer settings.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

<span data-ttu-id="53986-141">*Commande* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="53986-141">*Command* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53986-142">l’action à effectuer.</span><span class="sxs-lookup"><span data-stu-id="53986-142">The action to perform.</span></span>

<span data-ttu-id="53986-143">Si le paramètre de *niveau* est différent de zéro, définissez la valeur de ce paramètre sur zéro.</span><span class="sxs-lookup"><span data-stu-id="53986-143">If the *Level* parameter is nonzero, set the value of this parameter to zero.</span></span> <span data-ttu-id="53986-144">Dans ce cas, l’imprimante conserve son état actuel et la fonction reconfigure les données de l’imprimante, comme spécifié par les paramètres *Level* et *pPrinter* .</span><span class="sxs-lookup"><span data-stu-id="53986-144">In this case, the printer retains its current state and the function reconfigures the printer data as specified by the *Level* and *pPrinter* parameters.</span></span>

<span data-ttu-id="53986-145">Si le paramètre de *niveau* est égal à zéro, définissez la valeur de ce paramètre sur l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="53986-145">If the *Level* parameter is zero, set the value of this parameter to one of the following values.</span></span>



| <span data-ttu-id="53986-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="53986-146">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="53986-147">Signification</span><span class="sxs-lookup"><span data-stu-id="53986-147">Meaning</span></span>                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PRINTER_CONTROL_PAUSE"></span><span id="printer_control_pause"></span><dl> <span data-ttu-id="53986-148"><dt>**\_pause de contrôle de l’imprimante \_**</dt></span><span class="sxs-lookup"><span data-stu-id="53986-148"><dt>**PRINTER\_CONTROL\_PAUSE**</dt></span></span> </dl>                 | <span data-ttu-id="53986-149">Suspendez l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="53986-149">Pause the printer.</span></span><br/>                                                                                                                       |
| <span id="PRINTER_CONTROL_PURGE"></span><span id="printer_control_purge"></span><dl> <span data-ttu-id="53986-150"><dt>**\_purge du contrôle de l’imprimante \_**</dt></span><span class="sxs-lookup"><span data-stu-id="53986-150"><dt>**PRINTER\_CONTROL\_PURGE**</dt></span></span> </dl>                 | <span data-ttu-id="53986-151">Supprimer tous les travaux d’impression dans l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="53986-151">Delete all print jobs in the printer.</span></span><br/>                                                                                                    |
| <span id="PRINTER_CONTROL_RESUME"></span><span id="printer_control_resume"></span><dl> <span data-ttu-id="53986-152"><dt>**\_reprise du contrôle de l’imprimante \_**</dt></span><span class="sxs-lookup"><span data-stu-id="53986-152"><dt>**PRINTER\_CONTROL\_RESUME**</dt></span></span> </dl>              | <span data-ttu-id="53986-153">Reprendre une imprimante suspendue.</span><span class="sxs-lookup"><span data-stu-id="53986-153">Resume a paused printer.</span></span><br/>                                                                                                                 |
| <span id="PRINTER_CONTROL_SET_STATUS"></span><span id="printer_control_set_status"></span><dl> <span data-ttu-id="53986-154"><dt>**\_État du \_ jeu de contrôle d’imprimante \_**</dt></span><span class="sxs-lookup"><span data-stu-id="53986-154"><dt>**PRINTER\_CONTROL\_SET\_STATUS**</dt></span></span> </dl> | <span data-ttu-id="53986-155">Définissez l’état de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="53986-155">Set the printer status.</span></span><br/> <span data-ttu-id="53986-156">Définissez le paramètre *pPrinter* sur un pointeur désignant une valeur **DWORD** qui spécifie le nouvel état de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="53986-156">Set the *pPrinter* parameter to a pointer to a **DWORD** value that specifies the new printer status.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53986-157">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="53986-157">Return value</span></span>

<span data-ttu-id="53986-158">Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="53986-158">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="53986-159">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="53986-159">If the function fails, the return value is zero.</span></span>

<span data-ttu-id="53986-160">Si *Level* a la valeur 7 et que l’action de publication a échoué, **SetPrinter** retourne des **\_ e/s d’erreur \_ en attente** et tente de terminer l’action en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="53986-160">If *Level* is 7 and the publish action failed, **SetPrinter** returns **ERROR\_IO\_PENDING** and attempts to complete the action in the background.</span></span> <span data-ttu-id="53986-161">Si le *niveau* est 7 et que l’action de mise à jour a échoué, **SetPrinter** retourne le **fichier d’erreur \_ \_ \_ introuvable**.</span><span class="sxs-lookup"><span data-stu-id="53986-161">If *Level* is 7 and the update action failed, **SetPrinter** returns **ERROR\_FILE\_NOT\_FOUND**.</span></span>

## <a name="remarks"></a><span data-ttu-id="53986-162">Notes</span><span class="sxs-lookup"><span data-stu-id="53986-162">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="53986-163">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="53986-163">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="53986-164">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="53986-164">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="53986-165">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="53986-165">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="53986-166">Vous ne pouvez pas utiliser **SetPrinter** pour modifier l’imprimante par défaut.</span><span class="sxs-lookup"><span data-stu-id="53986-166">You cannot use **SetPrinter** to change the default printer.</span></span>

<span data-ttu-id="53986-167">Pour modifier les paramètres actuels de l’imprimante, appelez la fonction [**GetPrinter**](getprinter.md) pour récupérer les paramètres actuels dans une structure [**\_ info \_ 2**](printer-info-2.md) de l’imprimante, modifiez les membres de cette structure si nécessaire, puis appelez **SetPrinter**.</span><span class="sxs-lookup"><span data-stu-id="53986-167">To modify the current printer settings, call the [**GetPrinter**](getprinter.md) function to retrieve the current settings into a [**PRINTER\_INFO\_2**](printer-info-2.md) structure, modify the members of that structure as necessary, and then call **SetPrinter**.</span></span>

<span data-ttu-id="53986-168">La **fonction SetPrinter** ignore les membres **pServerName**, **AveragePPM**, **Status** et **cJobs** d’une structure [**Printer \_ info \_ 2**](printer-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="53986-168">The **SetPrinter** function ignores the **pServerName**, **AveragePPM**, **Status**, and **cJobs** members of a [**PRINTER\_INFO\_2**](printer-info-2.md) structure.</span></span>

<span data-ttu-id="53986-169">La suspension d’une imprimante interrompt la planification de tous les travaux d’impression pour cette imprimante, à l’exception du travail d’impression qui peut être en cours d’impression.</span><span class="sxs-lookup"><span data-stu-id="53986-169">Pausing a printer suspends scheduling of all print jobs for that printer, except for the one print job that may be currently printing.</span></span> <span data-ttu-id="53986-170">Les travaux d’impression peuvent être envoyés à une imprimante suspendue, mais aucun travail n’est planifié pour être imprimé sur cette imprimante tant que l’impression n’est pas reprise.</span><span class="sxs-lookup"><span data-stu-id="53986-170">Print jobs can be submitted to a paused printer, but no jobs will be scheduled to print on that printer until printing is resumed.</span></span> <span data-ttu-id="53986-171">Si une imprimante est désactivée, tous les travaux d’impression de cette imprimante sont supprimés, à l’exception du travail d’impression en cours.</span><span class="sxs-lookup"><span data-stu-id="53986-171">If a printer is cleared, all print jobs for that printer are deleted, except for the current print job.</span></span>

<span data-ttu-id="53986-172">Si vous utilisez **SetPrinter** pour modifier la structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) par défaut d’une imprimante (en définissant globalement les valeurs par défaut de l’imprimante), vous devez d’abord appeler la fonction [**DocumentProperties**](documentproperties.md) pour valider la structure **DEVMODE** .</span><span class="sxs-lookup"><span data-stu-id="53986-172">If you use **SetPrinter** to modify the default [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure for a printer (globally setting the printer defaults), you must first call the [**DocumentProperties**](documentproperties.md) function to validate the **DEVMODE** structure.</span></span>

<span data-ttu-id="53986-173">Pour les structures [**Printer \_ info \_ 2**](printer-info-2.md) et [**Printer \_ info \_ 3**](printer-info-3.md) qui contiennent un pointeur vers un descripteur de sécurité, la fonction ne peut définir que les composants du descripteur de sécurité que l’appelant est autorisé à modifier.</span><span class="sxs-lookup"><span data-stu-id="53986-173">For the [**PRINTER\_INFO\_2**](printer-info-2.md) and [**PRINTER\_INFO\_3**](printer-info-3.md) structures that contain a pointer to a security descriptor, the function can set only those components of the security descriptor that the caller has permission to modify.</span></span> <span data-ttu-id="53986-174">Pour définir des composants de descripteur de sécurité particuliers, vous devez spécifier les droits d’accès nécessaires lorsque vous appelez la fonction [**OpenPrinter**](openprinter.md) ou [**OpenPrinter2**](openprinter2.md) pour récupérer un handle vers l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="53986-174">To set particular security descriptor components, you must specify the necessary access rights when you call the [**OpenPrinter**](openprinter.md) or [**OpenPrinter2**](openprinter2.md) function to retrieve a handle to the printer.</span></span> <span data-ttu-id="53986-175">Le tableau suivant présente les droits d’accès requis pour modifier les différents composants du descripteur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="53986-175">The following table shows the access rights required to modify the various security descriptor components.</span></span>



| <span data-ttu-id="53986-176">Autorisation d’accès</span><span class="sxs-lookup"><span data-stu-id="53986-176">Access permission</span></span>            | <span data-ttu-id="53986-177">Composant descripteur de sécurité</span><span class="sxs-lookup"><span data-stu-id="53986-177">Security descriptor component</span></span>             |
|------------------------------|-------------------------------------------|
| <span data-ttu-id="53986-178">**propriétaire en écriture \_**</span><span class="sxs-lookup"><span data-stu-id="53986-178">**WRITE\_OWNER**</span></span>             | <span data-ttu-id="53986-179">Propriétaire</span><span class="sxs-lookup"><span data-stu-id="53986-179">Owner</span></span><br/> <span data-ttu-id="53986-180">Groupe principal</span><span class="sxs-lookup"><span data-stu-id="53986-180">Primary group</span></span><br/> |
| <span data-ttu-id="53986-181">**ÉCRITURE \_ DAC**</span><span class="sxs-lookup"><span data-stu-id="53986-181">**WRITE\_DAC**</span></span>               | <span data-ttu-id="53986-182">Liste de contrôle d’accès discrétionnaire (DACL)</span><span class="sxs-lookup"><span data-stu-id="53986-182">Discretionary access-control list (DACL)</span></span>  |
| <span data-ttu-id="53986-183">**ACCÉDER à la \_ sécurité du système \_**</span><span class="sxs-lookup"><span data-stu-id="53986-183">**ACCESS\_SYSTEM\_SECURITY**</span></span> | <span data-ttu-id="53986-184">Liste de contrôle d’accès système (SACL)</span><span class="sxs-lookup"><span data-stu-id="53986-184">System access-control list (SACL)</span></span>         |



 

<span data-ttu-id="53986-185">Si le descripteur de sécurité contient un composant pour lequel l’appelant n’a pas le droit d’accès à modifier, **SetPrinter** échoue.</span><span class="sxs-lookup"><span data-stu-id="53986-185">If the security descriptor contains a component that the caller does not have the access right to modify, **SetPrinter** fails.</span></span> <span data-ttu-id="53986-186">Les composants d’un descripteur de sécurité que vous ne souhaitez pas modifier doivent être **null** ou ne pas être présents, selon le cas.</span><span class="sxs-lookup"><span data-stu-id="53986-186">Those components of a security descriptor that you don't want to modify should be **NULL** or not be present, as appropriate.</span></span> <span data-ttu-id="53986-187">Si vous ne souhaitez pas modifier le descripteur de sécurité et que vous appelez **SetPrinter** avec une structure [**Printer \_ info \_ 2**](printer-info-2.md) , affectez la **valeur null** au membre **pSecurityDescriptor** de cette structure.</span><span class="sxs-lookup"><span data-stu-id="53986-187">If you do not want to modify the security descriptor, and are calling **SetPrinter** with a [**PRINTER\_INFO\_2**](printer-info-2.md) structure, set the **pSecurityDescriptor** member of that structure to **NULL**.</span></span>

<span data-ttu-id="53986-188">Le pare-feu de connexion Internet (ICF) bloque les ports d’imprimante par défaut, mais une exception pour le partage de fichiers et d’imprimantes peut être activée.</span><span class="sxs-lookup"><span data-stu-id="53986-188">The Internet Connection Firewall (ICF) blocks printer ports by default, but an exception for File and Print Sharing can be enabled.</span></span> <span data-ttu-id="53986-189">Si **SetPrinter** est appelé par un administrateur d’ordinateur, il active l’exception.</span><span class="sxs-lookup"><span data-stu-id="53986-189">If **SetPrinter** is called by a machine admin, it enables the exception.</span></span> <span data-ttu-id="53986-190">S’il est appelé par un non-administrateur et que l’exception n’a pas déjà été activée, l’appel échoue.</span><span class="sxs-lookup"><span data-stu-id="53986-190">If it is called by a non-admin and the exception has not already been enabled, the call fails.</span></span>

<span data-ttu-id="53986-191">Vous pouvez utiliser le niveau 7 avec la structure de l' [**imprimante \_ info \_ 7**](printer-info-7.md) pour publier, annuler la publication ou mettre à jour les données du service d’annuaire pour l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="53986-191">You can use level 7 with the [**PRINTER\_INFO\_7**](printer-info-7.md) structure to publish, unpublish, or update directory service data for the printer.</span></span> <span data-ttu-id="53986-192">Les données du service d’annuaire pour une imprimante incluent toutes les données stockées sous les \_ \* clés SPLDS par des appels à la fonction [**SetPrinterDataEx**](setprinterdataex.md) pour l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="53986-192">The directory service data for a printer includes all the data stored under the SPLDS\_\* keys by calls to the [**SetPrinterDataEx**](setprinterdataex.md) function for the printer.</span></span> <span data-ttu-id="53986-193">Avant d’appeler **SetPrinter**, définissez le membre **pszObjectGUID** de **Printer \_ info \_ 7** sur **null** et définissez le membre *dwAction* sur l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="53986-193">Before calling **SetPrinter**, set the **pszObjectGUID** member of **PRINTER\_INFO\_7** to **NULL** and set the *dwAction* member to one of the following values.</span></span>



| <span data-ttu-id="53986-194">Valeur</span><span class="sxs-lookup"><span data-stu-id="53986-194">Value</span></span>                             | <span data-ttu-id="53986-195">Description</span><span class="sxs-lookup"><span data-stu-id="53986-195">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53986-196">**\_publication DSPRINT**</span><span class="sxs-lookup"><span data-stu-id="53986-196">**DSPRINT\_PUBLISH**</span></span><br/>   | <span data-ttu-id="53986-197">Publie les données du service d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="53986-197">Publishes the directory service data.</span></span><br/>                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="53986-198">**\_REpublication DSPRINT**</span><span class="sxs-lookup"><span data-stu-id="53986-198">**DSPRINT\_REPUBLISH**</span></span><br/> | <span data-ttu-id="53986-199">Les données du service d’annuaire pour l’imprimante ne sont pas publiées, puis publiées à nouveau, ce qui a pour actualiser toutes les propriétés de l’imprimante publiée.</span><span class="sxs-lookup"><span data-stu-id="53986-199">The directory service data for the printer is unpublished and then published again, refreshing all properties in the published printer.</span></span> <span data-ttu-id="53986-200">La republication modifie également le GUID de l’imprimante publiée.</span><span class="sxs-lookup"><span data-stu-id="53986-200">Re-publishing also changes the GUID of the published printer.</span></span> <span data-ttu-id="53986-201">Utilisez cette valeur si vous pensez que les données publiées de l’imprimante ont été endommagées.</span><span class="sxs-lookup"><span data-stu-id="53986-201">Use this value if you suspect the printer's published data has been corrupted.</span></span><br/>                                                                                         |
| <span data-ttu-id="53986-202">**DSPRINT \_ annuler la publication**</span><span class="sxs-lookup"><span data-stu-id="53986-202">**DSPRINT\_UNPUBLISH**</span></span><br/> | <span data-ttu-id="53986-203">Annule la publication des données du service d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="53986-203">Unpublishes the directory service data.</span></span><br/>                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="53986-204">**\_mise à jour DSPRINT**</span><span class="sxs-lookup"><span data-stu-id="53986-204">**DSPRINT\_UPDATE**</span></span><br/>    | <span data-ttu-id="53986-205">Met à jour les données du service d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="53986-205">Updates the directory service data.</span></span> <span data-ttu-id="53986-206">C’est identique à la **\_ publication DSPRINT**, à ceci près que **SetPrinter** échoue avec un **fichier d’erreur \_ \_ \_ introuvable** si l’imprimante n’est pas encore publiée.</span><span class="sxs-lookup"><span data-stu-id="53986-206">This is the same as **DSPRINT\_PUBLISH**, except that **SetPrinter** fails with **ERROR\_FILE\_NOT\_FOUND** if the printer is not already published.</span></span><br/> <span data-ttu-id="53986-207">Utilisez **DSPRINT \_ Update** pour mettre à jour les propriétés publiées, mais ne forcez pas la publication.</span><span class="sxs-lookup"><span data-stu-id="53986-207">Use **DSPRINT\_UPDATE** to update published properties but not force publishing.</span></span> <span data-ttu-id="53986-208">Les pilotes d’imprimante doivent toujours utiliser la **\_ mise à jour DSPRINT** plutôt que la **\_ publication DSPRINT**.</span><span class="sxs-lookup"><span data-stu-id="53986-208">Printer drivers should always use **DSPRINT\_UPDATE** rather than **DSPRINT\_PUBLISH**.</span></span><br/> |



 

<span data-ttu-id="53986-209">**DSPRINT \_ L’instance en attente** n’est pas une valeur *dwAction* valide pour **SetPrinter**.</span><span class="sxs-lookup"><span data-stu-id="53986-209">**DSPRINT\_PENDING** is not a valid *dwAction* value for **SetPrinter**.</span></span>

## <a name="requirements"></a><span data-ttu-id="53986-210">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="53986-210">Requirements</span></span>



| <span data-ttu-id="53986-211">Condition requise</span><span class="sxs-lookup"><span data-stu-id="53986-211">Requirement</span></span> | <span data-ttu-id="53986-212">Valeur</span><span class="sxs-lookup"><span data-stu-id="53986-212">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53986-213">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53986-213">Minimum supported client</span></span><br/> | <span data-ttu-id="53986-214">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="53986-214">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="53986-215">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53986-215">Minimum supported server</span></span><br/> | <span data-ttu-id="53986-216">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="53986-216">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="53986-217">En-tête</span><span class="sxs-lookup"><span data-stu-id="53986-217">Header</span></span><br/>                   | <dl> <span data-ttu-id="53986-218"><dt>WinSpool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="53986-218"><dt>WinSpool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="53986-219">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="53986-219">Library</span></span><br/>                  | <dl> <span data-ttu-id="53986-220"><dt>WinSpool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="53986-220"><dt>WinSpool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="53986-221">DLL</span><span class="sxs-lookup"><span data-stu-id="53986-221">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53986-222"><dt>WinSpool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="53986-222"><dt>WinSpool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="53986-223">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="53986-223">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="53986-224">**SetPrinterW** (Unicode) et **SetPrinterA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="53986-224">**SetPrinterW** (Unicode) and **SetPrinterA** (ANSI)</span></span><br/>                                           |



## <a name="see-also"></a><span data-ttu-id="53986-225">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53986-225">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53986-226">Impression</span><span class="sxs-lookup"><span data-stu-id="53986-226">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="53986-227">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="53986-227">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="53986-228">**AddPrinter**</span><span class="sxs-lookup"><span data-stu-id="53986-228">**AddPrinter**</span></span>](addprinter.md)
</dt> <dt>

[<span data-ttu-id="53986-229">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="53986-229">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="53986-230">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="53986-230">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="53986-231">**OpenPrinter2**</span><span class="sxs-lookup"><span data-stu-id="53986-231">**OpenPrinter2**</span></span>](openprinter2.md)
</dt> <dt>

[<span data-ttu-id="53986-232">**\_Infos sur l’imprimante \_ 2**</span><span class="sxs-lookup"><span data-stu-id="53986-232">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="53986-233">**\_Infos sur l’imprimante \_ 3**</span><span class="sxs-lookup"><span data-stu-id="53986-233">**PRINTER\_INFO\_3**</span></span>](printer-info-3.md)
</dt> <dt>

[<span data-ttu-id="53986-234">**\_Infos sur l’imprimante \_ 4**</span><span class="sxs-lookup"><span data-stu-id="53986-234">**PRINTER\_INFO\_4**</span></span>](printer-info-4.md)
</dt> <dt>

[<span data-ttu-id="53986-235">**\_Infos sur l’imprimante \_ 5**</span><span class="sxs-lookup"><span data-stu-id="53986-235">**PRINTER\_INFO\_5**</span></span>](printer-info-5.md)
</dt> <dt>

[<span data-ttu-id="53986-236">**\_Infos sur l’imprimante \_ 6**</span><span class="sxs-lookup"><span data-stu-id="53986-236">**PRINTER\_INFO\_6**</span></span>](printer-info-6.md)
</dt> <dt>

[<span data-ttu-id="53986-237">**\_Infos sur l’imprimante \_ 7**</span><span class="sxs-lookup"><span data-stu-id="53986-237">**PRINTER\_INFO\_7**</span></span>](printer-info-7.md)
</dt> <dt>

[<span data-ttu-id="53986-238">**\_Infos sur l’imprimante \_ 8**</span><span class="sxs-lookup"><span data-stu-id="53986-238">**PRINTER\_INFO\_8**</span></span>](printer-info-8.md)
</dt> <dt>

[<span data-ttu-id="53986-239">**\_Infos sur l’imprimante \_ 9**</span><span class="sxs-lookup"><span data-stu-id="53986-239">**PRINTER\_INFO\_9**</span></span>](printer-info-9.md)
</dt> <dt>

[<span data-ttu-id="53986-240">**SetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="53986-240">**SetPrinterDataEx**</span></span>](setprinterdataex.md)
</dt> </dl>

 

 




