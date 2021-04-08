---
description: Représente une relation dans laquelle un élément managé est membre de et est agrégé par une collection.
ms.assetid: 324284fa-ece6-41df-9891-040a7561dce4
title: Classe CIM_MemberOfCollection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MemberOfCollection
- CIM_MemberOfCollection.Collection
- CIM_MemberOfCollection.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9bcebfb08cbbc0cb18e00f1b0e5e2646ca086faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034803"
---
# <a name="cim_memberofcollection-class"></a>\_Classe CIM MemberOfCollection

Représente une relation dans laquelle un élément managé est membre de et est agrégé par une collection.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Aggregation, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Core::Collection"), AMENDMENT]
class CIM_MemberOfCollection
{
  CIM_Collection     REF Collection;
  CIM_ManagedElement REF Member;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ MemberOfCollection** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ MemberOfCollection** possède les propriétés suivantes.

<dl> <dt>

**Collection**
</dt> <dd> <dl> <dt>

Type de données **: \_ collecte CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**agrégat**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Collection qui agrège les membres.

</dd> <dt>

**Membre**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ propriété ManagedElement**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Membre de la collection.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 10 uniquement\]<br/>                                                             |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

