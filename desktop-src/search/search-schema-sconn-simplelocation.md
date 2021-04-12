---
description: L' <simpleLocation> élément spécifie l’emplacement des connecteurs de recherche qui sont basés sur un système de fichiers ou un gestionnaire de protocole. Cet élément a deux éléments enfants et aucun attribut.
ms.assetid: 04ffc178-0a76-4870-a075-a2ecd31937a1
title: Élément simpleLocation (schéma du connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d12c17ace36314ceb180f14b6de0eb7a890a385b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318137"
---
# <a name="simplelocation-element-search-connector-schema"></a><span data-ttu-id="fb4bc-104">Élément simpleLocation (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="fb4bc-104">simpleLocation Element (Search Connector Schema)</span></span>

<span data-ttu-id="fb4bc-105">L' <simpleLocation> élément spécifie l’emplacement des connecteurs de recherche qui sont basés sur un système de fichiers ou un gestionnaire de protocole.</span><span class="sxs-lookup"><span data-stu-id="fb4bc-105">The <simpleLocation> element specifies the location for search connectors that are file-system based or protocol-handler based.</span></span> <span data-ttu-id="fb4bc-106">Cet élément a deux éléments enfants et aucun attribut.</span><span class="sxs-lookup"><span data-stu-id="fb4bc-106">This element has two child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb4bc-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fb4bc-107">Syntax</span></span>


```
<!-- simpleLocation -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="simpleLocation" type="shellLinkType" minOccurs="0">
                <xs:all>
                    <xs:element name="url" type="xs:anyURI"/>
                    <xs:element name="serialized" minOccurs="0"/>
                </xs:all>
                
            </xs:element>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="fb4bc-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="fb4bc-108">Element Information</span></span>



| <span data-ttu-id="fb4bc-109">Élément parent</span><span class="sxs-lookup"><span data-stu-id="fb4bc-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="fb4bc-110">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="fb4bc-110">Child Elements</span></span>                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fb4bc-111">Élément searchConnectorDescriptionType (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="fb4bc-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) | [<span data-ttu-id="fb4bc-112">Élément URL simpleLocation (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="fb4bc-112">simpleLocation url Element (Search Connector Schema)</span></span>](search-schema-sconn-url.md)                                                                                                                                                                                                                                |
|                                                                                                                  | <span data-ttu-id="fb4bc-113">sérialisé : cet élément contient les ShellLink encodés en base64 pointant vers l’emplacement défini dans l' <url> élément.</span><span class="sxs-lookup"><span data-stu-id="fb4bc-113">serialized: This element contains the base64-encoded ShellLink pointing to the location defined in the <url> element.</span></span> <span data-ttu-id="fb4bc-114">Windows 7 crée le ShellLink à partir de la valeur de l' <url> élément et met à jour correctement ce champ sur la première charge de cette bibliothèque. il doit donc rester vide par l’auteur.</span><span class="sxs-lookup"><span data-stu-id="fb4bc-114">Windows 7 creates the ShellLink from the value of the <url> element and properly updates this field on the first load of this library, so it should be left empty by the author.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="fb4bc-115">Notes</span><span class="sxs-lookup"><span data-stu-id="fb4bc-115">Remarks</span></span>

<span data-ttu-id="fb4bc-116">Cet élément peut être utilisé à la place de <locationProvider> lorsque l’emplacement est sur le système de fichiers ou que le connecteur est un gestionnaire de protocole connu (comme MAPI :).</span><span class="sxs-lookup"><span data-stu-id="fb4bc-116">This element can be used instead of <locationProvider> when the location is on the file system or the connector is a known protocol handler (like mapi:).</span></span> <span data-ttu-id="fb4bc-117">Si <simpleLocation> est présent, il ne doit pas s’agir d’un <locationProvider> élément.</span><span class="sxs-lookup"><span data-stu-id="fb4bc-117">If <simpleLocation> is present, there MUST NOT be a <locationProvider> element.</span></span> <span data-ttu-id="fb4bc-118">Pour les connecteurs de recherche de fournisseur de services Web, utilisez à la [<locationProvider>](search-schema-sconn-locationprovider.md) place l’élément.</span><span class="sxs-lookup"><span data-stu-id="fb4bc-118">For web service provider search connectors, use the [<locationProvider>](search-schema-sconn-locationprovider.md) element instead.</span></span>

## <a name="examples"></a><span data-ttu-id="fb4bc-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="fb4bc-119">Examples</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <simpleLocation>
        <url>mapi://{S-1-5-21-2127521184-1604012920-1887927527-2779359}/</url>
    </simpleLocation>
    ...
</searchConnectionDescription>
```



 

 



