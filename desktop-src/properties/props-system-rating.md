---
description: Système d’évaluation qui utilise des valeurs entières comprises entre 1 et 99. Il s’agit du système d’évaluation utilisé par l’interpréteur de commandes Windows Vista.
ms.assetid: a6288d29-1ef3-4da1-bd30-577336ab6817
title: System. Rating
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e411e313f0fa6042a8cbe3a076a7166928020af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106538880"
---
# <a name="systemrating"></a><span data-ttu-id="1dc0c-104">System. Rating</span><span class="sxs-lookup"><span data-stu-id="1dc0c-104">System.Rating</span></span>

<span data-ttu-id="1dc0c-105">Système d’évaluation qui utilise des valeurs entières comprises entre 1 et 99.</span><span class="sxs-lookup"><span data-stu-id="1dc0c-105">A rating system that uses integer values between 1 and 99.</span></span> <span data-ttu-id="1dc0c-106">Il s’agit du système d’évaluation utilisé par l’interpréteur de commandes Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1dc0c-106">This is the rating system used by the Windows Vista Shell.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="1dc0c-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="1dc0c-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Rating
   shellPKey = PKEY_Rating
   formatID = 64440492-4C8B-11D1-8B70-080036B11A03
   propID = 9
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt32
      EnumeratedList
         UseValueForDefault = True
         enumRange
            name = OneStar
            minValue = 1
            setValue = 1
            defineMaxValue = 12
            text = 1 Star
            defineToken = RATING_ONE_STAR
         enumRange
            name = TwoStars
            minValue = 13
            setValue = 25
            defineMaxValue = 37
            text = 2 Stars
            defineToken = RATING_TWO_STARS
         enumRange
            name = ThreeStars
            minValue = 38
            setValue = 50
            defineMaxValue = 62
            text = 3 Stars
            defineToken = RATING_THREE_STARS
         enumRange
            name = FourStars
            minValue = 63
            setValue = 75
            defineMaxValue = 87
            text = 4 Stars
            defineToken = RATING_FOUR_STARS
         enumRange
            name = FiveStars
            minValue = 88
            setValue = 99
            defineMaxValue = 99
            text = 5 Stars
            defineToken = RATING_FIVE_STARS
         enumRange
            name
            minValue = 100
```

## <a name="windows-vista"></a><span data-ttu-id="1dc0c-108">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1dc0c-108">Windows Vista</span></span>

```
propertyDescription
   name = System.Rating
   shellPKey = PKEY_Rating
   formatID = 64440492-4C8B-11D1-8B70-080036B11A03
   propID = 9
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt32
      EnumeratedList
         UseValueForDefault = True
         enumRange
            minValue = 0
            defineMinName = RATING_UNRATED_MIN
            setValue = 0
            defineSetName = RATING_UNRATED_SET
            defineMaxValue = 0
            defineMaxName = RATING_UNRATED_MAX
            text = Unrated
         enumRange
            minValue = 1
            defineMinName = RATING_ONE_STAR_MIN
            setValue = 1
            defineSetName = RATING_ONE_STAR_SET
            defineMaxValue = 12
            defineMaxName = RATING_ONE_STAR_MAX
            text = 1 Star
         enumRange
            minValue = 13
            defineMinName = RATING_TWO_STARS_MIN
            setValue = 25
            defineSetName = RATING_TWO_STARS_SET
            defineMaxValue = 37
            defineMaxName = RATING_TWO_STARS_MAX
            text = 2 Stars
         enumRange
            minValue = 38
            defineMinName = RATING_THREE_STARS_MIN
            setValue = 50
            defineSetName = RATING_THREE_STARS_SET
            defineMaxValue = 62
            defineMaxName = RATING_THREE_STARS_MAX
            text = 3 Stars
         enumRange
            minValue = 63
            defineMinName = RATING_FOUR_STARS_MIN
            setValue = 75
            defineSetName = RATING_FOUR_STARS_SET
            defineMaxValue = 87
            defineMaxName = RATING_FOUR_STARS_MAX
            text = 4 Stars
         enumRange
            minValue = 88
            defineMinName = RATING_FIVE_STARS_MIN
            setValue = 99
            defineSetName = RATING_FIVE_STARS_SET
            defineMaxValue = 99
            defineMaxName = RATING_FIVE_STARS_MAX
            text = 5 Stars
         enumRange
            minValue = 100
```

## <a name="remarks"></a><span data-ttu-id="1dc0c-109">Notes</span><span class="sxs-lookup"><span data-stu-id="1dc0c-109">Remarks</span></span>

<span data-ttu-id="1dc0c-110">Les valeurs de la valeur de l’une sont définies dans propKey. h.</span><span class="sxs-lookup"><span data-stu-id="1dc0c-110">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="1dc0c-111">Pour obtenir une compatibilité avec les systèmes de contrôle d’accès qui utilisent des valeurs comprises entre 1 et 5, consultez la propriété [System. SimpleRating](./props-system-simplerating.md).</span><span class="sxs-lookup"><span data-stu-id="1dc0c-111">For compatibility with ratings systems that use values between 1 and 5, see the property [System.SimpleRating](./props-system-simplerating.md).</span></span> <span data-ttu-id="1dc0c-112">Notez, toutefois, que System. SimpleRating n’est pas utilisé dans l’interpréteur de commandes de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1dc0c-112">Note, however, that System.SimpleRating is not used in the Windows Vista Shell.</span></span>

<span data-ttu-id="1dc0c-113">Le tableau suivant décrit ce que le système d’évaluation par étoile utilisé dans l’interface utilisateur du shell signifie en termes de valeur [System. Rating]() .</span><span class="sxs-lookup"><span data-stu-id="1dc0c-113">The following table describes what the star rating system used in the Shell UI means in terms of the [System.Rating]() value.</span></span>



| <span data-ttu-id="1dc0c-114">System. Rating</span><span class="sxs-lookup"><span data-stu-id="1dc0c-114">System.Rating</span></span> | <span data-ttu-id="1dc0c-115">Nombre d'étoiles</span><span class="sxs-lookup"><span data-stu-id="1dc0c-115">Star Rating</span></span> |
|---------------|-------------|
| <span data-ttu-id="1dc0c-116">1-12</span><span class="sxs-lookup"><span data-stu-id="1dc0c-116">1-12</span></span>          | <span data-ttu-id="1dc0c-117">1 étoile</span><span class="sxs-lookup"><span data-stu-id="1dc0c-117">1 Star</span></span>      |
| <span data-ttu-id="1dc0c-118">13-37</span><span class="sxs-lookup"><span data-stu-id="1dc0c-118">13-37</span></span>         | <span data-ttu-id="1dc0c-119">2 étoiles</span><span class="sxs-lookup"><span data-stu-id="1dc0c-119">2 Stars</span></span>     |
| <span data-ttu-id="1dc0c-120">38-62</span><span class="sxs-lookup"><span data-stu-id="1dc0c-120">38-62</span></span>         | <span data-ttu-id="1dc0c-121">3 étoiles</span><span class="sxs-lookup"><span data-stu-id="1dc0c-121">3 Stars</span></span>     |
| <span data-ttu-id="1dc0c-122">63-87</span><span class="sxs-lookup"><span data-stu-id="1dc0c-122">63-87</span></span>         | <span data-ttu-id="1dc0c-123">4 étoiles</span><span class="sxs-lookup"><span data-stu-id="1dc0c-123">4 Stars</span></span>     |
| <span data-ttu-id="1dc0c-124">88-99</span><span class="sxs-lookup"><span data-stu-id="1dc0c-124">88-99</span></span>         | <span data-ttu-id="1dc0c-125">5 étoiles</span><span class="sxs-lookup"><span data-stu-id="1dc0c-125">5 Stars</span></span>     |



 

<span data-ttu-id="1dc0c-126">Lorsqu’un utilisateur évalue un élément en choisissant une valeur d’évaluation en étoile dans l’interface utilisateur, les valeurs réelles de [System. Rating]() sont affectées comme indiqué dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="1dc0c-126">When a user rates an item by choosing a star rating value in the UI, actual [System.Rating]() values are assigned as shown in this table:</span></span>



| <span data-ttu-id="1dc0c-127">Nombre d'étoiles</span><span class="sxs-lookup"><span data-stu-id="1dc0c-127">Star Rating</span></span> | <span data-ttu-id="1dc0c-128">Valeur assignée via l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="1dc0c-128">Value Assigned Through UI</span></span> |
|-------------|---------------------------|
| <span data-ttu-id="1dc0c-129">1 étoile</span><span class="sxs-lookup"><span data-stu-id="1dc0c-129">1 Star</span></span>      | <span data-ttu-id="1dc0c-130">1</span><span class="sxs-lookup"><span data-stu-id="1dc0c-130">1</span></span>                         |
| <span data-ttu-id="1dc0c-131">2 étoiles</span><span class="sxs-lookup"><span data-stu-id="1dc0c-131">2 Stars</span></span>     | <span data-ttu-id="1dc0c-132">25</span><span class="sxs-lookup"><span data-stu-id="1dc0c-132">25</span></span>                        |
| <span data-ttu-id="1dc0c-133">3 étoiles</span><span class="sxs-lookup"><span data-stu-id="1dc0c-133">3 Stars</span></span>     | <span data-ttu-id="1dc0c-134">50</span><span class="sxs-lookup"><span data-stu-id="1dc0c-134">50</span></span>                        |
| <span data-ttu-id="1dc0c-135">4 étoiles</span><span class="sxs-lookup"><span data-stu-id="1dc0c-135">4 Stars</span></span>     | <span data-ttu-id="1dc0c-136">75</span><span class="sxs-lookup"><span data-stu-id="1dc0c-136">75</span></span>                        |
| <span data-ttu-id="1dc0c-137">5 étoiles</span><span class="sxs-lookup"><span data-stu-id="1dc0c-137">5 Stars</span></span>     | <span data-ttu-id="1dc0c-138">99</span><span class="sxs-lookup"><span data-stu-id="1dc0c-138">99</span></span>                        |



 

<span data-ttu-id="1dc0c-139">Si votre fichier a une valeur [System. SimpleRating](./props-system-simplerating.md) au lieu d’une valeur [System. Rating]() , utilisez le tableau ci-dessous pour convertir et spécifier des valeurs pour System. Rating.</span><span class="sxs-lookup"><span data-stu-id="1dc0c-139">If your file has a [System.SimpleRating](./props-system-simplerating.md) value rather than a [System.Rating]() value, use the table below to convert and specify values for System.Rating.</span></span>



| <span data-ttu-id="1dc0c-140">System. SimpleRating</span><span class="sxs-lookup"><span data-stu-id="1dc0c-140">System.SimpleRating</span></span> | <span data-ttu-id="1dc0c-141">System. Rating</span><span class="sxs-lookup"><span data-stu-id="1dc0c-141">System.Rating</span></span> |
|---------------------|---------------|
| <span data-ttu-id="1dc0c-142">1</span><span class="sxs-lookup"><span data-stu-id="1dc0c-142">1</span></span>                   | <span data-ttu-id="1dc0c-143">1</span><span class="sxs-lookup"><span data-stu-id="1dc0c-143">1</span></span>             |
| <span data-ttu-id="1dc0c-144">2</span><span class="sxs-lookup"><span data-stu-id="1dc0c-144">2</span></span>                   | <span data-ttu-id="1dc0c-145">25</span><span class="sxs-lookup"><span data-stu-id="1dc0c-145">25</span></span>            |
| <span data-ttu-id="1dc0c-146">3</span><span class="sxs-lookup"><span data-stu-id="1dc0c-146">3</span></span>                   | <span data-ttu-id="1dc0c-147">50</span><span class="sxs-lookup"><span data-stu-id="1dc0c-147">50</span></span>            |
| <span data-ttu-id="1dc0c-148">4</span><span class="sxs-lookup"><span data-stu-id="1dc0c-148">4</span></span>                   | <span data-ttu-id="1dc0c-149">75</span><span class="sxs-lookup"><span data-stu-id="1dc0c-149">75</span></span>            |
| <span data-ttu-id="1dc0c-150">5</span><span class="sxs-lookup"><span data-stu-id="1dc0c-150">5</span></span>                   | <span data-ttu-id="1dc0c-151">99</span><span class="sxs-lookup"><span data-stu-id="1dc0c-151">99</span></span>            |



 

<span data-ttu-id="1dc0c-152">Si votre fichier a des valeurs persistantes [System. Rating]() et [System. SimpleRating](./props-system-simplerating.md) , utilisez toujours la valeur System. Rating quand elle est demandée directement, sans référence à System. SimpleRating.</span><span class="sxs-lookup"><span data-stu-id="1dc0c-152">If your file has both [System.Rating]() and [System.SimpleRating](./props-system-simplerating.md) persisted values, always use the System.Rating value when it is directly requested, without reference to System.SimpleRating.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1dc0c-153">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1dc0c-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1dc0c-154">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="1dc0c-154">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="1dc0c-155">searchInfo</span><span class="sxs-lookup"><span data-stu-id="1dc0c-155">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="1dc0c-156">labelInfo</span><span class="sxs-lookup"><span data-stu-id="1dc0c-156">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="1dc0c-157">typeInfo</span><span class="sxs-lookup"><span data-stu-id="1dc0c-157">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="1dc0c-158">displayInfo</span><span class="sxs-lookup"><span data-stu-id="1dc0c-158">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="1dc0c-159">stringFormat</span><span class="sxs-lookup"><span data-stu-id="1dc0c-159">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="1dc0c-160">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="1dc0c-160">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="1dc0c-161">numberFormat</span><span class="sxs-lookup"><span data-stu-id="1dc0c-161">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="1dc0c-162">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="1dc0c-162">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="1dc0c-163">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="1dc0c-163">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="1dc0c-164">drawControl</span><span class="sxs-lookup"><span data-stu-id="1dc0c-164">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="1dc0c-165">editControl</span><span class="sxs-lookup"><span data-stu-id="1dc0c-165">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="1dc0c-166">filterControl</span><span class="sxs-lookup"><span data-stu-id="1dc0c-166">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="1dc0c-167">queryControl</span><span class="sxs-lookup"><span data-stu-id="1dc0c-167">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
