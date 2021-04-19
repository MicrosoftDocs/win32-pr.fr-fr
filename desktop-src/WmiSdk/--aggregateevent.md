---
description: Représente un événement d’agrégation de plusieurs événements intrinsèques ou extrinsèques individuels.
ms.assetid: 99afa390-01fe-4a13-ba21-27587470f111
ms.tgt_platform: multiple
title: Classe __AggregateEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __AggregateEvent
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: f93a962e57452ac555214e42f00af8ac8a4ea3db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534734"
---
# <a name="__aggregateevent-class"></a>\_\_AggregateEvent, classe

La classe système **\_ \_ AggregateEvent** représente un événement d’agrégation de plusieurs événements intrinsèques ou extrinsèques individuels. WMI génère une instance de **\_ \_ AggregateEvent** au lieu d’un [**\_ \_ événement**](--event.md) lorsque les consommateurs s’inscrivent auprès de la clause [Group within](group-clause.md) dans leur requête d’événement.

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class __AggregateEvent : __IndicationRelated
{
  uint32 NumberOfEvents;
  object Representative;
};
```

## <a name="members"></a>Membres

La classe **\_ \_ AggregateEvent** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **\_ \_ AggregateEvent** possède les propriétés suivantes.

<dl> <dt>

**NumberOfEvents**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre d’événements combinés pour produire cet événement de résumé unique.

</dd> <dt>

**Representative**
</dt> <dd> <dl> <dt>

Type de données : **objet**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Copie de l’un des événements remis dans l’intervalle d’agrégation. Par exemple, si un consommateur s’est inscrit pour les événements de modification de clé de Registre à partir du fournisseur d’événements du Registre, le **représentant** contiendrait une instance de la classe **RegistryKeyChangeEvent** .

</dd> </dl>

## <a name="remarks"></a>Notes

La classe **\_ \_ AggregateEvent** est dérivée de [**\_ \_ IndicationRelated**](--indicationrelated.md), qui n’a pas de propriétés.

Les fournisseurs d’événements ne génèrent jamais d’événements d’agrégation. Ils doivent ignorer la clause GROUP WITHIN dans le traitement des requêtes d’événements.

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

[Interrogation avec WQL](querying-with-wql.md)
</dt> </dl>

 

