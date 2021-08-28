---
description: Décrit les erreurs du fournisseur SNMP WMI 1011 à 1020.
ms.assetid: 5151a110-1532-48cc-832a-2cee21853b6b
ms.tgt_platform: multiple
title: Erreurs 1011 à 1020
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49642dd17180b32a683ec7937553dbe60c60584e
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886978"
---
# <a name="errors-1011-through-1020"></a>Erreurs 1011 à 1020

Décrit les erreurs du fournisseur SNMP WMI 1011 à 1020.

[Erreur irrécupérable 1011](#fatal-error-1011)

[Erreur irrécupérable 1012](#fatal-error-1012)

[Erreur irrécupérable 1013](#fatal-error-1013)

[AVERTISSEMENT 1014](#warning-1014)

[Erreur irrécupérable 1015](#fatal-error-1015)

[Erreur irrécupérable 1016](#fatal-error-1016)

[Erreur irrécupérable 1018](#fatal-error-1018)

[Erreur irrécupérable 1020](#fatal-error-1020)

## <a name="fatal-error-1011"></a>Erreur irrécupérable 1011

<dl> <dt>

<span id="_1011__Fatal_____fileName___line___the_SYNTAX_of_member__identifier__of_SEQUENCE___identifier___differs_from_the_SYNTAX_clause_of_the_OBJECT-TYPE_"></span><span id="_1011__fatal_____filename___line___the_syntax_of_member__identifier__of_sequence___identifier___differs_from_the_syntax_clause_of_the_object-type_"></span><span id="_1011__FATAL_____FILENAME___LINE___THE_SYNTAX_OF_MEMBER__IDENTIFIER__OF_SEQUENCE___IDENTIFIER___DIFFERS_FROM_THE_SYNTAX_CLAUSE_OF_THE_OBJECT-TYPE_"></span>**<1011,> fatale : " &lt; filename &gt; : <ligne \#> la syntaxe de l’identificateur de membre &lt; &gt; de la séquence, de l' &lt; identificateur &gt; , diffère de la clause de syntaxe du type d’objet"**
</dt> <dd>

Erreur sémantique du module d’appel **de macro de type objet** . Un élément d’une séquence doit être identique au type dans la clause de syntaxe de la définition de TYPE objet. Le paramètre <Line \#> est la ligne de la clause Syntax de la définition de type objet.

Cette erreur peut se produire dans SNMPv1 ou SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1012"></a>Erreur irrécupérable 1012

<dl> <dt>

<span id="_1012__Fatal_____fileName___line___An_INDEX_or_AUGMENTS_clause_is_required_only_for_SEQUENCE_OBJECT-TYPES_"></span><span id="_1012__fatal_____filename___line___an_index_or_augments_clause_is_required_only_for_sequence_object-types_"></span><span id="_1012__FATAL_____FILENAME___LINE___AN_INDEX_OR_AUGMENTS_CLAUSE_IS_REQUIRED_ONLY_FOR_SEQUENCE_OBJECT-TYPES_"></span>**<1012,> irrécupérable : " &lt; filename &gt; : <ligne \#> un index ou une clause d’augmentation n’est requise que pour les types d’objet Sequence**
</dt> <dd>

Erreur sémantique du module d’appel **de macro de type objet** . Une clause d’INDEX ne doit être présente que dans une définition de TYPE objet dont la syntaxe correspond à un type de séquence.

Cette erreur peut se produire lors de la compilation d’un MIB ou SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1013"></a>Erreur irrécupérable 1013

<dl> <dt>

<span id="_1013__Fatal_____fileName__line_____identifier__should_resolve_to_a_SEQUENCE_type_"></span><span id="_1013__fatal_____filename__line_____identifier__should_resolve_to_a_sequence_type_"></span><span id="_1013__FATAL_____FILENAME__LINE_____IDENTIFIER__SHOULD_RESOLVE_TO_A_SEQUENCE_TYPE_"></span>**<1013,> irrécupérable : " &lt; nomfichier &gt;<ligne \#> : l' &lt; identificateur &gt; doit être résolu en type de séquence"**
</dt> <dd>

Erreur sémantique du module d’appel **de macro de type objet** . Un type utilisé dans la construction « SEQUENCE OF » doit être résolu en un type de séquence.

Cette erreur peut se produire dans SNMPv1 ou SNMPv2C.

</dd> </dl>

## <a name="warning-1014"></a>AVERTISSEMENT 1014

<dl> <dt>

<span id="_1014__Warning_____fileName___line____Sub-identifier_of_value_0_not_recommended_in_OIDs_"></span><span id="_1014__warning_____filename___line____sub-identifier_of_value_0_not_recommended_in_oids_"></span><span id="_1014__WARNING_____FILENAME___LINE____SUB-IDENTIFIER_OF_VALUE_0_NOT_RECOMMENDED_IN_OIDS_"></span>**<1014, avertissement> : " &lt; NomFichier &gt; : <ligne \#> : sous-identificateur de valeur 0 non recommandé dans les OID"**
</dt> <dd>

AVERTISSEMENT sémantique du module d’appel **de macro de type objet** . Il est recommandé qu’aucun objet dans une base de MIB standard Internet n’utilise un sous-identificateur de zéro dans son identificateur d’objet.

Cet avertissement peut se produire dans SNMPv1 ou SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1015"></a>Erreur irrécupérable 1015

<dl> <dt>

<span id="_1015__Fatal_____fileName___line____OBJECT-TYPEs__identifier__from_module__identifier__and__identifier__from_module__identifier__are_assigned_the_same_OID_values_"></span><span id="_1015__fatal_____filename___line____object-types__identifier__from_module__identifier__and__identifier__from_module__identifier__are_assigned_the_same_oid_values_"></span><span id="_1015__FATAL_____FILENAME___LINE____OBJECT-TYPES__IDENTIFIER__FROM_MODULE__IDENTIFIER__AND__IDENTIFIER__FROM_MODULE__IDENTIFIER__ARE_ASSIGNED_THE_SAME_OID_VALUES_"></span>**<1015,> fatale : " &lt; filename &gt; : <ligne \#> : &lt; l’identificateur OBJECT-TYPEs de l’identificateur de &gt; module &lt; &gt; et &lt; l’identificateur &gt; de module &lt; identifier se voient &gt; attribuer les mêmes valeurs OID"**
</dt> <dd>

Erreur sémantique du module d’appel **de macro de type objet** . Deux appels de **type objet** (dans des modules identiques ou différents) ne doivent pas recevoir la même valeur d’identificateur d’objet.

Cette erreur peut se produire dans SNMPv1 ou SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1016"></a>Erreur irrécupérable 1016

<dl> <dt>

<span id="_1016__Fatal_____fileName___line____Value_in_the_DEFVAL_clause_does_not_match_the_type_in_the_SYNTAX_clause_"></span><span id="_1016__fatal_____filename___line____value_in_the_defval_clause_does_not_match_the_type_in_the_syntax_clause_"></span><span id="_1016__FATAL_____FILENAME___LINE____VALUE_IN_THE_DEFVAL_CLAUSE_DOES_NOT_MATCH_THE_TYPE_IN_THE_SYNTAX_CLAUSE_"></span>**<1016,> fatale : " &lt; filename &gt; : <Line \#> : value dans la clause DEFVAL ne correspond pas au type dans la clause Syntax"**
</dt> <dd>

Erreur sémantique du module d’appel **de macro de type objet** . Une valeur dans une clause DEFVAL doit être une valeur du type mentionné dans la clause SYNTAX.

Cette erreur peut se produire dans SNMPv1 ou SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1018"></a>Erreur irrécupérable 1018

<dl> <dt>

<span id="_1018__Fatal_____fileName__line_____symbol__in_ENTERPRISE_clause_of_TRAP-TYPE_does_not_resolve_to_an_OID_value_"></span><span id="_1018__fatal_____filename__line_____symbol__in_enterprise_clause_of_trap-type_does_not_resolve_to_an_oid_value_"></span><span id="_1018__FATAL_____FILENAME__LINE_____SYMBOL__IN_ENTERPRISE_CLAUSE_OF_TRAP-TYPE_DOES_NOT_RESOLVE_TO_AN_OID_VALUE_"></span>**<1018,> fatale : " &lt; fileName &gt;<Line \#> : &lt; symbol dans la &gt; clause Enterprise of Trap-type n’est pas résolu en valeur OID"**
</dt> <dd>

**Interruption-type de** macro invocation, erreur sémantique du module spécifique à SNMPv1. Le symbole utilisé dans la clause ENTERPRISE d’un appel de macro de **type Trap** doit être résolu en une valeur d’identificateur d’objet.

</dd> </dl>

## <a name="fatal-error-1020"></a>Erreur irrécupérable 1020

<dl> <dt>

<span id="_1020__Fatal_____fileName__line____Value_assigned_to_TRAP-TYPE__identifier__does_not_resolve_to_a_positive_integer_"></span><span id="_1020__fatal_____filename__line____value_assigned_to_trap-type__identifier__does_not_resolve_to_a_positive_integer_"></span><span id="_1020__FATAL_____FILENAME__LINE____VALUE_ASSIGNED_TO_TRAP-TYPE__IDENTIFIER__DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1020,> irrécupérable : " &lt; nomfichier &gt;<ligne \#> : la valeur assignée à l’identificateur de type d’interruption &lt; &gt; n’est pas résolue en entier positif"**
</dt> <dd>

**Interruption-type de** macro invocation, erreur sémantique du module spécifique à SNMPv1. Un symbole utilisé dans la spécification de la valeur de l’interruption n’est pas résolu en entier positif.

</dd> </dl>

 

 



