---
description: 'Spécifie comment IPropertyDescription :: FormatForDisplay doit mettre en forme la valeur de la propriété en tant que chaîne. Cela s’applique uniquement si <displayInfo displayType=&\#0034;String&\#0034;> .'
ms.assetid: f6384910-4411-4ac2-884d-3476c1b6ff96
title: booleanFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d91332f0cc062e7ee4a83e3584776ecf09c5c4b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952081"
---
# <a name="booleanformat"></a><span data-ttu-id="e9aa0-104">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="e9aa0-104">booleanFormat</span></span>

<span data-ttu-id="e9aa0-105">Spécifie comment [**IPropertyDescription :: FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) doit mettre en forme la valeur de la propriété en tant que chaîne.</span><span class="sxs-lookup"><span data-stu-id="e9aa0-105">Specifies how [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) should format the property's value as a string.</span></span> <span data-ttu-id="e9aa0-106">Cela s’applique uniquement si <displayInfo displayType="String"> .</span><span class="sxs-lookup"><span data-stu-id="e9aa0-106">This is applicable only if <displayInfo displayType="String">.</span></span> <span data-ttu-id="e9aa0-107">Il ne doit y avoir qu’un seul élément [BooleanFormat]() pour chaque élément [displayInfo](./propdesc-schema-displayinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="e9aa0-107">There should be only one [booleanFormat]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="e9aa0-108">S’il y a plusieurs éléments, le dernier est utilisé.</span><span class="sxs-lookup"><span data-stu-id="e9aa0-108">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="e9aa0-109">Si aucun élément [BooleanFormat]() n’est fourni, les paramètres d’attribut par défaut sont appliqués à la description de la propriété.</span><span class="sxs-lookup"><span data-stu-id="e9aa0-109">If no [booleanFormat]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9aa0-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e9aa0-110">Syntax</span></span>


```
      <!-- booleanFormat -->
      <xs:element name="booleanFormat"  minOccurs="0" maxOccurs="1">
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
```



## <a name="element-information"></a><span data-ttu-id="e9aa0-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="e9aa0-111">Element Information</span></span>



| <span data-ttu-id="e9aa0-112">Élément parent</span><span class="sxs-lookup"><span data-stu-id="e9aa0-112">Parent Element</span></span>                                   | <span data-ttu-id="e9aa0-113">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="e9aa0-113">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="e9aa0-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="e9aa0-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="e9aa0-115">Aucun</span><span class="sxs-lookup"><span data-stu-id="e9aa0-115">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="e9aa0-116">Attributs</span><span class="sxs-lookup"><span data-stu-id="e9aa0-116">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e9aa0-117">Attribut</span><span class="sxs-lookup"><span data-stu-id="e9aa0-117">Attribute</span></span></th>
<th><span data-ttu-id="e9aa0-118">Description</span><span class="sxs-lookup"><span data-stu-id="e9aa0-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e9aa0-119">formatas</span><span class="sxs-lookup"><span data-stu-id="e9aa0-119">formatAs</span></span></td>
<td><span data-ttu-id="e9aa0-120">Public.</span><span class="sxs-lookup"><span data-stu-id="e9aa0-120">Public.</span></span> <span data-ttu-id="e9aa0-121">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="e9aa0-121">Optional.</span></span> <span data-ttu-id="e9aa0-122">La valeur par défaut est &quot; YesNo &quot; .</span><span class="sxs-lookup"><span data-stu-id="e9aa0-122">Default is &quot;YesNo&quot;.</span></span> <span data-ttu-id="e9aa0-123">Les valeurs valides sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="e9aa0-123">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e9aa0-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="e9aa0-124">Value</span></span></th>
<th><span data-ttu-id="e9aa0-125">Signification</span><span class="sxs-lookup"><span data-stu-id="e9aa0-125">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e9aa0-126">OuiNon</span><span class="sxs-lookup"><span data-stu-id="e9aa0-126">YesNo</span></span></td>
<td><span data-ttu-id="e9aa0-127">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="e9aa0-127">Default.</span></span> <span data-ttu-id="e9aa0-128">Met en forme la valeur sur &quot; Oui &quot; ou &quot; non &quot; .</span><span class="sxs-lookup"><span data-stu-id="e9aa0-128">Formats the value as either &quot;Yes&quot; or &quot;No&quot;.</span></span> <span data-ttu-id="e9aa0-129">Requiert que le type de propriété soit booléen.</span><span class="sxs-lookup"><span data-stu-id="e9aa0-129">Requires the property type to be Boolean.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e9aa0-130">ActiverDésactiver</span><span class="sxs-lookup"><span data-stu-id="e9aa0-130">OnOff</span></span></td>
<td><span data-ttu-id="e9aa0-131">Met en forme la valeur en tant que &quot; activé &quot; ou &quot; désactivé &quot; .</span><span class="sxs-lookup"><span data-stu-id="e9aa0-131">Formats the value as either &quot;On&quot; or &quot;Off&quot;.</span></span> <span data-ttu-id="e9aa0-132">Requiert que le type de propriété soit booléen.</span><span class="sxs-lookup"><span data-stu-id="e9aa0-132">Requires the property type to be Boolean.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e9aa0-133">TrueFalse</span><span class="sxs-lookup"><span data-stu-id="e9aa0-133">TrueFalse</span></span></td>
<td><span data-ttu-id="e9aa0-134">Met en forme la valeur avec la valeur &quot; true &quot; ou &quot; false &quot; .</span><span class="sxs-lookup"><span data-stu-id="e9aa0-134">Formats the value as either &quot;True&quot; or &quot;False&quot;.</span></span> <span data-ttu-id="e9aa0-135">Requiert que le type de propriété soit booléen.</span><span class="sxs-lookup"><span data-stu-id="e9aa0-135">Requires the property type to be Boolean.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
