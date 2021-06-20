---
description: 'Spécifie comment IPropertyDescription :: FormatForDisplay doit mettre en forme la valeur de la propriété booleanFormat sous forme de chaîne.'
ms.assetid: f6384910-4411-4ac2-884d-3476c1b6ff96
title: booleanFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 528458d9c31d54ef43eca8325b1daeef4eee1195
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405962"
---
# <a name="booleanformat"></a><span data-ttu-id="1b38d-103">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="1b38d-103">booleanFormat</span></span>

<span data-ttu-id="1b38d-104">Spécifie comment [**IPropertyDescription :: FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) doit mettre en forme la valeur de la propriété en tant que chaîne.</span><span class="sxs-lookup"><span data-stu-id="1b38d-104">Specifies how [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) should format the property's value as a string.</span></span> <span data-ttu-id="1b38d-105">Cela s’applique uniquement si <displayInfo displayType="String"> .</span><span class="sxs-lookup"><span data-stu-id="1b38d-105">This is applicable only if <displayInfo displayType="String">.</span></span> <span data-ttu-id="1b38d-106">Il ne doit y avoir qu’un seul élément [BooleanFormat]() pour chaque élément [displayInfo](./propdesc-schema-displayinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="1b38d-106">There should be only one [booleanFormat]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="1b38d-107">S’il y a plusieurs éléments, le dernier est utilisé.</span><span class="sxs-lookup"><span data-stu-id="1b38d-107">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="1b38d-108">Si aucun élément [BooleanFormat]() n’est fourni, les paramètres d’attribut par défaut sont appliqués à la description de la propriété.</span><span class="sxs-lookup"><span data-stu-id="1b38d-108">If no [booleanFormat]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b38d-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1b38d-109">Syntax</span></span>


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



## <a name="element-information"></a><span data-ttu-id="1b38d-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="1b38d-110">Element Information</span></span>



| <span data-ttu-id="1b38d-111">Élément parent</span><span class="sxs-lookup"><span data-stu-id="1b38d-111">Parent Element</span></span>                                   | <span data-ttu-id="1b38d-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="1b38d-112">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="1b38d-113">displayInfo</span><span class="sxs-lookup"><span data-stu-id="1b38d-113">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="1b38d-114">Aucun</span><span class="sxs-lookup"><span data-stu-id="1b38d-114">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="1b38d-115">Attributs</span><span class="sxs-lookup"><span data-stu-id="1b38d-115">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1b38d-116">Attribut</span><span class="sxs-lookup"><span data-stu-id="1b38d-116">Attribute</span></span></th>
<th><span data-ttu-id="1b38d-117">Description</span><span class="sxs-lookup"><span data-stu-id="1b38d-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1b38d-118">formatas</span><span class="sxs-lookup"><span data-stu-id="1b38d-118">formatAs</span></span></td>
<td><span data-ttu-id="1b38d-119">Public.</span><span class="sxs-lookup"><span data-stu-id="1b38d-119">Public.</span></span> <span data-ttu-id="1b38d-120">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="1b38d-120">Optional.</span></span> <span data-ttu-id="1b38d-121">La valeur par défaut est &quot; YesNo &quot; .</span><span class="sxs-lookup"><span data-stu-id="1b38d-121">Default is &quot;YesNo&quot;.</span></span> <span data-ttu-id="1b38d-122">Les valeurs valides sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="1b38d-122">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1b38d-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="1b38d-123">Value</span></span></th>
<th><span data-ttu-id="1b38d-124">Signification</span><span class="sxs-lookup"><span data-stu-id="1b38d-124">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1b38d-125">OuiNon</span><span class="sxs-lookup"><span data-stu-id="1b38d-125">YesNo</span></span></td>
<td><span data-ttu-id="1b38d-126">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="1b38d-126">Default.</span></span> <span data-ttu-id="1b38d-127">Met en forme la valeur sur &quot; Oui &quot; ou &quot; non &quot; .</span><span class="sxs-lookup"><span data-stu-id="1b38d-127">Formats the value as either &quot;Yes&quot; or &quot;No&quot;.</span></span> <span data-ttu-id="1b38d-128">Requiert que le type de propriété soit booléen.</span><span class="sxs-lookup"><span data-stu-id="1b38d-128">Requires the property type to be Boolean.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b38d-129">ActiverDésactiver</span><span class="sxs-lookup"><span data-stu-id="1b38d-129">OnOff</span></span></td>
<td><span data-ttu-id="1b38d-130">Met en forme la valeur en tant que &quot; activé &quot; ou &quot; désactivé &quot; .</span><span class="sxs-lookup"><span data-stu-id="1b38d-130">Formats the value as either &quot;On&quot; or &quot;Off&quot;.</span></span> <span data-ttu-id="1b38d-131">Requiert que le type de propriété soit booléen.</span><span class="sxs-lookup"><span data-stu-id="1b38d-131">Requires the property type to be Boolean.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b38d-132">TrueFalse</span><span class="sxs-lookup"><span data-stu-id="1b38d-132">TrueFalse</span></span></td>
<td><span data-ttu-id="1b38d-133">Met en forme la valeur avec la valeur &quot; true &quot; ou &quot; false &quot; .</span><span class="sxs-lookup"><span data-stu-id="1b38d-133">Formats the value as either &quot;True&quot; or &quot;False&quot;.</span></span> <span data-ttu-id="1b38d-134">Requiert que le type de propriété soit booléen.</span><span class="sxs-lookup"><span data-stu-id="1b38d-134">Requires the property type to be Boolean.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
