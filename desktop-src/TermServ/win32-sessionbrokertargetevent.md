---
title: Classe Win32_SessionBrokerTargetEvent
description: Représente une modification apportée à une cible session Broker.
ms.assetid: ee3ae0ed-eb8b-4777-9b9e-0e50722cf52a
ms.tgt_platform: multiple
keywords:
- Win32_SessionBrokerTargetEvent de la classe Services Bureau à distance
- Win32_SessionBrokerTargetEvent de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_SessionBrokerTargetEvent
- Win32_SessionBrokerTargetEvent.SECURITY_DESCRIPTOR
- Win32_SessionBrokerTargetEvent.TIME_CREATED
- Win32_SessionBrokerTargetEvent.ChangeType
- Win32_SessionBrokerTargetEvent.PluginName
- Win32_SessionBrokerTargetEvent.TargetName
- Win32_SessionBrokerTargetEvent.FarmName
- Win32_SessionBrokerTargetEvent.Guid
- Win32_SessionBrokerTargetEvent.Environment
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d7f1cf6aab1c4497ce85cb93318c9ca79368853
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740701"
---
# <a name="win32_sessionbrokertargetevent-class"></a>\_Classe SessionBrokerTargetEvent Win32

Représente une modification apportée à une cible session Broker.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[AMENDMENT]
class Win32_SessionBrokerTargetEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  uint32 ChangeType;
  string PluginName;
  string TargetName;
  string FarmName;
  string Guid;
  string Environment;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ SessionBrokerTargetEvent** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ SessionBrokerTargetEvent** a ces propriétés.

<dl> <dt>

**ChangeType**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie la modification qui s’est produite. Il peut s’agir de l’une des valeurs suivantes.

<dt>

1 (0x1)
</dt> <dd>

Le type de modification n’est pas spécifié.

</dd> <dt>

2 (0X2)
</dt> <dd>

L’adresse IP externe a changé.

</dd> <dt>

4 (0x4)
</dt> <dd>

L’adresse IP interne a changé.

</dd> <dt>

8 (0x8)
</dt> <dd>

La cible a été jointe.

</dd> <dt>

16 (0x10)
</dt> <dd>

La cible a été supprimée.

</dd> <dt>

32 (0x20)
</dt> <dd>

L’état de la cible a changé.

</dd> <dt>

64 (0x40)
</dt> <dd>

La cible est inactive.

</dd> </dl>

</dd> <dt>

**Environment**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom d'environnement. Dans le cas d’une machine virtuelle (VM) cible, il peut s’agir du nom d’hôte de la machine virtuelle.

**Windows Server 2008 R2 :** Cette propriété n’est pas disponible avant Windows Server 2012

</dd> <dt>

**FarmName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de la batterie à laquelle la cible appartient.

**Windows Server 2008 R2 :** Cette propriété n’est pas disponible avant Windows Server 2012

</dd> <dt>

**Uniques**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

GUID de la cible.

**Windows Server 2008 R2 :** Cette propriété n’est pas disponible avant Windows Server 2012

</dd> <dt>

**PluginName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom du plug-in.

**Windows Server 2008 R2 :** Cette propriété n’est pas disponible avant Windows Server 2012

</dd> <dt>

**descripteur de sécurité \_**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Descripteur utilisé par le fournisseur d’événements pour déterminer les utilisateurs qui peuvent recevoir l’événement. Cette propriété est héritée de l' [**\_ \_ événement**](/windows/desktop/WmiSdk/--event). Pour plus d’informations sur les constantes utilisées pour définir ce descripteur de sécurité, voir la rubrique sur les [constantes de sécurité WMI](/windows/desktop/WmiSdk/wmi-security-constants).

</dd> <dt>

**TargetName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de la cible.

**Windows Server 2008 R2 :** Cette propriété n’est pas disponible avant Windows Server 2012

</dd> <dt>

**HEURE de \_ création**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Valeur unique qui indique l’heure à laquelle l’événement a été généré. Il s’agit d’une valeur 64 bits qui représente le nombre d’intervalles de 100 nanosecondes après le 1er janvier 1601. Les informations sont au format de temps universel coordonné (UTC). Cette propriété est héritée de l' [**\_ \_ événement**](/windows/desktop/WmiSdk/--event).

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2<br/>                                                      |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



 

