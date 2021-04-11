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
# <a name="return-values-in-c"></a>Valeurs de retour en C++

En C++, la valeur de retour est généralement de type **HRESULT**. C’est à partir de cette valeur de retour qu’il est possible de déterminer si la méthode a réussi ou non, et dans le cas contraire, quelle est l’erreur. Les services de certificats retournent généralement \_ les OK pour le **HRESULT** lorsque la méthode s’est terminée avec succès. Les valeurs de programmation qui doivent être retournées sont retournées via les paramètres « out » dans la méthode. L’exemple suivant illustre un appel de méthode C++ pour récupérer une propriété de requête :


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



Dans le fragment de code précédent, la réussite ou l’échec est retourné à la variable **HRESULT** , *HR*. Il est impératif de vérifier la réussite de la variable **HRESULT** \[ dans le code par la condition (S \_ OK ! = HR) \] . Si la méthode s’est terminée avec succès, la valeur de la propriété Request est retournée dans le paramètre **Variant** *varProp* .

 

 



