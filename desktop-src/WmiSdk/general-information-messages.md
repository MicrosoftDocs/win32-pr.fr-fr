---
description: Les messages d’informations suivants décrivent l’opération du compilateur.
ms.assetid: 838e598d-871d-4015-a372-4d94cacf8048
ms.tgt_platform: multiple
title: Messages d’informations générales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0997fad497299c7598fc1130edace49c20d7bb76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318941"
---
# <a name="general-information-messages"></a><span data-ttu-id="6f4fc-103">Messages d’informations générales</span><span class="sxs-lookup"><span data-stu-id="6f4fc-103">General Information Messages</span></span>

<span data-ttu-id="6f4fc-104">Les messages d’informations suivants décrivent l’opération du compilateur.</span><span class="sxs-lookup"><span data-stu-id="6f4fc-104">The following information messages describe the compiler operation.</span></span>

<dl> <dt>

<span data-ttu-id="6f4fc-105"><span id="smi2smir__Version__version____MIB_definitions_compiled_from__file_name_"></span><span id="smi2smir__version__version____mib_definitions_compiled_from__file_name_"></span><span id="SMI2SMIR__VERSION__VERSION____MIB_DEFINITIONS_COMPILED_FROM__FILE_NAME_"></span>**Smi2smir : version <version \#> les définitions MIB compilées à partir de <file name>**</span><span class="sxs-lookup"><span data-stu-id="6f4fc-105"><span id="smi2smir__Version__version____MIB_definitions_compiled_from__file_name_"></span><span id="smi2smir__version__version____mib_definitions_compiled_from__file_name_"></span><span id="SMI2SMIR__VERSION__VERSION____MIB_DEFINITIONS_COMPILED_FROM__FILE_NAME_"></span>**smi2smir: Version <version \#> MIB definitions compiled from <file name>**</span></span>
</dt> <dd>

<span data-ttu-id="6f4fc-106">Ce message apparaît au début de chaque compilation de fichier.</span><span class="sxs-lookup"><span data-stu-id="6f4fc-106">This message appears at the beginning of every file compilation.</span></span> <span data-ttu-id="6f4fc-107">Cela signifie que le fichier a peut-être été explicitement spécifié sur la ligne de commande par l’utilisateur, ou qu’il a peut-être été extrait par le compilateur à partir des répertoires Include du registre ou des répertoires Include mentionnés sur la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="6f4fc-107">It means the file may have been explicitly specified on the command line by the user, or it may have been pulled in by the compiler from the registry include directories or the include directories mentioned on the command line.</span></span>

</dd> <dt>

<span data-ttu-id="6f4fc-108"><span id="smi2smir__Syntax_check_failed_on__file_name_"></span><span id="smi2smir__syntax_check_failed_on__file_name_"></span><span id="SMI2SMIR__SYNTAX_CHECK_FAILED_ON__FILE_NAME_"></span>**Smi2smir : échec de la vérification de la syntaxe sur <file name>**</span><span class="sxs-lookup"><span data-stu-id="6f4fc-108"><span id="smi2smir__Syntax_check_failed_on__file_name_"></span><span id="smi2smir__syntax_check_failed_on__file_name_"></span><span id="SMI2SMIR__SYNTAX_CHECK_FAILED_ON__FILE_NAME_"></span>**smi2smir: Syntax check failed on <file name>**</span></span>
</dt> <dd>

<span data-ttu-id="6f4fc-109">Les messages d’erreur spécifiques qui précèdent ce message donnent la nature des erreurs de syntaxe.</span><span class="sxs-lookup"><span data-stu-id="6f4fc-109">The specific error messages that precede this message give the nature of the syntax errors.</span></span>

</dd> <dt>

<span data-ttu-id="6f4fc-110"><span id="smi2smir__Semantic_check_failed_on__file_name_"></span><span id="smi2smir__semantic_check_failed_on__file_name_"></span><span id="SMI2SMIR__SEMANTIC_CHECK_FAILED_ON__FILE_NAME_"></span>**Smi2smir : échec de la vérification sémantique sur <file name>**</span><span class="sxs-lookup"><span data-stu-id="6f4fc-110"><span id="smi2smir__Semantic_check_failed_on__file_name_"></span><span id="smi2smir__semantic_check_failed_on__file_name_"></span><span id="SMI2SMIR__SEMANTIC_CHECK_FAILED_ON__FILE_NAME_"></span>**smi2smir: Semantic check failed on <file name>**</span></span>
</dt> <dd>

<span data-ttu-id="6f4fc-111">Les messages d’erreur spécifiques qui précèdent ce message donnent la nature des erreurs sémantiques.</span><span class="sxs-lookup"><span data-stu-id="6f4fc-111">The specific error messages that precede this message give the nature of the semantic errors.</span></span>

</dd> <dt>

<span data-ttu-id="6f4fc-112"><span id="smi2smir__Could_not_load__file_name__into_the_smir"></span><span id="smi2smir__could_not_load__file_name__into_the_smir"></span><span id="SMI2SMIR__COULD_NOT_LOAD__FILE_NAME__INTO_THE_SMIR"></span>**Smi2smir : impossible de charger <file name> dans le stockage SMIR**</span><span class="sxs-lookup"><span data-stu-id="6f4fc-112"><span id="smi2smir__Could_not_load__file_name__into_the_smir"></span><span id="smi2smir__could_not_load__file_name__into_the_smir"></span><span id="SMI2SMIR__COULD_NOT_LOAD__FILE_NAME__INTO_THE_SMIR"></span>**smi2smir: Could not load <file name> into the smir**</span></span>
</dt> <dd>

<span data-ttu-id="6f4fc-113">Échec de la vérification de la syntaxe ou de la sémantique sur le module, ou l’interaction stockage SMIR n’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="6f4fc-113">Syntax or semantic check failed on the module, or SMIR interaction was not complete.</span></span>

</dd> <dt>

<span data-ttu-id="6f4fc-114"><span id="smi2smir__Syntax_check_successful_on__file_name_"></span><span id="smi2smir__syntax_check_successful_on__file_name_"></span><span id="SMI2SMIR__SYNTAX_CHECK_SUCCESSFUL_ON__FILE_NAME_"></span>**Smi2smir : vérification de la syntaxe réussie sur <file name>**</span><span class="sxs-lookup"><span data-stu-id="6f4fc-114"><span id="smi2smir__Syntax_check_successful_on__file_name_"></span><span id="smi2smir__syntax_check_successful_on__file_name_"></span><span id="SMI2SMIR__SYNTAX_CHECK_SUCCESSFUL_ON__FILE_NAME_"></span>**smi2smir: Syntax check successful on <file name>**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="6f4fc-115"><span id="smi2smir__Semantic_check_successful_on__file_name_"></span><span id="smi2smir__semantic_check_successful_on__file_name_"></span><span id="SMI2SMIR__SEMANTIC_CHECK_SUCCESSFUL_ON__FILE_NAME_"></span>**Smi2smir : vérification sémantique réussie sur <file name>**</span><span class="sxs-lookup"><span data-stu-id="6f4fc-115"><span id="smi2smir__Semantic_check_successful_on__file_name_"></span><span id="smi2smir__semantic_check_successful_on__file_name_"></span><span id="SMI2SMIR__SEMANTIC_CHECK_SUCCESSFUL_ON__FILE_NAME_"></span>**smi2smir: Semantic check successful on <file name>**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="6f4fc-116"><span id="smi2smir__Loaded__file_name__successfully_into_the_smir"></span><span id="smi2smir__loaded__file_name__successfully_into_the_smir"></span><span id="SMI2SMIR__LOADED__FILE_NAME__SUCCESSFULLY_INTO_THE_SMIR"></span>**Smi2smir : chargement <file name> réussi dans le stockage SMIR**</span><span class="sxs-lookup"><span data-stu-id="6f4fc-116"><span id="smi2smir__Loaded__file_name__successfully_into_the_smir"></span><span id="smi2smir__loaded__file_name__successfully_into_the_smir"></span><span id="SMI2SMIR__LOADED__FILE_NAME__SUCCESSFULLY_INTO_THE_SMIR"></span>**smi2smir: Loaded <file name> successfully into the smir**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="6f4fc-117"><span id="smi2smir__Could_not_resolve_one_or_more_symbols_in__module_name_"></span><span id="smi2smir__could_not_resolve_one_or_more_symbols_in__module_name_"></span><span id="SMI2SMIR__COULD_NOT_RESOLVE_ONE_OR_MORE_SYMBOLS_IN__MODULE_NAME_"></span>**Smi2smir : impossible de résoudre un ou plusieurs symboles dans <module name>**</span><span class="sxs-lookup"><span data-stu-id="6f4fc-117"><span id="smi2smir__Could_not_resolve_one_or_more_symbols_in__module_name_"></span><span id="smi2smir__could_not_resolve_one_or_more_symbols_in__module_name_"></span><span id="SMI2SMIR__COULD_NOT_RESOLVE_ONE_OR_MORE_SYMBOLS_IN__MODULE_NAME_"></span>**smi2smir: Could not resolve one or more symbols in <module name>**</span></span>
</dt> <dd>

<span data-ttu-id="6f4fc-118">Les modules correspondant à un ou plusieurs des symboles importés dans le module spécifié sont introuvables ou n’ont pas pu être compilés.</span><span class="sxs-lookup"><span data-stu-id="6f4fc-118">The modules corresponding to one or more of the imported symbols in the specified module were not found or could not be compiled.</span></span>

</dd> <dt>

<span data-ttu-id="6f4fc-119"><span id="smi2smir__Could_not_connect_to_the_SMIR"></span><span id="smi2smir__could_not_connect_to_the_smir"></span><span id="SMI2SMIR__COULD_NOT_CONNECT_TO_THE_SMIR"></span>**Smi2smir : impossible de se connecter au stockage SMIR**</span><span class="sxs-lookup"><span data-stu-id="6f4fc-119"><span id="smi2smir__Could_not_connect_to_the_SMIR"></span><span id="smi2smir__could_not_connect_to_the_smir"></span><span id="SMI2SMIR__COULD_NOT_CONNECT_TO_THE_SMIR"></span>**smi2smir: Could not connect to the SMIR**</span></span>
</dt> <dd>

<span data-ttu-id="6f4fc-120">Assurez-vous que Smir.dll existe, qu’il a été enregistré à l’aide de la commande regsvr32 et que le serveur Windows Management Instrumentation (WMI) est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="6f4fc-120">Ensure that Smir.dll exists, has been registered using the regsvr32 command, and that the Windows Management Instrumentation (WMI) server is up and running.</span></span>

</dd> <dt>

<span data-ttu-id="6f4fc-121"><span id="smi2smir__Modules_in_the_SMIR___list_of_modules__1_on_each_line_"></span><span id="smi2smir__modules_in_the_smir___list_of_modules__1_on_each_line_"></span><span id="SMI2SMIR__MODULES_IN_THE_SMIR___LIST_OF_MODULES__1_ON_EACH_LINE_"></span>**Smi2smir : Modules dans le stockage SMIR : <liste de modules, 1 sur chaque ligne>**</span><span class="sxs-lookup"><span data-stu-id="6f4fc-121"><span id="smi2smir__Modules_in_the_SMIR___list_of_modules__1_on_each_line_"></span><span id="smi2smir__modules_in_the_smir___list_of_modules__1_on_each_line_"></span><span id="SMI2SMIR__MODULES_IN_THE_SMIR___LIST_OF_MODULES__1_ON_EACH_LINE_"></span>**smi2smir: Modules in the SMIR: <list of modules, 1 on each line>**</span></span>
</dt> <dd>

<span data-ttu-id="6f4fc-122">Il s’agit de la sortie du commutateur **/l** .</span><span class="sxs-lookup"><span data-stu-id="6f4fc-122">This is the output of the **/l** switch.</span></span>

</dd> <dt>

<span data-ttu-id="6f4fc-123"><span id="smi2smir_Could_not_list_the_modules_in_the_SMIR"></span><span id="smi2smir_could_not_list_the_modules_in_the_smir"></span><span id="SMI2SMIR_COULD_NOT_LIST_THE_MODULES_IN_THE_SMIR"></span>**Smi2smir n’a pas pu répertorier les modules dans le stockage SMIR**</span><span class="sxs-lookup"><span data-stu-id="6f4fc-123"><span id="smi2smir_Could_not_list_the_modules_in_the_SMIR"></span><span id="smi2smir_could_not_list_the_modules_in_the_smir"></span><span id="SMI2SMIR_COULD_NOT_LIST_THE_MODULES_IN_THE_SMIR"></span>**smi2smir Could not list the modules in the SMIR**</span></span>
</dt> <dd>

<span data-ttu-id="6f4fc-124">Cela indique une défaillance du commutateur **/l** en raison de l’absence de connexion stockage SMIR.</span><span class="sxs-lookup"><span data-stu-id="6f4fc-124">This indicates a failure of the **/l** switch due to no SMIR connection.</span></span>

</dd> <dt>

<span data-ttu-id="6f4fc-125"><span id="smi2smir__Deleted_module__module_name__successfully"></span><span id="smi2smir__deleted_module__module_name__successfully"></span><span id="SMI2SMIR__DELETED_MODULE__MODULE_NAME__SUCCESSFULLY"></span>**Smi2smir : module supprimé <module name> avec succès**</span><span class="sxs-lookup"><span data-stu-id="6f4fc-125"><span id="smi2smir__Deleted_module__module_name__successfully"></span><span id="smi2smir__deleted_module__module_name__successfully"></span><span id="SMI2SMIR__DELETED_MODULE__MODULE_NAME__SUCCESSFULLY"></span>**smi2smir: Deleted module <module name> successfully**</span></span>
</dt> <dd>

<span data-ttu-id="6f4fc-126">Réussite du commutateur **/d** .</span><span class="sxs-lookup"><span data-stu-id="6f4fc-126">The **/d** switch succeeded.</span></span>

</dd> <dt>

<span data-ttu-id="6f4fc-127"><span id="smi2smir__Could_not_delete_module__module_name_"></span><span id="smi2smir__could_not_delete_module__module_name_"></span><span id="SMI2SMIR__COULD_NOT_DELETE_MODULE__MODULE_NAME_"></span>**Smi2smir : impossible de supprimer le module <module name>**</span><span class="sxs-lookup"><span data-stu-id="6f4fc-127"><span id="smi2smir__Could_not_delete_module__module_name_"></span><span id="smi2smir__could_not_delete_module__module_name_"></span><span id="SMI2SMIR__COULD_NOT_DELETE_MODULE__MODULE_NAME_"></span>**smi2smir: Could not delete module <module name>**</span></span>
</dt> <dd>

<span data-ttu-id="6f4fc-128">Cela indique un échec du commutateur **/d** en raison de l’absence de connexion stockage SMIR.</span><span class="sxs-lookup"><span data-stu-id="6f4fc-128">This indicates a failure of the **/d** switch due to no SMIR connection.</span></span>

</dd> <dt>

<span data-ttu-id="6f4fc-129"><span id="smi2smir__Deleted_all_the_modules_in_the_SMIR"></span><span id="smi2smir__deleted_all_the_modules_in_the_smir"></span><span id="SMI2SMIR__DELETED_ALL_THE_MODULES_IN_THE_SMIR"></span>**Smi2smir : suppression de tous les modules dans le stockage SMIR**</span><span class="sxs-lookup"><span data-stu-id="6f4fc-129"><span id="smi2smir__Deleted_all_the_modules_in_the_SMIR"></span><span id="smi2smir__deleted_all_the_modules_in_the_smir"></span><span id="SMI2SMIR__DELETED_ALL_THE_MODULES_IN_THE_SMIR"></span>**smi2smir: Deleted all the modules in the SMIR**</span></span>
</dt> <dd>

<span data-ttu-id="6f4fc-130">Le commutateur **/p** a réussi.</span><span class="sxs-lookup"><span data-stu-id="6f4fc-130">The **/p** switch succeeded.</span></span>

</dd> <dt>

<span data-ttu-id="6f4fc-131"><span id="smi2smir__Could_not_delete_all_the_modules_in_the_SMIR"></span><span id="smi2smir__could_not_delete_all_the_modules_in_the_smir"></span><span id="SMI2SMIR__COULD_NOT_DELETE_ALL_THE_MODULES_IN_THE_SMIR"></span>**Smi2smir : impossible de supprimer tous les modules dans le stockage SMIR**</span><span class="sxs-lookup"><span data-stu-id="6f4fc-131"><span id="smi2smir__Could_not_delete_all_the_modules_in_the_SMIR"></span><span id="smi2smir__could_not_delete_all_the_modules_in_the_smir"></span><span id="SMI2SMIR__COULD_NOT_DELETE_ALL_THE_MODULES_IN_THE_SMIR"></span>**smi2smir: Could not delete all the modules in the SMIR**</span></span>
</dt> <dd>

<span data-ttu-id="6f4fc-132">Échec du commutateur **/p** en raison de l’absence de connexion stockage SMIR.</span><span class="sxs-lookup"><span data-stu-id="6f4fc-132">The **/p** switch failed because there is no SMIR connection.</span></span>

</dd> <dt>

<span data-ttu-id="6f4fc-133"><span id="smi2smir__Module__module_name__does_not_exist_in_the_SMIR"></span><span id="smi2smir__module__module_name__does_not_exist_in_the_smir"></span><span id="SMI2SMIR__MODULE__MODULE_NAME__DOES_NOT_EXIST_IN_THE_SMIR"></span>**Smi2smir : <module name> le module n’existe pas dans le stockage SMIR**</span><span class="sxs-lookup"><span data-stu-id="6f4fc-133"><span id="smi2smir__Module__module_name__does_not_exist_in_the_SMIR"></span><span id="smi2smir__module__module_name__does_not_exist_in_the_smir"></span><span id="SMI2SMIR__MODULE__MODULE_NAME__DOES_NOT_EXIST_IN_THE_SMIR"></span>**smi2smir: Module <module name> does not exist in the SMIR**</span></span>
</dt> <dd>

<span data-ttu-id="6f4fc-134">Échec du commutateur **/d** , car le module spécifié n’est pas dans le stockage SMIR.</span><span class="sxs-lookup"><span data-stu-id="6f4fc-134">The **/d** switch failed because the specified module is not in the SMIR.</span></span>

</dd> <dt>

<span data-ttu-id="6f4fc-135"><span id="smi2smir__Generated_MOF_successfully"></span><span id="smi2smir__generated_mof_successfully"></span><span id="SMI2SMIR__GENERATED_MOF_SUCCESSFULLY"></span>**Smi2smir : MOF généré avec succès**</span><span class="sxs-lookup"><span data-stu-id="6f4fc-135"><span id="smi2smir__Generated_MOF_successfully"></span><span id="smi2smir__generated_mof_successfully"></span><span id="SMI2SMIR__GENERATED_MOF_SUCCESSFULLY"></span>**smi2smir: Generated MOF successfully**</span></span>
</dt> <dd>

<span data-ttu-id="6f4fc-136">Le commutateur **/g** ou **/GC** a fonctionné correctement.</span><span class="sxs-lookup"><span data-stu-id="6f4fc-136">The **/g** or **/gc** switch worked successfully.</span></span>

</dd> <dt>

<span data-ttu-id="6f4fc-137"><span id="smi2smir__Could_not_generate_MOF"></span><span id="smi2smir__could_not_generate_mof"></span><span id="SMI2SMIR__COULD_NOT_GENERATE_MOF"></span>**Smi2smir : impossible de générer MOF**</span><span class="sxs-lookup"><span data-stu-id="6f4fc-137"><span id="smi2smir__Could_not_generate_MOF"></span><span id="smi2smir__could_not_generate_mof"></span><span id="SMI2SMIR__COULD_NOT_GENERATE_MOF"></span>**smi2smir: Could not generate MOF**</span></span>
</dt> <dd>

<span data-ttu-id="6f4fc-138">Le commutateur **/g** ou **/GC** n’a pas pu fonctionner correctement en raison de l’absence de connexion stockage SMIR.</span><span class="sxs-lookup"><span data-stu-id="6f4fc-138">The **/g** or **/gc** switch did not work successfully due to no SMIR connection.</span></span>

</dd> <dt>

<span data-ttu-id="6f4fc-139"><span id="smi2smir__Name_of_the_module___module_name_"></span><span id="smi2smir__name_of_the_module___module_name_"></span><span id="SMI2SMIR__NAME_OF_THE_MODULE___MODULE_NAME_"></span>**Smi2smir : nom du module : <module name>**</span><span class="sxs-lookup"><span data-stu-id="6f4fc-139"><span id="smi2smir__Name_of_the_module___module_name_"></span><span id="smi2smir__name_of_the_module___module_name_"></span><span id="SMI2SMIR__NAME_OF_THE_MODULE___MODULE_NAME_"></span>**smi2smir: Name of the module: <module name>**</span></span>
</dt> <dd>

<span data-ttu-id="6f4fc-140">Il s’agit de la sortie réussie du commutateur **/n** .</span><span class="sxs-lookup"><span data-stu-id="6f4fc-140">This is the successful output of the **/n** switch.</span></span>

</dd> <dt>

<span data-ttu-id="6f4fc-141"><span id="smi2smir__Could_not_parse__file_name__successfully"></span><span id="smi2smir__could_not_parse__file_name__successfully"></span><span id="SMI2SMIR__COULD_NOT_PARSE__FILE_NAME__SUCCESSFULLY"></span>**Smi2smir : impossible d’analyser <file name> correctement**</span><span class="sxs-lookup"><span data-stu-id="6f4fc-141"><span id="smi2smir__Could_not_parse__file_name__successfully"></span><span id="smi2smir__could_not_parse__file_name__successfully"></span><span id="SMI2SMIR__COULD_NOT_PARSE__FILE_NAME__SUCCESSFULLY"></span>**smi2smir: Could not parse <file name> successfully**</span></span>
</dt> <dd>

<span data-ttu-id="6f4fc-142">Cela indique l’échec du commutateur **/n** ou **/ni** , car le fichier spécifié n’est pas un fichier MIB valide.</span><span class="sxs-lookup"><span data-stu-id="6f4fc-142">This indicates failure of the **/n** or **/ni** switch because the specified file is not a valid MIB file.</span></span>

</dd> <dt>

<span data-ttu-id="6f4fc-143"><span id="smi2smir__Processed__number__files_successfully"></span><span id="smi2smir__processed__number__files_successfully"></span><span id="SMI2SMIR__PROCESSED__NUMBER__FILES_SUCCESSFULLY"></span>**Smi2smir : <number> fichiers traités avec succès**</span><span class="sxs-lookup"><span data-stu-id="6f4fc-143"><span id="smi2smir__Processed__number__files_successfully"></span><span id="smi2smir__processed__number__files_successfully"></span><span id="SMI2SMIR__PROCESSED__NUMBER__FILES_SUCCESSFULLY"></span>**smi2smir: Processed <number> files successfully**</span></span>
</dt> <dd>

<span data-ttu-id="6f4fc-144">Spécifie le nombre de fichiers qui ont été analysés avec succès lorsque le commutateur **/r** ou **/auto** a été utilisé.</span><span class="sxs-lookup"><span data-stu-id="6f4fc-144">This specifies the number of files that were successfully parsed when the **/r** or the **/auto** switch were used.</span></span>

</dd> <dt>

<span data-ttu-id="6f4fc-145"><span id="smi2smir__Repeated_files_in_the_input_for_module__module_name_._Only_the_file__file_name__will_be_compiled"></span><span id="smi2smir__repeated_files_in_the_input_for_module__module_name_._only_the_file__file_name__will_be_compiled"></span><span id="SMI2SMIR__REPEATED_FILES_IN_THE_INPUT_FOR_MODULE__MODULE_NAME_._ONLY_THE_FILE__FILE_NAME__WILL_BE_COMPILED"></span>**Smi2smir : fichiers répétés dans l’entrée pour le module <module name> . Seul le fichier <file name> sera compilé**</span><span class="sxs-lookup"><span data-stu-id="6f4fc-145"><span id="smi2smir__Repeated_files_in_the_input_for_module__module_name_._Only_the_file__file_name__will_be_compiled"></span><span id="smi2smir__repeated_files_in_the_input_for_module__module_name_._only_the_file__file_name__will_be_compiled"></span><span id="SMI2SMIR__REPEATED_FILES_IN_THE_INPUT_FOR_MODULE__MODULE_NAME_._ONLY_THE_FILE__FILE_NAME__WILL_BE_COMPILED"></span>**smi2smir: Repeated files in the input for module <module name>. Only the file <file name> will be compiled**</span></span>
</dt> <dd>

<span data-ttu-id="6f4fc-146">L’utilisateur a explicitement spécifié plusieurs fichiers sur la ligne de commande, et au moins deux de ces fichiers ont le même module MIB.</span><span class="sxs-lookup"><span data-stu-id="6f4fc-146">The user has explicitly specified more than one file on the command line, and two or more of these files have the same MIB module.</span></span>

</dd> <dt>

<span data-ttu-id="6f4fc-147"><span id="smi2smir__Added_directory__directory_name__to_the_registry"></span><span id="smi2smir__added_directory__directory_name__to_the_registry"></span><span id="SMI2SMIR__ADDED_DIRECTORY__DIRECTORY_NAME__TO_THE_REGISTRY"></span>**Smi2smir : ajout <directory name> d’un répertoire au registre**</span><span class="sxs-lookup"><span data-stu-id="6f4fc-147"><span id="smi2smir__Added_directory__directory_name__to_the_registry"></span><span id="smi2smir__added_directory__directory_name__to_the_registry"></span><span id="SMI2SMIR__ADDED_DIRECTORY__DIRECTORY_NAME__TO_THE_REGISTRY"></span>**smi2smir: Added directory <directory name> to the registry**</span></span>
</dt> <dd>

<span data-ttu-id="6f4fc-148">Réussite du commutateur **/PA** .</span><span class="sxs-lookup"><span data-stu-id="6f4fc-148">Success of the **/pa** switch.</span></span>

</dd> <dt>

<span data-ttu-id="6f4fc-149"><span id="smi2smir__Could_not_add_directory__directory_name__to_the_registry"></span><span id="smi2smir__could_not_add_directory__directory_name__to_the_registry"></span><span id="SMI2SMIR__COULD_NOT_ADD_DIRECTORY__DIRECTORY_NAME__TO_THE_REGISTRY"></span>**Smi2smir : impossible <directory name> d’ajouter le répertoire au registre**</span><span class="sxs-lookup"><span data-stu-id="6f4fc-149"><span id="smi2smir__Could_not_add_directory__directory_name__to_the_registry"></span><span id="smi2smir__could_not_add_directory__directory_name__to_the_registry"></span><span id="SMI2SMIR__COULD_NOT_ADD_DIRECTORY__DIRECTORY_NAME__TO_THE_REGISTRY"></span>**smi2smir: Could not add directory <directory name> to the registry**</span></span>
</dt> <dd>

<span data-ttu-id="6f4fc-150">Échec du commutateur **/PA** , qui se produit uniquement en cas d’échec de l’API du Registre.</span><span class="sxs-lookup"><span data-stu-id="6f4fc-150">Failure of the **/pa** switch, which happens only if the registry API fails.</span></span>

</dd> <dt>

<span data-ttu-id="6f4fc-151"><span id="smi2smir__Deleted_directory__directory_name__from_the_registry"></span><span id="smi2smir__deleted_directory__directory_name__from_the_registry"></span><span id="SMI2SMIR__DELETED_DIRECTORY__DIRECTORY_NAME__FROM_THE_REGISTRY"></span>**Smi2smir : répertoire supprimé <directory name> du Registre**</span><span class="sxs-lookup"><span data-stu-id="6f4fc-151"><span id="smi2smir__Deleted_directory__directory_name__from_the_registry"></span><span id="smi2smir__deleted_directory__directory_name__from_the_registry"></span><span id="SMI2SMIR__DELETED_DIRECTORY__DIRECTORY_NAME__FROM_THE_REGISTRY"></span>**smi2smir: Deleted directory <directory name> from the registry**</span></span>
</dt> <dd>

<span data-ttu-id="6f4fc-152">Réussite du commutateur **/PD** .</span><span class="sxs-lookup"><span data-stu-id="6f4fc-152">Success of the **/pd** switch.</span></span>

</dd> <dt>

<span data-ttu-id="6f4fc-153"><span id="smi2smir__Could_not_delete__directory_name__from_the_registry"></span><span id="smi2smir__could_not_delete__directory_name__from_the_registry"></span><span id="SMI2SMIR__COULD_NOT_DELETE__DIRECTORY_NAME__FROM_THE_REGISTRY"></span>**Smi2smir : impossible de supprimer <directory name> du Registre**</span><span class="sxs-lookup"><span data-stu-id="6f4fc-153"><span id="smi2smir__Could_not_delete__directory_name__from_the_registry"></span><span id="smi2smir__could_not_delete__directory_name__from_the_registry"></span><span id="SMI2SMIR__COULD_NOT_DELETE__DIRECTORY_NAME__FROM_THE_REGISTRY"></span>**smi2smir: Could not delete <directory name> from the registry**</span></span>
</dt> <dd>

<span data-ttu-id="6f4fc-154">Échec du commutateur **/PD** .</span><span class="sxs-lookup"><span data-stu-id="6f4fc-154">Failure of the **/pd** switch.</span></span> <span data-ttu-id="6f4fc-155">Le répertoire spécifié n’existe pas dans la liste des répertoires du Registre.</span><span class="sxs-lookup"><span data-stu-id="6f4fc-155">The specified directory does not exist in the list of directories in the registry.</span></span>

</dd> <dt>

<span data-ttu-id="6f4fc-156"><span id="smi2smir___file_name__is_not_a_valid_mib_file"></span><span id="SMI2SMIR___FILE_NAME__IS_NOT_A_VALID_MIB_FILE"></span>**Smi2smir : <file name> n’est pas un fichier MIB valide**</span><span class="sxs-lookup"><span data-stu-id="6f4fc-156"><span id="smi2smir___file_name__is_not_a_valid_mib_file"></span><span id="SMI2SMIR___FILE_NAME__IS_NOT_A_VALID_MIB_FILE"></span>**smi2smir: <file name> is not a valid mib file**</span></span>
</dt> <dd>

<span data-ttu-id="6f4fc-157">Plusieurs fichiers ont été spécifiés sur la ligne de commande, dont l’un n’est pas un fichier MIB valide.</span><span class="sxs-lookup"><span data-stu-id="6f4fc-157">More than one file has been specified on the command line, one of which is not a valid MIB file.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="6f4fc-158">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6f4fc-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f4fc-159">Configuration de l’environnement WMI SNMP</span><span class="sxs-lookup"><span data-stu-id="6f4fc-159">Setting up the WMI SNMP Environment</span></span>](setting-up-the-wmi-snmp-environment.md)
</dt> </dl>

 

 



