---
title: Erreurs du compilateur
description: Liste des messages d’erreur générés pendant la compilation MIDL.
ms.assetid: 492eacdd-6bd1-49df-9112-3765f6c05f34
keywords:
- Erreurs MIDL, erreurs du compilateur
topic_type:
- apiref
api_name:
- Compiler Errors
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 56b610025d3012446daa7938e2f37c2efcf6c2ddb7edd2ee545db0a179953fad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067451"
---
# <a name="compiler-errors"></a>Erreurs du compilateur

Les messages d’erreur suivants sont générés au cours de la compilation MIDL :



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Code de retour</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="MIDL2000"></span><span id="midl2000"></span><dl> <dt><strong>MIDL2000</strong></dt> </dl></td>
<td><dl> <dt><span id="must_specify__c_ext_for_abstract_declarators"></span><span id="MUST_SPECIFY__C_EXT_FOR_ABSTRACT_DECLARATORS"></span>doit spécifier/c_ext pour les déclarateurs abstraits</dt> <dd> Les déclarateurs abstraits représentent une extension Microsoft de RPC et ne sont pas définis dans DCE RPC. Par conséquent, si votre fichier contient des déclarateurs abstraits, vous ne pouvez pas compiler avec le commutateur <a href="-osf.md"><strong>/OSF</strong></a> , qui applique une compatibilité DCE stricte. Les versions de MIDL 3,0 et ultérieures utilisent le commutateur <a href="-c-ext.md"><strong>/c_ext</strong></a> comme valeur par défaut ; le commutateur <strong>/OSF</strong> désactive le commutateur <strong>/c_ext</strong> . Pour plus d’informations sur les déclarateurs abstraits, consultez <a href="/windows/desktop/Rpc/the-acf-body">le corps de CCP</a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2001"></span><span id="midl2001"></span><dl> <dt><strong>MIDL2001</strong></dt> </dl></td>
<td><dl> <dt><span id="instantiation_of_data_is_illegal__you_must_use__extern__or__static_"></span><span id="INSTANTIATION_OF_DATA_IS_ILLEGAL__YOU_MUST_USE__EXTERN__OR__STATIC_"></span>l’instanciation des données n’est pas conforme ; vous devez utiliser &quot; extern &quot; ou &quot; static&quot;</dt> <dd> La déclaration et l’initialisation dans le fichier IDL ne sont pas compatibles avec la RPC DCE. Cette fonctionnalité est une extension Microsoft qui n’est pas disponible quand vous compilez en mode compatible DCE (<a href="-osf.md"><strong>/OSF</strong></a>).<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2002"></span><span id="midl2002"></span><dl> <dt><strong>MIDL2002</strong></dt> </dl></td>
<td><dl> <dt><span id="compiler_stack_overflow"></span><span id="COMPILER_STACK_OVERFLOW"></span>dépassement de capacité de la pile du compilateur</dt> <dd> Le compilateur a manqué d’espace de pile lors du traitement du fichier IDL. Ce problème peut se produire lorsque le compilateur traite une déclaration ou une expression complexe. Pour résoudre le problème, simplifiez la déclaration ou l’expression complexe.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2003"></span><span id="midl2003"></span><dl> <dt><strong>MIDL2003</strong></dt> </dl></td>
<td><dl> <dt><span id="redefinition"></span><span id="REDEFINITION"></span>redéfinition</dt> <dd> Ce message d’erreur peut s’afficher dans les circonstances suivantes : un type a été redéfini ; un prototype de procédure a été redéfini ; un membre d’une structure ou d’une Union du même nom existe déjà ; un paramètre du même nom existe déjà dans le prototype.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2004"></span><span id="midl2004"></span><dl> <dt><strong>MIDL2004</strong></dt> </dl></td>
<td><dl> <dt><span id="_auto_handle__binding_will_be_used"></span><span id="_AUTO_HANDLE__BINDING_WILL_BE_USED"></span>[auto_handle] la liaison sera utilisée</dt> <dd> Aucun type de handle n’a été défini comme type de handle par défaut. Le compilateur suppose qu’un handle automatique sera utilisé comme handle de liaison pour la procédure spécifiée.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2005"></span><span id="midl2005"></span><dl> <dt><strong>MIDL2005</strong></dt> </dl></td>
<td><dl> <dt><span id="out_of_memory"></span><span id="OUT_OF_MEMORY"></span>mémoire insuffisante</dt> <dd> Le compilateur a manqué de mémoire pendant la compilation. Réduisez la taille ou la complexité du fichier IDL ou allouez davantage de mémoire au processus.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2006"></span><span id="midl2006"></span><dl> <dt><strong>MIDL2006</strong></dt> </dl></td>
<td><dl> <dt><span id="recursive_definition"></span><span id="RECURSIVE_DEFINITION"></span>définition récursive</dt> <dd> Une structure ou une Union a été définie de manière récursive. Cette erreur peut se produire lorsqu’une spécification de pointeur dans une définition de structure imbriquée est manquée.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2007"></span><span id="midl2007"></span><dl> <dt><strong>MIDL2007</strong></dt> </dl></td>
<td><dl> <dt><span id="import_ignored__file_already_imported"></span><span id="IMPORT_IGNORED__FILE_ALREADY_IMPORTED"></span>importation ignorée ; fichier déjà importé</dt> <dd> L’importation d’un fichier IDL est une opération idempotent. L’inclusion plus d’une fois n’a aucun effet. Toutes les opérations d’importation sauf la première sont ignorées.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2008"></span><span id="midl2008"></span><dl> <dt><strong>MIDL2008</strong></dt> </dl></td>
<td><dl> <dt><span id="sparse_enums_require__c_ext_or__ms_ext"></span><span id="SPARSE_ENUMS_REQUIRE__C_EXT_OR__MS_EXT"></span>les énumérations éparses requièrent/c_ext ou/ms_ext</dt> <dd> L’attribution de valeurs aux constantes d’énumération n’est pas compatible avec la RPC DCE. Si vous souhaitez utiliser les extensions Microsoft de MIDL qui permettent d’assigner des valeurs à des constantes d’énumération, vous ne pouvez pas compiler avec le commutateur <a href="-osf.md"><strong>/OSF</strong></a> , qui applique une compatibilité DCE stricte. Les versions de MIDL 3,0 et ultérieures utilisent les commutateurs <a href="-c-ext.md"><strong>/c_ext</strong></a> et <a href="-ms-ext.md"><strong>/ms_ext</strong></a> comme valeurs par défaut. le commutateur <strong>/OSF</strong> désactive ces commutateurs d’extension.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2009"></span><span id="midl2009"></span><dl> <dt><strong>MIDL2009</strong></dt> </dl></td>
<td><dl> <dt><span id="undefined_symbol"></span><span id="UNDEFINED_SYMBOL"></span>symbole non défini</dt> <dd> Un symbole non défini a été utilisé dans une expression. Cette erreur peut se produire lorsque vous utilisez une valeur énumérée non définie.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2010"></span><span id="midl2010"></span><dl> <dt><strong>MIDL2010</strong></dt> </dl></td>
<td><dl> <dt><span id="type_used_in_ACF_file_not_defined_in_IDL_file"></span><span id="type_used_in_acf_file_not_defined_in_idl_file"></span><span id="TYPE_USED_IN_ACF_FILE_NOT_DEFINED_IN_IDL_FILE"></span>type utilisé dans le fichier ACF non défini dans le fichier IDL</dt> <dd> Un type non défini est utilisé.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2011"></span><span id="midl2011"></span><dl> <dt><strong>MIDL2011</strong></dt> </dl></td>
<td><dl> <dt><span id="unresolved_type_declaration"></span><span id="UNRESOLVED_TYPE_DECLARATION"></span>Déclaration de type non résolue</dt> <dd> Le type signalé dans le champ d’informations d’erreur supplémentaire n’a pas été défini ailleurs dans le fichier IDL.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2012"></span><span id="midl2012"></span><dl> <dt><strong>MIDL2012</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_wide-character_constants_requires__ms_ext_or__c_ext"></span><span id="USE_OF_WIDE-CHARACTER_CONSTANTS_REQUIRES__MS_EXT_OR__C_EXT"></span>l’utilisation de constantes à caractères larges requiert/ms_ext ou/c_ext</dt> <dd> Les constantes à caractères larges sont une extension Microsoft de l’IDL DCE. Pour utiliser le type de données <a href="wchar-t.md"><strong>wchar_t</strong></a>, vous ne pouvez pas compiler avec le commutateur <a href="-osf.md"><strong>/OSF</strong></a> , qui remplace les commutateurs <a href="-ms-ext.md"><strong>/MS_EXT</strong></a> par défaut du compilateur MIDL et <a href="-c-ext.md"><strong>/c_ext</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2013"></span><span id="midl2013"></span><dl> <dt><strong>MIDL2013</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_wide_character_strings_requires__ms_ext_or__c_ext"></span><span id="USE_OF_WIDE_CHARACTER_STRINGS_REQUIRES__MS_EXT_OR__C_EXT"></span>l’utilisation de chaînes à caractères larges requiert/ms_ext ou/c_ext</dt> <dd> Les constantes de chaîne à caractères larges sont une extension Microsoft de l’IDL DCE. Pour utiliser le type de données <a href="wchar-t.md"><strong>wchar_t</strong></a>, vous ne pouvez pas compiler avec le commutateur <a href="-osf.md"><strong>/OSF</strong></a> , qui remplace les commutateurs <a href="-ms-ext.md"><strong>/MS_EXT</strong></a> par défaut du compilateur MIDL et <a href="-c-ext.md"><strong>/c_ext</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2014"></span><span id="midl2014"></span><dl> <dt><strong>MIDL2014</strong></dt> </dl></td>
<td><dl> <dt><span id="inconsistent_redefinition_of_type_wchar_t"></span><span id="INCONSISTENT_REDEFINITION_OF_TYPE_WCHAR_T"></span>redéfinition incohérente de type wchar_t</dt> <dd> Le type <a href="wchar-t.md"><strong>wchar_t</strong></a> a été redéfini en tant que type qui n’est pas équivalent à la valeur dos Short * non signée.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2015"></span><span id="midl2015"></span><dl> <dt><strong>MIDL2015</strong></dt> </dl></td>
<td><dl> <dt><span id="importlib_not_found"></span><span id="IMPORTLIB_NOT_FOUND"></span>importlib introuvable</dt> <dd> Le compilateur n’a pas pu trouver la bibliothèque de types spécifiée par la directive [ <a href="importlib.md"><strong>importlib</strong></a>]. Vérifiez que le chemin d’accès et le nom de la bibliothèque sont corrects.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2016"></span><span id="midl2016"></span><dl> <dt><strong>MIDL2016</strong></dt> </dl></td>
<td><dl> <dt><span id="two_library_blocks"></span><span id="TWO_LIBRARY_BLOCKS"></span>deux blocs de bibliothèque</dt> <dd> Deux blocs de bibliothèque (même avec des noms différents) dans le même fichier source ne sont pas autorisés. Combinez tous les éléments en un seul bloc de bibliothèque.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2017"></span><span id="midl2017"></span><dl> <dt><strong>MIDL2017</strong></dt> </dl></td>
<td><dl> <dt><span id="the_dispinterface_statement_requires_a_definition_for_IDispatch"></span><span id="the_dispinterface_statement_requires_a_definition_for_idispatch"></span><span id="THE_DISPINTERFACE_STATEMENT_REQUIRES_A_DEFINITION_FOR_IDISPATCH"></span>l’instruction dispinterface requiert une définition pour IDispatch</dt> <dd> Cette erreur se produit généralement lorsque les fichiers stdole2. tlb ou Oaidl. idl ne sont pas importés.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2018"></span><span id="midl2018"></span><dl> <dt><strong>MIDL2018</strong></dt> </dl></td>
<td><dl> <dt><span id="error_accessing_type_library"></span><span id="ERROR_ACCESSING_TYPE_LIBRARY"></span>erreur lors de l’accès à la bibliothèque de types</dt> <dd> Le compilateur n’a pas pu trouver la bibliothèque de types spécifiée. Vérifiez que vous avez correctement spécifié le chemin d’accès.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2019"></span><span id="midl2019"></span><dl> <dt><strong>MIDL2019</strong></dt> </dl></td>
<td><dl> <dt><span id="error_accessing_type_info"></span><span id="ERROR_ACCESSING_TYPE_INFO"></span>erreur lors de l’accès aux informations de type</dt> <dd> La bibliothèque de types importée est endommagée, non valide ou uniquement construite partiellement.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2020"></span><span id="midl2020"></span><dl> <dt><strong>MIDL2020</strong></dt> </dl></td>
<td><dl> <dt><span id="error_generating_type_library"></span><span id="ERROR_GENERATING_TYPE_LIBRARY"></span>erreur lors de la génération de la bibliothèque de types</dt> <dd> Impossible de générer la bibliothèque de types. L’une des causes possibles de cette erreur est la spécification d’un chemin d’accès au fichier IDL qui dépasse 126 caractères. Oleaut32.dll ne prend pas en charge les noms de chemin d’accès de plus de 126 caractères.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2021"></span><span id="midl2021"></span><dl> <dt><strong>MIDL2021</strong></dt> </dl></td>
<td><dl> <dt><span id="duplicate_id"></span><span id="DUPLICATE_ID"></span>ID dupliqué</dt> <dd> Les applications utilisent l’instruction <a href="id.md"><strong>ID</strong></a> dans les fichiers idl pour spécifier un DISPID pour les fonctions membres. Les fonctions membres peuvent être des propriétés ou des méthodes d’interfaces ou de dispinterfaces. Cette erreur indique que le fichier IDL spécifie le même numéro d’identificateur pour deux méthodes ou propriétés.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2022"></span><span id="midl2022"></span><dl> <dt><strong>MIDL2022</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_or_missing_value_for_entry_attribute"></span><span id="ILLEGAL_OR_MISSING_VALUE_FOR_ENTRY_ATTRIBUTE"></span>valeur non conforme ou manquante pour l’attribut d’entrée</dt> <dd> L’argument de l’attribut d’entrée peut être une chaîne qui spécifie un point d’entrée nommé ou un nombre ordinal qui définit le point d’entrée. Cet argument est manquant ou contient une valeur non valide.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2023"></span><span id="midl2023"></span><dl> <dt><strong>MIDL2023</strong></dt> </dl></td>
<td><dl> <dt><span id="error_recovery_assumes"></span><span id="ERROR_RECOVERY_ASSUMES"></span>la récupération d’erreur suppose</dt> <dd> Le compilateur MIDL a détecté des caractères non conformes dans le fichier IDL.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2024"></span><span id="midl2024"></span><dl> <dt><strong>MIDL2024</strong></dt> </dl></td>
<td><dl> <dt><span id="error_recovery_discards"></span><span id="ERROR_RECOVERY_DISCARDS"></span>erreur de récupération des erreurs</dt> <dd> Le compilateur MIDL a détecté des caractères non conformes dans le fichier IDL. Les caractères non autorisés sont ignorés.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2025"></span><span id="midl2025"></span><dl> <dt><strong>MIDL2025</strong></dt> </dl></td>
<td><dl> <dt><span id="syntax_error"></span><span id="SYNTAX_ERROR"></span>erreur de syntaxe</dt> <dd> Le compilateur a détecté une erreur de syntaxe au niveau de la ligne spécifiée.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2026"></span><span id="midl2026"></span><dl> <dt><strong>MIDL2026</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_recover_from_earlier_syntax_errors__aborting_compilation"></span><span id="CANNOT_RECOVER_FROM_EARLIER_SYNTAX_ERRORS__ABORTING_COMPILATION"></span>Impossible de récupérer à partir d’erreurs de syntaxe antérieures ; abandon de la compilation</dt> <dd> Le compilateur MIDL tente automatiquement de récupérer à partir d’erreurs de syntaxe en ajoutant ou en supprimant des éléments syntaxiques. Ce message indique que malgré ces tentatives de récupération, le compilateur a détecté un trop grand nombre d’erreurs. Corrigez la ou les erreurs spécifiées et recompilez.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2027"></span><span id="midl2027"></span><dl> <dt><strong>MIDL2027</strong></dt> </dl></td>
<td><dl> <dt><span id="unknown_pragma_option"></span><span id="UNKNOWN_PRAGMA_OPTION"></span>option pragma inconnue</dt> <dd> Le pragma C spécifié n’est pas pris en charge dans MIDL. Supprimez le pragma du fichier IDL.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2028"></span><span id="midl2028"></span><dl> <dt><strong>MIDL2028</strong></dt> </dl></td>
<td><dl> <dt><span id="feature_not_implemented"></span><span id="FEATURE_NOT_IMPLEMENTED"></span>fonctionnalité non implémentée</dt> <dd> La fonctionnalité MIDL, bien qu’une partie de la définition du langage, n’est pas implémentée dans Microsoft RPC et n’est pas prise en charge par le compilateur MIDL. Par exemple, les fonctionnalités de langage suivantes ne sont pas implémentées : BitSet, pipe et le type de caractère international. La fonctionnalité de langue non implémentée s’affiche dans le champ autres informations sur l’erreur du message d’erreur.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2029"></span><span id="midl2029"></span><dl> <dt><strong>MIDL2029</strong></dt> </dl></td>
<td><dl> <dt><span id="type_not_implemented"></span><span id="TYPE_NOT_IMPLEMENTED"></span>type non implémenté</dt> <dd> Le type de données spécifié, bien qu’un mot clé MIDL légal, n’est pas implémenté dans Microsoft RPC.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2030"></span><span id="midl2030"></span><dl> <dt><strong>MIDL2030</strong></dt> </dl></td>
<td><dl> <dt><span id="non-pointer_used_in_a_dereference_operation"></span><span id="NON-POINTER_USED_IN_A_DEREFERENCE_OPERATION"></span>non-pointeur utilisé dans une opération de déréférencement</dt> <dd> Un type de données qui n’est pas un pointeur a été associé à des opérations de pointeur. Vous ne pouvez pas accéder à l’objet par le biais du pointeur non-pointeur spécifié.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2031"></span><span id="midl2031"></span><dl> <dt><strong>MIDL2031</strong></dt> </dl></td>
<td><dl> <dt><span id="expression_has_a_divide_by_zero"></span><span id="EXPRESSION_HAS_A_DIVIDE_BY_ZERO"></span>l’expression a une division par zéro</dt> <dd> L’expression constante contient une division par zéro.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2032"></span><span id="midl2032"></span><dl> <dt><strong>MIDL2032</strong></dt> </dl></td>
<td><dl> <dt><span id="expression_uses_incompatible_types"></span><span id="EXPRESSION_USES_INCOMPATIBLE_TYPES"></span>l’expression utilise des types incompatibles</dt> <dd> Les côtés gauche et droit de l’opérateur dans une expression sont de types incompatibles.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2033"></span><span id="midl2033"></span><dl> <dt><strong>MIDL2033</strong></dt> </dl></td>
<td><dl> <dt><span id="nonarray_expression_uses_index_operator"></span><span id="NONARRAY_EXPRESSION_USES_INDEX_OPERATOR"></span>l’expression non-tableau utilise l’opérateur index</dt> <dd> L’expression utilise l’opération d’indexation de tableau sur un élément de données qui n’est pas du type tableau.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2034"></span><span id="midl2034"></span><dl> <dt><strong>MIDL2034</strong></dt> </dl></td>
<td><dl> <dt><span id="left-hand_side_of_expression_does_not_evaluate_to_struct_union_enum"></span><span id="LEFT-HAND_SIDE_OF_EXPRESSION_DOES_NOT_EVALUATE_TO_STRUCT_UNION_ENUM"></span>la partie gauche de l’expression ne correspond pas à struct/union/enum</dt> <dd> Opérateur de référence directe ou indirecte &quot; . &quot; ou &quot; -> &quot; a été appliqué à un objet de données qui n’est pas une structure, une Union ou une énumération. Vous ne pouvez pas obtenir une référence directe ou indirecte à l’aide de l’objet spécifié.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2035"></span><span id="midl2035"></span><dl> <dt><strong>MIDL2035</strong></dt> </dl></td>
<td><dl> <dt><span id="constant_expression_expected"></span><span id="CONSTANT_EXPRESSION_EXPECTED"></span>expression constante attendue</dt> <dd> Une expression constante était attendue dans la syntaxe. Par exemple, les limites de tableau requièrent une expression constante. Le compilateur émet ce message d’erreur lorsque la liaison du tableau est définie avec une variable ou un symbole non défini.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2036"></span><span id="midl2036"></span><dl> <dt><strong>MIDL2036</strong></dt> </dl></td>
<td><dl> <dt><span id="expression_cannot_be_evaluated_at_compile_time"></span><span id="EXPRESSION_CANNOT_BE_EVALUATED_AT_COMPILE_TIME"></span>l’expression ne peut pas être évaluée au moment de la compilation</dt> <dd> Le compilateur ne peut pas évaluer une expression au moment de la compilation.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2037"></span><span id="midl2037"></span><dl> <dt><strong>MIDL2037</strong></dt> </dl></td>
<td><dl> <dt><span id="expression_not_implemented"></span><span id="EXPRESSION_NOT_IMPLEMENTED"></span>expression non implémentée</dt> <dd> Une fonctionnalité prise en charge dans les versions précédentes du compilateur MIDL n’est pas prise en charge dans la version du compilateur fournie avec Microsoft RPC. Supprime l’expression spécifiée.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2038"></span><span id="midl2038"></span><dl> <dt><strong>MIDL2038</strong></dt> </dl></td>
<td><dl> <dt><span id="no__pointer_default__attribute_specified__assuming__unique__for_all_unattributed_pointers"></span><span id="NO__POINTER_DEFAULT__ATTRIBUTE_SPECIFIED__ASSUMING__UNIQUE__FOR_ALL_UNATTRIBUTED_POINTERS"></span>aucun attribut [pointer_default] n’est spécifié, en supposant que [unique] pour tous les pointeurs non attributs</dt> <dd> Le compilateur MIDL propose trois cas par défaut différents pour les pointeurs qui n’ont pas d’attributs de pointeur. Les paramètres de fonction qui sont des pointeurs de niveau supérieur utilisent par défaut les pointeurs [<a href="ref.md"><strong>ref</strong></a>]. Les pointeurs incorporés dans les structures et les pointeurs vers d’autres pointeurs (et non des pointeurs de niveau supérieur) ont par défaut le type spécifié par l’attribut [<a href="pointer-default.md"><strong>pointer_default</strong></a>]. Quand aucun attribut [<strong>pointer_default</strong>] n’est fourni, ces pointeurs de niveau nontop ont par défaut des pointeurs uniques. Ce message d’erreur indique le dernier cas : aucun attribut [<strong>pointer_default</strong>] n’est fourni, et il y a au moins un pointeur non-de niveau supérieur qui sera traité comme un pointeur unique. Pour plus d’informations, consultez <a href="/windows/desktop/Rpc/default-pointer-types">types de pointeurs par défaut</a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2039"></span><span id="midl2039"></span><dl> <dt><strong>MIDL2039</strong></dt> </dl></td>
<td><dl> <dt><span id="interface_is_not_automation_marshaling_conformant"></span><span id="INTERFACE_IS_NOT_AUTOMATION_MARSHALING_CONFORMANT"></span>l’interface n’est pas conforme au marshaling Automation</dt> <dd> L’interface ne remplit pas les conditions requises pour une interface OLE Automation. Vérifiez que l’interface est dérivée de <strong>IUnknown</strong> ou <strong>IDispatch</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2040"></span><span id="midl2040"></span><dl> <dt><strong>MIDL2040</strong></dt> </dl></td>
<td><dl> <dt><span id="_out__only_parameter_cannot_be_a_pointer_to_an_open_structure"></span><span id="_OUT__ONLY_PARAMETER_CANNOT_BE_A_POINTER_TO_AN_OPEN_STRUCTURE"></span>[out] seul le paramètre ne peut pas être un pointeur vers une structure ouverte</dt> <dd> Un paramètre [<a href="out-idl.md"><strong>out</strong></a>] uniquement a été utilisé comme pointeur vers une structure, connu sous le nom de structure ouverte, dont la plage et la taille transmises sont déterminées au moment de l’exécution. Le stub serveur ne connaît pas la quantité d’espace à allouer pour une structure ouverte. Utilisez un pointeur vers un pointeur désignant la structure ouverte et assurez-vous que l’application serveur alloue suffisamment d’espace pour celle-ci.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2041"></span><span id="midl2041"></span><dl> <dt><strong>MIDL2041</strong></dt> </dl></td>
<td><dl> <dt><span id="_out__only_parameter_cannot_be_an_unsized_string"></span><span id="_OUT__ONLY_PARAMETER_CANNOT_BE_AN_UNSIZED_STRING"></span>[out] seul le paramètre ne peut pas être une chaîne non dimensionnée</dt> <dd> Un tableau avec l’attribut de chaîne a été déclaré en tant que paramètre [<a href="out-idl.md"><strong>out</strong></a>] uniquement sans spécification de taille. Le stub serveur a besoin d’informations de taille pour allouer de la mémoire à la chaîne. Vous pouvez supprimer l’attribut de chaîne et ajouter l’attribut [<a href="size-is.md"><strong>size_is</strong></a>], ou vous pouvez remplacer le paramètre par un paramètre [<strong>in, out</strong>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2042"></span><span id="midl2042"></span><dl> <dt><strong>MIDL2042</strong></dt> </dl></td>
<td><dl> <dt><span id="_out__parameter_is_not_a_pointer"></span><span id="_OUT__PARAMETER_IS_NOT_A_POINTER"></span>[out] le paramètre n’est pas un pointeur</dt> <dd> Tous les paramètres [<a href="out-idl.md"><strong>out</strong></a>] doivent être des pointeurs, conformément à la Convention d’appel par valeur du langage de programmation C. Le paramètre directionnel [<strong>out</strong>] indique que le serveur transmet une valeur au client. Avec la Convention d’appel par valeur, le serveur peut transmettre des données au client uniquement si l’argument de fonction est un pointeur.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2043"></span><span id="midl2043"></span><dl> <dt><strong>MIDL2043</strong></dt> </dl></td>
<td><dl> <dt><span id="open_structure_cannot_be_a_parameter"></span><span id="OPEN_STRUCTURE_CANNOT_BE_A_PARAMETER"></span>la structure ouverte ne peut pas être un paramètre</dt> <dd> Une structure ouverte contient un tableau conforme comme dernier élément. Une structure ou une Union est tronquée lorsque le dernier élément de cette structure ou Union est un tableau conforme.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2044"></span><span id="midl2044"></span><dl> <dt><strong>MIDL2044</strong></dt> </dl></td>
<td><dl> <dt><span id="_out__context_handle_generic_handle_must_be_specified_as_a_pointer_to_that_handle_type"></span><span id="_OUT__CONTEXT_HANDLE_GENERIC_HANDLE_MUST_BE_SPECIFIED_AS_A_POINTER_TO_THAT_HANDLE_TYPE"></span>[out] handle de contexte/handle générique doit être spécifié en tant que pointeur vers ce type de handle</dt> <dd> Un handle de contexte ou un paramètre de handle défini par l’utilisateur avec l’attribut directionnel [<a href="out-idl.md"><strong>out</strong></a>] doit être un pointeur vers un pointeur.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2045"></span><span id="midl2045"></span><dl> <dt><strong>MIDL2045</strong></dt> </dl></td>
<td><dl> <dt><span id="context_handle_must_not_derive_from_a_type_that_has_the__transmit_as__attribute"></span><span id="CONTEXT_HANDLE_MUST_NOT_DERIVE_FROM_A_TYPE_THAT_HAS_THE__TRANSMIT_AS__ATTRIBUTE"></span>le descripteur de contexte ne doit pas dériver d’un type qui a l’attribut [transmit_as]</dt> <dd> Les handles de contexte doivent être transmis en tant que types de handle de contexte. Elles ne peuvent pas être transmises en tant qu’autres types et ne peuvent pas dériver de [transmit_is], [<strong>represent_as</strong>], [<strong>wire_marshal</strong>] ou [<strong>user_marshal</strong>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2046"></span><span id="midl2046"></span><dl> <dt><strong>MIDL2046</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_specify_a_variable_number_of_arguments_to_a_remote_procedure"></span><span id="CANNOT_SPECIFY_A_VARIABLE_NUMBER_OF_ARGUMENTS_TO_A_REMOTE_PROCEDURE"></span>Impossible de spécifier un nombre variable d’arguments pour une procédure distante</dt> <dd> Les appels de procédure distante qui spécifient un nombre variable d’arguments au moment de la compilation ne sont pas compatibles avec la définition RPC DCE. Vous ne pouvez pas utiliser un nombre variable d’arguments dans Microsoft RPC.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2047"></span><span id="midl2047"></span><dl> <dt><strong>MIDL2047</strong></dt> </dl></td>
<td><dl> <dt><span id="named_parameter_cannot_be__void_"></span><span id="NAMED_PARAMETER_CANNOT_BE__VOID_"></span>le paramètre nommé ne peut pas être &quot; void&quot;</dt> <dd> Un paramètre avec le type de base <a href="void.md"><strong>void</strong></a> est spécifié avec un nom.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2048"></span><span id="midl2048"></span><dl> <dt><strong>MIDL2048</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_derives_from__coclass__or__module_"></span><span id="PARAMETER_DERIVES_FROM__COCLASS__OR__MODULE_"></span>le paramètre dérive d’une &quot; coclasse ou d’un &quot; &quot; module&quot;</dt> <dd> La <a href="coclass.md"><strong>coclasse</strong></a> spécifie un objet de niveau supérieur qui contient des interfaces et des dispinterfaces. Il ne peut pas être passé en tant que paramètre.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2049"></span><span id="midl2049"></span><dl> <dt><strong>MIDL2049</strong></dt> </dl></td>
<td><dl> <dt><span id="only_the_first_parameter_can_be_a_binding_handle__you_must_specify_the__ms_ext_switch"></span><span id="ONLY_THE_FIRST_PARAMETER_CAN_BE_A_BINDING_HANDLE__YOU_MUST_SPECIFY_THE__MS_EXT_SWITCH"></span>seul le premier paramètre peut être un handle de liaison ; vous devez spécifier le commutateur/ms_ext</dt> <dd> Le RPC DCE autorise uniquement le premier paramètre à être un handle de liaison. La compilation avec le commutateur <a href="-osf.md"><strong>/OSF</strong></a> désactive le commutateur par défaut <a href="-ms-ext.md"><strong>/ms_ext</strong></a> qui prend en charge plusieurs paramètres de handle et gère les paramètres en dehors de la position la plus à gauche.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2050"></span><span id="midl2050"></span><dl> <dt><strong>MIDL2050</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_use__comm_status__on_both_a_parameter_and_a_return_type"></span><span id="CANNOT_USE__COMM_STATUS__ON_BOTH_A_PARAMETER_AND_A_RETURN_TYPE"></span>Impossible d’utiliser [comm_status] sur un paramètre et un type de retour</dt> <dd> La procédure et l’un de ses paramètres ont l’attribut [<a href="comm-status.md"><strong>comm_status</strong></a>]. L’attribut [<strong>comm_status</strong>] spécifie qu’un seul objet de données à la fois peut être de type <a href="error-status-t.md"><strong>error_status_t</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2051"></span><span id="midl2051"></span><dl> <dt><strong>MIDL2051</strong></dt> </dl></td>
<td><dl> <dt><span id="__local__attribute_on_a_procedure_requires__ms_ext"></span><span id="__LOCAL__ATTRIBUTE_ON_A_PROCEDURE_REQUIRES__MS_EXT"></span> l’attribut [local] d’une procédure requiert/ms_ext</dt> <dd> L’attribut [<a href="local.md"><strong>local</strong></a>] est une extension Microsoft de l’IDL DCE. Pour utiliser cet attribut sur une fonction, vous ne pouvez pas effectuer de compilation avec le commutateur <a href="-osf.md"><strong>/OSF</strong></a> Le commutateur <strong>/OSF</strong> remplace les commutateurs <a href="-ms-ext.md"><strong>/ms_ext</strong></a> et <a href="-c-ext.md"><strong>/C_EXT</strong></a>par défaut du compilateur MIDL.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2052"></span><span id="midl2052"></span><dl> <dt><strong>MIDL2052</strong></dt> </dl></td>
<td><dl> <dt><span id="property_attributes_may_only_be_used_with_procedures"></span><span id="PROPERTY_ATTRIBUTES_MAY_ONLY_BE_USED_WITH_PROCEDURES"></span>les attributs de propriété ne peuvent être utilisés qu’avec des procédures</dt> <dd> Utilisation incorrecte d’un attribut [<a href="propget.md"><strong>propget</strong></a>], [<a href="propput.md"><strong>propput</strong></a>] ou [<a href="propputref.md"><strong>PROPPUTREF</strong></a>]. Vérifiez que vous avez correctement orthographié le nom de la fonction de la propriété et que la propriété et la fonction ont le même nom.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2053"></span><span id="midl2053"></span><dl> <dt><strong>MIDL2053</strong></dt> </dl></td>
<td><dl> <dt><span id="a_procedure_may_not_have_more_than_one_property_attribute"></span><span id="A_PROCEDURE_MAY_NOT_HAVE_MORE_THAN_ONE_PROPERTY_ATTRIBUTE"></span>une procédure ne peut pas avoir plus d’un attribut de propriété</dt> <dd> Au maximum, un seul des attributs [<a href="propget.md"><strong>propget</strong></a>], [<a href="propput.md"><strong>propput</strong></a>] ou [<a href="propputref.md"><strong>PROPPUTREF</strong></a>] peut être spécifié pour une fonction.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2054"></span><span id="midl2054"></span><dl> <dt><strong>MIDL2054</strong></dt> </dl></td>
<td><dl> <dt><span id="the_procedure_has_an_illegal_combination_of_operation_attributes"></span><span id="THE_PROCEDURE_HAS_AN_ILLEGAL_COMBINATION_OF_OPERATION_ATTRIBUTES"></span>la procédure a une combinaison non conforme d’attributs d’opération</dt> <dd> Certains attributs ne peuvent pas être utilisés en relation avec d’autres attributs. Consultez les informations de référence sur le langage MIDL pour déterminer les exigences et la syntaxe exacte des attributs utilisés dans cette procédure.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2055"></span><span id="midl2055"></span><dl> <dt><strong>MIDL2055</strong></dt> </dl></td>
<td><dl> <dt><span id="field_deriving_from_a_conformant_array_must_be_the_last_member_of_the_structure"></span><span id="FIELD_DERIVING_FROM_A_CONFORMANT_ARRAY_MUST_BE_THE_LAST_MEMBER_OF_THE_STRUCTURE"></span>le champ dérivant d’un tableau conforme doit être le dernier membre de la structure</dt> <dd> La structure contient un tableau conforme qui n’est pas le dernier élément de la structure. Le tableau conforme doit apparaître comme dernier élément de structure.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2056"></span><span id="midl2056"></span><dl> <dt><strong>MIDL2056</strong></dt> </dl></td>
<td><dl> <dt><span id="duplicate__case__label"></span><span id="DUPLICATE__CASE__LABEL"></span>étiquette [case] dupliquée</dt> <dd> Une étiquette case dupliquée a été spécifiée. L’étiquette en double s’affiche.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2057"></span><span id="midl2057"></span><dl> <dt><strong>MIDL2057</strong></dt> </dl></td>
<td><dl> <dt><span id="no__default__case_specified_for_discriminated_union"></span><span id="NO__DEFAULT__CASE_SPECIFIED_FOR_DISCRIMINATED_UNION"></span>non [Default] cas spécifié pour l’union discriminée</dt> <dd> Une union discriminée a été spécifiée sans casse par défaut.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2058"></span><span id="midl2058"></span><dl> <dt><strong>MIDL2058</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_expression_cannot_be_resolved"></span><span id="ATTRIBUTE_EXPRESSION_CANNOT_BE_RESOLVED"></span>l’expression d’attribut ne peut pas être résolue</dt> <dd> L’expression associée à l’attribut ne peut pas être résolue. Cette erreur se produit généralement lorsqu’une variable qui apparaît dans l’expression n’est pas définie. Par exemple, l’erreur peut se produire lorsque la variable <em>s</em> n’est pas définie et qu’elle est utilisée par l’attribut [<a href="size-is.md"><strong>size_is</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2059"></span><span id="midl2059"></span><dl> <dt><strong>MIDL2059</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_expression_must_be_of_integral_type__no_support_for_64-bit_expressions"></span><span id="ATTRIBUTE_EXPRESSION_MUST_BE_OF_INTEGRAL_TYPE__NO_SUPPORT_FOR_64-BIT_EXPRESSIONS"></span>l’expression d’attribut doit être de type intégral, aucune prise en charge pour les expressions 64 bits</dt> <dd> La variable d’attribut ou l’expression spécifiée doit être un type intégral. Cette erreur se produit lorsque le type d’expression d’attribut n’est pas résolu en entier.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2060"></span><span id="midl2060"></span><dl> <dt><strong>MIDL2060</strong></dt> </dl></td>
<td><dl> <dt><span id="_byte_count__requires__ms_ext"></span><span id="_BYTE_COUNT__REQUIRES__MS_EXT"></span>[byte_count] requiert/ms_ext</dt> <dd> L’attribut [<a href="byte-count.md"><strong>byte_count</strong></a>] est une extension Microsoft de l’IDL DCE. Pour utiliser cet attribut, vous ne pouvez pas effectuer de compilation avec le commutateur <a href="-osf.md"><strong>/OSF</strong></a> , qui remplace les commutateurs <a href="-ms-ext.md"><strong>/ms_ext</strong></a> par défaut du compilateur MIDL et <a href="-c-ext.md"><strong>/c_ext</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2061"></span><span id="midl2061"></span><dl> <dt><strong>MIDL2061</strong></dt> </dl></td>
<td><dl> <dt><span id="_byte_count__can_be_applied_only_to_out_parameters_of_pointer_type"></span><span id="_BYTE_COUNT__CAN_BE_APPLIED_ONLY_TO_OUT_PARAMETERS_OF_POINTER_TYPE"></span>[byte_count] ne peut être appliqué qu’aux paramètres de sortie de type pointeur</dt> <dd> L’attribut [<a href="byte-count.md"><strong>byte_count</strong></a>] ne peut être appliqué qu’aux paramètres [<a href="out-idl.md"><strong>out</strong></a>], et tous les paramètres [<strong>out</strong>] doivent être des types pointeur.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2062"></span><span id="midl2062"></span><dl> <dt><strong>MIDL2062</strong></dt> </dl></td>
<td><dl> <dt><span id="_byte_count__cannot_be_specified_on_a_pointer_to_a_conformant_array_or_structure"></span><span id="_BYTE_COUNT__CANNOT_BE_SPECIFIED_ON_A_POINTER_TO_A_CONFORMANT_ARRAY_OR_STRUCTURE"></span>[byte_count] ne peut pas être spécifié sur un pointeur vers un tableau ou une structure conforme</dt> <dd> L’attribut [<a href="byte-count.md"><strong>byte_count</strong></a>] ne peut pas être appliqué à un tableau ou une structure conforme.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2063"></span><span id="midl2063"></span><dl> <dt><strong>MIDL2063</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_specifying_the_byte_count_is_not__in__only_or_byte_count_parameter_is_not__out__only"></span><span id="PARAMETER_SPECIFYING_THE_BYTE_COUNT_IS_NOT__IN__ONLY_OR_BYTE_COUNT_PARAMETER_IS_NOT__OUT__ONLY"></span>le paramètre qui spécifie le nombre d’octets n’est pas [in] uniquement ou le paramètre du nombre d’octets n’est pas [out] uniquement</dt> <dd> La valeur associée au [<a href="byte-count.md"><strong>byte_count</strong></a>] doit être transmise à partir du client vers le serveur ; il doit s’agir d’un paramètre [<a href="in.md"><strong>in</strong></a>]. Le paramètre [<strong>byte_count</strong>] n’a pas besoin d’être un paramètre [<strong>in, out</strong>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2064"></span><span id="midl2064"></span><dl> <dt><strong>MIDL2064</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_specifying_the_byte_count_is_not_an_integral_type"></span><span id="PARAMETER_SPECIFYING_THE_BYTE_COUNT_IS_NOT_AN_INTEGRAL_TYPE"></span>le paramètre spécifiant le nombre d’octets n’est pas un type intégral</dt> <dd> La valeur associée au nombre d’octets doit être le type entier <a href="int.md"><strong>int</strong></a>, <a href="small.md"><strong>Small</strong></a>, <a href="short.md"><strong>short</strong></a>ou <a href="long.md"><strong>long</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2065"></span><span id="midl2065"></span><dl> <dt><strong>MIDL2065</strong></dt> </dl></td>
<td><dl> <dt><span id="_byte_count__cannot_be_specified_on_a_parameter_with_size_attributes"></span><span id="_BYTE_COUNT__CANNOT_BE_SPECIFIED_ON_A_PARAMETER_WITH_SIZE_ATTRIBUTES"></span>[byte_count] ne peut pas être spécifié sur un paramètre avec des attributs de taille</dt> <dd> L’attribut [<a href="byte-count.md"><strong>byte_count</strong></a>] ne peut pas être utilisé avec d’autres attributs de taille, tels que [<a href="size-is.md"><strong>size_is</strong></a>] ou [<a href="length-is.md"><strong>length_is</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2066"></span><span id="midl2066"></span><dl> <dt><strong>MIDL2066</strong></dt> </dl></td>
<td><dl> <dt><span id="_case__expression_is_not_constant"></span><span id="_CASE__EXPRESSION_IS_NOT_CONSTANT"></span>l’expression [case] n’est pas une constante</dt> <dd> L’expression spécifiée pour l’étiquette case n’est pas une constante.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2067"></span><span id="midl2067"></span><dl> <dt><strong>MIDL2067</strong></dt> </dl></td>
<td><dl> <dt><span id="_case__expression_is_not_of_integral_type"></span><span id="_CASE__EXPRESSION_IS_NOT_OF_INTEGRAL_TYPE"></span>l’expression [case] n’est pas de type intégral</dt> <dd> L’expression spécifiée pour l’étiquette case n’est pas un type entier.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2068"></span><span id="midl2068"></span><dl> <dt><strong>MIDL2068</strong></dt> </dl></td>
<td><dl> <dt><span id="specifying__context_handle__on_a_type_other_than_void___requires__ms_ext"></span><span id="SPECIFYING__CONTEXT_HANDLE__ON_A_TYPE_OTHER_THAN_VOID___REQUIRES__MS_EXT"></span>la spécification de [context_handle] sur un type autre que void * requiert/ms_ext</dt> <dd> Pour la compatibilité avec RPC-RPC, le handle de contexte doit être un pointeur de type <strong>void *</strong>. Si vous souhaitez que les handles de contexte soient associés à des types autres que <strong>void *</strong>, n’utilisez pas le commutateur du compilateur MIDL <a href="-osf.md"><strong>/OSF</strong></a>, qui remplace le commutateur <a href="-ms-ext.md"><strong>/MS_EXT</strong></a>par défaut du compilateur MIDL.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2069"></span><span id="midl2069"></span><dl> <dt><strong>MIDL2069</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_specify_more_than_one_parameter_with_each_of_comm_status_fault_status"></span><span id="CANNOT_SPECIFY_MORE_THAN_ONE_PARAMETER_WITH_EACH_OF_COMM_STATUS_FAULT_STATUS"></span>Impossible de spécifier plusieurs paramètres avec chacun des comm_status/fault_status</dt> <dd> Une procédure ne peut avoir qu’un seul paramètre avec l’attribut [<a href="comm-status.md"><strong>comm_status</strong></a>]. Elle ne peut avoir qu’un seul paramètre avec l’attribut [<a href="fault-status.md"><strong>fault_status</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2070"></span><span id="midl2070"></span><dl> <dt><strong>MIDL2070</strong></dt> </dl></td>
<td><dl> <dt><span id="comm_status_fault_status_parameter_must_be_an__out__only_pointer_parameter"></span><span id="COMM_STATUS_FAULT_STATUS_PARAMETER_MUST_BE_AN__OUT__ONLY_POINTER_PARAMETER"></span>le paramètre comm_status/fault_status doit être un paramètre de pointeur [out] uniquement</dt> <dd> Les types de code d’erreur [<a href="comm-status.md"><strong>comm_status</strong></a>] et [<a href="fault-status.md"><strong>fault_status</strong></a>] sont transmis du serveur au client et doivent donc être spécifiés en tant que paramètre [<a href="out-idl.md"><strong>out</strong></a>]. En raison des contraintes dans le langage de programmation C, tous les paramètres [<strong>out</strong>] doivent être des pointeurs.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2071"></span><span id="midl2071"></span><dl> <dt><strong>MIDL2071</strong></dt> </dl></td>
<td><dl> <dt><span id="endpoint_syntax_error"></span><span id="ENDPOINT_SYNTAX_ERROR"></span>erreur de syntaxe du point de terminaison</dt> <dd> La syntaxe du point de terminaison est incorrecte.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2072"></span><span id="midl2072"></span><dl> <dt><strong>MIDL2072</strong></dt> </dl></td>
<td><dl> <dt><span id="inapplicable_attribute"></span><span id="INAPPLICABLE_ATTRIBUTE"></span>attribut inapplicable</dt> <dd> L’attribut spécifié ne peut pas être appliqué dans cette construction. Par exemple, l’attribut de chaîne s’applique aux tableaux de <a href="char-idl.md"><strong>caractères</strong></a> ou aux pointeurs de <strong>caractère</strong> et ne peut pas être appliqué à une structure qui se compose de deux entiers <a href="short.md"><strong>courts</strong></a> : <br/>
<pre class="syntax" data-space="preserve"><code>typedef [string] struct moo 
{
    short x;
    short y;
};</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2073"></span><span id="midl2073"></span><dl> <dt><strong>MIDL2073</strong></dt> </dl></td>
<td><dl> <dt><span id="_allocate__requires__ms_ext"></span><span id="_ALLOCATE__REQUIRES__MS_EXT"></span>[Allocate] requiert/ms_ext</dt> <dd> L’attribut <a href="allocate.md"><strong>allocate</strong></a> représente une extension Microsoft qui n’est pas définie dans le cadre du RPC DCE. Pour utiliser cet attribut, vous ne pouvez pas compiler avec le commutateur <a href="-osf.md"><strong>/OSF</strong></a> , qui remplace le commutateur <a href="-ms-ext.md"><strong>/ms_ext</strong></a> par défaut du compilateur MIDL<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2074"></span><span id="midl2074"></span><dl> <dt><strong>MIDL2074</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid__allocate__mode"></span><span id="INVALID__ALLOCATE__MODE"></span>mode [Allocate] non valide</dt> <dd> Un mode non valide pour la construction d’attribut [<a href="allocate.md"><strong>allocate</strong></a>] a été spécifié. Les quatre modes valides sont single_node, all_nodes, on_null et Always.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2075"></span><span id="midl2075"></span><dl> <dt><strong>MIDL2075</strong></dt> </dl></td>
<td><dl> <dt><span id="length_attributes_cannot_be_applied_with_string_attribute"></span><span id="LENGTH_ATTRIBUTES_CANNOT_BE_APPLIED_WITH_STRING_ATTRIBUTE"></span>les attributs de longueur ne peuvent pas être appliqués avec l’attribut String</dt> <dd> Lorsque l’attribut de chaîne est utilisé, les fichiers stub générés appellent la fonction <strong>strlen</strong> pour déterminer la longueur de la chaîne. N’utilisez pas l’attribut Length et l’attribut String pour la même variable.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2076"></span><span id="midl2076"></span><dl> <dt><strong>MIDL2076</strong></dt> </dl></td>
<td><dl> <dt><span id="_last_is__and__length_is__cannot_be_specified_at_the_same_time"></span><span id="_LAST_IS__AND__LENGTH_IS__CANNOT_BE_SPECIFIED_AT_THE_SAME_TIME"></span>[last_is] et [length_is] ne peuvent pas être spécifiés en même temps</dt> <dd> [<a href="last-is.md"><strong>Last_is</strong></a>] et [<a href="length-is.md"><strong>length_is</strong></a>] ont été spécifiés pour le même tableau. Ces attributs sont liés comme suit : longueur = Last First + 1. Étant donné que chaque valeur peut être dérivée de l’autre, ne spécifiez pas les deux.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2077"></span><span id="midl2077"></span><dl> <dt><strong>MIDL2077</strong></dt> </dl></td>
<td><dl> <dt><span id="_max_is__and__size_is__cannot_be_specified_at_the_same_time"></span><span id="_MAX_IS__AND__SIZE_IS__CANNOT_BE_SPECIFIED_AT_THE_SAME_TIME"></span>[max_is] et [size_is] ne peuvent pas être spécifiés en même temps</dt> <dd> [ <a href="max-is.md"><strong>Max_is</strong></a>] et [ <a href="size-is.md"><strong>size_is</strong></a>] ont été spécifiés pour le même tableau. Ces attributs sont liés comme suit : max = Taille + 1. Étant donné que chaque valeur peut être dérivée de l’autre, ne spécifiez pas les deux.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2078"></span><span id="midl2078"></span><dl> <dt><strong>MIDL2078</strong></dt> </dl></td>
<td><dl> <dt><span id="no__switch_is__attribute_specified_at_use_of_union"></span><span id="NO__SWITCH_IS__ATTRIBUTE_SPECIFIED_AT_USE_OF_UNION"></span>aucun attribut [switch_is] n’est spécifié lors de l’utilisation de l’opérateur Union</dt> <dd> Aucun discriminante n’a été spécifié pour l’Union. L’attribut [<a href="switch-is.md"><strong>switch_is</strong></a>] indique le discriminante utilisé pour effectuer une sélection parmi les champs d’Union.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2079"></span><span id="midl2079"></span><dl> <dt><strong>MIDL2079</strong></dt> </dl></td>
<td><dl> <dt><span id="no__uuid__specified"></span><span id="NO__UUID__SPECIFIED"></span>non [UUID] spécifié</dt> <dd> Aucun UUID n’a été spécifié pour l’interface.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2080"></span><span id="midl2080"></span><dl> <dt><strong>MIDL2080</strong></dt> </dl></td>
<td><dl> <dt><span id="_uuid__ignored_on__local__interface"></span><span id="_UUID__IGNORED_ON__LOCAL__INTERFACE"></span>[UUID] ignoré sur l’interface [locale]</dt> <dd> L’utilisation de l’attribut [<a href="local.md"><strong>local</strong></a>] sur une interface d’objet fait que le compilateur MIDL ignore l’attribut [<a href="uuid.md"><strong>UUID</strong></a>]. Vous ne pouvez pas utiliser les deux attributs sur une interface RPC.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2081"></span><span id="midl2081"></span><dl> <dt><strong>MIDL2081</strong></dt> </dl></td>
<td><dl> <dt><span id="type_mismatch_between_length_and_size_attribute_expressions"></span><span id="TYPE_MISMATCH_BETWEEN_LENGTH_AND_SIZE_ATTRIBUTE_EXPRESSIONS"></span>incompatibilité de type entre les expressions d’attribut Length et Size</dt> <dd> Les expressions d’attribut Length et Size doivent être de même type. Par exemple, cet avertissement est émis lorsque la variable d’attribut de l’expression [<a href="size-is.md"><strong>size_is</strong></a>] est de type <strong>unsigned long</strong> et que la variable d’attribut de l’expression [<a href="length-is.md"><strong>length_is</strong></a>] est de type <a href="long.md"><strong>long</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2082"></span><span id="midl2082"></span><dl> <dt><strong>MIDL2082</strong></dt> </dl></td>
<td><dl> <dt><span id="_string__attribute_must_be_specified__byte____char___or__wchar_t__array_or_pointer"></span><span id="_STRING__ATTRIBUTE_MUST_BE_SPECIFIED__BYTE____CHAR___OR__WCHAR_T__ARRAY_OR_POINTER"></span>l’attribut [String] doit être un &quot; &quot; &quot; tableau ou un pointeur Byte, char &quot; ou &quot; wchar_t &quot;</dt> <dd> Un attribut de chaîne ne peut pas être appliqué à un pointeur ou un tableau dont le type de base n’est pas un <a href="byte.md"><strong>octet</strong></a>, un <a href="char-idl.md"><strong>caractère</strong></a>ou un <a href="struct.md"><strong>struct</strong></a> dans lequel les membres sont tous du type <strong>Byte</strong> ou <strong>char</strong> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2083"></span><span id="midl2083"></span><dl> <dt><strong>MIDL2083</strong></dt> </dl></td>
<td><dl> <dt><span id="mismatch_between_the_type_of_the__switch_is__expression_and_the_switch_type_of_the_union"></span><span id="MISMATCH_BETWEEN_THE_TYPE_OF_THE__SWITCH_IS__EXPRESSION_AND_THE_SWITCH_TYPE_OF_THE_UNION"></span>incompatibilité entre le type de l’expression [switch_is] et le type de commutateur de l’Union</dt> <dd> Si l’Union [<a href="switch-type.md"><strong>switch_type</strong></a>] n’est pas spécifiée, le type de commutateur est du même type que le champ [<a href="switch-is.md"><strong>switch_is</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2084"></span><span id="midl2084"></span><dl> <dt><strong>MIDL2084</strong></dt> </dl></td>
<td><dl> <dt><span id="_transmit_as__must_not_be_applied_to_a_type_that_derives_from_a_context_handle"></span><span id="_TRANSMIT_AS__MUST_NOT_BE_APPLIED_TO_A_TYPE_THAT_DERIVES_FROM_A_CONTEXT_HANDLE"></span>[transmit_as] ne doit pas être appliqué à un type qui dérive d’un handle de contexte</dt> <dd> Les handles de contexte ne peuvent pas être transmis comme d’autres types.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2085"></span><span id="midl2085"></span><dl> <dt><strong>MIDL2085</strong></dt> </dl></td>
<td><dl> <dt><span id="_transmit_as__must_specify_a_transmissible_type"></span><span id="_TRANSMIT_AS__MUST_SPECIFY_A_TRANSMISSIBLE_TYPE"></span>[transmit_as] doit spécifier un type transmissible</dt> <dd> Le type [<a href="transmit-as.md"><strong>transmit_as</strong></a>] spécifié dérive d’un type qui ne peut pas être transmis par Microsoft RPC, tel que <a href="void.md"><strong>void</strong></a>, <strong>void *</strong>ou <a href="int.md"><strong>int</strong></a>. Utiliser un type de base RPC défini ; dans le cas de <strong>int</strong>, ajoutez des spécificateurs de taille comme <a href="small.md"><strong>Small</strong></a>, <a href="short.md"><strong>short</strong></a>ou <a href="long.md"><strong>long</strong></a> pour qualifier <strong>int</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2086"></span><span id="midl2086"></span><dl> <dt><strong>MIDL2086</strong></dt> </dl></td>
<td><dl> <dt><span id="transmitted_type_for__transmit_as__and__represent_as__must_not_be_a_pointer_or_derive_from_a_pointer"></span><span id="TRANSMITTED_TYPE_FOR__TRANSMIT_AS__AND__REPRESENT_AS__MUST_NOT_BE_A_POINTER_OR_DERIVE_FROM_A_POINTER"></span>le type transmis pour [transmit_as] et [represent_as] ne doit pas être un pointeur ou dériver d’un pointeur</dt> <dd> Le type transmis ne peut pas être un pointeur ou dériver d’un pointeur.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2087"></span><span id="midl2087"></span><dl> <dt><strong>MIDL2087</strong></dt> </dl></td>
<td><dl> <dt><span id="presented_type_for__transmit_as__and__represent_as__must_not_derive_from_a_conformant_varying_array__its_pointer_equivalent__or_a_conformant_varying_structure"></span><span id="PRESENTED_TYPE_FOR__TRANSMIT_AS__AND__REPRESENT_AS__MUST_NOT_DERIVE_FROM_A_CONFORMANT_VARYING_ARRAY__ITS_POINTER_EQUIVALENT__OR_A_CONFORMANT_VARYING_STRUCTURE"></span>le type présenté pour [transmit_as] et [represent_as] ne doit pas dériver d’un tableau conforme/variable, de son équivalent de pointeur ou d’une structure conforme/variable</dt> <dd> Le type auquel [<a href="transmit-as.md"><strong>transmit_as</strong></a>] a été appliqué ne peut pas dériver d’un tableau ou d’une structure conforme (tableau ou structure dont la taille est déterminée au moment de l’exécution).<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2088"></span><span id="midl2088"></span><dl> <dt><strong>MIDL2088</strong></dt> </dl></td>
<td><dl> <dt><span id="_uuid__format_is_incorrect"></span><span id="_UUID__FORMAT_IS_INCORRECT"></span>le format [UUID] est incorrect</dt> <dd> Le format UUID n’est pas conforme à la spécification. L’UUID doit être une chaîne composée de cinq séquences de chiffres hexadécimaux d’une longueur de 8, 4, 4, 4 et 12 chiffres. &quot;12345678-1234-ABCD-EF01-28A49C28F17D &quot; est un UUID valide. Utilisez la fonction <a href="/windows/desktop/api/rpcdce/nf-rpcdce-uuidcreate"><strong>UuidCreate</strong></a> ou un utilitaire pour générer un UUID valide.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2089"></span><span id="midl2089"></span><dl> <dt><strong>MIDL2089</strong></dt> </dl></td>
<td><dl> <dt><span id="uuid_is_not_a_hexadecimal_number"></span><span id="UUID_IS_NOT_A_HEXADECIMAL_NUMBER"></span>UUID n’est pas un nombre hexadécimal</dt> <dd> L’UUID spécifié pour l’interface contient des caractères qui ne sont pas valides dans une représentation sous forme de nombre hexadécimal. Les caractères de 0 à 9 et de A à F sont valides dans une représentation hexadécimale.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2090"></span><span id="midl2090"></span><dl> <dt><strong>MIDL2090</strong></dt> </dl></td>
<td><dl> <dt><span id="optional_parameters_must_come_after_required_parameters"></span><span id="OPTIONAL_PARAMETERS_MUST_COME_AFTER_REQUIRED_PARAMETERS"></span>les paramètres facultatifs doivent venir après les paramètres requis</dt> <dd> Pour obtenir une description de l’ordre des listes de paramètres, consultez [<a href="optional.md"><strong>facultatif</strong></a>] dans la référence du langage MIDL.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2091"></span><span id="midl2091"></span><dl> <dt><strong>MIDL2091</strong></dt> </dl></td>
<td><dl> <dt><span id="_dllname__required_when__entry__is_used"></span><span id="_DLLNAME__REQUIRED_WHEN__ENTRY__IS_USED"></span>[DllName] obligatoire quand [Entry] est utilisé</dt> <dd> Si vous spécifiez un point d’entrée dans une DLL, vous devez également spécifier le nom de cette DLL à l’aide de l’attribut [<a href="dllname-str-.md"><strong>DllName</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2092"></span><span id="midl2092"></span><dl> <dt><strong>MIDL2092</strong></dt> </dl></td>
<td><dl> <dt><span id="_bindable__is_invalid_without__propget____propput___or__propputref_"></span><span id="_BINDABLE__IS_INVALID_WITHOUT__PROPGET____PROPPUT___OR__PROPPUTREF_"></span>[Binder] n’est pas valide sans [propget], [propput] ou [propputref]</dt> <dd> L’attribut [<a href="bindable.md"><strong>Binder</strong></a>] n’est valide que sur une propriété. par conséquent, vous devez également spécifier l’une des fonctions d’accès à la propriété ou de définition de propriété.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2093"></span><span id="midl2093"></span><dl> <dt><strong>MIDL2093</strong></dt> </dl></td>
<td><dl> <dt><span id="procedures_with__propput__or__propputref__must_have_at_least_one_parameter"></span><span id="PROCEDURES_WITH__PROPPUT__OR__PROPPUTREF__MUST_HAVE_AT_LEAST_ONE_PARAMETER"></span>les procédures avec [propput] ou [propputref] doivent avoir au moins un paramètre</dt> <dd> Une procédure [<a href="propput.md"><strong>propput</strong></a>] ou [ <a href="propputref.md"><strong>PROPPUTREF</strong></a>] doit avoir au moins un paramètre [<a href="in.md"><strong>in</strong></a>] avec la propriété à définir ; une procédure [<a href="propget.md"><strong>propget</strong></a>] doit avoir au moins un paramètre [<a href="out-idl.md"><strong>out</strong></a>, <a href="retval.md"><strong>retVal</strong></a>] pour recevoir la propriété ou la référence.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2094"></span><span id="midl2094"></span><dl> <dt><strong>MIDL2094</strong></dt> </dl></td>
<td><dl> <dt><span id="_id__attribute_is_required"></span><span id="_ID__ATTRIBUTE_IS_REQUIRED"></span>attribut [id] obligatoire</dt> <dd> Cette fonction membre, en raison de la syntaxe <a href="dispinterface.md"><strong>dispinterface</strong></a> utilisée, requiert un DISPID, que vous spécifiez à l’aide de l’attribut [ <a href="id.md"><strong>ID</strong></a>]. Quand vous spécifiez une <strong>dispinterface</strong> à l’aide de propriétés et de méthodes, vous devez spécifier un DISPID pour chaque propriété et méthode.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2095"></span><span id="midl2095"></span><dl> <dt><strong>MIDL2095</strong></dt> </dl></td>
<td><dl> <dt><span id="interface_name_specified_in_the_ACF_does_not_match_that_specified_in_the_IDL_file"></span><span id="interface_name_specified_in_the_acf_does_not_match_that_specified_in_the_idl_file"></span><span id="INTERFACE_NAME_SPECIFIED_IN_THE_ACF_DOES_NOT_MATCH_THAT_SPECIFIED_IN_THE_IDL_FILE"></span>le nom d’interface spécifié dans le ACF ne correspond pas à celui spécifié dans le fichier IDL</dt> <dd> Dans le mode de compilateur actuel, le nom qui suit le mot clé interface dans le CCP doit être le même que le nom qui suit le mot clé interface dans le fichier IDL. Les noms d’interface dans les fichiers IDL et ACF peuvent être différents quand vous compilez avec le commutateur MIDL du compilateur <a href="-acf.md"><strong>/ACF</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2096"></span><span id="midl2096"></span><dl> <dt><strong>MIDL2096</strong></dt> </dl></td>
<td><dl> <dt><span id="duplicated_attribute"></span><span id="DUPLICATED_ATTRIBUTE"></span>attribut dupliqué</dt> <dd> Des attributs en double ou en conflit ont été spécifiés. Cette erreur se produit souvent lorsque deux attributs s’excluent mutuellement. Par exemple, les attributs [<a href="code.md"><strong>code</strong></a>] et [<a href="nocode.md"><strong>nocode</strong></a>] ne peuvent pas être utilisés en même temps.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2097"></span><span id="midl2097"></span><dl> <dt><strong>MIDL2097</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_with__comm_status__or__fault_status__attribute_must_be_a_pointer_to_type_error_status_t"></span><span id="PARAMETER_WITH__COMM_STATUS__OR__FAULT_STATUS__ATTRIBUTE_MUST_BE_A_POINTER_TO_TYPE_ERROR_STATUS_T"></span>le paramètre avec l’attribut [comm_status] ou [fault_status] doit être un pointeur vers le type error_status_t</dt> <dd> Quand [<a href="fault-status.md"><strong>fault_status</strong></a>] ou [<a href="comm-status.md"><strong>comm_status</strong></a>] est utilisé en tant qu’attribut de paramètre, le paramètre doit être un paramètre [<a href="out-idl.md"><strong>out</strong></a>] de type <a href="error-status-t.md"><strong>error_status_t</strong></a>. Si une erreur de serveur se produit, le paramètre est défini sur le code d’erreur. Une fois l’appel distant terminé, la procédure définit la valeur.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2098"></span><span id="midl2098"></span><dl> <dt><strong>MIDL2098</strong></dt> </dl></td>
<td><dl> <dt><span id="a__local__procedure_cannot_be_specified_in_ACF_file"></span><span id="a__local__procedure_cannot_be_specified_in_acf_file"></span><span id="A__LOCAL__PROCEDURE_CANNOT_BE_SPECIFIED_IN_ACF_FILE"></span>une procédure [local] ne peut pas être spécifiée dans un fichier ACF</dt> <dd> Une procédure locale a été spécifiée dans le CCP. La procédure locale ne peut être spécifiée que dans le fichier IDL.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2099"></span><span id="midl2099"></span><dl> <dt><strong>MIDL2099</strong></dt> </dl></td>
<td><dl> <dt><span id="specified_type_is_not_defined_as_a_handle"></span><span id="SPECIFIED_TYPE_IS_NOT_DEFINED_AS_A_HANDLE"></span>le type spécifié n’est pas défini en tant que handle</dt> <dd> Le type spécifié dans l’attribut [<a href="implicit-handle.md"><strong>implicit_handle</strong></a>] n’est pas défini en tant que type de handle. Modifiez la définition de type ou le nom de type spécifié par l’attribut.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2100"></span><span id="midl2100"></span><dl> <dt><strong>MIDL2100</strong></dt> </dl></td>
<td><dl> <dt><span id="procedure_undefined"></span><span id="PROCEDURE_UNDEFINED"></span>procédure non définie</dt> <dd> Un attribut a été appliqué à une procédure dans le CCP et cette procédure n’est pas définie dans le fichier IDL.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2101"></span><span id="midl2101"></span><dl> <dt><strong>MIDL2101</strong></dt> </dl></td>
<td><dl> <dt><span id="this_parameter_does_not_exist_in_the_IDL_file"></span><span id="this_parameter_does_not_exist_in_the_idl_file"></span><span id="THIS_PARAMETER_DOES_NOT_EXIST_IN_THE_IDL_FILE"></span>ce paramètre n’existe pas dans le fichier IDL</dt> <dd> Un paramètre spécifié dans le ACF n’existe pas dans la définition du fichier IDL. Tous les paramètres, fonctions et définitions de type qui s’affichent dans le CCP doivent correspondre aux paramètres, aux fonctions et aux types précédemment définis dans le fichier IDL.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2102"></span><span id="midl2102"></span><dl> <dt><strong>MIDL2102</strong></dt> </dl></td>
<td><dl> <dt><span id="this_array-bounds_construct_is_not_supported"></span><span id="THIS_ARRAY-BOUNDS_CONSTRUCT_IS_NOT_SUPPORTED"></span>Cette construction de limites de tableau n’est pas prise en charge</dt> <dd> MIDL prend actuellement en charge l’expression des limites supérieure et inférieure d’un tableau dans le tableau de formulaires [Lower.. Upper] uniquement lorsque la constante qui spécifie la limite inférieure du tableau correspond à la valeur zéro.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2103"></span><span id="midl2103"></span><dl> <dt><strong>MIDL2103</strong></dt> </dl></td>
<td><dl> <dt><span id="array_bound_specification_is_illegal"></span><span id="ARRAY_BOUND_SPECIFICATION_IS_ILLEGAL"></span>spécification liée à un tableau non conforme</dt> <dd> La spécification de l’utilisateur des limites de tableau pour le tableau de taille fixe est non conforme. Par exemple : <br/>
<pre class="syntax" data-space="preserve"><code>typedef short Array[-1]</code></pre>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2104"></span><span id="midl2104"></span><dl> <dt><strong>MIDL2104</strong></dt> </dl></td>
<td><dl> <dt><span id="pointer_to_a_conformant_array_or_an_array_that_contains_a_conformant_array_is_not_supported"></span><span id="POINTER_TO_A_CONFORMANT_ARRAY_OR_AN_ARRAY_THAT_CONTAINS_A_CONFORMANT_ARRAY_IS_NOT_SUPPORTED"></span>un pointeur vers un tableau conforme ou un tableau qui contient un tableau conforme n’est pas pris en charge</dt> <dd> Utilisation de tableau conforme non conforme. Pour les règles régissant les tableaux conformes, consultez <a href="/windows/desktop/Rpc/arrays-and-rpc">tableaux et RPC</a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2105"></span><span id="midl2105"></span><dl> <dt><strong>MIDL2105</strong></dt> </dl></td>
<td><dl> <dt><span id="pointee_array_does_not_derive_any_size"></span><span id="POINTEE_ARRAY_DOES_NOT_DERIVE_ANY_SIZE"></span>le pointee/tableau ne dérive aucune taille</dt> <dd> Un tableau conforme a été spécifié sans spécification de taille. Vous pouvez spécifier la taille avec l’attribut [<a href="max-is.md"><strong>max_is</strong></a>] ou [<a href="size-is.md"><strong>size_is</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2106"></span><span id="midl2106"></span><dl> <dt><strong>MIDL2106</strong></dt> </dl></td>
<td><dl> <dt><span id="only_fixed_arrays_and_SAFEARRAYs_are_legal_in_a_type_library"></span><span id="only_fixed_arrays_and_safearrays_are_legal_in_a_type_library"></span><span id="ONLY_FIXED_ARRAYS_AND_SAFEARRAYS_ARE_LEGAL_IN_A_TYPE_LIBRARY"></span>Seuls les tableaux fixes et les SAFEARRAY sont valides dans une bibliothèque de types</dt> <dd> Vous avez utilisé un type de tableau à l’intérieur d’une instruction de bibliothèque qui ne peut pas être utilisée dans une bibliothèque de types.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2107"></span><span id="midl2107"></span><dl> <dt><strong>MIDL2107</strong></dt> </dl></td>
<td><dl> <dt><span id="SAFEARRAYs_are_only_legal_inside_a_library_block"></span><span id="safearrays_are_only_legal_inside_a_library_block"></span><span id="SAFEARRAYS_ARE_ONLY_LEGAL_INSIDE_A_LIBRARY_BLOCK"></span>SafeArray sont uniquement conformes à l’intérieur d’un bloc de bibliothèque</dt> <dd> Le compilateur MIDL ne reconnaît pas un SAFEARRAY comme un type de données valide, sauf lors de la génération d’une bibliothèque de types.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2108"></span><span id="midl2108"></span><dl> <dt><strong>MIDL2108</strong></dt> </dl></td>
<td><dl> <dt><span id="badly_formed_character_constant"></span><span id="BADLY_FORMED_CHARACTER_CONSTANT"></span>constante caractère incorrecte</dt> <dd> Le caractère de fin de ligne n’est pas autorisé dans les constantes caractère.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2109"></span><span id="midl2109"></span><dl> <dt><strong>MIDL2109</strong></dt> </dl></td>
<td><dl> <dt><span id="end_of_file_found_in_comment"></span><span id="END_OF_FILE_FOUND_IN_COMMENT"></span>fin de fichier trouvée dans le commentaire</dt> <dd> Le caractère de fin de fichier a été rencontré dans un commentaire.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2110"></span><span id="midl2110"></span><dl> <dt><strong>MIDL2110</strong></dt> </dl></td>
<td><dl> <dt><span id="end_of_file_found_in_string"></span><span id="END_OF_FILE_FOUND_IN_STRING"></span>fin de fichier trouvée dans la chaîne</dt> <dd> Le caractère de fin de fichier a été rencontré dans une chaîne.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2111"></span><span id="midl2111"></span><dl> <dt><strong>MIDL2111</strong></dt> </dl></td>
<td><dl> <dt><span id="identifier_length_exceeds_31_characters"></span><span id="IDENTIFIER_LENGTH_EXCEEDS_31_CHARACTERS"></span>la longueur de l’identificateur dépasse 31 caractères</dt> <dd> Les identificateurs sont limités à 31 caractères alphanumériques. Les noms d’identificateurs de plus de 31 caractères sont tronqués.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2112"></span><span id="midl2112"></span><dl> <dt><strong>MIDL2112</strong></dt> </dl></td>
<td><dl> <dt><span id="end_of_line_found_in_string"></span><span id="END_OF_LINE_FOUND_IN_STRING"></span>fin de ligne trouvée dans la chaîne</dt> <dd> Le caractère de fin de ligne a été rencontré dans la chaîne. Vérifiez que vous avez inclus le caractère guillemet double qui termine la chaîne.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2113"></span><span id="midl2113"></span><dl> <dt><strong>MIDL2113</strong></dt> </dl></td>
<td><dl> <dt><span id="string_constant_exceeds_limit_of_255_characters"></span><span id="STRING_CONSTANT_EXCEEDS_LIMIT_OF_255_CHARACTERS"></span>la constante de chaîne dépasse la limite de 255 caractères</dt> <dd> La chaîne dépasse la longueur maximale autorisée de 255 caractères.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2114"></span><span id="midl2114"></span><dl> <dt><strong>MIDL2114</strong></dt> </dl></td>
<td><dl> <dt><span id="identifier_exceeds_limit_of_255_characters_and_has_been_truncated"></span><span id="IDENTIFIER_EXCEEDS_LIMIT_OF_255_CHARACTERS_AND_HAS_BEEN_TRUNCATED"></span>l’identificateur dépasse la limite de 255 caractères et a été tronqué</dt> <dd> L’identificateur a dépassé la longueur maximale autorisée de 255 caractères. Les caractères excédentaires dans l’identificateur sont tronqués.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2115"></span><span id="midl2115"></span><dl> <dt><strong>MIDL2115</strong></dt> </dl></td>
<td><dl> <dt><span id="constant_too_big"></span><span id="CONSTANT_TOO_BIG"></span>constante trop grande</dt> <dd> La constante est trop grande pour être représentée en interne.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2116"></span><span id="midl2116"></span><dl> <dt><strong>MIDL2116</strong></dt> </dl></td>
<td><dl> <dt><span id="numerical_parsing_error"></span><span id="NUMERICAL_PARSING_ERROR"></span>erreur d’analyse numérique</dt> <dd> Le compilateur n’a pas pu analyser l’identificateur numérique.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2117"></span><span id="midl2117"></span><dl> <dt><strong>MIDL2117</strong></dt> </dl></td>
<td><dl> <dt><span id="error_in_opening_file"></span><span id="ERROR_IN_OPENING_FILE"></span>erreur lors de l’ouverture du fichier</dt> <dd> Le système d’exploitation a signalé une erreur lors de la tentative d’ouverture d’un fichier de sortie. Cette erreur peut être due à un nom trop long pour le système de fichiers ou à un nom de fichier dupliqué.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2118"></span><span id="midl2118"></span><dl> <dt><strong>MIDL2118</strong></dt> </dl></td>
<td>erreur lors de la liaison à la fonction<br/></td>
</tr>
<tr class="even">
<td><span id="MIDL2119"></span><span id="midl2119"></span><dl> <dt><strong>MIDL2119</strong></dt> </dl></td>
<td>erreur lors de l’initialisation d’OLE<br/></td>
</tr>
<tr class="odd">
<td><span id="MIDL2120"></span><span id="midl2120"></span><dl> <dt><strong>MIDL2120</strong></dt> </dl></td>
<td>erreur lors du chargement de la bibliothèque<br/></td>
</tr>
<tr class="even">
<td><span id="MIDL2121"></span><span id="midl2121"></span><dl> <dt><strong>MIDL2121</strong></dt> </dl></td>
<td><dl> <dt><span id="_out__only_parameter_must_not_derive_from_a_top-level__unique__or__ptr__pointer_array"></span><span id="_OUT__ONLY_PARAMETER_MUST_NOT_DERIVE_FROM_A_TOP-LEVEL__UNIQUE__OR__PTR__POINTER_ARRAY"></span>[out] seul le paramètre ne doit pas dériver d’un pointeur/tableau de niveau supérieur [unique] ou [PTR]</dt> <dd> Un pointeur unique ne peut pas être un paramètre [<a href="out-idl.md"><strong>out</strong></a>] uniquement. Par définition, un pointeur unique peut passer de la <strong>valeur null</strong> à une valeur non<strong>null</strong>. Aucune information sur le paramètre [<strong>out</strong>] uniquement n’est passée du client au serveur.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2122"></span><span id="midl2122"></span><dl> <dt><strong>MIDL2122</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_is_not_applicable_to_this_non-rpcable_union"></span><span id="ATTRIBUTE_IS_NOT_APPLICABLE_TO_THIS_NON-RPCABLE_UNION"></span>l’attribut n’est pas applicable à cette Union non rpcable</dt> <dd> Seuls les attributs [<a href="switch-is.md"><strong>switch_is</strong></a>] et [<a href="switch-type.md"><strong>switch_type</strong></a>] s’appliquent à une Union qui est transmise dans le cadre d’un appel de procédure distante.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2123"></span><span id="midl2123"></span><dl> <dt><strong>MIDL2123</strong></dt> </dl></td>
<td><dl> <dt><span id="expression_used_for_a_size_attribute_must_not_derive_from_an__out_-only_parameter"></span><span id="EXPRESSION_USED_FOR_A_SIZE_ATTRIBUTE_MUST_NOT_DERIVE_FROM_AN__OUT_-ONLY_PARAMETER"></span>l’expression utilisée pour un attribut de taille ne doit pas dériver d’un paramètre [out] uniquement</dt> <dd> La valeur d’un paramètre [<a href="out-idl.md"><strong>out</strong></a>] uniquement n’est pas transmise au serveur et ne peut pas être utilisée pour déterminer la longueur ou la taille du paramètre [<a href="in.md"><strong>in</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2124"></span><span id="midl2124"></span><dl> <dt><strong>MIDL2124</strong></dt> </dl></td>
<td><dl> <dt><span id="expression_used_for_a_length_attribute_for_an__in__parameter_cannot_derive_from_an__out_-only_parameter"></span><span id="EXPRESSION_USED_FOR_A_LENGTH_ATTRIBUTE_FOR_AN__IN__PARAMETER_CANNOT_DERIVE_FROM_AN__OUT_-ONLY_PARAMETER"></span>l’expression utilisée pour un attribut de longueur pour un paramètre [in] ne peut pas dériver d’un paramètre [out] uniquement</dt> <dd> La valeur d’un paramètre [<a href="out-idl.md"><strong>out</strong></a>] uniquement n’est pas transmise au serveur et ne peut pas être utilisée pour déterminer la longueur ou la taille du paramètre [<a href="in.md"><strong>in</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2125"></span><span id="midl2125"></span><dl> <dt><strong>MIDL2125</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of__int__needs__c_ext"></span><span id="USE_OF__INT__NEEDS__C_EXT"></span>utilisation des &quot; &quot; besoins/c_ext int</dt> <dd> MIDL est un langage fortement typé. Tous les paramètres transmis sur le réseau doivent être dérivés de l’un des types de base MIDL. Le type <a href="int.md"><strong>int</strong></a> n’est pas défini dans le cadre de MIDL. Les données transmises doivent inclure un spécificateur de taille : <a href="small.md"><strong>petite</strong></a>, <strong>courte</strong>ou <strong>longue</strong>. Les données qui ne sont pas transmises sur le réseau peuvent être incluses dans une interface ; Utilisez le commutateur <a href="-c-ext.md"><strong>/c_ext</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2126"></span><span id="midl2126"></span><dl> <dt><strong>MIDL2126</strong></dt> </dl></td>
<td><dl> <dt><span id="struct_union_field_must_not_be__void_"></span><span id="STRUCT_UNION_FIELD_MUST_NOT_BE__VOID_"></span>le champ struct/union ne doit pas être &quot; void&quot;</dt> <dd> Les champs d’une structure ou d’une Union doivent être déclarés comme étant d’un type de base spécifique pris en charge par MIDL ou d’un type dérivé des types de base. Les types void ne sont pas autorisés dans les opérations distantes.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2127"></span><span id="midl2127"></span><dl> <dt><strong>MIDL2127</strong></dt> </dl></td>
<td><dl> <dt><span id="array_element_must_not_be_void"></span><span id="ARRAY_ELEMENT_MUST_NOT_BE_VOID"></span>l’élément de tableau ne doit pas être void</dt> <dd> Un élément de tableau ne peut pas être void.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2128"></span><span id="midl2128"></span><dl> <dt><strong>MIDL2128</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_type_qualifiers_and_or_modifiers_needs__c_ext"></span><span id="USE_OF_TYPE_QUALIFIERS_AND_OR_MODIFIERS_NEEDS__C_EXT"></span>l’utilisation de qualificateurs de type et/ou de modificateurs a besoin/c_ext</dt> <dd> Les modificateurs de type tels que <strong>_cdecl</strong> et <strong>_far</strong> peuvent être compilés uniquement si vous spécifiez le commutateur <a href="-c-ext.md"><strong>/c_ext</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2129"></span><span id="midl2129"></span><dl> <dt><strong>MIDL2129</strong></dt> </dl></td>
<td><dl> <dt><span id="struct_union_field_must_not_derive_from_a_function"></span><span id="STRUCT_UNION_FIELD_MUST_NOT_DERIVE_FROM_A_FUNCTION"></span>le champ struct/union ne doit pas dériver d’une fonction</dt> <dd> Les champs d’une structure ou d’une Union doivent être des types de base MIDL ou des types dérivés de ces types de base. Les fonctions ne sont pas autorisées dans les champs de structure ou d’Union.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2130"></span><span id="midl2130"></span><dl> <dt><strong>MIDL2130</strong></dt> </dl></td>
<td><dl> <dt><span id="array_element_must_not_be_a_function"></span><span id="ARRAY_ELEMENT_MUST_NOT_BE_A_FUNCTION"></span>l’élément de tableau ne doit pas être une fonction</dt> <dd> Un élément de tableau ne peut pas être une fonction.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2131"></span><span id="midl2131"></span><dl> <dt><strong>MIDL2131</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_must_not_be_a_function"></span><span id="PARAMETER_MUST_NOT_BE_A_FUNCTION"></span>le paramètre ne doit pas être une fonction</dt> <dd> Le paramètre d’une procédure distante doit être une variable d’un type spécifié. Une fonction ne peut pas être un paramètre de la procédure distante.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2132"></span><span id="midl2132"></span><dl> <dt><strong>MIDL2132</strong></dt> </dl></td>
<td><dl> <dt><span id="struct_union_with_bit_fields_needs__c_ext"></span><span id="STRUCT_UNION_WITH_BIT_FIELDS_NEEDS__C_EXT"></span>struct/union avec les champs de bits a besoin/c_ext</dt> <dd> Vous devez spécifier le commutateur <a href="-c-ext.md"><strong>/c_ext</strong></a> du compilateur MIDL pour autoriser les champs de bits dans les structures qui ne sont pas transmises dans un appel de procédure distante.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2133"></span><span id="midl2133"></span><dl> <dt><strong>MIDL2133</strong></dt> </dl></td>
<td><dl> <dt><span id="bit_field_specification_on_a_type_other_that__int__is_a_non-ANSI-compatible_extension"></span><span id="bit_field_specification_on_a_type_other_that__int__is_a_non-ansi-compatible_extension"></span><span id="BIT_FIELD_SPECIFICATION_ON_A_TYPE_OTHER_THAT__INT__IS_A_NON-ANSI-COMPATIBLE_EXTENSION"></span>spécification de champ de bits sur un type autre que &quot; int &quot; est une extension non compatible ANSI</dt> <dd> La spécification du langage de programmation C ANSI n’autorise pas l’application des champs de bits aux types non entiers.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2134"></span><span id="midl2134"></span><dl> <dt><strong>MIDL2134</strong></dt> </dl></td>
<td><dl> <dt><span id="bit_field_specification_can_be_applied_only_to_simple__integral_types"></span><span id="BIT_FIELD_SPECIFICATION_CAN_BE_APPLIED_ONLY_TO_SIMPLE__INTEGRAL_TYPES"></span>la spécification de champ de bits ne peut être appliquée qu’aux types intégraux simples</dt> <dd> La spécification du langage de programmation C ANSI n’autorise pas l’application des champs de bits aux types non entiers.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2135"></span><span id="midl2135"></span><dl> <dt><strong>MIDL2135</strong></dt> </dl></td>
<td><dl> <dt><span id="struct_union_field_must_not_derive_from_handle_t_or_a_context-handle"></span><span id="STRUCT_UNION_FIELD_MUST_NOT_DERIVE_FROM_HANDLE_T_OR_A_CONTEXT-HANDLE"></span>le champ struct/union ne doit pas dériver de handle_t ou d’un handle de contexte</dt> <dd> Les handles de contexte ne peuvent pas être transmis dans le cadre d’une autre structure. Ils doivent être transmis en tant que handles de contexte.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2136"></span><span id="midl2136"></span><dl> <dt><strong>MIDL2136</strong></dt> </dl></td>
<td><dl> <dt><span id="array_element_must_not_derive_from_handle_t_or_a_context_handle"></span><span id="ARRAY_ELEMENT_MUST_NOT_DERIVE_FROM_HANDLE_T_OR_A_CONTEXT_HANDLE"></span>l’élément de tableau ne doit pas dériver de handle_t ou d’un handle de contexte</dt> <dd> Les handles de contexte ne peuvent pas être transmis dans le cadre d’un tableau.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2137"></span><span id="midl2137"></span><dl> <dt><strong>MIDL2137</strong></dt> </dl></td>
<td><dl> <dt><span id="this_specification_of_union_needs__c_ext"></span><span id="THIS_SPECIFICATION_OF_UNION_NEEDS__C_EXT"></span>Cette spécification des besoins/c_ext d’Union</dt> <dd> Une Union qui apparaît dans la définition de l’interface doit être associée à discriminante ou déclarée comme locale. Les données qui ne sont pas transmises sur le réseau peuvent être déclarées implicitement comme locales lorsque vous utilisez le commutateur <a href="-c-ext.md"><strong>/c_ext</strong></a> , qui est la valeur par défaut MIDL. Vous ne pouvez pas compiler cet IDL avec le commutateur <a href="-osf.md"><strong>/OSF</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2138"></span><span id="midl2138"></span><dl> <dt><strong>MIDL2138</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_deriving_from_an__int__must_have_size_specifier__small____short___or__long__with_the__int_"></span><span id="PARAMETER_DERIVING_FROM_AN__INT__MUST_HAVE_SIZE_SPECIFIER__SMALL____SHORT___OR__LONG__WITH_THE__INT_"></span>la dérivation d’un paramètre à partir d’un &quot; int &quot; doit avoir un spécificateur de taille &quot; petit, &quot; &quot; court &quot; ou &quot; long &quot; avec l' &quot; entier&quot;</dt> <dd> Le type <a href="int.md"><strong>int</strong></a> est uniquement un type MIDL valide sur les plateformes 32 bits, sur les systèmes 16 bits, <strong>int</strong> doit être accompagné d’une spécification de taille. Utilisez l’un des spécificateurs de taille <a href="small.md"><strong>Small</strong></a>, <a href="short.md"><strong>short</strong></a>ou <a href="long.md"><strong>long</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2139"></span><span id="midl2139"></span><dl> <dt><strong>MIDL2139</strong></dt> </dl></td>
<td><dl> <dt><span id="type_of_the_parameter_cannot_derive_from_void_or_void_"></span><span id="TYPE_OF_THE_PARAMETER_CANNOT_DERIVE_FROM_VOID_OR_VOID_"></span>le type du paramètre ne peut pas dériver de void ou void *</dt> <dd> MIDL est un langage fortement typé. Tous les paramètres transmis sur le réseau doivent être dérivés de l’un des types de base MIDL. MIDL ne prend pas en charge <a href="void.md"><strong>void</strong></a> comme type de base. Vous devez remplacer la déclaration par un type MIDL valide.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2140"></span><span id="midl2140"></span><dl> <dt><strong>MIDL2140</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_deriving_from_a_struct_union_containing_bit_fields_is_not_supported"></span><span id="PARAMETER_DERIVING_FROM_A_STRUCT_UNION_CONTAINING_BIT_FIELDS_IS_NOT_SUPPORTED"></span>le paramètre dérivant d’un struct/union contenant des champs de bits n’est pas pris en charge</dt> <dd> Les champs de bits ne sont pas définis comme un type de données valide par RPC DCE.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2141"></span><span id="midl2141"></span><dl> <dt><strong>MIDL2141</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_a_parameter_deriving_from_a_type_containing_type-modifiers_type-qualifiers_needs__c_ext"></span><span id="USE_OF_A_PARAMETER_DERIVING_FROM_A_TYPE_CONTAINING_TYPE-MODIFIERS_TYPE-QUALIFIERS_NEEDS__C_EXT"></span>l’utilisation d’un paramètre dérivant d’un type contenant des modificateurs de type/modificateurs de type a besoin/c_ext</dt> <dd> L’utilisation de mots clés tels que <strong>Far</strong>, <strong>pres</strong>, <a href="const.md"><strong>const</strong></a>et <strong>volatile</strong> dans le fichier IDL est une extension Microsoft de l’appel de procédure distante (RPC) DCE. Ces mots clés ne sont pas disponibles quand vous compilez avec le commutateur <a href="-osf.md"><strong>/OSF</strong></a> , qui désactive le commutateur d’extension par défaut <a href="-c-ext.md"><strong>/c_ext</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2142"></span><span id="midl2142"></span><dl> <dt><strong>MIDL2142</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_must_not_derive_from_a_pointer_to_a_function"></span><span id="PARAMETER_MUST_NOT_DERIVE_FROM_A_POINTER_TO_A_FUNCTION"></span>le paramètre ne doit pas dériver d’un pointeur vers une fonction</dt> <dd> Les bibliothèques Runtime RPC transmettent un pointeur et ses données associées entre le client et le serveur. Les pointeurs vers des fonctions ne peuvent pas être transmis en tant que paramètres, car la fonction ne peut pas être transmise sur le réseau.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2143"></span><span id="midl2143"></span><dl> <dt><strong>MIDL2143</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_must_not_derive_from_a_nonrpccapable_union"></span><span id="PARAMETER_MUST_NOT_DERIVE_FROM_A_NONRPCCAPABLE_UNION"></span>le paramètre ne doit pas dériver d’une Union de compatibilité nonrpc</dt> <dd> L’Union doit être associée à un discriminante. Utilisez les attributs [<a href="switch-is.md"><strong>switch_is</strong></a>] et [<a href="switch-type.md"><strong>switch_type</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2144"></span><span id="midl2144"></span><dl> <dt><strong>MIDL2144</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_derives_from_an__int.__You_must_use_size_specifiers_with_the__int_"></span><span id="return_type_derives_from_an__int.__you_must_use_size_specifiers_with_the__int_"></span><span id="RETURN_TYPE_DERIVES_FROM_AN__INT.__YOU_MUST_USE_SIZE_SPECIFIERS_WITH_THE__INT_"></span>le type de retour dérive d’un &quot; int. &quot; Vous devez utiliser des spécificateurs de taille avec l' &quot; entier&quot;</dt> <dd> Sur les systèmes 16 bits, le type <a href="int.md"><strong>int</strong></a> n’est pas un type MIDL valide, sauf s’il est accompagné d’une spécification de taille. Utilisez l’un des spécificateurs de taille <a href="small.md"><strong>Small</strong></a>, <a href="short.md"><strong>short</strong></a>ou <a href="long.md"><strong>long</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2145"></span><span id="midl2145"></span><dl> <dt><strong>MIDL2145</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_must_not_derive_from_a_void_pointer"></span><span id="RETURN_TYPE_MUST_NOT_DERIVE_FROM_A_VOID_POINTER"></span>le type de retour ne doit pas dériver d’un pointeur void</dt> <dd> MIDL est un langage fortement typé. Tous les paramètres transmis sur le réseau doivent être dérivés de l’un des types de base MIDL. Les types void ne sont pas définis dans le cadre de MIDL. Vous devez remplacer la déclaration par un type MIDL valide.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2146"></span><span id="midl2146"></span><dl> <dt><strong>MIDL2146</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_must_not_derive_from_a_structure_union_containing_bit-fields"></span><span id="RETURN_TYPE_MUST_NOT_DERIVE_FROM_A_STRUCTURE_UNION_CONTAINING_BIT-FIELDS"></span>le type de retour ne doit pas dériver d’une structure/Union contenant des champs de bits</dt> <dd> Les champs de bits ne sont pas définis comme un type de données valide par RPC DCE.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2147"></span><span id="midl2147"></span><dl> <dt><strong>MIDL2147</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_must_not_derive_from_a_nonrpccapable_union"></span><span id="RETURN_TYPE_MUST_NOT_DERIVE_FROM_A_NONRPCCAPABLE_UNION"></span>le type de retour ne doit pas dériver d’une Union de compatibilité nonrpc</dt> <dd> L’Union doit être associée à un discriminante. Utilisez les attributs [<a href="switch-is.md"><strong>switch_is</strong></a>] et [<a href="switch-type.md"><strong>switch_type</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2148"></span><span id="midl2148"></span><dl> <dt><strong>MIDL2148</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_must_not_derive_from_a_pointer_to_a_function"></span><span id="RETURN_TYPE_MUST_NOT_DERIVE_FROM_A_POINTER_TO_A_FUNCTION"></span>le type de retour ne doit pas dériver d’un pointeur vers une fonction</dt> <dd> Les bibliothèques Runtime RPC transmettent un pointeur et ses données associées entre le client et le serveur. Les pointeurs vers des fonctions ne peuvent pas être transmis en tant que paramètres, car RPC ne définit pas une méthode pour transmettre la fonction associée sur le réseau.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2149"></span><span id="midl2149"></span><dl> <dt><strong>MIDL2149</strong></dt> </dl></td>
<td><dl> <dt><span id="compound_initializers_are_not_supported"></span><span id="COMPOUND_INITIALIZERS_ARE_NOT_SUPPORTED"></span>les initialiseurs composés ne sont pas pris en charge</dt> <dd> DCE RPC ne prend en charge que l’initialisation simple. La structure ou le tableau ne peut pas être initialisé dans le fichier IDL.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2150"></span><span id="midl2150"></span><dl> <dt><strong>MIDL2150</strong></dt> </dl></td>
<td><dl> <dt><span id="ACF_attributes_in_the_IDL_file_need_the__app_config_switch"></span><span id="acf_attributes_in_the_idl_file_need_the__app_config_switch"></span><span id="ACF_ATTRIBUTES_IN_THE_IDL_FILE_NEED_THE__APP_CONFIG_SWITCH"></span>Les attributs ACF dans le fichier IDL nécessitent le commutateur/app_config</dt> <dd> Une extension Microsoft vous permet de spécifier des attributs ACF dans le fichier IDL. Utilisez le commutateur <a href="-app-config.md"><strong>/app_config</strong></a> pour activer cette extension.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2151"></span><span id="midl2151"></span><dl> <dt><strong>MIDL2151</strong></dt> </dl></td>
<td><dl> <dt><span id="single-line_comment_needs__ms_ext_or__c_ext"></span><span id="SINGLE-LINE_COMMENT_NEEDS__MS_EXT_OR__C_EXT"></span>Commentaires sur une seule ligne/ms_ext ou/c_ext</dt> <dd> Les commentaires sur une seule ligne qui utilisent deux barres obliques (//) représentent une extension Microsoft du RPC DCE. Vous ne pouvez pas utiliser de commentaires sur une seule ligne si vous compilez avec le commutateur <a href="-osf.md"><strong>/OSF</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2152"></span><span id="midl2152"></span><dl> <dt><strong>MIDL2152</strong></dt> </dl></td>
<td><dl> <dt><span id="_version__format_is_incorrect"></span><span id="_VERSION__FORMAT_IS_INCORRECT"></span>le format [version] est incorrect</dt> <dd> Le numéro de version de l’interface dans l’en-tête d’interface doit être spécifié au format <em>major</em>. <em>Minor</em>, où chaque nombre peut être compris entre 0 et 65535.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2153"></span><span id="midl2153"></span><dl> <dt><strong>MIDL2153</strong></dt> </dl></td>
<td><dl> <dt><span id="_signed__needs__ms_ext_or__c_ext"></span><span id="_SIGNED__NEEDS__MS_EXT_OR__C_EXT"></span>&quot;&quot;besoins/ms_ext signés/c_ext</dt> <dd> L’utilisation du mot clé <a href="signed.md"><strong>signed</strong></a> est une extension Microsoft du RPC DCE. Vous ne pouvez pas utiliser le commutateur <a href="-osf.md"><strong>/OSF</strong></a> si vous souhaitez utiliser cette fonctionnalité.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2154"></span><span id="midl2154"></span><dl> <dt><strong>MIDL2154</strong></dt> </dl></td>
<td><dl> <dt><span id="mismatch_in_assignment_type"></span><span id="MISMATCH_IN_ASSIGNMENT_TYPE"></span>incompatibilité dans le type d’affectation</dt> <dd> Le type de la variable ne correspond pas au type de la valeur qui est assignée à la variable.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2155"></span><span id="midl2155"></span><dl> <dt><strong>MIDL2155</strong></dt> </dl></td>
<td><dl> <dt><span id="declaration_must_be_of_the_form__const__type__declarator_____initializing_expression_"></span><span id="DECLARATION_MUST_BE_OF_THE_FORM__CONST__TYPE__DECLARATOR_____INITIALIZING_EXPRESSION_"></span>la déclaration doit se présenter sous la forme : const <type><declarator> = <initializing expression></dt> <dd> La déclaration n’est pas compatible avec la syntaxe RPC DCE. Utilisez le commutateur <a href="-ms-ext.md"><strong>/ms_ext</strong></a> ou <a href="-c-ext.md"><strong>/c_ext</strong></a> mode du compilateur MIDL.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2156"></span><span id="midl2156"></span><dl> <dt><strong>MIDL2156</strong></dt> </dl></td>
<td><dl> <dt><span id="declaration_must_have__const_"></span><span id="DECLARATION_MUST_HAVE__CONST_"></span>la déclaration doit avoir &quot; const&quot;</dt> <dd> Les déclarations dans le fichier IDL doivent être des expressions constantes qui utilisent le mot clé <a href="const.md"><strong>const</strong></a>, par exemple :<br/>
<pre class="syntax" data-space="preserve"><code>const short x = 2;</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2157"></span><span id="midl2157"></span><dl> <dt><strong>MIDL2157</strong></dt> </dl></td>
<td><dl> <dt><span id="struct_union_enum_must_not_be_defined_in_a_parameter-type_specification"></span><span id="STRUCT_UNION_ENUM_MUST_NOT_BE_DEFINED_IN_A_PARAMETER-TYPE_SPECIFICATION"></span>struct/union/enum ne doit pas être défini dans une spécification de type paramètre</dt> <dd> La structure, l’Union ou le type énuméré doit être explicitement déclaré en dehors du prototype de la fonction.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2158"></span><span id="midl2158"></span><dl> <dt><strong>MIDL2158</strong></dt> </dl></td>
<td><dl> <dt><span id="_allocate__attribute_must_be_applied_only_on_non-void_pointer_types"></span><span id="_ALLOCATE__ATTRIBUTE_MUST_BE_APPLIED_ONLY_ON_NON-VOID_POINTER_TYPES"></span>l’attribut [Allocate] doit être appliqué uniquement sur les types de pointeur non void</dt> <dd> L’attribut [<a href="allocate.md"><strong>allocate</strong></a>] est conçu pour les structures de données complexes basées sur un pointeur. Lorsque l’attribut [Allocate] est spécifié, le fichier stub parcourt la structure de données pour calculer la taille totale de tous les objets accessibles à partir du pointeur et de tous les autres pointeurs de la structure de données. Remplacez le type par un type de pointeur non void ou supprimez l’attribut [<strong>allocate</strong>] et utilisez une autre méthode pour déterminer sa taille d’allocation, telle que l’opérateur <strong>sizeof</strong> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2159"></span><span id="midl2159"></span><dl> <dt><strong>MIDL2159</strong></dt> </dl></td>
<td><dl> <dt><span id="array_or_equivalent_pointer_construct_cannot_derive_from_a_nonencapsulated_union"></span><span id="ARRAY_OR_EQUIVALENT_POINTER_CONSTRUCT_CANNOT_DERIVE_FROM_A_NONENCAPSULATED_UNION"></span>un tableau ou une construction de pointeur équivalent ne peut pas dériver d’une Union non encapsulée</dt> <dd> Chaque Union doit être associée à un discriminante. Les tableaux d’unions ne sont pas autorisés, car ils ne fournissent pas les discriminante associés. Les tableaux de structures dans lesquels la structure empaquette l’Union et ses discriminante sont autorisés, car les stubs peuvent utiliser le discriminante pour déterminer la taille de chaque Union.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2160"></span><span id="midl2160"></span><dl> <dt><strong>MIDL2160</strong></dt> </dl></td>
<td><dl> <dt><span id="field_must_not_derive_from_an_error_status_t_type"></span><span id="FIELD_MUST_NOT_DERIVE_FROM_AN_ERROR_STATUS_T_TYPE"></span>le champ ne doit pas dériver d’un type de error_status_t</dt> <dd> Le type de <a href="error-status-t.md"><strong>error_status_t</strong></a> ne peut être utilisé qu’en tant que paramètre ou type de retour. Il ne peut pas être incorporé dans le champ d’une structure ou d’une Union.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2161"></span><span id="midl2161"></span><dl> <dt><strong>MIDL2161</strong></dt> </dl></td>
<td><dl> <dt><span id="union_has_at_least_one_arm_without_a_case_label"></span><span id="UNION_HAS_AT_LEAST_ONE_ARM_WITHOUT_A_CASE_LABEL"></span>l’Union a au moins un ARM sans étiquette case</dt> <dd> La déclaration d’Union ne correspond pas à la syntaxe MIDL requise pour l’Union. Chaque ARM d’Union requiert une étiquette case ou une étiquette default qui sélectionne ce bras d’Union.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2162"></span><span id="midl2162"></span><dl> <dt><strong>MIDL2162</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_or_return_value_must_not_derive_from_a_type_that_has__ignore__applied_to_it"></span><span id="PARAMETER_OR_RETURN_VALUE_MUST_NOT_DERIVE_FROM_A_TYPE_THAT_HAS__IGNORE__APPLIED_TO_IT"></span>le paramètre ou la valeur de retour ne doit pas dériver d’un type auquel [ignore] est appliqué</dt> <dd> L’attribut [<a href="ignore.md"><strong>ignore</strong></a>] est un attribut de champ qui ne peut être appliqué qu’à des champs, tels que des champs de structures et des tableaux. L’attribut [<strong>ignore</strong>] indique que le stub ne doit pas déréférencer le pointeur pendant la transmission et n’est pas autorisé lorsqu’il est en conflit avec d’autres attributs qui doivent être déréférencés, tels que les paramètres [<a href="out-idl.md"><strong>out</strong></a>] et les valeurs de retour de fonction.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2163"></span><span id="midl2163"></span><dl> <dt><strong>MIDL2163</strong></dt> </dl></td>
<td><dl> <dt><span id="pointer_already_has_a_pointer_attribute_applied_to_it"></span><span id="POINTER_ALREADY_HAS_A_POINTER_ATTRIBUTE_APPLIED_TO_IT"></span>un pointeur a déjà un attribut de pointeur qui lui est appliqué</dt> <dd> Seul l’un des attributs de pointeur, [<a href="ref.md"><strong>ref</strong></a>], [<a href="unique.md"><strong>unique</strong></a>] ou [<a href="ptr.md"><strong>ptr</strong></a>], peut être appliqué à un seul pointeur.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2164"></span><span id="midl2164"></span><dl> <dt><strong>MIDL2164</strong></dt> </dl></td>
<td><dl> <dt><span id="field_parameter_must_not_derive_from_a_structure_that_is_recursive_through_a_ref_pointer"></span><span id="FIELD_PARAMETER_MUST_NOT_DERIVE_FROM_A_STRUCTURE_THAT_IS_RECURSIVE_THROUGH_A_REF_POINTER"></span>le champ/paramètre ne doit pas dériver d’une structure qui est récursive à l’aide d’un pointeur Ref</dt> <dd> Par définition, un pointeur de référence ne peut pas avoir la valeur <strong>null</strong>. Une structure de données récursive définie à l’aide d’un pointeur de référence n’a pas d’élément <strong>null</strong> et par Convention ne se termine pas. Utilisez un attribut de pointeur [<a href="unique.md"><strong>unique</strong></a>] pour permettre à la structure de données de spécifier un élément <strong>null</strong> ou de redéfinir la structure de données comme structure de données non récursive.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2165"></span><span id="midl2165"></span><dl> <dt><strong>MIDL2165</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_field_deriving_from_a_void_pointer_needs__c_ext"></span><span id="USE_OF_FIELD_DERIVING_FROM_A_VOID_POINTER_NEEDS__C_EXT"></span>utilisation d’une dérivation de champs à partir d’un pointeur void/c_ext</dt> <dd> Le type <strong>void *</strong> et d’autres types et qualificateurs de type qui ne sont pas pris en charge par l’IDL DCE ne sont autorisés dans le fichier IDL que lorsque vous utilisez les paramètres du compilateur MIDL par défaut. L’utilisation du commutateur <a href="-osf.md"><strong>/OSF</strong></a> remplace cette valeur par défaut. Si vous devez compiler en mode de compatibilité OSF, vous devrez redéfinir le type de pointeur.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2166"></span><span id="midl2166"></span><dl> <dt><strong>MIDL2166</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_this_attribute_needs__ms_ext"></span><span id="USE_OF_THIS_ATTRIBUTE_NEEDS__MS_EXT"></span>l’utilisation de cet attribut requiert/ms_ext</dt> <dd> Cette fonctionnalité de langage est une extension Microsoft de l’IDL DCE. Vous ne pouvez pas utiliser cette fonctionnalité si vous compilez en mode de compatibilité OSF ( <a href="-osf.md"><strong>/OSF</strong></a> ).<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2167"></span><span id="midl2167"></span><dl> <dt><strong>MIDL2167</strong></dt> </dl></td>
<td><dl> <dt><span id="this_attribute_only_allowed_with_new_format_type_libraries"></span><span id="THIS_ATTRIBUTE_ONLY_ALLOWED_WITH_NEW_FORMAT_TYPE_LIBRARIES"></span>Cet attribut est uniquement autorisé avec les nouvelles bibliothèques de types de format</dt> <dd> pour utiliser cet attribut, vous avez besoin de la version de Oleaut32.dll fournie avec Windows 2000 ou version ultérieure.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2168"></span><span id="midl2168"></span><dl> <dt><strong>MIDL2168</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_wchar_t_needs__ms_ext_or__c_ext"></span><span id="USE_OF_WCHAR_T_NEEDS__MS_EXT_OR__C_EXT"></span>utilisation des wchar_t besoins/ms_ext ou/c_ext</dt> <dd> Le type à caractères larges représente une extension de l’IDL DCE. Le compilateur MIDL n’accepte pas le type à caractères larges lorsque vous spécifiez le commutateur <a href="-osf.md"><strong>/OSF</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2169"></span><span id="midl2169"></span><dl> <dt><strong>MIDL2169</strong></dt> </dl></td>
<td><dl> <dt><span id="unnamed_fields_need__ms_ext_or__c_ext"></span><span id="UNNAMED_FIELDS_NEED__MS_EXT_OR__C_EXT"></span>les champs sans nom doivent avoir la ms_ext ou/c_ext</dt> <dd> L’IDL DCE ne prend pas en charge l’utilisation de structures sans nom ou d’unions incorporées dans d’autres structures ou unions. Dans l’IDL DCE, tous les champs incorporés de ce type doivent être nommés. Le compilateur MIDL n’autorise pas leur utilisation lorsque vous spécifiez le commutateur <a href="-osf.md"><strong>/OSF</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2170"></span><span id="midl2170"></span><dl> <dt><strong>MIDL2170</strong></dt> </dl></td>
<td><dl> <dt><span id="unnamed_fields_can_derive_only_from_struct_union_types"></span><span id="UNNAMED_FIELDS_CAN_DERIVE_ONLY_FROM_STRUCT_UNION_TYPES"></span>les champs sans nom peuvent dériver uniquement des types struct/union</dt> <dd> L’extension Microsoft de l’IDL DCE qui prend en charge les champs sans nom s’applique uniquement aux structures et aux unions. Vous devez attribuer un nom au champ ou redéfinir le champ pour qu’il soit conforme à cette restriction.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2171"></span><span id="midl2171"></span><dl> <dt><strong>MIDL2171</strong></dt> </dl></td>
<td><dl> <dt><span id="field_of_a_union_cannot_derive_from_a_conformant_varying_array_or_its_pointer_equivalent"></span><span id="FIELD_OF_A_UNION_CANNOT_DERIVE_FROM_A_CONFORMANT_VARYING_ARRAY_OR_ITS_POINTER_EQUIVALENT"></span>le champ d’une Union ne peut pas dériver d’un tableau conforme/variable ou de son pointeur équivalent</dt> <dd> Le tableau conforme ne peut pas apparaître seul dans l’Union, mais doit être accompagné de la valeur qui spécifie la taille du tableau. Au lieu d’utiliser le tableau comme ARM d’Union, utilisez une structure qui se compose du tableau conforme et de l’identificateur qui spécifie sa taille.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2172"></span><span id="midl2172"></span><dl> <dt><strong>MIDL2172</strong></dt> </dl></td>
<td><dl> <dt><span id="no__pointer_default__attribute_specified__assuming__ptr__for_all_unattributed_pointers_in_interface"></span><span id="NO__POINTER_DEFAULT__ATTRIBUTE_SPECIFIED__ASSUMING__PTR__FOR_ALL_UNATTRIBUTED_POINTERS_IN_INTERFACE"></span>aucun attribut [pointer_default] n’est spécifié, en supposant que [PTR] pour tous les pointeurs non attributs dans l’interface</dt> <dd> L’implémentation IDL DCE spécifie que tous les pointeurs de chaque fichier IDL doivent être associés à des attributs de pointeur. Lorsqu’un attribut de pointeur explicite n’est pas assigné au paramètre ou au type de pointeur et qu’aucun attribut [<a href="pointer-default.md"><strong>pointer_default</strong></a>] n’est spécifié dans le fichier IDL, l’attribut de pointeur complet <a href="ptr.md"><strong>ptr</strong></a> est associé au pointeur. Vous pouvez modifier les attributs de pointeur à l’aide d’attributs de pointeur explicites, en spécifiant un attribut [<strong>pointer_default</strong>], ou en spécifiant le commutateur <a href="-ms-ext.md"><strong>/ms_ext</strong></a> pour modifier la valeur par défaut des pointeurs non attributs en [<a href="unique.md"><strong>unique</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2173"></span><span id="midl2173"></span><dl> <dt><strong>MIDL2173</strong></dt> </dl></td>
<td><dl> <dt><span id="initializing_expression_must_resolve_to_a_constant_expression"></span><span id="INITIALIZING_EXPRESSION_MUST_RESOLVE_TO_A_CONSTANT_EXPRESSION"></span>l’initialisation de l’expression doit être résolue en une expression constante</dt> <dd> Si une expression est utilisée comme initialiseur, l’expression doit être une expression constante. Cela est vrai dans tous les modes de compilateur MIDL. L’expression doit pouvoir être résolue au moment de la compilation. Spécifiez une constante littérale ou une expression qui correspond à une constante, plutôt qu’à une variable.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2174"></span><span id="midl2174"></span><dl> <dt><strong>MIDL2174</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_expression_must_be_of_type_integer__char__Boolean_or_enum"></span><span id="attribute_expression_must_be_of_type_integer__char__boolean_or_enum"></span><span id="ATTRIBUTE_EXPRESSION_MUST_BE_OF_TYPE_INTEGER__CHAR__BOOLEAN_OR_ENUM"></span>l’expression d’attribut doit être de type entier, Char, Boolean ou enum</dt> <dd> Le type spécifié n’est pas résolu en un type de commutateur valide. Utilisez un type entier, caractère, <a href="byte.md"><strong>octet</strong></a>, <a href="boolean.md"><strong>booléen</strong></a>ou <a href="enum.md"><strong>enum</strong></a> , ou un type dérivé de l’un de ces types.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2175"></span><span id="midl2175"></span><dl> <dt><strong>MIDL2175</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_constant"></span><span id="ILLEGAL_CONSTANT"></span>constante non conforme</dt> <dd> La constante spécifiée est en dehors de la plage valide pour le type spécifié.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2176"></span><span id="midl2176"></span><dl> <dt><strong>MIDL2176</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_not_implemented__ignored"></span><span id="ATTRIBUTE_NOT_IMPLEMENTED__IGNORED"></span>attribut non implémenté ; pas</dt> <dd> L’attribut spécifié n’est pas implémenté dans cette version de Microsoft RPC. Le compilateur MIDL continue à traiter le fichier IDL comme si l’attribut n’était pas présent.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2177"></span><span id="midl2177"></span><dl> <dt><strong>MIDL2177</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_must_not_derive_from_a__ref__pointer"></span><span id="RETURN_TYPE_MUST_NOT_DERIVE_FROM_A__REF__POINTER"></span>le type de retour ne doit pas dériver d’un pointeur [ref]</dt> <dd> Les valeurs de retour de fonction qui sont définies comme étant des types pointeur doivent être spécifiées en tant que pointeurs [<a href="unique.md"><strong>unique</strong></a>] ou <a href="ptr.md"><strong>Full</strong></a> . Vous ne pouvez pas utiliser de pointeurs de référence.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2178"></span><span id="midl2178"></span><dl> <dt><strong>MIDL2178</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_expression_must_be_a_variable_name_or_a_pointer_dereference_expression_in_this_mode._You_must_specify_the__ms_ext_switch"></span><span id="attribute_expression_must_be_a_variable_name_or_a_pointer_dereference_expression_in_this_mode._you_must_specify_the__ms_ext_switch"></span><span id="ATTRIBUTE_EXPRESSION_MUST_BE_A_VARIABLE_NAME_OR_A_POINTER_DEREFERENCE_EXPRESSION_IN_THIS_MODE._YOU_MUST_SPECIFY_THE__MS_EXT_SWITCH"></span>l’expression d’attribut doit être un nom de variable ou une expression de déréférencement de pointeur dans ce mode. Vous devez spécifier le commutateur/ms_ext</dt> <dd> Le compilateur IDL DCE requiert que la taille associée à l’attribut [<a href="size-is.md"><strong>size_is</strong></a>] soit spécifiée par une variable ou une variable pointeur. Si vous souhaitez tirer parti de l’extension Microsoft qui permet de définir l’attribut [<strong>size_is</strong>] par une expression constante, vous ne pouvez pas utiliser le commutateur de compilateur <a href="-osf.md"><strong>/OSF</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2179"></span><span id="midl2179"></span><dl> <dt><strong>MIDL2179</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_must_not_derive_from_a_recursive_nonencapsulated_union"></span><span id="PARAMETER_MUST_NOT_DERIVE_FROM_A_RECURSIVE_NONENCAPSULATED_UNION"></span>le paramètre ne doit pas dériver d’une Union non encapsulée récursive</dt> <dd> Une Union doit inclure un discriminante, de sorte qu’une Union ne peut pas avoir une autre Union comme élément. Une Union peut être incorporée dans une autre Union uniquement lorsqu’elle fait partie d’une structure qui comprend discriminante.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2180"></span><span id="midl2180"></span><dl> <dt><strong>MIDL2180</strong></dt> </dl></td>
<td><dl> <dt><span id="binding-handle_parameter_cannot_be__out__only"></span><span id="BINDING-HANDLE_PARAMETER_CANNOT_BE__OUT__ONLY"></span>le paramètre de handle de liaison ne peut pas être [out] uniquement</dt> <dd> Le paramètre de handle identifié par le compilateur MIDL comme handle de liaison pour cette opération doit être un paramètre [<a href="in.md"><strong>in</strong></a>]. [<a href="out-idl.md"><strong>out</strong></a>]-seuls les paramètres ne sont pas définis sur le stub client et le descripteur de liaison doit être défini sur le client.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2181"></span><span id="midl2181"></span><dl> <dt><strong>MIDL2181</strong></dt> </dl></td>
<td><dl> <dt><span id="pointer_to_a_handle_cannot_be__unique__or__ptr_"></span><span id="POINTER_TO_A_HANDLE_CANNOT_BE__UNIQUE__OR__PTR_"></span>le pointeur vers un handle ne peut pas être [unique] ou [PTR]</dt> <dd> Vous ne pouvez pas utiliser les attributs de pointeur complet et unique pour un pointeur vers un handle. Ces attributs autorisent la valeur <strong>null</strong>et le handle de liaison ne peut pas être <strong>null</strong>. Utilisez l’attribut [<a href="ref.md"><strong>ref</strong></a>] pour dériver le paramètre de handle de liaison des pointeurs de référence.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2182"></span><span id="midl2182"></span><dl> <dt><strong>MIDL2182</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_that_is_not_a_binding_handle_must_not_derive_from_handle_t"></span><span id="PARAMETER_THAT_IS_NOT_A_BINDING_HANDLE_MUST_NOT_DERIVE_FROM_HANDLE_T"></span>le paramètre qui n’est pas un handle de liaison ne doit pas dériver de handle_t</dt> <dd> Le type de handle primitif <a href="handle-t.md"><strong>handle_t</strong></a> n’est pas un type de données valide transmis sur le réseau. Remplacez le type de paramètre par un type autre que <strong>handle_t</strong>ou supprimez le paramètre.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2183"></span><span id="midl2183"></span><dl> <dt><strong>MIDL2183</strong></dt> </dl></td>
<td><dl> <dt><span id="unexpected_end_of_file_found"></span><span id="UNEXPECTED_END_OF_FILE_FOUND"></span>fin de fichier inattendue trouvée</dt> <dd> Le compilateur MIDL a trouvé la fin du fichier avant de pouvoir résoudre tous les éléments syntaxiques du fichier. Vérifiez que le caractère de fin de l’accolade fermante (}) est présent à la fin du fichier, ou vérifiez la syntaxe.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2184"></span><span id="midl2184"></span><dl> <dt><strong>MIDL2184</strong></dt> </dl></td>
<td><dl> <dt><span id="type_deriving_from_handle_t_must_not_have__transmit_as__applied_to_it"></span><span id="TYPE_DERIVING_FROM_HANDLE_T_MUST_NOT_HAVE__TRANSMIT_AS__APPLIED_TO_IT"></span>[transmit_as] ne doit pas être appliqué au type dérivant de handle_t</dt> <dd> Le type de handle primitif <a href="handle-t.md"><strong>handle_t</strong></a> n’est pas transmis sur le réseau.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2185"></span><span id="midl2185"></span><dl> <dt><strong>MIDL2185</strong></dt> </dl></td>
<td><dl> <dt><span id="_context_handle__must_not_be_applied_to_a_type_that_has__handle__applied_to_it"></span><span id="_CONTEXT_HANDLE__MUST_NOT_BE_APPLIED_TO_A_TYPE_THAT_HAS__HANDLE__APPLIED_TO_IT"></span>[context_handle] ne doit pas être appliqué à un type auquel [handle] est appliqué</dt> <dd> Les attributs [<a href="context-handle.md"><strong>context_handle</strong></a>] et [<a href="handle.md"><strong>handle</strong></a>] ne peuvent pas être appliqués au même type.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2186"></span><span id="midl2186"></span><dl> <dt><strong>MIDL2186</strong></dt> </dl></td>
<td><dl> <dt><span id="_handle__must_not_be_specified_on_a_type_deriving_from_void_or_void__"></span><span id="_HANDLE__MUST_NOT_BE_SPECIFIED_ON_A_TYPE_DERIVING_FROM_VOID_OR_VOID__"></span>[handle] ne doit pas être spécifié sur un type dérivant de void ou void *</dt> <dd> Un type spécifié avec l’attribut [<a href="handle.md"><strong>handle</strong></a>] peut être transmis sur le réseau, mais le type <strong>void *</strong> n’est pas un type transmissible. Le type de handle doit être résolu en un type qui dérive des types de base transmissibles.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2187"></span><span id="midl2187"></span><dl> <dt><strong>MIDL2187</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_must_have_either__in____out__or__in_out__in_this_mode._You_must_specify__ms_ext_or__c_ext"></span><span id="parameter_must_have_either__in____out__or__in_out__in_this_mode._you_must_specify__ms_ext_or__c_ext"></span><span id="PARAMETER_MUST_HAVE_EITHER__IN____OUT__OR__IN_OUT__IN_THIS_MODE._YOU_MUST_SPECIFY__MS_EXT_OR__C_EXT"></span>le paramètre doit avoir la valeur [in], [out] ou [in, out] dans ce mode. Vous devez spécifier/ms_ext ou/c_ext</dt> <dd> Le compilateur IDL DCE requiert que tous les paramètres aient des paramètres directionnels explicites. Pour utiliser les extensions Microsoft de l’IDL DCE, vous ne pouvez pas utiliser le commutateur <a href="-osf.md"><strong>/OSF</strong></a> , qui remplace <a href="-ms-ext.md"><strong>/ms_ext</strong></a> et <a href="-c-ext.md"><strong>/c_ext</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2188"></span><span id="midl2188"></span><dl> <dt><strong>MIDL2188</strong></dt> </dl></td>
<td><dl> <dt><span id="transmitted_type_may_not_derive_from__void__for__transmit_as____represent_as____wire_marshal____user_marshal_"></span><span id="TRANSMITTED_TYPE_MAY_NOT_DERIVE_FROM__VOID__FOR__TRANSMIT_AS____REPRESENT_AS____WIRE_MARSHAL____USER_MARSHAL_"></span>le type transmis ne peut pas dériver de &quot; void &quot; pour [transmit_as], [represent_as], [wire_marshal], [user_marshal]</dt> <dd> L’attribut [<a href="transmit-as.md"><strong>transmit_as</strong></a>] s’applique uniquement aux types pointeur. Utilisez le type <strong>void *</strong> à la place de <a href="void.md"><strong>void</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2189"></span><span id="midl2189"></span><dl> <dt><strong>MIDL2189</strong></dt> </dl></td>
<td><dl> <dt><span id="_void__must_be_specified_on_the_first_and_only_parameter_specification"></span><span id="_VOID__MUST_BE_SPECIFIED_ON_THE_FIRST_AND_ONLY_PARAMETER_SPECIFICATION"></span>&quot;void &quot; doit être spécifié sur la première et la seule spécification de paramètre</dt> <dd> Le mot clé <a href="void.md"><strong>void</strong></a> n’apparaît pas correctement avec d’autres paramètres de fonction. Pour spécifier une fonction sans paramètres, le mot clé <strong>void</strong> doit être le seul élément de la liste de paramètres, comme dans l’exemple suivant :<br/>
<pre class="syntax" data-space="preserve"><code>void Moo(void)</code></pre>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2190"></span><span id="midl2190"></span><dl> <dt><strong>MIDL2190</strong></dt> </dl></td>
<td><dl> <dt><span id="_switch_is__must_be_specified_only_on_a_type_deriving_from_a_nonencapsulated_union"></span><span id="_SWITCH_IS__MUST_BE_SPECIFIED_ONLY_ON_A_TYPE_DERIVING_FROM_A_NONENCAPSULATED_UNION"></span>[switch_is] doit être spécifié uniquement sur un type dérivant d’une Union non encapsulée</dt> <dd> Le mot clé [<a href="switch-is.md"><strong>switch_is</strong></a>] est appliqué de façon incorrecte. Elle ne peut être utilisée qu’avec des <a href="nonencapsulated-unions.md">types d’Union non encapsulés</a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2191"></span><span id="midl2191"></span><dl> <dt><strong>MIDL2191</strong></dt> </dl></td>
<td><dl> <dt><span id="stringable_structures_are_not_implemented_in_this_version"></span><span id="STRINGABLE_STRUCTURES_ARE_NOT_IMPLEMENTED_IN_THIS_VERSION"></span>les structures à chaîner ne sont pas implémentées dans cette version</dt> <dd> Le IDL DCE permet à l’attribut [<a href="string.md"><strong>String</strong></a>] de s’appliquer à une structure dont les éléments se composent uniquement de caractères, d’octets ou de types qui sont résolus en caractères ou en octets. Cette fonctionnalité n’est pas prise en charge dans Microsoft RPC. L’attribut [<strong>String</strong>] ne peut pas être appliqué à la structure dans son ensemble. Toutefois, il peut être appliqué à chaque groupe individuel.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2192"></span><span id="midl2192"></span><dl> <dt><strong>MIDL2192</strong></dt> </dl></td>
<td><dl> <dt><span id="switch_type_can_only_be_integral__char__Boolean_or_enum"></span><span id="switch_type_can_only_be_integral__char__boolean_or_enum"></span><span id="SWITCH_TYPE_CAN_ONLY_BE_INTEGRAL__CHAR__BOOLEAN_OR_ENUM"></span>le type de commutateur peut uniquement être intégral, Char, Boolean ou enum</dt> <dd> Le type spécifié n’est pas résolu en un type de commutateur valide. Utilisez un entier, un caractère, un <a href="byte.md"><strong>octet</strong></a>, un <a href="boolean.md"><strong>booléen</strong></a>, un type <a href="enum.md"><strong>enum</strong></a> ou un type dérivé de l’un de ces types.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2193"></span><span id="midl2193"></span><dl> <dt><strong>MIDL2193</strong></dt> </dl></td>
<td><dl> <dt><span id="_handle__must_not_be_specified_on_a_type_deriving_from_handle_t"></span><span id="_HANDLE__MUST_NOT_BE_SPECIFIED_ON_A_TYPE_DERIVING_FROM_HANDLE_T"></span>[handle] ne doit pas être spécifié sur un type dérivant de handle_t</dt> <dd> Un type de handle doit être défini à l’aide d’un seul des types de handle ou d’attributs. Utilisez le type primitif <a href="handle-t.md"><strong>handle_t</strong></a> ou l’attribut [<a href="handle.md"><strong>handle</strong></a>], mais pas les deux. Le type de handle défini par l’utilisateur doit être transmissible, mais le type de <strong>handle_t</strong> n’est pas transmis sur le réseau.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2194"></span><span id="midl2194"></span><dl> <dt><strong>MIDL2194</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_deriving_from_handle_t_must_not_be_an__out__parameter"></span><span id="PARAMETER_DERIVING_FROM_HANDLE_T_MUST_NOT_BE_AN__OUT__PARAMETER"></span>le paramètre dérivant de handle_t ne doit pas être un paramètre [out]</dt> <dd> Un handle du type primitif <a href="handle-t.md"><strong>handle_t</strong></a> est explicite uniquement au côté de l’application dans laquelle il est défini. Le type <strong>handle_t</strong> n’est pas transmis sur le réseau.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2195"></span><span id="midl2195"></span><dl> <dt><strong>MIDL2195</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_expression_derives_from__unique__or__ptr__pointer_dereference"></span><span id="ATTRIBUTE_EXPRESSION_DERIVES_FROM__UNIQUE__OR__PTR__POINTER_DEREFERENCE"></span>l’expression d’attribut est dérivée du déréférencement du pointeur [unique] ou [PTR]</dt> <dd> Bien que les attributs [<a href="unique.md"><strong>unique</strong></a>] et pointeur <a href="ptr.md"><strong>complet</strong></a> autorisent les pointeurs à avoir des valeurs <strong>null</strong> , l’expression qui définit l’attribut de taille ou de longueur ne doit jamais avoir une valeur <strong>null</strong> . Lorsque des pointeurs sont utilisés, MIDL limite les expressions aux pointeurs [<a href="ref.md"><strong>ref</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2196"></span><span id="midl2196"></span><dl> <dt><strong>MIDL2196</strong></dt> </dl></td>
<td><dl> <dt><span id="_cpp_quote__requires__ms_ext"></span><span id="_CPP_QUOTE__REQUIRES__MS_EXT"></span>&quot;cpp_quote &quot; requiert/ms_ext</dt> <dd> L’attribut <a href="cpp-quote.md"><strong>cpp_quote</strong></a> est une extension Microsoft de l’IDL DCE. N’utilisez pas le commutateur de compilateur MIDL <a href="-osf.md"><strong>/OSF</strong></a>, qui remplace <a href="-ms-ext.md"><strong>/ms_ext</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2197"></span><span id="midl2197"></span><dl> <dt><strong>MIDL2197</strong></dt> </dl></td>
<td><dl> <dt><span id="quoted_uuid_requires__ms_ext"></span><span id="QUOTED_UUID_REQUIRES__MS_EXT"></span>l’UUID entre guillemets requiert/ms_ext</dt> <dd> La possibilité de spécifier une valeur UUID entre guillemets est une extension Microsoft de l’IDL DCE. N’utilisez pas le commutateur de compilateur MIDL <a href="-osf.md"><strong>/OSF</strong></a>, qui remplace <a href="-ms-ext.md"><strong>/ms_ext</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2198"></span><span id="midl2198"></span><dl> <dt><strong>MIDL2198</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_cannot_derive_from_a_nonencapsulated_union"></span><span id="RETURN_TYPE_CANNOT_DERIVE_FROM_A_NONENCAPSULATED_UNION"></span>le type de retour ne peut pas dériver d’une Union non encapsulée</dt> <dd> L’Union non encapsulée ne peut pas être utilisée en tant que type de retour de fonction. Pour retourner le type d’Union, spécifiez le type d’Union en tant que paramètre [<a href="out-idl.md"><strong>out</strong></a>] ou [<strong>in, out</strong>].<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2199"></span><span id="midl2199"></span><dl> <dt><strong>MIDL2199</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_cannot_derive_from_a_conformant_structure"></span><span id="RETURN_TYPE_CANNOT_DERIVE_FROM_A_CONFORMANT_STRUCTURE"></span>le type de retour ne peut pas dériver d’une structure conforme</dt> <dd> La taille du type de retour doit être une constante. Vous ne pouvez pas spécifier comme type de retour une structure qui contient un tableau conforme même lorsque la structure inclut également son spécificateur de taille. Pour retourner la structure conforme, spécifiez la structure en tant que paramètre [<a href="out-idl.md"><strong>out</strong></a>] ou [<strong>in, out</strong>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2200"></span><span id="midl2200"></span><dl> <dt><strong>MIDL2200</strong></dt> </dl></td>
<td><dl> <dt><span id="_transmit_as__must_not_be_applied_to_a_type_deriving_from_a_generic_handle"></span><span id="_TRANSMIT_AS__MUST_NOT_BE_APPLIED_TO_A_TYPE_DERIVING_FROM_A_GENERIC_HANDLE"></span>[transmit_as] ne doit pas être appliqué à un type dérivant d’un handle générique</dt> <dd> Dans cette version, les attributs [<a href="handle.md"><strong>handle</strong></a>] et [<a href="transmit-as.md"><strong>transmit_as</strong></a>] ne peuvent pas être combinés sur le même type.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2201"></span><span id="midl2201"></span><dl> <dt><strong>MIDL2201</strong></dt> </dl></td>
<td><dl> <dt><span id="_handle__must_not_be_applied_to_a_type_that_has__transmit_as__applied_to_it"></span><span id="_HANDLE__MUST_NOT_BE_APPLIED_TO_A_TYPE_THAT_HAS__TRANSMIT_AS__APPLIED_TO_IT"></span>[handle] ne doit pas être appliqué à un type auquel [transmit_as] s’applique</dt> <dd> Dans cette version, les attributs [<a href="handle.md"><strong>handle</strong></a>] et [<a href="transmit-as.md"><strong>transmit_as</strong></a>] ne peuvent pas être combinés sur le même type.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2202"></span><span id="midl2202"></span><dl> <dt><strong>MIDL2202</strong></dt> </dl></td>
<td><dl> <dt><span id="type_specified_for_the_const_declaration_is_invalid"></span><span id="TYPE_SPECIFIED_FOR_THE_CONST_DECLARATION_IS_INVALID"></span>le type spécifié pour la déclaration const n’est pas valide</dt> <dd> Les déclarations de constante sont limitées aux types entier, caractère, caractères larges, chaîne et booléen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2203"></span><span id="midl2203"></span><dl> <dt><strong>MIDL2203</strong></dt> </dl></td>
<td><dl> <dt><span id="operand_to_the_sizeof_operator_is_not_supported"></span><span id="OPERAND_TO_THE_SIZEOF_OPERATOR_IS_NOT_SUPPORTED"></span>l’opérande de l’opérateur sizeof n’est pas pris en charge</dt> <dd> Le compilateur MIDL prend en charge l’opération <strong>sizeof</strong> uniquement pour les types simples. L’opérande spécifié ne correspond pas à un type entier.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2204"></span><span id="midl2204"></span><dl> <dt><strong>MIDL2204</strong></dt> </dl></td>
<td><dl> <dt><span id="this_name_already_used_as_a_const_identifier_name"></span><span id="THIS_NAME_ALREADY_USED_AS_A_CONST_IDENTIFIER_NAME"></span>ce nom est déjà utilisé comme nom d’identificateur const</dt> <dd> L’identificateur a été précédemment utilisé pour identifier une constante dans une déclaration <a href="const.md"><strong>const</strong></a> . Modifiez le nom de l’un des identificateurs afin que les identificateurs soient uniques.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2205"></span><span id="midl2205"></span><dl> <dt><strong>MIDL2205</strong></dt> </dl></td>
<td><dl> <dt><span id="inconsistent_redefinition_of_type_error_status_t"></span><span id="INCONSISTENT_REDEFINITION_OF_TYPE_ERROR_STATUS_T"></span>redéfinition incohérente de type error_status_t</dt> <dd> Le type <a href="error-status-t.md"><strong>error_status_t</strong></a> doit être résolu en type <strong>unsigned long</strong>. D’autres définitions de type ne peuvent pas être utilisées.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2206"></span><span id="midl2206"></span><dl> <dt><strong>MIDL2206</strong></dt> </dl></td>
<td><dl> <dt><span id="_case__value_out_of_range_of_switch_type"></span><span id="_CASE__VALUE_OUT_OF_RANGE_OF_SWITCH_TYPE"></span>[case] valeur hors des limites du type de commutateur</dt> <dd> La valeur associée au cas de l’instruction switch est hors limites pour le type de commutateur spécifié. Par exemple, cette erreur se produit quand une valeur d’entier long est utilisée dans l’instruction case pour un type entier Short.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2207"></span><span id="midl2207"></span><dl> <dt><strong>MIDL2207</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_deriving_from_wchar_t_needs__ms_ext"></span><span id="PARAMETER_DERIVING_FROM_WCHAR_T_NEEDS__MS_EXT"></span>paramètre dérivant de wchar_t besoins/ms_ext</dt> <dd> Le type à caractères larges <a href="wchar-t.md"><strong>wchar_t</strong></a> est une extension Microsoft de l’IDL DCE. N’utilisez pas le commutateur de compilateur MIDL <a href="-osf.md"><strong>/OSF</strong></a>, qui remplace <a href="-ms-ext.md"><strong>/ms_ext</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2208"></span><span id="midl2208"></span><dl> <dt><strong>MIDL2208</strong></dt> </dl></td>
<td><dl> <dt><span id="this_interface_has_only_callbacks"></span><span id="THIS_INTERFACE_HAS_ONLY_CALLBACKS"></span>Cette interface n’a que des rappels</dt> <dd> Les rappels sont valides uniquement dans le contexte d’un appel de procédure distante. L’interface doit inclure au moins un prototype de fonction pour un appel de procédure distante qui n’inclut pas l’attribut [<a href="callback.md"><strong>callback</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2209"></span><span id="midl2209"></span><dl> <dt><strong>MIDL2209</strong></dt> </dl></td>
<td><dl> <dt><span id="redundantly_specified_attribute__ignored"></span><span id="REDUNDANTLY_SPECIFIED_ATTRIBUTE__IGNORED"></span>attribut spécifié de manière redondante ; pas</dt> <dd> L’attribut spécifié a été appliqué plusieurs fois. Plusieurs instances du même attribut sont ignorées.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2210"></span><span id="midl2210"></span><dl> <dt><strong>MIDL2210</strong></dt> </dl></td>
<td><dl> <dt><span id="context_handle_type_used_for_an_implicit_handle"></span><span id="CONTEXT_HANDLE_TYPE_USED_FOR_AN_IMPLICIT_HANDLE"></span>type de handle de contexte utilisé pour un handle implicite</dt> <dd> Un type qui a été défini à l’aide de l’attribut [<a href="context-handle.md"><strong>context_handle</strong></a>] a été spécifié en tant que type de handle dans un attribut [ <a href="implicit-handle.md"><strong>implicit_handle</strong></a>]. Les attributs ne peuvent pas être combinés de cette façon.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2211"></span><span id="midl2211"></span><dl> <dt><strong>MIDL2211</strong></dt> </dl></td>
<td><dl> <dt><span id="conflicting_options_specified_for__allocate_"></span><span id="CONFLICTING_OPTIONS_SPECIFIED_FOR__ALLOCATE_"></span>options spécifiées en conflit pour [Allocate]</dt> <dd> Les options spécifiées pour l’attribut ACF [<a href="allocate.md"><strong>allocate</strong></a>] représentent des directives conflictuelles. Par exemple, spécifiez l’option all_nodes ou l’option single_node, mais pas les deux.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2212"></span><span id="midl2212"></span><dl> <dt><strong>MIDL2212</strong></dt> </dl></td>
<td><dl> <dt><span id="error_while_writing_to_file"></span><span id="ERROR_WHILE_WRITING_TO_FILE"></span>erreur lors de l’écriture dans le fichier</dt> <dd> Une erreur s’est produite lors de l’écriture dans le fichier. Cette condition peut être due à des erreurs relatives à l’espace disque, aux descripteurs de fichiers, aux restrictions d’accès aux fichiers et aux défaillances matérielles.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2213"></span><span id="midl2213"></span><dl> <dt><strong>MIDL2213</strong></dt> </dl></td>
<td><dl> <dt><span id="no_switch_type_found_at_definition_of_union__using_the__switch_is__type"></span><span id="NO_SWITCH_TYPE_FOUND_AT_DEFINITION_OF_UNION__USING_THE__SWITCH_IS__TYPE"></span>aucun type de commutateur trouvé à la définition de Union, à l’aide du type [switch_is]</dt> <dd> La définition d’Union n’inclut pas d’attribut [<a href="switch-type.md"><strong>switch_type</strong></a>] explicite. Le type de la variable spécifiée par l’attribut [<a href="switch-is.md"><strong>switch_is</strong></a>] est utilisé comme type de commutateur.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2214"></span><span id="midl2214"></span><dl> <dt><strong>MIDL2214</strong></dt> </dl></td>
<td><dl> <dt><span id="semantic_check_incomplete_due_to_previous_errors"></span><span id="SEMANTIC_CHECK_INCOMPLETE_DUE_TO_PREVIOUS_ERRORS"></span>Vérification sémantique incomplète en raison d’erreurs précédentes</dt> <dd> Le compilateur MIDL effectue deux passes sur le ou les fichiers d’entrée pour résoudre toutes les déclarations anticipées. En raison d’erreurs rencontrées lors de la première passe, la vérification de la deuxième passe n’a pas été effectuée. Les erreurs qui ne sont pas signalées concernant les déclarations anticipées peuvent toujours être présentes dans le fichier.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2215"></span><span id="midl2215"></span><dl> <dt><strong>MIDL2215</strong></dt> </dl></td>
<td><dl> <dt><span id="handle_parameter_or_return_type_is_not_supported_on_a__callback__procedure"></span><span id="HANDLE_PARAMETER_OR_RETURN_TYPE_IS_NOT_SUPPORTED_ON_A__CALLBACK__PROCEDURE"></span>le paramètre de handle ou le type de retour n’est pas pris en charge sur une procédure [callback]</dt> <dd> Une procédure [<a href="callback.md"><strong>callback</strong></a>] se produit dans le contexte d’un appel d’un client au serveur et utilise le même handle de liaison que l’appel d’origine. Les paramètres de handle de liaison explicites ou les types de retour ne sont pas autorisés dans les fonctions de rappel.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2216"></span><span id="midl2216"></span><dl> <dt><strong>MIDL2216</strong></dt> </dl></td>
<td><dl> <dt><span id="_ptr__does_not_support_aliasing_in_this_version"></span><span id="_PTR__DOES_NOT_SUPPORT_ALIASING_IN_THIS_VERSION"></span>[PTR] ne prend pas en charge les alias dans cette version</dt> <dd> Un alias se produit lorsque les données sont accessibles par le biais de plusieurs pointeurs ou noms de variables. Supprimez l’alias. Pour plus d’informations, consultez <a href="/windows/desktop/Rpc/unique-pointers">pointeurs uniques</a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2217"></span><span id="midl2217"></span><dl> <dt><strong>MIDL2217</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_already_defined_as_a_context_handle"></span><span id="PARAMETER_ALREADY_DEFINED_AS_A_CONTEXT_HANDLE"></span>paramètre déjà défini comme handle de contexte</dt> <dd> Le paramètre a été précédemment défini comme handle de contexte.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2218"></span><span id="midl2218"></span><dl> <dt><strong>MIDL2218</strong></dt> </dl></td>
<td><dl> <dt><span id="_context_handle__must_not_derive_from_handle_t"></span><span id="_CONTEXT_HANDLE__MUST_NOT_DERIVE_FROM_HANDLE_T"></span>[context_handle] ne doit pas dériver de handle_t</dt> <dd> Les trois caractéristiques du handle : le type <a href="handle-t.md"><strong>handle_t</strong></a>, l’attribut [<a href="handle.md"><strong>handle</strong></a>] et l’attribut [<a href="context-handle.md"><strong>context_handle</strong></a>], s’excluent mutuellement. Une seule caractéristique peut être appliquée à un type ou à un paramètre à la fois.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2219"></span><span id="midl2219"></span><dl> <dt><strong>MIDL2219</strong></dt> </dl></td>
<td><dl> <dt><span id="array_size_exceeds_65536_bytes"></span><span id="ARRAY_SIZE_EXCEEDS_65536_BYTES"></span>la taille du tableau dépasse 65536 octets</dt> <dd> Sur certaines plateformes Microsoft, la taille maximale des données transmissibles est de 64 Ko. Reconcevez votre application afin que toutes les données transmises soient comprises dans la taille maximale transmissible.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2220"></span><span id="midl2220"></span><dl> <dt><strong>MIDL2220</strong></dt> </dl></td>
<td><dl> <dt><span id="structure_size_exceeds_65536_bytes"></span><span id="STRUCTURE_SIZE_EXCEEDS_65536_BYTES"></span>la taille de la structure dépasse 65536 octets</dt> <dd> Sur certaines plateformes Microsoft, la taille maximale des données transmissibles est de 64 Ko. Reconcevez votre application afin que toutes les données transmises soient comprises dans la taille maximale transmissible.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2221"></span><span id="midl2221"></span><dl> <dt><strong>MIDL2221</strong></dt> </dl></td>
<td><dl> <dt><span id="field_of_a_nonencapsulated_union_cannot_be_another_nonencapsulated_union"></span><span id="FIELD_OF_A_NONENCAPSULATED_UNION_CANNOT_BE_ANOTHER_NONENCAPSULATED_UNION"></span>le champ d’une Union non encapsulée ne peut pas être une autre Union non encapsulée</dt> <dd> Les unions transmises dans le cadre d’un appel de procédure distante nécessitent un élément de données associé, discriminante, qui sélectionne le bras d’Union. Les unions imbriquées dans d’autres unions n’offrent pas de discriminante ; par conséquent, ils ne peuvent pas être transmis sous cette forme. Créez une structure qui se compose de l’Union et de ses discriminante.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2222"></span><span id="midl2222"></span><dl> <dt><strong>MIDL2222</strong></dt> </dl></td>
<td><dl> <dt><span id="pointer_attribute_s__applied_on_an_embedded_array__ignored"></span><span id="POINTER_ATTRIBUTE_S__APPLIED_ON_AN_EMBEDDED_ARRAY__IGNORED"></span>attribut (s) pointeur appliqué (s) sur un tableau incorporé ; pas</dt> <dd> Un attribut de pointeur peut être appliqué à un tableau uniquement lorsque le tableau est un paramètre de niveau supérieur. Les autres attributs de pointeur appliqués aux tableaux incorporés dans d’autres structures de données sont ignorés.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2223"></span><span id="midl2223"></span><dl> <dt><strong>MIDL2223</strong></dt> </dl></td>
<td><dl> <dt><span id="_allocate__is_illegal_on_either_the_transmitted_or_presented_type_for__transmit_as____represent_as____wire_marshal___or__user_marshal_"></span><span id="_ALLOCATE__IS_ILLEGAL_ON_EITHER_THE_TRANSMITTED_OR_PRESENTED_TYPE_FOR__TRANSMIT_AS____REPRESENT_AS____WIRE_MARSHAL___OR__USER_MARSHAL_"></span>[Allocate] est non conforme sur le type transmis ou présenté pour [transmit_as], [represent_as], [wire_marshal] ou [user_marshal]</dt> <dd> Les attributs [<a href="transmit-as.md"><strong>transmit_as</strong></a>] et [<a href="allocate.md"><strong>allocate</strong></a>] ne peuvent pas être appliqués à la fois au même type. L’attribut [<strong>transmit_as</strong>] fait la distinction entre les types présentés et transmis, tandis que l’attribut [<strong>allocate</strong>] suppose que le type présenté est le même que le type transmis.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2224"></span><span id="midl2224"></span><dl> <dt><strong>MIDL2224</strong></dt> </dl></td>
<td>[switch_type] doit être spécifié dans ce mode d’importation<br/></td>
</tr>
<tr class="even">
<td><span id="MIDL2225"></span><span id="midl2225"></span><dl> <dt><strong>MIDL2225</strong></dt> </dl></td>
<td><dl> <dt><span id="_implicit_handle__type_undefined__assuming_generic_handle"></span><span id="_IMPLICIT_HANDLE__TYPE_UNDEFINED__ASSUMING_GENERIC_HANDLE"></span>[implicit_handle] le type n’est pas défini ; handle générique en supposant</dt> <dd> Le type de handle spécifié dans le ACF n’est pas défini dans le fichier IDL. Le compilateur MIDL suppose que le type de handle correspond au type de handle primitif <a href="handle-t.md"><strong>handle_t</strong></a>. Ajoutez l’attribut [<a href="handle.md"><strong>handle</strong></a>] à la définition de type si vous souhaitez que le handle se comporte comme un handle défini par l’utilisateur ou générique.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2226"></span><span id="midl2226"></span><dl> <dt><strong>MIDL2226</strong></dt> </dl></td>
<td><dl> <dt><span id="array_element_must_not_derive_from_error_status_t"></span><span id="ARRAY_ELEMENT_MUST_NOT_DERIVE_FROM_ERROR_STATUS_T"></span>l’élément de tableau ne doit pas dériver de error_status_t</dt> <dd> Dans cette version de Microsoft RPC, le type <a href="error-status-t.md"><strong>error_status_t</strong></a> peut apparaître uniquement en tant que paramètre ou type de retour. Il ne peut pas apparaître dans les tableaux.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2227"></span><span id="midl2227"></span><dl> <dt><strong>MIDL2227</strong></dt> </dl></td>
<td><dl> <dt><span id="_allocate__illegal_on_a_type_deriving_from_a_primitive_generic_context_handle"></span><span id="_ALLOCATE__ILLEGAL_ON_A_TYPE_DERIVING_FROM_A_PRIMITIVE_GENERIC_CONTEXT_HANDLE"></span>[Allocate] non conforme sur un type dérivant d’un handle primitif/générique/de contexte</dt> <dd> Par conception, l’attribut ACF [<a href="allocate.md"><strong>allocate</strong></a>] ne peut pas être appliqué aux types de handles.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2228"></span><span id="midl2228"></span><dl> <dt><strong>MIDL2228</strong></dt> </dl></td>
<td><dl> <dt><span id="transmitted_or_presented_type_must_not_derive_from_error_status_t"></span><span id="TRANSMITTED_OR_PRESENTED_TYPE_MUST_NOT_DERIVE_FROM_ERROR_STATUS_T"></span>le type transmis ou présenté ne doit pas dériver de error_status_t</dt> <dd> Dans cette version de Microsoft RPC, le type <a href="error-status-t.md"><strong>error_status_t</strong></a> ne peut pas être utilisé avec l’attribut [<a href="transmit-as.md"><strong>transmit_as</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2229"></span><span id="midl2229"></span><dl> <dt><strong>MIDL2229</strong></dt> </dl></td>
<td><dl> <dt><span id="discriminant_of_a_union_must_not_derive_from_a_field_with__ignore__applied_to_it"></span><span id="DISCRIMINANT_OF_A_UNION_MUST_NOT_DERIVE_FROM_A_FIELD_WITH__IGNORE__APPLIED_TO_IT"></span>discriminante d’une Union ne doit pas dériver d’un champ auquel [ignore] est appliqué</dt> <dd> Une Union utilisée dans un appel de procédure distante doit être associée à un autre élément de données, appelé discriminante, qui sélectionne le bras d’Union. Le discriminante doit être transmis. L’attribut [<a href="ignore.md"><strong>ignore</strong></a>] ne peut pas être appliqué à l’Union discriminante.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2230"></span><span id="midl2230"></span><dl> <dt><strong>MIDL2230</strong></dt> </dl></td>
<td><dl> <dt><span id="_nocode__ignored_for_server_side_since___server_none__not_specified"></span><span id="_NOCODE__IGNORED_FOR_SERVER_SIDE_SINCE___SERVER_NONE__NOT_SPECIFIED"></span>[nocode] ignoré pour le côté serveur, car &quot; /Server None &quot; n’est pas spécifié</dt> <dd> Certains compilateurs IDL DCE génèrent une erreur quand l’attribut [<a href="nocode.md"><strong>nocode</strong></a>] est appliqué à une procédure dans une interface pour laquelle des fichiers stub serveur sont générés. Étant donné que le serveur doit prendre en charge toutes les opérations, [<strong>nocode</strong>] ne doit pas être appliqué à une procédure dans ce mode, ou vous devez utiliser le commutateur du compilateur MIDL <a href="-server.md"><strong>/Server</strong></a> None pour spécifier explicitement qu’aucune routine de serveur ne doit être générée.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2231"></span><span id="midl2231"></span><dl> <dt><strong>MIDL2231</strong></dt> </dl></td>
<td><dl> <dt><span id="no_remote_procedures_specified_in_non-_local__interface__no_client_server_stubs_will_be_generated"></span><span id="NO_REMOTE_PROCEDURES_SPECIFIED_IN_NON-_LOCAL__INTERFACE__NO_CLIENT_SERVER_STUBS_WILL_BE_GENERATED"></span>aucune procédure distante spécifiée dans l’interface non [locale]; aucun stub client/serveur n’est généré</dt> <dd> L’interface fournie n’a pas de procédures distantes. par conséquent, seuls les fichiers d’en-tête seront générés.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2232"></span><span id="midl2232"></span><dl> <dt><strong>MIDL2232</strong></dt> </dl></td>
<td><dl> <dt><span id="too_many_default_cases_specified_for_encapsulated_union"></span><span id="TOO_MANY_DEFAULT_CASES_SPECIFIED_FOR_ENCAPSULATED_UNION"></span>trop de cas par défaut spécifiés pour l’Union encapsulée</dt> <dd> Une Union encapsulée ne peut avoir qu’une seule valeur par défaut : ARM.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2233"></span><span id="midl2233"></span><dl> <dt><strong>MIDL2233</strong></dt> </dl></td>
<td><dl> <dt><span id="too_many_default_interfaces_specified_for_coclass"></span><span id="TOO_MANY_DEFAULT_INTERFACES_SPECIFIED_FOR_COCLASS"></span>trop d’interfaces par défaut spécifiées pour la coclasse</dt> <dd> Une <a href="coclass.md"><strong>coclasse</strong></a> peut avoir au plus deux membres [<a href="default.md"><strong>default</strong></a>], l’un pour représenter l’interface sortante (source) ou dispinterface, et l’autre pour représenter l’interface entrante (sink) ou dispinterface.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2234"></span><span id="midl2234"></span><dl> <dt><strong>MIDL2234</strong></dt> </dl></td>
<td><dl> <dt><span id="items_with__defaultvtable__must_also_have__source_"></span><span id="ITEMS_WITH__DEFAULTVTABLE__MUST_ALSO_HAVE__SOURCE_"></span>les éléments avec [defaultvtable] doivent également avoir [source]</dt> <dd> L’interface <a href="defaultvtable.md"><strong>defaultvtable</strong></a> crée une deuxième interface source pour un objet, qui permet aux récepteurs de recevoir des événements via la V-table.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2235"></span><span id="midl2235"></span><dl> <dt><strong>MIDL2235</strong></dt> </dl></td>
<td><dl> <dt><span id="union_specification_with_no_fields_is_illegal"></span><span id="UNION_SPECIFICATION_WITH_NO_FIELDS_IS_ILLEGAL"></span>spécification d’Union sans champs non conforme</dt> <dd> Les unions doivent avoir au moins un champ.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2236"></span><span id="midl2236"></span><dl> <dt><strong>MIDL2236</strong></dt> </dl></td>
<td><dl> <dt><span id="value_out_of_range"></span><span id="VALUE_OUT_OF_RANGE"></span>valeur hors limites</dt> <dd> La valeur de cas fournie est en dehors de la plage du type de commutateur.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2237"></span><span id="midl2237"></span><dl> <dt><strong>MIDL2237</strong></dt> </dl></td>
<td><dl> <dt><span id="_context_handle__must_be_applied_on_a_pointer_type"></span><span id="_CONTEXT_HANDLE__MUST_BE_APPLIED_ON_A_POINTER_TYPE"></span>[context_handle] doit être appliqué à un type pointeur</dt> <dd> Les handles de contexte doivent toujours être des types pointeur. DCE spécifie que tous les descripteurs de contexte doivent être de type <strong>void *</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2238"></span><span id="midl2238"></span><dl> <dt><strong>MIDL2238</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_must_not_derive_from_handle_t"></span><span id="RETURN_TYPE_MUST_NOT_DERIVE_FROM_HANDLE_T"></span>le type de retour ne doit pas dériver de handle_t</dt> <dd><a href="handle-t.md"><strong>handle_t</strong></a> ne peut pas être retourné.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2239"></span><span id="midl2239"></span><dl> <dt><strong>MIDL2239</strong></dt> </dl></td>
<td><dl> <dt><span id="_handle__must_not_be_applied_to_a_type_deriving_from_a_context_handle"></span><span id="_HANDLE__MUST_NOT_BE_APPLIED_TO_A_TYPE_DERIVING_FROM_A_CONTEXT_HANDLE"></span>[handle] ne doit pas être appliqué à un type dérivant d’un handle de contexte</dt> <dd> Un type ne peut pas être à la fois un handle de contexte et un handle générique.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2240"></span><span id="midl2240"></span><dl> <dt><strong>MIDL2240</strong></dt> </dl></td>
<td><dl> <dt><span id="field_deriving_from_an__int__must_have_size_specifier__small____short___or__long__with_the__int_"></span><span id="FIELD_DERIVING_FROM_AN__INT__MUST_HAVE_SIZE_SPECIFIER__SMALL____SHORT___OR__LONG__WITH_THE__INT_"></span>le champ dérivant d’un &quot; int &quot; doit avoir un spécificateur de taille &quot; petit &quot; , &quot; court &quot; ou &quot; long &quot; avec l' &quot; entier&quot;</dt> <dd> Le type <a href="int.md"><strong>int</strong></a> n’est pas transmissible sur les systèmes 16 bits, car la taille de <strong>int</strong> peut être différente sur plusieurs ordinateurs.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2241"></span><span id="midl2241"></span><dl> <dt><strong>MIDL2241</strong></dt> </dl></td>
<td><dl> <dt><span id="field_must_not_derive_from_a_void_or_void__"></span><span id="FIELD_MUST_NOT_DERIVE_FROM_A_VOID_OR_VOID__"></span>le champ ne doit pas dériver de void ou void *</dt> <dd> <strong>void</strong> et <strong>void *</strong> ne peuvent pas être utilisés comme types de paramètres pour des procédures distantes.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2242"></span><span id="midl2242"></span><dl> <dt><strong>MIDL2242</strong></dt> </dl></td>
<td><dl> <dt><span id="field_must_not_derive_from_a_structure_containing_bit-fields"></span><span id="FIELD_MUST_NOT_DERIVE_FROM_A_STRUCTURE_CONTAINING_BIT-FIELDS"></span>le champ ne doit pas dériver d’une structure contenant des champs de bits</dt> <dd> Les structures contenant des champs de bits ne peuvent pas être utilisées comme paramètres ou types de retour pour les procédures distantes.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2243"></span><span id="midl2243"></span><dl> <dt><strong>MIDL2243</strong></dt> </dl></td>
<td><dl> <dt><span id="field_must_not_derive_from_a_non-rpcable_union"></span><span id="FIELD_MUST_NOT_DERIVE_FROM_A_NON-RPCABLE_UNION"></span>le champ ne doit pas dériver d’une Union non rpcable</dt> <dd> Une Union doit être spécifiée en tant qu’Union non encapsulée ou Union encapsulée afin d’être transmise. Les unions C ordinaires manquent les discriminante nécessaires pour transmettre l’Union sur le réseau.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2244"></span><span id="midl2244"></span><dl> <dt><strong>MIDL2244</strong></dt> </dl></td>
<td><dl> <dt><span id="field_must_not_derive_from_a_pointer_to_a_function"></span><span id="FIELD_MUST_NOT_DERIVE_FROM_A_POINTER_TO_A_FUNCTION"></span>le champ ne doit pas dériver d’un pointeur vers une fonction</dt> <dd> Les pointeurs vers des fonctions ne peuvent pas être transmis à des procédures distantes. Les pointeurs vers des fonctions pointent vers du code de fonction, et aucun code de fonction ne peut être transmis sur le réseau à l’aide de RPC.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2245"></span><span id="midl2245"></span><dl> <dt><strong>MIDL2245</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_use__fault_status__on_both_a_parameter_and_a_return_type"></span><span id="CANNOT_USE__FAULT_STATUS__ON_BOTH_A_PARAMETER_AND_A_RETURN_TYPE"></span>Impossible d’utiliser [fault_status] sur un paramètre et un type de retour</dt> <dd> L’attribut [<a href="fault-status.md"><strong>fault_status</strong></a>] ne peut être utilisé qu’une seule fois par procédure. L’attribut [<a href="comm-status.md"><strong>comm_status</strong></a>] peut être utilisé indépendamment.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2246"></span><span id="midl2246"></span><dl> <dt><strong>MIDL2246</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_too_complicated_for__Oi_modes__using__Os"></span><span id="return_type_too_complicated_for__oi_modes__using__os"></span><span id="RETURN_TYPE_TOO_COMPLICATED_FOR__OI_MODES__USING__OS"></span>type de retour trop compliqué pour les modes/OI, à l’aide de/OS</dt> <dd> Les types de retour volumineux passés par valeur ne peuvent être gérés que par des stubs d’optimisation <a href="-os.md"><strong>/OS</strong></a> . Les stubs pour cette routine seront générés à l’aide de l’optimisation de <strong>/OS</strong> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2247"></span><span id="midl2247"></span><dl> <dt><strong>MIDL2247</strong></dt> </dl></td>
<td><dl> <dt><span id="generic_handle_type_too_large_for__Oi_modes__using__Os"></span><span id="generic_handle_type_too_large_for__oi_modes__using__os"></span><span id="GENERIC_HANDLE_TYPE_TOO_LARGE_FOR__OI_MODES__USING__OS"></span>type de handle générique trop grand pour les modes/OI, à l’aide de/OS</dt> <dd> Les types de handles génériques volumineux qui sont passés par valeur ne peuvent être gérés que par des stubs d’optimisation <a href="-os.md"><strong>/OS</strong></a> . Les stubs pour cette routine seront générés à l’aide de l’optimisation de <strong>/OS</strong> .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2248"></span><span id="midl2248"></span><dl> <dt><strong>MIDL2248</strong></dt> </dl></td>
<td><dl> <dt><span id="_allocate_all_nodes___on_an__in_out__parameter_may_orphan_the_original_memory"></span><span id="_ALLOCATE_ALL_NODES___ON_AN__IN_OUT__PARAMETER_MAY_ORPHAN_THE_ORIGINAL_MEMORY"></span>[Allocate (all_nodes)] sur un paramètre [in, out] peut rendre orpheline la mémoire d’origine</dt> <dd> L’utilisation de [<a href="allocate.md"><strong>allocate</strong></a>(all_nodes)] sur un paramètre [<a href="in.md"><strong>in</strong></a>, <a href="out-idl.md"><strong>out</strong></a>] doit réallouer de la mémoire contiguë pour le sens [<strong>out</strong>], ce qui rend orphelin le paramètre [<strong>in</strong>]. Cette utilisation n’est pas recommandée.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2249"></span><span id="midl2249"></span><dl> <dt><strong>MIDL2249</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_have_a__ref__pointer_as_a_union_arm"></span><span id="CANNOT_HAVE_A__REF__POINTER_AS_A_UNION_ARM"></span>Impossible d’avoir un pointeur [ref] comme ARM d’Union</dt> <dd> Les pointeurs de référence doivent toujours pointer vers une mémoire valide, mais une Union [<a href="in.md"><strong>in</strong></a>, <a href="out-idl.md"><strong>out</strong></a>] avec un pointeur de référence peut retourner un pointeur de référence lorsque la direction [<strong>in</strong>] a utilisé un autre type.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2250"></span><span id="midl2250"></span><dl> <dt><strong>MIDL2250</strong></dt> </dl></td>
<td><dl> <dt><span id="return_of_context_handles_not_supported_for__Oi_modes__using__Os"></span><span id="return_of_context_handles_not_supported_for__oi_modes__using__os"></span><span id="RETURN_OF_CONTEXT_HANDLES_NOT_SUPPORTED_FOR__OI_MODES__USING__OS"></span>retour des handles de contexte non pris en charge pour les modes/OI, à l’aide de/OS</dt> <dd> MIDL ne prend pas en charge les handles de contexte dans les modes d’optimisation entièrement interprétés. Passage à l’optimisation en mode mixte.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2251"></span><span id="midl2251"></span><dl> <dt><strong>MIDL2251</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_the_extra__comm_status__or__fault_status__parameter_not_supported_for__Oi_modes__using__Os"></span><span id="use_of_the_extra__comm_status__or__fault_status__parameter_not_supported_for__oi_modes__using__os"></span><span id="USE_OF_THE_EXTRA__COMM_STATUS__OR__FAULT_STATUS__PARAMETER_NOT_SUPPORTED_FOR__OI_MODES__USING__OS"></span>l’utilisation du paramètre extra [comm_status] ou [fault_status] n’est pas prise en charge pour les modes/OI, à l’aide de/OS</dt> <dd> Les attributs [<a href="comm-status.md"><strong>comm_status</strong></a>] et [<a href="fault-status.md"><strong>fault_status</strong></a>] ne peuvent être gérés que par des stubs d’optimisation <a href="-os.md"><strong>/OS</strong></a> . Les stubs pour cette routine seront générés à l’aide de l’optimisation de <strong>/OS</strong> .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2252"></span><span id="midl2252"></span><dl> <dt><strong>MIDL2252</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_an_unknown_type_for__represent_as__or__user_marshal__not_supported_for__Oi_modes__using__Os"></span><span id="use_of_an_unknown_type_for__represent_as__or__user_marshal__not_supported_for__oi_modes__using__os"></span><span id="USE_OF_AN_UNKNOWN_TYPE_FOR__REPRESENT_AS__OR__USER_MARSHAL__NOT_SUPPORTED_FOR__OI_MODES__USING__OS"></span>l’utilisation d’un type inconnu pour [represent_as] ou [user_marshal] n’est pas prise en charge pour les modes/OI, à l’aide de/OS</dt> <dd> L’utilisation de l’attribut [<a href="represent-as.md"><strong>represent_as</strong></a>] avec un type local qui n’est pas défini dans le fichier IDL ou un fichier IDL importé ne peut être gérée que par les stubs d’optimisation <a href="-os.md"><strong>/OS</strong></a> . Les stubs pour cette routine seront générés à l’aide de l’optimisation de <strong>/OS</strong> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2253"></span><span id="midl2253"></span><dl> <dt><strong>MIDL2253</strong></dt> </dl></td>
<td><dl> <dt><span id="array_types_with__transmit_as__or__represent_as__not_supported_on_return_type_for__Oi_modes___using__Os"></span><span id="array_types_with__transmit_as__or__represent_as__not_supported_on_return_type_for__oi_modes___using__os"></span><span id="ARRAY_TYPES_WITH__TRANSMIT_AS__OR__REPRESENT_AS__NOT_SUPPORTED_ON_RETURN_TYPE_FOR__OI_MODES___USING__OS"></span>les types tableau avec [transmit_as] ou [represent_as] ne sont pas pris en charge sur le type de retour pour les modes/OI, à l’aide de/OS</dt> <dd> Le retour d’un tableau avec [<a href="transmit-as.md"><strong>transmit_as</strong></a>] ou [<a href="represent-as.md"><strong>represent_as</strong></a>] appliqué ne peut être géré que par des stubs d’optimisation <a href="-os.md"><strong>/OS</strong></a> . Les stubs pour cette routine seront générés à l’aide de l’optimisation de <strong>/OS</strong> .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2254"></span><span id="midl2254"></span><dl> <dt><strong>MIDL2254</strong></dt> </dl></td>
<td><dl> <dt><span id="array_types_with__transmit_as__or__represent_as__not_supported_pass-by-value_for__Oi_modes__using__Os"></span><span id="array_types_with__transmit_as__or__represent_as__not_supported_pass-by-value_for__oi_modes__using__os"></span><span id="ARRAY_TYPES_WITH__TRANSMIT_AS__OR__REPRESENT_AS__NOT_SUPPORTED_PASS-BY-VALUE_FOR__OI_MODES__USING__OS"></span>les types tableau avec [transmit_as] ou [represent_as] ne sont pas pris en charge par valeur pour les modes/OI, à l’aide de/OS</dt> <dd> Cette action n’est pas prise en charge pour l’optimisation entièrement interprétée. Passage à l’optimisation en mode mixte.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2255"></span><span id="midl2255"></span><dl> <dt><strong>MIDL2255</strong></dt> </dl></td>
<td><dl> <dt><span id="_callback__requires__ms_ext"></span><span id="_CALLBACK__REQUIRES__MS_EXT"></span>[callback] requiert/ms_ext</dt> <dd> L’attribut [<a href="callback.md"><strong>callback</strong></a>] est une extension Microsoft et requiert l’activation du commutateur <a href="-ms-ext.md"><strong>/ms_ext</strong></a> . Ne compilez pas avec <a href="-osf.md"><strong>/OSF</strong></a>, qui remplace <strong>/ms_ext</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2256"></span><span id="midl2256"></span><dl> <dt><strong>MIDL2256</strong></dt> </dl></td>
<td><dl> <dt><span id="circular_interface_dependency"></span><span id="CIRCULAR_INTERFACE_DEPENDENCY"></span>dépendance d’interface circulaire</dt> <dd> Cette interface s’utilise elle-même (directement ou indirectement) comme une interface de base.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2257"></span><span id="midl2257"></span><dl> <dt><strong>MIDL2257</strong></dt> </dl></td>
<td><dl> <dt><span id="only_IUnknown_may_be_used_as_the_root_interface"></span><span id="only_iunknown_may_be_used_as_the_root_interface"></span><span id="ONLY_IUNKNOWN_MAY_BE_USED_AS_THE_ROOT_INTERFACE"></span>seul IUnknown peut être utilisé en tant qu’interface racine</dt> <dd> Actuellement, toutes les interfaces doivent avoir <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a> comme interface racine.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2258"></span><span id="midl2258"></span><dl> <dt><strong>MIDL2258</strong></dt> </dl></td>
<td><dl> <dt><span id="_IID_IS__may_only_be_applied_to_pointers_to_interfaces"></span><span id="_iid_is__may_only_be_applied_to_pointers_to_interfaces"></span><span id="_IID_IS__MAY_ONLY_BE_APPLIED_TO_POINTERS_TO_INTERFACES"></span>[IID_IS] ne peut être appliqué qu’aux pointeurs vers des interfaces</dt> <dd> L’attribut [<a href="iid-is.md"><strong>iid_is</strong></a>] ne peut être appliqué qu’aux pointeurs d’interface, bien qu’ils puissent être spécifiés en tant que pointeurs vers <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a> *.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2259"></span><span id="midl2259"></span><dl> <dt><strong>MIDL2259</strong></dt> </dl></td>
<td><dl> <dt><span id="interfaces_may_only_be_used_in_pointer-to-interface_constructs"></span><span id="INTERFACES_MAY_ONLY_BE_USED_IN_POINTER-TO-INTERFACE_CONSTRUCTS"></span>les interfaces ne peuvent être utilisées que dans les constructions pointeur-à-interface</dt> <dd> Les noms d’interface ne peuvent pas être utilisés, sauf comme des interfaces de base ou des pointeurs d’interface.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2260"></span><span id="midl2260"></span><dl> <dt><strong>MIDL2260</strong></dt> </dl></td>
<td><dl> <dt><span id="interface_pointers_must_have_a_UUID_IID"></span><span id="interface_pointers_must_have_a_uuid_iid"></span><span id="INTERFACE_POINTERS_MUST_HAVE_A_UUID_IID"></span>les pointeurs d’interface doivent avoir un UUID/IID</dt> <dd> Le type de base de l’expression [<a href="iid-is.md"><strong>iid_is</strong></a>] doit être un type UUID/GUID/iid.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2261"></span><span id="midl2261"></span><dl> <dt><strong>MIDL2261</strong></dt> </dl></td>
<td><dl> <dt><span id="definitions_and_declarations_outside_of_interface_body_requires__ms_ext"></span><span id="DEFINITIONS_AND_DECLARATIONS_OUTSIDE_OF_INTERFACE_BODY_REQUIRES__MS_EXT"></span>les définitions et les déclarations en dehors du corps de l’interface requièrent/ms_ext</dt> <dd> Le fait de placer des déclarations et des définitions en dehors de tout corps d’interface est une extension Microsoft et requiert l’utilisation du commutateur <a href="-ms-ext.md"><strong>/ms_ext</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2262"></span><span id="midl2262"></span><dl> <dt><strong>MIDL2262</strong></dt> </dl></td>
<td><dl> <dt><span id="multiple_interfaces_in_one_file_requires__ms_ext"></span><span id="MULTIPLE_INTERFACES_IN_ONE_FILE_REQUIRES__MS_EXT"></span>plusieurs interfaces dans un fichier requièrent/ms_ext</dt> <dd> L’utilisation de plusieurs interfaces dans un seul fichier IDL est une extension Microsoft et n’est pas disponible quand vous compilez en mode <a href="-osf.md"><strong>/OSF</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2263"></span><span id="midl2263"></span><dl> <dt><strong>MIDL2263</strong></dt> </dl></td>
<td><dl> <dt><span id="only_one_of__implicit_handle____auto_handle___or__explicit_handle__allowed"></span><span id="ONLY_ONE_OF__IMPLICIT_HANDLE____AUTO_HANDLE___OR__EXPLICIT_HANDLE__ALLOWED"></span>une seule des [implicit_handle], [auto_handle] ou [explicit_handle] est autorisée</dt> <dd> Chaque interface ne peut avoir qu’un seul de ces trois attributs.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2264"></span><span id="midl2264"></span><dl> <dt><strong>MIDL2264</strong></dt> </dl></td>
<td><dl> <dt><span id="_implicit_handle__references_a_type_which_is_not_a_handle"></span><span id="_IMPLICIT_HANDLE__REFERENCES_A_TYPE_WHICH_IS_NOT_A_HANDLE"></span>[implicit_handle] référence un type qui n’est pas un handle</dt> <dd> Les handles implicites doivent être de l’un des types de handles.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2265"></span><span id="midl2265"></span><dl> <dt><strong>MIDL2265</strong></dt> </dl></td>
<td><dl> <dt><span id="_object__procs_may_only_be_used_with___env_win32_"></span><span id="_OBJECT__PROCS_MAY_ONLY_BE_USED_WITH___ENV_WIN32_"></span>[Object] les procédures peuvent uniquement être utilisées avec &quot; /env Win32&quot;</dt> <dd> Les interfaces avec l’attribut [<a href="object.md"><strong>Object</strong></a>] ne peuvent pas être utilisées avec des environnements 16 bits.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2266"></span><span id="midl2266"></span><dl> <dt><strong>MIDL2266</strong></dt> </dl></td>
<td><dl> <dt><span id="_callback__with_-env_dos_win16_not_supported_for__Oi__using__Os"></span><span id="_callback__with_-env_dos_win16_not_supported_for__oi__using__os"></span><span id="_CALLBACK__WITH_-ENV_DOS_WIN16_NOT_SUPPORTED_FOR__OI__USING__OS"></span>[callback] avec-env dos/Win16 non pris en charge pour/OI, à l’aide de/OS</dt> <dd> Les rappels dans les environnements 16 bits ne peuvent être gérés que par des stubs d’optimisation <a href="-os.md"><strong>/OS</strong></a> . Les stubs pour cette routine seront générés à l’aide de l’optimisation de <strong>/OS</strong> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2267"></span><span id="midl2267"></span><dl> <dt><strong>MIDL2267</strong></dt> </dl></td>
<td><dl> <dt><span id="float_double_not_supported_as_top-level_parameter_for__Oi_mode__using__Os"></span><span id="float_double_not_supported_as_top-level_parameter_for__oi_mode__using__os"></span><span id="FLOAT_DOUBLE_NOT_SUPPORTED_AS_TOP-LEVEL_PARAMETER_FOR__OI_MODE__USING__OS"></span>float/double non pris en charge en tant que paramètre de niveau supérieur pour le mode/OI, à l’aide de/OS</dt> <dd> Les types float et double peuvent uniquement être gérés en tant que paramètres par les stubs d’optimisation <a href="-os.md"><strong>/OS</strong></a> . Les stubs pour cette routine seront générés à l’aide de l’optimisation de <strong>/OS</strong> . Les types float et double dans les structures, les tableaux ou les unions peuvent toujours être gérés avec<strong>/OS</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2268"></span><span id="midl2268"></span><dl> <dt><strong>MIDL2268</strong></dt> </dl></td>
<td><dl> <dt><span id="pointers_to_context_handles_may_not_be_used_as_return_values"></span><span id="POINTERS_TO_CONTEXT_HANDLES_MAY_NOT_BE_USED_AS_RETURN_VALUES"></span>les pointeurs vers des handles de contexte ne peuvent pas être utilisés comme valeurs de retour</dt> <dd> Les handles de contexte doivent être utilisés en tant que valeurs de retour directes, pas en tant que valeurs de retour indirectes.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2269"></span><span id="midl2269"></span><dl> <dt><strong>MIDL2269</strong></dt> </dl></td>
<td><dl> <dt><span id="procedures_in_an_object_interface_must_return_an_HRESULT"></span><span id="procedures_in_an_object_interface_must_return_an_hresult"></span><span id="PROCEDURES_IN_AN_OBJECT_INTERFACE_MUST_RETURN_AN_HRESULT"></span>les procédures dans une interface d’objet doivent retourner un HRESULT</dt> <dd> Toutes les procédures dans une interface d’objet qui n’ont pas l’attribut-[<a href="local.md"><strong>local</strong></a>] doivent <strong></strong>retourner un / <strong>SCODE</strong>HRESULT.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2270"></span><span id="midl2270"></span><dl> <dt><strong>MIDL2270</strong></dt> </dl></td>
<td><dl> <dt><span id="duplicate_UUID"></span><span id="duplicate_uuid"></span><span id="DUPLICATE_UUID"></span>UUID en double</dt> <dd> Les mêmes que les UUID doivent être uniques.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2271"></span><span id="midl2271"></span><dl> <dt><strong>MIDL2271</strong></dt> </dl></td>
<td><dl> <dt><span id="_object__interfaces_must_derive_from_another__object__interface_such_as_IUnknown"></span><span id="_object__interfaces_must_derive_from_another__object__interface_such_as_iunknown"></span><span id="_OBJECT__INTERFACES_MUST_DERIVE_FROM_ANOTHER__OBJECT__INTERFACE_SUCH_AS_IUNKNOWN"></span>[Object] les interfaces doivent dériver d’une autre interface [Object] telle que IUnknown</dt> <dd> L’héritage de l’interface est autorisé uniquement lorsque vous utilisez des interfaces d’objet.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2272"></span><span id="midl2272"></span><dl> <dt><strong>MIDL2272</strong></dt> </dl></td>
<td><dl> <dt><span id="_async__interface_must_derive_from_another__async__interface"></span><span id="_ASYNC__INTERFACE_MUST_DERIVE_FROM_ANOTHER__ASYNC__INTERFACE"></span>l’interface (Async) doit dériver d’une autre interface (Async)</dt> <dd> Les interfaces d’objet, synchrones et asynchrones, doivent dériver de <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a> ou d’une autre interface OLE de base.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2273"></span><span id="midl2273"></span><dl> <dt><strong>MIDL2273</strong></dt> </dl></td>
<td><dl> <dt><span id="_IID_IS__expression_must_be_a_pointer_to_IID_structure"></span><span id="_iid_is__expression_must_be_a_pointer_to_iid_structure"></span><span id="_IID_IS__EXPRESSION_MUST_BE_A_POINTER_TO_IID_STRUCTURE"></span>[IID_IS] l’expression doit être un pointeur vers une structure IID</dt> <dd> Le type de base de l’expression [<a href="iid-is.md"><strong>iid_is</strong></a>] doit être un type UUID/GUID/iid.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2274"></span><span id="midl2274"></span><dl> <dt><strong>MIDL2274</strong></dt> </dl></td>
<td><dl> <dt><span id="_call_as__type_must_be_a__local__procedure"></span><span id="_CALL_AS__TYPE_MUST_BE_A__LOCAL__PROCEDURE"></span>[call_as] le type doit être une procédure [locale]</dt> <dd> La cible d’un type [<a href="call-as.md"><strong>call_as</strong></a>], si elle est définie, doit avoir [ <a href="local.md"><strong>local</strong></a>] appliqué.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2275"></span><span id="midl2275"></span><dl> <dt><strong>MIDL2275</strong></dt> </dl></td>
<td><dl> <dt><span id="undefined__call_as__must_not_be_used_in_an_object_interface"></span><span id="UNDEFINED__CALL_AS__MUST_NOT_BE_USED_IN_AN_OBJECT_INTERFACE"></span>le [call_as] non défini ne doit pas être utilisé dans une interface d’objet</dt> <dd> Vous devez définir la cible d’un type [<a href="call-as.md"><strong>call_as</strong></a>]. Assurez-vous que vous avez fourni <strong>call_as</strong> routines pour les applications appelantes et appelées.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2276"></span><span id="midl2276"></span><dl> <dt><strong>MIDL2276</strong></dt> </dl></td>
<td><dl> <dt><span id="_auto_handle__may_not_be_used_with__encode__or__decode_"></span><span id="_AUTO_HANDLE__MAY_NOT_BE_USED_WITH__ENCODE__OR__DECODE_"></span>[auto_handle] ne peut pas être utilisé avec [Encode] ou [Decode]</dt> <dd> Les attributs [ <a href="encode.md"><strong>encode</strong></a>] et [ <a href="decode.md"><strong>Decode</strong></a>] ne peuvent être utilisés qu’avec des handles explicites ou implicites.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2277"></span><span id="midl2277"></span><dl> <dt><strong>MIDL2277</strong></dt> </dl></td>
<td><dl> <dt><span id="normal_procedures_are_not_allowed_in_an_interface_with__encode__or__decode_"></span><span id="NORMAL_PROCEDURES_ARE_NOT_ALLOWED_IN_AN_INTERFACE_WITH__ENCODE__OR__DECODE_"></span>les procédures normales ne sont pas autorisées dans une interface avec [Encode] ou [Decode]</dt> <dd> Les interfaces contenant des procédures [<a href="encode.md"><strong>encode</strong></a>] ou [<a href="decode.md"><strong>Decode</strong></a>] ne peuvent pas également avoir de procédures distantes.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2278"></span><span id="midl2278"></span><dl> <dt><strong>MIDL2278</strong></dt> </dl></td>
<td><dl> <dt><span id="top-level_conformance_or_variance_not_allowed_with__encode__or__decode_"></span><span id="TOP-LEVEL_CONFORMANCE_OR_VARIANCE_NOT_ALLOWED_WITH__ENCODE__OR__DECODE_"></span>la conformité ou la variance de niveau supérieur ne sont pas autorisées avec [Encode] ou [Decode]</dt> <dd> Les types qui ont une conformité ou une variance de niveau supérieur ne peuvent pas utiliser la sérialisation de type, car il n’existe aucun moyen de fournir le dimensionnement/l’augmentation. Les structures qui les contiennent sont, toutefois, autorisées à utiliser la sérialisation de type.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2279"></span><span id="midl2279"></span><dl> <dt><strong>MIDL2279</strong></dt> </dl></td>
<td><dl> <dt><span id="_out__parameters_may_not_have__const_"></span><span id="_OUT__PARAMETERS_MAY_NOT_HAVE__CONST_"></span>[out] les paramètres ne peuvent pas avoir &quot; const&quot;</dt> <dd> Étant donné qu’un paramètre [<a href="out-idl.md"><strong>out</strong></a>] est modifié, il ne doit pas être déclaré comme une constante sa.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2280"></span><span id="midl2280"></span><dl> <dt><strong>MIDL2280</strong></dt> </dl></td>
<td><dl> <dt><span id="return_values_may_not_have__const_"></span><span id="RETURN_VALUES_MAY_NOT_HAVE__CONST_"></span>les valeurs de retour ne peuvent pas avoir &quot; const&quot;</dt> <dd> Dans la mesure où une valeur de fonction est définie au retour de la fonction, cette valeur ne doit pas être déclarée comme constante.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2281"></span><span id="midl2281"></span><dl> <dt><strong>MIDL2281</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid_use_of__retval__attribute"></span><span id="INVALID_USE_OF__RETVAL__ATTRIBUTE"></span>utilisation non valide de l' &quot; &quot; attribut retval</dt> <dd> Vérifiez que vous n’avez pas utilisé l’attribut [<a href="optional.md"><strong>Optional</strong></a>] et que le paramètre [<a href="retval.md"><strong>retVal</strong></a>] est le dernier paramètre de la liste.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2282"></span><span id="midl2282"></span><dl> <dt><strong>MIDL2282</strong></dt> </dl></td>
<td><dl> <dt><span id="multiple_calling_conventions_illegal"></span><span id="MULTIPLE_CALLING_CONVENTIONS_ILLEGAL"></span>conventions d’appel multiples non conformes</dt> <dd> Une seule convention d’appel peut être appliquée à une procédure unique.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2283"></span><span id="midl2283"></span><dl> <dt><strong>MIDL2283</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_illegal_on__object__procedure"></span><span id="ATTRIBUTE_ILLEGAL_ON__OBJECT__PROCEDURE"></span>attribut non conforme sur la procédure [Object]</dt> <dd> L’attribut ci-dessus s’applique uniquement aux procédures des interfaces qui n’ont pas l’attribut [<a href="object.md"><strong>Object</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2284"></span><span id="midl2284"></span><dl> <dt><strong>MIDL2284</strong></dt> </dl></td>
<td><dl> <dt><span id="_out__interface_pointers_must_use_double_indirection"></span><span id="_OUT__INTERFACE_POINTERS_MUST_USE_DOUBLE_INDIRECTION"></span>[out] les pointeurs d’interface doivent utiliser une double indirection</dt> <dd> Étant donné que la valeur modifiée est le pointeur vers l’interface, il doit y avoir un autre niveau d’indirection au-dessus du pointeur pour lui permettre d’être retourné.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2285"></span><span id="midl2285"></span><dl> <dt><strong>MIDL2285</strong></dt> </dl></td>
<td><dl> <dt><span id="procedure_used_twice_as_the_caller_in__call_as_"></span><span id="PROCEDURE_USED_TWICE_AS_THE_CALLER_IN__CALL_AS_"></span>procédure utilisée deux fois en tant qu’appelant dans [call_as]</dt> <dd> Une procédure [<a href="local.md"><strong>locale</strong></a>] donnée ne peut être utilisée qu’une seule fois en tant que cible d’un [<a href="call-as.md"><strong>call_as</strong></a>], afin d’éviter les conflits de noms.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2286"></span><span id="midl2286"></span><dl> <dt><strong>MIDL2286</strong></dt> </dl></td>
<td><dl> <dt><span id="_call_as__target_must_have__local__in_an_object_interface"></span><span id="_CALL_AS__TARGET_MUST_HAVE__LOCAL__IN_AN_OBJECT_INTERFACE"></span>[call_as] la cible doit avoir [local] dans une interface d’objet</dt> <dd> La cible d’un [<a href="call-as.md"><strong>call_as</strong></a>] doit être une procédure [<a href="local.md"><strong>locale</strong></a>] définie dans l’interface actuelle.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2287"></span><span id="midl2287"></span><dl> <dt><strong>MIDL2287</strong></dt> </dl></td>
<td><dl> <dt><span id="_code__and__nocode__may_not_be_used_together"></span><span id="_CODE__AND__NOCODE__MAY_NOT_BE_USED_TOGETHER"></span>[code] et [nocode] ne peuvent pas être utilisés ensemble</dt> <dd> Ces deux attributs sont contradictoires et ne peuvent pas être utilisés ensemble.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2288"></span><span id="midl2288"></span><dl> <dt><strong>MIDL2288</strong></dt> </dl></td>
<td><dl> <dt><span id="procedures_with__maybe__or__message__attributes_may_not_have__out__params__or_return_values_must_be_of_type_HRESULT_or_error_status_t"></span><span id="procedures_with__maybe__or__message__attributes_may_not_have__out__params__or_return_values_must_be_of_type_hresult_or_error_status_t"></span><span id="PROCEDURES_WITH__MAYBE__OR__MESSAGE__ATTRIBUTES_MAY_NOT_HAVE__OUT__PARAMS__OR_RETURN_VALUES_MUST_BE_OF_TYPE_HRESULT_OR_ERROR_STATUS_T"></span>les procédures avec les attributs [peut] ou [message] ne peuvent pas avoir [out] paramètres, ou les valeurs de retour doivent être de type HRESULT ou error_status_t</dt> <dd> Étant donné que les procédures [<a href="maybe.md"><strong>peut-être</strong></a>] ne retournent jamais, il n’existe aucun moyen d’obtenir des valeurs de retour.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2289"></span><span id="midl2289"></span><dl> <dt><strong>MIDL2289</strong></dt> </dl></td>
<td><dl> <dt><span id="pointer_to_function_must_be_used"></span><span id="POINTER_TO_FUNCTION_MUST_BE_USED"></span>un pointeur vers une fonction doit être utilisé</dt> <dd> Bien que les définitions de type fonction soient autorisées en mode <a href="-c-ext.md"><strong>/c_ext</strong></a> , elles peuvent uniquement être utilisées comme pointeurs vers des fonctions. Elles ne peuvent jamais être transmises en tant que paramètre ou valeur de retour d’une procédure distante.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2290"></span><span id="midl2290"></span><dl> <dt><strong>MIDL2290</strong></dt> </dl></td>
<td><dl> <dt><span id="functions_may_not_be_passed_in_an_RPC_operation"></span><span id="functions_may_not_be_passed_in_an_rpc_operation"></span><span id="FUNCTIONS_MAY_NOT_BE_PASSED_IN_AN_RPC_OPERATION"></span>les fonctions ne peuvent pas être passées dans une opération RPC</dt> <dd> Les fonctions et les pointeurs fonction ne peuvent pas être passés en tant que paramètres ou valeurs de retour de procédures distantes.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2291"></span><span id="midl2291"></span><dl> <dt><strong>MIDL2291</strong></dt> </dl></td>
<td><dl> <dt><span id="hyper_double_not_supported_as_return_value_for__Oi_modes__using__Os"></span><span id="hyper_double_not_supported_as_return_value_for__oi_modes__using__os"></span><span id="HYPER_DOUBLE_NOT_SUPPORTED_AS_RETURN_VALUE_FOR__OI_MODES__USING__OS"></span>Hyper/double non pris en charge comme valeur de retour pour les modes/OI, à l’aide de/OS</dt> <dd> Les valeurs de retour hyper et double peuvent être gérées uniquement par les stubs d’optimisation <a href="-os.md"><strong>/OS</strong></a> . Les stubs pour cette routine seront générés à l’aide de l’optimisation de <strong>/OS</strong> .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2292"></span><span id="midl2292"></span><dl> <dt><strong>MIDL2292</strong></dt> </dl></td>
<td><dl> <dt><span id="_pragma_pack_pop__without_matching__pragma_pack_push_"></span><span id="_PRAGMA_PACK_POP__WITHOUT_MATCHING__PRAGMA_PACK_PUSH_"></span>#pragma Pack (POP) sans #pragma Pack correspondant (push)</dt> <dd> #pragma Pack (push) et #pragma Pack (POP) doivent apparaître dans les paires correspondantes. Au moins un trop grand nombre de #pragma Pack (push) s ont été spécifiés.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2293"></span><span id="midl2293"></span><dl> <dt><strong>MIDL2293</strong></dt> </dl></td>
<td><dl> <dt><span id="stringable_structure_fields_must_be_byte_char_wchar_t"></span><span id="STRINGABLE_STRUCTURE_FIELDS_MUST_BE_BYTE_CHAR_WCHAR_T"></span>les champs de structure stringable doivent être de type Byte/char/wchar_t</dt> <dd> Le type [<a href="string.md"><strong>String</strong></a>] ne peut être appliqué qu’à une structure dont les champs sont de type Byte, ou une définition de type équivalant à Byte.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2294"></span><span id="midl2294"></span><dl> <dt><strong>MIDL2294</strong></dt> </dl></td>
<td><dl> <dt><span id="_notify__not_supported_for__Oi_modes__using__Os"></span><span id="_notify__not_supported_for__oi_modes__using__os"></span><span id="_NOTIFY__NOT_SUPPORTED_FOR__OI_MODES__USING__OS"></span>[Notify] non pris en charge pour les modes/OI, à l’aide de/OS</dt> <dd> L’attribut [<a href="notify.md"><strong>Notify</strong></a>] ne peut être traité que par des stubs d’optimisation <a href="-os.md"><strong>/OS</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2295"></span><span id="midl2295"></span><dl> <dt><strong>MIDL2295</strong></dt> </dl></td>
<td><dl> <dt><span id="_handle_parameter_or_return_type_is_not_supported_on_a_procedure_in_an__object__interface"></span><span id="_HANDLE_PARAMETER_OR_RETURN_TYPE_IS_NOT_SUPPORTED_ON_A_PROCEDURE_IN_AN__OBJECT__INTERFACE"></span> le paramètre de handle ou le type de retour n’est pas pris en charge sur une procédure dans une interface [Object]</dt> <dd> Les handles ne peuvent pas être utilisés avec les interfaces [ <a href="object.md"><strong>Object</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2296"></span><span id="midl2296"></span><dl> <dt><strong>MIDL2296</strong></dt> </dl></td>
<td><dl> <dt><span id="ANSI_C_only_allows_the_leftmost_array_bound_to_be_unspecified"></span><span id="ansi_c_only_allows_the_leftmost_array_bound_to_be_unspecified"></span><span id="ANSI_C_ONLY_ALLOWS_THE_LEFTMOST_ARRAY_BOUND_TO_BE_UNSPECIFIED"></span>ANSI C autorise uniquement l’non-spécification de la liaison du tableau à l’extrême gauche</dt> <dd> Dans un tableau conforme, ANSI C autorise l’non-spécification du tableau le plus à gauche (le plus significatif) lié. Si plusieurs dimensions sont conformes, MIDL tente de placer un &quot; 1 &quot; dans les autres dimensions conformes. Si les autres dimensions sont définies dans une définition de type différente, cela ne peut pas être possible. Essayez de placer toutes les dimensions du tableau dans la déclaration de tableau pour éviter cela. Dans tous les cas, Méfiez-vous des calculs d’indexation de tableau effectués par le compilateur ; vous devrez peut-être effectuer vos propres calculs à l’aide des tailles réelles.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2297"></span><span id="midl2297"></span><dl> <dt><strong>MIDL2297</strong></dt> </dl></td>
<td><dl> <dt><span id="by-value_union_parameters_not_supported_for__Oi_modes__using__Os"></span><span id="by-value_union_parameters_not_supported_for__oi_modes__using__os"></span><span id="BY-VALUE_UNION_PARAMETERS_NOT_SUPPORTED_FOR__OI_MODES__USING__OS"></span>paramètres d’Union par valeur non pris en charge pour les modes/OI, à l’aide de/OS</dt> <dd> Cette action n’est pas prise en charge pour l’optimisation entièrement interprétée. Passage à l’optimisation en mode mixte.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2298"></span><span id="midl2298"></span><dl> <dt><strong>MIDL2298</strong></dt> </dl></td>
<td><dl> <dt><span id="_version__attribute_is_ignored_on_an__object__interface"></span><span id="_VERSION__ATTRIBUTE_IS_IGNORED_ON_AN__OBJECT__INTERFACE"></span>l’attribut [version] est ignoré sur une interface [Object]</dt> <dd> L’attribut [<a href="object.md"><strong>Object</strong></a>] identifie une interface com. Une liste d’attributs d’interface pour une interface COM ne peut pas inclure l’attribut [ <a href="version.md"><strong>version</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2299"></span><span id="midl2299"></span><dl> <dt><strong>MIDL2299</strong></dt> </dl></td>
<td><dl> <dt><span id="_size_is__or__max_is__attribute_is_invalid_on_a_fixed_array"></span><span id="_SIZE_IS__OR__MAX_IS__ATTRIBUTE_IS_INVALID_ON_A_FIXED_ARRAY"></span>l’attribut [size_is] ou [max_is] n’est pas valide sur un tableau fixe</dt> <dd> Les tableaux de taille fixe ne peuvent pas utiliser les attributs <a href="size-is.md"><strong>size_is</strong></a> ou <a href="max-is.md"><strong>max_is</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2300"></span><span id="midl2300"></span><dl> <dt><strong>MIDL2300</strong></dt> </dl></td>
<td><dl> <dt><span id="_encode__or__decode__are_invalid_in_an__object__interface"></span><span id="_ENCODE__OR__DECODE__ARE_INVALID_IN_AN__OBJECT__INTERFACE"></span>[Encode] ou [Decode] ne sont pas valides dans une interface [Object]</dt> <dd> L’attribut [<a href="object.md"><strong>Object</strong></a>] identifie une interface com. Les attributs [<a href="encode.md"><strong>encode</strong></a>] et [ <a href="decode.md"><strong>Decode</strong></a>] activent la sérialisation. Autrement dit, vous pouvez fournir et contrôler des mémoires tampons pour le marshaling et le démarshaling de données. Toutefois, vous ne pouvez pas effectuer de sérialisation sur les interfaces COM.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2301"></span><span id="midl2301"></span><dl> <dt><strong>MIDL2301</strong></dt> </dl></td>
<td><dl> <dt><span id="_encode__or__decode__on_a_type_requires__ms_ext"></span><span id="_ENCODE__OR__DECODE__ON_A_TYPE_REQUIRES__MS_EXT"></span>[Encode] ou [Decode] sur un type requiert/ms_ext</dt> <dd> La sérialisation ne fait pas partie de la spécification DCE-IDL. Il s’agit d’une extension Microsoft qui requiert l’utilisation du commutateur de ligne de commande <a href="-ms-ext.md"><strong>/ms_ext</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2302"></span><span id="midl2302"></span><dl> <dt><strong>MIDL2302</strong></dt> </dl></td>
<td><dl> <dt><span id="int_not_supported_on__env_win16_or__env_dos"></span><span id="INT_NOT_SUPPORTED_ON__ENV_WIN16_OR__ENV_DOS"></span>int non pris en charge sur les dos/env ou/env</dt> <dd> Les plateformes Microsoft 16 bits ne prennent pas en charge l’utilisation du type <a href="int.md"><strong>int</strong></a> dans un fichier IDL. Qualifiez le type <strong>int</strong> avec <a href="small.md"><strong>Small</strong></a>, <a href="short.md"><strong>short</strong></a>ou <a href="long.md"><strong>long</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2303"></span><span id="midl2303"></span><dl> <dt><strong>MIDL2303</strong></dt> </dl></td>
<td><dl> <dt><span id="_bstring__may_only_be_applied_to_a_pointer_to__char__or__whchar_t_"></span><span id="_BSTRING__MAY_ONLY_BE_APPLIED_TO_A_POINTER_TO__CHAR__OR__WHCHAR_T_"></span>[bString] ne peut être appliqué qu’à un pointeur vers &quot; char &quot; ou &quot; whchar_t&quot;</dt> <dd> Cette erreur est obsolète. Elle est fournie uniquement à des fins de compatibilité descendante.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2304"></span><span id="midl2304"></span><dl> <dt><strong>MIDL2304</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_invalid_on_a_procedure_in_an__object__interface"></span><span id="ATTRIBUTE_INVALID_ON_A_PROCEDURE_IN_AN__OBJECT__INTERFACE"></span>attribut non valide sur une procédure dans une interface [Object]</dt> <dd> L’attribut spécifié n’est pas autorisé dans une procédure dans une interface COM.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2305"></span><span id="midl2305"></span><dl> <dt><strong>MIDL2305</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_invalid_on_an__object__interface"></span><span id="ATTRIBUTE_INVALID_ON_AN__OBJECT__INTERFACE"></span>attribut non valide sur une interface [Object]</dt> <dd> L’attribut spécifié n’est pas autorisé dans une interface COM.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2306"></span><span id="midl2306"></span><dl> <dt><strong>MIDL2306</strong></dt> </dl></td>
<td><dl> <dt><span id="too_many_parameters_or_stack_too_big_for__Oi_modes__using__Os"></span><span id="too_many_parameters_or_stack_too_big_for__oi_modes__using__os"></span><span id="TOO_MANY_PARAMETERS_OR_STACK_TOO_BIG_FOR__OI_MODES__USING__OS"></span>trop de paramètres ou Stack trop grand pour les modes/OI, à l’aide de/OS</dt> <dd> Cet avertissement est obsolète. Elle est fournie uniquement à des fins de compatibilité descendante. Elle indique que l’appel à la procédure distante entraîne une augmentation de la taille de la pile supérieure à 64 K.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2307"></span><span id="midl2307"></span><dl> <dt><strong>MIDL2307</strong></dt> </dl></td>
<td><dl> <dt><span id="no_attributes_on_ACF_file_typedef__so_no_effect"></span><span id="no_attributes_on_acf_file_typedef__so_no_effect"></span><span id="NO_ATTRIBUTES_ON_ACF_FILE_TYPEDEF__SO_NO_EFFECT"></span>aucun attribut sur le fichier ACF typedef, donc aucun effet</dt> <dd> Le fichier IDL doit contenir toutes les instructions typedef qui n’ont pas d’attributs. Ils ne doivent pas se produire dans les fichiers ACF. Si c’est le cas, le compilateur MIDL les interprète comme étant redondants et les ignore.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2308"></span><span id="midl2308"></span><dl> <dt><strong>MIDL2308</strong></dt> </dl></td>
<td><dl> <dt><span id="calling_conventions_other_than___stdcall_or___cdecl_not_supported_for__Oi_modes__using__Os"></span><span id="calling_conventions_other_than___stdcall_or___cdecl_not_supported_for__oi_modes__using__os"></span><span id="CALLING_CONVENTIONS_OTHER_THAN___STDCALL_OR___CDECL_NOT_SUPPORTED_FOR__OI_MODES__USING__OS"></span>conventions d’appel autres que __stdcall ou __cdecl non prises en charge pour les modes/OI, à l’aide de/OS</dt> <dd> Les conventions d’appel telles que <strong>__pascal</strong> ou <strong>__fastcall</strong> modifier le format de la pile. Les modes <a href="-oi.md"><strong>/OI</strong></a> prennent uniquement en charge les conventions d’appel <strong>__stdcall</strong> et <strong>__cdecl</strong> . Si vous devez utiliser d’autres conventions d’appel, utilisez le mode <a href="-os.md"><strong>/OS</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2309"></span><span id="midl2309"></span><dl> <dt><strong>MIDL2309</strong></dt> </dl></td>
<td><dl> <dt><span id="Too_many_delegation_methods_in_the_interface__require_Windows_2000_or_greater"></span><span id="too_many_delegation_methods_in_the_interface__require_windows_2000_or_greater"></span><span id="TOO_MANY_DELEGATION_METHODS_IN_THE_INTERFACE__REQUIRE_WINDOWS_2000_OR_GREATER"></span>un trop grand nombre de méthodes de délégation dans l’interface nécessitent Windows 2000 ou une version ultérieure</dt> <dd> Une interface peut hériter d’une autre. Dans ce cas, les méthodes de l’interface de base sont considérées comme déléguées. Aucune interface dérivée ne peut contenir plus de 256 méthodes déléguées.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2310"></span><span id="midl2310"></span><dl> <dt><strong>MIDL2310</strong></dt> </dl></td>
<td><dl> <dt><span id="auto_handles_not_supported_with__env_mac_or__env_powermac"></span><span id="AUTO_HANDLES_NOT_SUPPORTED_WITH__ENV_MAC_OR__ENV_POWERMAC"></span>Handles auto non pris en charge avec/env Mac ou/env PowerMac</dt> <dd> Lors de la compilation de votre fichier IDL pour un PowerMac, vous ne pouvez pas utiliser de handles de liaison automatiques. Vous devez spécifier des handles explicites ou implicites.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2311"></span><span id="midl2311"></span><dl> <dt><strong>MIDL2311</strong></dt> </dl></td>
<td><dl> <dt><span id="statements_outside_library_block_are_illegal_in_mktyplib_compatibility_mode"></span><span id="STATEMENTS_OUTSIDE_LIBRARY_BLOCK_ARE_ILLEGAL_IN_MKTYPLIB_COMPATIBILITY_MODE"></span>les instructions en dehors du bloc de bibliothèque ne sont pas conformes dans le mode de compatibilité mktyplib</dt> <dd> Vous devrez peut-être spécifier le commutateur de ligne de commande <a href="-mktyplib203.md"><strong>/mktyplib203</strong></a> quand vous compilerez votre fichier IDL.<br/>
<blockquote>
[!Note]<br />
L’outil Mktyplib.exe est obsolète. Utilisez plutôt le compilateur MIDL.
</blockquote>
<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2312"></span><span id="midl2312"></span><dl> <dt><strong>MIDL2312</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_syntax_unless_using_mktyplib_compatibility_mode"></span><span id="ILLEGAL_SYNTAX_UNLESS_USING_MKTYPLIB_COMPATIBILITY_MODE"></span>syntaxe non conforme, sauf en utilisant le mode de compatibilité mktyplib</dt> <dd> Vous devrez peut-être spécifier le commutateur de ligne de commande <a href="-mktyplib203.md"><strong>/mktyplib203</strong></a> quand vous compilerez votre fichier IDL.<br/>
<blockquote>
[!Note]<br />
L’outil Mktyplib.exe est obsolète. Utilisez plutôt le compilateur MIDL.
</blockquote>
<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2313"></span><span id="midl2313"></span><dl> <dt><strong>MIDL2313</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_definition__must_use_typedef_in_mktyplib_compatibility_mode"></span><span id="ILLEGAL_DEFINITION__MUST_USE_TYPEDEF_IN_MKTYPLIB_COMPATIBILITY_MODE"></span>définition non conforme, doit utiliser typedef en mode de compatibilité mktyplib</dt> <dd> Vous devrez peut-être spécifier le commutateur de ligne de commande <a href="-mktyplib203.md"><strong>/mktyplib203</strong></a> quand vous compilerez votre fichier IDL.<br/>
<blockquote>
[!Note]<br />
L’outil Mktyplib.exe est obsolète. Utilisez plutôt le compilateur MIDL.
</blockquote>
<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2314"></span><span id="midl2314"></span><dl> <dt><strong>MIDL2314</strong></dt> </dl></td>
<td><dl> <dt><span id="explicit_pointer_attribute__ptr___ref__ignored_for_interface_pointers"></span><span id="EXPLICIT_POINTER_ATTRIBUTE__PTR___REF__IGNORED_FOR_INTERFACE_POINTERS"></span>attribut de pointeur explicite [PTR] [ref] ignoré pour les pointeurs d’interface</dt> <dd> Les pointeurs vers des interfaces ne peuvent pas avoir d’attributs IDL.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2315"></span><span id="midl2315"></span><dl> <dt><strong>MIDL2315</strong></dt> </dl></td>
<td>Modes <a href="-oi.md"><strong>/OI</strong></a> non implémentés pour PowerMac, basculer vers <a href="-os.md"> <strong>/OS</strong></a><br/></td>
</tr>
<tr class="odd">
<td><span id="MIDL2316"></span><span id="midl2316"></span><dl> <dt><strong>MIDL2316</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_expression_type_used_in_attribute"></span><span id="ILLEGAL_EXPRESSION_TYPE_USED_IN_ATTRIBUTE"></span>type d’expression non conforme utilisé dans l’attribut</dt> <dd> La valeur par défaut du pointeur doit être une constante.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2317"></span><span id="midl2317"></span><dl> <dt><strong>MIDL2317</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_type_used_in_pipe"></span><span id="ILLEGAL_TYPE_USED_IN_PIPE"></span>type non conforme utilisé dans le canal</dt> <dd> Les canaux sont limités aux types de données IDL de base. Par exemple, vous ne pouvez pas spécifier un canal de tableaux.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2318"></span><span id="midl2318"></span><dl> <dt><strong>MIDL2318</strong></dt> </dl></td>
<td><dl> <dt><span id="procedure_uses_pipes__using__Oicf"></span><span id="procedure_uses_pipes__using__oicf"></span><span id="PROCEDURE_USES_PIPES__USING__OICF"></span>la procédure utilise des canaux à l’aide de/Oicf</dt> <dd> Le mode que vous avez sélectionné ne prend pas en charge les canaux. Le compilateur MIDL a détecté l’utilisation d’un ou plusieurs canaux dans votre interface. Par conséquent, il compile votre fichier IDL en mode <a href="-oi.md"><strong>/Oicf</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2319"></span><span id="midl2319"></span><dl> <dt><strong>MIDL2319</strong></dt> </dl></td>
<td><dl> <dt><span id="procedure_has_an_attribute_that_requires_use_of__Oif__switching_modes"></span><span id="procedure_has_an_attribute_that_requires_use_of__oif__switching_modes"></span><span id="PROCEDURE_HAS_AN_ATTRIBUTE_THAT_REQUIRES_USE_OF__OIF__SWITCHING_MODES"></span>la procédure a un attribut qui requiert l’utilisation de/OIF, les modes de basculement</dt> <dd> Vous devez compiler les procédures [<a href="async.md"><strong>Async</strong></a>] en mode <a href="-oi.md"><strong>/OIF</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2320"></span><span id="midl2320"></span><dl> <dt><strong>MIDL2320</strong></dt> </dl></td>
<td><dl> <dt><span id="conflicting_optimization_requirements__cannot_optimize"></span><span id="CONFLICTING_OPTIMIZATION_REQUIREMENTS__CANNOT_OPTIMIZE"></span>exigences d’optimisation en conflit, impossible d’optimiser</dt> <dd> Cette erreur indique souvent que vous avez spécifié à la fois les modes de compilateur <a href="-os.md"><strong>/OS</strong></a> et <a href="-oi.md"><strong>/OI</strong></a> (ou une variante de <strong>/OI</strong>). Cela peut également signifier que les fonctionnalités que vous avez spécifiées dans vos fichiers IDL et ACL requièrent l’utilisation des deux modes. Vous devez sélectionner un mode ou l’autre pour l’optimiser.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2321"></span><span id="midl2321"></span><dl> <dt><strong>MIDL2321</strong></dt> </dl></td>
<td><dl> <dt><span id="pipes_cannot_be_array_elements__or_members_of_structures_or_unions"></span><span id="PIPES_CANNOT_BE_ARRAY_ELEMENTS__OR_MEMBERS_OF_STRUCTURES_OR_UNIONS"></span>les canaux ne peuvent pas être des éléments de tableau ou des membres de structures ou d’unions</dt> <dd> Les types de données de canal ne peuvent être que des paramètres de niveau supérieur.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2322"></span><span id="midl2322"></span><dl> <dt><strong>MIDL2322</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid_pipe_usage"></span><span id="INVALID_PIPE_USAGE"></span>utilisation du canal non valide</dt> <dd> Vous ne pouvez pas utiliser de canaux avec les attributs [<a href="transmit-as.md"><strong>transmit_as</strong></a>], [<a href="represent-as.md"><strong>represent_as</strong></a>] ou [<a href="user-marshal.md"><strong>user_marshal</strong></a>]. En outre, les canaux ne peuvent pas être utilisés en tant que types de retour.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2323"></span><span id="midl2323"></span><dl> <dt><strong>MIDL2323</strong></dt> </dl></td>
<td><dl> <dt><span id="feature_requires_the_advanced_interpreted_optimization_option__use_-Oicf"></span><span id="feature_requires_the_advanced_interpreted_optimization_option__use_-oicf"></span><span id="FEATURE_REQUIRES_THE_ADVANCED_INTERPRETED_OPTIMIZATION_OPTION__USE_-OICF"></span>la fonctionnalité nécessite l’option d’optimisation interprétée avancée ; utilisation de-Oicf</dt> <dd> Cette erreur indique que les commutateurs de ligne de commande du compilateur MIDL tels que <a href="-robust.md"><strong>/Robust</strong></a> requièrent l’utilisation du mode <a href="-oi.md"><strong>/Oicf</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2324"></span><span id="midl2324"></span><dl> <dt><strong>MIDL2324</strong></dt> </dl></td>
<td><dl> <dt><span id="feature_requires_the_advanced_interpreted_optimization_option__use_-Oicf"></span><span id="feature_requires_the_advanced_interpreted_optimization_option__use_-oicf"></span><span id="FEATURE_REQUIRES_THE_ADVANCED_INTERPRETED_OPTIMIZATION_OPTION__USE_-OICF"></span>la fonctionnalité nécessite l’option d’optimisation interprétée avancée ; utilisation de-Oicf</dt> <dd> Cet avertissement indique que les commutateurs de ligne de commande du compilateur MIDL tels que <a href="-robust.md"><strong>/Robust</strong></a> requièrent l’utilisation du mode <a href="-oi.md"><strong>/Oicf</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2329"></span><span id="midl2329"></span><dl> <dt><strong>MIDL2329</strong></dt> </dl></td>
<td><dl> <dt><span id="the_optimization_option_is_being_phased_out__use_-Oic"></span><span id="the_optimization_option_is_being_phased_out__use_-oic"></span><span id="THE_OPTIMIZATION_OPTION_IS_BEING_PHASED_OUT__USE_-OIC"></span>l’option d’optimisation est en cours de sortie, utilisez-OIC</dt> <dd> Le mode d’optimisation <a href="-oi.md"><strong>/Oi1</strong></a> a été spécifié sur la ligne de commande MIDL. Ce mode n’est plus pris en charge et <strong>/Oicf</strong> doit être utilisé à la place.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2330"></span><span id="midl2330"></span><dl> <dt><strong>MIDL2330</strong></dt> </dl></td>
<td><dl> <dt><span id="the_optimization_option_is_being_phased_out__use_-Oicf"></span><span id="the_optimization_option_is_being_phased_out__use_-oicf"></span><span id="THE_OPTIMIZATION_OPTION_IS_BEING_PHASED_OUT__USE_-OICF"></span>l’option d’optimisation est en cours de sortie, utilisez-Oicf</dt> <dd> Le mode d’optimisation <a href="-oi.md"><strong>/Oi2</strong></a> a été spécifié sur la ligne de commande MIDL. Ce mode n’est plus pris en charge et <strong>/Oicf</strong> doit être utilisé à la place.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2331"></span><span id="midl2331"></span><dl> <dt><strong>MIDL2331</strong></dt> </dl></td>
<td><dl> <dt><span id="the_optimization_option_is_being_phased_out__use_-ic"></span><span id="THE_OPTIMIZATION_OPTION_IS_BEING_PHASED_OUT__USE_-IC"></span>l’option d’optimisation est en cours de sortie, use-IC</dt> <dd> Le mode d’optimisation I1 a été spécifié dans un attribut [Optimize] ACF. Ce mode n’est plus pris en charge et ICF doit être utilisé à la place.<br/> Exemple de fichier ACF :<br/>
<pre class="syntax" data-space="preserve"><code>[optimize(&quot;i1&quot;)] roo();    //MIDL 2331</code></pre>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2332"></span><span id="midl2332"></span><dl> <dt><strong>MIDL2332</strong></dt> </dl></td>
<td><dl> <dt><span id="the_optimization_option_is_being_phased_out__use_-icf"></span><span id="THE_OPTIMIZATION_OPTION_IS_BEING_PHASED_OUT__USE_-ICF"></span>l’option d’optimisation est en cours de sortie, utilisez-ICF</dt> <dd> Le mode d’optimisation I2 a été spécifié dans un attribut [Optimize] ACF. Ce mode n’est plus pris en charge et ICF doit être utilisé à la place.<br/> Exemple de fichier ACF :<br/>
<pre class="syntax" data-space="preserve"><code>[optimize(&quot;i2&quot;)] roo();    //MIDL 2332</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2333"></span><span id="midl2333"></span><dl> <dt><strong>MIDL2333</strong></dt> </dl></td>
<td><dl> <dt><span id="the_-old_and_-new_switches_are_obsolete__use_-oldtlb_and_-newtlb"></span><span id="THE_-OLD_AND_-NEW_SWITCHES_ARE_OBSOLETE__USE_-OLDTLB_AND_-NEWTLB"></span>les commutateurs-Old et-New sont obsolètes, utilisez-oldtlb et-newtlb</dt> <dd> Ce message est obsolète et n’est plus omis par MIDL.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2334"></span><span id="midl2334"></span><dl> <dt><strong>MIDL2334</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_argument_value"></span><span id="ILLEGAL_ARGUMENT_VALUE"></span>valeur d’argument non conforme</dt> <dd> Les variantes autorisées du commutateur de ligne de commande/O incluent <a href="-os.md"><strong>/OS</strong></a>, <a href="-oi.md"><strong>/OI</strong></a>, <strong>/OIC</strong>, <strong>/Oicf</strong>et <strong>/OIF</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2335"></span><span id="midl2335"></span><dl> <dt><strong>MIDL2335</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_expression_type_in_constant"></span><span id="ILLEGAL_EXPRESSION_TYPE_IN_CONSTANT"></span>type d’expression non conforme dans une constante</dt> <dd> L’expression ne correspond pas à une constante.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2336"></span><span id="midl2336"></span><dl> <dt><strong>MIDL2336</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_expression_type_in_enum"></span><span id="ILLEGAL_EXPRESSION_TYPE_IN_ENUM"></span>type d’expression non conforme dans enum</dt> <dd> Une valeur énumérée dans une définition d' <a href="enum.md"><strong>énumération</strong></a> n’est pas évaluée à un type intégral.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2337"></span><span id="midl2337"></span><dl> <dt><strong>MIDL2337</strong></dt> </dl></td>
<td><dl> <dt><span id="unsatisfied_forward_declaration"></span><span id="UNSATISFIED_FORWARD_DECLARATION"></span>déclaration anticipée insatisfaite</dt> <dd> Le compilateur MIDL n’a pas pu résoudre la définition d’une déclaration anticipée.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2338"></span><span id="midl2338"></span><dl> <dt><strong>MIDL2338</strong></dt> </dl></td>
<td><dl> <dt><span id="switches_are_contradictory"></span><span id="SWITCHES_ARE_CONTRADICTORY"></span>les commutateurs sont contradictoires</dt> <dd> Vous ne pouvez pas utiliser les commutateurs de ligne de commande <a href="-osf.md"><strong>/OSF</strong></a> et <a href="-ms-ext.md"><strong>/ms_ext</strong></a> lorsque vous compilez un fichier IDL. Vous devez choisir l’un ou l’autre.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2339"></span><span id="midl2339"></span><dl> <dt><strong>MIDL2339</strong></dt> </dl></td>
<td><dl> <dt><span id="MIDL_cannot_generate_HOOKOLE_information_for_the_non-rpc-able_union"></span><span id="midl_cannot_generate_hookole_information_for_the_non-rpc-able_union"></span><span id="MIDL_CANNOT_GENERATE_HOOKOLE_INFORMATION_FOR_THE_NON-RPC-ABLE_UNION"></span>MIDL ne peut pas générer d’informations HOOKOLE pour l’Union qui ne peut pas être RPC</dt> <dd> Cette erreur est obsolète. Elle est fournie exclusivement à des fins de compatibilité descendante.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2340"></span><span id="midl2340"></span><dl> <dt><strong>MIDL2340</strong></dt> </dl></td>
<td><dl> <dt><span id="no_case_expression_found_for_union"></span><span id="NO_CASE_EXPRESSION_FOUND_FOR_UNION"></span>aucune expression case trouvée pour Union</dt> <dd> Chaque champ d’une Union doit avoir une instruction case avec une expression constante.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2341"></span><span id="midl2341"></span><dl> <dt><strong>MIDL2341</strong></dt> </dl></td>
<td><dl> <dt><span id="_user_marshal__and__wire_marshal__not_supported_with_-Oi_and_-Oic_flags__use_-Os_or_-Oicf"></span><span id="_user_marshal__and__wire_marshal__not_supported_with_-oi_and_-oic_flags__use_-os_or_-oicf"></span><span id="_USER_MARSHAL__AND__WIRE_MARSHAL__NOT_SUPPORTED_WITH_-OI_AND_-OIC_FLAGS__USE_-OS_OR_-OICF"></span>[user_marshal] et [wire_marshal] ne sont pas pris en charge avec les indicateurs-OI et-OIC, utilisez-OS ou-Oicf</dt> <dd> Les attributs [<a href="user-marshal.md"><strong>user_marshal</strong></a>] et [<a href="wire-marshal.md"><strong>wire_marshal</strong></a>] requièrent les fonctionnalités d’optimisation spécifiques disponibles uniquement dans <a href="-oi.md"><strong>/Oicf</strong></a> (proxy sans code avec des chaînes de format rapide) ou <a href="-os.md"><strong>/OS</strong></a> (marshaling en mode mixte).<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2342"></span><span id="midl2342"></span><dl> <dt><strong>MIDL2342</strong></dt> </dl></td>
<td><dl> <dt><span id="pipes_can_t_be_used_with_data_serialization__i.e.__encode__and_or__decode_"></span><span id="PIPES_CAN_T_BE_USED_WITH_DATA_SERIALIZATION__I.E.__ENCODE__AND_OR__DECODE_"></span>les canaux ne peuvent pas être utilisés avec la sérialisation de données, par exemple [Encode] et/ou [Decode]</dt> <dd> Vous ne pouvez pas passer des canaux en tant que paramètres à des procédures qui ont les attributs [<a href="encode.md"><strong>encode</strong></a>] ou [<a href="decode.md"><strong>Decode</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2343"></span><span id="midl2343"></span><dl> <dt><strong>MIDL2343</strong></dt> </dl></td>
<td><dl> <dt><span id="all_pipe_interface_pointers_must_use_single_indirection"></span><span id="ALL_PIPE_INTERFACE_POINTERS_MUST_USE_SINGLE_INDIRECTION"></span>tous les pointeurs d’interface de canal doivent utiliser une indirection unique</dt> <dd> Vous ne pouvez pas utiliser un pointeur vers un pointeur vers une interface de canal de cette manière.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2344"></span><span id="midl2344"></span><dl> <dt><strong>MIDL2344</strong></dt> </dl></td>
<td><dl> <dt><span id="_iid_is____cannot_be_used_with_a_pipe_interface_pointer"></span><span id="_IID_IS____CANNOT_BE_USED_WITH_A_PIPE_INTERFACE_POINTER"></span>[iid_is ()] ne peut pas être utilisé avec un pointeur d’interface de canal</dt> <dd> Ce message est obsolète. Ce message n’est plus utilisé par le compilateur.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2345"></span><span id="midl2345"></span><dl> <dt><strong>MIDL2345</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid_or_inapplicable_-lcid_switch"></span><span id="INVALID_OR_INAPPLICABLE_-LCID_SWITCH"></span>commutateur LCID non valide ou inapplicable</dt> <dd> L’identificateur local (LCID) que vous avez spécifié n’est pas valide.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2346"></span><span id="midl2346"></span><dl> <dt><strong>MIDL2346</strong></dt> </dl></td>
<td><dl> <dt><span id="the_specified_lcid_is_different_from_previous_specification"></span><span id="THE_SPECIFIED_LCID_IS_DIFFERENT_FROM_PREVIOUS_SPECIFICATION"></span>le LCID spécifié est différent de la spécification précédente</dt> <dd> Les valeurs spécifiées dans/LCID et [<a href="lcid.md"><strong>LCID</strong></a>] sont différentes. Le compilateur MIDL utilise le dernier défini.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2347"></span><span id="midl2347"></span><dl> <dt><strong>MIDL2347</strong></dt> </dl></td>
<td><dl> <dt><span id="importlib_is_not_allowed_outside_of_a_library_block"></span><span id="IMPORTLIB_IS_NOT_ALLOWED_OUTSIDE_OF_A_LIBRARY_BLOCK"></span>importlib n’est pas autorisé en dehors d’un bloc de bibliothèque</dt> <dd> Toutes les instructions [<a href="importlib.md"><strong>importlib</strong></a>] doivent se produire dans un bloc [<a href="library.md"><strong>Library</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2348"></span><span id="midl2348"></span><dl> <dt><strong>MIDL2348</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid_floating_point_value"></span><span id="INVALID_FLOATING_POINT_VALUE"></span>valeur à virgule flottante non valide</dt> <dd> Cette erreur ne doit pas être émise par MIDL. Si vous voyez cette erreur, signalez un bogue à Microsoft en fournissant tous les fichiers nécessaires pour reproduire l’erreur, notamment vos fichiers IDL, les fichiers ACF, les en-têtes, etc.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2349"></span><span id="midl2349"></span><dl> <dt><strong>MIDL2349</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid_member"></span><span id="INVALID_MEMBER"></span>membre non valide</dt> <dd> Les procédures ne peuvent pas être membres d’une bibliothèque.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2350"></span><span id="midl2350"></span><dl> <dt><strong>MIDL2350</strong></dt> </dl></td>
<td><dl> <dt><span id="possible_invalid_member"></span><span id="POSSIBLE_INVALID_MEMBER"></span>membre non valide possible</dt> <dd> Pour être un membre valide d’une bibliothèque, l’élément de bibliothèque doit être un module, une dispinterface, une coclasse, une instruction if, une structure, une Union, une énumération ou une déclaration anticipée.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2351"></span><span id="midl2351"></span><dl> <dt><strong>MIDL2351</strong></dt> </dl></td>
<td><dl> <dt><span id="mismatch_in_pipe_and_interface_types"></span><span id="MISMATCH_IN_PIPE_AND_INTERFACE_TYPES"></span>incompatibilité dans les types de canaux et d’interfaces</dt> <dd> Ce message est obsolète.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2352"></span><span id="midl2352"></span><dl> <dt><strong>MIDL2352</strong></dt> </dl></td>
<td><dl> <dt><span id="string__varying_array__conformant_array_and_full_pointer_parameters_may_be_incompatible_with_pipe_parameters_during_run_time"></span><span id="STRING__VARYING_ARRAY__CONFORMANT_ARRAY_AND_FULL_POINTER_PARAMETERS_MAY_BE_INCOMPATIBLE_WITH_PIPE_PARAMETERS_DURING_RUN_TIME"></span>les paramètres de chaîne, de tableau variable, de tableau conforme et de pointeur complet peuvent être incompatibles avec les paramètres de canal au moment de l’exécution</dt> <dd> une méthode associant une ou plusieurs chaînes [in], des tableaux variables, des tableaux conformes et des paramètres de pointeur complet et n’importe quel paramètre de canal [in] entraîne la génération d’un stub qui s’exécute uniquement sur les séquences de protocole <strong>ncacn_ *</strong> et <a href="ncalrpc.md"><strong>ncalrpc</strong></a> sur les ordinateurs Windows. L’utilisation du stub pour effectuer des appels sur des séquences de protocole <strong>ncadg_ *</strong> ou accepter des appels d’autres fournisseurs RPC DCE ETCD peut générer des erreurs sur le serveur au moment de l’exécution. cette erreur se produit à partir de Windows Server 2003.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2353"></span><span id="midl2353"></span><dl> <dt><strong>MIDL2353</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_must_be_in"></span><span id="PARAMETER_MUST_BE_IN"></span>le paramètre doit être dans</dt> <dd> Les handles asynchrones doivent être [<a href="in.md"><strong>in</strong></a>] paramètres.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2354"></span><span id="midl2354"></span><dl> <dt><strong>MIDL2354</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_type_of_an__async__object_must_be_a_double_pointer_to_an_interface"></span><span id="PARAMETER_TYPE_OF_AN__ASYNC__OBJECT_MUST_BE_A_DOUBLE_POINTER_TO_AN_INTERFACE"></span>le type de paramètre d’un objet [Async] doit être un pointeur double vers une interface</dt> <dd> Le paramètre doit être de type <strong>IAsyncManager</strong> * *.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2355"></span><span id="midl2355"></span><dl> <dt><strong>MIDL2355</strong></dt> </dl></td>
<td><dl> <dt><span id="incorrect_async_handle_type"></span><span id="INCORRECT_ASYNC_HANDLE_TYPE"></span>type de handle asynchrone incorrect</dt> <dd> Le type de handle doit être <strong>IAsyncManager</strong> ou un type dérivé de <strong>IAsyncManager</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2356"></span><span id="midl2356"></span><dl> <dt><strong>MIDL2356</strong></dt> </dl></td>
<td><dl> <dt><span id="the__internal__switch_enables_unsupported_features__use_with_caution"></span><span id="THE__INTERNAL__SWITCH_ENABLES_UNSUPPORTED_FEATURES__USE_WITH_CAUTION"></span>le &quot; &quot; commutateur interne active les fonctionnalités non prises en charge, à utiliser avec précaution</dt> <dd> Évitez d’utiliser ce commutateur.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2357"></span><span id="midl2357"></span><dl> <dt><strong>MIDL2357</strong></dt> </dl></td>
<td><dl> <dt><span id="async_procedures_cannot_use_auto_handle"></span><span id="ASYNC_PROCEDURES_CANNOT_USE_AUTO_HANDLE"></span>les procédures Async ne peuvent pas utiliser le handle automatique</dt> <dd> Les procédures avec l’attribut [<a href="async.md"><strong>Async</strong></a>] requièrent des handles explicites.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2358"></span><span id="midl2358"></span><dl> <dt><strong>MIDL2358</strong></dt> </dl></td>
<td><dl> <dt><span id="error_status_t_should_have_both__comm_status__and__fault_status_"></span><span id="ERROR_STATUS_T_SHOULD_HAVE_BOTH__COMM_STATUS__AND__FAULT_STATUS_"></span>error_status_t doivent avoir [comm_status] et [fault_status]</dt> <dd> Une procédure a été spécifiée avec les attributs IDL [peut-être] ou [message], mais le type de retour a uniquement les attributs ACF [comm_status] ou [fault_status]. Les deux attributs ACF sont requis.<br/> Exemple de fichier ACF :<br/>
<pre class="syntax" data-space="preserve"><code>[comm_status] roo();    //MIDL 2358
[fault_status] bar();    //MIDL 2358
[comm_status, fault_status] baz();    //OK</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2359"></span><span id="midl2359"></span><dl> <dt><strong>MIDL2359</strong></dt> </dl></td>
<td><dl> <dt><span id="this_construct_is_only_allowed_within_a_library_block"></span><span id="THIS_CONSTRUCT_IS_ONLY_ALLOWED_WITHIN_A_LIBRARY_BLOCK"></span>Cette construction est uniquement autorisée dans un bloc de bibliothèque</dt> <dd> Un module ne peut se produire que dans un bloc de bibliothèque.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2360"></span><span id="midl2360"></span><dl> <dt><strong>MIDL2360</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid_type_redefinition"></span><span id="INVALID_TYPE_REDEFINITION"></span>redéfinition de type non valide</dt> <dd> Un nouveau type a été défini de manière récursive sur un type inexistant.<br/> Exemple :<br/>
<pre class="syntax" data-space="preserve"><code>typedef roo roo[10];    //MIDL 2360</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2361"></span><span id="midl2361"></span><dl> <dt><strong>MIDL2361</strong></dt> </dl></td>
<td><dl> <dt><span id="procedures_with_a__vararg__attribute_must_have_a_SAFEARRAY_VARIANT__parameter__param_order_is__vararg____lcid____retval_"></span><span id="procedures_with_a__vararg__attribute_must_have_a_safearray_variant__parameter__param_order_is__vararg____lcid____retval_"></span><span id="PROCEDURES_WITH_A__VARARG__ATTRIBUTE_MUST_HAVE_A_SAFEARRAY_VARIANT__PARAMETER__PARAM_ORDER_IS__VARARG____LCID____RETVAL_"></span>les procédures avec un attribut [vararg] doivent avoir un paramètre SAFEARRAY (VARIANT); l’ordre des paramètres est [vararg], [LCID], [retval]</dt> <dd> La plupart des paramètres des procédures avec l’attribut [<a href="vararg.md"><strong>vararg</strong></a>] doivent se produire avant le paramètre <strong>SAFEARRAY (variant)</strong> . Le paramètre <strong>SAFEARRAY (variant)</strong> doit être présent. Si la liste de paramètres contient un paramètre avec l’attribut [ <a href="lcid.md"><strong>LCID</strong></a>], elle doit suivre le paramètre <strong>SAFEARRAY (variant)</strong> . Si la liste de paramètres contient un paramètre avec l’attribut [<a href="retval.md"><strong>retVal</strong></a>], elle doit se produire après le paramètre avec l’attribut [<strong>LCID</strong>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2363"></span><span id="midl2363"></span><dl> <dt><strong>MIDL2363</strong></dt> </dl></td>
<td><dl> <dt><span id="too_many_methods_in_the_interface__requires_Windows_2000_or_greater"></span><span id="too_many_methods_in_the_interface__requires_windows_2000_or_greater"></span><span id="TOO_MANY_METHODS_IN_THE_INTERFACE__REQUIRES_WINDOWS_2000_OR_GREATER"></span>un trop grand nombre de méthodes dans l’interface requiert Windows 2000 ou une version ultérieure</dt> <dd> Le compilateur MIDL n’autorise pas plus de 1024 méthodes dans une interface lorsque vous compilez en mode <a href="-oi.md"><strong>/Oicf</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2364"></span><span id="midl2364"></span><dl> <dt><strong>MIDL2364</strong></dt> </dl></td>
<td><dl> <dt><span id="switch_is_being_phased_out"></span><span id="SWITCH_IS_BEING_PHASED_OUT"></span>le commutateur est en cours de sortie</dt> <dd> Les commutateurs suivants sont obsolètes:/<strong>hookole</strong>,/<strong>env Win16</strong>et/<strong>env</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2365"></span><span id="midl2365"></span><dl> <dt><strong>MIDL2365</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_derive_from_IAdviseSink__IAdviseSink2__or_IAdviseSinkEx"></span><span id="cannot_derive_from_iadvisesink__iadvisesink2__or_iadvisesinkex"></span><span id="CANNOT_DERIVE_FROM_IADVISESINK__IADVISESINK2__OR_IADVISESINKEX"></span>dérivation impossible à partir de IAdviseSink, IAdviseSink2 ou IAdviseSinkEx</dt> <dd> Ces interfaces ne peuvent pas être étendues.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2366"></span><span id="midl2366"></span><dl> <dt><strong>MIDL2366</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_assign_a_default_value"></span><span id="CANNOT_ASSIGN_A_DEFAULT_VALUE"></span>Impossible d’attribuer une valeur par défaut</dt> <dd> l’assignation d’une valeur par défaut à un paramètre est autorisée dans Visual Basic, mais pas en C++. Si vous utilisez C++, la valeur par défaut est ignorée.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2367"></span><span id="midl2367"></span><dl> <dt><strong>MIDL2367</strong></dt> </dl></td>
<td><dl> <dt><span id="type_library_generation_for_DOS_Win16_MAC_is_not_supported"></span><span id="type_library_generation_for_dos_win16_mac_is_not_supported"></span><span id="TYPE_LIBRARY_GENERATION_FOR_DOS_WIN16_MAC_IS_NOT_SUPPORTED"></span>la génération de la bibliothèque de types pour DOS/Win16/MAC n’est pas prise en charge</dt> <dd> MIDL ne prend pas en charge les bibliothèques de types 16 bits.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2368"></span><span id="midl2368"></span><dl> <dt><strong>MIDL2368</strong></dt> </dl></td>
<td><dl> <dt><span id="error_generating_type_library__ignored"></span><span id="ERROR_GENERATING_TYPE_LIBRARY__IGNORED"></span>erreur lors de la génération de la bibliothèque de types, ignoré</dt> <dd> Une erreur non irrécupérable s’est produite lors de la génération de la bibliothèque de types.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2369"></span><span id="midl2369"></span><dl> <dt><strong>MIDL2369</strong></dt> </dl></td>
<td><dl> <dt><span id="exceeded_stack_size_for__Oi__using__Os"></span><span id="exceeded_stack_size_for__oi__using__os"></span><span id="EXCEEDED_STACK_SIZE_FOR__OI__USING__OS"></span>taille de pile dépassée pour/OI, à l’aide de/OS</dt> <dd> Le mode d’optimisation-OI est limité à 128 octets d’espace de pile pour les paramètres. Le compilateur a automatiquement basculé vers le mode d’optimisation du système d’exploitation pour contourner cette limitation.<br/> Pour éviter cet avertissement, utilisez les modes d’optimisation-Oicf ou-OS. Le mode d’optimisation peut être modifié sur la ligne de commande en spécifiant-Oicf ou-OS au lieu de-OI, ou en ajoutant un attribut [optimize9 &quot; ICF &quot; )] ou optimiser [( &quot; s &quot; )] à la fonction dans le fichier ACF.<br/> Cet avertissement se produit généralement lors du passage de structures volumineuses en tant que paramètres par valeur. La taille de pile requise peut être abaissée en passant un pointeur vers la structure à la place.<br/> Exemple :<br/>
<pre class="syntax" data-space="preserve"><code>typedef struct
{
char a[127];
}
large;
//This function has a stack size of 132 (x86) or 136 (alpha) on 32-bit systems
void roo(large s, int a);    //MIDL 2360
// workaround: pass by reference
void bar (large *s, int a);</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2370"></span><span id="midl2370"></span><dl> <dt><strong>MIDL2370</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of__robust_requires__Oicf__switching_modes"></span><span id="use_of__robust_requires__oicf__switching_modes"></span><span id="USE_OF__ROBUST_REQUIRES__OICF__SWITCHING_MODES"></span>l’utilisation de/Robust requiert/Oicf, modes de basculement</dt> <dd> Vous devez compiler en mode <a href="-oi.md"><strong>/Oicf</strong></a> quand vous spécifiez le commutateur <a href="-robust.md"><strong>/Robust</strong></a> sur la ligne de commande.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2371"></span><span id="midl2371"></span><dl> <dt><strong>MIDL2371</strong></dt> </dl></td>
<td><dl> <dt><span id="incorrect_range_specified"></span><span id="INCORRECT_RANGE_SPECIFIED"></span>plage incorrecte spécifiée</dt> <dd> La valeur la plus élevée spécifiée dans un attribut [<a href="range.md"><strong>Range</strong></a>] est inférieure à la valeur la plus faible.<br/> Exemple :<br/>
<pre class="syntax" data-space="preserve"><code>void roo([range(3,2)] int a);    //MIDL 2371</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2372"></span><span id="midl2372"></span><dl> <dt><strong>MIDL2372</strong></dt> </dl></td>
<td><dl> <dt><span id="_invalid_combination_of__in__only_and__out__parameters_for__async_uuid__interface"></span><span id="_INVALID_COMBINATION_OF__IN__ONLY_AND__OUT__PARAMETERS_FOR__ASYNC_UUID__INTERFACE"></span> combinaison non valide de [in] et [out] paramètres pour l’interface [async_uuid]</dt> <dd> Seules des combinaisons simples d’attributs avec des paramètres [<a href="in.md"><strong>in</strong></a>] ou [<a href="out-idl.md"><strong>out</strong></a>] sont autorisées pour ce type d’interface.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2373"></span><span id="midl2373"></span><dl> <dt><strong>MIDL2373</strong></dt> </dl></td>
<td><dl> <dt><span id="DOS__Win16_and_MAC_platforms_are_not_supported_with__robust"></span><span id="dos__win16_and_mac_platforms_are_not_supported_with__robust"></span><span id="DOS__WIN16_AND_MAC_PLATFORMS_ARE_NOT_SUPPORTED_WITH__ROBUST"></span>Les plateformes DOS, Win16 et MAC ne sont pas prises en charge avec/Robust</dt> <dd> MIDL prend en charge le commutateur <a href="-robust.md"><strong>/robust</strong></a> sur Microsoft Windows 2000 ou version ultérieure.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2374"></span><span id="midl2374"></span><dl> <dt><strong>MIDL2374</strong></dt> </dl></td>
<td><dl> <dt><span id="support_for_NT_3.51_style_stubless_proxies_for_object_interfaces_will_be_phased_out__use__Oif."></span><span id="support_for_nt_3.51_style_stubless_proxies_for_object_interfaces_will_be_phased_out__use__oif."></span><span id="SUPPORT_FOR_NT_3.51_STYLE_STUBLESS_PROXIES_FOR_OBJECT_INTERFACES_WILL_BE_PHASED_OUT__USE__OIF."></span>la prise en charge des proxies de style NT 3,51 pour les interfaces d’objet sera supprimée. utiliser/OIF.</dt> <dd> Ce mode est obsolète. Utilisez <a href="-oi.md"><strong>/OIF</strong></a> ou <strong>/Oicf</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2375"></span><span id="midl2375"></span><dl> <dt><strong>MIDL2375</strong></dt> </dl></td>
<td><dl> <dt><span id="_encode__or__decode__with__robust_requires__Oicf"></span><span id="_encode__or__decode__with__robust_requires__oicf"></span><span id="_ENCODE__OR__DECODE__WITH__ROBUST_REQUIRES__OICF"></span>[Encode] ou [Decode] avec/Robust requiert/Oicf</dt> <dd> La sérialisation ne peut pas être effectuée quand le commutateur <a href="-robust.md"><strong>/Robust</strong></a> est spécifié.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2377"></span><span id="midl2377"></span><dl> <dt><strong>MIDL2377</strong></dt> </dl></td>
<td><dl> <dt><span id="conflicting_attributes_specified"></span><span id="CONFLICTING_ATTRIBUTES_SPECIFIED"></span>attributs spécifiés en conflit</dt> <dd> [<a href="context-handle-serialize.md"><strong>Context_handle_serialize</strong></a>] et [<a href="context-handle-noserialize.md"><strong>context_handle_noserialize</strong></a>] ont été spécifiés.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2378"></span><span id="midl2378"></span><dl> <dt><strong>MIDL2378</strong></dt> </dl></td>
<td><dl> <dt><span id="_serialize____noserialize__can_be_applied_to_context_handles"></span><span id="_SERIALIZE____NOSERIALIZE__CAN_BE_APPLIED_TO_CONTEXT_HANDLES"></span>[Serialize], [noserialize] peut être appliqué à context_handles</dt> <dd> Les attributs ACF [context_handle_serialize] ou [context_handle_noserialize] peuvent uniquement être appliqués aux types qui sont des handles de contexte.<br/> Exemple de fichier IDL :<br/>
<pre class="syntax" data-space="preserve"><code>typedef /*[context_handle] */ void *PV;    //Note: PV is *not* a context handle.</code></pre>
Exemple de fichier ACF :<br/>
<pre class="syntax" data-space="preserve"><code>typedef [context_handle_serialize] PV;    //MIDL 2378</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2379"></span><span id="midl2379"></span><dl> <dt><strong>MIDL2379</strong></dt> </dl></td>
<td><dl> <dt><span id="The_compiler_reached_a_limit_for_a_format_string_representation._See_documentation_for_advice."></span><span id="the_compiler_reached_a_limit_for_a_format_string_representation._see_documentation_for_advice."></span><span id="THE_COMPILER_REACHED_A_LIMIT_FOR_A_FORMAT_STRING_REPRESENTATION._SEE_DOCUMENTATION_FOR_ADVICE."></span>Le compilateur a atteint une limite pour une représentation sous forme de chaîne de format. Consultez la documentation pour obtenir des conseils.</dt> <dd> Le compilateur MIDL a une limite de 64 Ko pour les chaînes de format. Cette erreur se produit généralement lorsque des fichiers IDL incluent d’autres fichiers IDL. Le fichier IDL composite généré par toutes les instructions include dépasse les limites des tables de représentation de type de l’interpréteur du moteur de marshaling. Essayez d’utiliser la directive import plutôt que la directive include dans vos fichiers IDL. Pour plus d’informations, consultez <a href="importing-system-header-files.md">importation de fichiers d’en-tête système</a>, <a href="include.md"><strong>include</strong></a>et <a href="import.md"><strong>Import</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2380"></span><span id="midl2380"></span><dl> <dt><strong>MIDL2380</strong></dt> </dl></td>
<td><dl> <dt><span id="wire_format_may_be_incorrect__you_may_need_to_use_-ms_conf_struct__see_documentation_for_advice"></span><span id="WIRE_FORMAT_MAY_BE_INCORRECT__YOU_MAY_NEED_TO_USE_-MS_CONF_STRUCT__SEE_DOCUMENTATION_FOR_ADVICE"></span>le format de câble peut être incorrect, vous devrez peut-être utiliser-ms_conf_struct, consultez la documentation pour obtenir des conseils</dt> <dd> Le compilateur MIDL n’a pas pu générer un format transmissible pour les données. Une façon courante d’obtenir cette erreur consiste à définir un <strong>ms_conf_struct</strong> à l’intérieur d’une structure complexe.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2381"></span><span id="midl2381"></span><dl> <dt><strong>MIDL2381</strong></dt> </dl></td>
<td><dl> <dt><span id="a_stack_size_or_an_offset_bigger_than_64_K_limit._See_documentation_for_advice."></span><span id="a_stack_size_or_an_offset_bigger_than_64_k_limit._see_documentation_for_advice."></span><span id="A_STACK_SIZE_OR_AN_OFFSET_BIGGER_THAN_64_K_LIMIT._SEE_DOCUMENTATION_FOR_ADVICE."></span>taille de la pile ou décalage supérieur à 64 Ko. Consultez la documentation pour obtenir des conseils.</dt> <dd> L’appel aboutit à une pile supérieure à 64 Ko. Essayez de passer les données dans des blocs plus petits.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2382"></span><span id="midl2382"></span><dl> <dt><strong>MIDL2382</strong></dt> </dl></td>
<td><dl> <dt><span id="an_interpreter_mode_forced_for_64-bit_platform_"></span><span id="AN_INTERPRETER_MODE_FORCED_FOR_64-BIT_PLATFORM_"></span>mode interpréteur forcé pour une plateforme 64 bits </dt> <dd> les plateformes 64 bits requièrent le mode de compilation/Oicf.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2383"></span><span id="midl2383"></span><dl> <dt><strong>MIDL2383</strong></dt> </dl></td>
<td><dl> <dt><span id="The_array_element_size_is_bigger_than_64_KB_limit."></span><span id="the_array_element_size_is_bigger_than_64_kb_limit."></span><span id="THE_ARRAY_ELEMENT_SIZE_IS_BIGGER_THAN_64_KB_LIMIT."></span>La taille de l’élément de tableau est supérieure à la limite de 64 Ko.</dt> <dd> La taille de tous les éléments du tableau doit être inférieure à 64 Ko.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2384"></span><span id="midl2384"></span><dl> <dt><strong>MIDL2384</strong></dt> </dl></td>
<td><dl> <dt><span id="there_can_be_only_one__Icid__parameter_in_a_method__and_it_should_be_last_or_second_to_last_if_last_parameter_has__retval_"></span><span id="there_can_be_only_one__icid__parameter_in_a_method__and_it_should_be_last_or_second_to_last_if_last_parameter_has__retval_"></span><span id="THERE_CAN_BE_ONLY_ONE__ICID__PARAMETER_IN_A_METHOD__AND_IT_SHOULD_BE_LAST_OR_SECOND_TO_LAST_IF_LAST_PARAMETER_HAS__RETVAL_"></span>il ne peut y avoir qu’un seul paramètre [ICID] dans une méthode, et il doit s’agir de Last ou de second dans Last si le dernier paramètre a [retval]</dt> <dd> Un paramètre avec l’attribut [<a href="lcid.md"><strong>LCID</strong></a>] doit se produire en dernier. La seule exception est lorsqu’il y a également un paramètre avec l’attribut [<a href="retval.md"><strong>retVal</strong></a>]. Lorsque les deux se produisent, la seconde au dernier paramètre de la liste de paramètres doit avoir l’attribut [ <strong>LCID</strong>]. Le dernier paramètre doit avoir l’attribut [<strong>retVal</strong>].<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2385"></span><span id="midl2385"></span><dl> <dt><strong>MIDL2385</strong></dt> </dl></td>
<td><dl> <dt><span id="incorrect_syntax_for_midl_pragma"></span><span id="INCORRECT_SYNTAX_FOR_MIDL_PRAGMA"></span>syntaxe incorrecte pour midl_pragma</dt> <dd> Le compilateur MIDL a détecté une erreur de syntaxe inconnue dans une instruction midl_pragma.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2386"></span><span id="midl2386"></span><dl> <dt><strong>MIDL2386</strong></dt> </dl></td>
<td><dl> <dt><span id="__int3264_is_not_supported_in__osf_mode"></span><span id="__INT3264_IS_NOT_SUPPORTED_IN__OSF_MODE"></span>__int3264 n’est pas pris en charge en mode/OSF</dt> <dd> Si vous devez utiliser __int3264, compilez en mode/MS-ext.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2387"></span><span id="midl2387"></span><dl> <dt><strong>MIDL2387</strong></dt> </dl></td>
<td><dl> <dt><span id="unresolved_symbol_in_type_library"></span><span id="UNRESOLVED_SYMBOL_IN_TYPE_LIBRARY"></span>symbole non résolu dans la bibliothèque de types</dt> <dd> Le compilateur n’a pas pu résoudre une déclaration formelle ou un type référencé dans la bibliothèque de types.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2388"></span><span id="midl2388"></span><dl> <dt><strong>MIDL2388</strong></dt> </dl></td>
<td><dl> <dt><span id="async_pipes_cannot_be_passed_by_value"></span><span id="ASYNC_PIPES_CANNOT_BE_PASSED_BY_VALUE"></span>les canaux Async ne peuvent pas être passés par valeur</dt> <dd> Les canaux asynchrones doivent être passés par référence ou par adresse.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2389"></span><span id="midl2389"></span><dl> <dt><strong>MIDL2389</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_offset_exceed_64-KB_limit_for_interpreted_procedures"></span><span id="parameter_offset_exceed_64-kb_limit_for_interpreted_procedures"></span><span id="PARAMETER_OFFSET_EXCEED_64-KB_LIMIT_FOR_INTERPRETED_PROCEDURES"></span>le décalage du paramètre dépasse la limite de 64 Ko pour les procédures interprétées</dt> <dd> Cette erreur signifie généralement que les paramètres d’une procédure sont trop nombreux.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2390"></span><span id="midl2390"></span><dl> <dt><strong>MIDL2390</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid_array_element"></span><span id="INVALID_ARRAY_ELEMENT"></span>élément de tableau non valide</dt> <dd> Les canaux ne peuvent pas être utilisés en tant qu’éléments de tableau.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2391"></span><span id="midl2391"></span><dl> <dt><strong>MIDL2391</strong></dt> </dl></td>
<td><dl> <dt><span id="dispinterface_members_must_be_methods__properties_or_interfaces"></span><span id="DISPINTERFACE_MEMBERS_MUST_BE_METHODS__PROPERTIES_OR_INTERFACES"></span>les membres dispinterface doivent être des méthodes, des propriétés ou des interfaces</dt> <dd> Une dispinterface ne peut pas contenir de définitions, de structures, d’énumérations ou d’unions de type.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2392"></span><span id="midl2392"></span><dl> <dt><strong>MIDL2392</strong></dt> </dl></td>
<td><dl> <dt><span id="_local__procedure_without__call_as_"></span><span id="_LOCAL__PROCEDURE_WITHOUT__CALL_AS_"></span>[local] procédure sans [call_as]</dt> <dd> Les procédures d’objet qui ont l’attribut [<a href="local.md"><strong>local</strong></a>] requièrent également l’attribut [<a href="call-as.md"><strong>call_as</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2393"></span><span id="midl2393"></span><dl> <dt><strong>MIDL2393</strong></dt> </dl></td>
<td><dl> <dt><span id="multi_dimensional_vector__switching_to__Oicf"></span><span id="multi_dimensional_vector__switching_to__oicf"></span><span id="MULTI_DIMENSIONAL_VECTOR__SWITCHING_TO__OICF"></span>vecteur multidimensionnel, basculement vers/Oicf</dt> <dd> Le mode d’optimisation <a href="-os.md"><strong>/OS</strong></a> ne prend pas en charge les tableaux de tailles non fixes multidimensionnels. Le compilateur a automatiquement basculé le mode d’optimisation à/<strong>Oicf</strong> pour cette fonction. <br/> Cet avertissement peut être supprimé globalement en modifiant le mode du compilateur en spécifiant/<strong>Oicf</strong> sur la ligne de commande MIDL ou en utilisant <strong>midl_pragma</strong> avertissement (désactiver : 2393) dans le fichier IDL. Le mode d’optimisation peut être modifié pour une fonction individuelle en ajoutant l’attribut [<strong>optimize ( &quot; ICF &quot; )</strong>] à la fonction dans le fichier ACF.<br/> L’exemple suivant illustre cet avertissement :<br/>
<pre class="syntax" data-space="preserve"><code>void roo(long s1, [size_is(s1)] long a[][30];    //MIDL2393
void bar(long s1, long s2, [size_is(s1,s2) long **a);//MIDL2393</code></pre>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2395"></span><span id="midl2395"></span><dl> <dt><strong>MIDL2395</strong></dt> </dl></td>
<td><dl> <dt><span id="type_or_construct_not_supported_in_a_library_block_because_Oleaut32.dll_support_for_64-KB_polymorphic_types_is_missing"></span><span id="type_or_construct_not_supported_in_a_library_block_because_oleaut32.dll_support_for_64-kb_polymorphic_types_is_missing"></span><span id="TYPE_OR_CONSTRUCT_NOT_SUPPORTED_IN_A_LIBRARY_BLOCK_BECAUSE_OLEAUT32.DLL_SUPPORT_FOR_64-KB_POLYMORPHIC_TYPES_IS_MISSING"></span>type ou construction non pris en charge dans un bloc de bibliothèque, car Oleaut32.dll la prise en charge des types polymorphes 64 Ko est manquante</dt> <dd> OLE Automation ne prend pas en charge les types polymorphes (comme _int3264, INT_PTR, etc.). Ces types ont des représentations de données incompatibles entre les plateformes 32 bits et 64 bits. L’appel distant échouera au moment de l’exécution sur les plateformes 64 bits.<br/>
<blockquote>
[!Note]<br />
notez que à partir de Windows version 2000, les fichiers tlb 64 bits sont pris en charge par OLE Automation en convertissant les informations tlb 32 bits au moment de l’exécution. Par conséquent, seule la génération TLB 32 bits est prise en charge par MIDL.
</blockquote>
<br/> Si MIDL est utilisé uniquement pour générer un fichier d’en-tête, le commutateur <a href="-notlb.md"><strong>/notlb</strong></a> supprimera la génération du fichier TLB.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2396"></span><span id="midl2396"></span><dl> <dt><strong>MIDL2396</strong></dt> </dl></td>
<td><dl> <dt><span id="old_interpreter_code_being_generated_for_64b"></span><span id="OLD_INTERPRETER_CODE_BEING_GENERATED_FOR_64B"></span>ancien code d’interpréteur généré pour 64B</dt> <dd> Cette erreur est obsolète. Si vous voyez cette erreur, signalez un bogue à Microsoft en donnant vos fichiers IDL, les fichiers ACF et la ligne de commande MIDL complète.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2397"></span><span id="midl2397"></span><dl> <dt><strong>MIDL2397</strong></dt> </dl></td>
<td><dl> <dt><span id="the_compiler_switch_is_not_supported_anymore"></span><span id="THE_COMPILER_SWITCH_IS_NOT_SUPPORTED_ANYMORE"></span>le commutateur du compilateur n’est plus pris en charge</dt> <dd> Le ou les commutateurs spécifiés ne sont plus pris en charge.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2398"></span><span id="midl2398"></span><dl> <dt><strong>MIDL2398</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_execute_MIDL_engine"></span><span id="cannot_execute_midl_engine"></span><span id="CANNOT_EXECUTE_MIDL_ENGINE"></span>Impossible d’exécuter le moteur MIDL</dt> <dd> à partir de la version Windows 2000 (MIDL version 5.03.279), le compilateur midl est implémenté à l’aide de deux fichiers exécutables : Midl.exe (le pilote) et Midlc.exe (moteur de compilateur). Cette erreur indique que le Midl.exe ne peut pas lancer Midlc.exe. Assurez-vous que Midlc.exe se trouve dans le même répertoire que Midl.exe, et qu’il s’agit de la même version.<br/> L’erreur peut être due à la copie Midl.exe mais pas Midlx.exe de la distribution la plus récente. Exécutez <strong>MIDL</strong> et/ou <strong>Midlc</strong> sur la ligne de commande sans aucun paramètre pour voir le numéro de version de l’exécutable.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2399"></span><span id="midl2399"></span><dl> <dt><strong>MIDL2399</strong></dt> </dl></td>
<td><dl> <dt><span id="bad_commands_from_driver"></span><span id="BAD_COMMANDS_FROM_DRIVER"></span>commandes incorrectes du pilote</dt> <dd> à partir de la version Windows 2000 (MIDL version 5.03.279), le compilateur midl est implémenté à l’aide de deux fichiers exécutables : Midl.exe (le pilote) et Midlc.exe (moteur de compilateur). Cette erreur indique que le fichier temporaire utilisé pour passer des commandes de Midl.exe à Midlc.exe est manquant ou endommagé. Assurez-vous que Midlc.exe se trouve dans le même répertoire que Midl.exe, et qu’il s’agit de la même version.<br/> L’erreur peut être due à une tentative d’exécution de Midlc.exe directement ou à la copie Midl.exe mais pas Midlc.exe de la distribution la plus récente. Exécutez <strong>MIDL</strong> et/ou <strong>Midlc</strong> sur la ligne de commande sans aucun paramètre pour voir le numéro de version de l’exécutable.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2400"></span><span id="midl2400"></span><dl> <dt><strong>MIDL2400</strong></dt> </dl></td>
<td><dl> <dt><span id="for_ole_automation__optional_parameters_should_be_VARIANT_or_VARIANT__"></span><span id="for_ole_automation__optional_parameters_should_be_variant_or_variant__"></span><span id="FOR_OLE_AUTOMATION__OPTIONAL_PARAMETERS_SHOULD_BE_VARIANT_OR_VARIANT__"></span>pour OLE Automation, les paramètres facultatifs doivent être VARIANT ou VARIANT *</dt> <dd> OLE Automation requiert que tous les paramètres [facultatifs] soient de type <strong>Variant</strong> ou <strong>Variant *</strong>.<br/> Dans OLE Automation, l’utilisation de paramètres non VARIANTs peut provoquer l’échec de l’appel au moment de l’exécution ou la transmission de données non définies pour les paramètres [<a href="optional.md"><strong>facultatif</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2401"></span><span id="midl2401"></span><dl> <dt><strong>MIDL2401</strong></dt> </dl></td>
<td><dl> <dt><span id="_defaultvalue__is_applied_to_a_non-VARIANT_and__optional_._Please_remove__optional_"></span><span id="_defaultvalue__is_applied_to_a_non-variant_and__optional_._please_remove__optional_"></span><span id="_DEFAULTVALUE__IS_APPLIED_TO_A_NON-VARIANT_AND__OPTIONAL_._PLEASE_REMOVE__OPTIONAL_"></span>[DefaultValue] est appliqué à une valeur non VARIANT et [facultatif]. Veuillez supprimer [facultatif]</dt> <dd> L’attribut [<a href="defaultvalue.md"><strong>DefaultValue</strong></a>] implique [<a href="optional.md"><strong>facultatif</strong></a>]. L’attribut [ <strong>Optional</strong>] n’est pas nécessaire.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2402"></span><span id="midl2402"></span><dl> <dt><strong>MIDL2402</strong></dt> </dl></td>
<td><dl> <dt><span id="_optional__attribute_is_inapplicable_outside_of_a_library_block"></span><span id="_OPTIONAL__ATTRIBUTE_IS_INAPPLICABLE_OUTSIDE_OF_A_LIBRARY_BLOCK"></span>[optional] l’attribut n’est pas applicable en dehors d’un bloc de bibliothèque</dt> <dd> La fonctionnalité impliquée par l’attribut [ <a href="optional.md"><strong>Optional</strong></a>] n’est pas applicable aux proxies générés pour une interface en dehors d’un bloc de bibliothèque.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2403"></span><span id="midl2403"></span><dl> <dt><strong>MIDL2403</strong></dt> </dl></td>
<td><dl> <dt><span id="The_data_type_of_the__Icid__parameter_must_be_long"></span><span id="the_data_type_of_the__icid__parameter_must_be_long"></span><span id="THE_DATA_TYPE_OF_THE__ICID__PARAMETER_MUST_BE_LONG"></span>Le type de données du paramètre [ICID] doit être long</dt> <dd> OLE Automation requiert que les paramètres avec l’attribut [<strong>ICID</strong>] doivent être de type <a href="long.md"><strong>long</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2404"></span><span id="midl2404"></span><dl> <dt><strong>MIDL2404</strong></dt> </dl></td>
<td><dl> <dt><span id="procedures_with__propput____propget__or__propref__can_t_have_more_than_one_required_parameter_after__optional__one"></span><span id="PROCEDURES_WITH__PROPPUT____PROPGET__OR__PROPREF__CAN_T_HAVE_MORE_THAN_ONE_REQUIRED_PARAMETER_AFTER__OPTIONAL__ONE"></span>les procédures avec [propput], [propget] ou [propréférences] ne peuvent pas avoir plus d’un paramètre obligatoire après [optional] One</dt> <dd> Il ne peut pas y avoir plus d’un paramètre sans [<a href="optional.md"><strong>Optional</strong></a>] après le dernier paramètre avec [<strong>Optional</strong>] lors de l’utilisation de [<a href="propput.md"><strong>propput</strong></a>], [<a href="propget.md"><strong>propget</strong></a>] ou [ <a href="propputref.md"><strong>PROPPUTREF</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2405"></span><span id="midl2405"></span><dl> <dt><strong>MIDL2405</strong></dt> </dl></td>
<td><dl> <dt><span id="_comm_status__or__fault_status__with_pickling_requires_-Oicf"></span><span id="_comm_status__or__fault_status__with_pickling_requires_-oicf"></span><span id="_COMM_STATUS__OR__FAULT_STATUS__WITH_PICKLING_REQUIRES_-OICF"></span>[comm_status] ou [fault_status] avec picking requires-Oicf</dt> <dd> Le mode d’optimisation ancien-<strong>OI</strong> ne prend pas en charge les procédures ou les paramètres avec [ <a href="comm-status.md"><strong>comm_status</strong></a>] ou [ <a href="fault-status.md"><strong>fault_status</strong></a>] avec picking (à l’aide de [ <a href="encode.md"><strong>encode</strong></a>] et/ou [ <a href="decode.md"><strong>Decode</strong></a>]).<br/> Cet avertissement peut être supprimé globalement en spécifiant-<strong>Oicf</strong> sur la ligne de commande MIDL ou pour une fonction individuelle en ajoutant l’attribut [optimize ( &quot; ICF :)] à la fonction dans le fichier ACF.<br/> En général, le mode d’optimisation-<strong>Oicf</strong> est recommandé sur le mode-<strong>OI</strong> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2406"></span><span id="midl2406"></span><dl> <dt><strong>MIDL2406</strong></dt> </dl></td>
<td><dl> <dt><span id="midl_driver_and_compiler_version_mismatch"></span><span id="MIDL_DRIVER_AND_COMPILER_VERSION_MISMATCH"></span>incompatibilité des versions du compilateur et du pilote MIDL</dt> <dd> à partir de la version Windows 2000 (MIDL version 5.03.279), le compilateur midl est implémenté à l’aide de deux fichiers exécutables : Midl.exe (le pilote) et Midlc.exe (moteur de compilateur). Cette erreur indique que la version de Midl.exe ne correspond pas à la version de Midlc.exe.<br/> L’erreur peut être due à la copie Midl.exe mais pas Midlc.exe de la distribution la plus récente. Exécutez <strong>MIDL</strong> et/ou <strong>Midlc</strong> sur la ligne de commande sans aucun paramètre pour voir le numéro de version de l’exécutable.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2407"></span><span id="midl2407"></span><dl> <dt><strong>MIDL2407</strong></dt> </dl></td>
<td><dl> <dt><span id="no_intermediate_file_specified__use_Midl.exe"></span><span id="no_intermediate_file_specified__use_midl.exe"></span><span id="NO_INTERMEDIATE_FILE_SPECIFIED__USE_MIDL.EXE"></span>aucun fichier intermédiaire spécifié : utilisez Midl.exe</dt> <dd> à partir de la version Windows 2000 (MIDL version 5.03.279), le compilateur midl est implémenté à l’aide de deux fichiers exécutables : Midl.exe (le pilote) et Midlc.exe (moteur de compilateur). Cette erreur indique que Midlc.exe a été exécutée directement au lieu d’utiliser Midl.exe.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2408"></span><span id="midl2408"></span><dl> <dt><strong>MIDL2408</strong></dt> </dl></td>
<td><dl> <dt><span id="processing_problem_with_a_parameter_in_a_procedure"></span><span id="PROCESSING_PROBLEM_WITH_A_PARAMETER_IN_A_PROCEDURE"></span>problème de traitement avec un paramètre dans une procédure</dt> <dd> Cette erreur peut se produire lors de l’importation de données à partir d’un TLB et lorsqu’une procédure a un paramètre non valide. <br/> Si vous voyez cette erreur, signalez un bogue à Microsoft. Spécifiez vos fichiers IDL, fichiers ACF, fichier TLB et ligne de commande MIDL complète.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2409"></span><span id="midl2409"></span><dl> <dt><strong>MIDL2409</strong></dt> </dl></td>
<td><dl> <dt><span id="processing_problem_with_a_field_in_a_structure"></span><span id="PROCESSING_PROBLEM_WITH_A_FIELD_IN_A_STRUCTURE"></span>problème de traitement avec un champ dans une structure</dt> <dd> Cette erreur peut se produire lors de l’importation de données à partir d’un TLB et lorsqu’une structure a un champ de structure ou d’Union non valide.<br/> Si vous voyez cette erreur, signalez un bogue à Microsoft. Spécifiez vos fichiers IDL, fichiers ACF, fichier TLB et ligne de commande MIDL complète.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2410"></span><span id="midl2410"></span><dl> <dt><strong>MIDL2410</strong></dt> </dl></td>
<td><dl> <dt><span id="internal_compiler_inconsistency_detected__the_format_string_offset_is_invalid._See_the_documentation_for_more_information."></span><span id="internal_compiler_inconsistency_detected__the_format_string_offset_is_invalid._see_the_documentation_for_more_information."></span><span id="INTERNAL_COMPILER_INCONSISTENCY_DETECTED__THE_FORMAT_STRING_OFFSET_IS_INVALID._SEE_THE_DOCUMENTATION_FOR_MORE_INFORMATION."></span>incohérence du compilateur interne détectée : le décalage de la chaîne de format n’est pas valide. Pour plus d’informations, consultez la documentation.</dt> <dd> Le compilateur MIDL a détecté une valeur non valide dans ses structures de données internes. Cela peut être dû à des structures récursives ou à une violation par le compilateur de ses propres limites de représentation pour les données internes. Pour identifier et/ou contourner le problème, essayez de simplifier le fichier IDL. Pour ce faire, vous pouvez simplifier les paramètres complexes et les structures de données récursives, ou rendre le fichier IDL plus petit en le fractionnant. Ce message peut être accompagné d’une impression de diagnostic avec des informations supplémentaires sur le problème.<br/> Si vous voyez cette erreur, signalez un bogue à Microsoft. Spécifiez vos fichiers IDL, les fichiers ACF, la ligne de commande MIDL complète et la sortie de diagnostic, le cas échéant.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2411"></span><span id="midl2411"></span><dl> <dt><strong>MIDL2411</strong></dt> </dl></td>
<td><dl> <dt><span id="internal_compiler_inconsistency_detected__the_type_offset_is_invalid._See_the_documentation_for_more_information."></span><span id="internal_compiler_inconsistency_detected__the_type_offset_is_invalid._see_the_documentation_for_more_information."></span><span id="INTERNAL_COMPILER_INCONSISTENCY_DETECTED__THE_TYPE_OFFSET_IS_INVALID._SEE_THE_DOCUMENTATION_FOR_MORE_INFORMATION."></span>incohérence du compilateur interne détectée : le décalage de type n’est pas valide. Pour plus d’informations, consultez la documentation.</dt> <dd> Le compilateur MIDL a détecté une valeur non valide dans ses structures de données internes. Cela peut être dû à des structures récursives ou au compilateur qui enfreignent ses propres limites de représentation pour les données internes. Pour identifier et/ou résoudre le problème, essayez de simplifier le fichier IDL. Vous pouvez effectuer cette opération en simplifiant les paramètres complexes et les structures de données récursives, ou en rendant le fichier IDL plus petit en le fractionnant. Ce message peut être accompagné d’une impression de diagnostic avec des informations supplémentaires sur le problème.<br/> Si vous voyez cette erreur, signalez un bogue à Microsoft. Spécifiez vos fichiers IDL, les fichiers ACF, la ligne de commande MIDL complète et la sortie de diagnostic, le cas échéant.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2412"></span><span id="midl2412"></span><dl> <dt><strong>MIDL2412</strong></dt> </dl></td>
<td><dl> <dt><span id="SAFEARRAY_roo__syntax_is_not_supported_outside_of_the_library_block__use_LPSAFEARRAY_for_proxy"></span><span id="safearray_roo__syntax_is_not_supported_outside_of_the_library_block__use_lpsafearray_for_proxy"></span><span id="SAFEARRAY_ROO__SYNTAX_IS_NOT_SUPPORTED_OUTSIDE_OF_THE_LIBRARY_BLOCK__USE_LPSAFEARRAY_FOR_PROXY"></span>La syntaxe SAFEARRAY (Roo) n’est pas prise en charge en dehors du bloc de bibliothèque, utilisez LPSAFEARRAY pour le proxy</dt> <dd> Les SAFEARRAY explicitement typés ne sont pas autorisés en dehors d’un bloc de bibliothèque. Utilisez LPSAFEARRAY à la place.<br/> L’exemple suivant illustre cette erreur :<br/>
<pre class="syntax" data-space="preserve"><code>void roo(SAFEARRAY(long) *a); //MIDL2412 when outside a library block
void roo(LPSAFEAEEAY a);         //OK</code></pre>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2413"></span><span id="midl2413"></span><dl> <dt><strong>MIDL2413</strong></dt> </dl></td>
<td><dl> <dt><span id="bit_fields_are_not_supported"></span><span id="BIT_FIELDS_ARE_NOT_SUPPORTED"></span>les champs de bits ne sont pas pris en charge</dt> <dd> Les champs de bits de style C ne sont pas pris en charge par MIDL. Cela s’applique à la génération de proxy et à la génération TLB.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2414"></span><span id="midl2414"></span><dl> <dt><strong>MIDL2414</strong></dt> </dl></td>
<td><dl> <dt><span id="floating_point_or_complex_return_types_with__decode__are_not_supported_in_-Oicf__using_-OI"></span><span id="floating_point_or_complex_return_types_with__decode__are_not_supported_in_-oicf__using_-oi"></span><span id="FLOATING_POINT_OR_COMPLEX_RETURN_TYPES_WITH__DECODE__ARE_NOT_SUPPORTED_IN_-OICF__USING_-OI"></span>les types de retour à virgule flottante ou complexe avec [Decode] ne sont pas pris en charge dans-Oicf, à l’aide de-OI</dt> <dd> Les procédures avec des types de retour à virgule flottante ou structure/Union ne sont pas prises en charge dans la sélection de style-Oicf. Une solution de contournement pour 32 bits consiste à utiliser le mode d’optimisation-OI lors de la sérialisation des données (à l’aide de [Encode] et/ou [Decode]). toutefois, comme l’interpréteur de style ancien et le support de prise en charge sont prêts à être mis en œuvre après la version Windows 2000, l’utilisation de pointeurs est fortement suggérée pour résoudre ce problème. Notez également que, en règle générale, la modification d’une méthode d’interface pour utiliser un pointeur [out, ref] au lieu de la valeur de retour provoquant le problème est entièrement compatible avec le câble et peut être facilement masquée à partir de la couche d’application. <br/> Cet avertissement peut être supprimé globalement en spécifiant-OI sur la ligne de commande MIDL ou pour une fonction individuelle en ajoutant l’attribut [optimize ( &quot; i &quot; )] à la fonction dans le fichier ACF.<br/> L’exemple suivant illustre le problème :<br/> Roo. idl : <br/>
<pre class="syntax" data-space="preserve"><code>double GetDouble();</code></pre>
Roo. ACF : <br/>
<pre class="syntax" data-space="preserve"><code>[decode] GetDouble();</code></pre>
Une option permettant de contourner cette limitation consiste à passer un paramètre [out] pour conserver le résultat au lieu d’utiliser une valeur de retour :<br/> Roo. idl : <br/>
<pre class="syntax" data-space="preserve"><code>void GetDouble([out] double *result); //top level pointer is a [ref] pointer</code></pre>
Roo. ACF : <br/>
<pre class="syntax" data-space="preserve"><code>[decode] GetDouble();</code></pre>
Comme nous l’avons vu précédemment, la solution décrite ci-dessus est correcte non seulement pour les nouvelles interfaces, mais également pour les solutions de contournement pour les anciennes. La représentation filaire du nouvel &quot; argument out &quot; est la même que pour la valeur de retour (remarquez void comme nouvelle valeur de retour).<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2415"></span><span id="midl2415"></span><dl> <dt><strong>MIDL2415</strong></dt> </dl></td>
<td><dl> <dt><span id="the_return_type_is_not_supported_for_64-bit_when_using__decode_"></span><span id="THE_RETURN_TYPE_IS_NOT_SUPPORTED_FOR_64-BIT_WHEN_USING__DECODE_"></span>le type de retour n’est pas pris en charge pour 64 bits lors de l’utilisation de [Decode]</dt> <dd> Les procédures avec des types de retour à virgule flottante ou structure/Union ne sont pas prises en charge en mode 64 bits lors de la sérialisation des données (à l’aide de [ <a href="encode.md"><strong>encode</strong></a>] et/ou [ <a href="decode.md"><strong>Decode</strong></a>]). Cela est lié à l’ancien interpréteur de style OI et le sérialiseur de données ne sont pas pris en charge sur la plateforme 64 bits. Pour plus d’informations, consultez la description de MIDL2414. <br/> L’exemple suivant illustre cette erreur :<br/> Roo. idl : <br/>
<pre class="syntax" data-space="preserve"><code>double GetDouble();</code></pre>
Roo. ACF : <br/>
<pre class="syntax" data-space="preserve"><code>[decode] GetDouble();</code></pre>
Voici une solution de contournement pour les interfaces nouvelles et anciennes. Utilisez un paramètre [out] pour conserver le résultat au lieu d’utiliser une valeur de retour :<br/> Roo. idl : <br/>
<pre class="syntax" data-space="preserve"><code>void GetDouble([out] double *result); //top level pointer is a [ref] pointer.</code></pre>
Roo. ACF : <br/>
<pre class="syntax" data-space="preserve"><code>[decode] GetDouble();</code></pre>
Notez que cette solution offre une compatibilité descendante complète sur câble, car la représentation filaire d’un pointeur [ref, out] ou d’un double est identique à celle d’un double.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2416"></span><span id="midl2416"></span><dl> <dt><strong>MIDL2416</strong></dt> </dl></td>
<td><dl> <dt><span id="transmitted_type_may_not_contain_a_full_pointer_for_either__wire_marshal__or__user_marshal_"></span><span id="TRANSMITTED_TYPE_MAY_NOT_CONTAIN_A_FULL_POINTER_FOR_EITHER__WIRE_MARSHAL__OR__USER_MARSHAL_"></span>le type transmis ne peut pas contenir un pointeur complet pour [wire_marshal] ou [user_marshal]</dt> <dd> Les types avec les attributs [ <a href="wire-marshal.md"><strong>wire_marshal</strong></a>] ou [ <a href="user-marshal.md"><strong>user_marshal</strong></a>] ne peuvent pas contenir de pointeurs ([ <strong>ptr</strong>]) complets. Utilisez [ <a href="unique.md"><strong>unique</strong></a>] ou [ <a href="ref.md"><strong>ref</strong></a>] à la place.<br/> L’exemple suivant illustre cette erreur :<br/>
<pre class="syntax" data-space="preserve"><code>typedef struct
{
    [ptr] long *a;    //Should use [ref] or [unique] instead
}
st1;
typedef [wire_marshal(st1)] struct
{
    long a;
}
st2:
void roo(st2 *s);    //MIDL2416</code></pre>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2417"></span><span id="midl2417"></span><dl> <dt><strong>MIDL2417</strong></dt> </dl></td>
<td><dl> <dt><span id="transmitted_type_must_either_be_a_pointer_or_have_a_constant_size_for__wire_marshal__and__user_marshal_"></span><span id="TRANSMITTED_TYPE_MUST_EITHER_BE_A_POINTER_OR_HAVE_A_CONSTANT_SIZE_FOR__WIRE_MARSHAL__AND__USER_MARSHAL_"></span>le type transmis doit être un pointeur ou avoir une taille constante pour [wire_marshal] et [user_marshal]</dt> <dd> Les types de niveau supérieur avec les attributs [ <a href="wire-marshal.md"><strong>wire_marshal</strong></a>] ou [ <a href="user-marshal.md"><strong>user_marshal</strong></a>] doivent avoir une taille bien définie au moment de la compilation. Ils ne peuvent pas être ou contenir des tableaux conformes ou de taille variable.<br/> L’exemple suivant illustre cette erreur :<br/>
<pre class="syntax" data-space="preserve"><code>typedef struct        //Type contains variable-sized array
{
    long s;
    [size_is(s)] char a[];
}
st1;
typedef [wire_marshal(st1)] struct
{
    long a;
}
st2;
void roo(st2 *s);        //MIDL2417</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2418"></span><span id="midl2418"></span><dl> <dt><strong>MIDL2418</strong></dt> </dl></td>
<td><dl> <dt><span id="procedures_with__propget__must_have_at_least_one_parameter_or_a_return_value"></span><span id="PROCEDURES_WITH__PROPGET__MUST_HAVE_AT_LEAST_ONE_PARAMETER_OR_A_RETURN_VALUE"></span>les procédures avec [propget] doivent avoir au moins un paramètre ou une valeur de retour</dt> <dd> Les procédures avec l’attribut [propget] doivent avoir un moyen de retourner la valeur de la propriété. Ils doivent avoir au moins un paramètre [<a href="-out.md"><strong>out</strong></a>] ou une valeur de retour.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2461"></span><span id="midl2461"></span><dl> <dt><strong>MIDL2461</strong></dt> </dl></td>
<td><dl> <dt><span id="The__readonly__attribute_was_applied_at_the_method_level."></span><span id="the__readonly__attribute_was_applied_at_the_method_level."></span><span id="THE__READONLY__ATTRIBUTE_WAS_APPLIED_AT_THE_METHOD_LEVEL."></span>L’attribut [ReadOnly] a été appliqué au niveau de la méthode.</dt> <dd> L’attribut [ReadOnly] ne peut être appliqué qu’au niveau du paramètre.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2465"></span><span id="midl2465"></span><dl> <dt><strong>MIDL2465</strong></dt> </dl></td>
<td><dl> <dt><span id="Structures_containing_conformant_arrays_must_be_passed_by_reference"></span><span id="structures_containing_conformant_arrays_must_be_passed_by_reference"></span><span id="STRUCTURES_CONTAINING_CONFORMANT_ARRAYS_MUST_BE_PASSED_BY_REFERENCE"></span>Les structures contenant des tableaux conformes doivent être passées par référence</dt> <dd> Les paramètres de niveau supérieur dans RPC doivent avoir une taille bien définie au moment de la compilation. Ils ne peuvent pas être, ni contenir des tableaux conformes ou de taille variable. En outre, les utilisateurs ne peuvent pas coder/décoder un type sans taille bien définie. Les applications doivent passer une structure variable de type struct/conforme à une référence.<br/> L’exemple suivant illustre cette erreur :<br/>
<pre class="syntax" data-space="preserve"><code>typedef struct        //Type contains variable-sized array
{
    long s;
    [size_is(s)] char a[];
}
st1;
void roo(st1 s);        //MIDL2465
 
on .acf file
typedef [encode,decode] st1; //MIDL2465</code></pre>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL9008"></span><span id="midl9008"></span><dl> <dt><strong>MIDL9008</strong></dt> </dl></td>
<td><dl> <dt><span id="_internal_compiler_problem__system_error_code__-_the_compiler_cannot_continue_for_an_unknown_reason._See_documentation_for_a_workaround."></span><span id="_internal_compiler_problem__system_error_code__-_the_compiler_cannot_continue_for_an_unknown_reason._see_documentation_for_a_workaround."></span><span id="_INTERNAL_COMPILER_PROBLEM__SYSTEM_ERROR_CODE__-_THE_COMPILER_CANNOT_CONTINUE_FOR_AN_UNKNOWN_REASON._SEE_DOCUMENTATION_FOR_A_WORKAROUND."></span> problème interne du compilateur <system error code> - le compilateur ne peut pas continuer pour une raison inconnue. Consultez la documentation pour obtenir une solution de contournement.</dt> <dd> Le compilateur n’a pas pu continuer et la cause de l’erreur est inconnue. Le numéro d’erreur hexadécimal est un identificateur d’erreur système. La compilation a peut-être échoué en raison d’un problème externe, tel qu’une condition de mémoire insuffisante. Dans ce cas, vous trouverez plus d’informations dans Winerror. h ou Ntstatus. h. <br/> Il existe deux situations qui génèrent généralement cette erreur :<br/>
<ul>
<li>Le compilateur MIDL n’a pas pu effectuer la récupération après avoir détecté une erreur dans le fichier IDL. Si MIDL a retourné des messages d’erreur relatifs à votre fichier IDL, essayez de les corriger et de recompiler. S’il n’y a aucun message d’erreur, le compilateur peut avoir échoué avant de signaler une erreur. Recherchez une erreur de syntaxe sur la ligne pour laquelle l’erreur interne du compilateur est signalée.</li>
<li>Le compilateur MIDL n’a pas pu générer de code correct sous une option d’optimisation spécifiée. Essayez de modifier les modes de compilateur, de compiler en optimisation en mode mixte (/<a href="-os.md"><strong>OS</strong></a>) ou de supprimer toutes les optimisations. Ou recompilez à l’aide de l’indicateur/NO_FORMAT_OPT pour supprimer l’optimisation par défaut de MIDL des descripteurs de procédure et de type.</li>
</ul>
Parfois, cette erreur se produit même lorsque le fichier IDL est correct et qu’aucune option d’optimisation n’est utilisée. Si c’est le cas, essayez de réécrire la section de code à proximité de l’endroit où l’erreur a été signalée en supprimant les modifications récentes, en simplifiant ou en réorganisant les types de données, en modifiant les prototypes, ou bien commencer à commenter des parties du fichier IDL pour localiser le code de problème.<br/> Si aucune de ces options ne fonctionne, ou si vous pensez que le problème peut être lié à un bogue dans Midl.exe, contactez Microsoft, en donnant tous les détails appropriés.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



 

