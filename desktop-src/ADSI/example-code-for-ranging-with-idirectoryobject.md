---
title: Exemple de code pour IDirectoryObject
description: L’exemple de code suivant utilise pour récupérer les membres d’un groupe à l’aide de l’interface IDirectoryObject.
ms.assetid: 659b4c28-6534-45d2-80ee-14184433390d
ms.tgt_platform: multiple
keywords:
- Exemple de code pour IDirectoryObject ADSI
- Recherche de plages ADSI, exemple de code, à l’aide de IDirectoryObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0d049d629c347f0d85d8a4585436f4d7bbddf88b20186890643f7770070843a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082633"
---
# <a name="example-code-for-ranging-with-idirectoryobject"></a>Exemple de code pour IDirectoryObject

L’exemple de code suivant utilise pour récupérer les membres d’un groupe à l’aide de l’interface [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) .


```C++
//***************************************************************************
//
//  EnumGroupWithIDirectoryObject()
//
//***************************************************************************

HRESULT EnumGroupWithIDirectoryObject(LPCWSTR pwszGroupDN, 
                                      LPCWSTR pwszUsername, 
                                      LPCWSTR pwszPassword)
{
    if(NULL == pwszGroupDN)
    {
        return E_POINTER;
    }
    
    HRESULT hr;
    IDirectoryObject *pdo;

    hr = ADsOpenObject( pwszGroupDN,
                        pwszUsername,
                        pwszPassword,
                        ADS_SECURE_AUTHENTICATION,
                        IID_IDirectoryObject, 
                        (void**)&pdo);

    if(SUCCEEDED(hr))
    {
        PADS_ATTR_INFO pAttrInfo;
        const DWORD dwStep = 1000;
        DWORD dwLowRange;
        DWORD dwHighRange;
        DWORD dwRetrieved;
        WCHAR wszAttr[MAX_PATH];
        LPWSTR rgAttrs[1];

        rgAttrs[0] = wszAttr;

        dwLowRange = 0;
        dwHighRange = dwLowRange + (dwStep - 1);
         
        do
        {
            swprintf_s(wszAttr, L"member;range=%d-%d", dwLowRange, dwHighRange);
            hr = pdo->GetObjectAttributes(rgAttrs, 1, &pAttrInfo, &dwRetrieved);        
            if(SUCCEEDED(hr))
            {
                DWORD i;
                
                for(i = 0; i < dwRetrieved; i++)
                {
                    DWORD x;

                    for(x = 0; x < pAttrInfo[i].dwNumValues; x++)
                    {
                        wprintf(L"%s\n", pAttrInfo[i].pADsValues[x].CaseIgnoreString);
                    }
                }

                FreeADsMem(pAttrInfo);

                dwLowRange = dwHighRange + 1;
                dwHighRange = dwLowRange + (dwStep - 1);
            }

            if(0 == dwRetrieved)
            {
                break;
            }

        }while(SUCCEEDED(hr));
        
        pdo->Release();
    }

    return hr;
}
```



 

 




