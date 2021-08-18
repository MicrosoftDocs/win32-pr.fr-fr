---
description: Cette classe est la classe de type d’événement pour les événements de compteur de processus. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 7f1fa1c4-a2ff-4a1c-ac9d-e922a13c99a1
title: Classe Process_V2_TypeGroup2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_V2_TypeGroup2
- Process_V2_TypeGroup2.ProcessId
- Process_V2_TypeGroup2.PageFaultCount
- Process_V2_TypeGroup2.HandleCount
- Process_V2_TypeGroup2.Reserved
- Process_V2_TypeGroup2.PeakVirtualSize
- Process_V2_TypeGroup2.PeakWorkingSetSize
- Process_V2_TypeGroup2.PeakPagefileUsage
- Process_V2_TypeGroup2.QuotaPeakPagedPoolUsage
- Process_V2_TypeGroup2.QuotaPeakNonPagedPoolUsage
- Process_V2_TypeGroup2.VirtualSize
- Process_V2_TypeGroup2.WorkingSetSize
- Process_V2_TypeGroup2.PagefileUsage
- Process_V2_TypeGroup2.QuotaPagedPoolUsage
- Process_V2_TypeGroup2.QuotaNonPagedPoolUsage
- Process_V2_TypeGroup2.PrivatePageCount
api_type:
- NA
api_location: ''
ms.openlocfilehash: 51c24e12ed423b6240daeefee0b69a40f9b14b86813ca83cb09f74f807e24429
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069949"
---
# <a name="process_v2_typegroup2-class"></a>Traiter \_ la \_ classe TypeGroup2 v2

Cette classe est la classe de type d’événement pour les événements de compteur de processus.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[EventType{32, 33}, EventTypeName{"PerfCtr", PerfCtrRundown"}]
class Process_V2_TypeGroup2 : Process_V2
{
  uint32 ProcessId;
  uint32 PageFaultCount;
  uint32 HandleCount;
  uint32 Reserved;
  object PeakVirtualSize;
  object PeakWorkingSetSize;
  object PeakPagefileUsage;
  object QuotaPeakPagedPoolUsage;
  object QuotaPeakNonPagedPoolUsage;
  object VirtualSize;
  object WorkingSetSize;
  object PagefileUsage;
  object QuotaPagedPoolUsage;
  object QuotaNonPagedPoolUsage;
  object PrivatePageCount;
};
```

## <a name="members"></a>Membres

La classe **process \_ v2 \_ TypeGroup2** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **process \_ v2 \_ TypeGroup2** a ces propriétés.

<dl> <dt>

**HandleCount**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (3)
</dt> </dl>

Nombre de handles utilisés.

</dd> <dt>

**PageFaultCount**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (2)
</dt> </dl>

Nombre de défauts de page.

</dd> <dt>

**PagefileUsage**
</dt> <dd> <dl> <dt>

Type de données : **objet**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (12), extension ("Sizet")
</dt> </dl>

Utilisation du fichier d’échange actuel.

</dd> <dt>

**PeakPagefileUsage**
</dt> <dd> <dl> <dt>

Type de données : **objet**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (7), extension ("Sizet")
</dt> </dl>

Taille de fichier d’échange la plus grande utilisée.

</dd> <dt>

**PeakVirtualSize**
</dt> <dd> <dl> <dt>

Type de données : **objet**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (5), extension ("Sizet")
</dt> </dl>

Taille de page virtuelle la plus grande utilisée.

</dd> <dt>

**PeakWorkingSetSize**
</dt> <dd> <dl> <dt>

Type de données : **objet**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (6), extension ("Sizet")
</dt> </dl>

Taille de la plus grande plage de travail utilisée.

</dd> <dt>

**PrivatePageCount**
</dt> <dd> <dl> <dt>

Type de données : **objet**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (15), extension ("Sizet")
</dt> </dl>

Nombre de pages physiques privées actuelles.

</dd> <dt>

ProcessId
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (1), format ("x")
</dt> </dl>

Identificateur de processus global que vous pouvez utiliser pour identifier un processus. La valeur est valide à partir du moment où un processus est créé jusqu’à ce qu’il soit terminé.

</dd> <dt>

**QuotaNonPagedPoolUsage**
</dt> <dd> <dl> <dt>

Type de données : **objet**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (14), extension ("Sizet")
</dt> </dl>

Utilisation de la mémoire non paginée actuellement validée.

</dd> <dt>

**QuotaPagedPoolUsage**
</dt> <dd> <dl> <dt>

Type de données : **objet**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (13), extension ("Sizet")
</dt> </dl>

Utilisation de la mémoire paginée actuellement validée.

</dd> <dt>

**QuotaPeakNonPagedPoolUsage**
</dt> <dd> <dl> <dt>

Type de données : **objet**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (9), extension ("Sizet")
</dt> </dl>

Mémoire non paginée validée la plus grande utilisée.

</dd> <dt>

**QuotaPeakPagedPoolUsage**
</dt> <dd> <dl> <dt>

Type de données : **objet**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (8), extension ("Sizet")
</dt> </dl>

Mémoire paginée allouée la plus grande utilisée.

</dd> <dt>

**Reserved**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (4)
</dt> </dl>

Réservé.

</dd> <dt>

**VirtualSize**
</dt> <dd> <dl> <dt>

Type de données : **objet**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (10), extension ("Sizet")
</dt> </dl>

Taille de page virtuelle actuelle.

</dd> <dt>

**WorkingSetSize**
</dt> <dd> <dl> <dt>

Type de données : **objet**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (11), extension ("Sizet")
</dt> </dl>

Taille actuelle de la plage de travail.

</dd> </dl>

## <a name="remarks"></a>Remarques

Ces événements sont enregistrés lorsque le processus se termine. L’événement indique comment un processus a traité l’utilisation de la mémoire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Traitement \_ v2**](process-v2.md)
</dt> </dl>

 

 




