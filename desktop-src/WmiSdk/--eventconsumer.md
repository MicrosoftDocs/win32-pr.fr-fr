---
description: Est une classe de base abstraite utilisée pour l’inscription d’un consommateur d’événements permanent.
ms.assetid: c1dc9a91-76f9-4527-ad69-0323a9aef28a
ms.tgt_platform: multiple
title: Classe __EventConsumer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventConsumer
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: ba84549f1120f4f6d2045e9e9c999e56c38dd285e2ab25de5da1e1b12401f345
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120949"
---
# <a name="__eventconsumer-class"></a>\_\_EventConsumer, classe

La classe système **\_ \_ EventConsumer** est une classe de base abstraite utilisée pour l’inscription d’un consommateur d’événements permanent. Vous pouvez dériver une nouvelle classe de consommateur d’événements à partir de **\_ \_ EventConsumer**.

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[abstract]
class __EventConsumer : __IndicationRelated
{
  uint8  CreatorSID[];
  string MachineName;
  uint32 MaximumQueueSize;
};
```

## <a name="members"></a>Membres

La classe **\_ \_ EventConsumer** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **\_ \_ EventConsumer** possède les propriétés suivantes.

<dl> <dt>

**CreatorSID**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Identificateur de sécurité (SID) qui identifie de façon unique l’utilisateur qui crée un filtre. WMI stocke le SID de l’utilisateur qui crée une instance de **\_ \_ EventConsumer** ou le SID d’administrateur, selon le système d’exploitation. Pour plus d’informations, consultez [liaison d’un filtre d’événements avec un consommateur logique](binding-an-event-filter-with-a-logical-consumer.md) et [surveillance et réponse aux événements avec des consommateurs standard](monitoring-and-responding-to-events-with-standard-consumers.md).

</dd> <dt>

**MachineName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

nom de l’ordinateur sur lequel Windows Management Instrumentation (WMI) envoie des événements.

</dd> <dt>

**MaximumQueueSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

File d’attente maximale pour un consommateur spécifique, en octets.

</dd> </dl>

## <a name="remarks"></a>Remarques

La classe **\_ \_ EventConsumer** est dérivée de [**\_ \_ IndicationRelated**](--indicationrelated.md), qui n’a pas de propriétés.

Les consommateurs permanents définissent de nouvelles classes de consommateurs pour décrire une action à entreprendre et les données à traiter lorsque les consommateurs reçoivent des notifications d’événements. Les consommateurs permanents ont des problèmes de sécurité particuliers. Pour plus d’informations, consultez [sécurisation des événements WMI](securing-wmi-events.md).

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

[Réception d’événements à tout moment](receiving-events-at-all-times.md)
</dt> <dt>

[Création d’une classe de consommateur d’événements permanente](creating-a-new-permanent-event-consumer-class.md)
</dt> <dt>

[Création d’un consommateur logique](creating-a-logical-consumer.md)
</dt> <dt>

[Sécurisation des événements WMI](securing-wmi-events.md)
</dt> </dl>

 

