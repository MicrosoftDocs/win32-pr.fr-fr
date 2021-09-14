---
description: La \_ classe HWConfig LogDisk est la classe de type d’événement pour les événements de configuration de disque logique. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 2b7038fa-2f20-4bb5-bac1-76b272b3421c
title: Classe HWConfig_LogDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig_LogDisk
- HWConfig_LogDisk.DiskNumber
- HWConfig_LogDisk.Pad
- HWConfig_LogDisk.StartOffset
- HWConfig_LogDisk.PartitionSize
api_type:
- NA
api_location: ''
ms.openlocfilehash: dce4faed913d01f76ff23177b2dad42ea74e5c08
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416899"
---
# <a name="hwconfig_logdisk-class"></a>HWConfig \_ LogDisk, classe

La classe **HWConfig \_ LogDisk** est la classe de type d’événement pour les événements de configuration de disque logique.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[EventType(12), EventTypeName("LogDisk")]
class HWConfig_LogDisk : HWConfig
{
  uint32 DiskNumber;
  uint32 Pad;
  uint64 StartOffset;
  uint64 PartitionSize;
};
```

## <a name="members"></a>Membres

La classe **HWConfig \_ LogDisk** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **HWConfig \_ LogDisk** possède les propriétés suivantes.

<dl> <dt>

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

Remplir
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (2)
</dt> </dl>

Réservé.

</dd> <dt>

PartitionSize
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (4)
</dt> </dl>

Taille totale de la partition, en octets.

</dd> <dt>

StartOffset
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (3)
</dt> </dl>

Décalage de départ (en octets) de la partition à partir du début du disque.

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

 

 




