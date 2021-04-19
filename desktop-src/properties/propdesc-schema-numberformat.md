---
description: 'Spécifie comment IPropertyDescription :: FormatForDisplay doit mettre en forme la valeur de la propriété en tant que chaîne. Cela s’applique uniquement si <displayInfo displayType=&\#0034;Number&\#0034;> .'
ms.assetid: 9e8cfe5c-e17a-40d6-958f-a1bd1130c699
title: numberFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6750a9fb4dcf6a7a56c350fccf80241644b956da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106540845"
---
# <a name="numberformat"></a><span data-ttu-id="59c60-104">numberFormat</span><span class="sxs-lookup"><span data-stu-id="59c60-104">numberFormat</span></span>

<span data-ttu-id="59c60-105">Spécifie comment [**IPropertyDescription :: FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) doit mettre en forme la valeur de la propriété en tant que chaîne.</span><span class="sxs-lookup"><span data-stu-id="59c60-105">Specifies how [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) should format the property's value as a string.</span></span> <span data-ttu-id="59c60-106">Cela s’applique uniquement si <displayInfo displayType="Number"> .</span><span class="sxs-lookup"><span data-stu-id="59c60-106">This is applicable only if <displayInfo displayType="Number">.</span></span> <span data-ttu-id="59c60-107">Il ne doit y avoir qu’un seul élément [NumberFormat]() pour chaque élément [displayInfo](./propdesc-schema-displayinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="59c60-107">There should be only one [numberFormat]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="59c60-108">S’il y a plusieurs éléments, le dernier est utilisé.</span><span class="sxs-lookup"><span data-stu-id="59c60-108">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="59c60-109">Si aucun élément [NumberFormat]() n’est fourni, les paramètres d’attribut par défaut sont appliqués à la description de la propriété.</span><span class="sxs-lookup"><span data-stu-id="59c60-109">If no [numberFormat]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="59c60-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="59c60-110">Syntax</span></span>


```
      <!-- numberFormat -->
      <xs:element name="numberFormat"  minOccurs="0" maxOccurs="1">
        <xs:complexType>
          <xs:attribute name="formatAs">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="General"/>
                <xs:enumeration value="Percentage"/>
                <xs:enumeration value="ByteSize"/>
                <xs:enumeration value="KBSize"/>
                <xs:enumeration value="SampleSize"/>
                <xs:enumeration value="Bitrate"/>
                <xs:enumeration value="SampleRate"/>
                <xs:enumeration value="FrameRate"/>
                <xs:enumeration value="Pixels"/>
                <xs:enumeration value="DPI"/>
                <xs:enumeration value="Duration"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
          <xs:attribute name="formatDurationAs">
              <xs:restriction base="xs:string">
                <xs:enumeration value="hh:mm"/>
                <xs:enumeration value="hh:mm:ss"/>
                <xs:enumeration value="hh:mm:ss.fff"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
        </xs:complexType>
      </xs:element>
```



## <a name="element-information"></a><span data-ttu-id="59c60-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="59c60-111">Element Information</span></span>



| <span data-ttu-id="59c60-112">Élément parent</span><span class="sxs-lookup"><span data-stu-id="59c60-112">Parent Element</span></span>                                   | <span data-ttu-id="59c60-113">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="59c60-113">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="59c60-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="59c60-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="59c60-115">Aucun</span><span class="sxs-lookup"><span data-stu-id="59c60-115">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="59c60-116">Attributs</span><span class="sxs-lookup"><span data-stu-id="59c60-116">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="59c60-117">Attribut</span><span class="sxs-lookup"><span data-stu-id="59c60-117">Attribute</span></span></th>
<th><span data-ttu-id="59c60-118">Description</span><span class="sxs-lookup"><span data-stu-id="59c60-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="59c60-119">formatas</span><span class="sxs-lookup"><span data-stu-id="59c60-119">formatAs</span></span></td>
<td><span data-ttu-id="59c60-120">Public.</span><span class="sxs-lookup"><span data-stu-id="59c60-120">Public.</span></span> <span data-ttu-id="59c60-121">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="59c60-121">Optional.</span></span> <span data-ttu-id="59c60-122">La valeur par défaut est &quot; général &quot; .</span><span class="sxs-lookup"><span data-stu-id="59c60-122">Default is &quot;General&quot;.</span></span> <span data-ttu-id="59c60-123">Spécifie le format d’affichage.</span><span class="sxs-lookup"><span data-stu-id="59c60-123">Specifies the display format.</span></span> <span data-ttu-id="59c60-124">Les valeurs valides sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="59c60-124">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="59c60-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="59c60-125">Value</span></span></th>
<th><span data-ttu-id="59c60-126">Signification</span><span class="sxs-lookup"><span data-stu-id="59c60-126">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="59c60-127">Général</span><span class="sxs-lookup"><span data-stu-id="59c60-127">General</span></span></td>
<td><span data-ttu-id="59c60-128">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="59c60-128">Default.</span></span> <span data-ttu-id="59c60-129">Affiche la valeur sous la forme d’un nombre sans mise en forme.</span><span class="sxs-lookup"><span data-stu-id="59c60-129">Displays the value as an unformatted number.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="59c60-130">Pourcentage</span><span class="sxs-lookup"><span data-stu-id="59c60-130">Percentage</span></span></td>
<td><span data-ttu-id="59c60-131">Met en forme la valeur sous la forme d’un pourcentage.</span><span class="sxs-lookup"><span data-stu-id="59c60-131">Formats the value as a percentage.</span></span> <span data-ttu-id="59c60-132">Requiert que la propriété soit UInt32.</span><span class="sxs-lookup"><span data-stu-id="59c60-132">Requires the property to be UInt32.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="59c60-133">Taille d’octet</span><span class="sxs-lookup"><span data-stu-id="59c60-133">ByteSize</span></span></td>
<td><span data-ttu-id="59c60-134">Met en forme la valeur en tant qu’octet, &quot; Ko &quot; , &quot; Mo &quot; ou &quot; Go, selon le &quot; cas.</span><span class="sxs-lookup"><span data-stu-id="59c60-134">Formats the value as a byte, &quot;KB&quot;, &quot;MB&quot;, or &quot;GB&quot; as appropriate.</span></span> <span data-ttu-id="59c60-135">Requiert que la propriété soit UInt64.</span><span class="sxs-lookup"><span data-stu-id="59c60-135">Requires the property to be UInt64.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="59c60-136">KBSize</span><span class="sxs-lookup"><span data-stu-id="59c60-136">KBSize</span></span></td>
<td><span data-ttu-id="59c60-137">Met en forme la valeur en tant que &quot; Ko &quot; , quelle que soit la valeur.</span><span class="sxs-lookup"><span data-stu-id="59c60-137">Formats the value as a &quot;KB&quot;, no matter what the value is.</span></span> <span data-ttu-id="59c60-138">Requiert que la propriété soit UInt64.</span><span class="sxs-lookup"><span data-stu-id="59c60-138">Requires the property to be UInt64.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="59c60-139">SampleSize</span><span class="sxs-lookup"><span data-stu-id="59c60-139">SampleSize</span></span></td>
<td><span data-ttu-id="59c60-140">Met en forme la valeur en tant que nombre de bits.</span><span class="sxs-lookup"><span data-stu-id="59c60-140">Formats the value as a number of bits.</span></span> <span data-ttu-id="59c60-141">Requiert que la propriété soit UInt32.</span><span class="sxs-lookup"><span data-stu-id="59c60-141">Requires the property to be UInt32.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="59c60-142">Débit binaire</span><span class="sxs-lookup"><span data-stu-id="59c60-142">BitRate</span></span></td>
<td><span data-ttu-id="59c60-143">Met en forme la valeur en &quot; Kbits/s &quot; .</span><span class="sxs-lookup"><span data-stu-id="59c60-143">Formats the value in &quot;Kbps&quot;.</span></span> <span data-ttu-id="59c60-144">Requiert que la propriété soit UInt32.</span><span class="sxs-lookup"><span data-stu-id="59c60-144">Requires the property to be UInt32.</span></span> <span data-ttu-id="59c60-145">La valeur doit être stockée en &quot; unités de bits par seconde &quot; .</span><span class="sxs-lookup"><span data-stu-id="59c60-145">The value must be stored in &quot;bits-per-second&quot; units.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="59c60-146">SampleRate</span><span class="sxs-lookup"><span data-stu-id="59c60-146">SampleRate</span></span></td>
<td><span data-ttu-id="59c60-147">Met en forme la valeur en &quot; kHz &quot; .</span><span class="sxs-lookup"><span data-stu-id="59c60-147">Formats the value in &quot;KHz&quot;.</span></span> <span data-ttu-id="59c60-148">Requiert que la propriété soit UInt32.</span><span class="sxs-lookup"><span data-stu-id="59c60-148">Requires the property to be UInt32.</span></span> <span data-ttu-id="59c60-149">La valeur doit être stockée en &quot; Hertz &quot; unités.</span><span class="sxs-lookup"><span data-stu-id="59c60-149">The value must be stored in &quot;Hertz&quot; units.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="59c60-150">FrameRate</span><span class="sxs-lookup"><span data-stu-id="59c60-150">FrameRate</span></span></td>
<td><span data-ttu-id="59c60-151">Met en forme la valeur en images/seconde.</span><span class="sxs-lookup"><span data-stu-id="59c60-151">Formats the value in frames/second.</span></span> <span data-ttu-id="59c60-152">Requiert que la propriété soit UInt32.</span><span class="sxs-lookup"><span data-stu-id="59c60-152">Requires the property to be UInt32.</span></span> <span data-ttu-id="59c60-153">La valeur doit être stockée en &quot; unités de kilo-images par &quot; seconde.</span><span class="sxs-lookup"><span data-stu-id="59c60-153">The value must be stored in &quot;kilo-frames-per-second&quot; units.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="59c60-154">Pixels</span><span class="sxs-lookup"><span data-stu-id="59c60-154">Pixels</span></span></td>
<td><span data-ttu-id="59c60-155">Met en forme la valeur en unités en pixels.</span><span class="sxs-lookup"><span data-stu-id="59c60-155">Formats the value in pixel units.</span></span> <span data-ttu-id="59c60-156">Requiert que la propriété soit UInt32.</span><span class="sxs-lookup"><span data-stu-id="59c60-156">Requires the property to be UInt32.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="59c60-157">PPP</span><span class="sxs-lookup"><span data-stu-id="59c60-157">DPI</span></span></td>
<td><span data-ttu-id="59c60-158">Met en forme la valeur en points par pouce.</span><span class="sxs-lookup"><span data-stu-id="59c60-158">Formats the value in dots-per-inch.</span></span> <span data-ttu-id="59c60-159">Requiert que la propriété soit UInt32.</span><span class="sxs-lookup"><span data-stu-id="59c60-159">Requires the property to be UInt32.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="59c60-160">Duration</span><span class="sxs-lookup"><span data-stu-id="59c60-160">Duration</span></span></td>
<td><span data-ttu-id="59c60-161">Met en forme la valeur en tant que durée.</span><span class="sxs-lookup"><span data-stu-id="59c60-161">Formats the value as a duration.</span></span> <span data-ttu-id="59c60-162">Utilisez <formatDurationAs> pour spécifier le format de durée.</span><span class="sxs-lookup"><span data-stu-id="59c60-162">Use <formatDurationAs> to specify the duration format.</span></span> <span data-ttu-id="59c60-163">Requiert que la propriété soit UInt64.</span><span class="sxs-lookup"><span data-stu-id="59c60-163">Requires the property to be UInt64.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="59c60-164">formatDurationAs</span><span class="sxs-lookup"><span data-stu-id="59c60-164">formatDurationAs</span></span></td>
<td><span data-ttu-id="59c60-165">Public.</span><span class="sxs-lookup"><span data-stu-id="59c60-165">Public.</span></span> <span data-ttu-id="59c60-166">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="59c60-166">Optional.</span></span> <span data-ttu-id="59c60-167">La valeur par défaut est &quot; hh : mm : SS &quot; .</span><span class="sxs-lookup"><span data-stu-id="59c60-167">Default is &quot;hh:mm:ss&quot;.</span></span> <span data-ttu-id="59c60-168">S’applique uniquement si <em>formatas &quot; = &quot; Duration</em>.</span><span class="sxs-lookup"><span data-stu-id="59c60-168">Only applies if <em>formatAs=&quot;Duration&quot;</em>.</span></span> <span data-ttu-id="59c60-169">Requiert que la propriété soit UInt64.</span><span class="sxs-lookup"><span data-stu-id="59c60-169">Requires the property to be UInt64.</span></span> <span data-ttu-id="59c60-170">Les valeurs valides sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="59c60-170">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="59c60-171">Valeur</span><span class="sxs-lookup"><span data-stu-id="59c60-171">Value</span></span></th>
<th><span data-ttu-id="59c60-172">Signification</span><span class="sxs-lookup"><span data-stu-id="59c60-172">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="59c60-173">hh:mm</span><span class="sxs-lookup"><span data-stu-id="59c60-173">hh:mm</span></span></td>
<td><span data-ttu-id="59c60-174">Met en forme la valeur en heures et minutes.</span><span class="sxs-lookup"><span data-stu-id="59c60-174">Formats the value in hours and minutes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="59c60-175">hh:mm:ss</span><span class="sxs-lookup"><span data-stu-id="59c60-175">hh:mm:ss</span></span></td>
<td><span data-ttu-id="59c60-176">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="59c60-176">Default.</span></span> <span data-ttu-id="59c60-177">Met en forme la valeur en heures, minutes et secondes.</span><span class="sxs-lookup"><span data-stu-id="59c60-177">Formats the value in hours, minutes, and seconds.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="59c60-178">hh : mm : SS. fff</span><span class="sxs-lookup"><span data-stu-id="59c60-178">hh:mm:ss.fff</span></span></td>
<td><span data-ttu-id="59c60-179">Met en forme la valeur en heures, minutes, secondes et millisecondes.</span><span class="sxs-lookup"><span data-stu-id="59c60-179">Formats the value in hours, minutes, seconds, and milliseconds.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
