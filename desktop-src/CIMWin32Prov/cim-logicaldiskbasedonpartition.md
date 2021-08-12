---
description: La \_ classe CIM LogicalDiskBasedOnPartition associe un disque logique à la partition de disque sur laquelle il réside.
ms.assetid: 264b62ed-2af2-42dc-9cd2-41b26cc85ca4
ms.tgt_platform: multiple
title: Classe CIM_LogicalDiskBasedOnPartition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDiskBasedOnPartition
- CIM_LogicalDiskBasedOnPartition.EndingAddress
- CIM_LogicalDiskBasedOnPartition.StartingAddress
- CIM_LogicalDiskBasedOnPartition.Dependent
- CIM_LogicalDiskBasedOnPartition.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 27e0805d4fa3a4a59d59423b30b3644e78ccc6138509b2b0f71cdecb435ffc7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118679871"
---
# <a name="cim_logicaldiskbasedonpartition-class"></a>\_Classe CIM LogicalDiskBasedOnPartition

La classe **CIM \_ LogicalDiskBasedOnPartition** associe un disque logique à la partition de disque sur laquelle il réside.

Par exemple, le lecteur C d’un ordinateur peut se trouver sur une partition sur un support physique local, ce qui indique qu’un disque logique ne peut pas s’étendre sur plus d’une partition. Toutefois, lorsqu’un disque logique peut s’étendre sur plusieurs partitions, le disque logique est basé sur une configuration RAID (par exemple, un miroir ou un ensemble entrelacé). Dans ce cas, le disque logique est basé sur le volume de stockage. Pour empêcher l’utilisation incorrecte de l’Association **CIM \_ LogicalDiskBasedOnPartition** , le qualificateur **Max (1)** a été placé sur la référence **Antecedent** à la partition de disque.

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract, UUID("{8502C53F-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_LogicalDiskBasedOnPartition : CIM_BasedOn
{
  uint64                EndingAddress;
  uint64                StartingAddress;
  CIM_LogicalDisk   REF Dependent;
  CIM_DiskPartition REF Antecedent;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ LogicalDiskBasedOnPartition** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ LogicalDiskBasedOnPartition** possède les propriétés suivantes.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ DiskPartition**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

[**\_ DiskPartition CIM**](cim-diskpartition.md) qui décrit la partition de disque.

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données **: \_ disque logique CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)
</dt> </dl>

Un disque logique [**CIM \_**](cim-logicaldisk.md) qui décrit le disque logique qui est créé sur la partition.

</dd> <dt>

**EndingAddress**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique la fin de l’étendue de haut niveau dans le stockage de niveau inférieur. Cette propriété est utile lors du mappage d’étendues non contiguës dans un regroupement de niveau supérieur.

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

Cette propriété est héritée de [**CIM \_ BasedOn**](cim-basedon.md).

</dd> <dt>

**De la**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique le début de l’étendue de haut niveau dans le stockage de niveau inférieur.

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

Cette propriété est héritée de [**CIM \_ BasedOn**](cim-basedon.md).

</dd> </dl>

## <a name="remarks"></a>Remarques

La classe **CIM \_ LogicalDiskBasedOnPartition** est dérivée de [**CIM \_ BasedOn**](cim-basedon.md).

WMI n’implémente pas cette classe. Pour les classes dérivées de **CIM \_ LogicalDiskBasedOnPartition**, consultez [classes Win32](win32-provider.md).

Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF. Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Basé sur CIM \_**](cim-basedon.md)
</dt> </dl>

 

