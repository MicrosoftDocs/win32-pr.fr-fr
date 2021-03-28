---
description: Cette rubrique est une référence pour les entrées qui peuvent être utilisées dans un fichier autorun. inf. Une entrée se compose d’une clé et d’une valeur.
ms.assetid: 5b8fd559-b1be-4552-a7be-19ad107855af
title: Entrées autorun. inf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56d93244f177d107bddc720fab1d0c774fd94735
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201280"
---
# <a name="autoruninf-entries"></a><span data-ttu-id="7ae17-104">Entrées autorun. inf</span><span class="sxs-lookup"><span data-stu-id="7ae17-104">Autorun.inf Entries</span></span>

<span data-ttu-id="7ae17-105">Cette rubrique est une référence pour les entrées qui peuvent être utilisées dans un fichier autorun. inf.</span><span class="sxs-lookup"><span data-stu-id="7ae17-105">This topic is a reference for the entries that can be used in an Autorun.inf file.</span></span> <span data-ttu-id="7ae17-106">Une entrée se compose d’une clé et d’une valeur.</span><span class="sxs-lookup"><span data-stu-id="7ae17-106">An entry consists of a key and a value.</span></span>

-   <span data-ttu-id="7ae17-107">[\[Clés d’exécution automatique \]](#autorun-keys)</span><span class="sxs-lookup"><span data-stu-id="7ae17-107">[\[AutoRun\] Keys](#autorun-keys)</span></span>
    -   [<span data-ttu-id="7ae17-108">action</span><span class="sxs-lookup"><span data-stu-id="7ae17-108">action</span></span>](#parameters)
    -   [<span data-ttu-id="7ae17-109">CustomEvent</span><span class="sxs-lookup"><span data-stu-id="7ae17-109">CustomEvent</span></span>](#customevent)
    -   [<span data-ttu-id="7ae17-110">située</span><span class="sxs-lookup"><span data-stu-id="7ae17-110">icon</span></span>](#parameters)
    -   [<span data-ttu-id="7ae17-111">label</span><span class="sxs-lookup"><span data-stu-id="7ae17-111">label</span></span>](#parameters)
    -   [<span data-ttu-id="7ae17-112">open</span><span class="sxs-lookup"><span data-stu-id="7ae17-112">open</span></span>](#parameters)
    -   [<span data-ttu-id="7ae17-113">UseAutoPlay</span><span class="sxs-lookup"><span data-stu-id="7ae17-113">UseAutoPlay</span></span>](#parameters)
    -   [<span data-ttu-id="7ae17-114">ShellExecute</span><span class="sxs-lookup"><span data-stu-id="7ae17-114">shellexecute</span></span>](#shellexecute)
    -   [<span data-ttu-id="7ae17-115">Shell</span><span class="sxs-lookup"><span data-stu-id="7ae17-115">shell</span></span>](#autoruninf-entries)
    -   [<span data-ttu-id="7ae17-116">verbe de Shell \\</span><span class="sxs-lookup"><span data-stu-id="7ae17-116">shell\\verb</span></span>](#shellverb)
-   <span data-ttu-id="7ae17-117">[\[Clés de contenu \]](#content-keys)</span><span class="sxs-lookup"><span data-stu-id="7ae17-117">[\[Content\] Keys](#content-keys)</span></span>
-   <span data-ttu-id="7ae17-118">[\[\]Clés ExclusiveContentPaths](#exclusivecontentpaths-keys)</span><span class="sxs-lookup"><span data-stu-id="7ae17-118">[\[ExclusiveContentPaths\] Keys](#exclusivecontentpaths-keys)</span></span>
-   <span data-ttu-id="7ae17-119">[\[\]Clés IgnoreContentPaths](#ignorecontentpaths-keys)</span><span class="sxs-lookup"><span data-stu-id="7ae17-119">[\[IgnoreContentPaths\] Keys](#ignorecontentpaths-keys)</span></span>
-   <span data-ttu-id="7ae17-120">[\[\]Clés DeviceInstall](#deviceinstall-keys)</span><span class="sxs-lookup"><span data-stu-id="7ae17-120">[\[DeviceInstall\] Keys](#deviceinstall-keys)</span></span>
    -   [<span data-ttu-id="7ae17-121">DriverPath</span><span class="sxs-lookup"><span data-stu-id="7ae17-121">DriverPath</span></span>](#driverpath)

## <a name="autorun-keys"></a><span data-ttu-id="7ae17-122">\[Clés d’exécution automatique \]</span><span class="sxs-lookup"><span data-stu-id="7ae17-122">\[AutoRun\] Keys</span></span>

-   [<span data-ttu-id="7ae17-123">action</span><span class="sxs-lookup"><span data-stu-id="7ae17-123">action</span></span>](#parameters)
-   [<span data-ttu-id="7ae17-124">CustomEvent</span><span class="sxs-lookup"><span data-stu-id="7ae17-124">CustomEvent</span></span>](#customevent)
-   [<span data-ttu-id="7ae17-125">située</span><span class="sxs-lookup"><span data-stu-id="7ae17-125">icon</span></span>](#parameters)
-   [<span data-ttu-id="7ae17-126">label</span><span class="sxs-lookup"><span data-stu-id="7ae17-126">label</span></span>](#parameters)
-   [<span data-ttu-id="7ae17-127">open</span><span class="sxs-lookup"><span data-stu-id="7ae17-127">open</span></span>](#parameters)
-   [<span data-ttu-id="7ae17-128">UseAutoPlay</span><span class="sxs-lookup"><span data-stu-id="7ae17-128">UseAutoPlay</span></span>](#parameters)
-   [<span data-ttu-id="7ae17-129">ShellExecute</span><span class="sxs-lookup"><span data-stu-id="7ae17-129">shellexecute</span></span>](#shellexecute)
-   [<span data-ttu-id="7ae17-130">Shell</span><span class="sxs-lookup"><span data-stu-id="7ae17-130">shell</span></span>](#autoruninf-entries)
-   [<span data-ttu-id="7ae17-131">verbe de Shell \\</span><span class="sxs-lookup"><span data-stu-id="7ae17-131">shell\\verb</span></span>](#shellverb)

### <a name="action"></a><span data-ttu-id="7ae17-132">action</span><span class="sxs-lookup"><span data-stu-id="7ae17-132">action</span></span>

<span data-ttu-id="7ae17-133">L’entrée **action** spécifie le texte utilisé dans la boîte de dialogue d’exécution automatique pour le gestionnaire représentant le programme spécifié dans l’entrée [Open](#parameters) ou [ShellExecute](#shellexecute) du fichier autorun. inf du média.</span><span class="sxs-lookup"><span data-stu-id="7ae17-133">The **action** entry specifies the text that is used in the Autoplay dialog for the handler representing the program specified in the [open](#parameters) or [shellexecute](#shellexecute) entry in the media's Autorun.inf file.</span></span> <span data-ttu-id="7ae17-134">La valeur peut être exprimée sous forme de texte ou de ressource stockée dans un fichier binaire.</span><span class="sxs-lookup"><span data-stu-id="7ae17-134">The value can be expressed as either text or as a resource stored in a binary.</span></span>


```
action=ActionText
```




```
action=@[filepath\]filename,-resourceID
```



### <a name="parameters"></a><span data-ttu-id="7ae17-135">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7ae17-135">Parameters</span></span>

-   <span data-ttu-id="7ae17-136">*ActionText*</span><span class="sxs-lookup"><span data-stu-id="7ae17-136">*ActionText*</span></span>

    <span data-ttu-id="7ae17-137">Texte utilisé dans la boîte de dialogue d’exécution automatique pour le gestionnaire représentant le programme spécifié dans l’entrée [Open](#parameters) ou [ShellExecute](#shellexecute) du fichier autorun. inf du média.</span><span class="sxs-lookup"><span data-stu-id="7ae17-137">Text that is used in the Autoplay dialog for the handler representing the program specified in the [open](#parameters) or [shellexecute](#shellexecute) entry in the media's Autorun.inf file.</span></span>

-   <span data-ttu-id="7ae17-138">*cheminfichier*</span><span class="sxs-lookup"><span data-stu-id="7ae17-138">*filepath*</span></span>

    <span data-ttu-id="7ae17-139">Chaîne qui contient le chemin d’accès complet du répertoire qui contient le fichier binaire contenant la chaîne.</span><span class="sxs-lookup"><span data-stu-id="7ae17-139">A string that contains the fully qualified path of the directory that contains the binary file containing the string.</span></span> <span data-ttu-id="7ae17-140">Si aucun chemin d’accès n’est spécifié, le fichier doit se trouver dans le répertoire racine du lecteur.</span><span class="sxs-lookup"><span data-stu-id="7ae17-140">If no path is specified, the file must be in the drive's root directory.</span></span>

-   <span data-ttu-id="7ae17-141">*extension*</span><span class="sxs-lookup"><span data-stu-id="7ae17-141">*filename*</span></span>

    <span data-ttu-id="7ae17-142">Chaîne qui contient le nom du fichier binaire.</span><span class="sxs-lookup"><span data-stu-id="7ae17-142">A string that contains the binary file's name.</span></span>

-   <span data-ttu-id="7ae17-143">*IDRessource*</span><span class="sxs-lookup"><span data-stu-id="7ae17-143">*resourceID*</span></span>

    <span data-ttu-id="7ae17-144">ID de la chaîne dans le fichier binaire.</span><span class="sxs-lookup"><span data-stu-id="7ae17-144">The ID of the string within the binary file.</span></span>

### <a name="remarks"></a><span data-ttu-id="7ae17-145">Notes</span><span class="sxs-lookup"><span data-stu-id="7ae17-145">Remarks</span></span>

<span data-ttu-id="7ae17-146">La clé d' **action** est utilisée uniquement dans Windows XP Service Pack 2 (SP2) ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="7ae17-146">The **action** key is only used in Windows XP Service Pack 2 (SP2) or later.</span></span> <span data-ttu-id="7ae17-147">Il est uniquement pris en charge pour les lecteurs de type lecteur \_ amovible et lecteur \_ fixe.</span><span class="sxs-lookup"><span data-stu-id="7ae17-147">It is only supported for drives of type DRIVE\_REMOVABLE and DRIVE\_FIXED.</span></span> <span data-ttu-id="7ae17-148">Dans le cas d’un disque \_ amovible, la clé d' **action** est requise.</span><span class="sxs-lookup"><span data-stu-id="7ae17-148">In the case of DRIVE\_REMOVABLE, the **action** key is required.</span></span> <span data-ttu-id="7ae17-149">Une commande d' **action** dans le fichier autorun. inf d’un CD audio ou d’un DVD de film est ignorée, et ces médias continuent de se comporter comme dans Windows XP Service Pack 1 (SP1) et versions antérieures.</span><span class="sxs-lookup"><span data-stu-id="7ae17-149">An **action** command in the Autorun.inf file of an audio CD or movie DVD is ignored, and these media continue to behave as in Windows XP Service Pack 1 (SP1) and earlier.</span></span>

<span data-ttu-id="7ae17-150">La chaîne affichée dans la boîte de dialogue d’exécution automatique est construite en combinant le texte spécifié dans l’entrée d' **action** avec le texte codé en dur du fournisseur, fourni par l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="7ae17-150">The string displayed in the Autoplay dialog is constructed by combining the text specified in the **action** entry with hard-coded text naming the provider, provided by the Shell.</span></span> <span data-ttu-id="7ae17-151">L' [icône](#parameters) s’affiche en regard de celle-ci.</span><span class="sxs-lookup"><span data-stu-id="7ae17-151">The [icon](#parameters) is displayed next to it.</span></span> <span data-ttu-id="7ae17-152">Cette entrée apparaît toujours comme première option dans la boîte de dialogue d’exécution automatique et est sélectionnée par défaut.</span><span class="sxs-lookup"><span data-stu-id="7ae17-152">This entry always appears as the first option in the Autoplay dialog and is selected by default.</span></span> <span data-ttu-id="7ae17-153">Si l’utilisateur accepte l’option, l’application spécifiée par l’entrée [Open](#parameters) ou [ShellExecute](#shellexecute) dans le fichier autorun. inf du média est lancée.</span><span class="sxs-lookup"><span data-stu-id="7ae17-153">If the user accepts the option, the application specified by the [open](#parameters) or [shellexecute](#shellexecute) entry in the media's Autorun.inf file is launched.</span></span> <span data-ttu-id="7ae17-154">L’option **toujours effectuer l’action sélectionnée** n’est pas disponible dans cette situation.</span><span class="sxs-lookup"><span data-stu-id="7ae17-154">The **Always do the selected action** option is not available in this situation.</span></span>

<span data-ttu-id="7ae17-155">Les touches [action](#parameters) et [icône](#parameters) définissent ensemble la représentation de l’application qui est visible par l’utilisateur final dans la boîte de dialogue d’exécution automatique.</span><span class="sxs-lookup"><span data-stu-id="7ae17-155">The [action](#parameters) and [icon](#parameters) keys together define the representation of the application that is seen by the end user in the Autoplay dialog.</span></span> <span data-ttu-id="7ae17-156">Ils doivent être composés de manière à ce que les utilisateurs puissent facilement les identifier.</span><span class="sxs-lookup"><span data-stu-id="7ae17-156">They should be composed in such a way that users can easily identify them.</span></span> <span data-ttu-id="7ae17-157">Ils doivent indiquer l’application à exécuter, la société qui l’a créée et toute marque associée.</span><span class="sxs-lookup"><span data-stu-id="7ae17-157">They should indicate the application to be run, the company that created it, and any associated branding.</span></span>

<span data-ttu-id="7ae17-158">Pour la compatibilité descendante, l’entrée d' **action** est facultative pour les appareils de type Drive \_ fixed.</span><span class="sxs-lookup"><span data-stu-id="7ae17-158">For backward compatibility, the **action** entry is optional for devices of type DRIVE\_FIXED.</span></span> <span data-ttu-id="7ae17-159">Pour ce type, une entrée par défaut est utilisée dans la boîte de dialogue d’exécution automatique si aucune entrée d' **action** n’est présente dans le fichier autorun. inf.</span><span class="sxs-lookup"><span data-stu-id="7ae17-159">For this type, a default entry is used in the Autoplay dialog if no **action** entry is present in the Autorun.inf file.</span></span>

<span data-ttu-id="7ae17-160">L’entrée d' **action** est obligatoire pour les appareils de type lecteur \_ amovible, qui jusqu’à présent ne disposent pas de la prise en charge de autorun. inf.</span><span class="sxs-lookup"><span data-stu-id="7ae17-160">The **action** entry is mandatory for devices of type DRIVE\_REMOVABLE, which until now did not have Autorun.inf support.</span></span> <span data-ttu-id="7ae17-161">Si aucune entrée d' **action** n’est présente, la boîte de dialogue d’exécution automatique s’affiche, mais sans option pour lancer le contenu supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="7ae17-161">If no **action** entry is present, the Autoplay dialog is displayed but with no option to launch the additional content.</span></span>

### <a name="customevent"></a><span data-ttu-id="7ae17-162">CustomEvent</span><span class="sxs-lookup"><span data-stu-id="7ae17-162">CustomEvent</span></span>

<span data-ttu-id="7ae17-163">L’entrée **CustomEvent** spécifie un événement de contenu de lecture automatique personnalisé.</span><span class="sxs-lookup"><span data-stu-id="7ae17-163">The **CustomEvent** entry specifies a custom AutoPlay content event.</span></span>


```
CustomEvent=CustomEventName
```



### <a name="parameters"></a><span data-ttu-id="7ae17-164">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7ae17-164">Parameters</span></span>

-   <span data-ttu-id="7ae17-165">*CustomEventName*</span><span class="sxs-lookup"><span data-stu-id="7ae17-165">*CustomEventName*</span></span>

    <span data-ttu-id="7ae17-166">Chaîne de texte contenant le nom de l’événement de contenu de lecture automatique.</span><span class="sxs-lookup"><span data-stu-id="7ae17-166">A text string containing the name of the AutoPlay content event.</span></span> <span data-ttu-id="7ae17-167">Le nom ne doit pas comporter plus de 100 caractères alphanumériques.</span><span class="sxs-lookup"><span data-stu-id="7ae17-167">The name must be no more than 100 alphanumeric characters.</span></span>

### <a name="remarks"></a><span data-ttu-id="7ae17-168">Notes</span><span class="sxs-lookup"><span data-stu-id="7ae17-168">Remarks</span></span>

<span data-ttu-id="7ae17-169">Vous pouvez inclure un nom d’événement personnalisé dans le fichier autorun. inf d’un volume.</span><span class="sxs-lookup"><span data-stu-id="7ae17-169">You can include a custom event name in the Autorun.inf file of a volume.</span></span> <span data-ttu-id="7ae17-170">Lorsque l’exécution automatique invite l’utilisateur à utiliser une application avec le volume, il affiche uniquement les applications qui ont été inscrites pour le nom d’événement personnalisé spécifié.</span><span class="sxs-lookup"><span data-stu-id="7ae17-170">When AutoPlay prompts the user for an application to use with the volume, it displays only applications that have registered for the specified custom event name.</span></span> <span data-ttu-id="7ae17-171">Pour plus d’informations sur la façon dont vous pouvez inscrire une application en tant que gestionnaire pour votre événement de contenu de lecture automatique personnalisé, consultez [lancement automatique avec exécution](/previous-versions/windows/apps/hh452731(v=win.10)) automatique ou [inscription d’un gestionnaire d’événements](how-to-register-an-event-handler.md).</span><span class="sxs-lookup"><span data-stu-id="7ae17-171">For information on how you can register an application as a handler for your custom AutoPlay content event, see [Auto-launching with AutoPlay](/previous-versions/windows/apps/hh452731(v=win.10)) or [How to Register an Event Handler](how-to-register-an-event-handler.md).</span></span>

<span data-ttu-id="7ae17-172">L’exemple suivant spécifie la valeur « MyContentOnArrival » comme nouvel événement de contenu de lecture automatique.</span><span class="sxs-lookup"><span data-stu-id="7ae17-172">The following example specifies the value "MyContentOnArrival" as a new AutoPlay content event.</span></span>


```
CustomEvent=MyContentOnArrival
```



### <a name="icon"></a><span data-ttu-id="7ae17-173">icon</span><span class="sxs-lookup"><span data-stu-id="7ae17-173">icon</span></span>

<span data-ttu-id="7ae17-174">L’entrée d' **icône** spécifie une icône qui représente le lecteur avec activation automatique dans l’interface utilisateur Windows.</span><span class="sxs-lookup"><span data-stu-id="7ae17-174">The **icon** entry specifies an icon which represents the AutoRun-enabled drive in the Windows user interface.</span></span>


```
icon=iconfilename[,index]
```



### <a name="parameters"></a><span data-ttu-id="7ae17-175">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7ae17-175">Parameters</span></span>

-   <span data-ttu-id="7ae17-176">*argument*</span><span class="sxs-lookup"><span data-stu-id="7ae17-176">*iconfilename*</span></span>

    <span data-ttu-id="7ae17-177">Nom d’un fichier. ico,. bmp,. exe ou. dll contenant les informations sur l’icône.</span><span class="sxs-lookup"><span data-stu-id="7ae17-177">Name of an .ico, .bmp, .exe, or .dll file containing the icon information.</span></span> <span data-ttu-id="7ae17-178">Si un fichier contient plusieurs icônes, vous devez également spécifier un index de base zéro de l’icône.</span><span class="sxs-lookup"><span data-stu-id="7ae17-178">If a file contains more than one icon, you must also specify zero-based index of the icon.</span></span>

### <a name="remarks"></a><span data-ttu-id="7ae17-179">Notes</span><span class="sxs-lookup"><span data-stu-id="7ae17-179">Remarks</span></span>

<span data-ttu-id="7ae17-180">L’icône, ainsi que l’étiquette, représente le lecteur compatible avec la fonction AutoRun dans l’interface utilisateur Windows.</span><span class="sxs-lookup"><span data-stu-id="7ae17-180">The icon, together with the label, represents the AutoRun-enabled drive in the Windows user interface.</span></span> <span data-ttu-id="7ae17-181">Par exemple, dans l’Explorateur Windows, le lecteur est représenté par cette icône au lieu de l’icône de lecteur standard.</span><span class="sxs-lookup"><span data-stu-id="7ae17-181">For instance, in Windows Explorer, the drive is represented by this icon instead of the standard drive icon.</span></span> <span data-ttu-id="7ae17-182">Le fichier de l’icône doit se trouver dans le même répertoire que le fichier spécifié par la commande [ouvrir](#parameters) .</span><span class="sxs-lookup"><span data-stu-id="7ae17-182">The icon's file must be in the same directory as the file specified by the [open](#parameters) command.</span></span>

<span data-ttu-id="7ae17-183">L’exemple suivant spécifie la deuxième icône dans le fichier MyProg.exe.</span><span class="sxs-lookup"><span data-stu-id="7ae17-183">The following example specifies the second icon in the MyProg.exe file.</span></span>


```
icon=MyProg.exe,1
```



### <a name="label"></a><span data-ttu-id="7ae17-184">label</span><span class="sxs-lookup"><span data-stu-id="7ae17-184">label</span></span>

<span data-ttu-id="7ae17-185">L’entrée d' **étiquette** spécifie une étiquette de texte qui représente le lecteur avec activation automatique dans l’interface utilisateur Windows.</span><span class="sxs-lookup"><span data-stu-id="7ae17-185">The **label** entry specifies a text label which represents the AutoRun-enabled drive in the Windows user interface.</span></span>


```
label=LabelText
```



### <a name="parameters"></a><span data-ttu-id="7ae17-186">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7ae17-186">Parameters</span></span>

-   <span data-ttu-id="7ae17-187">*LabelText*</span><span class="sxs-lookup"><span data-stu-id="7ae17-187">*LabelText*</span></span>

    <span data-ttu-id="7ae17-188">Chaîne de texte contenant l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="7ae17-188">A text string containing the label.</span></span> <span data-ttu-id="7ae17-189">Il peut contenir des espaces et ne doit pas dépasser 32 caractères.</span><span class="sxs-lookup"><span data-stu-id="7ae17-189">It can contain spaces and should be no longer than 32 characters.</span></span>

> [!Note]  
> <span data-ttu-id="7ae17-190">Il est possible de placer une valeur dans le paramètre **LabelText** qui dépasse 32 caractères et de ne pas recevoir de message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="7ae17-190">It is possible to put a value in the **LabelText** parameter which exceeds 32 characters and receive no error message.</span></span> <span data-ttu-id="7ae17-191">Toutefois, le système affiche uniquement les 32 premiers caractères.</span><span class="sxs-lookup"><span data-stu-id="7ae17-191">However, the system only displays the first 32 characters.</span></span> <span data-ttu-id="7ae17-192">Les caractères qui suivent le 32e sont tronqués et ne s’affichent pas.</span><span class="sxs-lookup"><span data-stu-id="7ae17-192">Any characters after the 32nd are truncated and not displayed.</span></span> <span data-ttu-id="7ae17-193">Par exemple, si le **LabelText** est le suivant : label = « ce CD est conçu pour être le CD de musique ultime ».</span><span class="sxs-lookup"><span data-stu-id="7ae17-193">For example, if the **LabelText** is as follows: label="This CD is designed to be the ultimate music CD."</span></span> <span data-ttu-id="7ae17-194">les éléments suivants s’affichent : « ce CD est conçu pour être le UL ».</span><span class="sxs-lookup"><span data-stu-id="7ae17-194">the following will be displayed, "This CD is designed to be the ul".</span></span>

 

### <a name="remarks"></a><span data-ttu-id="7ae17-195">Notes</span><span class="sxs-lookup"><span data-stu-id="7ae17-195">Remarks</span></span>

<span data-ttu-id="7ae17-196">L’étiquette, ainsi qu’une icône, représente le lecteur prenant en charge l’exécution automatique dans l’interface utilisateur Windows.</span><span class="sxs-lookup"><span data-stu-id="7ae17-196">The label, together with an icon, represents the AutoRun-enabled drive in the Windows user interface.</span></span>

<span data-ttu-id="7ae17-197">L’exemple suivant spécifie la valeur « mon étiquette de lecteur » comme étiquette du lecteur.</span><span class="sxs-lookup"><span data-stu-id="7ae17-197">The following example specifies the value "My Drive Label" as the drive's label.</span></span>


```
label=My Drive Label
```



### <a name="open"></a><span data-ttu-id="7ae17-198">ouvert</span><span class="sxs-lookup"><span data-stu-id="7ae17-198">open</span></span>

<span data-ttu-id="7ae17-199">L’entrée **ouverte** spécifie le chemin d’accès et le nom de fichier de l’application que l’exécution automatique lance lorsqu’un utilisateur insère un disque dans le lecteur.</span><span class="sxs-lookup"><span data-stu-id="7ae17-199">The **open** entry specifies the path and file name of the application that AutoRun launches when a user inserts a disc in the drive.</span></span>


```
open=[exepath\]exefile [param1 [param2] ...] 
```



### <a name="parameters"></a><span data-ttu-id="7ae17-200">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7ae17-200">Parameters</span></span>

-   <span data-ttu-id="7ae17-201">*exefile*</span><span class="sxs-lookup"><span data-stu-id="7ae17-201">*exefile*</span></span>

    <span data-ttu-id="7ae17-202">Chemin complet d’un fichier exécutable qui s’exécute lors de l’insertion du CD.</span><span class="sxs-lookup"><span data-stu-id="7ae17-202">Fully qualified path of an executable file that runs when the CD is inserted.</span></span> <span data-ttu-id="7ae17-203">Si seul un nom de fichier est spécifié, il doit se trouver dans le répertoire racine du lecteur.</span><span class="sxs-lookup"><span data-stu-id="7ae17-203">If only a file name is specified, it must be in drive's root directory.</span></span> <span data-ttu-id="7ae17-204">Pour rechercher le fichier dans un sous-répertoire, vous devez spécifier un chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="7ae17-204">To locate the file in a subdirectory, you must specify a path.</span></span> <span data-ttu-id="7ae17-205">Vous pouvez également inclure un ou plusieurs paramètres de ligne de commande à passer à l’application de démarrage.</span><span class="sxs-lookup"><span data-stu-id="7ae17-205">You can also include one or more command-line parameters to pass to the startup application.</span></span>

### <a name="useautoplay"></a><span data-ttu-id="7ae17-206">UseAutoPlay</span><span class="sxs-lookup"><span data-stu-id="7ae17-206">UseAutoPlay</span></span>

<span data-ttu-id="7ae17-207">Sur Windows XP, l’entrée **UseAutoPlay** spécifie que l’exécution automatique doit être utilisée à la place de l’exécution automatique.</span><span class="sxs-lookup"><span data-stu-id="7ae17-207">On Windows XP, the **UseAutoPlay** entry specifies that AutoPlay should be used instead of AutoRun.</span></span>

<span data-ttu-id="7ae17-208">Sur Windows Vista et versions ultérieures, cette entrée entraîne la suppression des actions spécifiées pour l’exécution automatique (à l’aide des entrées **Open** ou **ShellExecute** ) à partir de la boîte de dialogue d’exécution automatique.</span><span class="sxs-lookup"><span data-stu-id="7ae17-208">On Windows Vista and later, this entry causes any actions specified for AutoRun (by using either the **open** or **shellexecute** entries) to be suppressed from the AutoPlay dialog.</span></span> <span data-ttu-id="7ae17-209">Cette entrée n’a aucun effet sur les versions de Windows antérieures à Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7ae17-209">This entry has no effect on versions of Windows earlier than Windows XP.</span></span>

<span data-ttu-id="7ae17-210">Sur Windows 8 et versions ultérieures, la spécification de la valeur 0 désactive l’exécution automatique pour cet appareil.</span><span class="sxs-lookup"><span data-stu-id="7ae17-210">On Windows 8 and later, specifying a value of 0 will disable autoplay for this device.</span></span>

### <a name="parameters"></a><span data-ttu-id="7ae17-211">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7ae17-211">Parameters</span></span>

<span data-ttu-id="7ae17-212">Pour utiliser cette option, ajoutez une entrée pour **UseAutoPlay** au fichier autorun. inf et affectez à l’entrée la valeur 1.</span><span class="sxs-lookup"><span data-stu-id="7ae17-212">To use this option, add an entry for **UseAutoPlay** to the Autorun.inf file and set the entry equal to 1.</span></span> <span data-ttu-id="7ae17-213">Aucune autre valeur n’est prise en charge sur les versions de Windows antérieures à Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7ae17-213">No other value is supported on versions of Windows earlier than Windows 8.</span></span>

<span data-ttu-id="7ae17-214">Sur Windows 8 et versions ultérieures, spécifiez la valeur 0 pour désactiver l’exécution automatique pour cet appareil.</span><span class="sxs-lookup"><span data-stu-id="7ae17-214">On Windows 8 and later, specify a value of 0 to disable autoplay for this device.</span></span>


```
UseAutoPlay=1
```



### <a name="remarks"></a><span data-ttu-id="7ae17-215">Notes</span><span class="sxs-lookup"><span data-stu-id="7ae17-215">Remarks</span></span>

<span data-ttu-id="7ae17-216">Actuellement, **UseAutoPlay** est uniquement applicable sur Windows XP ou version ultérieure et sur un lecteur que [**GetDriveType**](/windows/win32/api/fileapi/nf-fileapi-getdrivetypea) détermine comme étant du type **lecteur \_ cdrom**.</span><span class="sxs-lookup"><span data-stu-id="7ae17-216">Currently, **UseAutoPlay** is applicable only on Windows XP or later and only on a drive that [**GetDriveType**](/windows/win32/api/fileapi/nf-fileapi-getdrivetypea) determines to be of type **DRIVE\_CDROM**.</span></span>

<span data-ttu-id="7ae17-217">Lorsque **UseAutoPlay** est utilisé, toute action spécifiée par les entrées **Open** ou **ShellExecute** dans autorun. inf est ignorée sur Windows XP et omise de la boîte de dialogue d’exécution automatique sur Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7ae17-217">When **UseAutoPlay** is used, any action specified by the **open** or **shellexecute** entries in Autorun.inf is ignored on Windows XP and omitted from the AutoPlay dialog on Windows Vista.</span></span>

<span data-ttu-id="7ae17-218">AutoRun est généralement utilisé pour exécuter ou charger automatiquement un contenu sur le média inséré, tandis que la lecture automatique présente une boîte de dialogue qui comprend une liste des actions pertinentes qui peuvent être exécutées et permet à l’utilisateur de choisir l’action à entreprendre.</span><span class="sxs-lookup"><span data-stu-id="7ae17-218">AutoRun is typically used to automatically run or load something contained on the inserted media, whereas AutoPlay presents a dialog that includes a list of relevant actions that may be taken and enables the user to choose which action to take.</span></span> <span data-ttu-id="7ae17-219">Pour plus d’informations sur la différence entre l’exécution automatique et l’exécution automatique, consultez [création d’une application de CD-ROM compatible avec l’exécution automatique](autoplay.md) et [utilisation et configuration de l’exécution automatique](autoplay2k-using.md), respectivement.</span><span class="sxs-lookup"><span data-stu-id="7ae17-219">For more information about the difference between AutoRun and AutoPlay, see [Creating an AutoRun-enabled CD-ROM Application](autoplay.md) and [Using and Configuring AutoPlay](autoplay2k-using.md), respectively.</span></span>

### <a name="usage-example"></a><span data-ttu-id="7ae17-220">Exemple d'utilisation</span><span class="sxs-lookup"><span data-stu-id="7ae17-220">Usage Example</span></span>

<span data-ttu-id="7ae17-221">Un CD contient trois fichiers : autorun. inf, Readme.txt et Music. WMA.</span><span class="sxs-lookup"><span data-stu-id="7ae17-221">A CD contains three files: Autorun.inf, Readme.txt, and Music.wma.</span></span> <span data-ttu-id="7ae17-222">Selon la version de Windows utilisée et les options spécifiées dans autorun. inf, le CD peut être géré par l’exécution automatique ou l’exécution automatique lorsqu’il est inséré (en supposant que l’exécution automatique/exécution automatique est activée pour le lecteur dans lequel le CD est inséré).</span><span class="sxs-lookup"><span data-stu-id="7ae17-222">Depending on the version of Windows in use and options specified in Autorun.inf, the CD may be handled by either AutoRun or AutoPlay when it is inserted (assuming AutoRun/AutoPlay is enabled for the drive into which the CD is inserted).</span></span>

<span data-ttu-id="7ae17-223">Tout d’abord, envisagez d’utiliser un fichier autorun. inf avec le contenu suivant, en notant que **UseAutoPlay = 1** n’est pas spécifié :</span><span class="sxs-lookup"><span data-stu-id="7ae17-223">First, consider an Autorun.inf file with the following contents, noting that **UseAutoPlay=1** is not specified:</span></span>


```
[AutoRun]
shellexecute="Readme.txt"
```



<span data-ttu-id="7ae17-224">L’action effectuée par l’interpréteur de commandes lorsque ce CD est inséré dépend de la version de Windows utilisée :</span><span class="sxs-lookup"><span data-stu-id="7ae17-224">The action taken by the Shell when this CD is inserted depends on the version of Windows in use:</span></span>

-   <span data-ttu-id="7ae17-225">Sur Windows XP ou version antérieure, ce CD est géré par l’exécution automatique lorsqu’il est inséré.</span><span class="sxs-lookup"><span data-stu-id="7ae17-225">On Windows XP or earlier, this CD is handled by AutoRun when it is inserted.</span></span> <span data-ttu-id="7ae17-226">Dans ce cas, l’entrée **ShellExecute** est lue et l’interpréteur de commandes appelle le gestionnaire de fichiers associé aux fichiers. txt ; en général, cela ouvre Readme.txt dans le bloc-notes.</span><span class="sxs-lookup"><span data-stu-id="7ae17-226">In this case, the **shellexecute** entry is read, and the Shell invokes the file handler associated with .txt files; typically this would open Readme.txt in Notepad.</span></span>
-   <span data-ttu-id="7ae17-227">Sur Windows Vista, la présence d’un fichier autorun. inf avec une entrée **ShellExecute** entraîne l’identification du support en tant que type d’exécution automatique « logiciels et jeux ».</span><span class="sxs-lookup"><span data-stu-id="7ae17-227">On Windows Vista, the presence of an Autorun.inf file with a **shellexecute** entry causes the media to be identified as AutoPlay type "Software and games".</span></span> <span data-ttu-id="7ae17-228">Dans ce cas, l’utilisateur reçoit une boîte de dialogue d’exécution automatique qui comprend l’action spécifiée par l’entrée **ShellExecute** (présentée sous la forme « charger Readme.txt » dans la boîte de dialogue), ainsi que les actions par défaut associées aux médias de type « logiciels et jeux ».</span><span class="sxs-lookup"><span data-stu-id="7ae17-228">In this case the user is presented with an AutoPlay dialog that includes the action specified by the **shellexecute** entry (presented as "Load Readme.txt" in the dialog), along with default actions associated with media of type "Software and games".</span></span>

<span data-ttu-id="7ae17-229">Pour indiquer que l’exécution automatique doit être utilisée au lieu de l’exécution automatique sur Windows XP, et que l’action spécifiée par l’entrée ShellExecute d’AutoRun doit être supprimée de la boîte de dialogue d’exécution automatique sous Windows Vista, insérez **UseAutoPlay** dans le fichier autorun. inf comme suit :</span><span class="sxs-lookup"><span data-stu-id="7ae17-229">To indicate that AutoPlay should be used rather than AutoRun on Windows XP, and that the action specified by the AutoRun shellexecute entry should be suppressed from the AutoPlay dialog on Windows Vista, insert **UseAutoPlay** into the Autorun.inf file as follows:</span></span>


```
[AutoRun]
shellexecute="Readme.txt"
UseAutoPlay=1
```



<span data-ttu-id="7ae17-230">Là encore, l’action effectuée par l’interpréteur de commandes lorsque ce CD est inséré dépend de la version de Windows utilisée.</span><span class="sxs-lookup"><span data-stu-id="7ae17-230">Once again, the action taken by the Shell when this CD is inserted depends on the version of Windows in use.</span></span>

-   <span data-ttu-id="7ae17-231">Dans les versions de Windows antérieures à Windows XP, l’exécution automatique est toujours utilisée et l’action spécifiée par **ShellExecute** est effectuée, comme décrit précédemment.</span><span class="sxs-lookup"><span data-stu-id="7ae17-231">On versions of Windows earlier than Windows XP, AutoRun is still used and the action specified by **shellexecute** is performed, as described previously.</span></span> <span data-ttu-id="7ae17-232">(Notez que seule l’exécution automatique est disponible sur les versions de Windows antérieures à Windows XP.)</span><span class="sxs-lookup"><span data-stu-id="7ae17-232">(Note that only AutoRun is available on versions of Windows earlier than Windows XP.)</span></span>
-   <span data-ttu-id="7ae17-233">Sur Windows XP, l’entrée **UseAutoPlay** provoque l’utilisation de la lecture automatique à la place de l’exécution automatique.</span><span class="sxs-lookup"><span data-stu-id="7ae17-233">On Windows XP, the **UseAutoPlay** entry causes AutoPlay to be used in place of AutoRun.</span></span> <span data-ttu-id="7ae17-234">Dans ce cas, l’exécution automatique détermine que le média contient un fichier Windows Media Audio (. WMA) et classe le contenu comme « fichiers musicaux ».</span><span class="sxs-lookup"><span data-stu-id="7ae17-234">In this case, AutoPlay determines that the media contains a Windows Media Audio (.wma) file and categorizes the content as "Music files".</span></span> <span data-ttu-id="7ae17-235">L’utilisateur reçoit une boîte de dialogue d’exécution automatique contenant des gestionnaires enregistrés pour le type de média lecture automatique « fichiers de musique »; l’entrée ShellExecute d’AutoRun est ignorée.</span><span class="sxs-lookup"><span data-stu-id="7ae17-235">The user is presented with an AutoPlay dialog containing registered handlers for the "Music files" AutoPlay media type; the AutoRun shellexecute entry is ignored.</span></span>

### <a name="shellexecute"></a><span data-ttu-id="7ae17-236">ShellExecute</span><span class="sxs-lookup"><span data-stu-id="7ae17-236">shellexecute</span></span>

[<span data-ttu-id="7ae17-237">Version 5,0.</span><span class="sxs-lookup"><span data-stu-id="7ae17-237">Version 5.0.</span></span>](versions.md) <span data-ttu-id="7ae17-238">L’entrée **ShellExecute** spécifie un fichier d’application ou de données que l’exécution automatique utilisera pour appeler [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span><span class="sxs-lookup"><span data-stu-id="7ae17-238">The **shellexecute** entry specifies an application or data file that AutoRun will use to call [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span></span>


```
shellexecute=[filepath\]filename[param1, [param2]...] 
```



### <a name="parameters"></a><span data-ttu-id="7ae17-239">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7ae17-239">Parameters</span></span>

-   <span data-ttu-id="7ae17-240">*cheminfichier*</span><span class="sxs-lookup"><span data-stu-id="7ae17-240">*filepath*</span></span>

    <span data-ttu-id="7ae17-241">Chaîne qui contient le chemin d’accès complet du répertoire qui contient les données ou le fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="7ae17-241">A string that contains the fully qualified path of the directory that contains the data or executable file.</span></span> <span data-ttu-id="7ae17-242">Si aucun chemin d’accès n’est spécifié, le fichier doit se trouver dans le répertoire racine du lecteur.</span><span class="sxs-lookup"><span data-stu-id="7ae17-242">If no path is specified, the file must be in the drive's root directory.</span></span>

-   <span data-ttu-id="7ae17-243">*extension*</span><span class="sxs-lookup"><span data-stu-id="7ae17-243">*filename*</span></span>

    <span data-ttu-id="7ae17-244">Chaîne qui contient le nom du fichier.</span><span class="sxs-lookup"><span data-stu-id="7ae17-244">A string that contains the file's name.</span></span> <span data-ttu-id="7ae17-245">S’il s’agit d’un fichier exécutable, il est lancé.</span><span class="sxs-lookup"><span data-stu-id="7ae17-245">If it is an executable file, it is launched.</span></span> <span data-ttu-id="7ae17-246">S’il s’agit d’un fichier de données, il doit être membre d’un [type de fichier](fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="7ae17-246">If it is a data file, it must be a member of a [file type](fa-file-types.md).</span></span> <span data-ttu-id="7ae17-247">[**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) lance la commande par défaut associée au type de fichier.</span><span class="sxs-lookup"><span data-stu-id="7ae17-247">[**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) launches the default command associated with the file type.</span></span>

-   <span data-ttu-id="7ae17-248">*paramx*</span><span class="sxs-lookup"><span data-stu-id="7ae17-248">*paramx*</span></span>

    <span data-ttu-id="7ae17-249">Contient tous les paramètres supplémentaires qui doivent être passés à [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span><span class="sxs-lookup"><span data-stu-id="7ae17-249">Contains any additional parameters that should be passed to [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span></span>

### <a name="remarks"></a><span data-ttu-id="7ae17-250">Notes</span><span class="sxs-lookup"><span data-stu-id="7ae17-250">Remarks</span></span>

<span data-ttu-id="7ae17-251">Cette entrée est semblable à [Open](#parameters), mais elle vous permet d’utiliser les informations d' [Association de fichiers](fa-intro.md) pour exécuter l’application.</span><span class="sxs-lookup"><span data-stu-id="7ae17-251">This entry is similar to [open](#parameters), but it allows you to use [file association](fa-intro.md) information to run the application.</span></span>

### <a name="shell"></a><span data-ttu-id="7ae17-252">shell</span><span class="sxs-lookup"><span data-stu-id="7ae17-252">shell</span></span>

<span data-ttu-id="7ae17-253">L’entrée **Shell** spécifie une commande par défaut pour le menu contextuel du lecteur.</span><span class="sxs-lookup"><span data-stu-id="7ae17-253">The **shell** entry specifies a default command for the drive's shortcut menu.</span></span>


```
shell=verb
```



### <a name="parameters"></a><span data-ttu-id="7ae17-254">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7ae17-254">Parameters</span></span>

-   <span data-ttu-id="7ae17-255">*verbe*</span><span class="sxs-lookup"><span data-stu-id="7ae17-255">*verb*</span></span>

    <span data-ttu-id="7ae17-256">Verbe qui correspond à la commande de menu.</span><span class="sxs-lookup"><span data-stu-id="7ae17-256">The verb that corresponds to the menu command.</span></span> <span data-ttu-id="7ae17-257">Le verbe et sa commande de menu associée doivent être définis dans le fichier autorun. inf avec une entrée de [ \\ verbe de Shell](#shellverb) .</span><span class="sxs-lookup"><span data-stu-id="7ae17-257">The verb and its associated menu command must be defined in the Autorun.inf file with a [shell\\verb](#shellverb) entry.</span></span>

### <a name="remarks"></a><span data-ttu-id="7ae17-258">Notes</span><span class="sxs-lookup"><span data-stu-id="7ae17-258">Remarks</span></span>

<span data-ttu-id="7ae17-259">Quand un utilisateur clique avec le bouton droit sur l’icône du lecteur, un menu contextuel s’affiche.</span><span class="sxs-lookup"><span data-stu-id="7ae17-259">When a user right-clicks the drive icon, a shortcut menu appears.</span></span> <span data-ttu-id="7ae17-260">Si un fichier autorun. inf est présent, la commande de menu contextuel par défaut est extraite de celui-ci.</span><span class="sxs-lookup"><span data-stu-id="7ae17-260">If an Autorun.inf file is present, the default shortcut menu command is taken from it.</span></span> <span data-ttu-id="7ae17-261">Cette commande s’exécute également lorsque l’utilisateur double-clique sur l’icône du lecteur.</span><span class="sxs-lookup"><span data-stu-id="7ae17-261">This command also executes when the user double-clicks the drive's icon.</span></span>

<span data-ttu-id="7ae17-262">Pour spécifier la commande de menu contextuel par défaut, commencez par définir son verbe, sa chaîne de commande et son texte de menu avec le [ \\ verbe de Shell](#shellverb).</span><span class="sxs-lookup"><span data-stu-id="7ae17-262">To specify the default shortcut menu command, first define its verb, command string, and menu text with [shell\\verb](#shellverb).</span></span> <span data-ttu-id="7ae17-263">Utilisez ensuite l’interpréteur de commandes pour en faire la commande de menu contextuel par défaut.</span><span class="sxs-lookup"><span data-stu-id="7ae17-263">Then use shell to make it the default shortcut menu command.</span></span> <span data-ttu-id="7ae17-264">Dans le cas contraire, le texte de l’élément de menu par défaut sera « AutoPlay », ce qui lance l’application spécifiée par l’entrée [ouverte](#parameters) .</span><span class="sxs-lookup"><span data-stu-id="7ae17-264">Otherwise, the default menu item text will be "AutoPlay", which launches the application specified by the [open](#parameters) entry.</span></span>

### <a name="shellverb"></a><span data-ttu-id="7ae17-265">verbe de Shell \\</span><span class="sxs-lookup"><span data-stu-id="7ae17-265">shell\\verb</span></span>

<span data-ttu-id="7ae17-266">L’entrée de **\\ verbe de l’interpréteur** de commandes ajoute une commande personnalisée au menu contextuel du lecteur.</span><span class="sxs-lookup"><span data-stu-id="7ae17-266">The **shell\\verb** entry adds a custom command to the drive's shortcut menu.</span></span>


```
shell\verb\command=Filename.exe 
shell\verb=MenuText
```



### <a name="parameters"></a><span data-ttu-id="7ae17-267">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7ae17-267">Parameters</span></span>

-   <span data-ttu-id="7ae17-268">*verbe*</span><span class="sxs-lookup"><span data-stu-id="7ae17-268">*verb*</span></span>

    <span data-ttu-id="7ae17-269">Verbe de la commande de menu.</span><span class="sxs-lookup"><span data-stu-id="7ae17-269">The menu command's verb.</span></span> <span data-ttu-id="7ae17-270">L’entrée de *_\\ commande_* de _verbe_ de **Shell \\** associe le verbe à un fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="7ae17-270">The **shell\\**_verb_*_\\command_* entry associates the verb with an executable file.</span></span> <span data-ttu-id="7ae17-271">Les verbes ne doivent pas contenir d’espaces incorporés.</span><span class="sxs-lookup"><span data-stu-id="7ae17-271">Verbs must not contain embedded spaces.</span></span> <span data-ttu-id="7ae17-272">Par défaut, le *verbe* est le texte affiché dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="7ae17-272">By default, *verb* is the text that is displayed in the shortcut menu.</span></span>

-   <span data-ttu-id="7ae17-273">*Filename.exe*</span><span class="sxs-lookup"><span data-stu-id="7ae17-273">*Filename.exe*</span></span>

    <span data-ttu-id="7ae17-274">Chemin d’accès et nom de fichier de l’application qui exécute l’action.</span><span class="sxs-lookup"><span data-stu-id="7ae17-274">The path and file name of the application that performs the action.</span></span>

-   <span data-ttu-id="7ae17-275">*MenuText*</span><span class="sxs-lookup"><span data-stu-id="7ae17-275">*MenuText*</span></span>

    <span data-ttu-id="7ae17-276">Ce paramètre spécifie le texte affiché dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="7ae17-276">This parameter specifies the text that is displayed in the shortcut menu.</span></span> <span data-ttu-id="7ae17-277">Si elle est omise, le *verbe* est affiché.</span><span class="sxs-lookup"><span data-stu-id="7ae17-277">If it is omitted, *verb* is displayed.</span></span> <span data-ttu-id="7ae17-278">*MenuText* peut être à casse mixte et peut contenir des espaces.</span><span class="sxs-lookup"><span data-stu-id="7ae17-278">*MenuText* can be mixed-case and can contain spaces.</span></span> <span data-ttu-id="7ae17-279">Vous pouvez définir une touche de raccourci pour l’élément de menu en plaçant une esperluette (&) devant la lettre.</span><span class="sxs-lookup"><span data-stu-id="7ae17-279">You can set a shortcut key for the menu item by putting an ampersand (&) in front of the letter.</span></span>

### <a name="remarks"></a><span data-ttu-id="7ae17-280">Notes</span><span class="sxs-lookup"><span data-stu-id="7ae17-280">Remarks</span></span>

<span data-ttu-id="7ae17-281">Quand un utilisateur clique avec le bouton droit sur l’icône du lecteur, un menu contextuel s’affiche.</span><span class="sxs-lookup"><span data-stu-id="7ae17-281">When a user right-clicks the drive icon, a shortcut menu appears.</span></span> <span data-ttu-id="7ae17-282">L’ajout d’entrées de **\\ verbe de Shell** au fichier autorun. inf du lecteur vous permet d’ajouter des commandes à ce menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="7ae17-282">Adding **shell\\verb** entries to the drive's Autorun.inf file allows you to add commands to this shortcut menu.</span></span>

<span data-ttu-id="7ae17-283">Cette entrée comporte deux parties, qui doivent se trouver sur des lignes distinctes.</span><span class="sxs-lookup"><span data-stu-id="7ae17-283">There are two parts to this entry, which must be on separate lines.</span></span> <span data-ttu-id="7ae17-284">La première partie est la commande de _verbe_ de l' **\\ interpréteur** de *_\\ commandes_*.</span><span class="sxs-lookup"><span data-stu-id="7ae17-284">The first part is **shell\\**_verb_*_\\command_*.</span></span> <span data-ttu-id="7ae17-285">Elle est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="7ae17-285">It is required.</span></span> <span data-ttu-id="7ae17-286">Elle associe une chaîne, appelée *verbe*, à l’application à lancer lors de l’exécution de la commande.</span><span class="sxs-lookup"><span data-stu-id="7ae17-286">It associates a string, called a *verb*, with the application to launch when the command runs.</span></span> <span data-ttu-id="7ae17-287">La deuxième partie est l’entrée de _verbe_ de l' **interpréteur \\** de commandes.</span><span class="sxs-lookup"><span data-stu-id="7ae17-287">The second part is the **shell\\**_verb_ entry.</span></span> <span data-ttu-id="7ae17-288">Ce nom est facultatif.</span><span class="sxs-lookup"><span data-stu-id="7ae17-288">It is optional.</span></span> <span data-ttu-id="7ae17-289">Vous pouvez l’inclure pour spécifier le texte qui s’affiche dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="7ae17-289">You can include it to specify the text that displays in the shortcut menu.</span></span>

<span data-ttu-id="7ae17-290">Pour spécifier une commande de menu contextuel par défaut, définissez le verbe avec le **\\ verbe de Shell** et définissez-le comme commande par défaut avec l’entrée de [Shell](#autoruninf-entries) .</span><span class="sxs-lookup"><span data-stu-id="7ae17-290">To specify a default shortcut menu command, define the verb with **shell\\verb**, and make it the default command with the [shell](#autoruninf-entries) entry.</span></span>

<span data-ttu-id="7ae17-291">L’exemple de fragment autorun. inf suivant associe le verbe *readinesst* à la chaîne de commande « Notepad ABC \\readme.txt ».</span><span class="sxs-lookup"><span data-stu-id="7ae17-291">The following sample Autorun.inf fragment associates the *readit* verb with the command string "Notepad abc\\readme.txt".</span></span> <span data-ttu-id="7ae17-292">Le texte de menu est « read me », et « m » est défini comme touche de raccourci de l’élément.</span><span class="sxs-lookup"><span data-stu-id="7ae17-292">The menu text is "Read Me", and 'M' is defined as the item's shortcut key.</span></span> <span data-ttu-id="7ae17-293">Lorsque l’utilisateur sélectionne cette commande, le fichier ABCreadme.txt du lecteur \\ s’ouvre avec le bloc-notes Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7ae17-293">When the user selects this command, the drive's abc\\readme.txt file opens with Microsoft Notepad.</span></span>


```
shell\readit\command=notepad abc\readme.txt 
shell\readit=Read &Me
```



## <a name="content-keys"></a><span data-ttu-id="7ae17-294">\[Clés de contenu \]</span><span class="sxs-lookup"><span data-stu-id="7ae17-294">\[Content\] Keys</span></span>

<span data-ttu-id="7ae17-295">Il existe trois clés de type de fichier : **MusicFiles**, **PictureFiles** et **VideoFiles**.</span><span class="sxs-lookup"><span data-stu-id="7ae17-295">There are three file type keys: **MusicFiles**, **PictureFiles**, and **VideoFiles**.</span></span>

<span data-ttu-id="7ae17-296">Si l’un de ces contenus a la valeur true par le biais des valeurs non sensibles à la casse 1, y, Yes, t ou true, l’interface utilisateur de la lecture automatique affiche les gestionnaires associés à ce type de contenu, que le contenu de ce type existe ou non sur le média.</span><span class="sxs-lookup"><span data-stu-id="7ae17-296">If one of these contents is set to true through one the case-insensitive values 1, y, yes, t, or true, the Autoplay UI displays the handlers associated with that content type regardless of whether content of that type exists on the media.</span></span>

<span data-ttu-id="7ae17-297">Si l’un de ces contenus est défini sur false par le biais des valeurs non sensibles à la casse 0, n, no, f ou false, l’interface utilisateur de l’exécution automatique n’affiche pas les gestionnaires associés à ce type de contenu, même si le contenu de ce type est détecté sur le média.</span><span class="sxs-lookup"><span data-stu-id="7ae17-297">If one of these contents is set to false through one the case-insensitive values 0, n, no, f, or false, the Autoplay UI does not display the handlers associated with that content type even if content of that type is detected on the media.</span></span>

<span data-ttu-id="7ae17-298">L’utilisation de cette section a pour but d’autoriser les créateurs de contenu à communiquer l’intention du contenu à la lecture automatique.</span><span class="sxs-lookup"><span data-stu-id="7ae17-298">Use of this section is intended to allow content authors to communicate the intent of content to Autoplay.</span></span> <span data-ttu-id="7ae17-299">Par exemple, un CD peut être classé comme contenant uniquement du contenu musical, même s’il contient également des images et des vidéos et qu’il aurait été considéré comme ayant un contenu mixte.</span><span class="sxs-lookup"><span data-stu-id="7ae17-299">For instance, a CD can be categorized as containing only music content even though it also has pictures and videos and would otherwise be seen as having mixed content.</span></span>

<span data-ttu-id="7ae17-300">La section **\[ contenu \]** est uniquement prise en charge sous Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="7ae17-300">The **\[Content\]** section is only supported under Windows Vista and later.</span></span>


```
[Content]
MusicFiles=Y
PictureFiles=0
VideoFiles=false
```



## <a name="exclusivecontentpaths-keys"></a><span data-ttu-id="7ae17-301">\[\]Clés ExclusiveContentPaths</span><span class="sxs-lookup"><span data-stu-id="7ae17-301">\[ExclusiveContentPaths\] Keys</span></span>

<span data-ttu-id="7ae17-302">Les dossiers listés dans cette section limitent la lecture automatique à la recherche de contenu dans uniquement les dossiers et les sous-dossiers.</span><span class="sxs-lookup"><span data-stu-id="7ae17-302">Folders listed in this section limit Autoplay to searching only those folders and their subfolders for content.</span></span> <span data-ttu-id="7ae17-303">Ils peuvent être fournis avec ou sans barre oblique inverse de début ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="7ae17-303">They can be given with or without a leading backslash (\\).</span></span> <span data-ttu-id="7ae17-304">Dans les deux cas, ils sont considérés comme des chemins absolus à partir du répertoire racine du média.</span><span class="sxs-lookup"><span data-stu-id="7ae17-304">In either case they are taken as absolute paths from the root directory of the media.</span></span> <span data-ttu-id="7ae17-305">Dans le cas de dossiers dont le nom comporte des espaces, ne les placez pas entre guillemets, car les guillemets sont pris littéralement dans le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="7ae17-305">In the case of folders with spaces in their names, do not enclose them in quotes as the quotes are taken literally as part of the path.</span></span>

<span data-ttu-id="7ae17-306">L’utilisation de cette section a pour but de permettre aux auteurs de contenu de communiquer l’intention du contenu à la lecture automatique et de raccourcir le temps d’analyse en limitant l’analyse à certaines zones significatives du média.</span><span class="sxs-lookup"><span data-stu-id="7ae17-306">Use of this section is intended to allow content authors both to communicate the intent of content to Autoplay and to shorten its scan time by limiting the scan to certain significant areas of the media.</span></span>

<span data-ttu-id="7ae17-307">Les chemins d’accès valides sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="7ae17-307">The following are all valid paths</span></span>


```
[ExclusiveContentPaths]
\music
\music\more music
music2
```



<span data-ttu-id="7ae17-308">La section **\[ ExclusiveContentPaths \]** est uniquement prise en charge sous Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="7ae17-308">The **\[ExclusiveContentPaths\]** section is only supported under Windows Vista and later.</span></span>

## <a name="ignorecontentpaths-keys"></a><span data-ttu-id="7ae17-309">\[\]Clés IgnoreContentPaths</span><span class="sxs-lookup"><span data-stu-id="7ae17-309">\[IgnoreContentPaths\] Keys</span></span>

<span data-ttu-id="7ae17-310">Les dossiers répertoriés dans cette section et leurs sous-dossiers sont ignorés par l’exécution automatique lors de la recherche de contenu dans un média.</span><span class="sxs-lookup"><span data-stu-id="7ae17-310">Folders listed in this section, and their subfolders, are ignored by Autoplay when searching a media for content.</span></span> <span data-ttu-id="7ae17-311">Ils peuvent être fournis avec ou sans barre oblique inverse de début ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="7ae17-311">They can be given with or without a leading backslash (\\).</span></span> <span data-ttu-id="7ae17-312">Dans les deux cas, ils sont considérés comme des chemins absolus à partir du répertoire racine du média.</span><span class="sxs-lookup"><span data-stu-id="7ae17-312">In either case they are taken as absolute paths from the root directory of the media.</span></span> <span data-ttu-id="7ae17-313">Dans le cas de dossiers dont le nom comporte des espaces, ne les placez pas entre guillemets, car les guillemets sont pris littéralement dans le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="7ae17-313">In the case of folders with spaces in their names, do not enclose them in quotes as the quotes are taken literally as part of the path.</span></span>

<span data-ttu-id="7ae17-314">Les chemins d’accès de cette section sont prioritaires sur les chemins d’accès dans la section **\[ ExclusiveContentPaths \]** .</span><span class="sxs-lookup"><span data-stu-id="7ae17-314">Paths in this section take precedence over paths in the **\[ExclusiveContentPaths\]** section.</span></span> <span data-ttu-id="7ae17-315">Si un chemin d’accès donné dans **\[ IgnoreContentPaths \]** est un sous-dossier d’un chemin d’accès donné dans **\[ ExclusiveContentPaths \]**, il est toujours ignoré.</span><span class="sxs-lookup"><span data-stu-id="7ae17-315">If a path given in **\[IgnoreContentPaths\]** is a subfolder of a path given in **\[ExclusiveContentPaths\]**, it is still ignored.</span></span>

<span data-ttu-id="7ae17-316">L’utilisation de cette section a pour but de permettre aux auteurs de contenu de communiquer l’intention du contenu à la lecture automatique et de raccourcir le temps d’analyse en limitant l’analyse à certaines zones significatives du média.</span><span class="sxs-lookup"><span data-stu-id="7ae17-316">Use of this section is intended to allow content authors both to communicate the intent of content to Autoplay and to shorten its scan time by limiting the scan to certain significant areas of the media.</span></span>

<span data-ttu-id="7ae17-317">Les chemins d’accès valides sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="7ae17-317">The following are all valid paths</span></span>


```
[IgnoreContentPaths]
\music
\music\more music
music2
```



<span data-ttu-id="7ae17-318">La section **\[ IgnoreContentPaths \]** est uniquement prise en charge sous Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="7ae17-318">The **\[IgnoreContentPaths\]** section is only supported under Windows Vista and later.</span></span>

## <a name="deviceinstall-keys"></a><span data-ttu-id="7ae17-319">\[\]Clés DeviceInstall</span><span class="sxs-lookup"><span data-stu-id="7ae17-319">\[DeviceInstall\] Keys</span></span>

### <a name="driverpath"></a><span data-ttu-id="7ae17-320">DriverPath</span><span class="sxs-lookup"><span data-stu-id="7ae17-320">DriverPath</span></span>

<span data-ttu-id="7ae17-321">L’entrée **DriverPath** spécifie un répertoire à rechercher de manière récursive pour les fichiers de pilote.</span><span class="sxs-lookup"><span data-stu-id="7ae17-321">The **DriverPath** entry specifies a directory to search recursively for driver files.</span></span> <span data-ttu-id="7ae17-322">Cette commande est utilisée lors de l’installation d’un pilote et ne fait pas partie d’une opération d’exécution automatique.</span><span class="sxs-lookup"><span data-stu-id="7ae17-322">This command is used during a driver installation and is not part of an AutoRun operation.</span></span> <span data-ttu-id="7ae17-323">La section **\[ DeviceInstall \]** est uniquement prise en charge sous Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7ae17-323">The **\[DeviceInstall\]** section is only supported under Windows XP.</span></span>


```
[DeviceInstall]
DriverPath=directorypath
```



### <a name="parameters"></a><span data-ttu-id="7ae17-324">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7ae17-324">Parameters</span></span>

-   <span data-ttu-id="7ae17-325">*DirectoryPath*</span><span class="sxs-lookup"><span data-stu-id="7ae17-325">*directorypath*</span></span>

    <span data-ttu-id="7ae17-326">Chemin d’accès à un répertoire dans lequel Windows recherche des fichiers de pilote, ainsi que tous ses sous-répertoires.</span><span class="sxs-lookup"><span data-stu-id="7ae17-326">A path to a directory that Windows searches for driver files, along with all of its subdirectories.</span></span>

### <a name="remarks"></a><span data-ttu-id="7ae17-327">Notes</span><span class="sxs-lookup"><span data-stu-id="7ae17-327">Remarks</span></span>

<span data-ttu-id="7ae17-328">N’utilisez pas de lettres de lecteur dans *DirectoryPath* , car elles sont modifiées d’un ordinateur à l’autre.</span><span class="sxs-lookup"><span data-stu-id="7ae17-328">Do not use drive letters in *directorypath* as they change from one computer to the next.</span></span>

<span data-ttu-id="7ae17-329">Pour effectuer une recherche dans plusieurs répertoires, ajoutez une entrée **DriverPath** pour chaque répertoire, comme dans cet exemple.</span><span class="sxs-lookup"><span data-stu-id="7ae17-329">To search multiple directories, add a **DriverPath** entry for each directory as in this example.</span></span>


```
[DeviceInstall]
DriverPath=drivers\video 
DriverPath=drivers\audio
```



<span data-ttu-id="7ae17-330">Si aucune entrée **DriverPath** n’est fournie dans la section **\[ \] DeviceInstall** ou si l’entrée **DriverPath** n’a pas de valeur, ce lecteur est ignoré lors d’une recherche de fichiers de pilote.</span><span class="sxs-lookup"><span data-stu-id="7ae17-330">If no **DriverPath** entry is provided in the **\[DeviceInstall\]** section or the **DriverPath** entry has no value, then that drive is skipped during a search for driver files.</span></span>

 

 
