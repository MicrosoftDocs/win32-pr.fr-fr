---
description: Représente les traits d’encre collectés dans un espace d’encre.
ms.assetid: f942d6a3-f303-49df-a128-de9760b508ef
title: InkDisp, classe (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkDisp
- InkDisp.IInkDisp
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 429cbf85bdc92753cda1e58a0e89086b4b5b8b53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750212"
---
# <a name="inkdisp-class"></a><span data-ttu-id="ef765-103">InkDisp, classe</span><span class="sxs-lookup"><span data-stu-id="ef765-103">InkDisp class</span></span>

<span data-ttu-id="ef765-104">Représente les traits d’encre collectés dans un espace d’encre.</span><span class="sxs-lookup"><span data-stu-id="ef765-104">Represents the collected strokes of ink within an ink space.</span></span>

<span data-ttu-id="ef765-105">**InkDisp** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ef765-105">**InkDisp** has these types of members:</span></span>

-   [<span data-ttu-id="ef765-106">Événements</span><span class="sxs-lookup"><span data-stu-id="ef765-106">Events</span></span>](#events)
-   [<span data-ttu-id="ef765-107">Interfaces</span><span class="sxs-lookup"><span data-stu-id="ef765-107">Interfaces</span></span>](#interfaces)
-   [<span data-ttu-id="ef765-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ef765-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="ef765-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ef765-109">Properties</span></span>](#properties)

### <a name="events"></a><span data-ttu-id="ef765-110">Événements</span><span class="sxs-lookup"><span data-stu-id="ef765-110">Events</span></span>

<span data-ttu-id="ef765-111">La classe **InkDisp** contient ces événements.</span><span class="sxs-lookup"><span data-stu-id="ef765-111">The **InkDisp** class has these events.</span></span>



| <span data-ttu-id="ef765-112">Événement</span><span class="sxs-lookup"><span data-stu-id="ef765-112">Event</span></span>                                    | <span data-ttu-id="ef765-113">Description</span><span class="sxs-lookup"><span data-stu-id="ef765-113">Description</span></span>                                                             |
|:-----------------------------------------|:------------------------------------------------------------------------|
| [<span data-ttu-id="ef765-114">**InkAdded**</span><span class="sxs-lookup"><span data-stu-id="ef765-114">**InkAdded**</span></span>](inkdisp-inkadded.md)     | <span data-ttu-id="ef765-115">Se produit lorsqu’un trait est ajouté à l’objet **InkDisp** .</span><span class="sxs-lookup"><span data-stu-id="ef765-115">Occurs when a stroke is added to the **InkDisp** object.</span></span><br/>     |
| [<span data-ttu-id="ef765-116">**InkDeleted**</span><span class="sxs-lookup"><span data-stu-id="ef765-116">**InkDeleted**</span></span>](inkdisp-inkdeleted.md) | <span data-ttu-id="ef765-117">Se produit lorsqu’un trait est supprimé de l’objet **InkDisp** .</span><span class="sxs-lookup"><span data-stu-id="ef765-117">Occurs when a stroke is deleted from the **InkDisp** object.</span></span><br/> |



 

### <a name="interfaces"></a><span data-ttu-id="ef765-118">Interfaces</span><span class="sxs-lookup"><span data-stu-id="ef765-118">Interfaces</span></span>

<span data-ttu-id="ef765-119">La classe **InkDisp** définit ces interfaces.</span><span class="sxs-lookup"><span data-stu-id="ef765-119">The **InkDisp** class defines these interfaces.</span></span>



| <span data-ttu-id="ef765-120">Interface</span><span class="sxs-lookup"><span data-stu-id="ef765-120">Interface</span></span>    | <span data-ttu-id="ef765-121">Description</span><span class="sxs-lookup"><span data-stu-id="ef765-121">Description</span></span>                                                       |
|:-------------|:------------------------------------------------------------------|
| <span data-ttu-id="ef765-122">**IInkDisp**</span><span class="sxs-lookup"><span data-stu-id="ef765-122">**IInkDisp**</span></span> | <span data-ttu-id="ef765-123">Cet objet implémente l’interface com **IInkDisp** .</span><span class="sxs-lookup"><span data-stu-id="ef765-123">This object implements the **IInkDisp** COM interface.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="ef765-124">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ef765-124">Methods</span></span>

<span data-ttu-id="ef765-125">La classe **InkDisp** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="ef765-125">The **InkDisp** class has these methods.</span></span>



| <span data-ttu-id="ef765-126">Méthode</span><span class="sxs-lookup"><span data-stu-id="ef765-126">Method</span></span>                                                                   | <span data-ttu-id="ef765-127">Description</span><span class="sxs-lookup"><span data-stu-id="ef765-127">Description</span></span>                                                                                                                                                                                          |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ef765-128">**AddStrokesAtRectangle**</span><span class="sxs-lookup"><span data-stu-id="ef765-128">**AddStrokesAtRectangle**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-addstrokesatrectangle)           | <span data-ttu-id="ef765-129">Insère une collection de traits dans l’objet **InkDisp** au niveau du rectangle spécifié.</span><span class="sxs-lookup"><span data-stu-id="ef765-129">Inserts a stroke collection into the **InkDisp** object at the specified rectangle.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="ef765-130">**CanPaste**</span><span class="sxs-lookup"><span data-stu-id="ef765-130">**CanPaste**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-canpaste)                                     | <span data-ttu-id="ef765-131">Indique si [**IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject) peut être converti en objet **InkDisp** .</span><span class="sxs-lookup"><span data-stu-id="ef765-131">Indicates whether the [**IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject) can be converted to an **InkDisp** object.</span></span><br/>                                                                                       |
| [<span data-ttu-id="ef765-132">**Capture**</span><span class="sxs-lookup"><span data-stu-id="ef765-132">**Clip**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-clip)                                      | <span data-ttu-id="ef765-133">Supprime des parties d’un trait ou d’une collection de traits situés à l’extérieur d’un rectangle.</span><span class="sxs-lookup"><span data-stu-id="ef765-133">Removes portions of a stroke or collection of strokes that are outside a rectangle.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="ef765-134">**ClipboardCopy**</span><span class="sxs-lookup"><span data-stu-id="ef765-134">**ClipboardCopy**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopy)                           | <span data-ttu-id="ef765-135">Copie la collection [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) dans le presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="ef765-135">Copies the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection to the Clipboard.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="ef765-136">**ClipboardCopyWithRectangle**</span><span class="sxs-lookup"><span data-stu-id="ef765-136">**ClipboardCopyWithRectangle**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopywithrectangle) | <span data-ttu-id="ef765-137">Copie les objets [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) contenus dans le rectangle connu dans le presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="ef765-137">Copies the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects that are contained within the known rectangle to the Clipboard.</span></span><br/>                                                               |
| [<span data-ttu-id="ef765-138">**ClipboardPaste**</span><span class="sxs-lookup"><span data-stu-id="ef765-138">**ClipboardPaste**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardpaste)                         | <span data-ttu-id="ef765-139">Copie [**IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject) du presse-papiers vers l’objet **InkDisp** .</span><span class="sxs-lookup"><span data-stu-id="ef765-139">Copies the [**IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject) from the Clipboard to the **InkDisp** object.</span></span><br/>                                                                                               |
| [<span data-ttu-id="ef765-140">**Répliqué**</span><span class="sxs-lookup"><span data-stu-id="ef765-140">**Clone**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clone)                                           | <span data-ttu-id="ef765-141">Crée un objet **InkDisp** dupliqué.</span><span class="sxs-lookup"><span data-stu-id="ef765-141">Creates a duplicate **InkDisp** object.</span></span><br/>                                                                                                                                                   |
| [<span data-ttu-id="ef765-142">**CreateStroke**</span><span class="sxs-lookup"><span data-stu-id="ef765-142">**CreateStroke**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-createstroke)                             | <span data-ttu-id="ef765-143">Crée un trait à partir des points ou des données de paquet.</span><span class="sxs-lookup"><span data-stu-id="ef765-143">Creates a stroke from points or packet data.</span></span><br/>                                                                                                                                              |
| [<span data-ttu-id="ef765-144">**CreateStrokes**</span><span class="sxs-lookup"><span data-stu-id="ef765-144">**CreateStrokes**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-createstrokes)                           | <span data-ttu-id="ef765-145">Crée une collection [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) pour cet objet **InkDisp** .</span><span class="sxs-lookup"><span data-stu-id="ef765-145">Creates an [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection for this **InkDisp** object.</span></span><br/>                                                                                                |
| [<span data-ttu-id="ef765-146">**DeleteStroke**</span><span class="sxs-lookup"><span data-stu-id="ef765-146">**DeleteStroke**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-deletestroke)                             | <span data-ttu-id="ef765-147">Supprime un trait de l’objet **InkDisp** .</span><span class="sxs-lookup"><span data-stu-id="ef765-147">Deletes a stroke from the **InkDisp** object.</span></span><br/>                                                                                                                                             |
| [<span data-ttu-id="ef765-148">**DeleteStrokes**</span><span class="sxs-lookup"><span data-stu-id="ef765-148">**DeleteStrokes**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-deletestrokes)                           | <span data-ttu-id="ef765-149">Supprime les traits de l’objet **InkDisp** .</span><span class="sxs-lookup"><span data-stu-id="ef765-149">Deletes strokes from the **InkDisp** object.</span></span><br/>                                                                                                                                              |
| [<span data-ttu-id="ef765-150">**Méthode ExtractStrokes**</span><span class="sxs-lookup"><span data-stu-id="ef765-150">**ExtractStrokes Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-extractstrokes)                  | <span data-ttu-id="ef765-151">Extrait les traits de l’objet **InkDisp** et retourne un nouvel objet **InkDisp** contenant les traits extraits.</span><span class="sxs-lookup"><span data-stu-id="ef765-151">Extracts strokes from the **InkDisp** object and returns a new **InkDisp** object containing the extracted strokes.</span></span><br/>                                                                       |
| [<span data-ttu-id="ef765-152">**Méthode ExtractWithRectangle**</span><span class="sxs-lookup"><span data-stu-id="ef765-152">**ExtractWithRectangle Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-extractwithrectangle)      | <span data-ttu-id="ef765-153">Coupe ou copie les traits d’un objet de **classe InkDisp** existant et les colle dans un nouvel objet de **classe InkDisp** , en utilisant le rectangle connu pour déterminer les traits à extraire.</span><span class="sxs-lookup"><span data-stu-id="ef765-153">Cuts or copies strokes from an existing **InkDisp Class** object and pastes them into a new **InkDisp Class** object, by using the known rectangle to determine which strokes to extract.</span></span><br/> |
| [<span data-ttu-id="ef765-154">**GetBoundingBox**</span><span class="sxs-lookup"><span data-stu-id="ef765-154">**GetBoundingBox**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox)                  | <span data-ttu-id="ef765-155">Récupère le cadre englobant de tous les traits dans l’objet **InkDisp** .</span><span class="sxs-lookup"><span data-stu-id="ef765-155">Retrieves the bounding box of all of the strokes in the **InkDisp** object.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="ef765-156">**HitTestCircle**</span><span class="sxs-lookup"><span data-stu-id="ef765-156">**HitTestCircle**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestcircle)                   | <span data-ttu-id="ef765-157">Récupère la collection [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) qui est entièrement à l’intérieur ou à l’intersection d’un cercle connu.</span><span class="sxs-lookup"><span data-stu-id="ef765-157">Retrieves the [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection that are either completely inside or intersected by a known circle.</span></span><br/>                                                  |
| [<span data-ttu-id="ef765-158">**HitTestWithLasso**</span><span class="sxs-lookup"><span data-stu-id="ef765-158">**HitTestWithLasso**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestwithlasso)              | <span data-ttu-id="ef765-159">Récupère les traits dans une zone de sélection de polylignes.</span><span class="sxs-lookup"><span data-stu-id="ef765-159">Retrieves the strokes within a polyline selection area.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="ef765-160">**HitTestWithRectangle**</span><span class="sxs-lookup"><span data-stu-id="ef765-160">**HitTestWithRectangle**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestwithrectangle)        | <span data-ttu-id="ef765-161">Récupère les traits qui sont contenus dans un rectangle spécifié.</span><span class="sxs-lookup"><span data-stu-id="ef765-161">Retrieves the strokes that are contained within a specified rectangle.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="ef765-162">**Load**</span><span class="sxs-lookup"><span data-stu-id="ef765-162">**Load**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-load)                                             | <span data-ttu-id="ef765-163">Remplit un nouvel objet **InkDisp** avec des données binaires connues.</span><span class="sxs-lookup"><span data-stu-id="ef765-163">Populates a new **InkDisp** object with known binary data.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="ef765-164">**NearestPoint**</span><span class="sxs-lookup"><span data-stu-id="ef765-164">**NearestPoint**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-nearestpoint)                             | <span data-ttu-id="ef765-165">Récupère le [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) dans l’objet **InkDisp** le plus proche d’un point connu, en fournissant éventuellement des informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="ef765-165">Retrieves the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) within the **InkDisp** object that is nearest to a known point, optionally providing additional information.</span></span><br/>                       |
| [<span data-ttu-id="ef765-166">**Enregistrer**</span><span class="sxs-lookup"><span data-stu-id="ef765-166">**Save**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-save)                                             | <span data-ttu-id="ef765-167">Convertit l’encre dans un format spécifié et retourne les données binaires.</span><span class="sxs-lookup"><span data-stu-id="ef765-167">Converts the ink to a specified format and returns the binary data.</span></span><br/>                                                                                                                       |



 

### <a name="properties"></a><span data-ttu-id="ef765-168">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ef765-168">Properties</span></span>

<span data-ttu-id="ef765-169">La classe **InkDisp** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="ef765-169">The **InkDisp** class has these properties.</span></span>



| <span data-ttu-id="ef765-170">Propriété</span><span class="sxs-lookup"><span data-stu-id="ef765-170">Property</span></span>                                                                           | <span data-ttu-id="ef765-171">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="ef765-171">Access type</span></span>           | <span data-ttu-id="ef765-172">Description</span><span class="sxs-lookup"><span data-stu-id="ef765-172">Description</span></span>                                                                                                                             |
|:-----------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ef765-173">**CustomStrokes**</span><span class="sxs-lookup"><span data-stu-id="ef765-173">**CustomStrokes**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_customstrokes)<br/>                          | <span data-ttu-id="ef765-174">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ef765-174">Read-only</span></span><br/>  | <span data-ttu-id="ef765-175">Obtient la collection [**IInkCustomStrokes**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes) à rendre persistante avec l’encre.</span><span class="sxs-lookup"><span data-stu-id="ef765-175">Gets the [**IInkCustomStrokes**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes) collection to be persisted with the ink.</span></span><br/>                             |
| [<span data-ttu-id="ef765-176">**Dirt**</span><span class="sxs-lookup"><span data-stu-id="ef765-176">**Dirty**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_dirty)<br/>                                          | <span data-ttu-id="ef765-177">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ef765-177">Read/write</span></span><br/> | <span data-ttu-id="ef765-178">Obtient ou définit la valeur qui indique si un objet **InkDisp** a été modifié depuis le dernier enregistrement de l’encre.</span><span class="sxs-lookup"><span data-stu-id="ef765-178">Gets or sets the value that indicates whether an **InkDisp** object has been modified since the last time the ink was saved.</span></span><br/> |
| [<span data-ttu-id="ef765-179">**ExtendedProperties**</span><span class="sxs-lookup"><span data-stu-id="ef765-179">**ExtendedProperties**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_extendedproperties)<br/> | <span data-ttu-id="ef765-180">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ef765-180">Read-only</span></span><br/>  | <span data-ttu-id="ef765-181">Obtient la collection de données définies par l’application.</span><span class="sxs-lookup"><span data-stu-id="ef765-181">Gets the collection of application-defined data.</span></span><br/>                                                                             |
| [<span data-ttu-id="ef765-182">**Traits**</span><span class="sxs-lookup"><span data-stu-id="ef765-182">**Strokes**</span></span>](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes)<br/>                           | <span data-ttu-id="ef765-183">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ef765-183">Read-only</span></span><br/>  | <span data-ttu-id="ef765-184">Obtient la collection [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) contenue dans l’objet **InkDisp** .</span><span class="sxs-lookup"><span data-stu-id="ef765-184">Gets the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection contained in the **InkDisp** object.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="ef765-185">Notes</span><span class="sxs-lookup"><span data-stu-id="ef765-185">Remarks</span></span>

<span data-ttu-id="ef765-186">Cet objet peut être instancié en appelant la méthode [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) en C++.</span><span class="sxs-lookup"><span data-stu-id="ef765-186">This object can be instantiated by calling the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) method in C++.</span></span>

> [!Note]  
> <span data-ttu-id="ef765-187">La première instanciation de cet objet entraîne également l’instanciation de GDI+.</span><span class="sxs-lookup"><span data-stu-id="ef765-187">The first instantiation of this object causes GDI+ to be instantiated as well.</span></span> <span data-ttu-id="ef765-188">Un effet secondaire est que si vous utilisez un seul objet Ink dans une boucle et que vous le créez et le détruisez dans la boucle, vous recourez à l’instanciation de GDI+.</span><span class="sxs-lookup"><span data-stu-id="ef765-188">A side-effect is that if you are using a single ink object in a loop and create and destroy it within the loop, you will cause GDI+ to be instantiated over and over.</span></span> <span data-ttu-id="ef765-189">Cela peut entraîner une dégradation des performances dans votre application.</span><span class="sxs-lookup"><span data-stu-id="ef765-189">This can cause a performance degradation in your application.</span></span> <span data-ttu-id="ef765-190">Pour éviter cela, conservez une seule instance d’un objet Ink à tout moment pendant que votre application utilise de l’encre.</span><span class="sxs-lookup"><span data-stu-id="ef765-190">To prevent this, keep a single instance of an ink object at all times while your application is using ink.</span></span>

 

<span data-ttu-id="ef765-191">Un objet **InkDisp** est un conteneur de données de trait (point).</span><span class="sxs-lookup"><span data-stu-id="ef765-191">An **InkDisp** object is a container of stroke (point) data.</span></span> <span data-ttu-id="ef765-192">Les données de trait, ou les points recueillis par le stylet, sont placés dans un objet **InkDisp** .</span><span class="sxs-lookup"><span data-stu-id="ef765-192">The stroke data, or the points collected by the pen, are put into an **InkDisp** object.</span></span> <span data-ttu-id="ef765-193">La propriété [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) contient les données de tous les traits de l’objet **InkDisp** .</span><span class="sxs-lookup"><span data-stu-id="ef765-193">The [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) property contains the data for all strokes within the **InkDisp** object.</span></span>

<span data-ttu-id="ef765-194">L’objet [**InkCollector**](inkcollector-class.md) , l’objet [**InkOverlay**](inkoverlay-class.md) et le contrôle [InkPicture](inkpicture-control-reference.md) collectent les points de l’appareil d’entrée et les place dans un objet **InkDisp** .</span><span class="sxs-lookup"><span data-stu-id="ef765-194">The [**InkCollector**](inkcollector-class.md) object, [**InkOverlay**](inkoverlay-class.md) object, and [InkPicture](inkpicture-control-reference.md) control collects points from the input device and puts them into an **InkDisp** object.</span></span> <span data-ttu-id="ef765-195">Ces objets agissent essentiellement comme la source qui distribue l’encre dans un ou plusieurs objets **InkDisp** différents, qui jouent le rôle de conteneurs qui contiennent l’encre distribuée.</span><span class="sxs-lookup"><span data-stu-id="ef765-195">These objects essentially act as the source that distributes ink into one or many different **InkDisp** objects, which act as containers that hold the distributed ink.</span></span>

<span data-ttu-id="ef765-196">L’espace d’encre est un espace de coordonnées virtuelles auquel les coordonnées du contexte de tablette sont mappées.</span><span class="sxs-lookup"><span data-stu-id="ef765-196">The ink space is a virtual coordinate space to which the coordinates of the tablet context are mapped.</span></span> <span data-ttu-id="ef765-197">Cet espace est fixe à un système de coordonnées HIMETRIC.</span><span class="sxs-lookup"><span data-stu-id="ef765-197">This space is fixed to a HIMETRIC coordinate system.</span></span> <span data-ttu-id="ef765-198">Dans les coordonnées d’espace d’encre, un déplacement de 0 à 1 est égal à 1 unité HIMETRIC.</span><span class="sxs-lookup"><span data-stu-id="ef765-198">In ink space coordinates, a move from 0 to 1 equals 1 HIMETRIC unit.</span></span> <span data-ttu-id="ef765-199">Ce mappage facilite la mise en relation de plusieurs objets **InkDisp** .</span><span class="sxs-lookup"><span data-stu-id="ef765-199">This mapping makes it easy to relate multiple **InkDisp** objects.</span></span>

<span data-ttu-id="ef765-200">L’objet [**InkRenderer**](inkrenderer-class.md) gère les mappages entre l’encre et la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="ef765-200">The [**InkRenderer**](inkrenderer-class.md) object manages the mappings between ink and the display window.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef765-201">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ef765-201">Requirements</span></span>



| <span data-ttu-id="ef765-202">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ef765-202">Requirement</span></span> | <span data-ttu-id="ef765-203">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef765-203">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef765-204">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef765-204">Minimum supported client</span></span><br/> | <span data-ttu-id="ef765-205">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ef765-205">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="ef765-206">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef765-206">Minimum supported server</span></span><br/> | <span data-ttu-id="ef765-207">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef765-207">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="ef765-208">En-tête</span><span class="sxs-lookup"><span data-stu-id="ef765-208">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef765-209"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ef765-209"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ef765-210">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ef765-210">Library</span></span><br/>                  | <dl> <span data-ttu-id="ef765-211"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef765-211"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="ef765-212">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef765-212">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef765-213">**Interface IInkStrokeDisp**</span><span class="sxs-lookup"><span data-stu-id="ef765-213">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> <dt>

<span data-ttu-id="ef765-214">[Collection InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ef765-214">[InkStrokes Collection](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="ef765-215">**Interface IInkTablet**</span><span class="sxs-lookup"><span data-stu-id="ef765-215">**IInkTablet Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

