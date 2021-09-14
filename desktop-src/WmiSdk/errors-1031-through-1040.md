---
description: Décrit les erreurs du fournisseur SNMP WMI 1031 à 1040.
ms.assetid: 5fc519ac-ae05-4daf-a681-7935190f1d46
ms.tgt_platform: multiple
title: Erreurs 1031 à 1040
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5986ba80a55d2d8f3d4a87b0587331765aa38d67
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127237065"
---
# <a name="errors-1031-through-1040"></a>Erreurs 1031 à 1040

Décrit les erreurs du fournisseur SNMP WMI 1031 à 1040.

[AVERTISSEMENT 1031](#warning-1031)

[Erreur irrécupérable 1032](#fatal-error-1032)

[Erreur irrécupérable 1033](#fatal-error-1033)

[AVERTISSEMENT 1034](#warning-1034)

[AVERTISSEMENT 1036](#warning-1036)

[Erreur irrécupérable 1037](#fatal-error-1037)

[Erreur irrécupérable 1038](#fatal-error-1038)

[Erreur irrécupérable 1039](#fatal-error-1039)

[Erreur irrécupérable 1040](#fatal-error-1040)

## <a name="warning-1031"></a>AVERTISSEMENT 1031

<dl> <dt>

<span id="_1031__Warning_____fileName___line____Standard_symbol__identifier__should_be_imported_from_module__identifier_._Assuming_the_standard_definition._"></span><span id="_1031__warning_____filename___line____standard_symbol__identifier__should_be_imported_from_module__identifier_._assuming_the_standard_definition._"></span><span id="_1031__WARNING_____FILENAME___LINE____STANDARD_SYMBOL__IDENTIFIER__SHOULD_BE_IMPORTED_FROM_MODULE__IDENTIFIER_._ASSUMING_THE_STANDARD_DEFINITION._"></span>**<1031, avertissement> : " &lt; NomFichier &gt; : <ligne \#> : l' &lt; identificateur de symbole standard &gt; doit être importé à partir de l’identificateur de module &lt; &gt; . En supposant la définition standard.»**
</dt> <dd>

IMPORTE la section Avertissement sémantique de module, spécifique à ni SNMPv1 ni SNMPv2C. Si un identificateur SNMP connu du compilateur se trouve dans la section Imports, le module à partir duquel il est importé doit être l’un des modules standard.

Certaines importations couramment utilisées sont des « connaissances supposées » dans la partie du compilateur. Il n’est pas nécessaire que le compilateur requière l’accès à d’autres modules d’informations pour les résoudre.

Les importations de SNMPv1 et SNMPv2C intégrées sont décrites dans les tableaux suivants.

</dd> </dl>

**IMPORTATIONS SNMPv1 intégrées**



| Classe d’importation | Module      | Instances                                                           |
|--------------|-------------|---------------------------------------------------------------------|
| Valeur ASN. 1  | RFC1155-SMI | Internet, annuaire, gestion, expérimental, privé, entreprises |
|              | RFC1213-MIB | MIB-II et IP, interfaces, transmission                             |
| Type ASN. 1   | RFC1155-SMI | NetworkAddress, IpAddress, compteur, jauge, graduations, opaque        |
|              | RFC1213-MIB | DisplayString, PhysAddress                                          |
| Macro ASN. 1  | RFC 1212    | TYPE D’OBJET                                                         |
|              | RFC 1215    | TYPE D’INTERRUPTION                                                           |



 

**IMPORTATIONS SNMPv2C intégrées**



| Classe d’importation       | Module      | Instances                                                                                                                                                                                                      |
|--------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Valeur ASN. 1        | SNMPv2-SMI  | org, DOD, Internet, annuaire, gestion, MIB-2, transmission, expérimental, privé, Enterprises, Security, SNMPv2, snmpDomains, snmpProxys, snmpModules                                                           |
|                    | SNMPv2-TM   | rfc1157Proxy                                                                                                                                                                                                   |
| Identité d'un objet    | SNMPv2-SMI  | zeroDotZero                                                                                                                                                                                                    |
|                    | SNMPv2-TM   | snmpUDPDomain, snmpCLNSDomain, smnpCONSDomain, snmpDDPDomain, snmpIPXDomain, rfc1157Domain                                                                                                                     |
| Type ASN. 1         | SNMPv2-SMI  | Integer32, IpAddress, Counter32, graduations, opaque, Counter64, Unsigned32, gauge32                                                                                                                             |
| Macro ASN. 1        | SNMPv2-SMI  | MODULE-IDENTITY, OBJECT-IDENTITY, OBJECT-TYPE, NOTIFICATION-TYPE                                                                                                                                               |
|                    | SNMPv2-CONF | GROUPE D’OBJETS, NOTIFICATION-GROUPE, CONFORMITÉ DE MODULE, AGENT-FONCTIONNALITÉS                                                                                                                                        |
|                    | SNMPv2-TC   | CONVENTION TEXTUELLE                                                                                                                                                                                             |
| Convention textuelle | SNMPv2-TC   | DisplayString, PhysAddress, MacAddress, TruthValue, TestAndIncr, AutonomousType, InstancePointer, VariablePointer, RowPointer, RowStatus, TimeStamp, TimeInterval, DateAndTime, StorageType, TDomain, Taddress |
|                    | SNMPv2-TM   | SnmpUDPAddress, SnmpOSIAddress, SnmpNBPAddress, SnmpIPXAddress                                                                                                                                                 |



 

## <a name="fatal-error-1032"></a>Erreur irrécupérable 1032

<dl> <dt>

<span id="_1032__Fatal_____fileName__line____Duplicate_value__value__in_enumeration_"></span><span id="_1032__fatal_____filename__line____duplicate_value__value__in_enumeration_"></span><span id="_1032__FATAL_____FILENAME__LINE____DUPLICATE_VALUE__VALUE__IN_ENUMERATION_"></span>**<1032,> irrécupérable : " &lt; nomfichier &gt;<ligne \#> : valeur de valeur dupliquée &lt; &gt; dans l’énumération"**
</dt> <dd>

Erreur de sémantique de module dans une énumération, propre à SNMPv1 et SNMPv2C. Il ne doit pas y avoir de valeurs en double. Le paramètre de \#> de ligne <correspond à la position de la récurrence du nom/de la valeur.

</dd> </dl>

## <a name="fatal-error-1033"></a>Erreur irrécupérable 1033

<dl> <dt>

<span id="_1033__Fatal_____fileName__line____Duplicate_name__identifier__in_enumeration_"></span><span id="_1033__fatal_____filename__line____duplicate_name__identifier__in_enumeration_"></span><span id="_1033__FATAL_____FILENAME__LINE____DUPLICATE_NAME__IDENTIFIER__IN_ENUMERATION_"></span>**<1033,> fatale : " &lt; fileName &gt;<ligne \#> : identificateur de nom dupliqué &lt; &gt; dans l’énumération"**
</dt> <dd>

Erreur de sémantique de module dans une énumération, propre à SNMPv1 et SNMPv2C. Il ne doit pas y avoir de noms en double. Le paramètre de \#> de ligne <correspond à la position de la récurrence du nom/de la valeur.

</dd> </dl>

## <a name="warning-1034"></a>AVERTISSEMENT 1034

<dl> <dt>

<span id="_1034__Warning_____fileName__line____A_value_of_0_disallowed_in_an_enumeration_"></span><span id="_1034__warning_____filename__line____a_value_of_0_disallowed_in_an_enumeration_"></span><span id="_1034__WARNING_____FILENAME__LINE____A_VALUE_OF_0_DISALLOWED_IN_AN_ENUMERATION_"></span>**<1034, Warning> : " &lt; fileName &gt;<Line \#> : valeur 0 non autorisée dans une énumération"**
</dt> <dd>

AVERTISSEMENT sémantique de module dans une énumération, spécifique à, ou à SNMPv1 et à SNMPv2C. Il est recommandé d’utiliser une valeur nommée égale à zéro dans une énumération.

</dd> </dl>

## <a name="warning-1036"></a>AVERTISSEMENT 1036

<dl> <dt>

<span id="_1036__Warning____fileName__line____Value_in_enumeration_does_not_resolve_to_a_positive_integer_"></span><span id="_1036__warning____filename__line____value_in_enumeration_does_not_resolve_to_a_positive_integer_"></span><span id="_1036__WARNING____FILENAME__LINE____VALUE_IN_ENUMERATION_DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1036, avertissement> " &lt; fileName &gt;<ligne \#> : la valeur dans l’énumération n’est pas résolue en entier positif"**
</dt> <dd>

AVERTISSEMENT sémantique de module dans une énumération, spécifique à, ou à SNMPv1 et à SNMPv2C. Une valeur négative n’est pas autorisée dans une énumération.

</dd> </dl>

## <a name="fatal-error-1037"></a>Erreur irrécupérable 1037

<dl> <dt>

<span id="_1037__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_to_OCTET_STRING_or_Opaque_types_"></span><span id="_1037__fatal_____filename__line____identifier__identifier__does_not_resolve_to_octet_string_or_opaque_types_"></span><span id="_1037__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_TO_OCTET_STRING_OR_OPAQUE_TYPES_"></span>**<1037,> irrécupérable : " &lt; nomfichier &gt;<ligne \#> : l' &lt; identificateur d’identificateur &gt; n’est pas résolu en chaîne d’octets ou en types opaques"**
</dt> <dd>

Erreur de sémantique de module dans la spécification de taille, propre à ni SNMPv1 ni SNMPv2C. Le symbole utilisé dans une spécification de taille doit être converti en OCTET STRING ou opaque.

</dd> </dl>

## <a name="fatal-error-1038"></a>Erreur irrécupérable 1038

<dl> <dt>

<span id="_1038__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_an_INTEGER_or_Gauge_type_"></span><span id="_1038__fatal_____filename__line____identifier__identifier__does_not_resolve_an_integer_or_gauge_type_"></span><span id="_1038__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_AN_INTEGER_OR_GAUGE_TYPE_"></span>**<1038,> fatale : " &lt; fileName &gt;<Line \#> : identifier &lt; &gt; ne résout pas un entier ou un type de jauge"**
</dt> <dd>

Erreur de sémantique de module dans la spécification de plage. Cette erreur peut se produire dans SNMPv1 ou SNMPv2C.

Dans SNMPv1, le symbole utilisé dans une spécification de plage doit être résolu en entier ou jauge.

Dans SNMPv2C, le symbole utilisé dans une spécification de plage doit être converti en INTEGER, gauge32, Integer32 ou Unsigned32.

</dd> </dl>

## <a name="fatal-error-1039"></a>Erreur irrécupérable 1039

<dl> <dt>

<span id="_1039__Fatal___fileName__line____Negative_value_used_in_SIZE_specification_"></span><span id="_1039__fatal___filename__line____negative_value_used_in_size_specification_"></span><span id="_1039__FATAL___FILENAME__LINE____NEGATIVE_VALUE_USED_IN_SIZE_SPECIFICATION_"></span>**<1039,> fatale : &lt; fileName &gt;<ligne \#> : valeur négative utilisée dans la spécification de taille»**
</dt> <dd>

Erreur de sémantique de module dans la spécification de taille, propre à ni SNMPv1 ni SNMPv2C. Toute valeur utilisée dans la spécification de la taille ne doit pas être négative.

</dd> </dl>

## <a name="fatal-error-1040"></a>Erreur irrécupérable 1040

<dl> <dt>

<span id="_1040__Fatal_____fileName__line____Identifier__identifier__in_SIZE_specification_does_not_resolve_to_a_non-negative_integral_value_"></span><span id="_1040__fatal_____filename__line____identifier__identifier__in_size_specification_does_not_resolve_to_a_non-negative_integral_value_"></span><span id="_1040__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_SIZE_SPECIFICATION_DOES_NOT_RESOLVE_TO_A_NON-NEGATIVE_INTEGRAL_VALUE_"></span>**<1040,> irrécupérable : " &lt; fileName &gt;<Line \#> : &lt; l’identificateur d’identificateur &gt; dans la spécification de taille n’est pas résolu en une valeur intégrale non négative"**
</dt> <dd>

Erreur de sémantique de module dans la spécification de la plage ou de la taille, propre à non-SNMPv1 ou SNMPv2C. Tout symbole utilisé pour la spécification d’une valeur dans une spécification de taille correspond à une valeur non négative.

</dd> </dl>

 

 



