---
description: Obsolète. Spécifie les unités de date pour l’ajustement de la structure CALDATETIME.
ms.assetid: 20d0cd7a-6e6b-4c82-9cfa-e4f4315d6362
title: Énumération CALDATETIME_DATEUNIT
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CALDATETIME_DATEUNIT
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6ce1f8929dd6e2f7de59d32d66229f73c062505c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515437"
---
# <a name="caldatetime_dateunit-enumeration"></a>CALDATETIME \_ DATEUNIT, énumération

Action déconseillée. Spécifie les unités de date pour l’ajustement de la structure [**CALDATETIME**](caldatetime.md) .

## <a name="syntax"></a>Syntaxe


```C++
enum CALDATETIME_DATEUNIT {
  EraUnit, 
  YearUnit, 
  MonthUnit, 
  WeekUnit, 
  DayUnit, 
  HourUnit, 
  MinuteUnit, 
  SecondUnit, 
  TickUnit 

};
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="EraUnit"></span><span id="eraunit"></span><span id="ERAUNIT"></span>**EraUnit**
</dt> <dd>

Unité de date et d’heure de l’ère.

</dd> <dt>

<span id="YearUnit"></span><span id="yearunit"></span><span id="YEARUNIT"></span>**YearUnit**
</dt> <dd>

Unité date/heure.

</dd> <dt>

<span id="MonthUnit"></span><span id="monthunit"></span><span id="MONTHUNIT"></span>**MonthUnit**
</dt> <dd>

Unité date/heure du mois.

</dd> <dt>

<span id="WeekUnit"></span><span id="weekunit"></span><span id="WEEKUNIT"></span>**WeekUnit**
</dt> <dd>

Unité de date et d’heure de la semaine.

</dd> <dt>

<span id="DayUnit"></span><span id="dayunit"></span><span id="DAYUNIT"></span>**DayUnit**
</dt> <dd>

Unité de date et d’heure.

</dd> <dt>

<span id="HourUnit"></span><span id="hourunit"></span><span id="HOURUNIT"></span>**HourUnit**
</dt> <dd>

Unité de date et d’heure.

</dd> <dt>

<span id="MinuteUnit"></span><span id="minuteunit"></span><span id="MINUTEUNIT"></span>**MinuteUnit**
</dt> <dd>

Unité de date/heure.

</dd> <dt>

<span id="SecondUnit"></span><span id="secondunit"></span><span id="SECONDUNIT"></span>**SecondUnit**
</dt> <dd>

Deuxième unité de date et heure.

</dd> <dt>

<span id="TickUnit"></span><span id="tickunit"></span><span id="TICKUNIT"></span>**TickUnit**
</dt> <dd>

Unité de date et d’heure de la graduation.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Types d’énumération de prise en charge linguistique nationale](national-language-support-enumeration-types.md)
</dt> </dl>

 

 




