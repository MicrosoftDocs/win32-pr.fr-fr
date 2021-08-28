---
description: 'Classe SystemConfig_V0_PhyDisk : cette classe est la classe de type d’événement pour les événements de configuration de disque physique.'
ms.assetid: 90ca3089-de5c-4e15-8abf-eaab9aafff06
title: Classe SystemConfig_V0_PhyDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_PhyDisk
- SystemConfig_V0_PhyDisk.DiskNumber
- SystemConfig_V0_PhyDisk.BytesPerSector
- SystemConfig_V0_PhyDisk.SectorsPerTrack
- SystemConfig_V0_PhyDisk.TracksPerCylinder
- SystemConfig_V0_PhyDisk.Cylinders
- SystemConfig_V0_PhyDisk.SCSIPort
- SystemConfig_V0_PhyDisk.SCSIPath
- SystemConfig_V0_PhyDisk.SCSITarget
- SystemConfig_V0_PhyDisk.SCSILun
- SystemConfig_V0_PhyDisk.Manufacturer
- SystemConfig_V0_PhyDisk.PartitionCount
- SystemConfig_V0_PhyDisk.WriteCacheEnabled
- SystemConfig_V0_PhyDisk.BootDriveLetter
api_type:
- NA
api_location: ''
ms.openlocfilehash: c18a198934b7234121da02900896d67c39a3ab3c
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880725"
---
# <a name="systemconfig_v0_phydisk-class"></a>\_Classe SystemConfig v0 \_ PhyDisk

Cette classe est la classe de type d’événement pour les événements de configuration de disque physique.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[EventType(11), EventTypeName("PhyDisk")]
class SystemConfig_V0_PhyDisk : SystemConfig_V0
{
  uint32  DiskNumber;
  uint32  BytesPerSector;
  uint32  SectorsPerTrack;
  uint32  TracksPerCylinder;
  uint64  Cylinders;
  uint32  SCSIPort;
  uint32  SCSIPath;
  uint32  SCSITarget;
  uint32  SCSILun;
  char16  Manufacturer[];
  uint32  PartitionCount;
  boolean WriteCacheEnabled;
  char16  BootDriveLetter[];
};
```

## <a name="members"></a>Membres

La classe **SystemConfig \_ v0 \_ PhyDisk** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **SystemConfig \_ v0 \_ PhyDisk** possède ces propriétés.

<dl> <dt>

**BootDriveLetter**
</dt> <dd> <dl> <dt>

Type de données : tableau **char16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (13), **Max** (3)
</dt> </dl>

Lettre de lecteur du lecteur de démarrage sous la forme « &lt; letter &gt; : ».

</dd> <dt>

**BytesPerSector**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (2)
</dt> </dl>

Nombre d’octets dans chaque secteur pour le lecteur de disque physique.

</dd> <dt>

**Cylindres**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (5)
</dt> </dl>

Nombre total de cylindres sur le lecteur de disque physique. Remarque : la valeur de cette propriété est obtenue via des fonctions étendues de l’interruption du BIOS 13h. La valeur peut être incorrecte si le lecteur utilise un schéma de traduction pour prendre en charge des tailles de disque à grande capacité. Consultez le fabricant pour obtenir des spécifications précises sur les lecteurs.

</dd> <dt>

**DiskNumber**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (1)
</dt> </dl>

Numéro d’index du disque contenant cette partition.

</dd> <dt>

**Fabricant**
</dt> <dd> <dl> <dt>

Type de données : tableau **char16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (10), **Max** (256)
</dt> </dl>

Nom du fabricant du lecteur de disque.

</dd> <dt>

**PartitionCount**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (11)
</dt> </dl>

Nombre de partitions sur ce lecteur de disque physique qui sont reconnues par le système d’exploitation.

</dd> <dt>

**SCSILun**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (9)
</dt> </dl>

Numéro d’unité logique (LUN) SCSI de la carte SCSI.

</dd> <dt>

**SCSIPath**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (7)
</dt> </dl>

Numéro de bus SCSI de la carte SCSI.

</dd> <dt>

**SCSIPort**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (6)
</dt> </dl>

Numéro SCSI de la carte SCSI.

</dd> <dt>

**SCSITarget**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (8)
</dt> </dl>

Contient le numéro de l’appareil cible.

</dd> <dt>

**SectorsPerTrack**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (3)
</dt> </dl>

Nombre de secteurs dans chaque piste pour ce lecteur de disque physique.

</dd> <dt>

**TracksPerCylinder**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (4)
</dt> </dl>

Nombre de pistes dans chaque cylindre sur le lecteur de disque physique. Remarque : la valeur de cette propriété est obtenue via des fonctions étendues de l’interruption du BIOS 13h. La valeur peut être incorrecte si le lecteur utilise un schéma de traduction pour prendre en charge des tailles de disque à grande capacité. Consultez le fabricant pour obtenir des spécifications précises sur les lecteurs.

</dd> <dt>

**WriteCacheEnabled**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (12)
</dt> </dl>

True si le cache d’écriture est activé.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                            |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SystemConfig \_ v0**](systemconfig-v0.md)
</dt> </dl>

 

 




