---
description: L' <depth> élément spécifie si la portée du connecteur de recherche doit inclure des URL enfants. Les valeurs autorisées sont Deep et Shallow. Cet élément n’a pas d’éléments enfants ni d’attributs.
ms.assetid: 859decab-cbe3-4cec-b37c-6d0e7c353876
title: Élément Depth (schéma du connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf68bcbc96b6d1beb2c381f0a17532272b8d397e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951028"
---
# <a name="depth-element-search-connector-schema"></a><span data-ttu-id="898ec-105">Élément Depth (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="898ec-105">depth Element (Search Connector Schema)</span></span>

<span data-ttu-id="898ec-106">L' <depth> élément spécifie si la portée du connecteur de recherche doit inclure des URL enfants.</span><span class="sxs-lookup"><span data-stu-id="898ec-106">The <depth> element specifies whether the search connector's scope should include child URLs.</span></span> <span data-ttu-id="898ec-107">Les valeurs autorisées sont `Deep` et `Shallow`.</span><span class="sxs-lookup"><span data-stu-id="898ec-107">The allowed values are `Deep` and `Shallow`.</span></span> <span data-ttu-id="898ec-108">Cet élément n’a pas d’éléments enfants ni d’attributs.</span><span class="sxs-lookup"><span data-stu-id="898ec-108">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="898ec-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="898ec-109">Syntax</span></span>


```
<!-- depth -->
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
                                <xs:element name="depth" default="Shallow" minOccurs="0">
                                    <xs:simpleType>
                                        <xs:restriction base="xs:string">
                                            <xs:enumeration value="Shallow"/>
                                            <xs:enumeration value="Deep"/>
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



## <a name="element-information"></a><span data-ttu-id="898ec-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="898ec-110">Element Information</span></span>



| <span data-ttu-id="898ec-111">Élément parent</span><span class="sxs-lookup"><span data-stu-id="898ec-111">Parent Element</span></span>                                                                   | <span data-ttu-id="898ec-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="898ec-112">Child Elements</span></span> |
|----------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="898ec-113">Élément scopeItem (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="898ec-113">scopeItem Element (Search Connector Schema)</span></span>](search-schema-sconn-scopeitem.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="898ec-114">Notes</span><span class="sxs-lookup"><span data-stu-id="898ec-114">Remarks</span></span>

<span data-ttu-id="898ec-115">Si la profondeur est profonde, les utilisateurs peuvent parcourir ou Rechercher des éléments dans le niveau d’URL de scopeItem ou dans des URL enfants.</span><span class="sxs-lookup"><span data-stu-id="898ec-115">If the depth is deep, users can browse or search items in the scopeItem's URL level or within any child URLs.</span></span>

## <a name="example"></a><span data-ttu-id="898ec-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="898ec-116">Example</span></span>

<span data-ttu-id="898ec-117">L’exemple suivant montre une étendue de recherche qui comprend C : \\ dossier et tous ses dossiers enfants et c : \\ FolderB, mais aucun de ses dossiers enfants.</span><span class="sxs-lookup"><span data-stu-id="898ec-117">The following example shows a search scope that includes C:\\FolderA and all its child folders and C:\\FolderB but none of its child folders.</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <scope>
        <scopeItem>
            <mode>Include</mode>
            <depth>Deep</depth>
            <url>C:\FolderA</url>
        </scopeItem>
        <scopeItem>
            <mode>Include</mode>
            <depth>Shallow</depth>
            <url>C:\FolderB</url>
        </scopeItem>
    </scope>
    ...
</searchConnectionDescription>
```



 

 



