---
description: Spécifie les informations de type d’une propriété.
ms.assetid: ae1f8835-ef6c-42bb-b44f-ad374337a012
title: typeInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa783a606066163fd8b17f53ef8a0fe2da44e539
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533819"
---
# <a name="typeinfo"></a><span data-ttu-id="41363-103">typeInfo</span><span class="sxs-lookup"><span data-stu-id="41363-103">typeInfo</span></span>

<span data-ttu-id="41363-104">Spécifie les informations de type d’une propriété.</span><span class="sxs-lookup"><span data-stu-id="41363-104">Specifies a property's type information.</span></span> <span data-ttu-id="41363-105">Il ne doit y avoir qu’un seul élément [TypeInfo]() pour chaque [PropertyDescription](./propdesc-schema-propertydescription.md).</span><span class="sxs-lookup"><span data-stu-id="41363-105">There should be only one [typeInfo]() element for each [propertyDescription](./propdesc-schema-propertydescription.md).</span></span> <span data-ttu-id="41363-106">Cet élément a été modifié pour Windows 7.</span><span class="sxs-lookup"><span data-stu-id="41363-106">This element has changed for Windows 7.</span></span>

<span data-ttu-id="41363-107">S’il y a plusieurs éléments, le dernier est utilisé.</span><span class="sxs-lookup"><span data-stu-id="41363-107">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="41363-108">Si aucun élément [TypeInfo]() n’est fourni, les paramètres d’attribut par défaut sont appliqués à la description de la propriété.</span><span class="sxs-lookup"><span data-stu-id="41363-108">If no [typeInfo]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax-for-windows-7"></a><span data-ttu-id="41363-109">Syntaxe pour Windows 7</span><span class="sxs-lookup"><span data-stu-id="41363-109">Syntax for Windows 7</span></span>


```
<!-- typeInfo for Windows 7-->
<xs:element name="typeInfo">
    <xs:complexType>
        <xs:attribute name="type" default="Any">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Any"/>
                    <xs:enumeration value="Null"/>
                    <xs:enumeration value="String"/>
                    <xs:enumeration value="Boolean"/>
                    <xs:enumeration value="Byte"/>
                    <xs:enumeration value="Buffer"/>
                    <xs:enumeration value="Int16"/>
                    <xs:enumeration value="UInt16"/>
                    <xs:enumeration value="Int32"/>
                    <xs:enumeration value="UInt32"/>
                    <xs:enumeration value="Int64"/>
                    <xs:enumeration value="UInt64"/>
                    <xs:enumeration value="Double"/>
                    <xs:enumeration value="DateTime"/>
                    <xs:enumeration value="Guid"/>
                    <xs:enumeration value="Blob"/>
                    <xs:enumeration value="Stream"/>
                    <xs:enumeration value="Clipboard"/>
                    <xs:enumeration value="Object"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="groupingRange">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Discrete"/>
                    <xs:enumeration value="Alphanumeric"/>
                    <xs:enumeration value="Size"/>
                    <xs:enumeration value="Date"/>
                    <xs:enumeration value="Dynamic"/>
                    <xs:enumeration value="Percent"/>
                    <xs:enumeration value="Enumerated"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="isInnate" type="xs:boolean" default="false"/>
        <xs:attribute name="canBePurged" type="xs:boolean"/>
        <xs:attribute name="multipleValues" type="xs:boolean" default="false"/>
        <xs:attribute name="isGroup" type="xs:boolean" default="false"/>
        <xs:attribute name="aggregationType">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Default"/>
                    <xs:enumeration value="First"/>
                    <xs:enumeration value="Sum"/>
                    <xs:enumeration value="Average"/>
                    <xs:enumeration value="DateRange"/>
                    <xs:enumeration value="Union"/>
                    <xs:enumeration value="Maximum"/>
                    <xs:enumeration value="Minimum"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="isTreeProperty" type="xs:boolean" default="false"/>
        <xs:attribute name="isViewable" type="xs:boolean" default="false"/>
        <xs:attribute name="isQueryable" type="xs:boolean" default="false"/>
        <xs:attribute name="includeInFullTextQuery" type="xs:boolean" default="false"/>
        <xs:attribute name="searchRawValue" type="xs:boolean" default="false"/>
        <xs:attribute name="conditionType">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="None"/>
                    <xs:enumeration value="String"/>
                    <xs:enumeration value="Number"/>
                    <xs:enumeration value="DateTime"/>
                    <xs:enumeration value="Boolean"/>
                    <xs:enumeration value="Size"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="defaultOperation">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Equal"/>
                    <xs:enumeration value="NotEqual"/>
                    <xs:enumeration value="LessThan"/>
                    <xs:enumeration value="GreaterThan"/>
                    <xs:enumeration value="Contains"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="41363-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="41363-110">Element Information</span></span>



| <span data-ttu-id="41363-111">Élément parent</span><span class="sxs-lookup"><span data-stu-id="41363-111">Parent Element</span></span>                                                   | <span data-ttu-id="41363-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="41363-112">Child Elements</span></span> |
|------------------------------------------------------------------|----------------|
| [<span data-ttu-id="41363-113">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="41363-113">propertyDescription</span></span>](./propdesc-schema-propertydescription.md) | <span data-ttu-id="41363-114">Aucun</span><span class="sxs-lookup"><span data-stu-id="41363-114">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="41363-115">Attributs</span><span class="sxs-lookup"><span data-stu-id="41363-115">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="41363-116">Attribut</span><span class="sxs-lookup"><span data-stu-id="41363-116">Attribute</span></span></th>
<th><span data-ttu-id="41363-117">Description</span><span class="sxs-lookup"><span data-stu-id="41363-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="41363-118">type</span><span class="sxs-lookup"><span data-stu-id="41363-118">type</span></span></td>
<td><span data-ttu-id="41363-119">Public.</span><span class="sxs-lookup"><span data-stu-id="41363-119">Public.</span></span> <span data-ttu-id="41363-120">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="41363-120">Optional.</span></span> <span data-ttu-id="41363-121">La valeur par défaut est &quot; Any &quot; .</span><span class="sxs-lookup"><span data-stu-id="41363-121">Default is &quot;Any&quot;.</span></span> <span data-ttu-id="41363-122">Indique le type de la propriété.</span><span class="sxs-lookup"><span data-stu-id="41363-122">Indicates the type of the property.</span></span> <span data-ttu-id="41363-123">Les types suivants sont valides et les types de variantes associés sont récupérés par <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription :: GetPropertyType</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="41363-123">The following are valid types and their associated variant types are retrieved by <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription::GetPropertyType</strong></a>.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="41363-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="41363-124">Value</span></span></th>
<th><span data-ttu-id="41363-125">Signification</span><span class="sxs-lookup"><span data-stu-id="41363-125">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="41363-126">Quelconque</span><span class="sxs-lookup"><span data-stu-id="41363-126">Any</span></span></td>
<td><span data-ttu-id="41363-127">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="41363-127">Default.</span></span> <span data-ttu-id="41363-128">Le sous-système de propriété n’applique pas ou ne force pas la valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="41363-128">The property subsystem will not enforce or coerce the property value.</span></span> <span data-ttu-id="41363-129"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription :: GetPropertyType</strong></a> retourne VT_NULL.</span><span class="sxs-lookup"><span data-stu-id="41363-129"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription::GetPropertyType</strong></a> returns VT_NULL.</span></span> <span data-ttu-id="41363-130">Les éditeurs de logiciels indépendants (ISV) sont fortement encouragés à fournir un type au lieu de revenir sur cette valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="41363-130">Independent software vendors (ISVs) are strongly encouraged to provide a type rather than fall back on this default.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41363-131">Null</span><span class="sxs-lookup"><span data-stu-id="41363-131">Null</span></span></td>
<td><span data-ttu-id="41363-132">Il n’y a aucune valeur pour cette propriété.</span><span class="sxs-lookup"><span data-stu-id="41363-132">There is no value for this property.</span></span> <span data-ttu-id="41363-133"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription :: GetPropertyType</strong></a> retourne VT_NULL.</span><span class="sxs-lookup"><span data-stu-id="41363-133"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription::GetPropertyType</strong></a> returns VT_NULL.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41363-134">String</span><span class="sxs-lookup"><span data-stu-id="41363-134">String</span></span></td>
<td><span data-ttu-id="41363-135">La valeur doit être un VT_LPWSTR, qui est une chaîne Unicode terminée par une référence null.</span><span class="sxs-lookup"><span data-stu-id="41363-135">The value must be a VT_LPWSTR, which is a Unicode string terminated by a null reference.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41363-136">Boolean</span><span class="sxs-lookup"><span data-stu-id="41363-136">Boolean</span></span></td>
<td><span data-ttu-id="41363-137">La valeur doit être un VT_BOOL, qui est une valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="41363-137">The value must be a VT_BOOL, which is a boolean.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41363-138">Byte</span><span class="sxs-lookup"><span data-stu-id="41363-138">Byte</span></span></td>
<td><span data-ttu-id="41363-139">La valeur doit être un VT_UI1, qui est un octet.</span><span class="sxs-lookup"><span data-stu-id="41363-139">The value must be a VT_UI1, which is a byte.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41363-140">Buffer</span><span class="sxs-lookup"><span data-stu-id="41363-140">Buffer</span></span></td>
<td><span data-ttu-id="41363-141">La valeur doit être un VT_UI1 | Mémoire tampon d’octets VT_VECTOR.</span><span class="sxs-lookup"><span data-stu-id="41363-141">The value must be a VT_UI1 | VT_VECTOR buffer of bytes.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41363-142">Int16</span><span class="sxs-lookup"><span data-stu-id="41363-142">Int16</span></span></td>
<td><span data-ttu-id="41363-143">La valeur doit être un VT_I2, qui est un entier de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="41363-143">The value must be a VT_I2, which is a 16-bit integer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41363-144">UInt16</span><span class="sxs-lookup"><span data-stu-id="41363-144">UInt16</span></span></td>
<td><span data-ttu-id="41363-145">La valeur doit être un VT_UI2, qui est un entier non signé 16 bits.</span><span class="sxs-lookup"><span data-stu-id="41363-145">The value must be a VT_UI2, which is a 16-bit unsigned integer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41363-146">Int32</span><span class="sxs-lookup"><span data-stu-id="41363-146">Int32</span></span></td>
<td><span data-ttu-id="41363-147">La valeur doit être un VT_I4, qui est un entier 32 bits.</span><span class="sxs-lookup"><span data-stu-id="41363-147">The value must be a VT_I4, which is a 32-bit integer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41363-148">UInt32</span><span class="sxs-lookup"><span data-stu-id="41363-148">UInt32</span></span></td>
<td><span data-ttu-id="41363-149">La valeur doit être un VT_UI4, qui est un entier non signé 32 bits.</span><span class="sxs-lookup"><span data-stu-id="41363-149">The value must be a VT_UI4, which is a 32-bit unsigned integer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41363-150">Int64</span><span class="sxs-lookup"><span data-stu-id="41363-150">Int64</span></span></td>
<td><span data-ttu-id="41363-151">La valeur doit être un VT_I8, qui est un entier 64 bits.</span><span class="sxs-lookup"><span data-stu-id="41363-151">The value must be a VT_I8, which is a 64-bit integer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41363-152">UInt64</span><span class="sxs-lookup"><span data-stu-id="41363-152">UInt64</span></span></td>
<td><span data-ttu-id="41363-153">La valeur doit être un VT_UI8, qui est un entier non signé 64 bits.</span><span class="sxs-lookup"><span data-stu-id="41363-153">The value must be a VT_UI8, which is a 64-bit unsigned integer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41363-154">Double</span><span class="sxs-lookup"><span data-stu-id="41363-154">Double</span></span></td>
<td><span data-ttu-id="41363-155">La valeur doit être un VT_R8, qui est un double.</span><span class="sxs-lookup"><span data-stu-id="41363-155">The value must be a VT_R8, which is a double.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41363-156">DateTime</span><span class="sxs-lookup"><span data-stu-id="41363-156">DateTime</span></span></td>
<td><span data-ttu-id="41363-157">La valeur doit être un VT_FILETIME, qui est un <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime"><strong>fileTime</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="41363-157">The value must be a VT_FILETIME, which is a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime"><strong>FILETIME</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41363-158">Guid</span><span class="sxs-lookup"><span data-stu-id="41363-158">Guid</span></span></td>
<td><span data-ttu-id="41363-159">La valeur doit être un VT_CLSID, qui est un identificateur de classe (CLSID).</span><span class="sxs-lookup"><span data-stu-id="41363-159">The value must be a VT_CLSID, which is a class identifier (CLSID).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41363-160">Objet blob</span><span class="sxs-lookup"><span data-stu-id="41363-160">Blob</span></span></td>
<td><span data-ttu-id="41363-161">La valeur doit être un VT_BLOB, qui sont des octets à préfixe de longueur.</span><span class="sxs-lookup"><span data-stu-id="41363-161">The value must be a VT_BLOB, which are length-prefixed bytes.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41363-162">Stream</span><span class="sxs-lookup"><span data-stu-id="41363-162">Stream</span></span></td>
<td><span data-ttu-id="41363-163">La valeur doit être un VT_STREAM, qui est un objet qui implémente <a href="/windows/desktop/api/objidl/nn-objidl-istream"><strong>IStream</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="41363-163">The value must be a VT_STREAM, which is an object that implements <a href="/windows/desktop/api/objidl/nn-objidl-istream"><strong>IStream</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41363-164">Presse-papiers</span><span class="sxs-lookup"><span data-stu-id="41363-164">Clipboard</span></span></td>
<td><span data-ttu-id="41363-165">La valeur doit être un VT_CF, qui est un format de presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="41363-165">The value must be a VT_CF, which is a clipboard format.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41363-166">Object</span><span class="sxs-lookup"><span data-stu-id="41363-166">Object</span></span></td>
<td><span data-ttu-id="41363-167">La valeur doit être un VT_UNKNOWN, qui est un objet qui implémente <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="41363-167">The value must be a VT_UNKNOWN, which is an object that implements <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a>.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41363-168">groupingRange</span><span class="sxs-lookup"><span data-stu-id="41363-168">groupingRange</span></span></td>
<td><span data-ttu-id="41363-169">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="41363-169">Optional.</span></span> <span data-ttu-id="41363-170">La valeur par défaut est &quot; discrète &quot; .</span><span class="sxs-lookup"><span data-stu-id="41363-170">Default is &quot;Discrete&quot;.</span></span> <span data-ttu-id="41363-171">Spécifie le mode d’affichage de la propriété lorsqu’une vue est regroupée par cette propriété.</span><span class="sxs-lookup"><span data-stu-id="41363-171">Specifies how the property is displayed when a view is grouped by this property.</span></span> <span data-ttu-id="41363-172">Une fois définis ici, ces valeurs sont récupérées par <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getgroupingrange"><strong>IPropertyDescription :: GetGroupingRange</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="41363-172">Once set here, these values are retrieved by <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getgroupingrange"><strong>IPropertyDescription::GetGroupingRange</strong></a>.</span></span> <span data-ttu-id="41363-173">Les types suivants sont valides.</span><span class="sxs-lookup"><span data-stu-id="41363-173">The following are valid types.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="41363-174">Valeur</span><span class="sxs-lookup"><span data-stu-id="41363-174">Value</span></span></th>
<th><span data-ttu-id="41363-175">Signification</span><span class="sxs-lookup"><span data-stu-id="41363-175">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="41363-176">Discret</span><span class="sxs-lookup"><span data-stu-id="41363-176">Discrete</span></span></td>
<td><span data-ttu-id="41363-177">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="41363-177">Default.</span></span> <span data-ttu-id="41363-178">Affiche des valeurs individuelles.</span><span class="sxs-lookup"><span data-stu-id="41363-178">Displays individual values.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41363-179">Alphanumérique</span><span class="sxs-lookup"><span data-stu-id="41363-179">Alphanumeric</span></span></td>
<td><span data-ttu-id="41363-180">Affiche des plages alphanumériques statiques pour les valeurs.</span><span class="sxs-lookup"><span data-stu-id="41363-180">Displays static alphanumeric ranges for values.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41363-181">Taille</span><span class="sxs-lookup"><span data-stu-id="41363-181">Size</span></span></td>
<td><span data-ttu-id="41363-182">Affiche des plages de tailles statiques pour les valeurs.</span><span class="sxs-lookup"><span data-stu-id="41363-182">Displays static size ranges for values.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41363-183">Date</span><span class="sxs-lookup"><span data-stu-id="41363-183">Date</span></span></td>
<td><span data-ttu-id="41363-184">Affiche les groupes de mois/années.</span><span class="sxs-lookup"><span data-stu-id="41363-184">Displays month/year groups.</span></span> <span data-ttu-id="41363-185">Valeur par défaut pour les propriétés de type = &quot; DateTime &quot; .</span><span class="sxs-lookup"><span data-stu-id="41363-185">Default for properties of type=&quot;DateTime&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41363-186">TimeRelative</span><span class="sxs-lookup"><span data-stu-id="41363-186">TimeRelative</span></span></td>
<td><span data-ttu-id="41363-187">Affiche dans des groupes relatifs à l’heure.</span><span class="sxs-lookup"><span data-stu-id="41363-187">Displays in time-relative groups.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41363-188">Dynamique</span><span class="sxs-lookup"><span data-stu-id="41363-188">Dynamic</span></span></td>
<td><span data-ttu-id="41363-189">Affiche les plages créées dynamiquement pour les valeurs.</span><span class="sxs-lookup"><span data-stu-id="41363-189">Displays dynamically created ranges for the values.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41363-190">Pourcentage</span><span class="sxs-lookup"><span data-stu-id="41363-190">Percent</span></span></td>
<td><span data-ttu-id="41363-191">Affiche le pourcentage de compartiments.</span><span class="sxs-lookup"><span data-stu-id="41363-191">Displays percent buckets.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41363-192">isInnate</span><span class="sxs-lookup"><span data-stu-id="41363-192">isInnate</span></span></td>
<td><span data-ttu-id="41363-193">Public.</span><span class="sxs-lookup"><span data-stu-id="41363-193">Public.</span></span> <span data-ttu-id="41363-194">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="41363-194">Optional.</span></span> <span data-ttu-id="41363-195">La valeur par défaut est &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="41363-195">Default is &quot;false&quot;.</span></span> <span data-ttu-id="41363-196">Spécifie si la propriété est considérée comme innée.</span><span class="sxs-lookup"><span data-stu-id="41363-196">Specifies whether the property is considered innate.</span></span> <span data-ttu-id="41363-197">Une propriété innée est une propriété qui est soit calculée à partir du contenu d’un fichier, soit à partir d’autres ressources ou systèmes.</span><span class="sxs-lookup"><span data-stu-id="41363-197">An innate property is one which is either calculated from the content of a file, or from other resources or systems.</span></span> <span data-ttu-id="41363-198">Par exemple, System. Size est une propriété innée fournie par le système de fichiers. la modification de la valeur de la propriété dans et de elle-même ne fait rien.</span><span class="sxs-lookup"><span data-stu-id="41363-198">For example, System.Size is an innate property provided by the file system; changing the value of the property in and of itself does nothing.</span></span> <span data-ttu-id="41363-199">Les autres exemples sont System. image. dimensions et System.Document. PageCount, qui sont calculées par des programmes basés sur le contenu du fichier, et non sur la base d’un paramètre modifiable par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="41363-199">Other examples are System.Image.Dimensions and System.Document.PageCount, which are calculated by programs based upon the content of the file, not based upon a user-changeable setting.</span></span> <span data-ttu-id="41363-200">La définition de isInnate = &quot; true &quot; signifie que l’utilisateur ne peut pas modifier cette propriété directement via un contrôle de propriété.</span><span class="sxs-lookup"><span data-stu-id="41363-200">Setting isInnate=&quot;true&quot; means the user cannot edit this property directly via a property control.</span></span> <span data-ttu-id="41363-201">Cette valeur correspond à l’indicateur de PDTF_ISINNATE défini dans <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> et utilisé dans <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription :: GetTypeFlags</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="41363-201">This value maps to the PDTF_ISINNATE flag defined in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> and used in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription::GetTypeFlags</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41363-202">canBePurged</span><span class="sxs-lookup"><span data-stu-id="41363-202">canBePurged</span></span></td>
<td><span data-ttu-id="41363-203"><strong>Windows Vista avec Service Pack 1 (SP1) et versions ultérieures uniquement</strong>.</span><span class="sxs-lookup"><span data-stu-id="41363-203"><strong>Windows Vista with Service Pack 1 (SP1) and later only</strong>.</span></span> <span data-ttu-id="41363-204">Public.</span><span class="sxs-lookup"><span data-stu-id="41363-204">Public.</span></span> <span data-ttu-id="41363-205">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="41363-205">Optional.</span></span> <span data-ttu-id="41363-206">Quand la valeur &quot; &quot; est true, permet de supprimer une propriété innée.</span><span class="sxs-lookup"><span data-stu-id="41363-206">When set to &quot;true&quot;, allows an innate property to be deleted.</span></span> <span data-ttu-id="41363-207">Les propriétés innées, calculées à partir d’autres propriétés, sont en lecture seule par définition.</span><span class="sxs-lookup"><span data-stu-id="41363-207">Innate properties, which are calculated from other properties, are read-only by definition.</span></span> <span data-ttu-id="41363-208">La valeur par défaut de cet attribut dépend de la valeur <em>isInnate</em> .</span><span class="sxs-lookup"><span data-stu-id="41363-208">The default value for this attribute depends on the <em>isInnate</em> value.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="41363-209">isInnate</span><span class="sxs-lookup"><span data-stu-id="41363-209">isInnate</span></span></th>
<th><span data-ttu-id="41363-210">Valeur par défaut de canBePurged</span><span class="sxs-lookup"><span data-stu-id="41363-210">canBePurged Default Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="41363-211">true</span><span class="sxs-lookup"><span data-stu-id="41363-211">true</span></span></td>
<td><span data-ttu-id="41363-212">false</span><span class="sxs-lookup"><span data-stu-id="41363-212">false</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41363-213">false</span><span class="sxs-lookup"><span data-stu-id="41363-213">false</span></span></td>
<td><span data-ttu-id="41363-214">true</span><span class="sxs-lookup"><span data-stu-id="41363-214">true</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="41363-215">Une propriété dont la valeur <em>isInnate</em> est &quot; false &quot; (ce qui signifie que la propriété est en lecture/écriture) ne peut pas également définir la valeur <em>canBePurged</em> sur &quot; false &quot; .</span><span class="sxs-lookup"><span data-stu-id="41363-215">A property whose <em>isInnate</em> value is &quot;false&quot; (meaning that the property is read/write) cannot also set the <em>canBePurged</em> value to &quot;false&quot;.</span></span> <span data-ttu-id="41363-216">Cette restriction est appliquée par le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="41363-216">This restriction is enforced by the operating system.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="41363-217">Bien que cet attribut ait été introduit dans Windows Vista avec Service Pack 1 (SP1), un fichier. propDesc qui comprend cet attribut est compatible avec Windows Vista avant Windows Vista avec SP1.</span><span class="sxs-lookup"><span data-stu-id="41363-217">Although this attribute was introduced in Windows Vista with Service Pack 1 (SP1), a .propdesc file that includes this attribute is compatible with Windows Vista prior to Windows Vista with SP1.</span></span> <span data-ttu-id="41363-218">L’attribut <em>canBePurged</em> est simplement ignoré dans cette situation.</span><span class="sxs-lookup"><span data-stu-id="41363-218">The <em>canBePurged</em> attribute is simply ignored in that situation.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41363-219">multipleValues</span><span class="sxs-lookup"><span data-stu-id="41363-219">multipleValues</span></span></td>
<td><span data-ttu-id="41363-220">Public.</span><span class="sxs-lookup"><span data-stu-id="41363-220">Public.</span></span> <span data-ttu-id="41363-221">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="41363-221">Optional.</span></span> <span data-ttu-id="41363-222">La valeur par défaut est &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="41363-222">Default is &quot;false&quot;.</span></span> <span data-ttu-id="41363-223">Spécifie si cette propriété peut avoir plusieurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="41363-223">Specifies whether this property can have multiple values.</span></span> <span data-ttu-id="41363-224">Cette valeur correspond à l’indicateur de PDTF_MULTIPLEVALUES défini dans <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> et utilisé dans <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription :: GetTypeFlags</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="41363-224">This value maps to the PDTF_MULTIPLEVALUES flag defined in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> and used in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription::GetTypeFlags</strong></a>.</span></span> <span data-ttu-id="41363-225">Cela détermine également si VT_VECTOR est ou non le VARTYPE de la valeur de propriété.</span><span class="sxs-lookup"><span data-stu-id="41363-225">This also influences whether VT_VECTOR is OR'd to the VARTYPE of the property value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41363-226">isGroup</span><span class="sxs-lookup"><span data-stu-id="41363-226">isGroup</span></span></td>
<td><span data-ttu-id="41363-227">Public.</span><span class="sxs-lookup"><span data-stu-id="41363-227">Public.</span></span> <span data-ttu-id="41363-228">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="41363-228">Optional.</span></span> <span data-ttu-id="41363-229">La valeur par défaut est &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="41363-229">Default is &quot;false&quot;.</span></span> <span data-ttu-id="41363-230">Spécifie si la propriété est un en-tête de groupe.</span><span class="sxs-lookup"><span data-stu-id="41363-230">Specifies whether the property is a group heading.</span></span> <span data-ttu-id="41363-231">Un en-tête de groupe est strictement utilisé dans les fichiers. il n’a pas de valeur, n’est jamais stocké dans un fichier et doit également avoir <typeInfo type=&quot;Null&quot;> .</span><span class="sxs-lookup"><span data-stu-id="41363-231">A group heading is strictly used in proplists, has no value, is never stored in a file, and should also have <typeInfo type=&quot;Null&quot;>.</span></span> <span data-ttu-id="41363-232">Certaines interfaces utilisateur du système utilisent des plist pour indiquer la séquence des propriétés à afficher.</span><span class="sxs-lookup"><span data-stu-id="41363-232">Some UI in the system use proplists to indicate the sequence of the properties to display.</span></span> <span data-ttu-id="41363-233">Ces exemples peuvent inclure des références à des en-têtes de groupe (par exemple, System. PropGroup. Camera), qui indiquent à l’interface utilisateur de démarrer une nouvelle section de groupe (par exemple, les paramètres de l' &quot; appareil photo &quot; ).</span><span class="sxs-lookup"><span data-stu-id="41363-233">These proplists may include references to group headings (eg, System.PropGroup.Camera), which tell the UI to start a new group section (eg, &quot;Camera Settings&quot;).</span></span> <span data-ttu-id="41363-234">Une description de propriété avec isGroup = &quot; true &quot; doit spécifier un <labelInfo label=&quot;Some localized label&quot;> , sinon il ne s’agit pas d’une propriété utile.</span><span class="sxs-lookup"><span data-stu-id="41363-234">A property description with isGroup=&quot;true&quot; should specify a <labelInfo label=&quot;Some localized label&quot;>, otherwise it isn't a useful property.</span></span> <span data-ttu-id="41363-235">Cette valeur correspond à l’indicateur de PDTF_ISGROUP défini dans <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> et utilisé dans <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription :: GetTypeFlags</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="41363-235">This value maps to the PDTF_ISGROUP flag defined in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> and used in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription::GetTypeFlags</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41363-236">aggregationType</span><span class="sxs-lookup"><span data-stu-id="41363-236">aggregationType</span></span></td>
<td><span data-ttu-id="41363-237">Public.</span><span class="sxs-lookup"><span data-stu-id="41363-237">Public.</span></span> <span data-ttu-id="41363-238">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="41363-238">Optional.</span></span> <span data-ttu-id="41363-239">La valeur par défaut est &quot; default &quot; .</span><span class="sxs-lookup"><span data-stu-id="41363-239">Default is &quot;Default&quot;.</span></span> <span data-ttu-id="41363-240">Spécifie la manière dont les propriétés d’agrégation sont affichées lorsque plusieurs éléments sont sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="41363-240">Specifies how aggregate properties are displayed when multiple items are selected.</span></span> <span data-ttu-id="41363-241">Une fois définis ici, ces valeurs sont récupérées par <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getaggregationtype"><strong>IPropertyDescription :: GetAggregationType</strong></a> en tant que <a href="/windows/win32/api/propsys/ne-propsys-propdesc_aggregation_type"><strong>PROPDESC_AGGREGATION_TYPE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="41363-241">Once set here, these values are retrieved by <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getaggregationtype"><strong>IPropertyDescription::GetAggregationType</strong></a> as an <a href="/windows/win32/api/propsys/ne-propsys-propdesc_aggregation_type"><strong>PROPDESC_AGGREGATION_TYPE</strong></a>.</span></span> <span data-ttu-id="41363-242">Les types suivants sont valides.</span><span class="sxs-lookup"><span data-stu-id="41363-242">The following are valid types.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="41363-243">Valeur</span><span class="sxs-lookup"><span data-stu-id="41363-243">Value</span></span></th>
<th><span data-ttu-id="41363-244">Signification</span><span class="sxs-lookup"><span data-stu-id="41363-244">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="41363-245">Default</span><span class="sxs-lookup"><span data-stu-id="41363-245">Default</span></span></td>
<td><span data-ttu-id="41363-246">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="41363-246">Default.</span></span> <span data-ttu-id="41363-247">Affiche un espace réservé à <strong>plusieurs valeurs</strong> dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="41363-247">Displays a <strong>Multiple Values</strong> placeholder in the UI.</span></span> <span data-ttu-id="41363-248">Il s’agit de la valeur par défaut si le <em>type</em> est incompatible avec le <em>aggregationType</em>spécifié.</span><span class="sxs-lookup"><span data-stu-id="41363-248">This is the default if the <em>type</em> is incompatible with the specified <em>aggregationType</em>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41363-249">Premier</span><span class="sxs-lookup"><span data-stu-id="41363-249">First</span></span></td>
<td><span data-ttu-id="41363-250">Affiche la valeur de la propriété du premier élément de la sélection ou de la collection.</span><span class="sxs-lookup"><span data-stu-id="41363-250">Displays the property value of the first item in the selection or collection.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41363-251">SUM</span><span class="sxs-lookup"><span data-stu-id="41363-251">Sum</span></span></td>
<td><span data-ttu-id="41363-252">Affiche la somme des valeurs numériques.</span><span class="sxs-lookup"><span data-stu-id="41363-252">Displays the sum of the numerical values.</span></span> <span data-ttu-id="41363-253">Utile pour les propriétés telles que System. Media. Duration ou System. Size.</span><span class="sxs-lookup"><span data-stu-id="41363-253">Useful for properties such as System.Media.Duration or System.Size.</span></span> <span data-ttu-id="41363-254">Cette valeur n’est pas compatible avec les types non numériques.</span><span class="sxs-lookup"><span data-stu-id="41363-254">This value is not compatible with non-numeric types.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41363-255">Moyenne</span><span class="sxs-lookup"><span data-stu-id="41363-255">Average</span></span></td>
<td><span data-ttu-id="41363-256">Affiche la moyenne des valeurs numériques.</span><span class="sxs-lookup"><span data-stu-id="41363-256">Displays the average of the numerical values.</span></span> <span data-ttu-id="41363-257">Utile pour les propriétés telles que System. Rating.</span><span class="sxs-lookup"><span data-stu-id="41363-257">Useful for properties such as System.Rating.</span></span> <span data-ttu-id="41363-258">Cette valeur n’est pas compatible avec les types non numériques.</span><span class="sxs-lookup"><span data-stu-id="41363-258">This value is not compatible with non-numeric types.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41363-259">DateRange</span><span class="sxs-lookup"><span data-stu-id="41363-259">DateRange</span></span></td>
<td><span data-ttu-id="41363-260">Affiche une plage de dates.</span><span class="sxs-lookup"><span data-stu-id="41363-260">Displays a range of dates.</span></span> <span data-ttu-id="41363-261">Utile pour les propriétés telles que System. photo. DateTaken.</span><span class="sxs-lookup"><span data-stu-id="41363-261">Useful for properties like System.Photo.DateTaken.</span></span> <span data-ttu-id="41363-262">Cette valeur n’est pas compatible avec tout sauf type = &quot; DateTime &quot; et est la valeur par défaut pour les propriétés de ce type.</span><span class="sxs-lookup"><span data-stu-id="41363-262">This value is not compatible with anything except type=&quot;DateTime&quot; and is the default for properties of that type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41363-263">Union</span><span class="sxs-lookup"><span data-stu-id="41363-263">Union</span></span></td>
<td><span data-ttu-id="41363-264">Affiche une Union de toutes les valeurs dans la sélection ou la collection.</span><span class="sxs-lookup"><span data-stu-id="41363-264">Displays a union of all the values in the selection or collection.</span></span> <span data-ttu-id="41363-265">L’ordre dans lequel les valeurs sont affichées n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="41363-265">The order in which the values are shown is undefined.</span></span> <span data-ttu-id="41363-266">Cette valeur est la valeur par défaut pour les propriétés de type = &quot; String &quot; et multipleValues = &quot; true &quot; .</span><span class="sxs-lookup"><span data-stu-id="41363-266">This value is the default for properties of type=&quot;String&quot; and multipleValues=&quot;true&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41363-267">Maximale</span><span class="sxs-lookup"><span data-stu-id="41363-267">Maximum</span></span></td>
<td><span data-ttu-id="41363-268">Affiche la valeur maximale dans la collection.</span><span class="sxs-lookup"><span data-stu-id="41363-268">Displays the maximum value in the collection.</span></span> <span data-ttu-id="41363-269">Utile pour les propriétés telles que System. DateModified.</span><span class="sxs-lookup"><span data-stu-id="41363-269">Useful for properties like System.DateModified.</span></span> <span data-ttu-id="41363-270">Non compatible avec les types non numériques ou non-date.</span><span class="sxs-lookup"><span data-stu-id="41363-270">Not compatible with non-numeric or non-date types.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41363-271">Minimum</span><span class="sxs-lookup"><span data-stu-id="41363-271">Minimum</span></span></td>
<td><span data-ttu-id="41363-272">Affiche la valeur minimale dans la collection.</span><span class="sxs-lookup"><span data-stu-id="41363-272">Displays the minimum value in the collection.</span></span> <span data-ttu-id="41363-273">Non compatible avec les types non numériques ou non-date.</span><span class="sxs-lookup"><span data-stu-id="41363-273">Not compatible with non-numeric or non-date types.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41363-274">isTreeProperty</span><span class="sxs-lookup"><span data-stu-id="41363-274">isTreeProperty</span></span></td>
<td><span data-ttu-id="41363-275">Public.</span><span class="sxs-lookup"><span data-stu-id="41363-275">Public.</span></span> <span data-ttu-id="41363-276">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="41363-276">Optional.</span></span> <span data-ttu-id="41363-277">La valeur par défaut est &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="41363-277">Default value is &quot;false&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41363-278">isViewable</span><span class="sxs-lookup"><span data-stu-id="41363-278">isViewable</span></span></td>
<td><span data-ttu-id="41363-279">Public.</span><span class="sxs-lookup"><span data-stu-id="41363-279">Public.</span></span> <span data-ttu-id="41363-280">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="41363-280">Optional.</span></span> <span data-ttu-id="41363-281">La valeur par défaut est &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="41363-281">Default value is &quot;false&quot;.</span></span> <span data-ttu-id="41363-282">Spécifie si cette propriété doit être affichée à l’intention de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="41363-282">Specifies whether this property is intended to be viewable to the user.</span></span> <span data-ttu-id="41363-283">Par exemple, l’interface utilisateur du sélecteur de colonnes affiche uniquement les propriétés qui ont isViewable = &quot; true &quot; .</span><span class="sxs-lookup"><span data-stu-id="41363-283">For example, the Column Chooser UI only shows the properties that have isViewable=&quot;true&quot;.</span></span> <span data-ttu-id="41363-284">L’interface utilisateur est une exception pilotée par un PropList, qui affiche toujours la propriété.</span><span class="sxs-lookup"><span data-stu-id="41363-284">The exception is UI that is driven by a proplist, which will always show the property.</span></span> <span data-ttu-id="41363-285">Si vous avez une propriété qui est uniquement destinée à passer des données entre deux objets et qui ne sont jamais destinées à être consultées par l’utilisateur, cet attribut doit avoir la valeur false.</span><span class="sxs-lookup"><span data-stu-id="41363-285">If you have a property that is only meant to shuttle data between two objects, and never intended to be viewed by the user, this attribute should be false.</span></span> <span data-ttu-id="41363-286">Cette valeur correspond à l’indicateur de PDTF_ISVIEWABLE défini dans <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> et utilisé dans <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription :: GetTypeFlags</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="41363-286">This value maps to the PDTF_ISVIEWABLE flag defined in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> and used in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription::GetTypeFlags</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41363-287">isQueryable</span><span class="sxs-lookup"><span data-stu-id="41363-287">isQueryable</span></span></td>
<td><span data-ttu-id="41363-288">Windows Vista uniquement.</span><span class="sxs-lookup"><span data-stu-id="41363-288">Windows Vista only.</span></span> <span data-ttu-id="41363-289">Non pris en charge dans Windows 7 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="41363-289">Not supported in Windows 7 and later.</span></span> <span data-ttu-id="41363-290">Public.</span><span class="sxs-lookup"><span data-stu-id="41363-290">Public.</span></span> <span data-ttu-id="41363-291">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="41363-291">Optional.</span></span> <span data-ttu-id="41363-292">La valeur par défaut est &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="41363-292">Default value is &quot;false&quot;.</span></span> <span data-ttu-id="41363-293">Spécifie si cette propriété doit être disponible dans l’interface utilisateur de recherche Générateur de requêtes.</span><span class="sxs-lookup"><span data-stu-id="41363-293">Specifies whether this property is intended to be available in the Search Query Builder UI.</span></span> <span data-ttu-id="41363-294">Une propriété doit avoir isViewable = &quot; true &quot; avant que isQueryable = &quot; true &quot; soit respecté.</span><span class="sxs-lookup"><span data-stu-id="41363-294">A property must have isViewable=&quot;true&quot; before isQueryable=&quot;true&quot; is respected.</span></span> <span data-ttu-id="41363-295">Cette valeur correspond à l’indicateur de PDTF_ISQUERYABLE défini dans <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> et utilisé dans <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription :: GetTypeFlags</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="41363-295">This value maps to the PDTF_ISQUERYABLE flag defined in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> and used in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription::GetTypeFlags</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41363-296">searchRawValue</span><span class="sxs-lookup"><span data-stu-id="41363-296">searchRawValue</span></span></td>
<td><span data-ttu-id="41363-297"><strong>Windows 7 et versions ultérieures.</strong></span><span class="sxs-lookup"><span data-stu-id="41363-297"><strong>Windows 7 and later.</strong></span></span> <span data-ttu-id="41363-298">Public.</span><span class="sxs-lookup"><span data-stu-id="41363-298">Public.</span></span> <span data-ttu-id="41363-299">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="41363-299">Optional.</span></span> <span data-ttu-id="41363-300">La valeur par défaut est &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="41363-300">Default value is &quot;false&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41363-301">includeInFullTextQuery</span><span class="sxs-lookup"><span data-stu-id="41363-301">includeInFullTextQuery</span></span></td>
<td><span data-ttu-id="41363-302">Windows Vista uniquement.</span><span class="sxs-lookup"><span data-stu-id="41363-302">Windows Vista only.</span></span> <span data-ttu-id="41363-303">Non pris en charge dans Windows 7 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="41363-303">Not supported in Windows 7 and later.</span></span> <span data-ttu-id="41363-304">Public.</span><span class="sxs-lookup"><span data-stu-id="41363-304">Public.</span></span> <span data-ttu-id="41363-305">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="41363-305">Optional.</span></span> <span data-ttu-id="41363-306">La valeur par défaut est &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="41363-306">Default value is &quot;false&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41363-307">conditionType</span><span class="sxs-lookup"><span data-stu-id="41363-307">conditionType</span></span></td>
<td><span data-ttu-id="41363-308">Public.</span><span class="sxs-lookup"><span data-stu-id="41363-308">Public.</span></span> <span data-ttu-id="41363-309">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="41363-309">Optional.</span></span> <span data-ttu-id="41363-310">La valeur par défaut est &quot; String &quot; .</span><span class="sxs-lookup"><span data-stu-id="41363-310">Default is &quot;String&quot;.</span></span> <span data-ttu-id="41363-311">Spécifie un indicateur pour la recherche Générateur de requêtes l’interface utilisateur afin qu’elle puisse déterminer la liste des opérateurs de condition possibles à l’intérieur d’un prédicat.</span><span class="sxs-lookup"><span data-stu-id="41363-311">Specifies a hint to the Search Query Builder UI so that it can determine the list of possible condition operators inside a predicate.</span></span> <span data-ttu-id="41363-312">Les valeurs reconnues sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="41363-312">The following are recognized values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="41363-313">Valeur</span><span class="sxs-lookup"><span data-stu-id="41363-313">Value</span></span></th>
<th><span data-ttu-id="41363-314">Signification</span><span class="sxs-lookup"><span data-stu-id="41363-314">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="41363-315">String</span><span class="sxs-lookup"><span data-stu-id="41363-315">String</span></span></td>
<td><span data-ttu-id="41363-316">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="41363-316">Default.</span></span> <span data-ttu-id="41363-317">Les opérateurs suivants seront utilisés : &quot; est &quot; , n' &quot; est pas &quot; , &quot; &lt; &quot; ,, &quot; &gt; &quot; &quot; <= &quot; , &quot; >= &quot; , &quot; commence par &quot; , et &quot; se termine par &quot; , &quot; contient &quot; , &quot; ne contient pas &quot; , &quot; est comme &quot; .</span><span class="sxs-lookup"><span data-stu-id="41363-317">The following operators will be used: &quot;is&quot;, &quot;is not&quot;, &quot;&lt;&quot;, &quot;&gt;&quot;, &quot;<=&quot;, &quot;>=&quot;, &quot;starts with&quot;, &quot;ends with&quot;, &quot;contains&quot;, &quot;doesn't contain&quot;, &quot;is like&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41363-318">Number</span><span class="sxs-lookup"><span data-stu-id="41363-318">Number</span></span></td>
<td><span data-ttu-id="41363-319">Valeur par défaut pour les propriétés numériques.</span><span class="sxs-lookup"><span data-stu-id="41363-319">Default for numeric properties.</span></span> <span data-ttu-id="41363-320">Les opérateurs suivants seront utilisés : égal à, n' &quot; &quot; est pas égal à, est inférieur à &quot; &quot; &quot; &quot; , &quot; est supérieur à &quot; , &quot; est inférieur ou égal à &quot; , &quot; est supérieur ou égal à &quot; .</span><span class="sxs-lookup"><span data-stu-id="41363-320">The following operators will be used: &quot;equals&quot;, &quot;doesn't equal&quot;, &quot;is less than&quot;, &quot;is greater than&quot;, &quot;is less than or equal to&quot;, &quot;is greater than or equal to&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41363-321">DateTime</span><span class="sxs-lookup"><span data-stu-id="41363-321">DateTime</span></span></td>
<td><span data-ttu-id="41363-322">Valeur par défaut pour les propriétés de type = &quot; DateTime &quot; .</span><span class="sxs-lookup"><span data-stu-id="41363-322">Default for properties of type=&quot;DateTime&quot;.</span></span> <span data-ttu-id="41363-323">Les opérateurs suivants seront utilisés : &quot; est, n’est &quot; &quot; pas &quot; , est &quot; avant &quot; , est &quot; après &quot; , &quot; est avant, mais comprend &quot; , &quot; est après, mais contient &quot; .</span><span class="sxs-lookup"><span data-stu-id="41363-323">The following operators will be used: &quot;is&quot;, &quot;is not&quot;, &quot;is before&quot;, &quot;is after&quot;, &quot;is before but includes&quot;, &quot;is after but includes&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41363-324">Boolean</span><span class="sxs-lookup"><span data-stu-id="41363-324">Boolean</span></span></td>
<td><span data-ttu-id="41363-325">Valeur par défaut pour les propriétés de type = &quot; Boolean &quot; .</span><span class="sxs-lookup"><span data-stu-id="41363-325">Default for properties of type=&quot;Boolean&quot;.</span></span> <span data-ttu-id="41363-326">Identique au nombre.</span><span class="sxs-lookup"><span data-stu-id="41363-326">Same as Number.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41363-327">Taille</span><span class="sxs-lookup"><span data-stu-id="41363-327">Size</span></span></td>
<td><span data-ttu-id="41363-328">Identique au nombre.</span><span class="sxs-lookup"><span data-stu-id="41363-328">Same as Number.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41363-329">defaultOperation</span><span class="sxs-lookup"><span data-stu-id="41363-329">defaultOperation</span></span></td>
<td><span data-ttu-id="41363-330">Public.</span><span class="sxs-lookup"><span data-stu-id="41363-330">Public.</span></span> <span data-ttu-id="41363-331">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="41363-331">Optional.</span></span> <span data-ttu-id="41363-332">La valeur par défaut est &quot; égale à &quot; .</span><span class="sxs-lookup"><span data-stu-id="41363-332">Default is &quot;Equal&quot;.</span></span> <span data-ttu-id="41363-333">Spécifie un indicateur pour l’outil de Générateur de requêtes de recherche afin qu’il puisse déterminer l’opérateur par défaut.</span><span class="sxs-lookup"><span data-stu-id="41363-333">Specifies a hint to the Search Query Builder tool so that it can determine the default operator.</span></span> <span data-ttu-id="41363-334">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="41363-334">The possible values are as follows:</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="41363-335">Valeur</span><span class="sxs-lookup"><span data-stu-id="41363-335">Value</span></span></th>
<th><span data-ttu-id="41363-336">Signification</span><span class="sxs-lookup"><span data-stu-id="41363-336">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="41363-337">Égal à</span><span class="sxs-lookup"><span data-stu-id="41363-337">Equal</span></span></td>
<td><span data-ttu-id="41363-338">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="41363-338">Default.</span></span> <span data-ttu-id="41363-339">Indique un équivalent.</span><span class="sxs-lookup"><span data-stu-id="41363-339">Indicates equivalent.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41363-340">NotEqual</span><span class="sxs-lookup"><span data-stu-id="41363-340">NotEqual</span></span></td>
<td><span data-ttu-id="41363-341">N’indique pas l’équivalent.</span><span class="sxs-lookup"><span data-stu-id="41363-341">Indicates not equivalent.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41363-342">LessThan</span><span class="sxs-lookup"><span data-stu-id="41363-342">LessThan</span></span></td>
<td><span data-ttu-id="41363-343">Indique inférieur à.</span><span class="sxs-lookup"><span data-stu-id="41363-343">Indicates less than.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41363-344">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="41363-344">GreaterThan</span></span></td>
<td><span data-ttu-id="41363-345">Valeur par défaut pour les propriétés de conditionType = &quot; size &quot; .</span><span class="sxs-lookup"><span data-stu-id="41363-345">Default for properties of conditionType=&quot;Size&quot;.</span></span> <span data-ttu-id="41363-346">Indique supérieur à.</span><span class="sxs-lookup"><span data-stu-id="41363-346">Indicates greater than.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41363-347">Contient</span><span class="sxs-lookup"><span data-stu-id="41363-347">Contains</span></span></td>
<td><span data-ttu-id="41363-348">Valeur par défaut pour les propriétés de conditionType = &quot; String &quot; .</span><span class="sxs-lookup"><span data-stu-id="41363-348">Default for properties of conditionType=&quot;String&quot;.</span></span> <span data-ttu-id="41363-349">Indique l’inclusion.</span><span class="sxs-lookup"><span data-stu-id="41363-349">Indicates inclusion.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
