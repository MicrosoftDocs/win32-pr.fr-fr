---
description: Le test est un demandeur VSS qui teste les opérations de sauvegarde et de restauration avancées.
ms.assetid: a6cc7308-a9fa-4a84-9e7c-4d0adda28db5
title: Outil de test
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7559c304532b337214108435b740595897694f7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868769"
---
# <a name="betest-tool"></a><span data-ttu-id="13180-103">Outil de test</span><span class="sxs-lookup"><span data-stu-id="13180-103">BETest Tool</span></span>

<span data-ttu-id="13180-104">Le test est un demandeur VSS qui teste les opérations de sauvegarde et de restauration avancées.</span><span class="sxs-lookup"><span data-stu-id="13180-104">BETest is a VSS requester that tests advanced backup and restore operations.</span></span> <span data-ttu-id="13180-105">Cet outil peut être utilisé pour tester l’utilisation par une application de fonctionnalités VSS complexes, telles que les suivantes :</span><span class="sxs-lookup"><span data-stu-id="13180-105">This tool can be used to test an application's use of complex VSS features such as the following:</span></span>

-   <span data-ttu-id="13180-106">Sauvegarde incrémentielle et différentielle</span><span class="sxs-lookup"><span data-stu-id="13180-106">Incremental and differential backup</span></span>
-   <span data-ttu-id="13180-107">Options de restauration complexes, telles que la restauration faisant autorité</span><span class="sxs-lookup"><span data-stu-id="13180-107">Complex restore options, such as authoritative restore</span></span>
-   <span data-ttu-id="13180-108">Options de restauration par progression</span><span class="sxs-lookup"><span data-stu-id="13180-108">Rollforward options</span></span>

> [!Note]  
> <span data-ttu-id="13180-109">Le test est inclus dans le kit de développement logiciel (SDK) Microsoft Windows pour Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="13180-109">BETest is included in the Microsoft Windows Software Development Kit (SDK) for Windows Vista and later.</span></span> <span data-ttu-id="13180-110">Le kit de développement logiciel (SDK) VSS 7,2 comprend une version de test qui s’exécute uniquement sur Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="13180-110">The VSS 7.2 SDK includes a version of BETest that runs only on Windows Server 2003.</span></span> <span data-ttu-id="13180-111">Cette rubrique décrit la version SDK Windows de test, et non la version de Windows Server 2003 incluse dans le kit de développement logiciel (SDK) VSS 7,2.</span><span class="sxs-lookup"><span data-stu-id="13180-111">This topic describes the Windows SDK version of BETest, not the Windows Server 2003 version included in the VSS 7.2 SDK.</span></span> <span data-ttu-id="13180-112">Pour plus d’informations sur le téléchargement de la SDK Windows et du kit de développement logiciel (SDK) VSS 7,2, consultez [service VSS](volume-shadow-copy-service-portal.md).</span><span class="sxs-lookup"><span data-stu-id="13180-112">For information about downloading the Windows SDK and the VSS 7.2 SDK, see [Volume Shadow Copy Service](volume-shadow-copy-service-portal.md).</span></span>

 

<span data-ttu-id="13180-113">Dans l’installation SDK Windows, l’outil de test est disponible dans `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (pour windows 64 bits) et `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (pour Windows 32 bits).</span><span class="sxs-lookup"><span data-stu-id="13180-113">In the Windows SDK installation, the BETest tool can be found in `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (for 64-bit Windows) and `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (for 32-bit Windows).</span></span>

## <a name="running-the-betest-tool"></a><span data-ttu-id="13180-114">Exécution de l’outil de test</span><span class="sxs-lookup"><span data-stu-id="13180-114">Running the BETest Tool</span></span>

<span data-ttu-id="13180-115">Pour exécuter l’outil de test à partir de la ligne de commande, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="13180-115">To run the BETest tool from the command line, use the following syntax:</span></span>

<span data-ttu-id="13180-116"> *Options de ligne de commande* de test</span><span class="sxs-lookup"><span data-stu-id="13180-116">**BETest** *command-line-options*</span></span>

<span data-ttu-id="13180-117">L’exemple d’utilisation suivant montre comment utiliser l’outil posant un test avec l' [outil writer de test VSS](vss-test-writer-tool.md), qui est un enregistreur VSS.</span><span class="sxs-lookup"><span data-stu-id="13180-117">The following usage example shows how to use the BETest tool together with the [VSS Test Writer tool](vss-test-writer-tool.md), which is a VSS writer.</span></span>

<span data-ttu-id="13180-118">**Exemple d’utilisation de l’outil de test**</span><span class="sxs-lookup"><span data-stu-id="13180-118">**BETest Tool Usage Example**</span></span>

1.  <span data-ttu-id="13180-119">Créez un répertoire de test nommé C : \\ distest.</span><span class="sxs-lookup"><span data-stu-id="13180-119">Create a test directory named C:\\BETest.</span></span> <span data-ttu-id="13180-120">Copiez les fichiers suivants dans ce répertoire :</span><span class="sxs-lookup"><span data-stu-id="13180-120">Copy the following files into this directory:</span></span>
    -   <span data-ttu-id="13180-121">betest.exe</span><span class="sxs-lookup"><span data-stu-id="13180-121">betest.exe</span></span>
    -   <span data-ttu-id="13180-122">vswriter.exe</span><span class="sxs-lookup"><span data-stu-id="13180-122">vswriter.exe</span></span>
    -   [<span data-ttu-id="13180-123">BetestSample.xml</span><span class="sxs-lookup"><span data-stu-id="13180-123">BetestSample.xml</span></span>](#sample-xml-configuration-file-betestsamplexml)
    -   [<span data-ttu-id="13180-124">VswriterSample.xml</span><span class="sxs-lookup"><span data-stu-id="13180-124">VswriterSample.xml</span></span>](#sample-xml-configuration-file-vswritersamplexml)
2.  <span data-ttu-id="13180-125">Créez un répertoire nommé C : \\ TestPath.</span><span class="sxs-lookup"><span data-stu-id="13180-125">Create a directory named C:\\TestPath.</span></span> <span data-ttu-id="13180-126">Placez certains fichiers de données de test dans ce répertoire.</span><span class="sxs-lookup"><span data-stu-id="13180-126">Put some test data files in this directory.</span></span>
3.  <span data-ttu-id="13180-127">Créez un répertoire nommé C : \\ BackupDestination.</span><span class="sxs-lookup"><span data-stu-id="13180-127">Create a directory named C:\\BackupDestination.</span></span> <span data-ttu-id="13180-128">Laissez ce répertoire vide.</span><span class="sxs-lookup"><span data-stu-id="13180-128">Leave this directory empty.</span></span>
4.  <span data-ttu-id="13180-129">Ouvrez deux fenêtres de commandes avec élévation de privilèges et définissez le répertoire de travail de chacun sur C : disposant d’un \\ test.</span><span class="sxs-lookup"><span data-stu-id="13180-129">Open two elevated command windows and set the working directory in each to C:\\BETest.</span></span>
5.  <span data-ttu-id="13180-130">Dans la première fenêtre de commande, démarrez l' [outil enregistreur de test VSS](vss-test-writer-tool.md) comme suit :</span><span class="sxs-lookup"><span data-stu-id="13180-130">In the first command window, start the [VSS Test Writer tool](vss-test-writer-tool.md) as follows:</span></span>

    <span data-ttu-id="13180-131">**vswriter.exe VswriterSample.xml**</span><span class="sxs-lookup"><span data-stu-id="13180-131">**vswriter.exe VswriterSample.xml**</span></span>

    <span data-ttu-id="13180-132">Le fichier vswriterSample.xml configure l’outil VSS test Writer Tool (vswriter) pour qu’il signale le contenu du \\ répertoire c : TestPath en vue d’une opération de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="13180-132">The vswriterSample.xml file configures the VSS Test Writer tool (vswriter) to report the contents of the c:\\TestPath directory in preparation for a backup operation.</span></span> <span data-ttu-id="13180-133">Notez que l’outil VSS test Writer ne produira pas de sortie tant qu’il ne détectera pas l’activité d’un demandeur comme un test.</span><span class="sxs-lookup"><span data-stu-id="13180-133">Note that the VSS Test Writer tool will not produce output until it detects activity from a requester such as BETest.</span></span> <span data-ttu-id="13180-134">Pour arrêter l’outil enregistreur de test VSS, appuyez sur CTRL + C.</span><span class="sxs-lookup"><span data-stu-id="13180-134">To stop the VSS Test Writer tool, press CTRL+C.</span></span>

6.  <span data-ttu-id="13180-135">Dans la deuxième fenêtre de commande, utilisez l’outil de test pour effectuer une opération de sauvegarde comme suit :</span><span class="sxs-lookup"><span data-stu-id="13180-135">In the second command window, use the BETest tool to perform a backup operation as follows:</span></span>

    <span data-ttu-id="13180-136">**betest.exe/B/S backup.xml/D C : \\ BackupDestination/x BetestSample.xml**</span><span class="sxs-lookup"><span data-stu-id="13180-136">**betest.exe /B /S backup.xml /D C:\\BackupDestination /X BetestSample.xml**</span></span>

    <span data-ttu-id="13180-137">Le test va sauvegarder les fichiers du répertoire C : \\ TestPath dans le répertoire c : \\ BackupDestination.</span><span class="sxs-lookup"><span data-stu-id="13180-137">BETest will back up the files from the C:\\TestPath directory to the C:\\BackupDestination directory.</span></span> <span data-ttu-id="13180-138">Le document du composant de sauvegarde est enregistré dans le fichier C : \\ test \\backup.xml.</span><span class="sxs-lookup"><span data-stu-id="13180-138">It will save the backup component document to C:\\BETest\\backup.xml.</span></span>

7.  <span data-ttu-id="13180-139">Si l’opération de sauvegarde réussit, supprimez le contenu du répertoire C : \\ TestPath et utilisez l’outil de test pour effectuer une opération de restauration comme suit :</span><span class="sxs-lookup"><span data-stu-id="13180-139">If the backup operation is successful, delete the contents of the C:\\TestPath directory, and use the BETest tool to perform a restore operation as follows:</span></span>

    <span data-ttu-id="13180-140">**betest.exe/R/S backup.xml/D C : \\ BackupDestination/x BetestSample.xml**</span><span class="sxs-lookup"><span data-stu-id="13180-140">**betest.exe /R /S backup.xml /D C:\\BackupDestination /X BetestSample.xml**</span></span>

## <a name="betest-tool-command-line-options"></a><span data-ttu-id="13180-141">Outils de test Command-Line options</span><span class="sxs-lookup"><span data-stu-id="13180-141">BETest Tool Command-Line Options</span></span>

<span data-ttu-id="13180-142">L’outil Test Tool utilise les options de ligne de commande suivantes pour identifier le travail à effectuer.</span><span class="sxs-lookup"><span data-stu-id="13180-142">The BETest tool uses the following command-line options to identify the work to perform.</span></span>

<dl> <dt>

<span data-ttu-id="13180-143"><span id="_Auth"></span><span id="_auth"></span><span id="_AUTH"></span>**/Auth**</span><span class="sxs-lookup"><span data-stu-id="13180-143"><span id="_Auth"></span><span id="_auth"></span><span id="_AUTH"></span>**/Auth**</span></span>
</dt> <dd>

<span data-ttu-id="13180-144">Effectue une opération de restauration faisant autorité pour Active Directory ou Active Directory mode d’application.</span><span class="sxs-lookup"><span data-stu-id="13180-144">Performs an authoritative restore operation for Active Directory or Active Directory Application Mode.</span></span>

<span data-ttu-id="13180-145">**Windows Server 2003 :** Cette option de ligne de commande n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="13180-145">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="13180-146"><span id="_B"></span><span id="_b"></span>**/B**</span><span class="sxs-lookup"><span data-stu-id="13180-146"><span id="_B"></span><span id="_b"></span>**/B**</span></span>
</dt> <dd>

<span data-ttu-id="13180-147">Effectue une opération de sauvegarde, mais n’effectue pas de restauration.</span><span class="sxs-lookup"><span data-stu-id="13180-147">Performs a backup operation but does not perform a restore.</span></span>

</dd> <dt>

<span data-ttu-id="13180-148"><span id="_BC"></span><span id="_bc"></span>**/BC**</span><span class="sxs-lookup"><span data-stu-id="13180-148"><span id="_BC"></span><span id="_bc"></span>**/BC**</span></span>
</dt> <dd>

<span data-ttu-id="13180-149">Exécute uniquement l’opération de sauvegarde terminée.</span><span class="sxs-lookup"><span data-stu-id="13180-149">Performs only the backup complete operation.</span></span>

<span data-ttu-id="13180-150">**Windows Server 2003 :** Cette option de ligne de commande n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="13180-150">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="13180-151"><span id="_C_Filename"></span><span id="_c_filename"></span><span id="_C_FILENAME"></span> *Nom de fichier* /c</span><span class="sxs-lookup"><span data-stu-id="13180-151"><span id="_C_Filename"></span><span id="_c_filename"></span><span id="_C_FILENAME"></span>**/C** *Filename*</span></span>
</dt> <dd>

> [!Note]  
> <span data-ttu-id="13180-152">Cette option de ligne de commande est fournie uniquement pour la compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="13180-152">This command-line option is provided only for backward compatibility.</span></span> <span data-ttu-id="13180-153">L’option de ligne de commande **/x** doit être utilisée à la place.</span><span class="sxs-lookup"><span data-stu-id="13180-153">The **/X** command-line option should be used instead.</span></span>

 

<span data-ttu-id="13180-154">Sélectionne les composants à sauvegarder ou à restaurer en fonction du contenu du fichier de configuration spécifié par *filename*.</span><span class="sxs-lookup"><span data-stu-id="13180-154">Selects the components to be backed up or restored based on the contents of the configuration file specified by *Filename*.</span></span> <span data-ttu-id="13180-155">Ce fichier doit contenir uniquement des caractères ANSI dans la plage comprise entre 0 et 127, et il ne doit pas être supérieur à 1 Mo.</span><span class="sxs-lookup"><span data-stu-id="13180-155">This file must contain only ANSI characters in the range from 0 through 127, and it must be no larger than 1 MB.</span></span> <span data-ttu-id="13180-156">Chaque ligne du fichier doit utiliser le format suivant :</span><span class="sxs-lookup"><span data-stu-id="13180-156">Each line in the file must use the following format:</span></span>

<span data-ttu-id="13180-157">*WriterId* : *ComponentName*;</span><span class="sxs-lookup"><span data-stu-id="13180-157">*WriterId* : *ComponentName*;</span></span>

<span data-ttu-id="13180-158">Où *WriterId* est l’ID de l’enregistreur et *ComponentName* est le nom de l’un des composants du writer.</span><span class="sxs-lookup"><span data-stu-id="13180-158">Where *WriterId* is the writer ID, and *ComponentName* is the name of one of the writer's components.</span></span> <span data-ttu-id="13180-159">L’ID de l’enregistreur et les noms des composants doivent être placés entre guillemets, et il doit y avoir des espaces avant et après les deux-points ( :).</span><span class="sxs-lookup"><span data-stu-id="13180-159">The writer ID and component names must be in quotation marks, and there must be spaces before and after the colon (:).</span></span> <span data-ttu-id="13180-160">Si deux ou plusieurs composants sont spécifiés, ils doivent être séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="13180-160">If two or more components are specified, they must be separated by commas.</span></span> <span data-ttu-id="13180-161">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="13180-161">For example:</span></span>

<span data-ttu-id="13180-162">"5affb034-969f-4919-8875-88f830d0ef89" : "TestFiles1", "TestFiles2", "TestFiles3";</span><span class="sxs-lookup"><span data-stu-id="13180-162">"5affb034-969f-4919-8875-88f830d0ef89" : "TestFiles1", "TestFiles2", "TestFiles3";</span></span>

</dd> <dt>

<span data-ttu-id="13180-163"><span id="_D_Path"></span><span id="_d_path"></span><span id="_D_PATH"></span>**/D** *chemin d’accès*</span><span class="sxs-lookup"><span data-stu-id="13180-163"><span id="_D_Path"></span><span id="_d_path"></span><span id="_D_PATH"></span>**/D** *Path*</span></span>
</dt> <dd>

<span data-ttu-id="13180-164">Enregistrez les fichiers sauvegardés dans ou restaurez-les à partir du répertoire de sauvegarde spécifié par *chemin d’accès*.</span><span class="sxs-lookup"><span data-stu-id="13180-164">Save the backed-up files to or restore them from the backup directory specified by *Path*.</span></span>

</dd> <dt>

<span data-ttu-id="13180-165"><span id="_NBC"></span><span id="_nbc"></span>**/NBC**</span><span class="sxs-lookup"><span data-stu-id="13180-165"><span id="_NBC"></span><span id="_nbc"></span>**/NBC**</span></span>
</dt> <dd>

<span data-ttu-id="13180-166">Omet l’opération de sauvegarde terminée.</span><span class="sxs-lookup"><span data-stu-id="13180-166">Omits the backup complete operation.</span></span>

<span data-ttu-id="13180-167">**Windows Server 2003 :** Cette option de ligne de commande n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="13180-167">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="13180-168"><span id="_O"></span><span id="_o"></span>**/O**</span><span class="sxs-lookup"><span data-stu-id="13180-168"><span id="_O"></span><span id="_o"></span>**/O**</span></span>
</dt> <dd>

<span data-ttu-id="13180-169">Spécifie que la sauvegarde comprend un État du système de démarrage.</span><span class="sxs-lookup"><span data-stu-id="13180-169">Specifies that the backup includes a bootable system state.</span></span>

</dd> <dt>

<span data-ttu-id="13180-170"><span id="_P"></span><span id="_p"></span>**/P**</span><span class="sxs-lookup"><span data-stu-id="13180-170"><span id="_P"></span><span id="_p"></span>**/P**</span></span>
</dt> <dd>

<span data-ttu-id="13180-171">Crée un cliché instantané persistant.</span><span class="sxs-lookup"><span data-stu-id="13180-171">Creates a persistent shadow copy.</span></span>

<span data-ttu-id="13180-172">**Windows Server 2003 :** Cette option de ligne de commande n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="13180-172">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="13180-173"><span id="_Pre_Filename"></span><span id="_pre_filename"></span><span id="_PRE_FILENAME"></span> *Nom de fichier* /pre</span><span class="sxs-lookup"><span data-stu-id="13180-173"><span id="_Pre_Filename"></span><span id="_pre_filename"></span><span id="_PRE_FILENAME"></span>**/Pre** *Filename*</span></span>
</dt> <dd>

<span data-ttu-id="13180-174">Si le type de sauvegarde spécifié dans l’option de ligne de commande **/t** est INCRÉMENTIEL ou différentiel, définissez le document de sauvegarde sur le fichier spécifié par *nom* de fichier pour la sauvegarde complète ou incrémentielle précédente.</span><span class="sxs-lookup"><span data-stu-id="13180-174">If the backup type specified in the **/T** command-line option is INCREMENTAL or DIFFERENTIAL, set the backup document to the file specified by *Filename* for previous full or incremental backup.</span></span>

<span data-ttu-id="13180-175">**Windows Server 2003 et Windows XP :** Cette option de ligne de commande n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="13180-175">**Windows Server 2003 and Windows XP:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="13180-176"><span id="_R"></span><span id="_r"></span>**/R**</span><span class="sxs-lookup"><span data-stu-id="13180-176"><span id="_R"></span><span id="_r"></span>**/R**</span></span>
</dt> <dd>

<span data-ttu-id="13180-177">Effectue la restauration, mais n’effectue pas de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="13180-177">Performs restore but does not perform backup.</span></span> <span data-ttu-id="13180-178">Doit être utilisé avec l’option de ligne de commande **/s** .</span><span class="sxs-lookup"><span data-stu-id="13180-178">Must be used together with the **/S** command-line option.</span></span>

</dd> <dt>

<span data-ttu-id="13180-179"><span id="_Rollback"></span><span id="_rollback"></span><span id="_ROLLBACK"></span>**/Rollback**</span><span class="sxs-lookup"><span data-stu-id="13180-179"><span id="_Rollback"></span><span id="_rollback"></span><span id="_ROLLBACK"></span>**/Rollback**</span></span>
</dt> <dd>

<span data-ttu-id="13180-180">Crée un cliché instantané qui peut être utilisé pour la restauration de l’application.</span><span class="sxs-lookup"><span data-stu-id="13180-180">Creates a shadow copy that can be used for application rollback.</span></span>

<span data-ttu-id="13180-181">**Windows Server 2003 :** Cette option de ligne de commande n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="13180-181">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="13180-182"><span id="_S_Filename"></span><span id="_s_filename"></span><span id="_S_FILENAME"></span>**/S** *nom de fichier*</span><span class="sxs-lookup"><span data-stu-id="13180-182"><span id="_S_Filename"></span><span id="_s_filename"></span><span id="_S_FILENAME"></span>**/S** *Filename*</span></span>
</dt> <dd>

<span data-ttu-id="13180-183">En cas de sauvegarde, enregistre le document de sauvegarde dans le fichier spécifié par *filename*.</span><span class="sxs-lookup"><span data-stu-id="13180-183">In case of backup, saves the backup document to the file specified by *Filename*.</span></span> <span data-ttu-id="13180-184">En cas de restauration uniquement, charge le document de sauvegarde à partir de ce fichier.</span><span class="sxs-lookup"><span data-stu-id="13180-184">In case of restore only, loads the backup document from this file.</span></span>

</dd> <dt>

<span data-ttu-id="13180-185"><span id="_Snapshot"></span><span id="_snapshot"></span><span id="_SNAPSHOT"></span>**/Snapshot**</span><span class="sxs-lookup"><span data-stu-id="13180-185"><span id="_Snapshot"></span><span id="_snapshot"></span><span id="_SNAPSHOT"></span>**/Snapshot**</span></span>
</dt> <dd>

<span data-ttu-id="13180-186">Crée un cliché instantané du volume, mais n’effectue pas de sauvegarde ou de restauration.</span><span class="sxs-lookup"><span data-stu-id="13180-186">Creates a volume shadow copy but does not perform backup or restore.</span></span>

<span data-ttu-id="13180-187">**Windows Server 2003 :** Cette option de ligne de commande n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="13180-187">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="13180-188"><span id="_StopError"></span><span id="_stoperror"></span><span id="_STOPERROR"></span>**/StopError**</span><span class="sxs-lookup"><span data-stu-id="13180-188"><span id="_StopError"></span><span id="_stoperror"></span><span id="_STOPERROR"></span>**/StopError**</span></span>
</dt> <dd>

<span data-ttu-id="13180-189">Arrête le test lorsque la première erreur d’écriture est rencontrée.</span><span class="sxs-lookup"><span data-stu-id="13180-189">Stops BETest when the first writer error is encountered.</span></span>

<span data-ttu-id="13180-190">**Windows Server 2003 :** Cette option de ligne de commande n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="13180-190">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="13180-191"><span id="_T_BackupType"></span><span id="_t_backuptype"></span><span id="_T_BACKUPTYPE"></span>**/T** *BackupType*</span><span class="sxs-lookup"><span data-stu-id="13180-191"><span id="_T_BackupType"></span><span id="_t_backuptype"></span><span id="_T_BACKUPTYPE"></span>**/T** *BackupType*</span></span>
</dt> <dd>

<span data-ttu-id="13180-192">Spécifie le type de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="13180-192">Specifies the backup type.</span></span> <span data-ttu-id="13180-193">*BackupType* peut être complet, Journal, Copy, Incremental ou Differential.</span><span class="sxs-lookup"><span data-stu-id="13180-193">*BackupType* can be FULL, LOG, COPY, INCREMENTAL, or DIFFERENTIAL.</span></span> <span data-ttu-id="13180-194">Pour plus d’informations sur les types de sauvegardes, consultez la rubrique [**\_ \_ type de sauvegarde VSS**](/windows/desktop/api/Vss/ne-vss-vss_backup_type).</span><span class="sxs-lookup"><span data-stu-id="13180-194">For more information about backup types, see [**VSS\_BACKUP\_TYPE**](/windows/desktop/api/Vss/ne-vss-vss_backup_type).</span></span>

</dd> <dt>

<span data-ttu-id="13180-195"><span id="_V"></span><span id="_v"></span>**/F**</span><span class="sxs-lookup"><span data-stu-id="13180-195"><span id="_V"></span><span id="_v"></span>**/V**</span></span>
</dt> <dd>

<span data-ttu-id="13180-196">Génère une sortie détaillée qui peut être utilisée pour la résolution des problèmes.</span><span class="sxs-lookup"><span data-stu-id="13180-196">Generates verbose output that can be used for troubleshooting.</span></span>

<span data-ttu-id="13180-197">**Windows Server 2003 :** Cette option de ligne de commande n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="13180-197">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="13180-198"><span id="_X_Filename"></span><span id="_x_filename"></span><span id="_X_FILENAME"></span>**/X** *nom du fichier*</span><span class="sxs-lookup"><span data-stu-id="13180-198"><span id="_X_Filename"></span><span id="_x_filename"></span><span id="_X_FILENAME"></span>**/X** *Filename*</span></span>
</dt> <dd>

<span data-ttu-id="13180-199">Sélectionne les composants à sauvegarder ou à restaurer en fonction du contenu du fichier de configuration XML spécifié par *filename*.</span><span class="sxs-lookup"><span data-stu-id="13180-199">Selects the components to be backed up or restored based on the contents of the XML configuration file specified by *Filename*.</span></span> <span data-ttu-id="13180-200">Ce fichier doit contenir uniquement des caractères ANSI dans la plage comprise entre 0 et 127.</span><span class="sxs-lookup"><span data-stu-id="13180-200">This file must contain only ANSI characters in the range from 0 through 127.</span></span> <span data-ttu-id="13180-201">Le format du fichier XML est défini par le schéma dans le fichier BETest.xml.</span><span class="sxs-lookup"><span data-stu-id="13180-201">The format of the XML file is defined by the schema in the BETest.xml file.</span></span> <span data-ttu-id="13180-202">Pour obtenir un exemple de fichier de configuration, consultez BetestSample.xml.</span><span class="sxs-lookup"><span data-stu-id="13180-202">For a sample configuration file, see BetestSample.xml.</span></span> <span data-ttu-id="13180-203">Ces deux fichiers se trouvent dans le répertoire vsstools</span><span class="sxs-lookup"><span data-stu-id="13180-203">Both of these files are in the vsstools directory.</span></span>

> [!Note]  
> <span data-ttu-id="13180-204">Vous pouvez afficher le fichier BETest.xml dans Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="13180-204">You can view the BETest.xml file in Internet Explorer.</span></span> <span data-ttu-id="13180-205">Avant d’ouvrir ce fichier, assurez-vous que le fichier XDR-Schema. xsl se trouve dans le même répertoire que BETest.xml.</span><span class="sxs-lookup"><span data-stu-id="13180-205">Before you open this file, make sure that the xdr-schema.xsl file is in the same directory as BETest.xml.</span></span> <span data-ttu-id="13180-206">Le fichier XDR-Schema. xsl contient des instructions de rendu qui rendent le fichier BETest.xml plus lisible.</span><span class="sxs-lookup"><span data-stu-id="13180-206">The xdr-schema.xsl file contains rendering instructions that make the BETest.xml file more readable.</span></span>

 

<span data-ttu-id="13180-207">**Windows Server 2003 :** Cette option de ligne de commande n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="13180-207">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> </dl>

## <a name="sample-xml-configuration-file-betestsamplexml"></a><span data-ttu-id="13180-208">Exemple de fichier de configuration XML : BetestSample.xml</span><span class="sxs-lookup"><span data-stu-id="13180-208">Sample XML Configuration File: BetestSample.xml</span></span>

<span data-ttu-id="13180-209">L’exemple de fichier de configuration suivant, BetestSample.xml, se trouve dans le répertoire Vsstools</span><span class="sxs-lookup"><span data-stu-id="13180-209">The following sample configuration file, BetestSample.xml, can be found in the Vsstools directory.</span></span>

``` syntax
<BETest>
    <Writer writerid="5affb034-969f-4919-8875-88f830d0ef89">
        <Component componentName="TestFiles">
        </Component>
    </Writer>
</BETest>
```

<span data-ttu-id="13180-210">Cet exemple de fichier de configuration simple sélectionne un composant à sauvegarder ou à restaurer.</span><span class="sxs-lookup"><span data-stu-id="13180-210">This example of a simple configuration file selects one component to be backed up or restored.</span></span>

## <a name="sample-xml-configuration-file-vswritersamplexml"></a><span data-ttu-id="13180-211">Exemple de fichier de configuration XML : VswriterSample.xml</span><span class="sxs-lookup"><span data-stu-id="13180-211">Sample XML Configuration File: VswriterSample.xml</span></span>

<span data-ttu-id="13180-212">L’exemple de fichier de configuration suivant, VswriterSample.xml, se trouve dans le répertoire Vsstools</span><span class="sxs-lookup"><span data-stu-id="13180-212">The following sample configuration file, VswriterSample.xml, can be found in the Vsstools directory.</span></span>

``` syntax
<TestWriter   usage="USER_DATA"
                    deleteFiles="no">

    <RestoreMethod method="RESTORE_IF_CAN_BE_REPLACED" 
                   writerRestore="always"
                   rebootRequired="no" />
    
    <Component componentType="filegroup" 
               componentName="TestFiles">
               <ComponentFile path="c:\TestPath" filespec="*" recursive="no" />
    </Component>

</TestWriter>
```

<span data-ttu-id="13180-213">L’élément racine dans ce fichier de configuration est nommé TestWriter.</span><span class="sxs-lookup"><span data-stu-id="13180-213">The root element in this configuration file is named TestWriter.</span></span> <span data-ttu-id="13180-214">Tous les autres éléments sont organisés sous l’élément TestWriter.</span><span class="sxs-lookup"><span data-stu-id="13180-214">All other elements are arranged under the TestWriter element.</span></span>

<span data-ttu-id="13180-215">Le premier attribut associé à TestWriter est l’attribut d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="13180-215">The first attribute associated with TestWriter is the usage attribute.</span></span> <span data-ttu-id="13180-216">Cet attribut spécifie le type d’utilisation signalé par le biais de la méthode [**IVssExamineWriterMetadata :: GetIdentity**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getidentity) .</span><span class="sxs-lookup"><span data-stu-id="13180-216">This attribute specifies the usage type reported through the [**IVssExamineWriterMetadata::GetIdentity**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getidentity) method.</span></span> <span data-ttu-id="13180-217">L’une des valeurs possibles pour cet attribut est \_ données utilisateur.</span><span class="sxs-lookup"><span data-stu-id="13180-217">One of the possible values for this attribute is USER\_DATA.</span></span>

<span data-ttu-id="13180-218">Le deuxième attribut est l’attribut deleteFiles.</span><span class="sxs-lookup"><span data-stu-id="13180-218">The second attribute is the deleteFiles attribute.</span></span> <span data-ttu-id="13180-219">Cet attribut est décrit dans [Configuring Writer Attributes](vss-test-writer-tool.md).</span><span class="sxs-lookup"><span data-stu-id="13180-219">This attribute is described in [Configuring Writer Attributes](vss-test-writer-tool.md).</span></span>

<span data-ttu-id="13180-220">Le premier élément enfant de l’élément racine est un élément RestoreMethod.</span><span class="sxs-lookup"><span data-stu-id="13180-220">The first child element of the root element is a RestoreMethod element.</span></span> <span data-ttu-id="13180-221">Cet élément spécifie les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="13180-221">This element specifies the following:</span></span>

-   <span data-ttu-id="13180-222">La méthode Restore (dans ce cas, Restore \_ si \_ peut \_ être \_ remplacé)</span><span class="sxs-lookup"><span data-stu-id="13180-222">The restore method (in this case, RESTORE\_IF\_CAN\_BE\_REPLACED)</span></span>
-   <span data-ttu-id="13180-223">Si l’enregistreur requiert des événements de restauration (dans ce cas, toujours)</span><span class="sxs-lookup"><span data-stu-id="13180-223">Whether the writer requires restore events (in this case, always)</span></span>
-   <span data-ttu-id="13180-224">Si un redémarrage est nécessaire après la restauration de l’enregistreur (dans ce cas, non)</span><span class="sxs-lookup"><span data-stu-id="13180-224">Whether a reboot is required after the writer is restored (in this case, no)</span></span>

<span data-ttu-id="13180-225">Cet élément peut éventuellement spécifier un autre mappage d’emplacement.</span><span class="sxs-lookup"><span data-stu-id="13180-225">This element can optionally specify an alternate-location mapping.</span></span> <span data-ttu-id="13180-226">(Dans ce cas, aucun autre emplacement n’est spécifié.) Pour plus d’informations, consultez [spécification de mappages d’emplacements de substitution](vss-test-writer-tool.md).</span><span class="sxs-lookup"><span data-stu-id="13180-226">(In this case, no alternate location is specified.) For more information, see [Specifying Alternate Location Mappings](vss-test-writer-tool.md).</span></span>

<span data-ttu-id="13180-227">Le deuxième élément enfant est un élément de composant.</span><span class="sxs-lookup"><span data-stu-id="13180-227">The second child element is a Component element.</span></span> <span data-ttu-id="13180-228">Cet élément amène le writer à ajouter un composant à ses métadonnées.</span><span class="sxs-lookup"><span data-stu-id="13180-228">This element causes the writer to add a component to its metadata.</span></span> <span data-ttu-id="13180-229">Un élément composant contient des attributs permettant de décrire le composant et les éléments enfants pour décrire le contenu du composant, comme suit :</span><span class="sxs-lookup"><span data-stu-id="13180-229">A Component element contains attributes to describe the component and child elements to describe the content of the component, such as the following:</span></span>

-   <span data-ttu-id="13180-230">componentType pour indiquer s’il s’agit d’un groupe de fichiers ou d’une base de données (dans ce cas, un groupe de fichiers)</span><span class="sxs-lookup"><span data-stu-id="13180-230">componentType to indicate whether this is a filegroup or a database (in this case, a filegroup)</span></span>
-   <span data-ttu-id="13180-231">logicalPath pour le chemin d’accès logique du composant (dans ce cas, aucun n’est spécifié)</span><span class="sxs-lookup"><span data-stu-id="13180-231">logicalPath for the component logical path (in this case, none is specified)</span></span>
-   <span data-ttu-id="13180-232">componentName pour le nom du composant (dans ce cas, « TestFiles »)</span><span class="sxs-lookup"><span data-stu-id="13180-232">componentName for the name of the component (in this case, "TestFiles")</span></span>
-   <span data-ttu-id="13180-233">sélectionnable pour indiquer l’État sélectionnable pour la sauvegarde</span><span class="sxs-lookup"><span data-stu-id="13180-233">selectable to indicate selectable-for-backup status</span></span>

<span data-ttu-id="13180-234">L’élément Component a également un élément enfant nommé ComponentFile pour ajouter une spécification de fichier à ce composant.</span><span class="sxs-lookup"><span data-stu-id="13180-234">The Component element also has a child element named ComponentFile to add a file specification to this component.</span></span> <span data-ttu-id="13180-235">(Un élément de composant peut avoir un nombre arbitraire d’éléments ComponentFile qui peuvent être spécifiés pour chaque composant.) Cet élément ComponentFile a les attributs suivants :</span><span class="sxs-lookup"><span data-stu-id="13180-235">(A Component element can have an arbitrary number of ComponentFile elements that can be specified for each component.) This ComponentFile element has the following attributes:</span></span>

-   <span data-ttu-id="13180-236">path = "c : \\ TestPath"</span><span class="sxs-lookup"><span data-stu-id="13180-236">path="c:\\TestPath"</span></span>
-   <span data-ttu-id="13180-237">spécification de spécification = " \* "</span><span class="sxs-lookup"><span data-stu-id="13180-237">filespec="\*"</span></span>
-   <span data-ttu-id="13180-238">récursif = « non »</span><span class="sxs-lookup"><span data-stu-id="13180-238">recursive="no"</span></span>

 

 



