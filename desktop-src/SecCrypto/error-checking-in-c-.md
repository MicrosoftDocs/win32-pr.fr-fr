---
description: En C++, chaque méthode des services de certificats retourne directement une valeur HRESULT qui indique si l’appel de la méthode a réussi ou échoué. Si l’appel a échoué, la valeur de retour indique la raison de l’échec.
ms.assetid: 4ab1b5ba-dd19-4802-aa9c-02bd5406681f
title: Vérification des erreurs en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc3e374c6f0bd933c2e4de7a477fea02b4e1538a7a1fa9b4de78e45fd896b192
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874069"
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



 

 



