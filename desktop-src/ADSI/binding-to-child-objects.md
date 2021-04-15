---
title: Lier à des objets enfants
description: Dans ADSI, un objet conteneur expose l’interface IADsContainer.
ms.assetid: 16b913ea-06a4-4e85-ad6c-68817883bbd8
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, utilisation, liaison à des objets enfants
- Lier à des objets enfants
- Objets enfants, liaison à
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a73d7682dedb405c84dfaf048b8b4b2659e7fd3
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104463691"
---
# <a name="binding-to-child-objects"></a>Lier à des objets enfants

Dans ADSI, un objet conteneur expose l’interface [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) . La méthode [**IADsContainer :: GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) est utilisée pour effectuer une liaison directe à un objet enfant. L’objet retourné par **IADsContainer :: GetObject** a le même contexte de sécurité que l’objet sur lequel la méthode a été appelée. Cela signifie que si d’autres informations d’identification sont utilisées, les autres informations d’identification n’ont pas besoin d’être transmises à nouveau à la fonction ou à la méthode de liaison pour conserver les mêmes informations d’identification.

La méthode [**IADsContainer :: GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) accepte un nom unique relatif (RDN) relatif à l’objet actuel. Cette méthode prend également un nom de classe facultatif et retourne un pointeur d’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) qui représente l’objet enfant. Pour obtenir l’interface ADSI souhaitée, comme [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), appelez la méthode [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) de ce pointeur d’interface **IDispatch** .

L’exemple de code C++ suivant illustre une fonction qui récupère un objet enfant spécifié.


```C++
HRESULT GetChildObject(IADs *pObject, 
                       LPCWSTR pwszClass, 
                       LPCWSTR pwszRDN, 
                       IADs **ppChild)
{
    if(NULL == ppChild)
    {
        return E_INVALIDARG;
    }

    *ppChild = NULL;
    
    if((NULL == pObject) || (NULL == pwszRDN))
    {
        return E_INVALIDARG;
    }

    HRESULT hr;
    IADsContainer *pCont;

    hr = pObject->QueryInterface(IID_IADsContainer, (LPVOID*)&pCont);
    if(SUCCEEDED(hr))
    {
        BSTR bstrClass = NULL;
        if(pwszClass)
        {
            bstrClass = SysAllocString(pwszClass);
        }

        BSTR bstrRDN = SysAllocString(pwszRDN);
        if(bstrRDN)
        {
            IDispatch *pDisp;
            
            hr = pCont->GetObject(bstrClass, bstrRDN, &pDisp);
            if(SUCCEEDED(hr))
            {
                hr = pDisp->QueryInterface(IID_IADs, (LPVOID*)ppChild);
                
                pDisp->Release();
            }

        }
        else
        {
            hr = E_OUTOFMEMORY;
        }

        if(bstrRDN)
        {
            SysFreeString(bstrRDN);
        }

        if(bstrClass)
        {
            SysFreeString(bstrClass);
        }


        pCont->Release();
    }
    
    return hr;
}
```



 

 