---
description: Les fournisseurs d’événements SNMP prennent en charge les notifications SNMPv1 et SNMPv2.
ms.assetid: 715b2925-b01d-4631-86e3-a6239ff1dba7
ms.tgt_platform: multiple
title: Réception d’événements SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4f718d2bcea85d0ee942050108f337f8ecb78e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520028"
---
# <a name="receiving-snmp-events"></a>Réception d’événements SNMP

Les fournisseurs d’événements SNMP prennent en charge les notifications SNMPv1 et SNMPv2.

Les trois types suivants d’interruptions SNMPv1 et de notifications SNMPv2 sont pris en charge :

-   Générique

    Les notifications et les interruptions génériques correspondent à des événements nommés tels que le lien vers le haut et le démarrage à froid. Les notifications et les interruptions génériques sont représentées par des classes, telles que **SnmpLinkUpNotification** et **SnmpWarmStartExtendedNotification**, qui contiennent le nom de l’interruption dans le nom de la classe. Ces classes sont des sous-classes de [SnmpNotification](snmpnotification.md) et [SnmpExtendedNotification](snmpextendednotification.md).

-   Spécifique à l’entreprise

    Les notifications et les interruptions spécifiques à l’entreprise correspondent à des événements qui sont représentés par une classe WMI qui n’est pas une sous-classe de [SnmpNotification](snmpnotification.md) et [SnmpExtendedNotification](snmpextendednotification.md). Pour prendre en charge les notifications et les interruptions spécifiques à l’entreprise, un consommateur doit définir des classes en compilant les définitions MIB à l’aide du compilateur MIB SNMP.

-   Entreprise-non spécifique

    Les notifications et les interruptions spécifiques à l’entreprise ne correspondent à aucun type d’événement générique ou type d’événement spécifique à l’entreprise. Les notifications MIB et les interruptions non spécifiques à l’entreprise n’ont pas été compilées dans le stockage SMIR. Ils sont représentés par les classes [SnmpNotification](snmpnotification.md), **SnmpV2Notification**, **SnmpV1ExtendedNotification** et **SnmpV2ExtendedNotification** dérivées de SnmpNotification et [SnmpExtendedNotification](snmpextendednotification.md).

> [!Note]  
> Pour plus d’informations sur l’installation du fournisseur, consultez [configuration de l’environnement SNMP WMI](setting-up-the-wmi-snmp-environment.md).

 

Les sections suivantes sont présentées dans cette rubrique :

-   [Réception d’événements SNMP génériques](#receiving-generic-snmp-events)
-   [Réception des événements de Enterprise-Specific](#receiving-enterprise-specific-events)
-   [Réception des événements de Enterprise-Nonspecific](#receiving-enterprise-nonspecific-events)

## <a name="receiving-generic-snmp-events"></a>Réception d’événements SNMP génériques

SEEP et SREP prennent en charge tous les types d’interruptions SNMPv1 génériques et de notifications SNMPv2. Les événements SNMP génériques sont représentés par des sous-classes des classes [SnmpNotification](snmpnotification.md) et [SnmpExtendedNotification](snmpextendednotification.md) .

Chaque type d’événement est représenté par une classe SEEP et une classe SREP. Les classes SEEP dérivent de [SnmpNotification](snmpnotification.md); les classes SREP dérivent de [SnmpExtendedNotification](snmpextendednotification.md). Les fournisseurs d’événements requièrent des classes différentes car ils utilisent des mécanismes différents dans la présentation des données d’événement SNMP.

Le SEEP convertit les données d’événement SNMP directement en propriétés de classe WMI, contrairement à SREP. Le SREP ajoute un niveau d’indirection à l’interprétation requise pour utiliser les propriétés WMI. Les propriétés des sous-classes SREP [SnmpExtendedNotification](snmpextendednotification.md) sont des instances de classes SNMP. les propriétés des sous-classes SEEP [SnmpNotification](snmpnotification.md) sont des entiers et des chaînes.

Le tableau suivant répertorie les types d’événements SNMP génériques et les classes d’événements associées.



| Événement SNMP                                    | SEEP, classe                                | SREP, classe                                        |
|-----------------------------------------------|-------------------------------------------|---------------------------------------------------|
| Échec de l’authentification                        | **SnmpAuthenticationFailureNotification** | **SnmpAuthenticationFailureExtendedNotification** |
| Perte de voisinage du protocole de passerelle externe (EGP) | **SnmpEGPNeighborLossNotification**       | **SnmpEGPNeighborLossExtendedNotification**       |
| Démarrage à froid                                    | **SnmpColdStartNotification**             | **SnmpColdStartExtendedNotification**             |
| Démarrage à chaud                                    | **SnmpWarmStartNotification**             | **SnmpWarmStartExtendedNotification**             |
| Lien vers le haut                                       | **SnmpLinkUpNotification**                | **SnmpLinkUpExtendedNotification**                |
| Lien vers le dessous                                     | **SnmpLinkDownNotification**              | **SnmpLinkDownExtendedNotification**              |



 

Par exemple, les classes **SnmpLinkUpNotification** et **SnmpLinkUpExtendedNotification** décrivent l’événement Link-Up. Les deux classes incluent les propriétés **ifIndex**, **ifAdminStatus** et **ifOperStatus** , mais leurs types sont très différents. Les propriétés de la classe **SnmpLinkUpNotification** sont de type SINT32 et String. Les propriétés de la classe **SnmpLinkUpExtendedNotification** sont le type d’objet incorporé «IETF \_ SNMP \_ RFC1213 \_ MIB \_ ifTable.

## <a name="receiving-enterprise-specific-events"></a>Réception des événements de Enterprise-Specific

SEEP et SREP prennent en charge les notifications et les interruptions spécifiques à l’entreprise que vous avez compilées dans le stockage SMIR.

La procédure suivante décrit comment recevoir des événements spécifiques à l’entreprise.

**Pour recevoir des événements spécifiques à l’entreprise**

1.  Compilez les définitions MIB à partir du périphérique responsable de la génération de l’événement.

    Vous pouvez compiler les définitions MIB à l’aide du compilateur MIB SNMP. Pour plus d’informations, consultez [configuration de l’environnement SNMP WMI](setting-up-the-wmi-snmp-environment.md).

2.  Déterminez les types de classes que vous souhaitez mapper aux événements.

    Quand vous compilez la définition MIB pour un événement spécifique à l’entreprise, vous pouvez déterminer le type de classe que le compilateur génère. Plus précisément, vous pouvez indiquer au compilateur de créer l’une des options suivantes :

    -   [SnmpNotification](snmpnotification.md) sous-classes des définitions.
    -   [SnmpExtendedNotification](snmpextendednotification.md) sous-classes des définitions.
    -   Les sous-classes [SnmpNotification](snmpnotification.md) et [SnmpExtendedNotification](snmpextendednotification.md) des définitions.

    Pour plus d’informations, consultez [compilation des fichiers MOF](compiling-mof-files.md).

Si les fournisseurs d’événements SNMP reçoivent une notification ou une notification spécifique pour laquelle il n’existe aucune classe, les fournisseurs génèrent un événement qui n’est pas spécifique à l’entreprise. Pour plus d’informations, consultez [réception d’événements non spécifiques](#receiving-enterprise-nonspecific-events)de l’entreprise.

## <a name="receiving-enterprise-nonspecific-events"></a>Réception des événements de Enterprise-Nonspecific

Un événement qui n’est pas spécifique à l’entreprise est un événement qui ne mappe pas une notification SNMPv1 Trap ou SNMPv2 à l’une des sous-classes de [SnmpNotification](snmpnotification.md) ou [SnmpExtendedNotification](snmpextendednotification.md) ou toute classe qui représente un événement d’entreprise.

SEEP utilise les classes **SNMPV1Notification** ou **SNMPV2Notification** pour les événements non spécifiques, tandis que SREP utilise les classes **SNMPv1ExtendedNotification** et **SNMPV2ExtendedNotification** .

Les quatre classes non spécifiques à l’entreprise dérivent des classes [SnmpNotification](snmpnotification.md) ou [SnmpExtendedNotification](snmpextendednotification.md) et ont le même format. Les deux classes ont la propriété unique **VarBindList**. **VarBindList** est un tableau d’instances de la classe **SnmpVarBind** . **SnmpVarBind** est une classe de base prise en charge par les fournisseurs d’événements SNMP pour représenter une instance d’une liaison de variable SNMP. Le tableau suivant répertorie les propriétés de **SnmpVarBind**.



| Propriété         | Description                                                                                                    |
|------------------|----------------------------------------------------------------------------------------------------------------|
| Encodage         | Chaîne qui indique le type ASN. 1 (Abstract Syntax Notation One) de la variable dans la propriété **value** . |
| ObjectIdentifier | Chaîne qui identifie la variable dans la propriété **value** .                                                 |
| Valeur            | Données brutes en octets.                                                                                            |



 

Dans les classes **SnmpV1Notification** et **SnmpV2Notification** , l’ordre de liaison de variable de l’événement SNMP a été préservé, à l’exception des deux premières liaisons de variables, timestamp et SnmpTrapOID. Ces liaisons ont été supprimées et sont stockées dans les propriétés d' **horodatage** et d' **identification** de la classe parente [SnmpNotification](snmpnotification.md) ou [SnmpExtendedNotification](snmpextendednotification.md) .

 

 



