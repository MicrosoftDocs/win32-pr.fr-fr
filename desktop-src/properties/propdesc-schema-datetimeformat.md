---
description: 'Spécifie comment IPropertyDescription :: FormatForDisplay doit mettre en forme la valeur de la propriété en tant que chaîne. Cela s’applique uniquement si <displayInfo displayType=&\#0034;DateTime&\#0034;> .'
ms.assetid: c290fb2e-ef5b-4dea-ba42-7c9e273a89dc
title: dateTimeFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 091898f77f4dcc37bbe65515f8606104a4d968bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202237"
---
# <a name="datetimeformat"></a><span data-ttu-id="977d5-104">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="977d5-104">dateTimeFormat</span></span>

<span data-ttu-id="977d5-105">Spécifie comment [**IPropertyDescription :: FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) doit mettre en forme la valeur de la propriété en tant que chaîne.</span><span class="sxs-lookup"><span data-stu-id="977d5-105">Specifies how [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) should format the property's value as a string.</span></span> <span data-ttu-id="977d5-106">Cela s’applique uniquement si <displayInfo displayType="DateTime"> .</span><span class="sxs-lookup"><span data-stu-id="977d5-106">This is applicable only if <displayInfo displayType="DateTime">.</span></span> <span data-ttu-id="977d5-107">Il ne doit y avoir qu’un seul élément [DateTimeFormat]() pour chaque élément [displayInfo](./propdesc-schema-displayinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="977d5-107">There should be only one [dateTimeFormat]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="977d5-108">S’il y a plusieurs éléments, le dernier est utilisé.</span><span class="sxs-lookup"><span data-stu-id="977d5-108">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="977d5-109">Si aucun élément [DateTimeFormat]() n’est fourni, les paramètres d’attribut par défaut sont appliqués à la description de la propriété.</span><span class="sxs-lookup"><span data-stu-id="977d5-109">If no [dateTimeFormat]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="977d5-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="977d5-110">Syntax</span></span>


```
      <!-- dateTimeFormat -->
      <xs:element name="dateTimeFormat"  minOccurs="0" maxOccurs="1">
        <xs:complexType>
          <xs:attribute name="formatAs">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="General"/>
                <xs:enumeration value="Month"/>
                <xs:enumeration value="YearMonth"/>
                <xs:enumeration value="Year"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
          <xs:attribute name="formatTimeAs">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="ShortTime"/>
                <xs:enumeration value="LongTime"/>
                <xs:enumeration value="HideTime"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
          <xs:attribute name="formatDateAs">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="ShortDate"/>
                <xs:enumeration value="LongDate"/>
                <xs:enumeration value="HideDate"/>
                <xs:enumeration value="RelativeShortDate"/>
                <xs:enumeration value="RelativeLongDate"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
        </xs:complexType>
      </xs:element>
```



## <a name="element-information"></a><span data-ttu-id="977d5-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="977d5-111">Element Information</span></span>



| <span data-ttu-id="977d5-112">Élément parent</span><span class="sxs-lookup"><span data-stu-id="977d5-112">Parent Element</span></span>                                   | <span data-ttu-id="977d5-113">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="977d5-113">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="977d5-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="977d5-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="977d5-115">Aucun</span><span class="sxs-lookup"><span data-stu-id="977d5-115">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="977d5-116">Attributs</span><span class="sxs-lookup"><span data-stu-id="977d5-116">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="977d5-117">Attribut</span><span class="sxs-lookup"><span data-stu-id="977d5-117">Attribute</span></span></th>
<th><span data-ttu-id="977d5-118">Description</span><span class="sxs-lookup"><span data-stu-id="977d5-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="977d5-119">formatas</span><span class="sxs-lookup"><span data-stu-id="977d5-119">formatAs</span></span></td>
<td><span data-ttu-id="977d5-120">Public.</span><span class="sxs-lookup"><span data-stu-id="977d5-120">Public.</span></span> <span data-ttu-id="977d5-121">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="977d5-121">Optional.</span></span> <span data-ttu-id="977d5-122">La valeur par défaut est &quot; général &quot; .</span><span class="sxs-lookup"><span data-stu-id="977d5-122">Default is &quot;General&quot;.</span></span> <span data-ttu-id="977d5-123">Les valeurs valides sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="977d5-123">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="977d5-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="977d5-124">Value</span></span></th>
<th><span data-ttu-id="977d5-125">Signification</span><span class="sxs-lookup"><span data-stu-id="977d5-125">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="977d5-126">Général</span><span class="sxs-lookup"><span data-stu-id="977d5-126">General</span></span></td>
<td><span data-ttu-id="977d5-127">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="977d5-127">Default.</span></span> <span data-ttu-id="977d5-128">Met en forme la valeur de date et d’heure à l’aide de <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shformatdatetimea"><strong>SHFormatDateTime</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="977d5-128">Formats the date-time value using <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shformatdatetimea"><strong>SHFormatDateTime</strong></a>.</span></span> <span data-ttu-id="977d5-129">Utilisez les attributs <em>formatTimeAs</em> et <em>formatDateAs</em> pour spécifier le mode de mise en forme de la date et de l’heure.</span><span class="sxs-lookup"><span data-stu-id="977d5-129">Use the <em>formatTimeAs</em> and <em>formatDateAs</em> attributes to specify how the time and date are formatted.</span></span> <span data-ttu-id="977d5-130">Requiert que le type de propriété soit DateTime.</span><span class="sxs-lookup"><span data-stu-id="977d5-130">Requires the property type to be DateTime.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="977d5-131">Month</span><span class="sxs-lookup"><span data-stu-id="977d5-131">Month</span></span></td>
<td><span data-ttu-id="977d5-132">Met en forme la valeur en tant qu’un des mois de l’année.</span><span class="sxs-lookup"><span data-stu-id="977d5-132">Formats the value as one of the months of the year.</span></span> <span data-ttu-id="977d5-133">Requiert que le type de propriété soit Int32.</span><span class="sxs-lookup"><span data-stu-id="977d5-133">Requires the property type to be Int32.</span></span> <span data-ttu-id="977d5-134">La valeur doit être stockée sous la forme d’une valeur numérique avec 1 représentant le premier mois de l’année.</span><span class="sxs-lookup"><span data-stu-id="977d5-134">The value must be stored as a numeric value with 1 representing the first month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="977d5-135">YearMonth</span><span class="sxs-lookup"><span data-stu-id="977d5-135">YearMonth</span></span></td>
<td><span data-ttu-id="977d5-136">Met en forme la valeur en tant qu' &quot; année-mois &quot; .</span><span class="sxs-lookup"><span data-stu-id="977d5-136">Formats the value as &quot;Year - Month&quot;.</span></span> <span data-ttu-id="977d5-137">Requiert que le type de propriété soit Int32.</span><span class="sxs-lookup"><span data-stu-id="977d5-137">Requires the property type to be Int32.</span></span> <span data-ttu-id="977d5-138">La valeur doit être stockée de manière à ce que les deux octets les plus élevés spécifient l’année et les deux octets inférieurs spécifient le mois.</span><span class="sxs-lookup"><span data-stu-id="977d5-138">The value must be stored such that the two highest bytes specify the year and the lower two bytes specify the month.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="977d5-139">Year</span><span class="sxs-lookup"><span data-stu-id="977d5-139">Year</span></span></td>
<td><span data-ttu-id="977d5-140">Met en forme la valeur sous la forme d’une chaîne simple.</span><span class="sxs-lookup"><span data-stu-id="977d5-140">Formats the value as a simple string.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="977d5-141">formatTimeAs</span><span class="sxs-lookup"><span data-stu-id="977d5-141">formatTimeAs</span></span></td>
<td><span data-ttu-id="977d5-142">Public.</span><span class="sxs-lookup"><span data-stu-id="977d5-142">Public.</span></span> <span data-ttu-id="977d5-143">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="977d5-143">Optional.</span></span> <span data-ttu-id="977d5-144">La valeur par défaut est &quot; ShortTime &quot; .</span><span class="sxs-lookup"><span data-stu-id="977d5-144">Default is &quot;ShortTime&quot;.</span></span> <span data-ttu-id="977d5-145">Spécifie le format d’affichage de l’heure.</span><span class="sxs-lookup"><span data-stu-id="977d5-145">Specifies the format in which to display time.</span></span> <span data-ttu-id="977d5-146">S’applique quand <strong>formatas &quot; = &quot; General</strong>.</span><span class="sxs-lookup"><span data-stu-id="977d5-146">Applies when <strong>formatAs=&quot;General&quot;</strong>.</span></span> <span data-ttu-id="977d5-147">Les valeurs valides sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="977d5-147">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="977d5-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="977d5-148">Value</span></span></th>
<th><span data-ttu-id="977d5-149">Signification</span><span class="sxs-lookup"><span data-stu-id="977d5-149">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="977d5-150">ShortTime</span><span class="sxs-lookup"><span data-stu-id="977d5-150">ShortTime</span></span></td>
<td><span data-ttu-id="977d5-151">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="977d5-151">Default.</span></span> <span data-ttu-id="977d5-152">Affichez l’heure comme &quot; 7:48 PM &quot; .</span><span class="sxs-lookup"><span data-stu-id="977d5-152">Show the time like &quot;7:48 PM&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="977d5-153">Expérimenté</span><span class="sxs-lookup"><span data-stu-id="977d5-153">LongTime</span></span></td>
<td><span data-ttu-id="977d5-154">Affichez l’heure comme &quot; 7:48:33 PM &quot; .</span><span class="sxs-lookup"><span data-stu-id="977d5-154">Show the time like &quot;7:48:33 PM&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="977d5-155">HideTime</span><span class="sxs-lookup"><span data-stu-id="977d5-155">HideTime</span></span></td>
<td><span data-ttu-id="977d5-156">N’affiche pas la partie heure de la date.</span><span class="sxs-lookup"><span data-stu-id="977d5-156">Do not display the time portion of the date.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="977d5-157">formatDateAs</span><span class="sxs-lookup"><span data-stu-id="977d5-157">formatDateAs</span></span></td>
<td><span data-ttu-id="977d5-158">Public.</span><span class="sxs-lookup"><span data-stu-id="977d5-158">Public.</span></span> <span data-ttu-id="977d5-159">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="977d5-159">Optional.</span></span> <span data-ttu-id="977d5-160">La valeur par défaut est &quot; SHORTDATE &quot; .</span><span class="sxs-lookup"><span data-stu-id="977d5-160">Default is &quot;ShortDate&quot;.</span></span> <span data-ttu-id="977d5-161">Spécifie le format d’affichage de la date.</span><span class="sxs-lookup"><span data-stu-id="977d5-161">Specifies the format in which to display the date.</span></span> <span data-ttu-id="977d5-162">S’applique quand <strong>formatas &quot; = &quot; General</strong>.</span><span class="sxs-lookup"><span data-stu-id="977d5-162">Applies when <strong>formatAs=&quot;General&quot;</strong>.</span></span> <span data-ttu-id="977d5-163">Les valeurs valides sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="977d5-163">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="977d5-164">Valeur</span><span class="sxs-lookup"><span data-stu-id="977d5-164">Value</span></span></th>
<th><span data-ttu-id="977d5-165">Exemple</span><span class="sxs-lookup"><span data-stu-id="977d5-165">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="977d5-166">ShortDate</span><span class="sxs-lookup"><span data-stu-id="977d5-166">ShortDate</span></span></td>
<td><span data-ttu-id="977d5-167">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="977d5-167">Default.</span></span> <span data-ttu-id="977d5-168">Affichez la date comme &quot; 5/13/59 &quot; .</span><span class="sxs-lookup"><span data-stu-id="977d5-168">Show the date like &quot;5/13/59&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="977d5-169">LongDate</span><span class="sxs-lookup"><span data-stu-id="977d5-169">LongDate</span></span></td>
<td><span data-ttu-id="977d5-170">Affichez la date &quot; , par exemple mercredi 13 mai, 1959 &quot; .</span><span class="sxs-lookup"><span data-stu-id="977d5-170">Show the date like &quot;Wednesday, May 13, 1959&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="977d5-171">HideDate</span><span class="sxs-lookup"><span data-stu-id="977d5-171">HideDate</span></span></td>
<td><span data-ttu-id="977d5-172">N’affiche pas la partie date.</span><span class="sxs-lookup"><span data-stu-id="977d5-172">Do not display the date portion.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="977d5-173">RelativeShortDate</span><span class="sxs-lookup"><span data-stu-id="977d5-173">RelativeShortDate</span></span></td>
<td><span data-ttu-id="977d5-174">Affichez la date comme &quot; SHORTDATE &quot; , mais utilisez des descriptions relatives, par exemple hier, dans la mesure du &quot; &quot; possible.</span><span class="sxs-lookup"><span data-stu-id="977d5-174">Show the date like &quot;ShortDate&quot;, but use relative descriptions, such as &quot;yesterday&quot;, whenever possible.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="977d5-175">RelativeLongDate</span><span class="sxs-lookup"><span data-stu-id="977d5-175">RelativeLongDate</span></span></td>
<td><span data-ttu-id="977d5-176">Affichez la date comme &quot; LongDate &quot; , mais utilisez des descriptions relatives, par exemple hier, dans la mesure du &quot; &quot; possible.</span><span class="sxs-lookup"><span data-stu-id="977d5-176">Show the date like &quot;LongDate&quot;, but use relative descriptions, such as &quot;yesterday&quot;, whenever possible.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
