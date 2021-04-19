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
# <a name="caldatetime_dateunit-enumeration"></a><span data-ttu-id="ea397-104">CALDATETIME \_ DATEUNIT, énumération</span><span class="sxs-lookup"><span data-stu-id="ea397-104">CALDATETIME\_DATEUNIT enumeration</span></span>

<span data-ttu-id="ea397-105">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="ea397-105">Deprecated.</span></span> <span data-ttu-id="ea397-106">Spécifie les unités de date pour l’ajustement de la structure [**CALDATETIME**](caldatetime.md) .</span><span class="sxs-lookup"><span data-stu-id="ea397-106">Specifies the date units for adjusting the [**CALDATETIME**](caldatetime.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea397-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ea397-107">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="ea397-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="ea397-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ea397-109"><span id="EraUnit"></span><span id="eraunit"></span><span id="ERAUNIT"></span>**EraUnit**</span><span class="sxs-lookup"><span data-stu-id="ea397-109"><span id="EraUnit"></span><span id="eraunit"></span><span id="ERAUNIT"></span>**EraUnit**</span></span>
</dt> <dd>

<span data-ttu-id="ea397-110">Unité de date et d’heure de l’ère.</span><span class="sxs-lookup"><span data-stu-id="ea397-110">The era date time unit.</span></span>

</dd> <dt>

<span data-ttu-id="ea397-111"><span id="YearUnit"></span><span id="yearunit"></span><span id="YEARUNIT"></span>**YearUnit**</span><span class="sxs-lookup"><span data-stu-id="ea397-111"><span id="YearUnit"></span><span id="yearunit"></span><span id="YEARUNIT"></span>**YearUnit**</span></span>
</dt> <dd>

<span data-ttu-id="ea397-112">Unité date/heure.</span><span class="sxs-lookup"><span data-stu-id="ea397-112">The year date time unit.</span></span>

</dd> <dt>

<span data-ttu-id="ea397-113"><span id="MonthUnit"></span><span id="monthunit"></span><span id="MONTHUNIT"></span>**MonthUnit**</span><span class="sxs-lookup"><span data-stu-id="ea397-113"><span id="MonthUnit"></span><span id="monthunit"></span><span id="MONTHUNIT"></span>**MonthUnit**</span></span>
</dt> <dd>

<span data-ttu-id="ea397-114">Unité date/heure du mois.</span><span class="sxs-lookup"><span data-stu-id="ea397-114">The month date time unit.</span></span>

</dd> <dt>

<span data-ttu-id="ea397-115"><span id="WeekUnit"></span><span id="weekunit"></span><span id="WEEKUNIT"></span>**WeekUnit**</span><span class="sxs-lookup"><span data-stu-id="ea397-115"><span id="WeekUnit"></span><span id="weekunit"></span><span id="WEEKUNIT"></span>**WeekUnit**</span></span>
</dt> <dd>

<span data-ttu-id="ea397-116">Unité de date et d’heure de la semaine.</span><span class="sxs-lookup"><span data-stu-id="ea397-116">The week date time unit.</span></span>

</dd> <dt>

<span data-ttu-id="ea397-117"><span id="DayUnit"></span><span id="dayunit"></span><span id="DAYUNIT"></span>**DayUnit**</span><span class="sxs-lookup"><span data-stu-id="ea397-117"><span id="DayUnit"></span><span id="dayunit"></span><span id="DAYUNIT"></span>**DayUnit**</span></span>
</dt> <dd>

<span data-ttu-id="ea397-118">Unité de date et d’heure.</span><span class="sxs-lookup"><span data-stu-id="ea397-118">The day date time unit.</span></span>

</dd> <dt>

<span data-ttu-id="ea397-119"><span id="HourUnit"></span><span id="hourunit"></span><span id="HOURUNIT"></span>**HourUnit**</span><span class="sxs-lookup"><span data-stu-id="ea397-119"><span id="HourUnit"></span><span id="hourunit"></span><span id="HOURUNIT"></span>**HourUnit**</span></span>
</dt> <dd>

<span data-ttu-id="ea397-120">Unité de date et d’heure.</span><span class="sxs-lookup"><span data-stu-id="ea397-120">The hour date time unit.</span></span>

</dd> <dt>

<span data-ttu-id="ea397-121"><span id="MinuteUnit"></span><span id="minuteunit"></span><span id="MINUTEUNIT"></span>**MinuteUnit**</span><span class="sxs-lookup"><span data-stu-id="ea397-121"><span id="MinuteUnit"></span><span id="minuteunit"></span><span id="MINUTEUNIT"></span>**MinuteUnit**</span></span>
</dt> <dd>

<span data-ttu-id="ea397-122">Unité de date/heure.</span><span class="sxs-lookup"><span data-stu-id="ea397-122">The minute date time unit.</span></span>

</dd> <dt>

<span data-ttu-id="ea397-123"><span id="SecondUnit"></span><span id="secondunit"></span><span id="SECONDUNIT"></span>**SecondUnit**</span><span class="sxs-lookup"><span data-stu-id="ea397-123"><span id="SecondUnit"></span><span id="secondunit"></span><span id="SECONDUNIT"></span>**SecondUnit**</span></span>
</dt> <dd>

<span data-ttu-id="ea397-124">Deuxième unité de date et heure.</span><span class="sxs-lookup"><span data-stu-id="ea397-124">The second date time unit.</span></span>

</dd> <dt>

<span data-ttu-id="ea397-125"><span id="TickUnit"></span><span id="tickunit"></span><span id="TICKUNIT"></span>**TickUnit**</span><span class="sxs-lookup"><span data-stu-id="ea397-125"><span id="TickUnit"></span><span id="tickunit"></span><span id="TICKUNIT"></span>**TickUnit**</span></span>
</dt> <dd>

<span data-ttu-id="ea397-126">Unité de date et d’heure de la graduation.</span><span class="sxs-lookup"><span data-stu-id="ea397-126">The tick date time unit.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ea397-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ea397-127">Requirements</span></span>



| <span data-ttu-id="ea397-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ea397-128">Requirement</span></span> | <span data-ttu-id="ea397-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="ea397-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ea397-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ea397-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ea397-131">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ea397-131">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ea397-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ea397-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ea397-133">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ea397-133">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ea397-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ea397-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea397-135">Types d’énumération de prise en charge linguistique nationale</span><span class="sxs-lookup"><span data-stu-id="ea397-135">National Language Support Enumeration Types</span></span>](national-language-support-enumeration-types.md)
</dt> </dl>

 

 




