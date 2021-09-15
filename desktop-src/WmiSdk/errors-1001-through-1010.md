---
description: Décrit les erreurs du fournisseur SNMP WMI 1001 à 1010.
ms.assetid: dbc0e062-6b2f-41b1-8d6a-ab2c37d2dd1f
ms.tgt_platform: multiple
title: Erreurs 1001 à 1010
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc5c754936d8900a16b89be1f1137984ee6e7d40
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127526185"
---
# <a name="errors-1001-through-1010"></a>Erreurs 1001 à 1010

Décrit les erreurs du fournisseur SNMP WMI 1001 à 1010.

[Erreur irrécupérable 1001](#fatal-error-1001)

[Erreur irrécupérable 1002](#fatal-error-1002)

[Erreur irrécupérable 1003](#fatal-error-1003)

[AVERTISSEMENT 1004](#warning-1004)

[AVERTISSEMENT 1005](#warning-1005)

[Erreur irrécupérable 1006](#fatal-error-1006)

[Erreur irrécupérable 1008](#fatal-error-1008)

## <a name="fatal-error-1001"></a>Erreur irrécupérable 1001

<dl> <dt>

<span id="_1001__Fatal_____fileName___line____SYNTAX_clause_of_OBJECT-TYPE_does_not_resolve_to_allowed_types_"></span><span id="_1001__fatal_____filename___line____syntax_clause_of_object-type_does_not_resolve_to_allowed_types_"></span><span id="_1001__FATAL_____FILENAME___LINE____SYNTAX_CLAUSE_OF_OBJECT-TYPE_DOES_NOT_RESOLVE_TO_ALLOWED_TYPES_"></span><1001,> fatale : " &lt; filename &gt; : <Line \#> : la clause Syntax d’Object-type n’est pas résolue en types autorisés"
</dt> <dd>

Erreur sémantique du module d’appel de macro de TYPE objet. La clause de syntaxe de la macro de TYPE objet doit être résolue en un type ou un sous-type, formé à l’aide de la spécification de taille ou de plage autorisée par le SMI ou SNMPv2C SMI. Si ce n’est pas le cas, l’erreur irrécupérable 1001 est signalée.

Cette erreur peut se produire lors de la compilation d’un MIB ou SNMPv2C.

Les types autorisés par l’SMI SNMPv1 sont :

-   INTEGER
-   NULL
-   CHAÎNE D’OCTETS
-   IDENTIFICATEUR D’OBJET
-   NetworkAddress
-   IpAddress
-   Compteur
-   Jauge
-   Graduations
-   Opaque
-   DisplayString
-   PhysAddress

Les types autorisés par l’SMI SNMPv2C sont :

-   INTEGER
-   CHAÎNE D’OCTETS
-   IDENTIFICATEUR D’OBJET
-   BITS
-   Integer32
-   IpAddress
-   Counter32
-   Graduations
-   Opaque
-   Counter64
-   Unsigned32
-   DisplayString
-   PhysAddress
-   MacAddress
-   TruthValue
-   TestAndIncr
-   AutonomousType
-   InstancePointer
-   VariablePointer
-   RowPointer
-   RowStatus
-   TimeStamp
-   TimeInterval
-   DateAndTime
-   StorageType
-   Tdomain
-   Taddress

</dd> </dl>

## <a name="fatal-error-1002"></a>Erreur irrécupérable 1002

<dl> <dt>

<span id="_1002__Fatal_____fileName___line____Invalid_ACCESS_clause__clause__"></span><span id="_1002__fatal_____filename___line____invalid_access_clause__clause__"></span><span id="_1002__FATAL_____FILENAME___LINE____INVALID_ACCESS_CLAUSE__CLAUSE__"></span><1002,> fatale : " &lt; filename &gt; : <Line \#> : clause d’accès non valide &lt; &gt; "
</dt> <dd>

Erreur sémantique du module d’appel de macro de TYPE objet. Pour SNMPv1, la clause d’accès de la macro de TYPE objet doit être « lecture seule », « en écriture seule », « lecture/écriture » ou « non accessible ».

Pour SNMPv2C, la clause MAX-ACCESS doit être « lecture seule », « lecture-création », « lecture/écriture » ou « non accessible ».

</dd> </dl>

## <a name="fatal-error-1003"></a>Erreur irrécupérable 1003

<dl> <dt>

<span id="_1003__Fatal_____fileName___line____Invalid_STATUS_clause__clause__"></span><span id="_1003__fatal_____filename___line____invalid_status_clause__clause__"></span><span id="_1003__FATAL_____FILENAME___LINE____INVALID_STATUS_CLAUSE__CLAUSE__"></span><1003,> fatale : " &lt; filename &gt; : <Line \#> : clause d’État non valide &lt; &gt; "
</dt> <dd>

Erreur sémantique du module d’appel de macro de TYPE objet. Pour SNMPv1, la clause STATUs d’un appel de macro de TYPE objet doit être « obligatoire », « facultatif », « obsolète » ou « déconseillé ».

Pour SNMPv2C, la clause STATUs d’un appel de macro de TYPE objet doit être « Current », « Deprecated » ou « obsolete ».

</dd> </dl>

## <a name="warning-1004"></a>AVERTISSEMENT 1004

<dl> <dt>

<span id="_1004__Warning_____fileName___line____OBJECT-TYPE__identifier___whose_syntax_resolves_to_one_of_the_Counter_types_does_not_end_with_the_letter__s___"></span><span id="_1004__warning_____filename___line____object-type__identifier___whose_syntax_resolves_to_one_of_the_counter_types_does_not_end_with_the_letter__s___"></span><span id="_1004__WARNING_____FILENAME___LINE____OBJECT-TYPE__IDENTIFIER___WHOSE_SYNTAX_RESOLVES_TO_ONE_OF_THE_COUNTER_TYPES_DOES_NOT_END_WITH_THE_LETTER__S___"></span><1004, avertissement> : " &lt; filename &gt; : <Line \#> : Object-type &lt; identifier &gt; , dont la syntaxe est résolue en l’un des types de compteurs ne se termine pas par le' 'de la lettre
</dt> <dd>

AVERTISSEMENT sémantique du module d’appel de macro de TYPE objet. L’identificateur d’un objet de la syntaxe Counter (SNMPv1) ou Counter32 et Counter64 (SNMPv2C) doit être pluriel.

Cet avertissement peut se produire lors de la compilation d’un MIB ou SNMPv2C.

</dd> </dl>

## <a name="warning-1005"></a>AVERTISSEMENT 1005

<dl> <dt>

<span id="_1005__Warning_____fileName___line____OBJECT-TYPE_with_SYNTAX__SEQUENCE_OF___should_have_an_ACCESS_clause__not-accessible_"></span><span id="_1005__warning_____filename___line____object-type_with_syntax__sequence_of___should_have_an_access_clause__not-accessible_"></span><span id="_1005__WARNING_____FILENAME___LINE____OBJECT-TYPE_WITH_SYNTAX__SEQUENCE_OF___SHOULD_HAVE_AN_ACCESS_CLAUSE__NOT-ACCESSIBLE_"></span><1005, avertissement> : " &lt; filename &gt; : <Line \#> : Object-type avec la syntaxe" Sequence of ", doit avoir une clause d’accès" inaccessible "
</dt> <dd>

AVERTISSEMENT sémantique du module d’appel de macro de TYPE objet. Une ligne de table ou conceptuelle (en séquence de types d’objets de séquence ou, respectivement) doit être « non accessible ».

Cet avertissement peut se produire dans SNMPv1 ou SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1006"></a>Erreur irrécupérable 1006

<dl> <dt>

<span id="_1006__Fatal_____fileName___line___OBJECT-TYPE__identifier___which_is_of_SYNTAX_SEQUENCE__does_not_have_an_INDEX_or_AUGMENTS_clause_"></span><span id="_1006__fatal_____filename___line___object-type__identifier___which_is_of_syntax_sequence__does_not_have_an_index_or_augments_clause_"></span><span id="_1006__FATAL_____FILENAME___LINE___OBJECT-TYPE__IDENTIFIER___WHICH_IS_OF_SYNTAX_SEQUENCE__DOES_NOT_HAVE_AN_INDEX_OR_AUGMENTS_CLAUSE_"></span><1006,> irrécupérable : " &lt; filename &gt; : <Line \#> Object-type &lt; identificateur &gt; , qui est une séquence de syntaxe, n’a pas de clause d’index ou d’augmentations"
</dt> <dd>

Erreur sémantique du module d’appel de macro de TYPE objet. Pour SNMPv1, la clause INDEX doit être présente pour une définition de TYPE objet dont la syntaxe correspond à un type de séquence.

Pour SNMPv2C, la clause INDEX ou l’augmentation doit être présente pour une déclaration de ligne conceptuelle.

</dd> </dl>

## <a name="fatal-error-1008"></a>Erreur irrécupérable 1008

<dl> <dt>

<span id="_1008__Fatal_____fileName___line____OBJECT-TYPE__identifier___which_is_of_SYNTAX__SEQUENCE__has_not_been_referenced_"></span><span id="_1008__fatal_____filename___line____object-type__identifier___which_is_of_syntax__sequence__has_not_been_referenced_"></span><span id="_1008__FATAL_____FILENAME___LINE____OBJECT-TYPE__IDENTIFIER___WHICH_IS_OF_SYNTAX__SEQUENCE__HAS_NOT_BEEN_REFERENCED_"></span><1008,> fatale : " &lt; filename &gt; : <Line \#> : Object-type &lt; identifier &gt; , qui est de la syntaxe" Sequence "n’a pas été référencée"
</dt> <dd>

Erreur sémantique du module d’appel de macro de TYPE objet. Un TYPE d’objet avec la clause SYNTAX comme type de séquence doit figurer dans la clause syntaxique d’un seul appel de TYPE objet qui représente une déclaration de table, autrement dit un objet avec la clause SYNTAX comme une séquence de type. Le \# paramètre de> de ligne <fait référence au deuxième point de référence.

Cette erreur peut se produire dans SNMPv1 ou SNMPv2C.

</dd> </dl>

 

 



