---
description: Récupère un résumé booléen des résultats de l’opération d’analyse.
ms.assetid: 9bc690f4-fb5f-449e-bde0-bd2277c4573b
title: 'IAnalysisStatus :: IsSuccessful, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisStatus.IsSuccessful
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: daf7ec801773d855f0ed85a795bc492ef673a74e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318470"
---
# <a name="ianalysisstatusissuccessful-method"></a><span data-ttu-id="a7cf5-103">IAnalysisStatus :: IsSuccessful, méthode</span><span class="sxs-lookup"><span data-stu-id="a7cf5-103">IAnalysisStatus::IsSuccessful method</span></span>

<span data-ttu-id="a7cf5-104">Récupère un résumé booléen des résultats de l’opération d’analyse.</span><span class="sxs-lookup"><span data-stu-id="a7cf5-104">Retrieves a Boolean summary of the results of the analysis operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7cf5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a7cf5-105">Syntax</span></span>


```C++
HRESULT IsSuccessful(
  [out] VARIANT_BOOL *pfSuccessful
);
```



## <a name="parameters"></a><span data-ttu-id="a7cf5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a7cf5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7cf5-107">*pfSuccessful* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a7cf5-107">*pfSuccessful* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a7cf5-108">**Variante \_ TRUE** si l’opération d’analyse s’est terminée sans avertissement, ou **\_ false** si au moins un avertissement s’est produit.</span><span class="sxs-lookup"><span data-stu-id="a7cf5-108">**VARIANT\_TRUE** if the analysis operation completed without any warnings, or **VARIANT\_FALSE** if at least one warning occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7cf5-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a7cf5-109">Return value</span></span>

<span data-ttu-id="a7cf5-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="a7cf5-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a7cf5-111">Exemples</span><span class="sxs-lookup"><span data-stu-id="a7cf5-111">Examples</span></span>

<span data-ttu-id="a7cf5-112">L’exemple suivant montre un plan d’un gestionnaire d’événements pour l’événement [**\_ IAnalysisEvents :: Results**](-ianalysisevents-results.md) .</span><span class="sxs-lookup"><span data-stu-id="a7cf5-112">The following example shows an outline of an event handler for the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span> <span data-ttu-id="a7cf5-113">Le gestionnaire vérifie **IAnalysisStatus :: IsSuccessful**.</span><span class="sxs-lookup"><span data-stu-id="a7cf5-113">The handler checks **IAnalysisStatus::IsSuccessful**.</span></span> <span data-ttu-id="a7cf5-114">Si l’opération d’analyse génère des avertissements, le gestionnaire itère au sein de la collection d’objets [**IAnalysisWarning**](ianalysiswarning.md) .</span><span class="sxs-lookup"><span data-stu-id="a7cf5-114">If the analysis operation generates warnings, the handler iterates through the collection of [**IAnalysisWarning**](ianalysiswarning.md) objects.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="a7cf5-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a7cf5-115">Requirements</span></span>



| <span data-ttu-id="a7cf5-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a7cf5-116">Requirement</span></span> | <span data-ttu-id="a7cf5-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="a7cf5-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7cf5-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a7cf5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a7cf5-119">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a7cf5-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a7cf5-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a7cf5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a7cf5-121">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a7cf5-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="a7cf5-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="a7cf5-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7cf5-123"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a7cf5-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a7cf5-124">DLL</span><span class="sxs-lookup"><span data-stu-id="a7cf5-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7cf5-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7cf5-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="a7cf5-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a7cf5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7cf5-127">**IAnalysisStatus**</span><span class="sxs-lookup"><span data-stu-id="a7cf5-127">**IAnalysisStatus**</span></span>](ianalysisstatus.md)
</dt> <dt>

[<span data-ttu-id="a7cf5-128">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="a7cf5-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




