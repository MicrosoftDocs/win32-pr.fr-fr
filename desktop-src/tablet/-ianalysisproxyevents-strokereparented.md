---
description: Se produit lorsque le IInkAnalyzer déplace un trait d’un objet IContextNode à un autre.
ms.assetid: a90214af-c3ea-4e2a-94b4-bb5746a2b476
title: '_IAnalysisProxyEvents :: StrokeReparented, événement (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.StrokeReparented
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a587acb6534641d5d64981ab25247b0e23e4f347
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106530927"
---
# <a name="_ianalysisproxyeventsstrokereparented-event"></a><span data-ttu-id="26ed3-103">\_Événement IAnalysisProxyEvents :: StrokeReparented</span><span class="sxs-lookup"><span data-stu-id="26ed3-103">\_IAnalysisProxyEvents::StrokeReparented event</span></span>

<span data-ttu-id="26ed3-104">Se produit lorsque le [**IInkAnalyzer**](iinkanalyzer.md) déplace un trait d’un objet [**IContextNode**](icontextnode.md) à un autre.</span><span class="sxs-lookup"><span data-stu-id="26ed3-104">Occurs when the [**IInkAnalyzer**](iinkanalyzer.md) moves a stroke from one [**IContextNode**](icontextnode.md) object to another.</span></span>

## <a name="syntax"></a><span data-ttu-id="26ed3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="26ed3-105">Syntax</span></span>


```C++
HRESULT StrokeReparented(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] LONG         lStrokeIdToMove,
  [in] IContextNode *pSourceContextNode,
  [in] IContextNode *pDestinationContextNode
);
```



## <a name="parameters"></a><span data-ttu-id="26ed3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="26ed3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26ed3-107">*pInkAnalyzer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="26ed3-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26ed3-108">Objet [**IInkAnalyzer**](iinkanalyzer.md) qui déplace le trait.</span><span class="sxs-lookup"><span data-stu-id="26ed3-108">The [**IInkAnalyzer**](iinkanalyzer.md) object moving the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="26ed3-109">*lStrokeIdToMove* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="26ed3-109">*lStrokeIdToMove* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26ed3-110">Identificateur du trait à déplacer.</span><span class="sxs-lookup"><span data-stu-id="26ed3-110">The identifier of the stroke to move.</span></span>

</dd> <dt>

<span data-ttu-id="26ed3-111">*pSourceContextNode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="26ed3-111">*pSourceContextNode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26ed3-112">Objet [**IContextNode**](icontextnode.md) à partir duquel le trait est déplacé.</span><span class="sxs-lookup"><span data-stu-id="26ed3-112">The [**IContextNode**](icontextnode.md) object from which the stroke is moved.</span></span>

</dd> <dt>

<span data-ttu-id="26ed3-113">*pDestinationContextNode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="26ed3-113">*pDestinationContextNode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26ed3-114">Objet [**IContextNode**](icontextnode.md) vers lequel le trait est déplacé.</span><span class="sxs-lookup"><span data-stu-id="26ed3-114">The [**IContextNode**](icontextnode.md) object to which the stroke is moved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26ed3-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="26ed3-115">Return value</span></span>

<span data-ttu-id="26ed3-116">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="26ed3-116">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="26ed3-117">Notes</span><span class="sxs-lookup"><span data-stu-id="26ed3-117">Remarks</span></span>

<span data-ttu-id="26ed3-118">Utilisez cet événement lorsque votre application gère sa propre structure de données, qui est synchronisée avec celle du [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="26ed3-118">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="26ed3-119">Cet événement se produit pendant la phase de rapprochement de l’analyse de l’encre, ou en réponse à une méthode **IInkAnalyzer** qui déplace les données de trait d’un [**IContextNode**](icontextnode.md) vers un autre.</span><span class="sxs-lookup"><span data-stu-id="26ed3-119">This event occurs during the reconcile phase of ink analysis, or in response to an **IInkAnalyzer** method that moves stroke data from one [**IContextNode**](icontextnode.md) to another.</span></span>

<span data-ttu-id="26ed3-120">Pour plus d’informations sur la synchronisation des données de votre application avec [**IInkAnalyzer**](iinkanalyzer.md), consultez [Data proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="26ed3-120">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="26ed3-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="26ed3-121">Requirements</span></span>



| <span data-ttu-id="26ed3-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="26ed3-122">Requirement</span></span> | <span data-ttu-id="26ed3-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="26ed3-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26ed3-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26ed3-124">Minimum supported client</span></span><br/> | <span data-ttu-id="26ed3-125">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="26ed3-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="26ed3-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26ed3-126">Minimum supported server</span></span><br/> | <span data-ttu-id="26ed3-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="26ed3-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="26ed3-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="26ed3-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="26ed3-129"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="26ed3-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="26ed3-130">DLL</span><span class="sxs-lookup"><span data-stu-id="26ed3-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26ed3-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26ed3-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="26ed3-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26ed3-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26ed3-133">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="26ed3-133">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="26ed3-134">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="26ed3-134">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="26ed3-135">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="26ed3-135">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="26ed3-136">**IInkAnalyzer :: Analyze, méthode**</span><span class="sxs-lookup"><span data-stu-id="26ed3-136">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="26ed3-137">**IInkAnalyzer :: BackgroundAnalyze, méthode**</span><span class="sxs-lookup"><span data-stu-id="26ed3-137">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="26ed3-138">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="26ed3-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




