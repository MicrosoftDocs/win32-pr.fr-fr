---
description: Contient les détails relatifs à une page individuelle dans une note du journal.
ms.assetid: 8cada667-188b-42f9-8602-34e23d512b82
title: Élément JournalPage
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0939194585b067525fa841d6d41674180a40adb9
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432141"
---
# <a name="journalpage-element"></a><span data-ttu-id="2d016-103">Élément JournalPage</span><span class="sxs-lookup"><span data-stu-id="2d016-103">JournalPage Element</span></span>

<span data-ttu-id="2d016-104">Contient les détails relatifs à une page individuelle dans une note du journal.</span><span class="sxs-lookup"><span data-stu-id="2d016-104">Contains the details about an individual page in a Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="2d016-105">Définition</span><span class="sxs-lookup"><span data-stu-id="2d016-105">Definition</span></span>

``` syntax
<xs:element name="JournalPage" type="JournalPageType" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="2d016-106">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="2d016-106">Parent Elements</span></span>

[<span data-ttu-id="2d016-107">**JournalDocument**</span><span class="sxs-lookup"><span data-stu-id="2d016-107">**JournalDocument**</span></span>](journaldocument-element.md)

## <a name="child-elements"></a><span data-ttu-id="2d016-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="2d016-108">Child Elements</span></span>

[<span data-ttu-id="2d016-109">**Stationnaire**</span><span class="sxs-lookup"><span data-stu-id="2d016-109">**Stationary**</span></span>](stationery-element.md)

[<span data-ttu-id="2d016-110">**DocImage**</span><span class="sxs-lookup"><span data-stu-id="2d016-110">**DocImage**</span></span>](docimage-element.md)

[<span data-ttu-id="2d016-111">**TitleInfo**</span><span class="sxs-lookup"><span data-stu-id="2d016-111">**TitleInfo**</span></span>](titleinfo-element.md)

[<span data-ttu-id="2d016-112">**Humidité**</span><span class="sxs-lookup"><span data-stu-id="2d016-112">**Content**</span></span>](content-element--journal-reader.md)

## <a name="attributes"></a><span data-ttu-id="2d016-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="2d016-113">Attributes</span></span>



| <span data-ttu-id="2d016-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="2d016-114">Attribute</span></span>      | <span data-ttu-id="2d016-115">Type</span><span class="sxs-lookup"><span data-stu-id="2d016-115">Type</span></span>                      | <span data-ttu-id="2d016-116">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="2d016-116">Required</span></span> | <span data-ttu-id="2d016-117">Description</span><span class="sxs-lookup"><span data-stu-id="2d016-117">Description</span></span>                                                                        | <span data-ttu-id="2d016-118">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="2d016-118">Possible Values</span></span>                                          |
|----------------|---------------------------|----------|------------------------------------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="2d016-119">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="2d016-119">**Number**</span></span>     | <span data-ttu-id="2d016-120">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="2d016-120">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="2d016-121">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="2d016-121">Required</span></span> | <span data-ttu-id="2d016-122">Numéro ordinal de la page dans le document Journal, commençant par un (1).</span><span class="sxs-lookup"><span data-stu-id="2d016-122">The ordinal number of the page within the Journal document, starting with one (1).</span></span> | <span data-ttu-id="2d016-123">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="2d016-123">Any non-negative integer.</span></span>                                |
| <span data-ttu-id="2d016-124">**Width**</span><span class="sxs-lookup"><span data-stu-id="2d016-124">**Width**</span></span>      | <span data-ttu-id="2d016-125">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="2d016-125">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="2d016-126">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="2d016-126">Required</span></span> | <span data-ttu-id="2d016-127">Largeur de la page.</span><span class="sxs-lookup"><span data-stu-id="2d016-127">The width of the page.</span></span>                                                             | <span data-ttu-id="2d016-128">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="2d016-128">Any non-negative integer.</span></span>                                |
| <span data-ttu-id="2d016-129">**Height**</span><span class="sxs-lookup"><span data-stu-id="2d016-129">**Height**</span></span>     | <span data-ttu-id="2d016-130">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="2d016-130">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="2d016-131">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="2d016-131">Required</span></span> | <span data-ttu-id="2d016-132">Hauteur de la page.</span><span class="sxs-lookup"><span data-stu-id="2d016-132">The height of the page.</span></span>                                                            | <span data-ttu-id="2d016-133">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="2d016-133">Any non-negative integer.</span></span>                                |
| <span data-ttu-id="2d016-134">**LineHeight**</span><span class="sxs-lookup"><span data-stu-id="2d016-134">**LineHeight**</span></span> | <span data-ttu-id="2d016-135">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="2d016-135">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="2d016-136">Facultatif</span><span class="sxs-lookup"><span data-stu-id="2d016-136">Optional</span></span> | <span data-ttu-id="2d016-137">Hauteur de la ligne utilisée sur la page.</span><span class="sxs-lookup"><span data-stu-id="2d016-137">The height of the line used on the page.</span></span>                                           | <span data-ttu-id="2d016-138">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="2d016-138">Any non-negative integer.</span></span>                                |
| <span data-ttu-id="2d016-139">**LanguageId**</span><span class="sxs-lookup"><span data-stu-id="2d016-139">**LanguageId**</span></span> | <span data-ttu-id="2d016-140">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="2d016-140">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="2d016-141">Facultatif</span><span class="sxs-lookup"><span data-stu-id="2d016-141">Optional</span></span> | <span data-ttu-id="2d016-142">ID de langue utilisé pour la page.</span><span class="sxs-lookup"><span data-stu-id="2d016-142">The language id used for the page.</span></span>                                                 | <span data-ttu-id="2d016-143">Entier non négatif représentant un ID de langue valide.</span><span class="sxs-lookup"><span data-stu-id="2d016-143">A non-negative integer representing a valid language id.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="2d016-144">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="2d016-144">Element Information</span></span>



|  <span data-ttu-id="2d016-145">Élément</span><span class="sxs-lookup"><span data-stu-id="2d016-145">Element</span></span>     | <span data-ttu-id="2d016-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d016-146">Value</span></span>                                                     |
|--------------|---------------------------------------------------------------------|
| <span data-ttu-id="2d016-147">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="2d016-147">Element type</span></span> | <span data-ttu-id="2d016-148">ComplexType [**JournalPageType**](journalpagetype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="2d016-148">[**JournalPageType**](journalpagetype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="2d016-149">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2d016-149">Namespace</span></span>    | <span data-ttu-id="2d016-150">urn : schemas-microsoft-com : TabletPC : RichInk</span><span class="sxs-lookup"><span data-stu-id="2d016-150">urn:schemas-microsoft-com:tabletpc:richink</span></span>                          |
| <span data-ttu-id="2d016-151">Nom du schéma</span><span class="sxs-lookup"><span data-stu-id="2d016-151">Schema name</span></span>  | <span data-ttu-id="2d016-152">Lecteur de journal</span><span class="sxs-lookup"><span data-stu-id="2d016-152">Journal Reader</span></span>                                                      |



 

 

 



