---
description: Récupère les identificateurs pour les paramètres régionaux pris en charge par ce IInkAnalysisRecognizer.
ms.assetid: 14c91ad0-f49e-43e7-848c-abc96b0dffa8
title: 'IInkAnalysisRecognizer :: GetLanguages, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetLanguages
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 1e2b9792957b2de02daf45f8b662cfcb1174be72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862709"
---
# <a name="iinkanalysisrecognizergetlanguages-method"></a><span data-ttu-id="bf86e-103">IInkAnalysisRecognizer :: GetLanguages, méthode</span><span class="sxs-lookup"><span data-stu-id="bf86e-103">IInkAnalysisRecognizer::GetLanguages method</span></span>

<span data-ttu-id="bf86e-104">Récupère les identificateurs pour les paramètres régionaux pris en charge par ce [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) .</span><span class="sxs-lookup"><span data-stu-id="bf86e-104">Retrieves the identifiers for the locales that this [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf86e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bf86e-105">Syntax</span></span>


```C++
HRESULT GetLanguages(
  [in, out] ULONG *pulLanguagesCount,
  [out]     ULONG **ppulLanguages
);
```



## <a name="parameters"></a><span data-ttu-id="bf86e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bf86e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf86e-107">*pulLanguagesCount* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="bf86e-107">*pulLanguagesCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bf86e-108">Nombre d’identificateurs dans *ppulLanguages*.</span><span class="sxs-lookup"><span data-stu-id="bf86e-108">The number of identifiers in *ppulLanguages*.</span></span>

</dd> <dt>

<span data-ttu-id="bf86e-109">*ppulLanguages* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="bf86e-109">*ppulLanguages* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bf86e-110">Pointeur vers les identificateurs pour les paramètres régionaux pris en charge par ce [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) .</span><span class="sxs-lookup"><span data-stu-id="bf86e-110">A pointer to the identifiers for the locales that this [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) supports.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf86e-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bf86e-111">Return value</span></span>

<span data-ttu-id="bf86e-112">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="bf86e-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="bf86e-113">Notes</span><span class="sxs-lookup"><span data-stu-id="bf86e-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="bf86e-114">Pour éviter une fuite de mémoire, utilisez [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) pour libérer la mémoire à partir de \* *ppulLanguages* lorsque vous n’avez plus besoin des informations.</span><span class="sxs-lookup"><span data-stu-id="bf86e-114">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**ppulLanguages* when you no longer need the information.</span></span>

 

<span data-ttu-id="bf86e-115">Cette méthode retourne un tableau vide pour les objets et les modules de reconnaissance de mouvement.</span><span class="sxs-lookup"><span data-stu-id="bf86e-115">This method returns an empty array for object and gesture recognizers.</span></span>

<span data-ttu-id="bf86e-116">Pour plus d’informations sur les identificateurs de langue, consultez [constantes et chaînes d’identificateur de langue](/windows/desktop/Intl/language-identifier-constants-and-strings).</span><span class="sxs-lookup"><span data-stu-id="bf86e-116">For more information about language identifiers, see [Language Identifier Constants and Strings](/windows/desktop/Intl/language-identifier-constants-and-strings).</span></span>

## <a name="requirements"></a><span data-ttu-id="bf86e-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bf86e-117">Requirements</span></span>



| <span data-ttu-id="bf86e-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bf86e-118">Requirement</span></span> | <span data-ttu-id="bf86e-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="bf86e-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf86e-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf86e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bf86e-121">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bf86e-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="bf86e-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf86e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bf86e-123">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf86e-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="bf86e-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="bf86e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf86e-125"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="bf86e-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="bf86e-126">DLL</span><span class="sxs-lookup"><span data-stu-id="bf86e-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf86e-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf86e-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="bf86e-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf86e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf86e-129">**IInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="bf86e-129">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="bf86e-130">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="bf86e-130">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

