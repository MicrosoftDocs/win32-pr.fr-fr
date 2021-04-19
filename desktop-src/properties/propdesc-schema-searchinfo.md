---
description: Spécifie comment configurer le moteur de recherche Windows par rapport à une définition de propriété donnée.
ms.assetid: 1cb0b630-323c-41cf-8aaf-db3028b2e369
title: searchInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eee94585aaa66a761e527ac6ada1c33b0d23966d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517774"
---
# <a name="searchinfo"></a><span data-ttu-id="1a2b2-103">searchInfo</span><span class="sxs-lookup"><span data-stu-id="1a2b2-103">searchInfo</span></span>

<span data-ttu-id="1a2b2-104">Spécifie comment configurer le moteur de recherche Windows par rapport à une définition de propriété donnée.</span><span class="sxs-lookup"><span data-stu-id="1a2b2-104">Specifies how to configure the Windows search engine with respect to a given property definition.</span></span> <span data-ttu-id="1a2b2-105">Si aucun élément [searchInfo]() n’est fourni, la propriété n’est pas incluse dans le moteur de recherche Windows.</span><span class="sxs-lookup"><span data-stu-id="1a2b2-105">If no [searchInfo]() element is provided, then the property is not included in the Windows search engine.</span></span> <span data-ttu-id="1a2b2-106">Cet élément a été modifié pour Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1a2b2-106">This element has changed for Windows 7.</span></span>

## <a name="syntax-for-windows-7"></a><span data-ttu-id="1a2b2-107">Syntaxe pour Windows 7</span><span class="sxs-lookup"><span data-stu-id="1a2b2-107">Syntax for Windows 7</span></span>


```
<!-- searchInfo for Windows 7-->
<xs:element name="searchInfo">
    <xs:complexType>
        <xs:attribute name="inInvertedIndex"    type="xs:boolean" default="false"/>
        <xs:attribute name="isColumn"           type="xs:boolean" default="false"/>
        <xs:attribute name="isColumnSparse"     type="xs:boolean" default="true">
            <xs:annotation>
                <xs:documentation>
                    isColumnSparse: Default is true. If the property is multi-valued, this is always true.
                </xs:documentation>
            </xs:annotation>
        </xs:attribute>
        
        <xs:attribute name="columnIndexType" default="OnDemand">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="NotIndexed"/>
                    <xs:enumeration value="OnDisk"/>
                    <xs:enumeration value="OnDiskAll"/>
                    <xs:enumeration value="OnDiskVector"/>
                    <xs:enumeration value="OnDemand"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="maxSize" type="xs:nonNegativeInteger" default="512"/>
        <xs:attribute name="mnemonics" type="xs:string"/>                            
    </xs:complexType>
</xs:element>
```



## <a name="syntax-for-windows-vista"></a><span data-ttu-id="1a2b2-108">Syntaxe pour Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1a2b2-108">Syntax for Windows Vista</span></span>


```
<!-- searchInfo for Windows Vista-->
<xs:element name="searchInfo">
    <xs:complexType>
        <xs:attribute name="inInvertedIndex"    type="xs:boolean" default="false"/>
        <xs:attribute name="isColumn"           type="xs:boolean" default="false"/>
        <xs:attribute name="isColumnSparse"     type="xs:boolean" default="true">
            <xs:annotation>
                <xs:documentation>
                    isColumnSparse: Default is true. If the property is multi-valued, this is always true.
                </xs:documentation>
            </xs:annotation>
        </xs:attribute>
        
        <xs:attribute name="columnIndexType" default="OnDemand">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="NotIndexed"/>
                    <xs:enumeration value="OnDisk"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="maxSize" type="xs:nonNegativeInteger" default="128"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="1a2b2-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="1a2b2-109">Element Information</span></span>



| <span data-ttu-id="1a2b2-110">Élément parent</span><span class="sxs-lookup"><span data-stu-id="1a2b2-110">Parent Element</span></span>                                                   | <span data-ttu-id="1a2b2-111">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="1a2b2-111">Child Elements</span></span> |
|------------------------------------------------------------------|----------------|
| [<span data-ttu-id="1a2b2-112">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="1a2b2-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md) | <span data-ttu-id="1a2b2-113">Aucun</span><span class="sxs-lookup"><span data-stu-id="1a2b2-113">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="1a2b2-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="1a2b2-114">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1a2b2-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="1a2b2-115">Attribute</span></span></th>
<th><span data-ttu-id="1a2b2-116">Description</span><span class="sxs-lookup"><span data-stu-id="1a2b2-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1a2b2-117">inInvertedIndex</span><span class="sxs-lookup"><span data-stu-id="1a2b2-117">inInvertedIndex</span></span></td>
<td><span data-ttu-id="1a2b2-118">Public.</span><span class="sxs-lookup"><span data-stu-id="1a2b2-118">Public.</span></span> <span data-ttu-id="1a2b2-119">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="1a2b2-119">Optional.</span></span> <span data-ttu-id="1a2b2-120">Indique si la valeur de la propriété doit être stockée dans l’index inversé.</span><span class="sxs-lookup"><span data-stu-id="1a2b2-120">Indicates whether the property value should be stored in the inverted index.</span></span> <span data-ttu-id="1a2b2-121">Cela permet aux utilisateurs finaux d’effectuer des requêtes de texte intégral sur les valeurs de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="1a2b2-121">This lets end users perform full-text queries over the values of this property.</span></span> <span data-ttu-id="1a2b2-122">La valeur par défaut est &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="1a2b2-122">The default is &quot;false&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a2b2-123">isColumn</span><span class="sxs-lookup"><span data-stu-id="1a2b2-123">isColumn</span></span></td>
<td><span data-ttu-id="1a2b2-124">Public.</span><span class="sxs-lookup"><span data-stu-id="1a2b2-124">Public.</span></span> <span data-ttu-id="1a2b2-125">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="1a2b2-125">Optional.</span></span> <span data-ttu-id="1a2b2-126">Indique si la propriété doit également être stockée dans la base de données de recherche Windows en tant que colonne, de sorte que les éditeurs de logiciels indépendants puissent créer des requêtes basées sur des prédicats (par exemple, &quot; sélectionnez \* où &quot; System. title &quot; = 'qqq' &quot; ).</span><span class="sxs-lookup"><span data-stu-id="1a2b2-126">Indicates whether the property should also be stored in the Windows search database as a column, so that independent software vendors (ISVs) can create predicate-based queries (for example, &quot;Select \* Where &quot;System.Title&quot;='qqq'&quot;).</span></span> <span data-ttu-id="1a2b2-127">Si le créateur du schéma souhaite permettre aux utilisateurs finaux (ou aux développeurs) de créer des requêtes basées sur des prédicats sur les propriétés, cette valeur doit être définie sur &quot; true &quot; .</span><span class="sxs-lookup"><span data-stu-id="1a2b2-127">If the schema creator wants to enable end users (or developers) to create predicate based queries on the properties, then this needs to be set to &quot;true&quot;.</span></span> <span data-ttu-id="1a2b2-128">La valeur par défaut est &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="1a2b2-128">The default is &quot;false&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1a2b2-129">isColumnSparse</span><span class="sxs-lookup"><span data-stu-id="1a2b2-129">isColumnSparse</span></span></td>
<td><span data-ttu-id="1a2b2-130">Public.</span><span class="sxs-lookup"><span data-stu-id="1a2b2-130">Public.</span></span> <span data-ttu-id="1a2b2-131">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="1a2b2-131">Optional.</span></span> <span data-ttu-id="1a2b2-132">La valeur par défaut est &quot;true&quot;.</span><span class="sxs-lookup"><span data-stu-id="1a2b2-132">The default is &quot;true&quot;.</span></span> <span data-ttu-id="1a2b2-133">Si la propriété est à valeurs multiples, cet attribut a toujours la &quot; valeur true &quot; .</span><span class="sxs-lookup"><span data-stu-id="1a2b2-133">If the property is multi-valued, this attribute is always &quot;true&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a2b2-134">columnIndexType</span><span class="sxs-lookup"><span data-stu-id="1a2b2-134">columnIndexType</span></span></td>
<td><span data-ttu-id="1a2b2-135">Public.</span><span class="sxs-lookup"><span data-stu-id="1a2b2-135">Public.</span></span> <span data-ttu-id="1a2b2-136">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="1a2b2-136">Optional.</span></span> <span data-ttu-id="1a2b2-137">Pour optimiser le tri et le regroupement, le moteur de recherche Windows peut créer des index secondaires pour les propriétés qui ont isColumn = &quot; true &quot; .</span><span class="sxs-lookup"><span data-stu-id="1a2b2-137">To optimize sorting and grouping, the Windows search engine can create secondary indexes for properties that have isColumn=&quot;true&quot;.</span></span> <span data-ttu-id="1a2b2-138">Cet attribut est utile uniquement lorsque inInvertedIndex a la &quot; valeur true &quot; dans Windows Vista ou lorsque isColumn a la &quot; valeur true &quot; dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1a2b2-138">This attribute is only useful when inInvertedIndex is &quot;true&quot; in Windows Vista or when isColumn is &quot;true&quot; in Windows 7.</span></span> <span data-ttu-id="1a2b2-139">Si la propriété a tendance à être triée fréquemment par les utilisateurs, cet attribut doit être spécifié.</span><span class="sxs-lookup"><span data-stu-id="1a2b2-139">If the property tends to be sorted frequently by users, this attribute should be specified.</span></span> <span data-ttu-id="1a2b2-140">La valeur par défaut dans Windows Vista est &quot; NotIndexed &quot; .</span><span class="sxs-lookup"><span data-stu-id="1a2b2-140">The default value in Windows Vista is &quot;NotIndexed&quot;.</span></span> <span data-ttu-id="1a2b2-141">La valeur par défaut dans Windows 7 est &quot; OnDemand &quot; .</span><span class="sxs-lookup"><span data-stu-id="1a2b2-141">The default value in Windows 7 is &quot;OnDemand&quot;.</span></span> <span data-ttu-id="1a2b2-142">Les valeurs suivantes sont valides.</span><span class="sxs-lookup"><span data-stu-id="1a2b2-142">The following values are valid.</span></span>
<ul>
<li><span data-ttu-id="1a2b2-143"><strong>NotIndexed</strong>: ne jamais générer un index de valeur.</span><span class="sxs-lookup"><span data-stu-id="1a2b2-143"><strong>NotIndexed</strong>: Never build a value index.</span></span></li>
<li><span data-ttu-id="1a2b2-144"><strong>OnDisk</strong>: générer un index de valeur par défaut pour cette propriété.</span><span class="sxs-lookup"><span data-stu-id="1a2b2-144"><strong>OnDisk</strong>: Build a value index by default for this property.</span></span></li>
<li><span data-ttu-id="1a2b2-145"><strong>OnDiskAll</strong> (Windows 7 et versions ultérieures uniquement) : générez un index de valeur par défaut pour cette propriété, et s’il s’agit d’une propriété Vector, également un index de valeur pour toutes les valeurs de vecteur concaténées.</span><span class="sxs-lookup"><span data-stu-id="1a2b2-145"><strong>OnDiskAll</strong> (Windows 7 and later only): Build a value index by default for this property, and if it is a vector property, also a value index for all concatenated vector values.</span></span></li>
<li><span data-ttu-id="1a2b2-146"><strong>OnDiskVector</strong> (Windows 7 et versions ultérieures uniquement) : générez un index de valeur par défaut pour les valeurs de vecteur concaténées.</span><span class="sxs-lookup"><span data-stu-id="1a2b2-146"><strong>OnDiskVector</strong> (Windows 7 and later only): Build a value index by default for the concatenated vector values.</span></span></li>
<li><span data-ttu-id="1a2b2-147"><strong>OnDemand</strong> (Windows 7 et versions ultérieures uniquement) : générez uniquement les index de valeur par demande, autrement dit, la première fois qu’ils sont utilisés pour une requête.</span><span class="sxs-lookup"><span data-stu-id="1a2b2-147"><strong>OnDemand</strong> (Windows 7 and later only): Only build value indices by demand, that is, only first time they are used for a query.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1a2b2-148">maxSize</span><span class="sxs-lookup"><span data-stu-id="1a2b2-148">maxSize</span></span></td>
<td><span data-ttu-id="1a2b2-149">Public.</span><span class="sxs-lookup"><span data-stu-id="1a2b2-149">Public.</span></span> <span data-ttu-id="1a2b2-150">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="1a2b2-150">Optional.</span></span> <span data-ttu-id="1a2b2-151">Taille maximale, en octets, autorisée pour une certaine propriété qui est stockée dans la base de données de recherche Windows.</span><span class="sxs-lookup"><span data-stu-id="1a2b2-151">The maximum size, in bytes, allowed for a certain property that is stored in the Windows search database.</span></span> <span data-ttu-id="1a2b2-152">La valeur par défaut est :</span><span class="sxs-lookup"><span data-stu-id="1a2b2-152">The default is:</span></span>
<ul>
<li><span data-ttu-id="1a2b2-153"><strong>Windows Vista</strong>: 128 octets</span><span class="sxs-lookup"><span data-stu-id="1a2b2-153"><strong>Windows Vista</strong>: 128 bytes</span></span></li>
<li><span data-ttu-id="1a2b2-154"><strong>Windows 7 et versions ultérieures</strong>: 512 octets</span><span class="sxs-lookup"><span data-stu-id="1a2b2-154"><strong>Windows 7 and later</strong>: 512 bytes</span></span></li>
</ul>
<span data-ttu-id="1a2b2-155">Notez que cette taille maximale est mesurée en octets, et non en caractères.</span><span class="sxs-lookup"><span data-stu-id="1a2b2-155">Note that this maximum size is measured in bytes, not characters.</span></span> <span data-ttu-id="1a2b2-156">Le nombre maximal de caractères dépend de leur encodage.</span><span class="sxs-lookup"><span data-stu-id="1a2b2-156">The maximum number of characters depends on their encoding.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a2b2-157">mnémoniques</span><span class="sxs-lookup"><span data-stu-id="1a2b2-157">mnemonics</span></span></td>
<td><span data-ttu-id="1a2b2-158"><strong>Windows 7 et versions ultérieures.</strong></span><span class="sxs-lookup"><span data-stu-id="1a2b2-158"><strong>Windows 7 and later.</strong></span></span> <span data-ttu-id="1a2b2-159">Public.</span><span class="sxs-lookup"><span data-stu-id="1a2b2-159">Public.</span></span> <span data-ttu-id="1a2b2-160">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="1a2b2-160">Optional.</span></span> <span data-ttu-id="1a2b2-161">Liste de valeurs mnémoniques qui peuvent être utilisées pour faire référence à la propriété dans les requêtes de recherche.</span><span class="sxs-lookup"><span data-stu-id="1a2b2-161">A list of mnemonic values that can be used to refer to the property in search queries.</span></span> <span data-ttu-id="1a2b2-162">La liste est délimitée par le caractère « | ».</span><span class="sxs-lookup"><span data-stu-id="1a2b2-162">The list is delimited with the '|' character.</span></span></td>
</tr>
</tbody>
</table>



 

 

 
