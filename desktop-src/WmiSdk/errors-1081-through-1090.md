---
description: Décrit les erreurs du fournisseur SNMP WMI 1081 à 1090.
ms.assetid: aa953c53-a61f-48e4-9234-acc450b9bdf1
ms.tgt_platform: multiple
title: Erreurs 1081 à 1090
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c1ce7b1a8c575067fe2231108e0d314af2f8dc8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416113"
---
# <a name="errors-1081-through-1090"></a>Erreurs 1081 à 1090

Décrit les erreurs du fournisseur SNMP WMI 1081 à 1090.

[Erreur irrécupérable 1081](#fatal-error-1081)

[Erreur irrécupérable 1082](#fatal-error-1082)

[Erreur irrécupérable 1084](#fatal-error-1084)

[AVERTISSEMENT 1085](#warning-1085)

[AVERTISSEMENT 1086](#warning-1086)

[Erreur irrécupérable 1087](#fatal-error-1087)

[Erreur irrécupérable 1089](#fatal-error-1089)

[Erreur irrécupérable 1090](#fatal-error-1090)

## <a name="fatal-error-1081"></a>Erreur irrécupérable 1081

<dl> <dt>

<span id="_1081__Fatal_____fileName_line____Symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1081__fatal_____filename_line____symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1081__FATAL_____FILENAME_LINE____SYMBOL__IDENTIFIER__NOT_PRESENT_IN_IMPORTED_MODULE__IDENTIFIER__"></span>**<1081,> irrécupérable : " &lt; nom &gt; \# de fichier> de ligne : &lt; &gt; l’identificateur de symbole n’est pas présent dans l’identificateur de module importé &lt; &gt; "**
</dt> <dd>

Erreur de sémantique de module dans le référence croisée, spécifique à, ou à SNMPv1 et à SNMPv2C. Un symbole importé à partir d’un module n’est pas résolu en n’importe quoi dans ce module. Si ce symbole est réellement référencé dans la MIB, cette erreur se produit.

</dd> </dl>

## <a name="fatal-error-1082"></a>Erreur irrécupérable 1082

<dl> <dt>

<span id="_1082__Fatal_____fileName___line____Invalid_STATUS_clause__clause__"></span><span id="_1082__fatal_____filename___line____invalid_status_clause__clause__"></span><span id="_1082__FATAL_____FILENAME___LINE____INVALID_STATUS_CLAUSE__CLAUSE__"></span>**<1082,> fatale : " &lt; filename &gt; : <Line \#> : clause d’État non valide &lt; &gt; "**
</dt> <dd>

**Objet-Identity** , appel de macro, erreur sémantique de module spécifique à SNMPv2c. La clause STATUs d’un appel d' **identité d’objet** doit être « Current », « Deprecated » ou « obsolete ».

</dd> </dl>

## <a name="fatal-error-1084"></a>Erreur irrécupérable 1084

<dl> <dt>

<span id="_1084__Fatal____fileName__line____MODULE-IDENTITY_required_after_the_IMPORTS_section_for_all_SNMPv2_modules_"></span><span id="_1084__fatal____filename__line____module-identity_required_after_the_imports_section_for_all_snmpv2_modules_"></span><span id="_1084__FATAL____FILENAME__LINE____MODULE-IDENTITY_REQUIRED_AFTER_THE_IMPORTS_SECTION_FOR_ALL_SNMPV2_MODULES_"></span>**<1084,> fatale : "fileName><Line \#> : module-Identity required after the IMports for the SNMPv2 modules"**
</dt> <dd>

**Module-** invocation de macro d’identité, erreur sémantique de module spécifique à SNMPv2c. Il doit y avoir un et un seul appel d' **identité de module** dans une MIB SNMPv2C, immédiatement après la section Imports.

</dd> </dl>

## <a name="warning-1085"></a>AVERTISSEMENT 1085

<dl> <dt>

<span id="_1085__Warning_____fileName__line____No_groups_found_in_module__name_._Could_not_fabricate_MODULE-IDENTITY._Attempt_to_load_the_module_into_the_SMIR_will_fail_"></span><span id="_1085__warning_____filename__line____no_groups_found_in_module__name_._could_not_fabricate_module-identity._attempt_to_load_the_module_into_the_smir_will_fail_"></span><span id="_1085__WARNING_____FILENAME__LINE____NO_GROUPS_FOUND_IN_MODULE__NAME_._COULD_NOT_FABRICATE_MODULE-IDENTITY._ATTEMPT_TO_LOAD_THE_MODULE_INTO_THE_SMIR_WILL_FAIL_"></span>**<1085, avertissement> : " &lt; fileName &gt;<ligne \#> : aucun groupe trouvé dans le &lt; nom du module &gt; . Impossible de fabriquer le MODULE-IDENTity. La tentative de chargement du module dans le stockage SMIR échouera.»**
</dt> <dd>

Sémantique de module, avertissement spécifique à SNMPv1. Cette erreur est générée si aucun groupe d’objets n’est trouvé dans un module.

</dd> </dl>

## <a name="warning-1086"></a>AVERTISSEMENT 1086

<dl> <dt>

<span id="_1086__Warning_____fileName__line____No_groups_found_in_module__name__"></span><span id="_1086__warning_____filename__line____no_groups_found_in_module__name__"></span><span id="_1086__WARNING_____FILENAME__LINE____NO_GROUPS_FOUND_IN_MODULE__NAME__"></span>**<1086, avertissement> : " &lt; fileName &gt;<ligne \#> : aucun groupe trouvé dans le &lt; nom du module &gt; "**
</dt> <dd>

Sémantique de module, avertissement spécifique à SNMPv1. Cette erreur est générée si aucun groupe d’objets n’est trouvé dans un module.

</dd> </dl>

## <a name="fatal-error-1087"></a>Erreur irrécupérable 1087

<dl> <dt>

<span id="_1087._Fatal_____fileName__line____Invalid_STATUS_clause__clause__for_a_TEXTUAL-CONVENTION_macro_"></span><span id="_1087._fatal_____filename__line____invalid_status_clause__clause__for_a_textual-convention_macro_"></span><span id="_1087._FATAL_____FILENAME__LINE____INVALID_STATUS_CLAUSE__CLAUSE__FOR_A_TEXTUAL-CONVENTION_MACRO_"></span>**<1087.> irrécupérable : " &lt; nomfichier &gt;<ligne \#> : clause d’État non valide &lt; &gt; pour une macro de Convention textuelle"**
</dt> <dd>

Assignation de type, erreur sémantique de module spécifique à SNMPv2C. La clause Status d’un appel de macro de **Convention textuelle** doit être « Current », « Deprecated » ou « obsolete ».

</dd> </dl>

## <a name="fatal-error-1089"></a>Erreur irrécupérable 1089

<dl> <dt>

<span id="_1089__Fatal_____fileName___line____Symbol__identifier__in_AUGMENTS_clause_does_not_resolve_to_a_row_OBJECT-TYPE_"></span><span id="_1089__fatal_____filename___line____symbol__identifier__in_augments_clause_does_not_resolve_to_a_row_object-type_"></span><span id="_1089__FATAL_____FILENAME___LINE____SYMBOL__IDENTIFIER__IN_AUGMENTS_CLAUSE_DOES_NOT_RESOLVE_TO_A_ROW_OBJECT-TYPE_"></span><**1089,> fatale : " &lt; filename &gt; : <ligne \#> : &lt; l’identificateur &gt; de symbole dans la clause d’augmentation n’est pas résolu en un type d’objet de ligne"**
</dt> <dd>

Erreur sémantique de module spécifique à l’appel de macro de **type objet** SNMPv2c. Si une clause d’AUGMENTATIONs est présente, l’identificateur de la clause d’AUGMENTATIONs doit être résolu en un TYPE d’objet table.

</dd> </dl>

## <a name="fatal-error-1090"></a>Erreur irrécupérable 1090

<dl> <dt>

<span id="_1090__Fatal_____fileName___line___IMPLIED_clause_is_useful_only_for_the_last_INDEX_object_"></span><span id="_1090__fatal_____filename___line___implied_clause_is_useful_only_for_the_last_index_object_"></span><span id="_1090__FATAL_____FILENAME___LINE___IMPLIED_CLAUSE_IS_USEFUL_ONLY_FOR_THE_LAST_INDEX_OBJECT_"></span>**<1090,> irrécupérable : &lt; &gt; la clause "fileName : <Line \#> implicite est utile uniquement pour le dernier objet d’index"**
</dt> <dd>

Erreur sémantique de module spécifique à l’appel de macro de **type objet** SNMPv2c. La clause IMPLICITe ne peut être associée qu’au dernier objet de la clause INDEX.

</dd> </dl>

 

 



