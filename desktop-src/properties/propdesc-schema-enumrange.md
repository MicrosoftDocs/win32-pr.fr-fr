---
description: Assigne un texte d’énumération à une plage de valeurs. Chaque élément enumRange spécifie une valeur minimale et s’étend jusqu’à la valeur minimale de l’élément suivant, ou jusqu’à ce qu’il n’y ait plus d’éléments enumRange.
ms.assetid: 00c56c2d-6693-4b09-b28a-21d69930bf35
title: enumRange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 964835c376c5496d23e8d277409575758002a0d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951607"
---
# <a name="enumrange"></a><span data-ttu-id="0e53a-104">enumRange</span><span class="sxs-lookup"><span data-stu-id="0e53a-104">enumRange</span></span>

<span data-ttu-id="0e53a-105">Assigne un texte d’énumération à une plage de valeurs.</span><span class="sxs-lookup"><span data-stu-id="0e53a-105">Assigns enumeration text to a range of values.</span></span> <span data-ttu-id="0e53a-106">Chaque élément [enumRange]() spécifie une valeur minimale et s’étend jusqu’à la valeur minimale de l’élément suivant, ou jusqu’à ce qu’il n’y ait plus d’éléments enumRange.</span><span class="sxs-lookup"><span data-stu-id="0e53a-106">Each [enumRange]() element specifies a minimum value, and extends until the next element minimum value, or until there are no more enumRange elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e53a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0e53a-107">Syntax</span></span>

``` syntax
<!-- enumRange -->
<xs:element name="enumRange" minOccurs="0" maxOccurs="unbounded">
    <xs:complexType>
        <xs:sequence>
            <xs:element ref="image" minOccurs="0" maxOccurs="1"/>
        </xs:sequence>
            <xs:attribute name="minValue" type="xs:integer" use="required"/>
            <xs:attribute name="setValue" type="xs:integer"/>
            <xs:attribute name="text" type="xs:string"/>
            <xs:attribute name="name" type="canonical-name"/> <!--Maximum of 64 characters-->
            <xs:attribute name="mnemonics" type="xs:string"/> 
    </xs:complexType>
</xs:element>
```

## <a name="element-information"></a><span data-ttu-id="0e53a-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="0e53a-108">Element Information</span></span>



| <span data-ttu-id="0e53a-109">Élément parent</span><span class="sxs-lookup"><span data-stu-id="0e53a-109">Parent Element</span></span>                                         | <span data-ttu-id="0e53a-110">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="0e53a-110">Child Elements</span></span> |
|--------------------------------------------------------|----------------|
| [<span data-ttu-id="0e53a-111">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="0e53a-111">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md) | <span data-ttu-id="0e53a-112">aucun</span><span class="sxs-lookup"><span data-stu-id="0e53a-112">none</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="0e53a-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="0e53a-113">Attributes</span></span>



| <span data-ttu-id="0e53a-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="0e53a-114">Attribute</span></span> | <span data-ttu-id="0e53a-115">Description</span><span class="sxs-lookup"><span data-stu-id="0e53a-115">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e53a-116">minValue</span><span class="sxs-lookup"><span data-stu-id="0e53a-116">minValue</span></span>  | <span data-ttu-id="0e53a-117">Public.</span><span class="sxs-lookup"><span data-stu-id="0e53a-117">Public.</span></span> <span data-ttu-id="0e53a-118">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="0e53a-118">Required.</span></span> <span data-ttu-id="0e53a-119">Valeur minimale de la plage.</span><span class="sxs-lookup"><span data-stu-id="0e53a-119">The minimum value in the range.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="0e53a-120">setValue</span><span class="sxs-lookup"><span data-stu-id="0e53a-120">setValue</span></span>  | <span data-ttu-id="0e53a-121">Public.</span><span class="sxs-lookup"><span data-stu-id="0e53a-121">Public.</span></span> <span data-ttu-id="0e53a-122">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="0e53a-122">Optional.</span></span> <span data-ttu-id="0e53a-123">Lorsqu’un utilisateur sélectionne cette énumération à partir d’un contrôle de propriété ListBox, cette valeur discrète est affectée en tant que valeur de propriété.</span><span class="sxs-lookup"><span data-stu-id="0e53a-123">When a user selects this enumeration from a listbox property control, this discrete value is assigned as the property value.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="0e53a-124">text</span><span class="sxs-lookup"><span data-stu-id="0e53a-124">text</span></span>      | <span data-ttu-id="0e53a-125">Public.</span><span class="sxs-lookup"><span data-stu-id="0e53a-125">Public.</span></span> <span data-ttu-id="0e53a-126">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="0e53a-126">Optional.</span></span> <span data-ttu-id="0e53a-127">Texte utilisé pour afficher la valeur énumérée.</span><span class="sxs-lookup"><span data-stu-id="0e53a-127">The text used to display the enumerated value.</span></span> <span data-ttu-id="0e53a-128">La syntaxe autorise une chaîne d’affichage directe ou une référence à une chaîne d’affichage indirecte ; Utilisez la chaîne d’affichage indirecte afin qu’elle puisse être localisée.</span><span class="sxs-lookup"><span data-stu-id="0e53a-128">The syntax allows for a direct display string or an indirect display string reference; use the indirect display string so that it can be localized.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="0e53a-129">mnémoniques</span><span class="sxs-lookup"><span data-stu-id="0e53a-129">mnemonics</span></span> | <span data-ttu-id="0e53a-130">**Windows 7 et versions ultérieures.**</span><span class="sxs-lookup"><span data-stu-id="0e53a-130">**Windows 7 and later.**</span></span> <span data-ttu-id="0e53a-131">Public.</span><span class="sxs-lookup"><span data-stu-id="0e53a-131">Public.</span></span> <span data-ttu-id="0e53a-132">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="0e53a-132">Optional.</span></span> <span data-ttu-id="0e53a-133">Liste de valeurs mnémoniques qui peuvent être utilisées pour faire référence à la propriété dans les requêtes de recherche.</span><span class="sxs-lookup"><span data-stu-id="0e53a-133">A list of mnemonic values that can be used to refer to the property in search queries.</span></span> <span data-ttu-id="0e53a-134">La liste est délimitée par le \| caractère «».</span><span class="sxs-lookup"><span data-stu-id="0e53a-134">The list is delimited with the '\|' character.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="0e53a-135">name</span><span class="sxs-lookup"><span data-stu-id="0e53a-135">name</span></span>      | <span data-ttu-id="0e53a-136">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="0e53a-136">Required.</span></span> <span data-ttu-id="0e53a-137">Nom de propriété canonique, unique au système ; par exemple, System. Rating.</span><span class="sxs-lookup"><span data-stu-id="0e53a-137">The canonical property name, unique to the system; for example, System.Rating.</span></span> <span data-ttu-id="0e53a-138">Cet attribut est limité à 64 caractères.</span><span class="sxs-lookup"><span data-stu-id="0e53a-138">This attribute is limited to 64 characters.</span></span> <span data-ttu-id="0e53a-139">Le nom respecte la casse et doit utiliser la syntaxe suivante : Publisher. application. PropertyName.</span><span class="sxs-lookup"><span data-stu-id="0e53a-139">The name is case sensitive and should use the following syntax: Publisher.Application.PropertyName.</span></span> <span data-ttu-id="0e53a-140">Les méthodes suivantes retournent cette valeur : [**IExplorerCommand :: GetCanonicalName**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getcanonicalname), [**IPropertyDescription :: GetCanonicalName**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getcanonicalname), [**IPropertyDescription2 :: GetCanonicalName**](/windows/desktop/api/Propsys/nn-propsys-ipropertydescription2)et [**IPropertyUI :: GetCanonicalName**](/previous-versions/windows/desktop/legacy/dd758076(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0e53a-140">The following methods return this value: [**IExplorerCommand::GetCanonicalName**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getcanonicalname), [**IPropertyDescription::GetCanonicalName**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getcanonicalname), [**IPropertyDescription2::GetCanonicalName**](/windows/desktop/api/Propsys/nn-propsys-ipropertydescription2), and [**IPropertyUI::GetCanonicalName**](/previous-versions/windows/desktop/legacy/dd758076(v=vs.85)).</span></span> |



 

 

 
