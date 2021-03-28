---
description: La création d’une application compatible avec l’exécution automatique est une procédure simple. Cette rubrique utilise CD-ROM comme exemple (il s’agit du premier moyen d’implémenter cette technologie), mais aujourd’hui, il existe de nombreux types de médias différents qui peuvent l’utiliser.
title: Création d’une application AutoRun-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0d01f4a2-64c4-4b31-9fc9-361da6825ab8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 24a944b011c926d1638e5d0bcb0d35fc348e5783
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112351"
---
# <a name="creating-an-autorun-enabled-application"></a><span data-ttu-id="da653-104">Création d’une application AutoRun-Enabled</span><span class="sxs-lookup"><span data-stu-id="da653-104">Creating an AutoRun-Enabled Application</span></span>

<span data-ttu-id="da653-105">La création d’une application compatible avec l’exécution automatique est une procédure simple.</span><span class="sxs-lookup"><span data-stu-id="da653-105">Creating an AutoRun-enabled application is a straightforward procedure.</span></span> <span data-ttu-id="da653-106">Cette rubrique utilise CD-ROM comme exemple (il s’agit du premier moyen d’implémenter cette technologie), mais aujourd’hui, il existe de nombreux types de médias différents qui peuvent l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="da653-106">This topic uses CD-ROM as an example (it was the first medium to implement this technology) but today there are many different media types that can use it.</span></span>

<span data-ttu-id="da653-107">Pour activer l’exécution automatique dans votre application, il vous suffit d’inclure deux fichiers essentiels :</span><span class="sxs-lookup"><span data-stu-id="da653-107">To enable AutoRun in your application, you simply include two essential files:</span></span>

-   <span data-ttu-id="da653-108">Un fichier autorun. inf</span><span class="sxs-lookup"><span data-stu-id="da653-108">An Autorun.inf file</span></span>
-   <span data-ttu-id="da653-109">Une application de démarrage</span><span class="sxs-lookup"><span data-stu-id="da653-109">A startup application</span></span>

<span data-ttu-id="da653-110">Lorsqu’un utilisateur insère un disque dans un lecteur de CD-ROM sur un ordinateur compatible avec l’exécution automatique, le système vérifie immédiatement si le disque dispose d’un système de fichiers d’ordinateur personnel.</span><span class="sxs-lookup"><span data-stu-id="da653-110">When a user inserts a disc into a CD-ROM drive on a AutoRun-compatible computer, the system immediately checks to see if the disc has a personal computer file system.</span></span> <span data-ttu-id="da653-111">Si c’est le cas, le système recherche un fichier nommé [Autorun. inf](#creating-an-autoruninf-file).</span><span class="sxs-lookup"><span data-stu-id="da653-111">If it does, the system searches for a file named [Autorun.inf](#creating-an-autoruninf-file).</span></span> <span data-ttu-id="da653-112">Ce fichier spécifie une application d’installation qui sera exécutée, ainsi que divers paramètres facultatifs.</span><span class="sxs-lookup"><span data-stu-id="da653-112">This file specifies a setup application that will be run, along with a variety of optional settings.</span></span> <span data-ttu-id="da653-113">L’application de démarrage installe, désinstalle, configure et peut-être l’application.</span><span class="sxs-lookup"><span data-stu-id="da653-113">The startup application typically installs, uninstalls, configures, and perhaps runs the application.</span></span>

-   [<span data-ttu-id="da653-114">Création d’un fichier autorun. inf</span><span class="sxs-lookup"><span data-stu-id="da653-114">Creating an Autorun.inf File</span></span>](#creating-an-autoruninf-file)
-   <span data-ttu-id="da653-115">[\[Section DeviceInstall \]](#the-deviceinstall-section)</span><span class="sxs-lookup"><span data-stu-id="da653-115">[The \[DeviceInstall\] Section](#the-deviceinstall-section)</span></span>
-   [<span data-ttu-id="da653-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="da653-116">Related topics</span></span>](#related-topics)

## <a name="creating-an-autoruninf-file"></a><span data-ttu-id="da653-117">Création d’un fichier autorun. inf</span><span class="sxs-lookup"><span data-stu-id="da653-117">Creating an Autorun.inf File</span></span>

<span data-ttu-id="da653-118">Autorun. inf est un fichier texte situé dans le répertoire racine du CD-ROM qui contient votre application.</span><span class="sxs-lookup"><span data-stu-id="da653-118">Autorun.inf is a text file located in the root directory of the CD-ROM that contains your application.</span></span> <span data-ttu-id="da653-119">Sa fonction principale est de fournir au système le nom et l’emplacement du programme de démarrage de l’application qui sera exécuté lors de l’insertion du disque.</span><span class="sxs-lookup"><span data-stu-id="da653-119">Its primary function is to provide the system with the name and location of the application's startup program that will be run when the disc is inserted.</span></span>

> [!Note]  
> <span data-ttu-id="da653-120">Les fichiers autorun. inf ne sont pas pris en charge sous Windows XP pour les lecteurs qui retournent un lecteur \_ amovible de [**GetDriveType**](/windows/win32/api/fileapi/nf-fileapi-getdrivetypea).</span><span class="sxs-lookup"><span data-stu-id="da653-120">Autorun.inf files are not supported under Windows XP for drives that return DRIVE\_REMOVABLE from [**GetDriveType**](/windows/win32/api/fileapi/nf-fileapi-getdrivetypea).</span></span>

 

<span data-ttu-id="da653-121">Le fichier autorun. inf peut également contenir des informations facultatives, notamment :</span><span class="sxs-lookup"><span data-stu-id="da653-121">The Autorun.inf file can also contain optional information including:</span></span>

-   <span data-ttu-id="da653-122">Nom d’un fichier qui contient une icône qui représente le lecteur de CD-ROM de votre application.</span><span class="sxs-lookup"><span data-stu-id="da653-122">The name of a file that contains an icon that will represent your application's CD-ROM drive.</span></span> <span data-ttu-id="da653-123">Cette icône sera affichée par l’Explorateur Windows à la place de l’icône de lecteur standard.</span><span class="sxs-lookup"><span data-stu-id="da653-123">This icon will be displayed by Windows Explorer in place of the standard drive icon.</span></span>
-   <span data-ttu-id="da653-124">Commandes supplémentaires pour le menu contextuel qui s’affiche quand l’utilisateur clique avec le bouton droit sur l’icône CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="da653-124">Additional commands for the shortcut menu that is displayed when the user right-clicks the CD-ROM icon.</span></span> <span data-ttu-id="da653-125">Vous pouvez également spécifier la commande par défaut qui est exécutée lorsque l’utilisateur double-clique sur l’icône.</span><span class="sxs-lookup"><span data-stu-id="da653-125">You can also specify the default command that is run when the user double-clicks the icon.</span></span>

<span data-ttu-id="da653-126">Les fichiers autorun. inf sont similaires aux fichiers. ini.</span><span class="sxs-lookup"><span data-stu-id="da653-126">Autorun.inf files are similar to .ini files.</span></span> <span data-ttu-id="da653-127">Ils se composent d’une ou de plusieurs sections, chacune portant un nom placé entre crochets.</span><span class="sxs-lookup"><span data-stu-id="da653-127">They consist of one or more sections, each headed by a name enclosed in square brackets.</span></span> <span data-ttu-id="da653-128">Chaque section contient une série de commandes qui seront exécutées par l’interpréteur de commandes lorsque le disque est inséré.</span><span class="sxs-lookup"><span data-stu-id="da653-128">Each section contains a series of commands that will be run by the Shell when the disc is inserted.</span></span> <span data-ttu-id="da653-129">Deux sections sont actuellement définies pour les fichiers autorun. inf.</span><span class="sxs-lookup"><span data-stu-id="da653-129">There are two sections that are currently defined for Autorun.inf files.</span></span>

-   <span data-ttu-id="da653-130">La section **\[ Autorun \]** contient les commandes d’exécution automatique par défaut.</span><span class="sxs-lookup"><span data-stu-id="da653-130">The **\[autorun\]** section contains the default AutoRun commands.</span></span> <span data-ttu-id="da653-131">Tous les fichiers autorun. inf doivent disposer d’une section d' **\[ exécution automatique \]** .</span><span class="sxs-lookup"><span data-stu-id="da653-131">All Autorun.inf files must have an **\[autorun\]** section.</span></span>
-   <span data-ttu-id="da653-132">Une section **\[ Autorun. alpha \]** facultative peut être incluse pour les systèmes qui s’exécutent sur des ordinateurs basés sur RISC.</span><span class="sxs-lookup"><span data-stu-id="da653-132">An optional **\[autorun.alpha\]** section can be included for systems running on RISC-based computers.</span></span> <span data-ttu-id="da653-133">Lorsqu’un disque est inséré dans un lecteur de CD-ROM sur un système RISC, l’interpréteur de commandes exécute les commandes de cette section au lieu de celles figurant dans la section d' **\[ exécution automatique \]** .</span><span class="sxs-lookup"><span data-stu-id="da653-133">When a disc is inserted in a CD-ROM drive on a RISC-based system, the Shell will run the commands in this section instead of those in the **\[autorun\]** section.</span></span>

> [!Note]  
> <span data-ttu-id="da653-134">Le shell recherche d’abord une section spécifique à l’architecture.</span><span class="sxs-lookup"><span data-stu-id="da653-134">The Shell checks for an architecture-specific section first.</span></span> <span data-ttu-id="da653-135">S’il n’en trouve pas, il utilise les informations de la section **\[ exécution automatique \]** .</span><span class="sxs-lookup"><span data-stu-id="da653-135">If it does not find one, it uses the information in the **\[autorun\]** section.</span></span> <span data-ttu-id="da653-136">Une fois que l’interpréteur de commandes a trouvé une section, il ignore toutes les autres, donc chaque section doit être autonome.</span><span class="sxs-lookup"><span data-stu-id="da653-136">After the Shell finds a section, it ignores all others, so each section must be self-contained.</span></span>

 

<span data-ttu-id="da653-137">Chaque section contient une série de commandes qui déterminent la façon dont l’opération d’exécution automatique a lieu.</span><span class="sxs-lookup"><span data-stu-id="da653-137">Each section contains a series of commands that determine how the Autorun operation takes place.</span></span> <span data-ttu-id="da653-138">Cinq commandes sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="da653-138">There are five commands available.</span></span>



| <span data-ttu-id="da653-139">Commande</span><span class="sxs-lookup"><span data-stu-id="da653-139">Command</span></span>                         | <span data-ttu-id="da653-140">Description</span><span class="sxs-lookup"><span data-stu-id="da653-140">Description</span></span>                                                                            |
|---------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="da653-141">DefaultIcon</span><span class="sxs-lookup"><span data-stu-id="da653-141">defaulticon</span></span>](autorun-cmds.md) | <span data-ttu-id="da653-142">Spécifie l’icône par défaut pour l’application.</span><span class="sxs-lookup"><span data-stu-id="da653-142">Specifies the default icon for the application.</span></span>                                        |
| [<span data-ttu-id="da653-143">située</span><span class="sxs-lookup"><span data-stu-id="da653-143">icon</span></span>](autorun-cmds.md)        | <span data-ttu-id="da653-144">Spécifie le chemin d’accès et le nom de fichier d’une icône spécifique à l’application pour le lecteur de CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="da653-144">Specifies the path and file name of an application-specific icon for the CD-ROM drive.</span></span> |
| [<span data-ttu-id="da653-145">open</span><span class="sxs-lookup"><span data-stu-id="da653-145">open</span></span>](autorun-cmds.md)        | <span data-ttu-id="da653-146">Spécifie le chemin d’accès et le nom de fichier de l’application de démarrage.</span><span class="sxs-lookup"><span data-stu-id="da653-146">Specifies the path and file name of the startup application.</span></span>                           |
| [<span data-ttu-id="da653-147">useautorun</span><span class="sxs-lookup"><span data-stu-id="da653-147">useautorun</span></span>](autorun-cmds.md)  | <span data-ttu-id="da653-148">Spécifie que les fonctionnalités de lecture automatique v2 doivent être utilisées si elles sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="da653-148">Specifies that Autoplay V2 features should be used if supported.</span></span>                       |
| [<span data-ttu-id="da653-149">Shell</span><span class="sxs-lookup"><span data-stu-id="da653-149">shell</span></span>](autorun-cmds.md)       | <span data-ttu-id="da653-150">Définit la commande par défaut dans le menu contextuel du CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="da653-150">Defines the default command in the CD-ROM's shortcut menu.</span></span>                             |
| [<span data-ttu-id="da653-151">verbe de Shell \_</span><span class="sxs-lookup"><span data-stu-id="da653-151">shell\_verb</span></span>](autorun-cmds.md) | <span data-ttu-id="da653-152">Ajoute des commandes au menu contextuel du CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="da653-152">Adds commands to the CD-ROM's shortcut menu.</span></span>                                           |



 

<span data-ttu-id="da653-153">Voici un exemple de fichier autorun. inf simple.</span><span class="sxs-lookup"><span data-stu-id="da653-153">The following is an example of a simple Autorun.inf file.</span></span> <span data-ttu-id="da653-154">Il spécifie Filename.exe comme application de démarrage.</span><span class="sxs-lookup"><span data-stu-id="da653-154">It specifies Filename.exe as the startup application.</span></span> <span data-ttu-id="da653-155">La deuxième icône dans Filename.exe représente le lecteur de CD-ROM au lieu de l’icône de lecteur standard.</span><span class="sxs-lookup"><span data-stu-id="da653-155">The second icon in Filename.exe will represent the CD-ROM drive instead of the standard drive icon.</span></span>


```
[autorun] 
open=Filename.exe 
icon=Filename.exe,1
```



<span data-ttu-id="da653-156">Cet exemple autorun. inf exécute différentes applications de démarrage en fonction du type d’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="da653-156">This Autorun.inf sample runs different startup applications depending on the type of computer.</span></span>


```
[autorun] 
open=Filename_x86.exe 
icon=IconFile.ico 

[autorun.alpha] 
open=Filename_RISC.exe 
icon=IconFile.ico
```



## <a name="the-deviceinstall-section"></a><span data-ttu-id="da653-157">\[Section DeviceInstall \]</span><span class="sxs-lookup"><span data-stu-id="da653-157">The \[DeviceInstall\] Section</span></span>

<span data-ttu-id="da653-158">Vous pouvez utiliser la section **\[ DeviceInstall \]** sur n’importe quel support amovible.</span><span class="sxs-lookup"><span data-stu-id="da653-158">You can use the **\[DeviceInstall\]** section on any removable media.</span></span> <span data-ttu-id="da653-159">Il est pris en charge uniquement sous Windows XP.</span><span class="sxs-lookup"><span data-stu-id="da653-159">It is supported only under Windows XP.</span></span> <span data-ttu-id="da653-160">Vous utilisez **DriverPath** pour spécifier un chemin d’accès de répertoire dans lequel Windows XP recherche des fichiers de pilote, ce qui empêche une recherche longue dans tout le contenu.</span><span class="sxs-lookup"><span data-stu-id="da653-160">You use **DriverPath** to specify a directory path where Windows XP searches for driver files, which prevents a lengthy search through the entire contents.</span></span>

<span data-ttu-id="da653-161">Vous utilisez la section **\[ DeviceInstall \]** avec une installation de pilote pour spécifier les répertoires dans lesquels Windows XP doit rechercher les fichiers de pilote dans le média.</span><span class="sxs-lookup"><span data-stu-id="da653-161">You use the **\[DeviceInstall\]** section with a driver installation to specify directories where Windows XP should search the media for driver files.</span></span> <span data-ttu-id="da653-162">Sous Windows XP, les éléments multimédias complets ne sont plus recherchés par défaut, ce qui nécessite que **\[ DeviceInstall \]** spécifie les emplacements de recherche.</span><span class="sxs-lookup"><span data-stu-id="da653-162">Under Windows XP, entire media are no longer searched by default, therefore requiring **\[DeviceInstall\]** to specify search locations.</span></span> <span data-ttu-id="da653-163">Les éléments suivants sont les seuls supports amovibles que Windows XP recherche entièrement sans section **\[ DeviceInstall \]** dans un fichier autorun. inf.</span><span class="sxs-lookup"><span data-stu-id="da653-163">The following are the only removable media that Windows XP fully searches without a **\[DeviceInstall\]** section in an Autorun.inf file.</span></span>

-   <span data-ttu-id="da653-164">Disquettes détectées dans les lecteurs A ou B.</span><span class="sxs-lookup"><span data-stu-id="da653-164">Floppy disks found in drives A or B.</span></span>
-   <span data-ttu-id="da653-165">Support CD/DVD moins de 1 gigaoctet (Go).</span><span class="sxs-lookup"><span data-stu-id="da653-165">CD/DVD media less that 1 gigabyte (GB) in size.</span></span>

<span data-ttu-id="da653-166">Tous les autres supports doivent inclure une section **\[ DeviceInstall \]** pour Windows XP afin de détecter les pilotes stockés sur ce média.</span><span class="sxs-lookup"><span data-stu-id="da653-166">All other media must include a **\[DeviceInstall\]** section for Windows XP to detect any drivers stored on that media.</span></span>

> [!Note]  
> <span data-ttu-id="da653-167">Comme avec la section d' **\[ exécution automatique \]** , la section **\[ DeviceInstall \]** peut être spécifique à l’architecture.</span><span class="sxs-lookup"><span data-stu-id="da653-167">As with the **\[AutoRun\]** section, the **\[DeviceInstall\]** section can be architecture-specific.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="da653-168">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="da653-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da653-169">Comment implémenter des applications de démarrage autorun</span><span class="sxs-lookup"><span data-stu-id="da653-169">How to Implement Autorun Startup Applications</span></span>](how-to-implement-autorun-startup-applications.md)
</dt> <dt>

[<span data-ttu-id="da653-170">Écriture d’une application d’installation d’appareil</span><span class="sxs-lookup"><span data-stu-id="da653-170">Writing a Device Installation Application</span></span>](/windows-hardware/drivers/install/writing-a-device-installation-application)
</dt> </dl>

 

 
