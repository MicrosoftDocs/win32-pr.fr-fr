---
description: Contient une collection d’objets qui implémentent l’interface IInkAnalysisRecognizer et qui représentent la capacité de reconnaître l’écriture manuscrite, les objets ou les gestes.
ms.assetid: d9264c9f-bf75-493e-8e41-57ea69955e6b
title: Interface IInkAnalysisRecognizers (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizers
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ba9bbcd029803e613fb27d351de554c013c02616
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318462"
---
# <a name="iinkanalysisrecognizers-interface"></a><span data-ttu-id="8b4b8-103">Interface IInkAnalysisRecognizers</span><span class="sxs-lookup"><span data-stu-id="8b4b8-103">IInkAnalysisRecognizers interface</span></span>

<span data-ttu-id="8b4b8-104">Contient une collection d’objets qui implémentent l’interface [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) et qui représentent la capacité de reconnaître l’écriture manuscrite, les objets ou les gestes.</span><span class="sxs-lookup"><span data-stu-id="8b4b8-104">Contains a collection of objects that implement the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) interface and that represent the ability to recognize handwriting, objects, or gestures.</span></span>

## <a name="members"></a><span data-ttu-id="8b4b8-105">Membres</span><span class="sxs-lookup"><span data-stu-id="8b4b8-105">Members</span></span>

<span data-ttu-id="8b4b8-106">L’interface **IInkAnalysisRecognizers** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="8b4b8-106">The **IInkAnalysisRecognizers** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8b4b8-107">**IInkAnalysisRecognizers** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8b4b8-107">**IInkAnalysisRecognizers** also has these types of members:</span></span>

-   [<span data-ttu-id="8b4b8-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8b4b8-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8b4b8-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8b4b8-109">Methods</span></span>

<span data-ttu-id="8b4b8-110">L’interface **IInkAnalysisRecognizers** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="8b4b8-110">The **IInkAnalysisRecognizers** interface has these methods.</span></span>



| <span data-ttu-id="8b4b8-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="8b4b8-111">Method</span></span>                                                                               | <span data-ttu-id="8b4b8-112">Description</span><span class="sxs-lookup"><span data-stu-id="8b4b8-112">Description</span></span>                                                                                                             |
|:-------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8b4b8-113">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="8b4b8-113">**GetCount**</span></span>](iinkanalysisrecognizers-getcount.md)                                 | <span data-ttu-id="8b4b8-114">Récupère le nombre d’objets [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) dans cette collection.</span><span class="sxs-lookup"><span data-stu-id="8b4b8-114">Retrieves the number of [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) objects in this collection.</span></span><br/> |
| [<span data-ttu-id="8b4b8-115">**GetInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="8b4b8-115">**GetInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizers-getinkanalysisrecognizer.md) | <span data-ttu-id="8b4b8-116">Récupère le [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="8b4b8-116">Retrieves the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) at the specified index.</span></span><br/>               |



 

## <a name="remarks"></a><span data-ttu-id="8b4b8-117">Notes</span><span class="sxs-lookup"><span data-stu-id="8b4b8-117">Remarks</span></span>

<span data-ttu-id="8b4b8-118">La méthode [**IInkAnalyzer :: GetInkAnalysisRecognizersByPriority**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) méthode de [**IInkAnalyzer**](iinkanalyzer.md) retourne une collection **IInkAnalysisRecognizers** contenant les détecteurs d’encre disponibles sur le Tablet PC actuel.</span><span class="sxs-lookup"><span data-stu-id="8b4b8-118">The [**IInkAnalyzer::GetInkAnalysisRecognizersByPriority Method**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) method of [**IInkAnalyzer**](iinkanalyzer.md) returns an **IInkAnalysisRecognizers** collection containing the ink recognizers available on the current Tablet PC.</span></span>

<span data-ttu-id="8b4b8-119">Pour un module de reconnaissance de langage, la méthode [**IInkAnalysisRecognizer :: GetLanguages**](iinkanalysisrecognizer-getlanguages.md) retourne un tableau non vide.</span><span class="sxs-lookup"><span data-stu-id="8b4b8-119">For a language recognizer, the [**IInkAnalysisRecognizer::GetLanguages**](iinkanalysisrecognizer-getlanguages.md) method returns a non-empty array.</span></span> <span data-ttu-id="8b4b8-120">Pour les modules de reconnaissance de mouvement et d’objet, la méthode **IInkAnalysisRecognizer :: GetLanguages** retourne un tableau vide.</span><span class="sxs-lookup"><span data-stu-id="8b4b8-120">For both gesture recognizers and object recognizers, the **IInkAnalysisRecognizer::GetLanguages** method returns an empty array.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b4b8-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8b4b8-121">Requirements</span></span>



| <span data-ttu-id="8b4b8-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8b4b8-122">Requirement</span></span> | <span data-ttu-id="8b4b8-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="8b4b8-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b4b8-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8b4b8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="8b4b8-125">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8b4b8-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8b4b8-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8b4b8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="8b4b8-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="8b4b8-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="8b4b8-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="8b4b8-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b4b8-129"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="8b4b8-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8b4b8-130">DLL</span><span class="sxs-lookup"><span data-stu-id="8b4b8-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b4b8-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b4b8-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="8b4b8-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b4b8-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b4b8-133">**IInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="8b4b8-133">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="8b4b8-134">**IInkAnalyzer :: GetInkAnalysisRecognizersByPriority, méthode**</span><span class="sxs-lookup"><span data-stu-id="8b4b8-134">**IInkAnalyzer::GetInkAnalysisRecognizersByPriority Method**</span></span>](iinkanalyzer-getinkanalysisrecognizersbypriority.md)
</dt> <dt>

[<span data-ttu-id="8b4b8-135">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="8b4b8-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

