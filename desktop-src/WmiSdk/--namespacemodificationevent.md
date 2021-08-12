---
description: Signale un événement de modification d’espace de noms, qui est un type d’événement intrinsèque qui est généré lors de la modification d’un espace de noms.
ms.assetid: 168505d7-4677-4f41-935e-149f22de2cb5
ms.tgt_platform: multiple
title: Classe __NamespaceModificationEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NamespaceModificationEvent
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 3243afe0a8cae34e83ad85e2d89a3becab8d07775ba3ec0c3283fd4ea8ed8bbc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118557812"
---
# <a name="__namespacemodificationevent-class"></a>\_\_NamespaceModificationEvent, classe

La classe système **\_ \_ NamespaceModificationEvent** signale un événement de modification d’espace de noms, qui est un type d' [événement intrinsèque](determining-the-type-of-event-to-receive.md) qui est généré lors de la modification d’un espace de noms.

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class __NamespaceModificationEvent : __NamespaceOperationEvent
{
  uint8       SECURITY_DESCRIPTOR[];
  __Namespace PreviousNamespace;
  uint8       SECURITY_DESCRIPTOR [];
  __Namespace TargetNamespace;
  uint64      TIME_CREATED;
};
```

## <a name="members"></a>Membres

La classe **\_ \_ NamespaceModificationEvent** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **\_ \_ NamespaceModificationEvent** possède les propriétés suivantes.

<dl> <dt>

**PreviousNamespace**
</dt> <dd> <dl> <dt>

Type de données : **\_ \_ espace de noms**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Copie de la version d’origine d’une instance d' [**\_ \_ espace de noms**](--namespace.md) . La propriété **Name** de cette instance identifie l’espace de noms modifié.

</dd> <dt>

**descripteur de sécurité \_**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Descripteur utilisé par le fournisseur d’événements pour déterminer les utilisateurs qui peuvent recevoir l’événement. Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).

</dd> <dt>

**descripteur de sécurité \_** 
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Descripteur utilisé par le fournisseur d’événements pour déterminer les utilisateurs qui peuvent recevoir un événement. Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).

> [!Note]  
> Une liste de contrôle d’accès (ACL) **null** dans le [**\_ descripteur de sécurité**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) accorde un accès illimité à tout le monde en permanence. Pour plus d’informations, consultez [création d’un descripteur de sécurité pour un nouvel objet](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).

 

</dd> <dt>

**TargetNamespace**
</dt> <dd> <dl> <dt>

Type de données : **\_ \_ espace de noms**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Copie de l’instance de l' [**\_ \_ espace de noms**](--namespace.md) qui est modifiée. La propriété **Name** de l’instance d' **\_ \_ espace de noms** indique l’espace de noms modifié. Cette propriété est héritée de la classe [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md).

</dd> <dt>

**HEURE de \_ création**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Valeur unique qui indique l’heure à laquelle un événement est généré. Il s’agit d’une valeur 64 bits qui représente le nombre d’intervalles de 100 nanosecondes après le 1er janvier 1601. Les informations sont au format de temps universel coordonné (UTC, Coordinated Universal Time). Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> </dl>

## <a name="remarks"></a>Remarques

La classe **\_ \_ NamespaceModificationEvent** est dérivée de [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md).

Les seules différences entre l’espace de noms cible et l’espace de noms précédent sont les qualificateurs et les propriétés, à l’exception de [**Name**](--namespace.md).

Notez que la propriété [**Name**](--namespace.md) d’une instance d' **\_ \_ espace de noms** ne peut pas changer car les espaces de noms ne peuvent pas être renommés. Pour modifier le nom d’un espace de noms, l’instance d' **\_ \_ espace de noms** doit être supprimée et recréée avec un nouveau nom. Par conséquent, les événements de modification d’espace de noms sont générés lorsqu’une modification est apportée à des qualificateurs et des propriétés autres que **Name**. Un événement de modification d’espace de noms n’est pas généré lorsqu’un type de modification se produit dans l’espace de noms. Un événement de modification d’espace de noms est généré uniquement lors de la modification d’une instance d’espace de noms.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |
| Espace de noms<br/>                | Tous les espaces de noms WMI<br/>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_\_NamespaceOperationEvent**](/windows/desktop/WmiSdk/--namespaceoperationevent)
</dt> <dt>

[Classes système WMI](wmi-system-classes.md)
</dt> </dl>

 

