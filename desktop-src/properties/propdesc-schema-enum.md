---
description: Utilisé pour assigner du texte énuméré à des valeurs discrètes.
ms.assetid: c8cc040e-fcce-43a0-98c1-db2b2c616ac3
title: enum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b615697e669f8d02e0530a1763309cfe74113467
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106525074"
---
# <a name="enum"></a><span data-ttu-id="42782-103">enum</span><span class="sxs-lookup"><span data-stu-id="42782-103">enum</span></span>

<span data-ttu-id="42782-104">Utilisé pour assigner du texte énuméré à des valeurs discrètes.</span><span class="sxs-lookup"><span data-stu-id="42782-104">Used to assign enumerated text to discrete values.</span></span> <span data-ttu-id="42782-105">N’importe quel nombre de ces éléments peut exister sous un [enumeratedList](./propdesc-schema-enumeratedlist.md).</span><span class="sxs-lookup"><span data-stu-id="42782-105">Any number of these elements may exist under an [enumeratedList](./propdesc-schema-enumeratedlist.md).</span></span> <span data-ttu-id="42782-106">Par programme, elles sont représentées en tant qu’objets IPropertyEnumType, dont la méthode [**IPropertyEnumType :: GetEnumType**](/windows/win32/api/propsys/nf-propsys-ipropertyenumtype-getenumtype) retourne PET \_ DISCRETEVALUE.</span><span class="sxs-lookup"><span data-stu-id="42782-106">Programmatically, these are represented as IPropertyEnumType objects, whose [**IPropertyEnumType::GetEnumType**](/windows/win32/api/propsys/nf-propsys-ipropertyenumtype-getenumtype) method returns PET\_DISCRETEVALUE.</span></span>

## <a name="syntax"></a><span data-ttu-id="42782-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="42782-107">Syntax</span></span>


```
<!-- enum -->
<xs:element name="enum" minOccurs="0" maxOccurs="unbounded">
    <xs:complexType>
        <xs:sequence>
            <xs:element ref="image" minOccurs="0" maxOccurs="1"/>
        </xs:sequence>
        <xs:attribute name="value" type="xs:string" use="required"/>
        <xs:attribute name="text" type="xs:string" use="required"/>
        <xs:attribute name="mnemonics" type="xs:string"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="42782-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="42782-108">Element Information</span></span>



| <span data-ttu-id="42782-109">Élément parent</span><span class="sxs-lookup"><span data-stu-id="42782-109">Parent Element</span></span>                                         | <span data-ttu-id="42782-110">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="42782-110">Child Elements</span></span> |
|--------------------------------------------------------|----------------|
| [<span data-ttu-id="42782-111">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="42782-111">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md) | <span data-ttu-id="42782-112">aucun</span><span class="sxs-lookup"><span data-stu-id="42782-112">none</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="42782-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="42782-113">Attributes</span></span>



| <span data-ttu-id="42782-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="42782-114">Attribute</span></span> | <span data-ttu-id="42782-115">Description</span><span class="sxs-lookup"><span data-stu-id="42782-115">Description</span></span>                                                                                                                                                                                                          |
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42782-116">value</span><span class="sxs-lookup"><span data-stu-id="42782-116">value</span></span>     | <span data-ttu-id="42782-117">Public.</span><span class="sxs-lookup"><span data-stu-id="42782-117">Public.</span></span> <span data-ttu-id="42782-118">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="42782-118">Required.</span></span> <span data-ttu-id="42782-119">Valeur discrète (chaîne ou nombre) à laquelle assigner le texte énuméré.</span><span class="sxs-lookup"><span data-stu-id="42782-119">The discrete value (string or number) to be assigned enumerated text to.</span></span>                                                                                                                           |
| <span data-ttu-id="42782-120">text</span><span class="sxs-lookup"><span data-stu-id="42782-120">text</span></span>      | <span data-ttu-id="42782-121">Public.</span><span class="sxs-lookup"><span data-stu-id="42782-121">Public.</span></span> <span data-ttu-id="42782-122">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="42782-122">Required.</span></span> <span data-ttu-id="42782-123">Texte utilisé pour afficher la valeur énumérée.</span><span class="sxs-lookup"><span data-stu-id="42782-123">The text used to display the enumerated value.</span></span> <span data-ttu-id="42782-124">La syntaxe autorise une chaîne d’affichage directe ou une référence à une chaîne d’affichage indirecte ; Utilisez la chaîne d’affichage indirecte afin qu’elle puisse être localisée.</span><span class="sxs-lookup"><span data-stu-id="42782-124">The syntax allows for a direct display string or an indirect display string reference; use the indirect display string so that it can be localized.</span></span> |
| <span data-ttu-id="42782-125">mnémoniques</span><span class="sxs-lookup"><span data-stu-id="42782-125">mnemonics</span></span> | <span data-ttu-id="42782-126">**Windows 7 et versions ultérieures.**</span><span class="sxs-lookup"><span data-stu-id="42782-126">**Windows 7 and later.**</span></span> <span data-ttu-id="42782-127">Public.</span><span class="sxs-lookup"><span data-stu-id="42782-127">Public.</span></span> <span data-ttu-id="42782-128">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="42782-128">Optional.</span></span> <span data-ttu-id="42782-129">Liste de valeurs mnémoniques qui peuvent être utilisées pour faire référence à la propriété dans les requêtes de recherche.</span><span class="sxs-lookup"><span data-stu-id="42782-129">A list of mnemonic values that can be used to refer to the property in search queries.</span></span> <span data-ttu-id="42782-130">La liste est délimitée par le \| caractère «».</span><span class="sxs-lookup"><span data-stu-id="42782-130">The list is delimited with the '\|' character.</span></span>                                     |



 

 

 
