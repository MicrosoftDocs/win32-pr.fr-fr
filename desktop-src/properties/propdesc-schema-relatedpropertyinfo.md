---
description: Nouveauté de Windows 7. Élément conteneur pour les éléments relatedProperty.
ms.assetid: F8BAAE5C-A7EA-487a-B829-91A27E24B58D
title: relatedPropertyInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 442de657bed7e97f74064c39cc0934c65a6f520d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520483"
---
# <a name="relatedpropertyinfo"></a><span data-ttu-id="2d8ed-104">relatedPropertyInfo</span><span class="sxs-lookup"><span data-stu-id="2d8ed-104">relatedPropertyInfo</span></span>

<span data-ttu-id="2d8ed-105">Nouveauté de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2d8ed-105">New for Windows 7.</span></span> <span data-ttu-id="2d8ed-106">Élément conteneur pour les éléments [relatedProperty](./propdesc-schema-relatedproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="2d8ed-106">Container element for [relatedProperty](./propdesc-schema-relatedproperty.md) elements.</span></span> <span data-ttu-id="2d8ed-107">Il ne doit y avoir qu’un seul élément [relatedPropertyInfo]() pour chaque élément [PropertyDescription](./propdesc-schema-propertydescription.md) .</span><span class="sxs-lookup"><span data-stu-id="2d8ed-107">There should be only one [relatedPropertyInfo]() element for each [propertyDescription](./propdesc-schema-propertydescription.md) element.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d8ed-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2d8ed-108">Syntax</span></span>


```
<!-- relatedPropertyInfo -->
<xs:element name="relatedPropertyInfo">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="relatedProperty" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:attribute name="relationshipName" type="canonical-name" use="required"/>
                    <xs:attribute name="propertyName" type="canonical-name" use="required"/>
                </xs:complexType>
            </xs:element>
        </xs:sequence>
    </xs:complexType>

    <xs:unique name="No_two_relatedProperties_can_have_the_same_relationship_name">
        <xs:selector xpath="s:relatedProperty"/>
        <xs:field    xpath="@relationshipName"/>
    </xs:unique>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="2d8ed-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="2d8ed-109">Element Information</span></span>



| <span data-ttu-id="2d8ed-110">Élément parent</span><span class="sxs-lookup"><span data-stu-id="2d8ed-110">Parent Element</span></span>                                                   | <span data-ttu-id="2d8ed-111">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="2d8ed-111">Child Elements</span></span>                                           |
|------------------------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="2d8ed-112">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="2d8ed-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md) | [<span data-ttu-id="2d8ed-113">relatedProperty</span><span class="sxs-lookup"><span data-stu-id="2d8ed-113">relatedProperty</span></span>](./propdesc-schema-relatedproperty.md) |



 

## <a name="attributes"></a><span data-ttu-id="2d8ed-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="2d8ed-114">Attributes</span></span>

<span data-ttu-id="2d8ed-115">Cet élément n’a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="2d8ed-115">This element has no attributes.</span></span>

 

 
