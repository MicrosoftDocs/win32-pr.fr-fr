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
# <a name="errors-1041-through-1050"></a><span data-ttu-id="47e7b-103">Erreurs 1041 à 1050</span><span class="sxs-lookup"><span data-stu-id="47e7b-103">Errors 1041 through 1050</span></span>

<span data-ttu-id="47e7b-104">Décrit les erreurs du fournisseur SNMP WMI 1041 à 1050.</span><span class="sxs-lookup"><span data-stu-id="47e7b-104">Describes WMI SNMP provider errors 1041 through 1050.</span></span>

[<span data-ttu-id="47e7b-105">Erreur irrécupérable 1041</span><span class="sxs-lookup"><span data-stu-id="47e7b-105">Fatal Error 1041</span></span>](#fatal-error-1041)

[<span data-ttu-id="47e7b-106">Erreur irrécupérable 1042</span><span class="sxs-lookup"><span data-stu-id="47e7b-106">Fatal Error 1042</span></span>](#fatal-error-1042)

[<span data-ttu-id="47e7b-107">AVERTISSEMENT 1043</span><span class="sxs-lookup"><span data-stu-id="47e7b-107">Warning 1043</span></span>](#warning-1043)

[<span data-ttu-id="47e7b-108">Erreur irrécupérable 1044</span><span class="sxs-lookup"><span data-stu-id="47e7b-108">Fatal Error 1044</span></span>](#fatal-error-1044)

[<span data-ttu-id="47e7b-109">AVERTISSEMENT 1045</span><span class="sxs-lookup"><span data-stu-id="47e7b-109">Warning 1045</span></span>](#warning-1045)

[<span data-ttu-id="47e7b-110">AVERTISSEMENT 1046</span><span class="sxs-lookup"><span data-stu-id="47e7b-110">Warning 1046</span></span>](#warning-1046)

[<span data-ttu-id="47e7b-111">AVERTISSEMENT 1047</span><span class="sxs-lookup"><span data-stu-id="47e7b-111">Warning 1047</span></span>](#warning-1047)

[<span data-ttu-id="47e7b-112">AVERTISSEMENT 1048</span><span class="sxs-lookup"><span data-stu-id="47e7b-112">Warning 1048</span></span>](#warning-1048)

[<span data-ttu-id="47e7b-113">Erreur irrécupérable 1049</span><span class="sxs-lookup"><span data-stu-id="47e7b-113">Fatal Error 1049</span></span>](#fatal-error-1049)

## <a name="fatal-error-1041"></a><span data-ttu-id="47e7b-114">Erreur irrécupérable 1041</span><span class="sxs-lookup"><span data-stu-id="47e7b-114">Fatal Error 1041</span></span>

<dl> <dt>

<span data-ttu-id="47e7b-115"><span id="_1041__Fatal_____fileName__line____Identifier__identifier__in_range_specification_does_not_resolve_to_an_integral_value_"></span><span id="_1041__fatal_____filename__line____identifier__identifier__in_range_specification_does_not_resolve_to_an_integral_value_"></span><span id="_1041__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_RANGE_SPECIFICATION_DOES_NOT_RESOLVE_TO_AN_INTEGRAL_VALUE_"></span>**<1041,> fatale : " <fileName><ligne \#> : <identifier> l’identificateur dans la spécification de plage n’est pas résolu en valeur intégrale"**</span><span class="sxs-lookup"><span data-stu-id="47e7b-115"><span id="_1041__Fatal_____fileName__line____Identifier__identifier__in_range_specification_does_not_resolve_to_an_integral_value_"></span><span id="_1041__fatal_____filename__line____identifier__identifier__in_range_specification_does_not_resolve_to_an_integral_value_"></span><span id="_1041__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_RANGE_SPECIFICATION_DOES_NOT_RESOLVE_TO_AN_INTEGRAL_VALUE_"></span>**<1041, Fatal>: "<fileName><line\#>: Identifier <identifier> in range specification does not resolve to an integral value"**</span></span>
</dt> <dd>

<span data-ttu-id="47e7b-116">Erreur de sémantique de module dans la spécification de la plage ou de la taille, propre à non-SNMPv1 ou SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="47e7b-116">Module semantic error in range or size specification, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="47e7b-117">Le symbole utilisé dans une spécification de taille doit être converti en OCTET STRING ou opaque.</span><span class="sxs-lookup"><span data-stu-id="47e7b-117">The symbol used in a SIZE specification must resolve to OCTET STRING or Opaque.</span></span> <span data-ttu-id="47e7b-118">Toute valeur utilisée dans la spécification d’une plage doit être un entier.</span><span class="sxs-lookup"><span data-stu-id="47e7b-118">Any value used in specifying a range must be an integer.</span></span>

</dd> </dl>

## <a name="fatal-error-1042"></a><span data-ttu-id="47e7b-119">Erreur irrécupérable 1042</span><span class="sxs-lookup"><span data-stu-id="47e7b-119">Fatal Error 1042</span></span>

<dl> <dt>

<span data-ttu-id="47e7b-120"><span id="_1042__Fatal_____fileName__line____Upper_bound_of_range_specification_is_less_than_the_lower_bound_"></span><span id="_1042__fatal_____filename__line____upper_bound_of_range_specification_is_less_than_the_lower_bound_"></span><span id="_1042__FATAL_____FILENAME__LINE____UPPER_BOUND_OF_RANGE_SPECIFICATION_IS_LESS_THAN_THE_LOWER_BOUND_"></span>**<1042,> irrécupérable : " <fileName><ligne \#> : la limite supérieure de la spécification de plage est inférieure à la limite inférieure**</span><span class="sxs-lookup"><span data-stu-id="47e7b-120"><span id="_1042__Fatal_____fileName__line____Upper_bound_of_range_specification_is_less_than_the_lower_bound_"></span><span id="_1042__fatal_____filename__line____upper_bound_of_range_specification_is_less_than_the_lower_bound_"></span><span id="_1042__FATAL_____FILENAME__LINE____UPPER_BOUND_OF_RANGE_SPECIFICATION_IS_LESS_THAN_THE_LOWER_BOUND_"></span>**<1042, Fatal>: "<fileName><line\#>: Upper bound of range specification is less than the lower bound"**</span></span>
</dt> <dd>

<span data-ttu-id="47e7b-121">Erreur de sémantique de module dans la spécification de la plage ou de la taille, propre à non-SNMPv1 ou SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="47e7b-121">Module semantic error in range or size specification, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="47e7b-122">Le symbole utilisé dans une spécification de taille doit être converti en OCTET STRING ou opaque.</span><span class="sxs-lookup"><span data-stu-id="47e7b-122">The symbol used in a SIZE specification must resolve to OCTET STRING or Opaque.</span></span> <span data-ttu-id="47e7b-123">La limite inférieure d’une plage ou d’une spécification de taille ne doit pas être supérieure à la limite supérieure.</span><span class="sxs-lookup"><span data-stu-id="47e7b-123">The lower bound of a range or SIZE specification must be no greater than the upper bound.</span></span>

</dd> </dl>

## <a name="warning-1043"></a><span data-ttu-id="47e7b-124">AVERTISSEMENT 1043</span><span class="sxs-lookup"><span data-stu-id="47e7b-124">Warning 1043</span></span>

<dl> <dt>

<span data-ttu-id="47e7b-125"><span id="_1043__Warning_____fileName___line____OBJECT-TYPE_with_SYNTAX__SEQUENCE___should_have_an_ACCESS_clause__not-accessible_"></span><span id="_1043__warning_____filename___line____object-type_with_syntax__sequence___should_have_an_access_clause__not-accessible_"></span><span id="_1043__WARNING_____FILENAME___LINE____OBJECT-TYPE_WITH_SYNTAX__SEQUENCE___SHOULD_HAVE_AN_ACCESS_CLAUSE__NOT-ACCESSIBLE_"></span>**<1043, avertissement> : " <fileName> : <ligne \#> : Object-type avec la syntaxe" Sequence ", doit avoir une clause d’accès" inaccessible "**</span><span class="sxs-lookup"><span data-stu-id="47e7b-125"><span id="_1043__Warning_____fileName___line____OBJECT-TYPE_with_SYNTAX__SEQUENCE___should_have_an_ACCESS_clause__not-accessible_"></span><span id="_1043__warning_____filename___line____object-type_with_syntax__sequence___should_have_an_access_clause__not-accessible_"></span><span id="_1043__WARNING_____FILENAME___LINE____OBJECT-TYPE_WITH_SYNTAX__SEQUENCE___SHOULD_HAVE_AN_ACCESS_CLAUSE__NOT-ACCESSIBLE_"></span>**<1043, Warning>: "<fileName>:<line\#>: OBJECT-TYPE with SYNTAX "SEQUENCE", should have an ACCESS clause "not-accessible"**</span></span>
</dt> <dd>

<span data-ttu-id="47e7b-126">AVERTISSEMENT sémantique du module d’appel **de macro de type objet** .</span><span class="sxs-lookup"><span data-stu-id="47e7b-126">**OBJECT-TYPE** macro invocation module semantic warning.</span></span> <span data-ttu-id="47e7b-127">Une ligne de table ou conceptuelle (en séquence de types d’objets de séquence ou, respectivement) doit être « non accessible ».</span><span class="sxs-lookup"><span data-stu-id="47e7b-127">A table or conceptual row (SEQUENCE OF or SEQUENCE object types, respectively) must be "not-accessible."</span></span>

<span data-ttu-id="47e7b-128">Cet avertissement peut se produire dans SNMPv1 ou SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="47e7b-128">This warning can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

## <a name="fatal-error-1044"></a><span data-ttu-id="47e7b-129">Erreur irrécupérable 1044</span><span class="sxs-lookup"><span data-stu-id="47e7b-129">Fatal Error 1044</span></span>

<dl> <dt>

<span data-ttu-id="47e7b-130"><span id="_1044__Fatal_____fileName__line____Redefinition_of_symbol__identifier__"></span><span id="_1044__fatal_____filename__line____redefinition_of_symbol__identifier__"></span><span id="_1044__FATAL_____FILENAME__LINE____REDEFINITION_OF_SYMBOL__IDENTIFIER__"></span>**<1044,> irrécupérable : " <fileName><\#> de ligne : redéfinition du symbole <identifier> "**</span><span class="sxs-lookup"><span data-stu-id="47e7b-130"><span id="_1044__Fatal_____fileName__line____Redefinition_of_symbol__identifier__"></span><span id="_1044__fatal_____filename__line____redefinition_of_symbol__identifier__"></span><span id="_1044__FATAL_____FILENAME__LINE____REDEFINITION_OF_SYMBOL__IDENTIFIER__"></span>**<1044, Fatal>: "<fileName><line\#>: Redefinition of symbol <identifier>"**</span></span>
</dt> <dd>

<span data-ttu-id="47e7b-131">Erreur de sémantique de module, propre à SNMPv1 et SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="47e7b-131">Module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="47e7b-132">La redéfinition des descripteurs d’objets, des appels de macro et des types ASN. 1 génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="47e7b-132">Redefinition of object descriptors, macro invocations, and ASN.1 types cause an error.</span></span>

</dd> </dl>

## <a name="warning-1045"></a><span data-ttu-id="47e7b-133">AVERTISSEMENT 1045</span><span class="sxs-lookup"><span data-stu-id="47e7b-133">Warning 1045</span></span>

<dl> <dt>

<span data-ttu-id="47e7b-134"><span id="_1045__Warning_____fileName__lineReference_to_standard_symbol__symbolName__assumed_to_be_for_the_definition_as_in__moduleName_._Use_the__module.symbol__notations__if_you_want_to_refer_to_the_definition_in_the_current_module_"></span><span id="_1045__warning_____filename__linereference_to_standard_symbol__symbolname__assumed_to_be_for_the_definition_as_in__modulename_._use_the__module.symbol__notations__if_you_want_to_refer_to_the_definition_in_the_current_module_"></span><span id="_1045__WARNING_____FILENAME__LINEREFERENCE_TO_STANDARD_SYMBOL__SYMBOLNAME__ASSUMED_TO_BE_FOR_THE_DEFINITION_AS_IN__MODULENAME_._USE_THE__MODULE.SYMBOL__NOTATIONS__IF_YOU_WANT_TO_REFER_TO_THE_DEFINITION_IN_THE_CURRENT_MODULE_"></span>**<1045, avertissement> : « <fileName><lineReference à un symbole standard <symbolName> supposé être pour la définition comme dans <moduleName> . Utilisez les notations « module. Symbol », si vous souhaitez faire référence à la définition dans le module actuel.**</span><span class="sxs-lookup"><span data-stu-id="47e7b-134"><span id="_1045__Warning_____fileName__lineReference_to_standard_symbol__symbolName__assumed_to_be_for_the_definition_as_in__moduleName_._Use_the__module.symbol__notations__if_you_want_to_refer_to_the_definition_in_the_current_module_"></span><span id="_1045__warning_____filename__linereference_to_standard_symbol__symbolname__assumed_to_be_for_the_definition_as_in__modulename_._use_the__module.symbol__notations__if_you_want_to_refer_to_the_definition_in_the_current_module_"></span><span id="_1045__WARNING_____FILENAME__LINEREFERENCE_TO_STANDARD_SYMBOL__SYMBOLNAME__ASSUMED_TO_BE_FOR_THE_DEFINITION_AS_IN__MODULENAME_._USE_THE__MODULE.SYMBOL__NOTATIONS__IF_YOU_WANT_TO_REFER_TO_THE_DEFINITION_IN_THE_CURRENT_MODULE_"></span>**<1045, Warning>: "<fileName><lineReference to standard symbol <symbolName> assumed to be for the definition as in <moduleName>. Use the "module.symbol" notations, if you want to refer to the definition in the current module"**</span></span>
</dt> <dd>

<span data-ttu-id="47e7b-135">AVERTISSEMENT sémantique de module, propre à SNMPv1 et SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="47e7b-135">Module semantic warning, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="47e7b-136">Un symbole connu du compilateur a été redéfini et est en cours de référencement.</span><span class="sxs-lookup"><span data-stu-id="47e7b-136">A symbol known to the compiler has been redefined, and is being referenced.</span></span> <span data-ttu-id="47e7b-137">Le compilateur suppose la définition standard du symbole.</span><span class="sxs-lookup"><span data-stu-id="47e7b-137">The compiler assumes the standard definition of the symbol.</span></span> <span data-ttu-id="47e7b-138">Par conséquent, pour utiliser une redéfinition du symbole standard, vous devez utiliser la notation « module. Symbol ».</span><span class="sxs-lookup"><span data-stu-id="47e7b-138">Therefore, to use a redefinition of the standard symbol, you must use the "Module.Symbol" notation.</span></span>

</dd> </dl>

## <a name="warning-1046"></a><span data-ttu-id="47e7b-139">AVERTISSEMENT 1046</span><span class="sxs-lookup"><span data-stu-id="47e7b-139">Warning 1046</span></span>

<dl> <dt>

<span data-ttu-id="47e7b-140"><span id="_1046__Warning_____fileName__line_____symbol__undefined._Assuming_standard_definition_"></span><span id="_1046__warning_____filename__line_____symbol__undefined._assuming_standard_definition_"></span><span id="_1046__WARNING_____FILENAME__LINE_____SYMBOL__UNDEFINED._ASSUMING_STANDARD_DEFINITION_"></span>**<1046, avertissement> : « <fileName><> de ligne \# : <symbol> non défini. Définition standard en supposant**</span><span class="sxs-lookup"><span data-stu-id="47e7b-140"><span id="_1046__Warning_____fileName__line_____symbol__undefined._Assuming_standard_definition_"></span><span id="_1046__warning_____filename__line_____symbol__undefined._assuming_standard_definition_"></span><span id="_1046__WARNING_____FILENAME__LINE_____SYMBOL__UNDEFINED._ASSUMING_STANDARD_DEFINITION_"></span>**<1046, Warning>: "<fileName><line\#>: <symbol> undefined. Assuming standard definition"**</span></span>
</dt> <dd>

<span data-ttu-id="47e7b-141">AVERTISSEMENT sémantique de module, propre à SNMPv1 et SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="47e7b-141">Module semantic warning, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="47e7b-142">Un symbole connu du compilateur ne doit pas être redéfini ou utilisé sans être importé.</span><span class="sxs-lookup"><span data-stu-id="47e7b-142">A symbol known to the compiler must not be redefined or used without being imported.</span></span>

</dd> </dl>

## <a name="warning-1047"></a><span data-ttu-id="47e7b-143">AVERTISSEMENT 1047</span><span class="sxs-lookup"><span data-stu-id="47e7b-143">Warning 1047</span></span>

<dl> <dt>

<span data-ttu-id="47e7b-144"><span id="_1047__Warning_____fileName__line____Type_definition__symbol__defined_but_not_referenced_"></span><span id="_1047__warning_____filename__line____type_definition__symbol__defined_but_not_referenced_"></span><span id="_1047__WARNING_____FILENAME__LINE____TYPE_DEFINITION__SYMBOL__DEFINED_BUT_NOT_REFERENCED_"></span>**<1047, avertissement> : « <fileName><ligne \#> : définition de type <symbol> définie mais non référencée »**</span><span class="sxs-lookup"><span data-stu-id="47e7b-144"><span id="_1047__Warning_____fileName__line____Type_definition__symbol__defined_but_not_referenced_"></span><span id="_1047__warning_____filename__line____type_definition__symbol__defined_but_not_referenced_"></span><span id="_1047__WARNING_____FILENAME__LINE____TYPE_DEFINITION__SYMBOL__DEFINED_BUT_NOT_REFERENCED_"></span>**<1047, Warning>: "<fileName><line\#>: Type definition <symbol> defined but not referenced"**</span></span>
</dt> <dd>

<span data-ttu-id="47e7b-145">AVERTISSEMENT sémantique de module, propre à SNMPv1 et SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="47e7b-145">Module semantic warning, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="47e7b-146">Toutes les assignations de valeur et définitions de type doivent être référencées quelque part.</span><span class="sxs-lookup"><span data-stu-id="47e7b-146">All value assignments and type definitions must be referenced somewhere.</span></span>

</dd> </dl>

## <a name="warning-1048"></a><span data-ttu-id="47e7b-147">AVERTISSEMENT 1048</span><span class="sxs-lookup"><span data-stu-id="47e7b-147">Warning 1048</span></span>

<dl> <dt>

<span data-ttu-id="47e7b-148"><span id="_1048__Warning_____fileName__line____Value_definition__symbol__defined_but_not_referenced_"></span><span id="_1048__warning_____filename__line____value_definition__symbol__defined_but_not_referenced_"></span><span id="_1048__WARNING_____FILENAME__LINE____VALUE_DEFINITION__SYMBOL__DEFINED_BUT_NOT_REFERENCED_"></span>**<1048, avertissement> : « <fileName><ligne \#> : définition de valeur <symbol> définie mais non référencée »**</span><span class="sxs-lookup"><span data-stu-id="47e7b-148"><span id="_1048__Warning_____fileName__line____Value_definition__symbol__defined_but_not_referenced_"></span><span id="_1048__warning_____filename__line____value_definition__symbol__defined_but_not_referenced_"></span><span id="_1048__WARNING_____FILENAME__LINE____VALUE_DEFINITION__SYMBOL__DEFINED_BUT_NOT_REFERENCED_"></span>**<1048, Warning>: "<fileName><line\#>: Value definition <symbol> defined but not referenced"**</span></span>
</dt> <dd>

<span data-ttu-id="47e7b-149">AVERTISSEMENT sémantique de module, propre à SNMPv1 et SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="47e7b-149">Module semantic warning, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="47e7b-150">Toutes les assignations de valeur et définitions de type doivent être référencées quelque part.</span><span class="sxs-lookup"><span data-stu-id="47e7b-150">All value assignments and type definitions must be referenced somewhere.</span></span>

</dd> </dl>

## <a name="fatal-error-1049"></a><span data-ttu-id="47e7b-151">Erreur irrécupérable 1049</span><span class="sxs-lookup"><span data-stu-id="47e7b-151">Fatal Error 1049</span></span>

<dl> <dt>

<span data-ttu-id="47e7b-152"><span id="_1049__Fatal_____fileName___line____DEFVAL_clause_not_allowed_for_OBJECT-TYPE_with_SYNTAX_NetworkAddress_"></span><span id="_1049__fatal_____filename___line____defval_clause_not_allowed_for_object-type_with_syntax_networkaddress_"></span><span id="_1049__FATAL_____FILENAME___LINE____DEFVAL_CLAUSE_NOT_ALLOWED_FOR_OBJECT-TYPE_WITH_SYNTAX_NETWORKADDRESS_"></span>**<1049,> irrécupérable : " <fileName> : <ligne \#> : clause DEFVAL non autorisée pour Object-type avec la syntaxe networkAddress"**</span><span class="sxs-lookup"><span data-stu-id="47e7b-152"><span id="_1049__Fatal_____fileName___line____DEFVAL_clause_not_allowed_for_OBJECT-TYPE_with_SYNTAX_NetworkAddress_"></span><span id="_1049__fatal_____filename___line____defval_clause_not_allowed_for_object-type_with_syntax_networkaddress_"></span><span id="_1049__FATAL_____FILENAME___LINE____DEFVAL_CLAUSE_NOT_ALLOWED_FOR_OBJECT-TYPE_WITH_SYNTAX_NETWORKADDRESS_"></span>**<1049, Fatal>: "<fileName>:<line\#>: DEFVAL clause not allowed for OBJECT-TYPE with SYNTAX NetworkAddress"**</span></span>
</dt> <dd>

<span data-ttu-id="47e7b-153">Erreur sémantique de module spécifique à l’appel **de macro de type objet** SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="47e7b-153">**OBJECT-TYPE** macro invocation SNMPv1-specific module semantic error.</span></span> <span data-ttu-id="47e7b-154">La clause DEFVAL n’est pas autorisée pour un TYPE d’objet dont la clause de syntaxe correspond à NetworkAddress.</span><span class="sxs-lookup"><span data-stu-id="47e7b-154">The DEFVAL clause is not allowed for an OBJECT-TYPE whose SYNTAX clause resolves to NetworkAddress.</span></span>

</dd> </dl>

 

 



