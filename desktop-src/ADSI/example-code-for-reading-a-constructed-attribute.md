---
title: Exemple de code pour la lecture d’un attribut construit
description: cette rubrique contient des exemples de code VB et C++ qui montrent comment lire un attribut construit.
ms.assetid: c4acc848-f89e-4cd1-905a-2ed20443b03c
ms.tgt_platform: multiple
keywords:
- Exemple de code pour la lecture d’un attribut construit ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcd51e5649ec0b2b9e654eb160c4fe8708f4743fbdd1dfe55e85231c7a451e2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117840009"
---
# <a name="example-code-for-reading-a-constructed-attribute"></a>Exemple de code pour la lecture d’un attribut construit

L’exemple de code suivant montre une méthode qui peut être utilisée pour récupérer une valeur d’attribut qui fonctionne avec tous les types d’attributs.


```VB
Public Function GetAttribute(oObject As IADs, AttributeName As String) As String
    Const E_ADS_PROPERTY_NOT_FOUND = &H8000500D
    
    On Error Resume Next
    
    ' Attempt to get the attribute value.
    GetAttribute = oObject.Get(AttributeName)
    If (Err.Number = E_ADS_PROPERTY_NOT_FOUND) Then
        ' Reset the error number.
        Err.Number = 0
        
        ' Use IADs.GetInfoEx to explicitly load the attribute value into the cache.
        oObject.GetInfoEx Array(AttributeName), 0
        If Err.Number = 0 Then
            ' Attempt to get the attribute value.
            GetAttribute = oObject.Get(AttributeName)
        End If
    End If
End Function
```



L’exemple de code suivant montre une méthode qui peut être utilisée pour récupérer une valeur d’attribut qui fonctionne avec tous les types d’attributs.


```C++
/***************************************************************************

    GetAttribute()

***************************************************************************/

HRESULT GetAttribute(IADs *pads, BSTR bstrAttribute, VARIANT *pvar)
{
    if(!pads || !pvar)
    {
        return E_INVALIDARG;
    }

    HRESULT hr;
    CComVariant svar;

    // Attempt to get the attribute with IADs.Get.
    hr = pads->Get(bstrAttribute, &svar);
    if(E_ADS_PROPERTY_NOT_FOUND  == hr)
    {
        // Attempt to get the attribute with IADs.GetInfoEx and then IADs.Get.

        CComVariant svarArray;
        hr = ADsBuildVarArrayStr(&(LPWSTR)bstrAttribute, 1, &svarArray);
        if (SUCCEEDED(hr))
        {
            hr = pads->GetInfoEx(svarArray, 0L);
            if(SUCCEEDED(hr))
            {
                hr = pads->Get(bstrAttribute, &svar);
            }
        }

    }

    if(S_OK == hr)
    {
        hr = svar.Detach(pvar);
    }

    return hr;
}
```



 

 




