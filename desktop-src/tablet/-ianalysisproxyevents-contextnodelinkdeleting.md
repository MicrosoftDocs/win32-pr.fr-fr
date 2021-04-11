---
description: Se produit avant que le IInkAnalyzer supprime un objet IContextLink entre deux objets IContextNode.
ms.assetid: bc9716b8-8793-4886-aff4-d880024129a6
title: '_IAnalysisProxyEvents :: ContextNodeLinkDeleting, événement (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeLinkDeleting
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: bc4ba9586fc4c520b9ee44b039bd56f8ef2ade3c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104211295"
---
# <a name="_ianalysisproxyeventscontextnodelinkdeleting-event"></a><span data-ttu-id="471a9-103">\_Événement IAnalysisProxyEvents :: ContextNodeLinkDeleting</span><span class="sxs-lookup"><span data-stu-id="471a9-103">\_IAnalysisProxyEvents::ContextNodeLinkDeleting event</span></span>

<span data-ttu-id="471a9-104">Se produit avant que le [**IInkAnalyzer**](iinkanalyzer.md) supprime un objet [**IContextLink**](icontextlink.md) entre deux objets [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="471a9-104">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) deletes a [**IContextLink**](icontextlink.md) object between two [**IContextNode**](icontextnode.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="471a9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="471a9-105">Syntax</span></span>


```C++
HRESULT ContextNodeLinkDeleting(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextLink *pContextLinkToBeDeleted
);
```



## <a name="parameters"></a><span data-ttu-id="471a9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="471a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="471a9-107">*pInkAnalyzer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="471a9-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="471a9-108">[**IInkAnalyzer**](iinkanalyzer.md) supprimant le lien.</span><span class="sxs-lookup"><span data-stu-id="471a9-108">The [**IInkAnalyzer**](iinkanalyzer.md) deleting the link.</span></span>

</dd> <dt>

<span data-ttu-id="471a9-109">*pContextLinkToBeDeleted* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="471a9-109">*pContextLinkToBeDeleted* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="471a9-110">Objet [**IContextLink**](icontextlink.md) à supprimer.</span><span class="sxs-lookup"><span data-stu-id="471a9-110">The [**IContextLink**](icontextlink.md) object to be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="471a9-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="471a9-111">Return value</span></span>

<span data-ttu-id="471a9-112">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="471a9-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="471a9-113">Notes</span><span class="sxs-lookup"><span data-stu-id="471a9-113">Remarks</span></span>

<span data-ttu-id="471a9-114">Utilisez cet événement lorsque votre application gère sa propre structure de données, qui est synchronisée avec celle du [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="471a9-114">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="471a9-115">Cet événement se produit pendant la phase de rapprochement de l’analyse de l’encre, ou en réponse à une méthode **IInkAnalyzer** qui supprime un [**IContextLink**](icontextlink.md) d’un [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="471a9-115">This event occurs during the reconcile phase of ink analysis, or in response to an **IInkAnalyzer** method that removes an [**IContextLink**](icontextlink.md) from an [**IContextNode**](icontextnode.md).</span></span>

<span data-ttu-id="471a9-116">Pour plus d’informations sur la synchronisation des données de votre application avec [**IInkAnalyzer**](iinkanalyzer.md), consultez [Data proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="471a9-116">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="471a9-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="471a9-117">Requirements</span></span>



| <span data-ttu-id="471a9-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="471a9-118">Requirement</span></span> | <span data-ttu-id="471a9-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="471a9-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="471a9-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="471a9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="471a9-121">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="471a9-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="471a9-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="471a9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="471a9-123">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="471a9-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="471a9-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="471a9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="471a9-125"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="471a9-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="471a9-126">DLL</span><span class="sxs-lookup"><span data-stu-id="471a9-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="471a9-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="471a9-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="471a9-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="471a9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="471a9-129">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="471a9-129">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="471a9-130">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="471a9-130">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="471a9-131">**IContextLink**</span><span class="sxs-lookup"><span data-stu-id="471a9-131">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="471a9-132">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="471a9-132">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="471a9-133">**IInkAnalyzer :: Analyze, méthode**</span><span class="sxs-lookup"><span data-stu-id="471a9-133">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="471a9-134">**IInkAnalyzer :: BackgroundAnalyze, méthode**</span><span class="sxs-lookup"><span data-stu-id="471a9-134">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="471a9-135">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="471a9-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




