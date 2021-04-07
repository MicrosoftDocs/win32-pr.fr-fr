---
title: Extension de classe d’assistance NDF avec remise
description: Cette classe d’assistance a une dépendance d’intégrité faible sur le SimpleFileHelperClass codé dans le premier exemple.
ms.assetid: b59cd855-c68a-4f5c-b145-ceac395ddcc4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b799b795fcf23cbddf268056e23db433566c8a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939956"
---
# <a name="ndf-helper-class-extension-with-handoff"></a><span data-ttu-id="ca541-103">Extension de classe d’assistance NDF avec remise</span><span class="sxs-lookup"><span data-stu-id="ca541-103">NDF Helper Class Extension with Handoff</span></span>

<span data-ttu-id="ca541-104">Cette classe d’assistance a une dépendance d’intégrité faible sur le SimpleFileHelperClass codé dans le premier exemple.</span><span class="sxs-lookup"><span data-stu-id="ca541-104">This Helper Class has a low-health dependency on the SimpleFileHelperClass coded in the first example.</span></span>

<span data-ttu-id="ca541-105">La deuxième classe d’assistance de transfert est une classe d’assistance directe simple qui n’effectue pas de diagnostic lui-même.</span><span class="sxs-lookup"><span data-stu-id="ca541-105">The second handoff helper class is a simple pass-through helper class which does not perform any diagnosis itself.</span></span> <span data-ttu-id="ca541-106">Au lieu de cela, il génère toujours une hypothèse d’intégrité inférieure pour le SimpleFileHelperClass.</span><span class="sxs-lookup"><span data-stu-id="ca541-106">Instead, it always generates lower health hypothesis for the SimpleFileHelperClass.</span></span> <span data-ttu-id="ca541-107">Cela est utile pour servir d’espace réservé pour l’ajout ultérieur de la fonctionnalité de diagnostic dans cette classe d’assistance.</span><span class="sxs-lookup"><span data-stu-id="ca541-107">This is useful in serving as a placeholder for future addition of diagnostics capability in this helper class.</span></span> <span data-ttu-id="ca541-108">La classe d’assistance de transfert implémente deux méthodes.</span><span class="sxs-lookup"><span data-stu-id="ca541-108">The handoff helper class implements two methods.</span></span>

<span data-ttu-id="ca541-109">La méthode LowHealth est utilisée pour définir l’état du diagnostic sur DS \_ Indeterminate.</span><span class="sxs-lookup"><span data-stu-id="ca541-109">The LowHealth method is used to set the Diagnosis Status to DS\_INDETERMINATE.</span></span> <span data-ttu-id="ca541-110">Cela rend l’appel NDF GetLowerHypotheses.</span><span class="sxs-lookup"><span data-stu-id="ca541-110">This makes NDF call GetLowerHypotheses.</span></span>


```C++
#include <windows.h>

HRESULT HandOffTestHelperClass::LowHealth( 
    /* [unique][string][in] */ LPCWSTR pwszInstanceDescription,
    /* [string][out] */ LPWSTR *ppwszDescription,
    /* [out] */ long *pDeferredTime,
    /* [out] */ DIAGNOSIS_STATUS *pStatus) 

{
    *pStatus = DS_INDETERMINATE;
    return S_OK;
}

```



<span data-ttu-id="ca541-111">Ensuite, GetLowerHypotheses est implémenté pour indiquer à NDF la classe d’assistance à diagnostiquer.</span><span class="sxs-lookup"><span data-stu-id="ca541-111">Next, GetLowerHypotheses is implemented to tell NDF which Helper Class to diagnose.</span></span>


```C++
#include <windows.h>

HRESULT HandOffTestHelperClass::GetLowerHypotheses( 
ULONG *Count,
HYPOTHESIS **Hypotheses)
{
    HRESULT hr = S_OK;
    HYPOTHESIS *pHypothesis=NULL;
    HELPER_ATTRIBUTE *pAttr=NULL;

    pHypothesis = (PHYPOTHESIS)CoTaskMemAlloc(sizeof(HYPOTHESIS));
    if (pHypothesis == NULL)
    {
        return E_OUTOFMEMORY;
    }
    SecureZeroMemory(pHypothesis, sizeof(HYPOTHESIS));

    pAttr = (PHELPER_ATTRIBUTE)CoTaskMemAlloc(sizeof(HELPER_ATTRIBUTE));
    if (pAttr  == NULL)
    {
       hr = E_OUTOFMEMORY;
       goto Error;
    }
    SecureZeroMemory(pAttr, sizeof(HELPER_ATTRIBUTE));

    //set the helper class name to hand off to
    hr = StringCchCopyWithAlloc(&pHypothesis->pwszClassName, MAX_PATH,
                 L"SimpleFileHelperClass");
    if (FAILED(hr))
    {
        goto Error;
    }

    //populate the attribute
    //set the attribute name
    hr = StringCchCopyWithAlloc(&pAttr->pwszName, MAX_PATH, L"filename");
    if (FAILED(hr))
    {
        goto Error;  
    }

    //set attribute data
    pAttr->type = AT_STRING;
    hr = StringCchCopyWithAlloc(&pAttr->PWStr, MAX_PATH, m_pwszTestFile);
    if (FAILED(hr))
    {
        goto Error;
    }

    //set the attributes to the hypothesis  
    pHypothesis->celt = 1; //number of attributes
    pHypothesis->rgAttributes=pAttr;

    //pass data back
    *pcelt = 1; //one hypothesis
    *pprgHypotheses = pHypothesis;

    return S_OK;

Error:

    if (pAttr)
    {
        if (pAttr->PWStr) 
            CoTaskMemFree(pAttr->PWStr);
        if (pAttr->pwszName) 
            CoTaskMemFree(pAttr->pwszName);
    }

    if (pHypothesis)
    {
        if (pHypothesis->pwszClassName) 
            CoTaskMemFree(pHypothesis->pwszClassName);
        CoTaskMemFree(pHypothesis);
    }
    return hr;
}

```



 

 




