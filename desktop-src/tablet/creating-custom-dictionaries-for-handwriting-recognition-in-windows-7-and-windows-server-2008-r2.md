---
description: Cette section explique comment créer un dictionnaire personnalisé pour la reconnaissance de l’écriture manuscrite.
ms.assetid: 83abf534-740c-44a3-bbd4-babb54f2930e
title: Création de dictionnaires personnalisés pour la reconnaissance de l’écriture manuscrite dans Windows 7 et Windows Server 2008 R2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80b9b7b5a1d9dfadddd83825aea7d6f676439999
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514566"
---
# <a name="creating-custom-dictionaries-for-handwriting-recognition-in-windows-7-and-windows-server-2008-r2"></a><span data-ttu-id="6368f-103">Création de dictionnaires personnalisés pour la reconnaissance de l’écriture manuscrite dans Windows 7 et Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6368f-103">Creating Custom Dictionaries for Handwriting Recognition in Windows 7 and Windows Server 2008 R2</span></span>

<span data-ttu-id="6368f-104">Cette section explique comment créer un dictionnaire personnalisé pour la reconnaissance de l’écriture manuscrite.</span><span class="sxs-lookup"><span data-stu-id="6368f-104">This section explains how to create a custom dictionary for handwriting recognition.</span></span>

<span data-ttu-id="6368f-105">Dans le système d’exploitation Windows 7 et le système d’exploitation Windows Server 2008 R2, la précision de la reconnaissance de l’écriture manuscrite peut être considérablement améliorée grâce à l’utilisation de dictionnaires personnalisés.</span><span class="sxs-lookup"><span data-stu-id="6368f-105">In the Windows 7 operating system and the Windows Server 2008 R2 operating system, the accuracy of handwriting recognition can be significantly improved through the use of custom dictionaries.</span></span> <span data-ttu-id="6368f-106">Ces dictionnaires complètent ou remplacent les dictionnaires système utilisés pour l’écriture manuscrite.</span><span class="sxs-lookup"><span data-stu-id="6368f-106">These dictionaries supplement or replace system dictionaries used for handwriting.</span></span> <span data-ttu-id="6368f-107">La prise en charge de la reconnaissance de l’écriture manuscrite est fournie par la fonctionnalité Services de prise en charge de l’écriture manuscrite qui doit être activée via Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="6368f-107">Support for handwriting recognition is provided through the Ink and Handwriting Services feature that needs to be enabled through Server Manager.</span></span>

> [!Note]  
> <span data-ttu-id="6368f-108">Les dictionnaires personnalisés peuvent être installés pour une langue uniquement si le module de reconnaissance de l’écriture manuscrite pour cette langue est installé.</span><span class="sxs-lookup"><span data-stu-id="6368f-108">Custom dictionaries can be installed for a language only if the handwriting recognizer for that language is installed.</span></span>

 

<span data-ttu-id="6368f-109">Il existe deux étapes de base pour configurer un dictionnaire personnalisé pour l’écriture manuscrite :</span><span class="sxs-lookup"><span data-stu-id="6368f-109">There are two basic steps to setting up a custom dictionary for handwriting:</span></span>

-   <span data-ttu-id="6368f-110">Compiler une liste de mots.</span><span class="sxs-lookup"><span data-stu-id="6368f-110">Compile a word list.</span></span> <span data-ttu-id="6368f-111">La compilation crée un fichier de dictionnaire personnalisé (. hwrdict) compilé.</span><span class="sxs-lookup"><span data-stu-id="6368f-111">The compilation creates a compiled custom dictionary (.hwrdict) file.</span></span>
-   <span data-ttu-id="6368f-112">Installez le dictionnaire personnalisé compilé.</span><span class="sxs-lookup"><span data-stu-id="6368f-112">Install the compiled custom dictionary.</span></span>

## <a name="compiling-a-word-list"></a><span data-ttu-id="6368f-113">Compilation d’une liste de mots</span><span class="sxs-lookup"><span data-stu-id="6368f-113">Compiling a Word List</span></span>

<span data-ttu-id="6368f-114">La liste de mots à compiler doit être au format texte brut et doit être enregistrée à l’aide d’un encodage Unicode.</span><span class="sxs-lookup"><span data-stu-id="6368f-114">The word list to be compiled must be in plain-text format and should be saved using a Unicode encoding.</span></span> <span data-ttu-id="6368f-115">Les autres encodages ne fonctionneront pas.</span><span class="sxs-lookup"><span data-stu-id="6368f-115">Other encodings will not work.</span></span> <span data-ttu-id="6368f-116">Chaque ligne du fichier texte est considérée comme une seule entrée dans le dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="6368f-116">Each line of the text file is taken as a single entry in the dictionary.</span></span> <span data-ttu-id="6368f-117">Les entrées d’unités multimots contenant un ou plusieurs espaces sont autorisées.</span><span class="sxs-lookup"><span data-stu-id="6368f-117">Multiword units entries containing one or more spaces are allowed.</span></span> <span data-ttu-id="6368f-118">Les espaces au début ou à la fin d’une ligne sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="6368f-118">Spaces at the beginning or end of a line are ignored.</span></span>

<span data-ttu-id="6368f-119">Un dictionnaire personnalisé est compilé à partir d’une ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="6368f-119">A custom dictionary is compiled from a command line.</span></span> <span data-ttu-id="6368f-120">Pour compiler un dictionnaire, ouvrez une fenêtre de commande, accédez au dossier contenant la liste de mots, puis exécutez HwrComp.exe avec les options de ligne de commande que vous souhaitez utiliser.</span><span class="sxs-lookup"><span data-stu-id="6368f-120">To compile a dictionary, open a command window, navigate to the folder containing the word list, and then run HwrComp.exe with the command-line options you want to use.</span></span>

<span data-ttu-id="6368f-121">L’exemple suivant illustre la syntaxe d’utilisation pour les options de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="6368f-121">The following example shows the usage syntax for the command-line options.</span></span>

``` syntax
Usage: hwrcomp       [-lang <localename>] [-type <type>]
    [-comment <comment>]
    [-o <dictfile.hwrdict>]
    <inputfile>
     
```

### <a name="explanation-of-options"></a><span data-ttu-id="6368f-122">Explication des options</span><span class="sxs-lookup"><span data-stu-id="6368f-122">Explanation of Options</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6368f-123">Paramètre</span><span class="sxs-lookup"><span data-stu-id="6368f-123">Parameter</span></span></th>
<th><span data-ttu-id="6368f-124">Description</span><span class="sxs-lookup"><span data-stu-id="6368f-124">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6368f-125">-lang <localename></span><span class="sxs-lookup"><span data-stu-id="6368f-125">-lang <localename></span></span></td>
<td><span data-ttu-id="6368f-126">Nom des paramètres régionaux spécifiés attribués au fichier de dictionnaire personnalisé compilé.</span><span class="sxs-lookup"><span data-stu-id="6368f-126">The specified locale name assigned to the compiled custom dictionary file.</span></span> <span data-ttu-id="6368f-127">L’argument <localename> se présente sous la forme langue-région.</span><span class="sxs-lookup"><span data-stu-id="6368f-127">The argument <localename> has the form language-REGION.</span></span> <span data-ttu-id="6368f-128">Par exemple, est en-US, ce qui signifie la langue anglaise dans la région États-Unis.</span><span class="sxs-lookup"><span data-stu-id="6368f-128">An example of this is en-US, which signifies the English language in the United States region.</span></span> <span data-ttu-id="6368f-129">Pour obtenir des exemples de ce formulaire, consultez [constantes et chaînes](/windows/desktop/Intl/language-identifier-constants-and-strings)de l’identificateur de langage.</span><span class="sxs-lookup"><span data-stu-id="6368f-129">For examples of this form, see [Language Identifier Constants and Strings](/windows/desktop/Intl/language-identifier-constants-and-strings).</span></span> <span data-ttu-id="6368f-130">Les langues suivantes sont prises en charge pour Windows 7 et Windows Server 2008 R2 par cette fonctionnalité : en-US, en-GB, en-CA, en-au, de-DE, de-CH, fr-FR, es-ES, es-MX, es-AR, IT-IT, NL-NL, NL-is, PT-BR, PT-PT, da-DK, SV-SE, NB-NO, NN-NO, FI-FI, PL-PL, CS-CZ, ru-RU, RO-RO, SR-LATN-CS, SR-Cyrl-CS, ca-ES et HR-HR.</span><span class="sxs-lookup"><span data-stu-id="6368f-130">The following languages are supported for Windows 7 and Windows Server 2008 R2 by this feature: en-US, en-GB, en-CA, en-AU, de-DE, de-CH, fr-FR, es-ES, es-MX, es-AR, it-IT, nl-NL, nl-BE, pt-BR, pt-PT, da-DK, sv-SE, nb-NO, nn-NO, fi-FI, pl-PL, cs-CZ, ru-RU, ro-RO, sr-Latn-CS, sr-Cyrl-CS, ca-ES and hr-HR.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6368f-131">-type <type></span><span class="sxs-lookup"><span data-stu-id="6368f-131">-type <type></span></span></td>
<td><span data-ttu-id="6368f-132">L’argument option <type> est une concaténation à chaîne unique de l’utilisation de la ressource en tant que liste de mots principale (principale) ou en complément de la liste de mots principale (secondaire), suivie du nom de la liste de mots réelle à laquelle la ressource est appliquée (par exemple, dictionary ou Surname).</span><span class="sxs-lookup"><span data-stu-id="6368f-132">The option argument <type> is a single-string concatenation of the resource's use as either the main word list (PRIMARY) or as a supplement to the main word list (SECONDARY) followed by the actual word list name to which the resource is applied (such as DICTIONARY or SURNAME).</span></span> <span data-ttu-id="6368f-133">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="6368f-133">The following are possible values:</span></span>
<ul>
<li><span data-ttu-id="6368f-134">PRIMARY-NOM_VILLE-LIST</span><span class="sxs-lookup"><span data-stu-id="6368f-134">PRIMARY-CITYNAME-LIST</span></span></li>
<li><span data-ttu-id="6368f-135">PRIMARY-COUNTRYNAME-LIST</span><span class="sxs-lookup"><span data-stu-id="6368f-135">PRIMARY-COUNTRYNAME-LIST</span></span></li>
<li><span data-ttu-id="6368f-136">PRIMARY-COUNTRYSHORTNAME-LIST</span><span class="sxs-lookup"><span data-stu-id="6368f-136">PRIMARY-COUNTRYSHORTNAME-LIST</span></span></li>
<li><span data-ttu-id="6368f-137">DICTIONNAIRE PRINCIPAL</span><span class="sxs-lookup"><span data-stu-id="6368f-137">PRIMARY-DICTIONARY</span></span></li>
<li><span data-ttu-id="6368f-138">PRIMARY-GIVENNAME-LIST</span><span class="sxs-lookup"><span data-stu-id="6368f-138">PRIMARY-GIVENNAME-LIST</span></span></li>
<li><span data-ttu-id="6368f-139">PRIMARY-STATEORPROVINCE-LIST</span><span class="sxs-lookup"><span data-stu-id="6368f-139">PRIMARY-STATEORPROVINCE-LIST</span></span></li>
<li><span data-ttu-id="6368f-140">PRIMARY-STREETNAME-LIST</span><span class="sxs-lookup"><span data-stu-id="6368f-140">PRIMARY-STREETNAME-LIST</span></span></li>
<li><span data-ttu-id="6368f-141">PRIMARY-SURNAME-LIST</span><span class="sxs-lookup"><span data-stu-id="6368f-141">PRIMARY-SURNAME-LIST</span></span></li>
<li><span data-ttu-id="6368f-142">SECONDARY-NOM_VILLE-LIST</span><span class="sxs-lookup"><span data-stu-id="6368f-142">SECONDARY-CITYNAME-LIST</span></span></li>
<li><span data-ttu-id="6368f-143">COUNTRYNAME SECONDAIRE-LISTE</span><span class="sxs-lookup"><span data-stu-id="6368f-143">SECONDARY-COUNTRYNAME-LIST</span></span></li>
<li><span data-ttu-id="6368f-144">COUNTRYSHORTNAME SECONDAIRE-LISTE</span><span class="sxs-lookup"><span data-stu-id="6368f-144">SECONDARY-COUNTRYSHORTNAME-LIST</span></span></li>
<li><span data-ttu-id="6368f-145">DICTIONNAIRE SECONDAIRE</span><span class="sxs-lookup"><span data-stu-id="6368f-145">SECONDARY-DICTIONARY</span></span></li>
<li><span data-ttu-id="6368f-146">EMAILSMTP SECONDAIRE-LISTE</span><span class="sxs-lookup"><span data-stu-id="6368f-146">SECONDARY-EMAILSMTP-LIST</span></span></li>
<li><span data-ttu-id="6368f-147">EMAILUSERNAME SECONDAIRE-LISTE</span><span class="sxs-lookup"><span data-stu-id="6368f-147">SECONDARY-EMAILUSERNAME-LIST</span></span></li>
<li><span data-ttu-id="6368f-148">SECONDAIRE-GIVENNAME-LIST</span><span class="sxs-lookup"><span data-stu-id="6368f-148">SECONDARY-GIVENNAME-LIST</span></span></li>
<li><span data-ttu-id="6368f-149">STATEORPROVINCE SECONDAIRE-LISTE</span><span class="sxs-lookup"><span data-stu-id="6368f-149">SECONDARY-STATEORPROVINCE-LIST</span></span></li>
<li><span data-ttu-id="6368f-150">STREETNAME SECONDAIRE-LISTE</span><span class="sxs-lookup"><span data-stu-id="6368f-150">SECONDARY-STREETNAME-LIST</span></span></li>
<li><span data-ttu-id="6368f-151">SECONDAIRE-SURNAME-LIST</span><span class="sxs-lookup"><span data-stu-id="6368f-151">SECONDARY-SURNAME-LIST</span></span></li>
<li><span data-ttu-id="6368f-152">LISTE D’URL SECONDAIRE</span><span class="sxs-lookup"><span data-stu-id="6368f-152">SECONDARY-URL-LIST</span></span></li>
</ul>
<span data-ttu-id="6368f-153">Si une valeur de type commence par le préfixe PRIMARY, le dictionnaire compilé, après son installation, remplace le dictionnaire système pour cette langue.</span><span class="sxs-lookup"><span data-stu-id="6368f-153">If a type value starts with the prefix PRIMARY, the compiled dictionary, after it is installed, will replace the system dictionary for that language.</span></span> <span data-ttu-id="6368f-154">La valeur principal-DICTIONARY représente le dictionnaire principal du système pour une langue.</span><span class="sxs-lookup"><span data-stu-id="6368f-154">The value PRIMARY-DICTIONARY represents the main system dictionary for a language.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="6368f-155">Le remplacement d’un dictionnaire système n’a aucun effet sur le contenu du dictionnaire système d’origine, car le remplacement est effectif uniquement jusqu’à ce que le dictionnaire personnalisé ait été supprimé.</span><span class="sxs-lookup"><span data-stu-id="6368f-155">Replacing a system dictionary does nothing to the original system dictionary content, as the replacement is in effect only until the custom dictionary has been removed.</span></span>
</blockquote>
<br/> <span data-ttu-id="6368f-156">Si une valeur de type commence par le préfixe SECONDARY, le dictionnaire compilé complète le dictionnaire système sans le remplacer.</span><span class="sxs-lookup"><span data-stu-id="6368f-156">If a type value starts with the prefix SECONDARY, the compiled dictionary will supplement the system dictionary without replacing it.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6368f-157">-Comment</span><span class="sxs-lookup"><span data-stu-id="6368f-157">-comment</span></span> <comment></td>
<td><span data-ttu-id="6368f-158">Le commentaire spécifié est compilé dans le fichier de dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="6368f-158">The specified comment is compiled into the dictionary file.</span></span> <span data-ttu-id="6368f-159">Le commentaire doit être une chaîne unique et ne pas dépasser 64 caractères.</span><span class="sxs-lookup"><span data-stu-id="6368f-159">The comment must be a single string and no longer than 64 characters.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6368f-160">-o <dictfile.hwrdict></span><span class="sxs-lookup"><span data-stu-id="6368f-160">-o <dictfile.hwrdict></span></span></td>
<td><span data-ttu-id="6368f-161">La sortie est écrite dans le nom de fichier spécifié par <dictfile.hwrdict> .</span><span class="sxs-lookup"><span data-stu-id="6368f-161">Output is written to the file name specified by <dictfile.hwrdict>.</span></span><br/> <span data-ttu-id="6368f-162">Si cette option est manquante, le nom du fichier de sortie est dérivé du nom du fichier d’entrée d’origine, avec l’extension de fichier d’entrée remplacée par. hwrdict.</span><span class="sxs-lookup"><span data-stu-id="6368f-162">If this option is missing, the output file name is derived from the original input file name, with the input file extension replaced by .hwrdict.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="defaults"></a><span data-ttu-id="6368f-163">Valeurs par défaut</span><span class="sxs-lookup"><span data-stu-id="6368f-163">Defaults</span></span>

<span data-ttu-id="6368f-164">Si aucun paramètre n’est spécifié, les valeurs d’option par défaut sont</span><span class="sxs-lookup"><span data-stu-id="6368f-164">If no parameters are specified, the default option values are</span></span>

<span data-ttu-id="6368f-165">-lang <current input language> -type secondaire-dictionnaire</span><span class="sxs-lookup"><span data-stu-id="6368f-165">-lang <current input language> -type SECONDARY-DICTIONARY</span></span>

### <a name="examples"></a><span data-ttu-id="6368f-166">Exemples</span><span class="sxs-lookup"><span data-stu-id="6368f-166">Examples</span></span>

<span data-ttu-id="6368f-167">L’exemple suivant compile le fichier d’entrée mylist1.txt, applique les valeurs d’option par défaut et crée le fichier de sortie mylist1. hwrdict.</span><span class="sxs-lookup"><span data-stu-id="6368f-167">The following compiles the input file mylist1.txt, applies the default option values, and creates the output file mylist1.hwrdict.</span></span>

``` syntax
hwrcomp mylist1.txt
```

<span data-ttu-id="6368f-168">En revanche, le code suivant compile mylist1.txt dans myrsrc1. hwrdict, mais affecte « English (US) » (en-US) comme langage et le dictionnaire secondaire comme type.</span><span class="sxs-lookup"><span data-stu-id="6368f-168">In contrast, the following compiles mylist1.txt into myrsrc1.hwrdict, but assigns "English (US)" (en-US) as the language and SECONDARY-DICTIONARY as the type.</span></span>

``` syntax
hwrcomp -lang en-US -type SECONDARY-DICTIONARY -o myrsrc1 mylist1.txt 
```

## <a name="installing-a-compiled-custom-dictionary"></a><span data-ttu-id="6368f-169">Installation d’un dictionnaire personnalisé compilé</span><span class="sxs-lookup"><span data-stu-id="6368f-169">Installing a Compiled Custom Dictionary</span></span>

<span data-ttu-id="6368f-170">HwrComp.exe crée un fichier. hwrdict, qui est dans un format binaire utilisable par un module de reconnaissance de l’écriture manuscrite.</span><span class="sxs-lookup"><span data-stu-id="6368f-170">HwrComp.exe creates a .hwrdict file, which is in a binary format usable by a handwriting recognizer.</span></span> <span data-ttu-id="6368f-171">Ce fichier peut être installé sur n’importe quel ordinateur exécutant Windows 7 ou Windows Server 2008 R2 qui prend en charge la reconnaissance de l’écriture manuscrite.</span><span class="sxs-lookup"><span data-stu-id="6368f-171">This file can be installed on any computer running Windows 7 or Windows Server 2008 R2 that supports handwriting recognition.</span></span> <span data-ttu-id="6368f-172">Un dictionnaire est installé uniquement pour l’utilisateur actuel ou pour tous les utilisateurs sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="6368f-172">A dictionary is installed either for just the current user or for all users on a machine.</span></span>

<span data-ttu-id="6368f-173">Un fichier de dictionnaire personnalisé compilé peut être installé à partir de la ligne de commande à l’aide de l’outil HwrReg.exe.</span><span class="sxs-lookup"><span data-stu-id="6368f-173">A compiled custom dictionary file can be installed from the command line using the tool HwrReg.exe.</span></span> <span data-ttu-id="6368f-174">Cet outil est utile si vous souhaitez remplacer certaines des valeurs de configuration qui sont compilées dans le fichier ou qui sont les valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="6368f-174">This tool is useful if you wish to override some of the configuration values that either are compiled into the file or are the default values.</span></span> <span data-ttu-id="6368f-175">Il existe deux façons d’exécuter HwrReg.exe : en mode vérification/installation et en mode liste/suppression.</span><span class="sxs-lookup"><span data-stu-id="6368f-175">There are two ways to run HwrReg.exe: in check/install mode and in list/remove mode.</span></span>

### <a name="running-hwrregexe-in-checkinstall-mode"></a><span data-ttu-id="6368f-176">Exécution de HwrReg.exe en mode de vérification/installation</span><span class="sxs-lookup"><span data-stu-id="6368f-176">Running HwrReg.exe in Check/Install Mode</span></span>

<span data-ttu-id="6368f-177">Ce mode est destiné aux fichiers de dictionnaires personnalisés qui n’ont pas encore été installés.</span><span class="sxs-lookup"><span data-stu-id="6368f-177">This mode is for custom dictionary files that have not yet been installed.</span></span> <span data-ttu-id="6368f-178">L’exemple suivant illustre la syntaxe d’utilisation des options de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="6368f-178">The following shows the usage syntax for the command-line options.</span></span>

``` syntax
Usage: hwrreg        [-check]
    [-lang <localename>] 
    [-scope {all|me}]
    [-noprompt] 
    <dictfile.hwrdict>
```

### <a name="explanation-of-options"></a><span data-ttu-id="6368f-179">Explication des options</span><span class="sxs-lookup"><span data-stu-id="6368f-179">Explanation of Options</span></span>



| <span data-ttu-id="6368f-180">Paramètre</span><span class="sxs-lookup"><span data-stu-id="6368f-180">Parameter</span></span>                | <span data-ttu-id="6368f-181">Description</span><span class="sxs-lookup"><span data-stu-id="6368f-181">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                        |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6368f-182">-vérifier</span><span class="sxs-lookup"><span data-stu-id="6368f-182">-check</span></span>                   | <span data-ttu-id="6368f-183">Le fichier du dictionnaire est vérifié sans être installé.</span><span class="sxs-lookup"><span data-stu-id="6368f-183">The dictionary file is verified without being installed.</span></span> <span data-ttu-id="6368f-184">L’option vérifier affiche le commentaire du fichier, ainsi que les informations d’enregistrement qui seraient utilisées pour installer le fichier.</span><span class="sxs-lookup"><span data-stu-id="6368f-184">The  check option displays the file's comment, plus the registration information that would be used to install the file.</span></span> <span data-ttu-id="6368f-185">Cette option est utile pour vérifier les informations d’inscription avant l’exécution de l’installation.</span><span class="sxs-lookup"><span data-stu-id="6368f-185">This option is useful for verifying registration information before the installation is performed.</span></span> <br/> <span data-ttu-id="6368f-186">Si cette option est manquante, HwrReg.exe installe le dictionnaire personnalisé.</span><span class="sxs-lookup"><span data-stu-id="6368f-186">If this option is missing, HwrReg.exe installs the custom dictionary.</span></span><br/>  |
|  <span data-ttu-id="6368f-187">lang <localename></span><span class="sxs-lookup"><span data-stu-id="6368f-187">lang <localename></span></span> | <span data-ttu-id="6368f-188">Le fichier du dictionnaire est vérifié sans être installé.</span><span class="sxs-lookup"><span data-stu-id="6368f-188">The dictionary file is verified without being installed.</span></span> <span data-ttu-id="6368f-189">L’option vérifier affiche le commentaire du fichier, ainsi que les informations d’enregistrement qui seraient utilisées pour installer le fichier.</span><span class="sxs-lookup"><span data-stu-id="6368f-189">The  check option displays the file's comment, plus the registration information that would be used to install the file.</span></span> <span data-ttu-id="6368f-190">Cette option est utile pour vérifier les informations d’inscription avant l’exécution de l’installation.</span><span class="sxs-lookup"><span data-stu-id="6368f-190">This option is useful for verifying registration information before the installation is performed.</span></span> <br/> <span data-ttu-id="6368f-191">Si cette option est manquante, HwrReg.exe installe le dictionnaire personnalisé.</span><span class="sxs-lookup"><span data-stu-id="6368f-191">If this option is missing, HwrReg.exe installs the custom dictionary.</span></span> <br/> |
|  <span data-ttu-id="6368f-192">étendue {All \| me}</span><span class="sxs-lookup"><span data-stu-id="6368f-192">scope {all\|me}</span></span>         | <span data-ttu-id="6368f-193">Le dictionnaire personnalisé est installé pour tous les utilisateurs (étendue tous) ou uniquement pour l’utilisateur actuel (étendue me).</span><span class="sxs-lookup"><span data-stu-id="6368f-193">The custom dictionary is installed either for all users ( scope all) or for just the current user ( scope me).</span></span> <span data-ttu-id="6368f-194">L’installation de avec l’étendue All requiert que la commande soit exécutée dans une invite de commandes avec élévation de privilèges ; dans le cas contraire, un code d’erreur est retourné.</span><span class="sxs-lookup"><span data-stu-id="6368f-194">Installing with  scope all requires the command to be run in an elevated command prompt; otherwise, an error code will be returned.</span></span> <br/> <span data-ttu-id="6368f-195">Si cette option est manquante, l’installation est limitée à l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="6368f-195">If this option is missing, the installation is scoped to just the current user.</span></span><br/>                          |
|  <span data-ttu-id="6368f-196">commutateur noprompt</span><span class="sxs-lookup"><span data-stu-id="6368f-196">noprompt</span></span>                | <span data-ttu-id="6368f-197">HwrReg.exe ne demande pas de confirmation.</span><span class="sxs-lookup"><span data-stu-id="6368f-197">HwrReg.exe does not prompt for confirmation.</span></span> <span data-ttu-id="6368f-198">Cela peut être utile lors de l’exécution de hwrReg.exe à partir d’un script.</span><span class="sxs-lookup"><span data-stu-id="6368f-198">This can be useful when running hwrReg.exe from a script.</span></span> <br/>                                                                                                                                                                                                                                                                 |



 

<span data-ttu-id="6368f-199">L’exemple suivant installe le dictionnaire personnalisé myrsrc1. hwrdict pour le langage « danois (Denmark) » (da DK), avec uniquement l’étendue par défaut de l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="6368f-199">The following example installs the custom dictionary myrsrc1.hwrdict for language "Danish (Denmark)" (da DK), with the default scope of just the current user.</span></span>

``` syntax
hwrreg -lang da-DK myrsrc1.hwrdict 
```

### <a name="running-hwrregexe-in-listremove-mode"></a><span data-ttu-id="6368f-200">Exécution de HwrReg.exe en mode liste/suppression</span><span class="sxs-lookup"><span data-stu-id="6368f-200">Running HwrReg.exe in List/Remove Mode</span></span>

<span data-ttu-id="6368f-201">Ce mode permet de répertorier ou de supprimer les dictionnaires personnalisés installés.</span><span class="sxs-lookup"><span data-stu-id="6368f-201">This mode either lists or removes installed custom dictionaries.</span></span> <span data-ttu-id="6368f-202">L’exemple suivant illustre la syntaxe d’utilisation des options de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="6368f-202">The following shows the usage syntax for the command-line options.</span></span>

``` syntax
Usage: hwrreg        [-lang <localename>] 
    [-scope {all|me}] 
    [-type <type>]
    -list | -remove
```

### <a name="explanation-of-options"></a><span data-ttu-id="6368f-203">Explication des options</span><span class="sxs-lookup"><span data-stu-id="6368f-203">Explanation of Options</span></span>



| <span data-ttu-id="6368f-204">Paramètre</span><span class="sxs-lookup"><span data-stu-id="6368f-204">Parameter</span></span>                | <span data-ttu-id="6368f-205">Description</span><span class="sxs-lookup"><span data-stu-id="6368f-205">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  <span data-ttu-id="6368f-206">lang <localename></span><span class="sxs-lookup"><span data-stu-id="6368f-206">lang <localename></span></span> | <span data-ttu-id="6368f-207">Les dictionnaires inscrits pour uniquement ce nom de paramètres régionaux sont répertoriés ou supprimés.</span><span class="sxs-lookup"><span data-stu-id="6368f-207">The dictionaries registered for only this locale name are listed or removed.</span></span> <span data-ttu-id="6368f-208">L’argument <localename> a la région de langue du formulaire.</span><span class="sxs-lookup"><span data-stu-id="6368f-208">The argument <localename> has the form language REGION.</span></span> <span data-ttu-id="6368f-209">Pour obtenir des exemples de ce formulaire, consultez [constantes et chaînes](/windows/desktop/Intl/language-identifier-constants-and-strings)de l’identificateur de langage.</span><span class="sxs-lookup"><span data-stu-id="6368f-209">For examples of this form, see [Language Identifier Constants and Strings](/windows/desktop/Intl/language-identifier-constants-and-strings).</span></span> <br/> <span data-ttu-id="6368f-210">Si cette option est manquante, les dictionnaires pour toutes les langues sont répertoriés ou supprimés.</span><span class="sxs-lookup"><span data-stu-id="6368f-210">If this option is missing, dictionaries for all languages are listed or removed.</span></span><br/> |
|  <span data-ttu-id="6368f-211">étendue {All \| me}</span><span class="sxs-lookup"><span data-stu-id="6368f-211">scope {all\|me}</span></span>         | <span data-ttu-id="6368f-212">Le dictionnaire personnalisé est installé pour tous les utilisateurs (étendue tous) ou uniquement pour l’utilisateur actuel (étendue me).</span><span class="sxs-lookup"><span data-stu-id="6368f-212">The custom dictionary is installed either for all users ( scope all) or for just the current user ( scope me).</span></span> <span data-ttu-id="6368f-213">L’installation de avec l’étendue All requiert que la commande soit exécutée dans une invite de commandes avec élévation de privilèges ; dans le cas contraire, un code d’erreur est retourné.</span><span class="sxs-lookup"><span data-stu-id="6368f-213">Installing with  scope all requires the command to be run in an elevated command prompt; otherwise, an error code will be returned.</span></span> <br/> <span data-ttu-id="6368f-214">Si cette option est manquante, l’installation est limitée à l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="6368f-214">If this option is missing, the installation is scoped to just the current user.</span></span><br/>                      |
|  <span data-ttu-id="6368f-215">entrer <type></span><span class="sxs-lookup"><span data-stu-id="6368f-215">type <type></span></span>       | <span data-ttu-id="6368f-216">Répertorie ou supprime uniquement les dictionnaires inscrits avec le type spécifié.</span><span class="sxs-lookup"><span data-stu-id="6368f-216">Lists or removes only dictionaries that are registered with the specified type.</span></span><br/> <span data-ttu-id="6368f-217">Si cette option est manquante, tous les types de dictionnaires sont répertoriés ou supprimés.</span><span class="sxs-lookup"><span data-stu-id="6368f-217">If this option is missing, all dictionary types are listed or removed.</span></span> <span data-ttu-id="6368f-218">L’installation ou la suppression d’un dictionnaire personnalisé d’un autre type (par exemple, PRIMARY-COUNTRYNAME-LIST) peut affecter la reconnaissance de l’écriture manuscrite dans d’autres contextes.</span><span class="sxs-lookup"><span data-stu-id="6368f-218">Installing or removing a custom dictionary of another type (such as PRIMARY-COUNTRYNAME-LIST) may affect handwriting recognition in other contexts.</span></span> <br/>                                              |
|  <span data-ttu-id="6368f-219">list</span><span class="sxs-lookup"><span data-stu-id="6368f-219">list</span></span>                    | <span data-ttu-id="6368f-220">Répertorie tous les dictionnaires installés qui correspondent aux autres options.</span><span class="sxs-lookup"><span data-stu-id="6368f-220">Lists all installed dictionaries that match the other options.</span></span><br/> <span data-ttu-id="6368f-221">Si cette option est manquante, l’option supprimer doit être spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6368f-221">If this option is missing, the option  remove must be specified.</span></span><br/>                                                                                                                                                                                                                          |
|  <span data-ttu-id="6368f-222">remove</span><span class="sxs-lookup"><span data-stu-id="6368f-222">remove</span></span>                  | <span data-ttu-id="6368f-223">Demande la suppression d’un dictionnaire qui correspond aux autres options.</span><span class="sxs-lookup"><span data-stu-id="6368f-223">Prompts for removal of any dictionary that matches the other options.</span></span><br/> <span data-ttu-id="6368f-224">Si cette option est manquante, la liste d’options doit être spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6368f-224">If this option is missing, the option  list must be specified.</span></span><br/>                                                                                                                                                                                                                     |



 

### <a name="examples"></a><span data-ttu-id="6368f-225">Exemples</span><span class="sxs-lookup"><span data-stu-id="6368f-225">Examples</span></span>

<span data-ttu-id="6368f-226">Les listes suivantes répertorient les dictionnaires dont la langue est l’anglais (États-Unis) et le dictionnaire principal de type et qui sont installés uniquement pour l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="6368f-226">The following lists dictionaries that have language "English (US)" (en US) and type PRIMARY DICTIONARY and that are installed for just the current user.</span></span>

``` syntax
hwrreg -list -lang en-US -type PRIMARY-DICTIONARY
                  
```

<span data-ttu-id="6368f-227">De même, le code suivant supprime les dictionnaires qui correspondent aux mêmes critères.</span><span class="sxs-lookup"><span data-stu-id="6368f-227">Similarly, the following removes dictionaries that match the same criteria.</span></span>

``` syntax
hwrreg -remove -lang en-US -type PRIMARY-DICTIONARY
                  
```

## <a name="general-notes-on-custom-dictionaries"></a><span data-ttu-id="6368f-228">Remarques générales sur les dictionnaires personnalisés</span><span class="sxs-lookup"><span data-stu-id="6368f-228">General Notes on Custom Dictionaries</span></span>

-   <span data-ttu-id="6368f-229">Si vous installez deux dictionnaires personnalisés qui ont le même type, la même langue et la même étendue, la deuxième installation remplacera la première.</span><span class="sxs-lookup"><span data-stu-id="6368f-229">If you install two custom dictionaries that have the same type, language, and scope, the second installation will overwrite the first.</span></span>
-   <span data-ttu-id="6368f-230">Si vous installez deux dictionnaires personnalisés avec le même type et la même langue, mais avec des étendues différentes (une pour tous les utilisateurs et une pour l’utilisateur actuel), le dictionnaire installé pour l’utilisateur actuel est prioritaire et le dictionnaire installé pour tous les utilisateurs est ignoré.</span><span class="sxs-lookup"><span data-stu-id="6368f-230">If you install two custom dictionaries with the same type and language, but with different scopes (one for all users, and one for the current user), the dictionary installed for the current user takes precedence, and the dictionary installed for all users is ignored.</span></span>

 

