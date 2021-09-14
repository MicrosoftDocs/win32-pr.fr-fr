---
description: Cette rubrique définit les identificateurs de calendrier (type de données CALID) qui sont utilisés pour spécifier des calendriers différents.
ms.assetid: ba2e841e-e24e-476a-851e-a29b3af4f04d
title: Identificateurs de calendrier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab9b931aea4a186af0849dfe8f6642c53744d364
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127240443"
---
# <a name="calendar-identifiers"></a>Identificateurs de calendrier

Cette rubrique définit les identificateurs de calendrier (type de données CALID) qui sont utilisés pour spécifier des calendriers différents. Vos applications peuvent utiliser ces identificateurs lors de l’utilisation des fonctions NLS et des fonctions de rappel suivantes, qui ont des paramètres qui prennent le type de données CALID :

-   [**ConvertSystemTimeToCalDateTime**](convertsystemtimetocaldatetime.md)
-   [**EnumCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa)
-   [**EnumCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa)
-   [**EnumCalendarInfoExEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexex)
-   [**EnumCalendarInfoProcEx**](/previous-versions/windows/desktop/legacy/dd317807(v=vs.85))
-   [**EnumDateFormatsProcEx**](/previous-versions/windows/desktop/legacy/dd317814(v=vs.85))
-   [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa)
-   [**GetCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoex)
-   [**GetCalendarSupportedDateRange**](getcalendarsupporteddaterange.md)
-   [**IsCalendarLeapYear**](iscalendarleapyear.md)
-   [**SetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-setcalendarinfoa)

Les valeurs suivantes sont définies. Toutes les autres valeurs sont réservées. Ces valeurs ne peuvent pas être combinées les unes avec les autres.



Identificateur de calendrier

Signification

1

accès client \_ grégorien

Grégorien (localisé)

2

CAL \_ grégorien ( \_ États-Unis)

Grégorien (chaînes en anglais toujours)

3

CAL \_ Japon

Ère impériale japonaise

4

CAL \_ Taïwan

Calendrier taïwanais

5

Corée de la licence d’accès client \_

Ère Tangun coréenne

6

\_HIJRI Cal

Hijri (lunaire arabe)

7

licence d’accès client \_ thaï

Thaï

8

CAL- \_ Hébreu

Hébreu (lunaire)

9

licence d’accès client \_ grégorien- \_ \_ français

Grégorien (français du Moyen-Orient)

10

CAL \_ grégorien \_ arabe

Grégorien (arabe)

11

CAL \_ grégorien \_ XLIT \_ anglais

Grégorien (transcription anglaise)

12

CAL \_ grégorien \_ XLIT \_ français

Grégorien (translittération en français)

23

\_UMALQURA Cal

**Windows Vista et versions ultérieures :** Calendrier Um al Qura (lunaire arabe)



 

> [!Note]  
> L’intervalle de numérotation entre les identificateurs CAL \_ grégorien \_ XLIT \_ français et Cal \_ UMALQURA est intentionnel. L’indicateur pour la licence d’accès client \_ UMALQURA est 23, et non 13.

 

En outre, [**EnumCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa) et [**EnumCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa) permettent d’utiliser la valeur enum \_ All \_ Calendars pour demander une énumération de tous les calendriers applicables.

Valeur

Signification

0xffffffff

ÉNUMÉRer \_ tous les \_ calendriers

Tous les calendriers applicables pour les paramètres régionaux spécifiés



 

 

 
