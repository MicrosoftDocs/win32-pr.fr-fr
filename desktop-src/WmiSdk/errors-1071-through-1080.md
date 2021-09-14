---
description: Décrit les erreurs du fournisseur SNMP WMI 1071 à 1080.
ms.assetid: c9161c96-6839-4b32-b1bd-b40af18ab314
ms.tgt_platform: multiple
title: Erreurs 1071 à 1080
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bf2171306d1a8c97c7d343a32be62f69bdaa3cb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416114"
---
# <a name="errors-1071-through-1080"></a>Erreurs 1071 à 1080

Décrit les erreurs du fournisseur SNMP WMI 1071 à 1080.

[AVERTISSEMENT 1071](#warning-1071)

[AVERTISSEMENT 1072](#warning-1072)

[Erreur irrécupérable 1074](#fatal-error-1074)

[Erreur irrécupérable 1075](#fatal-error-1075)

[Erreur irrécupérable 1077](#fatal-error-1077)

[Erreur irrécupérable 1079](#fatal-error-1079)

[AVERTISSEMENT 1080](#warning-1080)

## <a name="warning-1071"></a>AVERTISSEMENT 1071

<dl> <dt>

<span id="_1071__Warning_____fileName__line____Symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1071__warning_____filename__line____symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1071__WARNING_____FILENAME__LINE____SYMBOL__IDENTIFIER__NOT_PRESENT_IN_IMPORTED_MODULE__IDENTIFIER__"></span>**<1071, avertissement> : « &lt; nom &gt; de fichier<ligne \#> : &lt; &gt; l’identificateur de symbole n’est pas présent dans l’identificateur de module importé &lt; &gt; »**
</dt> <dd>

AVERTISSEMENT sémantique de module concernant les références croisées, spécifiques à ni à SNMPv1 ni à SNMPv2C. Un symbole importé à partir d’un module n’est pas résolu en n’importe quoi dans ce module. Bien que ce module soit spécifié dans l’entrée, cet avertissement s’affiche.

</dd> </dl>

## <a name="warning-1072"></a>AVERTISSEMENT 1072

<dl> <dt>

<span id="_1072__Warning_____fileName___line___OBJECT-TYPE__name__is_a_descendant_of_OBJECT-TYPE__name__of_module__name__"></span><span id="_1072__warning_____filename___line___object-type__name__is_a_descendant_of_object-type__name__of_module__name__"></span><span id="_1072__WARNING_____FILENAME___LINE___OBJECT-TYPE__NAME__IS_A_DESCENDANT_OF_OBJECT-TYPE__NAME__OF_MODULE__NAME__"></span><**1072, avertissement> : " &lt; filename &gt; : <ligne \#> objet-le &lt; nom &gt; du type est un descendant du nom &lt; de type objet &gt; du nom du module &lt; &gt; "**
</dt> <dd>

AVERTISSEMENT sémantique du module d’appel **de macro de type objet** . Un objet scalaire ne peut pas avoir d’objets descendants.

Cet avertissement peut se produire dans SNMPv1 ou SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1074"></a>Erreur irrécupérable 1074

<dl> <dt>

<span id="_1074__Fatal_____fileName___line___SEQUENCE__Conceptual_row__OBJECT-TYPE__name__does_not_have_a_SEQUENCE_OF__Conceptual_table__OBJECT-TYPE_as_its_parent_"></span><span id="_1074__fatal_____filename___line___sequence__conceptual_row__object-type__name__does_not_have_a_sequence_of__conceptual_table__object-type_as_its_parent_"></span><span id="_1074__FATAL_____FILENAME___LINE___SEQUENCE__CONCEPTUAL_ROW__OBJECT-TYPE__NAME__DOES_NOT_HAVE_A_SEQUENCE_OF__CONCEPTUAL_TABLE__OBJECT-TYPE_AS_ITS_PARENT_"></span>**<1074,> irrécupérable : " &lt; filename &gt; : <Line \#> Sequence (ligne conceptuelle), objet-le &lt; nom &gt; de type n’a pas de séquence de type objet (table conceptuelle) comme parent**
</dt> <dd>

Erreur sémantique du module d’appel **de macro de type objet** . Chaque objet Row doit avoir un objet table comme parent.

Cette erreur peut se produire dans SNMPv1 ou SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1075"></a>Erreur irrécupérable 1075

<dl> <dt>

<span id="_1075__Fatal____fileName___line____OBJECT-TYPE__name__cannot_be_a_child_of_table_OBJECT-TYPE__name__of_module__name__unless_it_is_in_the_SEQUENCE_of_the_latter_"></span><span id="_1075__fatal____filename___line____object-type__name__cannot_be_a_child_of_table_object-type__name__of_module__name__unless_it_is_in_the_sequence_of_the_latter_"></span><span id="_1075__FATAL____FILENAME___LINE____OBJECT-TYPE__NAME__CANNOT_BE_A_CHILD_OF_TABLE_OBJECT-TYPE__NAME__OF_MODULE__NAME__UNLESS_IT_IS_IN_THE_SEQUENCE_OF_THE_LATTER_"></span>**<1075,> fatale : " &lt; filename &gt; : <Line \#> : Object-type &lt; name &gt; ne peut pas être un enfant de table Object-type &lt; name &gt; du nom du module &lt; &gt; , sauf s’il est dans la séquence de ce dernier**
</dt> <dd>

Erreur sémantique du module d’appel **de macro de type objet** . Chaque objet séquence doit avoir exactement les mêmes objets qui sont mentionnés dans la définition de type de séquence comme ses enfants. De même, chaque séquence d’objets doit avoir un seul enfant.

Cette erreur peut se produire dans SNMPv1 ou SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1077"></a>Erreur irrécupérable 1077

<dl> <dt>

<span id="_1077__Fatal_____fileName___line____The_syntax_of_table_OBJECT-TYPE__name__is_not_the_SEQUENCE_OF_the_syntax_of_the_child_OBJECT-TYPE__name__of_module__name__"></span><span id="_1077__fatal_____filename___line____the_syntax_of_table_object-type__name__is_not_the_sequence_of_the_syntax_of_the_child_object-type__name__of_module__name__"></span><span id="_1077__FATAL_____FILENAME___LINE____THE_SYNTAX_OF_TABLE_OBJECT-TYPE__NAME__IS_NOT_THE_SEQUENCE_OF_THE_SYNTAX_OF_THE_CHILD_OBJECT-TYPE__NAME__OF_MODULE__NAME__"></span>**<1077,> fatale : " &lt; filename &gt; : <Line \#> : la syntaxe du nom du type d’objet de table &lt; &gt; n’est pas la séquence de la syntaxe du nom de type d’objet enfant &lt; &gt; du nom de module &lt; &gt; "**
</dt> <dd>

Erreur sémantique du module d’appel **de macro de type objet** . La clause Syntax d’un objet table doit être la « séquence de » de la syntaxe de l’objet Row.

Cette erreur peut se produire dans SNMPv1 ou SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1079"></a>Erreur irrécupérable 1079

<dl> <dt>

<span id="_1079__Fatal___fileName___line____OBJECT-TYPE__name__is_an_extra_child_of_OBJECT-TYPE__name__of_module__name__"></span><span id="_1079__fatal___filename___line____object-type__name__is_an_extra_child_of_object-type__name__of_module__name__"></span><span id="_1079__FATAL___FILENAME___LINE____OBJECT-TYPE__NAME__IS_AN_EXTRA_CHILD_OF_OBJECT-TYPE__NAME__OF_MODULE__NAME__"></span>**<1079,> fatale : "fileName> : <Line \#> : Object-type &lt; name &gt; est un enfant supplémentaire du nom Object-type &lt; &gt; du &lt; nom du module &gt; "**
</dt> <dd>

Erreur sémantique du module d’appel **de macro de type objet** . Chaque séquence d’objets doit avoir un seul enfant.

Cette erreur peut se produire dans SNMPv1 ou SNMPv2C.

</dd> </dl>

## <a name="warning-1080"></a>AVERTISSEMENT 1080

<dl> <dt>

<span id="_1080__Warning_____fileName__line____MIB_Module__moduleName___from_which_symbol__symbolName__is_imported__is_not_present_in_input_"></span><span id="_1080__warning_____filename__line____mib_module__modulename___from_which_symbol__symbolname__is_imported__is_not_present_in_input_"></span><span id="_1080__WARNING_____FILENAME__LINE____MIB_MODULE__MODULENAME___FROM_WHICH_SYMBOL__SYMBOLNAME__IS_IMPORTED__IS_NOT_PRESENT_IN_INPUT_"></span>**<1080, Warning> : " &lt; fileName &gt;<Line \#> : MIB module &lt; modulename &gt; , à partir duquel le symbole &lt; symbolName &gt; est importé, n’est pas présent dans l’entrée"**
</dt> <dd>

AVERTISSEMENT sémantique de module concernant les références croisées, spécifiques à ni à SNMPv1 ni à SNMPv2C. Si l’un des modules de la section Imports du module principal ou d’un module subsidiaire n’existe pas, mais que les symboles de ce module ne sont pas référencés, cet avertissement s’affiche.

</dd> </dl>

 

 



