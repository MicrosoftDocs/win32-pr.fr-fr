---
description: 'Spécifie comment IPropertyDescription :: FormatForDisplay doit mettre en forme la valeur de la propriété en tant que chaîne. Cela s’applique uniquement si <displayInfo displayType=&\#0034;String&\#0034;> .'
ms.assetid: 7c38bc15-be86-4260-b2e4-13afc90de6d7
title: stringFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec05a6eedf1734c1d62c0503027810ad05916160
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519828"
---
# <a name="stringformat"></a><span data-ttu-id="3c75a-104">stringFormat</span><span class="sxs-lookup"><span data-stu-id="3c75a-104">stringFormat</span></span>

<span data-ttu-id="3c75a-105">Spécifie comment [**IPropertyDescription :: FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) doit mettre en forme la valeur de la propriété en tant que chaîne.</span><span class="sxs-lookup"><span data-stu-id="3c75a-105">Specifies how [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) should format the property's value as a string.</span></span> <span data-ttu-id="3c75a-106">Cela s’applique uniquement si <displayInfo displayType="String"> .</span><span class="sxs-lookup"><span data-stu-id="3c75a-106">This is applicable only if <displayInfo displayType="String">.</span></span> <span data-ttu-id="3c75a-107">Il ne doit y avoir qu’un seul élément [stringFormat]() pour chaque élément [displayInfo](./propdesc-schema-displayinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="3c75a-107">There should be only one [stringFormat]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="3c75a-108">S’il y a plusieurs éléments, le dernier est utilisé.</span><span class="sxs-lookup"><span data-stu-id="3c75a-108">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="3c75a-109">Si aucun élément [stringFormat]() n’est fourni, les paramètres d’attribut par défaut sont appliqués à la description de la propriété.</span><span class="sxs-lookup"><span data-stu-id="3c75a-109">If no [stringFormat]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c75a-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3c75a-110">Syntax</span></span>


```
<!-- stringFormat -->
<xs:element name="stringFormat"  minOccurs="0" maxOccurs="1">
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
```



## <a name="element-information"></a><span data-ttu-id="3c75a-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="3c75a-111">Element Information</span></span>



| <span data-ttu-id="3c75a-112">Élément parent</span><span class="sxs-lookup"><span data-stu-id="3c75a-112">Parent Element</span></span>                                   | <span data-ttu-id="3c75a-113">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="3c75a-113">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="3c75a-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="3c75a-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="3c75a-115">Aucun</span><span class="sxs-lookup"><span data-stu-id="3c75a-115">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="3c75a-116">Attributs</span><span class="sxs-lookup"><span data-stu-id="3c75a-116">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3c75a-117">Attribut</span><span class="sxs-lookup"><span data-stu-id="3c75a-117">Attribute</span></span></th>
<th><span data-ttu-id="3c75a-118">Description</span><span class="sxs-lookup"><span data-stu-id="3c75a-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3c75a-119">formatas</span><span class="sxs-lookup"><span data-stu-id="3c75a-119">formatAs</span></span></td>
<td><span data-ttu-id="3c75a-120">Public.</span><span class="sxs-lookup"><span data-stu-id="3c75a-120">Public.</span></span> <span data-ttu-id="3c75a-121">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="3c75a-121">Optional.</span></span> <span data-ttu-id="3c75a-122">La valeur par défaut est &quot; général &quot; .</span><span class="sxs-lookup"><span data-stu-id="3c75a-122">Default is &quot;General&quot;.</span></span> <span data-ttu-id="3c75a-123">Les valeurs valides sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="3c75a-123">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="3c75a-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="3c75a-124">Value</span></span></th>
<th><span data-ttu-id="3c75a-125">Signification</span><span class="sxs-lookup"><span data-stu-id="3c75a-125">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3c75a-126">Général</span><span class="sxs-lookup"><span data-stu-id="3c75a-126">General</span></span></td>
<td><span data-ttu-id="3c75a-127">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="3c75a-127">Default.</span></span> <span data-ttu-id="3c75a-128">Retourne la valeur sous forme de chaîne non mise en forme.</span><span class="sxs-lookup"><span data-stu-id="3c75a-128">Returns the value as an unformatted string.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3c75a-129">FileName</span><span class="sxs-lookup"><span data-stu-id="3c75a-129">FileName</span></span></td>
<td><span data-ttu-id="3c75a-130">Met en forme la valeur en tant que nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="3c75a-130">Formats the value as a file name.</span></span> <span data-ttu-id="3c75a-131">Masque l’extension en fonction des paramètres utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3c75a-131">Hides the extension according to user settings.</span></span> <span data-ttu-id="3c75a-132">Requiert que le type de propriété soit une chaîne.</span><span class="sxs-lookup"><span data-stu-id="3c75a-132">Requires the property type to be String.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3c75a-133">FilePath</span><span class="sxs-lookup"><span data-stu-id="3c75a-133">FilePath</span></span></td>
<td><span data-ttu-id="3c75a-134">Met en forme la valeur sous la forme d’un chemin d’accès de fichier.</span><span class="sxs-lookup"><span data-stu-id="3c75a-134">Formats the value as a file path.</span></span> <span data-ttu-id="3c75a-135">Masque l’extension en fonction des paramètres utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3c75a-135">Hides the extension according to user settings.</span></span> <span data-ttu-id="3c75a-136">Requiert que le type de propriété soit une chaîne.</span><span class="sxs-lookup"><span data-stu-id="3c75a-136">Requires the property type to be String.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3c75a-137">Hyperlink</span><span class="sxs-lookup"><span data-stu-id="3c75a-137">Hyperlink</span></span></td>
<td><span data-ttu-id="3c75a-138">Met en forme la valeur en tant que lien hypertexte.</span><span class="sxs-lookup"><span data-stu-id="3c75a-138">Formats the value as a hyperlink.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
