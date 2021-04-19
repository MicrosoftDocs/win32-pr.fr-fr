---
description: Décrit les erreurs du fournisseur SNMP WMI 1051 à 1060.
ms.assetid: 789cc5b6-e3ef-4f66-8dec-6970d6df1fe9
ms.tgt_platform: multiple
title: Erreurs 1051 à 1060
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 170eddf3126a40f929aa36899259b731fa244941
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530141"
---
# <a name="errors-1051-through-1060"></a><span data-ttu-id="c32e7-103">Erreurs 1051 à 1060</span><span class="sxs-lookup"><span data-stu-id="c32e7-103">Errors 1051 through 1060</span></span>

<span data-ttu-id="c32e7-104">Décrit les erreurs du fournisseur SNMP WMI 1051 à 1060.</span><span class="sxs-lookup"><span data-stu-id="c32e7-104">Describes WMI SNMP provider errors 1051 through 1060.</span></span>

[<span data-ttu-id="c32e7-105">Erreur irrécupérable 1051</span><span class="sxs-lookup"><span data-stu-id="c32e7-105">Fatal Error 1051</span></span>](#fatal-error-1051)

[<span data-ttu-id="c32e7-106">Erreur irrécupérable 1054</span><span class="sxs-lookup"><span data-stu-id="c32e7-106">Fatal Error 1054</span></span>](#fatal-error-1054)

[<span data-ttu-id="c32e7-107">Erreur irrécupérable 1055</span><span class="sxs-lookup"><span data-stu-id="c32e7-107">Fatal Error 1055</span></span>](#fatal-error-1055)

## <a name="fatal-error-1051"></a><span data-ttu-id="c32e7-108">Erreur irrécupérable 1051</span><span class="sxs-lookup"><span data-stu-id="c32e7-108">Fatal Error 1051</span></span>

<dl> <dt>

<span data-ttu-id="c32e7-109"><span id="_1051__Fatal_____fileName___line____Ambiguous_reference_to_symbol__identifier__"></span><span id="_1051__fatal_____filename___line____ambiguous_reference_to_symbol__identifier__"></span><span id="_1051__FATAL_____FILENAME___LINE____AMBIGUOUS_REFERENCE_TO_SYMBOL__IDENTIFIER__"></span>**<1051,> irrécupérable : " <fileName> : <ligne \#> : référence ambiguë au symbole <identifier> "**</span><span class="sxs-lookup"><span data-stu-id="c32e7-109"><span id="_1051__Fatal_____fileName___line____Ambiguous_reference_to_symbol__identifier__"></span><span id="_1051__fatal_____filename___line____ambiguous_reference_to_symbol__identifier__"></span><span id="_1051__FATAL_____FILENAME___LINE____AMBIGUOUS_REFERENCE_TO_SYMBOL__IDENTIFIER__"></span>**<1051, Fatal>: "<fileName>:<line\#>: Ambiguous reference to symbol <identifier>"**</span></span>
</dt> <dd>

<span data-ttu-id="c32e7-110">Erreur de sémantique du module d’importation, propre à SNMPv1 et SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="c32e7-110">IMPORTS section module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="c32e7-111">Chaque descripteur d’objet correspondant à un objet dans une MIB Internet standard doit être unique.</span><span class="sxs-lookup"><span data-stu-id="c32e7-111">Each object descriptor corresponding to an object in an Internet Standard MIB must be unique.</span></span> <span data-ttu-id="c32e7-112">Étant donné que les MIB d’entreprise peuvent avoir des descripteurs d’objets communs, ces descripteurs importés à partir de deux modules doivent être utilisés sans ambiguïté dans le module MIB à l’aide de la notation « module. Descriptor ».</span><span class="sxs-lookup"><span data-stu-id="c32e7-112">Since enterprise MIBs can have common object descriptors, such descriptors imported from two modules must be used unambiguously in the MIB module by using the notation "module.descriptor."</span></span>

</dd> </dl>

## <a name="fatal-error-1054"></a><span data-ttu-id="c32e7-113">Erreur irrécupérable 1054</span><span class="sxs-lookup"><span data-stu-id="c32e7-113">Fatal Error 1054</span></span>

<dl> <dt>

<span data-ttu-id="c32e7-114"><span id="_1054__Fatal_____fileName___line_____identifier__in_INDEX_clause_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1054__fatal_____filename___line_____identifier__in_index_clause_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1054__FATAL_____FILENAME___LINE_____IDENTIFIER__IN_INDEX_CLAUSE_DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1054,> irrécupérable : " <fileName> : <ligne \#> : <identifier> dans la clause d’index n’est pas résolue en l’un des types autorisés"**</span><span class="sxs-lookup"><span data-stu-id="c32e7-114"><span id="_1054__Fatal_____fileName___line_____identifier__in_INDEX_clause_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1054__fatal_____filename___line_____identifier__in_index_clause_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1054__FATAL_____FILENAME___LINE_____IDENTIFIER__IN_INDEX_CLAUSE_DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1054, Fatal>: "<fileName>:<line\#>: <identifier> in INDEX clause does not resolve to one of the allowed types"**</span></span>
</dt> <dd>

<span data-ttu-id="c32e7-115">Erreur sémantique du module d’appel **de macro de type objet** .</span><span class="sxs-lookup"><span data-stu-id="c32e7-115">**OBJECT-TYPE** macro invocation module semantic error.</span></span> <span data-ttu-id="c32e7-116">Le type d’un objet dans la clause d’INDEX, ou tout type spécifié dans la clause d’INDEX, doit correspondre à un type scalaire, c’est-à-dire à une séquence ou non de type.</span><span class="sxs-lookup"><span data-stu-id="c32e7-116">The type of an object in the INDEX clause, or any type specified in the INDEX clause, must resolve to a scalar type, that is, a non-SEQUENCE or non-SEQUENCE OF type.</span></span> <span data-ttu-id="c32e7-117">Tout type spécifié dans la clause INDEX doit également être résolu en l’un de ces types.</span><span class="sxs-lookup"><span data-stu-id="c32e7-117">Any type specified in the INDEX clause must also resolve to one of these.</span></span>

<span data-ttu-id="c32e7-118">Cette erreur peut se produire dans SNMPv1 ou SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="c32e7-118">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

## <a name="fatal-error-1055"></a><span data-ttu-id="c32e7-119">Erreur irrécupérable 1055</span><span class="sxs-lookup"><span data-stu-id="c32e7-119">Fatal Error 1055</span></span>

<dl> <dt>

<span data-ttu-id="c32e7-120"><span id="_1055__Fatal____fileName___line____SYNTAX_of_INDEX_OBJECT-TYPE__identifier___does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1055__fatal____filename___line____syntax_of_index_object-type__identifier___does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1055__FATAL____FILENAME___LINE____SYNTAX_OF_INDEX_OBJECT-TYPE__IDENTIFIER___DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1055,> irrécupérable : " <fileName> : <line \#> : syntax of index-type-Object <identifier> , n’est pas résolu en l’un des types autorisés"**</span><span class="sxs-lookup"><span data-stu-id="c32e7-120"><span id="_1055__Fatal____fileName___line____SYNTAX_of_INDEX_OBJECT-TYPE__identifier___does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1055__fatal____filename___line____syntax_of_index_object-type__identifier___does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1055__FATAL____FILENAME___LINE____SYNTAX_OF_INDEX_OBJECT-TYPE__IDENTIFIER___DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1055, Fatal>:"<fileName>:<line\#>: SYNTAX of INDEX OBJECT-TYPE <identifier>, does not resolve to one of the allowed types"**</span></span>
</dt> <dd>

<span data-ttu-id="c32e7-121">Erreur sémantique du module d’appel **de macro de type objet** .</span><span class="sxs-lookup"><span data-stu-id="c32e7-121">**OBJECT-TYPE** macro invocation module semantic error.</span></span> <span data-ttu-id="c32e7-122">Le type d’un objet dans la clause d’INDEX, ou tout type spécifié dans la clause d’INDEX, doit correspondre à un type scalaire, c’est-à-dire à une séquence ou non de type.</span><span class="sxs-lookup"><span data-stu-id="c32e7-122">The type of an object in the INDEX clause, or any type specified in the INDEX clause, must resolve to a scalar type, that is, a non-SEQUENCE or non-SEQUENCE OF type.</span></span>

<span data-ttu-id="c32e7-123">Cette erreur peut se produire dans SNMPv1 ou SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="c32e7-123">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

 

 



