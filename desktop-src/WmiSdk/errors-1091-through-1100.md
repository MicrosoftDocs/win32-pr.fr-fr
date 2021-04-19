---
description: Décrit les erreurs du fournisseur SNMP WMI 1091 à 1100.
ms.assetid: 9b7db4fc-8ae8-46f7-a40f-e4401a335c5d
ms.tgt_platform: multiple
title: Erreurs 1091 à 1100
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf582a3df41fbc7c329f5a993555a2d76145ded0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531408"
---
# <a name="errors-1091-through-1100"></a><span data-ttu-id="de620-103">Erreurs 1091 à 1100</span><span class="sxs-lookup"><span data-stu-id="de620-103">Errors 1091 through 1100</span></span>

<span data-ttu-id="de620-104">Décrit les erreurs du fournisseur SNMP WMI 1091 à 1100.</span><span class="sxs-lookup"><span data-stu-id="de620-104">Describes WMI SNMP provider errors 1091 through 1100.</span></span>

[<span data-ttu-id="de620-105">AVERTISSEMENT 1091</span><span class="sxs-lookup"><span data-stu-id="de620-105">Warning 1091</span></span>](#warning-1091)

[<span data-ttu-id="de620-106">Erreur irrécupérable 1092</span><span class="sxs-lookup"><span data-stu-id="de620-106">Fatal Error 1092</span></span>](#fatal-error-1092)

[<span data-ttu-id="de620-107">Erreur irrécupérable 1093</span><span class="sxs-lookup"><span data-stu-id="de620-107">Fatal Error 1093</span></span>](#fatal-error-1093)

[<span data-ttu-id="de620-108">Erreur irrécupérable 1094</span><span class="sxs-lookup"><span data-stu-id="de620-108">Fatal Error 1094</span></span>](#fatal-error-1094)

[<span data-ttu-id="de620-109">Erreur irrécupérable 1095</span><span class="sxs-lookup"><span data-stu-id="de620-109">Fatal Error 1095</span></span>](#fatal-error-1095)

[<span data-ttu-id="de620-110">Erreur irrécupérable 1097</span><span class="sxs-lookup"><span data-stu-id="de620-110">Fatal Error 1097</span></span>](#fatal-error-1097)

[<span data-ttu-id="de620-111">Erreur irrécupérable 1098</span><span class="sxs-lookup"><span data-stu-id="de620-111">Fatal Error 1098</span></span>](#fatal-error-1098)

[<span data-ttu-id="de620-112">Erreur irrécupérable 1099</span><span class="sxs-lookup"><span data-stu-id="de620-112">Fatal Error 1099</span></span>](#fatal-error-1099)

## <a name="warning-1091"></a><span data-ttu-id="de620-113">AVERTISSEMENT 1091</span><span class="sxs-lookup"><span data-stu-id="de620-113">Warning 1091</span></span>

<dl> <dt>

<span data-ttu-id="de620-114"><span id="_1091__Warning_____fileName___line___IMPLIED_clause_is_not_allowed_for_fixed_size_objects_"></span><span id="_1091__warning_____filename___line___implied_clause_is_not_allowed_for_fixed_size_objects_"></span><span id="_1091__WARNING_____FILENAME___LINE___IMPLIED_CLAUSE_IS_NOT_ALLOWED_FOR_FIXED_SIZE_OBJECTS_"></span>**<1091, avertissement> : « <fileName> : la ligne <\#> clause implicite n’est pas autorisée pour les objets de taille fixe »**</span><span class="sxs-lookup"><span data-stu-id="de620-114"><span id="_1091__Warning_____fileName___line___IMPLIED_clause_is_not_allowed_for_fixed_size_objects_"></span><span id="_1091__warning_____filename___line___implied_clause_is_not_allowed_for_fixed_size_objects_"></span><span id="_1091__WARNING_____FILENAME___LINE___IMPLIED_CLAUSE_IS_NOT_ALLOWED_FOR_FIXED_SIZE_OBJECTS_"></span>**<1091, Warning>: "<fileName>:<line\#> IMPLIED clause is not allowed for fixed size objects"**</span></span>
</dt> <dd>

<span data-ttu-id="de620-115">Avertissement de sémantique de module spécifique à l’appel de macro de **type objet** SNMPv2c.</span><span class="sxs-lookup"><span data-stu-id="de620-115">**OBJECT-TYPE** macro invocation SNMPv2C-specific module semantic warning.</span></span> <span data-ttu-id="de620-116">Le mot clé IMPLICITe peut uniquement être présent pour un objet ayant une syntaxe de longueur variable, tel qu’un identificateur d’objet ou une chaîne d’OCTET de longueur variable, dans la clause d’INDEX.</span><span class="sxs-lookup"><span data-stu-id="de620-116">The IMPLIED keyword can only be present for an object having a variable-length syntax, such as an OBJECT IDENTIFIER or variable-length OCTET STRING, in the INDEX clause.</span></span>

</dd> </dl>

## <a name="fatal-error-1092"></a><span data-ttu-id="de620-117">Erreur irrécupérable 1092</span><span class="sxs-lookup"><span data-stu-id="de620-117">Fatal Error 1092</span></span>

<dl> <dt>

<span data-ttu-id="de620-118"><span id="_1092__Fatal_____fileName___line___IMPLIED_clause_not_allowed_for_potentially_zero-length_objects_"></span><span id="_1092__fatal_____filename___line___implied_clause_not_allowed_for_potentially_zero-length_objects_"></span><span id="_1092__FATAL_____FILENAME___LINE___IMPLIED_CLAUSE_NOT_ALLOWED_FOR_POTENTIALLY_ZERO-LENGTH_OBJECTS_"></span>**<1092,> fatale : " <fileName> : <ligne \#> clause implicite non autorisée pour les objets potentiellement de longueur nulle.**</span><span class="sxs-lookup"><span data-stu-id="de620-118"><span id="_1092__Fatal_____fileName___line___IMPLIED_clause_not_allowed_for_potentially_zero-length_objects_"></span><span id="_1092__fatal_____filename___line___implied_clause_not_allowed_for_potentially_zero-length_objects_"></span><span id="_1092__FATAL_____FILENAME___LINE___IMPLIED_CLAUSE_NOT_ALLOWED_FOR_POTENTIALLY_ZERO-LENGTH_OBJECTS_"></span>**<1092, Fatal>: "<fileName>:<line\#> IMPLIED clause not allowed for potentially zero-length objects"**</span></span>
</dt> <dd>

<span data-ttu-id="de620-119">Erreur sémantique de module spécifique à l’appel de macro de **type objet** SNMPv2c.</span><span class="sxs-lookup"><span data-stu-id="de620-119">**OBJECT-TYPE** macro invocation SNMPv2C-specific module semantic error.</span></span> <span data-ttu-id="de620-120">La clause IMPLICITe ne peut pas être utilisée sur un objet de longueur variable si cet objet peut avoir une longueur égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="de620-120">The IMPLIED clause cannot be used on a variable-length object if that object can have a zero length.</span></span>

</dd> </dl>

## <a name="fatal-error-1093"></a><span data-ttu-id="de620-121">Erreur irrécupérable 1093</span><span class="sxs-lookup"><span data-stu-id="de620-121">Fatal Error 1093</span></span>

<dl> <dt>

<span data-ttu-id="de620-122"><span id="_1093._Fatal_____fileName__line____Only_the_type__INTEGER__can_be_enumerated_according_to_the_V1_SMI_"></span><span id="_1093._fatal_____filename__line____only_the_type__integer__can_be_enumerated_according_to_the_v1_smi_"></span><span id="_1093._FATAL_____FILENAME__LINE____ONLY_THE_TYPE__INTEGER__CAN_BE_ENUMERATED_ACCORDING_TO_THE_V1_SMI_"></span>**<1093.> irrécupérable : « <fileName><ligne \#> : seul le type «Integer » peut être énuméré selon l’SMI v1»**</span><span class="sxs-lookup"><span data-stu-id="de620-122"><span id="_1093._Fatal_____fileName__line____Only_the_type__INTEGER__can_be_enumerated_according_to_the_V1_SMI_"></span><span id="_1093._fatal_____filename__line____only_the_type__integer__can_be_enumerated_according_to_the_v1_smi_"></span><span id="_1093._FATAL_____FILENAME__LINE____ONLY_THE_TYPE__INTEGER__CAN_BE_ENUMERATED_ACCORDING_TO_THE_V1_SMI_"></span>**<1093. Fatal>: "<fileName><line\#>: Only the type "INTEGER" can be enumerated according to the V1 SMI"**</span></span>
</dt> <dd>

<span data-ttu-id="de620-123">Assignation de type, erreur sémantique de module spécifique à SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="de620-123">Type assignment, SNMPv1-specific module semantic error.</span></span> <span data-ttu-id="de620-124">Une énumération SNMPv1 MIB ne peut utiliser que le type INTEGER.</span><span class="sxs-lookup"><span data-stu-id="de620-124">An SNMPv1 MIB enumeration can use only the type INTEGER.</span></span>

</dd> </dl>

## <a name="fatal-error-1094"></a><span data-ttu-id="de620-125">Erreur irrécupérable 1094</span><span class="sxs-lookup"><span data-stu-id="de620-125">Fatal Error 1094</span></span>

<dl> <dt>

<span data-ttu-id="de620-126"><span id="_1094._Fatal_____fileName__line____The_type_used_in_the_enumeration_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1094._fatal_____filename__line____the_type_used_in_the_enumeration_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1094._FATAL_____FILENAME__LINE____THE_TYPE_USED_IN_THE_ENUMERATION_DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1094.> irrécupérable : « <fileName><ligne \#> : le type utilisé dans l’énumération n’est pas résolu en l’un des types autorisés »**</span><span class="sxs-lookup"><span data-stu-id="de620-126"><span id="_1094._Fatal_____fileName__line____The_type_used_in_the_enumeration_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1094._fatal_____filename__line____the_type_used_in_the_enumeration_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1094._FATAL_____FILENAME__LINE____THE_TYPE_USED_IN_THE_ENUMERATION_DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1094. Fatal>: "<fileName><line\#>: The type used in the enumeration does not resolve to one of the allowed types"**</span></span>
</dt> <dd>

<span data-ttu-id="de620-127">Assignation de type, erreur sémantique de module spécifique à SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="de620-127">Type assignment, SNMPv2C-specific module semantic error.</span></span> <span data-ttu-id="de620-128">Le type utilisé dans une énumération doit être un entier ou un type équivalent, ou une autre énumération.</span><span class="sxs-lookup"><span data-stu-id="de620-128">The type used in an enumeration must be INTEGER or an equivalent type, or another enumeration.</span></span>

</dd> </dl>

## <a name="fatal-error-1095"></a><span data-ttu-id="de620-129">Erreur irrécupérable 1095</span><span class="sxs-lookup"><span data-stu-id="de620-129">Fatal Error 1095</span></span>

<dl> <dt>

<span data-ttu-id="de620-130"><span id="_1095._Fatal_____fileName__line____Enumeration_member_is_not_a_member_of_the_parent_enumeration_"></span><span id="_1095._fatal_____filename__line____enumeration_member_is_not_a_member_of_the_parent_enumeration_"></span><span id="_1095._FATAL_____FILENAME__LINE____ENUMERATION_MEMBER_IS_NOT_A_MEMBER_OF_THE_PARENT_ENUMERATION_"></span>**<1095.> irrécupérable : « <fileName><ligne \#> : le membre de l’énumération n’est pas un membre de l’énumération parente »**</span><span class="sxs-lookup"><span data-stu-id="de620-130"><span id="_1095._Fatal_____fileName__line____Enumeration_member_is_not_a_member_of_the_parent_enumeration_"></span><span id="_1095._fatal_____filename__line____enumeration_member_is_not_a_member_of_the_parent_enumeration_"></span><span id="_1095._FATAL_____FILENAME__LINE____ENUMERATION_MEMBER_IS_NOT_A_MEMBER_OF_THE_PARENT_ENUMERATION_"></span>**<1095. Fatal>: "<fileName><line\#>: Enumeration member is not a member of the parent enumeration"**</span></span>
</dt> <dd>

<span data-ttu-id="de620-131">Assignation de type, erreur sémantique de module spécifique à SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="de620-131">Type assignment, SNMPv2C-specific module semantic error.</span></span> <span data-ttu-id="de620-132">Si une autre énumération est utilisée, son ensemble d’éléments doit être un sous-ensemble de l’ensemble d’éléments de l’énumération parente.</span><span class="sxs-lookup"><span data-stu-id="de620-132">If another enumeration is used, its set of items must be a subset of the parent enumeration's set of items.</span></span>

</dd> </dl>

## <a name="fatal-error-1097"></a><span data-ttu-id="de620-133">Erreur irrécupérable 1097</span><span class="sxs-lookup"><span data-stu-id="de620-133">Fatal Error 1097</span></span>

<dl> <dt>

<span data-ttu-id="de620-134"><span id="_1097__Fatal_____fileName__line____identifier__name__does_not_resolve_to_an_integer_value_"></span><span id="_1097__fatal_____filename__line____identifier__name__does_not_resolve_to_an_integer_value_"></span><span id="_1097__FATAL_____FILENAME__LINE____IDENTIFIER__NAME__DOES_NOT_RESOLVE_TO_AN_INTEGER_VALUE_"></span>**<1097,> irrécupérable : " <fileName><ligne \#> : l’identificateur <name> n’est pas résolu en valeur entière"**</span><span class="sxs-lookup"><span data-stu-id="de620-134"><span id="_1097__Fatal_____fileName__line____identifier__name__does_not_resolve_to_an_integer_value_"></span><span id="_1097__fatal_____filename__line____identifier__name__does_not_resolve_to_an_integer_value_"></span><span id="_1097__FATAL_____FILENAME__LINE____IDENTIFIER__NAME__DOES_NOT_RESOLVE_TO_AN_INTEGER_VALUE_"></span>**<1097, Fatal>: "<fileName><line\#>: identifier <name> does not resolve to an integer value"**</span></span>
</dt> <dd>

<span data-ttu-id="de620-135">Assignation de type, erreur sémantique de module spécifique à SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="de620-135">Type assignment, SNMPv2C-specific module semantic error.</span></span> <span data-ttu-id="de620-136">Les valeurs du type BITS doivent être des valeurs entières.</span><span class="sxs-lookup"><span data-stu-id="de620-136">The values in the BITS type must be integer values.</span></span>

</dd> </dl>

## <a name="fatal-error-1098"></a><span data-ttu-id="de620-137">Erreur irrécupérable 1098</span><span class="sxs-lookup"><span data-stu-id="de620-137">Fatal Error 1098</span></span>

<dl> <dt>

<span data-ttu-id="de620-138"><span id="_1098__Fatal_____fileName__line____Duplicate_value__value__in_BITS_construct_"></span><span id="_1098__fatal_____filename__line____duplicate_value__value__in_bits_construct_"></span><span id="_1098__FATAL_____FILENAME__LINE____DUPLICATE_VALUE__VALUE__IN_BITS_CONSTRUCT_"></span>**<1098,> irrécupérable : " <fileName><ligne \#> : valeur dupliquée <value> dans la construction bits"**</span><span class="sxs-lookup"><span data-stu-id="de620-138"><span id="_1098__Fatal_____fileName__line____Duplicate_value__value__in_BITS_construct_"></span><span id="_1098__fatal_____filename__line____duplicate_value__value__in_bits_construct_"></span><span id="_1098__FATAL_____FILENAME__LINE____DUPLICATE_VALUE__VALUE__IN_BITS_CONSTRUCT_"></span>**<1098, Fatal>: "<fileName><line\#>: Duplicate value <value> in BITS construct"**</span></span>
</dt> <dd>

<span data-ttu-id="de620-139">Assignation de type, erreur sémantique de module spécifique à SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="de620-139">Type assignment, SNMPv2C-specific module semantic error.</span></span> <span data-ttu-id="de620-140">Il ne doit pas y avoir de noms et de valeurs en double dans une construction BITS.</span><span class="sxs-lookup"><span data-stu-id="de620-140">There must be no duplicate names and values in a BITS construct.</span></span> <span data-ttu-id="de620-141">Le paramètre de \#> de ligne <correspond à la position de la récurrence du nom/de la valeur.</span><span class="sxs-lookup"><span data-stu-id="de620-141">The <line\#> parameter is the position of the recurrence of the name/value.</span></span>

</dd> </dl>

## <a name="fatal-error-1099"></a><span data-ttu-id="de620-142">Erreur irrécupérable 1099</span><span class="sxs-lookup"><span data-stu-id="de620-142">Fatal Error 1099</span></span>

<dl> <dt>

<span data-ttu-id="de620-143"><span id="_1099__Fatal_____fileName__line____Duplicate_name__identifier__in_BITS_construct_"></span><span id="_1099__fatal_____filename__line____duplicate_name__identifier__in_bits_construct_"></span><span id="_1099__FATAL_____FILENAME__LINE____DUPLICATE_NAME__IDENTIFIER__IN_BITS_CONSTRUCT_"></span>**<1099,> irrécupérable : " <fileName><ligne \#> : nom dupliqué <identifier> dans la construction bits"**</span><span class="sxs-lookup"><span data-stu-id="de620-143"><span id="_1099__Fatal_____fileName__line____Duplicate_name__identifier__in_BITS_construct_"></span><span id="_1099__fatal_____filename__line____duplicate_name__identifier__in_bits_construct_"></span><span id="_1099__FATAL_____FILENAME__LINE____DUPLICATE_NAME__IDENTIFIER__IN_BITS_CONSTRUCT_"></span>**<1099, Fatal>: "<fileName><line\#>: Duplicate name <identifier> in BITS construct"**</span></span>
</dt> <dd>

<span data-ttu-id="de620-144">Assignation de type, erreur sémantique de module spécifique à SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="de620-144">Type assignment, SNMPv2C-specific module semantic error.</span></span> <span data-ttu-id="de620-145">Il ne doit pas y avoir de noms et de valeurs en double dans une construction BITS.</span><span class="sxs-lookup"><span data-stu-id="de620-145">There must be no duplicate names and values in a BITS construct.</span></span> <span data-ttu-id="de620-146">Le paramètre de \#> de ligne <correspond à la position de la récurrence du nom/de la valeur.</span><span class="sxs-lookup"><span data-stu-id="de620-146">The <line\#> parameter is the position of the recurrence of the name/value.</span></span>

</dd> </dl>

 

 



