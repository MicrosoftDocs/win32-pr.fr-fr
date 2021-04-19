---
description: Spécifie le repère ou la zone où l’encre est dessinée et reconnue.
ms.assetid: 5bd874ff-003b-4471-b4ef-50731007dc5a
title: InkAnalysisRecognizerGuide, structure (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkAnalysisRecognizerGuide
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: eab5b1d09354f021f2c0a7e66a41b53e761d51e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513213"
---
# <a name="inkanalysisrecognizerguide-structure"></a><span data-ttu-id="2e964-103">InkAnalysisRecognizerGuide, structure</span><span class="sxs-lookup"><span data-stu-id="2e964-103">InkAnalysisRecognizerGuide structure</span></span>

<span data-ttu-id="2e964-104">Spécifie le repère ou la zone où l’encre est dessinée et reconnue.</span><span class="sxs-lookup"><span data-stu-id="2e964-104">Specifies the guide, or area where ink is drawn and recognized.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e964-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2e964-105">Syntax</span></span>


```C++
typedef struct InkAnalysisRecognizerGuide {
  RECT rectWritingBox;
  RECT rectDrawnBox;
  long cRows;
  long cColumns;
  long midline;
} InkAnalysisRecognizerGuide;
```



## <a name="members"></a><span data-ttu-id="2e964-106">Membres</span><span class="sxs-lookup"><span data-stu-id="2e964-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="2e964-107">**rectWritingBox**</span><span class="sxs-lookup"><span data-stu-id="2e964-107">**rectWritingBox**</span></span>
</dt> <dd>

<span data-ttu-id="2e964-108">Zone d’écriture invisible du Guide de reconnaissance dans laquelle l’écriture peut réellement avoir lieu.</span><span class="sxs-lookup"><span data-stu-id="2e964-108">The invisible writing area of the recognition guide in which writing can actually take place.</span></span>

</dd> <dt>

<span data-ttu-id="2e964-109">**rectDrawnBox**</span><span class="sxs-lookup"><span data-stu-id="2e964-109">**rectDrawnBox**</span></span>
</dt> <dd>

<span data-ttu-id="2e964-110">Rectangle qui est dessiné sur l’écran du Tablet PC et dans lequel l’écriture a lieu.</span><span class="sxs-lookup"><span data-stu-id="2e964-110">The rectangle that is drawn on the tablet screen and in which writing takes place.</span></span>

</dd> <dt>

<span data-ttu-id="2e964-111">**cRows**</span><span class="sxs-lookup"><span data-stu-id="2e964-111">**cRows**</span></span>
</dt> <dd>

<span data-ttu-id="2e964-112">Nombre de lignes dans la zone Guide de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="2e964-112">The number of rows in the recognition guide box.</span></span>

</dd> <dt>

<span data-ttu-id="2e964-113">**cColumns**</span><span class="sxs-lookup"><span data-stu-id="2e964-113">**cColumns**</span></span>
</dt> <dd>

<span data-ttu-id="2e964-114">Nombre de colonnes dans la zone Guide de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="2e964-114">The number of columns in the recognition guide box.</span></span>

</dd> <dt>

<span data-ttu-id="2e964-115">**médian**</span><span class="sxs-lookup"><span data-stu-id="2e964-115">**midline**</span></span>
</dt> <dd>

<span data-ttu-id="2e964-116">Hauteur de la médiane de la boîte du Guide de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="2e964-116">The midline height of the recognition guide box.</span></span> <span data-ttu-id="2e964-117">La hauteur de la ligne médiane est la distance entre la ligne de base et la ligne médiane de la zone dessinée.</span><span class="sxs-lookup"><span data-stu-id="2e964-117">The midline height is the distance from the baseline to the midline, of the drawn box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2e964-118">Notes</span><span class="sxs-lookup"><span data-stu-id="2e964-118">Remarks</span></span>

<span data-ttu-id="2e964-119">Un **InkAnalysisRecognizerGuide** définit une zone d’entrée attendue, par exemple une ligne ou des zones, pour les caractères.</span><span class="sxs-lookup"><span data-stu-id="2e964-119">An **InkAnalysisRecognizerGuide** defines an expected area of input, such as a line or boxes, for characters.</span></span> <span data-ttu-id="2e964-120">Une structure **InkAnalysisRecognizerGuide** peut être définie uniquement sur un nœud de contexte d’indicateur d’analyse (consultez [**IContextNode :: GetType**](icontextnode-gettype.md)).</span><span class="sxs-lookup"><span data-stu-id="2e964-120">An **InkAnalysisRecognizerGuide** structure can be set only on an analysis hint context node (see [**IContextNode::GetType**](icontextnode-gettype.md)).</span></span> <span data-ttu-id="2e964-121">Le [**IInkAnalyzer**](iinkanalyzer.md) utilise l’emplacement du nœud de l’indicateur d’analyse et les emplacements des traits d’encre pour associer un trait au nœud de l’indicateur d’analyse.</span><span class="sxs-lookup"><span data-stu-id="2e964-121">The [**IInkAnalyzer**](iinkanalyzer.md) uses the location of the analysis hint node and the locations of the ink strokes to associate a stroke with the analysis hint node.</span></span> <span data-ttu-id="2e964-122">Tout trait avec une association au nœud de l’indicateur d’analyse aura le **InkAnalysisRecognizerGuide** spécifié utilisé lorsqu’il est reconnu par un **IInkAnalyzer**, à condition que le **IInkAnalyzer** prenne en charge **InkAnalysisRecognizerGuide**.</span><span class="sxs-lookup"><span data-stu-id="2e964-122">Any strokes with an association to the analysis hint node will have the specified **InkAnalysisRecognizerGuide** used when recognized by an **IInkAnalyzer**, provided the **IInkAnalyzer** supports the **InkAnalysisRecognizerGuide**.</span></span> <span data-ttu-id="2e964-123">Les valeurs exprimées dans la classe **InkAnalysisRecognizerGuide** sont toujours relatives à l’emplacement du nœud d’indicateur d’analyse et sont spécifiées dans les coordonnées de l’espace d’encre.</span><span class="sxs-lookup"><span data-stu-id="2e964-123">The values expressed in the **InkAnalysisRecognizerGuide** class are always relative to the location of the analysis hint node and are specified in ink space coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e964-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2e964-124">Requirements</span></span>



| <span data-ttu-id="2e964-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2e964-125">Requirement</span></span> | <span data-ttu-id="2e964-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="2e964-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e964-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e964-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2e964-128">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2e964-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2e964-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e964-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2e964-130">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e964-130">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="2e964-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="2e964-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e964-132"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="2e964-132"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e964-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2e964-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e964-134">Propriétés de l’indicateur d’analyse</span><span class="sxs-lookup"><span data-stu-id="2e964-134">Analysis Hint Properties</span></span>](analysis-hint-properties.md)
</dt> <dt>

[<span data-ttu-id="2e964-135">**IInkAnalyzer :: CreateAnalysisHint, méthode**</span><span class="sxs-lookup"><span data-stu-id="2e964-135">**IInkAnalyzer::CreateAnalysisHint Method**</span></span>](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[<span data-ttu-id="2e964-136">**IContextNode::AddPropertyData**</span><span class="sxs-lookup"><span data-stu-id="2e964-136">**IContextNode::AddPropertyData**</span></span>](icontextnode-addpropertydata.md)
</dt> <dt>

[<span data-ttu-id="2e964-137">**IContextNode::GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="2e964-137">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="2e964-138">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="2e964-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




