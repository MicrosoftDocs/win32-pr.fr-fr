---
description: Décrit les erreurs du fournisseur SNMP WMI 1021 à 1033.
ms.assetid: fc638d0f-20f4-46d0-a36a-c3898415f35c
ms.tgt_platform: multiple
title: Erreurs 1021 à 1030
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8bce9c7c4d70250fa63ad0100cf93c8d5b26984
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527627"
---
# <a name="errors-1021-through-1030"></a><span data-ttu-id="b899a-103">Erreurs 1021 à 1030</span><span class="sxs-lookup"><span data-stu-id="b899a-103">Errors 1021 through 1030</span></span>

<span data-ttu-id="b899a-104">Décrit les erreurs du fournisseur SNMP WMI 1021 à 1033.</span><span class="sxs-lookup"><span data-stu-id="b899a-104">Describes WMI SNMP provider errors 1021 through 1033.</span></span>

[<span data-ttu-id="b899a-105">Erreur irrécupérable 1021</span><span class="sxs-lookup"><span data-stu-id="b899a-105">Fatal Error 1021</span></span>](#fatal-error-1021)

[<span data-ttu-id="b899a-106">Erreur irrécupérable 1022</span><span class="sxs-lookup"><span data-stu-id="b899a-106">Fatal Error 1022</span></span>](#fatal-error-1022)

[<span data-ttu-id="b899a-107">Erreur irrécupérable 1023</span><span class="sxs-lookup"><span data-stu-id="b899a-107">Fatal Error 1023</span></span>](#fatal-error-1023)

[<span data-ttu-id="b899a-108">Erreur irrécupérable 1024</span><span class="sxs-lookup"><span data-stu-id="b899a-108">Fatal Error 1024</span></span>](#fatal-error-1024)

[<span data-ttu-id="b899a-109">Erreur irrécupérable 1025</span><span class="sxs-lookup"><span data-stu-id="b899a-109">Fatal Error 1025</span></span>](#fatal-error-1025)

[<span data-ttu-id="b899a-110">Erreur irrécupérable 1026</span><span class="sxs-lookup"><span data-stu-id="b899a-110">Fatal Error 1026</span></span>](#fatal-error-1026)

[<span data-ttu-id="b899a-111">AVERTISSEMENT 1027</span><span class="sxs-lookup"><span data-stu-id="b899a-111">Warning 1027</span></span>](#warning-1027)

[<span data-ttu-id="b899a-112">Erreur irrécupérable 1028</span><span class="sxs-lookup"><span data-stu-id="b899a-112">Fatal Error 1028</span></span>](#fatal-error-1028)

[<span data-ttu-id="b899a-113">Erreur irrécupérable 1029</span><span class="sxs-lookup"><span data-stu-id="b899a-113">Fatal Error 1029</span></span>](#fatal-error-1029)

[<span data-ttu-id="b899a-114">Erreur irrécupérable 1030</span><span class="sxs-lookup"><span data-stu-id="b899a-114">Fatal Error 1030</span></span>](#fatal-error-1030)

## <a name="fatal-error-1021"></a><span data-ttu-id="b899a-115">Erreur irrécupérable 1021</span><span class="sxs-lookup"><span data-stu-id="b899a-115">Fatal Error 1021</span></span>

<dl> <dt>

<span data-ttu-id="b899a-116"><span id="_1021__Fatal_____fileName__line____Identifier__identifier__in_the_VARIABLES_clause_of_TRAP-TYPE_does_not_resolve_to_a_scalar_OBJECT-TYPE_"></span><span id="_1021__fatal_____filename__line____identifier__identifier__in_the_variables_clause_of_trap-type_does_not_resolve_to_a_scalar_object-type_"></span><span id="_1021__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_THE_VARIABLES_CLAUSE_OF_TRAP-TYPE_DOES_NOT_RESOLVE_TO_A_SCALAR_OBJECT-TYPE_"></span>**<1021,> irrécupérable : " <fileName><line \#> : identifier <identifier> dans la clause variables de Trap-type n’est pas résolu en TYPE Object-type scalaire"**</span><span class="sxs-lookup"><span data-stu-id="b899a-116"><span id="_1021__Fatal_____fileName__line____Identifier__identifier__in_the_VARIABLES_clause_of_TRAP-TYPE_does_not_resolve_to_a_scalar_OBJECT-TYPE_"></span><span id="_1021__fatal_____filename__line____identifier__identifier__in_the_variables_clause_of_trap-type_does_not_resolve_to_a_scalar_object-type_"></span><span id="_1021__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_THE_VARIABLES_CLAUSE_OF_TRAP-TYPE_DOES_NOT_RESOLVE_TO_A_SCALAR_OBJECT-TYPE_"></span>**<1021, Fatal>: "<fileName><line\#>: Identifier <identifier> in the VARIABLES clause of TRAP-TYPE does not resolve to a scalar OBJECT-TYPE"**</span></span>
</dt> <dd>

<span data-ttu-id="b899a-117">**Interruption-type de** macro invocation, erreur sémantique du module spécifique à SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="b899a-117">**TRAP-TYPE** macro invocation, SNMPv1-specific module semantic error.</span></span> <span data-ttu-id="b899a-118">Chaque élément de la liste des variables utilisées dans la clause VARIABLES d’un appel de macro de **type interruption** doit correspondre au nom d’une instance de type objet scalaire.</span><span class="sxs-lookup"><span data-stu-id="b899a-118">Each item in the list of variables used in the VARIABLES clause of a **TRAP-TYPE** macro invocation must resolve to the name of a scalar OBJECT-TYPE instance.</span></span>

</dd> </dl>

## <a name="fatal-error-1022"></a><span data-ttu-id="b899a-119">Erreur irrécupérable 1022</span><span class="sxs-lookup"><span data-stu-id="b899a-119">Fatal Error 1022</span></span>

<dl> <dt>

<span data-ttu-id="b899a-120"><span id="_1022__Fatal_____fileName__line____Value_does_not_resolve_to_type__type__"></span><span id="_1022__fatal_____filename__line____value_does_not_resolve_to_type__type__"></span><span id="_1022__FATAL_____FILENAME__LINE____VALUE_DOES_NOT_RESOLVE_TO_TYPE__TYPE__"></span>**<1022,> irrécupérable : " <fileName><\#> de ligne : la valeur n’est pas résolue en type <type> "**</span><span class="sxs-lookup"><span data-stu-id="b899a-120"><span id="_1022__Fatal_____fileName__line____Value_does_not_resolve_to_type__type__"></span><span id="_1022__fatal_____filename__line____value_does_not_resolve_to_type__type__"></span><span id="_1022__FATAL_____FILENAME__LINE____VALUE_DOES_NOT_RESOLVE_TO_TYPE__TYPE__"></span>**<1022, Fatal>: "<fileName><line\#>: Value does not resolve to type <type>"**</span></span>
</dt> <dd>

<span data-ttu-id="b899a-121">Erreur de sémantique du module d’assignation de valeur, propre à SNMPv1 et SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="b899a-121">Value assignment module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="b899a-122">Le type de la valeur sur le RHS d’un entier, d’une valeur **null**, d’une chaîne d’octet ou d’une attribution de valeur d’identificateur d’objet est incorrect.</span><span class="sxs-lookup"><span data-stu-id="b899a-122">The value on the RHS of an INTEGER, **NULL**, OCTET STRING, or OBJECT IDENTIFIER value assignment is of the wrong type.</span></span>

</dd> </dl>

## <a name="fatal-error-1023"></a><span data-ttu-id="b899a-123">Erreur irrécupérable 1023</span><span class="sxs-lookup"><span data-stu-id="b899a-123">Fatal Error 1023</span></span>

<dl> <dt>

<span data-ttu-id="b899a-124"><span id="_1023__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_to_the_type__identifier__"></span><span id="_1023__fatal_____filename__line____identifier__identifier__does_not_resolve_to_the_type__identifier__"></span><span id="_1023__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_TO_THE_TYPE__IDENTIFIER__"></span>**<1023,> irrécupérable : " <fileName><ligne \#> : l’identificateur <identifier> n’est pas résolu en type <identifier> "**</span><span class="sxs-lookup"><span data-stu-id="b899a-124"><span id="_1023__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_to_the_type__identifier__"></span><span id="_1023__fatal_____filename__line____identifier__identifier__does_not_resolve_to_the_type__identifier__"></span><span id="_1023__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_TO_THE_TYPE__IDENTIFIER__"></span>**<1023, Fatal>: "<fileName><line\#>: Identifier <identifier> does not resolve to the type <identifier>"**</span></span>
</dt> <dd>

<span data-ttu-id="b899a-125">Erreur de sémantique du module d’assignation de valeur, propre à SNMPv1 et SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="b899a-125">Value assignment module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="b899a-126">Un symbole (référence de valeur) sur le RHS d’un entier, une valeur **null**, une chaîne d’octet ou une assignation de valeur d’identificateur d’objet ne se résout pas vers le type approprié.</span><span class="sxs-lookup"><span data-stu-id="b899a-126">A symbol (value reference) on the RHS of an INTEGER, **NULL**, OCTET STRING, or OBJECT IDENTIFIER value assignment does not resolve to the right type.</span></span>

</dd> </dl>

## <a name="fatal-error-1024"></a><span data-ttu-id="b899a-127">Erreur irrécupérable 1024</span><span class="sxs-lookup"><span data-stu-id="b899a-127">Fatal Error 1024</span></span>

<dl> <dt>

<span data-ttu-id="b899a-128"><span id="_1024__Fatal_____fileName__line____Negative_integer_in_OID_value_definition_"></span><span id="_1024__fatal_____filename__line____negative_integer_in_oid_value_definition_"></span><span id="_1024__FATAL_____FILENAME__LINE____NEGATIVE_INTEGER_IN_OID_VALUE_DEFINITION_"></span>**<1024,> irrécupérable : " <fileName><ligne \#> : entier négatif dans la définition de valeur OID"**</span><span class="sxs-lookup"><span data-stu-id="b899a-128"><span id="_1024__Fatal_____fileName__line____Negative_integer_in_OID_value_definition_"></span><span id="_1024__fatal_____filename__line____negative_integer_in_oid_value_definition_"></span><span id="_1024__FATAL_____FILENAME__LINE____NEGATIVE_INTEGER_IN_OID_VALUE_DEFINITION_"></span>**<1024, Fatal>: "<fileName><line\#>: Negative integer in OID value definition"**</span></span>
</dt> <dd>

<span data-ttu-id="b899a-129">Erreur de sémantique du module d’assignation de valeur, propre à SNMPv1 et SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="b899a-129">Value assignment module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="b899a-130">Toutes les valeurs d’une liste de composants OID doivent être des entiers non négatifs (de préférence positive).</span><span class="sxs-lookup"><span data-stu-id="b899a-130">All values in an OID component list must be non-negative (preferably positive) integers.</span></span>

</dd> </dl>

## <a name="fatal-error-1025"></a><span data-ttu-id="b899a-131">Erreur irrécupérable 1025</span><span class="sxs-lookup"><span data-stu-id="b899a-131">Fatal Error 1025</span></span>

<dl> <dt>

<span data-ttu-id="b899a-132"><span id="_1025__Fatal____Identifier__identifier__in_OID_value_does_not_resolve_to_a_positive_integer_"></span><span id="_1025__fatal____identifier__identifier__in_oid_value_does_not_resolve_to_a_positive_integer_"></span><span id="_1025__FATAL____IDENTIFIER__IDENTIFIER__IN_OID_VALUE_DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1025,> irrécupérable : « l’identificateur <identifier> dans la valeur OID n’est pas résolu en entier positif »**</span><span class="sxs-lookup"><span data-stu-id="b899a-132"><span id="_1025__Fatal____Identifier__identifier__in_OID_value_does_not_resolve_to_a_positive_integer_"></span><span id="_1025__fatal____identifier__identifier__in_oid_value_does_not_resolve_to_a_positive_integer_"></span><span id="_1025__FATAL____IDENTIFIER__IDENTIFIER__IN_OID_VALUE_DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1025, Fatal>: "Identifier <identifier> in OID value does not resolve to a positive integer"**</span></span>
</dt> <dd>

<span data-ttu-id="b899a-133">Erreur de sémantique du module d’assignation de valeur, propre à SNMPv1 et SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="b899a-133">Value assignment module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="b899a-134">Toutes les valeurs d’une liste de composants OID doivent être des entiers non négatifs (de préférence positive).</span><span class="sxs-lookup"><span data-stu-id="b899a-134">All values in an OID component list must be non-negative (preferably positive) integers.</span></span>

</dd> </dl>

## <a name="fatal-error-1026"></a><span data-ttu-id="b899a-135">Erreur irrécupérable 1026</span><span class="sxs-lookup"><span data-stu-id="b899a-135">Fatal Error 1026</span></span>

<dl> <dt>

<span data-ttu-id="b899a-136"><span id="_1026__Fatal_____fileName__line____Identifier__identifier__in_OID_value_neither_resolves_to_an_OID_value_nor_a_positive_integer_"></span><span id="_1026__fatal_____filename__line____identifier__identifier__in_oid_value_neither_resolves_to_an_oid_value_nor_a_positive_integer_"></span><span id="_1026__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_OID_VALUE_NEITHER_RESOLVES_TO_AN_OID_VALUE_NOR_A_POSITIVE_INTEGER_"></span>**<1026,> irrécupérable : « <fileName><ligne \#> : l’identificateur <identifier> dans la valeur OID n’est pas résolu en valeur OID ni en entier positif »**</span><span class="sxs-lookup"><span data-stu-id="b899a-136"><span id="_1026__Fatal_____fileName__line____Identifier__identifier__in_OID_value_neither_resolves_to_an_OID_value_nor_a_positive_integer_"></span><span id="_1026__fatal_____filename__line____identifier__identifier__in_oid_value_neither_resolves_to_an_oid_value_nor_a_positive_integer_"></span><span id="_1026__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_OID_VALUE_NEITHER_RESOLVES_TO_AN_OID_VALUE_NOR_A_POSITIVE_INTEGER_"></span>**<1026, Fatal>: "<fileName><line\#>: Identifier <identifier> in OID value neither resolves to an OID value nor a positive integer"**</span></span>
</dt> <dd>

<span data-ttu-id="b899a-137">Erreur de sémantique du module d’assignation de valeur, propre à SNMPv1 et SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="b899a-137">Value assignment module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="b899a-138">Le premier composant utilisé dans une valeur OID doit être résolu en valeur OID ou en entier.</span><span class="sxs-lookup"><span data-stu-id="b899a-138">The first component used in an OID value must resolve to an OID value or an INTEGER.</span></span>

</dd> </dl>

## <a name="warning-1027"></a><span data-ttu-id="b899a-139">AVERTISSEMENT 1027</span><span class="sxs-lookup"><span data-stu-id="b899a-139">Warning 1027</span></span>

<dl> <dt>

<span data-ttu-id="b899a-140"><span id="_1027__Warning_____fileName__line____Imported_symbol__identifier__unused_"></span><span id="_1027__warning_____filename__line____imported_symbol__identifier__unused_"></span><span id="_1027__WARNING_____FILENAME__LINE____IMPORTED_SYMBOL__IDENTIFIER__UNUSED_"></span>**<1027, avertissement> : « <fileName><ligne \#> : symbole importé <identifier> inutilisé »**</span><span class="sxs-lookup"><span data-stu-id="b899a-140"><span id="_1027__Warning_____fileName__line____Imported_symbol__identifier__unused_"></span><span id="_1027__warning_____filename__line____imported_symbol__identifier__unused_"></span><span id="_1027__WARNING_____FILENAME__LINE____IMPORTED_SYMBOL__IDENTIFIER__UNUSED_"></span>**<1027, Warning>: "<fileName><line\#>: Imported symbol <identifier> unused"**</span></span>
</dt> <dd>

<span data-ttu-id="b899a-141">IMPORTE la section Avertissement sémantique de module, spécifique à ni SNMPv1 ni SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="b899a-141">IMPORTS section module semantic warning, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="b899a-142">Un avertissement est émis pour chaque symbole importé inutilisé.</span><span class="sxs-lookup"><span data-stu-id="b899a-142">A warning is issued for every unused imported symbol.</span></span>

</dd> </dl>

## <a name="fatal-error-1028"></a><span data-ttu-id="b899a-143">Erreur irrécupérable 1028</span><span class="sxs-lookup"><span data-stu-id="b899a-143">Fatal Error 1028</span></span>

<dl> <dt>

<span data-ttu-id="b899a-144"><span id="_1028__Fatal____Module__identifier__not_imported_in_the_IMPORTS_section_"></span><span id="_1028__fatal____module__identifier__not_imported_in_the_imports_section_"></span><span id="_1028__FATAL____MODULE__IDENTIFIER__NOT_IMPORTED_IN_THE_IMPORTS_SECTION_"></span>**<1028,> fatale : « <identifier> le module n’a pas été importé dans la section Imports »**</span><span class="sxs-lookup"><span data-stu-id="b899a-144"><span id="_1028__Fatal____Module__identifier__not_imported_in_the_IMPORTS_section_"></span><span id="_1028__fatal____module__identifier__not_imported_in_the_imports_section_"></span><span id="_1028__FATAL____MODULE__IDENTIFIER__NOT_IMPORTED_IN_THE_IMPORTS_SECTION_"></span>**<1028, Fatal>: "Module <identifier> not imported in the IMPORTS section"**</span></span>
</dt> <dd>

<span data-ttu-id="b899a-145">Erreur de sémantique du module d’importation, propre à SNMPv1 et SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="b899a-145">IMPORTS section module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="b899a-146">Un nom de module utilisé pour faire référence à un symbole doit être présent dans la clause Imports ou être le nom du module actuel.</span><span class="sxs-lookup"><span data-stu-id="b899a-146">A module name used in referencing a symbol must either be present in the IMPORTS clause, or be the name of the current module.</span></span>

</dd> </dl>

## <a name="fatal-error-1029"></a><span data-ttu-id="b899a-147">Erreur irrécupérable 1029</span><span class="sxs-lookup"><span data-stu-id="b899a-147">Fatal Error 1029</span></span>

<dl> <dt>

<span data-ttu-id="b899a-148"><span id="_1029__Fatal_____fileName__line____Current_module__identifier__cannot_be_imported_"></span><span id="_1029__fatal_____filename__line____current_module__identifier__cannot_be_imported_"></span><span id="_1029__FATAL_____FILENAME__LINE____CURRENT_MODULE__IDENTIFIER__CANNOT_BE_IMPORTED_"></span>**<1029,> irrécupérable : " <fileName><ligne \#> : le module actuel <identifier> ne peut pas être importé"**</span><span class="sxs-lookup"><span data-stu-id="b899a-148"><span id="_1029__Fatal_____fileName__line____Current_module__identifier__cannot_be_imported_"></span><span id="_1029__fatal_____filename__line____current_module__identifier__cannot_be_imported_"></span><span id="_1029__FATAL_____FILENAME__LINE____CURRENT_MODULE__IDENTIFIER__CANNOT_BE_IMPORTED_"></span>**<1029, Fatal>: "<fileName><line\#>: Current module <identifier> cannot be imported"**</span></span>
</dt> <dd>

<span data-ttu-id="b899a-149">Erreur de sémantique du module d’importation, propre à SNMPv1 et SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="b899a-149">IMPORTS section module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="b899a-150">Le nom du module actuel figure également dans la liste des importations.</span><span class="sxs-lookup"><span data-stu-id="b899a-150">The name of the current module also figures in the IMPORTS list.</span></span>

</dd> </dl>

## <a name="fatal-error-1030"></a><span data-ttu-id="b899a-151">Erreur irrécupérable 1030</span><span class="sxs-lookup"><span data-stu-id="b899a-151">Fatal Error 1030</span></span>

<dl> <dt>

<span data-ttu-id="b899a-152"><span id="_1030__Fatal____fileName__line____Symbol__identifier__not_imported_from_Module__identifier__"></span><span id="_1030__fatal____filename__line____symbol__identifier__not_imported_from_module__identifier__"></span><span id="_1030__FATAL____FILENAME__LINE____SYMBOL__IDENTIFIER__NOT_IMPORTED_FROM_MODULE__IDENTIFIER__"></span>**<1030,> fatale : " <fileName><line \#> : Symbol <identifier> not imported from module <identifier> "**</span><span class="sxs-lookup"><span data-stu-id="b899a-152"><span id="_1030__Fatal____fileName__line____Symbol__identifier__not_imported_from_Module__identifier__"></span><span id="_1030__fatal____filename__line____symbol__identifier__not_imported_from_module__identifier__"></span><span id="_1030__FATAL____FILENAME__LINE____SYMBOL__IDENTIFIER__NOT_IMPORTED_FROM_MODULE__IDENTIFIER__"></span>**<1030, Fatal>:"<fileName><line\#>: Symbol <identifier> not imported from Module <identifier>"**</span></span>
</dt> <dd>

<span data-ttu-id="b899a-153">Erreur de sémantique du module d’importation, propre à SNMPv1 et SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="b899a-153">IMPORTS section module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="b899a-154">Vous avez utilisé la notation « module. Symbol », mais le symbole n’a pas été importé à partir du module spécifié dans la section Imports.</span><span class="sxs-lookup"><span data-stu-id="b899a-154">You have used the "Module.Symbol" notation, but the symbol has not been imported from the specified module in the IMPORTS section.</span></span>

</dd> </dl>

 

 



