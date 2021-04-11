---
description: Indique si un trait doit être analysé dans le cadre d’un dessin ou dans le cadre de l’écriture.
ms.assetid: 3f4c4522-ada7-4759-bca7-88b2a71f36ea
title: Énumération StrokeType (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StrokeType
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: 3b59be130c6c7055bb7636760451dcadf5acf841
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204038"
---
# <a name="stroketype-enumeration"></a><span data-ttu-id="26f6e-103">Énumération StrokeType</span><span class="sxs-lookup"><span data-stu-id="26f6e-103">StrokeType enumeration</span></span>

<span data-ttu-id="26f6e-104">Indique si un trait doit être analysé dans le cadre d’un dessin ou dans le cadre de l’écriture.</span><span class="sxs-lookup"><span data-stu-id="26f6e-104">Indicates whether a stroke should be analyzed as part of a drawing or as part of writing.</span></span>

## <a name="syntax"></a><span data-ttu-id="26f6e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="26f6e-105">Syntax</span></span>


```C++
typedef enum StrokeType { 
  StrokeType_Unclassified  = 0,
  StrokeType_Writing       = 1,
  StrokeType_Drawing       = 2
} StrokeType;
```



## <a name="constants"></a><span data-ttu-id="26f6e-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="26f6e-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="26f6e-107"><span id="StrokeType_Unclassified"></span><span id="stroketype_unclassified"></span><span id="STROKETYPE_UNCLASSIFIED"></span>**StrokeType non \_ classé**</span><span class="sxs-lookup"><span data-stu-id="26f6e-107"><span id="StrokeType_Unclassified"></span><span id="stroketype_unclassified"></span><span id="STROKETYPE_UNCLASSIFIED"></span>**StrokeType\_Unclassified**</span></span>
</dt> <dd>

<span data-ttu-id="26f6e-108">Le trait peut faire partie d’un dessin ou d’une partie de l’écriture.</span><span class="sxs-lookup"><span data-stu-id="26f6e-108">The stroke might be either part of a drawing or part of writing.</span></span>

</dd> <dt>

<span data-ttu-id="26f6e-109"><span id="StrokeType_Writing"></span><span id="stroketype_writing"></span><span id="STROKETYPE_WRITING"></span>**\_Écriture StrokeType**</span><span class="sxs-lookup"><span data-stu-id="26f6e-109"><span id="StrokeType_Writing"></span><span id="stroketype_writing"></span><span id="STROKETYPE_WRITING"></span>**StrokeType\_Writing**</span></span>
</dt> <dd>

<span data-ttu-id="26f6e-110">Le trait fait partie de l’écriture.</span><span class="sxs-lookup"><span data-stu-id="26f6e-110">The stroke is part of writing.</span></span>

</dd> <dt>

<span data-ttu-id="26f6e-111"><span id="StrokeType_Drawing"></span><span id="stroketype_drawing"></span><span id="STROKETYPE_DRAWING"></span>**\_Dessin StrokeType**</span><span class="sxs-lookup"><span data-stu-id="26f6e-111"><span id="StrokeType_Drawing"></span><span id="stroketype_drawing"></span><span id="STROKETYPE_DRAWING"></span>**StrokeType\_Drawing**</span></span>
</dt> <dd>

<span data-ttu-id="26f6e-112">Le trait fait partie d’un dessin.</span><span class="sxs-lookup"><span data-stu-id="26f6e-112">The stroke is part of a drawing.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="26f6e-113">Exemples</span><span class="sxs-lookup"><span data-stu-id="26f6e-113">Examples</span></span>

<span data-ttu-id="26f6e-114">L’exemple suivant montre une partie d’un gestionnaire d’événements Stroke, implémentée de façon similaire à l' [exemple de récepteurs d’événements C++](c---event-sinks-sample.md).</span><span class="sxs-lookup"><span data-stu-id="26f6e-114">The following example shows part of a stroke event handler, implemented in a similar fashion to the [C++ Event Sinks Sample](c---event-sinks-sample.md).</span></span> <span data-ttu-id="26f6e-115">Le trait ajouté est vérifié pour voir si le haut de son cadre englobant a été dessiné sous une marge, `drawingMargin` .</span><span class="sxs-lookup"><span data-stu-id="26f6e-115">The added stroke is checked to see if the top of its bounding box has been drawn below a margin, `drawingMargin`.</span></span> <span data-ttu-id="26f6e-116">Dans ce cas, l’objet [**IInkAnalyzer**](iinkanalyzer.md) , `m_spInkAnalyzer` , est défini pour analyser le trait comme un trait de dessin, plutôt que comme un trait d’écriture manuscrite.</span><span class="sxs-lookup"><span data-stu-id="26f6e-116">If so, the [**IInkAnalyzer**](iinkanalyzer.md) object, `m_spInkAnalyzer`, is set to analyze the stroke as a drawing stroke, rather than as a handwriting stroke.</span></span> <span data-ttu-id="26f6e-117">`CheckHResult` est une fonction qui accepte un `HRESULT` et une chaîne, et lève une exception créée avec la chaîne si le `HRESULT` n’a pas **réussi**.</span><span class="sxs-lookup"><span data-stu-id="26f6e-117">`CheckHResult` is a function that takes an `HRESULT` and a string, and throws an exception created with the string if the `HRESULT` is not **SUCCESS**.</span></span>


```C++
IInkRectangle* bounds;
CheckHResult(pStroke->GetBoundingBox(IBBM_Default, &bounds), "IInkStrokeDisp::GetBoundingBox failed");
long top;
CheckHResult(bounds->get_Top(&top), "IInkRectangle::get_Top failed");
if (top > drawingMargin)
{
    long strokeId;
    CheckHResult(pStroke->get_ID(&strokeId), "IInkStrokeDisp::get_ID failed");
    m_pInkAnalyzer->SetStrokeType(strokeId, StrokeType_Drawing);
}
```



## <a name="requirements"></a><span data-ttu-id="26f6e-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="26f6e-118">Requirements</span></span>



| <span data-ttu-id="26f6e-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="26f6e-119">Requirement</span></span> | <span data-ttu-id="26f6e-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="26f6e-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26f6e-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26f6e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="26f6e-122">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="26f6e-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="26f6e-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26f6e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="26f6e-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="26f6e-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="26f6e-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="26f6e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="26f6e-126"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="26f6e-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26f6e-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26f6e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26f6e-128">**IInkAnalyzer :: SetStrokeType, méthode**</span><span class="sxs-lookup"><span data-stu-id="26f6e-128">**IInkAnalyzer::SetStrokeType Method**</span></span>](iinkanalyzer-setstroketype.md)
</dt> </dl>

 

 




