---
description: Le serveur source permet à un client de récupérer la version exacte des fichiers sources qui ont été utilisés pour générer une application.
ms.assetid: c7bf51ce-7fb4-49aa-ad33-e551b2c8362b
title: Serveur source
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b3d8d76c70b67c176126d8e424bd5b55b616697
ms.sourcegitcommit: bfb5d94f754d017307b4cc9d914a2716701331d1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106539360"
---
# <a name="source-server"></a><span data-ttu-id="b3ccb-103">Serveur source</span><span class="sxs-lookup"><span data-stu-id="b3ccb-103">Source Server</span></span>

<span data-ttu-id="b3ccb-104">Le serveur source permet à un client de récupérer la version exacte des fichiers sources qui ont été utilisés pour générer une application.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-104">Source server enables a client to retrieve the exact version of the source files that were used to build an application.</span></span> <span data-ttu-id="b3ccb-105">Étant donné que le code source d’un module peut changer d’une version à l’autre, il est important d’examiner le code source tel qu’il existait lors de la création de la version du module en question.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-105">Because the source code for a module can change between versions and over a course of years, it is important to look at the source code as it existed when the version of the module in question was built.</span></span>

<span data-ttu-id="b3ccb-106">Le serveur source récupère les fichiers appropriés à partir du contrôle de code source.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-106">Source server retrieves the appropriate files from source control.</span></span> <span data-ttu-id="b3ccb-107">Pour utiliser le serveur source, l’application doit avoir été indexée source.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-107">To use source server, the application must have been source indexed.</span></span>

## <a name="source-indexing"></a><span data-ttu-id="b3ccb-108">Indexation source</span><span class="sxs-lookup"><span data-stu-id="b3ccb-108">Source Indexing</span></span>

<span data-ttu-id="b3ccb-109">Le système d’indexation source est une collection de fichiers exécutables et de scripts Perl.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-109">The source indexing system is a collection of executable files and Perl scripts.</span></span> <span data-ttu-id="b3ccb-110">Les scripts perl requièrent Perl 5,6 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-110">The Perl scripts require Perl 5.6 or greater.</span></span>

<span data-ttu-id="b3ccb-111">En règle générale, les fichiers binaires sont indexés à la source pendant le processus de génération après la génération de l’application.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-111">Generally, binaries are source indexed during the build process after the application has been built.</span></span> <span data-ttu-id="b3ccb-112">Les informations requises par le serveur source sont stockées dans les fichiers PDB.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-112">The information needed by source server is stored in the PDB files.</span></span>

<span data-ttu-id="b3ccb-113">Le serveur source est actuellement fourni avec des scripts qui doivent fonctionner avec les systèmes de contrôle de code source suivants.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-113">Source server currently ships with scripts that should work with the following source-control systems.</span></span>

-   <span data-ttu-id="b3ccb-114">Team Foundation Server</span><span class="sxs-lookup"><span data-stu-id="b3ccb-114">Team Foundation Server</span></span>
-   <span data-ttu-id="b3ccb-115">Perforce</span><span class="sxs-lookup"><span data-stu-id="b3ccb-115">Perforce</span></span>
-   <span data-ttu-id="b3ccb-116">Visual SourceSafe</span><span class="sxs-lookup"><span data-stu-id="b3ccb-116">Visual SourceSafe</span></span>
-   <span data-ttu-id="b3ccb-117">ÉCHANTILLON</span><span class="sxs-lookup"><span data-stu-id="b3ccb-117">CVS</span></span>
-   <span data-ttu-id="b3ccb-118">Subversion</span><span class="sxs-lookup"><span data-stu-id="b3ccb-118">Subversion</span></span>

<span data-ttu-id="b3ccb-119">Vous pouvez également créer un script personnalisé pour indexer votre code pour un autre système de contrôle de code source.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-119">You can also create a custom script to index your code for a different source-control system.</span></span>

<span data-ttu-id="b3ccb-120">Le tableau suivant répertorie les outils du serveur source.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-120">The following table lists the source server tools.</span></span>



| <span data-ttu-id="b3ccb-121">Outil</span><span class="sxs-lookup"><span data-stu-id="b3ccb-121">Tool</span></span>        | <span data-ttu-id="b3ccb-122">Description</span><span class="sxs-lookup"><span data-stu-id="b3ccb-122">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3ccb-123">Srcsrv.ini</span><span class="sxs-lookup"><span data-stu-id="b3ccb-123">Srcsrv.ini</span></span>  | <span data-ttu-id="b3ccb-124">Ce fichier est la liste principale de tous les serveurs de contrôle de code source.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-124">This file is the master list of all source control servers.</span></span> <span data-ttu-id="b3ccb-125">Chaque entrée a le format suivant :*MyServer* = *du*</span><span class="sxs-lookup"><span data-stu-id="b3ccb-125">Each entry has the following format:*MYSERVER*=*serverinfo*</span></span><br/> <span data-ttu-id="b3ccb-126">Lors de l’utilisation de Perforce, les informations sur le serveur se composent du chemin d’accès réseau complet au serveur, suivi d’un signe deux-points, suivi du numéro de port qu’il utilise.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-126">When using Perforce, the server info consists of the full network path to the server, followed by a colon, followed by the port number it uses.</span></span> <span data-ttu-id="b3ccb-127">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="b3ccb-127">For example:</span></span><br/> <span data-ttu-id="b3ccb-128">MYSERVER = machine. Corp. Company. com : 1666</span><span class="sxs-lookup"><span data-stu-id="b3ccb-128">MYSERVER=machine.corp.company.com:1666</span></span><br/> <span data-ttu-id="b3ccb-129">Ce fichier peut être installé sur l’ordinateur qui exécute le débogueur.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-129">This file can be installed on the computer running the debugger.</span></span> <span data-ttu-id="b3ccb-130">Lorsque le serveur source démarre, il recherche des valeurs dans Srcsrv.ini ; ces valeurs remplacent les informations contenues dans le fichier PDB.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-130">When source server starts, it looks at Srcsrv.ini for values; these values will override the information contained in the PDB file.</span></span> <span data-ttu-id="b3ccb-131">Cela permet aux utilisateurs de configurer un débogueur pour qu’il utilise un autre serveur de contrôle de code source au moment du débogage.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-131">This enables users to configure a debugger to use an alternate source control server at debug time.</span></span><br/> <span data-ttu-id="b3ccb-132">Pour plus d’informations, consultez l’exemple Srcsrv.ini installé avec les outils du serveur source.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-132">For more information, see the example Srcsrv.ini installed with the source server tools.</span></span><br/> |
| <span data-ttu-id="b3ccb-133">SSINDEX. cmd</span><span class="sxs-lookup"><span data-stu-id="b3ccb-133">Ssindex.cmd</span></span> | <span data-ttu-id="b3ccb-134">Ce script génère la liste des fichiers archivés dans le contrôle de code source, ainsi que les informations de version de chaque fichier.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-134">This script builds the list of files checked into source control along with the version information of each file.</span></span> <span data-ttu-id="b3ccb-135">Il stocke un sous-ensemble de ces informations dans les fichiers. pdb générés au moment de la génération de l’application.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-135">It stores a subset of this information in the .pdb files generated when you built the application.</span></span> <span data-ttu-id="b3ccb-136">Le script utilise l’un des modules perl suivants pour l’interface avec le contrôle de code source : P4.pm (Perforce) ou Vss.pm (Visual Source Safe). Pour plus d’informations, exécutez le script avec le- ?</span><span class="sxs-lookup"><span data-stu-id="b3ccb-136">The script uses one of the following Perl modules to interface with source control: P4.pm (Perforce) or Vss.pm (Visual Source Safe).For more information, run the script with the -?</span></span> <span data-ttu-id="b3ccb-137">ou- ??</span><span class="sxs-lookup"><span data-stu-id="b3ccb-137">or -??</span></span> <span data-ttu-id="b3ccb-138">(aide détaillée) ou examinez le script.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-138">(verbose help) option or examine the script.</span></span><br/>                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="b3ccb-139">Srctool.exe</span><span class="sxs-lookup"><span data-stu-id="b3ccb-139">Srctool.exe</span></span> | <span data-ttu-id="b3ccb-140">Cet utilitaire répertorie tous les fichiers indexés dans un fichier. pdb.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-140">This utility lists all files indexed within a .pdb file.</span></span> <span data-ttu-id="b3ccb-141">Pour chaque fichier, il répertorie le chemin d’accès complet, le serveur de contrôle de code source et le numéro de version du fichier.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-141">For each file, it lists the full path, source control server, and version number of the file.</span></span> <span data-ttu-id="b3ccb-142">Vous pouvez utiliser ces informations pour récupérer des fichiers sans utiliser le serveur source. Pour plus d’informations, exécutez l’utilitaire avec le/ ?</span><span class="sxs-lookup"><span data-stu-id="b3ccb-142">You can use this information to retrieve files without using the source server.For more information, run the utility with the /?</span></span> <span data-ttu-id="b3ccb-143">option.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-143">option.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="b3ccb-144">Pdbstr.exe</span><span class="sxs-lookup"><span data-stu-id="b3ccb-144">Pdbstr.exe</span></span>  | <span data-ttu-id="b3ccb-145">Cet utilitaire est utilisé par les scripts d’indexation pour insérer les informations de contrôle de version dans le flux alternatif « SRCSRV » du fichier. pdb cible.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-145">This utility is used by the indexing scripts to insert the version control information into the "srcsrv" alternate stream of the target .pdb file.</span></span> <span data-ttu-id="b3ccb-146">Il peut également lire n’importe quel flux à partir d’un fichier. pdb.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-146">It can also read any stream from a .pdb file.</span></span> <span data-ttu-id="b3ccb-147">Vous pouvez utiliser ces informations pour vérifier que les scripts d’indexation fonctionnent correctement. Pour plus d’informations, exécutez l’utilitaire avec le/ ?</span><span class="sxs-lookup"><span data-stu-id="b3ccb-147">You can use this information to verify that the indexing scripts are working properly.For more information, run the utility with the /?</span></span> <span data-ttu-id="b3ccb-148">option.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-148">option.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="retrieving-the-source-file"></a><span data-ttu-id="b3ccb-149">Récupération du fichier source</span><span class="sxs-lookup"><span data-stu-id="b3ccb-149">Retrieving the Source File</span></span>

<span data-ttu-id="b3ccb-150">L’API DbgHelp fournit un accès aux fonctionnalités du serveur source via la fonction [**SymGetSourceFile**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefile) .</span><span class="sxs-lookup"><span data-stu-id="b3ccb-150">The DbgHelp API provides access to source server functionality through the [**SymGetSourceFile**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefile) function.</span></span> <span data-ttu-id="b3ccb-151">Pour récupérer le nom du fichier source à récupérer, appelez la fonction [**SymEnumSourceFiles**](/windows/desktop/api/DbgHelp/nf-dbghelp-symenumsourcefiles) ou [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr) .</span><span class="sxs-lookup"><span data-stu-id="b3ccb-151">To retrieve the name of the source file to be retrieved, call the [**SymEnumSourceFiles**](/windows/desktop/api/DbgHelp/nf-dbghelp-symenumsourcefiles) or [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr) function.</span></span>

## <a name="using-source-server-with-a-debugger"></a><span data-ttu-id="b3ccb-152">Utilisation du serveur source avec un débogueur</span><span class="sxs-lookup"><span data-stu-id="b3ccb-152">Using Source Server with a Debugger</span></span>

<span data-ttu-id="b3ccb-153">Pour utiliser le serveur source avec WinDbg, KD, NTSD ou CDB, vérifiez que vous avez installé une version récente du package outils de débogage pour Windows (version 6,3 ou ultérieure).</span><span class="sxs-lookup"><span data-stu-id="b3ccb-153">To use the source server with WinDbg, KD, NTSD, or CDB, ensure that you have installed a recent version of the Debugging Tools for Windows package (version 6.3 or later).</span></span> <span data-ttu-id="b3ccb-154">Ensuite, incluez SRV \* dans la commande. srcpath comme suit :</span><span class="sxs-lookup"><span data-stu-id="b3ccb-154">Then, include srv\* in the .srcpath command as follows:</span></span>

<span data-ttu-id="b3ccb-155">**\. srcpath SRV \* ;** _c : \\ MySource_</span><span class="sxs-lookup"><span data-stu-id="b3ccb-155">**\.srcpath srv\*;**_c:\\mysource_</span></span>

<span data-ttu-id="b3ccb-156">Notez que cet exemple comprend également un chemin d’accès source traditionnel.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-156">Note that this example also includes a traditional source path.</span></span> <span data-ttu-id="b3ccb-157">Si le débogueur ne peut pas récupérer le fichier à partir du serveur source, il recherche le chemin d’accès spécifié.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-157">If the debugger cannot retrieve the file from the source server, it will search the specified path.</span></span>

<span data-ttu-id="b3ccb-158">Si un fichier source est récupéré par le serveur source, il est conservé sur votre disque dur une fois la session de débogage terminée.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-158">If a source file is retrieved by the source server, it will remain on your hard drive after the debugging session is over.</span></span> <span data-ttu-id="b3ccb-159">Les fichiers sources sont stockés localement dans le sous-répertoire SRC du répertoire d’installation des outils de débogage pour Windows.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-159">Source files are stored locally in the src subdirectory of the Debugging Tools for Windows installation directory.</span></span>

## <a name="source-server-data-blocks"></a><span data-ttu-id="b3ccb-160">Blocs de données du serveur source</span><span class="sxs-lookup"><span data-stu-id="b3ccb-160">Source Server Data Blocks</span></span>

<span data-ttu-id="b3ccb-161">Le serveur source s’appuie sur deux blocs de données dans le fichier PDB.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-161">Source server relies on two blocks of data within the PDB file.</span></span>

-   <span data-ttu-id="b3ccb-162">Liste des fichiers sources.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-162">Source file list.</span></span> <span data-ttu-id="b3ccb-163">La génération d’un module crée automatiquement une liste de chemins d’accès complets aux fichiers sources utilisés pour générer le module.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-163">Building a module automatically creates a list of fully qualified paths to the source files used to build the module.</span></span>
-   <span data-ttu-id="b3ccb-164">Bloc de données.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-164">Data block.</span></span> <span data-ttu-id="b3ccb-165">L’indexation de la source comme décrit précédemment ajoute un flux de remplacement au fichier PDB nommé « srcsrv ».</span><span class="sxs-lookup"><span data-stu-id="b3ccb-165">Indexing the source as described previously adds an alternate stream to the PDB file named "srcsrv".</span></span> <span data-ttu-id="b3ccb-166">Le script qui insère ces données dépend du processus de génération spécifique et du système de contrôle de code source en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-166">The script that inserts this data is dependent on the specific build process and source control system in use.</span></span>

<span data-ttu-id="b3ccb-167">Dans la spécification de langage version 1, le bloc de données est divisé en trois sections : ini, variables et fichiers sources.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-167">In the language specification version 1, the data block is divided into three sections: ini, variables, and source files.</span></span> <span data-ttu-id="b3ccb-168">Sa syntaxe est la suivante.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-168">It has the following syntax.</span></span>

``` syntax
SRCSRV: ini ------------------------------------------------ 
VERSION=1
VERCTRL=<source_control_str>
DATETIME=<date_time_str>
SRCSRV: variables ------------------------------------------ 
SRCSRVTRG=%sdtrg% 
SRCSRVCMD=%sdcmd% 
SRCSRVENV=var1=string1\bvar2=string2 
DEPOT=//depot 
SDCMD=sd.exe -p %fnvar%(%var2%) print -o %srcsrvtrg% -q %depot%/%var3%#%var4%
SDTRG=%targ%\%var2%\%fnbksl%(%var3%)\%var4%\%fnfile%(%var1%) 
WIN_SDKTOOLS= sserver.microsoft.com:4444 
SRCSRV: source files --------------------------------------- 
<path1>*<var2>*<var3>*<var4> 
<path2>*<var2>*<var3>*<var4> 
<path3>*<var2>*<var3>*<var4> 
<path4>*<var2>*<var3>*<var4> 
SRCSRV: end ------------------------------------------------
```

<span data-ttu-id="b3ccb-169">Tout le texte est interprété littéralement, à l’exception du texte placé entre les signes de pourcentage (%).</span><span class="sxs-lookup"><span data-stu-id="b3ccb-169">All text is interpreted literally, except for text enclosed in percent signs (%).</span></span> <span data-ttu-id="b3ccb-170">Le texte placé entre les signes de pourcentage est traité comme un nom de variable à résoudre de manière récursive, sauf s’il s’agit de l’une des fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="b3ccb-170">Text enclosed in percent signs is treated as a variable name to be resolved recursively, unless it is one of the following functions:</span></span>

<dl> <dt>

<span data-ttu-id="b3ccb-171"><span id="_fnvar___"></span><span id="_FNVAR___"></span>%fnvar%()</span><span class="sxs-lookup"><span data-stu-id="b3ccb-171"><span id="_fnvar___"></span><span id="_FNVAR___"></span>%fnvar%()</span></span>
</dt> <dd>

<span data-ttu-id="b3ccb-172">Le texte du paramètre doit être placé entre des signes de pourcentage et traité comme une variable à développer.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-172">The parameter text should be enclosed in percent signs and treated as a variable to be expanded.</span></span>

</dd> <dt>

<span data-ttu-id="b3ccb-173"><span id="_fnbksl___"></span><span id="_FNBKSL___"></span>%fnbksl%()</span><span class="sxs-lookup"><span data-stu-id="b3ccb-173"><span id="_fnbksl___"></span><span id="_FNBKSL___"></span>%fnbksl%()</span></span>
</dt> <dd>

<span data-ttu-id="b3ccb-174">Toutes les barres obliques (/) dans le texte du paramètre doivent être remplacées par des barres obliques inverses ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="b3ccb-174">All forward slashes (/) in the parameter text should be replaced with backward slashes (\\).</span></span>

</dd> <dt>

<span data-ttu-id="b3ccb-175"><span id="_fnfile___"></span><span id="_FNFILE___"></span>%fnfile%()</span><span class="sxs-lookup"><span data-stu-id="b3ccb-175"><span id="_fnfile___"></span><span id="_FNFILE___"></span>%fnfile%()</span></span>
</dt> <dd>

<span data-ttu-id="b3ccb-176">Toutes les informations de chemin d’accès dans le texte du paramètre doivent être supprimées, en laissant uniquement le nom du fichier.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-176">All path information in the parameter text should be stripped out, leaving only the file name.</span></span>

</dd> </dl>

<span data-ttu-id="b3ccb-177">La section ini contient des variables qui décrivent les exigences.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-177">The ini section contains variables that describe the requirements.</span></span> <span data-ttu-id="b3ccb-178">Le script d’indexation peut ajouter n’importe quel nombre de variables à cette section.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-178">The indexing script can add any number of variables to this section.</span></span> <span data-ttu-id="b3ccb-179">Voici quelques exemples :</span><span class="sxs-lookup"><span data-stu-id="b3ccb-179">The following are examples:</span></span>

<dl> <dt>

<span data-ttu-id="b3ccb-180"><span id="VERSION"></span><span id="version"></span>Version</span><span class="sxs-lookup"><span data-stu-id="b3ccb-180"><span id="VERSION"></span><span id="version"></span>VERSION</span></span>
</dt> <dd>

<span data-ttu-id="b3ccb-181">Version de la spécification de langage.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-181">The language specification version.</span></span> <span data-ttu-id="b3ccb-182">Cette variable est requise.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-182">This variable is required.</span></span>

</dd> <dt>

<span data-ttu-id="b3ccb-183"><span id="VERCTL"></span><span id="verctl"></span>VERCTL</span><span class="sxs-lookup"><span data-stu-id="b3ccb-183"><span id="VERCTL"></span><span id="verctl"></span>VERCTL</span></span>
</dt> <dd>

<span data-ttu-id="b3ccb-184">Chaîne qui décrit le produit de contrôle de code source.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-184">A string that describes the source control product.</span></span> <span data-ttu-id="b3ccb-185">Cette variable est facultative.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-185">This variable is optional.</span></span>

</dd> <dt>

<span data-ttu-id="b3ccb-186"><span id="DATETIME"></span><span id="datetime"></span>Date/heure</span><span class="sxs-lookup"><span data-stu-id="b3ccb-186"><span id="DATETIME"></span><span id="datetime"></span>DATETIME</span></span>
</dt> <dd>

<span data-ttu-id="b3ccb-187">Chaîne qui indique la date et l’heure de traitement du fichier PDB.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-187">A string that indicates the date and time the PDB file was processed.</span></span> <span data-ttu-id="b3ccb-188">Cette variable est facultative.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-188">This variable is optional.</span></span>

</dd> </dl>

<span data-ttu-id="b3ccb-189">La section variables contient des variables qui décrivent comment extraire un fichier du contrôle de code source.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-189">The variables section contains variables that describe how to extract a file from source control.</span></span> <span data-ttu-id="b3ccb-190">Il peut également être utilisé pour définir des variables de texte couramment utilisées en tant que variables afin de réduire la taille du bloc de données.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-190">It can also be used to define commonly used text as variables to reduce the size of the data block.</span></span>

<dl> <dt>

<span data-ttu-id="b3ccb-191"><span id="SRCSRVTRG"></span><span id="srcsrvtrg"></span>SRCSRVTRG</span><span class="sxs-lookup"><span data-stu-id="b3ccb-191"><span id="SRCSRVTRG"></span><span id="srcsrvtrg"></span>SRCSRVTRG</span></span>
</dt> <dd>

<span data-ttu-id="b3ccb-192">Décrit comment générer le chemin d’accès cible pour le fichier extrait.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-192">Describes how to build the target path for the extracted file.</span></span> <span data-ttu-id="b3ccb-193">Il s’agit d’une variable obligatoire.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-193">This is a required variable.</span></span>

</dd> <dt>

<span data-ttu-id="b3ccb-194"><span id="SRCSRVCMD"></span><span id="srcsrvcmd"></span>SRCSRVCMD</span><span class="sxs-lookup"><span data-stu-id="b3ccb-194"><span id="SRCSRVCMD"></span><span id="srcsrvcmd"></span>SRCSRVCMD</span></span>
</dt> <dd>

<span data-ttu-id="b3ccb-195">Décrit comment générer la commande pour extraire le fichier du contrôle de code source.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-195">Describes how to build the command to extract the file from source control.</span></span> <span data-ttu-id="b3ccb-196">Cela comprend le nom du fichier exécutable et ses paramètres de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-196">This includes the name of the executable file and its command-line parameters.</span></span> <span data-ttu-id="b3ccb-197">Il s’agit d’une variable obligatoire.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-197">This is a required variable.</span></span>

</dd> <dt>

<span data-ttu-id="b3ccb-198"><span id="SRCSRVENV"></span><span id="srcsrvenv"></span>SRCSRVENV</span><span class="sxs-lookup"><span data-stu-id="b3ccb-198"><span id="SRCSRVENV"></span><span id="srcsrvenv"></span>SRCSRVENV</span></span>
</dt> <dd>

<span data-ttu-id="b3ccb-199">Chaîne qui répertorie les variables d’environnement à créer lors de l’extraction de fichier.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-199">A string that lists environment variables to be created during the file extraction.</span></span> <span data-ttu-id="b3ccb-200">Séparez plusieurs entrées par un caractère de retour arrière ( \\ b).</span><span class="sxs-lookup"><span data-stu-id="b3ccb-200">Separate multiple entries with a backspace character (\\b).</span></span> <span data-ttu-id="b3ccb-201">Il s’agit d’une variable facultative.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-201">This is an optional variable.</span></span>

</dd> </dl>

<span data-ttu-id="b3ccb-202">La section fichiers sources contient une entrée pour chaque fichier source qui a été indexé.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-202">The source files section contains an entry for each source file that has been indexed.</span></span> <span data-ttu-id="b3ccb-203">Le contenu de chaque ligne est interprété comme une variable avec les noms VAR1, VAR2, VAR3, et ainsi de suite jusqu’à VAR10.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-203">The contents of each line are interpreted as variables with the names VAR1, VAR2, VAR3, and so on until VAR10.</span></span> <span data-ttu-id="b3ccb-204">Les variables sont séparées par des astérisques.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-204">The variables are separated by asterisks.</span></span> <span data-ttu-id="b3ccb-205">VAR1 doit spécifier le chemin d’accès complet au fichier source, comme indiqué ailleurs dans le fichier PDB.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-205">VAR1 must specify the fully qualified path to the source file as listed elsewhere in the PDB file.</span></span> <span data-ttu-id="b3ccb-206">Par exemple, la ligne suivante :</span><span class="sxs-lookup"><span data-stu-id="b3ccb-206">For example, the following line:</span></span>

``` syntax
c:\proj\src\file.cpp*TOOLS_PRJ*tools/mytool/src/file.cpp*3
```

<span data-ttu-id="b3ccb-207">est interprété comme suit :</span><span class="sxs-lookup"><span data-stu-id="b3ccb-207">is interpreted as follows:</span></span>

``` syntax
VAR1=c:\proj\src\file.cpp
VAR2=TOOLS_PRJ
VAR3=tools/mytool/src/file.cpp
VAR4=3
```

<span data-ttu-id="b3ccb-208">Dans cet exemple, VAR4 est un numéro de version.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-208">In this example, VAR4 is a version number.</span></span> <span data-ttu-id="b3ccb-209">Toutefois, la plupart des systèmes de contrôle de code source prennent en charge l’étiquetage des fichiers de sorte que l’état source d’une build donnée puisse être restauré.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-209">However, most source control systems support labeling files in such a way that the source state for a given build can be restored.</span></span> <span data-ttu-id="b3ccb-210">Par conséquent, vous pouvez également utiliser l’étiquette pour la Build.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-210">Therefore, you could alternately use the label for the build.</span></span> <span data-ttu-id="b3ccb-211">L’exemple de bloc de données peut être modifié pour contenir une variable telle que la suivante :</span><span class="sxs-lookup"><span data-stu-id="b3ccb-211">The sample data block could be modified to contain a variable such as the following:</span></span>

``` syntax
LABEL=BUILD47
```

<span data-ttu-id="b3ccb-212">Ensuite, en supposant que le système de contrôle de code source utilise l’arobase (@) pour indiquer une étiquette, vous pouvez modifier la variable SRCSRVCMD comme suit :</span><span class="sxs-lookup"><span data-stu-id="b3ccb-212">Then, presuming the source control system uses the at sign (@) to indicate a label, you could modify the SRCSRVCMD variable as follows:</span></span>

<span data-ttu-id="b3ccb-213">**sd.exe-p% fnvar%(% Var2%) imprimer-o% srcsrvtrg%-q% Depot%/%var3% @% label%**</span><span class="sxs-lookup"><span data-stu-id="b3ccb-213">**sd.exe -p %fnvar%(%var2%) print -o %srcsrvtrg% -q %depot%/%var3%@%label%**</span></span>

## <a name="how-source-server-works"></a><span data-ttu-id="b3ccb-214">Fonctionnement du serveur source</span><span class="sxs-lookup"><span data-stu-id="b3ccb-214">How Source Server Works</span></span>

<span data-ttu-id="b3ccb-215">Le client du serveur source est implémenté dans Symsrv.dll.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-215">The source server client is implemented in Symsrv.dll.</span></span> <span data-ttu-id="b3ccb-216">Le client n’extrait pas les informations directement à partir du fichier PDB ; elle utilise un gestionnaire de symboles comme celui implémenté dans Dbghelp.dll.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-216">The client does not extract information directly from the PDB file; it uses a symbol handler such as the one implemented in Dbghelp.dll.</span></span> <span data-ttu-id="b3ccb-217">Il s’agit essentiellement d’un moteur de substitution de variables récursives qui crée une ligne de commande qui peut être utilisée pour extraire le fichier source approprié du système de contrôle de code source.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-217">It is essentially a recursive variable substitution engine that creates a command line that can be used to extract the proper source file from the source control system.</span></span> <span data-ttu-id="b3ccb-218">Votre code ne doit pas appeler Symsrv.dll directement.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-218">Your code should not call Symsrv.dll directly.</span></span> <span data-ttu-id="b3ccb-219">Pour intégrer ses fonctionnalités à votre application, utilisez la fonction [**SymGetSourceFile**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefile) .</span><span class="sxs-lookup"><span data-stu-id="b3ccb-219">To integrate its functionality into your application, use the [**SymGetSourceFile**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefile) function.</span></span>

<span data-ttu-id="b3ccb-220">La première version du serveur source fonctionne comme suit.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-220">The first version of source server works as follows.</span></span> <span data-ttu-id="b3ccb-221">Ce comportement peut changer dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-221">This behavior may change in future versions.</span></span>

-   <span data-ttu-id="b3ccb-222">Le client appelle la fonction **SrcSrvInit** avec le chemin d’accès cible à utiliser comme base pour toutes les extractions de fichiers sources.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-222">The client calls the **SrcSrvInit** function with the target path to be used as a base for all source file extractions.</span></span> <span data-ttu-id="b3ccb-223">Elle stocke ce chemin d’accès dans la variable ENSION.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-223">It stores this path in the TARG variable.</span></span>
-   <span data-ttu-id="b3ccb-224">Le client extrait le flux SRCSRV du fichier PDB lorsque le PDB du module est chargé et appelle la fonction **SrcSrvLoadModule** pour passer le bloc de données au serveur source.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-224">The client extracts the Srcsrv stream from the PDB when the module PDB is loaded and calls the **SrcSrvLoadModule** function to pass the data block to source server.</span></span>
-   <span data-ttu-id="b3ccb-225">Lorsque dbghelp récupère un fichier source, le client appelle la fonction **SrcSrvGetFile** pour récupérer les fichiers sources à partir du contrôle de code source.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-225">When Dbghelp retrieves a source file, the client calls the **SrcSrvGetFile** function to retrieve the source files from source control.</span></span>
-   <span data-ttu-id="b3ccb-226">Le serveur source recherche dans le bloc de données les entrées de fichier source pour une entrée qui correspond au fichier demandé.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-226">Source server searches the source file entries in the data block for an entry that matches the requested file.</span></span> <span data-ttu-id="b3ccb-227">Il remplit VAR1 en VAR *n* avec le contenu de l’entrée du fichier source.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-227">It fills VAR1 to VAR *n* with the contents of the source file entry.</span></span> <span data-ttu-id="b3ccb-228">Ensuite, il étend la variable SRCSRVTRG en utilisant VAR1 à VAR *n*.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-228">Next, it expands the SRCSRVTRG variable using VAR1 to VAR *n*.</span></span> <span data-ttu-id="b3ccb-229">Si le fichier se trouve déjà à cet emplacement, il retourne l’emplacement à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-229">If the file is already in this location, it returns the location to the caller.</span></span> <span data-ttu-id="b3ccb-230">Dans le cas contraire, il développe la variable SRCSRVCMD pour générer la commande nécessaire pour récupérer le fichier du contrôle de code source et le copier à l’emplacement cible.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-230">Otherwise, it expands the SRCSRVCMD variable to build the command needed to retrieve the file from source control and copy it to the target location.</span></span> <span data-ttu-id="b3ccb-231">Enfin, elle exécute cette commande.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-231">Finally, it executes this command.</span></span>

## <a name="creating-a-source-control-provider-module"></a><span data-ttu-id="b3ccb-232">Création d’un module fournisseur de contrôle de code source</span><span class="sxs-lookup"><span data-stu-id="b3ccb-232">Creating a Source Control Provider Module</span></span>

<span data-ttu-id="b3ccb-233">Le serveur source comprend des modules de fournisseur pour Perforce (p4.pm) et Visual Source Safe (vss.pm).</span><span class="sxs-lookup"><span data-stu-id="b3ccb-233">The source server includes provider modules for Perforce (p4.pm) and Visual Source Safe (vss.pm).</span></span> <span data-ttu-id="b3ccb-234">Pour créer votre propre module de fournisseur, vous devez implémenter l’ensemble d’interfaces suivant.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-234">To create your own provider module, you must implement the following set of interfaces.</span></span>

<dl> <dt>

<span data-ttu-id="b3ccb-235"><span id="_module__SimpleUsage__"></span><span id="_module__simpleusage__"></span><span id="_MODULE__SIMPLEUSAGE__"></span>**$module :: SimpleUsage ()**</span><span class="sxs-lookup"><span data-stu-id="b3ccb-235"><span id="_module__SimpleUsage__"></span><span id="_module__simpleusage__"></span><span id="_MODULE__SIMPLEUSAGE__"></span>**$module::SimpleUsage()**</span></span>
</dt> <dd>

<span data-ttu-id="b3ccb-236">Objectif : affiche des informations d’utilisation de module simples dans STDOUT.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-236">Purpose: Displays simple module usage information to STDOUT.</span></span>

<span data-ttu-id="b3ccb-237">Paramètres : aucun</span><span class="sxs-lookup"><span data-stu-id="b3ccb-237">Parameters: None</span></span>

<span data-ttu-id="b3ccb-238">Valeur de retour : aucune</span><span class="sxs-lookup"><span data-stu-id="b3ccb-238">Return value: None</span></span>

</dd> <dt>

<span data-ttu-id="b3ccb-239"><span id="_module__VerboseUsage__"></span><span id="_module__verboseusage__"></span><span id="_MODULE__VERBOSEUSAGE__"></span>**$module :: VerboseUsage ()**</span><span class="sxs-lookup"><span data-stu-id="b3ccb-239"><span id="_module__VerboseUsage__"></span><span id="_module__verboseusage__"></span><span id="_MODULE__VERBOSEUSAGE__"></span>**$module::VerboseUsage()**</span></span>
</dt> <dd>

<span data-ttu-id="b3ccb-240">Objectif : affiche des informations d’utilisation de module approfondies dans STDOUT.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-240">Purpose: Displays in-depth module usage information to STDOUT.</span></span>

<span data-ttu-id="b3ccb-241">Paramètres : aucun</span><span class="sxs-lookup"><span data-stu-id="b3ccb-241">Parameters: None</span></span>

<span data-ttu-id="b3ccb-242">Valeur de retour : aucune</span><span class="sxs-lookup"><span data-stu-id="b3ccb-242">Return value: None</span></span>

</dd> <dt>

<span data-ttu-id="b3ccb-243"><span id="_objref____module__new__CommandArguments_"></span><span id="_objref____module__new__commandarguments_"></span><span id="_OBJREF____MODULE__NEW__COMMANDARGUMENTS_"></span>**$objref = $module :: New ( \@ CommandArguments)**</span><span class="sxs-lookup"><span data-stu-id="b3ccb-243"><span id="_objref____module__new__CommandArguments_"></span><span id="_objref____module__new__commandarguments_"></span><span id="_OBJREF____MODULE__NEW__COMMANDARGUMENTS_"></span>**$objref = $module::new(\@CommandArguments)**</span></span>
</dt> <dd>

<span data-ttu-id="b3ccb-244">Objectif : Initialise une instance du module fournisseur.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-244">Purpose: Initializes an instance of the provider module.</span></span>

<span data-ttu-id="b3ccb-245">Parameters : tous les @ARGV arguments qui n’ont pas été reconnus par SSIndex. cmd comme des arguments généraux.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-245">Parameters: All @ARGV arguments that were not recognized by SSIndex.cmd as being general arguments.</span></span>

<span data-ttu-id="b3ccb-246">Valeur de retour : référence qui peut être utilisée dans les opérations ultérieures.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-246">Return value: A reference that can be used in later operations.</span></span>

</dd> <dt>

<span data-ttu-id="b3ccb-247"><span id="_objref-_GatherFileInformation__SourcePath___ServerHashReference_"></span><span id="_objref-_gatherfileinformation__sourcepath___serverhashreference_"></span><span id="_OBJREF-_GATHERFILEINFORMATION__SOURCEPATH___SERVERHASHREFERENCE_"></span>**$objref->GatherFileInformation ($SourcePath, $ServerHashReference)**</span><span class="sxs-lookup"><span data-stu-id="b3ccb-247"><span id="_objref-_GatherFileInformation__SourcePath___ServerHashReference_"></span><span id="_objref-_gatherfileinformation__sourcepath___serverhashreference_"></span><span id="_OBJREF-_GATHERFILEINFORMATION__SOURCEPATH___SERVERHASHREFERENCE_"></span>**$objref->GatherFileInformation($SourcePath, $ServerHashReference)**</span></span>
</dt> <dd>

<span data-ttu-id="b3ccb-248">Objectif : permet au module de collecter les informations d’indexation source requises pour le répertoire spécifié par le paramètre $SourcePath.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-248">Purpose: Enables the module to gather the required source indexing information for the directory specified by the $SourcePath parameter.</span></span> <span data-ttu-id="b3ccb-249">Le module ne doit pas supposer que cette entrée sera appelée une seule fois pour chaque instance d’objet, car SSIndex. cmd peut l’appeler plusieurs fois pour différents chemins d’accès.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-249">The module should not assume that this entry will be called only once for each object instance, as SSIndex.cmd may call it multiple times for different paths.</span></span>

<span data-ttu-id="b3ccb-250">Paramètres : (1) répertoire local contenant la source à indexer.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-250">Parameters: (1) The local directory containing the source to be indexed.</span></span> <span data-ttu-id="b3ccb-251">(2) référence à un hachage contenant toutes les entrées du fichier de Srcsrv.ini spécifié.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-251">(2) A reference to a hash containing all of the entries from the specified Srcsrv.ini file.</span></span>

<span data-ttu-id="b3ccb-252">Valeur de retour : aucune</span><span class="sxs-lookup"><span data-stu-id="b3ccb-252">Return value: None</span></span>

</dd> <dt>

<span data-ttu-id="b3ccb-253"><span id="__VariableHashReference___FileEntry_____objref-_GetFileInfo__LocalFile_"></span><span id="__variablehashreference___fileentry_____objref-_getfileinfo__localfile_"></span><span id="__VARIABLEHASHREFERENCE___FILEENTRY_____OBJREF-_GETFILEINFO__LOCALFILE_"></span>**($VariableHashReference, $FileEntry) = $objref->GetFileInfo ($LocalFile)**</span><span class="sxs-lookup"><span data-stu-id="b3ccb-253"><span id="__VariableHashReference___FileEntry_____objref-_GetFileInfo__LocalFile_"></span><span id="__variablehashreference___fileentry_____objref-_getfileinfo__localfile_"></span><span id="__VARIABLEHASHREFERENCE___FILEENTRY_____OBJREF-_GETFILEINFO__LOCALFILE_"></span>**($VariableHashReference, $FileEntry) = $objref->GetFileInfo($LocalFile)**</span></span>
</dt> <dd>

<span data-ttu-id="b3ccb-254">Objectif : fournit les informations nécessaires pour extraire un seul fichier spécifique du système de contrôle de code source.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-254">Purpose: Provides the necessary information to extract a single, specific file from the source control system.</span></span>

<span data-ttu-id="b3ccb-255">Paramètres : nom de fichier complet</span><span class="sxs-lookup"><span data-stu-id="b3ccb-255">Parameters: A fully qualified file name</span></span>

<span data-ttu-id="b3ccb-256">Valeur de retour : (1) référence de hachage des variables nécessaires à l’interprétation de la $FileEntry retournée.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-256">Return value: (1) A hash reference of the variables necessary to interpret the returned $FileEntry.</span></span> <span data-ttu-id="b3ccb-257">SSIndex. cmd met en cache ces variables pour chaque fichier source utilisé par un fichier de débogage unique pour réduire la quantité d’informations écrites dans le flux d’index source.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-257">SSIndex.cmd caches these variables for every source file used by a single debug file to reduce the amount of information written to the source index stream.</span></span> <span data-ttu-id="b3ccb-258">(2) entrée de fichier à écrire dans le flux d’index source pour permettre SrcSrv.dll d’extraire ce fichier du contrôle de code source.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-258">(2) The file entry to be written to the source index stream to allow SrcSrv.dll to extract this file from source control.</span></span> <span data-ttu-id="b3ccb-259">Le format exact de cette ligne est spécifique au système de contrôle de code source.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-259">The exact format of this line is specific to the source control system.</span></span>

</dd> <dt>

<span data-ttu-id="b3ccb-260"><span id="_TextString____objref-_LongName__"></span><span id="_textstring____objref-_longname__"></span><span id="_TEXTSTRING____OBJREF-_LONGNAME__"></span>**$TextString = $objref->LongName ()**</span><span class="sxs-lookup"><span data-stu-id="b3ccb-260"><span id="_TextString____objref-_LongName__"></span><span id="_textstring____objref-_longname__"></span><span id="_TEXTSTRING____OBJREF-_LONGNAME__"></span>**$TextString = $objref->LongName()**</span></span>
</dt> <dd>

<span data-ttu-id="b3ccb-261">Objectif : fournit une chaîne descriptive permettant d’identifier le fournisseur de contrôle de code source pour l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-261">Purpose: Provides a descriptive string to identify the source control provider to the end user.</span></span>

<span data-ttu-id="b3ccb-262">Paramètres : aucun</span><span class="sxs-lookup"><span data-stu-id="b3ccb-262">Parameters: None</span></span>

<span data-ttu-id="b3ccb-263">Valeur de retour : nom descriptif du système de contrôle de code source.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-263">Return value: The descriptive name of the source control system.</span></span>

</dd> <dt>

<span data-ttu-id="b3ccb-264"><span id="_StreamVariableLines____objref-_SourceStreamVariables__"></span><span id="_streamvariablelines____objref-_sourcestreamvariables__"></span><span id="_STREAMVARIABLELINES____OBJREF-_SOURCESTREAMVARIABLES__"></span>**@StreamVariableLines = $objref->SourceStreamVariables ()**</span><span class="sxs-lookup"><span data-stu-id="b3ccb-264"><span id="_StreamVariableLines____objref-_SourceStreamVariables__"></span><span id="_streamvariablelines____objref-_sourcestreamvariables__"></span><span id="_STREAMVARIABLELINES____OBJREF-_SOURCESTREAMVARIABLES__"></span>**@StreamVariableLines = $objref->SourceStreamVariables()**</span></span>
</dt> <dd>

<span data-ttu-id="b3ccb-265">Objectif : permet au fournisseur de contrôle de code source d’ajouter des variables spécifiques au contrôle de code source dans le flux source pour chaque fichier de débogage.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-265">Purpose: Enables the source control provider to add source control specific variables to the source stream for each debug file.</span></span> <span data-ttu-id="b3ccb-266">Les exemples de modules utilisent cette méthode pour écrire les \_ variables cibles Extract cmd et extract \_ .</span><span class="sxs-lookup"><span data-stu-id="b3ccb-266">The sample modules use this method for writing the required EXTRACT\_CMD and EXTRACT\_TARGET variables.</span></span>

<span data-ttu-id="b3ccb-267">Paramètres : aucun</span><span class="sxs-lookup"><span data-stu-id="b3ccb-267">Parameters: None</span></span>

<span data-ttu-id="b3ccb-268">Valeur de retour : liste des entrées pour les variables de flux source.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-268">Return value: The list of entries for the source stream variables.</span></span>

</dd> </dl>

 

 




