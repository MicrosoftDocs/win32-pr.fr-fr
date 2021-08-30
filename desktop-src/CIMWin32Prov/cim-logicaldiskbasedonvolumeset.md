---
description: L' \_ Association CIM LogicalDiskBasedOnVolumeSet associe les disques logiques au volume sur lequel ils sont trouvés. Les disques logiques peuvent être basés sur un volume unique (par exemple, exposé par un gestionnaire de volume logiciel) ou sur une partition de disque.
ms.assetid: 15a588c9-a6b0-4393-927f-8e8818315542
ms.tgt_platform: multiple
title: Classe CIM_LogicalDiskBasedOnVolumeSet
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDiskBasedOnVolumeSet
- CIM_LogicalDiskBasedOnVolumeSet.EndingAddress
- CIM_LogicalDiskBasedOnVolumeSet.StartingAddress
- CIM_LogicalDiskBasedOnVolumeSet.Dependent
- CIM_LogicalDiskBasedOnVolumeSet.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 38ecbcf35ed46cb22a254289d617f9086780c087d932ba17a4cbd60bc1782f52
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119923139"
---
# <a name="cim_logicaldiskbasedonvolumeset-class"></a>\_Classe CIM LogicalDiskBasedOnVolumeSet

L’Association **CIM \_ LogicalDiskBasedOnVolumeSet** associe les disques logiques au volume sur lequel ils sont trouvés. Les disques logiques peuvent être basés sur un volume unique (par exemple, exposé par un gestionnaire de volume logiciel) ou sur une partition de disque.

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract, UUID("{3A608798-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_LogicalDiskBasedOnVolumeSet : CIM_BasedOn
{
  uint64              EndingAddress;
  uint64              StartingAddress;
  CIM_LogicalDisk REF Dependent;
  CIM_VolumeSet   REF Antecedent;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ LogicalDiskBasedOnVolumeSet** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ LogicalDiskBasedOnVolumeSet** possède les propriétés suivantes.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ VolumeSet**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Antecedent »)
</dt> </dl>

[**\_ VolumeSet CIM**](cim-volumeset.md) qui décrit l’ensemble de volumes.

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données **: \_ disque logique CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)
</dt> </dl>

Un disque logique [**CIM \_**](cim-logicaldisk.md) qui décrit le disque logique qui est créé sur le jeu de volumes.

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

La classe **CIM \_ LogicalDiskBasedOnVolumeSet** est dérivée de [**CIM \_ BasedOn**](cim-basedon.md).

WMI n’implémente pas cette classe.

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

 

