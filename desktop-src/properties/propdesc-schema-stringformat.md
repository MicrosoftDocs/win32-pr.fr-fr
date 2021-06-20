---
description: 'Spécifie comment IPropertyDescription :: FormatForDisplay doit mettre en forme la valeur de la propriété stringFormat sous forme de chaîne.'
ms.assetid: 7c38bc15-be86-4260-b2e4-13afc90de6d7
title: stringFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 730355507b78d99eba02e82666427dd29425c942
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408352"
---
# <a name="stringformat"></a><span data-ttu-id="55666-103">stringFormat</span><span class="sxs-lookup"><span data-stu-id="55666-103">stringFormat</span></span>

<span data-ttu-id="55666-104">Spécifie comment [**IPropertyDescription :: FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) doit mettre en forme la valeur de la propriété en tant que chaîne.</span><span class="sxs-lookup"><span data-stu-id="55666-104">Specifies how [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) should format the property's value as a string.</span></span> <span data-ttu-id="55666-105">Cela s’applique uniquement si <displayInfo displayType="String"> .</span><span class="sxs-lookup"><span data-stu-id="55666-105">This is applicable only if <displayInfo displayType="String">.</span></span> <span data-ttu-id="55666-106">Il ne doit y avoir qu’un seul élément [stringFormat]() pour chaque élément [displayInfo](./propdesc-schema-displayinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="55666-106">There should be only one [stringFormat]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="55666-107">S’il y a plusieurs éléments, le dernier est utilisé.</span><span class="sxs-lookup"><span data-stu-id="55666-107">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="55666-108">Si aucun élément [stringFormat]() n’est fourni, les paramètres d’attribut par défaut sont appliqués à la description de la propriété.</span><span class="sxs-lookup"><span data-stu-id="55666-108">If no [stringFormat]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="55666-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="55666-109">Syntax</span></span>


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



## <a name="element-information"></a><span data-ttu-id="55666-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="55666-110">Element Information</span></span>



| <span data-ttu-id="55666-111">Élément parent</span><span class="sxs-lookup"><span data-stu-id="55666-111">Parent Element</span></span>                                   | <span data-ttu-id="55666-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="55666-112">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="55666-113">displayInfo</span><span class="sxs-lookup"><span data-stu-id="55666-113">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="55666-114">Aucun</span><span class="sxs-lookup"><span data-stu-id="55666-114">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="55666-115">Attributs</span><span class="sxs-lookup"><span data-stu-id="55666-115">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="55666-116">Attribut</span><span class="sxs-lookup"><span data-stu-id="55666-116">Attribute</span></span></th>
<th><span data-ttu-id="55666-117">Description</span><span class="sxs-lookup"><span data-stu-id="55666-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="55666-118">formatas</span><span class="sxs-lookup"><span data-stu-id="55666-118">formatAs</span></span></td>
<td><span data-ttu-id="55666-119">Public.</span><span class="sxs-lookup"><span data-stu-id="55666-119">Public.</span></span> <span data-ttu-id="55666-120">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="55666-120">Optional.</span></span> <span data-ttu-id="55666-121">La valeur par défaut est &quot; général &quot; .</span><span class="sxs-lookup"><span data-stu-id="55666-121">Default is &quot;General&quot;.</span></span> <span data-ttu-id="55666-122">Les valeurs valides sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="55666-122">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="55666-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="55666-123">Value</span></span></th>
<th><span data-ttu-id="55666-124">Signification</span><span class="sxs-lookup"><span data-stu-id="55666-124">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="55666-125">Généralités</span><span class="sxs-lookup"><span data-stu-id="55666-125">General</span></span></td>
<td><span data-ttu-id="55666-126">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="55666-126">Default.</span></span> <span data-ttu-id="55666-127">Retourne la valeur sous forme de chaîne non mise en forme.</span><span class="sxs-lookup"><span data-stu-id="55666-127">Returns the value as an unformatted string.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="55666-128">FileName</span><span class="sxs-lookup"><span data-stu-id="55666-128">FileName</span></span></td>
<td><span data-ttu-id="55666-129">Met en forme la valeur en tant que nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="55666-129">Formats the value as a file name.</span></span> <span data-ttu-id="55666-130">Masque l’extension en fonction des paramètres utilisateur.</span><span class="sxs-lookup"><span data-stu-id="55666-130">Hides the extension according to user settings.</span></span> <span data-ttu-id="55666-131">Requiert que le type de propriété soit une chaîne.</span><span class="sxs-lookup"><span data-stu-id="55666-131">Requires the property type to be String.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="55666-132">FilePath</span><span class="sxs-lookup"><span data-stu-id="55666-132">FilePath</span></span></td>
<td><span data-ttu-id="55666-133">Met en forme la valeur sous la forme d’un chemin d’accès de fichier.</span><span class="sxs-lookup"><span data-stu-id="55666-133">Formats the value as a file path.</span></span> <span data-ttu-id="55666-134">Masque l’extension en fonction des paramètres utilisateur.</span><span class="sxs-lookup"><span data-stu-id="55666-134">Hides the extension according to user settings.</span></span> <span data-ttu-id="55666-135">Requiert que le type de propriété soit une chaîne.</span><span class="sxs-lookup"><span data-stu-id="55666-135">Requires the property type to be String.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="55666-136">Hyperlink</span><span class="sxs-lookup"><span data-stu-id="55666-136">Hyperlink</span></span></td>
<td><span data-ttu-id="55666-137">Met en forme la valeur en tant que lien hypertexte.</span><span class="sxs-lookup"><span data-stu-id="55666-137">Formats the value as a hyperlink.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
