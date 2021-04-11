---
description: L' <url> élément spécifie une URL qui représente la portée du connecteur de recherche. Cet élément n’a pas d’éléments enfants ni d’attributs.
ms.assetid: 5afd84aa-98e3-4118-845a-d4efad19a488
title: Élément URL scopeItem (schéma du connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c573308fe406fe4500f6bb8e88b3762fa0bbac05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862142"
---
# <a name="scopeitem-url-element-search-connector-schema"></a><span data-ttu-id="f272c-104">Élément URL scopeItem (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="f272c-104">scopeItem url Element (Search Connector Schema)</span></span>

<span data-ttu-id="f272c-105">L' <url> élément spécifie une URL qui représente la portée du connecteur de recherche.</span><span class="sxs-lookup"><span data-stu-id="f272c-105">The <url> element specifies a URL that represents the scope of the search connector.</span></span> <span data-ttu-id="f272c-106">Cet élément n’a pas d’éléments enfants ni d’attributs.</span><span class="sxs-lookup"><span data-stu-id="f272c-106">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="f272c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f272c-107">Syntax</span></span>


```
<!-- url -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="scope" minOccurs="0">
            <xs:complexType>
                <xs:sequence minOccurs="0"><xs:all>
                    <xs:element name="scopeItem" maxOccurs="unbounded">
                        <xs:complexType>
                            <xs:all>
                                ...
                                <xs:element name="url" type="xs:anyURI"/>
                            </xs:all>
                        </xs:complexType>
                    </xs:element>
                </xs:sequence></xs:all>
            </xs:complexType>
        </xs:element>
        ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="f272c-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="f272c-108">Element Information</span></span>



| <span data-ttu-id="f272c-109">Élément parent</span><span class="sxs-lookup"><span data-stu-id="f272c-109">Parent Element</span></span>                                                                   | <span data-ttu-id="f272c-110">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="f272c-110">Child Elements</span></span> |
|----------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="f272c-111">Élément scopeItem (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="f272c-111">scopeItem Element (Search Connector Schema)</span></span>](search-schema-sconn-scopeitem.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="f272c-112">Notes</span><span class="sxs-lookup"><span data-stu-id="f272c-112">Remarks</span></span>

<span data-ttu-id="f272c-113">La valeur peut être un chemin d’accès au système de fichiers local ou une URL.</span><span class="sxs-lookup"><span data-stu-id="f272c-113">The value can be a local file system path or a URL.</span></span>

## <a name="example"></a><span data-ttu-id="f272c-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="f272c-114">Example</span></span>

<span data-ttu-id="f272c-115">L’exemple suivant montre une étendue de recherche qui comprend C : \\ ExampleFolder et tous ses dossiers enfants, à l’exception de c : \\ ExampleFolder \\ ExcludeMe.</span><span class="sxs-lookup"><span data-stu-id="f272c-115">The following example shows a search scope that includes C:\\ExampleFolder and all its child folders except C:\\ExampleFolder\\ExcludeMe.</span></span>


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
            <mode>Exclude</mode>
            <depth>Deep</depth>
            <url>C:\ExampleFolder\ExcludeMe</url>
        </scopeItem>
    </scope>
    ...
</searchConnectionDescription>
```



 

 



