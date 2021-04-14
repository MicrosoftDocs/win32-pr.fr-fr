---
description: Récupère le IInkAnalysisRecognizer à l’index spécifié.
ms.assetid: e4db56c6-7c15-4336-bc0a-f50222c3520e
title: 'IInkAnalysisRecognizers :: GetInkAnalysisRecognizer, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizers.GetInkAnalysisRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 1008ae0b26d30233c3b00167391523d321cd381e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485089"
---
# <a name="iinkanalysisrecognizersgetinkanalysisrecognizer-method"></a><span data-ttu-id="ec89e-103">IInkAnalysisRecognizers :: GetInkAnalysisRecognizer, méthode</span><span class="sxs-lookup"><span data-stu-id="ec89e-103">IInkAnalysisRecognizers::GetInkAnalysisRecognizer method</span></span>

<span data-ttu-id="ec89e-104">Récupère le [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="ec89e-104">Retrieves the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec89e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ec89e-105">Syntax</span></span>


```C++
HRESULT GetInkAnalysisRecognizer(
  [in]  ULONG                  ulIndex,
  [out] IInkAnalysisRecognizer **ppInkAnalysisRecognizer
);
```



## <a name="parameters"></a><span data-ttu-id="ec89e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ec89e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec89e-107">*ulIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ec89e-107">*ulIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec89e-108">Index de base zéro de l’objet [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) à récupérer.</span><span class="sxs-lookup"><span data-stu-id="ec89e-108">The zero-based index of the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) object to get.</span></span>

</dd> <dt>

<span data-ttu-id="ec89e-109">*ppInkAnalysisRecognizer* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ec89e-109">*ppInkAnalysisRecognizer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ec89e-110">Pointeur vers le [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="ec89e-110">A pointer to the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) at the specified index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec89e-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ec89e-111">Return value</span></span>

<span data-ttu-id="ec89e-112">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="ec89e-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ec89e-113">Notes</span><span class="sxs-lookup"><span data-stu-id="ec89e-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="ec89e-114">Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur \* *ppInkAnalysisRecognizer* lorsque vous n’avez plus besoin d’utiliser le module de reconnaissance de l’analyse de l’encre.</span><span class="sxs-lookup"><span data-stu-id="ec89e-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppInkAnalysisRecognizer* when you no longer need to use the ink analysis recognizer.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ec89e-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ec89e-115">Requirements</span></span>



| <span data-ttu-id="ec89e-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ec89e-116">Requirement</span></span> | <span data-ttu-id="ec89e-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec89e-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec89e-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ec89e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ec89e-119">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ec89e-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ec89e-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ec89e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ec89e-121">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="ec89e-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="ec89e-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="ec89e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec89e-123"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ec89e-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ec89e-124">DLL</span><span class="sxs-lookup"><span data-stu-id="ec89e-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec89e-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec89e-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="ec89e-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec89e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec89e-127">**InkAnalysisRecognizers**</span><span class="sxs-lookup"><span data-stu-id="ec89e-127">**InkAnalysisRecognizers**</span></span>](iinkanalysisrecognizers.md)
</dt> <dt>

[<span data-ttu-id="ec89e-128">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="ec89e-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

