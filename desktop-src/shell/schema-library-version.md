---
description: L' <version> élément spécifie la version de contenu de cette bibliothèque. Cet élément n’a pas d’attributs ni d’éléments enfants.
ms.assetid: 77FD5EF6-6B6F-48e1-973F-AC069F729613
title: version, élément (schéma de bibliothèque)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7b16a6078a16f4ebbe5e995503114996572f1b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972295"
---
# <a name="version-element-library-schema"></a><span data-ttu-id="a686c-104">version, élément (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="a686c-104">version Element (Library Schema)</span></span>

<span data-ttu-id="a686c-105">L' <version> élément spécifie la version de contenu de cette bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="a686c-105">The <version> element specifies the content version of this library.</span></span> <span data-ttu-id="a686c-106">Cet élément n’a pas d’attributs ni d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="a686c-106">This element has no attributes and no child elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="a686c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a686c-107">Syntax</span></span>

``` syntax
<!-- version -->
<xs:element name="version" type="xs:int" minOccurs="0"/>
```

## <a name="element-information"></a><span data-ttu-id="a686c-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="a686c-108">Element Information</span></span>



| <span data-ttu-id="a686c-109">Élément parent</span><span class="sxs-lookup"><span data-stu-id="a686c-109">Parent Element</span></span>                                                               | <span data-ttu-id="a686c-110">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a686c-110">Child Elements</span></span> |
|------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="a686c-111">Élément libraryDescription (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="a686c-111">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md) | <span data-ttu-id="a686c-112">None</span><span class="sxs-lookup"><span data-stu-id="a686c-112">None</span></span>           |



 

## <a name="remarks"></a><span data-ttu-id="a686c-113">Notes</span><span class="sxs-lookup"><span data-stu-id="a686c-113">Remarks</span></span>

<span data-ttu-id="a686c-114">La version de contenu de la bibliothèque est différente de la version de format de fichier ( \* . Library-ms) de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="a686c-114">The content version of the library is different from the library's file format (\*.library-ms) version.</span></span> <span data-ttu-id="a686c-115">La version du format de fichier de la bibliothèque est spécifiée dans l' [espace de noms](library-schema-entry.md).</span><span class="sxs-lookup"><span data-stu-id="a686c-115">The library's file format version is specified in the [namespace](library-schema-entry.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a686c-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a686c-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a686c-117">Schéma de description de la bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a686c-117">Library Description Schema</span></span>](library-schema-entry.md)
</dt> <dt>

[<span data-ttu-id="a686c-118">Schéma de la description du connecteur de recherche</span><span class="sxs-lookup"><span data-stu-id="a686c-118">Search Connector Description Schema</span></span>](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
