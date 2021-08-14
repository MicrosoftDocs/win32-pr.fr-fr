---
description: Sert de classe de base pour tous les événements intrinsèques liés à une instance.
ms.assetid: f6d2b6e5-0dca-4cb5-95a5-33b45cd76807
ms.tgt_platform: multiple
title: Classe __InstanceOperationEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceOperationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: a4e988f26b64d0d8bd4a23f853b7bf9dc92f2610936239b4363439d5c7d70170
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118320806"
---
# <a name="__instanceoperationevent-class"></a>\_\_InstanceOperationEvent, classe

La classe système **\_ \_ InstanceOperationEvent** sert de classe de base pour tous les événements intrinsèques liés à une instance.

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class __InstanceOperationEvent : __Event
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetInstance;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>Membres

La classe **\_ \_ InstanceOperationEvent** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **\_ \_ InstanceOperationEvent** possède les propriétés suivantes.

<dl> <dt>

**descripteur de sécurité \_**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Descripteur utilisé par le fournisseur d’événements pour déterminer les utilisateurs qui peuvent recevoir l’événement. Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).

</dd> <dt>

**TargetInstance**
</dt> <dd> <dl> <dt>

Type de données : **objet**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Instance affectée par l’événement. Pour les événements de création, il s’agit de l’instance nouvellement créée. Pour les événements de modification, il s’agit de la nouvelle version de l’instance modifiée. Pour les événements de suppression, il s’agit de l’instance supprimée.

</dd> <dt>

**HEURE de \_ création**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Valeur unique qui indique l’heure à laquelle l’événement a été généré. Il s’agit d’une valeur 64 bits qui représente le nombre d’intervalles de 100 nanosecondes après le 1er janvier 1601. Les informations sont au format de temps universel coordonné (UTC). Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> </dl>

## <a name="remarks"></a>Remarques

La classe **\_ \_ InstanceOperationEvent** est dérivée de [**\_ \_ Event**](--event.md).

Les instances de **\_ \_ InstanceOperationEvent** ne sont pas créées ; seules les instances de ses sous-classes sont créées. Les classes suivantes dérivent de **\_ \_ InstanceOperationEvent**:

[**\_\_InstanceCreationEvent**](--instancecreationevent.md)

[**\_\_InstanceModificationEvent**](--instancemodificationevent.md)

[**\_\_InstanceDeletionEvent**](--instancedeletionevent.md)

**Vue d'ensemble**

De même qu’il existe une classe WMI qui représente chaque type de ressource système qui peut être gérée à l’aide de WMI, il existe une classe WMI qui représente chaque type d’événement WMI. Lorsqu’un événement qui peut être surveillé par WMI se produit, une instance de la classe d’événements WMI correspondante est créée. Un événement WMI se produit lorsque cette instance est créée.

Il existe trois types principaux de classes d’événements WMI, qui sont tous dérivés de la classe d' [**\_ \_ événements**](--event.md) WMI : les événements intrinsèques, les événements extrinsèques et les événements de minuterie. Les événements intrinsèques, à leur tour, sont représentés par trois classes distinctes dérivées de la classe d' **\_ \_ événements** : [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md), **\_ \_ InstanceOperationEvent** et [**\_ \_ ClassOperationEvent**](--classoperationevent.md).

Événements intrinsèques

Les événements intrinsèques permettent de surveiller une ressource représentée par une classe dans le référentiel CIM. Chaque ressource est représentée par une instance d’une classe. Cela signifie que la surveillance d’une ressource à l’aide de WMI implique en fait la surveillance des instances qui correspondent à la ressource.

Vous pouvez également utiliser des événements intrinsèques pour surveiller les modifications apportées à un espace de noms ou à une classe dans le référentiel. Toutefois, l’analyse des modifications apportées aux espaces de noms ou aux classes est une valeur limitée pour les administrateurs système.

Un événement intrinsèque est représenté par une instance d’une classe dérivée de \_ \_ InstanceOperationEvent, \_ \_ NamespaceOperationEvent ou \_ \_ ClassOperationEvent. Toutes les modifications apportées aux instances dans WMI sont représentées par la \_ \_ classe InstanceOperationEvent et les classes dérivées de celle-ci : \_ \_ InstanceCreationEvent, \_ \_ InstanceModificationEvent et \_ \_ InstanceDeletionEvent.

La surveillance des ressources à l’aide de WMI implique l’analyse des instances et toutes les modifications apportées aux instances sont représentées par \_ \_ InstanceOperationEvent et les classes qui en sont dérivées. Cela signifie que les ressources d’analyse impliquent en fin de la surveillance des instances de \_ \_ classes dérivées de InstanceOperationEvent.

Vous inscrivez un intérêt pour les instances de l’une de ces classes en émettant une requête de notification exprimée dans WQL. La requête utilise une syntaxe similaire à ce qui suit :

`SELECT * FROM __InstanceOperationEventOrDerivedClass WITHIN PollingInterval WHERE TargetInstance ISA WMIClassName AND TargetInstance.WMIClassPropertyName = Value`

Pour plus d’informations sur l’utilisation des événements d’instance WMI pour surveiller l’activité des ordinateurs, consultez [Comment puis-je surveiller les différents types d’événements avec un seul script ?](https://blogs.technet.com/b/heyscriptingguy/archive/2005/04/04/how-can-i-monitor-for-different-types-of-events-with-just-one-script.aspx)

## <a name="examples"></a>Exemples

L’exemple de code VBScript d' [événement de processus Monitor](https://Gallery.TechNet.Microsoft.Com/94c7dc4c-813a-411d-aa3f-f98982cd2a2f) sur la Galerie TechNet utilise **\_ \_ InstanceOperationEvent** pour surveiller le premier événement d’instance WMI pour le [**\_ processus Win32**](/windows/desktop/CIMWin32Prov/win32-process).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |
| Espace de noms<br/>                | Tous les espaces de noms WMI<br/>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_\_Événement**](/windows/desktop/WmiSdk/--event)
</dt> <dt>

[Classes système WMI](wmi-system-classes.md)
</dt> <dt>

[Détermination du type d’événement à recevoir](determining-the-type-of-event-to-receive.md)
</dt> <dt>

[Écriture dans un fichier journal basé sur un événement](writing-to-a-log-file-based-on-an-event.md)
</dt> </dl>

 

