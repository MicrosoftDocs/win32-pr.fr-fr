---
description: L' <imageLink> élément facultatif spécifie une miniature pour ce connecteur de recherche. Cet élément a un élément enfant obligatoire et aucun attribut.
ms.assetid: 71078d83-72f4-41f9-b80c-7ba0139206fb
title: Élément imageLink (schéma du connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d84b2e5cbbfc8bbd98557ebd0405a09cf998e6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513188"
---
# <a name="imagelink-element-search-connector-schema"></a><span data-ttu-id="72fbe-104">Élément imageLink (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="72fbe-104">imageLink Element (Search Connector Schema)</span></span>

<span data-ttu-id="72fbe-105">L' <imageLink> élément facultatif spécifie une miniature pour ce connecteur de recherche.</span><span class="sxs-lookup"><span data-stu-id="72fbe-105">The optional <imageLink> element specifies a thumbnail for this search connector.</span></span> <span data-ttu-id="72fbe-106">Cet élément a un élément enfant obligatoire et aucun attribut.</span><span class="sxs-lookup"><span data-stu-id="72fbe-106">This element has one mandatory child element and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="72fbe-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="72fbe-107">Syntax</span></span>


```
<!-- imageLink -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="imageLink" minOccurs="0">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="url" type="xs:anyURI"/>
                    </xs:sequence>
                </xs:complexType>
            </xs:element>            
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="72fbe-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="72fbe-108">Element Information</span></span>



| <span data-ttu-id="72fbe-109">Élément parent</span><span class="sxs-lookup"><span data-stu-id="72fbe-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="72fbe-110">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="72fbe-110">Child Elements</span></span>                                                                           |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="72fbe-111">Élément searchConnectorDescriptionType (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="72fbe-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) | [<span data-ttu-id="72fbe-112">Élément URL imageLink (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="72fbe-112">imageLink url Element (Search Connector Schema)</span></span>](search-schema-sconn-imagelink-url.md) |



 

## <a name="remarks"></a><span data-ttu-id="72fbe-113">Notes</span><span class="sxs-lookup"><span data-stu-id="72fbe-113">Remarks</span></span>

<span data-ttu-id="72fbe-114">La valeur imageLink peut être un chemin d’accès au système de fichiers local ou une URL.</span><span class="sxs-lookup"><span data-stu-id="72fbe-114">The imageLink value can be a local file system path or a URL.</span></span> <span data-ttu-id="72fbe-115">Le fichier image peut être l’un des types d’images de base pris en charge par Windows 7 (PNG, BMP, JPG, GIF).</span><span class="sxs-lookup"><span data-stu-id="72fbe-115">The image file can be any of the basic image types supported by Windows 7 (PNG, BMP, JPG, GIF).</span></span>

## <a name="example-of-an-imagelink-element"></a><span data-ttu-id="72fbe-116">Exemple d’élément imageLink</span><span class="sxs-lookup"><span data-stu-id="72fbe-116">Example of an imageLink Element</span></span>


```
<imageLink>
    <imageLinkurl>%ProgramFiles%\Example\examplethumbnail.jpg</imageLinkurl>
</imageLink>
```



 

 



