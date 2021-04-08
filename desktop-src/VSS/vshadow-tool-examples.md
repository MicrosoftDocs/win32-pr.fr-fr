---
description: 'En savoir plus sur : exemples d’outils VShadow'
ms.assetid: 6a69b75b-ee4a-4613-ba05-d2deb42759b7
title: Exemples d’outils VShadow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b65fd2bfa1c390b1bd5310cd80f02e029dbf935f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751572"
---
# <a name="vshadow-tool-examples"></a><span data-ttu-id="5b25d-103">Exemples d’outils VShadow</span><span class="sxs-lookup"><span data-stu-id="5b25d-103">VShadow Tool Examples</span></span>

<span data-ttu-id="5b25d-104">Les exemples suivants montrent comment utiliser l’outil VShadow pour effectuer les tâches les plus courantes :</span><span class="sxs-lookup"><span data-stu-id="5b25d-104">The following examples show how to use the VShadow tool to perform the most common tasks:</span></span>

-   [<span data-ttu-id="5b25d-105">Accès aux propriétés des clichés instantanés à partir d’un script CMD</span><span class="sxs-lookup"><span data-stu-id="5b25d-105">Accessing Shadow Copy Properties from a CMD Script</span></span>](#accessing-shadow-copy-properties-from-a-cmd-script)
-   [<span data-ttu-id="5b25d-106">Accès aux clichés instantanés non persistants</span><span class="sxs-lookup"><span data-stu-id="5b25d-106">Accessing Nonpersistent Shadow Copies</span></span>](#accessing-nonpersistent-shadow-copies)
-   [<span data-ttu-id="5b25d-107">Copie d’un fichier à partir d’un cliché instantané</span><span class="sxs-lookup"><span data-stu-id="5b25d-107">Copying a File from a Shadow Copy</span></span>](#copying-a-file-from-a-shadow-copy)
-   [<span data-ttu-id="5b25d-108">Énumération de tous les fichiers sur un appareil de clichés instantanés</span><span class="sxs-lookup"><span data-stu-id="5b25d-108">Enumerating All Files on a Shadow Copy Device</span></span>](#enumerating-all-files-on-a-shadow-copy-device)
-   [<span data-ttu-id="5b25d-109">Importation d’un cliché instantané transportable</span><span class="sxs-lookup"><span data-stu-id="5b25d-109">Importing a Transportable Shadow Copy</span></span>](#importing-a-transportable-shadow-copy)
-   [<span data-ttu-id="5b25d-110">Ajout d’enregistreurs ou de composants</span><span class="sxs-lookup"><span data-stu-id="5b25d-110">Including Writers or Components</span></span>](#including-writers-or-components)
-   [<span data-ttu-id="5b25d-111">Exclusion d’enregistreurs ou de composants</span><span class="sxs-lookup"><span data-stu-id="5b25d-111">Excluding Writers or Components</span></span>](#excluding-writers-or-components)
-   [<span data-ttu-id="5b25d-112">Interruption des jeux de clichés instantanés à l’aide de la méthode BreakSnapshotSetEx</span><span class="sxs-lookup"><span data-stu-id="5b25d-112">Breaking Shadow Copy Sets Using the BreakSnapshotSetEx Method</span></span>](#breaking-shadow-copy-sets-using-the-breaksnapshotsetex-method)

<span data-ttu-id="5b25d-113">Pour obtenir la liste complète des options de ligne de commande et leur utilisation, consultez [outil VShadow et exemple](vshadow-tool-and-sample.md).</span><span class="sxs-lookup"><span data-stu-id="5b25d-113">For a complete list of command-line options and their use, see [VShadow Tool and Sample](vshadow-tool-and-sample.md).</span></span>

## <a name="accessing-shadow-copy-properties-from-a-cmd-script"></a><span data-ttu-id="5b25d-114">Accès aux propriétés des clichés instantanés à partir d’un script CMD</span><span class="sxs-lookup"><span data-stu-id="5b25d-114">Accessing Shadow Copy Properties from a CMD Script</span></span>

<span data-ttu-id="5b25d-115">Si vous utilisez l’indicateur **-script** facultatif lors de la création de clichés instantanés, VShadow crée un fichier de script cmd contenant les variables d’environnement associées aux clichés instantanés nouvellement créés, comme suit :</span><span class="sxs-lookup"><span data-stu-id="5b25d-115">If you use the **-script** optional flag when you create shadow copies, VShadow creates a CMD script file containing environment variables related to the newly created shadow copies, such as the following:</span></span>

-   <span data-ttu-id="5b25d-116">L’ID du jeu de clichés instantanés, qui est stocké dans la variable d’environnement% VSHADOW \_ Set \_ ID%</span><span class="sxs-lookup"><span data-stu-id="5b25d-116">The shadow copy set ID, which is stored in the %VSHADOW\_SET\_ID% environment variable</span></span>
-   <span data-ttu-id="5b25d-117">Les ID de cliché instantané, qui sont stockés dans des variables au format% VSHADOW \_ ID \_ *nnn*%, où *nnn* représente l’index du volume source dans la ligne de commande VSHADOW</span><span class="sxs-lookup"><span data-stu-id="5b25d-117">The shadow copy IDs, which are stored in variables of the form %VSHADOW\_ID\_*NNN*%, where *NNN* represents the index of the source volume in the VShadow command line</span></span>
-   <span data-ttu-id="5b25d-118">Les noms des appareils de clichés instantanés, qui sont stockés dans des variables au format% VSHADOW de l' \_ appareil \_ *nnn*%, où *nnn* est l’index du volume source dans la ligne de commande VSHADOW</span><span class="sxs-lookup"><span data-stu-id="5b25d-118">The shadow copy device names, which are stored in variables of the form %VSHADOW\_DEVICE\_*NNN*%, where *NNN* is the index of the source volume in the VShadow command line</span></span>

<span data-ttu-id="5b25d-119">Vous pouvez utiliser le fichier CMD généré pour effectuer des opérations de gestion limitées sur les clichés instantanés.</span><span class="sxs-lookup"><span data-stu-id="5b25d-119">You can use the generated CMD file to perform limited management operations on the shadow copies.</span></span>

> [!Note]  
> <span data-ttu-id="5b25d-120">L’événement du writer [**BackupComplete**](/windows/win32/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) est envoyé après l’exécution du script **-Exec** .</span><span class="sxs-lookup"><span data-stu-id="5b25d-120">The [**BackupComplete**](/windows/win32/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) writer event is sent after the **-exec** script is executed.</span></span> <span data-ttu-id="5b25d-121">VSS appelle la méthode **IVssBackupComponents :: BackupComplete** pour signaler aux rédacteurs que la sauvegarde est terminée, et les enregistreurs peuvent potentiellement tronquer les journaux à ce stade.</span><span class="sxs-lookup"><span data-stu-id="5b25d-121">VSS calls the **IVssBackupComponents::BackupComplete** method to signal to the writers that the backup is completed, and the writers can potentially truncate logs at this point.</span></span> <span data-ttu-id="5b25d-122">Par conséquent, il est important de vérifier que l’ombre/sauvegarde est effectivement terminée.</span><span class="sxs-lookup"><span data-stu-id="5b25d-122">Therefore, it is important to verify that the shadow/backup actually completed.</span></span> <span data-ttu-id="5b25d-123">En cas d’échec de la sauvegarde, vous pouvez annuler le processus de création en retournant un code de sortie différent de zéro dans le script/la commande exécuté (e).</span><span class="sxs-lookup"><span data-stu-id="5b25d-123">If the backup failed, you can cancel the creation process by returning a nonzero exit code in the executed script/command.</span></span> <span data-ttu-id="5b25d-124">(Consultez la documentation de la commande exit dans la [référence de la ligne de commande Windows](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754340(v=ws.11)).) Si la commande personnalisée retourne avec un code de sortie différent de zéro, la création de clichés instantanés est annulée et **IVssBackupComponents :: BackupComplete** n’est pas appelé.</span><span class="sxs-lookup"><span data-stu-id="5b25d-124">(See the documentation for the exit command in the [Windows Command Line Reference](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754340(v=ws.11)).) If the custom command returns with a nonzero exit code, then the shadow copy creation is canceled and **IVssBackupComponents::BackupComplete** will not be called.</span></span>

 

<span data-ttu-id="5b25d-125">L’exemple suivant montre comment créer un cliché instantané persistant à partir de la ligne de commande et utiliser le script CMD pour l’exposer.</span><span class="sxs-lookup"><span data-stu-id="5b25d-125">The following example shows how to create a persistent shadow copy from the command line and use the CMD script to expose it.</span></span>

1.  <span data-ttu-id="5b25d-126">**vshadow-p-NW-script = SETVAR1. cmd c :**</span><span class="sxs-lookup"><span data-stu-id="5b25d-126">**vshadow -p -nw -script=SETVAR1.cmd c:**</span></span>
2.  <span data-ttu-id="5b25d-127">**appeler SETVAR1. cmd**</span><span class="sxs-lookup"><span data-stu-id="5b25d-127">**call SETVAR1.cmd**</span></span>
3.  <span data-ttu-id="5b25d-128">**C : \\>vshadow-El =% vshadow \_ ID \_ 1%, c : \\ Directory1**</span><span class="sxs-lookup"><span data-stu-id="5b25d-128">**C:\\>vshadow -el=%VSHADOW\_ID\_1%,c:\\directory1**</span></span>

## <a name="accessing-nonpersistent-shadow-copies"></a><span data-ttu-id="5b25d-129">Accès aux clichés instantanés non persistants</span><span class="sxs-lookup"><span data-stu-id="5b25d-129">Accessing Nonpersistent Shadow Copies</span></span>

<span data-ttu-id="5b25d-130">Les clichés instantanés non persistants sont automatiquement supprimés lorsque le programme qui les crée (dans ce cas, VShadow) se termine.</span><span class="sxs-lookup"><span data-stu-id="5b25d-130">Nonpersistent shadow copies are automatically deleted when the program that creates them (in this case, VShadow) exits.</span></span> <span data-ttu-id="5b25d-131">Pour accéder au contenu de ces clichés instantanés, VShadow vous permet d’exécuter un script après la création des clichés instantanés, mais avant la fermeture du programme VShadow.</span><span class="sxs-lookup"><span data-stu-id="5b25d-131">To access the contents of these shadow copies, VShadow allows you to execute a script after the shadow copies are created but before the VShadow program exits.</span></span>

<span data-ttu-id="5b25d-132">L’exemple suivant montre comment utiliser l’option de ligne de commande-exec pour exécuter un script appelé « Enum. cmd » :</span><span class="sxs-lookup"><span data-stu-id="5b25d-132">The following example shows how to use the -exec command-line option to run a script called "enum.cmd":</span></span>

<span data-ttu-id="5b25d-133">**vshadow-NW-exec = Enum. cmd c :**</span><span class="sxs-lookup"><span data-stu-id="5b25d-133">**vshadow -nw -exec=enum.cmd c:**</span></span>

<span data-ttu-id="5b25d-134">Dans le script exécuté, vous pouvez également exécuter le script SETVAR généré dans cette commande personnalisée.</span><span class="sxs-lookup"><span data-stu-id="5b25d-134">In the executed script, you can also run the generated SETVAR script in this custom command.</span></span> <span data-ttu-id="5b25d-135">Cela permet au script d’accéder directement au contenu des clichés instantanés.</span><span class="sxs-lookup"><span data-stu-id="5b25d-135">This allows the script to access the contents of the shadow copies directly.</span></span> <span data-ttu-id="5b25d-136">N’oubliez pas que l’appareil instantané peut être récupéré à partir de la \_ variable d’environnement VSHADOW Device \_ nnn.</span><span class="sxs-lookup"><span data-stu-id="5b25d-136">Remember that the shadow device can be retrieved from the VSHADOW\_DEVICE\_NNN environment variable.</span></span>

<span data-ttu-id="5b25d-137">Voici un exemple de script Enum. cmd :</span><span class="sxs-lookup"><span data-stu-id="5b25d-137">Here is an example enum.cmd script:</span></span>

``` syntax
call SETVAR1.cmd
for /R %VSHADOW_DEVICE_1%\ %%i in (*.*) do @echo %%i
```

<span data-ttu-id="5b25d-138">Voici la ligne de commande permettant d’exécuter le script Enum. cmd :</span><span class="sxs-lookup"><span data-stu-id="5b25d-138">Here is the command line to execute the enum.cmd script:</span></span>

<span data-ttu-id="5b25d-139">**vshadow-NW-exec = c : \\ enum. cmd-script = setvar1. cmd c :**</span><span class="sxs-lookup"><span data-stu-id="5b25d-139">**vshadow -nw -exec=c:\\enum.cmd -script=setvar1.cmd c:**</span></span>

## <a name="copying-a-file-from-a-shadow-copy"></a><span data-ttu-id="5b25d-140">Copie d’un fichier à partir d’un cliché instantané</span><span class="sxs-lookup"><span data-stu-id="5b25d-140">Copying a File from a Shadow Copy</span></span>

<span data-ttu-id="5b25d-141">L’exemple suivant montre comment copier un fichier à partir d’un cliché instantané.</span><span class="sxs-lookup"><span data-stu-id="5b25d-141">The following example shows how to copy a file from a shadow copy.</span></span>

1.  <span data-ttu-id="5b25d-142">**Répertoire > c : \\somefile.txt**</span><span class="sxs-lookup"><span data-stu-id="5b25d-142">**dir > c:\\somefile.txt**</span></span>
2.  <span data-ttu-id="5b25d-143">**vshadow-p-NW-script = SETVAR1. cmd c :**</span><span class="sxs-lookup"><span data-stu-id="5b25d-143">**vshadow -p -nw -script=SETVAR1.cmd c:**</span></span>
3.  <span data-ttu-id="5b25d-144">**appeler SETVAR1. cmd**</span><span class="sxs-lookup"><span data-stu-id="5b25d-144">**call SETVAR1.cmd**</span></span>
4.  <span data-ttu-id="5b25d-145">**copier% VSHADOW \_ appareil \_ 1% \\somefile.txt c : \\ somefile \_bak.txt**</span><span class="sxs-lookup"><span data-stu-id="5b25d-145">**copy %VSHADOW\_DEVICE\_1%\\somefile.txt c:\\somefile\_bak.txt**</span></span>

## <a name="enumerating-all-files-on-a-shadow-copy-device"></a><span data-ttu-id="5b25d-146">Énumération de tous les fichiers sur un appareil de clichés instantanés</span><span class="sxs-lookup"><span data-stu-id="5b25d-146">Enumerating All Files on a Shadow Copy Device</span></span>

<span data-ttu-id="5b25d-147">L’exemple suivant montre comment énumérer tous les fichiers sur un appareil de clichés instantanés à partir d’un fichier de commandes.</span><span class="sxs-lookup"><span data-stu-id="5b25d-147">The following example shows how to enumerate all files on a shadow copy device from a batch file.</span></span>

1.  <span data-ttu-id="5b25d-148">**Répertoire > c : \\somefile.txt**</span><span class="sxs-lookup"><span data-stu-id="5b25d-148">**dir > c:\\somefile.txt**</span></span>
2.  <span data-ttu-id="5b25d-149">**vshadow-p-NW-script = SETVAR1. cmd c :**</span><span class="sxs-lookup"><span data-stu-id="5b25d-149">**vshadow -p -nw -script=SETVAR1.cmd c:**</span></span>
3.  <span data-ttu-id="5b25d-150">**appeler SETVAR1. cmd**</span><span class="sxs-lookup"><span data-stu-id="5b25d-150">**call SETVAR1.cmd**</span></span>
4.  <span data-ttu-id="5b25d-151">**pour l’appareil/R% VSHADOW \_ \_ 1% \\ %% i dans ( \* ) do @echo %% i**</span><span class="sxs-lookup"><span data-stu-id="5b25d-151">**for /R %VSHADOW\_DEVICE\_1%\\ %%i in (\*) do @echo %%i**</span></span>

## <a name="importing-a-transportable-shadow-copy"></a><span data-ttu-id="5b25d-152">Importation d’un cliché instantané transportable</span><span class="sxs-lookup"><span data-stu-id="5b25d-152">Importing a Transportable Shadow Copy</span></span>

<span data-ttu-id="5b25d-153">Pour créer un cliché instantané transportable sur un ordinateur et l’importer sur un autre ordinateur, vous devez disposer de deux ordinateurs connectés (via une configuration SAN) à un groupe de stockage qui prend en charge les clichés instantanés de matériel VSS.</span><span class="sxs-lookup"><span data-stu-id="5b25d-153">To create a transportable shadow copy on one machine and import it to another machine, you must have two computers that are connected (through a SAN configuration) to a storage array that supports VSS hardware shadow copies.</span></span> <span data-ttu-id="5b25d-154">Un fournisseur de matériel VSS doit être installé sur chaque ordinateur.</span><span class="sxs-lookup"><span data-stu-id="5b25d-154">A VSS hardware provider must be installed on each computer.</span></span>

<span data-ttu-id="5b25d-155">L’exemple suivant montre comment créer et importer le cliché instantané.</span><span class="sxs-lookup"><span data-stu-id="5b25d-155">The following example shows how to create and import the shadow copy.</span></span>

1.  <span data-ttu-id="5b25d-156">Créez le jeu de clichés instantanés sur l’ordinateur A (serveur de production) en tapant la commande suivante après l’invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="5b25d-156">Create the shadow copy set on computer A (the production server) by typing the following command after the command prompt:</span></span>

    <span data-ttu-id="5b25d-157">**vshadow-p-t =bc1.xml**</span><span class="sxs-lookup"><span data-stu-id="5b25d-157">**vshadow -p -t=bc1.xml**</span></span>

    <span data-ttu-id="5b25d-158">Cela n’expose pas les appareils de clichés instantanés sur l’ordinateur A.</span><span class="sxs-lookup"><span data-stu-id="5b25d-158">This will not expose any shadow copy devices on computer A.</span></span>

2.  <span data-ttu-id="5b25d-159">Copiez le document des composants de sauvegarde (bc1.xml) de l’ordinateur A vers l’ordinateur B.</span><span class="sxs-lookup"><span data-stu-id="5b25d-159">Copy the backup components document (bc1.xml) from computer A to computer B.</span></span>
3.  <span data-ttu-id="5b25d-160">Importez le jeu d’ombres sur l’ordinateur B en tapant la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="5b25d-160">Import the shadow set on machine B by typing the following command:</span></span>

    <span data-ttu-id="5b25d-161">**vshadow-i =bc1.xml**</span><span class="sxs-lookup"><span data-stu-id="5b25d-161">**vshadow -i=bc1.xml**</span></span>

<span data-ttu-id="5b25d-162">Vous pouvez éventuellement exposer ces clichés instantanés en tant que lettres de lecteur ou dossiers montés.</span><span class="sxs-lookup"><span data-stu-id="5b25d-162">Optionally, you could expose these shadow copies as drive letters or mounted folders.</span></span> <span data-ttu-id="5b25d-163">En outre, vous pouvez potentiellement rompre le jeu d’ombres pour que les nouveaux volumes de clichés instantanés soient accessibles en lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="5b25d-163">Also, you could potentially break the shadow set to make the new shadow copy volumes read-write.</span></span>

<span data-ttu-id="5b25d-164">Pour automatiser le processus de gestion des jeux de clichés instantanés, vous pouvez utiliser l’option de ligne de commande **-script** pour générer le script cmd contenant les ID de cliché instantané.</span><span class="sxs-lookup"><span data-stu-id="5b25d-164">To automate the shadow set management process you might use the **-script** command-line option to generate the CMD script containing the shadow copy IDs.</span></span> <span data-ttu-id="5b25d-165">Ensuite, vous pouvez copier le script généré avec les composants de sauvegarde sur l’autre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="5b25d-165">Then you can copy the generated script along with the backup components to the other computer.</span></span>

<span data-ttu-id="5b25d-166">L’exemple suivant montre comment créer, exposer et rompre les clichés instantanés transportables à l’aide de scripts CMD.</span><span class="sxs-lookup"><span data-stu-id="5b25d-166">The following example shows how to create, expose, and break transportable shadow copies using CMD scripts.</span></span>

1.  <span data-ttu-id="5b25d-167">Créez le jeu de clichés instantanés sur l’ordinateur A (serveur de production) à partir de la ligne de commande comme suit :</span><span class="sxs-lookup"><span data-stu-id="5b25d-167">Create the shadow copy set on computer A (the production server) from the command line as follows:</span></span>

    <span data-ttu-id="5b25d-168">**vshadow-p-t =bc1.xml-script = SC1. cmd**</span><span class="sxs-lookup"><span data-stu-id="5b25d-168">**vshadow -p -t=bc1.xml -script=sc1.cmd**</span></span>

    <span data-ttu-id="5b25d-169">Spécifiez l’option **-script** pour générer le script contenant les définitions de variables d’environnement appropriées.</span><span class="sxs-lookup"><span data-stu-id="5b25d-169">Specify the **-script** option to generate the script containing the proper environment variable definitions.</span></span> <span data-ttu-id="5b25d-170">Notez que cela n’exposera aucun appareil de clichés instantanés sur l’ordinateur A.</span><span class="sxs-lookup"><span data-stu-id="5b25d-170">Note that this will not expose any shadow copy devices on computer A.</span></span>

2.  <span data-ttu-id="5b25d-171">Copiez le document des composants de sauvegarde (bc1.xml) et le script généré (SC1. cmd) de l’ordinateur A vers l’ordinateur B.</span><span class="sxs-lookup"><span data-stu-id="5b25d-171">Copy the backup components document (bc1.xml) and the generated script (sc1.cmd) from computer A to computer B.</span></span>
3.  <span data-ttu-id="5b25d-172">Importez le jeu d’ombres sur l’ordinateur B en tapant la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="5b25d-172">Import the shadow set on machine B by typing the following command:</span></span>

    <span data-ttu-id="5b25d-173">**vshadow-i =bc1.xml**</span><span class="sxs-lookup"><span data-stu-id="5b25d-173">**vshadow -i=bc1.xml**</span></span>

    <span data-ttu-id="5b25d-174">Cela entraînera l’exposition des appareils créés sur l’ordinateur B.</span><span class="sxs-lookup"><span data-stu-id="5b25d-174">This will surface the created devices on computer B.</span></span>

4.  <span data-ttu-id="5b25d-175">Exécutez le script généré pour définir les variables d’environnement pour le jeu de clichés instantanés en tapant le nom de fichier à l’invite de commandes, comme dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="5b25d-175">Run the generated script to set the environment variables for the shadow copy set by typing the file name at the command prompt as in the following example:</span></span>

    <span data-ttu-id="5b25d-176">**SC1. cmd**</span><span class="sxs-lookup"><span data-stu-id="5b25d-176">**sc1.cmd**</span></span>

    <span data-ttu-id="5b25d-177">Cela permet de définir les variables d’environnement appropriées comme décrit dans accéder aux propriétés des clichés instantanés à partir d’un script CMD.</span><span class="sxs-lookup"><span data-stu-id="5b25d-177">This will set the relevant environment variables as described in Access Shadow Copy Properties from a CMD Script.</span></span>

5.  <span data-ttu-id="5b25d-178">Exposez les clichés instantanés sur l’ordinateur B en tapant les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="5b25d-178">Expose the shadow copies on computer B by typing the following commands:</span></span>
    1.  <span data-ttu-id="5b25d-179">**rmdir/s c : \\ point de montage \_**</span><span class="sxs-lookup"><span data-stu-id="5b25d-179">**rmdir /s c:\\mount\_point**</span></span>
    2.  <span data-ttu-id="5b25d-180">**mkdir c : \\ point de montage \_**</span><span class="sxs-lookup"><span data-stu-id="5b25d-180">**mkdir c:\\mount\_point**</span></span>
    3.  <span data-ttu-id="5b25d-181">**vshadow – El =% VSHADOW \_ ID \_ 1%, c : \\ point de montage \_**</span><span class="sxs-lookup"><span data-stu-id="5b25d-181">**vshadow –el=%VSHADOW\_ID\_1%,c:\\mount\_point**</span></span>

    <span data-ttu-id="5b25d-182">Les appareils de clichés instantanés créés sont alors exposés sur l’ordinateur B.</span><span class="sxs-lookup"><span data-stu-id="5b25d-182">This will surface the created shadow copy devices on computer B.</span></span>
6.  <span data-ttu-id="5b25d-183">Rompez le jeu de clichés instantanés pour rendre les volumes accessibles en écriture en tapant la commande suivante :**C : \\>vshadow – BW =% vshadow \_ Set \_ ID%**</span><span class="sxs-lookup"><span data-stu-id="5b25d-183">Break the shadow copy set to make the volumes writable by typing the following command:**C:\\>vshadow –bw=%VSHADOW\_SET\_ID%**</span></span>

<span data-ttu-id="5b25d-184">Notez que les clichés instantanés transportables non persistants peuvent également être importés, mais ils sont automatiquement supprimés lorsque le processus **vshadow** **-i** s’arrête.</span><span class="sxs-lookup"><span data-stu-id="5b25d-184">Note that nonpersistent transportable shadow copies can also be imported, but they are automatically deleted when the **vshadow** **-i** process exits.</span></span> <span data-ttu-id="5b25d-185">Pour importer les clichés instantanés avant leur suppression, vous devez utiliser l’option de ligne de commande **-Exec** comme décrit dans accéder aux clichés instantanés non persistants.</span><span class="sxs-lookup"><span data-stu-id="5b25d-185">To import the shadow copies before they are deleted, you must use the **-exec** command-line option as described in Access Nonpersistent Shadow Copies.</span></span>

## <a name="including-writers-or-components"></a><span data-ttu-id="5b25d-186">Ajout d’enregistreurs ou de composants</span><span class="sxs-lookup"><span data-stu-id="5b25d-186">Including Writers or Components</span></span>

<span data-ttu-id="5b25d-187">Par défaut, tous les enregistreurs participent à la création de clichés instantanés.</span><span class="sxs-lookup"><span data-stu-id="5b25d-187">By default, all writers participate in shadow copy creation.</span></span> <span data-ttu-id="5b25d-188">Pour déterminer les rédacteurs et les composants qui seront inclus dans un jeu de clichés instantanés, utilisez l’option de ligne de commande **-WM** ou **-wm2** comme décrit dans la section Affichage de l' [État et des métadonnées](vshadow-tool-and-sample.md)de l’enregistreur.</span><span class="sxs-lookup"><span data-stu-id="5b25d-188">To determine which writers and components will be included in a shadow copy set, use the **-wm** or **-wm2** command-line option as described in [Listing Writer Status and Metadata](vshadow-tool-and-sample.md).</span></span>

<span data-ttu-id="5b25d-189">Pour vérifier que tous les composants d’un enregistreur sont inclus, utilisez l’indicateur **-Wi** facultatif dans l’un des formats suivants :</span><span class="sxs-lookup"><span data-stu-id="5b25d-189">To verify that all of a writer's components are included, use the **-wi** optional flag in any of the following formats:</span></span>

-   <span data-ttu-id="5b25d-190">**vshadow** **-Wi** *WriterName*</span><span class="sxs-lookup"><span data-stu-id="5b25d-190">**vshadow** **-wi** *WriterName*</span></span>
-   <span data-ttu-id="5b25d-191">**vshadow** **-Wi** **"**_chaîne de nom de l’enregistreur_*_"_*</span><span class="sxs-lookup"><span data-stu-id="5b25d-191">**vshadow** **-wi** **"**_Writer Name String_*_"_*</span></span>
-   <span data-ttu-id="5b25d-192">**vshadow** **-Wi** **{**_WriterID_*_}_*</span><span class="sxs-lookup"><span data-stu-id="5b25d-192">**vshadow** **-wi** **{**_WriterID_*_}_*</span></span>
-   <span data-ttu-id="5b25d-193">**vshadow** **-Wi** **{**_InstanceID_*_}_*</span><span class="sxs-lookup"><span data-stu-id="5b25d-193">**vshadow** **-wi** **{**_InstanceID_*_}_*</span></span>

<span data-ttu-id="5b25d-194">Pour vérifier que des composants spécifiques sont inclus, utilisez l’indicateur **-Wi** facultatif dans l’un des formats suivants :</span><span class="sxs-lookup"><span data-stu-id="5b25d-194">To verify that specific components are included, use the **-wi** optional flag in any of the following formats:</span></span>

-   <span data-ttu-id="5b25d-195">**vshadow** **-Wi** \*WriterName \***: \\**_LogicalPath_\* _\\_ \* _ComponentName_</span><span class="sxs-lookup"><span data-stu-id="5b25d-195">**vshadow** **-wi** *WriterName\***:\\**_LogicalPath_*_\\_\*_ComponentName_</span></span>
-   <span data-ttu-id="5b25d-196">**vshadow** **-Wi** **"**_chaîne de nom de l’enregistreur_*_" : \\_*_LogicalPath_ *_\\_* _ComponentName_</span><span class="sxs-lookup"><span data-stu-id="5b25d-196">**vshadow** **-wi** **"**_Writer Name String_*_":\\_*_LogicalPath_*_\\_*_ComponentName_</span></span>
-   <span data-ttu-id="5b25d-197">**vshadow** **-Wi** **{**_WriterID_*_} : \\_*_LogicalPath_ *_\\_* _ComponentName_</span><span class="sxs-lookup"><span data-stu-id="5b25d-197">**vshadow** **-wi** **{**_WriterID_*_}:\\_*_LogicalPath_*_\\_*_ComponentName_</span></span>
-   <span data-ttu-id="5b25d-198">**vshadow** **-Wi** **{**_InstanceID_*_} : \\_*_LogicalPath_ *_\\_* _ComponentName_</span><span class="sxs-lookup"><span data-stu-id="5b25d-198">**vshadow** **-wi** **{**_InstanceID_*_}:\\_*_LogicalPath_*_\\_*_ComponentName_</span></span>

<span data-ttu-id="5b25d-199">Les exemples suivants montrent comment utiliser l’indicateur facultatif **-Wi** .</span><span class="sxs-lookup"><span data-stu-id="5b25d-199">The following examples show how to use the **-wi** optional flag.</span></span>

-   <span data-ttu-id="5b25d-200">Spécification de *WriterName*: \\ *LogicalPath* \\ *ComponentName*:</span><span class="sxs-lookup"><span data-stu-id="5b25d-200">Specifying *WriterName*:\\*LogicalPath*\\*ComponentName*:</span></span>

    <span data-ttu-id="5b25d-201">**vshadow-Wi = "Registry writer : \\ Registry"**</span><span class="sxs-lookup"><span data-stu-id="5b25d-201">**vshadow -wi="Registry Writer:\\Registry"**</span></span>

-   <span data-ttu-id="5b25d-202">Spécification de {*WriterID*} :</span><span class="sxs-lookup"><span data-stu-id="5b25d-202">Specifying {*WriterID*}:</span></span>

    <span data-ttu-id="5b25d-203">**vshadow-Wi = {BE000CBE-11FE-4426-9C58-531AA6355FC4}**</span><span class="sxs-lookup"><span data-stu-id="5b25d-203">**vshadow -wi={BE000CBE-11FE-4426-9C58-531AA6355FC4}**</span></span>

-   <span data-ttu-id="5b25d-204">Spécification de plusieurs rédacteurs ou composants :</span><span class="sxs-lookup"><span data-stu-id="5b25d-204">Specifying more than one writer or component:</span></span>

    <span data-ttu-id="5b25d-205">**vshadow-Wi = "Registry writer : \\ Registry"-Wi = "com+ RegDB Writer"**</span><span class="sxs-lookup"><span data-stu-id="5b25d-205">**vshadow -wi="Registry Writer:\\Registry" -wi="COM+ REGDB Writer"**</span></span>

## <a name="excluding-writers-or-components"></a><span data-ttu-id="5b25d-206">Exclusion d’enregistreurs ou de composants</span><span class="sxs-lookup"><span data-stu-id="5b25d-206">Excluding Writers or Components</span></span>

<span data-ttu-id="5b25d-207">Pour exclure tous les enregistreurs, utilisez l’indicateur **-NW** facultatif lors de la création du cliché instantané.</span><span class="sxs-lookup"><span data-stu-id="5b25d-207">To exclude all writers, use the **-nw** optional flag when creating the shadow copy.</span></span>

<span data-ttu-id="5b25d-208">Pour exclure tous les composants d’un enregistreur, utilisez l’indicateur **-WX** facultatif dans l’un des formats suivants :</span><span class="sxs-lookup"><span data-stu-id="5b25d-208">To exclude all of a writer's components, use the **-wx** optional flag in any of the following formats:</span></span>

-   <span data-ttu-id="5b25d-209">**vshadow** **-WX** *WriterName*</span><span class="sxs-lookup"><span data-stu-id="5b25d-209">**vshadow** **-wx** *WriterName*</span></span>
-   <span data-ttu-id="5b25d-210">**vshadow** **-WX** **"**_chaîne de nom de l’enregistreur_*_"_*</span><span class="sxs-lookup"><span data-stu-id="5b25d-210">**vshadow** **-wx** **"**_Writer Name String_*_"_*</span></span>
-   <span data-ttu-id="5b25d-211">**vshadow** **-WX** **{**_WriterID_*_}_*</span><span class="sxs-lookup"><span data-stu-id="5b25d-211">**vshadow** **-wx** **{**_WriterID_*_}_*</span></span>
-   <span data-ttu-id="5b25d-212">**vshadow** **-WX** **{**_InstanceID_*_}_*</span><span class="sxs-lookup"><span data-stu-id="5b25d-212">**vshadow** **-wx** **{**_InstanceID_*_}_*</span></span>

<span data-ttu-id="5b25d-213">Pour exclure des composants spécifiques, utilisez l’indicateur **-WX** facultatif dans l’un des formats suivants :</span><span class="sxs-lookup"><span data-stu-id="5b25d-213">To exclude specific components, use the **-wx** optional flag in any of the following formats:</span></span>

-   <span data-ttu-id="5b25d-214">**vshadow** **-WX** \*WriterName \***: \\**_LogicalPath_\* _\\_ \* _ComponentName_</span><span class="sxs-lookup"><span data-stu-id="5b25d-214">**vshadow** **-wx** *WriterName\***:\\**_LogicalPath_*_\\_\*_ComponentName_</span></span>
-   <span data-ttu-id="5b25d-215">**vshadow** **-WX** **"**_chaîne de nom de l’enregistreur_*_" : \\_*_LogicalPath_ *_\\_* _ComponentName_</span><span class="sxs-lookup"><span data-stu-id="5b25d-215">**vshadow** **-wx** **"**_Writer Name String_*_":\\_*_LogicalPath_*_\\_*_ComponentName_</span></span>
-   <span data-ttu-id="5b25d-216">**vshadow** **-WX** **{**_WriterID_*_} : \\_*_LogicalPath_ *_\\_* _ComponentName_</span><span class="sxs-lookup"><span data-stu-id="5b25d-216">**vshadow** **-wx** **{**_WriterID_*_}:\\_*_LogicalPath_*_\\_*_ComponentName_</span></span>
-   <span data-ttu-id="5b25d-217">**vshadow** **-WX** **{**_InstanceID_*_} : \\_*_LogicalPath_ *_\\_* _ComponentName_</span><span class="sxs-lookup"><span data-stu-id="5b25d-217">**vshadow** **-wx** **{**_InstanceID_*_}:\\_*_LogicalPath_*_\\_*_ComponentName_</span></span>

<span data-ttu-id="5b25d-218">Les exemples suivants montrent comment utiliser l’indicateur facultatif **-WX** .</span><span class="sxs-lookup"><span data-stu-id="5b25d-218">The following examples show how to use the **-wx** optional flag.</span></span>

-   <span data-ttu-id="5b25d-219">Spécification de *WriterName*: \\ *LogicalPath* \\ *ComponentName*:</span><span class="sxs-lookup"><span data-stu-id="5b25d-219">Specifying *WriterName*:\\*LogicalPath*\\*ComponentName*:</span></span>

    <span data-ttu-id="5b25d-220">**vshadow-WX = "Registry writer : \\ Registry"**</span><span class="sxs-lookup"><span data-stu-id="5b25d-220">**vshadow -wx="Registry Writer:\\Registry"**</span></span>

-   <span data-ttu-id="5b25d-221">Spécification de {*WriterID*} :</span><span class="sxs-lookup"><span data-stu-id="5b25d-221">Specifying {*WriterID*}:</span></span>

    <span data-ttu-id="5b25d-222">**vshadow-WX = {BE000CBE-11FE-4426-9C58-531AA6355FC4}**</span><span class="sxs-lookup"><span data-stu-id="5b25d-222">**vshadow -wx={BE000CBE-11FE-4426-9C58-531AA6355FC4}**</span></span>

-   <span data-ttu-id="5b25d-223">Spécification de plusieurs rédacteurs ou composants :</span><span class="sxs-lookup"><span data-stu-id="5b25d-223">Specifying more than one writer or component:</span></span>

    <span data-ttu-id="5b25d-224">**vshadow-WX = "Registry writer : \\ Registry"-WX = "com+ RegDB Writer"**</span><span class="sxs-lookup"><span data-stu-id="5b25d-224">**vshadow -wx="Registry Writer:\\Registry" -wx="COM+ REGDB Writer"**</span></span>

## <a name="breaking-shadow-copy-sets-using-the-breaksnapshotsetex-method"></a><span data-ttu-id="5b25d-225">Interruption des jeux de clichés instantanés à l’aide de la méthode BreakSnapshotSetEx</span><span class="sxs-lookup"><span data-stu-id="5b25d-225">Breaking Shadow Copy Sets Using the BreakSnapshotSetEx Method</span></span>

<span data-ttu-id="5b25d-226">Les exemples suivants montrent comment utiliser l’option de ligne de commande **-Bex** .</span><span class="sxs-lookup"><span data-stu-id="5b25d-226">The following examples show how to use the **-bex** command-line option.</span></span>

-   <span data-ttu-id="5b25d-227">Spécifiez que le numéro d’unité logique de cliché instantané sera masqué de l’hôte :</span><span class="sxs-lookup"><span data-stu-id="5b25d-227">Specifying that the shadow copy LUN will be masked from the host:</span></span>

    <span data-ttu-id="5b25d-228">**vshadow** **-Bex** **-Mask**</span><span class="sxs-lookup"><span data-stu-id="5b25d-228">**vshadow** **-bex** **-mask**</span></span>

-   <span data-ttu-id="5b25d-229">Spécifiez que le numéro d’unité logique de cliché instantané sera exposé à l’hôte en tant que volume en lecture/écriture :</span><span class="sxs-lookup"><span data-stu-id="5b25d-229">Specifying that the shadow copy LUN will be exposed to the host as a read/write volume:</span></span>

    <span data-ttu-id="5b25d-230">**vshadow** **-Bex** **-RW**</span><span class="sxs-lookup"><span data-stu-id="5b25d-230">**vshadow** **-bex** **-rw**</span></span>

-   <span data-ttu-id="5b25d-231">En spécifiant que le numéro d’unité logique de cliché instantané sera exposé à l’hôte en tant que volume en lecture/écriture, et qu’aucune des signatures de disque sur les numéros d’unités logiques de cliché instantané ne sera restaurée à celle des numéros d’unités logiques d’origine :</span><span class="sxs-lookup"><span data-stu-id="5b25d-231">Specifying that the shadow copy LUN will be exposed to the host as a read/write volume, and that none of the disk signatures on the shadow copy LUNs will be reverted to that of the original LUNs:</span></span>

    <span data-ttu-id="5b25d-232">**vshadow** **-Bex** **-Revert**</span><span class="sxs-lookup"><span data-stu-id="5b25d-232">**vshadow** **-bex** **-norevert**</span></span>

 

 
