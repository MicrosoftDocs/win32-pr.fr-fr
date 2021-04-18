---
description: L’objet SWbemDateTime est un objet d’assistance pour analyser et définir des valeurs DateTime Common Information Model (CIM).
ms.assetid: 3dd34c73-3c2b-4d59-827b-169cf8020213
ms.tgt_platform: multiple
title: Objet SWbemDateTime (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime
- ISWbemDateTime
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 65f3f9836b52693e3f74bac5cfd94553e02d7bf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519747"
---
# <a name="swbemdatetime-object"></a><span data-ttu-id="a77de-103">Objet SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="a77de-103">SWbemDateTime object</span></span>

<span data-ttu-id="a77de-104">L’objet **SWbemDateTime** est un objet d’assistance pour analyser et définir des valeurs [DateTime](datetime.md) Common Information Model (CIM).</span><span class="sxs-lookup"><span data-stu-id="a77de-104">The **SWbemDateTime** object is a helper object to parse and set Common Information Model (CIM) [datetime](datetime.md) values.</span></span> <span data-ttu-id="a77de-105">Il joue un rôle similaire à [**SWbemObjectPath**](swbemobjectpath.md), qui fournit une assistance pour mettre en forme et interpréter les chemins d’accès aux objets.</span><span class="sxs-lookup"><span data-stu-id="a77de-105">It plays a role similar to [**SWbemObjectPath**](swbemobjectpath.md), which provides assistance to format and interpret object paths.</span></span> <span data-ttu-id="a77de-106">Vous pouvez utiliser l’appel VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) pour créer l’objet **SWbemDateTime** .</span><span class="sxs-lookup"><span data-stu-id="a77de-106">You can use the VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) call to create the **SWbemDateTime** object.</span></span>

<span data-ttu-id="a77de-107">Un objet **SWbemDateTime** peut être initialisé à partir de et mis en forme dans les valeurs **VT \_ Date** ou **fileTime** à l’aide de méthodes sur l’objet.</span><span class="sxs-lookup"><span data-stu-id="a77de-107">An **SWbemDateTime** object can be initialized from and formatted in either **VT\_DATE** or **FILETIME** values using methods on the object.</span></span> <span data-ttu-id="a77de-108">À l’aide des propriétés de l’objet, la valeur peut être analysée en composant l’année, le mois, le jour, l’heure, les minutes, les secondes ou les microsecondes.</span><span class="sxs-lookup"><span data-stu-id="a77de-108">Using properties of the object, the value can be parsed into component year, month, day, hour, minutes, seconds, or microseconds.</span></span> <span data-ttu-id="a77de-109">L’objet **SWbemDateTime** peut être mis en forme en valeurs locales ou de temps universel coordonné (UTC, Universal Time Coordinated).</span><span class="sxs-lookup"><span data-stu-id="a77de-109">The **SWbemDateTime** object can be formatted into either local or Coordinated Universal Time (UTC) values.</span></span> <span data-ttu-id="a77de-110">Pour plus d’informations, consultez [format de date et d’heure](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="a77de-110">For more information, see [Date and Time Format](date-and-time-format.md).</span></span>

<span data-ttu-id="a77de-111">**SWbemDateTime** est le seul objet de script Windows Management Instrumentation (WMI) qui est marqué comme sécurisé pour l’initialisation et les scripts s’exécutant sur les pages HTML dans Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="a77de-111">**SWbemDateTime** is the only Windows Management Instrumentation (WMI) scripting object that is marked safe for initialization and scripts running on HTML pages in Internet Explorer.</span></span>

## <a name="members"></a><span data-ttu-id="a77de-112">Membres</span><span class="sxs-lookup"><span data-stu-id="a77de-112">Members</span></span>

<span data-ttu-id="a77de-113">L’objet **SWbemDateTime** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a77de-113">The **SWbemDateTime** object has these types of members:</span></span>

-   [<span data-ttu-id="a77de-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a77de-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="a77de-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a77de-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a77de-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a77de-116">Methods</span></span>

<span data-ttu-id="a77de-117">L’objet **SWbemDateTime** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="a77de-117">The **SWbemDateTime** object has these methods.</span></span>



| <span data-ttu-id="a77de-118">Méthode</span><span class="sxs-lookup"><span data-stu-id="a77de-118">Method</span></span>                                           | <span data-ttu-id="a77de-119">Description</span><span class="sxs-lookup"><span data-stu-id="a77de-119">Description</span></span>                                                                                                          |
|:-------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a77de-120">**GetFileTime**</span><span class="sxs-lookup"><span data-stu-id="a77de-120">**GetFileTime**</span></span>](swbemdatetime-getfiletime.md) | <span data-ttu-id="a77de-121">Convertit une date et une heure de **fileTime** , exprimées sous forme de **BSTR**, au format [DateTime](datetime.md) WMI.</span><span class="sxs-lookup"><span data-stu-id="a77de-121">Converts a **FILETIME** date and time, expressed as a **BSTR**, to a WMI [DATETIME](datetime.md) format.</span></span><br/> |
| [<span data-ttu-id="a77de-122">**GetVarDate,**</span><span class="sxs-lookup"><span data-stu-id="a77de-122">**GetVarDate**</span></span>](swbemdatetime-getvardate.md)   | <span data-ttu-id="a77de-123">Convertit une valeur de date et d’heure au format [DateTime](datetime.md) WMI en une **\_ Date VT**.</span><span class="sxs-lookup"><span data-stu-id="a77de-123">Converts a WMI [DATETIME](datetime.md) formatted date and time value to a **VT\_DATE**.</span></span><br/>                  |
| [<span data-ttu-id="a77de-124">**SetFileTime**</span><span class="sxs-lookup"><span data-stu-id="a77de-124">**SetFileTime**</span></span>](swbemdatetime-setfiletime.md) | <span data-ttu-id="a77de-125">Convertit un format [DateTime](datetime.md) WMI en date et heure **fileTime** , exprimé sous forme de **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="a77de-125">Converts a WMI [DATETIME](datetime.md) format to a **FILETIME** date and time, expressed as a **BSTR**.</span></span><br/>  |
| [<span data-ttu-id="a77de-126">**SetVarDate**</span><span class="sxs-lookup"><span data-stu-id="a77de-126">**SetVarDate**</span></span>](swbemdatetime-setvardate.md)   | <span data-ttu-id="a77de-127">Convertit une date et une heure au format de **\_ Date VT** en [DateTime](datetime.md)WMI.</span><span class="sxs-lookup"><span data-stu-id="a77de-127">Converts a **VT\_DATE** formatted date and time to a WMI [DATETIME](datetime.md).</span></span><br/>                        |



 

### <a name="properties"></a><span data-ttu-id="a77de-128">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a77de-128">Properties</span></span>

<span data-ttu-id="a77de-129">L’objet **SWbemDateTime** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="a77de-129">The **SWbemDateTime** object has these properties.</span></span>



| <span data-ttu-id="a77de-130">Propriété</span><span class="sxs-lookup"><span data-stu-id="a77de-130">Property</span></span>                                                                        | <span data-ttu-id="a77de-131">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="a77de-131">Access type</span></span>           | <span data-ttu-id="a77de-132">Description</span><span class="sxs-lookup"><span data-stu-id="a77de-132">Description</span></span>                                                                                                                     |
|:--------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a77de-133">**Temps**</span><span class="sxs-lookup"><span data-stu-id="a77de-133">**Day**</span></span>](swbemdatetime-day.md)<br/>                                     | <span data-ttu-id="a77de-134">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a77de-134">Read/write</span></span><br/> | <span data-ttu-id="a77de-135">Composant « jour » d’une valeur [DateTime](datetime.md) CIM.</span><span class="sxs-lookup"><span data-stu-id="a77de-135">The day component of a CIM [datetime](datetime.md) value.</span></span><br/>                                                           |
| [<span data-ttu-id="a77de-136">**DaySpecified**</span><span class="sxs-lookup"><span data-stu-id="a77de-136">**DaySpecified**</span></span>](swbemdatetime-dayspecified.md)<br/>                   | <span data-ttu-id="a77de-137">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a77de-137">Read/write</span></span><br/> | <span data-ttu-id="a77de-138">Indique si le jour est spécifié ou laissé comme caractère générique.</span><span class="sxs-lookup"><span data-stu-id="a77de-138">Indicates whether the day is specified or left as a wildcard.</span></span><br/>                                                        |
| [<span data-ttu-id="a77de-139">**Heures**</span><span class="sxs-lookup"><span data-stu-id="a77de-139">**Hours**</span></span>](swbemdatetime-hours.md)<br/>                                 | <span data-ttu-id="a77de-140">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a77de-140">Read/write</span></span><br/> | <span data-ttu-id="a77de-141">Heures du composant « jour » d’une valeur [DateTime](datetime.md) CIM.</span><span class="sxs-lookup"><span data-stu-id="a77de-141">The hours of the day component of a CIM [datetime](datetime.md) value.</span></span><br/>                                              |
| [<span data-ttu-id="a77de-142">**HoursSpecified**</span><span class="sxs-lookup"><span data-stu-id="a77de-142">**HoursSpecified**</span></span>](swbemdatetime-hoursspecified.md)<br/>               | <span data-ttu-id="a77de-143">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a77de-143">Read/write</span></span><br/> | <span data-ttu-id="a77de-144">Indique si l’heure est spécifiée ou laissée comme caractère générique.</span><span class="sxs-lookup"><span data-stu-id="a77de-144">Indicates whether the hour is specified or left as a wildcard.</span></span><br/>                                                       |
| [<span data-ttu-id="a77de-145">**IsInterval**</span><span class="sxs-lookup"><span data-stu-id="a77de-145">**IsInterval**</span></span>](swbemdatetime-isinterval.md)<br/>                       | <span data-ttu-id="a77de-146">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a77de-146">Read/write</span></span><br/> | <span data-ttu-id="a77de-147">Indique qu’au moins un composant de la valeur [DateTime](datetime.md) CIM représente un intervalle et non une date.</span><span class="sxs-lookup"><span data-stu-id="a77de-147">Indicates that at least one component of the CIM [datetime](datetime.md) represents an interval rather than a date.</span></span><br/> |
| [<span data-ttu-id="a77de-148">**Microsecondes**</span><span class="sxs-lookup"><span data-stu-id="a77de-148">**Microseconds**</span></span>](swbemdatetime-microseconds.md)<br/>                   | <span data-ttu-id="a77de-149">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a77de-149">Read/write</span></span><br/> | <span data-ttu-id="a77de-150">Composant microsecondes d’une valeur [DateTime](datetime.md) CIM.</span><span class="sxs-lookup"><span data-stu-id="a77de-150">The microseconds component of a CIM [datetime](datetime.md) value.</span></span><br/>                                                  |
| [<span data-ttu-id="a77de-151">**MicrosecondsSpecified**</span><span class="sxs-lookup"><span data-stu-id="a77de-151">**MicrosecondsSpecified**</span></span>](swbemdatetime-microsecondsspecified.md)<br/> | <span data-ttu-id="a77de-152">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a77de-152">Read/write</span></span><br/> | <span data-ttu-id="a77de-153">Indique si le composant microsecondes est spécifié ou laissé comme caractère générique.</span><span class="sxs-lookup"><span data-stu-id="a77de-153">Indicates whether the microseconds component is specified or left as a wildcard.</span></span><br/>                                     |
| [<span data-ttu-id="a77de-154">**Maximum**</span><span class="sxs-lookup"><span data-stu-id="a77de-154">**Minutes**</span></span>](swbemdatetime-minutes.md)<br/>                             | <span data-ttu-id="a77de-155">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a77de-155">Read/write</span></span><br/> | <span data-ttu-id="a77de-156">Composant « minutes » d’une valeur [DateTime](datetime.md) CIM.</span><span class="sxs-lookup"><span data-stu-id="a77de-156">The minutes component of a CIM [datetime](datetime.md) value.</span></span><br/>                                                       |
| [<span data-ttu-id="a77de-157">**MinutesSpecified**</span><span class="sxs-lookup"><span data-stu-id="a77de-157">**MinutesSpecified**</span></span>](swbemdatetime-minutesspecified.md)<br/>           | <span data-ttu-id="a77de-158">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a77de-158">Read/write</span></span><br/> | <span data-ttu-id="a77de-159">Indique si le composant « minutes » est spécifié ou laissé comme caractère générique.</span><span class="sxs-lookup"><span data-stu-id="a77de-159">Indicates whether the minutes component is specified or left as a wildcard.</span></span><br/>                                          |
| [<span data-ttu-id="a77de-160">**Chronique**</span><span class="sxs-lookup"><span data-stu-id="a77de-160">**Month**</span></span>](swbemdatetime-month.md)<br/>                                 | <span data-ttu-id="a77de-161">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a77de-161">Read/write</span></span><br/> | <span data-ttu-id="a77de-162">Composant « mois » d’une valeur [DateTime](datetime.md) CIM.</span><span class="sxs-lookup"><span data-stu-id="a77de-162">The month component of a CIM [datetime](datetime.md) value.</span></span><br/>                                                         |
| [<span data-ttu-id="a77de-163">**MonthSpecified**</span><span class="sxs-lookup"><span data-stu-id="a77de-163">**MonthSpecified**</span></span>](swbemdatetime-monthspecified.md)<br/>               | <span data-ttu-id="a77de-164">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a77de-164">Read/write</span></span><br/> | <span data-ttu-id="a77de-165">Indique si le mois est spécifié ou laissé comme caractère générique.</span><span class="sxs-lookup"><span data-stu-id="a77de-165">Indicates whether the month is specified or left as a wildcard.</span></span><br/>                                                      |
| [<span data-ttu-id="a77de-166">**Durée**</span><span class="sxs-lookup"><span data-stu-id="a77de-166">**Seconds**</span></span>](swbemdatetime-seconds.md)<br/>                             | <span data-ttu-id="a77de-167">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a77de-167">Read/write</span></span><br/> | <span data-ttu-id="a77de-168">Composant « secondes » d’une valeur [DateTime](datetime.md) CIM.</span><span class="sxs-lookup"><span data-stu-id="a77de-168">The seconds component of a CIM [datetime](datetime.md) value.</span></span><br/>                                                       |
| [<span data-ttu-id="a77de-169">**SecondsSpecified**</span><span class="sxs-lookup"><span data-stu-id="a77de-169">**SecondsSpecified**</span></span>](swbemdatetime-secondsspecified.md)<br/>           | <span data-ttu-id="a77de-170">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a77de-170">Read/write</span></span><br/> | <span data-ttu-id="a77de-171">Indique si le composant seconds est spécifié ou laissé comme caractère générique.</span><span class="sxs-lookup"><span data-stu-id="a77de-171">Indicates whether the seconds component is specified or left as a wildcard.</span></span><br/>                                          |
| [<span data-ttu-id="a77de-172">**UNIVERSEL**</span><span class="sxs-lookup"><span data-stu-id="a77de-172">**UTC**</span></span>](swbemdatetime-utc.md)<br/>                                     | <span data-ttu-id="a77de-173">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a77de-173">Read/write</span></span><br/> | <span data-ttu-id="a77de-174">Composant UTC d’une valeur [DateTime](datetime.md) CIM.</span><span class="sxs-lookup"><span data-stu-id="a77de-174">The UTC component of a CIM [datetime](datetime.md) value.</span></span><br/>                                                           |
| [<span data-ttu-id="a77de-175">**UTCSpecified**</span><span class="sxs-lookup"><span data-stu-id="a77de-175">**UTCSpecified**</span></span>](swbemdatetime-utcspecified.md)<br/>                   | <span data-ttu-id="a77de-176">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a77de-176">Read/write</span></span><br/> | <span data-ttu-id="a77de-177">Indique si le composant UTC est spécifié ou laissé comme caractère générique.</span><span class="sxs-lookup"><span data-stu-id="a77de-177">Indicates whether the UTC component is specified or left as a wildcard.</span></span><br/>                                              |
| [<span data-ttu-id="a77de-178">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="a77de-178">**Value**</span></span>](swbemdatetime-value.md)<br/>                                 | <span data-ttu-id="a77de-179">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a77de-179">Read/write</span></span><br/> | <span data-ttu-id="a77de-180">Valeur [DateTime](datetime.md) CIM complète.</span><span class="sxs-lookup"><span data-stu-id="a77de-180">The full CIM [datetime](datetime.md) value.</span></span><br/>                                                                         |
| [<span data-ttu-id="a77de-181">**Year**</span><span class="sxs-lookup"><span data-stu-id="a77de-181">**Year**</span></span>](swbemdatetime-year.md)<br/>                                   | <span data-ttu-id="a77de-182">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a77de-182">Read/write</span></span><br/> | <span data-ttu-id="a77de-183">Composant d’année d’une valeur [DateTime](datetime.md) CIM.</span><span class="sxs-lookup"><span data-stu-id="a77de-183">The year component of a CIM [datetime](datetime.md) value.</span></span><br/>                                                          |
| [<span data-ttu-id="a77de-184">**YearSpecified**</span><span class="sxs-lookup"><span data-stu-id="a77de-184">**YearSpecified**</span></span>](swbemdatetime-yearspecified.md)<br/>                 | <span data-ttu-id="a77de-185">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a77de-185">Read/write</span></span><br/> | <span data-ttu-id="a77de-186">Indique si l’année est spécifiée ou conservée comme caractère générique.</span><span class="sxs-lookup"><span data-stu-id="a77de-186">Indicates whether or not the year is specified or left as a wildcard.</span></span><br/>                                                |



 

## <a name="remarks"></a><span data-ttu-id="a77de-187">Notes</span><span class="sxs-lookup"><span data-stu-id="a77de-187">Remarks</span></span>

<span data-ttu-id="a77de-188">WMI enregistre les horodateurs au format UTC (Universal Time Coordinate).</span><span class="sxs-lookup"><span data-stu-id="a77de-188">WMI records timestamps in universal time coordinate (UTC) format.</span></span> <span data-ttu-id="a77de-189">L’heure UTC n’est pas le format utilisé par la plupart des développeurs et administrateurs informatiques.</span><span class="sxs-lookup"><span data-stu-id="a77de-189">UTC is not the format that most developers and IT administrators use.</span></span> <span data-ttu-id="a77de-190">Par conséquent, un problème courant consiste à déterminer comment traduire le temps universel coordonné (UTC) en un nom plus lisible.</span><span class="sxs-lookup"><span data-stu-id="a77de-190">Therefore, a common issue is determining how to translate UTC into something more readable.</span></span> <span data-ttu-id="a77de-191">Pour plus d’informations sur l’utilisation du temps universel coordonné (UTC), consultez [tâches WMI : dates et heures](wmi-tasks--dates-and-times.md) et [utilisation de dates et d’heures à l’aide de WMI](/previous-versions/tn-archive/ee198928(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="a77de-191">For more information on how to work with UTC, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md) and [Working with Dates and Times using WMI](/previous-versions/tn-archive/ee198928(v=technet.10)).</span></span> <span data-ttu-id="a77de-192">Vous pouvez également lire les informations [sur le temps (OH et sur les dates)](/previous-versions/technet-magazine/cc160973(v=msdn.10)) et [comment soustraire un nombre spécifié de jours d’une valeur UTC ?](https://blogs.technet.com/b/heyscriptingguy/archive/2006/07/21/how-can-i-subtract-a-specified-number-of-days-from-a-utc-value.aspx) billets de blog pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="a77de-192">You can also read the [It s About Time (Oh, and About Dates, Too)](/previous-versions/technet-magazine/cc160973(v=msdn.10)) and [How Can I Subtract a Specified Number of Days from a UTC Value?](https://blogs.technet.com/b/heyscriptingguy/archive/2006/07/21/how-can-i-subtract-a-specified-number-of-days-from-a-utc-value.aspx) blog posts for additional information.</span></span>

<span data-ttu-id="a77de-193">Tout champ numérique peut avoir une valeur générique si la propriété [**IsInterval**](swbemdatetime-isinterval.md) est définie sur **false**.</span><span class="sxs-lookup"><span data-stu-id="a77de-193">Any numeric field can have a wildcard value if the [**IsInterval**](swbemdatetime-isinterval.md) property is set to **FALSE**.</span></span> <span data-ttu-id="a77de-194">Les champs avec des valeurs de caractère générique contiennent des astérisques dans le champ entier.</span><span class="sxs-lookup"><span data-stu-id="a77de-194">Fields with wildcard values contain asterisks in the entire field.</span></span>

<span data-ttu-id="a77de-195">Chaque propriété, par exemple [**Day**](swbemdatetime-day.md), a une valeur booléenne spécifiée correspondante, telle que [**DaySpecified**](swbemdatetime-dayspecified.md).</span><span class="sxs-lookup"><span data-stu-id="a77de-195">Each property, for example [**Day**](swbemdatetime-day.md), has a corresponding specified Boolean value, such as [**DaySpecified**](swbemdatetime-dayspecified.md).</span></span> <span data-ttu-id="a77de-196">Quand **DaySpecified** a la valeur **false**, la valeur est interprétée comme un intervalle plutôt que comme un nombre compris entre 01 et 31.</span><span class="sxs-lookup"><span data-stu-id="a77de-196">When **DaySpecified** is **FALSE**, then the value is interpreted as an interval rather than a number between 01 and 31.</span></span> <span data-ttu-id="a77de-197">Si un intervalle est utilisé n’importe où dans la valeur [DateTime](datetime.md) CIM, [**IsInterval**](swbemdatetime-isinterval.md) est également défini sur **true**.</span><span class="sxs-lookup"><span data-stu-id="a77de-197">If an interval is used anywhere in the CIM [datetime](datetime.md) value, then [**IsInterval**](swbemdatetime-isinterval.md) is also set to **TRUE**.</span></span> <span data-ttu-id="a77de-198">La valeur par défaut est pour une valeur DateTime CIM qui contient une date plutôt qu’un ou plusieurs intervalles.</span><span class="sxs-lookup"><span data-stu-id="a77de-198">The default is for a CIM datetime value to contain a date rather than one or more intervals.</span></span>

<span data-ttu-id="a77de-199">Par exemple, si [**SWbemDateTime. DaySpecified**](swbemdatetime-dayspecified.md) a la valeur **true**, [**SWbemDateTime. Value**](swbemdatetime-value.md) comprend la valeur actuelle de [**SWbemDateTime. Day**](swbemdatetime-day.md), sinon il s’agit d’une valeur générique.</span><span class="sxs-lookup"><span data-stu-id="a77de-199">For example, if [**SWbemDateTime.DaySpecified**](swbemdatetime-dayspecified.md) is **TRUE**, then [**SWbemDateTime.Value**](swbemdatetime-value.md) includes the current value of [**SWbemDateTime.Day**](swbemdatetime-day.md), otherwise it is a wildcard value.</span></span> <span data-ttu-id="a77de-200">Dans les deux cas, la propriété [**IsInterval**](swbemdatetime-isinterval.md) a la **valeur false** .</span><span class="sxs-lookup"><span data-stu-id="a77de-200">The [**IsInterval**](swbemdatetime-isinterval.md) property is **FALSE** in either case.</span></span>

## <a name="examples"></a><span data-ttu-id="a77de-201">Exemples</span><span class="sxs-lookup"><span data-stu-id="a77de-201">Examples</span></span>

<span data-ttu-id="a77de-202">L’exemple de code de script suivant montre comment utiliser un objet **SWbemDateTime** pour analyser une valeur de propriété DateTime lue à partir de l’espace de stockage WMI, la propriété **InstallDate** dans [**Win32 \_ OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem).</span><span class="sxs-lookup"><span data-stu-id="a77de-202">The following script code example shows how to use an **SWbemDateTime** object to parse a datetime property value read from the WMI repository, the **InstallDate** property in [**Win32\_OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem).</span></span>


```VB
' Create a new datetime object.
Set dateTime = CreateObject("WbemScripting.SWbemDateTime")

' Retrieve a WMI object that contains a datetime value.
for each os in GetObject( _
    "winmgmts:").InstancesOf ("Win32_OperatingSystem")

    ' The InstallDate property is a CIM_DATETIME. 
    MsgBox os.InstallDate
    dateTime.Value = os.InstallDate

    ' Display the year of installation.
    MsgBox "This OS was installed in the year " & dateTime.Year

    ' Display the installation date using the VT_DATE format.
    MsgBox "Full installation date (VT_DATE format) is " _
    & dateTime.GetVarDate

    ' Display the installation date using the FILETIME format.
    MsgBox "Full installation date (FILETIME format) is " _
    & dateTime.GetFileTime 
next
Set datetime = Nothing
```



<span data-ttu-id="a77de-203">L’exemple suivant montre comment créer un objet **SWbemDateTime** , stocker une valeur de date dans l’objet, afficher la date comme locale et le temps universel coordonné (UTC), et stocker la valeur dans une classe et une propriété nouvellement créées.</span><span class="sxs-lookup"><span data-stu-id="a77de-203">The following example shows how to create an **SWbemDateTime** object, store a date value in the object, display the date as local and Coordinated Universal Time (UTC), and store the value in a newly created class and property.</span></span> <span data-ttu-id="a77de-204">Pour plus d’informations sur la constante **wbemCimtypeDatetime**, consultez [WbemCimtypeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum).</span><span class="sxs-lookup"><span data-stu-id="a77de-204">For more information about the constant **wbemCimtypeDatetime**, see [WbemCimtypeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum).</span></span>


```VB
' Create an SWbemDateTime object.
Set dateTime = CreateObject("WbemScripting.SWbemDateTime")
' Set the value 
Const wbemCimTypeDatetime = 101

' Construct a datetime value using the intrinsic VBScript CDate
' function interpreting this as a local date/time in
' the Pacific time zone (-8 hrs GMT). Convert to CIM datetime
' using SetVarDate method. The year defaults to current year.
dateTime.SetVarDate (CDate ("January 20 11:56:32"))

' The value in dateTime displays as 
' 20000120195632.000000-480. This is the equivalent time
' in GMT with the specified offset for PST of -8 hrs.
MsgBox "CIM datetime " & dateTime

' The value now displays as B=0/2000 11:56:32 AM because the
' parameter contains the default TRUE value causing the value to be
' interpreted as a local time.
MsgBox "Local datetime " & dateTime.GetVarDate ()

' The value now displays as B=0/2000 7:56:32 PM because the
' parameter value is FALSE, which indicates a GMT time.
' non-local time.
MsgBox "Datetime in GMT " & dateTime.GetVarDate (false)

' Create a new class and add a DateTime property value.
' SWbemServices.Get returns an empty SWbemObject
' which can become a new class. SWbemObject.Path_ returns an
' SWbemObjectPath object. 
set NewObject = GetObject("winmgmts:root\default").Get
NewObject.Path_.Class = "NewClass"

' Add a new property named "InterestingDate" to the NewObject class
' and define its datatype as a CIM datetime value.
NewObject.Properties_.Add "InterestingDate", wbemCimtypeDatetime

' Set the new value of the SWbemDateTime object in the InterestingDate
' property.
NewObject.InterestingDate = dateTime.Value
MsgBox "Datetime in new object " & NewObject.InterestingDate

' Write the new class (named "NewClass") containing
' the SWbemDateTime object to the repository.
NewObject.Put_
WScript.Echo "NewClass is now in WMI repository"

' Clean up the example by deleting the new class from the repository
NewObject.Delete_
```



<span data-ttu-id="a77de-205">L’exemple de code de script suivant montre comment utiliser un objet **SWbemDateTime** pour modifier une valeur d’intervalle sur une propriété lue à partir de l’espace de stockage WMI.</span><span class="sxs-lookup"><span data-stu-id="a77de-205">The following script code example shows how to use an **SWbemDateTime** object to modify an interval value on a property that is read from the WMI repository.</span></span>


```VB
' Construct an interval value of 100 days, 1 hour, and 3 seconds.
dateTime.IsInterval = true 
dateTime.Day = 100
dateTime.Hours = 1
dateTime.Seconds = 3

' The datetime displays as 00000100010003.000000:000.
MsgBox "Constructed interval value " & datetime

' Retrieve an empty WMI object and add a datetime property. 
Const wbemCimTypeDatetime = 101
Set NewObject = GetObject("winmgmts:root\default").Get
NewObject.Path_.Class = "Empty"
NewObject.Properties_.Add "InterestingDate", wbemCimtypeDatetime

' Set the new value in the property and update. 
NewObject.InterestingDate = dateTime.Value
MsgBox "NewObject.InterestingDate = " & NewObject.InterestingDate

' Write the new SWbemDateTime object to the repository.
NewObject.Put_

' Delete the object.
NewObject.Delete_
```



<span data-ttu-id="a77de-206">L’exemple de code de script suivant montre comment utiliser un objet **SWbemDate** pour lire une valeur **fileTime** .</span><span class="sxs-lookup"><span data-stu-id="a77de-206">The following script code example shows how to use an **SWbemDate** object to read a **FILETIME** value.</span></span>


```VB
' Create a new datetime object.
Set datetime = CreateObject("WbemScripting.SWbemDateTime")

' Set from a FILETIME value (non-local).
' Assume a timezone -7 hrs. GMT.
MsgBox "FILETIME value " & "126036951652030000"
datetime.SetFileTime "126036951652030000", false

' Displays as 5/24/2000 7:26:05 PM.
MsgBox "GMT time " & dateTime.GetVarDate   

' Set from a FILETIME value (local).
datetime.SetFileTime "126036951652030000"

' Displays as 5/25/2000 2:26:05 AM.
MsgBox "Same value in local time " & dateTime.GetVarDate
Set datetime = Nothing
```



<span data-ttu-id="a77de-207">Le code PowerShell suivant crée une instance d’un objet SWbemDateTime, récupère la date d’installation du système d’exploitation et convertit la date dans un format différent.</span><span class="sxs-lookup"><span data-stu-id="a77de-207">The following PowerShell code creates an instance of a SWbemDateTime object, retrieves the OS install date, and converts the date to a different format</span></span>


```PowerShell
# Create swbemdatetime object
$datetime = New-Object -ComObject WbemScripting.SWbemDateTime

#  Get OS installation time and assign to datetime object
$os = Get-WmiObject -Class Win32_OperatingSystem
$dateTime.Value = $os.InstallDate

# Now display the time
"This OS was installed in the year {0}"           -f $dateTime.Year
"Full installation date (VT_DATE format) is {0}"  -f $dateTime.GetVarDate()
"Full installation date (FILETIME format) is {0}" -f $dateTime.GetFileTime() 
```



<span data-ttu-id="a77de-208">Le code PowerShell suivant convertit le code dans un format prêt à être utilisé par un fournisseur CIM.</span><span class="sxs-lookup"><span data-stu-id="a77de-208">The following Powershell code translates the code into a format ready to be consumed by a CIM provider.</span></span>


```PowerShell
 $time = (Get-Date)
 $objScriptTime = New-Object -ComObject WbemScripting.SWbemDateTime
 $objScriptTime.SetVarDate($time)
 $cimTime = $objScriptTime.Value
```



## <a name="requirements"></a><span data-ttu-id="a77de-209">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a77de-209">Requirements</span></span>



| <span data-ttu-id="a77de-210">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a77de-210">Requirement</span></span> | <span data-ttu-id="a77de-211">Valeur</span><span class="sxs-lookup"><span data-stu-id="a77de-211">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a77de-212">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a77de-212">Minimum supported client</span></span><br/> | <span data-ttu-id="a77de-213">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a77de-213">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a77de-214">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a77de-214">Minimum supported server</span></span><br/> | <span data-ttu-id="a77de-215">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a77de-215">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a77de-216">En-tête</span><span class="sxs-lookup"><span data-stu-id="a77de-216">Header</span></span><br/>                   | <dl> <span data-ttu-id="a77de-217"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a77de-217"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a77de-218">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="a77de-218">Type library</span></span><br/>             | <dl> <span data-ttu-id="a77de-219"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a77de-219"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a77de-220">DLL</span><span class="sxs-lookup"><span data-stu-id="a77de-220">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a77de-221"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a77de-221"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a77de-222">CLSID</span><span class="sxs-lookup"><span data-stu-id="a77de-222">CLSID</span></span><br/>                    | <span data-ttu-id="a77de-223">CLSID \_ SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="a77de-223">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="a77de-224">IID</span><span class="sxs-lookup"><span data-stu-id="a77de-224">IID</span></span><br/>                      | <span data-ttu-id="a77de-225">IID \_ ISWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="a77de-225">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="a77de-226">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a77de-226">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a77de-227">WbemCimtypeEnum</span><span class="sxs-lookup"><span data-stu-id="a77de-227">WbemCimtypeEnum</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum)
</dt> <dt>

[<span data-ttu-id="a77de-228">Date/heure</span><span class="sxs-lookup"><span data-stu-id="a77de-228">DATETIME</span></span>](datetime.md)
</dt> <dt>

[<span data-ttu-id="a77de-229">Scripts d’objets d’API</span><span class="sxs-lookup"><span data-stu-id="a77de-229">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

