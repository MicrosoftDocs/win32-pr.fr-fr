---
description: L’élément booléen facultatif <isDefaultNonOwnerSaveLocation> spécifie si l’emplacement décrit dans le connecteur de recherche doit être utilisé comme emplacement d’enregistrement par défaut lorsqu’un utilisateur d’un autre ordinateur d’un groupe résidentiel choisit d’enregistrer un élément.
ms.assetid: 4286b122-2454-4dc3-9c06-9967b7a763dd
title: Élément isDefaultNonOwnerSaveLocation (schéma du connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edd39ab76ae1b99d6518ca40407d328f5da9778c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517236"
---
# <a name="isdefaultnonownersavelocation-element-search-connector-schema"></a><span data-ttu-id="84bb5-103">Élément isDefaultNonOwnerSaveLocation (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="84bb5-103">isDefaultNonOwnerSaveLocation Element (Search Connector Schema)</span></span>

<span data-ttu-id="84bb5-104">L’élément booléen facultatif <isDefaultNonOwnerSaveLocation> spécifie si l’emplacement décrit dans le connecteur de recherche doit être utilisé comme emplacement d’enregistrement par défaut lorsqu’un utilisateur d’un autre ordinateur d’un groupe résidentiel choisit d’enregistrer un élément.</span><span class="sxs-lookup"><span data-stu-id="84bb5-104">The optional Boolean <isDefaultNonOwnerSaveLocation> element specifies whether the location described in the search connector should be used as the default save location when a user from another computer in a Homegroup chooses to save an item.</span></span> <span data-ttu-id="84bb5-105">Cet élément n’a pas d’éléments enfants ni d’attributs.</span><span class="sxs-lookup"><span data-stu-id="84bb5-105">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="84bb5-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="84bb5-106">Syntax</span></span>


```
<!-- isDefaultNonOwnerSaveLocation -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="isDefaultNonOwnerSaveLocation" type="xs:boolean" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="84bb5-107">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="84bb5-107">Element Information</span></span>



| <span data-ttu-id="84bb5-108">Élément parent</span><span class="sxs-lookup"><span data-stu-id="84bb5-108">Parent Element</span></span>                                                                                                   | <span data-ttu-id="84bb5-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="84bb5-109">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="84bb5-110">Élément searchConnectorDescriptionType (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="84bb5-110">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="84bb5-111">Notes</span><span class="sxs-lookup"><span data-stu-id="84bb5-111">Remarks</span></span>

<span data-ttu-id="84bb5-112">Si la valeur est true, lorsqu’un utilisateur d’un autre ordinateur d’un groupe résidentiel choisit d’enregistrer un élément, l’Explorateur Windows l’enregistre à l’emplacement spécifié dans l' <simpleLocation> élément.</span><span class="sxs-lookup"><span data-stu-id="84bb5-112">If true, when a user from another computer in a Homegroup chooses to save an item, Windows Explorer saves the item to the location specified in the <simpleLocation> element.</span></span>

## <a name="example"></a><span data-ttu-id="84bb5-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="84bb5-113">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <isDefaultNonOwnerSaveLocation>true</isDefaultNonOwnerSaveLocation>
    ...
</searchConnectionDescription>
```



 

 



