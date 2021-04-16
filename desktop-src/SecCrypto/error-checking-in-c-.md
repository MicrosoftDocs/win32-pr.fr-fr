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
# <a name="error-checking-in-c"></a>Vérification des erreurs en C++

En C++, chaque méthode des services de certificats retourne directement une valeur **HRESULT** qui indique si l’appel de la méthode a réussi ou échoué. Si l’appel a échoué, la valeur de retour indique la raison de l’échec.

L’exemple suivant montre comment les valeurs **HRESULT** retournées peuvent être utilisées pour la vérification des erreurs. Pour obtenir des exemples de codes d’erreur, consultez [valeurs HRESULT communes](common-hresult-values.md).


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



 

 



