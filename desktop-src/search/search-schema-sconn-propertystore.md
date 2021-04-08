---
description: L' <propertyStore> élément facultatif spécifie l’emplacement d’un IPropertyStore basé sur XML pour stocker les métadonnées ouvertes pour ce connecteur de recherche. Cet élément n’a pas d’attributs et un seul élément enfant.
ms.assetid: 5720c69f-af87-432b-857c-dbd66ba74e80
title: Élément propertyStore (schéma du connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11f8cda6457de764b00519a81a1134e7eecc8638
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750332"
---
# <a name="propertystore-element-search-connector-schema"></a><span data-ttu-id="21efd-104">Élément propertyStore (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="21efd-104">propertyStore Element (Search Connector Schema)</span></span>

<span data-ttu-id="21efd-105">L' <propertyStore> élément facultatif spécifie l’emplacement d’un IPropertyStore basé sur XML pour stocker les métadonnées ouvertes pour ce connecteur de recherche.</span><span class="sxs-lookup"><span data-stu-id="21efd-105">The optional <propertyStore> element specifies the location of an XML-based IPropertyStore to store open metadata for this search connector.</span></span> <span data-ttu-id="21efd-106">Cet élément n’a pas d’attributs et un seul élément enfant.</span><span class="sxs-lookup"><span data-stu-id="21efd-106">This element has no attributes and only one child element.</span></span>

## <a name="syntax"></a><span data-ttu-id="21efd-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="21efd-107">Syntax</span></span>


```
<!-- propertyStore -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="propertyStore" type="propertyStoreType" minOccurs="0">
            <xs:element name="property" minOccurs="0" maxOccurrs="unbounded"/>
        </xs:element>
        ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="21efd-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="21efd-108">Element Information</span></span>



| <span data-ttu-id="21efd-109">Élément parent</span><span class="sxs-lookup"><span data-stu-id="21efd-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="21efd-110">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="21efd-110">Child Elements</span></span>                                                                                            |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="21efd-111">Élément searchConnectorDescriptionType (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="21efd-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) | [<span data-ttu-id="21efd-112">Élément Property de propertyStore (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="21efd-112">property Element of propertyStore (Search Connector Schema)</span></span>](search-schema-sconn-propstore-property.md) |



 

## <a name="example"></a><span data-ttu-id="21efd-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="21efd-113">Example</span></span>

<span data-ttu-id="21efd-114">L’exemple suivant illustre un <propertyStore> élément avec deux <property> éléments.</span><span class="sxs-lookup"><span data-stu-id="21efd-114">The following example shows a <propertyStore> element with two <property> elements.</span></span>


```
<propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://www.adventureworks.com/Search/?Query={searchTerms}</property>
    <property name="isExternal" type="boolean">true</property>
</propertyStore>
```



 

 



