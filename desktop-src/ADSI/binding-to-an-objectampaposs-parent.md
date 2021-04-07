---
title: Liaison au parent d’un objet
description: Dans ADSI, chaque objet d’annuaire est représenté par un objet COM ADSI qui expose l’interface IADs.
ms.assetid: 3740e862-4cfe-484c-8c8e-3923c64cdd47
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, à l’aide de, liaison au parent d’un objet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7d72f3b3db3af9f13892494d3855dc5dcb2a74d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839233"
---
# <a name="binding-to-an-objects-parent"></a>Liaison au parent d’un objet

Dans ADSI, chaque objet d’annuaire est représenté par un objet COM ADSI qui expose l’interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) . Pour obtenir le conteneur parent d’un objet, utilisez la méthode [**IADs :: obtenir \_ parent**](iads-property-methods.md) pour obtenir le ADsPath de l’objet parent, puis liez-le à l’ADsPath du parent.

L’exemple de code C++ suivant montre comment obtenir le parent d’un objet.


```C++
HRESULT GetParentObject(IADs *pObject,   // Pointer to the object whose parent to bind to.
                        IADs **ppParent) // Return a pointer to the parent object.
{
    if(NULL == ppParent)
    {
        return E_INVALIDARG;
    }
 
    *ppParent = NULL;

    if(NULL == pObject)
    {
        return E_INVALIDARG;
    }
 
    HRESULT hr;
    BSTR bstr;

    // Get the ADsPath of the parent.
    hr = pObject->get_Parent(&bstr);
    if(SUCCEEDED(hr))
    {
        // Bind to the parent.
        hr = ADsOpenObject(bstr,
             NULL,
             NULL,
             ADS_SECURE_AUTHENTICATION,
             IID_IADs,
             (void**)ppParent);

        SysFreeString(bstr);
    }

    return hr;
}
```



 

 




