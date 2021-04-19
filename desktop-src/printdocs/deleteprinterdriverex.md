---
description: La fonction DeletePrinterDriverEx supprime le nom du pilote d’imprimante spécifié de la liste des noms des pilotes pris en charge sur un serveur et supprime les fichiers associés au pilote. Cette fonction peut également supprimer des versions spécifiques du pilote.
ms.assetid: 1a3d7c7f-1d45-4877-a8f7-a77f40e3c319
title: DeletePrinterDriverEx, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterDriverEx
- DeletePrinterDriverExA
- DeletePrinterDriverExW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: b88ef38236961286875a1885dad9dde936887d13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527648"
---
# <a name="deleteprinterdriverex-function"></a><span data-ttu-id="416b2-104">DeletePrinterDriverEx fonction)</span><span class="sxs-lookup"><span data-stu-id="416b2-104">DeletePrinterDriverEx function</span></span>

<span data-ttu-id="416b2-105">La fonction **DeletePrinterDriverEx** supprime le nom du pilote d’imprimante spécifié de la liste des noms des pilotes pris en charge sur un serveur et supprime les fichiers associés au pilote.</span><span class="sxs-lookup"><span data-stu-id="416b2-105">The **DeletePrinterDriverEx** function removes the specified printer-driver name from the list of names of supported drivers on a server and deletes the files associated with the driver.</span></span> <span data-ttu-id="416b2-106">Cette fonction peut également supprimer des versions spécifiques du pilote.</span><span class="sxs-lookup"><span data-stu-id="416b2-106">This function can also delete specific versions of the driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="416b2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="416b2-107">Syntax</span></span>


```C++
BOOL DeletePrinterDriverEx(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pDriverName,
  _In_ DWORD  dwDeleteFlag,
  _In_ DWORD  dwVersionFlag
);
```



## <a name="parameters"></a><span data-ttu-id="416b2-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="416b2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="416b2-109">*pname* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="416b2-109">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="416b2-110">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du serveur à partir duquel le pilote doit être supprimé.</span><span class="sxs-lookup"><span data-stu-id="416b2-110">A pointer to a null-terminated string that specifies the name of the server from which the driver is to be deleted.</span></span> <span data-ttu-id="416b2-111">Si ce paramètre a la **valeur null**, la fonction supprime le pilote d’imprimante de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="416b2-111">If this parameter is **NULL**, the function deletes the printer-driver from the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="416b2-112">*pEnvironment* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="416b2-112">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="416b2-113">Pointeur vers une chaîne se terminant par un caractère null qui spécifie l’environnement à partir duquel le pilote doit être supprimé (par exemple, Windows NT x86, Windows IA64 ou Windows x64).</span><span class="sxs-lookup"><span data-stu-id="416b2-113">A pointer to a null-terminated string that specifies the environment from which the driver is to be deleted (for example, Windows NT x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="416b2-114">Si ce paramètre a la **valeur null**, le nom du pilote est supprimé de l’environnement actuel de l’application appelante et de l’ordinateur client (et non de l’application de destination et du serveur d’impression).</span><span class="sxs-lookup"><span data-stu-id="416b2-114">If this parameter is **NULL**, the driver name is deleted from the current environment of the calling application and client computer (not of the destination application and print server).</span></span>

</dd> <dt>

<span data-ttu-id="416b2-115">*pDriverName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="416b2-115">*pDriverName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="416b2-116">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du pilote à supprimer.</span><span class="sxs-lookup"><span data-stu-id="416b2-116">A pointer to a null-terminated string specifying the name of the driver to delete.</span></span>

</dd> <dt>

<span data-ttu-id="416b2-117">*dwDeleteFlag* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="416b2-117">*dwDeleteFlag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="416b2-118">Options permettant de supprimer des fichiers et des versions du pilote.</span><span class="sxs-lookup"><span data-stu-id="416b2-118">The options for deleting files and versions of the driver.</span></span> <span data-ttu-id="416b2-119">Ce paramètre peut être une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="416b2-119">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="416b2-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="416b2-120">Value</span></span>                                                                                                                                                                                                     | <span data-ttu-id="416b2-121">Signification</span><span class="sxs-lookup"><span data-stu-id="416b2-121">Meaning</span></span>                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DPD_DELETE_SPECIFIC_VERSION"></span><span id="dpd_delete_specific_version"></span><dl> <span data-ttu-id="416b2-122"><dt>**MORT \_ supprimer \_ une \_ version spécifique**</dt></span><span class="sxs-lookup"><span data-stu-id="416b2-122"><dt>**DPD\_DELETE\_SPECIFIC\_VERSION**</dt></span></span> </dl> | <span data-ttu-id="416b2-123">Supprime la version spécifiée dans *dwVersionFlag*.</span><span class="sxs-lookup"><span data-stu-id="416b2-123">Deletes the version specified in *dwVersionFlag*.</span></span> <span data-ttu-id="416b2-124">Cela ne garantit pas que le pilote sera supprimé de la liste des pilotes pris en charge pour le serveur.</span><span class="sxs-lookup"><span data-stu-id="416b2-124">This does not ensure that the driver will be removed from the list of supported drivers for the server.</span></span><br/>                  |
| <span id="DPD_DELETE_UNUSED_FILES"></span><span id="dpd_delete_unused_files"></span><dl> <span data-ttu-id="416b2-125"><dt>**MORT \_ Supprimer les \_ fichiers inutilisés \_**</dt></span><span class="sxs-lookup"><span data-stu-id="416b2-125"><dt>**DPD\_DELETE\_UNUSED\_FILES**</dt></span></span> </dl>             | <span data-ttu-id="416b2-126">Supprime tous les fichiers de pilote inutilisés.</span><span class="sxs-lookup"><span data-stu-id="416b2-126">Removes any unused driver files.</span></span><br/>                                                                                                                                           |
| <span id="DPD_DELETE_ALL_FILES"></span><span id="dpd_delete_all_files"></span><dl> <span data-ttu-id="416b2-127"><dt>**MORT \_ supprimer \_ tous les \_ fichiers**</dt></span><span class="sxs-lookup"><span data-stu-id="416b2-127"><dt>**DPD\_DELETE\_ALL\_FILES**</dt></span></span> </dl>                      | <span data-ttu-id="416b2-128">Supprime le pilote uniquement si tous ses fichiers associés peuvent être supprimés.</span><span class="sxs-lookup"><span data-stu-id="416b2-128">Deletes the driver only if all its associated files can be removed.</span></span> <span data-ttu-id="416b2-129">L’opération de suppression échoue si l’un des fichiers du pilote est utilisé par un autre pilote installé.</span><span class="sxs-lookup"><span data-stu-id="416b2-129">The delete operation fails if any of the driver's files are being used by some other installed driver.</span></span><br/> |



 

<span data-ttu-id="416b2-130">Si mort \_ supprimer \_ une \_ version spécifique n’est pas spécifié, la fonction supprime toutes les versions du pilote si aucune d’entre elles n’est en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="416b2-130">If DPD\_DELETE\_SPECIFIC\_VERSION is not specified, the function deletes all versions of the driver if none of them is in use.</span></span> <span data-ttu-id="416b2-131">Si ni mort \_ supprimer \_ les fichiers inutilisés \_ , ni mort \_ supprimer \_ tous les \_ fichiers n’est spécifié, la fonction ne supprime pas les fichiers de pilote.</span><span class="sxs-lookup"><span data-stu-id="416b2-131">If neither DPD\_DELETE\_UNUSED\_FILES nor DPD\_DELETE\_ALL\_FILES is specified, the function does not delete driver files.</span></span>

</dd> <dt>

<span data-ttu-id="416b2-132">*dwVersionFlag* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="416b2-132">*dwVersionFlag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="416b2-133">Version du pilote à supprimer.</span><span class="sxs-lookup"><span data-stu-id="416b2-133">The version of the driver to be deleted.</span></span> <span data-ttu-id="416b2-134">Ce paramètre peut avoir la valeur 0, 1, 2 ou 3.</span><span class="sxs-lookup"><span data-stu-id="416b2-134">This parameter can be 0, 1, 2 or 3.</span></span> <span data-ttu-id="416b2-135">Ce paramètre est utilisé uniquement si *dwDeleteFlag* comprend l' \_ indicateur mort supprimer la \_ \_ version spécifique.</span><span class="sxs-lookup"><span data-stu-id="416b2-135">This parameter is used only if *dwDeleteFlag* includes the DPD\_DELETE\_SPECIFIC\_VERSION flag.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="416b2-136">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="416b2-136">Return value</span></span>

<span data-ttu-id="416b2-137">Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="416b2-137">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="416b2-138">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="416b2-138">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="416b2-139">Notes</span><span class="sxs-lookup"><span data-stu-id="416b2-139">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="416b2-140">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="416b2-140">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="416b2-141">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="416b2-141">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="416b2-142">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="416b2-142">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="416b2-143">Avant de supprimer les fichiers de pilote, la fonction appelle la fonction **DrvDriverEvent** du pilote, ce qui permet au pilote de supprimer tous les fichiers privés qui ne sont pas utilisés.</span><span class="sxs-lookup"><span data-stu-id="416b2-143">Before the function deletes the driver files, it calls the driver's **DrvDriverEvent** function, allowing the driver to remove any private files that are not used.</span></span> <span data-ttu-id="416b2-144">Pour plus d’informations sur **DrvDriverEvent**, consultez le kit de développement de pilotes (DDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="416b2-144">For more information about **DrvDriverEvent**, see the Microsoft Windows Driver Development Kit (DDK).</span></span>

<span data-ttu-id="416b2-145">Si les fichiers de pilote sont actuellement chargés, la fonction les déplace vers un répertoire temporaire et les marque pour la suppression au redémarrage.</span><span class="sxs-lookup"><span data-stu-id="416b2-145">If the driver files are currently loaded, the function moves them to a temp directory and marks them for deletion on restart.</span></span>

<span data-ttu-id="416b2-146">Avant d’appeler **DeletePrinterDriverEx**, vous devez supprimer tous les objets d’imprimante qui utilisent le pilote d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="416b2-146">Before calling **DeletePrinterDriverEx**, you must delete all printer objects that use the printer driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="416b2-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="416b2-147">Requirements</span></span>



| <span data-ttu-id="416b2-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="416b2-148">Requirement</span></span> | <span data-ttu-id="416b2-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="416b2-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="416b2-150">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="416b2-150">Minimum supported client</span></span><br/> | <span data-ttu-id="416b2-151">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="416b2-151">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="416b2-152">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="416b2-152">Minimum supported server</span></span><br/> | <span data-ttu-id="416b2-153">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="416b2-153">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="416b2-154">En-tête</span><span class="sxs-lookup"><span data-stu-id="416b2-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="416b2-155"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="416b2-155"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="416b2-156">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="416b2-156">Library</span></span><br/>                  | <dl> <span data-ttu-id="416b2-157"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="416b2-157"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="416b2-158">DLL</span><span class="sxs-lookup"><span data-stu-id="416b2-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="416b2-159"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="416b2-159"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="416b2-160">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="416b2-160">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="416b2-161">**DeletePrinterDriverExW** (Unicode) et **DeletePrinterDriverExA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="416b2-161">**DeletePrinterDriverExW** (Unicode) and **DeletePrinterDriverExA** (ANSI)</span></span><br/>                     |



## <a name="see-also"></a><span data-ttu-id="416b2-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="416b2-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="416b2-163">Impression</span><span class="sxs-lookup"><span data-stu-id="416b2-163">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="416b2-164">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="416b2-164">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="416b2-165">**AddPrinterDriverEx**</span><span class="sxs-lookup"><span data-stu-id="416b2-165">**AddPrinterDriverEx**</span></span>](addprinterdriverex.md)
</dt> </dl>

 

 




