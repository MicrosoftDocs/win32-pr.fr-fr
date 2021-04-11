---
description: Nouveauté de Windows 7. Identifie une propriété qui est associée à la propriété définie dans le fichier de description de la propriété.
ms.assetid: 30167942-141A-4f37-B019-0811BA654124
title: relatedProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cabde093a47a25834598659d3ad38e0847c1351d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318897"
---
# <a name="relatedproperty"></a><span data-ttu-id="26ae5-104">relatedProperty</span><span class="sxs-lookup"><span data-stu-id="26ae5-104">relatedProperty</span></span>

<span data-ttu-id="26ae5-105">Nouveauté de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="26ae5-105">New for Windows 7.</span></span> <span data-ttu-id="26ae5-106">Identifie une propriété qui est associée à la propriété définie dans le fichier de description de la propriété.</span><span class="sxs-lookup"><span data-stu-id="26ae5-106">Identifies a property that is related to the property defined in the property description file.</span></span> <span data-ttu-id="26ae5-107">Au besoin, il peut y avoir autant d’éléments [relatedProperty]() dans un [relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="26ae5-107">There can be as many [relatedProperty]() elements within a [relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md) as needed.</span></span>

## <a name="syntax"></a><span data-ttu-id="26ae5-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="26ae5-108">Syntax</span></span>


```
<!-- relatedPropertyInfo -->
<xs:element name="relatedProperty" minOccurs="0" maxOccurs="unbounded">
    <xs:complexType>
        <xs:attribute name="relationshipName" type="canonical-name" use="required"/>
        <xs:attribute name="propertyName" type="canonical-name" use="required"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="26ae5-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="26ae5-109">Element Information</span></span>



| <span data-ttu-id="26ae5-110">Élément parent</span><span class="sxs-lookup"><span data-stu-id="26ae5-110">Parent Element</span></span>                                                   | <span data-ttu-id="26ae5-111">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="26ae5-111">Child Elements</span></span> |
|------------------------------------------------------------------|----------------|
| [<span data-ttu-id="26ae5-112">relatedPropertyInfo</span><span class="sxs-lookup"><span data-stu-id="26ae5-112">relatedPropertyInfo</span></span>](./propdesc-schema-relatedpropertyinfo.md) | <span data-ttu-id="26ae5-113">Aucun</span><span class="sxs-lookup"><span data-stu-id="26ae5-113">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="26ae5-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="26ae5-114">Attributes</span></span>



| <span data-ttu-id="26ae5-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="26ae5-115">Attribute</span></span>        | <span data-ttu-id="26ae5-116">Description</span><span class="sxs-lookup"><span data-stu-id="26ae5-116">Description</span></span>                                                        |
|------------------|--------------------------------------------------------------------|
| <span data-ttu-id="26ae5-117">relationshipName</span><span class="sxs-lookup"><span data-stu-id="26ae5-117">relationshipName</span></span> | <span data-ttu-id="26ae5-118">Public.</span><span class="sxs-lookup"><span data-stu-id="26ae5-118">Public.</span></span> <span data-ttu-id="26ae5-119">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="26ae5-119">Required.</span></span> <span data-ttu-id="26ae5-120">Nom canonique de la relation de propriété.</span><span class="sxs-lookup"><span data-stu-id="26ae5-120">The canonical name of the property relationship.</span></span> |
| <span data-ttu-id="26ae5-121">propertyName</span><span class="sxs-lookup"><span data-stu-id="26ae5-121">propertyName</span></span>     | <span data-ttu-id="26ae5-122">Public.</span><span class="sxs-lookup"><span data-stu-id="26ae5-122">Public.</span></span> <span data-ttu-id="26ae5-123">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="26ae5-123">Required.</span></span> <span data-ttu-id="26ae5-124">Nom canonique de la propriété associée.</span><span class="sxs-lookup"><span data-stu-id="26ae5-124">The canonical name of the related property.</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="26ae5-125">Notes</span><span class="sxs-lookup"><span data-stu-id="26ae5-125">Remarks</span></span>

<span data-ttu-id="26ae5-126">Cet élément vous permet de mapper une propriété à une autre.</span><span class="sxs-lookup"><span data-stu-id="26ae5-126">This element enables you to map one property to another.</span></span> <span data-ttu-id="26ae5-127">Par exemple, vous pouvez mapper le texte de votre propriété personnalisée, fabrikam. StorageCapacity, à System. Capacity :</span><span class="sxs-lookup"><span data-stu-id="26ae5-127">For example, you can map the text of your custom property, Fabrikam.StorageCapacity, to System.Capacity:</span></span>


```
<!-- relatedPropertyInfo -->
<propertyDescription name="Fabrikam.StorageCapacity" ... >
    ...
    <relatedPropertyInfo>
        <relatedProperty relationshipName="System.RelatedProperty.Text" propertyName="System.Capacity"/>
    </relatedPropertyInfo>
</propertyDescription>
```



 

 
