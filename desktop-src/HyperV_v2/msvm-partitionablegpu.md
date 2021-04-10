---
description: Représente un GPU partitionné. Chaque GPU peut être divisé en plusieurs partitions GPU, qui peuvent être attribuées à un ordinateur virtuel en tant que processeur graphique virtuel.
ms.assetid: a32dfc03-6967-4fa3-ae32-bf074137740b
title: Classe Msvm_PartitionableGpu
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PartitionableGpu
- Msvm_PartitionableGpu.ValidPartitionCounts
- Msvm_PartitionableGpu.PartitionCount
- Msvm_PartitionableGpu.TotalVRAM
- Msvm_PartitionableGpu.AvailableVRAM
- Msvm_PartitionableGpu.MinPartitionVRAM
- Msvm_PartitionableGpu.MaxPartitionVRAM
- Msvm_PartitionableGpu.OptimalPartitionVRAM
- Msvm_PartitionableGpu.TotalEncode
- Msvm_PartitionableGpu.AvailableEncode
- Msvm_PartitionableGpu.MinPartitionEncode
- Msvm_PartitionableGpu.MaxPartitionEncode
- Msvm_PartitionableGpu.OptimalPartitionEncode
- Msvm_PartitionableGpu.TotalDecode
- Msvm_PartitionableGpu.AvailableDecode
- Msvm_PartitionableGpu.MinPartitionDecode
- Msvm_PartitionableGpu.MaxPartitionDecode
- Msvm_PartitionableGpu.OptimalPartitionDecode
- Msvm_PartitionableGpu.TotalCompute
- Msvm_PartitionableGpu.AvailableCompute
- Msvm_PartitionableGpu.MinPartitionCompute
- Msvm_PartitionableGpu.MaxPartitionCompute
- Msvm_PartitionableGpu.OptimalPartitionCompute
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7f82904608a8e2ee4dfa13942066d57d35d511f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868494"
---
# <a name="msvm_partitionablegpu-class"></a>MSVM \_ PartitionableGpu, classe

Représente un GPU partitionné. Chaque GPU peut être divisé en plusieurs partitions GPU, qui peuvent être attribuées à un ordinateur virtuel en tant que processeur graphique virtuel.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_PartitionableGpu : CIM_ComputerSystem
{
  uint16 ValidPartitionCounts[];
  uint16 PartitionCount;
  uint64 TotalVRAM;
  uint64 AvailableVRAM;
  uint64 MinPartitionVRAM;
  uint64 MaxPartitionVRAM;
  uint64 OptimalPartitionVRAM;
  uint64 TotalEncode;
  uint64 AvailableEncode;
  uint64 MinPartitionEncode;
  uint64 MaxPartitionEncode;
  uint64 OptimalPartitionEncode;
  uint64 TotalDecode;
  uint64 AvailableDecode;
  uint64 MinPartitionDecode;
  uint64 MaxPartitionDecode;
  uint64 OptimalPartitionDecode;
  uint64 TotalCompute;
  uint64 AvailableCompute;
  uint64 MinPartitionCompute;
  uint64 MaxPartitionCompute;
  uint64 OptimalPartitionCompute;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ PartitionableGpu** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ PartitionableGpu** possède les propriétés suivantes.

<dl> <dt>

**AvailableCompute**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Quantité de moteurs de calcul disponibles qui s’affiche dans la partition GPU.

</dd> <dt>

**AvailableDecode**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Quantité de moteurs de décodage disponibles qui apparaîtra dans la partition GPU.

</dd> <dt>

**AvailableEncode**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Quantité de moteurs d’encodage disponibles qui s’affiche dans la partition GPU.

</dd> <dt>

**AvailableVRAM**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Quantité de VRAM disponible qui s’affiche dans la partition GPU.

</dd> <dt>

**MaxPartitionCompute**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Quantité maximale de moteurs de calcul qui s’affichera dans la partition GPU.

</dd> <dt>

**MaxPartitionDecode**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Quantité maximale de moteurs de décodage qui s’affichent dans la partition GPU.

</dd> <dt>

**MaxPartitionEncode**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Quantité maximale de moteurs d’encodage qui s’affiche dans la partition GPU.

</dd> <dt>

**MaxPartitionVRAM**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Quantité maximale de VRAM qui s’affichera dans la partition GPU.

</dd> <dt>

**MinPartitionCompute**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Quantité minimale de moteurs de calcul qui s’affichera dans la partition GPU.

</dd> <dt>

**MinPartitionDecode**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Quantité minimale de moteurs de décodage qui s’affichent dans la partition GPU.

</dd> <dt>

**MinPartitionEncode**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Quantité minimale de moteurs d’encodage qui s’affiche dans la partition GPU.

</dd> <dt>

**MinPartitionVRAM**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Quantité minimale de VRAM qui apparaîtra dans la partition GPU.

</dd> <dt>

**OptimalPartitionCompute**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Quantité optimale de moteurs de calcul qui s’affichera dans la partition GPU.

</dd> <dt>

**OptimalPartitionDecode**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Quantité optimale de moteurs de décodage qui s’affichent dans la partition GPU.

</dd> <dt>

**OptimalPartitionEncode**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Quantité optimale de moteurs d’encodage qui s’affiche dans la partition GPU.

</dd> <dt>

**OptimalPartitionVRAM**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Quantité optimale de VRAM qui apparaîtra dans la partition GPU.

</dd> <dt>

**PartitionCount**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Quantité de partitions GPU dans laquelle le GPU physique est découpé.

</dd> <dt>

**TotalCompute**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Quantité totale de moteurs de calcul qui s’affichera dans la partition GPU.

</dd> <dt>

**TotalDecode**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Quantité totale de moteurs de décodage qui s’affichent dans la partition GPU.

</dd> <dt>

**TotalEncode**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Quantité totale de moteurs d’encodage qui s’affiche dans la partition GPU.

</dd> <dt>

**TotalVRAM**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Quantité totale de VRAM qui s’affichera dans la partition GPU.

</dd> <dt>

**ValidPartitionCounts**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Tableau des options de partition GPU valides dans lesquelles le GPU physique peut être découpé.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 10, version 1703 \[ uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_ComputerSystem CIM**](cim-computersystem.md)
</dt> </dl>

 

 




