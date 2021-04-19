---
description: Se produit avant que l’analyseur d’encre ajoute un objet IContextLink entre deux objets IContextNode.
ms.assetid: ec56cb8e-5154-45ee-911d-e2a240d19dc3
title: '_IAnalysisProxyEvents :: ContextNodeLinkAdding, événement (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeLinkAdding
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 341c551064869532e8b51ddecdbe1d5a78878abd
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106523762"
---
# <a name="_ianalysisproxyeventscontextnodelinkadding-event"></a><span data-ttu-id="33fc5-103">\_Événement IAnalysisProxyEvents :: ContextNodeLinkAdding</span><span class="sxs-lookup"><span data-stu-id="33fc5-103">\_IAnalysisProxyEvents::ContextNodeLinkAdding event</span></span>

<span data-ttu-id="33fc5-104">Se produit avant que l’analyseur d’encre ajoute un objet [**IContextLink**](icontextlink.md) entre deux objets [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="33fc5-104">Occurs before the ink analyzer adds an [**IContextLink**](icontextlink.md) object between two [**IContextNode**](icontextnode.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="33fc5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="33fc5-105">Syntax</span></span>


```C++
HRESULT ContextNodeLinkAdding(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextLink *pContextLinkToBeAdded
);
```



## <a name="parameters"></a><span data-ttu-id="33fc5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="33fc5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33fc5-107">*pInkAnalyzer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="33fc5-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33fc5-108">[**IInkAnalyzer**](iinkanalyzer.md) ajoutant le lien.</span><span class="sxs-lookup"><span data-stu-id="33fc5-108">The [**IInkAnalyzer**](iinkanalyzer.md) adding the link.</span></span>

</dd> <dt>

<span data-ttu-id="33fc5-109">*pContextLinkToBeAdded* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="33fc5-109">*pContextLinkToBeAdded* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33fc5-110">Objet [**IContextLink**](icontextlink.md) à ajouter.</span><span class="sxs-lookup"><span data-stu-id="33fc5-110">The [**IContextLink**](icontextlink.md) object to be added.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33fc5-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="33fc5-111">Return value</span></span>

<span data-ttu-id="33fc5-112">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="33fc5-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="33fc5-113">Notes</span><span class="sxs-lookup"><span data-stu-id="33fc5-113">Remarks</span></span>

<span data-ttu-id="33fc5-114">Utilisez cet événement lorsque votre application gère sa propre structure de données, qui est synchronisée avec celle du [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="33fc5-114">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="33fc5-115">Cet événement se produit pendant la phase de rapprochement de l’analyse de l’encre, ou en réponse à une méthode d’analyseur d’encre qui ajoute un nouveau [**IContextLink**](icontextlink.md) à un [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="33fc5-115">This event occurs during the reconcile phase of ink analysis, or in response to an ink analyzer method that adds a new [**IContextLink**](icontextlink.md) to an [**IContextNode**](icontextnode.md).</span></span>

<span data-ttu-id="33fc5-116">Pour plus d’informations sur la synchronisation des données de votre application avec [**IInkAnalyzer**](iinkanalyzer.md), consultez [Data proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="33fc5-116">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="33fc5-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="33fc5-117">Requirements</span></span>



| <span data-ttu-id="33fc5-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="33fc5-118">Requirement</span></span> | <span data-ttu-id="33fc5-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="33fc5-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33fc5-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33fc5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="33fc5-121">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="33fc5-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="33fc5-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33fc5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="33fc5-123">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="33fc5-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="33fc5-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="33fc5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="33fc5-125"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="33fc5-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="33fc5-126">DLL</span><span class="sxs-lookup"><span data-stu-id="33fc5-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33fc5-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33fc5-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="33fc5-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33fc5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33fc5-129">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="33fc5-129">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="33fc5-130">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="33fc5-130">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="33fc5-131">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="33fc5-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="33fc5-132">**IContextLink**</span><span class="sxs-lookup"><span data-stu-id="33fc5-132">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="33fc5-133">**IInkAnalyzer :: Analyze, méthode**</span><span class="sxs-lookup"><span data-stu-id="33fc5-133">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="33fc5-134">**IInkAnalyzer :: BackgroundAnalyze, méthode**</span><span class="sxs-lookup"><span data-stu-id="33fc5-134">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="33fc5-135">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="33fc5-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




