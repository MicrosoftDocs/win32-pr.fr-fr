---
description: Récupère un tableau de plages de caractères qui représentent les plages de caractères Unicode prises en charge.
ms.assetid: 334cf545-832a-4e8a-8fe6-76a173676be7
title: 'IInkAnalysisRecognizer :: GetUnicodeRanges, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetUnicodeRanges
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 939c2d5bf45c5dfbf0f1866cb6d0c7a58c38320f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862706"
---
# <a name="iinkanalysisrecognizergetunicoderanges-method"></a><span data-ttu-id="141d8-103">IInkAnalysisRecognizer :: GetUnicodeRanges, méthode</span><span class="sxs-lookup"><span data-stu-id="141d8-103">IInkAnalysisRecognizer::GetUnicodeRanges method</span></span>

<span data-ttu-id="141d8-104">Récupère un tableau de plages de caractères qui représentent les plages de caractères Unicode prises en charge.</span><span class="sxs-lookup"><span data-stu-id="141d8-104">Retrieves an array of character ranges representing the supported Unicode character ranges.</span></span>

## <a name="syntax"></a><span data-ttu-id="141d8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="141d8-105">Syntax</span></span>


```C++
HRESULT GetUnicodeRanges(
  [in, out] ULONG  *pulNumberOfRanges,
  [out]     WCHAR  **ppulLowUnicode,
  [out]     USHORT **ppusUnicodeRangeLength
);
```



## <a name="parameters"></a><span data-ttu-id="141d8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="141d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="141d8-107">*pulNumberOfRanges* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="141d8-107">*pulNumberOfRanges* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="141d8-108">Nombre de plages de caractères pointées par *ppulLowUnicode*.</span><span class="sxs-lookup"><span data-stu-id="141d8-108">The number of character ranges pointed to by *ppulLowUnicode*.</span></span>

</dd> <dt>

<span data-ttu-id="141d8-109">*ppulLowUnicode* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="141d8-109">*ppulLowUnicode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="141d8-110">Pointeur vers un tableau de plages de caractères représentant les plages de caractères Unicode prises en charge.</span><span class="sxs-lookup"><span data-stu-id="141d8-110">Pointer to an array of character ranges representing the supported Unicode character ranges.</span></span>

</dd> <dt>

<span data-ttu-id="141d8-111">*ppusUnicodeRangeLength* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="141d8-111">*ppusUnicodeRangeLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="141d8-112">Pointeur vers un tableau de valeurs indiquant la longueur de chaque tableau vers par *ppulLowUnicode*.</span><span class="sxs-lookup"><span data-stu-id="141d8-112">Pointer to an array of values indicating the length of each array point to by *ppulLowUnicode*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="141d8-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="141d8-113">Return value</span></span>

<span data-ttu-id="141d8-114">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="141d8-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="141d8-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="141d8-115">Requirements</span></span>



| <span data-ttu-id="141d8-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="141d8-116">Requirement</span></span> | <span data-ttu-id="141d8-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="141d8-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="141d8-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="141d8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="141d8-119">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="141d8-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="141d8-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="141d8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="141d8-121">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="141d8-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="141d8-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="141d8-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="141d8-123"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="141d8-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="141d8-124">DLL</span><span class="sxs-lookup"><span data-stu-id="141d8-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="141d8-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="141d8-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="141d8-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="141d8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="141d8-127">**IInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="141d8-127">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> </dl>

 

 




