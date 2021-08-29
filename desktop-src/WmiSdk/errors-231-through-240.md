---
description: Décrit les erreurs du fournisseur SNMP WMI 231 à 240.
ms.assetid: edb3dabb-6a65-4285-97d3-f7025d3bb5da
ms.tgt_platform: multiple
title: Erreurs 231 à 240
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5bf38ca62f543122ee937d7759ebd5655470a54
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880875"
---
# <a name="errors-231-through-240"></a>Erreurs 231 à 240

Décrit les erreurs du fournisseur SNMP WMI 231 à 240.

[Erreur irrécupérable 232](#fatal-error-232)

[Erreur irrécupérable 233](#fatal-error-233)

[Erreur irrécupérable 234](#fatal-error-234)

[Erreur irrécupérable 236](#fatal-error-236)

## <a name="fatal-error-232"></a>Erreur irrécupérable 232

<dl> <dt>

<span id="_232__Fatal____fileName___line___Invocation_of_SNMPv1_SMI_OBJECT-TYPE_disallowed_"></span><span id="_232__fatal____filename___line___invocation_of_snmpv1_smi_object-type_disallowed_"></span><span id="_232__FATAL____FILENAME___LINE___INVOCATION_OF_SNMPV1_SMI_OBJECT-TYPE_DISALLOWED_"></span>**<232,> fatale : " &lt; filename &gt; : <Line \#> : invocation of SNMPv1 SMI Object-type unallowed"**
</dt> <dd>

Erreur de syntaxe du module. Vous avez utilisé l’appel de **type objet** spécifique à SNMPv1 dans la MIB, mais vous avez spécifié le commutateur **/V2C** , qui requiert une conformité stricte à la syntaxe SNMPv2c.

</dd> </dl>

## <a name="fatal-error-233"></a>Erreur irrécupérable 233

<dl> <dt>

<span id="_233__Fatal_____fileName___line____Invocation_of_SNMPv1_SMI_TRAP-TYPE_disallowed_"></span><span id="_233__fatal_____filename___line____invocation_of_snmpv1_smi_trap-type_disallowed_"></span><span id="_233__FATAL_____FILENAME___LINE____INVOCATION_OF_SNMPV1_SMI_TRAP-TYPE_DISALLOWED_"></span>**<233,> irrécupérable : " &lt; NomFichier &gt; : <ligne \#> : appel de l’interruption SMI SNMPv1-type non autorisé"**
</dt> <dd>

Erreur de syntaxe du module. Vous avez utilisé l’appel de **type d’interruption** spécifique à SNMPv1 dans la MIB, mais vous avez spécifié le commutateur **/V2C** , qui requiert une conformité stricte à la syntaxe SNMPv2c.

</dd> </dl>

## <a name="fatal-error-234"></a>Erreur irrécupérable 234

<dl> <dt>

<span id="_234__Fatal____fileName___line____MODULE-IDENTITY_invocation_is_allowed_only_immediately_after_the_IMPORTS_section_"></span><span id="_234__fatal____filename___line____module-identity_invocation_is_allowed_only_immediately_after_the_imports_section_"></span><span id="_234__FATAL____FILENAME___LINE____MODULE-IDENTITY_INVOCATION_IS_ALLOWED_ONLY_IMMEDIATELY_AFTER_THE_IMPORTS_SECTION_"></span>**<234,> irrécupérable : " &lt; filename &gt; : <Line \#> : module-l’appel d’identité n’est autorisé qu’immédiatement après la section Imports»**
</dt> <dd>

Erreur de syntaxe du module. L’appel **de module-Identity** est mal placé.

</dd> </dl>

## <a name="fatal-error-236"></a>Erreur irrécupérable 236

<dl> <dt>

<span id="_236__Fatal_____fileName___line____Number_does_not_fit_into_the_32_bit_representation_used_by_the_compiler_"></span><span id="_236__fatal_____filename___line____number_does_not_fit_into_the_32_bit_representation_used_by_the_compiler_"></span><span id="_236__FATAL_____FILENAME___LINE____NUMBER_DOES_NOT_FIT_INTO_THE_32_BIT_REPRESENTATION_USED_BY_THE_COMPILER_"></span>**<236,> irrécupérable : " &lt; NomFichier &gt; : <ligne \#> : le nombre ne tient pas dans la représentation 32 bits utilisée par le compilateur»**
</dt> <dd>

Erreur de syntaxe de module dans l’assignation de valeur. Il y a une erreur d’assignation de valeur MIB dans laquelle une valeur entière est tellement importante qu’elle nécessite plus de 32 bits pour la représenter.

</dd> </dl>

 

 



