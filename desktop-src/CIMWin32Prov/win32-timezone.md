---
description: Le \_ fuseau horaire Win32&\# 8194 ; La classe WMI représente les informations de fuseau horaire pour un système informatique exécutant Windows, qui comprend les modifications requises pour la transition vers l’heure d’été.
ms.assetid: c1c7731e-768f-42ea-a36c-57b00df6848e
ms.tgt_platform: multiple
title: Classe Win32_TimeZone
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_TimeZone
- Win32_TimeZone.Caption
- Win32_TimeZone.Description
- Win32_TimeZone.SettingID
- Win32_TimeZone.Bias
- Win32_TimeZone.DaylightBias
- Win32_TimeZone.DaylightDay
- Win32_TimeZone.DaylightDayOfWeek
- Win32_TimeZone.DaylightHour
- Win32_TimeZone.DaylightMillisecond
- Win32_TimeZone.DaylightMinute
- Win32_TimeZone.DaylightMonth
- Win32_TimeZone.DaylightName
- Win32_TimeZone.DaylightSecond
- Win32_TimeZone.DaylightYear
- Win32_TimeZone.StandardBias
- Win32_TimeZone.StandardDay
- Win32_TimeZone.StandardDayOfWeek
- Win32_TimeZone.StandardHour
- Win32_TimeZone.StandardMillisecond
- Win32_TimeZone.StandardMinute
- Win32_TimeZone.StandardMonth
- Win32_TimeZone.StandardName
- Win32_TimeZone.StandardSecond
- Win32_TimeZone.StandardYear
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 433682f045ca7fb127c7dc69e3a26ed8356371ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861017"
---
# <a name="win32_timezone-class"></a><span data-ttu-id="d9e6c-103">\_Classe TimeZone Win32</span><span class="sxs-lookup"><span data-stu-id="d9e6c-103">Win32\_TimeZone class</span></span>

<span data-ttu-id="d9e6c-104">La  [classe WMI](../wmisdk/retrieving-a-class.md) de **\_ fuseau horaire Win32** représente les informations de fuseau horaire pour un système informatique exécutant Windows, qui comprend les modifications requises pour la transition vers l’heure d’été.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-104">The **Win32\_TimeZone** [WMI class](../wmisdk/retrieving-a-class.md) represents the time zone information for a computer system running Windows, which includes the changes required for transitioning to daylight saving time transition.</span></span>

<span data-ttu-id="d9e6c-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="d9e6c-106">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9e6c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d9e6c-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4EC-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_TimeZone : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  sint32 Bias;
  sint32 DaylightBias;
  uint32 DaylightDay;
  uint8  DaylightDayOfWeek;
  uint32 DaylightHour;
  uint32 DaylightMillisecond;
  uint32 DaylightMinute;
  uint32 DaylightMonth;
  string DaylightName;
  uint32 DaylightSecond;
  uint32 DaylightYear;
  uint32 StandardBias;
  uint32 StandardDay;
  uint8  StandardDayOfWeek;
  uint32 StandardHour;
  uint32 StandardMillisecond;
  uint32 StandardMinute;
  uint32 StandardMonth;
  string StandardName;
  uint32 StandardSecond;
  uint32 StandardYear;
};
```

## <a name="members"></a><span data-ttu-id="d9e6c-108">Membres</span><span class="sxs-lookup"><span data-stu-id="d9e6c-108">Members</span></span>

<span data-ttu-id="d9e6c-109">La classe **Win32 \_ TimeZone** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d9e6c-109">The **Win32\_TimeZone** class has these types of members:</span></span>

-   [<span data-ttu-id="d9e6c-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d9e6c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d9e6c-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d9e6c-111">Properties</span></span>

<span data-ttu-id="d9e6c-112">La classe **Win32 \_ TimeZone** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-112">The **Win32\_TimeZone** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d9e6c-113">**Décalage**</span><span class="sxs-lookup"><span data-stu-id="d9e6c-113">**Bias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9e6c-114">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="d9e6c-114">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d9e6c-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d9e6c-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9e6c-116">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Time structures \| [**\_ \_ information fuseau horaire**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| Bias"), [**unités**](../wmisdk/standard-qualifiers.md) ("minutes")</span><span class="sxs-lookup"><span data-stu-id="d9e6c-116">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|Bias"), [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="d9e6c-117">Décalage actuel pour la traduction de l’heure locale.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-117">Current bias for local time translation.</span></span> <span data-ttu-id="d9e6c-118">Le biais correspond à la différence entre le temps universel coordonné (UTC, Universal Time Coordinated) et l’heure locale.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-118">The bias is the difference between Coordinated Universal Time (UTC) and local time.</span></span> <span data-ttu-id="d9e6c-119">Toutes les traductions entre l’heure UTC et l’heure locale sont basées sur la formule suivante : UTC = heure locale.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-119">All translations between UTC and local time are based on the following formula: UTC = local time - bias.</span></span> <span data-ttu-id="d9e6c-120">Cette propriété est requise.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-120">This property is required.</span></span>

</dd> <dt>

<span data-ttu-id="d9e6c-121">**Caption**</span><span class="sxs-lookup"><span data-stu-id="d9e6c-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9e6c-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d9e6c-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9e6c-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d9e6c-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9e6c-124">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="d9e6c-124">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d9e6c-125">Courte description textuelle de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-125">Short textual description of the current object.</span></span>

<span data-ttu-id="d9e6c-126">Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="d9e6c-126">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="d9e6c-127">**DaylightBias**</span><span class="sxs-lookup"><span data-stu-id="d9e6c-127">**DaylightBias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9e6c-128">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="d9e6c-128">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d9e6c-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d9e6c-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9e6c-130">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Time structures \| [**\_ \_ information de fuseau horaire**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightBias"), [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span><span class="sxs-lookup"><span data-stu-id="d9e6c-130">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightBias"), [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="d9e6c-131">Valeur de décalage à utiliser lors des traductions d’heure locales qui se produisent pendant l’heure d’été.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-131">Bias value to be used during local time translations that occur during daylight saving time.</span></span> <span data-ttu-id="d9e6c-132">Cette propriété est ignorée si aucune valeur n’est fournie pour la propriété **DaylightDay** .</span><span class="sxs-lookup"><span data-stu-id="d9e6c-132">This property is ignored if a value for the **DaylightDay** property is not supplied.</span></span> <span data-ttu-id="d9e6c-133">La valeur de cette propriété est ajoutée à la propriété **Bias** pour former le biais utilisé pendant l’heure d’été.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-133">The value of this property is added to the **Bias** property to form the bias used during daylight time.</span></span> <span data-ttu-id="d9e6c-134">Dans la plupart des fuseaux horaires, la valeur de cette propriété est-60.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-134">In most time zones, the value of this property is -60.</span></span>

</dd> <dt>

<span data-ttu-id="d9e6c-135">**DaylightDay**</span><span class="sxs-lookup"><span data-stu-id="d9e6c-135">**DaylightDay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9e6c-136">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d9e6c-136">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d9e6c-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d9e6c-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9e6c-138">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Time structures \| [**\_ \_ information de fuseau horaire**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| WDAY")</span><span class="sxs-lookup"><span data-stu-id="d9e6c-138">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightDate\|wDay")</span></span>
</dt> </dl>

<span data-ttu-id="d9e6c-139">**DaylightDayOfWeek** du **DaylightMonth** lorsque le passage de l’heure d’hiver à l’heure d’été se produit sur ce système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-139">**DaylightDayOfWeek** of the **DaylightMonth** when the transition from standard time to daylight saving time occurs on this operating system.</span></span>

<span data-ttu-id="d9e6c-140">Exemple : si le jour de transition (**DaylightDayOfWeek**) se produit un dimanche, la valeur « 1 » indique le premier dimanche du **DaylightMonth**, « 2 » indique le deuxième dimanche, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-140">Example: If the transition day (**DaylightDayOfWeek**) occurs on a Sunday, then the value "1" indicates the first Sunday of the **DaylightMonth**, "2" indicates the second Sunday, and so on.</span></span> <span data-ttu-id="d9e6c-141">La valeur « 5 » indique le dernier **DaylightDayOfWeek** du mois.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-141">The value "5" indicates the last **DaylightDayOfWeek** in the month.</span></span>

</dd> <dt>

<span data-ttu-id="d9e6c-142">**DaylightDayOfWeek**</span><span class="sxs-lookup"><span data-stu-id="d9e6c-142">**DaylightDayOfWeek**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9e6c-143">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="d9e6c-143">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="d9e6c-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d9e6c-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9e6c-145">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Time structures \| [**\_ \_ information de fuseau horaire**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wDayOfWeek")</span><span class="sxs-lookup"><span data-stu-id="d9e6c-145">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightDate\|wDayOfWeek")</span></span>
</dt> </dl>

<span data-ttu-id="d9e6c-146">Jour de la semaine où le passage de l’heure d’hiver à l’heure d’été se produit sur un système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-146">Day of the week when the transition from standard time to daylight saving time occurs on an operating system.</span></span>

<dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

<span data-ttu-id="d9e6c-147">**Dimanche** (0)</span><span class="sxs-lookup"><span data-stu-id="d9e6c-147">**Sunday** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

<span data-ttu-id="d9e6c-148">**Lundi** (1)</span><span class="sxs-lookup"><span data-stu-id="d9e6c-148">**Monday** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

<span data-ttu-id="d9e6c-149">**Mardi** (2)</span><span class="sxs-lookup"><span data-stu-id="d9e6c-149">**Tuesday** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

<span data-ttu-id="d9e6c-150">**Mercredi** (3)</span><span class="sxs-lookup"><span data-stu-id="d9e6c-150">**Wednesday** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

<span data-ttu-id="d9e6c-151">**Jeudi** (4)</span><span class="sxs-lookup"><span data-stu-id="d9e6c-151">**Thursday** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

<span data-ttu-id="d9e6c-152">**Vendredi** (5)</span><span class="sxs-lookup"><span data-stu-id="d9e6c-152">**Friday** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

<span data-ttu-id="d9e6c-153">**Samedi** (6)</span><span class="sxs-lookup"><span data-stu-id="d9e6c-153">**Saturday** (6)</span></span>


<span data-ttu-id="d9e6c-154"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="d9e6c-154"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="d9e6c-155">Exemple : 1</span><span class="sxs-lookup"><span data-stu-id="d9e6c-155">Example: 1</span></span>

</dd> <dt>

<span data-ttu-id="d9e6c-156">**DaylightHour**</span><span class="sxs-lookup"><span data-stu-id="d9e6c-156">**DaylightHour**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9e6c-157">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d9e6c-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d9e6c-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d9e6c-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9e6c-159">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Time structures \| [**\_ \_ information de fuseau horaire**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wHour")</span><span class="sxs-lookup"><span data-stu-id="d9e6c-159">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightDate\|wHour")</span></span>
</dt> </dl>

<span data-ttu-id="d9e6c-160">Heure de la journée à laquelle le passage de l’heure d’hiver à l’heure d’été se produit sur un système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-160">Hour of the day when the transition from standard time to daylight saving time occurs on an operating system.</span></span>

<span data-ttu-id="d9e6c-161">Exemple : 2</span><span class="sxs-lookup"><span data-stu-id="d9e6c-161">Example: 2</span></span>

</dd> <dt>

<span data-ttu-id="d9e6c-162">**DaylightMillisecond**</span><span class="sxs-lookup"><span data-stu-id="d9e6c-162">**DaylightMillisecond**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9e6c-163">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d9e6c-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d9e6c-164">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d9e6c-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9e6c-165">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Time structures \| [**\_ \_ information de fuseau horaire**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wMilliseconds")</span><span class="sxs-lookup"><span data-stu-id="d9e6c-165">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightDate\|wMilliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="d9e6c-166">Milliseconde du **DaylightSecond** lorsque le passage de l’heure d’hiver à l’heure d’été se produit sur un système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-166">Millisecond of the **DaylightSecond** when the transition from standard time to daylight saving time occurs on an operating system.</span></span>

</dd> <dt>

<span data-ttu-id="d9e6c-167">**DaylightMinute**</span><span class="sxs-lookup"><span data-stu-id="d9e6c-167">**DaylightMinute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9e6c-168">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d9e6c-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d9e6c-169">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d9e6c-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9e6c-170">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Time structures \| [**\_ \_ information de fuseau horaire**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wMinute")</span><span class="sxs-lookup"><span data-stu-id="d9e6c-170">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightDate\|wMinute")</span></span>
</dt> </dl>

<span data-ttu-id="d9e6c-171">Minute de **DaylightHour** lorsque le passage de l’heure d’hiver à l’heure d’été se produit sur un système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-171">Minute of the **DaylightHour** when the transition from standard time to daylight saving time occurs on an operating system.</span></span>

<span data-ttu-id="d9e6c-172">Exemple : 59</span><span class="sxs-lookup"><span data-stu-id="d9e6c-172">Example: 59</span></span>

</dd> <dt>

<span data-ttu-id="d9e6c-173">**DaylightMonth**</span><span class="sxs-lookup"><span data-stu-id="d9e6c-173">**DaylightMonth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9e6c-174">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d9e6c-174">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d9e6c-175">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d9e6c-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9e6c-176">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Time structures \| [**\_ \_ information de fuseau horaire**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wMonth")</span><span class="sxs-lookup"><span data-stu-id="d9e6c-176">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightDate\|wMonth")</span></span>
</dt> </dl>

<span data-ttu-id="d9e6c-177">Mois où le passage de l’heure d’hiver à l’heure d’été se produit sur un système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-177">Month when the transition from standard time to daylight saving time occurs on an operating system.</span></span>

<dt>

<span id="January"></span><span id="january"></span><span id="JANUARY"></span>

<span data-ttu-id="d9e6c-178">**Janvier** (1)</span><span class="sxs-lookup"><span data-stu-id="d9e6c-178">**January** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>

<span data-ttu-id="d9e6c-179">**Février** (2)</span><span class="sxs-lookup"><span data-stu-id="d9e6c-179">**February** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="March"></span><span id="march"></span><span id="MARCH"></span>

<span data-ttu-id="d9e6c-180">**Mars** (3)</span><span class="sxs-lookup"><span data-stu-id="d9e6c-180">**March** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="April"></span><span id="april"></span><span id="APRIL"></span>

<span data-ttu-id="d9e6c-181">**Avril** (4)</span><span class="sxs-lookup"><span data-stu-id="d9e6c-181">**April** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="May"></span><span id="may"></span><span id="MAY"></span>

<span data-ttu-id="d9e6c-182">**Mai** (5)</span><span class="sxs-lookup"><span data-stu-id="d9e6c-182">**May** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="June"></span><span id="june"></span><span id="JUNE"></span>

<span data-ttu-id="d9e6c-183">**Juin** (6)</span><span class="sxs-lookup"><span data-stu-id="d9e6c-183">**June** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="July"></span><span id="july"></span><span id="JULY"></span>

<span data-ttu-id="d9e6c-184">**Juillet** (7)</span><span class="sxs-lookup"><span data-stu-id="d9e6c-184">**July** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="August"></span><span id="august"></span><span id="AUGUST"></span>

<span data-ttu-id="d9e6c-185">**Août** (8)</span><span class="sxs-lookup"><span data-stu-id="d9e6c-185">**August** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>

<span data-ttu-id="d9e6c-186">**Septembre** (9)</span><span class="sxs-lookup"><span data-stu-id="d9e6c-186">**September** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="October"></span><span id="october"></span><span id="OCTOBER"></span>

<span data-ttu-id="d9e6c-187">**Octobre** (10)</span><span class="sxs-lookup"><span data-stu-id="d9e6c-187">**October** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>

<span data-ttu-id="d9e6c-188">**Novembre** (11)</span><span class="sxs-lookup"><span data-stu-id="d9e6c-188">**November** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="December"></span><span id="december"></span><span id="DECEMBER"></span>

<span data-ttu-id="d9e6c-189">**Décembre** (12)</span><span class="sxs-lookup"><span data-stu-id="d9e6c-189">**December** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d9e6c-190">**DaylightName**</span><span class="sxs-lookup"><span data-stu-id="d9e6c-190">**DaylightName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9e6c-191">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d9e6c-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9e6c-192">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d9e6c-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9e6c-193">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Time structures \| [**\_ \_ information fuseau horaire**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightName")</span><span class="sxs-lookup"><span data-stu-id="d9e6c-193">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightName")</span></span>
</dt> </dl>

<span data-ttu-id="d9e6c-194">Fuseau horaire représenté lorsque l’heure d’été est en vigueur.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-194">Time zone being represented when daylight saving time is in effect.</span></span>

<span data-ttu-id="d9e6c-195">Exemple : « EDT » (heure d’été de l’est)</span><span class="sxs-lookup"><span data-stu-id="d9e6c-195">Example: "EDT" (Eastern Daylight Time)</span></span>

</dd> <dt>

<span data-ttu-id="d9e6c-196">**DaylightSecond**</span><span class="sxs-lookup"><span data-stu-id="d9e6c-196">**DaylightSecond**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9e6c-197">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d9e6c-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d9e6c-198">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d9e6c-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9e6c-199">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Time structures \| [**\_ \_ information de fuseau horaire**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wSecond")</span><span class="sxs-lookup"><span data-stu-id="d9e6c-199">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightDate\|wSecond")</span></span>
</dt> </dl>

<span data-ttu-id="d9e6c-200">Deuxième des **DaylightMinute** lorsque le passage de l’heure d’hiver à l’heure d’été se produit sur un système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-200">Second of the **DaylightMinute** when the transition from standard time to daylight saving time occurs on an operating system.</span></span>

<span data-ttu-id="d9e6c-201">Exemple : 59</span><span class="sxs-lookup"><span data-stu-id="d9e6c-201">Example: 59</span></span>

</dd> <dt>

<span data-ttu-id="d9e6c-202">**DaylightYear**</span><span class="sxs-lookup"><span data-stu-id="d9e6c-202">**DaylightYear**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9e6c-203">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d9e6c-203">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d9e6c-204">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d9e6c-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9e6c-205">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Time structures \| [**\_ \_ information de fuseau horaire**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wYear")</span><span class="sxs-lookup"><span data-stu-id="d9e6c-205">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightDate\|wYear")</span></span>
</dt> </dl>

<span data-ttu-id="d9e6c-206">Année lorsque l’heure d’été est en vigueur.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-206">Year when daylight saving time is in effect.</span></span> <span data-ttu-id="d9e6c-207">Cette propriété n’est pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-207">This property is not required.</span></span>

<span data-ttu-id="d9e6c-208">Exemple : 1997</span><span class="sxs-lookup"><span data-stu-id="d9e6c-208">Example: 1997</span></span>

</dd> <dt>

<span data-ttu-id="d9e6c-209">**Description**</span><span class="sxs-lookup"><span data-stu-id="d9e6c-209">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9e6c-210">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d9e6c-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9e6c-211">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d9e6c-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9e6c-212">Description textuelle de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-212">Textual description of the current object.</span></span>

<span data-ttu-id="d9e6c-213">Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="d9e6c-213">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="d9e6c-214">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="d9e6c-214">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9e6c-215">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d9e6c-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9e6c-216">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d9e6c-216">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9e6c-217">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="d9e6c-217">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="d9e6c-218">Identificateur par lequel l’objet actuel est connu.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-218">Identifier by which the current object is known.</span></span>

<span data-ttu-id="d9e6c-219">Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="d9e6c-219">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="d9e6c-220">**StandardBias**</span><span class="sxs-lookup"><span data-stu-id="d9e6c-220">**StandardBias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9e6c-221">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d9e6c-221">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d9e6c-222">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d9e6c-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9e6c-223">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Time structures \| [**\_ \_ information de fuseau horaire**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardBias"), [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span><span class="sxs-lookup"><span data-stu-id="d9e6c-223">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardBias"), [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="d9e6c-224">Valeur de décalage à utiliser lorsque l’heure d’été n’est pas appliquée.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-224">Bias value to use when daylight saving time is not in effect.</span></span> <span data-ttu-id="d9e6c-225">Cette propriété est ignorée si aucune valeur n’est fournie pour **StandardDay** .</span><span class="sxs-lookup"><span data-stu-id="d9e6c-225">This property is ignored if a value for **StandardDay** is not supplied.</span></span> <span data-ttu-id="d9e6c-226">La valeur de cette propriété est ajoutée à la propriété **Bias** pour former le décalage pendant l’heure standard.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-226">The value of this property is added to the **Bias** property to form the bias during standard time.</span></span>

<span data-ttu-id="d9e6c-227">Exemple : 0</span><span class="sxs-lookup"><span data-stu-id="d9e6c-227">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="d9e6c-228">**StandardDay**</span><span class="sxs-lookup"><span data-stu-id="d9e6c-228">**StandardDay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9e6c-229">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d9e6c-229">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d9e6c-230">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d9e6c-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9e6c-231">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Time structures \| [**\_ \_ information de fuseau horaire**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| WDAY")</span><span class="sxs-lookup"><span data-stu-id="d9e6c-231">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardDate\|wDay")</span></span>
</dt> </dl>

<span data-ttu-id="d9e6c-232">**StandardDayOfWeek** du **StandardMonth** lorsque le passage de l’heure d’été à l’heure d’hiver se produit sur un système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-232">**StandardDayOfWeek** of the **StandardMonth** when the transition from daylight saving time to standard time occurs on an operating system.</span></span>

<span data-ttu-id="d9e6c-233">Si le jour de transition (**StandardDayOfWeek**) se produit un dimanche, la valeur « 1 » indique le premier dimanche du **StandardMonth**, « 2 » indique le deuxième dimanche, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-233">If the transition day (**StandardDayOfWeek**) occurs on a Sunday, then the value "1" indicates the first Sunday of the **StandardMonth**, "2" indicates the second Sunday, and so on.</span></span> <span data-ttu-id="d9e6c-234">La valeur « 5 » indique le dernier **StandardDayOfWeek** du mois.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-234">The value "5" indicates the last **StandardDayOfWeek** in the month.</span></span>

</dd> <dt>

<span data-ttu-id="d9e6c-235">**StandardDayOfWeek**</span><span class="sxs-lookup"><span data-stu-id="d9e6c-235">**StandardDayOfWeek**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9e6c-236">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="d9e6c-236">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="d9e6c-237">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d9e6c-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9e6c-238">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Time structures \| [**\_ \_ information de fuseau horaire**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wDayOfWeek")</span><span class="sxs-lookup"><span data-stu-id="d9e6c-238">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardDate\|wDayOfWeek")</span></span>
</dt> </dl>

<span data-ttu-id="d9e6c-239">Jour de la semaine où le passage de l’heure d’été à l’heure d’hiver se produit sur un système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-239">Day of the week when the transition from daylight saving time to standard time occurs on an operating system.</span></span>

<dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

<span data-ttu-id="d9e6c-240">**Dimanche** (0)</span><span class="sxs-lookup"><span data-stu-id="d9e6c-240">**Sunday** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

<span data-ttu-id="d9e6c-241">**Lundi** (1)</span><span class="sxs-lookup"><span data-stu-id="d9e6c-241">**Monday** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

<span data-ttu-id="d9e6c-242">**Mardi** (2)</span><span class="sxs-lookup"><span data-stu-id="d9e6c-242">**Tuesday** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

<span data-ttu-id="d9e6c-243">**Mercredi** (3)</span><span class="sxs-lookup"><span data-stu-id="d9e6c-243">**Wednesday** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

<span data-ttu-id="d9e6c-244">**Jeudi** (4)</span><span class="sxs-lookup"><span data-stu-id="d9e6c-244">**Thursday** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

<span data-ttu-id="d9e6c-245">**Vendredi** (5)</span><span class="sxs-lookup"><span data-stu-id="d9e6c-245">**Friday** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

<span data-ttu-id="d9e6c-246">**Samedi** (6)</span><span class="sxs-lookup"><span data-stu-id="d9e6c-246">**Saturday** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d9e6c-247">**StandardHour**</span><span class="sxs-lookup"><span data-stu-id="d9e6c-247">**StandardHour**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9e6c-248">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d9e6c-248">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d9e6c-249">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d9e6c-249">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9e6c-250">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Time structures \| [**\_ \_ information de fuseau horaire**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wHour")</span><span class="sxs-lookup"><span data-stu-id="d9e6c-250">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardDate\|wHour")</span></span>
</dt> </dl>

<span data-ttu-id="d9e6c-251">Heure de la journée à laquelle le passage de l’heure d’été à l’heure d’hiver se produit sur un système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-251">Hour of the day when the transition from daylight saving time to standard time occurs on an operating system.</span></span>

<span data-ttu-id="d9e6c-252">Exemple : 11</span><span class="sxs-lookup"><span data-stu-id="d9e6c-252">Example: 11</span></span>

</dd> <dt>

<span data-ttu-id="d9e6c-253">**StandardMillisecond**</span><span class="sxs-lookup"><span data-stu-id="d9e6c-253">**StandardMillisecond**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9e6c-254">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d9e6c-254">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d9e6c-255">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d9e6c-255">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9e6c-256">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Time structures \| [**\_ \_ information de fuseau horaire**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wMilliseconds")</span><span class="sxs-lookup"><span data-stu-id="d9e6c-256">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardDate\|wMilliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="d9e6c-257">Milliseconde du **StandardSecond** lorsque le passage de l’heure d’été à l’heure d’hiver se produit sur un système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-257">Millisecond of the **StandardSecond** when the transition from daylight saving time to standard time occurs on an operating system.</span></span>

</dd> <dt>

<span data-ttu-id="d9e6c-258">**StandardMinute**</span><span class="sxs-lookup"><span data-stu-id="d9e6c-258">**StandardMinute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9e6c-259">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d9e6c-259">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d9e6c-260">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d9e6c-260">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9e6c-261">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Time structures \| [**\_ \_ information de fuseau horaire**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wMinute")</span><span class="sxs-lookup"><span data-stu-id="d9e6c-261">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardDate\|wMinute")</span></span>
</dt> </dl>

<span data-ttu-id="d9e6c-262">Minute de **StandardDay** lorsque le passage de l’heure d’été à l’heure d’hiver se produit sur un système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-262">Minute of the **StandardDay** when the transition from daylight saving time to standard time occurs on an operating system.</span></span>

<span data-ttu-id="d9e6c-263">Exemple : 59</span><span class="sxs-lookup"><span data-stu-id="d9e6c-263">Example: 59</span></span>

</dd> <dt>

<span data-ttu-id="d9e6c-264">**StandardMonth**</span><span class="sxs-lookup"><span data-stu-id="d9e6c-264">**StandardMonth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9e6c-265">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d9e6c-265">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d9e6c-266">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d9e6c-266">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9e6c-267">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Time structures \| [**\_ \_ information de fuseau horaire**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wMonth")</span><span class="sxs-lookup"><span data-stu-id="d9e6c-267">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardDate\|wMonth")</span></span>
</dt> </dl>

<span data-ttu-id="d9e6c-268">Mois où le passage de l’heure d’été à l’heure d’hiver se produit sur un système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-268">Month when the transition from daylight saving time to standard time occurs on an operating system.</span></span>

<dt>

<span id="January"></span><span id="january"></span><span id="JANUARY"></span>

<span data-ttu-id="d9e6c-269">**Janvier** (1)</span><span class="sxs-lookup"><span data-stu-id="d9e6c-269">**January** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>

<span data-ttu-id="d9e6c-270">**Février** (2)</span><span class="sxs-lookup"><span data-stu-id="d9e6c-270">**February** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="March"></span><span id="march"></span><span id="MARCH"></span>

<span data-ttu-id="d9e6c-271">**Mars** (3)</span><span class="sxs-lookup"><span data-stu-id="d9e6c-271">**March** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="April"></span><span id="april"></span><span id="APRIL"></span>

<span data-ttu-id="d9e6c-272">**Avril** (4)</span><span class="sxs-lookup"><span data-stu-id="d9e6c-272">**April** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="May"></span><span id="may"></span><span id="MAY"></span>

<span data-ttu-id="d9e6c-273">**Mai** (5)</span><span class="sxs-lookup"><span data-stu-id="d9e6c-273">**May** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="June"></span><span id="june"></span><span id="JUNE"></span>

<span data-ttu-id="d9e6c-274">**Juin** (6)</span><span class="sxs-lookup"><span data-stu-id="d9e6c-274">**June** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="July"></span><span id="july"></span><span id="JULY"></span>

<span data-ttu-id="d9e6c-275">**Juillet** (7)</span><span class="sxs-lookup"><span data-stu-id="d9e6c-275">**July** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="August"></span><span id="august"></span><span id="AUGUST"></span>

<span data-ttu-id="d9e6c-276">**Août** (8)</span><span class="sxs-lookup"><span data-stu-id="d9e6c-276">**August** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>

<span data-ttu-id="d9e6c-277">**Septembre** (9)</span><span class="sxs-lookup"><span data-stu-id="d9e6c-277">**September** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="October"></span><span id="october"></span><span id="OCTOBER"></span>

<span data-ttu-id="d9e6c-278">**Octobre** (10)</span><span class="sxs-lookup"><span data-stu-id="d9e6c-278">**October** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>

<span data-ttu-id="d9e6c-279">**Novembre** (11)</span><span class="sxs-lookup"><span data-stu-id="d9e6c-279">**November** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="December"></span><span id="december"></span><span id="DECEMBER"></span>

<span data-ttu-id="d9e6c-280">**Décembre** (12)</span><span class="sxs-lookup"><span data-stu-id="d9e6c-280">**December** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d9e6c-281">**StandardName**</span><span class="sxs-lookup"><span data-stu-id="d9e6c-281">**StandardName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9e6c-282">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d9e6c-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9e6c-283">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d9e6c-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9e6c-284">Qualificateurs : [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Time structures \| [**\_ \_ information fuseau horaire**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardName")</span><span class="sxs-lookup"><span data-stu-id="d9e6c-284">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardName")</span></span>
</dt> </dl>

<span data-ttu-id="d9e6c-285">Nom du fuseau horaire représenté lorsque l’heure standard est en vigueur.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-285">Name of the time zone being represented when standard time is in effect.</span></span>

<span data-ttu-id="d9e6c-286">Exemple : « est » (heure d’hiver de l’est)</span><span class="sxs-lookup"><span data-stu-id="d9e6c-286">Example: "EST" (Eastern Standard Time)</span></span>

</dd> <dt>

<span data-ttu-id="d9e6c-287">**StandardSecond**</span><span class="sxs-lookup"><span data-stu-id="d9e6c-287">**StandardSecond**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9e6c-288">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d9e6c-288">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d9e6c-289">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d9e6c-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9e6c-290">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Time structures \| [**\_ \_ information de fuseau horaire**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wSecond")</span><span class="sxs-lookup"><span data-stu-id="d9e6c-290">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardDate\|wSecond")</span></span>
</dt> </dl>

<span data-ttu-id="d9e6c-291">Deuxième des **StandardMinute** lorsque le passage de l’heure d’été à l’heure d’hiver se produit sur un système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-291">Second of the **StandardMinute** when the transition from daylight saving time to standard time occurs on an operating system.</span></span>

<span data-ttu-id="d9e6c-292">Exemple : 59</span><span class="sxs-lookup"><span data-stu-id="d9e6c-292">Example: 59</span></span>

</dd> <dt>

<span data-ttu-id="d9e6c-293">**StandardYear**</span><span class="sxs-lookup"><span data-stu-id="d9e6c-293">**StandardYear**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9e6c-294">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d9e6c-294">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d9e6c-295">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d9e6c-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9e6c-296">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Time structures \| [**\_ \_ information de fuseau horaire**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wYear")</span><span class="sxs-lookup"><span data-stu-id="d9e6c-296">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardDate\|wYear")</span></span>
</dt> </dl>

<span data-ttu-id="d9e6c-297">Année lorsque l’heure standard est activée.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-297">Year when standard time is in effect.</span></span> <span data-ttu-id="d9e6c-298">Cette propriété n’est pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-298">This property is not required.</span></span>

<span data-ttu-id="d9e6c-299">Exemple : 1997</span><span class="sxs-lookup"><span data-stu-id="d9e6c-299">Example: 1997</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d9e6c-300">Notes</span><span class="sxs-lookup"><span data-stu-id="d9e6c-300">Remarks</span></span>

<span data-ttu-id="d9e6c-301">La classe **Win32 \_ TimeZone** est dérivée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="d9e6c-301">The **Win32\_TimeZone** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

<span data-ttu-id="d9e6c-302">Vous ne pouvez pas utiliser des formats de date et d’heure standard, tels que 10/18/2002-lors de l’écriture de requêtes WMI.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-302">You cannot use standard date-time formats - such as 10/18/2002 - when writing WMI queries.</span></span> <span data-ttu-id="d9e6c-303">Au lieu de cela, vous devez convertir toutes les dates utilisées dans vos requêtes au format UTC.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-303">Instead, you need to convert any dates used in your queries to UTC format.</span></span> <span data-ttu-id="d9e6c-304">Cela implique deux étapes : 1) vous devez déterminer le décalage (différence en minutes) entre votre fuseau horaire et l’heure de Greenwich, et 2) vous devez convertir 10/18/2002 en valeur UTC.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-304">This requires two steps: 1) You must determine the offset (difference in minutes) between your time zone and Greenwich Mean Time, and 2) you must convert 10/18/2002 to a UTC value.</span></span>

<span data-ttu-id="d9e6c-305">Détermination du décalage par rapport à l’heure de Greenwich</span><span class="sxs-lookup"><span data-stu-id="d9e6c-305">Determining the Offset from Greenwich Mean Time</span></span>

<span data-ttu-id="d9e6c-306">Certes, WMI complique l’utilisation des dates et heures. Heureusement, WMI au moins facilite la détermination du décalage entre votre fuseau horaire et le temps moyen de Greenwich.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-306">Admittedly, WMI makes it difficult to work with dates and times; fortunately, WMI at least makes it easy to determine the offset between your time zone and Greenwich Mean Time.</span></span> <span data-ttu-id="d9e6c-307">La classe WMI Win32 \_ TimeZone comprend une propriété-Bias-qui retourne le décalage GMT.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-307">The WMI class Win32\_TimeZone includes a property - Bias - that returns the GMT offset.</span></span>


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colTimeZone = objSWbemServices.ExecQuery _
 ("SELECT * FROM Win32_TimeZone")
For Each objTimeZone in colTimeZone
 Wscript.Echo "Offset: "& objTimeZone.Bias
Next
```



<span data-ttu-id="d9e6c-308">Conversion d’une date en valeur UTC</span><span class="sxs-lookup"><span data-stu-id="d9e6c-308">Converting a Date to a UTC Value</span></span>

<span data-ttu-id="d9e6c-309">Après avoir déterminé le décalage GMT, vous devez convertir une date standard telle que 10/18/2002 en date UTC.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-309">After you determine the GMT offset, you must then convert a standard date such as 10/18/2002 to a UTC date.</span></span> <span data-ttu-id="d9e6c-310">Pour convertir une date standard en date UTC, vous pouvez utiliser des fonctions de date VBScript telles que l’année, le mois et le jour pour isoler les composants individuels qui composent une date UTC.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-310">To convert a standard date to a UTC date, you can use VBScript date functions such as Year, Month, and Day to isolate the individual components that make up a UTC date.</span></span> <span data-ttu-id="d9e6c-311">Une fois que vous avez des valeurs individuelles pour ces composants, vous pouvez les concaténer de la même façon que vous le feriez pour toute autre valeur de chaîne.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-311">After you have individual values for these components, you can concatenate them in the same manner as you would any other string value.</span></span> <span data-ttu-id="d9e6c-312">Les dates UTC sont traitées comme des chaînes, car le décalage GMT doit être ajouté à la fin.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-312">UTC dates are treated as strings because the GMT offset must be appended to the end.</span></span> <span data-ttu-id="d9e6c-313">Si la date a été considérée comme un nombre, cette valeur :</span><span class="sxs-lookup"><span data-stu-id="d9e6c-313">If the date were seen as a number, this value:</span></span>

`20011018113047.000000-480`

<span data-ttu-id="d9e6c-314">Serait traité par erreur comme une équation mathématique (parenthèses ajoutées pour plus de clarté) :</span><span class="sxs-lookup"><span data-stu-id="d9e6c-314">Would be erroneously treated as a mathematical equation (parentheses added for clarity):</span></span>

`(20011018113047.000000) - (480)`

<span data-ttu-id="d9e6c-315">Par exemple, dans la date 10/18/2002, les composants individuels sont :</span><span class="sxs-lookup"><span data-stu-id="d9e6c-315">For example, in the date 10/18/2002, the individual components are:</span></span>

-   <span data-ttu-id="d9e6c-316">Année : 2002</span><span class="sxs-lookup"><span data-stu-id="d9e6c-316">Year: 2002</span></span>
-   <span data-ttu-id="d9e6c-317">Mois : 10</span><span class="sxs-lookup"><span data-stu-id="d9e6c-317">Month: 10</span></span>
-   <span data-ttu-id="d9e6c-318">Jour : 18</span><span class="sxs-lookup"><span data-stu-id="d9e6c-318">Day: 18</span></span>

<span data-ttu-id="d9e6c-319">Le script doit combiner ces trois valeurs, la chaîne « 113047,000000 » (représentant l’heure, y compris les millisecondes) et le décalage GMT pour dériver une date UTC.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-319">The script would need to combine these three values, the string "113047.000000" (representing the time, including milliseconds), and the GMT offset to derive a UTC date.</span></span> <span data-ttu-id="d9e6c-320">Par exemple, (à nouveau, les parenthèses ont été ajoutées pour plus de clarté) :</span><span class="sxs-lookup"><span data-stu-id="d9e6c-320">For example, (parentheses again added for clarity):</span></span>

`(2002) & (10) & (18) & (113047.000000) & (-480)`

> [!Note]  
> <span data-ttu-id="d9e6c-321">Vous pouvez utiliser les fonctions VBScript Hour, minute et second pour convertir la partie heure d’une date UTC.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-321">You can use the VBScript functions Hour, Minute, and Second to convert the time portion of a UTC date.</span></span> <span data-ttu-id="d9e6c-322">Par conséquent, une heure telle que 11:30:47 h 00</span><span class="sxs-lookup"><span data-stu-id="d9e6c-322">Thus, a time such as 11:30:47 A.M.</span></span> <span data-ttu-id="d9e6c-323">est converti en 113047.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-323">would be converted to 113047.</span></span>

 

<span data-ttu-id="d9e6c-324">Il y a un facteur de compliquation.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-324">There is one complicating factor.</span></span> <span data-ttu-id="d9e6c-325">Le mois doit prendre les positions 5 et 6 dans la chaîne ; le jour doit prendre les positions 7 et 8.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-325">The month must take up positions 5 and 6 in the string; the day must take up positions 7 and 8.</span></span> <span data-ttu-id="d9e6c-326">Il ne s’agit pas d’un problème avec le mois 10 et le jour 18.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-326">This is no problem with month 10 and day 18.</span></span> <span data-ttu-id="d9e6c-327">Mais comment pouvez-vous utiliser le 5 juillet (mois 7, jour 5) pour remplir les positions requises ?</span><span class="sxs-lookup"><span data-stu-id="d9e6c-327">But how do you get July 5 (month 7, day 5) to fill up the requisite positions?</span></span> <span data-ttu-id="d9e6c-328">La réponse consiste à ajouter un zéro non significatif à chaque valeur, ce qui a pour conséquence de remplacer 7 par 07 et 5 par 05.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-328">The answer is to add a leading zero to each value, thus changing the 7 to 07 and the 5 to 05.</span></span>

<span data-ttu-id="d9e6c-329">Pour ce faire, utilisez la fonction VBScript Len pour vérifier la longueur (nombre de caractères) du mois et du jour.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-329">To do this, use the VBScript Len function to check the length (number of characters) in the month and the day.</span></span> <span data-ttu-id="d9e6c-330">Si la longueur est égale à 1 (ce qui signifie qu’il n’y a qu’un seul caractère), ajoutez un zéro non significatif.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-330">If the length is 1 (meaning that there is just one character), add a leading zero.</span></span> <span data-ttu-id="d9e6c-331">Faisant</span><span class="sxs-lookup"><span data-stu-id="d9e6c-331">Thus:</span></span>


```VB
If Len(dtmMonth) = 1 Then
    dtmMonth = "0" & dtmMonth
End If
```



## <a name="examples"></a><span data-ttu-id="d9e6c-332">Exemples</span><span class="sxs-lookup"><span data-stu-id="d9e6c-332">Examples</span></span>

<span data-ttu-id="d9e6c-333">L’exemple VBScript suivant convertit la date actuelle en date UTC.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-333">The following VBScript example converts the current date to a UTC date.</span></span>


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colTimeZone = objSWbemServices.ExecQuery _
 ("SELECT * FROM Win32_TimeZone")
For Each objTimeZone in colTimeZone
 strBias = objTimeZone.Bias
Next

dtmCurrentDate = Date
dtmTargetDate = Year(dtmCurrentDate)

dtmMonth = Month(dtmCurrentDate)
If Len(dtmMonth) = 1 Then
 dtmMonth = "0" & dtmMonth
End If

dtmTargetDate = dtmTargetDate & dtmMonth

dtmDay = Day(dtmCurrentDate)
If Len(dtmDay) = 1 Then
 dtmDay = "0" & dtmDay
End If

dtmTargetDate = dtmTargetDate & dtmDay & "000000.000000"
dtmTargetDate = dtmTargetDate & Cstr(strBias)
```



<span data-ttu-id="d9e6c-334">Le code VBScript suivant sampledetermines le décalage GMT, puis convertit une date actuelle spécifiée (dans le cas présent, 10/18/2002) au format de date et d’heure UTC.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-334">The following VBScript sampledetermines the GMT offset, and then converts a specified current date (in this case, 10/18/2002) to UTC date-time format.</span></span> <span data-ttu-id="d9e6c-335">Une fois la date convertie, cette valeur est utilisée pour rechercher un ordinateur et retourne la liste de tous les dossiers créés après 10/18/2002.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-335">After the date has been converted, that value is used to search a computer and returns a list of all the folders that were created after 10/18/2002.</span></span>


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colTimeZone = objSWbemServices.ExecQuery _
 ("SELECT * FROM Win32_TimeZone")
For Each objTimeZone in colTimeZone
 strBias = objTimeZone.Bias
Next

dtmCurrentDate = "10/18/2002"
dtmTargetDate = Year(dtmCurrentDate)

dtmMonth = Month(dtmCurrentDate)
If Len(dtmMonth) = 1 Then
 dtmMonth = "0" & dtmMonth
End If

dtmTargetDate = dtmTargetDate & dtmMonth

dtmDay = Day(dtmCurrentDate)
If Len(dtmDay) = 1 Then
 dtmDay = "0" & dtmDay
End If

dtmTargetDate = dtmTargetDate & dtmDay & "000000.000000"
dtmTargetDate = dtmTargetDate & Cstr(strBias)

Set colFolders = objSWbemServices.ExecQuery _
 ("SELECT * FROM Win32_Directory WHERE CreationDate < '" & _
 dtmtargetDate & "'")
For Each objFolder in colFolders
 Wscript.Echo objFolder.Name
Next
```



<span data-ttu-id="d9e6c-336">L’exemple de code VBScript suivant affiche les paramètres des \_ instances TimeZone Win32.</span><span class="sxs-lookup"><span data-stu-id="d9e6c-336">The following VBScript code example displays the settings for Win32\_TimeZone instances.</span></span>


```VB
Dim arDayOrWeek(7)
arDayOrWeek(0) = "Sunday"
arDayOrWeek(1) = "Monday"
arDayOrWeek(2) = "Tuesday"
arDayOrWeek(3) = "Wednesday"
arDayOrWeek(4) = "Thursday"
arDayOrWeek(5) = "Friday"
arDayOrWeek(6) = "Saturday"

Dim arMonth(13)
arMonth(1) = "January"
arMonth(2) = "Feburary"
arMonth(3) = "March"
arMonth(4) = "April"
arMonth(5) = "May"
arMonth(6) = "June"
arMonth(7) = "July"
arMonth(8) = "August"
arMonth(9) = "September"
arMonth(10) = "October"
arMonth(11) = "November"
arMonth(12) = "December"

strComputer = "."
wmiQuery = "Select * from Win32_TimeZone"
Set objWMIService = GetObject("winmgmts:\\" & _
    strComputer & "\root\cimv2")
Set colItems = objWMIService.ExecQuery(wmiQuery)

For Each objItem in colItems
    WScript.Echo "Day of Week setting is: " _
        & objItem.dayLightDayOfWeek _
        & " which is: " & arDayOrWeek(objItem.DaylightDayOfWeek)
    WScript.Echo "Hour: " & objItem.DaylightHour 
    WScript.Echo "Month: " & objItem.DaylightMonth _
        & " which is: " & arMonth(objItem.DaylightMonth )
    WScript.Echo "Description: " & objItem.DaylightName 
    WScript.Echo "The transition from DLS to Standard occurs: " 
    WScript.Echo "Day of Week setting is: " _
        & objItem.standardDayOfWeek _
        & " which is: " & arDayOrWeek(objItem.DaylightDayOfWeek)
    WScript.Echo "Hour: " & objItem.StandardHour 
    WScript.Echo "Month: " & objItem.StandardMonth _ 
        & " which is: " & arMonth(objItem.StandardMonth )
    WScript.Echo "Description: " & objItem.StandardName 
Next

```



## <a name="requirements"></a><span data-ttu-id="d9e6c-337">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d9e6c-337">Requirements</span></span>



| <span data-ttu-id="d9e6c-338">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d9e6c-338">Requirement</span></span> | <span data-ttu-id="d9e6c-339">Valeur</span><span class="sxs-lookup"><span data-stu-id="d9e6c-339">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d9e6c-340">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d9e6c-340">Minimum supported client</span></span><br/> | <span data-ttu-id="d9e6c-341">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d9e6c-341">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d9e6c-342">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d9e6c-342">Minimum supported server</span></span><br/> | <span data-ttu-id="d9e6c-343">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d9e6c-343">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d9e6c-344">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d9e6c-344">Namespace</span></span><br/>                | <span data-ttu-id="d9e6c-345">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="d9e6c-345">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d9e6c-346">MOF</span><span class="sxs-lookup"><span data-stu-id="d9e6c-346">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d9e6c-347"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d9e6c-347"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d9e6c-348">DLL</span><span class="sxs-lookup"><span data-stu-id="d9e6c-348">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9e6c-349"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9e6c-349"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9e6c-350">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d9e6c-350">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9e6c-351">**\_Paramètre CIM**</span><span class="sxs-lookup"><span data-stu-id="d9e6c-351">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="d9e6c-352">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="d9e6c-352">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="d9e6c-353">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="d9e6c-353">**SWbemDateTime**</span></span>](../wmisdk/swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="d9e6c-354">Format de date et d’heure</span><span class="sxs-lookup"><span data-stu-id="d9e6c-354">Date and Time Format</span></span>](../wmisdk/date-and-time-format.md)
</dt> <dt>

[<span data-ttu-id="d9e6c-355">Tâches WMI : dates et heures</span><span class="sxs-lookup"><span data-stu-id="d9e6c-355">WMI Tasks: Dates and Times</span></span>](../wmisdk/wmi-tasks--dates-and-times.md)
</dt> </dl>

 

 
