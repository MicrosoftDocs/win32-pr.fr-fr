---
description: Les variables de type VARIANT ont un champ de balise de type VT qui indique le type de données des données.
ms.assetid: 3436faf6-2e66-46a1-b1e8-84f513282c16
title: Définition du champ de balise de type
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e443fae33b14bd4270e63188ff96a042a91c8e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201209"
---
# <a name="setting-the-type-tag-field"></a>Définition du champ de balise de type

Les variables de type **Variant** ont un champ de balise de type **VT** qui indique le type de données des données. Les valeurs de retour de type **Variant** sont retournées par les méthodes avec le champ type tag défini sur le type de données de la valeur de retour. Les paramètres d’entrée de type **Variant** dans un appel de méthode doivent avoir le champ de balise de type défini par l’application sur l’une des valeurs prises en charge. La correspondance entre les types de paramètres et les types de données est la suivante.



| Type de paramètre              | Type de données                                      |
|-----------------------------|------------------------------------------------|
| PROPTYPE \_ long<br/>   | VT \_ I2 ou VT \_ I4<br/>                    |
| \_Date PROPTYPE<br/>   | \_Date VT<br/>                            |
| \_binaire PROPTYPE<br/> | VT \_ BSTR ou (VT \_ BSTR \| VT \_ ByRef)<br/> |
| \_chaîne PROPTYPE<br/> | VT \_ BSTR ou (VT \_ BSTR \| VT \_ ByRef)<br/> |



 

L’exemple suivant montre comment initialiser les types de données variant listés ci-dessus.


```C++
HRESULT hr;
VARIANT vEMail;
VARIANT vNotBefore;
VARIANT vCount;
VARIANT vByRef;
BSTR bstr = NULL;
SYSTEMTIME st;

//Set the BSTR variant data type.
VariantInit(&vEMail);
vEMail.vt = VT_BSTR;   
vEMail.bstrVal = SysAllocString(L"someone@example.com");
if (NULL == vEMail.bstrVal)
{
    hr = E_OUTOFMEMORY;
    //Handle error.   
}
//Use the variant.
VariantClear(&vEMail);  //when done


//Set the BSTR|BYREF variant data type.
VariantInit(&vByRef);
vByRef.vt = VT_BSTR | VT_BYREF;   
vByRef.pbstrVal = &bstr;
//Use the variant.
VariantClear(&vByRef);  //when done
SysFreeString(bstr);


//Set the DATE variant data type.
memset(&st, 0, sizeof(SYSTEMTIME));
st.wYear = 2000;
st.wMonth = 1;
st.wDay = 1;
st.wHour = 12;

VariantInit(&vNotBefore);
vNotBefore.vt = VT_DATE;
if (!SystemTimeToVariantTime(&st, &vNotBefore.date))
{
    hr = E_FAIL;
    //Handle error.
}
//Use the variant.
VariantClear(&vNotBefore);  //when done


//Set the LONG variant data type.
VariantInit(&vCount);
vCount.vt = VT_I4;
vCount.long = 123456;
//Use the variant.
VariantClear(&vCount);  //when done
```



 

 




