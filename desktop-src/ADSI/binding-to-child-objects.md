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
# <a name="binding-to-child-objects"></a><span data-ttu-id="d96d9-106">Lier à des objets enfants</span><span class="sxs-lookup"><span data-stu-id="d96d9-106">Binding to Child Objects</span></span>

<span data-ttu-id="d96d9-107">Dans ADSI, un objet conteneur expose l’interface [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) .</span><span class="sxs-lookup"><span data-stu-id="d96d9-107">In ADSI, a container object exposes the [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) interface.</span></span> <span data-ttu-id="d96d9-108">La méthode [**IADsContainer :: GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) est utilisée pour effectuer une liaison directe à un objet enfant.</span><span class="sxs-lookup"><span data-stu-id="d96d9-108">The [**IADsContainer::GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) method is used to bind directly to a child object.</span></span> <span data-ttu-id="d96d9-109">L’objet retourné par **IADsContainer :: GetObject** a le même contexte de sécurité que l’objet sur lequel la méthode a été appelée.</span><span class="sxs-lookup"><span data-stu-id="d96d9-109">The object returned by **IADsContainer::GetObject** has the same security context as the object on which the method was called.</span></span> <span data-ttu-id="d96d9-110">Cela signifie que si d’autres informations d’identification sont utilisées, les autres informations d’identification n’ont pas besoin d’être transmises à nouveau à la fonction ou à la méthode de liaison pour conserver les mêmes informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="d96d9-110">This means that if alternate credentials are used, the alternate credentials do not have to be passed to the binding function or method again to maintain the same credentials.</span></span>

<span data-ttu-id="d96d9-111">La méthode [**IADsContainer :: GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) accepte un nom unique relatif (RDN) relatif à l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="d96d9-111">The [**IADsContainer::GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) method takes a relative distinguished name (RDN) that is relative to the current object.</span></span> <span data-ttu-id="d96d9-112">Cette méthode prend également un nom de classe facultatif et retourne un pointeur d’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) qui représente l’objet enfant.</span><span class="sxs-lookup"><span data-stu-id="d96d9-112">This method also takes an optional class name and returns an [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface pointer that represents the child object.</span></span> <span data-ttu-id="d96d9-113">Pour obtenir l’interface ADSI souhaitée, comme [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), appelez la méthode [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) de ce pointeur d’interface **IDispatch** .</span><span class="sxs-lookup"><span data-stu-id="d96d9-113">To obtain the desired ADSI interface, such as [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), call the [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method of this **IDispatch** interface pointer.</span></span>

<span data-ttu-id="d96d9-114">L’exemple de code C++ suivant illustre une fonction qui récupère un objet enfant spécifié.</span><span class="sxs-lookup"><span data-stu-id="d96d9-114">The following C++ code example shows a function that retrieves a specified child object.</span></span>


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



 

 