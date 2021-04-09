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
ms.openlocfilehash: e7ff5b44288289f118c41463a22e619aa815ecb2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839181"
---
# <a name="iadsnametranslate-interface"></a>Interface IADsNameTranslate

L’interface [**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate) est utilisée pour traduire les noms distinctifs entre différents formats. Les traductions de noms sont effectuées sur le serveur d’annuaire, et cette interface n’est actuellement disponible que pour les objets de Active Directory.

L’exemple de code suivant convertit un nom de compte à partir du format Windows au format LDAP.


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



 

 




