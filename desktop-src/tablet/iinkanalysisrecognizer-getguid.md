---
description: Récupère l’identificateur global unique (GUID) du module de reconnaissance.
ms.assetid: 9b98993b-eaf3-4207-9d56-33efeceb75cf
title: 'IInkAnalysisRecognizer :: GetGuid, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetGuid
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 9a027a405829e6d1237a8ec90dd59fcc8905006d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862710"
---
# <a name="iinkanalysisrecognizergetguid-method"></a><span data-ttu-id="c4582-103">IInkAnalysisRecognizer :: GetGuid, méthode</span><span class="sxs-lookup"><span data-stu-id="c4582-103">IInkAnalysisRecognizer::GetGuid method</span></span>

<span data-ttu-id="c4582-104">Récupère l’identificateur global unique (GUID) du module de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="c4582-104">Retrieves the globally unique identifier (GUID) of the recognizer.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4582-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c4582-105">Syntax</span></span>


```C++
HRESULT GetGuid(
  [out] GUID *pId
);
```



## <a name="parameters"></a><span data-ttu-id="c4582-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c4582-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4582-107">*PID* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c4582-107">*pId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c4582-108">GUID qui identifie ce [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span><span class="sxs-lookup"><span data-stu-id="c4582-108">The GUID that identifies this [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4582-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c4582-109">Return value</span></span>

<span data-ttu-id="c4582-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="c4582-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c4582-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c4582-111">Requirements</span></span>



| <span data-ttu-id="c4582-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c4582-112">Requirement</span></span> | <span data-ttu-id="c4582-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4582-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4582-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4582-114">Minimum supported client</span></span><br/> | <span data-ttu-id="c4582-115">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c4582-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c4582-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4582-116">Minimum supported server</span></span><br/> | <span data-ttu-id="c4582-117">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4582-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="c4582-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="c4582-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4582-119"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="c4582-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c4582-120">DLL</span><span class="sxs-lookup"><span data-stu-id="c4582-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4582-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4582-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="c4582-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4582-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4582-123">**IInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="c4582-123">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="c4582-124">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="c4582-124">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




