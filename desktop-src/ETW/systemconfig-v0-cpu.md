---
description: Classe SystemConfig_V0_CPU-cette classe est la classe de type d’événement pour les événements de configuration de l’UC.
ms.assetid: 9ca77676-ff0e-4c47-ae4e-f8192376d3ca
title: Classe SystemConfig_V0_CPU
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_CPU
- SystemConfig_V0_CPU.MHz
- SystemConfig_V0_CPU.NumberOfProcessors
- SystemConfig_V0_CPU.MemSize
- SystemConfig_V0_CPU.PageSize
- SystemConfig_V0_CPU.AllocationGranularity
- SystemConfig_V0_CPU.ComputerName
- SystemConfig_V0_CPU.DomainName
api_type:
- NA
api_location: ''
ms.openlocfilehash: d533eb06aca34ffdb5996bb0c08c7d40645042e7ccab7645cfd3a04adf0db2ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069659"
---
# <a name="systemconfig_v0_cpu-class"></a>\_Classe de \_ processeur SystemConfig v0

Cette classe est la classe de type d’événement pour les événements de configuration de l’UC.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[EventType(10), EventTypeName("CPU")]
class SystemConfig_V0_CPU : SystemConfig_V0
{
  uint32 MHz;
  uint32 NumberOfProcessors;
  uint32 MemSize;
  uint32 PageSize;
  uint32 AllocationGranularity;
  char16 ComputerName[];
  char16 DomainName[];
};
```

## <a name="members"></a>Membres

La classe d' **\_ \_ UC SystemConfig v0** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe d' **\_ \_ UC SystemConfig v0** a ces propriétés.

<dl> <dt>

**AllocationGranularity**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (5)
</dt> </dl>

Granularité avec laquelle la mémoire virtuelle est allouée.

</dd> <dt>

**ComputerName**
</dt> <dd> <dl> <dt>

Type de données : tableau **char16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (6), **Max** (256)
</dt> </dl>

Nom de l’ordinateur.

</dd> <dt>

**DomainName**
</dt> <dd> <dl> <dt>

Type de données : tableau **char16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (7), **Max** (132)
</dt> </dl>

Nom du domaine dans lequel l’ordinateur est membre.

</dd> <dt>

**MemS**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (3)
</dt> </dl>

Quantité totale de mémoire physique disponible pour le système d’exploitation.

</dd> <dt>

**MHz**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (1)
</dt> </dl>

Vitesse maximale du processeur, en mégahertz.

</dd> <dt>

**NumberOfProcessors**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (2)
</dt> </dl>

Nombre de processeurs sur l’ordinateur.

</dd> <dt>

**PageSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (4)
</dt> </dl>

Taille d’une page d’échange, en octets.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                            |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SystemConfig \_ v0**](systemconfig-v0.md)
</dt> </dl>

 

 




