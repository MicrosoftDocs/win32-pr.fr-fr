---
description: Contient une collection d’objets qui implémentent l’interface IAnalysisAlternate et qui sont le résultat de l’analyse de l’encre.
ms.assetid: 53802a62-4425-40fd-bf48-0da55ea8ffbe
title: Interface IAnalysisAlternates (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternates
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4e43feaa40f519707531894936bf34ce19e57723
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515870"
---
# <a name="ianalysisalternates-interface"></a><span data-ttu-id="e9483-103">Interface IAnalysisAlternates</span><span class="sxs-lookup"><span data-stu-id="e9483-103">IAnalysisAlternates interface</span></span>

<span data-ttu-id="e9483-104">Contient une collection d’objets qui implémentent l’interface [**IAnalysisAlternate**](ianalysisalternate.md) et qui sont le résultat de l’analyse de l’encre.</span><span class="sxs-lookup"><span data-stu-id="e9483-104">Contains a collection of objects that implement the [**IAnalysisAlternate**](ianalysisalternate.md) interface and that are the result of ink analysis.</span></span>

## <a name="members"></a><span data-ttu-id="e9483-105">Membres</span><span class="sxs-lookup"><span data-stu-id="e9483-105">Members</span></span>

<span data-ttu-id="e9483-106">L’interface **IAnalysisAlternates** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="e9483-106">The **IAnalysisAlternates** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e9483-107">**IAnalysisAlternates** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e9483-107">**IAnalysisAlternates** also has these types of members:</span></span>

-   [<span data-ttu-id="e9483-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e9483-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e9483-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e9483-109">Methods</span></span>

<span data-ttu-id="e9483-110">L’interface **IAnalysisAlternates** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="e9483-110">The **IAnalysisAlternates** interface has these methods.</span></span>



| <span data-ttu-id="e9483-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="e9483-111">Method</span></span>                                                                   | <span data-ttu-id="e9483-112">Description</span><span class="sxs-lookup"><span data-stu-id="e9483-112">Description</span></span>                                                                                                                                      |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e9483-113">**GetAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="e9483-113">**GetAnalysisAlternate**</span></span>](ianalysisalternates-getanalysisalternate.md) | <span data-ttu-id="e9483-114">Récupère l’objet [**IAnalysisAlternate**](ianalysisalternate.md) à l’index spécifié dans la collection.</span><span class="sxs-lookup"><span data-stu-id="e9483-114">Retrieves the [**IAnalysisAlternate**](ianalysisalternate.md) object at the specified index within the collection.</span></span><br/>                   |
| [<span data-ttu-id="e9483-115">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="e9483-115">**GetCount**</span></span>](ianalysisalternates-getcount.md)                         | <span data-ttu-id="e9483-116">Récupère le nombre d’objets [**IAnalysisAlternate**](ianalysisalternate.md) contenus dans la collection **IAnalysisAlternates** .</span><span class="sxs-lookup"><span data-stu-id="e9483-116">Retrieves the number of [**IAnalysisAlternate**](ianalysisalternate.md) objects contained in the **IAnalysisAlternates** collection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e9483-117">Notes</span><span class="sxs-lookup"><span data-stu-id="e9483-117">Remarks</span></span>

<span data-ttu-id="e9483-118">Cette interface est équivalente à la classe [**System. Windows. Ink. AnalysisCore. AnalysisAlternateBaseCollection**](/previous-versions/ms610094(v=vs.100)) dans la .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="e9483-118">This interface is equivalent to the [**System.Windows.Ink.AnalysisCore.AnalysisAlternateBaseCollection**](/previous-versions/ms610094(v=vs.100)) class in the .NET Framework.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9483-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e9483-119">Requirements</span></span>



| <span data-ttu-id="e9483-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e9483-120">Requirement</span></span> | <span data-ttu-id="e9483-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="e9483-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9483-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e9483-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e9483-123">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e9483-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e9483-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e9483-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e9483-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e9483-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="e9483-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="e9483-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9483-127"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e9483-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e9483-128">DLL</span><span class="sxs-lookup"><span data-stu-id="e9483-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9483-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9483-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="e9483-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e9483-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9483-131">**IAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="e9483-131">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="e9483-132">**IInkAnalyzer :: GetAlternates, méthode**</span><span class="sxs-lookup"><span data-stu-id="e9483-132">**IInkAnalyzer::GetAlternates Method**</span></span>](iinkanalyzer-getalternates.md)
</dt> <dt>

[<span data-ttu-id="e9483-133">**IInkAnalyzer :: GetAlternatesForContextNodes, méthode**</span><span class="sxs-lookup"><span data-stu-id="e9483-133">**IInkAnalyzer::GetAlternatesForContextNodes Method**</span></span>](iinkanalyzer-getalternatesforcontextnodes.md)
</dt> <dt>

[<span data-ttu-id="e9483-134">**IInkAnalyzer :: GetAlternatesForStrokes, méthode**</span><span class="sxs-lookup"><span data-stu-id="e9483-134">**IInkAnalyzer::GetAlternatesForStrokes Method**</span></span>](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="e9483-135">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="e9483-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

