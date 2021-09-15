---
description: Signale un événement de suppression d’instance, qui est un type d’événement intrinsèque généré lorsqu’une instance est supprimée de l’espace de noms.
ms.assetid: a370fc95-15e3-49c3-98de-2f40d742f207
ms.tgt_platform: multiple
title: Classe __InstanceDeletionEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceDeletionEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 018bac665aa95393fc1a9c7e51ad42038e8b27c3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404104"
---
# <a name="__instancedeletionevent-class"></a>\_\_InstanceDeletionEvent, classe

La classe système **\_ \_ InstanceDeletionEvent** signale un événement de suppression d’instance, qui est un type d' [événement intrinsèque](determining-the-type-of-event-to-receive.md) généré lorsqu’une instance est supprimée de l’espace de noms.

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class __InstanceDeletionEvent : __InstanceOperationEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetInstance;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>Membres

La classe **\_ \_ InstanceDeletionEvent** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **\_ \_ InstanceDeletionEvent** possède les propriétés suivantes.

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

Copie de l’instance qui a été supprimée. Cette propriété est héritée de [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md).

</dd> <dt>

**HEURE de \_ création**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Valeur unique qui indique l’heure à laquelle l’événement a été généré. Il s’agit d’une valeur 64 bits qui représente le nombre d’intervalles de 100 nanosecondes après le 1er janvier 1601. Les informations sont au format de temps universel coordonné (UTC, Coordinated Universal Time). Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> </dl>

## <a name="remarks"></a>Notes

La classe **\_ \_ InstanceDeletionEvent** est dérivée de [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md).

**Suppression d’une ressource : \_ \_ InstanceDeletionEvent**

Si vous souhaitez vous assurer qu’un programme antivirus spécifique continue à s’exécuter sur un ordinateur, vous pouvez écrire un script qui surveille les processus sur l’ordinateur pour déterminer s’ils arrêtent.

Les requêtes de notification qui demandent la notification de la suppression d’une ressource et utilisent des événements intrinsèques utilisent une syntaxe similaire à ce qui suit :

`SELECT * FROM __InstanceDeletionEvent WHERE TargetInstance ISA 'Win32_Process' and TargetInstance.Name = 'notepad.exe' `

## <a name="examples"></a>Exemples

L’exemple de code VBScript de l' [événement analyser le processus de suppression](https://Gallery.TechNet.Microsoft.Com/060a9adb-f99b-4f34-ba65-19b5f5815a38) dans la Galerie TechNet utilise **\_ \_ InstanceDeletionEvent** pour surveiller la première occurrence d’un événement de suppression d’instance WMI pour le [**\_ processus Win32**](/windows/desktop/CIMWin32Prov/win32-process).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |
| Espace de noms<br/>                | Tous les espaces de noms WMI<br/>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_\_InstanceOperationEvent**](/windows/desktop/WmiSdk/--instanceoperationevent)
</dt> <dt>

[Classes système WMI](wmi-system-classes.md)
</dt> </dl>

 

