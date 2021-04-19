---
description: Décrit les erreurs du fournisseur SNMP WMI 1071 à 1080.
ms.assetid: c9161c96-6839-4b32-b1bd-b40af18ab314
ms.tgt_platform: multiple
title: Erreurs 1071 à 1080
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 277aa7dd69d674ebc16bc0a2b4d104c349e593a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538202"
---
# <a name="errors-1071-through-1080"></a><span data-ttu-id="6041f-103">Erreurs 1071 à 1080</span><span class="sxs-lookup"><span data-stu-id="6041f-103">Errors 1071 through 1080</span></span>

<span data-ttu-id="6041f-104">Décrit les erreurs du fournisseur SNMP WMI 1071 à 1080.</span><span class="sxs-lookup"><span data-stu-id="6041f-104">Describes WMI SNMP provider errors 1071 through 1080.</span></span>

[<span data-ttu-id="6041f-105">AVERTISSEMENT 1071</span><span class="sxs-lookup"><span data-stu-id="6041f-105">Warning 1071</span></span>](#warning-1071)

[<span data-ttu-id="6041f-106">AVERTISSEMENT 1072</span><span class="sxs-lookup"><span data-stu-id="6041f-106">Warning 1072</span></span>](#warning-1072)

[<span data-ttu-id="6041f-107">Erreur irrécupérable 1074</span><span class="sxs-lookup"><span data-stu-id="6041f-107">Fatal Error 1074</span></span>](#fatal-error-1074)

[<span data-ttu-id="6041f-108">Erreur irrécupérable 1075</span><span class="sxs-lookup"><span data-stu-id="6041f-108">Fatal Error 1075</span></span>](#fatal-error-1075)

[<span data-ttu-id="6041f-109">Erreur irrécupérable 1077</span><span class="sxs-lookup"><span data-stu-id="6041f-109">Fatal Error 1077</span></span>](#fatal-error-1077)

[<span data-ttu-id="6041f-110">Erreur irrécupérable 1079</span><span class="sxs-lookup"><span data-stu-id="6041f-110">Fatal Error 1079</span></span>](#fatal-error-1079)

[<span data-ttu-id="6041f-111">AVERTISSEMENT 1080</span><span class="sxs-lookup"><span data-stu-id="6041f-111">Warning 1080</span></span>](#warning-1080)

## <a name="warning-1071"></a><span data-ttu-id="6041f-112">AVERTISSEMENT 1071</span><span class="sxs-lookup"><span data-stu-id="6041f-112">Warning 1071</span></span>

<dl> <dt>

<span data-ttu-id="6041f-113"><span id="_1071__Warning_____fileName__line____Symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1071__warning_____filename__line____symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1071__WARNING_____FILENAME__LINE____SYMBOL__IDENTIFIER__NOT_PRESENT_IN_IMPORTED_MODULE__IDENTIFIER__"></span>**<1071, avertissement> : « <fileName><ligne \#> : symbole <identifier> non présent dans le module importé <identifier> »**</span><span class="sxs-lookup"><span data-stu-id="6041f-113"><span id="_1071__Warning_____fileName__line____Symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1071__warning_____filename__line____symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1071__WARNING_____FILENAME__LINE____SYMBOL__IDENTIFIER__NOT_PRESENT_IN_IMPORTED_MODULE__IDENTIFIER__"></span>**<1071, Warning>: "<fileName><line\#>: Symbol <identifier> not present in imported module <identifier>"**</span></span>
</dt> <dd>

<span data-ttu-id="6041f-114">AVERTISSEMENT sémantique de module concernant les références croisées, spécifiques à ni à SNMPv1 ni à SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="6041f-114">Module semantic warning about cross-referencing, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="6041f-115">Un symbole importé à partir d’un module n’est pas résolu en n’importe quoi dans ce module.</span><span class="sxs-lookup"><span data-stu-id="6041f-115">A symbol imported from a module does not resolve to anything in that module.</span></span> <span data-ttu-id="6041f-116">Bien que ce module soit spécifié dans l’entrée, cet avertissement s’affiche.</span><span class="sxs-lookup"><span data-stu-id="6041f-116">Even though that module is specified in the input, this warning appears.</span></span>

</dd> </dl>

## <a name="warning-1072"></a><span data-ttu-id="6041f-117">AVERTISSEMENT 1072</span><span class="sxs-lookup"><span data-stu-id="6041f-117">Warning 1072</span></span>

<dl> <dt>

<span data-ttu-id="6041f-118"><span id="_1072__Warning_____fileName___line___OBJECT-TYPE__name__is_a_descendant_of_OBJECT-TYPE__name__of_module__name__"></span><span id="_1072__warning_____filename___line___object-type__name__is_a_descendant_of_object-type__name__of_module__name__"></span><span id="_1072__WARNING_____FILENAME___LINE___OBJECT-TYPE__NAME__IS_A_DESCENDANT_OF_OBJECT-TYPE__NAME__OF_MODULE__NAME__"></span><**1072, avertissement> : " <fileName> : <ligne \#> objet-type <name> est un descendant d’un type objet <name> de module <name> "**</span><span class="sxs-lookup"><span data-stu-id="6041f-118"><span id="_1072__Warning_____fileName___line___OBJECT-TYPE__name__is_a_descendant_of_OBJECT-TYPE__name__of_module__name__"></span><span id="_1072__warning_____filename___line___object-type__name__is_a_descendant_of_object-type__name__of_module__name__"></span><span id="_1072__WARNING_____FILENAME___LINE___OBJECT-TYPE__NAME__IS_A_DESCENDANT_OF_OBJECT-TYPE__NAME__OF_MODULE__NAME__"></span><**1072, Warning>: "<fileName>:<line\#> OBJECT-TYPE <name> is a descendant of OBJECT-TYPE <name> of module <name>"**</span></span>
</dt> <dd>

<span data-ttu-id="6041f-119">AVERTISSEMENT sémantique du module d’appel **de macro de type objet** .</span><span class="sxs-lookup"><span data-stu-id="6041f-119">**OBJECT-TYPE** macro invocation module semantic warning.</span></span> <span data-ttu-id="6041f-120">Un objet scalaire ne peut pas avoir d’objets descendants.</span><span class="sxs-lookup"><span data-stu-id="6041f-120">A scalar object cannot have any descendant objects.</span></span>

<span data-ttu-id="6041f-121">Cet avertissement peut se produire dans SNMPv1 ou SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="6041f-121">This warning can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

## <a name="fatal-error-1074"></a><span data-ttu-id="6041f-122">Erreur irrécupérable 1074</span><span class="sxs-lookup"><span data-stu-id="6041f-122">Fatal Error 1074</span></span>

<dl> <dt>

<span data-ttu-id="6041f-123"><span id="_1074__Fatal_____fileName___line___SEQUENCE__Conceptual_row__OBJECT-TYPE__name__does_not_have_a_SEQUENCE_OF__Conceptual_table__OBJECT-TYPE_as_its_parent_"></span><span id="_1074__fatal_____filename___line___sequence__conceptual_row__object-type__name__does_not_have_a_sequence_of__conceptual_table__object-type_as_its_parent_"></span><span id="_1074__FATAL_____FILENAME___LINE___SEQUENCE__CONCEPTUAL_ROW__OBJECT-TYPE__NAME__DOES_NOT_HAVE_A_SEQUENCE_OF__CONCEPTUAL_TABLE__OBJECT-TYPE_AS_ITS_PARENT_"></span>**<1074,> irrécupérable : " <fileName> : <\# séquence de> de ligne (ligne conceptuelle), le type <name> d’objet n’a pas de séquence de type objet (table conceptuelle) comme parent**</span><span class="sxs-lookup"><span data-stu-id="6041f-123"><span id="_1074__Fatal_____fileName___line___SEQUENCE__Conceptual_row__OBJECT-TYPE__name__does_not_have_a_SEQUENCE_OF__Conceptual_table__OBJECT-TYPE_as_its_parent_"></span><span id="_1074__fatal_____filename___line___sequence__conceptual_row__object-type__name__does_not_have_a_sequence_of__conceptual_table__object-type_as_its_parent_"></span><span id="_1074__FATAL_____FILENAME___LINE___SEQUENCE__CONCEPTUAL_ROW__OBJECT-TYPE__NAME__DOES_NOT_HAVE_A_SEQUENCE_OF__CONCEPTUAL_TABLE__OBJECT-TYPE_AS_ITS_PARENT_"></span>**<1074, Fatal>: "<fileName>:<line\#> SEQUENCE (Conceptual row) OBJECT-TYPE <name> does not have a SEQUENCE OF (Conceptual table) OBJECT-TYPE as its parent"**</span></span>
</dt> <dd>

<span data-ttu-id="6041f-124">Erreur sémantique du module d’appel **de macro de type objet** .</span><span class="sxs-lookup"><span data-stu-id="6041f-124">**OBJECT-TYPE** macro invocation module semantic error.</span></span> <span data-ttu-id="6041f-125">Chaque objet Row doit avoir un objet table comme parent.</span><span class="sxs-lookup"><span data-stu-id="6041f-125">Every row object must have a table object as its parent.</span></span>

<span data-ttu-id="6041f-126">Cette erreur peut se produire dans SNMPv1 ou SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="6041f-126">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

## <a name="fatal-error-1075"></a><span data-ttu-id="6041f-127">Erreur irrécupérable 1075</span><span class="sxs-lookup"><span data-stu-id="6041f-127">Fatal Error 1075</span></span>

<dl> <dt>

<span data-ttu-id="6041f-128"><span id="_1075__Fatal____fileName___line____OBJECT-TYPE__name__cannot_be_a_child_of_table_OBJECT-TYPE__name__of_module__name__unless_it_is_in_the_SEQUENCE_of_the_latter_"></span><span id="_1075__fatal____filename___line____object-type__name__cannot_be_a_child_of_table_object-type__name__of_module__name__unless_it_is_in_the_sequence_of_the_latter_"></span><span id="_1075__FATAL____FILENAME___LINE____OBJECT-TYPE__NAME__CANNOT_BE_A_CHILD_OF_TABLE_OBJECT-TYPE__NAME__OF_MODULE__NAME__UNLESS_IT_IS_IN_THE_SEQUENCE_OF_THE_LATTER_"></span>**<1075,> fatale : " <fileName> : <\#> de ligne : Object-type <name> ne peut pas être un enfant de table Object-type <name> de module <name> , sauf s’il est dans la séquence de ce dernier**</span><span class="sxs-lookup"><span data-stu-id="6041f-128"><span id="_1075__Fatal____fileName___line____OBJECT-TYPE__name__cannot_be_a_child_of_table_OBJECT-TYPE__name__of_module__name__unless_it_is_in_the_SEQUENCE_of_the_latter_"></span><span id="_1075__fatal____filename___line____object-type__name__cannot_be_a_child_of_table_object-type__name__of_module__name__unless_it_is_in_the_sequence_of_the_latter_"></span><span id="_1075__FATAL____FILENAME___LINE____OBJECT-TYPE__NAME__CANNOT_BE_A_CHILD_OF_TABLE_OBJECT-TYPE__NAME__OF_MODULE__NAME__UNLESS_IT_IS_IN_THE_SEQUENCE_OF_THE_LATTER_"></span>**<1075, Fatal>:"<fileName>:<line\#>: OBJECT-TYPE <name> cannot be a child of table OBJECT-TYPE <name> of module <name> unless it is in the SEQUENCE of the latter"**</span></span>
</dt> <dd>

<span data-ttu-id="6041f-129">Erreur sémantique du module d’appel **de macro de type objet** .</span><span class="sxs-lookup"><span data-stu-id="6041f-129">**OBJECT-TYPE** macro invocation module semantic error.</span></span> <span data-ttu-id="6041f-130">Chaque objet séquence doit avoir exactement les mêmes objets qui sont mentionnés dans la définition de type de séquence comme ses enfants.</span><span class="sxs-lookup"><span data-stu-id="6041f-130">Every SEQUENCE object must have exactly the same objects that are mentioned in the SEQUENCE type definition as its children.</span></span> <span data-ttu-id="6041f-131">De même, chaque séquence d’objets doit avoir un seul enfant.</span><span class="sxs-lookup"><span data-stu-id="6041f-131">Similarly, every SEQUENCE OF object must have exactly one child.</span></span>

<span data-ttu-id="6041f-132">Cette erreur peut se produire dans SNMPv1 ou SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="6041f-132">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

## <a name="fatal-error-1077"></a><span data-ttu-id="6041f-133">Erreur irrécupérable 1077</span><span class="sxs-lookup"><span data-stu-id="6041f-133">Fatal Error 1077</span></span>

<dl> <dt>

<span data-ttu-id="6041f-134"><span id="_1077__Fatal_____fileName___line____The_syntax_of_table_OBJECT-TYPE__name__is_not_the_SEQUENCE_OF_the_syntax_of_the_child_OBJECT-TYPE__name__of_module__name__"></span><span id="_1077__fatal_____filename___line____the_syntax_of_table_object-type__name__is_not_the_sequence_of_the_syntax_of_the_child_object-type__name__of_module__name__"></span><span id="_1077__FATAL_____FILENAME___LINE____THE_SYNTAX_OF_TABLE_OBJECT-TYPE__NAME__IS_NOT_THE_SEQUENCE_OF_THE_SYNTAX_OF_THE_CHILD_OBJECT-TYPE__NAME__OF_MODULE__NAME__"></span>**<1077,> irrécupérable : " <fileName> : <ligne \#> : la syntaxe de la table Object-type <name> n’est pas la séquence de la syntaxe du type objet enfant <name> du module <name> "**</span><span class="sxs-lookup"><span data-stu-id="6041f-134"><span id="_1077__Fatal_____fileName___line____The_syntax_of_table_OBJECT-TYPE__name__is_not_the_SEQUENCE_OF_the_syntax_of_the_child_OBJECT-TYPE__name__of_module__name__"></span><span id="_1077__fatal_____filename___line____the_syntax_of_table_object-type__name__is_not_the_sequence_of_the_syntax_of_the_child_object-type__name__of_module__name__"></span><span id="_1077__FATAL_____FILENAME___LINE____THE_SYNTAX_OF_TABLE_OBJECT-TYPE__NAME__IS_NOT_THE_SEQUENCE_OF_THE_SYNTAX_OF_THE_CHILD_OBJECT-TYPE__NAME__OF_MODULE__NAME__"></span>**<1077, Fatal>: "<fileName>:<line\#>: The syntax of table OBJECT-TYPE <name> is not the SEQUENCE OF the syntax of the child OBJECT-TYPE <name> of module <name>"**</span></span>
</dt> <dd>

<span data-ttu-id="6041f-135">Erreur sémantique du module d’appel **de macro de type objet** .</span><span class="sxs-lookup"><span data-stu-id="6041f-135">**OBJECT-TYPE** macro invocation module semantic error.</span></span> <span data-ttu-id="6041f-136">La clause Syntax d’un objet table doit être la « séquence de » de la syntaxe de l’objet Row.</span><span class="sxs-lookup"><span data-stu-id="6041f-136">The syntax clause of a table object must be the "SEQUENCE OF" of the syntax of the row object.</span></span>

<span data-ttu-id="6041f-137">Cette erreur peut se produire dans SNMPv1 ou SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="6041f-137">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

## <a name="fatal-error-1079"></a><span data-ttu-id="6041f-138">Erreur irrécupérable 1079</span><span class="sxs-lookup"><span data-stu-id="6041f-138">Fatal Error 1079</span></span>

<dl> <dt>

<span data-ttu-id="6041f-139"><span id="_1079__Fatal___fileName___line____OBJECT-TYPE__name__is_an_extra_child_of_OBJECT-TYPE__name__of_module__name__"></span><span id="_1079__fatal___filename___line____object-type__name__is_an_extra_child_of_object-type__name__of_module__name__"></span><span id="_1079__FATAL___FILENAME___LINE____OBJECT-TYPE__NAME__IS_AN_EXTRA_CHILD_OF_OBJECT-TYPE__NAME__OF_MODULE__NAME__"></span>**<1079,> irrécupérable : "NomFichier> : <ligne \#> : Object-type <name> est un enfant supplémentaire de Object-type <name> de module <name> "**</span><span class="sxs-lookup"><span data-stu-id="6041f-139"><span id="_1079__Fatal___fileName___line____OBJECT-TYPE__name__is_an_extra_child_of_OBJECT-TYPE__name__of_module__name__"></span><span id="_1079__fatal___filename___line____object-type__name__is_an_extra_child_of_object-type__name__of_module__name__"></span><span id="_1079__FATAL___FILENAME___LINE____OBJECT-TYPE__NAME__IS_AN_EXTRA_CHILD_OF_OBJECT-TYPE__NAME__OF_MODULE__NAME__"></span>**<1079, Fatal>:"fileName>:<line\#>: OBJECT-TYPE <name> is an extra child of OBJECT-TYPE <name> of module <name>"**</span></span>
</dt> <dd>

<span data-ttu-id="6041f-140">Erreur sémantique du module d’appel **de macro de type objet** .</span><span class="sxs-lookup"><span data-stu-id="6041f-140">**OBJECT-TYPE** macro invocation module semantic error.</span></span> <span data-ttu-id="6041f-141">Chaque séquence d’objets doit avoir un seul enfant.</span><span class="sxs-lookup"><span data-stu-id="6041f-141">Every SEQUENCE OF object must have exactly one child.</span></span>

<span data-ttu-id="6041f-142">Cette erreur peut se produire dans SNMPv1 ou SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="6041f-142">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

## <a name="warning-1080"></a><span data-ttu-id="6041f-143">AVERTISSEMENT 1080</span><span class="sxs-lookup"><span data-stu-id="6041f-143">Warning 1080</span></span>

<dl> <dt>

<span data-ttu-id="6041f-144"><span id="_1080__Warning_____fileName__line____MIB_Module__moduleName___from_which_symbol__symbolName__is_imported__is_not_present_in_input_"></span><span id="_1080__warning_____filename__line____mib_module__modulename___from_which_symbol__symbolname__is_imported__is_not_present_in_input_"></span><span id="_1080__WARNING_____FILENAME__LINE____MIB_MODULE__MODULENAME___FROM_WHICH_SYMBOL__SYMBOLNAME__IS_IMPORTED__IS_NOT_PRESENT_IN_INPUT_"></span>**<1080, avertissement> : « <fileName><ligne \#> : le module MIB <moduleName> , à partir duquel le symbole <symbolName> est importé, n’est pas présent dans l’entrée »**</span><span class="sxs-lookup"><span data-stu-id="6041f-144"><span id="_1080__Warning_____fileName__line____MIB_Module__moduleName___from_which_symbol__symbolName__is_imported__is_not_present_in_input_"></span><span id="_1080__warning_____filename__line____mib_module__modulename___from_which_symbol__symbolname__is_imported__is_not_present_in_input_"></span><span id="_1080__WARNING_____FILENAME__LINE____MIB_MODULE__MODULENAME___FROM_WHICH_SYMBOL__SYMBOLNAME__IS_IMPORTED__IS_NOT_PRESENT_IN_INPUT_"></span>**<1080, Warning>: "<fileName><line\#>: MIB Module <moduleName>, from which symbol <symbolName> is imported, is not present in input"**</span></span>
</dt> <dd>

<span data-ttu-id="6041f-145">AVERTISSEMENT sémantique de module concernant les références croisées, spécifiques à ni à SNMPv1 ni à SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="6041f-145">Module semantic warning about cross-referencing, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="6041f-146">Si l’un des modules de la section Imports du module principal ou d’un module subsidiaire n’existe pas, mais que les symboles de ce module ne sont pas référencés, cet avertissement s’affiche.</span><span class="sxs-lookup"><span data-stu-id="6041f-146">If one of the modules in the IMPORTS section of the main module or a subsidiary module does not exist, but symbols from this module are not referenced, this warning appears.</span></span>

</dd> </dl>

 

 



