---
description: Retourne l’identificateur de paramètres régionaux du trait spécifié.
ms.assetid: a5fb9b7a-ed3e-4552-9412-39529203bd81
title: 'IInkAnalyzer :: GetStrokeLanguageId, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetStrokeLanguageId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a231dde453467ad2973d729fa068cedcc35151c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751804"
---
# <a name="iinkanalyzergetstrokelanguageid-method"></a><span data-ttu-id="a8941-103">IInkAnalyzer :: GetStrokeLanguageId, méthode</span><span class="sxs-lookup"><span data-stu-id="a8941-103">IInkAnalyzer::GetStrokeLanguageId method</span></span>

<span data-ttu-id="a8941-104">Retourne l’identificateur de paramètres régionaux du trait spécifié.</span><span class="sxs-lookup"><span data-stu-id="a8941-104">Returns the locale identifier of the specified stroke.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8941-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a8941-105">Syntax</span></span>


```C++
HRESULT GetStrokeLanguageId(
  [in]  LONG lStrokeId,
  [out] LONG *lStrokeLCID
);
```



## <a name="parameters"></a><span data-ttu-id="a8941-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a8941-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8941-107">*lStrokeId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a8941-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8941-108">Identificateur du trait.</span><span class="sxs-lookup"><span data-stu-id="a8941-108">The stroke identifier.</span></span>

</dd> <dt>

<span data-ttu-id="a8941-109">*lStrokeLCID* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a8941-109">*lStrokeLCID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a8941-110">Identificateur de paramètres régionaux pour le trait spécifié.</span><span class="sxs-lookup"><span data-stu-id="a8941-110">The locale identifier for the specified stroke.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8941-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a8941-111">Return value</span></span>

<span data-ttu-id="a8941-112">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="a8941-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a8941-113">Notes</span><span class="sxs-lookup"><span data-stu-id="a8941-113">Remarks</span></span>

<span data-ttu-id="a8941-114">Les paramètres régionaux du trait sont définis lorsque vous ajoutez le trait en appelant la méthode [**IInkAnalyzer :: AddStroke**](iinkanalyzer-addstroke.md), méthode [**IInkAnalyzer :: AddStrokeForLanguage**](iinkanalyzer-addstrokeforlanguage.md), [**IInkAnalyzer :: AddStrokes**](iinkanalyzer-addstrokes.md)ou [**IInkAnalyzer :: AddStrokesForLanguage**](iinkanalyzer-addstrokesforlanguage.md).</span><span class="sxs-lookup"><span data-stu-id="a8941-114">The stroke's locale is set when you add the stroke by calling [**IInkAnalyzer::AddStroke Method**](iinkanalyzer-addstroke.md), [**IInkAnalyzer::AddStrokeForLanguage Method**](iinkanalyzer-addstrokeforlanguage.md), [**IInkAnalyzer::AddStrokes Method**](iinkanalyzer-addstrokes.md), or [**IInkAnalyzer::AddStrokesForLanguage Method**](iinkanalyzer-addstrokesforlanguage.md).</span></span> <span data-ttu-id="a8941-115">Pour modifier les paramètres régionaux du trait, utilisez la méthode [**IInkAnalyzer :: SetStrokeLanguageId**](iinkanalyzer-setstrokelanguageid.md) ou [**IInkAnalyzer :: SetStrokesLanguageId**](iinkanalyzer-setstrokeslanguageid.md).</span><span class="sxs-lookup"><span data-stu-id="a8941-115">To change the stroke's locale, use [**IInkAnalyzer::SetStrokeLanguageId Method**](iinkanalyzer-setstrokelanguageid.md) or [**IInkAnalyzer::SetStrokesLanguageId Method**](iinkanalyzer-setstrokeslanguageid.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a8941-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a8941-116">Requirements</span></span>



| <span data-ttu-id="a8941-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a8941-117">Requirement</span></span> | <span data-ttu-id="a8941-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="a8941-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8941-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8941-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a8941-120">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a8941-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a8941-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8941-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a8941-122">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8941-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="a8941-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="a8941-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8941-124"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a8941-124"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a8941-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a8941-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8941-126"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8941-126"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="a8941-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8941-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8941-128">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="a8941-128">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="a8941-129">**IInkAnalyzer :: SetStrokeLanguageId, méthode**</span><span class="sxs-lookup"><span data-stu-id="a8941-129">**IInkAnalyzer::SetStrokeLanguageId Method**</span></span>](iinkanalyzer-setstrokelanguageid.md)
</dt> <dt>

[<span data-ttu-id="a8941-130">**IInkAnalyzer :: SetStrokesLanguageId, méthode**</span><span class="sxs-lookup"><span data-stu-id="a8941-130">**IInkAnalyzer::SetStrokesLanguageId Method**</span></span>](iinkanalyzer-setstrokeslanguageid.md)
</dt> <dt>

[<span data-ttu-id="a8941-131">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="a8941-131">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




