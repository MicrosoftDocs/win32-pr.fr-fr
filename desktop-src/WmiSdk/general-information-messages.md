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
# <a name="general-information-messages"></a>Messages d’informations générales

Les messages d’informations suivants décrivent l’opération du compilateur.

<dl> <dt>

<span id="smi2smir__Version__version____MIB_definitions_compiled_from__file_name_"></span><span id="smi2smir__version__version____mib_definitions_compiled_from__file_name_"></span><span id="SMI2SMIR__VERSION__VERSION____MIB_DEFINITIONS_COMPILED_FROM__FILE_NAME_"></span>**Smi2smir : version <version \#> les définitions MIB compilées à partir de <file name>**
</dt> <dd>

Ce message apparaît au début de chaque compilation de fichier. Cela signifie que le fichier a peut-être été explicitement spécifié sur la ligne de commande par l’utilisateur, ou qu’il a peut-être été extrait par le compilateur à partir des répertoires Include du registre ou des répertoires Include mentionnés sur la ligne de commande.

</dd> <dt>

<span id="smi2smir__Syntax_check_failed_on__file_name_"></span><span id="smi2smir__syntax_check_failed_on__file_name_"></span><span id="SMI2SMIR__SYNTAX_CHECK_FAILED_ON__FILE_NAME_"></span>**Smi2smir : échec de la vérification de la syntaxe sur <file name>**
</dt> <dd>

Les messages d’erreur spécifiques qui précèdent ce message donnent la nature des erreurs de syntaxe.

</dd> <dt>

<span id="smi2smir__Semantic_check_failed_on__file_name_"></span><span id="smi2smir__semantic_check_failed_on__file_name_"></span><span id="SMI2SMIR__SEMANTIC_CHECK_FAILED_ON__FILE_NAME_"></span>**Smi2smir : échec de la vérification sémantique sur <file name>**
</dt> <dd>

Les messages d’erreur spécifiques qui précèdent ce message donnent la nature des erreurs sémantiques.

</dd> <dt>

<span id="smi2smir__Could_not_load__file_name__into_the_smir"></span><span id="smi2smir__could_not_load__file_name__into_the_smir"></span><span id="SMI2SMIR__COULD_NOT_LOAD__FILE_NAME__INTO_THE_SMIR"></span>**Smi2smir : impossible de charger <file name> dans le stockage SMIR**
</dt> <dd>

Échec de la vérification de la syntaxe ou de la sémantique sur le module, ou l’interaction stockage SMIR n’est pas terminée.

</dd> <dt>

<span id="smi2smir__Syntax_check_successful_on__file_name_"></span><span id="smi2smir__syntax_check_successful_on__file_name_"></span><span id="SMI2SMIR__SYNTAX_CHECK_SUCCESSFUL_ON__FILE_NAME_"></span>**Smi2smir : vérification de la syntaxe réussie sur <file name>**
</dt> <dd></dd> <dt>

<span id="smi2smir__Semantic_check_successful_on__file_name_"></span><span id="smi2smir__semantic_check_successful_on__file_name_"></span><span id="SMI2SMIR__SEMANTIC_CHECK_SUCCESSFUL_ON__FILE_NAME_"></span>**Smi2smir : vérification sémantique réussie sur <file name>**
</dt> <dd></dd> <dt>

<span id="smi2smir__Loaded__file_name__successfully_into_the_smir"></span><span id="smi2smir__loaded__file_name__successfully_into_the_smir"></span><span id="SMI2SMIR__LOADED__FILE_NAME__SUCCESSFULLY_INTO_THE_SMIR"></span>**Smi2smir : chargement <file name> réussi dans le stockage SMIR**
</dt> <dd></dd> <dt>

<span id="smi2smir__Could_not_resolve_one_or_more_symbols_in__module_name_"></span><span id="smi2smir__could_not_resolve_one_or_more_symbols_in__module_name_"></span><span id="SMI2SMIR__COULD_NOT_RESOLVE_ONE_OR_MORE_SYMBOLS_IN__MODULE_NAME_"></span>**Smi2smir : impossible de résoudre un ou plusieurs symboles dans <module name>**
</dt> <dd>

Les modules correspondant à un ou plusieurs des symboles importés dans le module spécifié sont introuvables ou n’ont pas pu être compilés.

</dd> <dt>

<span id="smi2smir__Could_not_connect_to_the_SMIR"></span><span id="smi2smir__could_not_connect_to_the_smir"></span><span id="SMI2SMIR__COULD_NOT_CONNECT_TO_THE_SMIR"></span>**Smi2smir : impossible de se connecter au stockage SMIR**
</dt> <dd>

Assurez-vous que Smir.dll existe, qu’il a été enregistré à l’aide de la commande regsvr32 et que le serveur Windows Management Instrumentation (WMI) est en cours d’exécution.

</dd> <dt>

<span id="smi2smir__Modules_in_the_SMIR___list_of_modules__1_on_each_line_"></span><span id="smi2smir__modules_in_the_smir___list_of_modules__1_on_each_line_"></span><span id="SMI2SMIR__MODULES_IN_THE_SMIR___LIST_OF_MODULES__1_ON_EACH_LINE_"></span>**Smi2smir : Modules dans le stockage SMIR : <liste de modules, 1 sur chaque ligne>**
</dt> <dd>

Il s’agit de la sortie du commutateur **/l** .

</dd> <dt>

<span id="smi2smir_Could_not_list_the_modules_in_the_SMIR"></span><span id="smi2smir_could_not_list_the_modules_in_the_smir"></span><span id="SMI2SMIR_COULD_NOT_LIST_THE_MODULES_IN_THE_SMIR"></span>**Smi2smir n’a pas pu répertorier les modules dans le stockage SMIR**
</dt> <dd>

Cela indique une défaillance du commutateur **/l** en raison de l’absence de connexion stockage SMIR.

</dd> <dt>

<span id="smi2smir__Deleted_module__module_name__successfully"></span><span id="smi2smir__deleted_module__module_name__successfully"></span><span id="SMI2SMIR__DELETED_MODULE__MODULE_NAME__SUCCESSFULLY"></span>**Smi2smir : module supprimé <module name> avec succès**
</dt> <dd>

Réussite du commutateur **/d** .

</dd> <dt>

<span id="smi2smir__Could_not_delete_module__module_name_"></span><span id="smi2smir__could_not_delete_module__module_name_"></span><span id="SMI2SMIR__COULD_NOT_DELETE_MODULE__MODULE_NAME_"></span>**Smi2smir : impossible de supprimer le module <module name>**
</dt> <dd>

Cela indique un échec du commutateur **/d** en raison de l’absence de connexion stockage SMIR.

</dd> <dt>

<span id="smi2smir__Deleted_all_the_modules_in_the_SMIR"></span><span id="smi2smir__deleted_all_the_modules_in_the_smir"></span><span id="SMI2SMIR__DELETED_ALL_THE_MODULES_IN_THE_SMIR"></span>**Smi2smir : suppression de tous les modules dans le stockage SMIR**
</dt> <dd>

Le commutateur **/p** a réussi.

</dd> <dt>

<span id="smi2smir__Could_not_delete_all_the_modules_in_the_SMIR"></span><span id="smi2smir__could_not_delete_all_the_modules_in_the_smir"></span><span id="SMI2SMIR__COULD_NOT_DELETE_ALL_THE_MODULES_IN_THE_SMIR"></span>**Smi2smir : impossible de supprimer tous les modules dans le stockage SMIR**
</dt> <dd>

Échec du commutateur **/p** en raison de l’absence de connexion stockage SMIR.

</dd> <dt>

<span id="smi2smir__Module__module_name__does_not_exist_in_the_SMIR"></span><span id="smi2smir__module__module_name__does_not_exist_in_the_smir"></span><span id="SMI2SMIR__MODULE__MODULE_NAME__DOES_NOT_EXIST_IN_THE_SMIR"></span>**Smi2smir : <module name> le module n’existe pas dans le stockage SMIR**
</dt> <dd>

Échec du commutateur **/d** , car le module spécifié n’est pas dans le stockage SMIR.

</dd> <dt>

<span id="smi2smir__Generated_MOF_successfully"></span><span id="smi2smir__generated_mof_successfully"></span><span id="SMI2SMIR__GENERATED_MOF_SUCCESSFULLY"></span>**Smi2smir : MOF généré avec succès**
</dt> <dd>

Le commutateur **/g** ou **/GC** a fonctionné correctement.

</dd> <dt>

<span id="smi2smir__Could_not_generate_MOF"></span><span id="smi2smir__could_not_generate_mof"></span><span id="SMI2SMIR__COULD_NOT_GENERATE_MOF"></span>**Smi2smir : impossible de générer MOF**
</dt> <dd>

Le commutateur **/g** ou **/GC** n’a pas pu fonctionner correctement en raison de l’absence de connexion stockage SMIR.

</dd> <dt>

<span id="smi2smir__Name_of_the_module___module_name_"></span><span id="smi2smir__name_of_the_module___module_name_"></span><span id="SMI2SMIR__NAME_OF_THE_MODULE___MODULE_NAME_"></span>**Smi2smir : nom du module : <module name>**
</dt> <dd>

Il s’agit de la sortie réussie du commutateur **/n** .

</dd> <dt>

<span id="smi2smir__Could_not_parse__file_name__successfully"></span><span id="smi2smir__could_not_parse__file_name__successfully"></span><span id="SMI2SMIR__COULD_NOT_PARSE__FILE_NAME__SUCCESSFULLY"></span>**Smi2smir : impossible d’analyser <file name> correctement**
</dt> <dd>

Cela indique l’échec du commutateur **/n** ou **/ni** , car le fichier spécifié n’est pas un fichier MIB valide.

</dd> <dt>

<span id="smi2smir__Processed__number__files_successfully"></span><span id="smi2smir__processed__number__files_successfully"></span><span id="SMI2SMIR__PROCESSED__NUMBER__FILES_SUCCESSFULLY"></span>**Smi2smir : <number> fichiers traités avec succès**
</dt> <dd>

Spécifie le nombre de fichiers qui ont été analysés avec succès lorsque le commutateur **/r** ou **/auto** a été utilisé.

</dd> <dt>

<span id="smi2smir__Repeated_files_in_the_input_for_module__module_name_._Only_the_file__file_name__will_be_compiled"></span><span id="smi2smir__repeated_files_in_the_input_for_module__module_name_._only_the_file__file_name__will_be_compiled"></span><span id="SMI2SMIR__REPEATED_FILES_IN_THE_INPUT_FOR_MODULE__MODULE_NAME_._ONLY_THE_FILE__FILE_NAME__WILL_BE_COMPILED"></span>**Smi2smir : fichiers répétés dans l’entrée pour le module <module name> . Seul le fichier <file name> sera compilé**
</dt> <dd>

L’utilisateur a explicitement spécifié plusieurs fichiers sur la ligne de commande, et au moins deux de ces fichiers ont le même module MIB.

</dd> <dt>

<span id="smi2smir__Added_directory__directory_name__to_the_registry"></span><span id="smi2smir__added_directory__directory_name__to_the_registry"></span><span id="SMI2SMIR__ADDED_DIRECTORY__DIRECTORY_NAME__TO_THE_REGISTRY"></span>**Smi2smir : ajout <directory name> d’un répertoire au registre**
</dt> <dd>

Réussite du commutateur **/PA** .

</dd> <dt>

<span id="smi2smir__Could_not_add_directory__directory_name__to_the_registry"></span><span id="smi2smir__could_not_add_directory__directory_name__to_the_registry"></span><span id="SMI2SMIR__COULD_NOT_ADD_DIRECTORY__DIRECTORY_NAME__TO_THE_REGISTRY"></span>**Smi2smir : impossible <directory name> d’ajouter le répertoire au registre**
</dt> <dd>

Échec du commutateur **/PA** , qui se produit uniquement en cas d’échec de l’API du Registre.

</dd> <dt>

<span id="smi2smir__Deleted_directory__directory_name__from_the_registry"></span><span id="smi2smir__deleted_directory__directory_name__from_the_registry"></span><span id="SMI2SMIR__DELETED_DIRECTORY__DIRECTORY_NAME__FROM_THE_REGISTRY"></span>**Smi2smir : répertoire supprimé <directory name> du Registre**
</dt> <dd>

Réussite du commutateur **/PD** .

</dd> <dt>

<span id="smi2smir__Could_not_delete__directory_name__from_the_registry"></span><span id="smi2smir__could_not_delete__directory_name__from_the_registry"></span><span id="SMI2SMIR__COULD_NOT_DELETE__DIRECTORY_NAME__FROM_THE_REGISTRY"></span>**Smi2smir : impossible de supprimer <directory name> du Registre**
</dt> <dd>

Échec du commutateur **/PD** . Le répertoire spécifié n’existe pas dans la liste des répertoires du Registre.

</dd> <dt>

<span id="smi2smir___file_name__is_not_a_valid_mib_file"></span><span id="SMI2SMIR___FILE_NAME__IS_NOT_A_VALID_MIB_FILE"></span>**Smi2smir : <file name> n’est pas un fichier MIB valide**
</dt> <dd>

Plusieurs fichiers ont été spécifiés sur la ligne de commande, dont l’un n’est pas un fichier MIB valide.

</dd> </dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Configuration de l’environnement WMI SNMP](setting-up-the-wmi-snmp-environment.md)
</dt> </dl>

 

 



