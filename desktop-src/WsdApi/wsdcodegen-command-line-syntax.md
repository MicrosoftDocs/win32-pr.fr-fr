---
description: 'WsdCodeGen a deux fonctions : la génération de fichiers de configuration et la génération de code source pour le client WSDAPI et les applications hôtes.'
ms.assetid: 75f5071c-040b-4e65-a80e-e1fea63535b0
title: Syntaxe de la ligne de commande WsdCodeGen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff7db3afe9b13286833f8563c0cacb41919d77bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863750"
---
# <a name="wsdcodegen-command-line-syntax"></a><span data-ttu-id="59ea9-103">Syntaxe de la ligne de commande WsdCodeGen</span><span class="sxs-lookup"><span data-stu-id="59ea9-103">WsdCodeGen Command Line Syntax</span></span>

<span data-ttu-id="59ea9-104">WsdCodeGen a deux fonctions : la génération de fichiers de configuration et la génération de code source pour le client WSDAPI et les applications hôtes.</span><span class="sxs-lookup"><span data-stu-id="59ea9-104">WsdCodeGen has two functions: generating configuration files and generating source code for WSDAPI client and host applications.</span></span> <span data-ttu-id="59ea9-105">Cette rubrique indique la syntaxe de ligne de commande utilisée pour effectuer chaque tâche.</span><span class="sxs-lookup"><span data-stu-id="59ea9-105">This topic gives the command line syntax used to perform each task.</span></span>

## <a name="generating-a-configuration-file"></a><span data-ttu-id="59ea9-106">Génération d’un fichier de configuration</span><span class="sxs-lookup"><span data-stu-id="59ea9-106">Generating a Configuration File</span></span>

### <a name="syntax"></a><span data-ttu-id="59ea9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="59ea9-107">Syntax</span></span>

<span data-ttu-id="59ea9-108">**WSDCODEGEN.EXE** **/generateconfig :**{**client** \| **Host** \| **All**} **\[ /outputfile :**_ConfigFileName_ *_\]_* *WSDLFileNameList*</span><span class="sxs-lookup"><span data-stu-id="59ea9-108">**WSDCODEGEN.EXE** **/generateconfig:**{**client**\|**host**\|**all**} **\[/outputfile:**_ConfigFileName_*_\]_* *WSDLFileNameList*</span></span>

### <a name="parameters"></a><span data-ttu-id="59ea9-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="59ea9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59ea9-110"><span id="_generateconfig__client___host___all_"></span><span id="_GENERATECONFIG__CLIENT___HOST___ALL_"></span>**/generateconfig : {client \| host \| All}**</span><span class="sxs-lookup"><span data-stu-id="59ea9-110"><span id="_generateconfig__client___host___all_"></span><span id="_GENERATECONFIG__CLIENT___HOST___ALL_"></span>**/generateconfig:{client \| host \| all}**</span></span>
</dt> <dd>

<span data-ttu-id="59ea9-111">Type de code généré par le fichier de configuration de sortie.</span><span class="sxs-lookup"><span data-stu-id="59ea9-111">The type of code that the output configuration file will generate.</span></span> <span data-ttu-id="59ea9-112">**/generateconfig : le client** est utilisé pour générer un fichier de configuration pour générer le code client, **/generateconfig : Host** est utilisé pour générer un fichier de configuration pour la génération de code hôte, et **/generateconfig : All** est utilisé pour générer un fichier de configuration pour la génération du code client et du code hôte.</span><span class="sxs-lookup"><span data-stu-id="59ea9-112">**/generateconfig:client** is used to generate a configuration file for generating client code, **/generateconfig:host** is used to generate a configuration file for generating host code, and **/generateconfig:all** is used to generate a configuration file for generating both client and host code.</span></span>

</dd> <dt>

<span data-ttu-id="59ea9-113"><span id="_outputfile_ConfigFileName"></span><span id="_outputfile_configfilename"></span><span id="_OUTPUTFILE_CONFIGFILENAME"></span>**/outputfile :**_ConfigFileName_</span><span class="sxs-lookup"><span data-stu-id="59ea9-113"><span id="_outputfile_ConfigFileName"></span><span id="_outputfile_configfilename"></span><span id="_OUTPUTFILE_CONFIGFILENAME"></span>**/outputfile:**_ConfigFileName_</span></span>
</dt> <dd>

<span data-ttu-id="59ea9-114">Ce paramètre facultatif est utilisé pour spécifier le nom de fichier du fichier de configuration de sortie.</span><span class="sxs-lookup"><span data-stu-id="59ea9-114">This optional parameter is used to specify the file name of the output configuration file.</span></span> <span data-ttu-id="59ea9-115">Si ce paramètre est exclu, le nom du fichier de configuration de sortie est codegen.config.</span><span class="sxs-lookup"><span data-stu-id="59ea9-115">If this parameter is excluded, the name of the output configuration file is codegen.config.</span></span>

</dd> <dt>

<span data-ttu-id="59ea9-116"><span id="_pnpx"></span><span id="_PNPX"></span>*/pnpx*</span><span class="sxs-lookup"><span data-stu-id="59ea9-116"><span id="_pnpx"></span><span id="_PNPX"></span>*/pnpx*</span></span>
</dt> <dd>

<span data-ttu-id="59ea9-117">Incluez un modèle PnP-X dans le fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="59ea9-117">Include a PnP-X template in the configuration file.</span></span>

</dd> <dt>

<span data-ttu-id="59ea9-118"><span id="WSDLFileNameList"></span><span id="wsdlfilenamelist"></span><span id="WSDLFILENAMELIST"></span>*WSDLFileNameList*</span><span class="sxs-lookup"><span data-stu-id="59ea9-118"><span id="WSDLFileNameList"></span><span id="wsdlfilenamelist"></span><span id="WSDLFILENAMELIST"></span>*WSDLFileNameList*</span></span>
</dt> <dd>

<span data-ttu-id="59ea9-119">Liste délimitée par des espaces des fichiers WSDL à traiter par WsdCodeGen.</span><span class="sxs-lookup"><span data-stu-id="59ea9-119">A space-delimited list of the WSDL file(s) to be processed by WsdCodeGen.</span></span>

</dd> </dl>

## <a name="generating-source-code"></a><span data-ttu-id="59ea9-120">Génération du code source</span><span class="sxs-lookup"><span data-stu-id="59ea9-120">Generating Source Code</span></span>

### <a name="syntax"></a><span data-ttu-id="59ea9-121">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="59ea9-121">Syntax</span></span>

<span data-ttu-id="59ea9-122">**WSDCODEGEN.EXE** **/GenerateCode** **\[ /download \]** **\[ /GBC \]** **\[ outputroot :**_chemin_ *_\]_* **\[ /WriteAccess :**_commande_ *_\]_* *nomdefichierdeconfiguration*</span><span class="sxs-lookup"><span data-stu-id="59ea9-122">**WSDCODEGEN.EXE** **/generatecode** **\[/download\]** **\[/gbc\]** **\[outputroot:**_path_*_\]_* **\[/writeaccess:**_command_*_\]_* *ConfigFileName*</span></span>

### <a name="parameters"></a><span data-ttu-id="59ea9-123">Paramètres</span><span class="sxs-lookup"><span data-stu-id="59ea9-123">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59ea9-124"><span id="_generatecode"></span><span id="_GENERATECODE"></span>**/generatecode**</span><span class="sxs-lookup"><span data-stu-id="59ea9-124"><span id="_generatecode"></span><span id="_GENERATECODE"></span>**/generatecode**</span></span>
</dt> <dd>

<span data-ttu-id="59ea9-125">Indique à WsdCodeGen de générer le code source.</span><span class="sxs-lookup"><span data-stu-id="59ea9-125">Directs WsdCodeGen to generate source code.</span></span> <span data-ttu-id="59ea9-126">Il s’agit du mode par défaut si aucun mode n’est spécifié.</span><span class="sxs-lookup"><span data-stu-id="59ea9-126">This is the default mode if no mode is specified.</span></span>

</dd> <dt>

<span data-ttu-id="59ea9-127"><span id="_download"></span><span id="_DOWNLOAD"></span>**/Download**</span><span class="sxs-lookup"><span data-stu-id="59ea9-127"><span id="_download"></span><span id="_DOWNLOAD"></span>**/download**</span></span>
</dt> <dd>

<span data-ttu-id="59ea9-128">Télécharge les documents importés référencés par le fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="59ea9-128">Downloads imported documents referenced by the configuration file.</span></span> <span data-ttu-id="59ea9-129">Ce paramètre est facultatif.</span><span class="sxs-lookup"><span data-stu-id="59ea9-129">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="59ea9-130"><span id="_gbc"></span><span id="_GBC"></span>**/gbc**</span><span class="sxs-lookup"><span data-stu-id="59ea9-130"><span id="_gbc"></span><span id="_GBC"></span>**/gbc**</span></span>
</dt> <dd>

<span data-ttu-id="59ea9-131">Ajoute des commentaires au code source qui indique que le code a été généré.</span><span class="sxs-lookup"><span data-stu-id="59ea9-131">Adds comments to the source code that indicates the code was generated.</span></span> <span data-ttu-id="59ea9-132">Ces commentaires sont précédés de l’expression « généré par ».</span><span class="sxs-lookup"><span data-stu-id="59ea9-132">These comments are prefixed with the phrase "Generated by".</span></span> <span data-ttu-id="59ea9-133">Ce paramètre est facultatif.</span><span class="sxs-lookup"><span data-stu-id="59ea9-133">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="59ea9-134"><span id="_outputroot_path"></span><span id="_OUTPUTROOT_PATH"></span>**/outputroot :**_chemin d’accès_</span><span class="sxs-lookup"><span data-stu-id="59ea9-134"><span id="_outputroot_path"></span><span id="_OUTPUTROOT_PATH"></span>**/outputroot:**_path_</span></span>
</dt> <dd>

<span data-ttu-id="59ea9-135">Emplacement de sortie pour les fichiers générés.</span><span class="sxs-lookup"><span data-stu-id="59ea9-135">The output location for generated files.</span></span> <span data-ttu-id="59ea9-136">le *chemin d’accès* peut être un chemin d’accès absolu ou relatif.</span><span class="sxs-lookup"><span data-stu-id="59ea9-136">*path* can be an absolute or relative path.</span></span> <span data-ttu-id="59ea9-137">Ce paramètre est facultatif.</span><span class="sxs-lookup"><span data-stu-id="59ea9-137">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="59ea9-138"><span id="_writeaccess_command"></span><span id="_WRITEACCESS_COMMAND"></span>**/WriteAccess :**_commande_</span><span class="sxs-lookup"><span data-stu-id="59ea9-138"><span id="_writeaccess_command"></span><span id="_WRITEACCESS_COMMAND"></span>**/writeaccess:**_command_</span></span>
</dt> <dd>

<span data-ttu-id="59ea9-139">Indique à WsdCodeGen d’exécuter la commande spécifiée avant de modifier les fichiers existants sur le disque.</span><span class="sxs-lookup"><span data-stu-id="59ea9-139">Directs WsdCodeGen to execute the specified command before it modifies any existing files on disk.</span></span> <span data-ttu-id="59ea9-140">Les fichiers de sortie qui sont identiques à ceux du disque ne reçoivent pas cette commande et ne sont pas écrits dans.</span><span class="sxs-lookup"><span data-stu-id="59ea9-140">Output files that are identical to those on disk will not receive this command, nor will they be written to.</span></span> <span data-ttu-id="59ea9-141">Si la commande contient la séquence « {0} », cette séquence sera remplacée par le nom du fichier à modifier.</span><span class="sxs-lookup"><span data-stu-id="59ea9-141">If the command contains the sequence "{0}", this sequence will be replaced with the filename of the file to be modified.</span></span> <span data-ttu-id="59ea9-142">Si ce n’est pas le cas, le nom de fichier est ajouté à la commande.</span><span class="sxs-lookup"><span data-stu-id="59ea9-142">If not, the filename will be appended to the command.</span></span>

<span data-ttu-id="59ea9-143">Exemples :</span><span class="sxs-lookup"><span data-stu-id="59ea9-143">Examples:</span></span>

<span data-ttu-id="59ea9-144">**/WriteAccess : "attrib-r"**</span><span class="sxs-lookup"><span data-stu-id="59ea9-144">**/writeaccess:"attrib -r"**</span></span>

<span data-ttu-id="59ea9-145">**/WriteAccess : "attrib-r {0} "**</span><span class="sxs-lookup"><span data-stu-id="59ea9-145">**/writeaccess:"attrib -r {0}"**</span></span>

<span data-ttu-id="59ea9-146">**/WriteAccess : «copier {0} .. \\ sauvegarde \\ »**</span><span class="sxs-lookup"><span data-stu-id="59ea9-146">**/writeaccess:"copy {0} ..\\backup\\"**</span></span>

</dd> <dt>

<span data-ttu-id="59ea9-147"><span id="ConfigFileName"></span><span id="configfilename"></span><span id="CONFIGFILENAME"></span>*Nomdefichierdeconfiguration*</span><span class="sxs-lookup"><span data-stu-id="59ea9-147"><span id="ConfigFileName"></span><span id="configfilename"></span><span id="CONFIGFILENAME"></span>*ConfigFileName*</span></span>
</dt> <dd>

<span data-ttu-id="59ea9-148">Nom du fichier de configuration à traiter avant de générer le code.</span><span class="sxs-lookup"><span data-stu-id="59ea9-148">The name of the configuration file to process before generating code.</span></span>

</dd> </dl>

## <a name="formatting-legend"></a><span data-ttu-id="59ea9-149">Légende de mise en forme</span><span class="sxs-lookup"><span data-stu-id="59ea9-149">Formatting Legend</span></span>



| <span data-ttu-id="59ea9-150">Format</span><span class="sxs-lookup"><span data-stu-id="59ea9-150">Format</span></span>                                                                    | <span data-ttu-id="59ea9-151">Signification</span><span class="sxs-lookup"><span data-stu-id="59ea9-151">Meaning</span></span>                                                 |
|---------------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="59ea9-152">*Italique*</span><span class="sxs-lookup"><span data-stu-id="59ea9-152">*Italic*</span></span>                                                                  | <span data-ttu-id="59ea9-153">Informations que l’utilisateur doit fournir</span><span class="sxs-lookup"><span data-stu-id="59ea9-153">Information that the user must provide</span></span>                  |
| <span data-ttu-id="59ea9-154">**Gras**</span><span class="sxs-lookup"><span data-stu-id="59ea9-154">**Bold**</span></span>                                                                  | <span data-ttu-id="59ea9-155">Éléments que l'utilisateur doit taper exactement comme indiqué</span><span class="sxs-lookup"><span data-stu-id="59ea9-155">Elements that the user must type exactly as shown</span></span>       |
| <span data-ttu-id="59ea9-156">Entre crochets ( \[ \] )</span><span class="sxs-lookup"><span data-stu-id="59ea9-156">Between brackets (\[\])</span></span>                                                   | <span data-ttu-id="59ea9-157">Éléments facultatifs</span><span class="sxs-lookup"><span data-stu-id="59ea9-157">Optional items</span></span>                                          |
| <span data-ttu-id="59ea9-158">Entre accolades ( {} ); choix séparés par une barre verticale ( \| ).</span><span class="sxs-lookup"><span data-stu-id="59ea9-158">Between braces ({}); choices separated by pipe (\|).</span></span> <span data-ttu-id="59ea9-159">Exemple : {même \| impair}</span><span class="sxs-lookup"><span data-stu-id="59ea9-159">Example: {even\|odd}</span></span> | <span data-ttu-id="59ea9-160">Ensemble de choix à partir duquel l’utilisateur ne doit en choisir qu’un seul</span><span class="sxs-lookup"><span data-stu-id="59ea9-160">Set of choices from which the user must choose only one</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="59ea9-161">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="59ea9-161">Requirements</span></span>



| <span data-ttu-id="59ea9-162">Condition requise</span><span class="sxs-lookup"><span data-stu-id="59ea9-162">Requirement</span></span> | <span data-ttu-id="59ea9-163">Valeur</span><span class="sxs-lookup"><span data-stu-id="59ea9-163">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="59ea9-164">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59ea9-164">Minimum supported client</span></span><br/> | <span data-ttu-id="59ea9-165">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="59ea9-165">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="59ea9-166">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59ea9-166">Minimum supported server</span></span><br/> | <span data-ttu-id="59ea9-167">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="59ea9-167">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="59ea9-168">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59ea9-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59ea9-169">Fichier de configuration WsdCodeGen</span><span class="sxs-lookup"><span data-stu-id="59ea9-169">WsdCodeGen Configuration File</span></span>](wsdcodegen-configuration-file.md)
</dt> <dt>

[<span data-ttu-id="59ea9-170">Utilisation de WsdCodeGen</span><span class="sxs-lookup"><span data-stu-id="59ea9-170">Using WsdCodeGen</span></span>](using-wsdcodegen.md)
</dt> </dl>

 

 




