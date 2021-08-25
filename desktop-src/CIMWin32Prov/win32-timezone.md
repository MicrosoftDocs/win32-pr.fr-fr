---
description: Le \_ fuseau horaire Win32&\# 8194 ; la classe WMI représente les informations de fuseau horaire pour un système informatique exécutant Windows, qui comprend les modifications requises pour la transition vers la transition à l’heure d’été.
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
ms.openlocfilehash: 02b6d9d5c6100a652cf50096f5ef513fc164cfcfd2d8036e8444adc702459d1e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827659"
---
# <a name="win32_timezone-class"></a>\_Classe TimeZone Win32

la  [classe WMI](../wmisdk/retrieving-a-class.md) de **\_ fuseau horaire Win32** représente les informations de fuseau horaire pour un système informatique exécutant Windows, qui comprend les modifications requises pour la transition vers la transition à l’heure d’été.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

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

## <a name="members"></a>Membres

La classe **Win32 \_ TimeZone** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ TimeZone** possède ces propriétés.

<dl> <dt>

**Décalage**
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Time structures \| [**\_ \_ information fuseau horaire**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| Bias"), [**unités**](../wmisdk/standard-qualifiers.md) ("minutes")
</dt> </dl>

Décalage actuel pour la traduction de l’heure locale. Le biais correspond à la différence entre le temps universel coordonné (UTC, Universal Time Coordinated) et l’heure locale. Toutes les traductions entre l’heure UTC et l’heure locale sont basées sur la formule suivante : UTC = heure locale. Cette propriété est obligatoire.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Courte description textuelle de l’objet actuel.

Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).

</dd> <dt>

**DaylightBias**
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Time structures \| [**\_ \_ information de fuseau horaire**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightBias"), [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")
</dt> </dl>

Valeur de décalage à utiliser lors des traductions d’heure locales qui se produisent pendant l’heure d’été. Cette propriété est ignorée si aucune valeur n’est fournie pour la propriété **DaylightDay** . La valeur de cette propriété est ajoutée à la propriété **Bias** pour former le biais utilisé pendant l’heure d’été. Dans la plupart des fuseaux horaires, la valeur de cette propriété est-60.

</dd> <dt>

**DaylightDay**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Time structures \| [**\_ \_ information de fuseau horaire**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| WDAY")
</dt> </dl>

**DaylightDayOfWeek** du **DaylightMonth** lorsque le passage de l’heure d’hiver à l’heure d’été se produit sur ce système d’exploitation.

Exemple : si le jour de transition (**DaylightDayOfWeek**) se produit un dimanche, la valeur « 1 » indique le premier dimanche du **DaylightMonth**, « 2 » indique le deuxième dimanche, et ainsi de suite. La valeur « 5 » indique le dernier **DaylightDayOfWeek** du mois.

</dd> <dt>

**DaylightDayOfWeek**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Time structures \| [**\_ \_ information de fuseau horaire**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wDayOfWeek")
</dt> </dl>

Jour de la semaine où le passage de l’heure d’hiver à l’heure d’été se produit sur un système d’exploitation.

<dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

**Dimanche** (0)


</dt> <dd></dd> <dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

**Lundi** (1)


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

**Mardi** (2)


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

**Mercredi** (3)


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

**Jeudi** (4)


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

**Vendredi** (5)


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

**Samedi** (6)


</dt> <dd></dd> </dl>

Exemple : 1

</dd> <dt>

**DaylightHour**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Time structures \| [**\_ \_ information de fuseau horaire**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wHour")
</dt> </dl>

Heure de la journée à laquelle le passage de l’heure d’hiver à l’heure d’été se produit sur un système d’exploitation.

Exemple : 2

</dd> <dt>

**DaylightMillisecond**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Time structures \| [**\_ \_ information de fuseau horaire**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wMilliseconds")
</dt> </dl>

Milliseconde du **DaylightSecond** lorsque le passage de l’heure d’hiver à l’heure d’été se produit sur un système d’exploitation.

</dd> <dt>

**DaylightMinute**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Time structures \| [**\_ \_ information de fuseau horaire**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wMinute")
</dt> </dl>

Minute de **DaylightHour** lorsque le passage de l’heure d’hiver à l’heure d’été se produit sur un système d’exploitation.

Exemple : 59

</dd> <dt>

**DaylightMonth**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Time structures \| [**\_ \_ information de fuseau horaire**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wMonth")
</dt> </dl>

Mois où le passage de l’heure d’hiver à l’heure d’été se produit sur un système d’exploitation.

<dt>

<span id="January"></span><span id="january"></span><span id="JANUARY"></span>

**Janvier** (1)


</dt> <dd></dd> <dt>

<span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>

**Février** (2)


</dt> <dd></dd> <dt>

<span id="March"></span><span id="march"></span><span id="MARCH"></span>

**Mars** (3)


</dt> <dd></dd> <dt>

<span id="April"></span><span id="april"></span><span id="APRIL"></span>

**Avril** (4)


</dt> <dd></dd> <dt>

<span id="May"></span><span id="may"></span><span id="MAY"></span>

**Mai** (5)


</dt> <dd></dd> <dt>

<span id="June"></span><span id="june"></span><span id="JUNE"></span>

**Juin** (6)


</dt> <dd></dd> <dt>

<span id="July"></span><span id="july"></span><span id="JULY"></span>

**Juillet** (7)


</dt> <dd></dd> <dt>

<span id="August"></span><span id="august"></span><span id="AUGUST"></span>

**Août** (8)


</dt> <dd></dd> <dt>

<span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>

**Septembre** (9)


</dt> <dd></dd> <dt>

<span id="October"></span><span id="october"></span><span id="OCTOBER"></span>

**Octobre** (10)


</dt> <dd></dd> <dt>

<span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>

**Novembre** (11)


</dt> <dd></dd> <dt>

<span id="December"></span><span id="december"></span><span id="DECEMBER"></span>

**Décembre** (12)


</dt> <dd></dd> </dl>

</dd> <dt>

**DaylightName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Time structures \| [**\_ \_ information fuseau horaire**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightName")
</dt> </dl>

Fuseau horaire représenté lorsque l’heure d’été est en vigueur.

Exemple : « EDT » (heure d’été de l’est)

</dd> <dt>

**DaylightSecond**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Time structures \| [**\_ \_ information de fuseau horaire**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wSecond")
</dt> </dl>

Deuxième des **DaylightMinute** lorsque le passage de l’heure d’hiver à l’heure d’été se produit sur un système d’exploitation.

Exemple : 59

</dd> <dt>

**DaylightYear**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Time structures \| [**\_ \_ information de fuseau horaire**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wYear")
</dt> </dl>

Année lorsque l’heure d’été est en vigueur. Cette propriété n’est pas obligatoire.

Exemple : 1997

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description textuelle de l’objet actuel.

Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Identificateur par lequel l’objet actuel est connu.

Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).

</dd> <dt>

**StandardBias**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Time structures \| [**\_ \_ information de fuseau horaire**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardBias"), [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")
</dt> </dl>

Valeur de décalage à utiliser lorsque l’heure d’été n’est pas appliquée. Cette propriété est ignorée si aucune valeur n’est fournie pour **StandardDay** . La valeur de cette propriété est ajoutée à la propriété **Bias** pour former le décalage pendant l’heure standard.

Exemple : 0

</dd> <dt>

**StandardDay**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Time structures \| [**\_ \_ information de fuseau horaire**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| WDAY")
</dt> </dl>

**StandardDayOfWeek** du **StandardMonth** lorsque le passage de l’heure d’été à l’heure d’hiver se produit sur un système d’exploitation.

Si le jour de transition (**StandardDayOfWeek**) se produit un dimanche, la valeur « 1 » indique le premier dimanche du **StandardMonth**, « 2 » indique le deuxième dimanche, et ainsi de suite. La valeur « 5 » indique le dernier **StandardDayOfWeek** du mois.

</dd> <dt>

**StandardDayOfWeek**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Time structures \| [**\_ \_ information de fuseau horaire**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wDayOfWeek")
</dt> </dl>

Jour de la semaine où le passage de l’heure d’été à l’heure d’hiver se produit sur un système d’exploitation.

<dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

**Dimanche** (0)


</dt> <dd></dd> <dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

**Lundi** (1)


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

**Mardi** (2)


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

**Mercredi** (3)


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

**Jeudi** (4)


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

**Vendredi** (5)


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

**Samedi** (6)


</dt> <dd></dd> </dl>

</dd> <dt>

**StandardHour**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Time structures \| [**\_ \_ information de fuseau horaire**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wHour")
</dt> </dl>

Heure de la journée à laquelle le passage de l’heure d’été à l’heure d’hiver se produit sur un système d’exploitation.

Exemple : 11

</dd> <dt>

**StandardMillisecond**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Time structures \| [**\_ \_ information de fuseau horaire**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wMilliseconds")
</dt> </dl>

Milliseconde du **StandardSecond** lorsque le passage de l’heure d’été à l’heure d’hiver se produit sur un système d’exploitation.

</dd> <dt>

**StandardMinute**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Time structures \| [**\_ \_ information de fuseau horaire**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wMinute")
</dt> </dl>

Minute de **StandardDay** lorsque le passage de l’heure d’été à l’heure d’hiver se produit sur un système d’exploitation.

Exemple : 59

</dd> <dt>

**StandardMonth**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Time structures \| [**\_ \_ information de fuseau horaire**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wMonth")
</dt> </dl>

Mois où le passage de l’heure d’été à l’heure d’hiver se produit sur un système d’exploitation.

<dt>

<span id="January"></span><span id="january"></span><span id="JANUARY"></span>

**Janvier** (1)


</dt> <dd></dd> <dt>

<span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>

**Février** (2)


</dt> <dd></dd> <dt>

<span id="March"></span><span id="march"></span><span id="MARCH"></span>

**Mars** (3)


</dt> <dd></dd> <dt>

<span id="April"></span><span id="april"></span><span id="APRIL"></span>

**Avril** (4)


</dt> <dd></dd> <dt>

<span id="May"></span><span id="may"></span><span id="MAY"></span>

**Mai** (5)


</dt> <dd></dd> <dt>

<span id="June"></span><span id="june"></span><span id="JUNE"></span>

**Juin** (6)


</dt> <dd></dd> <dt>

<span id="July"></span><span id="july"></span><span id="JULY"></span>

**Juillet** (7)


</dt> <dd></dd> <dt>

<span id="August"></span><span id="august"></span><span id="AUGUST"></span>

**Août** (8)


</dt> <dd></dd> <dt>

<span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>

**Septembre** (9)


</dt> <dd></dd> <dt>

<span id="October"></span><span id="october"></span><span id="OCTOBER"></span>

**Octobre** (10)


</dt> <dd></dd> <dt>

<span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>

**Novembre** (11)


</dt> <dd></dd> <dt>

<span id="December"></span><span id="december"></span><span id="DECEMBER"></span>

**Décembre** (12)


</dt> <dd></dd> </dl>

</dd> <dt>

**StandardName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Time structures \| [**\_ \_ information fuseau horaire**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardName")
</dt> </dl>

Nom du fuseau horaire représenté lorsque l’heure standard est en vigueur.

Exemple : « est » (heure d’hiver de l’est)

</dd> <dt>

**StandardSecond**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Time structures \| [**\_ \_ information de fuseau horaire**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wSecond")
</dt> </dl>

Deuxième des **StandardMinute** lorsque le passage de l’heure d’été à l’heure d’hiver se produit sur un système d’exploitation.

Exemple : 59

</dd> <dt>

**StandardYear**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Time structures \| [**\_ \_ information de fuseau horaire**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wYear")
</dt> </dl>

Année lorsque l’heure standard est activée. Cette propriété n’est pas obligatoire.

Exemple : 1997

</dd> </dl>

## <a name="remarks"></a>Remarques

La classe **Win32 \_ TimeZone** est dérivée [**du \_ paramètre CIM**](cim-setting.md).

Vous ne pouvez pas utiliser des formats de date et d’heure standard, tels que 10/18/2002-lors de l’écriture de requêtes WMI. Au lieu de cela, vous devez convertir toutes les dates utilisées dans vos requêtes au format UTC. Cela implique deux étapes : 1) vous devez déterminer le décalage (différence en minutes) entre votre fuseau horaire et l’heure de Greenwich, et 2) vous devez convertir 10/18/2002 en valeur UTC.

Détermination du décalage par rapport à l’heure de Greenwich

Certes, WMI complique l’utilisation des dates et heures. Heureusement, WMI au moins facilite la détermination du décalage entre votre fuseau horaire et le temps moyen de Greenwich. La classe WMI Win32 \_ TimeZone comprend une propriété-Bias-qui retourne le décalage GMT.


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



Conversion d’une date en valeur UTC

Après avoir déterminé le décalage GMT, vous devez convertir une date standard telle que 10/18/2002 en date UTC. Pour convertir une date standard en date UTC, vous pouvez utiliser des fonctions de date VBScript telles que l’année, le mois et le jour pour isoler les composants individuels qui composent une date UTC. Une fois que vous avez des valeurs individuelles pour ces composants, vous pouvez les concaténer de la même façon que vous le feriez pour toute autre valeur de chaîne. Les dates UTC sont traitées comme des chaînes, car le décalage GMT doit être ajouté à la fin. Si la date a été considérée comme un nombre, cette valeur :

`20011018113047.000000-480`

Serait traité par erreur comme une équation mathématique (parenthèses ajoutées pour plus de clarté) :

`(20011018113047.000000) - (480)`

Par exemple, dans la date 10/18/2002, les composants individuels sont :

-   Année : 2002
-   Mois : 10
-   Jour : 18

Le script doit combiner ces trois valeurs, la chaîne « 113047,000000 » (représentant l’heure, y compris les millisecondes) et le décalage GMT pour dériver une date UTC. Par exemple, (à nouveau, les parenthèses ont été ajoutées pour plus de clarté) :

`(2002) & (10) & (18) & (113047.000000) & (-480)`

> [!Note]  
> Vous pouvez utiliser les fonctions VBScript Hour, minute et second pour convertir la partie heure d’une date UTC. Par conséquent, une heure telle que 11:30:47 h 00 est converti en 113047.

 

Il y a un facteur de compliquation. Le mois doit prendre les positions 5 et 6 dans la chaîne ; le jour doit prendre les positions 7 et 8. Il ne s’agit pas d’un problème avec le mois 10 et le jour 18. Mais comment pouvez-vous utiliser le 5 juillet (mois 7, jour 5) pour remplir les positions requises ? La réponse consiste à ajouter un zéro non significatif à chaque valeur, ce qui a pour conséquence de remplacer 7 par 07 et 5 par 05.

Pour ce faire, utilisez la fonction VBScript Len pour vérifier la longueur (nombre de caractères) du mois et du jour. Si la longueur est égale à 1 (ce qui signifie qu’il n’y a qu’un seul caractère), ajoutez un zéro non significatif. Faisant


```VB
If Len(dtmMonth) = 1 Then
    dtmMonth = "0" & dtmMonth
End If
```



## <a name="examples"></a>Exemples

L’exemple VBScript suivant convertit la date actuelle en date UTC.


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



Le code VBScript suivant sampledetermines le décalage GMT, puis convertit une date actuelle spécifiée (dans le cas présent, 10/18/2002) au format de date et d’heure UTC. Une fois la date convertie, cette valeur est utilisée pour rechercher un ordinateur et retourne la liste de tous les dossiers créés après 10/18/2002.


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



L’exemple de code VBScript suivant affiche les paramètres des \_ instances TimeZone Win32.


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



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Paramètre CIM**](cim-setting.md)
</dt> <dt>

[Classes du système d’exploitation](./operating-system-classes.md)
</dt> <dt>

[**SWbemDateTime**](../wmisdk/swbemdatetime.md)
</dt> <dt>

[Format de date et d’heure](../wmisdk/date-and-time-format.md)
</dt> <dt>

[Tâches WMI : dates et heures](../wmisdk/wmi-tasks--dates-and-times.md)
</dt> </dl>

 

 
