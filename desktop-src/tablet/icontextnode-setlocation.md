---
description: Met à jour la zone de ce IContextNode.
ms.assetid: e7001411-17e4-4f33-af04-dd3220275895
title: 'IContextNode :: SetLocation, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.SetLocation
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 20daefeab7a9e36d5e968d5d14bfa5110d733487
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517511"
---
# <a name="icontextnodesetlocation-method"></a><span data-ttu-id="1888e-103">IContextNode :: SetLocation, méthode</span><span class="sxs-lookup"><span data-stu-id="1888e-103">IContextNode::SetLocation method</span></span>

<span data-ttu-id="1888e-104">Met à jour la zone de ce [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="1888e-104">Updates the area of this [**IContextNode**](icontextnode.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1888e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1888e-105">Syntax</span></span>


```C++
HRESULT SetLocation(
  [in] IAnalysisRegion *pIAnalysisRegion
);
```



## <a name="parameters"></a><span data-ttu-id="1888e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1888e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1888e-107">*pIAnalysisRegion* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1888e-107">*pIAnalysisRegion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1888e-108">[**IAnalysisRegion**](ianalysisregion.md) décrivant la zone dans laquelle définir l’emplacement de l’objet [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="1888e-108">The [**IAnalysisRegion**](ianalysisregion.md) describing the area to which to set the [**IContextNode**](icontextnode.md) object's location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1888e-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1888e-109">Return value</span></span>

<span data-ttu-id="1888e-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="1888e-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1888e-111">Notes</span><span class="sxs-lookup"><span data-stu-id="1888e-111">Remarks</span></span>

<span data-ttu-id="1888e-112">Utilisez cette méthode pour mettre à jour l’emplacement du nœud de contexte (consultez [**IContextNode :: GetLocation**](icontextnode-getlocation.md)).</span><span class="sxs-lookup"><span data-stu-id="1888e-112">Use this method to update the context node's location (see [**IContextNode::GetLocation**](icontextnode-getlocation.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="1888e-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1888e-113">Requirements</span></span>



| <span data-ttu-id="1888e-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1888e-114">Requirement</span></span> | <span data-ttu-id="1888e-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="1888e-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1888e-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1888e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1888e-117">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1888e-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1888e-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1888e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1888e-119">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="1888e-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="1888e-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="1888e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1888e-121"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="1888e-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="1888e-122">DLL</span><span class="sxs-lookup"><span data-stu-id="1888e-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1888e-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1888e-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="1888e-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1888e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1888e-125">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="1888e-125">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="1888e-126">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="1888e-126">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="1888e-127">**IContextNode::GetLocation**</span><span class="sxs-lookup"><span data-stu-id="1888e-127">**IContextNode::GetLocation**</span></span>](icontextnode-getlocation.md)
</dt> <dt>

[<span data-ttu-id="1888e-128">**IContextNode::GetPartiallyPopulated**</span><span class="sxs-lookup"><span data-stu-id="1888e-128">**IContextNode::GetPartiallyPopulated**</span></span>](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[<span data-ttu-id="1888e-129">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="1888e-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




