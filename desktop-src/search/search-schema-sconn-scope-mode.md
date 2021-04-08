---
description: L' <mode> élément spécifie si l’URL doit être incluse ou exclue de l’étendue du connecteur de recherche. Les valeurs autorisées sont include et Exclude. Cet élément n’a pas d’éléments enfants ni d’attributs.
ms.assetid: 7654c04a-31c4-4260-a51c-0600804e62a9
title: mode, élément (schéma du connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec8c09b4c6de138e6e390d2c31a82fe5d1f56566
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750325"
---
# <a name="mode-element-search-connector-schema"></a><span data-ttu-id="5ff70-105">mode, élément (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="5ff70-105">mode Element (Search Connector Schema)</span></span>

<span data-ttu-id="5ff70-106">L' <mode> élément spécifie si l’URL doit être incluse ou exclue de l’étendue du connecteur de recherche.</span><span class="sxs-lookup"><span data-stu-id="5ff70-106">The <mode> element specifies whether the URL should be included or excluded from the scope of the search connector.</span></span> <span data-ttu-id="5ff70-107">Les valeurs autorisées sont `Include` et `Exclude`.</span><span class="sxs-lookup"><span data-stu-id="5ff70-107">The allowed values are `Include` and `Exclude`.</span></span> <span data-ttu-id="5ff70-108">Cet élément n’a pas d’éléments enfants ni d’attributs.</span><span class="sxs-lookup"><span data-stu-id="5ff70-108">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ff70-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5ff70-109">Syntax</span></span>


```
<!-- mode -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="scope" minOccurs="0">
            <xs:complexType>
                <xs:sequence minOccurs="0">
                    <xs:element name="scopeItem" maxOccurs="unbounded">
                        <xs:complexType>
                            <xs:all>
                                ...
                                <xs:element name="mode" default="Include">
                                    <xs:simpleType>
                                        <xs:restriction base="xs:string">
                                            <xs:enumeration value="Include"/>
                                            <xs:enumeration value="Exclude"/>
                                        </xs:restriction>
                                    </xs:simpleType>
                                </xs:element>
                                ...
                            </xs:all>
                        </xs:complexType>
                    </xs:element>
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="5ff70-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="5ff70-110">Element Information</span></span>



| <span data-ttu-id="5ff70-111">Élément parent</span><span class="sxs-lookup"><span data-stu-id="5ff70-111">Parent Element</span></span>                                                                   | <span data-ttu-id="5ff70-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="5ff70-112">Child Elements</span></span> |
|----------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="5ff70-113">Élément scopeItem (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="5ff70-113">scopeItem Element (Search Connector Schema)</span></span>](search-schema-sconn-scopeitem.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="5ff70-114">Notes</span><span class="sxs-lookup"><span data-stu-id="5ff70-114">Remarks</span></span>

<span data-ttu-id="5ff70-115">Une étendue exclue ne peut pas être recherchée ou parcourue.</span><span class="sxs-lookup"><span data-stu-id="5ff70-115">An excluded scope cannot be searched or browsed.</span></span> <span data-ttu-id="5ff70-116">Vous pouvez imbriquer des URL scopeItem.</span><span class="sxs-lookup"><span data-stu-id="5ff70-116">You can nest scopeItem URLs.</span></span> <span data-ttu-id="5ff70-117">Par exemple, vous pouvez inclure une étendue parente et tous ses enfants à l’exception d’un en ajoutant l’URL parente telle qu’elle est incluse, avec une valeur de profondeur de profondeur et en excluant l’URL enfant.</span><span class="sxs-lookup"><span data-stu-id="5ff70-117">For example, you can include a parent scope and all its children except one by adding the parent URL as included, with depth value of Deep, and excluding the child URL.</span></span>

## <a name="example"></a><span data-ttu-id="5ff70-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="5ff70-118">Example</span></span>

<span data-ttu-id="5ff70-119">L’exemple suivant montre une étendue de recherche qui comprend C : \\ ExampleFolder et tous ses dossiers enfants, à l’exception de c : \\ ExampleFolder \\ ExcludeMe.</span><span class="sxs-lookup"><span data-stu-id="5ff70-119">The following example shows a search scope that includes C:\\ExampleFolder and all its child folders except C:\\ExampleFolder\\ExcludeMe.</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <scope>
        <scopeItem>
            <mode>Include</mode>
            <depth>Deep</depth>
            <url>C:\ExampleFolder</url>
        </scopeItem>
        <scopeItem>
            <mode>Include</mode>
            <depth>Shallow</depth>
            <url>C:\ExampleFolder\ExcludeMe</url>
        </scopeItem>
    </scope>
    ...
</searchConnectionDescription>
```



 

 



