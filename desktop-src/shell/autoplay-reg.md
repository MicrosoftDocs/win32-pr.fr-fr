---
description: Il existe de nombreuses situations où l’exécution automatique peut être désactivée de manière temporaire ou permanente.
ms.assetid: 5e65a3d8-04b9-46ba-b4e5-a976e1923bfd
title: Activation et désactivation de l’exécution automatique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a567f50db75cd129346e193e66ba0ae5f74fa955
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393455"
---
# <a name="enabling-and-disabling-autorun"></a><span data-ttu-id="3f384-103">Activation et désactivation de l’exécution automatique</span><span class="sxs-lookup"><span data-stu-id="3f384-103">Enabling and Disabling AutoRun</span></span>

<span data-ttu-id="3f384-104">Il existe de nombreuses situations où l’exécution automatique peut être désactivée de manière temporaire ou permanente.</span><span class="sxs-lookup"><span data-stu-id="3f384-104">There are many situations where AutoRun may need to be temporarily or persistently disabled.</span></span> <span data-ttu-id="3f384-105">Par exemple, l’exécution automatique peut interférer avec le fonctionnement d’une application en cours d’exécution et doit être désactivée pendant toute la durée.</span><span class="sxs-lookup"><span data-stu-id="3f384-105">For example, AutoRun might interfere with the operation of a running application and need to be disabled for the duration.</span></span> <span data-ttu-id="3f384-106">Le système offre plusieurs moyens de désactiver l’exécution automatique.</span><span class="sxs-lookup"><span data-stu-id="3f384-106">The system provides several ways to disable AutoRun.</span></span>

-   [<span data-ttu-id="3f384-107">Suppression de l’exécution automatique par programmation</span><span class="sxs-lookup"><span data-stu-id="3f384-107">Suppressing AutoRun Programmatically</span></span>](#suppressing-autorun-programmatically)
-   [<span data-ttu-id="3f384-108">Utilisation du Registre pour désactiver l’exécution automatique</span><span class="sxs-lookup"><span data-stu-id="3f384-108">Using the Registry to Disable AutoRun</span></span>](#using-the-registry-to-disable-autorun)
-   [<span data-ttu-id="3f384-109">Exécution automatique pour d’autres types de supports de stockage</span><span class="sxs-lookup"><span data-stu-id="3f384-109">AutoRun for Other Types of Storage Media</span></span>](#autorun-for-other-types-of-storage-media)

## <a name="suppressing-autorun-programmatically"></a><span data-ttu-id="3f384-110">Suppression de l’exécution automatique par programmation</span><span class="sxs-lookup"><span data-stu-id="3f384-110">Suppressing AutoRun Programmatically</span></span>

<span data-ttu-id="3f384-111">Il existe plusieurs situations dans lesquelles l’exécution automatique peut être supprimée par programmation.</span><span class="sxs-lookup"><span data-stu-id="3f384-111">There are a variety of situations where AutoRun may need to be suppressed programmatically.</span></span> <span data-ttu-id="3f384-112">En voici deux exemples:</span><span class="sxs-lookup"><span data-stu-id="3f384-112">Two examples are:</span></span>

-   <span data-ttu-id="3f384-113">Votre application dispose d’un programme d’installation qui oblige l’utilisateur à insérer un autre disque pouvant contenir un fichier autorun. inf.</span><span class="sxs-lookup"><span data-stu-id="3f384-113">Your application has a setup program that requires the user to insert another disc that may contain an Autorun.inf file.</span></span>
-   <span data-ttu-id="3f384-114">Pendant le fonctionnement de votre application, l’utilisateur peut être amené à insérer un autre disque pouvant contenir un fichier autorun. inf.</span><span class="sxs-lookup"><span data-stu-id="3f384-114">During the operation of your application, the user may need to insert another disc that may contain an Autorun.inf file.</span></span>

<span data-ttu-id="3f384-115">Dans les deux cas, vous ne souhaitez généralement pas lancer une autre application tant que l’original est en cours.</span><span class="sxs-lookup"><span data-stu-id="3f384-115">In either case, you will normally not want to launch another application while the original is in progress.</span></span>

<span data-ttu-id="3f384-116">Les utilisateurs peuvent supprimer manuellement l’exécution automatique en maintenant la touche Maj enfoncée lorsqu’ils insèrent le CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="3f384-116">Users can manually suppress AutoRun by holding down the SHIFT key when they insert the CD-ROM.</span></span> <span data-ttu-id="3f384-117">Toutefois, il est généralement préférable de gérer cette opération par programme plutôt qu’en fonction de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3f384-117">However, it is usually preferable to handle this operation programmatically rather than depending on the user.</span></span>

<span data-ttu-id="3f384-118">Avec les systèmes qui disposent de Shell [version 4,70](versions.md) et versions ultérieures, Windows envoie un message « QueryCancelAutoPlay » à la fenêtre de premier plan.</span><span class="sxs-lookup"><span data-stu-id="3f384-118">With systems that have Shell [version 4.70](versions.md) and later, Windows sends a "QueryCancelAutoPlay" message to the foreground window.</span></span> <span data-ttu-id="3f384-119">Votre application peut répondre à ce message pour supprimer l’exécution automatique.</span><span class="sxs-lookup"><span data-stu-id="3f384-119">Your application can respond to this message to suppress AutoRun.</span></span> <span data-ttu-id="3f384-120">Cette approche est utilisée par les utilitaires système tels que la boîte de dialogue [ouvrir](../dlgbox/open-and-save-as-dialog-boxes.md) un courant pour désactiver l’exécution automatique.</span><span class="sxs-lookup"><span data-stu-id="3f384-120">This approach is used by system utilities such as the [Open](../dlgbox/open-and-save-as-dialog-boxes.md) common dialog box to disable AutoRun.</span></span>

<span data-ttu-id="3f384-121">Les fragments de code suivants montrent comment configurer et gérer ce message.</span><span class="sxs-lookup"><span data-stu-id="3f384-121">The following code fragments illustrate how to set up and handle this message.</span></span> <span data-ttu-id="3f384-122">Votre application doit être en cours d’exécution dans la fenêtre de premier plan.</span><span class="sxs-lookup"><span data-stu-id="3f384-122">Your application must be running in the foreground window.</span></span> <span data-ttu-id="3f384-123">Tout d’abord, inscrivez « QueryCancelAutoPlay » en tant que message Windows :</span><span class="sxs-lookup"><span data-stu-id="3f384-123">First, register "QueryCancelAutoPlay" as a Windows message:</span></span>


```C++
uMessage = RegisterWindowMessage(TEXT("QueryCancelAutoPlay"));
```



<span data-ttu-id="3f384-124">La fenêtre de votre application doit être au premier plan pour recevoir ce message.</span><span class="sxs-lookup"><span data-stu-id="3f384-124">Your application's window must be in the foreground to receive this message.</span></span> <span data-ttu-id="3f384-125">Le gestionnaire de messages doit retourner la **valeur true** pour annuler l’exécution automatique et **false** pour l’activer.</span><span class="sxs-lookup"><span data-stu-id="3f384-125">The message handler should return **TRUE** to cancel AutoRun and **FALSE** to enable it.</span></span> <span data-ttu-id="3f384-126">Le fragment de code suivant illustre l’utilisation de ce message pour désactiver l’exécution automatique.</span><span class="sxs-lookup"><span data-stu-id="3f384-126">The following code fragment illustrates how to use this message to disable AutoRun.</span></span>


```C++
UINT g_uQueryCancelAutoPlay = 0;

LRESULT WndProc(HWND hwnd, UINT uMsg,  WPARAM wParam, LPARAM lParam) 
{ 
    switch (uMsg) 
    { 
    ... 
    default: 
        if (!g_uQueryCancelAutoPlay)
        { 
            g_uQueryCancelAutoPlay = RegisterWindowMessage(TEXT("QueryCancelAutoPlay"));
        } 
        if (uMsg && uMsg == g_uQueryCancelAutoPlay)
        { 
            return TRUE;       // Cancel AutoRun
        }
    }
}
```



<span data-ttu-id="3f384-127">Si votre application utilise une boîte de dialogue et doit répondre à un message « QueryCancelAutoPlay », elle ne peut pas simplement retourner **true** ou **false**.</span><span class="sxs-lookup"><span data-stu-id="3f384-127">If your application is using a dialog box and needs to respond to a "QueryCancelAutoPlay" message, it cannot simply return **TRUE** or **FALSE**.</span></span> <span data-ttu-id="3f384-128">Au lieu de cela, appelez [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) avec *NIndex* défini sur **DWL \_ MSGRESULT**.</span><span class="sxs-lookup"><span data-stu-id="3f384-128">Instead, call [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) with *nIndex* set to **DWL\_MSGRESULT**.</span></span> <span data-ttu-id="3f384-129">Affectez la valeur **true** au paramètre *dwNewLong* pour annuler l’exécution automatique, et **false** pour l’activer.</span><span class="sxs-lookup"><span data-stu-id="3f384-129">Set the *dwNewLong* parameter to **TRUE** to cancel AutoRun, and **FALSE** to enable it.</span></span> <span data-ttu-id="3f384-130">Par exemple, l’exemple de procédure de boîte de dialogue suivant annule l’exécution automatique lorsqu’il reçoit un message « QueryCancelAutoPlay ».</span><span class="sxs-lookup"><span data-stu-id="3f384-130">For example, the following sample dialog box procedure cancels AutoRun when it receives a "QueryCancelAutoPlay" message.</span></span>


```C++
UINT g_uQueryCancelAutoPlay = 0;

BOOL DialogProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    switch (uMsg) 
    { 
    ...
    default: 
        if (!g_uQueryCancelAutoPlay)
        {
            g_uQueryCancelAutoPlay = RegisterWindowMessage(TEXT("QueryCancelAutoPlay"));
        } 
        if (uMsg == g_uQueryCancelAutoPlay) 
        {
            SetWindowLong(hDlg, DWL_MSGRESULT, TRUE);          
            return 1;               
        }
    } 
```



## <a name="using-the-registry-to-disable-autorun"></a><span data-ttu-id="3f384-131">Utilisation du Registre pour désactiver l’exécution automatique</span><span class="sxs-lookup"><span data-stu-id="3f384-131">Using the Registry to Disable AutoRun</span></span>

<span data-ttu-id="3f384-132">Il existe deux valeurs de Registre qui peuvent être utilisées pour désactiver de manière permanente l’exécution automatique : NoDriveAutoRun et NoDriveTypeAutoRun.</span><span class="sxs-lookup"><span data-stu-id="3f384-132">There are two registry values that can be used to persistently disable AutoRun: NoDriveAutoRun and NoDriveTypeAutoRun.</span></span> <span data-ttu-id="3f384-133">La première valeur désactive l’exécution automatique pour les lettres de lecteur spécifiées et la seconde désactive l’exécution automatique pour une classe de lecteurs.</span><span class="sxs-lookup"><span data-stu-id="3f384-133">The first value disables AutoRun for specified drive letters and the second disables AutoRun for a class of drives.</span></span> <span data-ttu-id="3f384-134">Si l’une de ces valeurs est définie pour désactiver l’exécution automatique pour un appareil particulier, elle est désactivée.</span><span class="sxs-lookup"><span data-stu-id="3f384-134">If either of these values is set to disable AutoRun for a particular device, it will be disabled.</span></span> <span data-ttu-id="3f384-135">Consultez l’article de la base de connaissances [Comment désactiver la fonctionnalité d’exécution automatique dans Windows](https://support.microsoft.com/kb/967715) pour plus d’informations sur la désactivation de la fonctionnalité d’exécution automatique.</span><span class="sxs-lookup"><span data-stu-id="3f384-135">See the Knowledge Base article [How to disable the Autorun functionality in Windows](https://support.microsoft.com/kb/967715) for more information on disabling AutoRun functionality.</span></span> <span data-ttu-id="3f384-136">Cet article répertorie les différentes mises à jour que vous devez avoir installées pour désactiver correctement la fonctionnalité d’exécution automatique.</span><span class="sxs-lookup"><span data-stu-id="3f384-136">This article lists the different updates that you must have installed to correctly disable the Autorun functionality.</span></span>

> [!Note]  
> <span data-ttu-id="3f384-137">Les valeurs NoDriveAutoRun et NoDriveTypeAutoRun doivent uniquement être modifiées par les administrateurs système pour modifier la valeur de l’ensemble du système à des fins de test ou d’administration.</span><span class="sxs-lookup"><span data-stu-id="3f384-137">The NoDriveAutoRun and NoDriveTypeAutoRun values should only be modified by system administrators to change the value for the entire system for testing or administrative purposes.</span></span> <span data-ttu-id="3f384-138">Les applications ne doivent pas modifier ces valeurs, car il n’existe aucun moyen de les restaurer de manière fiable à leurs valeurs d’origine.</span><span class="sxs-lookup"><span data-stu-id="3f384-138">Applications should not modify these values, as there is no way to reliably restore them to their original values.</span></span>

 

<span data-ttu-id="3f384-139">La valeur NoDriveAutoRun désactive l’exécution automatique pour les lettres de lecteur spécifiées.</span><span class="sxs-lookup"><span data-stu-id="3f384-139">The NoDriveAutoRun value disables AutoRun for specified drive letters.</span></span> <span data-ttu-id="3f384-140">Il s’agit d’une valeur de données de Registre \_ DWORD, trouvée sous la clé suivante :</span><span class="sxs-lookup"><span data-stu-id="3f384-140">It is a REG\_DWORD data value, found under the following key:</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
                  Explorer
```

<span data-ttu-id="3f384-141">Le premier bit de la valeur correspond au lecteur A :, au deuxième à B :, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="3f384-141">The first bit of the value corresponds to drive A:, the second to B:, and so on.</span></span> <span data-ttu-id="3f384-142">Pour désactiver l’exécution automatique pour une ou plusieurs lettres de lecteur, définissez les bits correspondants.</span><span class="sxs-lookup"><span data-stu-id="3f384-142">To disable AutoRun for one or more drive letters, set the corresponding bits.</span></span> <span data-ttu-id="3f384-143">Par exemple, pour désactiver les lecteurs A : et C :, affectez à NoDriveAutoRun la valeur `0x00000005` .</span><span class="sxs-lookup"><span data-stu-id="3f384-143">For example, to disable the A: and C: drives, set NoDriveAutoRun to `0x00000005`.</span></span>

<span data-ttu-id="3f384-144">La valeur NoDriveTypeAutoRun désactive l’exécution automatique pour une classe de lecteurs.</span><span class="sxs-lookup"><span data-stu-id="3f384-144">The NoDriveTypeAutoRun value disables AutoRun for a class of drives.</span></span> <span data-ttu-id="3f384-145">Il s’agit d’une \_ valeur de données binaires reg DWORD ou de 4 octets \_ , trouvée sous la même clé.</span><span class="sxs-lookup"><span data-stu-id="3f384-145">It is a REG\_DWORD or 4-byte REG\_BINARY data value, found under the same key.</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
                  Explorer
```

<span data-ttu-id="3f384-146">En définissant les bits du premier octet de cette valeur, différents lecteurs peuvent être exclus de l’utilisation de l’exécution automatique.</span><span class="sxs-lookup"><span data-stu-id="3f384-146">By setting the bits of this value's first byte, different drives can be excluded from working with AutoRun.</span></span>

<span data-ttu-id="3f384-147">Le tableau suivant indique les constantes bits et de masque de bits, qui peuvent être définies dans le premier octet de NoDriveTypeAutoRun pour désactiver l’exécution automatique pour un type de lecteur particulier.</span><span class="sxs-lookup"><span data-stu-id="3f384-147">The following table gives the bits and bitmask constants, that can be set in the first byte of NoDriveTypeAutoRun to disable AutoRun for a particular drive type.</span></span> <span data-ttu-id="3f384-148">Vous devez redémarrer l’Explorateur Windows pour que les modifications soient prises en compte.</span><span class="sxs-lookup"><span data-stu-id="3f384-148">You must restart Windows Explorer before the changes take effect.</span></span>



| <span data-ttu-id="3f384-149">Nombre de bits</span><span class="sxs-lookup"><span data-stu-id="3f384-149">Bit Number</span></span> | <span data-ttu-id="3f384-150">Constante de masque binaire</span><span class="sxs-lookup"><span data-stu-id="3f384-150">Bitmask Constant</span></span>      | <span data-ttu-id="3f384-151">Description</span><span class="sxs-lookup"><span data-stu-id="3f384-151">Description</span></span>                                             |
|------------|-----------------------|---------------------------------------------------------|
| <span data-ttu-id="3f384-152">0x04</span><span class="sxs-lookup"><span data-stu-id="3f384-152">0x04</span></span>       | <span data-ttu-id="3f384-153">**LECTEUR à \_ Supprimer**</span><span class="sxs-lookup"><span data-stu-id="3f384-153">**DRIVE\_REMOVEABLE**</span></span> | <span data-ttu-id="3f384-154">Un disque peut être supprimé d’un lecteur (par exemple une disquette).</span><span class="sxs-lookup"><span data-stu-id="3f384-154">Disk can be removed from drive (such as a floppy disk).</span></span> |
| <span data-ttu-id="3f384-155">0x08</span><span class="sxs-lookup"><span data-stu-id="3f384-155">0x08</span></span>       | <span data-ttu-id="3f384-156">**LECTEUR \_ fixe**</span><span class="sxs-lookup"><span data-stu-id="3f384-156">**DRIVE\_FIXED**</span></span>      | <span data-ttu-id="3f384-157">Impossible de supprimer le disque du lecteur (disque dur).</span><span class="sxs-lookup"><span data-stu-id="3f384-157">Disk cannot be removed from drive (a hard disk).</span></span>        |
| <span data-ttu-id="3f384-158">0x10</span><span class="sxs-lookup"><span data-stu-id="3f384-158">0x10</span></span>       | <span data-ttu-id="3f384-159">**LECTEUR \_ distant**</span><span class="sxs-lookup"><span data-stu-id="3f384-159">**DRIVE\_REMOTE**</span></span>     | <span data-ttu-id="3f384-160">Lecteur réseau.</span><span class="sxs-lookup"><span data-stu-id="3f384-160">Network drive.</span></span>                                          |
| <span data-ttu-id="3f384-161">0x20</span><span class="sxs-lookup"><span data-stu-id="3f384-161">0x20</span></span>       | <span data-ttu-id="3f384-162">**LECTEUR \_ cdrom**</span><span class="sxs-lookup"><span data-stu-id="3f384-162">**DRIVE\_CDROM**</span></span>      | <span data-ttu-id="3f384-163">Lecteur de CD-ROM</span><span class="sxs-lookup"><span data-stu-id="3f384-163">CD-ROM drive.</span></span>                                           |
| <span data-ttu-id="3f384-164">0x40</span><span class="sxs-lookup"><span data-stu-id="3f384-164">0x40</span></span>       | <span data-ttu-id="3f384-165">**LECTEUR \_ ramdisk**</span><span class="sxs-lookup"><span data-stu-id="3f384-165">**DRIVE\_RAMDISK**</span></span>    | <span data-ttu-id="3f384-166">Disque RAM.</span><span class="sxs-lookup"><span data-stu-id="3f384-166">RAM disk.</span></span>                                               |



 

## <a name="autorun-for-other-types-of-storage-media"></a><span data-ttu-id="3f384-167">Exécution automatique pour d’autres types de supports de stockage</span><span class="sxs-lookup"><span data-stu-id="3f384-167">AutoRun for Other Types of Storage Media</span></span>

<span data-ttu-id="3f384-168">L’exécution automatique est principalement destinée à la distribution publique des applications sur CD-ROM et DVD-ROM, et son utilisation est déconseillée pour d’autres supports de stockage.</span><span class="sxs-lookup"><span data-stu-id="3f384-168">AutoRun is primarily intended for public distribution of applications on CD-ROM and DVD-ROM, and its use is discouraged for other storage media.</span></span> <span data-ttu-id="3f384-169">Toutefois, il est souvent utile d’activer l’exécution automatique sur d’autres types de supports de stockage amovibles.</span><span class="sxs-lookup"><span data-stu-id="3f384-169">However, it is often useful to enable AutoRun on other types of removable storage media.</span></span> <span data-ttu-id="3f384-170">Cette fonctionnalité est généralement utilisée pour simplifier le débogage des fichiers AutoRun. inf.</span><span class="sxs-lookup"><span data-stu-id="3f384-170">This feature is typically used simplify the debugging of AutoRun.inf files.</span></span> <span data-ttu-id="3f384-171">L’exécution automatique fonctionne uniquement sur les périphériques de stockage amovibles lorsque les critères suivants sont satisfaits :</span><span class="sxs-lookup"><span data-stu-id="3f384-171">AutoRun only works on removable storage devices when the following criteria are met:</span></span>

-   <span data-ttu-id="3f384-172">L’appareil doit avoir des pilotes compatibles avec l’exécution automatique.</span><span class="sxs-lookup"><span data-stu-id="3f384-172">The device must have AutoRun-compatible drivers.</span></span> <span data-ttu-id="3f384-173">Pour être compatible avec l’exécution automatique, un pilote doit informer le système qu’un disque a été inséré en envoyant un message [**WM \_ DEVICECHANGE**](../devio/wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="3f384-173">To be AutoRun-compatible, a driver must notify the system that a disk has been inserted by sending a [**WM\_DEVICECHANGE**](../devio/wm-devicechange.md) message.</span></span>
-   <span data-ttu-id="3f384-174">Le répertoire racine du support inséré doit contenir un fichier autorun. inf.</span><span class="sxs-lookup"><span data-stu-id="3f384-174">The root directory of the inserted media must contain an Autorun.inf file.</span></span>
-   <span data-ttu-id="3f384-175">L’exécution de l’exécution automatique ne doit pas être désactivée dans le [Registre](#using-the-registry-to-disable-autorun).</span><span class="sxs-lookup"><span data-stu-id="3f384-175">The device must not have AutoRun disabled through the [registry](#using-the-registry-to-disable-autorun).</span></span>
-   <span data-ttu-id="3f384-176">L’application de premier plan n’a pas [supprimé](#suppressing-autorun-programmatically) l’exécution automatique.</span><span class="sxs-lookup"><span data-stu-id="3f384-176">The foreground application has not [suppressed](#suppressing-autorun-programmatically) AutoRun.</span></span>

> [!Note]  
> <span data-ttu-id="3f384-177">Cette fonctionnalité ne doit pas être utilisée pour distribuer des applications sur un support amovible.</span><span class="sxs-lookup"><span data-stu-id="3f384-177">This feature should not be used to distribute applications on removable media.</span></span> <span data-ttu-id="3f384-178">Étant donné que l’implémentation de l’exécution automatique sur un support amovible offre un moyen simple de propager des virus informatiques, les utilisateurs doivent être suspects de toute disquette distribuée publiquement qui contient un fichier autorun. inf.</span><span class="sxs-lookup"><span data-stu-id="3f384-178">Because implementing AutoRun on removable media provides an easy way to spread computer viruses, users should be suspicious of any publicly distributed floppy disk that contains an Autorun.inf file.</span></span>

 

<span data-ttu-id="3f384-179">Normalement, l’exécution automatique démarre automatiquement, mais elle peut également être démarrée manuellement.</span><span class="sxs-lookup"><span data-stu-id="3f384-179">Normally, AutoRun starts automatically, but it can also be started manually.</span></span> <span data-ttu-id="3f384-180">Si l’appareil est conforme aux critères ci-dessus, le menu contextuel de la lettre de lecteur inclut une commande d' **exécution automatique** .</span><span class="sxs-lookup"><span data-stu-id="3f384-180">If the device meets the criteria listed above, the drive letter's shortcut menu will include an **AutoPlay** command.</span></span> <span data-ttu-id="3f384-181">Pour exécuter l’exécution automatique manuellement, cliquez avec le bouton droit sur l’icône du lecteur et sélectionnez **exécution automatique** dans le menu contextuel ou double-cliquez sur l’icône du lecteur.</span><span class="sxs-lookup"><span data-stu-id="3f384-181">To run AutoRun manually, either right-click the drive icon and select **AutoPlay** from the shortcut menu or double-click the drive icon.</span></span> <span data-ttu-id="3f384-182">Si les pilotes ne sont pas compatibles avec l’exécution automatique, le menu contextuel n’a pas d’élément de **lecture automatique** et l’exécution automatique ne peut pas être démarrée.</span><span class="sxs-lookup"><span data-stu-id="3f384-182">If the drivers are not AutoRun-compatible, the shortcut menu will not have an **AutoPlay** item and AutoRun cannot be started.</span></span>

<span data-ttu-id="3f384-183">Les pilotes compatibles avec l’exécution automatique sont fournis avec des lecteurs de disque amovibles, ainsi que d’autres types de supports amovibles, tels que les cartes CompactFlash.</span><span class="sxs-lookup"><span data-stu-id="3f384-183">AutoRun-compatible drivers are provided with some removable disk drives, as well as some other types of removable media such as CompactFlash cards.</span></span> <span data-ttu-id="3f384-184">AutoRun fonctionne également avec les lecteurs réseau mappés à une lettre de lecteur avec l’Explorateur Windows ou montés avec la [console MMC (Microsoft Management Console)](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page).</span><span class="sxs-lookup"><span data-stu-id="3f384-184">AutoRun also works with network drives that are mapped to a drive letter with Windows Explorer or mounted with the [Microsoft Management Console (MMC)](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page).</span></span> <span data-ttu-id="3f384-185">Comme pour le matériel monté, un lecteur réseau monté doit avoir un fichier autorun. inf dans son répertoire racine et ne doit pas être désactivé par le biais du [Registre](#using-the-registry-to-disable-autorun).</span><span class="sxs-lookup"><span data-stu-id="3f384-185">As with mounted hardware, a mounted network drive must have an Autorun.inf file in its root directory, and must not be disabled through the [registry](#using-the-registry-to-disable-autorun).</span></span>

 

 
