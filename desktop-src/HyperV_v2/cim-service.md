---
description: Représente un élément logique qui contient des informations pour représenter et gérer les fonctionnalités fournies par un périphérique ou une fonctionnalité logicielle.
ms.assetid: 0b2312da-433b-43d8-8d21-babab12a5b2c
title: Classe CIM_Service (gestion Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service
- CIM_Service.SystemCreationClassName
- CIM_Service.SystemName
- CIM_Service.CreationClassName
- CIM_Service.Name
- CIM_Service.PrimaryOwnerName
- CIM_Service.PrimaryOwnerContact
- CIM_Service.StartMode
- CIM_Service.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b6ee3c51b6af50d77e94bb0a29bd1c8148cda8f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527195"
---
# <a name="cim_service-class-hyper-v-management"></a>Classe CIM_Service (gestion Hyper-V)

Représente un élément logique qui contient des informations pour représenter et gérer les fonctionnalités fournies par un périphérique ou une fonctionnalité logicielle. Un service est un objet à usage général permettant de configurer et de gérer l’implémentation des fonctionnalités. il ne s’agit pas de la fonctionnalité elle-même.

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract, Version("2.14.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_Service : CIM_EnabledLogicalElement
{
  string  SystemCreationClassName;
  string  SystemName;
  string  CreationClassName;
  string  Name;
  string  PrimaryOwnerName;
  string  PrimaryOwnerContact;
  string  StartMode;
  boolean Started;
};
```

## <a name="members"></a>Membres

La classe de **\_ service CIM** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe de **\_ service CIM** possède ces méthodes.



| Méthode                                           | Description                    |
|:-------------------------------------------------|:-------------------------------|
| [**StartService**](cim-service-startservice.md) | démarre le service.<br/> |
| [**StopService**](cim-service-stopservice.md)   | arrête le service.<br/>  |



 

### <a name="properties"></a>Propriétés

La classe de **\_ service CIM** possède ces propriétés.

<dl> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nom de classe utilisé pour créer une instance de cette classe. **CreationClassName** est combiné avec d’autres propriétés de clé de cette classe pour identifier de manière unique les instances de cette classe et de ses sous-classes.

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) ("nom"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Identificateur unique du service qui indique les fonctionnalités du service.

</dd> <dt>

**PrimaryOwnerContact**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informations générales sur DMTF \| 001,4»)
</dt> </dl>

Informations de contact pour le propriétaire principal du service.

</dd> <dt>

**PrimaryOwnerName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informations générales sur DMTF \| 001,3»)
</dt> </dl>

Nom du propriétaire principal du service.

</dd> <dt>

**Cours**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

**true** si le service a été démarré ; Sinon, **false**.

</dd> <dt>

**StartMode**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**\_ service CIM**.**EnabledDefault**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)
</dt> </dl>

Cette propriété est déconseillée. Utilisez plutôt la propriété **EnabledDefault** héritée de [**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md).

> [!Note]  
> Description déconseillée : indique si le service est démarré automatiquement (par exemple, par un système d’exploitation) ou s’il est démarré uniquement à la demande.

 

<dt>



 (« Automatique »)


</dt> <dd></dd> <dt>



 (« Manuel »)


</dt> <dd></dd> </dl>

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagée**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ système CIM**](cim-system.md).**CreationClassName**»)
</dt> </dl>

Nom de la classe utilisé pour créer une instance du système qui contient le service. **SystemCreationClassName** est combiné avec d’autres propriétés de clé de cette classe pour identifier de manière unique les instances de cette classe et de ses sous-classes.

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagée**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ système CIM**](cim-system.md).**Name**»)
</dt> </dl>

Nom du système d’étendue.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                                    |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_ENABLEDLOGICALELEMENT CIM**](cim-enabledlogicalelement.md)
</dt> </dl>

 

