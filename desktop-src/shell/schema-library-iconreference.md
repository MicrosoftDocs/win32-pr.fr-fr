---
description: L' <iconReference> élément spécifie une icône personnalisée pour cette bibliothèque. Cet élément est facultatif et n’a pas d’attributs ni d’éléments enfants.
title: Élément iconReference (schéma de bibliothèque)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 7A35B014-1E01-4da2-AA64-4CFC3436C6D9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 1f307ecd4fa523cc28881164869dca3329dfd698
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991297"
---
# <a name="iconreference-element-library-schema"></a><span data-ttu-id="2287f-104">Élément iconReference (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="2287f-104">iconReference Element (Library Schema)</span></span>

<span data-ttu-id="2287f-105">L' <iconReference> élément spécifie une icône personnalisée pour cette bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="2287f-105">The <iconReference> element specifies a custom icon for this library.</span></span> <span data-ttu-id="2287f-106">Cet élément est facultatif et n’a pas d’attributs ni d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="2287f-106">This element is optional and has no attributes or child elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="2287f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2287f-107">Syntax</span></span>


```
<!-- iconReference -->
    <xs:element name="iconReference" type="xs:string" minOccurs="0"/>
```



## <a name="element-information"></a><span data-ttu-id="2287f-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="2287f-108">Element Information</span></span>



| <span data-ttu-id="2287f-109">Élément parent</span><span class="sxs-lookup"><span data-stu-id="2287f-109">Parent Element</span></span>                                                               | <span data-ttu-id="2287f-110">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="2287f-110">Child Elements</span></span> |
|------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="2287f-111">Élément libraryDescription (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="2287f-111">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="2287f-112">Notes</span><span class="sxs-lookup"><span data-stu-id="2287f-112">Remarks</span></span>

<span data-ttu-id="2287f-113">La référence d’icône doit être spécifiée sous une forme appropriée pour la fonction [**PathParseIconLocation**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathparseiconlocationa) .</span><span class="sxs-lookup"><span data-stu-id="2287f-113">The icon reference must be specified in a form suitable for the [**PathParseIconLocation**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathparseiconlocationa) function.</span></span> <span data-ttu-id="2287f-114">Par exemple : `ModuleFileName,IconResourceIndex`.</span><span class="sxs-lookup"><span data-stu-id="2287f-114">For example: `ModuleFileName,IconResourceIndex`.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2287f-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2287f-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2287f-116">Élément folderType (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="2287f-116">folderType Element (Library Schema)</span></span>](schema-library-foldertype.md)
</dt> <dt>

[<span data-ttu-id="2287f-117">Élément isLibraryPinned (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="2287f-117">isLibraryPinned Element (Library Schema)</span></span>](schema-library-islibrarypinned.md)
</dt> <dt>

[<span data-ttu-id="2287f-118">Élément libraryDescription (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="2287f-118">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md)
</dt> <dt>

[<span data-ttu-id="2287f-119">Élément Name (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="2287f-119">name Element (Library Schema)</span></span>](schema-library-name.md)
</dt> <dt>

[<span data-ttu-id="2287f-120">Élément ownerSID (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="2287f-120">ownerSID Element (Library Schema)</span></span>](schema-library-ownersid.md)
</dt> <dt>

[<span data-ttu-id="2287f-121">Élément propertyStore (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="2287f-121">propertyStore Element (Library Schema)</span></span>](schema-library-propertystore.md)
</dt> <dt>

[<span data-ttu-id="2287f-122">Élément searchConnectorDescription (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="2287f-122">searchConnectorDescription Element (Library Schema)</span></span>](schema-library-searchconnectordescription.md)
</dt> <dt>

[<span data-ttu-id="2287f-123">Élément searchConnectorDescriptionList (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="2287f-123">searchConnectorDescriptionList Element (Library Schema)</span></span>](schema-library-searchconnectordescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="2287f-124">Élément templateInfo (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="2287f-124">templateInfo Element (Library Schema)</span></span>](schema-library-templateinfo.md)
</dt> <dt>

[<span data-ttu-id="2287f-125">version, élément (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="2287f-125">version Element (Library Schema)</span></span>](schema-library-version.md)
</dt> </dl>

 

 



