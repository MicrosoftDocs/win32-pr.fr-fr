---
description: Contient les détails relatifs à une page individuelle dans une note du journal.
ms.assetid: 8cada667-188b-42f9-8602-34e23d512b82
title: Élément JournalPage
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e7223818de8200f2ff7748edd7eb472f49e92e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866774"
---
# <a name="journalpage-element"></a><span data-ttu-id="e6637-103">Élément JournalPage</span><span class="sxs-lookup"><span data-stu-id="e6637-103">JournalPage Element</span></span>

<span data-ttu-id="e6637-104">Contient les détails relatifs à une page individuelle dans une note du journal.</span><span class="sxs-lookup"><span data-stu-id="e6637-104">Contains the details about an individual page in a Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="e6637-105">Définition</span><span class="sxs-lookup"><span data-stu-id="e6637-105">Definition</span></span>

``` syntax
<xs:element name="JournalPage" type="JournalPageType" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="e6637-106">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="e6637-106">Parent Elements</span></span>

[<span data-ttu-id="e6637-107">**JournalDocument**</span><span class="sxs-lookup"><span data-stu-id="e6637-107">**JournalDocument**</span></span>](journaldocument-element.md)

## <a name="child-elements"></a><span data-ttu-id="e6637-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="e6637-108">Child Elements</span></span>

[<span data-ttu-id="e6637-109">**Stationnaire**</span><span class="sxs-lookup"><span data-stu-id="e6637-109">**Stationary**</span></span>](stationery-element.md)

[<span data-ttu-id="e6637-110">**DocImage**</span><span class="sxs-lookup"><span data-stu-id="e6637-110">**DocImage**</span></span>](docimage-element.md)

[<span data-ttu-id="e6637-111">**TitleInfo**</span><span class="sxs-lookup"><span data-stu-id="e6637-111">**TitleInfo**</span></span>](titleinfo-element.md)

[<span data-ttu-id="e6637-112">**Content**</span><span class="sxs-lookup"><span data-stu-id="e6637-112">**Content**</span></span>](content-element--journal-reader.md)

## <a name="attributes"></a><span data-ttu-id="e6637-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="e6637-113">Attributes</span></span>



| <span data-ttu-id="e6637-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="e6637-114">Attribute</span></span>      | <span data-ttu-id="e6637-115">Type</span><span class="sxs-lookup"><span data-stu-id="e6637-115">Type</span></span>                      | <span data-ttu-id="e6637-116">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="e6637-116">Required</span></span> | <span data-ttu-id="e6637-117">Description</span><span class="sxs-lookup"><span data-stu-id="e6637-117">Description</span></span>                                                                        | <span data-ttu-id="e6637-118">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="e6637-118">Possible Values</span></span>                                          |
|----------------|---------------------------|----------|------------------------------------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="e6637-119">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="e6637-119">**Number**</span></span>     | <span data-ttu-id="e6637-120">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="e6637-120">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="e6637-121">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="e6637-121">Required</span></span> | <span data-ttu-id="e6637-122">Numéro ordinal de la page dans le document Journal, commençant par un (1).</span><span class="sxs-lookup"><span data-stu-id="e6637-122">The ordinal number of the page within the Journal document, starting with one (1).</span></span> | <span data-ttu-id="e6637-123">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="e6637-123">Any non-negative integer.</span></span>                                |
| <span data-ttu-id="e6637-124">**Width**</span><span class="sxs-lookup"><span data-stu-id="e6637-124">**Width**</span></span>      | <span data-ttu-id="e6637-125">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="e6637-125">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="e6637-126">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="e6637-126">Required</span></span> | <span data-ttu-id="e6637-127">Largeur de la page.</span><span class="sxs-lookup"><span data-stu-id="e6637-127">The width of the page.</span></span>                                                             | <span data-ttu-id="e6637-128">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="e6637-128">Any non-negative integer.</span></span>                                |
| <span data-ttu-id="e6637-129">**Height**</span><span class="sxs-lookup"><span data-stu-id="e6637-129">**Height**</span></span>     | <span data-ttu-id="e6637-130">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="e6637-130">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="e6637-131">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="e6637-131">Required</span></span> | <span data-ttu-id="e6637-132">Hauteur de la page.</span><span class="sxs-lookup"><span data-stu-id="e6637-132">The height of the page.</span></span>                                                            | <span data-ttu-id="e6637-133">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="e6637-133">Any non-negative integer.</span></span>                                |
| <span data-ttu-id="e6637-134">**LineHeight**</span><span class="sxs-lookup"><span data-stu-id="e6637-134">**LineHeight**</span></span> | <span data-ttu-id="e6637-135">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="e6637-135">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="e6637-136">Facultatif</span><span class="sxs-lookup"><span data-stu-id="e6637-136">Optional</span></span> | <span data-ttu-id="e6637-137">Hauteur de la ligne utilisée sur la page.</span><span class="sxs-lookup"><span data-stu-id="e6637-137">The height of the line used on the page.</span></span>                                           | <span data-ttu-id="e6637-138">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="e6637-138">Any non-negative integer.</span></span>                                |
| <span data-ttu-id="e6637-139">**LanguageId**</span><span class="sxs-lookup"><span data-stu-id="e6637-139">**LanguageId**</span></span> | <span data-ttu-id="e6637-140">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="e6637-140">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="e6637-141">Facultatif</span><span class="sxs-lookup"><span data-stu-id="e6637-141">Optional</span></span> | <span data-ttu-id="e6637-142">ID de langue utilisé pour la page.</span><span class="sxs-lookup"><span data-stu-id="e6637-142">The language id used for the page.</span></span>                                                 | <span data-ttu-id="e6637-143">Entier non négatif représentant un ID de langue valide.</span><span class="sxs-lookup"><span data-stu-id="e6637-143">A non-negative integer representing a valid language id.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="e6637-144">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="e6637-144">Element Information</span></span>



|              |                                                                     |
|--------------|---------------------------------------------------------------------|
| <span data-ttu-id="e6637-145">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="e6637-145">Element type</span></span> | <span data-ttu-id="e6637-146">ComplexType [**JournalPageType**](journalpagetype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="e6637-146">[**JournalPageType**](journalpagetype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="e6637-147">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e6637-147">Namespace</span></span>    | <span data-ttu-id="e6637-148">urn : schemas-microsoft-com : TabletPC : RichInk</span><span class="sxs-lookup"><span data-stu-id="e6637-148">urn:schemas-microsoft-com:tabletpc:richink</span></span>                          |
| <span data-ttu-id="e6637-149">Nom du schéma</span><span class="sxs-lookup"><span data-stu-id="e6637-149">Schema name</span></span>  | <span data-ttu-id="e6637-150">Lecteur de journal</span><span class="sxs-lookup"><span data-stu-id="e6637-150">Journal Reader</span></span>                                                      |



 

 

 



