---
description: L' <author> élément facultatif spécifie l’auteur de cette bibliothèque. Cet élément n’a pas d’éléments enfants ni d’attributs.
ms.assetid: c91042d5-9564-463a-9104-97b927027fc9
title: auteur, élément (schéma du connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74a2facbf4e3fa743b4dbe56a1c83eb57509c067
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106545777"
---
# <a name="author-element-search-connector-schema"></a><span data-ttu-id="b3c32-104">auteur, élément (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="b3c32-104">author Element (Search Connector Schema)</span></span>

<span data-ttu-id="b3c32-105">L' <author> élément facultatif spécifie l’auteur de cette bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="b3c32-105">The optional <author> element specifies the author of this library.</span></span> <span data-ttu-id="b3c32-106">Cet élément n’a pas d’éléments enfants ni d’attributs.</span><span class="sxs-lookup"><span data-stu-id="b3c32-106">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3c32-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b3c32-107">Syntax</span></span>


```
<!-- author -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="author" type="xs:string" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="b3c32-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="b3c32-108">Element Information</span></span>



| <span data-ttu-id="b3c32-109">Élément parent</span><span class="sxs-lookup"><span data-stu-id="b3c32-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="b3c32-110">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b3c32-110">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="b3c32-111">Élément searchConnectorDescriptionType (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="b3c32-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="example"></a><span data-ttu-id="b3c32-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="b3c32-112">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <author>Joe Smith</author>
    ...
</searchConnectionDescription>
```



 

 



