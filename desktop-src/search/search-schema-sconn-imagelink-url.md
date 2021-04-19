---
description: L' <url> élément spécifie une URL vers la miniature pour ce connecteur de recherche. Si <imageLink> existe, cet élément est obligatoire. Elle n’a pas d’éléments enfants ni d’attributs.
ms.assetid: addb2614-9f4f-4cab-a678-b6020b8c4648
title: Élément URL imageLink (schéma du connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c97daaafcbf6336dd4d88c3c92315e656d137b1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513365"
---
# <a name="imagelink-url-element-search-connector-schema"></a><span data-ttu-id="ef91f-105">Élément URL imageLink (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="ef91f-105">imageLink url Element (Search Connector Schema)</span></span>

<span data-ttu-id="ef91f-106">L' <url> élément spécifie une URL vers la miniature pour ce connecteur de recherche.</span><span class="sxs-lookup"><span data-stu-id="ef91f-106">The <url> element specifies a URL to the thumbnail for this search connector.</span></span> <span data-ttu-id="ef91f-107">Si <imageLink> existe, cet élément est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="ef91f-107">If <imageLink> exists, this element is required.</span></span> <span data-ttu-id="ef91f-108">Elle n’a pas d’éléments enfants ni d’attributs.</span><span class="sxs-lookup"><span data-stu-id="ef91f-108">It has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef91f-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ef91f-109">Syntax</span></span>


```
<!-- url -->
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



## <a name="element-information"></a><span data-ttu-id="ef91f-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="ef91f-110">Element Information</span></span>



| <span data-ttu-id="ef91f-111">Élément parent</span><span class="sxs-lookup"><span data-stu-id="ef91f-111">Parent Element</span></span>                                                                   | <span data-ttu-id="ef91f-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ef91f-112">Child Elements</span></span> |
|----------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="ef91f-113">Élément imageLink (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="ef91f-113">imageLink Element (Search Connector Schema)</span></span>](search-schema-sconn-imagelink.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="ef91f-114">Notes</span><span class="sxs-lookup"><span data-stu-id="ef91f-114">Remarks</span></span>

<span data-ttu-id="ef91f-115">La valeur peut être un chemin d’accès au système de fichiers local ou une URL.</span><span class="sxs-lookup"><span data-stu-id="ef91f-115">The value can be a local file system path or a URL.</span></span> <span data-ttu-id="ef91f-116">Le fichier image peut être l’un des types d’images de base pris en charge par Windows 7 (PNG, BMP, JPG, GIF).</span><span class="sxs-lookup"><span data-stu-id="ef91f-116">The image file can be any of the basic image types supported by Windows 7 (PNG, BMP, JPG, GIF).</span></span>

## <a name="example-of-an-imagelinkurl-element"></a><span data-ttu-id="ef91f-117">Exemple d’élément imageLinkurl</span><span class="sxs-lookup"><span data-stu-id="ef91f-117">Example of an imageLinkurl Element</span></span>


```
<imageLink>
    <imageLinkurl>%ProgramFiles%\Example\examplethumbnail.jpg</imageLinkurl>
</imageLink>
```



 

 



