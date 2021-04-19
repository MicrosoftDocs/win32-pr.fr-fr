---
description: Représente une matrice 3x3 qui, à son tour, représente une transformation affine.
ms.assetid: 79abff2e-d1d3-4a32-9ac2-f46c1b21f742
title: InkTransform, classe (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkTransform
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 61641f0fed8ec98321e155f82ff9a35150e7fdcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518945"
---
# <a name="inktransform-class"></a><span data-ttu-id="e2549-103">InkTransform, classe</span><span class="sxs-lookup"><span data-stu-id="e2549-103">InkTransform class</span></span>

<span data-ttu-id="e2549-104">Représente une matrice 3x3 qui, à son tour, représente une transformation affine.</span><span class="sxs-lookup"><span data-stu-id="e2549-104">Represents a 3x3 matrix that, in turn, represents an affine transformation.</span></span>

<span data-ttu-id="e2549-105">**InkTransform** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e2549-105">**InkTransform** has these types of members:</span></span>

-   [<span data-ttu-id="e2549-106">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e2549-106">Methods</span></span>](#methods)
-   [<span data-ttu-id="e2549-107">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e2549-107">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e2549-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e2549-108">Methods</span></span>

<span data-ttu-id="e2549-109">La classe **InkTransform** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="e2549-109">The **InkTransform** class has these methods.</span></span>



| <span data-ttu-id="e2549-110">Méthode</span><span class="sxs-lookup"><span data-stu-id="e2549-110">Method</span></span>                                                  | <span data-ttu-id="e2549-111">Description</span><span class="sxs-lookup"><span data-stu-id="e2549-111">Description</span></span>                                                                                                                 |
|:--------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e2549-112">**GetTransform**</span><span class="sxs-lookup"><span data-stu-id="e2549-112">**GetTransform**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-gettransform)       | <span data-ttu-id="e2549-113">Récupère le **InkTransform** sous la forme de 6 valeurs à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="e2549-113">Retrieves the **InkTransform** as 6 floats.</span></span><br/>                                                                      |
| [<span data-ttu-id="e2549-114">**Correspond**</span><span class="sxs-lookup"><span data-stu-id="e2549-114">**Reflect**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-reflect)                 | <span data-ttu-id="e2549-115">Reflète la transformation dans les directions horizontale ou verticale.</span><span class="sxs-lookup"><span data-stu-id="e2549-115">Reflects the transform in either the horizontal or vertical directions.</span></span><br/>                                          |
| [<span data-ttu-id="e2549-116">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="e2549-116">**Reset**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-reset)                     | <span data-ttu-id="e2549-117">Rétablit l’état d’origine de la transformation.</span><span class="sxs-lookup"><span data-stu-id="e2549-117">Resets the transform to its original state.</span></span><br/>                                                                      |
| [<span data-ttu-id="e2549-118">**Faire pivoter**</span><span class="sxs-lookup"><span data-stu-id="e2549-118">**Rotate**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-rotate)                   | <span data-ttu-id="e2549-119">Fait pivoter la transformation d’un angle mesuré en degrés, et spécifie éventuellement un point central pour la rotation.</span><span class="sxs-lookup"><span data-stu-id="e2549-119">Rotates the transform by an angle measured in degrees, and optionally specifies a center point for the rotation.</span></span><br/> |
| [<span data-ttu-id="e2549-120">**ScaleTransform**</span><span class="sxs-lookup"><span data-stu-id="e2549-120">**ScaleTransform**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-scaletransform) | <span data-ttu-id="e2549-121">Met à l’échelle la transformation par facteurs X et Y.</span><span class="sxs-lookup"><span data-stu-id="e2549-121">Scales the transform by X and Y factors.</span></span><br/>                                                                         |
| [<span data-ttu-id="e2549-122">**SetTransform**</span><span class="sxs-lookup"><span data-stu-id="e2549-122">**SetTransform**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-settransform)       | <span data-ttu-id="e2549-123">Modifie le **InkTransform** à l’aide de 6 valeurs float.</span><span class="sxs-lookup"><span data-stu-id="e2549-123">Modifies the **InkTransform** using 6 floats.</span></span><br/>                                                                    |
| [<span data-ttu-id="e2549-124">**Incliné**</span><span class="sxs-lookup"><span data-stu-id="e2549-124">**Shear**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-shear)                     | <span data-ttu-id="e2549-125">Applique une inclinaison avec les facteurs horizontaux et verticaux spécifiés.</span><span class="sxs-lookup"><span data-stu-id="e2549-125">Applies a shear with the specified horizontal and vertical factors.</span></span><br/>                                              |
| [<span data-ttu-id="e2549-126">**Traduire**</span><span class="sxs-lookup"><span data-stu-id="e2549-126">**Translate**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-translate)             | <span data-ttu-id="e2549-127">Déplace la transformation selon les composants horizontaux et verticaux spécifiés.</span><span class="sxs-lookup"><span data-stu-id="e2549-127">Moves the transform by the specified horizontal and vertical components.</span></span><br/>                                         |



 

### <a name="properties"></a><span data-ttu-id="e2549-128">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e2549-128">Properties</span></span>

<span data-ttu-id="e2549-129">La classe **InkTransform** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="e2549-129">The **InkTransform** class has these properties.</span></span>



| <span data-ttu-id="e2549-130">Propriété</span><span class="sxs-lookup"><span data-stu-id="e2549-130">Property</span></span>                                     | <span data-ttu-id="e2549-131">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="e2549-131">Access type</span></span>           | <span data-ttu-id="e2549-132">Description</span><span class="sxs-lookup"><span data-stu-id="e2549-132">Description</span></span>                                                                                          |
|:---------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e2549-133">**Métadonnée**</span><span class="sxs-lookup"><span data-stu-id="e2549-133">**Data**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_data)<br/> | <span data-ttu-id="e2549-134">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e2549-134">Read/write</span></span><br/> | <span data-ttu-id="e2549-135">Obtient ou définit la version Automation de la structure WIN32 XFORM.</span><span class="sxs-lookup"><span data-stu-id="e2549-135">Gets or sets the Automation version of the WIN32 XFORM struct.</span></span><br/>                            |
| [<span data-ttu-id="e2549-136">**eDx**</span><span class="sxs-lookup"><span data-stu-id="e2549-136">**eDx**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_edx)<br/>   | <span data-ttu-id="e2549-137">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e2549-137">Read/write</span></span><br/> | <span data-ttu-id="e2549-138">Obtient ou définit le nombre réel qui spécifie l’élément de la troisième ligne, première colonne.</span><span class="sxs-lookup"><span data-stu-id="e2549-138">Gets or sets the real number that specifies the element in the third row, first column.</span></span><br/>   |
| [<span data-ttu-id="e2549-139">**eDy**</span><span class="sxs-lookup"><span data-stu-id="e2549-139">**eDy**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_edy)<br/>   | <span data-ttu-id="e2549-140">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e2549-140">Read/write</span></span><br/> | <span data-ttu-id="e2549-141">Obtient ou définit le nombre réel qui spécifie l’élément de la troisième ligne, deuxième colonne.</span><span class="sxs-lookup"><span data-stu-id="e2549-141">Gets or sets the real number that specifies the element in the third row, second column.</span></span><br/>  |
| [<span data-ttu-id="e2549-142">**eM11**</span><span class="sxs-lookup"><span data-stu-id="e2549-142">**eM11**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em11)<br/> | <span data-ttu-id="e2549-143">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e2549-143">Read/write</span></span><br/> | <span data-ttu-id="e2549-144">Obtient ou définit le nombre réel qui spécifie l’élément dans la première ligne, première colonne.</span><span class="sxs-lookup"><span data-stu-id="e2549-144">Gets or sets the real number that specifies the element in the first row, first column.</span></span><br/>   |
| [<span data-ttu-id="e2549-145">**eM12**</span><span class="sxs-lookup"><span data-stu-id="e2549-145">**eM12**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em12)<br/> | <span data-ttu-id="e2549-146">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e2549-146">Read/write</span></span><br/> | <span data-ttu-id="e2549-147">Obtient ou définit le nombre réel qui spécifie l’élément dans la première ligne, deuxième colonne.</span><span class="sxs-lookup"><span data-stu-id="e2549-147">Gets or sets the real number that specifies the element in the first row, second column.</span></span><br/>  |
| [<span data-ttu-id="e2549-148">**eM21**</span><span class="sxs-lookup"><span data-stu-id="e2549-148">**eM21**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em21)<br/> | <span data-ttu-id="e2549-149">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e2549-149">Read/write</span></span><br/> | <span data-ttu-id="e2549-150">Obtient ou définit le nombre réel qui spécifie l’élément dans la deuxième ligne, première colonne.</span><span class="sxs-lookup"><span data-stu-id="e2549-150">Gets or sets the real number that specifies the element in the second row, first column.</span></span><br/>  |
| [<span data-ttu-id="e2549-151">**eM22**</span><span class="sxs-lookup"><span data-stu-id="e2549-151">**eM22**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em22)<br/> | <span data-ttu-id="e2549-152">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e2549-152">Read/write</span></span><br/> | <span data-ttu-id="e2549-153">Obtient ou définit le nombre réel qui spécifie l’élément dans la deuxième ligne, deuxième colonne.</span><span class="sxs-lookup"><span data-stu-id="e2549-153">Gets or sets the real number that specifies the element in the second row, second column.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e2549-154">Notes</span><span class="sxs-lookup"><span data-stu-id="e2549-154">Remarks</span></span>

<span data-ttu-id="e2549-155">Cet objet peut être instancié en appelant la méthode [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) en C++.</span><span class="sxs-lookup"><span data-stu-id="e2549-155">This object can be instantiated by calling the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) method in C++.</span></span>

<span data-ttu-id="e2549-156">L’objet stocke uniquement six des neuf chiffres dans une matrice 3x3, car toutes les matrices 3x3 qui représentent des transformations affines ont la même troisième colonne (0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="e2549-156">The object stores only six of the nine numbers in a 3x3 matrix because all 3x3 matrices that represent affine transformations have the same third column (0, 0, 1).</span></span> <span data-ttu-id="e2549-157">Cet objet est utilisé à son tour pour décrire des opérations de transformation telles que le déplacement, la déformation, la mise à l’échelle ou la rotation dans un objet [**InkRenderer**](inkrenderer-class.md) , un objet [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) ou une collection [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e2549-157">This object in turn is used to describe transformation operations such as moving, shearing, scaling, or rotating in an [**InkRenderer**](inkrenderer-class.md) object, [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object, or [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection.</span></span>

> [!Note]  
> <span data-ttu-id="e2549-158">L’objet **InkTransform** est corrélé à la structure [**XForm**](/windows/win32/api/wingdi/ns-wingdi-xform) .</span><span class="sxs-lookup"><span data-stu-id="e2549-158">The **InkTransform** object correlates to the [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) structure.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e2549-159">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e2549-159">Requirements</span></span>



| <span data-ttu-id="e2549-160">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e2549-160">Requirement</span></span> | <span data-ttu-id="e2549-161">Valeur</span><span class="sxs-lookup"><span data-stu-id="e2549-161">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2549-162">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e2549-162">Minimum supported client</span></span><br/> | <span data-ttu-id="e2549-163">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e2549-163">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="e2549-164">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e2549-164">Minimum supported server</span></span><br/> | <span data-ttu-id="e2549-165">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e2549-165">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="e2549-166">En-tête</span><span class="sxs-lookup"><span data-stu-id="e2549-166">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2549-167"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e2549-167"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e2549-168">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e2549-168">Library</span></span><br/>                  | <dl> <span data-ttu-id="e2549-169"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2549-169"><dt>InkObj.dll</dt></span></span> </dl>                               |



 

