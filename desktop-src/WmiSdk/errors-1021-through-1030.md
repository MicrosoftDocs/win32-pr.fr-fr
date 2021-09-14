---
description: Décrit les erreurs du fournisseur SNMP WMI 1021 à 1033.
ms.assetid: fc638d0f-20f4-46d0-a36a-c3898415f35c
ms.tgt_platform: multiple
title: Erreurs 1021 à 1030
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8b7b7c914354e1865d8f3da47f076ddd785a7ec
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127237071"
---
# <a name="errors-1021-through-1030"></a>Erreurs 1021 à 1030

Décrit les erreurs du fournisseur SNMP WMI 1021 à 1033.

[Erreur irrécupérable 1021](#fatal-error-1021)

[Erreur irrécupérable 1022](#fatal-error-1022)

[Erreur irrécupérable 1023](#fatal-error-1023)

[Erreur irrécupérable 1024](#fatal-error-1024)

[Erreur irrécupérable 1025](#fatal-error-1025)

[Erreur irrécupérable 1026](#fatal-error-1026)

[AVERTISSEMENT 1027](#warning-1027)

[Erreur irrécupérable 1028](#fatal-error-1028)

[Erreur irrécupérable 1029](#fatal-error-1029)

[Erreur irrécupérable 1030](#fatal-error-1030)

## <a name="fatal-error-1021"></a>Erreur irrécupérable 1021

<dl> <dt>

<span id="_1021__Fatal_____fileName__line____Identifier__identifier__in_the_VARIABLES_clause_of_TRAP-TYPE_does_not_resolve_to_a_scalar_OBJECT-TYPE_"></span><span id="_1021__fatal_____filename__line____identifier__identifier__in_the_variables_clause_of_trap-type_does_not_resolve_to_a_scalar_object-type_"></span><span id="_1021__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_THE_VARIABLES_CLAUSE_OF_TRAP-TYPE_DOES_NOT_RESOLVE_TO_A_SCALAR_OBJECT-TYPE_"></span>**<1021,> irrécupérable : " &lt; fileName &gt;<Line \#> : identifier identificateur &lt; &gt; dans la clause variables de Trap-type n’est pas résolu en type Object-type scalaire"**
</dt> <dd>

**Interruption-type de** macro invocation, erreur sémantique du module spécifique à SNMPv1. Chaque élément de la liste des variables utilisées dans la clause VARIABLES d’un appel de macro de **type interruption** doit correspondre au nom d’une instance de type objet scalaire.

</dd> </dl>

## <a name="fatal-error-1022"></a>Erreur irrécupérable 1022

<dl> <dt>

<span id="_1022__Fatal_____fileName__line____Value_does_not_resolve_to_type__type__"></span><span id="_1022__fatal_____filename__line____value_does_not_resolve_to_type__type__"></span><span id="_1022__FATAL_____FILENAME__LINE____VALUE_DOES_NOT_RESOLVE_TO_TYPE__TYPE__"></span>**<1022,> fatale : " &lt; nomfichier &gt;<ligne \#> : la valeur n’est pas résolue en type type &lt; &gt; "**
</dt> <dd>

Erreur de sémantique du module d’assignation de valeur, propre à SNMPv1 et SNMPv2C. Le type de la valeur sur le RHS d’un entier, d’une valeur **null**, d’une chaîne d’octet ou d’une attribution de valeur d’identificateur d’objet est incorrect.

</dd> </dl>

## <a name="fatal-error-1023"></a>Erreur irrécupérable 1023

<dl> <dt>

<span id="_1023__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_to_the_type__identifier__"></span><span id="_1023__fatal_____filename__line____identifier__identifier__does_not_resolve_to_the_type__identifier__"></span><span id="_1023__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_TO_THE_TYPE__IDENTIFIER__"></span>**<1023,> irrécupérable : " &lt; nomfichier &gt;<ligne \#> : l’identificateur &lt; d’identificateur &gt; ne correspond pas à l' &lt; identificateur de type &gt; "**
</dt> <dd>

Erreur de sémantique du module d’assignation de valeur, propre à SNMPv1 et SNMPv2C. Un symbole (référence de valeur) sur le RHS d’un entier, une valeur **null**, une chaîne d’octet ou une assignation de valeur d’identificateur d’objet ne se résout pas vers le type approprié.

</dd> </dl>

## <a name="fatal-error-1024"></a>Erreur irrécupérable 1024

<dl> <dt>

<span id="_1024__Fatal_____fileName__line____Negative_integer_in_OID_value_definition_"></span><span id="_1024__fatal_____filename__line____negative_integer_in_oid_value_definition_"></span><span id="_1024__FATAL_____FILENAME__LINE____NEGATIVE_INTEGER_IN_OID_VALUE_DEFINITION_"></span>**<1024,> irrécupérable : " &lt; nomfichier &gt;<ligne \#> : entier négatif dans la définition de valeur OID"**
</dt> <dd>

Erreur de sémantique du module d’assignation de valeur, propre à SNMPv1 et SNMPv2C. Toutes les valeurs d’une liste de composants OID doivent être des entiers non négatifs (de préférence positive).

</dd> </dl>

## <a name="fatal-error-1025"></a>Erreur irrécupérable 1025

<dl> <dt>

<span id="_1025__Fatal____Identifier__identifier__in_OID_value_does_not_resolve_to_a_positive_integer_"></span><span id="_1025__fatal____identifier__identifier__in_oid_value_does_not_resolve_to_a_positive_integer_"></span><span id="_1025__FATAL____IDENTIFIER__IDENTIFIER__IN_OID_VALUE_DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1025,> irrécupérable : « l’identificateur &lt; &gt; de l’identificateur dans la valeur OID n’est pas résolu en entier positif »**
</dt> <dd>

Erreur de sémantique du module d’assignation de valeur, propre à SNMPv1 et SNMPv2C. Toutes les valeurs d’une liste de composants OID doivent être des entiers non négatifs (de préférence positive).

</dd> </dl>

## <a name="fatal-error-1026"></a>Erreur irrécupérable 1026

<dl> <dt>

<span id="_1026__Fatal_____fileName__line____Identifier__identifier__in_OID_value_neither_resolves_to_an_OID_value_nor_a_positive_integer_"></span><span id="_1026__fatal_____filename__line____identifier__identifier__in_oid_value_neither_resolves_to_an_oid_value_nor_a_positive_integer_"></span><span id="_1026__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_OID_VALUE_NEITHER_RESOLVES_TO_AN_OID_VALUE_NOR_A_POSITIVE_INTEGER_"></span>**<1026,> irrécupérable : " &lt; nomfichier &gt;<ligne \#> : &lt; l’identificateur d’identificateur &gt; dans la valeur OID n’est pas résolu en valeur OID ni en entier positif"**
</dt> <dd>

Erreur de sémantique du module d’assignation de valeur, propre à SNMPv1 et SNMPv2C. Le premier composant utilisé dans une valeur OID doit être résolu en valeur OID ou en entier.

</dd> </dl>

## <a name="warning-1027"></a>AVERTISSEMENT 1027

<dl> <dt>

<span id="_1027__Warning_____fileName__line____Imported_symbol__identifier__unused_"></span><span id="_1027__warning_____filename__line____imported_symbol__identifier__unused_"></span><span id="_1027__WARNING_____FILENAME__LINE____IMPORTED_SYMBOL__IDENTIFIER__UNUSED_"></span>**<1027, avertissement> : « &lt; nom de fichier &gt;<ligne \#> : identificateur de symbole importé &lt; &gt; inutilisé »**
</dt> <dd>

IMPORTE la section Avertissement sémantique de module, spécifique à ni SNMPv1 ni SNMPv2C. Un avertissement est émis pour chaque symbole importé inutilisé.

</dd> </dl>

## <a name="fatal-error-1028"></a>Erreur irrécupérable 1028

<dl> <dt>

<span id="_1028__Fatal____Module__identifier__not_imported_in_the_IMPORTS_section_"></span><span id="_1028__fatal____module__identifier__not_imported_in_the_imports_section_"></span><span id="_1028__FATAL____MODULE__IDENTIFIER__NOT_IMPORTED_IN_THE_IMPORTS_SECTION_"></span>**<1028,> irrécupérable : « &lt; identificateur de module &gt; non importé dans la section Imports »**
</dt> <dd>

Erreur de sémantique du module d’importation, propre à SNMPv1 et SNMPv2C. Un nom de module utilisé pour faire référence à un symbole doit être présent dans la clause Imports ou être le nom du module actuel.

</dd> </dl>

## <a name="fatal-error-1029"></a>Erreur irrécupérable 1029

<dl> <dt>

<span id="_1029__Fatal_____fileName__line____Current_module__identifier__cannot_be_imported_"></span><span id="_1029__fatal_____filename__line____current_module__identifier__cannot_be_imported_"></span><span id="_1029__FATAL_____FILENAME__LINE____CURRENT_MODULE__IDENTIFIER__CANNOT_BE_IMPORTED_"></span>**<1029,> irrécupérable : " &lt; nom_fichier &gt;<ligne \#> : l’identificateur de module actuel &lt; &gt; ne peut pas être importé"**
</dt> <dd>

Erreur de sémantique du module d’importation, propre à SNMPv1 et SNMPv2C. Le nom du module actuel figure également dans la liste des importations.

</dd> </dl>

## <a name="fatal-error-1030"></a>Erreur irrécupérable 1030

<dl> <dt>

<span id="_1030__Fatal____fileName__line____Symbol__identifier__not_imported_from_Module__identifier__"></span><span id="_1030__fatal____filename__line____symbol__identifier__not_imported_from_module__identifier__"></span><span id="_1030__FATAL____FILENAME__LINE____SYMBOL__IDENTIFIER__NOT_IMPORTED_FROM_MODULE__IDENTIFIER__"></span>**<1030,> irrécupérable : " &lt; nomfichier &gt;<ligne \#> : &lt; identificateur de symbole &gt; non importé à partir de l’identificateur de module &lt; &gt; "**
</dt> <dd>

Erreur de sémantique du module d’importation, propre à SNMPv1 et SNMPv2C. Vous avez utilisé la notation « module. Symbol », mais le symbole n’a pas été importé à partir du module spécifié dans la section Imports.

</dd> </dl>

 

 



