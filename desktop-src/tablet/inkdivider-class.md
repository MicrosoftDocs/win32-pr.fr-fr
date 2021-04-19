---
description: Représente la capacité à analyser la disposition d’une collection de traits et à les diviser en texte et en graphiques.
ms.assetid: 2c8e67fb-1032-4fcc-b419-82bae978daf8
title: InkDivider, classe (Msinkaut15. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkDivider
- InkDivider.IInkDivider
api_type:
- COM
api_location:
- Inkdiv.dll
- Inkdiv.dll.dll
ms.openlocfilehash: c0658504303968803bd2abff063694701d121390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536401"
---
# <a name="inkdivider-class"></a><span data-ttu-id="0a752-103">InkDivider, classe</span><span class="sxs-lookup"><span data-stu-id="0a752-103">InkDivider class</span></span>

<span data-ttu-id="0a752-104">Représente la capacité à analyser la disposition d’une collection de traits et à les diviser en texte et en graphiques.</span><span class="sxs-lookup"><span data-stu-id="0a752-104">Represents the ability to analyze the layout of a collection of strokes and divide them into text and graphics.</span></span>

<span data-ttu-id="0a752-105">**InkDivider** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0a752-105">**InkDivider** has these types of members:</span></span>

-   [<span data-ttu-id="0a752-106">Interfaces</span><span class="sxs-lookup"><span data-stu-id="0a752-106">Interfaces</span></span>](#interfaces)
-   [<span data-ttu-id="0a752-107">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0a752-107">Methods</span></span>](#methods)
-   [<span data-ttu-id="0a752-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0a752-108">Properties</span></span>](#properties)

### <a name="interfaces"></a><span data-ttu-id="0a752-109">Interfaces</span><span class="sxs-lookup"><span data-stu-id="0a752-109">Interfaces</span></span>

<span data-ttu-id="0a752-110">La classe **InkDivider** définit ces interfaces.</span><span class="sxs-lookup"><span data-stu-id="0a752-110">The **InkDivider** class defines these interfaces.</span></span>



| <span data-ttu-id="0a752-111">Interface</span><span class="sxs-lookup"><span data-stu-id="0a752-111">Interface</span></span>       | <span data-ttu-id="0a752-112">Description</span><span class="sxs-lookup"><span data-stu-id="0a752-112">Description</span></span>                                                          |
|:----------------|:---------------------------------------------------------------------|
| <span data-ttu-id="0a752-113">**IInkDivider**</span><span class="sxs-lookup"><span data-stu-id="0a752-113">**IInkDivider**</span></span> | <span data-ttu-id="0a752-114">Cet objet implémente l’interface com **IInkDivider** .</span><span class="sxs-lookup"><span data-stu-id="0a752-114">This object implements the **IInkDivider** COM interface.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="0a752-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0a752-115">Methods</span></span>

<span data-ttu-id="0a752-116">La classe **InkDivider** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="0a752-116">The **InkDivider** class has these methods.</span></span>



| <span data-ttu-id="0a752-117">Méthode</span><span class="sxs-lookup"><span data-stu-id="0a752-117">Method</span></span>                              | <span data-ttu-id="0a752-118">Description</span><span class="sxs-lookup"><span data-stu-id="0a752-118">Description</span></span>                                                                                                                                                        |
|:------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0a752-119">**Diviser**</span><span class="sxs-lookup"><span data-stu-id="0a752-119">**Divide**</span></span>](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-divide) | <span data-ttu-id="0a752-120">Retourne un objet [**IInkDivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) qui contient des informations structurelles sur les traits de l’objet **InkDivider** .</span><span class="sxs-lookup"><span data-stu-id="0a752-120">Returns an [**IInkDivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) object that contains structural information about the strokes in the **InkDivider** object.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="0a752-121">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0a752-121">Properties</span></span>

<span data-ttu-id="0a752-122">La classe **InkDivider** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="0a752-122">The **InkDivider** class has these properties.</span></span>



| <span data-ttu-id="0a752-123">Propriété</span><span class="sxs-lookup"><span data-stu-id="0a752-123">Property</span></span>                                                             | <span data-ttu-id="0a752-124">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="0a752-124">Access type</span></span>           | <span data-ttu-id="0a752-125">Description</span><span class="sxs-lookup"><span data-stu-id="0a752-125">Description</span></span>                                                                                                                     |
|:---------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0a752-126">**LineHeight**</span><span class="sxs-lookup"><span data-stu-id="0a752-126">**LineHeight**</span></span>](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight)<br/>               | <span data-ttu-id="0a752-127">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0a752-127">Read/write</span></span><br/> | <span data-ttu-id="0a752-128">Obtient ou définit la hauteur attendue de l’écriture manuscrite en unités HIMETRIC.</span><span class="sxs-lookup"><span data-stu-id="0a752-128">Gets or sets the expected handwriting height in HIMETRIC units.</span></span><br/>                                                      |
| [<span data-ttu-id="0a752-129">**RecognizerContext**</span><span class="sxs-lookup"><span data-stu-id="0a752-129">**RecognizerContext**</span></span>](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext)<br/> | <span data-ttu-id="0a752-130">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0a752-130">Read/write</span></span><br/> | <span data-ttu-id="0a752-131">Obtient ou définit l’objet [**InkRecognizerContext**](inkrecognizercontext-class.md) utilisé pour la reconnaissance de l’écriture manuscrite.</span><span class="sxs-lookup"><span data-stu-id="0a752-131">Gets or sets the [**InkRecognizerContext**](inkrecognizercontext-class.md) object used for handwriting recognition.</span></span><br/> |
| [<span data-ttu-id="0a752-132">**Traits**</span><span class="sxs-lookup"><span data-stu-id="0a752-132">**Strokes**</span></span>](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes)<br/>                     | <span data-ttu-id="0a752-133">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0a752-133">Read/write</span></span><br/> | <span data-ttu-id="0a752-134">Obtient ou définit la collection [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) contenue par l’objet **InkDivider** .</span><span class="sxs-lookup"><span data-stu-id="0a752-134">Gets or sets the [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection contained by the **InkDivider** object.</span></span> <br/>     |



 

## <a name="remarks"></a><span data-ttu-id="0a752-135">Notes</span><span class="sxs-lookup"><span data-stu-id="0a752-135">Remarks</span></span>

<span data-ttu-id="0a752-136">Cet objet peut être instancié en appelant la méthode [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) en C++.</span><span class="sxs-lookup"><span data-stu-id="0a752-136">This object can be instantiated by calling the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) method in C++.</span></span>

<span data-ttu-id="0a752-137">L’objet **InkDivider** utilise la disposition des traits, l’ordre dans lequel les traits sont ajoutés, la direction dans laquelle les traits sont dessinés et d’autres facteurs pour effectuer l’analyse de l’encre.</span><span class="sxs-lookup"><span data-stu-id="0a752-137">The **InkDivider** object uses the layout of the strokes, the order in which the strokes are added, the direction in which the strokes are drawn, and other factors to perform the analysis of the ink.</span></span> <span data-ttu-id="0a752-138">La collection [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) analysée par l’objet **InkDivider** est contenue dans la propriété [**Strokes**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes) de l’objet **InkDivider** .</span><span class="sxs-lookup"><span data-stu-id="0a752-138">The [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection that the **InkDivider** object analyzes is contained in the [**Strokes**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes) property of the **InkDivider** object.</span></span> <span data-ttu-id="0a752-139">L’objet **InkDivider** analyse dynamiquement la collection InkStrokes à mesure que vous ajoutez ou supprimez la collection, mais il n’effectue aucune modification des traits.</span><span class="sxs-lookup"><span data-stu-id="0a752-139">The **InkDivider** object dynamically analyzes the InkStrokes collection as you add to or delete from the collection, but it performs no modification of the strokes.</span></span>

<span data-ttu-id="0a752-140">Les résultats de l’analyse sont retournés dans un objet [**IInkDivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) .</span><span class="sxs-lookup"><span data-stu-id="0a752-140">The analysis results are returned in an [**IInkDivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) object.</span></span>

<span data-ttu-id="0a752-141">L’objet **InkDivider** utilise un objet [**InkRecognizerContext**](inkrecognizercontext-class.md) pour diviser plus précisément les traits et assigner une chaîne de reconnaissance aux résultats.</span><span class="sxs-lookup"><span data-stu-id="0a752-141">The **InkDivider** object uses an [**InkRecognizerContext**](inkrecognizercontext-class.md) object to more accurately divide the strokes and to assign a recognition string to the results.</span></span>

> [!Note]  
> <span data-ttu-id="0a752-142">L’objet **InkDivider** utilise les paramètres de propriété par défaut de l’objet [**InkRecognizerContext**](inkrecognizercontext-class.md) .</span><span class="sxs-lookup"><span data-stu-id="0a752-142">The **InkDivider** object uses the default property settings of the [**InkRecognizerContext**](inkrecognizercontext-class.md) object.</span></span>

 

<span data-ttu-id="0a752-143">Si vous n’assignez pas de contexte de module de reconnaissance à l’objet **InkDivider** , l’objet **InkDivider** analyse toujours l’encre, mais divise les traits moins précisément et n’associe pas de texte aux résultats de la Division.</span><span class="sxs-lookup"><span data-stu-id="0a752-143">If you do not assign a recognizer context to the **InkDivider** object, the **InkDivider** object still analyzes the ink, but it divides the strokes less accurately and does not associate text with the division results.</span></span>

> [!Note]  
> <span data-ttu-id="0a752-144">La propriété [**RecognizerContext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) doit être définie avant l’ajout de traits à la propriété [**Strokes**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes) .</span><span class="sxs-lookup"><span data-stu-id="0a752-144">The [**RecognizerContext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) property should be set before adding strokes to the [**Strokes**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes) property.</span></span> <span data-ttu-id="0a752-145">Une fois que les traits ont été ajoutés à l’objet **InkDivider** , la propriété **RecognizerContext** ne peut pas être modifiée.</span><span class="sxs-lookup"><span data-stu-id="0a752-145">After strokes have been added to the **InkDivider** object, the **RecognizerContext** property cannot be changed.</span></span>

 

<span data-ttu-id="0a752-146">Le **InkDivider** ne prend pas actuellement en charge les langues verticales.</span><span class="sxs-lookup"><span data-stu-id="0a752-146">The **InkDivider** does not currently support vertical languages.</span></span> <span data-ttu-id="0a752-147">Pour que l’objet **InkDivider** reconnaisse ces langues correctement, l’objet [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) de la langue doit prendre en charge la fonctionnalité d’entrée gratuite et les caractères doivent être écrits de gauche à droite.</span><span class="sxs-lookup"><span data-stu-id="0a752-147">For the **InkDivider** object to recognize these languages properly the [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) object for the language must support the free input capability and the characters must be written from left to right.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a752-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0a752-148">Requirements</span></span>



| <span data-ttu-id="0a752-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0a752-149">Requirement</span></span> | <span data-ttu-id="0a752-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="0a752-150">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a752-151">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0a752-151">Minimum supported client</span></span><br/> | <span data-ttu-id="0a752-152">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0a752-152">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0a752-153">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0a752-153">Minimum supported server</span></span><br/> | <span data-ttu-id="0a752-154">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="0a752-154">None supported</span></span><br/>                                                                                               |
| <span data-ttu-id="0a752-155">En-tête</span><span class="sxs-lookup"><span data-stu-id="0a752-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a752-156"><dt>Msinkaut15. h (nécessite également Msinkaut15 \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="0a752-156"><dt>Msinkaut15.h (also requires Msinkaut15\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="0a752-157">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0a752-157">Library</span></span><br/>                  | <dl> <span data-ttu-id="0a752-158"><dt>Inkdiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a752-158"><dt>Inkdiv.dll</dt></span></span> </dl>                                   |



## <a name="see-also"></a><span data-ttu-id="0a752-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a752-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a752-160">**Interface IInkDivisionResult**</span><span class="sxs-lookup"><span data-stu-id="0a752-160">**IInkDivisionResult Interface**</span></span>](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult)
</dt> <dt>

[<span data-ttu-id="0a752-161">**InkRecognizerContext, classe**</span><span class="sxs-lookup"><span data-stu-id="0a752-161">**InkRecognizerContext Class**</span></span>](inkrecognizercontext-class.md)
</dt> <dt>

<span data-ttu-id="0a752-162">[Collection InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0a752-162">[InkStrokes Collection](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span></span>
</dt> </dl>

 

