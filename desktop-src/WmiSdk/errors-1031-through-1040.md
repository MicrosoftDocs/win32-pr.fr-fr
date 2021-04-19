---
description: Décrit les erreurs du fournisseur SNMP WMI 1031 à 1040.
ms.assetid: 5fc519ac-ae05-4daf-a681-7935190f1d46
ms.tgt_platform: multiple
title: Erreurs 1031 à 1040
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d34079c2cbdb8e50aef04e8c364ba99abee760fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530142"
---
# <a name="errors-1031-through-1040"></a><span data-ttu-id="3e6b7-103">Erreurs 1031 à 1040</span><span class="sxs-lookup"><span data-stu-id="3e6b7-103">Errors 1031 through 1040</span></span>

<span data-ttu-id="3e6b7-104">Décrit les erreurs du fournisseur SNMP WMI 1031 à 1040.</span><span class="sxs-lookup"><span data-stu-id="3e6b7-104">Describes WMI SNMP provider errors 1031 through 1040.</span></span>

[<span data-ttu-id="3e6b7-105">AVERTISSEMENT 1031</span><span class="sxs-lookup"><span data-stu-id="3e6b7-105">Warning 1031</span></span>](#warning-1031)

[<span data-ttu-id="3e6b7-106">Erreur irrécupérable 1032</span><span class="sxs-lookup"><span data-stu-id="3e6b7-106">Fatal Error 1032</span></span>](#fatal-error-1032)

[<span data-ttu-id="3e6b7-107">Erreur irrécupérable 1033</span><span class="sxs-lookup"><span data-stu-id="3e6b7-107">Fatal Error 1033</span></span>](#fatal-error-1033)

[<span data-ttu-id="3e6b7-108">AVERTISSEMENT 1034</span><span class="sxs-lookup"><span data-stu-id="3e6b7-108">Warning 1034</span></span>](#warning-1034)

[<span data-ttu-id="3e6b7-109">AVERTISSEMENT 1036</span><span class="sxs-lookup"><span data-stu-id="3e6b7-109">Warning 1036</span></span>](#warning-1036)

[<span data-ttu-id="3e6b7-110">Erreur irrécupérable 1037</span><span class="sxs-lookup"><span data-stu-id="3e6b7-110">Fatal Error 1037</span></span>](#fatal-error-1037)

[<span data-ttu-id="3e6b7-111">Erreur irrécupérable 1038</span><span class="sxs-lookup"><span data-stu-id="3e6b7-111">Fatal Error 1038</span></span>](#fatal-error-1038)

[<span data-ttu-id="3e6b7-112">Erreur irrécupérable 1039</span><span class="sxs-lookup"><span data-stu-id="3e6b7-112">Fatal Error 1039</span></span>](#fatal-error-1039)

[<span data-ttu-id="3e6b7-113">Erreur irrécupérable 1040</span><span class="sxs-lookup"><span data-stu-id="3e6b7-113">Fatal Error 1040</span></span>](#fatal-error-1040)

## <a name="warning-1031"></a><span data-ttu-id="3e6b7-114">AVERTISSEMENT 1031</span><span class="sxs-lookup"><span data-stu-id="3e6b7-114">Warning 1031</span></span>

<dl> <dt>

<span data-ttu-id="3e6b7-115"><span id="_1031__Warning_____fileName___line____Standard_symbol__identifier__should_be_imported_from_module__identifier_._Assuming_the_standard_definition._"></span><span id="_1031__warning_____filename___line____standard_symbol__identifier__should_be_imported_from_module__identifier_._assuming_the_standard_definition._"></span><span id="_1031__WARNING_____FILENAME___LINE____STANDARD_SYMBOL__IDENTIFIER__SHOULD_BE_IMPORTED_FROM_MODULE__IDENTIFIER_._ASSUMING_THE_STANDARD_DEFINITION._"></span>**<1031, avertissement> : " <fileName> : <\#> de ligne : le symbole standard <identifier> doit être importé à partir du module <identifier> . En supposant la définition standard.»**</span><span class="sxs-lookup"><span data-stu-id="3e6b7-115"><span id="_1031__Warning_____fileName___line____Standard_symbol__identifier__should_be_imported_from_module__identifier_._Assuming_the_standard_definition._"></span><span id="_1031__warning_____filename___line____standard_symbol__identifier__should_be_imported_from_module__identifier_._assuming_the_standard_definition._"></span><span id="_1031__WARNING_____FILENAME___LINE____STANDARD_SYMBOL__IDENTIFIER__SHOULD_BE_IMPORTED_FROM_MODULE__IDENTIFIER_._ASSUMING_THE_STANDARD_DEFINITION._"></span>**<1031, Warning>: "<fileName>:<line\#>: Standard symbol <identifier> should be imported from module <identifier>. Assuming the standard definition."**</span></span>
</dt> <dd>

<span data-ttu-id="3e6b7-116">IMPORTE la section Avertissement sémantique de module, spécifique à ni SNMPv1 ni SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="3e6b7-116">IMPORTS section module semantic warning, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="3e6b7-117">Si un identificateur SNMP connu du compilateur se trouve dans la section Imports, le module à partir duquel il est importé doit être l’un des modules standard.</span><span class="sxs-lookup"><span data-stu-id="3e6b7-117">If an SNMP identifier known to the compiler is in the IMPORTS section, then the module from which it is imported must be one of the standard modules.</span></span>

<span data-ttu-id="3e6b7-118">Certaines importations couramment utilisées sont des « connaissances supposées » dans la partie du compilateur.</span><span class="sxs-lookup"><span data-stu-id="3e6b7-118">Certain commonly used IMPORTS are "assumed knowledge" on the part of the compiler.</span></span> <span data-ttu-id="3e6b7-119">Il n’est pas nécessaire que le compilateur requière l’accès à d’autres modules d’informations pour les résoudre.</span><span class="sxs-lookup"><span data-stu-id="3e6b7-119">It is unnecessary for the compiler to require access to other information modules to resolve these.</span></span>

<span data-ttu-id="3e6b7-120">Les importations de SNMPv1 et SNMPv2C intégrées sont décrites dans les tableaux suivants.</span><span class="sxs-lookup"><span data-stu-id="3e6b7-120">The built-in SNMPv1 and SNMPv2C IMPORTS are described in the following tables.</span></span>

</dd> </dl>

<span data-ttu-id="3e6b7-121">**IMPORTATIONS SNMPv1 intégrées**</span><span class="sxs-lookup"><span data-stu-id="3e6b7-121">**Built-in SNMPv1 IMPORTS**</span></span>



| <span data-ttu-id="3e6b7-122">Classe d’importation</span><span class="sxs-lookup"><span data-stu-id="3e6b7-122">Import Class</span></span> | <span data-ttu-id="3e6b7-123">Module</span><span class="sxs-lookup"><span data-stu-id="3e6b7-123">Module</span></span>      | <span data-ttu-id="3e6b7-124">Instances</span><span class="sxs-lookup"><span data-stu-id="3e6b7-124">Instances</span></span>                                                           |
|--------------|-------------|---------------------------------------------------------------------|
| <span data-ttu-id="3e6b7-125">Valeur ASN. 1</span><span class="sxs-lookup"><span data-stu-id="3e6b7-125">ASN.1 Value</span></span>  | <span data-ttu-id="3e6b7-126">RFC1155-SMI</span><span class="sxs-lookup"><span data-stu-id="3e6b7-126">RFC1155-SMI</span></span> | <span data-ttu-id="3e6b7-127">Internet, annuaire, gestion, expérimental, privé, entreprises</span><span class="sxs-lookup"><span data-stu-id="3e6b7-127">Internet, directory, management, experimental, private, enterprises</span></span> |
|              | <span data-ttu-id="3e6b7-128">RFC1213-MIB</span><span class="sxs-lookup"><span data-stu-id="3e6b7-128">RFC1213-MIB</span></span> | <span data-ttu-id="3e6b7-129">MIB-II et IP, interfaces, transmission</span><span class="sxs-lookup"><span data-stu-id="3e6b7-129">MIB-II and IP, interfaces, transmission</span></span>                             |
| <span data-ttu-id="3e6b7-130">Type ASN. 1</span><span class="sxs-lookup"><span data-stu-id="3e6b7-130">ASN.1 Type</span></span>   | <span data-ttu-id="3e6b7-131">RFC1155-SMI</span><span class="sxs-lookup"><span data-stu-id="3e6b7-131">RFC1155-SMI</span></span> | <span data-ttu-id="3e6b7-132">NetworkAddress, IpAddress, compteur, jauge, graduations, opaque</span><span class="sxs-lookup"><span data-stu-id="3e6b7-132">NetworkAddress, IpAddress, Counter, Gauge, TimeTicks, Opaque</span></span>        |
|              | <span data-ttu-id="3e6b7-133">RFC1213-MIB</span><span class="sxs-lookup"><span data-stu-id="3e6b7-133">RFC1213-MIB</span></span> | <span data-ttu-id="3e6b7-134">DisplayString, PhysAddress</span><span class="sxs-lookup"><span data-stu-id="3e6b7-134">DisplayString, PhysAddress</span></span>                                          |
| <span data-ttu-id="3e6b7-135">Macro ASN. 1</span><span class="sxs-lookup"><span data-stu-id="3e6b7-135">ASN.1 Macro</span></span>  | <span data-ttu-id="3e6b7-136">RFC 1212</span><span class="sxs-lookup"><span data-stu-id="3e6b7-136">RFC-1212</span></span>    | <span data-ttu-id="3e6b7-137">TYPE D’OBJET</span><span class="sxs-lookup"><span data-stu-id="3e6b7-137">OBJECT-TYPE</span></span>                                                         |
|              | <span data-ttu-id="3e6b7-138">RFC 1215</span><span class="sxs-lookup"><span data-stu-id="3e6b7-138">RFC-1215</span></span>    | <span data-ttu-id="3e6b7-139">TYPE D’INTERRUPTION</span><span class="sxs-lookup"><span data-stu-id="3e6b7-139">TRAP-TYPE</span></span>                                                           |



 

<span data-ttu-id="3e6b7-140">**IMPORTATIONS SNMPv2C intégrées**</span><span class="sxs-lookup"><span data-stu-id="3e6b7-140">**Built-in SNMPv2C IMPORTS**</span></span>



| <span data-ttu-id="3e6b7-141">Classe d’importation</span><span class="sxs-lookup"><span data-stu-id="3e6b7-141">Import Class</span></span>       | <span data-ttu-id="3e6b7-142">Module</span><span class="sxs-lookup"><span data-stu-id="3e6b7-142">Module</span></span>      | <span data-ttu-id="3e6b7-143">Instances</span><span class="sxs-lookup"><span data-stu-id="3e6b7-143">Instances</span></span>                                                                                                                                                                                                      |
|--------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e6b7-144">Valeur ASN. 1</span><span class="sxs-lookup"><span data-stu-id="3e6b7-144">ASN.1 Value</span></span>        | <span data-ttu-id="3e6b7-145">SNMPv2-SMI</span><span class="sxs-lookup"><span data-stu-id="3e6b7-145">SNMPv2-SMI</span></span>  | <span data-ttu-id="3e6b7-146">org, DOD, Internet, annuaire, gestion, MIB-2, transmission, expérimental, privé, Enterprises, Security, SNMPv2, snmpDomains, snmpProxys, snmpModules</span><span class="sxs-lookup"><span data-stu-id="3e6b7-146">org, dod, Internet, directory, mgmt, mib-2, transmission, experimental, private, enterprises, security, snmpv2, snmpDomains, snmpProxys, snmpModules</span></span>                                                           |
|                    | <span data-ttu-id="3e6b7-147">SNMPv2-TM</span><span class="sxs-lookup"><span data-stu-id="3e6b7-147">SNMPv2-TM</span></span>   | <span data-ttu-id="3e6b7-148">rfc1157Proxy</span><span class="sxs-lookup"><span data-stu-id="3e6b7-148">rfc1157Proxy</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="3e6b7-149">Identité d'un objet</span><span class="sxs-lookup"><span data-stu-id="3e6b7-149">Object Identity</span></span>    | <span data-ttu-id="3e6b7-150">SNMPv2-SMI</span><span class="sxs-lookup"><span data-stu-id="3e6b7-150">SNMPv2-SMI</span></span>  | <span data-ttu-id="3e6b7-151">zeroDotZero</span><span class="sxs-lookup"><span data-stu-id="3e6b7-151">zeroDotZero</span></span>                                                                                                                                                                                                    |
|                    | <span data-ttu-id="3e6b7-152">SNMPv2-TM</span><span class="sxs-lookup"><span data-stu-id="3e6b7-152">SNMPv2-TM</span></span>   | <span data-ttu-id="3e6b7-153">snmpUDPDomain, snmpCLNSDomain, smnpCONSDomain, snmpDDPDomain, snmpIPXDomain, rfc1157Domain</span><span class="sxs-lookup"><span data-stu-id="3e6b7-153">snmpUDPDomain, snmpCLNSDomain, smnpCONSDomain, snmpDDPDomain, snmpIPXDomain, rfc1157Domain</span></span>                                                                                                                     |
| <span data-ttu-id="3e6b7-154">Type ASN. 1</span><span class="sxs-lookup"><span data-stu-id="3e6b7-154">ASN.1 Type</span></span>         | <span data-ttu-id="3e6b7-155">SNMPv2-SMI</span><span class="sxs-lookup"><span data-stu-id="3e6b7-155">SNMPv2-SMI</span></span>  | <span data-ttu-id="3e6b7-156">Integer32, IpAddress, Counter32, graduations, opaque, Counter64, Unsigned32, gauge32</span><span class="sxs-lookup"><span data-stu-id="3e6b7-156">Integer32, IpAddress, Counter32, TimeTicks, Opaque, Counter64, Unsigned32, Gauge32</span></span>                                                                                                                             |
| <span data-ttu-id="3e6b7-157">Macro ASN. 1</span><span class="sxs-lookup"><span data-stu-id="3e6b7-157">ASN.1 Macro</span></span>        | <span data-ttu-id="3e6b7-158">SNMPv2-SMI</span><span class="sxs-lookup"><span data-stu-id="3e6b7-158">SNMPv2-SMI</span></span>  | <span data-ttu-id="3e6b7-159">MODULE-IDENTITY, OBJECT-IDENTITY, OBJECT-TYPE, NOTIFICATION-TYPE</span><span class="sxs-lookup"><span data-stu-id="3e6b7-159">MODULE-IDENTITY, OBJECT-IDENTITY, OBJECT-TYPE, NOTIFICATION-TYPE</span></span>                                                                                                                                               |
|                    | <span data-ttu-id="3e6b7-160">SNMPv2-CONF</span><span class="sxs-lookup"><span data-stu-id="3e6b7-160">SNMPv2-CONF</span></span> | <span data-ttu-id="3e6b7-161">GROUPE D’OBJETS, NOTIFICATION-GROUPE, CONFORMITÉ DE MODULE, AGENT-FONCTIONNALITÉS</span><span class="sxs-lookup"><span data-stu-id="3e6b7-161">OBJECT-GROUP, NOTIFICATION-GROUP, MODULE-COMPLIANCE, AGENT-CAPABILITIES</span></span>                                                                                                                                        |
|                    | <span data-ttu-id="3e6b7-162">SNMPv2-TC</span><span class="sxs-lookup"><span data-stu-id="3e6b7-162">SNMPv2-TC</span></span>   | <span data-ttu-id="3e6b7-163">CONVENTION TEXTUELLE</span><span class="sxs-lookup"><span data-stu-id="3e6b7-163">TEXTUAL-CONVENTION</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="3e6b7-164">Convention textuelle</span><span class="sxs-lookup"><span data-stu-id="3e6b7-164">Textual Convention</span></span> | <span data-ttu-id="3e6b7-165">SNMPv2-TC</span><span class="sxs-lookup"><span data-stu-id="3e6b7-165">SNMPv2-TC</span></span>   | <span data-ttu-id="3e6b7-166">DisplayString, PhysAddress, MacAddress, TruthValue, TestAndIncr, AutonomousType, InstancePointer, VariablePointer, RowPointer, RowStatus, TimeStamp, TimeInterval, DateAndTime, StorageType, TDomain, Taddress</span><span class="sxs-lookup"><span data-stu-id="3e6b7-166">DisplayString, PhysAddress, MacAddress, TruthValue, TestAndIncr, AutonomousType, InstancePointer, VariablePointer, RowPointer, RowStatus, TimeStamp, TimeInterval, DateAndTime, StorageType, Tdomain, Taddress</span></span> |
|                    | <span data-ttu-id="3e6b7-167">SNMPv2-TM</span><span class="sxs-lookup"><span data-stu-id="3e6b7-167">SNMPv2-TM</span></span>   | <span data-ttu-id="3e6b7-168">SnmpUDPAddress, SnmpOSIAddress, SnmpNBPAddress, SnmpIPXAddress</span><span class="sxs-lookup"><span data-stu-id="3e6b7-168">SnmpUDPAddress, SnmpOSIAddress, SnmpNBPAddress, SnmpIPXAddress</span></span>                                                                                                                                                 |



 

## <a name="fatal-error-1032"></a><span data-ttu-id="3e6b7-169">Erreur irrécupérable 1032</span><span class="sxs-lookup"><span data-stu-id="3e6b7-169">Fatal Error 1032</span></span>

<dl> <dt>

<span data-ttu-id="3e6b7-170"><span id="_1032__Fatal_____fileName__line____Duplicate_value__value__in_enumeration_"></span><span id="_1032__fatal_____filename__line____duplicate_value__value__in_enumeration_"></span><span id="_1032__FATAL_____FILENAME__LINE____DUPLICATE_VALUE__VALUE__IN_ENUMERATION_"></span>**<1032,> irrécupérable : " <fileName><ligne \#> : valeur dupliquée <value> dans l’énumération"**</span><span class="sxs-lookup"><span data-stu-id="3e6b7-170"><span id="_1032__Fatal_____fileName__line____Duplicate_value__value__in_enumeration_"></span><span id="_1032__fatal_____filename__line____duplicate_value__value__in_enumeration_"></span><span id="_1032__FATAL_____FILENAME__LINE____DUPLICATE_VALUE__VALUE__IN_ENUMERATION_"></span>**<1032, Fatal>: "<fileName><line\#>: Duplicate value <value> in enumeration"**</span></span>
</dt> <dd>

<span data-ttu-id="3e6b7-171">Erreur de sémantique de module dans une énumération, propre à SNMPv1 et SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="3e6b7-171">Module semantic error in an enumeration, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="3e6b7-172">Il ne doit pas y avoir de valeurs en double.</span><span class="sxs-lookup"><span data-stu-id="3e6b7-172">There must not be any duplicate values.</span></span> <span data-ttu-id="3e6b7-173">Le paramètre de \#> de ligne <correspond à la position de la récurrence du nom/de la valeur.</span><span class="sxs-lookup"><span data-stu-id="3e6b7-173">The <line\#> parameter is the position of the recurrence of the name/value.</span></span>

</dd> </dl>

## <a name="fatal-error-1033"></a><span data-ttu-id="3e6b7-174">Erreur irrécupérable 1033</span><span class="sxs-lookup"><span data-stu-id="3e6b7-174">Fatal Error 1033</span></span>

<dl> <dt>

<span data-ttu-id="3e6b7-175"><span id="_1033__Fatal_____fileName__line____Duplicate_name__identifier__in_enumeration_"></span><span id="_1033__fatal_____filename__line____duplicate_name__identifier__in_enumeration_"></span><span id="_1033__FATAL_____FILENAME__LINE____DUPLICATE_NAME__IDENTIFIER__IN_ENUMERATION_"></span>**<1033,> irrécupérable : " <fileName><ligne \#> : nom dupliqué <identifier> dans l’énumération"**</span><span class="sxs-lookup"><span data-stu-id="3e6b7-175"><span id="_1033__Fatal_____fileName__line____Duplicate_name__identifier__in_enumeration_"></span><span id="_1033__fatal_____filename__line____duplicate_name__identifier__in_enumeration_"></span><span id="_1033__FATAL_____FILENAME__LINE____DUPLICATE_NAME__IDENTIFIER__IN_ENUMERATION_"></span>**<1033, Fatal>: "<fileName><line\#>: Duplicate name <identifier> in enumeration"**</span></span>
</dt> <dd>

<span data-ttu-id="3e6b7-176">Erreur de sémantique de module dans une énumération, propre à SNMPv1 et SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="3e6b7-176">Module semantic error in an enumeration, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="3e6b7-177">Il ne doit pas y avoir de noms en double.</span><span class="sxs-lookup"><span data-stu-id="3e6b7-177">There must not be any duplicate names.</span></span> <span data-ttu-id="3e6b7-178">Le paramètre de \#> de ligne <correspond à la position de la récurrence du nom/de la valeur.</span><span class="sxs-lookup"><span data-stu-id="3e6b7-178">The <line\#> parameter is the position of the recurrence of the name/value.</span></span>

</dd> </dl>

## <a name="warning-1034"></a><span data-ttu-id="3e6b7-179">AVERTISSEMENT 1034</span><span class="sxs-lookup"><span data-stu-id="3e6b7-179">Warning 1034</span></span>

<dl> <dt>

<span data-ttu-id="3e6b7-180"><span id="_1034__Warning_____fileName__line____A_value_of_0_disallowed_in_an_enumeration_"></span><span id="_1034__warning_____filename__line____a_value_of_0_disallowed_in_an_enumeration_"></span><span id="_1034__WARNING_____FILENAME__LINE____A_VALUE_OF_0_DISALLOWED_IN_AN_ENUMERATION_"></span>**<1034, avertissement> : « <fileName><ligne \#> : valeur 0 non autorisée dans une énumération »**</span><span class="sxs-lookup"><span data-stu-id="3e6b7-180"><span id="_1034__Warning_____fileName__line____A_value_of_0_disallowed_in_an_enumeration_"></span><span id="_1034__warning_____filename__line____a_value_of_0_disallowed_in_an_enumeration_"></span><span id="_1034__WARNING_____FILENAME__LINE____A_VALUE_OF_0_DISALLOWED_IN_AN_ENUMERATION_"></span>**<1034, Warning>: "<fileName><line\#>: A value of 0 disallowed in an enumeration"**</span></span>
</dt> <dd>

<span data-ttu-id="3e6b7-181">AVERTISSEMENT sémantique de module dans une énumération, spécifique à, ou à SNMPv1 et à SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="3e6b7-181">Module semantic warning in an enumeration, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="3e6b7-182">Il est recommandé d’utiliser une valeur nommée égale à zéro dans une énumération.</span><span class="sxs-lookup"><span data-stu-id="3e6b7-182">It is recommended that a named value of zero not be used in an enumeration.</span></span>

</dd> </dl>

## <a name="warning-1036"></a><span data-ttu-id="3e6b7-183">AVERTISSEMENT 1036</span><span class="sxs-lookup"><span data-stu-id="3e6b7-183">Warning 1036</span></span>

<dl> <dt>

<span data-ttu-id="3e6b7-184"><span id="_1036__Warning____fileName__line____Value_in_enumeration_does_not_resolve_to_a_positive_integer_"></span><span id="_1036__warning____filename__line____value_in_enumeration_does_not_resolve_to_a_positive_integer_"></span><span id="_1036__WARNING____FILENAME__LINE____VALUE_IN_ENUMERATION_DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1036, avertissement> « <fileName><\#> de ligne : la valeur dans l’énumération n’est pas résolue en entier positif »**</span><span class="sxs-lookup"><span data-stu-id="3e6b7-184"><span id="_1036__Warning____fileName__line____Value_in_enumeration_does_not_resolve_to_a_positive_integer_"></span><span id="_1036__warning____filename__line____value_in_enumeration_does_not_resolve_to_a_positive_integer_"></span><span id="_1036__WARNING____FILENAME__LINE____VALUE_IN_ENUMERATION_DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1036, Warning> "<fileName><line\#>: Value in enumeration does not resolve to a positive integer"**</span></span>
</dt> <dd>

<span data-ttu-id="3e6b7-185">AVERTISSEMENT sémantique de module dans une énumération, spécifique à, ou à SNMPv1 et à SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="3e6b7-185">Module semantic warning in an enumeration, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="3e6b7-186">Une valeur négative n’est pas autorisée dans une énumération.</span><span class="sxs-lookup"><span data-stu-id="3e6b7-186">A negative value is not allowed in an enumeration.</span></span>

</dd> </dl>

## <a name="fatal-error-1037"></a><span data-ttu-id="3e6b7-187">Erreur irrécupérable 1037</span><span class="sxs-lookup"><span data-stu-id="3e6b7-187">Fatal Error 1037</span></span>

<dl> <dt>

<span data-ttu-id="3e6b7-188"><span id="_1037__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_to_OCTET_STRING_or_Opaque_types_"></span><span id="_1037__fatal_____filename__line____identifier__identifier__does_not_resolve_to_octet_string_or_opaque_types_"></span><span id="_1037__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_TO_OCTET_STRING_OR_OPAQUE_TYPES_"></span>**<1037,> irrécupérable : " <fileName><\#> de ligne : l’identificateur <identifier> n’est pas résolu en chaîne d’octets ou en types opaques"**</span><span class="sxs-lookup"><span data-stu-id="3e6b7-188"><span id="_1037__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_to_OCTET_STRING_or_Opaque_types_"></span><span id="_1037__fatal_____filename__line____identifier__identifier__does_not_resolve_to_octet_string_or_opaque_types_"></span><span id="_1037__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_TO_OCTET_STRING_OR_OPAQUE_TYPES_"></span>**<1037, Fatal>: "<fileName><line\#>: Identifier <identifier> does not resolve to OCTET STRING or Opaque types"**</span></span>
</dt> <dd>

<span data-ttu-id="3e6b7-189">Erreur de sémantique de module dans la spécification de taille, propre à ni SNMPv1 ni SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="3e6b7-189">Module semantic error in SIZE specification, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="3e6b7-190">Le symbole utilisé dans une spécification de taille doit être converti en OCTET STRING ou opaque.</span><span class="sxs-lookup"><span data-stu-id="3e6b7-190">The symbol used in a SIZE specification must resolve to OCTET STRING or Opaque.</span></span>

</dd> </dl>

## <a name="fatal-error-1038"></a><span data-ttu-id="3e6b7-191">Erreur irrécupérable 1038</span><span class="sxs-lookup"><span data-stu-id="3e6b7-191">Fatal Error 1038</span></span>

<dl> <dt>

<span data-ttu-id="3e6b7-192"><span id="_1038__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_an_INTEGER_or_Gauge_type_"></span><span id="_1038__fatal_____filename__line____identifier__identifier__does_not_resolve_an_integer_or_gauge_type_"></span><span id="_1038__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_AN_INTEGER_OR_GAUGE_TYPE_"></span>**<1038,> irrécupérable : " <fileName><line \#> : identifier <identifier> ne résout pas un entier ou un type de jauge"**</span><span class="sxs-lookup"><span data-stu-id="3e6b7-192"><span id="_1038__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_an_INTEGER_or_Gauge_type_"></span><span id="_1038__fatal_____filename__line____identifier__identifier__does_not_resolve_an_integer_or_gauge_type_"></span><span id="_1038__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_AN_INTEGER_OR_GAUGE_TYPE_"></span>**<1038, Fatal>: "<fileName><line\#>: Identifier <identifier> does not resolve an INTEGER or Gauge type"**</span></span>
</dt> <dd>

<span data-ttu-id="3e6b7-193">Erreur de sémantique de module dans la spécification de plage.</span><span class="sxs-lookup"><span data-stu-id="3e6b7-193">Module semantic error in range specification.</span></span> <span data-ttu-id="3e6b7-194">Cette erreur peut se produire dans SNMPv1 ou SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="3e6b7-194">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

<span data-ttu-id="3e6b7-195">Dans SNMPv1, le symbole utilisé dans une spécification de plage doit être résolu en entier ou jauge.</span><span class="sxs-lookup"><span data-stu-id="3e6b7-195">In SNMPv1, the symbol used in a Range specification must resolve to INTEGER or Gauge.</span></span>

<span data-ttu-id="3e6b7-196">Dans SNMPv2C, le symbole utilisé dans une spécification de plage doit être converti en INTEGER, gauge32, Integer32 ou Unsigned32.</span><span class="sxs-lookup"><span data-stu-id="3e6b7-196">In SNMPv2C, the symbol used in a Range specification must resolve to INTEGER, Gauge32, Integer32, or Unsigned32.</span></span>

</dd> </dl>

## <a name="fatal-error-1039"></a><span data-ttu-id="3e6b7-197">Erreur irrécupérable 1039</span><span class="sxs-lookup"><span data-stu-id="3e6b7-197">Fatal Error 1039</span></span>

<dl> <dt>

<span data-ttu-id="3e6b7-198"><span id="_1039__Fatal___fileName__line____Negative_value_used_in_SIZE_specification_"></span><span id="_1039__fatal___filename__line____negative_value_used_in_size_specification_"></span><span id="_1039__FATAL___FILENAME__LINE____NEGATIVE_VALUE_USED_IN_SIZE_SPECIFICATION_"></span>**<1039,> fatale : <fileName><ligne \#> : valeur négative utilisée dans la spécification de taille»**</span><span class="sxs-lookup"><span data-stu-id="3e6b7-198"><span id="_1039__Fatal___fileName__line____Negative_value_used_in_SIZE_specification_"></span><span id="_1039__fatal___filename__line____negative_value_used_in_size_specification_"></span><span id="_1039__FATAL___FILENAME__LINE____NEGATIVE_VALUE_USED_IN_SIZE_SPECIFICATION_"></span>**<1039, Fatal>:<fileName><line\#>: Negative value used in SIZE specification"**</span></span>
</dt> <dd>

<span data-ttu-id="3e6b7-199">Erreur de sémantique de module dans la spécification de taille, propre à ni SNMPv1 ni SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="3e6b7-199">Module semantic error in SIZE specification, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="3e6b7-200">Toute valeur utilisée dans la spécification de la taille ne doit pas être négative.</span><span class="sxs-lookup"><span data-stu-id="3e6b7-200">Any value used in specifying the SIZE must be non-negative.</span></span>

</dd> </dl>

## <a name="fatal-error-1040"></a><span data-ttu-id="3e6b7-201">Erreur irrécupérable 1040</span><span class="sxs-lookup"><span data-stu-id="3e6b7-201">Fatal Error 1040</span></span>

<dl> <dt>

<span data-ttu-id="3e6b7-202"><span id="_1040__Fatal_____fileName__line____Identifier__identifier__in_SIZE_specification_does_not_resolve_to_a_non-negative_integral_value_"></span><span id="_1040__fatal_____filename__line____identifier__identifier__in_size_specification_does_not_resolve_to_a_non-negative_integral_value_"></span><span id="_1040__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_SIZE_SPECIFICATION_DOES_NOT_RESOLVE_TO_A_NON-NEGATIVE_INTEGRAL_VALUE_"></span>**<1040,> irrécupérable : « <fileName><ligne \#> : l’identificateur <identifier> dans la spécification de taille n’est pas résolu en une valeur intégrale non négative »**</span><span class="sxs-lookup"><span data-stu-id="3e6b7-202"><span id="_1040__Fatal_____fileName__line____Identifier__identifier__in_SIZE_specification_does_not_resolve_to_a_non-negative_integral_value_"></span><span id="_1040__fatal_____filename__line____identifier__identifier__in_size_specification_does_not_resolve_to_a_non-negative_integral_value_"></span><span id="_1040__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_SIZE_SPECIFICATION_DOES_NOT_RESOLVE_TO_A_NON-NEGATIVE_INTEGRAL_VALUE_"></span>**<1040, Fatal>: "<fileName><line\#>: Identifier <identifier> in SIZE specification does not resolve to a non-negative integral value"**</span></span>
</dt> <dd>

<span data-ttu-id="3e6b7-203">Erreur de sémantique de module dans la spécification de la plage ou de la taille, propre à non-SNMPv1 ou SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="3e6b7-203">Module semantic error in range or size specification, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="3e6b7-204">Tout symbole utilisé pour la spécification d’une valeur dans une spécification de taille correspond à une valeur non négative.</span><span class="sxs-lookup"><span data-stu-id="3e6b7-204">Any symbol used in specifying a value in a SIZE specification resolves to a non-negative value.</span></span>

</dd> </dl>

 

 



