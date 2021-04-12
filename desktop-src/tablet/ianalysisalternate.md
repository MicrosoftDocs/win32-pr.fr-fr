---
description: Représente les correspondances possibles pour les mots de reconnaissance de l’écriture manuscrite pour les objets IContextNode.
ms.assetid: a497c140-6166-4309-af0f-851af09015c6
title: Interface IAnalysisAlternate (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8f65b97ca3811212b73c6bdb12e9b889636dd6ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201521"
---
# <a name="ianalysisalternate-interface"></a><span data-ttu-id="d7739-103">Interface IAnalysisAlternate</span><span class="sxs-lookup"><span data-stu-id="d7739-103">IAnalysisAlternate interface</span></span>

<span data-ttu-id="d7739-104">Représente les correspondances possibles pour les mots de reconnaissance de l’écriture manuscrite pour les objets [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="d7739-104">Represents the possible handwriting recognition word matches for [**IContextNode**](icontextnode.md) objects.</span></span>

## <a name="members"></a><span data-ttu-id="d7739-105">Membres</span><span class="sxs-lookup"><span data-stu-id="d7739-105">Members</span></span>

<span data-ttu-id="d7739-106">L’interface **IAnalysisAlternate** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="d7739-106">The **IAnalysisAlternate** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d7739-107">**IAnalysisAlternate** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d7739-107">**IAnalysisAlternate** also has these types of members:</span></span>

-   [<span data-ttu-id="d7739-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d7739-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d7739-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d7739-109">Methods</span></span>

<span data-ttu-id="d7739-110">L’interface **IAnalysisAlternate** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="d7739-110">The **IAnalysisAlternate** interface has these methods.</span></span>



| <span data-ttu-id="d7739-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="d7739-111">Method</span></span>                                                                          | <span data-ttu-id="d7739-112">Description</span><span class="sxs-lookup"><span data-stu-id="d7739-112">Description</span></span>                                                                                                                                                          |
|:--------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d7739-113">**GetAlternateNodes**</span><span class="sxs-lookup"><span data-stu-id="d7739-113">**GetAlternateNodes**</span></span>](ianalysisalternate-getalternatenodes.md)               | <span data-ttu-id="d7739-114">Récupère les objets [**IContextNode**](icontextnode.md) associés à cet autre.</span><span class="sxs-lookup"><span data-stu-id="d7739-114">Retrieves the [**IContextNode**](icontextnode.md) objects that are associated with this alternate.</span></span><br/>                                                       |
| [<span data-ttu-id="d7739-115">**GetRecognitionConfidence**</span><span class="sxs-lookup"><span data-stu-id="d7739-115">**GetRecognitionConfidence**</span></span>](ianalysisalternate-getrecognitionconfidence.md) | <span data-ttu-id="d7739-116">Récupère une valeur qui indique le niveau de confiance de l' [**IInkAnalyzer**](iinkanalyzer.md) dans la précision du **IAnalysisAlternate**.</span><span class="sxs-lookup"><span data-stu-id="d7739-116">Retrieves a value that indicates the level of confidence that the [**IInkAnalyzer**](iinkanalyzer.md) has in the accuracy of the **IAnalysisAlternate**.</span></span><br/> |
| [<span data-ttu-id="d7739-117">**GetRecognizedString**</span><span class="sxs-lookup"><span data-stu-id="d7739-117">**GetRecognizedString**</span></span>](ianalysisalternate-getrecognizedstring.md)           | <span data-ttu-id="d7739-118">Récupère la valeur de chaîne reconnue de l’objet **IAnalysisAlternate** .</span><span class="sxs-lookup"><span data-stu-id="d7739-118">Retrieves the recognized string value of the **IAnalysisAlternate** object.</span></span><br/>                                                                               |
| [<span data-ttu-id="d7739-119">**GetStrokeIds**</span><span class="sxs-lookup"><span data-stu-id="d7739-119">**GetStrokeIds**</span></span>](ianalysisalternate-getstrokeids.md)                         | <span data-ttu-id="d7739-120">Récupère les identificateurs de trait associés à ce **IAnalysisAlternate**.</span><span class="sxs-lookup"><span data-stu-id="d7739-120">Retrieves the stroke identifiers that are associated with this **IAnalysisAlternate**.</span></span><br/>                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="d7739-121">Notes</span><span class="sxs-lookup"><span data-stu-id="d7739-121">Remarks</span></span>

<span data-ttu-id="d7739-122">Il existe de nombreuses variantes dans l’écriture manuscrite des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="d7739-122">There are many variations in users' handwriting.</span></span> <span data-ttu-id="d7739-123">Pour cette raison, les reconnaissance de l’écriture manuscrite peuvent parfois convertir l’écriture manuscrite en texte qui diffère de celui prévu par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d7739-123">For that reason, handwriting recognizers can sometimes convert handwriting into text that is different from what the user intended.</span></span> <span data-ttu-id="d7739-124">Lorsqu’un [**IInkAnalyzer**](iinkanalyzer.md) effectue une analyse sur une collection de traits, le **IInkAnalyzer** recherche l’ensemble de mots le plus probable représenté par l’écriture manuscrite.</span><span class="sxs-lookup"><span data-stu-id="d7739-124">When an [**IInkAnalyzer**](iinkanalyzer.md) performs analysis on a collection of strokes, the **IInkAnalyzer** finds the most likely set of words that the handwriting represents.</span></span> <span data-ttu-id="d7739-125">En outre, le **IInkAnalyzer** trouve également des ensembles d’autres correspondances de reconnaissance, qui sont stockées dans une collection [**IAnalysisAlternates**](ianalysisalternates.md) .</span><span class="sxs-lookup"><span data-stu-id="d7739-125">In addition, the **IInkAnalyzer** also finds sets of alternative recognition matches, which are stored in an [**IAnalysisAlternates**](ianalysisalternates.md) collection.</span></span> <span data-ttu-id="d7739-126">Pour qu’un utilisateur puisse tirer parti des alternatives de reconnaissance, vous devez créer une interface utilisateur qui permet à l’utilisateur de sélectionner le **IAnalysisAlternate** approprié.</span><span class="sxs-lookup"><span data-stu-id="d7739-126">In order for a user to take advantage of recognition alternates, you must create a user interface that allows the user to select the correct **IAnalysisAlternate**.</span></span>

<span data-ttu-id="d7739-127">Les objets **IAnalysisAlternate** sont généralement obtenus par le biais de la [**méthode IInkAnalyzer :: GetAlternates**](iinkanalyzer-getalternates.md).</span><span class="sxs-lookup"><span data-stu-id="d7739-127">**IAnalysisAlternate** objects are generally obtained through [**IInkAnalyzer::GetAlternates Method**](iinkanalyzer-getalternates.md).</span></span> <span data-ttu-id="d7739-128">Le premier objet **IAnalysisAlternate** de la collection est ce que le [**IInkAnalyzer**](iinkanalyzer.md) considère comme étant le plus probable.</span><span class="sxs-lookup"><span data-stu-id="d7739-128">The first **IAnalysisAlternate** object in the collection is what the [**IInkAnalyzer**](iinkanalyzer.md) considers to be the most likely alternate.</span></span>

<span data-ttu-id="d7739-129">Cette interface est équivalente à [System. Windows. Ink. AnalysisCore. AnalysisAlternateBase](/previous-versions/ms610092(v=vs.100)) dans le .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="d7739-129">This interface is equivalent to [System.Windows.Ink.AnalysisCore.AnalysisAlternateBase](/previous-versions/ms610092(v=vs.100)) in the .NET Framework.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7739-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d7739-130">Requirements</span></span>



| <span data-ttu-id="d7739-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d7739-131">Requirement</span></span> | <span data-ttu-id="d7739-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="d7739-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7739-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7739-133">Minimum supported client</span></span><br/> | <span data-ttu-id="d7739-134">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d7739-134">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d7739-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7739-135">Minimum supported server</span></span><br/> | <span data-ttu-id="d7739-136">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7739-136">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="d7739-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="d7739-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7739-138"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d7739-138"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d7739-139">DLL</span><span class="sxs-lookup"><span data-stu-id="d7739-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7739-140"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7739-140"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="d7739-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7739-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7739-142">**IAnalysisAlternates**</span><span class="sxs-lookup"><span data-stu-id="d7739-142">**IAnalysisAlternates**</span></span>](ianalysisalternates.md)
</dt> <dt>

[<span data-ttu-id="d7739-143">**IInkAnalyzer :: GetAlternatesForContextNodes, méthode**</span><span class="sxs-lookup"><span data-stu-id="d7739-143">**IInkAnalyzer::GetAlternatesForContextNodes Method**</span></span>](iinkanalyzer-getalternatesforcontextnodes.md)
</dt> <dt>

[<span data-ttu-id="d7739-144">**IInkAnalyzer :: GetAlternatesForStrokes, méthode**</span><span class="sxs-lookup"><span data-stu-id="d7739-144">**IInkAnalyzer::GetAlternatesForStrokes Method**</span></span>](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="d7739-145">**IInkAnalyzer :: GetAlternates, méthode**</span><span class="sxs-lookup"><span data-stu-id="d7739-145">**IInkAnalyzer::GetAlternates Method**</span></span>](iinkanalyzer-getalternates.md)
</dt> <dt>

[<span data-ttu-id="d7739-146">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="d7739-146">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

