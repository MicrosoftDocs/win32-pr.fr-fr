---
description: Décrit les erreurs du fournisseur SNMP WMI 1041 à 1050.
ms.assetid: e7e70fb3-12c6-40b1-91a4-c550e8210c09
ms.tgt_platform: multiple
title: Erreurs 1041 à 1050
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 327ef466d1b1226b14d895fef81be24baee45354
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034308"
---
# <a name="errors-1041-through-1050"></a>Erreurs 1041 à 1050

Décrit les erreurs du fournisseur SNMP WMI 1041 à 1050.

[Erreur irrécupérable 1041](#fatal-error-1041)

[Erreur irrécupérable 1042](#fatal-error-1042)

[AVERTISSEMENT 1043](#warning-1043)

[Erreur irrécupérable 1044](#fatal-error-1044)

[AVERTISSEMENT 1045](#warning-1045)

[AVERTISSEMENT 1046](#warning-1046)

[AVERTISSEMENT 1047](#warning-1047)

[AVERTISSEMENT 1048](#warning-1048)

[Erreur irrécupérable 1049](#fatal-error-1049)

## <a name="fatal-error-1041"></a>Erreur irrécupérable 1041

<dl> <dt>

<span id="_1041__Fatal_____fileName__line____Identifier__identifier__in_range_specification_does_not_resolve_to_an_integral_value_"></span><span id="_1041__fatal_____filename__line____identifier__identifier__in_range_specification_does_not_resolve_to_an_integral_value_"></span><span id="_1041__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_RANGE_SPECIFICATION_DOES_NOT_RESOLVE_TO_AN_INTEGRAL_VALUE_"></span>**<1041,> fatale : " <fileName><ligne \#> : <identifier> l’identificateur dans la spécification de plage n’est pas résolu en valeur intégrale"**
</dt> <dd>

Erreur de sémantique de module dans la spécification de la plage ou de la taille, propre à non-SNMPv1 ou SNMPv2C. Le symbole utilisé dans une spécification de taille doit être converti en OCTET STRING ou opaque. Toute valeur utilisée dans la spécification d’une plage doit être un entier.

</dd> </dl>

## <a name="fatal-error-1042"></a>Erreur irrécupérable 1042

<dl> <dt>

<span id="_1042__Fatal_____fileName__line____Upper_bound_of_range_specification_is_less_than_the_lower_bound_"></span><span id="_1042__fatal_____filename__line____upper_bound_of_range_specification_is_less_than_the_lower_bound_"></span><span id="_1042__FATAL_____FILENAME__LINE____UPPER_BOUND_OF_RANGE_SPECIFICATION_IS_LESS_THAN_THE_LOWER_BOUND_"></span>**<1042,> irrécupérable : " <fileName><ligne \#> : la limite supérieure de la spécification de plage est inférieure à la limite inférieure**
</dt> <dd>

Erreur de sémantique de module dans la spécification de la plage ou de la taille, propre à non-SNMPv1 ou SNMPv2C. Le symbole utilisé dans une spécification de taille doit être converti en OCTET STRING ou opaque. La limite inférieure d’une plage ou d’une spécification de taille ne doit pas être supérieure à la limite supérieure.

</dd> </dl>

## <a name="warning-1043"></a>AVERTISSEMENT 1043

<dl> <dt>

<span id="_1043__Warning_____fileName___line____OBJECT-TYPE_with_SYNTAX__SEQUENCE___should_have_an_ACCESS_clause__not-accessible_"></span><span id="_1043__warning_____filename___line____object-type_with_syntax__sequence___should_have_an_access_clause__not-accessible_"></span><span id="_1043__WARNING_____FILENAME___LINE____OBJECT-TYPE_WITH_SYNTAX__SEQUENCE___SHOULD_HAVE_AN_ACCESS_CLAUSE__NOT-ACCESSIBLE_"></span>**<1043, avertissement> : " <fileName> : <ligne \#> : Object-type avec la syntaxe" Sequence ", doit avoir une clause d’accès" inaccessible "**
</dt> <dd>

AVERTISSEMENT sémantique du module d’appel **de macro de type objet** . Une ligne de table ou conceptuelle (en séquence de types d’objets de séquence ou, respectivement) doit être « non accessible ».

Cet avertissement peut se produire dans SNMPv1 ou SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1044"></a>Erreur irrécupérable 1044

<dl> <dt>

<span id="_1044__Fatal_____fileName__line____Redefinition_of_symbol__identifier__"></span><span id="_1044__fatal_____filename__line____redefinition_of_symbol__identifier__"></span><span id="_1044__FATAL_____FILENAME__LINE____REDEFINITION_OF_SYMBOL__IDENTIFIER__"></span>**<1044,> irrécupérable : " <fileName><\#> de ligne : redéfinition du symbole <identifier> "**
</dt> <dd>

Erreur de sémantique de module, propre à SNMPv1 et SNMPv2C. La redéfinition des descripteurs d’objets, des appels de macro et des types ASN. 1 génère une erreur.

</dd> </dl>

## <a name="warning-1045"></a>AVERTISSEMENT 1045

<dl> <dt>

<span id="_1045__Warning_____fileName__lineReference_to_standard_symbol__symbolName__assumed_to_be_for_the_definition_as_in__moduleName_._Use_the__module.symbol__notations__if_you_want_to_refer_to_the_definition_in_the_current_module_"></span><span id="_1045__warning_____filename__linereference_to_standard_symbol__symbolname__assumed_to_be_for_the_definition_as_in__modulename_._use_the__module.symbol__notations__if_you_want_to_refer_to_the_definition_in_the_current_module_"></span><span id="_1045__WARNING_____FILENAME__LINEREFERENCE_TO_STANDARD_SYMBOL__SYMBOLNAME__ASSUMED_TO_BE_FOR_THE_DEFINITION_AS_IN__MODULENAME_._USE_THE__MODULE.SYMBOL__NOTATIONS__IF_YOU_WANT_TO_REFER_TO_THE_DEFINITION_IN_THE_CURRENT_MODULE_"></span>**<1045, avertissement> : « <fileName><lineReference à un symbole standard <symbolName> supposé être pour la définition comme dans <moduleName> . Utilisez les notations « module. Symbol », si vous souhaitez faire référence à la définition dans le module actuel.**
</dt> <dd>

AVERTISSEMENT sémantique de module, propre à SNMPv1 et SNMPv2C. Un symbole connu du compilateur a été redéfini et est en cours de référencement. Le compilateur suppose la définition standard du symbole. Par conséquent, pour utiliser une redéfinition du symbole standard, vous devez utiliser la notation « module. Symbol ».

</dd> </dl>

## <a name="warning-1046"></a>AVERTISSEMENT 1046

<dl> <dt>

<span id="_1046__Warning_____fileName__line_____symbol__undefined._Assuming_standard_definition_"></span><span id="_1046__warning_____filename__line_____symbol__undefined._assuming_standard_definition_"></span><span id="_1046__WARNING_____FILENAME__LINE_____SYMBOL__UNDEFINED._ASSUMING_STANDARD_DEFINITION_"></span>**<1046, avertissement> : « <fileName><> de ligne \# : <symbol> non défini. Définition standard en supposant**
</dt> <dd>

AVERTISSEMENT sémantique de module, propre à SNMPv1 et SNMPv2C. Un symbole connu du compilateur ne doit pas être redéfini ou utilisé sans être importé.

</dd> </dl>

## <a name="warning-1047"></a>AVERTISSEMENT 1047

<dl> <dt>

<span id="_1047__Warning_____fileName__line____Type_definition__symbol__defined_but_not_referenced_"></span><span id="_1047__warning_____filename__line____type_definition__symbol__defined_but_not_referenced_"></span><span id="_1047__WARNING_____FILENAME__LINE____TYPE_DEFINITION__SYMBOL__DEFINED_BUT_NOT_REFERENCED_"></span>**<1047, avertissement> : « <fileName><ligne \#> : définition de type <symbol> définie mais non référencée »**
</dt> <dd>

AVERTISSEMENT sémantique de module, propre à SNMPv1 et SNMPv2C. Toutes les assignations de valeur et définitions de type doivent être référencées quelque part.

</dd> </dl>

## <a name="warning-1048"></a>AVERTISSEMENT 1048

<dl> <dt>

<span id="_1048__Warning_____fileName__line____Value_definition__symbol__defined_but_not_referenced_"></span><span id="_1048__warning_____filename__line____value_definition__symbol__defined_but_not_referenced_"></span><span id="_1048__WARNING_____FILENAME__LINE____VALUE_DEFINITION__SYMBOL__DEFINED_BUT_NOT_REFERENCED_"></span>**<1048, avertissement> : « <fileName><ligne \#> : définition de valeur <symbol> définie mais non référencée »**
</dt> <dd>

AVERTISSEMENT sémantique de module, propre à SNMPv1 et SNMPv2C. Toutes les assignations de valeur et définitions de type doivent être référencées quelque part.

</dd> </dl>

## <a name="fatal-error-1049"></a>Erreur irrécupérable 1049

<dl> <dt>

<span id="_1049__Fatal_____fileName___line____DEFVAL_clause_not_allowed_for_OBJECT-TYPE_with_SYNTAX_NetworkAddress_"></span><span id="_1049__fatal_____filename___line____defval_clause_not_allowed_for_object-type_with_syntax_networkaddress_"></span><span id="_1049__FATAL_____FILENAME___LINE____DEFVAL_CLAUSE_NOT_ALLOWED_FOR_OBJECT-TYPE_WITH_SYNTAX_NETWORKADDRESS_"></span>**<1049,> irrécupérable : " <fileName> : <ligne \#> : clause DEFVAL non autorisée pour Object-type avec la syntaxe networkAddress"**
</dt> <dd>

Erreur sémantique de module spécifique à l’appel **de macro de type objet** SNMPv1. La clause DEFVAL n’est pas autorisée pour un TYPE d’objet dont la clause de syntaxe correspond à NetworkAddress.

</dd> </dl>

 

 



