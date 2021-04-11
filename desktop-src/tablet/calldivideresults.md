---
description: Récupère les résultats de l’analyse à partir de l’objet InkDivider.
ms.assetid: 7fc2bb5a-172f-4f4e-84dd-e31925f86982
title: CallDivideResults fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CallDivideResults
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 11878e6a0ac953b9b7eb27ce21bb67001f9d88d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111703"
---
# <a name="calldivideresults-function"></a><span data-ttu-id="1eabd-103">CallDivideResults fonction)</span><span class="sxs-lookup"><span data-stu-id="1eabd-103">CallDivideResults function</span></span>

<span data-ttu-id="1eabd-104">Récupère les résultats de l’analyse à partir de l’objet [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="1eabd-104">Retrieves analysis results from the [**InkDivider**](inkdivider-class.md) object.</span></span>

<span data-ttu-id="1eabd-105">Cette fonction n’est pas destinée à être utilisée par le code d’application.</span><span class="sxs-lookup"><span data-stu-id="1eabd-105">This function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="1eabd-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1eabd-106">Syntax</span></span>


```C++
HRESULT WINAPI CallDivideResults(
  _In_  INT_PTR   hDivider,
  _Out_ int       aWordStrokeIds[],
  _Out_ int       aLineStrokeIds[],
  _Out_ int       aParagraphStrokeIds[],
  _Out_ int       aDrawingStrokeIds[],
  _Out_ SAFEARRAY **pastrWords,
  _Out_ SAFEARRAY **pastrLines,
  _Out_ SAFEARRAY **pastrParagraphs,
  _Out_ int       *aWordRotationCenterX,
  _Out_ int       *aWordRotationCenterY,
  _Out_ float     *aWordAngle,
  _Out_ int       *aLineRotationCenterX,
  _Out_ int       *aLineRotationCenterY,
  _Out_ float     *aLineAngle
);
```



## <a name="parameters"></a><span data-ttu-id="1eabd-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1eabd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1eabd-108">*hDivider* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1eabd-108">*hDivider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1eabd-109">Handle de l’objet [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="1eabd-109">A handle to the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="1eabd-110">*aWordStrokeIds* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1eabd-110">*aWordStrokeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1eabd-111">Tableau d’identificateurs associés au mot passé à la classe [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="1eabd-111">An array of identifiers associated with the word that is passed in to the [**InkDivider**](inkdivider-class.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="1eabd-112">*aLineStrokeIds* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1eabd-112">*aLineStrokeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1eabd-113">Tableau de propriétés d' [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) pour les objets [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) associés à la ligne passée à la classe [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="1eabd-113">An array of [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) properties for the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects associated with the line that is passed in to the [**InkDivider**](inkdivider-class.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="1eabd-114">*aParagraphStrokeIds* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1eabd-114">*aParagraphStrokeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1eabd-115">Tableau des propriétés d' [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) pour les objets [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) associés au paragraphe de la classe [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="1eabd-115">An array of the [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) properties for the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects associated with the paragraph from the [**InkDivider**](inkdivider-class.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="1eabd-116">*aDrawingStrokeIds* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1eabd-116">*aDrawingStrokeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1eabd-117">Tableau de propriétés d' [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) pour les objets [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) associés au dessin à partir de la classe [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="1eabd-117">An array of [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) properties for the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects associated with the drawing from the [**InkDivider**](inkdivider-class.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="1eabd-118">*pastrWords* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1eabd-118">*pastrWords* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1eabd-119">Tableau de mots retournés par l’analyse de l’encre.</span><span class="sxs-lookup"><span data-stu-id="1eabd-119">An array of words returned from ink analysis.</span></span>

</dd> <dt>

<span data-ttu-id="1eabd-120">*pastrLines* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1eabd-120">*pastrLines* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1eabd-121">Tableau de lignes retournées par l’analyse de l’encre.</span><span class="sxs-lookup"><span data-stu-id="1eabd-121">An array of lines returned from ink analysis.</span></span>

</dd> <dt>

<span data-ttu-id="1eabd-122">*pastrParagraphs* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1eabd-122">*pastrParagraphs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1eabd-123">Tableau de paragraphes renvoyés à partir de l’analyse de l’encre.</span><span class="sxs-lookup"><span data-stu-id="1eabd-123">An array of paragraphs returned from ink analysis.</span></span>

</dd> <dt>

<span data-ttu-id="1eabd-124">*aWordRotationCenterX* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1eabd-124">*aWordRotationCenterX* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1eabd-125">Tableau des points centraux des mots le long de l’axe x à partir de l’analyse de l’encre.</span><span class="sxs-lookup"><span data-stu-id="1eabd-125">An array of the center points of the words along the x-axis from ink analysis.</span></span>

</dd> <dt>

<span data-ttu-id="1eabd-126">*aWordRotationCenterY* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1eabd-126">*aWordRotationCenterY* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1eabd-127">Tableau des points centraux des mots situés le long de l’axe des y à partir de l’analyse de l’encre.</span><span class="sxs-lookup"><span data-stu-id="1eabd-127">An array of the center points of the words along the y-axis from ink analysis.</span></span>

</dd> <dt>

<span data-ttu-id="1eabd-128">*aWordAngle* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1eabd-128">*aWordAngle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1eabd-129">Tableau contenant les angles de rotation des mots pour obtenir les meilleurs résultats d’analyse.</span><span class="sxs-lookup"><span data-stu-id="1eabd-129">An array containing the angles by which to rotate the words for best analysis results.</span></span>

</dd> <dt>

<span data-ttu-id="1eabd-130">*aLineRotationCenterX* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1eabd-130">*aLineRotationCenterX* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1eabd-131">Tableau contenant les points centraux des lignes le long de l’axe x.</span><span class="sxs-lookup"><span data-stu-id="1eabd-131">An array containing the center points of the lines along the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="1eabd-132">*aLineRotationCenterY* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1eabd-132">*aLineRotationCenterY* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1eabd-133">Tableau contenant les points centraux des lignes le long de l’axe y.</span><span class="sxs-lookup"><span data-stu-id="1eabd-133">An array containing the center points of the lines along the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="1eabd-134">*aLineAngle* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1eabd-134">*aLineAngle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1eabd-135">Tableau contenant les angles de rotation des lignes pour obtenir les meilleurs résultats d’analyse.</span><span class="sxs-lookup"><span data-stu-id="1eabd-135">An array containing the angles by which to rotate the lines for best analysis results.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1eabd-136">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1eabd-136">Return value</span></span>

<span data-ttu-id="1eabd-137">Cette fonction peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="1eabd-137">This function can return one of these values.</span></span>



| <span data-ttu-id="1eabd-138">Code de retour</span><span class="sxs-lookup"><span data-stu-id="1eabd-138">Return code</span></span>                                                                                   | <span data-ttu-id="1eabd-139">Description</span><span class="sxs-lookup"><span data-stu-id="1eabd-139">Description</span></span>                                                       |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <span data-ttu-id="1eabd-140"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1eabd-140"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="1eabd-141">La fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="1eabd-141">The function succeeded.</span></span><br/>                                |
| <dl> <span data-ttu-id="1eabd-142"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="1eabd-142"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="1eabd-143">Le paramètre *hDivider* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="1eabd-143">The *hDivider* parameter is invalid.</span></span><br/>                   |
| <dl> <span data-ttu-id="1eabd-144"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="1eabd-144"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="1eabd-145">Impossible d’allouer suffisamment de mémoire pour stocker les résultats.</span><span class="sxs-lookup"><span data-stu-id="1eabd-145">Could not allocate enough memory to store the results.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1eabd-146">Notes</span><span class="sxs-lookup"><span data-stu-id="1eabd-146">Remarks</span></span>

<span data-ttu-id="1eabd-147">Pour éviter les fuites de mémoire, vous devez libérer les ressources pour *pastrWords*, *pastrLines* et *pastrParagraphs*.</span><span class="sxs-lookup"><span data-stu-id="1eabd-147">To avoid memory leaks you must release the resources for *pastrWords*, *pastrLines*, and *pastrParagraphs*.</span></span>

## <a name="requirements"></a><span data-ttu-id="1eabd-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1eabd-148">Requirements</span></span>



| <span data-ttu-id="1eabd-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1eabd-149">Requirement</span></span> | <span data-ttu-id="1eabd-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="1eabd-150">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1eabd-151">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1eabd-151">Minimum supported client</span></span><br/> | <span data-ttu-id="1eabd-152">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1eabd-152">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="1eabd-153">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1eabd-153">Minimum supported server</span></span><br/> | <span data-ttu-id="1eabd-154">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="1eabd-154">None supported</span></span><br/>                                                             |
| <span data-ttu-id="1eabd-155">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1eabd-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="1eabd-156"><dt>InkDiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1eabd-156"><dt>InkDiv.dll</dt></span></span> </dl> |



 

 




