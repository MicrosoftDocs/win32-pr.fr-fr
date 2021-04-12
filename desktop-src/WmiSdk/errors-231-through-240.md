---
description: Décrit les erreurs du fournisseur SNMP WMI 231 à 240.
ms.assetid: edb3dabb-6a65-4285-97d3-f7025d3bb5da
ms.tgt_platform: multiple
title: Erreurs 231 à 240
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76d053cac57eec9d0055dec56bbfab8304ad3f97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210209"
---
# <a name="errors-231-through-240"></a><span data-ttu-id="a9743-103">Erreurs 231 à 240</span><span class="sxs-lookup"><span data-stu-id="a9743-103">Errors 231 through 240</span></span>

<span data-ttu-id="a9743-104">Décrit les erreurs du fournisseur SNMP WMI 231 à 240.</span><span class="sxs-lookup"><span data-stu-id="a9743-104">Describes WMI SNMP provider errors 231 through 240.</span></span>

[<span data-ttu-id="a9743-105">Erreur irrécupérable 232</span><span class="sxs-lookup"><span data-stu-id="a9743-105">Fatal Error 232</span></span>](#fatal-error-232)

[<span data-ttu-id="a9743-106">Erreur irrécupérable 233</span><span class="sxs-lookup"><span data-stu-id="a9743-106">Fatal Error 233</span></span>](#fatal-error-233)

[<span data-ttu-id="a9743-107">Erreur irrécupérable 234</span><span class="sxs-lookup"><span data-stu-id="a9743-107">Fatal Error 234</span></span>](#fatal-error-234)

[<span data-ttu-id="a9743-108">Erreur irrécupérable 236</span><span class="sxs-lookup"><span data-stu-id="a9743-108">Fatal Error 236</span></span>](#fatal-error-236)

## <a name="fatal-error-232"></a><span data-ttu-id="a9743-109">Erreur irrécupérable 232</span><span class="sxs-lookup"><span data-stu-id="a9743-109">Fatal Error 232</span></span>

<dl> <dt>

<span data-ttu-id="a9743-110"><span id="_232__Fatal____fileName___line___Invocation_of_SNMPv1_SMI_OBJECT-TYPE_disallowed_"></span><span id="_232__fatal____filename___line___invocation_of_snmpv1_smi_object-type_disallowed_"></span><span id="_232__FATAL____FILENAME___LINE___INVOCATION_OF_SNMPV1_SMI_OBJECT-TYPE_DISALLOWED_"></span>**<232,> fatale : " <fileName> : <\#> de ligne : appel de SNMPV1 SMI Object-type non autorisé"**</span><span class="sxs-lookup"><span data-stu-id="a9743-110"><span id="_232__Fatal____fileName___line___Invocation_of_SNMPv1_SMI_OBJECT-TYPE_disallowed_"></span><span id="_232__fatal____filename___line___invocation_of_snmpv1_smi_object-type_disallowed_"></span><span id="_232__FATAL____FILENAME___LINE___INVOCATION_OF_SNMPV1_SMI_OBJECT-TYPE_DISALLOWED_"></span>**<232, Fatal>:"<fileName>:<line\#>:Invocation of SNMPv1 SMI OBJECT-TYPE disallowed"**</span></span>
</dt> <dd>

<span data-ttu-id="a9743-111">Erreur de syntaxe du module.</span><span class="sxs-lookup"><span data-stu-id="a9743-111">Module syntax error.</span></span> <span data-ttu-id="a9743-112">Vous avez utilisé l’appel de **type objet** spécifique à SNMPv1 dans la MIB, mais vous avez spécifié le commutateur **/V2C** , qui requiert une conformité stricte à la syntaxe SNMPv2c.</span><span class="sxs-lookup"><span data-stu-id="a9743-112">You have used the SNMPv1-specific **OBJECT-TYPE** invocation in the MIB, but have specified the **/v2c** switch, which requires strict conformance to SNMPv2C syntax.</span></span>

</dd> </dl>

## <a name="fatal-error-233"></a><span data-ttu-id="a9743-113">Erreur irrécupérable 233</span><span class="sxs-lookup"><span data-stu-id="a9743-113">Fatal Error 233</span></span>

<dl> <dt>

<span data-ttu-id="a9743-114"><span id="_233__Fatal_____fileName___line____Invocation_of_SNMPv1_SMI_TRAP-TYPE_disallowed_"></span><span id="_233__fatal_____filename___line____invocation_of_snmpv1_smi_trap-type_disallowed_"></span><span id="_233__FATAL_____FILENAME___LINE____INVOCATION_OF_SNMPV1_SMI_TRAP-TYPE_DISALLOWED_"></span>**<233,> fatale : " <fileName> : <\#> de ligne : appel de l’interruption SMI SNMPV1-type non autorisé"**</span><span class="sxs-lookup"><span data-stu-id="a9743-114"><span id="_233__Fatal_____fileName___line____Invocation_of_SNMPv1_SMI_TRAP-TYPE_disallowed_"></span><span id="_233__fatal_____filename___line____invocation_of_snmpv1_smi_trap-type_disallowed_"></span><span id="_233__FATAL_____FILENAME___LINE____INVOCATION_OF_SNMPV1_SMI_TRAP-TYPE_DISALLOWED_"></span>**<233, Fatal>: "<fileName>:<line\#>: Invocation of SNMPv1 SMI TRAP-TYPE disallowed"**</span></span>
</dt> <dd>

<span data-ttu-id="a9743-115">Erreur de syntaxe du module.</span><span class="sxs-lookup"><span data-stu-id="a9743-115">Module syntax error.</span></span> <span data-ttu-id="a9743-116">Vous avez utilisé l’appel de **type d’interruption** spécifique à SNMPv1 dans la MIB, mais vous avez spécifié le commutateur **/V2C** , qui requiert une conformité stricte à la syntaxe SNMPv2c.</span><span class="sxs-lookup"><span data-stu-id="a9743-116">You have used the SNMPv1-specific **TRAP-TYPE** invocation in the MIB, but have specified the **/v2c** switch, which requires strict conformance to SNMPv2C syntax.</span></span>

</dd> </dl>

## <a name="fatal-error-234"></a><span data-ttu-id="a9743-117">Erreur irrécupérable 234</span><span class="sxs-lookup"><span data-stu-id="a9743-117">Fatal Error 234</span></span>

<dl> <dt>

<span data-ttu-id="a9743-118"><span id="_234__Fatal____fileName___line____MODULE-IDENTITY_invocation_is_allowed_only_immediately_after_the_IMPORTS_section_"></span><span id="_234__fatal____filename___line____module-identity_invocation_is_allowed_only_immediately_after_the_imports_section_"></span><span id="_234__FATAL____FILENAME___LINE____MODULE-IDENTITY_INVOCATION_IS_ALLOWED_ONLY_IMMEDIATELY_AFTER_THE_IMPORTS_SECTION_"></span>**<234,> irrécupérable : " <fileName> : <ligne \#> : l’appel de module-Identity est autorisé uniquement juste après la section Imports**</span><span class="sxs-lookup"><span data-stu-id="a9743-118"><span id="_234__Fatal____fileName___line____MODULE-IDENTITY_invocation_is_allowed_only_immediately_after_the_IMPORTS_section_"></span><span id="_234__fatal____filename___line____module-identity_invocation_is_allowed_only_immediately_after_the_imports_section_"></span><span id="_234__FATAL____FILENAME___LINE____MODULE-IDENTITY_INVOCATION_IS_ALLOWED_ONLY_IMMEDIATELY_AFTER_THE_IMPORTS_SECTION_"></span>**<234, Fatal>:"<fileName>:<line\#>: MODULE-IDENTITY invocation is allowed only immediately after the IMPORTS section"**</span></span>
</dt> <dd>

<span data-ttu-id="a9743-119">Erreur de syntaxe du module.</span><span class="sxs-lookup"><span data-stu-id="a9743-119">Module syntax error.</span></span> <span data-ttu-id="a9743-120">L’appel **de module-Identity** est mal placé.</span><span class="sxs-lookup"><span data-stu-id="a9743-120">The **MODULE-IDENTITY** invocation is misplaced.</span></span>

</dd> </dl>

## <a name="fatal-error-236"></a><span data-ttu-id="a9743-121">Erreur irrécupérable 236</span><span class="sxs-lookup"><span data-stu-id="a9743-121">Fatal Error 236</span></span>

<dl> <dt>

<span data-ttu-id="a9743-122"><span id="_236__Fatal_____fileName___line____Number_does_not_fit_into_the_32_bit_representation_used_by_the_compiler_"></span><span id="_236__fatal_____filename___line____number_does_not_fit_into_the_32_bit_representation_used_by_the_compiler_"></span><span id="_236__FATAL_____FILENAME___LINE____NUMBER_DOES_NOT_FIT_INTO_THE_32_BIT_REPRESENTATION_USED_BY_THE_COMPILER_"></span>**<236,> irrécupérable : " <fileName> : <ligne \#> : le nombre ne tient pas dans la représentation 32 bits utilisée par le compilateur"**</span><span class="sxs-lookup"><span data-stu-id="a9743-122"><span id="_236__Fatal_____fileName___line____Number_does_not_fit_into_the_32_bit_representation_used_by_the_compiler_"></span><span id="_236__fatal_____filename___line____number_does_not_fit_into_the_32_bit_representation_used_by_the_compiler_"></span><span id="_236__FATAL_____FILENAME___LINE____NUMBER_DOES_NOT_FIT_INTO_THE_32_BIT_REPRESENTATION_USED_BY_THE_COMPILER_"></span>**<236, Fatal>: "<fileName>:<line\#>: Number does not fit into the 32 bit representation used by the compiler"**</span></span>
</dt> <dd>

<span data-ttu-id="a9743-123">Erreur de syntaxe de module dans l’assignation de valeur.</span><span class="sxs-lookup"><span data-stu-id="a9743-123">Module syntax error in value assignment.</span></span> <span data-ttu-id="a9743-124">Il y a une erreur d’assignation de valeur MIB dans laquelle une valeur entière est tellement importante qu’elle nécessite plus de 32 bits pour la représenter.</span><span class="sxs-lookup"><span data-stu-id="a9743-124">There is a MIB value assignment error in which an integer value is so large that it requires more than 32 bits to represent it.</span></span>

</dd> </dl>

 

 



