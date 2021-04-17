---
description: Obtient la valeur de chaîne reconnue de l’objet IAnalysisAlternate.
ms.assetid: cdf41824-77a4-4c71-8712-f380a6cbf4c5
title: 'IAnalysisAlternate :: GetRecognizedString, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate.GetRecognizedString
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 5489773b29ade35d4b7297065c1104bfecefa117
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526571"
---
# <a name="ianalysisalternategetrecognizedstring-method"></a><span data-ttu-id="123ae-103">IAnalysisAlternate :: GetRecognizedString, méthode</span><span class="sxs-lookup"><span data-stu-id="123ae-103">IAnalysisAlternate::GetRecognizedString method</span></span>

<span data-ttu-id="123ae-104">Obtient la valeur de chaîne reconnue de l’objet [**IAnalysisAlternate**](ianalysisalternate.md) .</span><span class="sxs-lookup"><span data-stu-id="123ae-104">Gets the recognized string value of the [**IAnalysisAlternate**](ianalysisalternate.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="123ae-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="123ae-105">Syntax</span></span>


```C++
HRESULT GetRecognizedString(
  [out] BSTR *pbstrRecognizedString
);
```



## <a name="parameters"></a><span data-ttu-id="123ae-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="123ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="123ae-107">*pbstrRecognizedString* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="123ae-107">*pbstrRecognizedString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="123ae-108">Pointeur vers le **BSTR** qui a pour valeur la valeur de chaîne reconnue.</span><span class="sxs-lookup"><span data-stu-id="123ae-108">A pointer to the **BSTR** that is set to the recognized string value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="123ae-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="123ae-109">Return value</span></span>

<span data-ttu-id="123ae-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="123ae-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="123ae-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="123ae-111">Requirements</span></span>



| <span data-ttu-id="123ae-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="123ae-112">Requirement</span></span> | <span data-ttu-id="123ae-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="123ae-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="123ae-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="123ae-114">Minimum supported client</span></span><br/> | <span data-ttu-id="123ae-115">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="123ae-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="123ae-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="123ae-116">Minimum supported server</span></span><br/> | <span data-ttu-id="123ae-117">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="123ae-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="123ae-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="123ae-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="123ae-119"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="123ae-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="123ae-120">DLL</span><span class="sxs-lookup"><span data-stu-id="123ae-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="123ae-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="123ae-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="123ae-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="123ae-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="123ae-123">**IAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="123ae-123">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="123ae-124">**IInkAnalyzer :: GetRecognizedString, méthode**</span><span class="sxs-lookup"><span data-stu-id="123ae-124">**IInkAnalyzer::GetRecognizedString Method**</span></span>](iinkanalyzer-getrecognizedstring.md)
</dt> </dl>

 

 




