---
description: L' <templateInfo> élément est un conteneur pour l’élément FolderType, qui spécifie un type de dossier pour afficher les résultats d’une requête sur cette bibliothèque. Cet élément est facultatif et n’a pas d’attributs.
ms.assetid: C555097A-E7B8-45ef-8CFA-19CFBC5E9D5A
title: Élément templateInfo (schéma de bibliothèque)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dae06a57a1b30407e2513e03f30ae6a4da13e849
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527304"
---
# <a name="templateinfo-element-library-schema"></a><span data-ttu-id="43861-104">Élément templateInfo (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="43861-104">templateInfo Element (Library Schema)</span></span>

<span data-ttu-id="43861-105">L' <templateInfo> élément est un conteneur pour l’élément [FolderType](schema-library-foldertype.md) , qui spécifie un type de dossier pour afficher les résultats d’une requête sur cette bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="43861-105">The <templateInfo> element is a container for the [folderType](schema-library-foldertype.md) element, which specifies a folder type for displaying the results from a query over this library.</span></span> <span data-ttu-id="43861-106">Cet élément est facultatif et n’a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="43861-106">This element is optional and has no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="43861-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="43861-107">Syntax</span></span>

``` syntax
<!-- templateInfo -->
<xs:element name="templateInfo" minOccurs="0">
    <xs:complexType>
        <xs:all>
            <xs:element name="folderType" minOccurs="0"/>
        </xs:all>
    </xs:complexType>
</xs:element>
```

## <a name="element-information"></a><span data-ttu-id="43861-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="43861-108">Element Information</span></span>



| <span data-ttu-id="43861-109">Élément parent</span><span class="sxs-lookup"><span data-stu-id="43861-109">Parent Element</span></span>                                                               | <span data-ttu-id="43861-110">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="43861-110">Child Elements</span></span>                                                             |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="43861-111">Élément libraryDescription (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="43861-111">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md) | [<span data-ttu-id="43861-112">Élément folderType (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="43861-112">folderType Element (Library Schema)</span></span>](schema-library-foldertype.md)       |
|                                                                              | [<span data-ttu-id="43861-113">Élément propertyStore (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="43861-113">propertyStore Element (Library Schema)</span></span>](schema-library-propertystore.md) |



 

## <a name="related-topics"></a><span data-ttu-id="43861-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="43861-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43861-115">Schéma de description de la bibliothèque</span><span class="sxs-lookup"><span data-stu-id="43861-115">Library Description Schema</span></span>](library-schema-entry.md)
</dt> <dt>

<span data-ttu-id="43861-116">[Schéma de la description du connecteur de recherche](/previous-versions//dd743009(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="43861-116">[Search Connector Description Schema](/previous-versions//dd743009(v=vs.85))</span></span>
</dt> </dl>

 

 
