---
description: Représente la zone utilisée par le module de reconnaissance dans laquelle l’encre peut être dessinée. La zone est appelée Guide de reconnaissance.
ms.assetid: c4990aa5-8c8b-4206-8376-b5c0d0c8e0a7
title: InkRecognizerGuide, classe (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkRecognizerGuide
- InkRecognizerGuide.IInkRecognizerGuide
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 55729513f748afc87f184b73eaba976184307bc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210826"
---
# <a name="inkrecognizerguide-class"></a><span data-ttu-id="a30e7-104">InkRecognizerGuide, classe</span><span class="sxs-lookup"><span data-stu-id="a30e7-104">InkRecognizerGuide class</span></span>

<span data-ttu-id="a30e7-105">Représente la zone utilisée par le module de reconnaissance dans laquelle l’encre peut être dessinée.</span><span class="sxs-lookup"><span data-stu-id="a30e7-105">Represents the area that the recognizer uses in which ink can be drawn.</span></span> <span data-ttu-id="a30e7-106">La zone est appelée Guide de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="a30e7-106">The area is known as the recognition guide.</span></span>

<span data-ttu-id="a30e7-107">**InkRecognizerGuide** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a30e7-107">**InkRecognizerGuide** has these types of members:</span></span>

-   [<span data-ttu-id="a30e7-108">Interfaces</span><span class="sxs-lookup"><span data-stu-id="a30e7-108">Interfaces</span></span>](#interfaces)
-   [<span data-ttu-id="a30e7-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a30e7-109">Properties</span></span>](#properties)

### <a name="interfaces"></a><span data-ttu-id="a30e7-110">Interfaces</span><span class="sxs-lookup"><span data-stu-id="a30e7-110">Interfaces</span></span>

<span data-ttu-id="a30e7-111">La classe **InkRecognizerGuide** définit ces interfaces.</span><span class="sxs-lookup"><span data-stu-id="a30e7-111">The **InkRecognizerGuide** class defines these interfaces.</span></span>



| <span data-ttu-id="a30e7-112">Interface</span><span class="sxs-lookup"><span data-stu-id="a30e7-112">Interface</span></span>               | <span data-ttu-id="a30e7-113">Description</span><span class="sxs-lookup"><span data-stu-id="a30e7-113">Description</span></span>                                                                  |
|:------------------------|:-----------------------------------------------------------------------------|
| <span data-ttu-id="a30e7-114">**IInkRecognizerGuide**</span><span class="sxs-lookup"><span data-stu-id="a30e7-114">**IInkRecognizerGuide**</span></span> | <span data-ttu-id="a30e7-115">Cet objet implémente l’interface com **IInkRecognizerGuide** .</span><span class="sxs-lookup"><span data-stu-id="a30e7-115">This object implements the **IInkRecognizerGuide** COM interface.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a30e7-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a30e7-116">Properties</span></span>

<span data-ttu-id="a30e7-117">La classe **InkRecognizerGuide** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="a30e7-117">The **InkRecognizerGuide** class has these properties.</span></span>



| <span data-ttu-id="a30e7-118">Propriété</span><span class="sxs-lookup"><span data-stu-id="a30e7-118">Property</span></span>                                                       | <span data-ttu-id="a30e7-119">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="a30e7-119">Access type</span></span>           | <span data-ttu-id="a30e7-120">Description</span><span class="sxs-lookup"><span data-stu-id="a30e7-120">Description</span></span>                                                                                                                    |
|:---------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a30e7-121">**Colonnes**</span><span class="sxs-lookup"><span data-stu-id="a30e7-121">**Columns**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_columns)<br/>       | <span data-ttu-id="a30e7-122">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a30e7-122">Read/write</span></span><br/> | <span data-ttu-id="a30e7-123">Obtient ou définit le nombre de colonnes dans la zone du repère.</span><span class="sxs-lookup"><span data-stu-id="a30e7-123">Gets or sets the number of columns in the guide box.</span></span><br/>                                                                |
| [<span data-ttu-id="a30e7-124">**DrawnBox**</span><span class="sxs-lookup"><span data-stu-id="a30e7-124">**DrawnBox**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_drawnbox)<br/>     | <span data-ttu-id="a30e7-125">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a30e7-125">Read/write</span></span><br/> | <span data-ttu-id="a30e7-126">Obtient ou définit la zone qui est physiquement dessinée sur l’écran de la tablette et dans laquelle l’écriture a lieu.</span><span class="sxs-lookup"><span data-stu-id="a30e7-126">Gets or sets the box that is physically drawn on the tablet's screen and in which writing takes place.</span></span><br/>              |
| [<span data-ttu-id="a30e7-127">**GuideData**</span><span class="sxs-lookup"><span data-stu-id="a30e7-127">**GuideData**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_guidedata)<br/>   | <span data-ttu-id="a30e7-128">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a30e7-128">Read/write</span></span><br/> | <span data-ttu-id="a30e7-129">Obtient ou définit les données de guide pour les développeurs C++.</span><span class="sxs-lookup"><span data-stu-id="a30e7-129">Gets or sets guide data for C++ developers.</span></span><br/>                                                                         |
| [<span data-ttu-id="a30e7-130">**Médian**</span><span class="sxs-lookup"><span data-stu-id="a30e7-130">**Midline**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_midline)<br/>       | <span data-ttu-id="a30e7-131">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a30e7-131">Read/write</span></span><br/> | <span data-ttu-id="a30e7-132">Obtient ou définit la hauteur de la médiane.</span><span class="sxs-lookup"><span data-stu-id="a30e7-132">Gets or sets the midline height.</span></span> <span data-ttu-id="a30e7-133">La hauteur de la ligne médiane est la distance entre la ligne de base et la ligne médiane de la zone dessinée.</span><span class="sxs-lookup"><span data-stu-id="a30e7-133">The midline height is distance from the baseline to the midline, of the drawn box.</span></span><br/> |
| [<span data-ttu-id="a30e7-134">**Lignes**</span><span class="sxs-lookup"><span data-stu-id="a30e7-134">**Rows**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_rows)<br/>             | <span data-ttu-id="a30e7-135">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a30e7-135">Read/write</span></span><br/> | <span data-ttu-id="a30e7-136">Obtient ou définit le nombre de lignes dans la zone du repère.</span><span class="sxs-lookup"><span data-stu-id="a30e7-136">Gets or sets the number of rows in the guide box.</span></span><br/>                                                                   |
| [<span data-ttu-id="a30e7-137">**WritingBox**</span><span class="sxs-lookup"><span data-stu-id="a30e7-137">**WritingBox**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_writingbox)<br/> | <span data-ttu-id="a30e7-138">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a30e7-138">Read/write</span></span><br/> | <span data-ttu-id="a30e7-139">Obtient ou définit la zone d’écriture invisible de la zone de repère dans laquelle l’écriture peut avoir lieu.</span><span class="sxs-lookup"><span data-stu-id="a30e7-139">Gets or sets the invisible writing area of the guide box in which writing can actually take place.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="a30e7-140">Notes</span><span class="sxs-lookup"><span data-stu-id="a30e7-140">Remarks</span></span>

<span data-ttu-id="a30e7-141">Cet objet peut être instancié en appelant la méthode [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) .</span><span class="sxs-lookup"><span data-stu-id="a30e7-141">This object can be instantiated by calling the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) method.</span></span>

<span data-ttu-id="a30e7-142">Par défaut, il n’existe aucun guide de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="a30e7-142">By default, there is no recognizer guide.</span></span> <span data-ttu-id="a30e7-143">Toutes les valeurs de propriété d’un repère par défaut sont définies sur 0.</span><span class="sxs-lookup"><span data-stu-id="a30e7-143">A default guide has all property values set to 0.</span></span> <span data-ttu-id="a30e7-144">Vous devez utiliser les propriétés de cet objet pour définir le repère.</span><span class="sxs-lookup"><span data-stu-id="a30e7-144">You must use the properties of this object to set the guide.</span></span>

<span data-ttu-id="a30e7-145">Si l’application a dessiné des instructions à l’écran sur lequel l’utilisateur est censé écrire, l’application doit définir les valeurs des propriétés du Guide de reconnaissance pour informer le module de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="a30e7-145">If the application has drawn guidelines on the screen on which the user is expected to write, the application should set the values of the properties of the recognizer guide to inform the recognizer.</span></span> <span data-ttu-id="a30e7-146">Ces propriétés sont réservées à l’utilisation du module de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="a30e7-146">These properties are for the recognizer's use only.</span></span> <span data-ttu-id="a30e7-147">Leur définition ne fait pas, en soi, des indices visuels à l’écran.</span><span class="sxs-lookup"><span data-stu-id="a30e7-147">Setting them does not, by itself, draw visual clues on the display.</span></span> <span data-ttu-id="a30e7-148">L’application ou le contrôle dessine les indices visuels.</span><span class="sxs-lookup"><span data-stu-id="a30e7-148">The application or the control draws the visual clues.</span></span>

<span data-ttu-id="a30e7-149">Le Guide de reconnaissance peut se composer de lignes et de colonnes, et ceux-ci donnent au module de reconnaissance un meilleur contexte dans lequel effectuer la reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="a30e7-149">The recognizer guide can consist of rows and columns, and these give the recognizer a better context in which to perform recognition.</span></span> <span data-ttu-id="a30e7-150">Les lettres telles que « t » et « I » sont plus facilement reconnues lorsqu’un guide est utilisé pour fournir le contexte à l’encre.</span><span class="sxs-lookup"><span data-stu-id="a30e7-150">Letters such as "t" and "I" are more easily recognized when a guide is used to give context to the ink.</span></span> <span data-ttu-id="a30e7-151">Par exemple, vous pouvez dessiner des lignes horizontales sur un écran, qui indiquent où l’écriture doit se produire (ce type de repère se compose uniquement de lignes et pas de colonnes).</span><span class="sxs-lookup"><span data-stu-id="a30e7-151">For example, you can draw horizontal lines on a screen, that show where writing should occur (this type of guide would consist only of rows, and no columns).</span></span> <span data-ttu-id="a30e7-152">En écrivant sur les lignes, au lieu d’un espace arbitraire, la précision de la reconnaissance est améliorée.</span><span class="sxs-lookup"><span data-stu-id="a30e7-152">By writing on the lines, instead of some arbitrary space, recognition accuracy improves.</span></span>

<span data-ttu-id="a30e7-153">Le repère spécifie les limites de l’encre dans les coordonnées de l’espace d’encre.</span><span class="sxs-lookup"><span data-stu-id="a30e7-153">The guide specifies the boundaries of the ink in ink space coordinates.</span></span>

<span data-ttu-id="a30e7-154">La propriété [**DrawnBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_drawnbox) peut définir une zone de taille inférieure ou égale à la zone définie par la propriété [**WritingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_writingbox) .</span><span class="sxs-lookup"><span data-stu-id="a30e7-154">The [**DrawnBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_drawnbox) property can define a box which is the same size as or smaller than the box defined by the [**WritingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_writingbox) property.</span></span>

<span data-ttu-id="a30e7-155">L’illustration suivante montre les éléments d’un guide de reconnaissance avec deux lignes et aucune colonne.</span><span class="sxs-lookup"><span data-stu-id="a30e7-155">The following figure shows the elements of a recognizer guide with two rows and no columns.</span></span>

![Illustration montrant des éléments du Guide de reconnaissance](images/927cc2f3-549f-4279-aab9-bd5ade070eaf.jpg)

<span data-ttu-id="a30e7-157">En plus de dessiner des lignes sur l’écran qui indiquent aux utilisateurs où écrire, vous pouvez dessiner des cellules à l’écran dans lesquelles des caractères ou des mots sont écrits.</span><span class="sxs-lookup"><span data-stu-id="a30e7-157">In addition to drawing lines on the screen that show users where to write, you can draw cells on the screen in which characters or words are written.</span></span> <span data-ttu-id="a30e7-158">C’est ce que l’on appelle une entrée boxed et est utile avec certaines langues asiatiques.</span><span class="sxs-lookup"><span data-stu-id="a30e7-158">This is called boxed input and is useful with some Asian languages.</span></span> <span data-ttu-id="a30e7-159">Pour déterminer si le module de reconnaissance est apte à l’entrée boxed, appelez la propriété [**Capabilities**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities) de l’objet [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) .</span><span class="sxs-lookup"><span data-stu-id="a30e7-159">To determine if the recognizer is capable of boxed input, call the [**Capabilities**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities) property of the [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) object.</span></span>

<span data-ttu-id="a30e7-160">L’illustration suivante montre un guide de reconnaissance avec quatre colonnes.</span><span class="sxs-lookup"><span data-stu-id="a30e7-160">The following figure shows a recognizer guide with four columns.</span></span>

![illustration illustrant le Guide de reconnaissance avec quatre colonnes](images/de44c07e-4b55-42d0-8e8b-997e2da79e52.jpg)

## <a name="requirements"></a><span data-ttu-id="a30e7-162">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a30e7-162">Requirements</span></span>



| <span data-ttu-id="a30e7-163">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a30e7-163">Requirement</span></span> | <span data-ttu-id="a30e7-164">Valeur</span><span class="sxs-lookup"><span data-stu-id="a30e7-164">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a30e7-165">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a30e7-165">Minimum supported client</span></span><br/> | <span data-ttu-id="a30e7-166">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a30e7-166">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="a30e7-167">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a30e7-167">Minimum supported server</span></span><br/> | <span data-ttu-id="a30e7-168">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a30e7-168">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="a30e7-169">En-tête</span><span class="sxs-lookup"><span data-stu-id="a30e7-169">Header</span></span><br/>                   | <dl> <span data-ttu-id="a30e7-170"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a30e7-170"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a30e7-171">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a30e7-171">Library</span></span><br/>                  | <dl> <span data-ttu-id="a30e7-172"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a30e7-172"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="a30e7-173">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a30e7-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a30e7-174">**Interface IInkRecognizer**</span><span class="sxs-lookup"><span data-stu-id="a30e7-174">**IInkRecognizer Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer)
</dt> <dt>

[<span data-ttu-id="a30e7-175">**InkRecognizerContext, classe**</span><span class="sxs-lookup"><span data-stu-id="a30e7-175">**InkRecognizerContext Class**</span></span>](inkrecognizercontext-class.md)
</dt> </dl>

 

