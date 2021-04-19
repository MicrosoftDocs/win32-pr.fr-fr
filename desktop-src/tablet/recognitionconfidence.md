---
description: Indique le niveau de confiance que le IInkAnalyzer a dans la précision du résultat de la reconnaissance.
ms.assetid: fd4fc350-b4db-4f9a-a5ae-00065e33606c
title: Énumération RecognitionConfidence (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecognitionConfidence
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: e0358aacf789c391d99c10fc0fea64670dc4710e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530258"
---
# <a name="recognitionconfidence-enumeration"></a><span data-ttu-id="70716-103">Énumération RecognitionConfidence</span><span class="sxs-lookup"><span data-stu-id="70716-103">RecognitionConfidence enumeration</span></span>

<span data-ttu-id="70716-104">Indique le niveau de confiance que le [**IInkAnalyzer**](iinkanalyzer.md) a dans la précision du résultat de la reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="70716-104">Indicates the level of confidence that the [**IInkAnalyzer**](iinkanalyzer.md) has in the accuracy of the recognition result.</span></span>

## <a name="syntax"></a><span data-ttu-id="70716-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="70716-105">Syntax</span></span>


```C++
typedef enum RecognitionConfidence { 
  RecognitionConfidence_Strong        = 0,
  RecognitionConfidence_Intermediate  = 1,
  RecognitionConfidence_Poor          = 2,
  RecognitionConfidence_Unknown       = 3
} RecognitionConfidence;
```



## <a name="constants"></a><span data-ttu-id="70716-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="70716-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="70716-107"><span id="RecognitionConfidence_Strong"></span><span id="recognitionconfidence_strong"></span><span id="RECOGNITIONCONFIDENCE_STRONG"></span>**RecognitionConfidence \_ Strong**</span><span class="sxs-lookup"><span data-stu-id="70716-107"><span id="RecognitionConfidence_Strong"></span><span id="recognitionconfidence_strong"></span><span id="RECOGNITIONCONFIDENCE_STRONG"></span>**RecognitionConfidence\_Strong**</span></span>
</dt> <dd>

<span data-ttu-id="70716-108">Confiance forte dans le résultat ou l’autre.</span><span class="sxs-lookup"><span data-stu-id="70716-108">Strong confidence in the result or alternate.</span></span>

</dd> <dt>

<span data-ttu-id="70716-109"><span id="RecognitionConfidence_Intermediate"></span><span id="recognitionconfidence_intermediate"></span><span id="RECOGNITIONCONFIDENCE_INTERMEDIATE"></span>**RecognitionConfidence \_ intermédiaire**</span><span class="sxs-lookup"><span data-stu-id="70716-109"><span id="RecognitionConfidence_Intermediate"></span><span id="recognitionconfidence_intermediate"></span><span id="RECOGNITIONCONFIDENCE_INTERMEDIATE"></span>**RecognitionConfidence\_Intermediate**</span></span>
</dt> <dd>

<span data-ttu-id="70716-110">Confiance intermédiaire dans le résultat ou l’autre.</span><span class="sxs-lookup"><span data-stu-id="70716-110">Intermediate confidence in the result or alternate.</span></span>

</dd> <dt>

<span data-ttu-id="70716-111"><span id="RecognitionConfidence_Poor"></span><span id="recognitionconfidence_poor"></span><span id="RECOGNITIONCONFIDENCE_POOR"></span>**RecognitionConfidence \_ médiocre**</span><span class="sxs-lookup"><span data-stu-id="70716-111"><span id="RecognitionConfidence_Poor"></span><span id="recognitionconfidence_poor"></span><span id="RECOGNITIONCONFIDENCE_POOR"></span>**RecognitionConfidence\_Poor**</span></span>
</dt> <dd>

<span data-ttu-id="70716-112">Confiance faible dans le résultat ou l’autre.</span><span class="sxs-lookup"><span data-stu-id="70716-112">Poor confidence in the result or alternate.</span></span>

</dd> <dt>

<span data-ttu-id="70716-113"><span id="RecognitionConfidence_Unknown"></span><span id="recognitionconfidence_unknown"></span><span id="RECOGNITIONCONFIDENCE_UNKNOWN"></span>**RecognitionConfidence \_ inconnu**</span><span class="sxs-lookup"><span data-stu-id="70716-113"><span id="RecognitionConfidence_Unknown"></span><span id="recognitionconfidence_unknown"></span><span id="RECOGNITIONCONFIDENCE_UNKNOWN"></span>**RecognitionConfidence\_Unknown**</span></span>
</dt> <dd>

<span data-ttu-id="70716-114">Le [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) qui a généré le texte reconnu ne prend pas en charge les niveaux de confiance.</span><span class="sxs-lookup"><span data-stu-id="70716-114">The [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) that generated the recognized text does not support confidence levels.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="70716-115">Notes</span><span class="sxs-lookup"><span data-stu-id="70716-115">Remarks</span></span>

<span data-ttu-id="70716-116">[**IInkAnalyzer**](iinkanalyzer.md) utilise un ou plusieurs objets [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) pour convertir l’écriture manuscrite en texte.</span><span class="sxs-lookup"><span data-stu-id="70716-116">The [**IInkAnalyzer**](iinkanalyzer.md) uses one or more [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) objects to convert handwriting to text.</span></span>

## <a name="requirements"></a><span data-ttu-id="70716-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="70716-117">Requirements</span></span>



| <span data-ttu-id="70716-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="70716-118">Requirement</span></span> | <span data-ttu-id="70716-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="70716-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70716-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="70716-120">Minimum supported client</span></span><br/> | <span data-ttu-id="70716-121">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="70716-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="70716-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="70716-122">Minimum supported server</span></span><br/> | <span data-ttu-id="70716-123">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="70716-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="70716-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="70716-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="70716-125"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="70716-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70716-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="70716-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70716-127">**IAnalysisAlternate :: GetRecognitionConfidence, méthode**</span><span class="sxs-lookup"><span data-stu-id="70716-127">**IAnalysisAlternate::GetRecognitionConfidence Method**</span></span>](ianalysisalternate-getrecognitionconfidence.md)
</dt> <dt>

[<span data-ttu-id="70716-128">**IContextNode::GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="70716-128">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="70716-129">Propriétés du nœud de contexte</span><span class="sxs-lookup"><span data-stu-id="70716-129">Context Node Properties</span></span>](context-node-properties.md)
</dt> <dt>

[<span data-ttu-id="70716-130">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="70716-130">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




