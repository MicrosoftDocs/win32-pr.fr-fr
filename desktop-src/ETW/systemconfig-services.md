---
description: Classe SystemConfig_Services-cette classe est la classe de type d’événement pour les événements de configuration de service.
ms.assetid: 7cba9992-d154-44b8-87d8-b46a8438f607
title: Classe SystemConfig_Services
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_Services
- SystemConfig_Services.ProcessId
- SystemConfig_Services.ServiceState
- SystemConfig_Services.SubProcessTag
- SystemConfig_Services.ServiceName
- SystemConfig_Services.DisplayName
- SystemConfig_Services.ProcessName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 754b0e10c3882911c6e91fc2590c11739c3f7531
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106057"
---
# <a name="systemconfig_services-class"></a>\_Classe de services SystemConfig

Cette classe est la classe de type d’événement pour les événements de configuration de service.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[EventType(15), EventTypeName("Services")]
class SystemConfig_Services : SystemConfig
{
  uint32 ProcessId;
  uint32 ServiceState;
  uint32 SubProcessTag;
  string ServiceName[];
  string DisplayName[];
  string ProcessName[];
};
```

## <a name="members"></a>Membres

La classe **SystemConfig \_ services** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **SystemConfig \_ services** possède ces propriétés.

<dl> <dt>

**DisplayName**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (5), **StringTermination ("NullTerminated")**, **format ("w")**
</dt> </dl>

Nom complet du service. Le nom est conservé dans le gestionnaire de contrôle des services. Toutefois, les comparaisons de noms complets ne respectent jamais pas la casse.

</dd> <dt>

**ProcessId**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (1), **format ("x")**
</dt> </dl>

Identificateur du processus dans lequel le service s’exécute.

</dd> <dt>

**ProcessName**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (6), **StringTermination ("NullTerminated")**, **format ("w")**
</dt> </dl>

Nom du processus dans lequel le service s’exécute.

</dd> <dt>

**FormName**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (4), **StringTermination ("NullTerminated")**, **format ("w")**
</dt> </dl>

Identificateur unique du service. L’identificateur fournit une indication de la fonctionnalité fournie par le service.

</dd> <dt>

**ServiceState**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (2), **format ("x")**
</dt> </dl>

État actuel du service. Pour connaître les valeurs possibles, consultez le membre **dwCurrentState** du **processus d' \_ état \_ du service**.

</dd> <dt>

**SubProcessTag**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (3), **format ("x")**
</dt> </dl>

Identifie le service.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SystemConfig**](systemconfig.md)
</dt> </dl>

 

 




