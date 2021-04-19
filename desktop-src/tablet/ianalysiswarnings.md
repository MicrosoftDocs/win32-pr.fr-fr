---
description: Contient une collection d’objets qui implémentent l’interface IAnalysisWarning et qui sont le résultat d’une opération d’analyse d’encre.
ms.assetid: 2118c18b-d316-4e91-8652-62969115e8b5
title: Interface IAnalysisWarnings (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarnings
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 938d406ea90d86cc05ac84b69304b7a85e0e54fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514634"
---
# <a name="ianalysiswarnings-interface"></a><span data-ttu-id="321e9-103">Interface IAnalysisWarnings</span><span class="sxs-lookup"><span data-stu-id="321e9-103">IAnalysisWarnings interface</span></span>

<span data-ttu-id="321e9-104">Contient une collection d’objets qui implémentent l’interface [**IAnalysisWarning**](ianalysiswarning.md) et qui sont le résultat d’une opération d’analyse d’encre.</span><span class="sxs-lookup"><span data-stu-id="321e9-104">Contains a collection of objects that implement the [**IAnalysisWarning**](ianalysiswarning.md) interface and that are the result of an ink analysis operation.</span></span>

## <a name="members"></a><span data-ttu-id="321e9-105">Membres</span><span class="sxs-lookup"><span data-stu-id="321e9-105">Members</span></span>

<span data-ttu-id="321e9-106">L’interface **IAnalysisWarnings** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="321e9-106">The **IAnalysisWarnings** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="321e9-107">**IAnalysisWarnings** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="321e9-107">**IAnalysisWarnings** also has these types of members:</span></span>

-   [<span data-ttu-id="321e9-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="321e9-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="321e9-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="321e9-109">Methods</span></span>

<span data-ttu-id="321e9-110">L’interface **IAnalysisWarnings** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="321e9-110">The **IAnalysisWarnings** interface has these methods.</span></span>



| <span data-ttu-id="321e9-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="321e9-111">Method</span></span>                                                             | <span data-ttu-id="321e9-112">Description</span><span class="sxs-lookup"><span data-stu-id="321e9-112">Description</span></span>                                                                                                                                |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="321e9-113">**GetAnalysisWarning**</span><span class="sxs-lookup"><span data-stu-id="321e9-113">**GetAnalysisWarning**</span></span>](ianalysiswarnings-getanalysiswarning.md) | <span data-ttu-id="321e9-114">Récupère l’objet [**IAnalysisWarning**](ianalysiswarning.md) à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="321e9-114">Retrieves the [**IAnalysisWarning**](ianalysiswarning.md) object at the specified index.</span></span><br/>                                       |
| [<span data-ttu-id="321e9-115">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="321e9-115">**GetCount**</span></span>](ianalysiswarnings-getcount.md)                     | <span data-ttu-id="321e9-116">Récupère le nombre d’objets [**IAnalysisWarning**](ianalysiswarning.md) contenus dans la collection **IAnalysisWarnings** .</span><span class="sxs-lookup"><span data-stu-id="321e9-116">Retrieves the number of [**IAnalysisWarning**](ianalysiswarning.md) objects contained in the **IAnalysisWarnings** collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="321e9-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="321e9-117">Examples</span></span>

<span data-ttu-id="321e9-118">L’exemple suivant montre un plan d’un gestionnaire d’événements pour l’événement [**\_ IAnalysisEvents :: Results**](-ianalysisevents-results.md) .</span><span class="sxs-lookup"><span data-stu-id="321e9-118">The following example shows an outline of an event handler for the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span> <span data-ttu-id="321e9-119">Le gestionnaire vérifie [**IAnalysisStatus :: IsSuccessful**](ianalysisstatus-issuccessful.md).</span><span class="sxs-lookup"><span data-stu-id="321e9-119">The handler checks [**IAnalysisStatus::IsSuccessful**](ianalysisstatus-issuccessful.md).</span></span> <span data-ttu-id="321e9-120">Si l’opération d’analyse a généré des avertissements, le gestionnaire itère au sein de la collection d’objets [**IAnalysisWarning**](ianalysiswarning.md) .</span><span class="sxs-lookup"><span data-stu-id="321e9-120">If the analysis operation generated warnings, the handler iterates through the collection of [**IAnalysisWarning**](ianalysiswarning.md) objects.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="321e9-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="321e9-121">Requirements</span></span>



| <span data-ttu-id="321e9-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="321e9-122">Requirement</span></span> | <span data-ttu-id="321e9-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="321e9-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="321e9-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="321e9-124">Minimum supported client</span></span><br/> | <span data-ttu-id="321e9-125">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="321e9-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="321e9-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="321e9-126">Minimum supported server</span></span><br/> | <span data-ttu-id="321e9-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="321e9-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="321e9-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="321e9-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="321e9-129"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="321e9-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="321e9-130">DLL</span><span class="sxs-lookup"><span data-stu-id="321e9-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="321e9-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="321e9-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="321e9-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="321e9-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="321e9-133">**IAnalysisStatus**</span><span class="sxs-lookup"><span data-stu-id="321e9-133">**IAnalysisStatus**</span></span>](ianalysisstatus.md)
</dt> <dt>

[<span data-ttu-id="321e9-134">**IAnalysisWarning**</span><span class="sxs-lookup"><span data-stu-id="321e9-134">**IAnalysisWarning**</span></span>](ianalysiswarning.md)
</dt> <dt>

[<span data-ttu-id="321e9-135">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="321e9-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

