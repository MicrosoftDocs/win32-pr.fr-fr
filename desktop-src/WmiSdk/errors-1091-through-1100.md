---
description: Décrit les erreurs du fournisseur SNMP WMI 1091 à 1100.
ms.assetid: 9b7db4fc-8ae8-46f7-a40f-e4401a335c5d
ms.tgt_platform: multiple
title: Erreurs 1091 à 1100
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cedd1fc12fa5f547e041201f5411a262ddb3a3958ef58e8bed3bfcf8270d7058
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119244319"
---
# <a name="errors-1091-through-1100"></a>Erreurs 1091 à 1100

Décrit les erreurs du fournisseur SNMP WMI 1091 à 1100.

[AVERTISSEMENT 1091](#warning-1091)

[Erreur irrécupérable 1092](#fatal-error-1092)

[Erreur irrécupérable 1093](#fatal-error-1093)

[Erreur irrécupérable 1094](#fatal-error-1094)

[Erreur irrécupérable 1095](#fatal-error-1095)

[Erreur irrécupérable 1097](#fatal-error-1097)

[Erreur irrécupérable 1098](#fatal-error-1098)

[Erreur irrécupérable 1099](#fatal-error-1099)

## <a name="warning-1091"></a>AVERTISSEMENT 1091

<dl> <dt>

<span id="_1091__Warning_____fileName___line___IMPLIED_clause_is_not_allowed_for_fixed_size_objects_"></span><span id="_1091__warning_____filename___line___implied_clause_is_not_allowed_for_fixed_size_objects_"></span><span id="_1091__WARNING_____FILENAME___LINE___IMPLIED_CLAUSE_IS_NOT_ALLOWED_FOR_FIXED_SIZE_OBJECTS_"></span>**<1091, avertissement> : « <fileName> : la ligne <\#> clause implicite n’est pas autorisée pour les objets de taille fixe »**
</dt> <dd>

Avertissement de sémantique de module spécifique à l’appel de macro de **type objet** SNMPv2c. Le mot clé IMPLICITe peut uniquement être présent pour un objet ayant une syntaxe de longueur variable, tel qu’un identificateur d’objet ou une chaîne d’OCTET de longueur variable, dans la clause d’INDEX.

</dd> </dl>

## <a name="fatal-error-1092"></a>Erreur irrécupérable 1092

<dl> <dt>

<span id="_1092__Fatal_____fileName___line___IMPLIED_clause_not_allowed_for_potentially_zero-length_objects_"></span><span id="_1092__fatal_____filename___line___implied_clause_not_allowed_for_potentially_zero-length_objects_"></span><span id="_1092__FATAL_____FILENAME___LINE___IMPLIED_CLAUSE_NOT_ALLOWED_FOR_POTENTIALLY_ZERO-LENGTH_OBJECTS_"></span>**<1092,> fatale : " <fileName> : <ligne \#> clause implicite non autorisée pour les objets potentiellement de longueur nulle.**
</dt> <dd>

Erreur sémantique de module spécifique à l’appel de macro de **type objet** SNMPv2c. La clause IMPLICITe ne peut pas être utilisée sur un objet de longueur variable si cet objet peut avoir une longueur égale à zéro.

</dd> </dl>

## <a name="fatal-error-1093"></a>Erreur irrécupérable 1093

<dl> <dt>

<span id="_1093._Fatal_____fileName__line____Only_the_type__INTEGER__can_be_enumerated_according_to_the_V1_SMI_"></span><span id="_1093._fatal_____filename__line____only_the_type__integer__can_be_enumerated_according_to_the_v1_smi_"></span><span id="_1093._FATAL_____FILENAME__LINE____ONLY_THE_TYPE__INTEGER__CAN_BE_ENUMERATED_ACCORDING_TO_THE_V1_SMI_"></span>**<1093.> irrécupérable : « <fileName><ligne \#> : seul le type «Integer » peut être énuméré selon l’SMI v1»**
</dt> <dd>

Assignation de type, erreur sémantique de module spécifique à SNMPv1. Une énumération SNMPv1 MIB ne peut utiliser que le type INTEGER.

</dd> </dl>

## <a name="fatal-error-1094"></a>Erreur irrécupérable 1094

<dl> <dt>

<span id="_1094._Fatal_____fileName__line____The_type_used_in_the_enumeration_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1094._fatal_____filename__line____the_type_used_in_the_enumeration_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1094._FATAL_____FILENAME__LINE____THE_TYPE_USED_IN_THE_ENUMERATION_DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1094.> irrécupérable : « <fileName><ligne \#> : le type utilisé dans l’énumération n’est pas résolu en l’un des types autorisés »**
</dt> <dd>

Assignation de type, erreur sémantique de module spécifique à SNMPv2C. Le type utilisé dans une énumération doit être un entier ou un type équivalent, ou une autre énumération.

</dd> </dl>

## <a name="fatal-error-1095"></a>Erreur irrécupérable 1095

<dl> <dt>

<span id="_1095._Fatal_____fileName__line____Enumeration_member_is_not_a_member_of_the_parent_enumeration_"></span><span id="_1095._fatal_____filename__line____enumeration_member_is_not_a_member_of_the_parent_enumeration_"></span><span id="_1095._FATAL_____FILENAME__LINE____ENUMERATION_MEMBER_IS_NOT_A_MEMBER_OF_THE_PARENT_ENUMERATION_"></span>**<1095.> irrécupérable : « <fileName><ligne \#> : le membre de l’énumération n’est pas un membre de l’énumération parente »**
</dt> <dd>

Assignation de type, erreur sémantique de module spécifique à SNMPv2C. Si une autre énumération est utilisée, son ensemble d’éléments doit être un sous-ensemble de l’ensemble d’éléments de l’énumération parente.

</dd> </dl>

## <a name="fatal-error-1097"></a>Erreur irrécupérable 1097

<dl> <dt>

<span id="_1097__Fatal_____fileName__line____identifier__name__does_not_resolve_to_an_integer_value_"></span><span id="_1097__fatal_____filename__line____identifier__name__does_not_resolve_to_an_integer_value_"></span><span id="_1097__FATAL_____FILENAME__LINE____IDENTIFIER__NAME__DOES_NOT_RESOLVE_TO_AN_INTEGER_VALUE_"></span>**<1097,> irrécupérable : " <fileName><ligne \#> : l’identificateur <name> n’est pas résolu en valeur entière"**
</dt> <dd>

Assignation de type, erreur sémantique de module spécifique à SNMPv2C. Les valeurs du type BITS doivent être des valeurs entières.

</dd> </dl>

## <a name="fatal-error-1098"></a>Erreur irrécupérable 1098

<dl> <dt>

<span id="_1098__Fatal_____fileName__line____Duplicate_value__value__in_BITS_construct_"></span><span id="_1098__fatal_____filename__line____duplicate_value__value__in_bits_construct_"></span><span id="_1098__FATAL_____FILENAME__LINE____DUPLICATE_VALUE__VALUE__IN_BITS_CONSTRUCT_"></span>**<1098,> irrécupérable : " <fileName><ligne \#> : valeur dupliquée <value> dans la construction bits"**
</dt> <dd>

Assignation de type, erreur sémantique de module spécifique à SNMPv2C. Il ne doit pas y avoir de noms et de valeurs en double dans une construction BITS. Le paramètre de \#> de ligne <correspond à la position de la récurrence du nom/de la valeur.

</dd> </dl>

## <a name="fatal-error-1099"></a>Erreur irrécupérable 1099

<dl> <dt>

<span id="_1099__Fatal_____fileName__line____Duplicate_name__identifier__in_BITS_construct_"></span><span id="_1099__fatal_____filename__line____duplicate_name__identifier__in_bits_construct_"></span><span id="_1099__FATAL_____FILENAME__LINE____DUPLICATE_NAME__IDENTIFIER__IN_BITS_CONSTRUCT_"></span>**<1099,> irrécupérable : " <fileName><ligne \#> : nom dupliqué <identifier> dans la construction bits"**
</dt> <dd>

Assignation de type, erreur sémantique de module spécifique à SNMPv2C. Il ne doit pas y avoir de noms et de valeurs en double dans une construction BITS. Le paramètre de \#> de ligne <correspond à la position de la récurrence du nom/de la valeur.

</dd> </dl>

 

 



