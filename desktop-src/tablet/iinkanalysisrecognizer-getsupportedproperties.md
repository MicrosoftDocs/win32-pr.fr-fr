---
description: Récupère les identificateurs globaux uniques (GUID) pour les propriétés que ce IInkAnalysisRecognizer peut générer pour les résultats d’analyse.
ms.assetid: 3a36bc6c-5067-4291-9119-bc6836d32c21
title: 'IInkAnalysisRecognizer :: GetSupportedProperties, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetSupportedProperties
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 5507e135241285b8f316d3ff3c2a4ef4d904296f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951220"
---
# <a name="iinkanalysisrecognizergetsupportedproperties-method"></a><span data-ttu-id="8a11e-103">IInkAnalysisRecognizer :: GetSupportedProperties, méthode</span><span class="sxs-lookup"><span data-stu-id="8a11e-103">IInkAnalysisRecognizer::GetSupportedProperties method</span></span>

<span data-ttu-id="8a11e-104">Récupère les identificateurs globaux uniques (GUID) pour les propriétés que ce [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) peut générer pour les résultats d’analyse.</span><span class="sxs-lookup"><span data-stu-id="8a11e-104">Retrieves the globally unique identifiers (GUIDs) for the properties that this [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) can generate for analysis results.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a11e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8a11e-105">Syntax</span></span>


```C++
HRESULT GetSupportedProperties(
  [in, out] ULONG *pulPropertiesCount,
  [out]     GUID  **ppProperties
);
```



## <a name="parameters"></a><span data-ttu-id="8a11e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8a11e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a11e-107">*pulPropertiesCount* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="8a11e-107">*pulPropertiesCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a11e-108">Nombre de GUID dans *ppProperties*.</span><span class="sxs-lookup"><span data-stu-id="8a11e-108">The number of GUIDs in *ppProperties*.</span></span>

</dd> <dt>

<span data-ttu-id="8a11e-109">*ppProperties* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="8a11e-109">*ppProperties* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a11e-110">Pointeur vers les GUID des propriétés que ce [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) peut générer pour les résultats d’analyse.</span><span class="sxs-lookup"><span data-stu-id="8a11e-110">A pointer to the GUIDs of properties that this [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) can generate for analysis results.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a11e-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8a11e-111">Return value</span></span>

<span data-ttu-id="8a11e-112">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="8a11e-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8a11e-113">Notes</span><span class="sxs-lookup"><span data-stu-id="8a11e-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="8a11e-114">Pour éviter une fuite de mémoire, utilisez [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) pour libérer la mémoire à partir de \* *ppProperties* lorsque vous n’avez plus besoin des informations.</span><span class="sxs-lookup"><span data-stu-id="8a11e-114">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**ppProperties* when you no longer need the information.</span></span>

 

<span data-ttu-id="8a11e-115">Un module de reconnaissance peut prendre en charge les métriques de ligne, les numéros de ligne, les niveaux de confiance, etc.</span><span class="sxs-lookup"><span data-stu-id="8a11e-115">A recognizer can support line metrics, line numbers, confidence levels, and so on.</span></span> <span data-ttu-id="8a11e-116">Pour obtenir la liste complète des propriétés qu’un module de reconnaissance peut prendre en charge, consultez [constantes RecognitionProperty](recognitionproperty-constants.md).</span><span class="sxs-lookup"><span data-stu-id="8a11e-116">For a complete list of the properties that a recognizer can support, see [RecognitionProperty Constants](recognitionproperty-constants.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8a11e-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8a11e-117">Requirements</span></span>



| <span data-ttu-id="8a11e-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8a11e-118">Requirement</span></span> | <span data-ttu-id="8a11e-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a11e-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a11e-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8a11e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8a11e-121">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8a11e-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8a11e-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8a11e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8a11e-123">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="8a11e-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="8a11e-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="8a11e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a11e-125"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="8a11e-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8a11e-126">DLL</span><span class="sxs-lookup"><span data-stu-id="8a11e-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a11e-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a11e-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="8a11e-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a11e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a11e-129">**IInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="8a11e-129">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="8a11e-130">Constantes RecognitionProperty</span><span class="sxs-lookup"><span data-stu-id="8a11e-130">RecognitionProperty Constants</span></span>](recognitionproperty-constants.md)
</dt> <dt>

[<span data-ttu-id="8a11e-131">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="8a11e-131">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

