---
description: Récupère les fonctionnalités du module de reconnaissance.
ms.assetid: 9014bd9b-54fb-4735-9eb8-56a6188a5fc0
title: 'IInkAnalysisRecognizer :: GetCapabilities, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetCapabilities
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 07b66ffbed6f3e57edb8a6bfad36959fabbc047c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113362"
---
# <a name="iinkanalysisrecognizergetcapabilities-method"></a><span data-ttu-id="6c428-103">IInkAnalysisRecognizer :: GetCapabilities, méthode</span><span class="sxs-lookup"><span data-stu-id="6c428-103">IInkAnalysisRecognizer::GetCapabilities method</span></span>

<span data-ttu-id="6c428-104">Récupère les fonctionnalités du module de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="6c428-104">Retrieves the capabilities of the recognizer.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c428-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6c428-105">Syntax</span></span>


```C++
HRESULT GetCapabilities(
  [out] InkAnalysisRecognizerCapabilities *pCapabilities
);
```



## <a name="parameters"></a><span data-ttu-id="6c428-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6c428-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c428-107">*pCapabilities* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6c428-107">*pCapabilities* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c428-108">Combinaison d’opérations de bits de valeurs [**RecognizerCapabilities**](recognizercapabilities.md) .</span><span class="sxs-lookup"><span data-stu-id="6c428-108">A bitwise combination of [**RecognizerCapabilities**](recognizercapabilities.md) values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c428-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6c428-109">Return value</span></span>

<span data-ttu-id="6c428-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="6c428-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6c428-111">Notes</span><span class="sxs-lookup"><span data-stu-id="6c428-111">Remarks</span></span>

<span data-ttu-id="6c428-112">Cette valeur est constante pour chaque [ **IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)</span><span class="sxs-lookup"><span data-stu-id="6c428-112">This value is constant for each [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="6c428-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6c428-113">Requirements</span></span>



| <span data-ttu-id="6c428-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6c428-114">Requirement</span></span> | <span data-ttu-id="6c428-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="6c428-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c428-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6c428-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6c428-117">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6c428-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6c428-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6c428-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6c428-119">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="6c428-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="6c428-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="6c428-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c428-121"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="6c428-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="6c428-122">DLL</span><span class="sxs-lookup"><span data-stu-id="6c428-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c428-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c428-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="6c428-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6c428-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c428-125">**IInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="6c428-125">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="6c428-126">**RecognizerCapabilities**</span><span class="sxs-lookup"><span data-stu-id="6c428-126">**RecognizerCapabilities**</span></span>](recognizercapabilities.md)
</dt> <dt>

[<span data-ttu-id="6c428-127">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="6c428-127">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




