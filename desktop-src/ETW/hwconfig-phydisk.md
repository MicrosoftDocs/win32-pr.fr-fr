---
description: La \_ classe HWConfig PhyDisk est la classe de type d’événement pour les événements de configuration de disque physique. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: b134ab45-b161-452f-be84-ccbdfa3fe4af
title: Classe HWConfig_PhyDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig_PhyDisk
- HWConfig_PhyDisk.DiskNumber
- HWConfig_PhyDisk.BytesPerSector
- HWConfig_PhyDisk.SectorsPerTrack
- HWConfig_PhyDisk.TracksPerCylinder
- HWConfig_PhyDisk.Cylinders
- HWConfig_PhyDisk.SCSIPort
- HWConfig_PhyDisk.SCSIPath
- HWConfig_PhyDisk.SCSITarget
- HWConfig_PhyDisk.SCSILun
- HWConfig_PhyDisk.Manufacturer
api_type:
- NA
api_location: ''
ms.openlocfilehash: 453f06ae11bb8b1e11c9efddd6f63bffd38540e7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416896"
---
# <a name="hwconfig_phydisk-class"></a>HWConfig \_ PhyDisk, classe

La classe **HWConfig \_ PhyDisk** est la classe de type d’événement pour les événements de configuration de disque physique.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[EventType(11), EventTypeName("PhyDisk")]
class HWConfig_PhyDisk : HWConfig
{
  uint32 DiskNumber;
  uint32 BytesPerSector;
  uint32 SectorsPerTrack;
  uint32 TracksPerCylinder;
  uint64 Cylinders;
  uint32 SCSIPort;
  uint32 SCSIPath;
  uint32 SCSITarget;
  uint32 SCSILun;
  string Manufacturer;
};
```

## <a name="members"></a>Membres

La classe **HWConfig \_ PhyDisk** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **HWConfig \_ PhyDisk** possède les propriétés suivantes.

<dl> <dt>

BytesPerSector
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (2)
</dt> </dl>

Nombre d’octets dans chaque secteur pour le lecteur de disque physique.

</dd> <dt>

Cylindres
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (5)
</dt> </dl>

Nombre total de cylindres sur le lecteur de disque physique. Remarque : la valeur de cette propriété est obtenue via des fonctions étendues de l’interruption du BIOS 13h. La valeur peut être incorrecte si le lecteur utilise un schéma de traduction pour prendre en charge des tailles de disque à grande capacité. Consultez le fabricant pour obtenir des spécifications précises sur les lecteurs.

</dd> <dt>

DiskNumber
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (1)
</dt> </dl>

Numéro d’index du disque contenant cette partition.

</dd> <dt>

Fabricant
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (10), StringTermination ("NullTerminated"), format ("w")
</dt> </dl>

Nom du fabricant du lecteur de disque.

</dd> <dt>

SCSILun
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (9)
</dt> </dl>

Numéro d’unité logique (LUN) SCSI de la carte SCSI.

</dd> <dt>

SCSIPath
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (7)
</dt> </dl>

Numéro de bus SCSI de la carte SCSI.

</dd> <dt>

SCSIPort
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (6)
</dt> </dl>

Numéro SCSI de la carte SCSI.

</dd> <dt>

SCSITarget
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (8)
</dt> </dl>

Contient le numéro de l’appareil cible.

</dd> <dt>

SectorsPerTrack
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (3)
</dt> </dl>

Nombre de secteurs dans chaque piste pour ce lecteur de disque physique.

</dd> <dt>

TracksPerCylinder
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (4)
</dt> </dl>

Nombre de pistes dans chaque cylindre sur le lecteur de disque physique. Remarque : la valeur de cette propriété est obtenue via des fonctions étendues de l’interruption du BIOS 13h. La valeur peut être incorrecte si le lecteur utilise un schéma de traduction pour prendre en charge des tailles de disque à grande capacité. Consultez le fabricant pour obtenir des spécifications précises sur les lecteurs.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**HWConfig**](hwconfig.md)
</dt> </dl>

 

 




