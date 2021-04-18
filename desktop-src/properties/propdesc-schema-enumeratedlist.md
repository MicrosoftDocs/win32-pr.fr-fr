---
description: 'Spécifie comment IPropertyDescription :: FormatForDisplay doit mettre en forme la valeur de la propriété en tant que chaîne.'
ms.assetid: 49ba57b8-3e08-425f-98b2-52ed2c41a488
title: enumeratedList
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d098b47463b65c483be68eb7750da929df43cee7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519720"
---
# <a name="enumeratedlist"></a><span data-ttu-id="4a013-103">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="4a013-103">enumeratedList</span></span>

<span data-ttu-id="4a013-104">Spécifie comment [**IPropertyDescription :: FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) doit mettre en forme la valeur de la propriété en tant que chaîne.</span><span class="sxs-lookup"><span data-stu-id="4a013-104">Specifies how [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) should format the property's value as a string.</span></span> <span data-ttu-id="4a013-105">Elle influence également la manière dont la propriété peut être regroupée, ou les valeurs à afficher dans la liste si « editControl » est un listblox.</span><span class="sxs-lookup"><span data-stu-id="4a013-105">It also influences how the property may be grouped, or what values to show in the list if the "editControl" is a listblox.</span></span> <span data-ttu-id="4a013-106">Cela s’applique uniquement si <displayInfo displayType="Enumerated"> .</span><span class="sxs-lookup"><span data-stu-id="4a013-106">This is applicable only if <displayInfo displayType="Enumerated">.</span></span> <span data-ttu-id="4a013-107">Il ne doit y avoir qu’un seul élément [enumeratedList]() pour chaque élément [displayInfo](./propdesc-schema-displayinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="4a013-107">There should be only one [enumeratedList]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="4a013-108">S’il y a plusieurs éléments, le dernier est utilisé.</span><span class="sxs-lookup"><span data-stu-id="4a013-108">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="4a013-109">Si aucun élément [enumeratedList]() n’est fourni, les paramètres d’attribut par défaut sont appliqués à la description de la propriété.</span><span class="sxs-lookup"><span data-stu-id="4a013-109">If no [enumeratedList]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a013-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4a013-110">Syntax</span></span>


```
<!-- enumeratedList -->
<xs:element name="enumeratedList"  minOccurs="0" maxOccurs="1">
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
                    <xs:attribute name="minValue" type="xs:integer" use="required"/>
                    <xs:attribute name="setValue" type="xs:integer"/>
                    <xs:attribute name="text" type="xs:string"/>
                </xs:complexType>
            </xs:element>
        </xs:sequence>
        <xs:attribute name="defaultText" type="xs:string"/>
        <xs:attribute name="useValueForDefault" type="xs:boolean"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="4a013-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="4a013-111">Element Information</span></span>



| <span data-ttu-id="4a013-112">Élément parent</span><span class="sxs-lookup"><span data-stu-id="4a013-112">Parent Element</span></span>                                   | <span data-ttu-id="4a013-113">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="4a013-113">Child Elements</span></span>                               |
|--------------------------------------------------|----------------------------------------------|
| [<span data-ttu-id="4a013-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="4a013-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | [<span data-ttu-id="4a013-115">variables</span><span class="sxs-lookup"><span data-stu-id="4a013-115">enum</span></span>](./propdesc-schema-enum.md)           |
|                                                  | [<span data-ttu-id="4a013-116">enumRange</span><span class="sxs-lookup"><span data-stu-id="4a013-116">enumRange</span></span>](./propdesc-schema-enumrange.md) |



 

## <a name="attributes"></a><span data-ttu-id="4a013-117">Attributs</span><span class="sxs-lookup"><span data-stu-id="4a013-117">Attributes</span></span>



| <span data-ttu-id="4a013-118">Attribut</span><span class="sxs-lookup"><span data-stu-id="4a013-118">Attribute</span></span>          | <span data-ttu-id="4a013-119">Description</span><span class="sxs-lookup"><span data-stu-id="4a013-119">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a013-120">defaultText</span><span class="sxs-lookup"><span data-stu-id="4a013-120">defaultText</span></span>        | <span data-ttu-id="4a013-121">Public.</span><span class="sxs-lookup"><span data-stu-id="4a013-121">Public.</span></span> <span data-ttu-id="4a013-122">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="4a013-122">Optional.</span></span> <span data-ttu-id="4a013-123">Spécifiez le texte par défaut à utiliser si une valeur est donnée à [**IPropertyDescription :: FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) qui n’est pas mappée à l’un des éléments énumérés dans la liste.</span><span class="sxs-lookup"><span data-stu-id="4a013-123">Specify default text to use if a value is given to [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) that does not map to one of the enumerated elements in the list.</span></span> <span data-ttu-id="4a013-124">La syntaxe autorise une chaîne d’affichage directe ou une référence à une chaîne d’affichage indirecte ; Utilisez la référence, afin qu’elle puisse être localisée.</span><span class="sxs-lookup"><span data-stu-id="4a013-124">The syntax allows for a direct display string or an indirect display string reference; use the reference, so it can be localized.</span></span>                              |
| <span data-ttu-id="4a013-125">useValueForDefault</span><span class="sxs-lookup"><span data-stu-id="4a013-125">useValueForDefault</span></span> | <span data-ttu-id="4a013-126">Public.</span><span class="sxs-lookup"><span data-stu-id="4a013-126">Public.</span></span> <span data-ttu-id="4a013-127">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="4a013-127">Optional.</span></span> <span data-ttu-id="4a013-128">Si la valeur est définie sur « true », [**IPropertyDescription :: FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) utilise la valeur telle quelle si la valeur n’est pas mappée à l’un des éléments énumérés dans la liste.</span><span class="sxs-lookup"><span data-stu-id="4a013-128">Setting this to "true" will inform [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) to use the value as-is if the value does not map to one of the enumerated elements in the list.</span></span> <span data-ttu-id="4a013-129">Pour **IPropertyDescription :: FormatForDisplay**, l’affectation de la valeur « true » a priorité sur la définition de « DefaultText ».</span><span class="sxs-lookup"><span data-stu-id="4a013-129">For **IPropertyDescription::FormatForDisplay**, setting this to "true" takes precedence over setting the "defaultText".</span></span> <span data-ttu-id="4a013-130">La valeur par défaut est « false ».</span><span class="sxs-lookup"><span data-stu-id="4a013-130">The default is "false".</span></span> |



 

 

 
