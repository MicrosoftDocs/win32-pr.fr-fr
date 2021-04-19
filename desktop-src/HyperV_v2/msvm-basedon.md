---
description: Association qui décrit comment les extensions de stockage peuvent être assemblées à partir d’extensions de niveau inférieur.
ms.assetid: 8be9bb2c-ef46-454b-bfc3-0398c64d17b7
title: Classe Msvm_BasedOn
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BasedOn
- Msvm_BasedOn.Antecedent
- Msvm_BasedOn.Dependent
- Msvm_BasedOn.StartingAddress
- Msvm_BasedOn.EndingAddress
- Msvm_BasedOn.OrderIndex
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8262ae5e510574bf02630410b584d9df10d64ecf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106537063"
---
# <a name="msvm_basedon-class"></a>MSVM, \_ classe BasedOn

Association qui décrit comment les extensions de stockage peuvent être assemblées à partir d’extensions de niveau inférieur. Par exemple, les ProtectedSpaceExtents sont des parties de PhysicalExtents, tandis que les VolumeSets sont assemblés à partir d’un ou de plusieurs ProtectedSpaceExtents ou physiques. En guise d’autre exemple, CacheMemory peut être défini indépendamment et réalisé dans un PhysicalElement ou peut être basé sur volatile ou NonVolatileStorageExtents.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BasedOn : CIM_BasedOn
{
  CIM_StorageExtent REF Antecedent;
  CIM_StorageExtent REF Dependent;
  uint64                StartingAddress;
  uint64                EndingAddress;
  uint16                OrderIndex;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ BasedOn** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ BasedOn** a ces propriétés.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données : **[ **CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Extension de stockage de niveau inférieur. Cette propriété est héritée de [**CIM \_ BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données : **[ **CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Extension de stockage de niveau supérieur. Cette propriété est héritée de [**CIM \_ BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).

</dd> <dt>

**EndingAddress**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Adresse de fin dans laquelle, dans un stockage de niveau inférieur, l’étendue de niveau supérieur se termine. Cette propriété est utile lors du mappage d’étendues non contiguës dans un regroupement de niveau supérieur. Cette propriété est héritée de [**CIM \_ BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).

</dd> <dt>

**OrderIndex**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

S’il existe une commande pour le basé sur des associations qui décrivent comment une extension de stockage de niveau supérieur est Assemblée, la propriété **OrderIndex** indique cela. Lorsqu’il existe une commande, les instances ayant la même valeur **dépendante** (même extension de niveau supérieur) doivent placer des valeurs uniques dans la propriété **OrderIndex** . La valeur la plus faible implique le premier membre de la collection d’étendues de niveau inférieur, et les valeurs croissantes impliquent des membres successifs de la collection. S’il n’existe aucune relation ordonnée, la valeur zéro doit être spécifiée. Un exemple de l’utilisation de cette propriété consiste à définir un groupe entrelacé RAID-0 de trois disques. Le groupe RAID qui en résulte est une étendue de stockage qui dépend des extensions de stockage qui décrivent chacun des trois disques. Le **OrderIndex** de chaque association entre les étendues de disque et le groupe RAID peut être spécifié comme 1, 2 et 3 pour indiquer l’ordre dans lequel les étendues de disque sont utilisées pour accéder aux données RAID. Cette propriété est héritée de [**CIM \_ BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).

</dd> <dt>

**De la**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

L’adresse de départ où, dans un stockage de niveau inférieur, l’extension de niveau supérieur commence. Cette propriété est héritée de [**CIM \_ BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

