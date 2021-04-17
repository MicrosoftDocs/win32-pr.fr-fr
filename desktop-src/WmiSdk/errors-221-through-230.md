---
description: Décrit les erreurs du fournisseur SNMP WMI 221 à 230.
ms.assetid: 50ca7a6b-2367-464b-98af-b65b0fab42c4
ms.tgt_platform: multiple
title: Erreurs 221 à 230
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c89dc0fc15d039bca5f1d8740996928b3586fc61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202290"
---
# <a name="errors-221-through-230"></a><span data-ttu-id="388df-103">Erreurs 221 à 230</span><span class="sxs-lookup"><span data-stu-id="388df-103">Errors 221 through 230</span></span>

<span data-ttu-id="388df-104">Décrit les erreurs du fournisseur SNMP WMI 221 à 230.</span><span class="sxs-lookup"><span data-stu-id="388df-104">Describes WMI SNMP provider errors 221 through 230.</span></span>

[<span data-ttu-id="388df-105">Erreur irrécupérable 222</span><span class="sxs-lookup"><span data-stu-id="388df-105">Fatal Error 222</span></span>](#fatal-error-222)

[<span data-ttu-id="388df-106">Erreur irrécupérable 223</span><span class="sxs-lookup"><span data-stu-id="388df-106">Fatal Error 223</span></span>](#fatal-error-223)

[<span data-ttu-id="388df-107">Erreur irrécupérable 224</span><span class="sxs-lookup"><span data-stu-id="388df-107">Fatal Error 224</span></span>](#fatal-error-224)

[<span data-ttu-id="388df-108">Erreur irrécupérable 225</span><span class="sxs-lookup"><span data-stu-id="388df-108">Fatal Error 225</span></span>](#fatal-error-225)

[<span data-ttu-id="388df-109">Erreur irrécupérable 226</span><span class="sxs-lookup"><span data-stu-id="388df-109">Fatal Error 226</span></span>](#fatal-error-226)

[<span data-ttu-id="388df-110">Erreur irrécupérable 227</span><span class="sxs-lookup"><span data-stu-id="388df-110">Fatal Error 227</span></span>](#fatal-error-227)

[<span data-ttu-id="388df-111">Erreur irrécupérable 228</span><span class="sxs-lookup"><span data-stu-id="388df-111">Fatal Error 228</span></span>](#fatal-error-228)

[<span data-ttu-id="388df-112">Erreur irrécupérable 229</span><span class="sxs-lookup"><span data-stu-id="388df-112">Fatal Error 229</span></span>](#fatal-error-229)

[<span data-ttu-id="388df-113">AVERTISSEMENT 230</span><span class="sxs-lookup"><span data-stu-id="388df-113">Warning 230</span></span>](#warning-230)

## <a name="fatal-error-222"></a><span data-ttu-id="388df-114">Erreur irrécupérable 222</span><span class="sxs-lookup"><span data-stu-id="388df-114">Fatal Error 222</span></span>

<dl> <dt>

<span data-ttu-id="388df-115"><span id="_222__Fatal_____fileName___line____NOTIFICATION-TYPE_not_allowed_in_SNMPv1_SMI_"></span><span id="_222__fatal_____filename___line____notification-type_not_allowed_in_snmpv1_smi_"></span><span id="_222__FATAL_____FILENAME___LINE____NOTIFICATION-TYPE_NOT_ALLOWED_IN_SNMPV1_SMI_"></span>**<222,> irrécupérable : " <fileName> : <\#> de ligne : notification-type non autorisé dans l’SMI SNMPv1"**</span><span class="sxs-lookup"><span data-stu-id="388df-115"><span id="_222__Fatal_____fileName___line____NOTIFICATION-TYPE_not_allowed_in_SNMPv1_SMI_"></span><span id="_222__fatal_____filename___line____notification-type_not_allowed_in_snmpv1_smi_"></span><span id="_222__FATAL_____FILENAME___LINE____NOTIFICATION-TYPE_NOT_ALLOWED_IN_SNMPV1_SMI_"></span>**<222, Fatal>: "<fileName>:<line\#>: NOTIFICATION-TYPE not allowed in SNMPv1 SMI"**</span></span>
</dt> <dd>

<span data-ttu-id="388df-116">Erreur de syntaxe du module.</span><span class="sxs-lookup"><span data-stu-id="388df-116">Module syntax error.</span></span> <span data-ttu-id="388df-117">Vous avez utilisé le TYPE de NOTIFICATION spécifique à SNMPv2C dans la MIB, mais vous avez spécifié le commutateur **/v1** , qui requiert une conformité stricte à la syntaxe SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="388df-117">You have used the SNMPv2C-specific NOTIFICATION-TYPE in the MIB, but have specified the **/v1** switch, which requires strict conformance to SNMPv1 syntax.</span></span>

</dd> </dl>

## <a name="fatal-error-223"></a><span data-ttu-id="388df-118">Erreur irrécupérable 223</span><span class="sxs-lookup"><span data-stu-id="388df-118">Fatal Error 223</span></span>

<dl> <dt>

<span data-ttu-id="388df-119"><span id="_223__Fatal_____fileName___line____MODULE-IDENTITY_not_allowed_in_SNMPv1_SMI_"></span><span id="_223__fatal_____filename___line____module-identity_not_allowed_in_snmpv1_smi_"></span><span id="_223__FATAL_____FILENAME___LINE____MODULE-IDENTITY_NOT_ALLOWED_IN_SNMPV1_SMI_"></span>**<223,> fatale : " <fileName> : <\#> de ligne : module-Identity non autorisé dans l’SMI SNMPv1"**</span><span class="sxs-lookup"><span data-stu-id="388df-119"><span id="_223__Fatal_____fileName___line____MODULE-IDENTITY_not_allowed_in_SNMPv1_SMI_"></span><span id="_223__fatal_____filename___line____module-identity_not_allowed_in_snmpv1_smi_"></span><span id="_223__FATAL_____FILENAME___LINE____MODULE-IDENTITY_NOT_ALLOWED_IN_SNMPV1_SMI_"></span>**<223, Fatal>: "<fileName>:<line\#>: MODULE-IDENTITY not allowed in SNMPv1 SMI"**</span></span>
</dt> <dd>

<span data-ttu-id="388df-120">Erreur de syntaxe du module.</span><span class="sxs-lookup"><span data-stu-id="388df-120">Module syntax error.</span></span> <span data-ttu-id="388df-121">Vous avez utilisé l’identité de MODULE spécifique à SNMPv2C dans la MIB, mais vous avez spécifié le commutateur **/v1** , qui requiert une conformité stricte à la syntaxe SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="388df-121">You have used the SNMPv2C-specific MODULE IDENTITY in the MIB, but have specified the **/v1** switch, which requires strict conformance to SNMPv1 syntax.</span></span>

</dd> </dl>

## <a name="fatal-error-224"></a><span data-ttu-id="388df-122">Erreur irrécupérable 224</span><span class="sxs-lookup"><span data-stu-id="388df-122">Fatal Error 224</span></span>

<dl> <dt>

<span data-ttu-id="388df-123"><span id="_224__Fatal_____fileName___line____OBJECT-IDENTITY_not_allowed_in_SNMPv1_SMI_"></span><span id="_224__fatal_____filename___line____object-identity_not_allowed_in_snmpv1_smi_"></span><span id="_224__FATAL_____FILENAME___LINE____OBJECT-IDENTITY_NOT_ALLOWED_IN_SNMPV1_SMI_"></span>**<224,> irrécupérable : " <fileName> : <\#> de ligne : objet-identité non autorisé dans l’SMI SNMPv1"**</span><span class="sxs-lookup"><span data-stu-id="388df-123"><span id="_224__Fatal_____fileName___line____OBJECT-IDENTITY_not_allowed_in_SNMPv1_SMI_"></span><span id="_224__fatal_____filename___line____object-identity_not_allowed_in_snmpv1_smi_"></span><span id="_224__FATAL_____FILENAME___LINE____OBJECT-IDENTITY_NOT_ALLOWED_IN_SNMPV1_SMI_"></span>**<224, Fatal>: "<fileName>:<line\#>: OBJECT-IDENTITY not allowed in SNMPv1 SMI"**</span></span>
</dt> <dd>

<span data-ttu-id="388df-124">Erreur de syntaxe du module.</span><span class="sxs-lookup"><span data-stu-id="388df-124">Module syntax error.</span></span> <span data-ttu-id="388df-125">Vous avez utilisé l’identité d’objet spécifique à SNMPv2C dans la MIB, mais vous avez spécifié le commutateur **/v1** , qui requiert une conformité stricte à la syntaxe SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="388df-125">You have used the SNMPv2C-specific OBJECT-IDENTITY in the MIB, but have specified the **/v1** switch, which requires strict conformance to SNMPv1 syntax.</span></span>

</dd> </dl>

## <a name="fatal-error-225"></a><span data-ttu-id="388df-126">Erreur irrécupérable 225</span><span class="sxs-lookup"><span data-stu-id="388df-126">Fatal Error 225</span></span>

<dl> <dt>

<span data-ttu-id="388df-127"><span id="_225__Fatal_____fileName___line____TEXTUAL-CONVENTION_not_allowed_in_SNMPv1_SMI_"></span><span id="_225__fatal_____filename___line____textual-convention_not_allowed_in_snmpv1_smi_"></span><span id="_225__FATAL_____FILENAME___LINE____TEXTUAL-CONVENTION_NOT_ALLOWED_IN_SNMPV1_SMI_"></span>**<225,> irrécupérable : " <fileName> : <ligne \#> : texte-Convention non autorisée dans SNMPv1 SMI"**</span><span class="sxs-lookup"><span data-stu-id="388df-127"><span id="_225__Fatal_____fileName___line____TEXTUAL-CONVENTION_not_allowed_in_SNMPv1_SMI_"></span><span id="_225__fatal_____filename___line____textual-convention_not_allowed_in_snmpv1_smi_"></span><span id="_225__FATAL_____FILENAME___LINE____TEXTUAL-CONVENTION_NOT_ALLOWED_IN_SNMPV1_SMI_"></span>**<225, Fatal>: "<fileName>:<line\#>: TEXTUAL-CONVENTION not allowed in SNMPv1 SMI"**</span></span>
</dt> <dd>

<span data-ttu-id="388df-128">Erreur de syntaxe du module.</span><span class="sxs-lookup"><span data-stu-id="388df-128">Module syntax error.</span></span> <span data-ttu-id="388df-129">Vous avez utilisé la CONVENTION de texte spécifique à SNMPv2C dans la MIB, mais vous avez spécifié le commutateur **/v1** , qui requiert une conformité stricte à la syntaxe SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="388df-129">You have used the SNMPv2C-specific TEXTUAL-CONVENTION in the MIB, but have specified the **/v1** switch, which requires strict conformance to SNMPv1 syntax.</span></span>

</dd> </dl>

## <a name="fatal-error-226"></a><span data-ttu-id="388df-130">Erreur irrécupérable 226</span><span class="sxs-lookup"><span data-stu-id="388df-130">Fatal Error 226</span></span>

<dl> <dt>

<span data-ttu-id="388df-131"><span id="_226__Fatal_____fileName___line____OBJECT-GROUP_not_allowed_in_SNMPv1_SMI_"></span><span id="_226__fatal_____filename___line____object-group_not_allowed_in_snmpv1_smi_"></span><span id="_226__FATAL_____FILENAME___LINE____OBJECT-GROUP_NOT_ALLOWED_IN_SNMPV1_SMI_"></span>**<226,> irrécupérable : " <fileName> : <\#> de ligne : objet-groupe non autorisé dans l’SMI SNMPv1"**</span><span class="sxs-lookup"><span data-stu-id="388df-131"><span id="_226__Fatal_____fileName___line____OBJECT-GROUP_not_allowed_in_SNMPv1_SMI_"></span><span id="_226__fatal_____filename___line____object-group_not_allowed_in_snmpv1_smi_"></span><span id="_226__FATAL_____FILENAME___LINE____OBJECT-GROUP_NOT_ALLOWED_IN_SNMPV1_SMI_"></span>**<226, Fatal>: "<fileName>:<line\#>: OBJECT-GROUP not allowed in SNMPv1 SMI"**</span></span>
</dt> <dd>

<span data-ttu-id="388df-132">Erreur de syntaxe du module.</span><span class="sxs-lookup"><span data-stu-id="388df-132">Module syntax error.</span></span> <span data-ttu-id="388df-133">Vous avez utilisé le groupe d’objets spécifique à SNMPv2C dans la MIB, mais vous avez spécifié le commutateur **/v1** , qui requiert une conformité stricte à la syntaxe SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="388df-133">You have used the SNMPv2C-specific OBJECT-GROUP in the MIB, but have specified the **/v1** switch, which requires strict conformance to SNMPv1 syntax.</span></span>

</dd> </dl>

## <a name="fatal-error-227"></a><span data-ttu-id="388df-134">Erreur irrécupérable 227</span><span class="sxs-lookup"><span data-stu-id="388df-134">Fatal Error 227</span></span>

<dl> <dt>

<span data-ttu-id="388df-135"><span id="_227__Fatal_____fileName___line____NOTIFICATION-GROUP_not_allowed_in_SNMPv1_SMI_"></span><span id="_227__fatal_____filename___line____notification-group_not_allowed_in_snmpv1_smi_"></span><span id="_227__FATAL_____FILENAME___LINE____NOTIFICATION-GROUP_NOT_ALLOWED_IN_SNMPV1_SMI_"></span>**<227,> irrécupérable : " <fileName> : <\#> de ligne : notification-groupe non autorisé dans l’SMI SNMPv1"**</span><span class="sxs-lookup"><span data-stu-id="388df-135"><span id="_227__Fatal_____fileName___line____NOTIFICATION-GROUP_not_allowed_in_SNMPv1_SMI_"></span><span id="_227__fatal_____filename___line____notification-group_not_allowed_in_snmpv1_smi_"></span><span id="_227__FATAL_____FILENAME___LINE____NOTIFICATION-GROUP_NOT_ALLOWED_IN_SNMPV1_SMI_"></span>**<227, Fatal>: "<fileName>:<line\#>: NOTIFICATION-GROUP not allowed in SNMPv1 SMI"**</span></span>
</dt> <dd>

<span data-ttu-id="388df-136">Erreur de syntaxe du module.</span><span class="sxs-lookup"><span data-stu-id="388df-136">Module syntax error.</span></span> <span data-ttu-id="388df-137">Vous avez utilisé le groupe de NOTIFICATION spécifique à SNMPv2C dans la MIB, mais vous avez spécifié le commutateur **/v1** , qui requiert une conformité stricte à la syntaxe SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="388df-137">You have used the SNMPv2C-specific NOTIFICATION-GROUP in the MIB, but have specified the **/v1** switch, which requires strict conformance to SNMPv1 syntax.</span></span>

</dd> </dl>

## <a name="fatal-error-228"></a><span data-ttu-id="388df-138">Erreur irrécupérable 228</span><span class="sxs-lookup"><span data-stu-id="388df-138">Fatal Error 228</span></span>

<dl> <dt>

<span data-ttu-id="388df-139"><span id="_228__Fatal_____fileName___line____MODULE-COMPLIANCE_not_allowed_in_SNMPv1_SMI_"></span><span id="_228__fatal_____filename___line____module-compliance_not_allowed_in_snmpv1_smi_"></span><span id="_228__FATAL_____FILENAME___LINE____MODULE-COMPLIANCE_NOT_ALLOWED_IN_SNMPV1_SMI_"></span>**<228,> irrécupérable : " <fileName> : <ligne \#> : module-Compliance non autorisé dans SNMPv1 SMI"**</span><span class="sxs-lookup"><span data-stu-id="388df-139"><span id="_228__Fatal_____fileName___line____MODULE-COMPLIANCE_not_allowed_in_SNMPv1_SMI_"></span><span id="_228__fatal_____filename___line____module-compliance_not_allowed_in_snmpv1_smi_"></span><span id="_228__FATAL_____FILENAME___LINE____MODULE-COMPLIANCE_NOT_ALLOWED_IN_SNMPV1_SMI_"></span>**<228, Fatal>: "<fileName>:<line\#>: MODULE-COMPLIANCE not allowed in SNMPv1 SMI"**</span></span>
</dt> <dd>

<span data-ttu-id="388df-140">Erreur de syntaxe du module.</span><span class="sxs-lookup"><span data-stu-id="388df-140">Module syntax error.</span></span> <span data-ttu-id="388df-141">Vous avez utilisé la conformité de MODULE spécifique à SNMPv2C dans la MIB, mais vous avez spécifié le commutateur **/v1** , qui requiert une conformité stricte à la syntaxe SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="388df-141">You have used the SNMPv2C-specific MODULE-COMPLIANCE in the MIB, but have specified the **/v1** switch, which requires strict conformance to SNMPv1 syntax.</span></span>

</dd> </dl>

## <a name="fatal-error-229"></a><span data-ttu-id="388df-142">Erreur irrécupérable 229</span><span class="sxs-lookup"><span data-stu-id="388df-142">Fatal Error 229</span></span>

<dl> <dt>

<span data-ttu-id="388df-143"><span id="_229__Fatal_____fileName___line____AGENT-CAPABILITIES_not_allowed_in_SNMPv1_SMI_"></span><span id="_229__fatal_____filename___line____agent-capabilities_not_allowed_in_snmpv1_smi_"></span><span id="_229__FATAL_____FILENAME___LINE____AGENT-CAPABILITIES_NOT_ALLOWED_IN_SNMPV1_SMI_"></span>**<229,> fatale : " <fileName> : <\#> de ligne : agent-fonctionnalités non autorisées dans SNMPv1 SMI"**</span><span class="sxs-lookup"><span data-stu-id="388df-143"><span id="_229__Fatal_____fileName___line____AGENT-CAPABILITIES_not_allowed_in_SNMPv1_SMI_"></span><span id="_229__fatal_____filename___line____agent-capabilities_not_allowed_in_snmpv1_smi_"></span><span id="_229__FATAL_____FILENAME___LINE____AGENT-CAPABILITIES_NOT_ALLOWED_IN_SNMPV1_SMI_"></span>**<229, Fatal>: "<fileName>:<line\#>: AGENT-CAPABILITIES not allowed in SNMPv1 SMI"**</span></span>
</dt> <dd>

<span data-ttu-id="388df-144">Erreur de syntaxe du module.</span><span class="sxs-lookup"><span data-stu-id="388df-144">Module syntax error.</span></span> <span data-ttu-id="388df-145">Vous avez utilisé les fonctionnalités de l’AGENT SNMPv2C spécifiques à la MIB, mais vous avez spécifié le commutateur **/v1** , qui requiert une conformité stricte à la syntaxe SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="388df-145">You have used the SNMPv2C-specific AGENT-CAPABILITIES in the MIB, but have specified the **/v1** switch, which requires strict conformance to SNMPv1 syntax.</span></span>

</dd> </dl>

## <a name="warning-230"></a><span data-ttu-id="388df-146">AVERTISSEMENT 230</span><span class="sxs-lookup"><span data-stu-id="388df-146">Warning 230</span></span>

<dl> <dt>

<span data-ttu-id="388df-147"><span id="_230__Warning_____fileName___line______the_wrong_token___used._Assuming________"></span><span id="_230__warning_____filename___line______the_wrong_token___used._assuming________"></span><span id="_230__WARNING_____FILENAME___LINE______THE_WRONG_TOKEN___USED._ASSUMING________"></span>**<230, avertissement> : " <fileName> : <> de ligne \# : ' <the wrong token> 'utilisé. En supposant que' :: = ' "**</span><span class="sxs-lookup"><span data-stu-id="388df-147"><span id="_230__Warning_____fileName___line______the_wrong_token___used._Assuming________"></span><span id="_230__warning_____filename___line______the_wrong_token___used._assuming________"></span><span id="_230__WARNING_____FILENAME___LINE______THE_WRONG_TOKEN___USED._ASSUMING________"></span>**<230, Warning>: "<fileName>:<line\#>: '<the wrong token>' used. Assuming '::=' "**</span></span>
</dt> <dd>

<span data-ttu-id="388df-148">Le jeton " : =", " ::" ou "=" a été utilisé à la place de " :: =".</span><span class="sxs-lookup"><span data-stu-id="388df-148">The token ":=", "::", or "=" has been used instead of "::=".</span></span>

</dd> </dl>

 

 



