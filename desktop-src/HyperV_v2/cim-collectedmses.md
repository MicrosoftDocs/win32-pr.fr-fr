---
description: Représente une association générique entre une collection d’éléments système managés et les membres de la collection.
ms.assetid: c9e2bbca-67be-41f2-a94c-cf4eaf5f4694
title: Classe CIM_CollectedMSEs (gestion Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectedMSEs
- CIM_CollectedMSEs.Collection
- CIM_CollectedMSEs.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 74486e12eb4b4ee155554db8ba9f6f8774728217ca6d0ac70b5faac11958726a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790529"
---
# <a name="cim_collectedmses-class-hyper-v-management"></a>Classe CIM_CollectedMSEs (gestion Hyper-V)

Représente une association générique entre une collection d’éléments système managés et les membres de la collection.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Aggregation, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Core::Collection"), AMENDMENT]
class CIM_CollectedMSEs : CIM_MemberOfCollection
{
  CIM_CollectionOfMSEs     REF Collection;
  CIM_ManagedSystemElement REF Member;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ CollectedMSEs** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ CollectedMSEs** possède les propriétés suivantes.

<dl> <dt>

**Collection**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ CollectionOfMSEs**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("collection")
</dt> </dl>

Collection.

</dd> <dt>

**Membre**
</dt> <dd> <dl> <dt>

Type de données **: \_ CIM CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")
</dt> </dl>

Membres de la collection.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/>                                                             |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_MEMBEROFCOLLECTION CIM**](cim-memberofcollection.md)
</dt> </dl>

 

