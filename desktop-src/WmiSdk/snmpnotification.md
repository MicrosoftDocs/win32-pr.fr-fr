---
description: La classe SnmpNotification mappe la macro de TYPE NOTIFICATION à une classe CIM encapsulée.
ms.assetid: b90d8bab-7cae-4dbe-9f6e-daba4e68a10a
ms.tgt_platform: multiple
title: SnmpNotification, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SnmpNotification
- Root\snmp\localhost.SnmpNotification.SECURITY_DESCRIPTOR
- Root\snmp\localhost.SnmpNotification.TIME_CREATED
- Root\snmp\localhost.SnmpNotification.AgentAddress
- Root\snmp\localhost.SnmpNotification.AgentTransport
- Root\snmp\localhost.SnmpNotification.AgentTransportAddress
- Root\snmp\localhost.SnmpNotification.Community
- Root\snmp\localhost.SnmpNotification.Identification
- Root\snmp\localhost.SnmpNotification.TimeStamp
- Root\snmp\localhost.SnmpNotification.AgentTransportProtocol
api_type:
- Schema
api_location:
- Root\snmp\localhost
ms.openlocfilehash: be0847c7a7d96fb7491274350c828d0cc319240823fa006e972bb295ad477773
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860359"
---
# <a name="snmpnotification-class"></a>SnmpNotification, classe

La classe **SnmpNotification** mappe la macro de [type notification](notification-type-macro.md) à une classe CIM encapsulée. Il s’agit d’une classe de base utilisée par le [fournisseur SNMP](snmp-provider.md) pour toute classe mappée à partir de la macro de [type notification](notification-type-macro.md) à une classe CIM encapsulée par le fournisseur SNMP.

> [!Note]  
> Pour plus d’informations sur l’installation du fournisseur, consultez [configuration de l’environnement SNMP WMI](setting-up-the-wmi-snmp-environment.md).

 

## <a name="syntax"></a>Syntaxe

``` syntax
class SnmpNotification : __ExtrinsicEvent
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

La classe **SnmpNotification** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **SnmpNotification** possède les propriétés suivantes.

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

Identification faisant autorité de cette notification. Cartes directement à la liaison de variable SnmpTrapOID. Cette propriété est valide uniquement pour SNMPv2C.

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

Durée en centièmes de seconde depuis la dernière réinitialisation de la partie gestion du réseau de l’agent. Variable MIB sysUptime. 0, qui est de type **INTEGER32**. Cette propriété est mappée à l' **horodateur** de propriété de la classe CIM, qui est de type **UInt32**. Cette propriété est valide uniquement pour SNMPv2C.

</dd> </dl>

## <a name="remarks"></a>Remarques

Une macro de [type notification](notification-type-macro.md) qui contient des références à une macro de [type objet](object-type-macro.md) nommée **timestamp** ou **identification** provoque un conflit de mappage. Si ce conflit se produit, les propriétés requises sont prioritaires et les références en conflit doivent être renommées.

une macro de [type NOTIFICATION](notification-type-macro.md) qui contient des références à une macro de [type objet](object-type-macro.md) nommée **Community** provoque un conflit de mappage. Si ce conflit se produit, les propriétés requises sont prioritaires et les références en conflit doivent être renommées.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>         |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>   |
| Espace de noms<br/>                | \\Hôte SNMP \\ racine<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_\_ExtrinsicEvent**](--extrinsicevent.md)
</dt> <dt>

[Macro de TYPE NOTIFICATION](notification-type-macro.md)
</dt> </dl>

 

