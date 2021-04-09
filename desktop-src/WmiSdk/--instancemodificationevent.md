---
description: Signale un événement de modification d’instance, qui est un type d’événement intrinsèque généré lorsqu’une instance change dans l’espace de noms.
ms.assetid: aa35f349-8b57-435f-bf82-76daf2b43ec9
ms.tgt_platform: multiple
title: Classe __InstanceModificationEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceModificationEvent
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: e644db16b6638bbc87006819e186540a9ce1874e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866905"
---
# <a name="__instancemodificationevent-class"></a>\_\_InstanceModificationEvent, classe

La classe système **\_ \_ InstanceModificationEvent** signale un événement de modification d’instance, qui est un type d' [événement intrinsèque](determining-the-type-of-event-to-receive.md) généré lorsqu’une instance change dans l’espace de noms.

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class __InstanceModificationEvent : __InstanceOperationEvent
{
  object PreviousInstance;
  uint8  SECURITY_DESCRIPTOR[];
  object TargetInstance;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>Membres

La classe **\_ \_ InstanceModificationEvent** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **\_ \_ InstanceModificationEvent** possède les propriétés suivantes.

<dl> <dt>

**PreviousInstance**
</dt> <dd> <dl> <dt>

Type de données : **objet**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Copie de l’instance avant modification.

</dd> <dt>

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

Nouvelle version de l’instance modifiée. Cette propriété est héritée de [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md).

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

## <a name="remarks"></a>Notes

La classe **\_ \_ InstanceModificationEvent** est dérivée de [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md).

**Modification d’une ressource : \_ \_ InstanceModificationEvent**

Supposons que vous soupçonnez qu’une application de gestion que vous utilisez modifie par erreur le type de démarrage d’un service sur l’un de vos serveurs. Vous souhaitez écrire un script WMI pour surveiller toutes les modifications apportées à la configuration du service. Dès qu’une modification est apportée à un service, son TargetInstance correspondant reflète la modification.

Si vous enregistrez votre intérêt dans cet événement, une modification de la configuration du service entraîne la création d’une instance de la classe **\_ \_ InstanceModificationEvent** .

Les requêtes de notification qui demandent la notification de la modification d’une ressource et utilisent des événements intrinsèques utilisent une syntaxe similaire à ce qui suit :

`SELECT * FROM __InstanceModificationEvent WITHIN PollingInterval WHERE TargetInstance ISA 'Win32_Service' and TargetInstance.Name = 'alerter'`

## <a name="examples"></a>Exemples

L’exemple VBScript d' [événement de modification de processus Monitor](https://Gallery.TechNet.Microsoft.Com/daa06cdd-c1d9-4179-ba67-83aef2b9a079) sur la Galerie TechNet utilise **\_ \_ InstanceModificationEvent** pour surveiller la première occurrence d’un événement de modification d’instance WMI pour le [**\_ processus Win32**](/windows/desktop/CIMWin32Prov/win32-process).

## <a name="requirements"></a>Configuration requise



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

 

