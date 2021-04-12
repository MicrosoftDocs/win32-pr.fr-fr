---
description: Récupère le type du trait spécifié.
ms.assetid: bbd0bc23-89f9-4033-bc32-f9bd737c960c
title: 'IInkAnalyzer :: GetStrokeType, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetStrokeType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d9358b2583f31fd26310ea880470f36404021fec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201497"
---
# <a name="iinkanalyzergetstroketype-method"></a><span data-ttu-id="2db60-103">IInkAnalyzer :: GetStrokeType, méthode</span><span class="sxs-lookup"><span data-stu-id="2db60-103">IInkAnalyzer::GetStrokeType method</span></span>

<span data-ttu-id="2db60-104">Récupère le type du trait spécifié.</span><span class="sxs-lookup"><span data-stu-id="2db60-104">Retrieves the type of the specified stroke.</span></span>

## <a name="syntax"></a><span data-ttu-id="2db60-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2db60-105">Syntax</span></span>


```C++
HRESULT GetStrokeType(
  [in]  LONG       lStrokeId,
  [out] StrokeType *pStrokeType
);
```



## <a name="parameters"></a><span data-ttu-id="2db60-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2db60-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2db60-107">*lStrokeId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2db60-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2db60-108">Identificateur du trait.</span><span class="sxs-lookup"><span data-stu-id="2db60-108">The stroke identifier.</span></span>

</dd> <dt>

<span data-ttu-id="2db60-109">*pStrokeType* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2db60-109">*pStrokeType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2db60-110">Classification du trait spécifié.</span><span class="sxs-lookup"><span data-stu-id="2db60-110">The classification of the specified stroke.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2db60-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2db60-111">Return value</span></span>

<span data-ttu-id="2db60-112">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="2db60-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2db60-113">Notes</span><span class="sxs-lookup"><span data-stu-id="2db60-113">Remarks</span></span>

<span data-ttu-id="2db60-114">Si le type du trait est la valeur [**StrokeType**](stroketype.md) StrokeType non \_ classifiée, le [**IInkAnalyzer**](iinkanalyzer.md) classe le trait pendant l’analyse de l’encre.</span><span class="sxs-lookup"><span data-stu-id="2db60-114">If the stroke's type is the [**StrokeType**](stroketype.md) value StrokeType\_Unclassified, the [**IInkAnalyzer**](iinkanalyzer.md) classifies the stroke during ink analysis.</span></span> <span data-ttu-id="2db60-115">Dans le cas contraire, le **IInkAnalyzer** utilise le type défini sur le trait.</span><span class="sxs-lookup"><span data-stu-id="2db60-115">Otherwise, the **IInkAnalyzer** uses the type set on the stroke.</span></span>

<span data-ttu-id="2db60-116">[**IInkAnalyzer**](iinkanalyzer.md) ne définit pas la valeur de type de trait dans le cadre de l’analyse de l’encre.</span><span class="sxs-lookup"><span data-stu-id="2db60-116">The [**IInkAnalyzer**](iinkanalyzer.md) does not set the stroke type value as part of ink analysis.</span></span> <span data-ttu-id="2db60-117">Pour spécifier ou modifier le type de trait, utilisez la méthode [**IInkAnalyzer :: SetStrokeType**](iinkanalyzer-setstroketype.md) ou [**IInkAnalyzer :: SetStrokesType**](iinkanalyzer-setstrokestype.md).</span><span class="sxs-lookup"><span data-stu-id="2db60-117">To specify or change the stroke type, use [**IInkAnalyzer::SetStrokeType Method**](iinkanalyzer-setstroketype.md) or [**IInkAnalyzer::SetStrokesType Method**](iinkanalyzer-setstrokestype.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2db60-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2db60-118">Requirements</span></span>



| <span data-ttu-id="2db60-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2db60-119">Requirement</span></span> | <span data-ttu-id="2db60-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="2db60-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2db60-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2db60-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2db60-122">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2db60-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2db60-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2db60-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2db60-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="2db60-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="2db60-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="2db60-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2db60-126"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="2db60-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="2db60-127">DLL</span><span class="sxs-lookup"><span data-stu-id="2db60-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2db60-128"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2db60-128"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="2db60-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2db60-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2db60-130">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="2db60-130">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="2db60-131">**IInkAnalyzer :: SetStrokeType, méthode**</span><span class="sxs-lookup"><span data-stu-id="2db60-131">**IInkAnalyzer::SetStrokeType Method**</span></span>](iinkanalyzer-setstroketype.md)
</dt> <dt>

[<span data-ttu-id="2db60-132">**IInkAnalyzer :: SetStrokesType, méthode**</span><span class="sxs-lookup"><span data-stu-id="2db60-132">**IInkAnalyzer::SetStrokesType Method**</span></span>](iinkanalyzer-setstrokestype.md)
</dt> <dt>

[<span data-ttu-id="2db60-133">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="2db60-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




