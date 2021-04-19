---
title: Obtention des interfaces ADSI à partir de votre extension
description: Une extension doit souvent recevoir des données de l’objet annuaire auquel elle est liée.
ms.assetid: 2d2e6dc6-1eed-491b-9d6a-7f35c24a7ba8
ms.tgt_platform: multiple
keywords:
- extensions ADSI, obtention des interfaces ADSI à partir de votre extension
- ADSI ADSI, exemple de code C/C++, obtention des interfaces ADSI à partir de votre extension
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a1eeff55f2e382ce2816f59ee53dbd78033b79c
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "106509062"
---
# <a name="getting-adsi-interfaces-from-your-extension"></a>Obtention des interfaces ADSI à partir de votre extension

Une extension doit souvent recevoir des données de l’objet annuaire auquel elle est liée. Par exemple, une extension pour un objet **ordinateur** peut vouloir obtenir le **dNSHostName** de l’objet actuel à partir de l’annuaire. Cela peut être facilement effectué en émettant un appel **QueryInterface** sur l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) pour l’agrégation.


```C++
HRESULT hr;
IADs *pADs; ' ADSI Interface to get/set attributes.
 
hr = m_pOuterUnk->QueryInterface(IID_IADs,(void**)&pADs);
 
if ( SUCCEEDED(hr) )
{
    VARIANT var;
    VariantInit(&var);
    hr  = pADs ->Get(_bstr_t("dnsHostName"), &var);
    if ( SUCCEEDED(hr) )
    { 
        printf("%S\n", V_BSTR(&var));
    }
    VariantClear(&var);
    pADs->Release();
}
```



Vous devez libérer l’interface immédiatement après l’avoir utilisée. Si l’extension a une référence ouverte à l’agrégation, vous avez créé une référence circulaire et l’agrégation ne peut pas libérer l’extension. Par conséquent, l’agrégation ne peut pas être libérée et le résultat est une fuite de mémoire dans votre application.

 

 