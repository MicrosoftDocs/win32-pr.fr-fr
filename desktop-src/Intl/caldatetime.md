---
description: Obsolète. Représente un instant, généralement exprimé sous la forme d’une date et d’une heure de jour et d’un calendrier correspondant.
ms.assetid: a714ff32-2b1f-4256-931e-324d64daf2ac
title: CALDATETIME, structure
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CALDATETIME
api_type:
- NA
api_location: ''
ms.openlocfilehash: 5e3f0099a8e1dd7794b960af3d753085f2a32eaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524747"
---
# <a name="caldatetime-structure"></a>CALDATETIME, structure

Action déconseillée. Représente un instant, généralement exprimé sous la forme d’une date et d’une heure de jour et d’un calendrier correspondant.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _caldatetime {
  CALID CalId;
  UINT  Era;
  UINT  Year;
  UINT  Month;
  UINT  Day;
  UINT  DayOfWeek;
  UINT  Hour;
  UINT  Minute;
  UINT  Second;
  ULONG Tick;
} CALDATETIME, *LPCALDATETIME;
```



## <a name="members"></a>Membres

<dl> <dt>

**CalId**
</dt> <dd>

[Identificateur de calendrier](calendar-identifiers.md) pour l’instant dans le temps.

</dd> <dt>

**Européen**
</dt> <dd>

Informations sur l’ère pour l’instant dans le temps.

</dd> <dt>

**Year**
</dt> <dd>

Année pour l’instant.

</dd> <dt>

**Chronique**
</dt> <dd>

Mois pour l’instant.

</dd> <dt>

**Jour**
</dt> <dd>

Jour de l’instant dans le temps.

</dd> <dt>

**DayOfWeek**
</dt> <dd>

Jour de la semaine pour l’instant dans le temps.

</dd> <dt>

**Plages**
</dt> <dd>

Heure de l’instant dans le temps.

</dd> <dt>

**Dernières**
</dt> <dd>

Minute pour l’instant.

</dd> <dt>

**Tache**
</dt> <dd>

Seconde pour l’instant.

</dd> <dt>

**Graduations**
</dt> <dd>

Cycle de l’instant dans le temps.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures de prise en charge linguistique nationale](national-language-support-structures.md)
</dt> </dl>

 

 




