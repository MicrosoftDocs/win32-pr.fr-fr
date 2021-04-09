---
description: Représente une association entre un objet CIM StorageExtent de niveau supérieur \_ et un objet CIM StorageExtent de niveau inférieur \_ . Par exemple, un \_ objet CIM ProtectedSpaceExtent fait partie d’un \_ objet CIM PhysicalExtent.
ms.assetid: 40a88927-981b-4fc4-af5f-be91d9933284
title: Classe CIM_BasedOn (gestion Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BasedOn
- CIM_BasedOn.Antecedent
- CIM_BasedOn.Dependent
- CIM_BasedOn.StartingAddress
- CIM_BasedOn.EndingAddress
- CIM_BasedOn.OrderIndex
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 47d2e44d1106eba57f4c46c0957662c348c9ca1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862465"
---
# <a name="cim_basedon-class-hyper-v-management"></a>Classe CIM_BasedOn (gestion Hyper-V)

Représente une association entre un objet **CIM \_ StorageExtent** de niveau supérieur et un objet **CIM \_ StorageExtent** de niveau inférieur. Par exemple, un objet [**CIM \_ ProtectedSpaceExtent**](/windows/desktop/CIMWin32Prov/cim-protectedspaceextent) fait partie d’un objet [**CIM \_ PhysicalExtent**](/windows/desktop/CIMWin32Prov/cim-physicalextent) .

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Core::StorageExtent"), AMENDMENT]
class CIM_BasedOn : CIM_Dependency
{
  CIM_StorageExtent REF Antecedent;
  CIM_StorageExtent REF Dependent;
  uint64                StartingAddress;
  uint64                EndingAddress;
  uint16                OrderIndex;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ basé** sur les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe de type **CIM \_** avec ces propriétés.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ StorageExtent**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Objet **\_ StorageExtent CIM** de niveau inférieur.

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ StorageExtent**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)
</dt> </dl>

Objet **\_ StorageExtent CIM** de niveau supérieur.

</dd> <dt>

**EndingAddress**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Adresse qui indique où se trouve dans le stockage de niveau inférieur, l’objet **CIM \_ StorageExtent** de niveau supérieur se termine. Cette propriété est utile lors du mappage d’objets **\_ StorageExtent CIM** non contigus dans un regroupement de niveau supérieur.

</dd> <dt>

**OrderIndex**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Index utilisé pour spécifier l’ordre des associations de **modèle CIM \_** dans une collection ; sinon, « 0 » n’indique aucun ordre. **CIM \_ Les instances BasedOn** avec la même valeur dépendante doivent placer des valeurs uniques dans la propriété **OrderIndex** . La valeur **OrderIndex** la plus basse spécifie le premier membre de la collection.

Un exemple de l’utilisation de cette propriété consiste à définir un groupe entrelacé RAID-0 de 3 disques. Le groupe RAID qui en résulte est une étendue de stockage qui dépend des extensions de stockage qui décrivent chacun des 3 disques. La valeur **OrderIndex** de chaque **Association \_ CIM** à partir des étendues de disque vers le groupe RAID peut être spécifiée comme 1, 2 et 3 pour indiquer l’ordre dans lequel les étendues de disque sont utilisées pour accéder aux données RAID.

</dd> <dt>

**De la**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Adresse qui indique où se trouve dans le stockage de niveau inférieur, l’objet **CIM \_ StorageExtent** de niveau supérieur commence.

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

[**\_Dépendance CIM**](cim-dependency.md)
</dt> </dl>

 

