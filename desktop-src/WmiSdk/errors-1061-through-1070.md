---
description: Décrit les erreurs du fournisseur SNMP WMI 1061 à 1070.
ms.assetid: 1bbd6153-7241-4673-ae17-1caa92b2e6a6
ms.tgt_platform: multiple
title: Erreurs 1061 à 1070
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76a4bf0773ade1f62eb11f0c496aea340410c4a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520497"
---
# <a name="errors-1061-through-1070"></a><span data-ttu-id="dc8e3-103">Erreurs 1061 à 1070</span><span class="sxs-lookup"><span data-stu-id="dc8e3-103">Errors 1061 through 1070</span></span>

<span data-ttu-id="dc8e3-104">Décrit les erreurs du fournisseur SNMP WMI 1061 à 1070.</span><span class="sxs-lookup"><span data-stu-id="dc8e3-104">Describes WMI SNMP provider errors 1061 through 1070.</span></span>

[<span data-ttu-id="dc8e3-105">Erreur irrécupérable 1063</span><span class="sxs-lookup"><span data-stu-id="dc8e3-105">Fatal Error 1063</span></span>](#fatal-error-1063)

[<span data-ttu-id="dc8e3-106">Erreur irrécupérable 1064</span><span class="sxs-lookup"><span data-stu-id="dc8e3-106">Fatal Error 1064</span></span>](#fatal-error-1064)

[<span data-ttu-id="dc8e3-107">Erreur irrécupérable 1070</span><span class="sxs-lookup"><span data-stu-id="dc8e3-107">Fatal Error 1070</span></span>](#fatal-error-1070)

## <a name="fatal-error-1063"></a><span data-ttu-id="dc8e3-108">Erreur irrécupérable 1063</span><span class="sxs-lookup"><span data-stu-id="dc8e3-108">Fatal Error 1063</span></span>

<dl> <dt>

<span data-ttu-id="dc8e3-109"><span id="_1063__Fatal_____fileName__line____Upper_bound_of_SIZE_specification_is_less_than_the_lower_bound_"></span><span id="_1063__fatal_____filename__line____upper_bound_of_size_specification_is_less_than_the_lower_bound_"></span><span id="_1063__FATAL_____FILENAME__LINE____UPPER_BOUND_OF_SIZE_SPECIFICATION_IS_LESS_THAN_THE_LOWER_BOUND_"></span>**<1063,> irrécupérable : " <fileName><ligne \#> : la limite supérieure de la spécification de taille est inférieure à la limite inférieure**</span><span class="sxs-lookup"><span data-stu-id="dc8e3-109"><span id="_1063__Fatal_____fileName__line____Upper_bound_of_SIZE_specification_is_less_than_the_lower_bound_"></span><span id="_1063__fatal_____filename__line____upper_bound_of_size_specification_is_less_than_the_lower_bound_"></span><span id="_1063__FATAL_____FILENAME__LINE____UPPER_BOUND_OF_SIZE_SPECIFICATION_IS_LESS_THAN_THE_LOWER_BOUND_"></span>**<1063, Fatal>: "<fileName><line\#>: Upper bound of SIZE specification is less than the lower bound"**</span></span>
</dt> <dd>

<span data-ttu-id="dc8e3-110">Erreur de sémantique de module dans la spécification de taille, propre à ni SNMPv1 ni SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="dc8e3-110">Module semantic error in SIZE specification, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="dc8e3-111">Le symbole utilisé dans une spécification de taille doit être converti en OCTET STRING ou opaque.</span><span class="sxs-lookup"><span data-stu-id="dc8e3-111">The symbol used in a SIZE specification must resolve to OCTET STRING or Opaque.</span></span> <span data-ttu-id="dc8e3-112">La limite inférieure d’une plage ou d’une spécification de taille ne doit pas être supérieure à la limite supérieure.</span><span class="sxs-lookup"><span data-stu-id="dc8e3-112">The lower bound of a range or SIZE specification must be no greater than the upper bound.</span></span>

</dd> </dl>

## <a name="fatal-error-1064"></a><span data-ttu-id="dc8e3-113">Erreur irrécupérable 1064</span><span class="sxs-lookup"><span data-stu-id="dc8e3-113">Fatal Error 1064</span></span>

<dl> <dt>

<span data-ttu-id="dc8e3-114"><span id="_1064__Fatal_____fileName___line____SEQUENCE_item__identifier__does_not_resolve_to_an_OBJECT-TYPE_"></span><span id="_1064__fatal_____filename___line____sequence_item__identifier__does_not_resolve_to_an_object-type_"></span><span id="_1064__FATAL_____FILENAME___LINE____SEQUENCE_ITEM__IDENTIFIER__DOES_NOT_RESOLVE_TO_AN_OBJECT-TYPE_"></span>**<1064,> fatale : " <fileName> : <\#> de ligne : l’élément de séquence <identifier> n’est pas résolu en type-objet"**</span><span class="sxs-lookup"><span data-stu-id="dc8e3-114"><span id="_1064__Fatal_____fileName___line____SEQUENCE_item__identifier__does_not_resolve_to_an_OBJECT-TYPE_"></span><span id="_1064__fatal_____filename___line____sequence_item__identifier__does_not_resolve_to_an_object-type_"></span><span id="_1064__FATAL_____FILENAME___LINE____SEQUENCE_ITEM__IDENTIFIER__DOES_NOT_RESOLVE_TO_AN_OBJECT-TYPE_"></span>**<1064, Fatal>: "<fileName>:<line\#>: SEQUENCE item <identifier> does not resolve to an OBJECT-TYPE"**</span></span>
</dt> <dd>

<span data-ttu-id="dc8e3-115">Erreur de sémantique du module d’assignation de type, propre à SNMPv1 et SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="dc8e3-115">Type assignment module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="dc8e3-116">Tous les éléments individuels d’une déclaration de séquence doivent être résolus en un TYPE d’objet.</span><span class="sxs-lookup"><span data-stu-id="dc8e3-116">All of the individual elements of a SEQUENCE declaration must resolve to an OBJECT-TYPE.</span></span>

</dd> </dl>

## <a name="fatal-error-1070"></a><span data-ttu-id="dc8e3-117">Erreur irrécupérable 1070</span><span class="sxs-lookup"><span data-stu-id="dc8e3-117">Fatal Error 1070</span></span>

<dl> <dt>

<span data-ttu-id="dc8e3-118"><span id="_1070__Fatal_____fileName__line____MIB_Module__moduleName___from_which_symbol__symbolName__is_imported__is_not_present_in_input_"></span><span id="_1070__fatal_____filename__line____mib_module__modulename___from_which_symbol__symbolname__is_imported__is_not_present_in_input_"></span><span id="_1070__FATAL_____FILENAME__LINE____MIB_MODULE__MODULENAME___FROM_WHICH_SYMBOL__SYMBOLNAME__IS_IMPORTED__IS_NOT_PRESENT_IN_INPUT_"></span>**<1070,> irrécupérable : « <fileName><ligne \#> : le module MIB <moduleName> , à partir duquel le symbole <symbolName> est importé, n’est pas présent dans l’entrée »**</span><span class="sxs-lookup"><span data-stu-id="dc8e3-118"><span id="_1070__Fatal_____fileName__line____MIB_Module__moduleName___from_which_symbol__symbolName__is_imported__is_not_present_in_input_"></span><span id="_1070__fatal_____filename__line____mib_module__modulename___from_which_symbol__symbolname__is_imported__is_not_present_in_input_"></span><span id="_1070__FATAL_____FILENAME__LINE____MIB_MODULE__MODULENAME___FROM_WHICH_SYMBOL__SYMBOLNAME__IS_IMPORTED__IS_NOT_PRESENT_IN_INPUT_"></span>**<1070, Fatal>: "<fileName><line\#>: MIB Module <moduleName>, from which symbol <symbolName> is imported, is not present in input"**</span></span>
</dt> <dd>

<span data-ttu-id="dc8e3-119">Erreur de sémantique de module dans le référence croisée, spécifique à, ou à SNMPv1 et à SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="dc8e3-119">Module semantic error in cross-referencing, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="dc8e3-120">Si l’un des modules de la section Imports du module principal ou d’un module subsidiaire n’existe pas et qu’un ou plusieurs symboles de ce module sont réellement référencés, cette erreur irrécupérable se produit.</span><span class="sxs-lookup"><span data-stu-id="dc8e3-120">If one of the modules in the IMPORTS section of the main module or a subsidiary module does not exist and one or more symbols from this module are actually referenced, this fatal error occurs.</span></span>

</dd> </dl>

 

 



