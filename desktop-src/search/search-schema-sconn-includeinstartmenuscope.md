---
description: L’élément booléen facultatif <includeInStartMenuScope> spécifie si ce connecteur de recherche doit être inclus dans l’étendue de recherche du menu Démarrer.
ms.assetid: 934a3834-9ddc-4c15-b738-68ea74adc24c
title: Élément includeInStartMenuScope (schéma du connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 126d10a2b69dcec5057e732679c8531fd6e82bca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531652"
---
# <a name="includeinstartmenuscope-element-search-connector-schema"></a><span data-ttu-id="9ca41-103">Élément includeInStartMenuScope (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="9ca41-103">includeInStartMenuScope Element (Search Connector Schema)</span></span>

<span data-ttu-id="9ca41-104">L’élément booléen facultatif <includeInStartMenuScope> spécifie si ce connecteur de recherche doit être inclus dans l’étendue de recherche du menu Démarrer.</span><span class="sxs-lookup"><span data-stu-id="9ca41-104">The optional Boolean <includeInStartMenuScope> element specifies whether this search connector should be included in the Start menu search scope.</span></span> <span data-ttu-id="9ca41-105">La valeur par défaut est true pour les connecteurs de recherche utilisant le système de fichiers comme source de données, et false pour les connecteurs de recherche utilisés par les gestionnaires de propriétés.</span><span class="sxs-lookup"><span data-stu-id="9ca41-105">The default value is true for search connectors using the file system as a data source, and false for search connectors used by property handlers.</span></span> <span data-ttu-id="9ca41-106">Cet élément n’a pas d’éléments enfants ni d’attributs.</span><span class="sxs-lookup"><span data-stu-id="9ca41-106">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ca41-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9ca41-107">Syntax</span></span>


```
<!-- includeInStartMenuScope -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="includeInStartMenuScope" type="xs:boolean" default="false" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="9ca41-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="9ca41-108">Element Information</span></span>



| <span data-ttu-id="9ca41-109">Élément parent</span><span class="sxs-lookup"><span data-stu-id="9ca41-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="9ca41-110">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="9ca41-110">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="9ca41-111">Élément searchConnectorDescriptionType (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="9ca41-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="9ca41-112">Notes</span><span class="sxs-lookup"><span data-stu-id="9ca41-112">Remarks</span></span>

<span data-ttu-id="9ca41-113">Si vous incluez le connecteur de recherche dans l’étendue du menu Démarrer, les utilisateurs peuvent effectuer une recherche dans votre emplacement à partir de la zone de recherche dans le menu Démarrer.</span><span class="sxs-lookup"><span data-stu-id="9ca41-113">If you include the search connector in the Start menu scope, users can search your location from the search box in the Start menu.</span></span>

## <a name="example"></a><span data-ttu-id="9ca41-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="9ca41-114">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <includeinStartMenuScope>true</includeinStartMenuScope>
    ...
</searchConnectionDescription>
```



 

 



