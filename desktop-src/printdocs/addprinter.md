---
description: La fonction AddPrinter ajoute une imprimante à la liste des imprimantes prises en charge pour un serveur spécifié.
ms.assetid: ffc4fee8-46c6-47ad-803d-623bf8efdefd
title: AddPrinter, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinter
- AddPrinterA
- AddPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 51416ed59bc1c6df1d2c69de87d61bdecab522f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202704"
---
# <a name="addprinter-function"></a><span data-ttu-id="4af6a-103">AddPrinter fonction)</span><span class="sxs-lookup"><span data-stu-id="4af6a-103">AddPrinter function</span></span>

<span data-ttu-id="4af6a-104">La fonction **AddPrinter** ajoute une imprimante à la liste des imprimantes prises en charge pour un serveur spécifié.</span><span class="sxs-lookup"><span data-stu-id="4af6a-104">The **AddPrinter** function adds a printer to the list of supported printers for a specified server.</span></span>

## <a name="syntax"></a><span data-ttu-id="4af6a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4af6a-105">Syntax</span></span>


```C++
HANDLE AddPrinter(
  _In_ LPTSTR *pName,
  _In_ DWORD  Level,
  _In_ LPBYTE pPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="4af6a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4af6a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4af6a-107">*pname* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4af6a-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4af6a-108">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du serveur sur lequel l’imprimante doit être installée.</span><span class="sxs-lookup"><span data-stu-id="4af6a-108">A pointer to a null-terminated string that specifies the name of the server on which the printer should be installed.</span></span> <span data-ttu-id="4af6a-109">Si cette chaîne est **null**, l’imprimante est installée localement.</span><span class="sxs-lookup"><span data-stu-id="4af6a-109">If this string is **NULL**, the printer is installed locally.</span></span>

</dd> <dt>

<span data-ttu-id="4af6a-110">De *niveau* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4af6a-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4af6a-111">Version de la structure vers laquelle *pPrinter* pointe.</span><span class="sxs-lookup"><span data-stu-id="4af6a-111">The version of the structure to which *pPrinter* points.</span></span> <span data-ttu-id="4af6a-112">Cette valeur doit être 2.</span><span class="sxs-lookup"><span data-stu-id="4af6a-112">This value must be 2.</span></span>

</dd> <dt>

<span data-ttu-id="4af6a-113">*pPrinter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4af6a-113">*pPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4af6a-114">Pointeur vers une structure [**d' \_ informations \_ d’imprimante 2**](printer-info-2.md) qui contient des informations sur l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="4af6a-114">A pointer to a [**PRINTER\_INFO\_2**](printer-info-2.md) structure that contains information about the printer.</span></span> <span data-ttu-id="4af6a-115">Vous devez spécifier des valeurs **non null** pour les membres **pPrinterName**, **pPortName**, **pDriverName** et **pPrintProcessor** de cette structure avant d’appeler **AddPrinter**.</span><span class="sxs-lookup"><span data-stu-id="4af6a-115">You must specify non-**NULL** values for the **pPrinterName**, **pPortName**, **pDriverName**, and **pPrintProcessor** members of this structure before calling **AddPrinter**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4af6a-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4af6a-116">Return value</span></span>

<span data-ttu-id="4af6a-117">Si la fonction est réussie, la valeur de retour est un handle (pas thread-safe) vers un nouvel objet Printer.</span><span class="sxs-lookup"><span data-stu-id="4af6a-117">If the function succeeds, the return value is a handle (not thread safe) to a new printer object.</span></span> <span data-ttu-id="4af6a-118">Lorsque vous avez terminé avec le descripteur, transmettez-le à la fonction [**ClosePrinter**](closeprinter.md) pour le fermer.</span><span class="sxs-lookup"><span data-stu-id="4af6a-118">When you are finished with the handle, pass it to the [**ClosePrinter**](closeprinter.md) function to close it.</span></span>

<span data-ttu-id="4af6a-119">Si la fonction échoue, la valeur de retour est **null**.</span><span class="sxs-lookup"><span data-stu-id="4af6a-119">If the function fails, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="4af6a-120">Notes</span><span class="sxs-lookup"><span data-stu-id="4af6a-120">Remarks</span></span>

<span data-ttu-id="4af6a-121">N’appelez pas cette méthode dans [**DllMain**](/windows/desktop/Dlls/dllmain).</span><span class="sxs-lookup"><span data-stu-id="4af6a-121">Do not call this method in [**DllMain**](/windows/desktop/Dlls/dllmain).</span></span>

> [!Note]  
> <span data-ttu-id="4af6a-122">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="4af6a-122">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="4af6a-123">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="4af6a-123">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="4af6a-124">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="4af6a-124">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="4af6a-125">L’appelant doit avoir le [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span><span class="sxs-lookup"><span data-stu-id="4af6a-125">The caller must have the [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

<span data-ttu-id="4af6a-126">Le handle retourné n’est pas thread-safe.</span><span class="sxs-lookup"><span data-stu-id="4af6a-126">The returned handle is not thread safe.</span></span> <span data-ttu-id="4af6a-127">Si les appelants doivent l’utiliser simultanément sur plusieurs threads, ils doivent fournir un accès de synchronisation personnalisé au handle d’imprimante à l’aide des [fonctions de synchronisation](/windows/desktop/Sync/synchronization-functions).</span><span class="sxs-lookup"><span data-stu-id="4af6a-127">If callers need to use it concurrently on multiple threads, they must provide custom synchronization access to the printer handle using the [Synchronization Functions](/windows/desktop/Sync/synchronization-functions).</span></span> <span data-ttu-id="4af6a-128">Pour éviter d’écrire du code personnalisé, l’application peut ouvrir un handle d’imprimante sur chaque thread, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="4af6a-128">To avoid writing custom code the application can open a printer handle on each thread, as needed.</span></span>

<span data-ttu-id="4af6a-129">Voici les membres de la structure [**Printer \_ info \_ 2**](printer-info-2.md) qui peuvent être définis avant l’appel de la fonction **AddPrinter** :</span><span class="sxs-lookup"><span data-stu-id="4af6a-129">The following are the members of the [**PRINTER\_INFO\_2**](printer-info-2.md) structure that can be set before the **AddPrinter** function is called:</span></span>

-   <span data-ttu-id="4af6a-130">**Attributs**</span><span class="sxs-lookup"><span data-stu-id="4af6a-130">**Attributes**</span></span>
-   <span data-ttu-id="4af6a-131">**pPrintProcessor**</span><span class="sxs-lookup"><span data-stu-id="4af6a-131">**pPrintProcessor**</span></span>
-   <span data-ttu-id="4af6a-132">**DefaultPriority**</span><span class="sxs-lookup"><span data-stu-id="4af6a-132">**DefaultPriority**</span></span>
-   <span data-ttu-id="4af6a-133">**Priorité**</span><span class="sxs-lookup"><span data-stu-id="4af6a-133">**Priority**</span></span>
-   <span data-ttu-id="4af6a-134">**pComment**</span><span class="sxs-lookup"><span data-stu-id="4af6a-134">**pComment**</span></span>
-   <span data-ttu-id="4af6a-135">**pSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="4af6a-135">**pSecurityDescriptor**</span></span>
-   <span data-ttu-id="4af6a-136">**pDatatype**</span><span class="sxs-lookup"><span data-stu-id="4af6a-136">**pDatatype**</span></span>
-   <span data-ttu-id="4af6a-137">**pSepFile**</span><span class="sxs-lookup"><span data-stu-id="4af6a-137">**pSepFile**</span></span>
-   <span data-ttu-id="4af6a-138">**pDevMode**</span><span class="sxs-lookup"><span data-stu-id="4af6a-138">**pDevMode**</span></span>
-   <span data-ttu-id="4af6a-139">**pShareName**</span><span class="sxs-lookup"><span data-stu-id="4af6a-139">**pShareName**</span></span>
-   <span data-ttu-id="4af6a-140">**pLocation**</span><span class="sxs-lookup"><span data-stu-id="4af6a-140">**pLocation**</span></span>
-   <span data-ttu-id="4af6a-141">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="4af6a-141">**StartTime**</span></span>
-   <span data-ttu-id="4af6a-142">**pParameters**</span><span class="sxs-lookup"><span data-stu-id="4af6a-142">**pParameters**</span></span>
-   <span data-ttu-id="4af6a-143">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="4af6a-143">**UntilTime**</span></span>

<span data-ttu-id="4af6a-144">Les membres **Status**, **cJobs** et **AveragePPM** de la structure [**Printer \_ info \_ 2**](printer-info-2.md) sont réservés pour une utilisation par la fonction [**GetPrinter**](getprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="4af6a-144">The **Status**, **cJobs**, and **AveragePPM** members of the [**PRINTER\_INFO\_2**](printer-info-2.md) structure are reserved for use by the [**GetPrinter**](getprinter.md) function.</span></span> <span data-ttu-id="4af6a-145">Ils ne doivent pas être définis avant d’appeler **AddPrinter**.</span><span class="sxs-lookup"><span data-stu-id="4af6a-145">They must not be set before calling **AddPrinter**.</span></span>

<span data-ttu-id="4af6a-146">Si **pSecurityDescriptor** a la **valeur null**, le système affecte un descripteur de sécurité par défaut à l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="4af6a-146">If **pSecurityDescriptor** is **NULL**, the system assigns a default security descriptor to the printer.</span></span> <span data-ttu-id="4af6a-147">Le descripteur de sécurité par défaut dispose des autorisations suivantes.</span><span class="sxs-lookup"><span data-stu-id="4af6a-147">The default security descriptor has the following permissions.</span></span>



| <span data-ttu-id="4af6a-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="4af6a-148">Value</span></span>                          | <span data-ttu-id="4af6a-149">Description</span><span class="sxs-lookup"><span data-stu-id="4af6a-149">Description</span></span>                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4af6a-150">Administrateurs et utilisateurs avec pouvoir</span><span class="sxs-lookup"><span data-stu-id="4af6a-150">Administrators and Power Users</span></span> | <span data-ttu-id="4af6a-151">Contrôle total sur la file d’attente à l’impression.</span><span class="sxs-lookup"><span data-stu-id="4af6a-151">Full control on the print queue.</span></span> <span data-ttu-id="4af6a-152">Cela signifie que les membres de ces groupes peuvent imprimer, gérer la file d’attente (peut supprimer la file d’attente, modifier les paramètres de la file d’attente, y compris le descripteur de sécurité) et gérer les travaux d’impression de tous les utilisateurs (supprimer, suspendre, reprendre, redémarrer les travaux). Notez que les utilisateurs avec pouvoir n’existent pas avant Windows XP professionnel.</span><span class="sxs-lookup"><span data-stu-id="4af6a-152">This means members of these groups can print, manage the queue (can delete the queue, change any setting of the queue, including the security descriptor), and manage the print jobs of all users (delete, pause, resume, restart jobs).Note that Power Users do not exist before Windows XP Professional.</span></span><br/> |
| <span data-ttu-id="4af6a-153">Propriétaire créateur</span><span class="sxs-lookup"><span data-stu-id="4af6a-153">Creator/Owner</span></span>                  | <span data-ttu-id="4af6a-154">Peut gérer ses propres travaux.</span><span class="sxs-lookup"><span data-stu-id="4af6a-154">Can manage own jobs.</span></span> <span data-ttu-id="4af6a-155">Cela signifie que les utilisateurs qui envoient des travaux peuvent gérer (supprimer, suspendre, reprendre, redémarrer) leurs propres travaux.</span><span class="sxs-lookup"><span data-stu-id="4af6a-155">This means that user who submit jobs can manage (delete, pause, resume, restart) their own jobs.</span></span>                                                                                                                                                                                                                                  |
| <span data-ttu-id="4af6a-156">Tout le monde</span><span class="sxs-lookup"><span data-stu-id="4af6a-156">Everyone</span></span>                       | <span data-ttu-id="4af6a-157">Exécution et contrôle de lecture standard.</span><span class="sxs-lookup"><span data-stu-id="4af6a-157">Execute and standard read control.</span></span> <span data-ttu-id="4af6a-158">Cela signifie que les membres du groupe tout le monde peuvent imprimer et lire les propriétés de la file d’attente à l’impression.</span><span class="sxs-lookup"><span data-stu-id="4af6a-158">This means that members of the everyone group can print and read properties of the print queue.</span></span>                                                                                                                                                                                                                     |



 

<span data-ttu-id="4af6a-159">Une fois qu’une application a créé un objet Printer avec la fonction **AddPrinter** , elle doit utiliser la fonction [**PrinterProperties**](printerproperties.md) pour spécifier les paramètres corrects pour le pilote d’imprimante associé à l’objet Printer.</span><span class="sxs-lookup"><span data-stu-id="4af6a-159">After an application creates a printer object with the **AddPrinter** function, it must use the [**PrinterProperties**](printerproperties.md) function to specify the correct settings for the printer driver associated with the printer object.</span></span>

<span data-ttu-id="4af6a-160">La fonction **AddPrinter** renvoie une erreur si un objet Printer portant le même nom existe déjà, sauf si cet objet est marqué comme étant en attente de suppression.</span><span class="sxs-lookup"><span data-stu-id="4af6a-160">The **AddPrinter** function returns an error if a printer object with the same name already exists, unless that object is marked as pending deletion.</span></span> <span data-ttu-id="4af6a-161">Dans ce cas, l’imprimante existante n’est pas supprimée et les paramètres de création de **AddPrinter** sont utilisés pour modifier les paramètres d’imprimante existants (comme si l’application avait utilisé la fonction [**SetPrinter**](setprinter.md) ).</span><span class="sxs-lookup"><span data-stu-id="4af6a-161">In that case, the existing printer is not deleted, and the **AddPrinter** creation parameters are used to change the existing printer settings (as if the application had used the [**SetPrinter**](setprinter.md) function).</span></span>

<span data-ttu-id="4af6a-162">Utilisez la fonction [**EnumPrintProcessors**](enumprintprocessors.md) pour énumérer l’ensemble des processeurs d’impression installés sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="4af6a-162">Use the [**EnumPrintProcessors**](enumprintprocessors.md) function to enumerate the set of print processors installed on a server.</span></span> <span data-ttu-id="4af6a-163">Utilisez la fonction [**EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md) pour énumérer l’ensemble des types de données pris en charge par un processeur d’impression.</span><span class="sxs-lookup"><span data-stu-id="4af6a-163">Use the [**EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md) function to enumerate the set of data types that a print processor supports.</span></span> <span data-ttu-id="4af6a-164">Utilisez la fonction [**EnumPorts**](enumports.md) pour énumérer l’ensemble des ports disponibles.</span><span class="sxs-lookup"><span data-stu-id="4af6a-164">Use the [**EnumPorts**](enumports.md) function to enumerate the set of available ports.</span></span> <span data-ttu-id="4af6a-165">Utilisez la fonction [**EnumPrinterDrivers**](enumprinterdrivers.md) pour énumérer les pilotes d’imprimante installés.</span><span class="sxs-lookup"><span data-stu-id="4af6a-165">Use the [**EnumPrinterDrivers**](enumprinterdrivers.md) function to enumerate the installed printer drivers.</span></span>

<span data-ttu-id="4af6a-166">L’appelant de la fonction **AddPrinter** doit disposer d’un accès serveur \_ \_ administrer l’accès au serveur sur lequel l’imprimante doit être créée.</span><span class="sxs-lookup"><span data-stu-id="4af6a-166">The caller of the **AddPrinter** function must have SERVER\_ACCESS\_ADMINISTER access to the server on which the printer is to be created.</span></span> <span data-ttu-id="4af6a-167">Le descripteur retourné par la fonction disposera de l' \_ autorisation d’accès imprimante All \_ et pourra être utilisé pour effectuer des opérations administratives sur l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="4af6a-167">The handle returned by the function will have PRINTER\_ALL\_ACCESS permission, and can be used to perform administrative operations on the printer.</span></span>

<span data-ttu-id="4af6a-168">Si la fonction **DrvPrinterEvent** est passée à l' \_ indicateur \_ d’événement d’imprimante \_ no \_ UI, le pilote ne doit pas utiliser d’appel d’interface utilisateur pendant **DrvPrinterEvent**.</span><span class="sxs-lookup"><span data-stu-id="4af6a-168">If the **DrvPrinterEvent** function is passed the PRINTER\_EVENT\_FLAG\_NO\_UI flag, the driver should not use a UI call during **DrvPrinterEvent**.</span></span> <span data-ttu-id="4af6a-169">Pour effectuer des tâches liées à l’interface utilisateur, le programme d’installation doit utiliser l’entrée **VendorSetup** dans le fichier. inf de l’imprimante ou, pour plug-and-Play appareils, le programme d’installation peut utiliser un co-programme d’installation spécifique à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="4af6a-169">To do UI-related jobs, the installer should either use the **VendorSetup** entry in the printer's .inf file or, for Plug and Play devices, the installer can use a device-specific co-installer.</span></span> <span data-ttu-id="4af6a-170">Pour plus d’informations sur **VendorSetup**, consultez le kit de développement de pilotes (DDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="4af6a-170">For more information about **VendorSetup**, see the Microsoft Windows Driver Development Kit (DDK).</span></span>

<span data-ttu-id="4af6a-171">Le pare-feu de connexion Internet (ICF) bloque les ports d’imprimante par défaut, mais une exception pour le partage de fichiers et d’imprimantes est activée lorsque vous exécutez **AddPrinter**.</span><span class="sxs-lookup"><span data-stu-id="4af6a-171">The Internet Connection Firewall (ICF) blocks printer ports by default, but an exception for File and Print Sharing is enabled when you run **AddPrinter**.</span></span>

## <a name="requirements"></a><span data-ttu-id="4af6a-172">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4af6a-172">Requirements</span></span>



| <span data-ttu-id="4af6a-173">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4af6a-173">Requirement</span></span> | <span data-ttu-id="4af6a-174">Valeur</span><span class="sxs-lookup"><span data-stu-id="4af6a-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4af6a-175">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4af6a-175">Minimum supported client</span></span><br/> | <span data-ttu-id="4af6a-176">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4af6a-176">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4af6a-177">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4af6a-177">Minimum supported server</span></span><br/> | <span data-ttu-id="4af6a-178">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4af6a-178">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4af6a-179">En-tête</span><span class="sxs-lookup"><span data-stu-id="4af6a-179">Header</span></span><br/>                   | <dl> <span data-ttu-id="4af6a-180"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4af6a-180"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="4af6a-181">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4af6a-181">Library</span></span><br/>                  | <dl> <span data-ttu-id="4af6a-182"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4af6a-182"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="4af6a-183">DLL</span><span class="sxs-lookup"><span data-stu-id="4af6a-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4af6a-184"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="4af6a-184"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="4af6a-185">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="4af6a-185">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="4af6a-186">**AddPrinterW** (Unicode) et **AddPrinterA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="4af6a-186">**AddPrinterW** (Unicode) and **AddPrinterA** (ANSI)</span></span><br/>                                           |



## <a name="see-also"></a><span data-ttu-id="4af6a-187">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4af6a-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4af6a-188">Impression</span><span class="sxs-lookup"><span data-stu-id="4af6a-188">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="4af6a-189">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="4af6a-189">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="4af6a-190">**ClosePrinter**</span><span class="sxs-lookup"><span data-stu-id="4af6a-190">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="4af6a-191">**DeletePrinter**</span><span class="sxs-lookup"><span data-stu-id="4af6a-191">**DeletePrinter**</span></span>](deleteprinter.md)
</dt> <dt>

[<span data-ttu-id="4af6a-192">**EnumPorts**</span><span class="sxs-lookup"><span data-stu-id="4af6a-192">**EnumPorts**</span></span>](enumports.md)
</dt> <dt>

[<span data-ttu-id="4af6a-193">**EnumPrinterDrivers**</span><span class="sxs-lookup"><span data-stu-id="4af6a-193">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="4af6a-194">**EnumPrintProcessors**</span><span class="sxs-lookup"><span data-stu-id="4af6a-194">**EnumPrintProcessors**</span></span>](enumprintprocessors.md)
</dt> <dt>

[<span data-ttu-id="4af6a-195">**EnumPrintProcessorDatatypes**</span><span class="sxs-lookup"><span data-stu-id="4af6a-195">**EnumPrintProcessorDatatypes**</span></span>](enumprintprocessordatatypes.md)
</dt> <dt>

[<span data-ttu-id="4af6a-196">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="4af6a-196">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="4af6a-197">**\_Infos sur l’imprimante \_ 2**</span><span class="sxs-lookup"><span data-stu-id="4af6a-197">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="4af6a-198">**PrinterProperties**</span><span class="sxs-lookup"><span data-stu-id="4af6a-198">**PrinterProperties**</span></span>](printerproperties.md)
</dt> <dt>

[<span data-ttu-id="4af6a-199">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="4af6a-199">**SetPrinter**</span></span>](setprinter.md)
</dt> </dl>

 

