---
description: En C++, chaque méthode des services de certificats retourne directement une valeur HRESULT qui indique si l’appel de la méthode a réussi ou échoué. Si l’appel a échoué, la valeur de retour indique la raison de l’échec.
ms.assetid: 4ab1b5ba-dd19-4802-aa9c-02bd5406681f
title: Vérification des erreurs en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f2a56acd41269ece0f9a5c7de4a2dff1960bb10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528719"
---
# <a name="error-checking-in-c"></a><span data-ttu-id="91f24-104">Vérification des erreurs en C++</span><span class="sxs-lookup"><span data-stu-id="91f24-104">Error Checking in C++</span></span>

<span data-ttu-id="91f24-105">En C++, chaque méthode des services de certificats retourne directement une valeur **HRESULT** qui indique si l’appel de la méthode a réussi ou échoué.</span><span class="sxs-lookup"><span data-stu-id="91f24-105">In C++, every Certificate Services method directly returns an **HRESULT** value that indicates whether the method call succeeded or failed.</span></span> <span data-ttu-id="91f24-106">Si l’appel a échoué, la valeur de retour indique la raison de l’échec.</span><span class="sxs-lookup"><span data-stu-id="91f24-106">If the call failed, the return value indicates why it failed.</span></span>

<span data-ttu-id="91f24-107">L’exemple suivant montre comment les valeurs **HRESULT** retournées peuvent être utilisées pour la vérification des erreurs.</span><span class="sxs-lookup"><span data-stu-id="91f24-107">The following example shows how the returned **HRESULT** values can be used for error checking.</span></span> <span data-ttu-id="91f24-108">Pour obtenir des exemples de codes d’erreur, consultez [valeurs HRESULT communes](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="91f24-108">For example error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>


```C++
HRESULT hr;
BSTR strAttributeName;
BSTR strAttributeValue = NULL;

if(!(strAttributeName = SysAllocString(L"TheAttribute")))
{
     printf("Could not allocate memory for attribute name.\n");
     exit(1);
}

hr = pICertServerPolicy->GetRequestAttribute(
                                strAttributeName,
                                &strAttributeValue);
if(S_OK != hr)          // Check to determine whether method failed
{
    if (E_INVALIDARG == hr)
    {
        //... Do something to recover from errors and so on.
    }
}
// Free BSTRs when finished.
if (NULL != strAttributeName)
    SysFreeString(strAttributeName);
if (NULL != strAttributeValue)
    SysFreeString(strAttributeValue);
```



 

 



