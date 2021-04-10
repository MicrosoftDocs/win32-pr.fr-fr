---
description: Récupère la valeur qui indique si un objet IContextNode est partiellement rempli ou entièrement rempli.
ms.assetid: 13ac3fb2-7baa-48d7-bf8e-f36b4031fbc4
title: 'IContextNode :: GetPartiallyPopulated, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetPartiallyPopulated
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4b05cb8aae681a7302ae7da40a7412cf828fc159
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113386"
---
# <a name="icontextnodegetpartiallypopulated-method"></a><span data-ttu-id="eb39d-103">IContextNode :: GetPartiallyPopulated, méthode</span><span class="sxs-lookup"><span data-stu-id="eb39d-103">IContextNode::GetPartiallyPopulated method</span></span>

<span data-ttu-id="eb39d-104">Récupère la valeur qui indique si un objet [**IContextNode**](icontextnode.md) est partiellement rempli ou entièrement rempli.</span><span class="sxs-lookup"><span data-stu-id="eb39d-104">Retrieves the value that indicates whether an [**IContextNode**](icontextnode.md) object is partially populated or fully populated.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb39d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eb39d-105">Syntax</span></span>


```C++
HRESULT GetPartiallyPopulated(
  [out] VARIANT_BOOL *pfPartiallyPopulated
);
```



## <a name="parameters"></a><span data-ttu-id="eb39d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eb39d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb39d-107">*pfPartiallyPopulated* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="eb39d-107">*pfPartiallyPopulated* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eb39d-108">**Variante \_ TRUE** si cet objet [**IContextNode**](icontextnode.md) ne contient pas de données complètes ; Sinon, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="eb39d-108">**VARIANT\_TRUE** if this [**IContextNode**](icontextnode.md) object does not contain complete data; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb39d-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="eb39d-109">Return value</span></span>

<span data-ttu-id="eb39d-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="eb39d-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="eb39d-111">Notes</span><span class="sxs-lookup"><span data-stu-id="eb39d-111">Remarks</span></span>

<span data-ttu-id="eb39d-112">Utilisez cette méthode lorsque votre application gère sa propre structure de données, qui est synchronisée avec celle du [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="eb39d-112">Use this method when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="eb39d-113">Pour plus d’informations, consultez [Data proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="eb39d-113">For more information, see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eb39d-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eb39d-114">Requirements</span></span>



| <span data-ttu-id="eb39d-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eb39d-115">Requirement</span></span> | <span data-ttu-id="eb39d-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="eb39d-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb39d-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eb39d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="eb39d-118">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eb39d-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="eb39d-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eb39d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="eb39d-120">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="eb39d-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="eb39d-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="eb39d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb39d-122"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="eb39d-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="eb39d-123">DLL</span><span class="sxs-lookup"><span data-stu-id="eb39d-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb39d-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb39d-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="eb39d-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb39d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb39d-126">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="eb39d-126">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="eb39d-127">**IContextNode::SetPartiallyPopulated**</span><span class="sxs-lookup"><span data-stu-id="eb39d-127">**IContextNode::SetPartiallyPopulated**</span></span>](icontextnode-setpartiallypopulated.md)
</dt> <dt>

[<span data-ttu-id="eb39d-128">**IContextNode::CreatePartiallyPopulatedSubNode**</span><span class="sxs-lookup"><span data-stu-id="eb39d-128">**IContextNode::CreatePartiallyPopulatedSubNode**</span></span>](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[<span data-ttu-id="eb39d-129">**\_IAnalysisProxyEvents ::P opulateContextNode**</span><span class="sxs-lookup"><span data-stu-id="eb39d-129">**\_IAnalysisProxyEvents::PopulateContextNode**</span></span>](-ianalysisproxyevents-populatecontextnode.md)
</dt> <dt>

[<span data-ttu-id="eb39d-130">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="eb39d-130">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




