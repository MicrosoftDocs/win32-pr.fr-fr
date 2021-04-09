---
description: Représente un avertissement ou une erreur qui se produit pendant une opération d’analyse d’encre.
ms.assetid: a9b0564b-8a49-44bc-9dbc-60a2fd5b60f2
title: Interface IAnalysisWarning (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 79e865ac909d6f9ee1862926ffab06f538661d6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113399"
---
# <a name="ianalysiswarning-interface"></a><span data-ttu-id="530b3-103">Interface IAnalysisWarning</span><span class="sxs-lookup"><span data-stu-id="530b3-103">IAnalysisWarning interface</span></span>

<span data-ttu-id="530b3-104">Représente un avertissement ou une erreur qui se produit pendant une opération d’analyse d’encre.</span><span class="sxs-lookup"><span data-stu-id="530b3-104">Represents a warning or error that occurs during an ink analysis operation.</span></span>

## <a name="members"></a><span data-ttu-id="530b3-105">Membres</span><span class="sxs-lookup"><span data-stu-id="530b3-105">Members</span></span>

<span data-ttu-id="530b3-106">L’interface **IAnalysisWarning** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="530b3-106">The **IAnalysisWarning** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="530b3-107">**IAnalysisWarning** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="530b3-107">**IAnalysisWarning** also has these types of members:</span></span>

-   [<span data-ttu-id="530b3-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="530b3-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="530b3-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="530b3-109">Methods</span></span>

<span data-ttu-id="530b3-110">L’interface **IAnalysisWarning** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="530b3-110">The **IAnalysisWarning** interface has these methods.</span></span>



| <span data-ttu-id="530b3-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="530b3-111">Method</span></span>                                                            | <span data-ttu-id="530b3-112">Description</span><span class="sxs-lookup"><span data-stu-id="530b3-112">Description</span></span>                                                                                                                            |
|:------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="530b3-113">**GetBackgroundError**</span><span class="sxs-lookup"><span data-stu-id="530b3-113">**GetBackgroundError**</span></span>](ianalysiswarning-getbackgrounderror.md) | <span data-ttu-id="530b3-114">Récupère le code d’erreur de l’opération d’analyse de l’encre en arrière-plan si une erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="530b3-114">Retrieves the error code for the background ink analysis operation if an error occurred.</span></span><br/>                                    |
| [<span data-ttu-id="530b3-115">**GetHint**</span><span class="sxs-lookup"><span data-stu-id="530b3-115">**GetHint**</span></span>](ianalysiswarning-gethint.md)                       | <span data-ttu-id="530b3-116">Récupère l’indicateur d’analyse à l’origine de cet avertissement</span><span class="sxs-lookup"><span data-stu-id="530b3-116">Retrieves the analysis hint that caused this warning</span></span><br/>                                                                        |
| [<span data-ttu-id="530b3-117">**GetNodeIds**</span><span class="sxs-lookup"><span data-stu-id="530b3-117">**GetNodeIds**</span></span>](ianalysiswarning-getnodeids.md)                 | <span data-ttu-id="530b3-118">Récupère les identificateurs de tous les nœuds de contexte appropriés associés à cet avertissement.</span><span class="sxs-lookup"><span data-stu-id="530b3-118">Retrieves the identifiers of any relevant context nodes that are associated with this warning.</span></span><br/>                              |
| [<span data-ttu-id="530b3-119">**GetWarningCode**</span><span class="sxs-lookup"><span data-stu-id="530b3-119">**GetWarningCode**</span></span>](ianalysiswarning-getwarningcode.md)         | <span data-ttu-id="530b3-120">Récupère le type d’avertissement qui s’est produit à l’aide de l’énumération [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) .</span><span class="sxs-lookup"><span data-stu-id="530b3-120">Retrieves the type of warning that occurred by using the [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) enumeration.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="530b3-121">Notes</span><span class="sxs-lookup"><span data-stu-id="530b3-121">Remarks</span></span>

<span data-ttu-id="530b3-122">Les types d’avertissements qui peuvent se produire sont décrits par l’énumération [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) .</span><span class="sxs-lookup"><span data-stu-id="530b3-122">The types of warnings that can occur are described by the [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) enumeration.</span></span> <span data-ttu-id="530b3-123">Souvent, les avertissements se produisent lorsque vous essayez d’utiliser une fonctionnalité qui n’est pas prise en charge par le [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) utilisé par le [**IInkAnalyzer**](iinkanalyzer.md) .</span><span class="sxs-lookup"><span data-stu-id="530b3-123">Often warnings occur when you try to use a feature that is not supported by the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) that the [**IInkAnalyzer**](iinkanalyzer.md) is using.</span></span>

<span data-ttu-id="530b3-124">Certains avertissements indiquent que le [**IInkAnalyzer**](iinkanalyzer.md) n’a pas terminé l’opération d’analyse.</span><span class="sxs-lookup"><span data-stu-id="530b3-124">Some warnings indicate that the [**IInkAnalyzer**](iinkanalyzer.md) did not complete the analysis operation.</span></span> <span data-ttu-id="530b3-125">Pour plus d’informations, consultez [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode).</span><span class="sxs-lookup"><span data-stu-id="530b3-125">For more information, see [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode).</span></span>

## <a name="examples"></a><span data-ttu-id="530b3-126">Exemples</span><span class="sxs-lookup"><span data-stu-id="530b3-126">Examples</span></span>

<span data-ttu-id="530b3-127">L’exemple suivant montre un plan d’un gestionnaire d’événements pour l’événement [**\_ IAnalysisEvents :: Results**](-ianalysisevents-results.md) .</span><span class="sxs-lookup"><span data-stu-id="530b3-127">The following example shows an outline of an event handler for the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span> <span data-ttu-id="530b3-128">Le gestionnaire vérifie [**IAnalysisStatus :: IsSuccessful**](ianalysisstatus-issuccessful.md).</span><span class="sxs-lookup"><span data-stu-id="530b3-128">The handler checks [**IAnalysisStatus::IsSuccessful**](ianalysisstatus-issuccessful.md).</span></span> <span data-ttu-id="530b3-129">Si l’opération d’analyse génère des avertissements, le gestionnaire itère au sein de la collection d’objets **IAnalysisWarning** .</span><span class="sxs-lookup"><span data-stu-id="530b3-129">If the analysis operation generates warnings, the handler iterates through the collection of **IAnalysisWarning** objects.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="530b3-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="530b3-130">Requirements</span></span>



| <span data-ttu-id="530b3-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="530b3-131">Requirement</span></span> | <span data-ttu-id="530b3-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="530b3-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="530b3-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="530b3-133">Minimum supported client</span></span><br/> | <span data-ttu-id="530b3-134">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="530b3-134">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="530b3-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="530b3-135">Minimum supported server</span></span><br/> | <span data-ttu-id="530b3-136">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="530b3-136">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="530b3-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="530b3-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="530b3-138"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="530b3-138"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="530b3-139">DLL</span><span class="sxs-lookup"><span data-stu-id="530b3-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="530b3-140"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="530b3-140"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="530b3-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="530b3-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="530b3-142">**IAnalysisWarnings**</span><span class="sxs-lookup"><span data-stu-id="530b3-142">**IAnalysisWarnings**</span></span>](ianalysiswarnings.md)
</dt> <dt>

[<span data-ttu-id="530b3-143">**AnalysisWarningCode**</span><span class="sxs-lookup"><span data-stu-id="530b3-143">**AnalysisWarningCode**</span></span>](analysiswarningcode.md)
</dt> <dt>

[<span data-ttu-id="530b3-144">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="530b3-144">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

