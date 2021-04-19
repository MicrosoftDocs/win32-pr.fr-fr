---
description: Obtient le nombre d’objets IAnalysisWarning contenus dans la collection IAnalysisWarnings.
ms.assetid: a0ad46d5-fb1b-40f6-bfc1-28ea1bf4eb44
title: 'IAnalysisWarnings :: GetCount, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarnings.GetCount
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: bc795d310f4bc532a39e2c1a2b4d2ba68f0401f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544682"
---
# <a name="ianalysiswarningsgetcount-method"></a><span data-ttu-id="ecd36-103">IAnalysisWarnings :: GetCount, méthode</span><span class="sxs-lookup"><span data-stu-id="ecd36-103">IAnalysisWarnings::GetCount method</span></span>

<span data-ttu-id="ecd36-104">Obtient le nombre d’objets [**IAnalysisWarning**](ianalysiswarning.md) contenus dans la collection [**IAnalysisWarnings**](ianalysiswarnings.md) .</span><span class="sxs-lookup"><span data-stu-id="ecd36-104">Gets the number of [**IAnalysisWarning**](ianalysiswarning.md) objects contained in the [**IAnalysisWarnings**](ianalysiswarnings.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecd36-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ecd36-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [out, retval] ULONG *pulCount
);
```



## <a name="parameters"></a><span data-ttu-id="ecd36-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ecd36-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecd36-107">*pulCount* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="ecd36-107">*pulCount* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="ecd36-108">Nombre d’objets [**IAnalysisWarning**](ianalysiswarning.md) contenus dans la collection [**IAnalysisWarnings**](ianalysiswarnings.md) .</span><span class="sxs-lookup"><span data-stu-id="ecd36-108">The number of [**IAnalysisWarning**](ianalysiswarning.md) objects contained in the [**IAnalysisWarnings**](ianalysiswarnings.md) collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ecd36-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ecd36-109">Return value</span></span>

<span data-ttu-id="ecd36-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="ecd36-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ecd36-111">Exemples</span><span class="sxs-lookup"><span data-stu-id="ecd36-111">Examples</span></span>

<span data-ttu-id="ecd36-112">L’exemple suivant montre un plan d’un gestionnaire d’événements pour l’événement [**\_ IAnalysisEvents :: Results**](-ianalysisevents-results.md) .</span><span class="sxs-lookup"><span data-stu-id="ecd36-112">The following example shows an outline of an event handler for the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span> <span data-ttu-id="ecd36-113">Le gestionnaire vérifie [**IAnalysisStatus :: IsSuccessful**](ianalysisstatus-issuccessful.md).</span><span class="sxs-lookup"><span data-stu-id="ecd36-113">The handler checks [**IAnalysisStatus::IsSuccessful**](ianalysisstatus-issuccessful.md).</span></span> <span data-ttu-id="ecd36-114">Si l’opération d’analyse génère des avertissements, le gestionnaire itère au sein de la collection d’objets [**IAnalysisWarning**](ianalysiswarning.md) .</span><span class="sxs-lookup"><span data-stu-id="ecd36-114">If the analysis operation generates warnings, the handler iterates through the collection of [**IAnalysisWarning**](ianalysiswarning.md) objects.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="ecd36-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ecd36-115">Requirements</span></span>



| <span data-ttu-id="ecd36-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ecd36-116">Requirement</span></span> | <span data-ttu-id="ecd36-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="ecd36-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecd36-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ecd36-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ecd36-119">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ecd36-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ecd36-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ecd36-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ecd36-121">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="ecd36-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="ecd36-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="ecd36-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ecd36-123"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ecd36-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ecd36-124">DLL</span><span class="sxs-lookup"><span data-stu-id="ecd36-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ecd36-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ecd36-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="ecd36-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ecd36-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecd36-127">**IAnalysisWarnings**</span><span class="sxs-lookup"><span data-stu-id="ecd36-127">**IAnalysisWarnings**</span></span>](ianalysiswarnings.md)
</dt> <dt>

[<span data-ttu-id="ecd36-128">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="ecd36-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




