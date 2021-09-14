---
description: Signale un événement de création d’instance, qui est un type d’événement intrinsèque qui est généré quand une nouvelle instance est ajoutée à l’espace de noms.
ms.assetid: 41976479-70e3-4914-a56a-fa94a1fd31c7
ms.tgt_platform: multiple
title: Classe __InstanceCreationEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceCreationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 29bdefbe1db20cd8b55b74433061b6c0cf152378
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127124517"
---
# <a name="__instancecreationevent-class"></a>\_\_InstanceCreationEvent, classe

La classe système **\_ \_ InstanceCreationEvent** signale un événement de création d’instance, qui est un type d' [événement intrinsèque](determining-the-type-of-event-to-receive.md) qui est généré quand une nouvelle instance est ajoutée à l’espace de noms.

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class __InstanceCreationEvent : __InstanceOperationEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetInstance;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>Membres

La classe **\_ \_ InstanceCreationEvent** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **\_ \_ InstanceCreationEvent** possède les propriétés suivantes.

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

Copie de l’instance qui a été créée. Cette propriété est héritée de [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md).

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

La classe **\_ \_ InstanceCreationEvent** est dérivée de [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md).

**Création d’une ressource : \_ \_ InstanceCreationEvent**

supposons que vous soyez intéressé par la réception d’une notification si Bloc-notes est exécuté sur un ordinateur donné. lorsque Bloc-notes s’exécute, un processus correspondant est créé. Les processus peuvent être gérés à l’aide de WMI et sont représentés par la \_ classe de processus Win32. lorsque Bloc-notes commence à s’exécuter, une instance correspondante de la \_ classe de processus Win32 devient disponible via WMI. Si vous avez enregistré votre intérêt dans cet événement (en émettant la requête de notification d’événement appropriée), la disponibilité de cette instance entraîne la création d’une instance de la classe **\_ \_ InstanceCreationEvent** .

Les requêtes de notification qui demandent la notification de la création d’une ressource et utilisent des événements intrinsèques utilisent une syntaxe similaire à ce qui suit :

`SELECT * FROM __InstanceCreationEvent WITHIN PollingInterval WHERE TargetInstance ISA 'Win32_Process' and TargetInstance.Name = 'notepad.exe'`

Pour plus d’informations sur l’utilisation de **\_ \_ InstanceCreationEvent** comme moyen de surveiller les systèmes de fichiers, consultez [WMI et surveillance du système de fichiers](https://www.codeproject.com/Articles/42212/WMI-and-File-System-Monitoring) sur CodeProject.

## <a name="examples"></a>Exemples

L’exemple de création d’un [événement WMI permanent pour surveiller les fichiers](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) PowerShell sur la Galerie TechNet utilise **\_ \_ InstanceCreationEvent** dans le cadre d’un script complexe pour configurer une inscription d’événement WMI permanente.

L’exemple PowerShell d' [événements permanents WMI PowerShell](https://Gallery.TechNet.Microsoft.Com/PowerShell-WMI-Permanent-7e17f262) sur la Galerie TechNet utilise **\_ \_ InstanceCreationEvent** dans le cadre d’un script de démonstration pour la configuration d’une inscription d’événement permanent.

L’exemple VBScript d' [événement de création de processus Monitor](https://Gallery.TechNet.Microsoft.Com/6f137d9e-f00a-4f0a-ad07-7d752ff5251d) sur TechNet utilise **\_ \_ InstanceCreationEvent** pour surveiller le premier événement de création d’instance WMI pour le [**\_ processus Win32**](/windows/desktop/CIMWin32Prov/win32-process).

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

 

