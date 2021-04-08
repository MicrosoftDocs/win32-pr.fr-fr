---
description: Cette rubrique définit les identificateurs de calendrier (type de données CALID) qui sont utilisés pour spécifier des calendriers différents.
ms.assetid: ba2e841e-e24e-476a-851e-a29b3af4f04d
title: Identificateurs de calendrier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab9b931aea4a186af0849dfe8f6642c53744d364
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751156"
---
# <a name="calendar-identifiers"></a><span data-ttu-id="068db-103">Identificateurs de calendrier</span><span class="sxs-lookup"><span data-stu-id="068db-103">Calendar Identifiers</span></span>

<span data-ttu-id="068db-104">Cette rubrique définit les identificateurs de calendrier (type de données CALID) qui sont utilisés pour spécifier des calendriers différents.</span><span class="sxs-lookup"><span data-stu-id="068db-104">This topic defines the calendar identifiers (data type CALID) that are used to specify different calendars.</span></span> <span data-ttu-id="068db-105">Vos applications peuvent utiliser ces identificateurs lors de l’utilisation des fonctions NLS et des fonctions de rappel suivantes, qui ont des paramètres qui prennent le type de données CALID :</span><span class="sxs-lookup"><span data-stu-id="068db-105">Your applications can use these identifiers when using the following NLS functions and callback functions, which have parameters that take the CALID data type:</span></span>

-   [<span data-ttu-id="068db-106">**ConvertSystemTimeToCalDateTime**</span><span class="sxs-lookup"><span data-stu-id="068db-106">**ConvertSystemTimeToCalDateTime**</span></span>](convertsystemtimetocaldatetime.md)
-   [<span data-ttu-id="068db-107">**EnumCalendarInfo**</span><span class="sxs-lookup"><span data-stu-id="068db-107">**EnumCalendarInfo**</span></span>](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa)
-   [<span data-ttu-id="068db-108">**EnumCalendarInfoEx**</span><span class="sxs-lookup"><span data-stu-id="068db-108">**EnumCalendarInfoEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa)
-   [<span data-ttu-id="068db-109">**EnumCalendarInfoExEx**</span><span class="sxs-lookup"><span data-stu-id="068db-109">**EnumCalendarInfoExEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexex)
-   <span data-ttu-id="068db-110">[**EnumCalendarInfoProcEx**](/previous-versions/windows/desktop/legacy/dd317807(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="068db-110">[**EnumCalendarInfoProcEx**](/previous-versions/windows/desktop/legacy/dd317807(v=vs.85))</span></span>
-   <span data-ttu-id="068db-111">[**EnumDateFormatsProcEx**](/previous-versions/windows/desktop/legacy/dd317814(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="068db-111">[**EnumDateFormatsProcEx**](/previous-versions/windows/desktop/legacy/dd317814(v=vs.85))</span></span>
-   [<span data-ttu-id="068db-112">**GetCalendarInfo**</span><span class="sxs-lookup"><span data-stu-id="068db-112">**GetCalendarInfo**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa)
-   [<span data-ttu-id="068db-113">**GetCalendarInfoEx**</span><span class="sxs-lookup"><span data-stu-id="068db-113">**GetCalendarInfoEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoex)
-   [<span data-ttu-id="068db-114">**GetCalendarSupportedDateRange**</span><span class="sxs-lookup"><span data-stu-id="068db-114">**GetCalendarSupportedDateRange**</span></span>](getcalendarsupporteddaterange.md)
-   [<span data-ttu-id="068db-115">**IsCalendarLeapYear**</span><span class="sxs-lookup"><span data-stu-id="068db-115">**IsCalendarLeapYear**</span></span>](iscalendarleapyear.md)
-   [<span data-ttu-id="068db-116">**SetCalendarInfo**</span><span class="sxs-lookup"><span data-stu-id="068db-116">**SetCalendarInfo**</span></span>](/windows/desktop/api/Winnls/nf-winnls-setcalendarinfoa)

<span data-ttu-id="068db-117">Les valeurs suivantes sont définies.</span><span class="sxs-lookup"><span data-stu-id="068db-117">The following values are defined.</span></span> <span data-ttu-id="068db-118">Toutes les autres valeurs sont réservées.</span><span class="sxs-lookup"><span data-stu-id="068db-118">All other values are reserved.</span></span> <span data-ttu-id="068db-119">Ces valeurs ne peuvent pas être combinées les unes avec les autres.</span><span class="sxs-lookup"><span data-stu-id="068db-119">These values cannot be combined with one another.</span></span>



<span data-ttu-id="068db-120">Identificateur de calendrier</span><span class="sxs-lookup"><span data-stu-id="068db-120">Calendar identifier</span></span>

<span data-ttu-id="068db-121">Signification</span><span class="sxs-lookup"><span data-stu-id="068db-121">Meaning</span></span>

<span data-ttu-id="068db-122">1</span><span class="sxs-lookup"><span data-stu-id="068db-122">1</span></span>

<span data-ttu-id="068db-123">accès client \_ grégorien</span><span class="sxs-lookup"><span data-stu-id="068db-123">CAL\_GREGORIAN</span></span>

<span data-ttu-id="068db-124">Grégorien (localisé)</span><span class="sxs-lookup"><span data-stu-id="068db-124">Gregorian (localized)</span></span>

<span data-ttu-id="068db-125">2</span><span class="sxs-lookup"><span data-stu-id="068db-125">2</span></span>

<span data-ttu-id="068db-126">CAL \_ grégorien ( \_ États-Unis)</span><span class="sxs-lookup"><span data-stu-id="068db-126">CAL\_GREGORIAN\_US</span></span>

<span data-ttu-id="068db-127">Grégorien (chaînes en anglais toujours)</span><span class="sxs-lookup"><span data-stu-id="068db-127">Gregorian (English strings always)</span></span>

<span data-ttu-id="068db-128">3</span><span class="sxs-lookup"><span data-stu-id="068db-128">3</span></span>

<span data-ttu-id="068db-129">CAL \_ Japon</span><span class="sxs-lookup"><span data-stu-id="068db-129">CAL\_JAPAN</span></span>

<span data-ttu-id="068db-130">Ère impériale japonaise</span><span class="sxs-lookup"><span data-stu-id="068db-130">Japanese Emperor Era</span></span>

<span data-ttu-id="068db-131">4</span><span class="sxs-lookup"><span data-stu-id="068db-131">4</span></span>

<span data-ttu-id="068db-132">CAL \_ Taïwan</span><span class="sxs-lookup"><span data-stu-id="068db-132">CAL\_TAIWAN</span></span>

<span data-ttu-id="068db-133">Calendrier taïwanais</span><span class="sxs-lookup"><span data-stu-id="068db-133">Taiwan calendar</span></span>

<span data-ttu-id="068db-134">5</span><span class="sxs-lookup"><span data-stu-id="068db-134">5</span></span>

<span data-ttu-id="068db-135">Corée de la licence d’accès client \_</span><span class="sxs-lookup"><span data-stu-id="068db-135">CAL\_KOREA</span></span>

<span data-ttu-id="068db-136">Ère Tangun coréenne</span><span class="sxs-lookup"><span data-stu-id="068db-136">Korean Tangun Era</span></span>

<span data-ttu-id="068db-137">6</span><span class="sxs-lookup"><span data-stu-id="068db-137">6</span></span>

<span data-ttu-id="068db-138">\_HIJRI Cal</span><span class="sxs-lookup"><span data-stu-id="068db-138">CAL\_HIJRI</span></span>

<span data-ttu-id="068db-139">Hijri (lunaire arabe)</span><span class="sxs-lookup"><span data-stu-id="068db-139">Hijri (Arabic Lunar)</span></span>

<span data-ttu-id="068db-140">7</span><span class="sxs-lookup"><span data-stu-id="068db-140">7</span></span>

<span data-ttu-id="068db-141">licence d’accès client \_ thaï</span><span class="sxs-lookup"><span data-stu-id="068db-141">CAL\_THAI</span></span>

<span data-ttu-id="068db-142">Thaï</span><span class="sxs-lookup"><span data-stu-id="068db-142">Thai</span></span>

<span data-ttu-id="068db-143">8</span><span class="sxs-lookup"><span data-stu-id="068db-143">8</span></span>

<span data-ttu-id="068db-144">CAL- \_ Hébreu</span><span class="sxs-lookup"><span data-stu-id="068db-144">CAL\_HEBREW</span></span>

<span data-ttu-id="068db-145">Hébreu (lunaire)</span><span class="sxs-lookup"><span data-stu-id="068db-145">Hebrew (Lunar)</span></span>

<span data-ttu-id="068db-146">9</span><span class="sxs-lookup"><span data-stu-id="068db-146">9</span></span>

<span data-ttu-id="068db-147">licence d’accès client \_ grégorien- \_ \_ français</span><span class="sxs-lookup"><span data-stu-id="068db-147">CAL\_GREGORIAN\_ME\_FRENCH</span></span>

<span data-ttu-id="068db-148">Grégorien (français du Moyen-Orient)</span><span class="sxs-lookup"><span data-stu-id="068db-148">Gregorian Middle East French</span></span>

<span data-ttu-id="068db-149">10</span><span class="sxs-lookup"><span data-stu-id="068db-149">10</span></span>

<span data-ttu-id="068db-150">CAL \_ grégorien \_ arabe</span><span class="sxs-lookup"><span data-stu-id="068db-150">CAL\_GREGORIAN\_ARABIC</span></span>

<span data-ttu-id="068db-151">Grégorien (arabe)</span><span class="sxs-lookup"><span data-stu-id="068db-151">Gregorian Arabic</span></span>

<span data-ttu-id="068db-152">11</span><span class="sxs-lookup"><span data-stu-id="068db-152">11</span></span>

<span data-ttu-id="068db-153">CAL \_ grégorien \_ XLIT \_ anglais</span><span class="sxs-lookup"><span data-stu-id="068db-153">CAL\_GREGORIAN\_XLIT\_ENGLISH</span></span>

<span data-ttu-id="068db-154">Grégorien (transcription anglaise)</span><span class="sxs-lookup"><span data-stu-id="068db-154">Gregorian transliterated English</span></span>

<span data-ttu-id="068db-155">12</span><span class="sxs-lookup"><span data-stu-id="068db-155">12</span></span>

<span data-ttu-id="068db-156">CAL \_ grégorien \_ XLIT \_ français</span><span class="sxs-lookup"><span data-stu-id="068db-156">CAL\_GREGORIAN\_XLIT\_FRENCH</span></span>

<span data-ttu-id="068db-157">Grégorien (translittération en français)</span><span class="sxs-lookup"><span data-stu-id="068db-157">Gregorian transliterated French</span></span>

<span data-ttu-id="068db-158">23</span><span class="sxs-lookup"><span data-stu-id="068db-158">23</span></span>

<span data-ttu-id="068db-159">\_UMALQURA Cal</span><span class="sxs-lookup"><span data-stu-id="068db-159">CAL\_UMALQURA</span></span>

<span data-ttu-id="068db-160">**Windows Vista et versions ultérieures :** Calendrier Um al Qura (lunaire arabe)</span><span class="sxs-lookup"><span data-stu-id="068db-160">**Windows Vista and later:** Um Al Qura (Arabic lunar) calendar</span></span>



 

> [!Note]  
> <span data-ttu-id="068db-161">L’intervalle de numérotation entre les identificateurs CAL \_ grégorien \_ XLIT \_ français et Cal \_ UMALQURA est intentionnel.</span><span class="sxs-lookup"><span data-stu-id="068db-161">The gap in numbering between the identifiers CAL\_GREGORIAN\_XLIT\_FRENCH and CAL\_UMALQURA is intentional.</span></span> <span data-ttu-id="068db-162">L’indicateur pour la licence d’accès client \_ UMALQURA est 23, et non 13.</span><span class="sxs-lookup"><span data-stu-id="068db-162">The designator for CAL\_UMALQURA is 23, not 13.</span></span>

 

<span data-ttu-id="068db-163">En outre, [**EnumCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa) et [**EnumCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa) permettent d’utiliser la valeur enum \_ All \_ Calendars pour demander une énumération de tous les calendriers applicables.</span><span class="sxs-lookup"><span data-stu-id="068db-163">In addition, [**EnumCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa) and [**EnumCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa) allow the use of the value ENUM\_ALL\_CALENDARS to request an enumeration of all applicable calendars.</span></span>

<span data-ttu-id="068db-164">Valeur</span><span class="sxs-lookup"><span data-stu-id="068db-164">Value</span></span>

<span data-ttu-id="068db-165">Signification</span><span class="sxs-lookup"><span data-stu-id="068db-165">Meaning</span></span>

<span data-ttu-id="068db-166">égale</span><span class="sxs-lookup"><span data-stu-id="068db-166">0xffffffff</span></span>

<span data-ttu-id="068db-167">ÉNUMÉRer \_ tous les \_ calendriers</span><span class="sxs-lookup"><span data-stu-id="068db-167">ENUM\_ALL\_CALENDARS</span></span>

<span data-ttu-id="068db-168">Tous les calendriers applicables pour les paramètres régionaux spécifiés</span><span class="sxs-lookup"><span data-stu-id="068db-168">All applicable calendars for the specified locale</span></span>



 

 

 
