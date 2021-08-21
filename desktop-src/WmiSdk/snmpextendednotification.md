---
description: La classe SnmpExtendedNotification est la classe de base pour toute classe mappée à partir de la macro de TYPE NOTIFICATION à une classe CIM par le fournisseur SNMP.
ms.assetid: 207966c1-14cf-4a47-8176-0f58838cfa1e
ms.tgt_platform: multiple
title: SnmpExtendedNotification, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SnmpExtendedNotification
- SnmpExtendedNotification.SECURITY_DESCRIPTOR
- SnmpExtendedNotification.TIME_CREATED
- SnmpExtendedNotification.AgentAddress
- SnmpExtendedNotification.AgentTransport
- SnmpExtendedNotification.AgentTransportAddress
- SnmpExtendedNotification.Community
- SnmpExtendedNotification.Identification
- SnmpExtendedNotification.TimeStamp
- SnmpExtendedNotification.AgentTransportProtocol
api_type:
- Schema
api_location:
- Root\snmp\SMIR
ms.openlocfilehash: d8da8533e9ac5c86dfa3291092fb5165b94e2e393e507c55f15b64c1e30cd6a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118816539"
---
# <a name="snmpextendednotification-class"></a>SnmpExtendedNotification, classe

La classe **SnmpExtendedNotification** est la classe de base pour toute classe mappée à partir de la macro de [type notification](notification-type-macro.md) à une classe CIM par le [fournisseur SNMP](snmp-provider.md).

> [!Note]  
> Pour plus d’informations sur l’installation du fournisseur, consultez [configuration de l’environnement SNMP WMI](setting-up-the-wmi-snmp-environment.md).

 

La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées. Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class SnmpExtendedNotification : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  string AgentAddress;
  string AgentTransport;
  string AgentTransportAddress;
  string Community;
  string Identification;
  string TimeStamp;
  string AgentTransportProtocol;
};
```

## <a name="members"></a>Membres

La classe **SnmpExtendedNotification** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **SnmpExtendedNotification** possède les propriétés suivantes.

<dl> <dt>

**AgentAddress**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Adresse réseau de l’entité qui a créé la notification. Il s’agit de l’adresse réelle de l’appareil. Lorsque l’entité de gestion utilise SNMP sur UDP, l’adresse de transport fait référence à une adresse IP. Lorsque l’entité de gestion utilise SNMP sur IPX, l’adresse de transport est définie sur **null**. Cette propriété est valide uniquement pour SNMPv1.

</dd> <dt>

**AgentTransport**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Protocole de transport utilisé par l’entité émettrice. Cette propriété est valide pour SNMPv1 et SNMPv2C.

</dd> <dt>

**AgentTransportAddress**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Adresse réseau de l’entité qui a envoyé la notification. Il s’agit de l’adresse de la dernière entité qui a transféré la notification. Lorsque l’entité de gestion utilise SNMP sur UDP, l’adresse de transport fait référence à une adresse IP. Lorsque l’entité de gestion utilise SNMP sur IPX, l’adresse de transport fait référence à une adresse IPX. Cette propriété est valide pour SNMPv1 et SNMPv2C.

</dd> <dt>

**AgentTransportProtocol**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Protocole de transport utilisé par l’entité émettrice.

</dd> <dt>

**Communauté**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

nom de Community associé à une instance de la PDU. Le nom de la communauté authentifie l’expéditeur de l’PDU. Cette propriété est valide pour SNMPv1 et SNMPv2C.

</dd> <dt>

**Identification**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **\_ Convention textuelle** (« OBJECTIDENTIFIER »), **encodage** (« OBJECTIDENTIFIER ») **, \_ syntaxe d’objet** (« OBJECTIDENTIFIER »), **\_ identificateur d’objet** (« 1.3.6.1.6.3.1.1.4.1 »)
</dt> </dl>

Identification faisant autorité de cette notification. Cartes directement à l’entrée MIB liaison de variable SnmpTrapOID. Cette propriété est valide uniquement pour SNMPv2C.

</dd> <dt>

**descripteur de sécurité \_**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Descripteur utilisé par le fournisseur d’événements pour déterminer les utilisateurs qui peuvent recevoir l’événement. Cette propriété est héritée de l' [**\_ \_ événement**](--event.md). Pour plus d’informations sur les constantes utilisées pour définir ce descripteur de sécurité, voir la rubrique sur les [constantes de sécurité WMI](wmi-security-constants.md).

</dd> <dt>

**HEURE de \_ création**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Valeur unique qui indique l’heure à laquelle l’événement a été généré. Il s’agit d’une valeur 64 bits qui représente le nombre d’intervalles de 100 nanosecondes après le 1er janvier 1601. Les informations sont au format de temps universel coordonné (UTC). Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**Confirmé**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **\_ Convention textuelle** (« graduations »), **encodage** (« graduations ») **, \_ syntaxe d’objet** (« graduations »), **\_ identificateur d’objet** (« 1.3.6.1.2.1.1.3 »)
</dt> </dl>

Durée en centièmes de seconde depuis la dernière réinitialisation de la partie gestion du réseau de l’agent. Correspond à la variable MIB sysUptime. 0, qui est de type **INTEGER32**. Cette propriété est mappée à l' **horodateur** de propriété de la classe CIM, qui est de type **UInt32**. Cette propriété est valide uniquement pour SNMPv2C.

</dd> </dl>

## <a name="remarks"></a>Remarques

Une macro de [type notification](notification-type-macro.md) qui contient des références à une macro de [type objet](object-type-macro.md) nommée **timestamp** ou **identification** provoque un conflit de mappage. Si ce conflit se produit, les propriétés requises sont prioritaires et les références en conflit doivent être renommées.

une macro de [type NOTIFICATION](notification-type-macro.md) qui contient des références à une macro de [type objet](object-type-macro.md) nommée **Community** provoque un conflit de mappage. Si ce conflit se produit, les propriétés requises sont prioritaires et les références en conflit doivent être renommées.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Stockage SMIR SNMP \\ racine<br/>                                                             |
| MOF<br/>                      | <dl> <dt>SnmpSmiR. mof</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_\_ExtrinsicEvent**](--extrinsicevent.md)
</dt> <dt>

[Macro de TYPE NOTIFICATION](notification-type-macro.md)
</dt> </dl>

 

