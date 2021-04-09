---
description: Cette rubrique décrit les informations de type de calendrier (type de données CALTYPE) utilisées dans les fonctions EnumCalendarInfo, EnumCalendarInfoEx, EnumCalendarInfoExEx, GetCalendarInfo et GetCalendarInfoEx.
ms.assetid: 33361a97-0f27-477a-a0ee-3d4d3aaeaacf
title: Informations sur le type de calendrier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17a8e334a1b05f372f51c81ab8158294d46eebfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867946"
---
# <a name="calendar-type-information"></a><span data-ttu-id="1f52e-103">Informations sur le type de calendrier</span><span class="sxs-lookup"><span data-stu-id="1f52e-103">Calendar Type Information</span></span>

<span data-ttu-id="1f52e-104">Cette rubrique décrit les informations de type de calendrier (type de données CALTYPE) utilisées dans les fonctions [**EnumCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa), [**EnumCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa), [**EnumCalendarInfoExEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexex), [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa)et [**GetCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoex) .</span><span class="sxs-lookup"><span data-stu-id="1f52e-104">This topic describes the calendar type information (CALTYPE data type) used in the [**EnumCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa), [**EnumCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa), [**EnumCalendarInfoExEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexex), [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa), and [**GetCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoex) functions.</span></span> <span data-ttu-id="1f52e-105">Certaines de ces valeurs sont également utilisées par la fonction [**SetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-setcalendarinfoa) .</span><span class="sxs-lookup"><span data-stu-id="1f52e-105">Some of these values are also used by the [**SetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-setcalendarinfoa) function.</span></span>

<span data-ttu-id="1f52e-106">Les constantes CALTYPE suivantes peuvent être utilisées en association avec d’autres constantes CALTYPE.</span><span class="sxs-lookup"><span data-stu-id="1f52e-106">The following CALTYPE constants can be used in combination with any other CALTYPE constants.</span></span>



| <span data-ttu-id="1f52e-107">Constante</span><span class="sxs-lookup"><span data-stu-id="1f52e-107">Constant</span></span>                     | <span data-ttu-id="1f52e-108">Description</span><span class="sxs-lookup"><span data-stu-id="1f52e-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f52e-109">\_NOUSEROVERRIDE Cal</span><span class="sxs-lookup"><span data-stu-id="1f52e-109">CAL\_NOUSEROVERRIDE</span></span>          | <span data-ttu-id="1f52e-110">**Windows Me/98, windows 2000 :** Utilisez la valeur par défaut du système au lieu du choix de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1f52e-110">**Windows Me/98, Windows 2000:** Use the system default instead of the user's choice.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="1f52e-111">\_ \_ noms génitif de retour de licence d’accès client \_</span><span class="sxs-lookup"><span data-stu-id="1f52e-111">CAL\_RETURN\_GENITIVE\_NAMES</span></span> | <span data-ttu-id="1f52e-112">**Windows 7 et versions ultérieures :** Récupérez le résultat de [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) sous la forme de noms génitif de mois, qui sont les noms utilisés lorsque les noms de mois sont combinés à d’autres éléments.</span><span class="sxs-lookup"><span data-stu-id="1f52e-112">**Windows 7 and later:** Retrieve the result from [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) in the form of genitive names of months, which are the names used when the month names are combined with other items.</span></span> <span data-ttu-id="1f52e-113">Par exemple, en ukrainien, l’équivalent de janvier est écrit « Січень » lorsque le mois est nommé seul.</span><span class="sxs-lookup"><span data-stu-id="1f52e-113">For example, in Ukrainian the equivalent of January is written "Січень" when the month is named alone.</span></span> <span data-ttu-id="1f52e-114">Toutefois, lorsque le nom du mois est utilisé en combinaison, par exemple, dans une date telle que le 5 janvier 2003, la forme génitif du nom est utilisée.</span><span class="sxs-lookup"><span data-stu-id="1f52e-114">However, when the month name is used in combination, for example, in a date such as January 5th, 2003, the genitive form of the name is used.</span></span> <span data-ttu-id="1f52e-115">Pour l’exemple ukrainien, le nom du mois génitif est affiché sous la forme « 5 січня 2003 ».</span><span class="sxs-lookup"><span data-stu-id="1f52e-115">For the Ukrainian example, the genitive month name is displayed as "5 січня 2003".</span></span> <span data-ttu-id="1f52e-116">Pour plus d’informations, consultez [ \_ \_ \_ noms de paramètres régionaux](locale-return-constants.md).</span><span class="sxs-lookup"><span data-stu-id="1f52e-116">For more information, see [LOCALE\_RETURN\_GENITIVE\_NAMES](locale-return-constants.md).</span></span> |
| <span data-ttu-id="1f52e-117">\_numéro de retour Cal \_</span><span class="sxs-lookup"><span data-stu-id="1f52e-117">CAL\_RETURN\_NUMBER</span></span>          | <span data-ttu-id="1f52e-118">**Windows Me/98, windows 2000 :** Récupère le résultat de [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) sous la forme d’un nombre au lieu d’une chaîne.</span><span class="sxs-lookup"><span data-stu-id="1f52e-118">**Windows Me/98, Windows 2000:** Retrieve the result from [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) as a number instead of a string.</span></span> <span data-ttu-id="1f52e-119">Cela n’est valide que pour les valeurs commençant par la licence d’accès client \_ I.</span><span class="sxs-lookup"><span data-stu-id="1f52e-119">This is only valid for values beginning with CAL\_I.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="1f52e-120">CAL- \_ utiliser \_ CP \_ ACP</span><span class="sxs-lookup"><span data-stu-id="1f52e-120">CAL\_USE\_CP\_ACP</span></span>            | <span data-ttu-id="1f52e-121">**Windows Me/98, windows 2000 :** Utilisez la page de codes ANSI du système au lieu de la page de codes des paramètres régionaux pour la conversion de chaînes.</span><span class="sxs-lookup"><span data-stu-id="1f52e-121">**Windows Me/98, Windows 2000:** Use the system ANSI code page (ACP) instead of the locale code page for string translation.</span></span> <span data-ttu-id="1f52e-122">Cela s’applique uniquement aux versions ANSI des fonctions, par exemple **EnumCalendarInfoA**.</span><span class="sxs-lookup"><span data-stu-id="1f52e-122">This is only relevant for ANSI versions of functions, for example, **EnumCalendarInfoA**.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

<span data-ttu-id="1f52e-123">Les constantes CALTYPE suivantes s’excluent mutuellement et ne peuvent pas être utilisées en combinaison les unes avec les autres dans un appel de fonction.</span><span class="sxs-lookup"><span data-stu-id="1f52e-123">The following CALTYPE constants are mutually exclusive and cannot be used in combination with each other in a function call.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1f52e-124">Constante</span><span class="sxs-lookup"><span data-stu-id="1f52e-124">Constant</span></span></th>
<th><span data-ttu-id="1f52e-125">Description</span><span class="sxs-lookup"><span data-stu-id="1f52e-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1f52e-126">CAL_ICALINTVALUE</span><span class="sxs-lookup"><span data-stu-id="1f52e-126">CAL_ICALINTVALUE</span></span></td>
<td><span data-ttu-id="1f52e-127">Valeur entière indiquant le type de calendrier de l’autre calendrier.</span><span class="sxs-lookup"><span data-stu-id="1f52e-127">An integer value indicating the calendar type of the alternate calendar.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f52e-128">CAL_ITWODIGITYEARMAX</span><span class="sxs-lookup"><span data-stu-id="1f52e-128">CAL_ITWODIGITYEARMAX</span></span></td>
<td><span data-ttu-id="1f52e-129"><strong>Windows Me/98, windows 2000 :</strong> Valeur entière indiquant la limite supérieure de la plage d’années à deux chiffres.</span><span class="sxs-lookup"><span data-stu-id="1f52e-129"><strong>Windows Me/98, Windows 2000:</strong> An integer value indicating the upper boundary of the two-digit year range.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f52e-130">CAL_IYEAROFFSETRANGE</span><span class="sxs-lookup"><span data-stu-id="1f52e-130">CAL_IYEAROFFSETRANGE</span></span></td>
<td><span data-ttu-id="1f52e-131">Une ou plusieurs chaînes se terminant par un caractère null qui spécifient les décalages d’année pour chaque plage d’ère.</span><span class="sxs-lookup"><span data-stu-id="1f52e-131">One or more null-terminated strings that specify the year offsets for each of the era ranges.</span></span> <span data-ttu-id="1f52e-132">La dernière chaîne comporte un caractère null de fin supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="1f52e-132">The last string has an extra terminating null character.</span></span> <span data-ttu-id="1f52e-133">Cette valeur varie en fonction du type de calendrier facultatif.</span><span class="sxs-lookup"><span data-stu-id="1f52e-133">This value varies in format depending on the type of optional calendar.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f52e-134">CAL_SABBREVDAYNAME1</span><span class="sxs-lookup"><span data-stu-id="1f52e-134">CAL_SABBREVDAYNAME1</span></span></td>
<td><span data-ttu-id="1f52e-135">Nom natif abrégé du premier jour de la semaine.</span><span class="sxs-lookup"><span data-stu-id="1f52e-135">Abbreviated native name of the first day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f52e-136">CAL_SABBREVDAYNAME2</span><span class="sxs-lookup"><span data-stu-id="1f52e-136">CAL_SABBREVDAYNAME2</span></span></td>
<td><span data-ttu-id="1f52e-137">Nom natif abrégé du deuxième jour de la semaine.</span><span class="sxs-lookup"><span data-stu-id="1f52e-137">Abbreviated native name of the second day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f52e-138">CAL_SABBREVDAYNAME3</span><span class="sxs-lookup"><span data-stu-id="1f52e-138">CAL_SABBREVDAYNAME3</span></span></td>
<td><span data-ttu-id="1f52e-139">Nom natif abrégé du troisième jour de la semaine.</span><span class="sxs-lookup"><span data-stu-id="1f52e-139">Abbreviated native name of the third day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f52e-140">CAL_SABBREVDAYNAME4</span><span class="sxs-lookup"><span data-stu-id="1f52e-140">CAL_SABBREVDAYNAME4</span></span></td>
<td><span data-ttu-id="1f52e-141">Nom natif abrégé du quatrième jour de la semaine.</span><span class="sxs-lookup"><span data-stu-id="1f52e-141">Abbreviated native name of the fourth day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f52e-142">CAL_SABBREVDAYNAME5</span><span class="sxs-lookup"><span data-stu-id="1f52e-142">CAL_SABBREVDAYNAME5</span></span></td>
<td><span data-ttu-id="1f52e-143">Nom natif abrégé du cinquième jour de la semaine.</span><span class="sxs-lookup"><span data-stu-id="1f52e-143">Abbreviated native name of the fifth day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f52e-144">CAL_SABBREVDAYNAME6</span><span class="sxs-lookup"><span data-stu-id="1f52e-144">CAL_SABBREVDAYNAME6</span></span></td>
<td><span data-ttu-id="1f52e-145">Nom natif abrégé du sixième jour de la semaine.</span><span class="sxs-lookup"><span data-stu-id="1f52e-145">Abbreviated native name of the sixth day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f52e-146">CAL_SABBREVDAYNAME7</span><span class="sxs-lookup"><span data-stu-id="1f52e-146">CAL_SABBREVDAYNAME7</span></span></td>
<td><span data-ttu-id="1f52e-147">Nom natif abrégé du septième jour de la semaine.</span><span class="sxs-lookup"><span data-stu-id="1f52e-147">Abbreviated native name of the seventh day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f52e-148">CAL_SABBREVERASTRING</span><span class="sxs-lookup"><span data-stu-id="1f52e-148">CAL_SABBREVERASTRING</span></span></td>
<td><span data-ttu-id="1f52e-149"><strong>Windows 7 et versions ultérieures :</strong> Nom natif abrégé d’une ère.</span><span class="sxs-lookup"><span data-stu-id="1f52e-149"><strong>Windows 7 and later:</strong> Abbreviated native name of an era.</span></span> <span data-ttu-id="1f52e-150">L’ère complète est représentée par la constante CAL_SERASTRING.</span><span class="sxs-lookup"><span data-stu-id="1f52e-150">The full era is represented by the CAL_SERASTRING constant.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f52e-151">CAL_SABBREVMONTHNAME1</span><span class="sxs-lookup"><span data-stu-id="1f52e-151">CAL_SABBREVMONTHNAME1</span></span></td>
<td><span data-ttu-id="1f52e-152">Nom natif abrégé du premier mois de l’année.</span><span class="sxs-lookup"><span data-stu-id="1f52e-152">Abbreviated native name of the first month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f52e-153">CAL_SABBREVMONTHNAME2</span><span class="sxs-lookup"><span data-stu-id="1f52e-153">CAL_SABBREVMONTHNAME2</span></span></td>
<td><span data-ttu-id="1f52e-154">Nom natif abrégé du deuxième mois de l’année.</span><span class="sxs-lookup"><span data-stu-id="1f52e-154">Abbreviated native name of the second month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f52e-155">CAL_SABBREVMONTHNAME3</span><span class="sxs-lookup"><span data-stu-id="1f52e-155">CAL_SABBREVMONTHNAME3</span></span></td>
<td><span data-ttu-id="1f52e-156">Nom natif abrégé du troisième mois de l’année.</span><span class="sxs-lookup"><span data-stu-id="1f52e-156">Abbreviated native name of the third month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f52e-157">CAL_SABBREVMONTHNAME4</span><span class="sxs-lookup"><span data-stu-id="1f52e-157">CAL_SABBREVMONTHNAME4</span></span></td>
<td><span data-ttu-id="1f52e-158">Nom natif abrégé du quatrième mois de l’année.</span><span class="sxs-lookup"><span data-stu-id="1f52e-158">Abbreviated native name of the fourth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f52e-159">CAL_SABBREVMONTHNAME5</span><span class="sxs-lookup"><span data-stu-id="1f52e-159">CAL_SABBREVMONTHNAME5</span></span></td>
<td><span data-ttu-id="1f52e-160">Nom natif abrégé du cinquième mois de l’année.</span><span class="sxs-lookup"><span data-stu-id="1f52e-160">Abbreviated native name of the fifth month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f52e-161">CAL_SABBREVMONTHNAME6</span><span class="sxs-lookup"><span data-stu-id="1f52e-161">CAL_SABBREVMONTHNAME6</span></span></td>
<td><span data-ttu-id="1f52e-162">Nom natif abrégé du sixième mois de l’année.</span><span class="sxs-lookup"><span data-stu-id="1f52e-162">Abbreviated native name of the sixth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f52e-163">CAL_SABBREVMONTHNAME7</span><span class="sxs-lookup"><span data-stu-id="1f52e-163">CAL_SABBREVMONTHNAME7</span></span></td>
<td><span data-ttu-id="1f52e-164">Nom natif abrégé du septième mois de l’année.</span><span class="sxs-lookup"><span data-stu-id="1f52e-164">Abbreviated native name of the seventh month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f52e-165">CAL_SABBREVMONTHNAME8</span><span class="sxs-lookup"><span data-stu-id="1f52e-165">CAL_SABBREVMONTHNAME8</span></span></td>
<td><span data-ttu-id="1f52e-166">Nom natif abrégé du huitième mois de l’année.</span><span class="sxs-lookup"><span data-stu-id="1f52e-166">Abbreviated native name of the eighth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f52e-167">CAL_SABBREVMONTHNAME9</span><span class="sxs-lookup"><span data-stu-id="1f52e-167">CAL_SABBREVMONTHNAME9</span></span></td>
<td><span data-ttu-id="1f52e-168">Nom natif abrégé du neuvième mois de l’année.</span><span class="sxs-lookup"><span data-stu-id="1f52e-168">Abbreviated native name of the ninth month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f52e-169">CAL_SABBREVMONTHNAME10</span><span class="sxs-lookup"><span data-stu-id="1f52e-169">CAL_SABBREVMONTHNAME10</span></span></td>
<td><span data-ttu-id="1f52e-170">Nom natif abrégé du dixième mois de l’année.</span><span class="sxs-lookup"><span data-stu-id="1f52e-170">Abbreviated native name of the tenth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f52e-171">CAL_SABBREVMONTHNAME11</span><span class="sxs-lookup"><span data-stu-id="1f52e-171">CAL_SABBREVMONTHNAME11</span></span></td>
<td><span data-ttu-id="1f52e-172">Nom natif abrégé du onzième mois de l’année.</span><span class="sxs-lookup"><span data-stu-id="1f52e-172">Abbreviated native name of the eleventh month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f52e-173">CAL_SABBREVMONTHNAME12</span><span class="sxs-lookup"><span data-stu-id="1f52e-173">CAL_SABBREVMONTHNAME12</span></span></td>
<td><span data-ttu-id="1f52e-174">Nom natif abrégé du douzième mois de l’année.</span><span class="sxs-lookup"><span data-stu-id="1f52e-174">Abbreviated native name of the twelfth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f52e-175">CAL_SABBREVMONTHNAME13</span><span class="sxs-lookup"><span data-stu-id="1f52e-175">CAL_SABBREVMONTHNAME13</span></span></td>
<td><span data-ttu-id="1f52e-176">Nom natif abrégé du treizième mois de l’année, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="1f52e-176">Abbreviated native name of the thirteenth month of the year, if it exists.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f52e-177">CAL_SCALNAME</span><span class="sxs-lookup"><span data-stu-id="1f52e-177">CAL_SCALNAME</span></span></td>
<td><span data-ttu-id="1f52e-178">Nom natif de l’autre calendrier.</span><span class="sxs-lookup"><span data-stu-id="1f52e-178">Native name of the alternate calendar.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f52e-179">CAL_SDAYNAME1</span><span class="sxs-lookup"><span data-stu-id="1f52e-179">CAL_SDAYNAME1</span></span></td>
<td><span data-ttu-id="1f52e-180">Nom natif du premier jour de la semaine.</span><span class="sxs-lookup"><span data-stu-id="1f52e-180">Native name of the first day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f52e-181">CAL_SDAYNAME2</span><span class="sxs-lookup"><span data-stu-id="1f52e-181">CAL_SDAYNAME2</span></span></td>
<td><span data-ttu-id="1f52e-182">Nom natif du deuxième jour de la semaine.</span><span class="sxs-lookup"><span data-stu-id="1f52e-182">Native name of the second day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f52e-183">CAL_SDAYNAME3</span><span class="sxs-lookup"><span data-stu-id="1f52e-183">CAL_SDAYNAME3</span></span></td>
<td><span data-ttu-id="1f52e-184">Nom natif du troisième jour de la semaine.</span><span class="sxs-lookup"><span data-stu-id="1f52e-184">Native name of the third day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f52e-185">CAL_SDAYNAME4</span><span class="sxs-lookup"><span data-stu-id="1f52e-185">CAL_SDAYNAME4</span></span></td>
<td><span data-ttu-id="1f52e-186">Nom natif du quatrième jour de la semaine.</span><span class="sxs-lookup"><span data-stu-id="1f52e-186">Native name of the fourth day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f52e-187">CAL_SDAYNAME5</span><span class="sxs-lookup"><span data-stu-id="1f52e-187">CAL_SDAYNAME5</span></span></td>
<td><span data-ttu-id="1f52e-188">Nom natif du cinquième jour de la semaine.</span><span class="sxs-lookup"><span data-stu-id="1f52e-188">Native name of the fifth day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f52e-189">CAL_SDAYNAME6</span><span class="sxs-lookup"><span data-stu-id="1f52e-189">CAL_SDAYNAME6</span></span></td>
<td><span data-ttu-id="1f52e-190">Nom natif du sixième jour de la semaine.</span><span class="sxs-lookup"><span data-stu-id="1f52e-190">Native name of the sixth day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f52e-191">CAL_SDAYNAME7</span><span class="sxs-lookup"><span data-stu-id="1f52e-191">CAL_SDAYNAME7</span></span></td>
<td><span data-ttu-id="1f52e-192">Nom natif du septième jour de la semaine.</span><span class="sxs-lookup"><span data-stu-id="1f52e-192">Native name of the seventh day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f52e-193">CAL_SERASTRING</span><span class="sxs-lookup"><span data-stu-id="1f52e-193">CAL_SERASTRING</span></span></td>
<td><span data-ttu-id="1f52e-194">Une ou plusieurs chaînes se terminant par un caractère null qui spécifient chacun des points de code Unicode spécifiant l’ère associée à CAL_IYEAROFFSETRANGE.</span><span class="sxs-lookup"><span data-stu-id="1f52e-194">One or more null-terminated strings that specify each of the Unicode code points specifying the era associated with CAL_IYEAROFFSETRANGE.</span></span> <span data-ttu-id="1f52e-195">La dernière chaîne comporte un caractère null de fin supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="1f52e-195">The last string has an extra terminating null character.</span></span> <span data-ttu-id="1f52e-196">Cette valeur varie en fonction du type de calendrier facultatif.</span><span class="sxs-lookup"><span data-stu-id="1f52e-196">This value varies in format depending on the type of optional calendar.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f52e-197">CAL_SLONGDATE</span><span class="sxs-lookup"><span data-stu-id="1f52e-197">CAL_SLONGDATE</span></span></td>
<td><span data-ttu-id="1f52e-198">Formats de date longue pour le type de calendrier.</span><span class="sxs-lookup"><span data-stu-id="1f52e-198">Long date formats for the calendar type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f52e-199">CAL_SMONTHDAY</span><span class="sxs-lookup"><span data-stu-id="1f52e-199">CAL_SMONTHDAY</span></span></td>
<td><span data-ttu-id="1f52e-200"><strong>Windows 7 et versions ultérieures :</strong> Format du mois et du jour pour le type de calendrier.</span><span class="sxs-lookup"><span data-stu-id="1f52e-200"><strong>Windows 7 and later:</strong> Format of the month and day for the calendar type.</span></span> <span data-ttu-id="1f52e-201">La mise en forme est similaire à celle de CAL_SLONGDATE.</span><span class="sxs-lookup"><span data-stu-id="1f52e-201">The formatting is similar to that for CAL_SLONGDATE.</span></span> <span data-ttu-id="1f52e-202">Par exemple, si le modèle de mois/jour est le nom complet du mois suivi du nombre de jours avec des zéros non significatifs, par exemple, &quot; &quot; le format est &quot; Mmmm jj &quot; .</span><span class="sxs-lookup"><span data-stu-id="1f52e-202">For example, if the Month/Day pattern is the full month name followed by the day number with leading zeros, for example, &quot;September 03&quot;, the format is &quot;MMMM dd&quot;.</span></span> <span data-ttu-id="1f52e-203">Des guillemets simples peuvent être utilisés pour insérer des caractères qui ne sont pas de format, par exemple « de » en espagnol.</span><span class="sxs-lookup"><span data-stu-id="1f52e-203">Single quotation marks can be used to insert non-format characters, for example, 'de' in Spanish.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="1f52e-204">Ce type de calendrier ne prend en charge qu’un seul format.</span><span class="sxs-lookup"><span data-stu-id="1f52e-204">This calendar type supports only one format.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f52e-205">CAL_SMONTHNAME1</span><span class="sxs-lookup"><span data-stu-id="1f52e-205">CAL_SMONTHNAME1</span></span></td>
<td><span data-ttu-id="1f52e-206">Nom natif du premier mois de l’année.</span><span class="sxs-lookup"><span data-stu-id="1f52e-206">Native name of the first month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f52e-207">CAL_SMONTHNAME2</span><span class="sxs-lookup"><span data-stu-id="1f52e-207">CAL_SMONTHNAME2</span></span></td>
<td><span data-ttu-id="1f52e-208">Nom natif du deuxième mois de l’année.</span><span class="sxs-lookup"><span data-stu-id="1f52e-208">Native name of the second month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f52e-209">CAL_SMONTHNAME3</span><span class="sxs-lookup"><span data-stu-id="1f52e-209">CAL_SMONTHNAME3</span></span></td>
<td><span data-ttu-id="1f52e-210">Nom natif du troisième mois de l’année.</span><span class="sxs-lookup"><span data-stu-id="1f52e-210">Native name of the third month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f52e-211">CAL_SMONTHNAME4</span><span class="sxs-lookup"><span data-stu-id="1f52e-211">CAL_SMONTHNAME4</span></span></td>
<td><span data-ttu-id="1f52e-212">Nom natif du quatrième mois de l’année.</span><span class="sxs-lookup"><span data-stu-id="1f52e-212">Native name of the fourth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f52e-213">CAL_SMONTHNAME5</span><span class="sxs-lookup"><span data-stu-id="1f52e-213">CAL_SMONTHNAME5</span></span></td>
<td><span data-ttu-id="1f52e-214">Nom natif du cinquième mois de l’année.</span><span class="sxs-lookup"><span data-stu-id="1f52e-214">Native name of the fifth month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f52e-215">CAL_SMONTHNAME6</span><span class="sxs-lookup"><span data-stu-id="1f52e-215">CAL_SMONTHNAME6</span></span></td>
<td><span data-ttu-id="1f52e-216">Nom natif du sixième mois de l’année.</span><span class="sxs-lookup"><span data-stu-id="1f52e-216">Native name of the sixth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f52e-217">CAL_SMONTHNAME7</span><span class="sxs-lookup"><span data-stu-id="1f52e-217">CAL_SMONTHNAME7</span></span></td>
<td><span data-ttu-id="1f52e-218">Nom natif du septième mois de l’année.</span><span class="sxs-lookup"><span data-stu-id="1f52e-218">Native name of the seventh month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f52e-219">CAL_SMONTHNAME8</span><span class="sxs-lookup"><span data-stu-id="1f52e-219">CAL_SMONTHNAME8</span></span></td>
<td><span data-ttu-id="1f52e-220">Nom natif du huitième mois de l’année.</span><span class="sxs-lookup"><span data-stu-id="1f52e-220">Native name of the eighth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f52e-221">CAL_SMONTHNAME9</span><span class="sxs-lookup"><span data-stu-id="1f52e-221">CAL_SMONTHNAME9</span></span></td>
<td><span data-ttu-id="1f52e-222">Nom natif du neuvième mois de l’année.</span><span class="sxs-lookup"><span data-stu-id="1f52e-222">Native name of the ninth month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f52e-223">CAL_SMONTHNAME10</span><span class="sxs-lookup"><span data-stu-id="1f52e-223">CAL_SMONTHNAME10</span></span></td>
<td><span data-ttu-id="1f52e-224">Nom natif du dixième mois de l’année.</span><span class="sxs-lookup"><span data-stu-id="1f52e-224">Native name of the tenth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f52e-225">CAL_SMONTHNAME11</span><span class="sxs-lookup"><span data-stu-id="1f52e-225">CAL_SMONTHNAME11</span></span></td>
<td><span data-ttu-id="1f52e-226">Nom natif du onzième mois de l’année.</span><span class="sxs-lookup"><span data-stu-id="1f52e-226">Native name of the eleventh month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f52e-227">CAL_SMONTHNAME12</span><span class="sxs-lookup"><span data-stu-id="1f52e-227">CAL_SMONTHNAME12</span></span></td>
<td><span data-ttu-id="1f52e-228">Nom natif du douzième mois de l’année.</span><span class="sxs-lookup"><span data-stu-id="1f52e-228">Native name of the twelfth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f52e-229">CAL_SMONTHNAME13</span><span class="sxs-lookup"><span data-stu-id="1f52e-229">CAL_SMONTHNAME13</span></span></td>
<td><span data-ttu-id="1f52e-230">Nom natif du treizième mois de l’année, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="1f52e-230">Native name of the thirteenth month of the year, if it exists.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f52e-231">CAL_SSHORTDATE</span><span class="sxs-lookup"><span data-stu-id="1f52e-231">CAL_SSHORTDATE</span></span></td>
<td><span data-ttu-id="1f52e-232">Formats de date courts pour le type de calendrier.</span><span class="sxs-lookup"><span data-stu-id="1f52e-232">Short date formats for the calendar type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f52e-233">CAL_SSHORTESTDAYNAME1</span><span class="sxs-lookup"><span data-stu-id="1f52e-233">CAL_SSHORTESTDAYNAME1</span></span></td>
<td><span data-ttu-id="1f52e-234"><strong>Windows Vista et versions ultérieures :</strong> Nom natif abrégé du premier jour de la semaine.</span><span class="sxs-lookup"><span data-stu-id="1f52e-234"><strong>Windows Vista and later:</strong> Short native name of the first day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f52e-235">CAL_SSHORTESTDAYNAME2</span><span class="sxs-lookup"><span data-stu-id="1f52e-235">CAL_SSHORTESTDAYNAME2</span></span></td>
<td><span data-ttu-id="1f52e-236"><strong>Windows Vista et versions ultérieures :</strong> Nom natif abrégé du deuxième jour de la semaine.</span><span class="sxs-lookup"><span data-stu-id="1f52e-236"><strong>Windows Vista and later:</strong> Short native name of the second day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f52e-237">CAL_SSHORTESTDAYNAME3</span><span class="sxs-lookup"><span data-stu-id="1f52e-237">CAL_SSHORTESTDAYNAME3</span></span></td>
<td><span data-ttu-id="1f52e-238"><strong>Windows Vista et versions ultérieures :</strong> Nom natif abrégé du troisième jour de la semaine.</span><span class="sxs-lookup"><span data-stu-id="1f52e-238"><strong>Windows Vista and later:</strong> Short native name of the third day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f52e-239">CAL_SSHORTESTDAYNAME4</span><span class="sxs-lookup"><span data-stu-id="1f52e-239">CAL_SSHORTESTDAYNAME4</span></span></td>
<td><span data-ttu-id="1f52e-240"><strong>Windows Vista et versions ultérieures :</strong> Nom natif abrégé du quatrième jour de la semaine.</span><span class="sxs-lookup"><span data-stu-id="1f52e-240"><strong>Windows Vista and later:</strong> Short native name of the fourth day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f52e-241">CAL_SSHORTESTDAYNAME5</span><span class="sxs-lookup"><span data-stu-id="1f52e-241">CAL_SSHORTESTDAYNAME5</span></span></td>
<td><span data-ttu-id="1f52e-242"><strong>Windows Vista et versions ultérieures :</strong> Nom natif abrégé du cinquième jour de la semaine.</span><span class="sxs-lookup"><span data-stu-id="1f52e-242"><strong>Windows Vista and later:</strong> Short native name of the fifth day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f52e-243">CAL_SSHORTESTDAYNAME6</span><span class="sxs-lookup"><span data-stu-id="1f52e-243">CAL_SSHORTESTDAYNAME6</span></span></td>
<td><span data-ttu-id="1f52e-244"><strong>Windows Vista et versions ultérieures :</strong> Nom natif abrégé du sixième jour de la semaine.</span><span class="sxs-lookup"><span data-stu-id="1f52e-244"><strong>Windows Vista and later:</strong> Short native name of the sixth day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f52e-245">CAL_SSHORTESTDAYNAME7</span><span class="sxs-lookup"><span data-stu-id="1f52e-245">CAL_SSHORTESTDAYNAME7</span></span></td>
<td><span data-ttu-id="1f52e-246"><strong>Windows Vista et versions ultérieures :</strong> Nom natif abrégé du septième jour de la semaine.</span><span class="sxs-lookup"><span data-stu-id="1f52e-246"><strong>Windows Vista and later:</strong> Short native name of the seventh day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f52e-247">CAL_SYEARMONTH</span><span class="sxs-lookup"><span data-stu-id="1f52e-247">CAL_SYEARMONTH</span></span></td>
<td><span data-ttu-id="1f52e-248"><strong>Windows Me/98, windows 2000 :</strong> Formats année/mois pour les calendriers spécifiés.</span><span class="sxs-lookup"><span data-stu-id="1f52e-248"><strong>Windows Me/98, Windows 2000:</strong> The year/month formats for the specified calendars.</span></span></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="1f52e-249">Si le nom natif du jour de la semaine ou pour un mois est une chaîne vide, ce nom est identique au nom spécifié dans les informations de paramètres régionaux correspondants et n’est donc pas dupliqué ici.</span><span class="sxs-lookup"><span data-stu-id="1f52e-249">If the native name for the day of the week or for a month is an empty string, that name is identical to the name specified in the corresponding locale information and therefore is not duplicated here.</span></span>

 

 

 




