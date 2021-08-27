---
description: Cette classe est la classe de type d’événement pour les événements de sortie d’appel système. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: bb9a2770-f37b-4055-8811-59ba117adf82
title: SysCallExit, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SysCallExit
- SysCallExit.SysCallNtStatus
api_type:
- NA
api_location: ''
ms.openlocfilehash: aa297ced8f6c0d17c0c01da9ce11705d30fe7448c8bc2f2ae6358ddc85f653be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102059"
---
# <a name="syscallexit-class"></a>SysCallExit, classe

Cette classe est la classe de type d’événement pour les événements de sortie d’appel système.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[EventType{52}, EventTypeName{"SysClExit"}]
class SysCallExit : PerfInfo
{
  uint32 SysCallNtStatus;
};
```

## <a name="members"></a>Membres

La classe **SysCallExit** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **SysCallExit** possède les propriétés suivantes.

<dl> <dt>

**SysCallNtStatus**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (1), format ("x")
</dt> </dl>

Code d’état retourné par l’appel système NT.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 




