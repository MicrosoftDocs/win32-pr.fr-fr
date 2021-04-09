---
description: Cette rubrique décrit deux utilitaires utilisés pour créer des applications MUI.
ms.assetid: 8ba94001-fc46-41e0-a071-0dc500a20753
title: Utilitaires de ressource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 550cf283779a57bc5ca35f88d336646b061c3f1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952602"
---
# <a name="resource-utilities"></a><span data-ttu-id="61afd-103">Utilitaires de ressource</span><span class="sxs-lookup"><span data-stu-id="61afd-103">Resource Utilities</span></span>

<span data-ttu-id="61afd-104">Cette rubrique décrit deux utilitaires utilisés pour créer des applications MUI.</span><span class="sxs-lookup"><span data-stu-id="61afd-104">This topic describes two utilities used to build MUI applications.</span></span> <span data-ttu-id="61afd-105">Bien que MUIRCT soit un outil spécifique à MUI, MUI utilise également l’utilitaire de compilation Windows RC standard.</span><span class="sxs-lookup"><span data-stu-id="61afd-105">While MUIRCT is a MUI-specific tool, MUI also makes use of the standard Windows RC Compiler utility.</span></span> <span data-ttu-id="61afd-106">Les instructions relatives à l’utilisation de ces utilitaires sont fournies dans [localisation des ressources et génération de l’application](localizing-resources-and-building-the-application.md).</span><span class="sxs-lookup"><span data-stu-id="61afd-106">Instructions for using these utilities are provided in [Localizing Resources and Building the Application](localizing-resources-and-building-the-application.md).</span></span>

## <a name="muirct-utility"></a><span data-ttu-id="61afd-107">Utilitaire MUIRCT</span><span class="sxs-lookup"><span data-stu-id="61afd-107">MUIRCT Utility</span></span>

<span data-ttu-id="61afd-108">MUIRCT (Muirct.exe) est un utilitaire de ligne de commande permettant de fractionner un fichier exécutable standard en fichier LN et de fichiers de ressources spécifiques à une langue (c’est-à-dire localisables).</span><span class="sxs-lookup"><span data-stu-id="61afd-108">MUIRCT (Muirct.exe) is a command line utility for splitting a standard executable file into an LN file and language-specific (that is, localizable) resource files.</span></span> <span data-ttu-id="61afd-109">Chacun des fichiers résultants contient des données de configuration de ressource pour l’Association de fichiers.</span><span class="sxs-lookup"><span data-stu-id="61afd-109">Each of the resulting files contains resource configuration data for file association.</span></span> <span data-ttu-id="61afd-110">MUIRCT est inclus dans le Microsoft Windows SDK pour Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="61afd-110">MUIRCT is included in the Microsoft Windows SDK for Windows Vista.</span></span>

> [!Note]  
> <span data-ttu-id="61afd-111">À compter de Windows Vista, le chargeur de ressources Win32 est mis à jour pour charger des ressources à partir de fichiers spécifiques à une langue et à partir de fichiers LN.</span><span class="sxs-lookup"><span data-stu-id="61afd-111">Starting with Windows Vista, the Win32 resource loader is updated to load resources from language-specific files as well as from LN files.</span></span>

 

### <a name="muirct-usages"></a><span data-ttu-id="61afd-112">Utilisations de MUIRCT</span><span class="sxs-lookup"><span data-stu-id="61afd-112">MUIRCT Usages</span></span>

1.  <span data-ttu-id="61afd-113">Fractionnez le binaire en fichier binaire principal et en fichier MUI basé sur le \_ fichier de configuration RC.</span><span class="sxs-lookup"><span data-stu-id="61afd-113">Split binary into main binary and mui file based on rc\_config file.</span></span>

    `Muirct -q rc_config [-c checksum_file [-b LangID]] [-x LangID] [-g LangId]     [-f] [-m] [-v level] source_file [output_LN_file] [output_MUI_file]`

2.  <span data-ttu-id="61afd-114">Extrayez la somme de contrôle du fichier de somme de contrôle \_ et insérez-la dans le fichier de sortie \_ .</span><span class="sxs-lookup"><span data-stu-id="61afd-114">Extract checksum from checksum\_file and insert it in output\_file.</span></span>

    `Muirct -c checksum_file [-b LangID] -e output_file`

3.  <span data-ttu-id="61afd-115">Calculez la somme de contrôle en fonction du fichier de somme de contrôle \_ et insérez-la dans le fichier de sortie \_ .</span><span class="sxs-lookup"><span data-stu-id="61afd-115">Calculate checksum based on checksum\_file and insert it in output\_file.</span></span>

    `Muirct  -c checksum_file [-b LangID] -q rc_config  -z output_file`

4.  <span data-ttu-id="61afd-116">Vider le contenu des données de configuration des ressources à partir du fichier d’entrée \_ .</span><span class="sxs-lookup"><span data-stu-id="61afd-116">Dump resource configuration data contents from input\_file.</span></span>

    `Muirct -d input_file`

### <a name="muirct-syntax"></a><span data-ttu-id="61afd-117">Syntaxe MUIRCT</span><span class="sxs-lookup"><span data-stu-id="61afd-117">MUIRCT Syntax</span></span>

<span data-ttu-id="61afd-118">MUIRCT peut prendre la direction des commutateurs de ligne de commande et/ou d’un fichier de configuration de ressource, spécifié à l’aide du commutateur-q.</span><span class="sxs-lookup"><span data-stu-id="61afd-118">MUIRCT can take direction from command line switches and/or from a resource configuration file, specified using the -q switch.</span></span>


```C++
muirct [-h|-?] [ -c checksum_file] [-b langid]  ]
     [-g langid] [-q resource configuration file<RCF>] [-v level] [-x langid]
     [-e output_file]  [-z output_file] [-f] [-d MUI'ized file] [-m file_version]

source_filename [language_neutral_filename] [mui_filename]
```



<span data-ttu-id="61afd-119">**Commutateurs et arguments**</span><span class="sxs-lookup"><span data-stu-id="61afd-119">**Switches and Arguments**</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="61afd-120">-h |- ?</span><span class="sxs-lookup"><span data-stu-id="61afd-120">-h|-?</span></span></td>
<td><span data-ttu-id="61afd-121">Affiche l’écran d’aide.</span><span class="sxs-lookup"><span data-stu-id="61afd-121">Shows help screen.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="61afd-122">-c</span><span class="sxs-lookup"><span data-stu-id="61afd-122">-c</span></span></td>
<td><span data-ttu-id="61afd-123">Spécifie le checksum_file d’entrée à partir duquel extraire ou calculer la somme de contrôle de la ressource.</span><span class="sxs-lookup"><span data-stu-id="61afd-123">Specifies the input checksum_file from which to extract or calculate the resource checksum.</span></span> <span data-ttu-id="61afd-124">Checksum_file doit être un fichier binaire Win32 contenant des ressources localisables.</span><span class="sxs-lookup"><span data-stu-id="61afd-124">Checksum_file must be a Win32 binary file containing localizable resources.</span></span> <span data-ttu-id="61afd-125">Si checksum_file contient des ressources pour plusieurs langages, le commutateur-b doit être utilisé pour spécifier ceux qui doivent être utilisés, sans quoi MUIRCT échoue.</span><span class="sxs-lookup"><span data-stu-id="61afd-125">If checksum_file contains resources for more than one language, the -b switch must be used to specify which of these should be used otherwise MUIRCT fails.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="61afd-126">-b</span><span class="sxs-lookup"><span data-stu-id="61afd-126">-b</span></span></td>
<td><span data-ttu-id="61afd-127">Spécifie la langue à utiliser lorsque la checksum_file spécifiée avec-c contient des ressources dans plusieurs langues.</span><span class="sxs-lookup"><span data-stu-id="61afd-127">Specifies the language to be used when the checksum_file specified with -c contains resources in multiple languages.</span></span> <span data-ttu-id="61afd-128">Ce commutateur peut être utilisé uniquement conjointement avec le commutateur-c.</span><span class="sxs-lookup"><span data-stu-id="61afd-128">This switch can only be used in conjunction with the -c switch.</span></span> <span data-ttu-id="61afd-129">L’identificateur de langue peut être au format décimal ou hexadécimal.</span><span class="sxs-lookup"><span data-stu-id="61afd-129">The language identifier can be in decimal or hexadecimal format.</span></span> <span data-ttu-id="61afd-130">MUIRCT échoue si le checksum_file contient des ressources dans plusieurs langues et que-b n’est pas spécifié ou si la langue spécifiée par le commutateur-b est introuvable dans le checksum_file.</span><span class="sxs-lookup"><span data-stu-id="61afd-130">MUIRCT fails if the checksum_file contains resources in multiple language and the -b is not specified or if the language specified by the -b switch cannot be found in the checksum_file.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="61afd-131">-g</span><span class="sxs-lookup"><span data-stu-id="61afd-131">-g</span></span></td>
<td><span data-ttu-id="61afd-132">Spécifie l’ID de langue à inclure comme langue de secours ultime dans la section des données de configuration de ressource du fichier LN.</span><span class="sxs-lookup"><span data-stu-id="61afd-132">Specifies the language ID to be included as the ultimate fallback language in the resource configuration data section of the LN file.</span></span> <span data-ttu-id="61afd-133">Si le chargeur de ressources ne parvient pas à charger un fichier. mui demandé à partir des langues d’interface utilisateur préférées du thread, il utilise le langage de secours ultime comme dernière tentative.</span><span class="sxs-lookup"><span data-stu-id="61afd-133">If the resource loader fails to load a requested .mui file from the thread preferred UI languages, it uses the ultimate fallback language as its last attempt.</span></span> <span data-ttu-id="61afd-134">La valeur LangID peut être spécifiée au format décimal ou hexadécimal.</span><span class="sxs-lookup"><span data-stu-id="61afd-134">The LangID value can be specified in decimal or hexadecimal format.</span></span> <span data-ttu-id="61afd-135">Par exemple, l’anglais (États-Unis) peut être spécifié par-g 0x40C ou-g 1033.</span><span class="sxs-lookup"><span data-stu-id="61afd-135">For example English (United States) can be specified by -g 0x409 or -g 1033.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="61afd-136">-q</span><span class="sxs-lookup"><span data-stu-id="61afd-136">-q</span></span></td>
<td><span data-ttu-id="61afd-137">Spécifie que le source_file doit être fractionné dans le output_LN_file et le output_MUI_file en fonction de la disposition de fichier rc_config.</span><span class="sxs-lookup"><span data-stu-id="61afd-137">Specifies that the source_file is to be split into the output_LN_file and the output_MUI_file according to the rc_config file layout.</span></span> <span data-ttu-id="61afd-138">Le fichier rc_config est un fichier au format XML qui spécifie les ressources qui seront extraites dans le fichier. mui et qui seront conservées dans le fichier LN.</span><span class="sxs-lookup"><span data-stu-id="61afd-138">The rc_config file is an XML formatted file that specifies which resources will be extracted to the .mui file and which will be left in the LN file.</span></span> <span data-ttu-id="61afd-139">La rc_config peut spécifier la distribution des types de ressources et des éléments nommés individuels entre le output_LN_file et le output_MUI_file.</span><span class="sxs-lookup"><span data-stu-id="61afd-139">The rc_config can specify the distribution of resource types and individual named items between the output_LN_file and output_MUI_file.</span></span> <span data-ttu-id="61afd-140">Le source_file doit être un fichier binaire Win32 qui contient des ressources dans une seule langue, sans quoi MUIRCT échoue.</span><span class="sxs-lookup"><span data-stu-id="61afd-140">The source_file must be a Win32 binary that contains resources in a single language otherwise MUIRCT fails.</span></span> <span data-ttu-id="61afd-141">MUIRCT ne fractionne pas le fichier s’il est indépendant de la langue, ce qui est indiqué par la présence d’une seule valeur d’ID de langue égale à 0 dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="61afd-141">MUIRCT does not split the file if it is language neutral which is indicated by having only language ID value 0 in the file.</span></span> <span data-ttu-id="61afd-142">Les output_LN_file et output_mui_file sont les noms du fichier. mui et du langage neutre dans lequel l’source_file est fractionné.</span><span class="sxs-lookup"><span data-stu-id="61afd-142">The output_LN_file and output_mui_file are the names of the language neutral and .mui file into which the source_file is split.</span></span> <span data-ttu-id="61afd-143">Ces noms de fichiers sont facultatifs.</span><span class="sxs-lookup"><span data-stu-id="61afd-143">These file names are optional.</span></span> <span data-ttu-id="61afd-144">Si elles ne sont pas spécifiées, MUIRCT ajoute les extensions. ln et. mui pour source_file.</span><span class="sxs-lookup"><span data-stu-id="61afd-144">If they are not specified, MUIRCT appends the extensions .ln and .mui to source_file.</span></span> <span data-ttu-id="61afd-145">En général, vous devez supprimer l' &quot; extension. ln &quot; avant de déployer le fichier.</span><span class="sxs-lookup"><span data-stu-id="61afd-145">Typically you should remove the &quot;.ln&quot; extension before deploying the file.</span></span> <span data-ttu-id="61afd-146">MUIRCT associe le output_LN_file et output_MUI_file en calculant une somme de contrôle en fonction du nom de la source_file et de la version du fichier et en insérant le résultat dans la section de configuration des ressources de chaque fichier de sortie.</span><span class="sxs-lookup"><span data-stu-id="61afd-146">MUIRCT associates the output_LN_file and output_MUI_file by calculating a checksum based on the source_file name and file version and inserting the result into the resource configuration section of each output file.</span></span> <span data-ttu-id="61afd-147">Lorsqu’il est utilisé conjointement avec le commutateur-c, le commutateur-q est prioritaire.</span><span class="sxs-lookup"><span data-stu-id="61afd-147">When used in conjunction with the -c switch, the -q switch takes precedence.</span></span> <span data-ttu-id="61afd-148">Si le rc_config fichier fourni avec le commutateur-q contient une somme de contrôle MUIRCT ignore le commutateur-c et insère la valeur de somme de contrôle à partir de la valeur, rc_config fichier dans les fichiers LN et. mui.</span><span class="sxs-lookup"><span data-stu-id="61afd-148">If the rc_config file supplied with the -q switch contains a checksum MUIRCT ignores the -c switch and inserts the checksum value from the value, rc_config file into the LN and.mui files.</span></span> <span data-ttu-id="61afd-149">Si aucune valeur de somme de contrôle n’est trouvée dans le rc_config, MUIRCT calcule la somme de contrôle de ressource en fonction du comportement du commutateur-c.</span><span class="sxs-lookup"><span data-stu-id="61afd-149">If no checksum value is found in the rc_config, MUIRCT calculates the resource checksum based on the behavior of the -c switch.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="61afd-150">-v</span><span class="sxs-lookup"><span data-stu-id="61afd-150">-v</span></span></td>
<td><span data-ttu-id="61afd-151">Spécifie le niveau de verboseness pour la journalisation.</span><span class="sxs-lookup"><span data-stu-id="61afd-151">Specifies the level of verboseness for logging.</span></span> <span data-ttu-id="61afd-152">Spécifiez 1 pour imprimer tous les messages d’erreur et les résultats de l’opération de base.</span><span class="sxs-lookup"><span data-stu-id="61afd-152">Specify 1 to print all basic error messages and operation results.</span></span> <span data-ttu-id="61afd-153">Spécifiez 2 pour inclure également les informations de ressource (type, nom, identificateur de langue) incluses dans le fichier. mui et le fichier LN.</span><span class="sxs-lookup"><span data-stu-id="61afd-153">Specify 2 to also include the resource information (type, name, language identifier) included in the .mui file and LN file.</span></span> <span data-ttu-id="61afd-154">La valeur par défaut est-v 1</span><span class="sxs-lookup"><span data-stu-id="61afd-154">The default is -v 1</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="61afd-155">-X</span><span class="sxs-lookup"><span data-stu-id="61afd-155">-x</span></span></td>
<td><span data-ttu-id="61afd-156">Spécifie l’ID de langue avec lequel MUIRCT marque tous les types de ressources ajoutés à la section de la ressource du fichier. mui.</span><span class="sxs-lookup"><span data-stu-id="61afd-156">Specifies the language ID with which MUIRCT marks all resource types added to the resource section of the .mui file.</span></span> <span data-ttu-id="61afd-157">La valeur LangID peut être spécifiée au format décimal ou hexadécimal.</span><span class="sxs-lookup"><span data-stu-id="61afd-157">The LangID value can be specified in decimal or hexadecimal format.</span></span> <span data-ttu-id="61afd-158">Par exemple, l’anglais (États-Unis) peut être spécifié par-x 0x40C ou-x 1033.</span><span class="sxs-lookup"><span data-stu-id="61afd-158">For example English (United States) can be specified by -x 0x409 or -x 1033.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="61afd-159">-E</span><span class="sxs-lookup"><span data-stu-id="61afd-159">-e</span></span></td>
<td><span data-ttu-id="61afd-160">Extrait la somme de contrôle de la ressource contenue dans le checksum_file fourni avec le commutateur-c et l’insère dans le output_file spécifié.</span><span class="sxs-lookup"><span data-stu-id="61afd-160">Extracts the resource checksum contained in the checksum_file provided with the -c switch and inserts it in the specified output_file.</span></span> <span data-ttu-id="61afd-161">Quand-e est spécifié, MUIRCT ignore tous les commutateurs autres que le commutateur-c.</span><span class="sxs-lookup"><span data-stu-id="61afd-161">When -e is specified, MUIRCT ignores all switches other than the -c switch.</span></span> <span data-ttu-id="61afd-162">Dans ce cas, le checksum_file doit être un fichier binaire Win32 qui contient une section de données de configuration de ressource avec une valeur de somme de contrôle.</span><span class="sxs-lookup"><span data-stu-id="61afd-162">In this case the checksum_file must be a Win32 binary file that contains a resource configuration data section with a checksum value.</span></span> <span data-ttu-id="61afd-163">Le output_file doit être un fichier LN ou. mui existant.</span><span class="sxs-lookup"><span data-stu-id="61afd-163">The output_file must be an existing LN file or .mui file.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="61afd-164">-Z</span><span class="sxs-lookup"><span data-stu-id="61afd-164">-z</span></span></td>
<td><span data-ttu-id="61afd-165">Calcule et insère les données de somme de contrôle de ressource dans le fichier de sortie spécifié.</span><span class="sxs-lookup"><span data-stu-id="61afd-165">Calculates and inserts resource checksum data in the specified output file.</span></span> <span data-ttu-id="61afd-166">MUIRCT base le calcul de la somme de contrôle sur l’entrée fournie avec le commutateur-c et le commutateur facultatif-b.</span><span class="sxs-lookup"><span data-stu-id="61afd-166">MUIRCT bases checksum calculation on the input provided with the -c switch, and the optional -b switch.</span></span> <span data-ttu-id="61afd-167">Si vous spécifiez un fichier de sortie pour le commutateur-z qui n’existe pas, MUIRCT se termine avec un échec.</span><span class="sxs-lookup"><span data-stu-id="61afd-167">If you specify an output file for the -z switch that does not exist, MUIRCT exits with a failure.</span></span><br/> <span data-ttu-id="61afd-168">Exemple : calcule la somme de contrôle en fonction des ressources localisables dans Notepad.exe et insère la somme de contrôle dans le fichier de sortie Notepad2.exe.</span><span class="sxs-lookup"><span data-stu-id="61afd-168">Example: Calculates the checksum based on localizable resources in Notepad.exe and inserts the checksum into the output file Notepad2.exe.</span></span><br/> <code>muirct -c notepad.exe -q myprog.rcconfig -z notepad2.exe</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="61afd-169">-f</span><span class="sxs-lookup"><span data-stu-id="61afd-169">-f</span></span></td>
<td><span data-ttu-id="61afd-170">Permet de créer un fichier. mui dont la ressource de version est la seule ressource localisable.</span><span class="sxs-lookup"><span data-stu-id="61afd-170">Enables creating a .mui file with the version resource being the only localizable resource.</span></span> <span data-ttu-id="61afd-171">Par défaut, MUIRCT ne l’autorise pas.</span><span class="sxs-lookup"><span data-stu-id="61afd-171">By default, MUIRCT does not allow this.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="61afd-172">-d</span><span class="sxs-lookup"><span data-stu-id="61afd-172">-d</span></span></td>
<td><span data-ttu-id="61afd-173">Localise et affiche les données de configuration de ressources incorporées dans le fichier source.</span><span class="sxs-lookup"><span data-stu-id="61afd-173">Locates and displays embedded resource configuration data in the source file.</span></span> <span data-ttu-id="61afd-174">Lorsque vous spécifiez ce commutateur, MUIRCT ignore toutes les autres options de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="61afd-174">When you specify this switch, MUIRCT ignores all other command line options.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="61afd-175">-M</span><span class="sxs-lookup"><span data-stu-id="61afd-175">-m</span></span></td>
<td><span data-ttu-id="61afd-176">Spécifie le numéro de version à utiliser lors du calcul de la somme de contrôle pour associer les output_LN_file et les output_MUI_file.</span><span class="sxs-lookup"><span data-stu-id="61afd-176">Specifies the version number to use when calculating the checksum for associating the output_LN_file and output_MUI_file.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="61afd-177">source_filename</span><span class="sxs-lookup"><span data-stu-id="61afd-177">source_filename</span></span></td>
<td><span data-ttu-id="61afd-178">Nom du fichier source binaire localisé ; les caractères génériques ne peuvent pas être utilisés.</span><span class="sxs-lookup"><span data-stu-id="61afd-178">Name of the localized binary source file; wildcards cannot be used.</span></span> <span data-ttu-id="61afd-179">Ce fichier ne peut contenir que des ressources dans une seule langue.</span><span class="sxs-lookup"><span data-stu-id="61afd-179">This file can only contain resources in one language.</span></span> <span data-ttu-id="61afd-180">Si le fichier contient des ressources dans plusieurs langues, MUIRCT échoue, sauf si le commutateur-b est utilisé.</span><span class="sxs-lookup"><span data-stu-id="61afd-180">If there are resources in multiple languages in the file, MUIRCT fails, unless the -b switch is used.</span></span> <span data-ttu-id="61afd-181">Si le fichier contient des ressources avec des identificateurs de langue ayant uniquement la valeur 0, MUIRCT ne fractionne pas le fichier, car un identificateur de langue de 0 indique une langue neutre.</span><span class="sxs-lookup"><span data-stu-id="61afd-181">If the file contains resources with language identifiers having value 0 only, MUIRCT does not split the file because a language identifier of 0 indicates a neutral language.</span></span><br/> <span data-ttu-id="61afd-182">Pour le commutateur-d, source_filename est soit un fichier LN, soit un fichier de ressources spécifique à une langue pour lequel MUIRCT doit afficher les données de configuration de ressource.</span><span class="sxs-lookup"><span data-stu-id="61afd-182">For the -d switch, source_filename is either an LN file or a language-specific resource file for which MUIRCT is to display resource configuration data.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="61afd-183">language_neutral_filename</span><span class="sxs-lookup"><span data-stu-id="61afd-183">language_neutral_filename</span></span></td>
<td><span data-ttu-id="61afd-184">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="61afd-184">Optional.</span></span> <span data-ttu-id="61afd-185">Nom du fichier LN.</span><span class="sxs-lookup"><span data-stu-id="61afd-185">Name of LN file.</span></span> <span data-ttu-id="61afd-186">Si vous ne spécifiez pas le nom de ce fichier, MUIRCT ajoute une seconde extension &quot; . ln &quot; au nom du fichier source à utiliser comme nom de fichier indépendant de la langue.</span><span class="sxs-lookup"><span data-stu-id="61afd-186">If you do not specify the name of this file, MUIRCT appends a second extension &quot;.ln&quot; to the source file name to use as the language-neutral file name.</span></span> <span data-ttu-id="61afd-187">En général, vous devez supprimer l' &quot; extension. ln &quot; avant de déployer le fichier.</span><span class="sxs-lookup"><span data-stu-id="61afd-187">Typically you should remove the &quot;.ln&quot; extension before deploying the file.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="61afd-188">Le fichier LN ne doit pas contenir de chaînes ou de menus.</span><span class="sxs-lookup"><span data-stu-id="61afd-188">The LN file should not contain strings or menus.</span></span> <span data-ttu-id="61afd-189">Vous devez les supprimer manuellement.</span><span class="sxs-lookup"><span data-stu-id="61afd-189">You should remove them manually.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="61afd-190">mui_filename</span><span class="sxs-lookup"><span data-stu-id="61afd-190">mui_filename</span></span></td>
<td><span data-ttu-id="61afd-191">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="61afd-191">Optional.</span></span> <span data-ttu-id="61afd-192">Nom du fichier de ressources spécifique à la langue.</span><span class="sxs-lookup"><span data-stu-id="61afd-192">Name of language-specific resource file.</span></span> <span data-ttu-id="61afd-193">Si vous ne spécifiez pas de nom, MUIRCT ajoute un second extension &quot; . mui &quot; au nom du fichier source à utiliser comme nom de fichier. Normalement, MUIRCT crée un fichier de ressources spécifique à une langue.</span><span class="sxs-lookup"><span data-stu-id="61afd-193">If you do not specify a name, MUIRCT appends a second extension &quot;.mui&quot; to the source file name to use as the file name.Normally, MUIRCT creates a language-specific resource file.</span></span> <span data-ttu-id="61afd-194">Toutefois, il ne crée pas de fichier de ressources si l’une des conditions suivantes est remplie :</span><span class="sxs-lookup"><span data-stu-id="61afd-194">However, it does not create a resource file if any of the following conditions exist:</span></span><br/>
<ul>
<li><span data-ttu-id="61afd-195">Aucune ressource localisable n’est dans le fichier binaire d’origine.</span><span class="sxs-lookup"><span data-stu-id="61afd-195">No localizable resources are in the original binary file.</span></span></li>
<li><span data-ttu-id="61afd-196">Le seul langage des ressources trouvé dans le fichier binaire d’origine est le langage neutre.</span><span class="sxs-lookup"><span data-stu-id="61afd-196">The only resource language found in the original binary file is the neutral language.</span></span></li>
<li><span data-ttu-id="61afd-197">Le fichier binaire d’origine contient des ressources pour plusieurs langues, sans compter la langue neutre.</span><span class="sxs-lookup"><span data-stu-id="61afd-197">The original binary file has resources for more than one language, not counting the neutral language.</span></span> <span data-ttu-id="61afd-198">Si le fichier binaire contient des ressources pour deux langues et que l’une d’entre elles est la langue neutre, l’utilitaire considère que le fichier est monolingue et crée un fichier de ressources spécifique à la langue s’il existe des ressources localisables.</span><span class="sxs-lookup"><span data-stu-id="61afd-198">If the binary file contains resources for two languages, and one of them is the neutral language, the utility considers the file to be monolingual and creates a language-specific resource file if there are localizable resources.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="muirct-language-output"></a><span data-ttu-id="61afd-199">Sortie du langage MUIRCT</span><span class="sxs-lookup"><span data-stu-id="61afd-199">MUIRCT Language Output</span></span>

<span data-ttu-id="61afd-200">MUIRCT choisit la valeur de l’attribut « UltimateFallbackLanguage » à insérer dans les données de configuration de ressource du fichier LN en fonction de l’ordre suivant, de la priorité la plus élevée à la plus faible :</span><span class="sxs-lookup"><span data-stu-id="61afd-200">MUIRCT chooses the "UltimateFallbackLanguage" attribute value to insert in the LN file resource configuration data based on the following order, from highest priority to lowest:</span></span>

1.  <span data-ttu-id="61afd-201">Attribut « UltimateFallbackLanguage » dans le fichier de configuration de ressource source, s’il est passé en tant qu’entrée.</span><span class="sxs-lookup"><span data-stu-id="61afd-201">"UltimateFallbackLanguage" attribute in the source resource configuration file, if one is passed in as input.</span></span>
2.  <span data-ttu-id="61afd-202">Langue spécifiée avec le commutateur-g.</span><span class="sxs-lookup"><span data-stu-id="61afd-202">The language specified with the -g switch.</span></span>
3.  <span data-ttu-id="61afd-203">Langue du fichier d’entrée.</span><span class="sxs-lookup"><span data-stu-id="61afd-203">Input file language.</span></span>

<span data-ttu-id="61afd-204">MUIRCT choisit la valeur de l’attribut « Language » à insérer dans les données de configuration de ressource de fichier. mui selon l’ordre suivant :</span><span class="sxs-lookup"><span data-stu-id="61afd-204">MUIRCT picks the "language" attribute value to insert in the .mui file resource configuration data based on the following order:</span></span>

1.  <span data-ttu-id="61afd-205">attribut « Language » dans le fichier de configuration de ressource source, s’il est passé en tant qu’entrée.</span><span class="sxs-lookup"><span data-stu-id="61afd-205">"language" attribute in the source resource configuration file, if one is passed in as input.</span></span>
2.  <span data-ttu-id="61afd-206">Langue spécifiée par le commutateur-x (forcer la langue).</span><span class="sxs-lookup"><span data-stu-id="61afd-206">The language specified by the -x switch (force language).</span></span>
3.  <span data-ttu-id="61afd-207">Langue du fichier d’entrée.</span><span class="sxs-lookup"><span data-stu-id="61afd-207">Input file language.</span></span>

### <a name="muirct-checksum-handling"></a><span data-ttu-id="61afd-208">Gestion de la somme de contrôle MUIRCT</span><span class="sxs-lookup"><span data-stu-id="61afd-208">MUIRCT Checksum Handling</span></span>

<span data-ttu-id="61afd-209">Le système d’exploitation calcule normalement la somme de contrôle sur les ressources spécifiques à une langue dans un fichier, sauf si vous spécifiez la somme de contrôle via un fichier de configuration de ressource.</span><span class="sxs-lookup"><span data-stu-id="61afd-209">The operating system normally calculates the checksum over the language-specific resources in a file unless you specify the checksum through a resource configuration file.</span></span> <span data-ttu-id="61afd-210">Tant que la somme de contrôle est la même pour le fichier LN et tous les fichiers de ressources spécifiques à la langue associés, et que l’attribut Language dans la configuration de ressource dans le LN et le Language dépendent, le chargeur de ressources peut charger des ressources avec succès.</span><span class="sxs-lookup"><span data-stu-id="61afd-210">As long as the checksum is the same for the LN file and all associated language-specific resource files, and the language attribute in the resource configuration in the LN and language dependent match, the resource loader can successfully load resources.</span></span>

<span data-ttu-id="61afd-211">MUIRCT prend en charge plusieurs méthodes pour placer les sommes de contrôle appropriées dans les données de configuration de ressource :</span><span class="sxs-lookup"><span data-stu-id="61afd-211">MUIRCT supports several methods for placing appropriate checksums in the resource configuration data:</span></span>

1.  <span data-ttu-id="61afd-212">Générez un exécutable pour chaque langage, contenant à la fois le code et les ressources.</span><span class="sxs-lookup"><span data-stu-id="61afd-212">Build an executable for each language, containing both code and resources.</span></span> <span data-ttu-id="61afd-213">Après cela, utilisez MUIRCT pour fractionner chacun de ces fichiers en un fichier LN et un fichier de ressources spécifique à une langue.</span><span class="sxs-lookup"><span data-stu-id="61afd-213">After this, use MUIRCT to split each of these files into an LN file and a language-specific resource file.</span></span> <span data-ttu-id="61afd-214">MUIRCT s’exécute plusieurs fois, une fois pour générer un fichier de ressources pour chaque langue.</span><span class="sxs-lookup"><span data-stu-id="61afd-214">MUIRCT runs multiple times, once to generate a resource file for each language.</span></span> <span data-ttu-id="61afd-215">Vous pouvez effectuer la génération des manières suivantes :</span><span class="sxs-lookup"><span data-stu-id="61afd-215">You can perform the build in the following ways:</span></span>
    1.  <span data-ttu-id="61afd-216">Utilisez le commutateur-q pour spécifier une valeur de somme de contrôle dans le fichier de configuration de ressource.</span><span class="sxs-lookup"><span data-stu-id="61afd-216">Use the -q switch to specify a checksum value in the resource configuration file.</span></span> <span data-ttu-id="61afd-217">MUIRCT place cette valeur dans tous les fichiers LN et les fichiers de ressources spécifiques à la langue produits.</span><span class="sxs-lookup"><span data-stu-id="61afd-217">MUIRCT places this value in all the LN files and language-specific resource files produced.</span></span> <span data-ttu-id="61afd-218">Vous devez adopter une stratégie pour choisir cette valeur, comme décrit plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="61afd-218">You need to adopt a strategy for choosing this value, as described later in this topic.</span></span>
    2.  <span data-ttu-id="61afd-219">Utilisez le commutateur-c (et, éventuellement, le commutateur-b) pour choisir une seule langue dont les ressources dont MUIRCT extrait la somme de contrôle.</span><span class="sxs-lookup"><span data-stu-id="61afd-219">Use the -c switch (and, optionally, the -b switch) to choose a single language having resources from which MUIRCT extracts the checksum.</span></span>
    3.  <span data-ttu-id="61afd-220">Utilisez le commutateur-z pour choisir une seule langue dont les ressources sont à partir desquelles MUIRCT extrait toujours la somme de contrôle.</span><span class="sxs-lookup"><span data-stu-id="61afd-220">Use the -z switch to choose a single language having resources from which MUIRCT always extracts the checksum.</span></span> <span data-ttu-id="61afd-221">Appliquez cette somme de contrôle une fois que les fichiers ont été générés à l’aide d’autres méthodes.</span><span class="sxs-lookup"><span data-stu-id="61afd-221">Apply this checksum after the files have been built using other methods.</span></span>
2.  <span data-ttu-id="61afd-222">Créez un exécutable contenant à la fois le code et les ressources pour une seule langue.</span><span class="sxs-lookup"><span data-stu-id="61afd-222">Build an executable containing both code and resources for a single language.</span></span> <span data-ttu-id="61afd-223">Ensuite, utilisez MUIRCT pour fractionner les ressources entre le fichier LN et le fichier de ressources spécifique à la langue.</span><span class="sxs-lookup"><span data-stu-id="61afd-223">After this, use MUIRCT to split the resources between the LN file and the language-specific resource file.</span></span> <span data-ttu-id="61afd-224">Enfin, utilisez un outil de localisation binaire pour modifier le fichier de ressources résultant pour chaque langue.</span><span class="sxs-lookup"><span data-stu-id="61afd-224">Finally, use a binary localization tool to modify the resulting resource file for each language.</span></span>

<span data-ttu-id="61afd-225">La Convention la plus courante pour gérer les sommes de contrôle consiste à baser la somme de contrôle sur les ressources anglaises (États-Unis).</span><span class="sxs-lookup"><span data-stu-id="61afd-225">The most common convention for checksum handling is to base the checksum on the English (United States) resources.</span></span> <span data-ttu-id="61afd-226">Vous êtes libre d’adopter une convention différente, à condition qu’elle soit cohérente pour chaque fichier LN.</span><span class="sxs-lookup"><span data-stu-id="61afd-226">You are free to adopt a different convention, as long as it is consistent for each LN file.</span></span> <span data-ttu-id="61afd-227">Par exemple, il est parfaitement acceptable pour une entreprise de développement de logiciels de baser ses sommes de contrôle dans le logiciel qu’elle construit sur des ressources françaises (France) à la place des ressources anglais (États-Unis), à condition que toutes les applications aient des ressources françaises (France) sur lesquelles baser les sommes de contrôle.</span><span class="sxs-lookup"><span data-stu-id="61afd-227">For example, it is perfectly acceptable for a software development enterprise to base its checksums in the software it builds on French (France) resources instead of English (United States) resources, as long as all the applications have French (France) resources on which to base the checksums.</span></span> <span data-ttu-id="61afd-228">Il est également possible d’utiliser le fichier de configuration de ressources pour assigner une valeur hexadécimale arbitraire pouvant atteindre 16 chiffres hexadécimaux en tant que somme de contrôle.</span><span class="sxs-lookup"><span data-stu-id="61afd-228">It is also acceptable to use the resource configuration file to assign an arbitrary hexadecimal value of up to 16 hexadecimal digits as a checksum.</span></span> <span data-ttu-id="61afd-229">Cette dernière stratégie exclut l’utilisation effective des commutateurs-z,-c et-b de MUIRCT.</span><span class="sxs-lookup"><span data-stu-id="61afd-229">This last strategy precludes the effective use of the -z, -c, and -b switches of MUIRCT.</span></span> <span data-ttu-id="61afd-230">Elle nécessite l’adoption d’une méthode à l’aide de [**Guidgen**](/previous-versions/windows/embedded/ms924300(v=msdn.10)) ou d’un autre outil pour générer des valeurs de somme de contrôle.</span><span class="sxs-lookup"><span data-stu-id="61afd-230">It requires adoption of a method using either [**GuidGen**](/previous-versions/windows/embedded/ms924300(v=msdn.10)) or some other tool to generate checksum values.</span></span> <span data-ttu-id="61afd-231">Cette stratégie vous oblige également à configurer une stratégie pour déterminer quand modifier la valeur lors de l’ajout de nouvelles ressources localisables.</span><span class="sxs-lookup"><span data-stu-id="61afd-231">This strategy also requires you to set up a policy for determining when to modify the value when adding new localizable resources.</span></span>

<span data-ttu-id="61afd-232">Pour appliquer la somme de contrôle anglais (États-Unis) à tous les fichiers, vous pouvez utiliser l’une des méthodes de gestion de la somme de contrôle décrites ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="61afd-232">To apply the English (United States) checksum to all files, you can use any of the checksum handling methods described above.</span></span> <span data-ttu-id="61afd-233">Par exemple, vous pouvez générer le fichier de LN et le fichier de ressources spécifique à la langue pour l’anglais (États-Unis), puis utiliser le commutateur MUIRCT-d pour obtenir la somme de contrôle résultante.</span><span class="sxs-lookup"><span data-stu-id="61afd-233">For example, you can generate the LN file and language-specific resource file for English (United States), then use the MUIRCT -d switch to obtain the resulting checksum.</span></span> <span data-ttu-id="61afd-234">Vous pouvez copier cette somme de contrôle dans votre fichier de configuration de ressources et utiliser le commutateur-q avec MUIRCT pour appliquer la somme de contrôle à tous les autres fichiers.</span><span class="sxs-lookup"><span data-stu-id="61afd-234">You can copy this checksum into your resource configuration file and use the -q switch with MUIRCT to apply the checksum to all other files.</span></span>

### <a name="use-of-a-resource-configuration-file-with-muirct"></a><span data-ttu-id="61afd-235">Utilisation d’un fichier de configuration de ressource avec MUIRCT</span><span class="sxs-lookup"><span data-stu-id="61afd-235">Use of a Resource Configuration File with MUIRCT</span></span>

<span data-ttu-id="61afd-236">Vous pouvez spécifier des données de configuration de ressources lors de l’utilisation de MUIRCT.</span><span class="sxs-lookup"><span data-stu-id="61afd-236">You can specify resource configuration data when using MUIRCT.</span></span> <span data-ttu-id="61afd-237">Que vous fournissiez ou non explicitement un fichier de configuration de ressource, chaque fichier de ressources spécifique à une langue contient des données de configuration de ressource, comme tout fichier LN avec un fichier de ressources associé.</span><span class="sxs-lookup"><span data-stu-id="61afd-237">Whether or not you explicitly supply a resource configuration file, every language-specific resource file has resource configuration data, as does any LN file with an associated resource file.</span></span> <span data-ttu-id="61afd-238">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="61afd-238">For example:</span></span>

-   <span data-ttu-id="61afd-239">Si vous utilisez le commutateur-q pour spécifier un fichier de configuration de ressource, mais qu’il n’existe pas de ressources localisables dans votre fichier source d’entrée, aucun fichier de ressources spécifique à la langue n’est généré et le fichier LN résultant ne contient pas de données de configuration de ressource.</span><span class="sxs-lookup"><span data-stu-id="61afd-239">If you use the -q switch to specify a resource configuration file, but there are no localizable resources in your input source file, no language-specific resource file is generated and the resulting LN file does not contain resource configuration data.</span></span> <span data-ttu-id="61afd-240">En outre, si le fichier source d’entrée contient des ressources multilingues, MUIRCT ne fractionne pas le fichier.</span><span class="sxs-lookup"><span data-stu-id="61afd-240">Also, if the input source file has multilingual resources, then MUIRCT won't split the file.</span></span>

> [!Note]  
> <span data-ttu-id="61afd-241">Actuellement, le comportement de MUIRCT est incohérent lorsque l’élément neutralResources du fichier de configuration de ressource ne contient pas d’éléments resourceType et que l’élément localizedResources contient des chaînes et des menus, par exemple.</span><span class="sxs-lookup"><span data-stu-id="61afd-241">Currently the behavior of MUIRCT is inconsistent when the neutralResources element of the resource configuration file contains no resourceType elements and the localizedResources element contains strings and menus, for example.</span></span> <span data-ttu-id="61afd-242">Dans ce cas, MUIRCT fractionne les ressources comme suit :</span><span class="sxs-lookup"><span data-stu-id="61afd-242">In such a case, MUIRCT splits the resources as follows:</span></span>
>
> -   <span data-ttu-id="61afd-243">Toutes les ressources du fichier binaire d’origine (y compris les chaînes et les menus), ainsi que les ressources MUI, sont placées dans le fichier LN.</span><span class="sxs-lookup"><span data-stu-id="61afd-243">All resources in the original binary (including strings and menus), plus the MUI resources, are placed in the LN file.</span></span>
> -   <span data-ttu-id="61afd-244">Les chaînes, les menus et les ressources MUI sont placés dans le fichier de ressources propre à la langue approprié.</span><span class="sxs-lookup"><span data-stu-id="61afd-244">Strings, menus, and MUI resources are placed in the appropriate language-specific resource file.</span></span>

 

### <a name="examples-for-using-muirct"></a><span data-ttu-id="61afd-245">Exemples d’utilisation de MUIRCT</span><span class="sxs-lookup"><span data-stu-id="61afd-245">Examples for Using MUIRCT</span></span>

<span data-ttu-id="61afd-246">**Exemples d’utilisation standard**</span><span class="sxs-lookup"><span data-stu-id="61afd-246">**Examples of Standard Usage**</span></span>


```C++
muirct -q mui.MMF bar.exe barnew.exe barnew.exe.mui

muirct -d myprog.exe.mui
```



<span data-ttu-id="61afd-247">**Exemple de sortie de fichier LN en utilisant le commutateur-d**</span><span class="sxs-lookup"><span data-stu-id="61afd-247">**Example of LN File Output Using -d Switch**</span></span>

<span data-ttu-id="61afd-248">Voici un exemple de la sortie de données de configuration de ressource d’un fichier LN, Shell32.dll, à l’aide du commutateur-d avec MUIRCT :</span><span class="sxs-lookup"><span data-stu-id="61afd-248">Here is an example of the resource configuration data output from an LN file, Shell32.dll, using the -d switch with MUIRCT:</span></span>


```C++
Signature          -    fecdfecd
Length             -    148
RC Config Version  -    10000
FileType           -    11
SystemAttributes   -    100
UltimateFallback location    -  external
Service Checksum   -    14f44a8d86bef14af26d9a885964c935
Checksum           -    f5b3b7ab330439d6fcc07582c3afb613
MainNameTypes      -    AVI FTR ORDERSTREAM TYPELIB UIFILE XML MUI
MainIDTypes        -    1 2 3 12 14 16 24
MuiNameTypes       -    MUI
MuiIDTypes         -    2 3 4 5 6 9 14 16
UltimateFallbackLanguage   -   en-US
```



<span data-ttu-id="61afd-249">**Exemple de Language-Specific sortie de fichier de ressources à l’aide du commutateur-d**</span><span class="sxs-lookup"><span data-stu-id="61afd-249">**Example of Language-Specific Resource File Output Using -d Switch**</span></span>

<span data-ttu-id="61afd-250">Voici un exemple de la sortie de données de configuration de ressources à partir d’un fichier. mui, Shell32.dll. mui, à l’aide du commutateur-d pour MUIRCT :</span><span class="sxs-lookup"><span data-stu-id="61afd-250">Here is an example of the resource configuration data output from a .mui file, Shell32.dll.mui, using the -d switch for MUIRCT:</span></span>


```C++
Signature          -    fecdfecd
Length             -     c8
RC Config Version  -    10000
FileType           -    12
SystemAttributes   -    100
Service Checksum   -    14f44a8d86bef14af26d9a885964c935
Checksum           -    f5b3b7ab330439d6fcc07582c3afb613
MainNameTypes      -    MUI
MainIDTypes        -    2 3 4 5 6 9 14 16
Language           -    en-US
```



## <a name="rc-compiler-utility"></a><span data-ttu-id="61afd-251">Utilitaire de compilation RC</span><span class="sxs-lookup"><span data-stu-id="61afd-251">RC Compiler Utility</span></span>

<span data-ttu-id="61afd-252">Le compilateur RC (Rc.exe) est un utilitaire de ligne de commande permettant de compiler un fichier de script de définition de ressource (extension. RC) dans des fichiers de ressources (extension. res).</span><span class="sxs-lookup"><span data-stu-id="61afd-252">RC Compiler (Rc.exe) is a command line utility for compiling a resource definition script file (.rc extension) into resource files (.res extension).</span></span> <span data-ttu-id="61afd-253">Le compilateur RC est inclus dans le SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="61afd-253">RC Compiler is included in the Windows SDK.</span></span> <span data-ttu-id="61afd-254">Ce document explique uniquement comment utiliser le compilateur RC avec les fonctionnalités MUI du chargeur de ressources.</span><span class="sxs-lookup"><span data-stu-id="61afd-254">This document only explains the use of RC Compiler with MUI-related capabilities of the resource loader.</span></span> <span data-ttu-id="61afd-255">Pour obtenir des informations complètes sur le compilateur, consultez [à propos des fichiers de ressources](../menurc/about-resource-files.md).</span><span class="sxs-lookup"><span data-stu-id="61afd-255">For complete information about the compiler, see [About Resource Files](../menurc/about-resource-files.md).</span></span>

<span data-ttu-id="61afd-256">Le compilateur RC vous permet de générer, à partir d’un seul ensemble de sources, un fichier LN et un fichier de ressources propre au langage.</span><span class="sxs-lookup"><span data-stu-id="61afd-256">RC Compiler allows you to build, from a single set of sources, an LN file and a separate language-specific resource file.</span></span> <span data-ttu-id="61afd-257">Comme pour MUIRCT, les fichiers sont associés à des données de configuration de ressource.</span><span class="sxs-lookup"><span data-stu-id="61afd-257">As for MUIRCT, the files are associated by resource configuration data.</span></span>

### <a name="rc-compiler-syntax-as-used-for-mui-resources"></a><span data-ttu-id="61afd-258">Syntaxe du compilateur RC utilisée pour les ressources MUI</span><span class="sxs-lookup"><span data-stu-id="61afd-258">RC Compiler Syntax as Used for MUI Resources</span></span>

<span data-ttu-id="61afd-259">Les commutateurs du compilateur RC sont définis en détail dans [utilisation de RC](../menurc/using-rc-the-rc-command-line-.md).</span><span class="sxs-lookup"><span data-stu-id="61afd-259">RC Compiler switches are defined in detail in [Using RC](../menurc/using-rc-the-rc-command-line-.md).</span></span> <span data-ttu-id="61afd-260">Cette section définit uniquement les commutateurs utilisés pour créer des ressources MUI.</span><span class="sxs-lookup"><span data-stu-id="61afd-260">This section only defines the switches used to build MUI resources.</span></span> <span data-ttu-id="61afd-261">N’oubliez pas que chaque commutateur ne respecte pas la casse.</span><span class="sxs-lookup"><span data-stu-id="61afd-261">Remember that each switch is case-insensitive.</span></span> <span data-ttu-id="61afd-262">Les types de ressources sont supposés être indépendants du langage, sauf indication contraire.</span><span class="sxs-lookup"><span data-stu-id="61afd-262">Resource types are assumed to be language-neutral unless otherwise indicated.</span></span>


```C++
rc [-h|-?] -fm mui_res_name [-q rc_config_file_name] [-g langid] [-g1 ] [-g2 version]
```



<span data-ttu-id="61afd-263">**Commutateurs et arguments**</span><span class="sxs-lookup"><span data-stu-id="61afd-263">**Switches and Arguments**</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="61afd-264">-h |- ?</span><span class="sxs-lookup"><span data-stu-id="61afd-264">-h|-?</span></span></td>
<td><span data-ttu-id="61afd-265">Affiche l’écran d’aide.</span><span class="sxs-lookup"><span data-stu-id="61afd-265">Shows help screen.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="61afd-266">-FM</span><span class="sxs-lookup"><span data-stu-id="61afd-266">-fm</span></span></td>
<td><span data-ttu-id="61afd-267">Utilise le fichier de ressources spécifié pour les ressources spécifiques à une langue.</span><span class="sxs-lookup"><span data-stu-id="61afd-267">Uses the specified resource file for language-specific resources.</span></span> <span data-ttu-id="61afd-268">Normalement, le compilateur de ressources crée un fichier de ressources spécifique à une langue.</span><span class="sxs-lookup"><span data-stu-id="61afd-268">Normally the resource compiler creates a language-specific resource file.</span></span> <span data-ttu-id="61afd-269">Toutefois, il ne crée pas le fichier si l’une des conditions suivantes est remplie :</span><span class="sxs-lookup"><span data-stu-id="61afd-269">However, it does not create the file if any of the following conditions exist:</span></span><br/>
<ul>
<li><span data-ttu-id="61afd-270">Il n’existe pas de ressources localisables dans le fichier. rc.</span><span class="sxs-lookup"><span data-stu-id="61afd-270">There are no localizable resources in the .rc file.</span></span></li>
<li><span data-ttu-id="61afd-271">Le seul langage des ressources trouvé dans le fichier. RC est le langage neutre.</span><span class="sxs-lookup"><span data-stu-id="61afd-271">The only resource language found in the .rc file is the neutral language.</span></span></li>
<li><span data-ttu-id="61afd-272">Le fichier. rc contient des ressources pour plusieurs langues, sans compter la langue neutre.</span><span class="sxs-lookup"><span data-stu-id="61afd-272">The .rc file has resources for more than one language, not counting the neutral language.</span></span> <span data-ttu-id="61afd-273">Si le fichier. rc contient des ressources pour deux langues et que l’une d’entre elles est la langue neutre, le compilateur considère que le fichier est monolingue.</span><span class="sxs-lookup"><span data-stu-id="61afd-273">If the .rc file contains resources for two languages, and one of them is the neutral language, the compiler considers the file to be monolingual.</span></span> <span data-ttu-id="61afd-274">S’il existe des ressources localisables, le compilateur crée un fichier de ressources spécifique à la langue.</span><span class="sxs-lookup"><span data-stu-id="61afd-274">If there are any localizable resources, the compiler creates a language-specific resource file.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="61afd-275">-q</span><span class="sxs-lookup"><span data-stu-id="61afd-275">-q</span></span></td>
<td><span data-ttu-id="61afd-276">Utilise le fichier de configuration de ressource spécifié pour obtenir les types de ressources à placer dans le fichier de ressources spécifique à la langue et dans le fichier LN.</span><span class="sxs-lookup"><span data-stu-id="61afd-276">Uses the specified resource configuration file to obtain the resource types to place in the language-specific resource file and the LN file.</span></span> <span data-ttu-id="61afd-277">Pour plus d’informations, consultez <a href="preparing-a-resource-configuration-file.md">préparation d’un fichier de configuration de ressource</a>.</span><span class="sxs-lookup"><span data-stu-id="61afd-277">For more information, see <a href="preparing-a-resource-configuration-file.md">Preparing a Resource Configuration File</a>.</span></span> <span data-ttu-id="61afd-278">Comme alternative à ce commutateur, vous pouvez utiliser les commutateurs-j et-k, mais il est préférable d’utiliser un fichier de configuration de ressource.</span><span class="sxs-lookup"><span data-stu-id="61afd-278">As an alternative to this switch, you can use the -j and -k switches, but it is preferred to use a resource configuration file.</span></span> <br/> <span data-ttu-id="61afd-279">En utilisant le commutateur-q avec un fichier de configuration de ressource, vous pouvez implémenter un fractionnement basé sur les éléments et fournir des attributs qui finissent par la configuration des ressources binaires dans le fichier de ressources en LN et spécifiques à une langue.</span><span class="sxs-lookup"><span data-stu-id="61afd-279">By using the -q switch with a resource configuration file, you can implement an item-based split and provide attributes that will end up with the binary resource configuration in the LN and language-specific resource file.</span></span> <span data-ttu-id="61afd-280">Ce fractionnement n’est pas possible à l’aide des commutateurs-j et-k.</span><span class="sxs-lookup"><span data-stu-id="61afd-280">This split is not possible using the -j and -k switches.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="61afd-281">Le processus de fractionnement du compilateur RC ne fonctionne pas correctement si vous stockez des ressources et des informations de version dans des fichiers de configuration de ressources différents.</span><span class="sxs-lookup"><span data-stu-id="61afd-281">The RC Compiler split process does not work properly if you store resources and version information in different resource configuration files.</span></span> <span data-ttu-id="61afd-282">Dans ce cas, le compilateur RC ne fractionne pas les informations de version.</span><span class="sxs-lookup"><span data-stu-id="61afd-282">In this case, RC Compiler does not split the version information.</span></span> <span data-ttu-id="61afd-283">Par conséquent, une erreur de l’éditeur de liens se produit lors de la liaison du fichier de ressources spécifique à la langue, car le fichier n’a pas de ressources de version.</span><span class="sxs-lookup"><span data-stu-id="61afd-283">Therefore a linker error occurs during linking of the language-specific resource file because the file does not have version resources.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="61afd-284">-g</span><span class="sxs-lookup"><span data-stu-id="61afd-284">-g</span></span></td>
<td><span data-ttu-id="61afd-285">Spécifie l’identificateur de <a href="language-identifiers.md">langue de secours</a> ultime en notation hexadécimale.</span><span class="sxs-lookup"><span data-stu-id="61afd-285">Specifies the ultimate <a href="language-identifiers.md">fallback language</a> identifier in hexadecimal.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="61afd-286">-G1</span><span class="sxs-lookup"><span data-stu-id="61afd-286">-g1</span></span></td>
<td><span data-ttu-id="61afd-287">Crée un fichier MUI. res même si la ressource de VERSION est le seul contenu localisable.</span><span class="sxs-lookup"><span data-stu-id="61afd-287">Creates a MUI .res file even if the VERSION resource is the only localizable content.</span></span> <span data-ttu-id="61afd-288">Par défaut, le compilateur RC ne produit pas de fichier. res si la VERSION est la seule ressource localisable.</span><span class="sxs-lookup"><span data-stu-id="61afd-288">By default, RC Compiler does not produce a .res file if VERSION is the only localizable resource.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="61afd-289">-g2</span><span class="sxs-lookup"><span data-stu-id="61afd-289">-g2</span></span></td>
<td><span data-ttu-id="61afd-290">Spécifie le numéro de version personnalisé à utiliser lors du calcul de la somme de contrôle.</span><span class="sxs-lookup"><span data-stu-id="61afd-290">Specifies the custom version number to use when calculating the checksum.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="61afd-291">mui_res_name</span><span class="sxs-lookup"><span data-stu-id="61afd-291">mui_res_name</span></span></td>
<td><span data-ttu-id="61afd-292">Fichier de ressources pour les ressources spécifiques à une langue.</span><span class="sxs-lookup"><span data-stu-id="61afd-292">Resource file for language-specific resources.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="61afd-293">rc_config_file_name</span><span class="sxs-lookup"><span data-stu-id="61afd-293">rc_config_file_name</span></span></td>
<td><span data-ttu-id="61afd-294">Fichier de configuration de ressource.</span><span class="sxs-lookup"><span data-stu-id="61afd-294">Resource configuration file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="61afd-295">langid</span><span class="sxs-lookup"><span data-stu-id="61afd-295">langid</span></span></td>
<td><span data-ttu-id="61afd-296">Identificateur de langue.</span><span class="sxs-lookup"><span data-stu-id="61afd-296">Language identifier.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="61afd-297">version</span><span class="sxs-lookup"><span data-stu-id="61afd-297">version</span></span></td>
<td><span data-ttu-id="61afd-298">Numéro de version personnalisé, dans un format tel que &quot; 6.2.0.0 &quot; .</span><span class="sxs-lookup"><span data-stu-id="61afd-298">Custom version number, in a format such as &quot;6.2.0.0&quot;.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="example-for-using-rc-compiler-to-build-mui-resources"></a><span data-ttu-id="61afd-299">Exemple d’utilisation du compilateur RC pour générer des ressources MUI</span><span class="sxs-lookup"><span data-stu-id="61afd-299">Example for Using RC Compiler to Build MUI Resources</span></span>

<span data-ttu-id="61afd-300">Pour illustrer l’opération du compilateur RC avec les ressources MUI, examinons la ligne de commande suivante pour le fichier de ressources MyFile. RC :</span><span class="sxs-lookup"><span data-stu-id="61afd-300">To illustrate RC Compiler operation with MUI resources, let's examine the following command line, for the resource file Myfile.rc:</span></span>


```C++
rc -fm myfile_res.res -q myfile.rcconfig myfile.rc
```



<span data-ttu-id="61afd-301">Cette ligne de commande force le compilateur RC à effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="61afd-301">This command line causes RC Compiler to do the following:</span></span>

-   <span data-ttu-id="61afd-302">Créez le fichier de ressources propre à la langue MyFile \_ res. res et un fichier de ressources indépendant de la langue dont la valeur par défaut est MyFile. res, en fonction du nom du fichier. rc.</span><span class="sxs-lookup"><span data-stu-id="61afd-302">Create the language-specific resource file Myfile\_res.res and a language-neutral resource file that defaults to Myfile.res, based on the name of the .rc file.</span></span>
-   <span data-ttu-id="61afd-303">Ajoutez le 2 (élément 5 6 7 8 9 10 11 12), 4, 5, 6, 9, 11, 16, 23, 240, 1024 \_ types de ressources de type dans le fichier. res spécifique à la langue, s’ils se trouvent dans le fichier. rc.</span><span class="sxs-lookup"><span data-stu-id="61afd-303">Add the 2 (item 5 6 7 8 9 10 11 12), 4, 5, 6, 9, 11, 16, 23, 240, 1024 MY\_TYPE resource types to the language-specific .res file if they are in the .rc file.</span></span>
-   <span data-ttu-id="61afd-304">Ajoutez le type de ressource 16, ainsi que tous les autres types de ressources décrits dans le fichier de ressources au fichier. res indépendant de la langue et au fichier. res propre à la langue.</span><span class="sxs-lookup"><span data-stu-id="61afd-304">Add resource type 16, along with any other resource types described in the resource file to the language-neutral .res file and to the language-specific .res file.</span></span> <span data-ttu-id="61afd-305">Notez que, dans cet exemple, le type de ressource 16 est ajouté à deux emplacements.</span><span class="sxs-lookup"><span data-stu-id="61afd-305">Note that, in this example, resource type 16 is being added in two places.</span></span>
-   <span data-ttu-id="61afd-306">Choisissez la valeur de l’attribut « UltimateFallbackLanguage » pour insérer les données de configuration de ressource du fichier LN en fonction des critères suivants, classés de la plus haute à la plus faible :</span><span class="sxs-lookup"><span data-stu-id="61afd-306">Choose the "UltimateFallbackLanguage" attribute value to insert into the LN file resource configuration data based on the following criteria, ordered from highest priority to lowest:</span></span>
    -   <span data-ttu-id="61afd-307">Attribut « UltimateFallbackLanguage » dans le fichier de configuration de ressource, s’il est passé en tant qu’entrée.</span><span class="sxs-lookup"><span data-stu-id="61afd-307">"UltimateFallbackLanguage" attribute in the resource configuration file if one is passed in as input.</span></span>
    -   <span data-ttu-id="61afd-308">Valeur de l’attribut de langage à insérer dans les données de configuration de ressource en fonction de l’ordre de la langue du compilateur RC (langue indépendante de la langue et langue du fichier de ressources propre à la langue).</span><span class="sxs-lookup"><span data-stu-id="61afd-308">Language attribute value to insert in the resource configuration data based on the RC Compiler language order (language-neutral and language-specific resource file language).</span></span> <span data-ttu-id="61afd-309">Les considérations incluent le langage dans le fichier. RC, la valeur de langue du commutateur-GL et l’identificateur 0x0409 pour l’anglais (États-Unis).</span><span class="sxs-lookup"><span data-stu-id="61afd-309">Considerations include language in the .rc file, language value of the -gl switch, and identifier 0x0409 for English (United States).</span></span>

## <a name="remarks"></a><span data-ttu-id="61afd-310">Notes</span><span class="sxs-lookup"><span data-stu-id="61afd-310">Remarks</span></span>

<span data-ttu-id="61afd-311">Si vous incluez des types de ressources icône (3), boîte de dialogue (5), chaîne (6) ou VERSION (16) dans l’élément neutralResources, vous devez dupliquer cette entrée dans l’élément localizedResources dans le fichier de configuration de ressource.</span><span class="sxs-lookup"><span data-stu-id="61afd-311">If you include any ICON(3), DIALOG(5), STRING(6), or VERSION(16) resource type in the neutralResources element, then you have to duplicate that entry in the localizedResources element in the resource configuration file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="61afd-312">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="61afd-312">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61afd-313">Informations de référence sur l’interface utilisateur multilingue</span><span class="sxs-lookup"><span data-stu-id="61afd-313">Multilingual User Interface Reference</span></span>](multilingual-user-interface-reference.md)
</dt> <dt>

[<span data-ttu-id="61afd-314">Gestion des ressources MUI</span><span class="sxs-lookup"><span data-stu-id="61afd-314">MUI Resource Management</span></span>](mui-resource-management.md)
</dt> <dt>

[<span data-ttu-id="61afd-315">Localisation des ressources et génération de l’application</span><span class="sxs-lookup"><span data-stu-id="61afd-315">Localizing Resources and Building the Application</span></span>](localizing-resources-and-building-the-application.md)
</dt> </dl>

 

 
