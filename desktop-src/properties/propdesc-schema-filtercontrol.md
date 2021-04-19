---
description: Spécifie le contrôle à utiliser dans le menu filtre d’en-tête.
ms.assetid: a3117e16-20d0-4637-b726-9fa49516ad5c
title: filterControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0c0de28eaa349b9a999ba39c1bad47aa01d43d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520484"
---
# <a name="filtercontrol"></a><span data-ttu-id="7cbc4-103">filterControl</span><span class="sxs-lookup"><span data-stu-id="7cbc4-103">filterControl</span></span>

<span data-ttu-id="7cbc4-104">Spécifie le contrôle à utiliser dans le menu filtre d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="7cbc4-104">Specifies what control to use in the header filter menu.</span></span> <span data-ttu-id="7cbc4-105">Il ne doit y avoir qu’un seul élément [filterControl]() pour chaque élément [displayInfo](./propdesc-schema-displayinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="7cbc4-105">There should be only one [filterControl]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="7cbc4-106">S’il y a plusieurs éléments, le dernier est utilisé.</span><span class="sxs-lookup"><span data-stu-id="7cbc4-106">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="7cbc4-107">Si aucun élément [filterControl]() n’est fourni, les paramètres d’attribut par défaut sont appliqués à la description de la propriété.</span><span class="sxs-lookup"><span data-stu-id="7cbc4-107">If no [filterControl]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cbc4-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7cbc4-108">Syntax</span></span>


```
      <!-- filterControl -->
      <xs:element name="filterControl"  minOccurs="0" maxOccurs="1">
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
```



## <a name="element-information"></a><span data-ttu-id="7cbc4-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="7cbc4-109">Element Information</span></span>



| <span data-ttu-id="7cbc4-110">Élément parent</span><span class="sxs-lookup"><span data-stu-id="7cbc4-110">Parent Element</span></span>                                   | <span data-ttu-id="7cbc4-111">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="7cbc4-111">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="7cbc4-112">displayInfo</span><span class="sxs-lookup"><span data-stu-id="7cbc4-112">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="7cbc4-113">Aucun</span><span class="sxs-lookup"><span data-stu-id="7cbc4-113">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="7cbc4-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="7cbc4-114">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7cbc4-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="7cbc4-115">Attribute</span></span></th>
<th><span data-ttu-id="7cbc4-116">Description</span><span class="sxs-lookup"><span data-stu-id="7cbc4-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7cbc4-117">contrôle</span><span class="sxs-lookup"><span data-stu-id="7cbc4-117">control</span></span></td>
<td><span data-ttu-id="7cbc4-118">Public.</span><span class="sxs-lookup"><span data-stu-id="7cbc4-118">Public.</span></span> <span data-ttu-id="7cbc4-119">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="7cbc4-119">Optional.</span></span> <span data-ttu-id="7cbc4-120">La valeur par défaut est &quot; default &quot; .</span><span class="sxs-lookup"><span data-stu-id="7cbc4-120">Default is &quot;Default&quot;.</span></span> <span data-ttu-id="7cbc4-121">Les valeurs valides sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="7cbc4-121">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="7cbc4-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="7cbc4-122">Value</span></span></th>
<th><span data-ttu-id="7cbc4-123">Signification</span><span class="sxs-lookup"><span data-stu-id="7cbc4-123">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7cbc4-124">Default</span><span class="sxs-lookup"><span data-stu-id="7cbc4-124">Default</span></span></td>
<td><span data-ttu-id="7cbc4-125">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="7cbc4-125">Default.</span></span> <span data-ttu-id="7cbc4-126">Utilise le contrôle par défaut basé sur l' <typeInfo type=&quot;&quot;> attribut.</span><span class="sxs-lookup"><span data-stu-id="7cbc4-126">Uses the default control, based upon the <typeInfo type=&quot;&quot;> attribute.</span></span> <span data-ttu-id="7cbc4-127">Le type par défaut est &quot; DateTime &quot; et le contrôle par défaut est &quot; Calendar &quot; .</span><span class="sxs-lookup"><span data-stu-id="7cbc4-127">The default type is &quot;DateTime&quot; and the default control is &quot;Calendar&quot;.</span></span> <span data-ttu-id="7cbc4-128">Tout autre type ne produit aucun contrôle de filtre spécial.</span><span class="sxs-lookup"><span data-stu-id="7cbc4-128">Any other type results in no special filter control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cbc4-129">Calendrier</span><span class="sxs-lookup"><span data-stu-id="7cbc4-129">Calendar</span></span></td>
<td><span data-ttu-id="7cbc4-130">Utilise le contrôle calendrier.</span><span class="sxs-lookup"><span data-stu-id="7cbc4-130">Uses the calendar control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7cbc4-131">Rating</span><span class="sxs-lookup"><span data-stu-id="7cbc4-131">Rating</span></span></td>
<td><span data-ttu-id="7cbc4-132">Utilise le contrôle d’évaluation 5 étoiles.</span><span class="sxs-lookup"><span data-stu-id="7cbc4-132">Uses the 5-star rating control.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
