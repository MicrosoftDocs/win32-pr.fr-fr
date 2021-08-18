---
title: Interface IADsNameTranslate
description: L’interface IADsNameTranslate est utilisée pour traduire les noms distinctifs entre différents formats. Les traductions de noms sont effectuées sur le serveur d’annuaire, et cette interface n’est actuellement disponible que pour les objets de Active Directory.
ms.assetid: c5c6e821-f19b-4269-81de-34c79dd2731f
ms.tgt_platform: multiple
keywords:
- Interface ADSI de l’interface IADsNameTranslate
- IADsTranslate ADSI, utilisation
- ADSI ADSI, exemple de code C/C++, utilisant IADsTranslate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60e167363e3c35337e74851dc43126593772aac56236f27e10a98a81b533159e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023447"
---
# <a name="iadsnametranslate-interface"></a>Interface IADsNameTranslate

L’interface [**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate) est utilisée pour traduire les noms distinctifs entre différents formats. Les traductions de noms sont effectuées sur le serveur d’annuaire, et cette interface n’est actuellement disponible que pour les objets de Active Directory.

l’exemple de code suivant convertit un nom de compte de Windows format au format LDAP.


```C++
HRESULT TranslateNTNameToLDAPName( BSTR * pNTName, BSTR * pLDAPName )
{
    IADsNameTranslate *pTrans;
    HRESULT hr = S_OK;
 
    hr = CoCreateInstance(CLSID_NameTranslate, 
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IADsNameTranslate,
                          (void**) &pTrans );
    if (FAILED(hr)) { return hr; }

    hr = pTrans->Init(ADS_NAME_INITTYPE_DOMAIN, 
                      CComBSTR("Fabrikam.com"));
    if (FAILED(hr)) { return hr; }

    hr = pTrans->Set(ADS_NAME_TYPE_NT4, *pNTName);
    if (FAILED(hr)) { return hr; }

    hr = pTrans->Get(ADS_NAME_TYPE_1779, pLDAPName);
    pTrans->Release();
    return hr;
}
```



 

 




