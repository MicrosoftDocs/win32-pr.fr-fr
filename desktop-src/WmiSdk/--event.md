---
description: Est une classe de base abstraite qui sert de classe parente pour tous les événements intrinsèques et extrinsèques.
ms.assetid: 4d2e4715-041c-49e9-b948-a148dfe85483
ms.tgt_platform: multiple
title: Classe __Event
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __Event
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: a74abb8a02676ba97ffb7a41df6ee4a3bd7f428d5288e376f85d61927fbb0e06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118821089"
---
# <a name="__event-class"></a>\_\_Event, classe

La classe de système d' **\_ \_ événements** est une classe de base abstraite qui sert de classe parente pour tous les événements intrinsèques et extrinsèques. Tous les nouveaux types d’événements doivent finalement dériver d' **\_ \_ Event**. Les événements intrinsèques dérivent directement de cette classe. Les événements extrinsèques définis par l’utilisateur dérivent d’une sous-classe de cette classe appelée [**\_ \_ ExtrinsicEvent**](--extrinsicevent.md).

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[abstract]
class __Event : __IndicationRelated
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>Membres

La classe d' **\_ \_ événements** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe d' **\_ \_ événements** a ces propriétés.

<dl> <dt>

**descripteur de sécurité \_**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Descripteur utilisé par le fournisseur d’événements pour déterminer les utilisateurs qui peuvent recevoir l’événement. Pour plus d’informations, consultez [constantes de sécurité WMI](wmi-security-constants.md).

</dd> <dt>

**HEURE de \_ création**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Valeur unique qui indique l’heure à laquelle l’événement est généré. Il s’agit d’une valeur 64 bits qui représente le nombre d’intervalles de 100 nanosecondes après le 1er janvier 1601. Les informations sont au format de temps universel coordonné (UTC, Coordinated Universal Time).

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> </dl>

## <a name="remarks"></a>Remarques

La classe d' **\_ \_ événements** est dérivée de [**\_ \_ IndicationRelated**](--indicationrelated.md), qui n’a pas de propriétés.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |
| Espace de noms<br/>                | Tous les espaces de noms WMI<br/>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_\_IndicationRelated**](/windows/desktop/WmiSdk/--indicationrelated)
</dt> <dt>

[Classes système WMI](wmi-system-classes.md)
</dt> <dt>

[Détermination du type d’événement à recevoir](determining-the-type-of-event-to-receive.md)
</dt> <dt>

[**\_\_ClassOperationEvent**](--classoperationevent.md)
</dt> <dt>

[**\_\_InstanceOperationEvent**](--instanceoperationevent.md)
</dt> <dt>

[**\_\_NamespaceOperationEvent**](--namespaceoperationevent.md)
</dt> </dl>

 

