---
description: Classe de base pour tous les événements intrinsèques liés à un espace de noms.
ms.assetid: 168637b1-217e-4b6d-bd07-25127b9e9f6c
ms.tgt_platform: multiple
title: Classe __NamespaceOperationEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NamespaceOperationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: b5293f97eed0716b3add1d5f06513d556355b157d8e594b1f9e55cb8df6ca7ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118320621"
---
# <a name="__namespaceoperationevent-class"></a>\_\_NamespaceOperationEvent, classe

La classe système **\_ \_ NamespaceOperationEvent** est une classe de base pour tous les événements intrinsèques liés à un espace de noms.

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class __NamespaceOperationEvent : __Event
{
  uint8       SECURITY_DESCRIPTOR[];
  __Namespace TargetNamespace;
  uint64      TIME_CREATED;
};
```

## <a name="members"></a>Membres

La classe **\_ \_ NamespaceOperationEvent** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **\_ \_ NamespaceOperationEvent** possède les propriétés suivantes.

<dl> <dt>

**descripteur de sécurité \_**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Descripteur utilisé par le fournisseur d’événements pour déterminer les utilisateurs qui peuvent recevoir l’événement. Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).

</dd> <dt>

**TargetNamespace**
</dt> <dd> <dl> <dt>

Type de données : **\_ \_ espace de noms**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Espace de noms affecté par l’événement. Pour les événements de création, il s’agit de l’espace de noms nouvellement créé. Pour les événements de modification, il s’agit de l’espace de noms modifié. Pour les événements de suppression, il s’agit de l’espace de noms supprimé.

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

La classe **\_ \_ NamespaceOperationEvent** est dérivée de [**\_ \_ Event**](--event.md).

Les instances de cette classe ne sont pas créées. WMI crée des instances de l’une des classes suivantes dérivées de cette classe :

[**\_\_NamespaceCreationEvent**](--namespacecreationevent.md)

[**\_\_NamespaceModificationEvent**](--namespacemodificationevent.md)

[**\_\_NamespaceDeletionEvent**](--namespacedeletionevent.md)

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
</dt> </dl>

 

