---
description: L' <scopeItem> élément représente une entrée unique dans la table d’étendue d’exclusion/d’inclusion.
ms.assetid: 18a58b3b-771c-4829-b3d4-253383b4bee8
title: Élément scopeItem (schéma du connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c2033202be6d904880ec9c4efa1c60db4bb7e50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112375"
---
# <a name="scopeitem-element-search-connector-schema"></a><span data-ttu-id="cebba-103">Élément scopeItem (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="cebba-103">scopeItem Element (Search Connector Schema)</span></span>

<span data-ttu-id="cebba-104">L' <scopeItem> élément représente une entrée unique dans la table d’étendue d’exclusion/d’inclusion.</span><span class="sxs-lookup"><span data-stu-id="cebba-104">The <scopeItem> element represents a single entry in the exclusion/inclusion scope table.</span></span> <span data-ttu-id="cebba-105"><scopeItem> étend le type shellLinkType standard en ajoutant trois nouveaux éléments qui contrôlent l’inclusion et l’exclusion de dossiers, contrôlent la profondeur des résultats et spécifient l’emplacement de l’étendue.</span><span class="sxs-lookup"><span data-stu-id="cebba-105"><scopeItem> extends the standard shellLinkType type by adding three new elements that control inclusion and exclusion of folders, control the depth of results, and specify the location of the scope.</span></span> <span data-ttu-id="cebba-106">Si l' <scope> élément existe, cet élément est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="cebba-106">If the <scope> element exists, this element is required.</span></span> <span data-ttu-id="cebba-107">Il a trois éléments enfants et aucun attribut.</span><span class="sxs-lookup"><span data-stu-id="cebba-107">It has three child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="cebba-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cebba-108">Syntax</span></span>


```
<!-- scopeItem -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="scope" minOccurs="0">
            <xs:complexType>
                <xs:sequence minOccurs="0">
                    <xs:element name="scopeItem" maxOccurs="unbounded">
                        <xs:complexType>
                            <xs:all>
                                <xs:element name="mode" default="Include">
                                    ...
                                </xs:element>
                                <xs:element name="depth" default="Shallow" minOccurs="0">
                                    ...
                                </xs:element>
                                <xs:element name="url" type="xs:anyURI"/>
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



## <a name="element-information"></a><span data-ttu-id="cebba-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="cebba-109">Element Information</span></span>



| <span data-ttu-id="cebba-110">Élément parent</span><span class="sxs-lookup"><span data-stu-id="cebba-110">Parent Element</span></span>                                                           | <span data-ttu-id="cebba-111">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="cebba-111">Child Elements</span></span>                                                                        |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="cebba-112">Élément Scope (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="cebba-112">scope Element (Search Connector Schema)</span></span>](search-schema-sconn-scope.md) | <span data-ttu-id="cebba-113">[élément Scope (schéma du connecteur de recherche)](search-schema-sconn-scope-mode.md).</span><span class="sxs-lookup"><span data-stu-id="cebba-113">[scope Element (Search Connector Schema)](search-schema-sconn-scope-mode.md).</span></span>        |
|                                                                          | <span data-ttu-id="cebba-114">[élément Scope (schéma du connecteur de recherche)](search-schema-sconn-scope-depth.md).</span><span class="sxs-lookup"><span data-stu-id="cebba-114">[scope Element (Search Connector Schema)](search-schema-sconn-scope-depth.md).</span></span>       |
|                                                                          | <span data-ttu-id="cebba-115">[élément URL scopeItem (schéma du connecteur de recherche)](search-schema-sconn-scope-url.md).</span><span class="sxs-lookup"><span data-stu-id="cebba-115">[scopeItem url Element (Search Connector Schema)](search-schema-sconn-scope-url.md).</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="cebba-116">Notes</span><span class="sxs-lookup"><span data-stu-id="cebba-116">Remarks</span></span>

<span data-ttu-id="cebba-117">Utilisez les <scope> <scopeItem> éléments et pour identifier les emplacements à rechercher et les emplacements qui doivent être exclus de la recherche.</span><span class="sxs-lookup"><span data-stu-id="cebba-117">Use the <scope> and <scopeItem> elements to identify which locations should be searched and which locations should be excluded from searching.</span></span>

## <a name="example"></a><span data-ttu-id="cebba-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="cebba-118">Example</span></span>

<span data-ttu-id="cebba-119">L’exemple suivant montre une étendue de recherche qui comprend C : \\ ExampleFolder et tous ses dossiers enfants, à l’exception de c : \\ ExampleFolder \\ ExcludeMe.</span><span class="sxs-lookup"><span data-stu-id="cebba-119">The following example shows a search scope that includes C:\\ExampleFolder and all its child folders except C:\\ExampleFolder\\ExcludeMe.</span></span>


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



 

 



