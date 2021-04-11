---
description: En C++, la valeur de retour est généralement de type HRESULT.
ms.assetid: 7abf1b3e-b94b-4846-a813-5eab5b34324c
title: Valeurs de retour en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ff7a5417019468945054f24701636fcece1d3d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202833"
---
# <a name="return-values-in-c"></a><span data-ttu-id="c4eff-103">Valeurs de retour en C++</span><span class="sxs-lookup"><span data-stu-id="c4eff-103">Return Values in C++</span></span>

<span data-ttu-id="c4eff-104">En C++, la valeur de retour est généralement de type **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="c4eff-104">In C++, the return value is typically of type **HRESULT**.</span></span> <span data-ttu-id="c4eff-105">C’est à partir de cette valeur de retour qu’il est possible de déterminer si la méthode a réussi ou non, et dans le cas contraire, quelle est l’erreur.</span><span class="sxs-lookup"><span data-stu-id="c4eff-105">It is from this return value that it can be determined whether the method succeeded or not, and if not, what the error was.</span></span> <span data-ttu-id="c4eff-106">Les services de certificats retournent généralement \_ les OK pour le **HRESULT** lorsque la méthode s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="c4eff-106">Certificate Services typically returns S\_OK for the **HRESULT** when the method has completed successfully.</span></span> <span data-ttu-id="c4eff-107">Les valeurs de programmation qui doivent être retournées sont retournées via les paramètres « out » dans la méthode.</span><span class="sxs-lookup"><span data-stu-id="c4eff-107">Programmatic values that need to be returned are returned through "out" parameters in the method.</span></span> <span data-ttu-id="c4eff-108">L’exemple suivant illustre un appel de méthode C++ pour récupérer une propriété de requête :</span><span class="sxs-lookup"><span data-stu-id="c4eff-108">The following example shows a C++ method call to retrieve a request property:</span></span>


```C++
BSTR      bstrPropName = NULL;
VARIANT   varProp;
HRESULT   hr;

VariantInit(&varProp);

bstrPropName = SysAllocString(L"RequestID");
if (NULL == bstrPropName)
{
    printf("Failed SysAllocString\n");
    // Take application-specific error action.
    exit(1);
}

// Retrieve the request property.
// pCertServerPolicy is a pointer to a previously
// instantiated ICertServerPolicy object.
hr = pCertServerPolicy->GetRequestProperty(bstrPropName,
                                           PROPTYPE_LONG,
                                           &varProp);
if (S_OK != hr)
{
    printf("Failed GetRequestProperty [%x]\n", hr);
    // Take application-specific error action.
    // ...
}
else
{
    // Successfully retrieved property; use varProp as needed.
    // ...
}

// Done processing.
VariantClear(&varProp);
if (NULL != bstrPropName)
    SysFreeString(bstrPropName);
```



<span data-ttu-id="c4eff-109">Dans le fragment de code précédent, la réussite ou l’échec est retourné à la variable **HRESULT** , *HR*.</span><span class="sxs-lookup"><span data-stu-id="c4eff-109">In the preceding code fragment, success or failure is returned to the **HRESULT** variable, *hr*.</span></span> <span data-ttu-id="c4eff-110">Il est impératif de vérifier la réussite de la variable **HRESULT** \[ dans le code par la condition (S \_ OK ! = HR) \] .</span><span class="sxs-lookup"><span data-stu-id="c4eff-110">It is imperative to check the **HRESULT** variable for success \[handled in the code by the condition (S\_OK != hr)\].</span></span> <span data-ttu-id="c4eff-111">Si la méthode s’est terminée avec succès, la valeur de la propriété Request est retournée dans le paramètre **Variant** *varProp* .</span><span class="sxs-lookup"><span data-stu-id="c4eff-111">If the method completed successfully, the request property value is returned in the **VARIANT** *varProp* parameter.</span></span>

 

 



