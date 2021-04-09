---
description: Récupère l’objet IAnalysisWarning à l’index spécifié.
ms.assetid: 8f5d5642-73ec-496e-bad7-9f636fc00217
title: 'IAnalysisWarnings :: GetAnalysisWarning, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarnings.GetAnalysisWarning
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 88ed3686ecf3861a2b097ebfc005214ab0cdd1c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034021"
---
# <a name="ianalysiswarningsgetanalysiswarning-method"></a><span data-ttu-id="e0822-103">IAnalysisWarnings :: GetAnalysisWarning, méthode</span><span class="sxs-lookup"><span data-stu-id="e0822-103">IAnalysisWarnings::GetAnalysisWarning method</span></span>

<span data-ttu-id="e0822-104">Récupère l’objet [**IAnalysisWarning**](ianalysiswarning.md) à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="e0822-104">Retrieves the [**IAnalysisWarning**](ianalysiswarning.md) object at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0822-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e0822-105">Syntax</span></span>


```C++
HRESULT GetAnalysisWarning(
  [in]  ULONG            ulIndex,
  [out] IAnalysisWarning **ppWarning
);
```



## <a name="parameters"></a><span data-ttu-id="e0822-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e0822-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0822-107">*ulIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e0822-107">*ulIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0822-108">Index de base zéro de l’objet [**IAnalysisWarning**](ianalysiswarning.md) à récupérer.</span><span class="sxs-lookup"><span data-stu-id="e0822-108">The zero-based index of the [**IAnalysisWarning**](ianalysiswarning.md) object to get.</span></span>

</dd> <dt>

<span data-ttu-id="e0822-109">*ppWarning* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e0822-109">*ppWarning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e0822-110">Pointeur vers l’objet [**IAnalysisWarning**](ianalysiswarning.md) à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="e0822-110">A pointer to the [**IAnalysisWarning**](ianalysiswarning.md) object at the specified index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0822-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e0822-111">Return value</span></span>

<span data-ttu-id="e0822-112">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="e0822-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e0822-113">Notes</span><span class="sxs-lookup"><span data-stu-id="e0822-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="e0822-114">Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur \* *ppWarning* lorsque vous n’avez plus besoin d’utiliser l’avertissement.</span><span class="sxs-lookup"><span data-stu-id="e0822-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppWarning* when you no longer need to use the warning.</span></span>

 

## <a name="examples"></a><span data-ttu-id="e0822-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="e0822-115">Examples</span></span>

<span data-ttu-id="e0822-116">L’exemple suivant montre un plan d’un gestionnaire d’événements pour l’événement [**\_ IAnalysisEvents :: Results**](-ianalysisevents-results.md) .</span><span class="sxs-lookup"><span data-stu-id="e0822-116">The following example shows an outline of an event handler for the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span> <span data-ttu-id="e0822-117">Le gestionnaire vérifie [**IAnalysisStatus :: IsSuccessful**](ianalysisstatus-issuccessful.md).</span><span class="sxs-lookup"><span data-stu-id="e0822-117">The handler checks [**IAnalysisStatus::IsSuccessful**](ianalysisstatus-issuccessful.md).</span></span> <span data-ttu-id="e0822-118">Si l’opération d’analyse génère des avertissements, le gestionnaire itère au sein de la collection d’objets [**IAnalysisWarning**](ianalysiswarning.md) .</span><span class="sxs-lookup"><span data-stu-id="e0822-118">If the analysis operation generates warnings, the handler iterates through the collection of [**IAnalysisWarning**](ianalysiswarning.md) objects.</span></span>


```C++
// _IAnalysisEvents::Results event handler.
STDMETHODIMP CMyClass::Results(
    IInkAnalyzer *pInkAnalyzer,
    IAnalysisStatus *pAnalysisStatus)
{
    // Check the status of the analysis operation.
    VARIANT_BOOL bResult = VARIANT_FALSE;
    HRESULT hr = pAnalysisStatus->IsSuccessful(&bResult);

    if( SUCCEEDED(hr) )
    {
        if( bResult )
        {
            // Insert code that handles a successful result.
        }
        else
        {
            // Get the analysis warnings.
            IAnalysisWarnings* pAnalysisWarnings = NULL;
            hr = pAnalysisStatus->GetWarnings(&pAnalysisWarnings);
            if (SUCCEEDED(hr))
            {
                // Iterate through the warning collection.
                ULONG warningCount = 0;
                hr = pAnalysisWarnings->GetCount(&warningCount);
                if (SUCCEEDED(hr))
                {
                    IAnalysisWarning *pAnalysisWarning = NULL;
                    AnalysisWarningCode analysisWarningCode;
                    for (ULONG index=0; index<warningCount; index++)
                    {
                        // Get an analysis warning.
                        hr = pAnalysisWarnings->GetAnalysisWarning(
                            index, &pAnalysisWarning);

                        if (SUCCEEDED(hr))
                        {
                            // Get the warning code for the warning.
                            hr = pAnalysisWarning->GetWarningCode(
                                &analysisWarningCode);

                            if (SUCCEEDED(hr))
                            {
                                // Insert code that handles each
                                // analysis warning.
                            }
                        }

                        // Release this reference to the analysis warning.
                        if (pAnalysisWarning != NULL)
                        {
                            pAnalysisWarning->Release();
                            pAnalysisWarning = NULL;
                        }

                        if (FAILED(hr))
                        {
                            break;
                        }
                    }
                }
            }

            // Release this reference to the analysis warnings collection.
            if (pAnalysisWarnings != NULL)
            {
                pAnalysisWarnings->Release();
                pAnalysisWarnings = NULL;
            }
        }
    }
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="e0822-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e0822-119">Requirements</span></span>



| <span data-ttu-id="e0822-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e0822-120">Requirement</span></span> | <span data-ttu-id="e0822-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="e0822-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0822-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e0822-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e0822-123">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e0822-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e0822-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e0822-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e0822-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e0822-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="e0822-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="e0822-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0822-127"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e0822-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e0822-128">DLL</span><span class="sxs-lookup"><span data-stu-id="e0822-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0822-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0822-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="e0822-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e0822-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0822-131">**IAnalysisWarnings**</span><span class="sxs-lookup"><span data-stu-id="e0822-131">**IAnalysisWarnings**</span></span>](ianalysiswarnings.md)
</dt> <dt>

[<span data-ttu-id="e0822-132">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="e0822-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

