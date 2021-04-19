---
description: Se produit après que le IInkAnalyzer a mis à jour une ou plusieurs propriétés d’un objet IContextNode.
ms.assetid: f626c263-31a4-45ee-ae04-3251eac0d652
title: '_IAnalysisProxyEvents :: ContextNodePropertiesUpdated, événement (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodePropertiesUpdated
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fa035b89c531f3b2d230ab849ba20b945dd2d25c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106531260"
---
# <a name="_ianalysisproxyeventscontextnodepropertiesupdated-event"></a><span data-ttu-id="d46c7-103">\_Événement IAnalysisProxyEvents :: ContextNodePropertiesUpdated</span><span class="sxs-lookup"><span data-stu-id="d46c7-103">\_IAnalysisProxyEvents::ContextNodePropertiesUpdated event</span></span>

<span data-ttu-id="d46c7-104">Se produit après que le [**IInkAnalyzer**](iinkanalyzer.md) a mis à jour une ou plusieurs propriétés d’un objet [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="d46c7-104">Occurs after the [**IInkAnalyzer**](iinkanalyzer.md) updates one or more properties of an [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d46c7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d46c7-105">Syntax</span></span>


```C++
HRESULT ContextNodePropertiesUpdated(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeUpdated
);
```



## <a name="parameters"></a><span data-ttu-id="d46c7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d46c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d46c7-107">*pInkAnalyzer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d46c7-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d46c7-108">Objet [**IInkAnalyzer**](iinkanalyzer.md) qui met à jour les propriétés.</span><span class="sxs-lookup"><span data-stu-id="d46c7-108">The [**IInkAnalyzer**](iinkanalyzer.md) object updating the properties.</span></span>

</dd> <dt>

<span data-ttu-id="d46c7-109">*pContextNodeUpdated* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d46c7-109">*pContextNodeUpdated* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d46c7-110">Objet [**IContextNode**](icontextnode.md) dont les propriétés sont mises à jour.</span><span class="sxs-lookup"><span data-stu-id="d46c7-110">The [**IContextNode**](icontextnode.md) object whose properties are updated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d46c7-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d46c7-111">Return value</span></span>

<span data-ttu-id="d46c7-112">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="d46c7-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d46c7-113">Notes</span><span class="sxs-lookup"><span data-stu-id="d46c7-113">Remarks</span></span>

<span data-ttu-id="d46c7-114">Utilisez cet événement lorsque votre application gère sa propre structure de données, qui est synchronisée avec celle du [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="d46c7-114">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="d46c7-115">Cet événement se produit pendant la phase de rapprochement de l’analyse de l’encre, ou en réponse à une méthode d’analyseur d’encre qui modifie les propriétés d’un [**IContextNode**](icontextnode.md) (consultez [**IContextNode :: GetPropertyData**](icontextnode-getpropertydata.md)).</span><span class="sxs-lookup"><span data-stu-id="d46c7-115">This event occurs during the reconcile phase of ink analysis, or in response to an ink analyzer method that changes the properties of an [**IContextNode**](icontextnode.md) (see [**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md)).</span></span>

<span data-ttu-id="d46c7-116">Pour plus d’informations sur la synchronisation des données de votre application avec [**IInkAnalyzer**](iinkanalyzer.md), consultez [Data proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="d46c7-116">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d46c7-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d46c7-117">Requirements</span></span>



| <span data-ttu-id="d46c7-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d46c7-118">Requirement</span></span> | <span data-ttu-id="d46c7-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="d46c7-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d46c7-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d46c7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d46c7-121">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d46c7-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d46c7-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d46c7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d46c7-123">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d46c7-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="d46c7-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="d46c7-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d46c7-125"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d46c7-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d46c7-126">DLL</span><span class="sxs-lookup"><span data-stu-id="d46c7-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d46c7-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d46c7-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="d46c7-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d46c7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d46c7-129">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="d46c7-129">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="d46c7-130">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="d46c7-130">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="d46c7-131">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="d46c7-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="d46c7-132">**IInkAnalyzer :: Analyze, méthode**</span><span class="sxs-lookup"><span data-stu-id="d46c7-132">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="d46c7-133">**IInkAnalyzer :: BackgroundAnalyze, méthode**</span><span class="sxs-lookup"><span data-stu-id="d46c7-133">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="d46c7-134">Propriétés du nœud de contexte</span><span class="sxs-lookup"><span data-stu-id="d46c7-134">Context Node Properties</span></span>](context-node-properties.md)
</dt> <dt>

[<span data-ttu-id="d46c7-135">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="d46c7-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




