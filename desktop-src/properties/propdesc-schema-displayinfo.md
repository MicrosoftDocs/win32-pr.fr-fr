---
description: Spécifie les informations d’affichage d’une propriété.
ms.assetid: 27c03ced-a5fa-4ab4-b88e-5b78701da878
title: displayInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fff0bb441b4535c0b6c6f3183671fbe8ade09183
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518701"
---
# <a name="displayinfo"></a><span data-ttu-id="34703-103">displayInfo</span><span class="sxs-lookup"><span data-stu-id="34703-103">displayInfo</span></span>

<span data-ttu-id="34703-104">Spécifie les informations d’affichage d’une propriété.</span><span class="sxs-lookup"><span data-stu-id="34703-104">Specifies a property's display information.</span></span> <span data-ttu-id="34703-105">Il ne doit y avoir qu’un seul élément [displayInfo]() pour chaque [PropertyDescription](./propdesc-schema-propertydescription.md).</span><span class="sxs-lookup"><span data-stu-id="34703-105">There should be only one [displayInfo]() element for each [propertyDescription](./propdesc-schema-propertydescription.md).</span></span>

<span data-ttu-id="34703-106">S’il y a plusieurs éléments, le dernier est utilisé.</span><span class="sxs-lookup"><span data-stu-id="34703-106">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="34703-107">Si aucun élément [displayInfo]() n’est fourni, les paramètres d’attribut par défaut sont appliqués à la description de la propriété.</span><span class="sxs-lookup"><span data-stu-id="34703-107">If no [displayInfo]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="34703-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="34703-108">Syntax</span></span>


```
<!-- displayInfo -->
<xs:element name="displayInfo">
    <xs:complexType>
        <xs:all>
            <xs:element name="stringFormat" minOccurs="0" maxOccurs="1">
                <xs:complexType>
                    <xs:attribute name="formatAs">
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="General"/>
                                <xs:enumeration value="FileName"/>
                                <xs:enumeration value="FilePath"/>
                                <xs:enumeration value="Hyperlink"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
            <xs:element name="booleanFormat" minOccurs="0" maxOccurs="1">
                <xs:complexType>
                    <xs:attribute name="formatAs">
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="YesNo"/>
                                <xs:enumeration value="OnOff"/>
                                <xs:enumeration value="TrueFalse"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
            <xs:element name="numberFormat" minOccurs="0" maxOccurs="1">
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
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="hh:mm"/>
                                <xs:enumeration value="hh:mm:ss"/>
                                <xs:enumeration value="hh:mm:ss.fff"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
            <xs:element name="dateTimeFormat" minOccurs="0" maxOccurs="1">
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
            <xs:element name="enumeratedList" minOccurs="0" maxOccurs="1">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="enum" minOccurs="0" maxOccurs="unbounded">
                            <xs:complexType>
                                <xs:attribute name="value" type="xs:string" use="required"/>
                                <xs:attribute name="text" type="xs:string" use="required"/>
                            </xs:complexType>
                        </xs:element>
                        <xs:element name="enumRange" minOccurs="0" maxOccurs="unbounded">
                            <xs:complexType>
                                <xs:attribute name="minValue" type="xs:string" use="required"/>
                                <xs:attribute name="setValue" type="xs:string"/>
                                <xs:attribute name="text" type="xs:string"/>
                            </xs:complexType>
                        </xs:element>
                    </xs:sequence>

                    <xs:attribute name="defaultText" type="xs:string"/>
                    <xs:attribute name="useValueForDefault" type="xs:boolean"/>
                </xs:complexType>
            </xs:element>
            <xs:element name="drawControl" minOccurs="0" maxOccurs="1">
                <xs:complexType>
                    <xs:attribute name="control">
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="Default"/>
                                <xs:enumeration value="MultiLineText"/>
                                <xs:enumeration value="MultiValueText"/>
                                <xs:enumeration value="PercentBar"/>
                                <xs:enumeration value="ProgressBar"/>
                                <xs:enumeration value="Rating"/>
                                <xs:enumeration value="StaticText"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
            <xs:element name="editControl" minOccurs="0" maxOccurs="1">
                <xs:complexType>
                    <xs:attribute name="control">
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="Default"/>
                                <xs:enumeration value="Calendar"/>
                                <xs:enumeration value="CheckboxDropList"/>
                                <xs:enumeration value="DropList"/>
                                <xs:enumeration value="MultiLineText"/>
                                <xs:enumeration value="MultiValueText"/>
                                <xs:enumeration value="Rating"/>
                                <xs:enumeration value="Text"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
            <xs:element name="filterControl" minOccurs="0" maxOccurs="1">
                <xs:complexType>
                    <xs:attribute name="control">
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="Default"/>
                                <xs:enumeration value="Calendar"/>
                                <xs:enumeration value="Rating"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
            <xs:element name="queryControl" minOccurs="0" maxOccurs="1">
                <xs:complexType>
                    <xs:attribute name="control">
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="Default"/>
                                <xs:enumeration value="Boolean"/>
                                <xs:enumeration value="Calendar"/>
                                <xs:enumeration value="CheckboxDropList"/>
                                <xs:enumeration value="DropList"/>
                                <xs:enumeration value="MultiValueText"/>
                                <xs:enumeration value="NumericText"/>
                                <xs:enumeration value="Rating"/>
                                <xs:enumeration value="Text"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
        </xs:all>

        <xs:attribute name="defaultColumnWidth" type="xs:nonNegativeInteger" default="20"/>
        <xs:attribute name="displayType">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="String"/>
                    <xs:enumeration value="Number"/>
                    <xs:enumeration value="Boolean"/>
                    <xs:enumeration value="DateTime"/>
                    <xs:enumeration value="Enumerated"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        
        <xs:attribute name="alignment" default="Left">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Left"/>
                    <xs:enumeration value="Center"/>
                    <xs:enumeration value="Right"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="relativeDescriptionType">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="General"/>
                    <xs:enumeration value="Date"/>
                    <xs:enumeration value="Size"/>
                    <xs:enumeration value="Count"/>
                    <xs:enumeration value="Revision"/>
                    <xs:enumeration value="Length"/>
                    <xs:enumeration value="Duration"/>
                    <xs:enumeration value="Speed"/>
                    <xs:enumeration value="Rate"/>
                    <xs:enumeration value="Rating"/>
                    <xs:enumeration value="Priority"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="defaultSortDirection" default="Ascending">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                  <xs:enumeration value="Ascending"/>
                  <xs:enumeration value="Descending"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="34703-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="34703-109">Element Information</span></span>



| <span data-ttu-id="34703-110">Élément parent</span><span class="sxs-lookup"><span data-stu-id="34703-110">Parent Element</span></span>                                                   | <span data-ttu-id="34703-111">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="34703-111">Child Elements</span></span>                                                                                                 |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="34703-112">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="34703-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md) | [<span data-ttu-id="34703-113">stringFormat</span><span class="sxs-lookup"><span data-stu-id="34703-113">stringFormat</span></span>](./propdesc-schema-stringformat.md)                                                             |
|                                                                  | [<span data-ttu-id="34703-114">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="34703-114">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)                                                           |
|                                                                  | [<span data-ttu-id="34703-115">numberFormat</span><span class="sxs-lookup"><span data-stu-id="34703-115">numberFormat</span></span>](./propdesc-schema-numberformat.md)                                                             |
|                                                                  | [<span data-ttu-id="34703-116">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="34703-116">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)                                                         |
|                                                                  | [<span data-ttu-id="34703-117">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="34703-117">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)                                                         |
|                                                                  | [<span data-ttu-id="34703-118">drawControl</span><span class="sxs-lookup"><span data-stu-id="34703-118">drawControl</span></span>](./propdesc-schema-drawcontrol.md)                                                               |
|                                                                  | [<span data-ttu-id="34703-119">editControl</span><span class="sxs-lookup"><span data-stu-id="34703-119">editControl</span></span>](./propdesc-schema-editcontrol.md)                                                               |
|                                                                  | [<span data-ttu-id="34703-120">filterControl</span><span class="sxs-lookup"><span data-stu-id="34703-120">filterControl</span></span>](./propdesc-schema-filtercontrol.md)                                                           |
|                                                                  | <span data-ttu-id="34703-121">[queryControl](./propdesc-schema-querycontrol.md) (Windows Vista uniquement.</span><span class="sxs-lookup"><span data-stu-id="34703-121">[queryControl](./propdesc-schema-querycontrol.md) (Windows Vista only.</span></span> <span data-ttu-id="34703-122">Non pris en charge dans Windows 7 et versions ultérieures.)</span><span class="sxs-lookup"><span data-stu-id="34703-122">Not supported in Windows 7 and later.)</span></span> |



 

## <a name="attributes"></a><span data-ttu-id="34703-123">Attributs</span><span class="sxs-lookup"><span data-stu-id="34703-123">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="34703-124">Attribut</span><span class="sxs-lookup"><span data-stu-id="34703-124">Attribute</span></span></th>
<th><span data-ttu-id="34703-125">Description</span><span class="sxs-lookup"><span data-stu-id="34703-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="34703-126">defaultColumnWidth</span><span class="sxs-lookup"><span data-stu-id="34703-126">defaultColumnWidth</span></span></td>
<td><span data-ttu-id="34703-127">Public.</span><span class="sxs-lookup"><span data-stu-id="34703-127">Public.</span></span> <span data-ttu-id="34703-128">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="34703-128">Optional.</span></span> <span data-ttu-id="34703-129">La valeur par défaut est &quot; 20 &quot; .</span><span class="sxs-lookup"><span data-stu-id="34703-129">Default is &quot;20&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34703-130">displayType</span><span class="sxs-lookup"><span data-stu-id="34703-130">displayType</span></span></td>
<td><span data-ttu-id="34703-131">Public.</span><span class="sxs-lookup"><span data-stu-id="34703-131">Public.</span></span> <span data-ttu-id="34703-132">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="34703-132">Optional.</span></span> <span data-ttu-id="34703-133">La valeur par défaut est &quot; String &quot; .</span><span class="sxs-lookup"><span data-stu-id="34703-133">Default is &quot;String&quot;.</span></span> <span data-ttu-id="34703-134">Spécifie le type de la chaîne d’affichage.</span><span class="sxs-lookup"><span data-stu-id="34703-134">Specifies the type of the display string.</span></span> <span data-ttu-id="34703-135">Une fois définis ici, les valeurs de <strong>PROPDESC_DISPLAYTYPE</strong> associées sont récupérées par <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getdisplaytype"><strong>IPropertyDescription :: GetDisplayType</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="34703-135">Once set here, the associated <strong>PROPDESC_DISPLAYTYPE</strong> values are retrieved by <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getdisplaytype"><strong>IPropertyDescription::GetDisplayType</strong></a>.</span></span> <span data-ttu-id="34703-136">Les types suivants sont valides.</span><span class="sxs-lookup"><span data-stu-id="34703-136">The following are valid types.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="34703-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="34703-137">Value</span></span></th>
<th><span data-ttu-id="34703-138">Signification</span><span class="sxs-lookup"><span data-stu-id="34703-138">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="34703-139">String</span><span class="sxs-lookup"><span data-stu-id="34703-139">String</span></span></td>
<td><span data-ttu-id="34703-140">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="34703-140">Default.</span></span> <span data-ttu-id="34703-141">La valeur est affichée sous la forme d’une chaîne.</span><span class="sxs-lookup"><span data-stu-id="34703-141">Value is displayed as a string.</span></span> <span data-ttu-id="34703-142">Utilisez &quot; stringFormat &quot; pour mettre en forme.</span><span class="sxs-lookup"><span data-stu-id="34703-142">Use &quot;stringFormat&quot; to format.</span></span> <span data-ttu-id="34703-143">La méthode retourne PDDT_STRING.</span><span class="sxs-lookup"><span data-stu-id="34703-143">Method returns PDDT_STRING.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34703-144">Number</span><span class="sxs-lookup"><span data-stu-id="34703-144">Number</span></span></td>
<td><span data-ttu-id="34703-145">Valeur par défaut pour les propriétés numériques.</span><span class="sxs-lookup"><span data-stu-id="34703-145">Default for numeric properties.</span></span> <span data-ttu-id="34703-146">La valeur est affichée sous la forme d’un nombre.</span><span class="sxs-lookup"><span data-stu-id="34703-146">Value is displayed as a number.</span></span> <span data-ttu-id="34703-147">Utilisez &quot; NumberFormat &quot; pour mettre en forme.</span><span class="sxs-lookup"><span data-stu-id="34703-147">Use &quot;numberFormat&quot; to format.</span></span> <span data-ttu-id="34703-148">La méthode retourne PDDT_NUMBER.</span><span class="sxs-lookup"><span data-stu-id="34703-148">Method returns PDDT_NUMBER.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34703-149">Boolean</span><span class="sxs-lookup"><span data-stu-id="34703-149">Boolean</span></span></td>
<td><span data-ttu-id="34703-150">Valeur par défaut si <typeInfo type=&quot;Boolean&quot;> .</span><span class="sxs-lookup"><span data-stu-id="34703-150">Default if <typeInfo type=&quot;Boolean&quot;>.</span></span> <span data-ttu-id="34703-151">La valeur est affichée sous la forme d’une valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="34703-151">Value is displayed as a boolean.</span></span> <span data-ttu-id="34703-152">Utilisez &quot; BooleanFormat &quot; pour mettre en forme.</span><span class="sxs-lookup"><span data-stu-id="34703-152">Use &quot;booleanFormat&quot; to format.</span></span> <span data-ttu-id="34703-153">La méthode retourne PDDT_BOOLEAN.</span><span class="sxs-lookup"><span data-stu-id="34703-153">Method returns PDDT_BOOLEAN.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34703-154">DateTime</span><span class="sxs-lookup"><span data-stu-id="34703-154">DateTime</span></span></td>
<td><span data-ttu-id="34703-155">Valeur par défaut si <typeInfo type=&quot;DateTime&quot;> .</span><span class="sxs-lookup"><span data-stu-id="34703-155">Default if <typeInfo type=&quot;DateTime&quot;>.</span></span> <span data-ttu-id="34703-156">La valeur est affichée sous la forme d’une date ou d’une heure.</span><span class="sxs-lookup"><span data-stu-id="34703-156">Value is displayed as a date or time.</span></span> <span data-ttu-id="34703-157">Utilisez &quot; DateTimeFormat &quot; pour mettre en forme.</span><span class="sxs-lookup"><span data-stu-id="34703-157">Use &quot;dateTimeFormat&quot; to format.</span></span> <span data-ttu-id="34703-158">La méthode retourne PDDT_DATETIME.</span><span class="sxs-lookup"><span data-stu-id="34703-158">Method returns PDDT_DATETIME.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34703-159">Énumération</span><span class="sxs-lookup"><span data-stu-id="34703-159">Enumeration</span></span></td>
<td><span data-ttu-id="34703-160">La valeur est affichée sous la forme d’un mappage de chaîne d’affichage fourni par l' &quot; &quot; élément enumeratedList.</span><span class="sxs-lookup"><span data-stu-id="34703-160">Value is displayed as a display string mapping provided by the &quot;enumeratedList&quot; element.</span></span> <span data-ttu-id="34703-161">La méthode retourne PDDT_ENUMERATED.</span><span class="sxs-lookup"><span data-stu-id="34703-161">Method returns PDDT_ENUMERATED.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34703-162">alignement</span><span class="sxs-lookup"><span data-stu-id="34703-162">alignment</span></span></td>
<td><span data-ttu-id="34703-163">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="34703-163">Optional.</span></span> <span data-ttu-id="34703-164">La valeur par défaut est &quot; gauche &quot; .</span><span class="sxs-lookup"><span data-stu-id="34703-164">Default is &quot;Left&quot;.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="34703-165">Valeur</span><span class="sxs-lookup"><span data-stu-id="34703-165">Value</span></span></th>
<th><span data-ttu-id="34703-166">Signification</span><span class="sxs-lookup"><span data-stu-id="34703-166">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="34703-167">Gauche</span><span class="sxs-lookup"><span data-stu-id="34703-167">Left</span></span></td>
<td><span data-ttu-id="34703-168">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="34703-168">Default.</span></span> <span data-ttu-id="34703-169">Aligner à gauche.</span><span class="sxs-lookup"><span data-stu-id="34703-169">Align left.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34703-170">Center</span><span class="sxs-lookup"><span data-stu-id="34703-170">Center</span></span></td>
<td><span data-ttu-id="34703-171">Aligner le centre.</span><span class="sxs-lookup"><span data-stu-id="34703-171">Align center.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34703-172">Right</span><span class="sxs-lookup"><span data-stu-id="34703-172">Right</span></span></td>
<td><span data-ttu-id="34703-173">Aligner à droite.</span><span class="sxs-lookup"><span data-stu-id="34703-173">Align right.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34703-174">relativeDescriptionType</span><span class="sxs-lookup"><span data-stu-id="34703-174">relativeDescriptionType</span></span></td>
<td><span data-ttu-id="34703-175">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="34703-175">Optional.</span></span> <span data-ttu-id="34703-176">La valeur par défaut est &quot; général &quot; .</span><span class="sxs-lookup"><span data-stu-id="34703-176">Default is &quot;General&quot;.</span></span> <span data-ttu-id="34703-177">Spécifie comment deux valeurs de cette propriété doivent être décrites lorsqu’elles sont comparées les unes avec les autres.</span><span class="sxs-lookup"><span data-stu-id="34703-177">Specifies how two values of this property should be described when they are compared with one another.</span></span> <span data-ttu-id="34703-178">Dans le cas d’une équivalence, &quot; même &quot; est toujours utilisé.</span><span class="sxs-lookup"><span data-stu-id="34703-178">In the case of equivalency, &quot;Same&quot; is always used.</span></span> <span data-ttu-id="34703-179"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getrelativedescription"><strong>IPropertyDescription :: GetRelativeDescription</strong></a> et <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getrelativedescriptiontype"><strong>IPropertyDescription :: GetRelativeDescriptionType</strong></a> utilisent cette valeur pour déterminer les noms d’affichage de description relative à utiliser.</span><span class="sxs-lookup"><span data-stu-id="34703-179"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getrelativedescription"><strong>IPropertyDescription::GetRelativeDescription</strong></a> and <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getrelativedescriptiontype"><strong>IPropertyDescription::GetRelativeDescriptionType</strong></a> use this value to determine what relative description display names to use.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="34703-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="34703-180">Value</span></span></th>
<th><span data-ttu-id="34703-181">Signification</span><span class="sxs-lookup"><span data-stu-id="34703-181">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="34703-182">Général</span><span class="sxs-lookup"><span data-stu-id="34703-182">General</span></span></td>
<td><span data-ttu-id="34703-183">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="34703-183">Default.</span></span> <span data-ttu-id="34703-184">Utilise des différences différentes &quot; &quot;  /  &quot; &quot;  /  &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="34703-184">Uses &quot;Different&quot; / &quot;Same&quot; / &quot;Different&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34703-185">Date</span><span class="sxs-lookup"><span data-stu-id="34703-185">Date</span></span></td>
<td><span data-ttu-id="34703-186">Valeur par défaut si <typeInfo type=&quot;DateTime&quot;> .</span><span class="sxs-lookup"><span data-stu-id="34703-186">Default if <typeInfo type=&quot;DateTime&quot;>.</span></span> <span data-ttu-id="34703-187">Utilise le même plus &quot; &quot;  /  &quot; &quot;  /  &quot; tard &quot; , ou utilise une version plus &quot; &quot;  /  &quot; &quot;  /  &quot; récente &quot; , &quot; ou &quot;  /  &quot; &quot;  /  &quot; &quot; utilise la même version plus tôt.</span><span class="sxs-lookup"><span data-stu-id="34703-187">Uses &quot;Earlier&quot; / &quot;Same&quot; / &quot;Later&quot;, or uses &quot;Older&quot; / &quot;Same&quot; / &quot;Newer&quot;, or uses &quot;Sooner&quot; / &quot;Same&quot; / &quot;Later&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34703-188">Taille</span><span class="sxs-lookup"><span data-stu-id="34703-188">Size</span></span></td>
<td><span data-ttu-id="34703-189">Utilise &quot; le &quot;  /  &quot; même &quot;  /  &quot; plus petit&quot;</span><span class="sxs-lookup"><span data-stu-id="34703-189">Uses &quot;Smaller&quot; / &quot;Same&quot; / &quot;Larger&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34703-190">Count</span><span class="sxs-lookup"><span data-stu-id="34703-190">Count</span></span></td>
<td><span data-ttu-id="34703-191">Utilise &quot; le &quot;  /  &quot; même &quot;  /  &quot; plus petit&quot;</span><span class="sxs-lookup"><span data-stu-id="34703-191">Uses &quot;Smaller&quot; / &quot;Same&quot; / &quot;Larger&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34703-192">Révision</span><span class="sxs-lookup"><span data-stu-id="34703-192">Revision</span></span></td>
<td><span data-ttu-id="34703-193">Utilise &quot; le &quot;  /  &quot; même plus &quot;  /  &quot; tard&quot;</span><span class="sxs-lookup"><span data-stu-id="34703-193">Uses &quot;Earlier&quot; / &quot;Same&quot; / &quot;Later&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34703-194">Longueur</span><span class="sxs-lookup"><span data-stu-id="34703-194">Length</span></span></td>
<td><span data-ttu-id="34703-195">Utilise une &quot; &quot;  /  &quot; &quot;  /  &quot; longueur plus faible&quot;</span><span class="sxs-lookup"><span data-stu-id="34703-195">Uses &quot;Shorter&quot; / &quot;Same&quot; / &quot;Longer&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34703-196">Duration</span><span class="sxs-lookup"><span data-stu-id="34703-196">Duration</span></span></td>
<td><span data-ttu-id="34703-197">Utilise une &quot; &quot;  /  &quot; &quot;  /  &quot; longueur plus faible&quot;</span><span class="sxs-lookup"><span data-stu-id="34703-197">Uses &quot;Shorter&quot; / &quot;Same&quot; / &quot;Longer&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34703-198">Vitesse</span><span class="sxs-lookup"><span data-stu-id="34703-198">Speed</span></span></td>
<td><span data-ttu-id="34703-199">Utilise plus &quot; lentement que &quot;  /  &quot; &quot;  /  &quot; plus rapide&quot;</span><span class="sxs-lookup"><span data-stu-id="34703-199">Uses &quot;Slower&quot; / &quot;Same&quot; / &quot;Faster&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34703-200">Tarif</span><span class="sxs-lookup"><span data-stu-id="34703-200">Rate</span></span></td>
<td><span data-ttu-id="34703-201">Utilise plus &quot; lentement que &quot;  /  &quot; &quot;  /  &quot; plus rapide&quot;</span><span class="sxs-lookup"><span data-stu-id="34703-201">Uses &quot;Slower&quot; / &quot;Same&quot; / &quot;Faster&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34703-202">Rating</span><span class="sxs-lookup"><span data-stu-id="34703-202">Rating</span></span></td>
<td><span data-ttu-id="34703-203">Utilise &quot; &quot;  /  &quot; &quot;  /  &quot; une valeur inférieure identique&quot;</span><span class="sxs-lookup"><span data-stu-id="34703-203">Uses &quot;Lower&quot; / &quot;Same&quot; / &quot;Higher&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34703-204">Priority</span><span class="sxs-lookup"><span data-stu-id="34703-204">Priority</span></span></td>
<td><span data-ttu-id="34703-205">Utilise &quot; &quot;  /  &quot; &quot;  /  &quot; une valeur inférieure identique&quot;</span><span class="sxs-lookup"><span data-stu-id="34703-205">Uses &quot;Lower&quot; / &quot;Same&quot; / &quot;Higher&quot;</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34703-206">defaultSortDirection</span><span class="sxs-lookup"><span data-stu-id="34703-206">defaultSortDirection</span></span></td>
<td><span data-ttu-id="34703-207">Spécifie le sens du tri.</span><span class="sxs-lookup"><span data-stu-id="34703-207">Specifies sort direction.</span></span> <span data-ttu-id="34703-208">La valeur par défaut est &quot; croissant &quot; .</span><span class="sxs-lookup"><span data-stu-id="34703-208">Default is &quot;Ascending&quot;.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="34703-209">Valeur</span><span class="sxs-lookup"><span data-stu-id="34703-209">Value</span></span></th>
<th><span data-ttu-id="34703-210">Signification</span><span class="sxs-lookup"><span data-stu-id="34703-210">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="34703-211">Croissant</span><span class="sxs-lookup"><span data-stu-id="34703-211">Ascending</span></span></td>
<td><span data-ttu-id="34703-212">Trie l’ordre croissant.</span><span class="sxs-lookup"><span data-stu-id="34703-212">Sorts ascending.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34703-213">Décroissant</span><span class="sxs-lookup"><span data-stu-id="34703-213">Descending</span></span></td>
<td><span data-ttu-id="34703-214">Trie dans l’ordre décroissant.</span><span class="sxs-lookup"><span data-stu-id="34703-214">Sorts descending.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
