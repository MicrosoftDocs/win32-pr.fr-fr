---
title: Interface IADsObjectOptions
description: L’interface IADsObjectOptions permet un accès direct à la définition et à la récupération d’options spécifiques au fournisseur.
ms.assetid: b4ac114f-1a23-4be6-af02-0c0d34a8f78f
ms.tgt_platform: multiple
keywords:
- Interface ADSI de l’interface IADsObjectOptions
- IADsObjectOptions ADSI, utilisation
- ADSI ADSI, exemple de code C/C++, utilisant IADsObjectOptions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43701b4b846e4bf4e69dc8882397b5aba6b19ffc370ba418a34239782433073f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117839922"
---
# <a name="iadsobjectoptions-interface"></a>Interface IADsObjectOptions

L’interface [**IADsObjectOptions**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions) permet un accès direct à la définition et à la récupération d’options spécifiques au fournisseur.

L’une des options de l’objet Active Directory consiste à retourner le nom d’hôte d’un serveur. L’exemple de code suivant utilise l’interface pour récupérer le nom d’hôte du serveur de catalogue global.


```C++
HRESULT GetGCServerName(VARIANT *vGCServer) 
{
    HRESULT hr = S_OK
    HRESULT hre = S_OK;
    IADsContainer *pContainer = NULL;
    IUnknown *pUnk = NULL;
    IEnumVARIANT *pEnum = NULL;
    IDispatch *pDisp = NULL;
    IADsObjectOptions *pOpt = NULL;
    VARIANT var;
    ULONG lFetch = 0;

    VariantInit(&var);
 
    // Bind to the global catalog using a serverless bind.
    hr = ADsOpenObject(L"GC:", NULL, NULL,
                       ADS_SECURE_AUTHENTICATION,
                       IID_IADsContainer, (void**) &pContainer );
    if (FAILED(hr))
        return (hr);
 
    hr = pContainer->get__NewEnum(&pUnk);
    if (SUCCEEDED(hr))
    {
        hr = pUnk->QueryInterface(IID_IEnumVARIANT, (void**) &pEnum);
        if (SUCCEEDED(hr))
        {
            // Enumerate.
            hr = pEnum->Next(1, &var, &lFetch);
            if (SUCCEEDED(hr))
            {
                while (SUCCEEDED(hr))
                {
                    if (lFetch == 1)
                    {
                        pDisp = V_DISPATCH(&var);
                        hre = pDisp->QueryInterface(
                                          IID_IADsObjectOptions,
                                          (void**)&pOpt);
                        if (pDisp)
                            pDisp->Release();
                    }
                    VariantClear(&var);
                    hr = pEnum->Next(1, &var, &lFetch);
                }
                // S_FALSE indicates that the row was read properly.
                if (hr == S_FALSE)
                    hr = hre;
            }
 
            if (SUCCEEDED(hr))
            {
                // There is a valid pOpt, so request the server name.
                VariantInit(vGCServer);
                hr = pOpt->GetOption(ADS_OPTION_SERVERNAME,vGCServer);
            }
        }
    }
 
// Cleanup.
    VariantClear(&var);
    if (pOpt)
        pOpt->Release();
    if (pEnum)
        pEnum->Release();
    if (pUnk)
        pUnk->Release();
    if (pContainer)
        pContainer->Release();
    return (hr);
}
```



 

 




