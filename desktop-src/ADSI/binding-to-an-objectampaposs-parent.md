---
title: Liaison au parent d’un objet
description: Dans ADSI, chaque objet d’annuaire est représenté par un objet COM ADSI qui expose l’interface IADs.
ms.assetid: 3740e862-4cfe-484c-8c8e-3923c64cdd47
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, à l’aide de, liaison au parent d’un objet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b47bfd71491c3eb0e8410f421630cec20255364b1cfc41bba7d6b48ba67fdd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118180394"
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



 

 




