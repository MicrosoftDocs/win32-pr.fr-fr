---
description: L’élément booléen facultatif <isIndexed> spécifie si l’emplacement décrit par le connecteur de recherche est indexé (localement ou à distance à l’aide de Windows Search 4 ou version ultérieure).
ms.assetid: e72b5614-454c-481f-bc31-897d2dea8042
title: Élément isIndexed (schéma du connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f658f6b932f6241b7af84e763d564ca0a8f1b5f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112379"
---
# <a name="isindexed-element-search-connector-schema"></a><span data-ttu-id="02d08-103">Élément isIndexed (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="02d08-103">isIndexed Element (Search Connector Schema)</span></span>

<span data-ttu-id="02d08-104">L’élément booléen facultatif <isIndexed> spécifie si l’emplacement décrit par le connecteur de recherche est indexé (localement ou à distance à l’aide de Windows Search 4 ou version ultérieure).</span><span class="sxs-lookup"><span data-stu-id="02d08-104">The optional Boolean <isIndexed> element specifies whether the location described by the search connector is indexed (either locally or remotely using Windows Search 4 or higher).</span></span> <span data-ttu-id="02d08-105">La valeur par défaut est true pour les dossiers locaux.</span><span class="sxs-lookup"><span data-stu-id="02d08-105">The default value is true for local folders.</span></span> <span data-ttu-id="02d08-106">Cet élément n’a pas d’éléments enfants ni d’attributs.</span><span class="sxs-lookup"><span data-stu-id="02d08-106">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="02d08-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="02d08-107">Syntax</span></span>


```
<!-- isIndexed -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="isIndexed" type="xsIboolean" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="02d08-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="02d08-108">Element Information</span></span>



| <span data-ttu-id="02d08-109">Élément parent</span><span class="sxs-lookup"><span data-stu-id="02d08-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="02d08-110">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="02d08-110">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="02d08-111">Élément searchConnectorDescriptionType (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="02d08-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="example"></a><span data-ttu-id="02d08-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="02d08-112">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <isIndexed>false</isIndexed>
    ...
</searchConnectionDescription>
```



 

 



