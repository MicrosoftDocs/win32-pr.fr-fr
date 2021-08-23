---
title: Méthodes de propriété IADsPropertyList (IADs. h)
description: Les méthodes de propriété de l’interface IADsPropertyList lisent les propriétés décrites dans le tableau suivant. Pour plus d’informations, consultez Méthodes de propriété d’interface.
ms.assetid: 3564b61a-5950-4d00-8ea1-86fecd5c6c4e
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsPropertyList ADSI
topic_type:
- apiref
api_name:
- IADsPropertyList Property Methods
- IADsPropertyList.PropertyCount
- IADsPropertyList.get_PropertyCount
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5db37280cd72d51e0f47daa67d3b277418c077d91c9d0a07a1631ac184b4a91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023387"
---
# <a name="iadspropertylist-property-methods"></a>Méthodes de propriété IADsPropertyList

Les méthodes de propriété de l’interface [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) lisent les propriétés décrites dans le tableau suivant. Pour plus d’informations, consultez [méthodes de propriété d’interface](interface-property-methods.md).

## <a name="properties"></a>Propriétés

<dl> <dt>

**PropertyCount**
</dt> <dd> <dl>

Nombre d’éléments dans la liste de propriétés.

<dt>

Type d'accès : Lecture seule
</dt> <dt>

Type de données de script : **long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PropertyCount(
  [out] LONG* plCount
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a>Exemples

L’exemple de code suivant montre comment déterminer le nombre d’éléments dans une liste de propriétés.


```VB
Dim propList As IADsPropertyList
Dim count As Long

On Error GoTo Cleanup
 
Set propList = GetObject("LDAP://dc01/DC=Fabrikam,DC=com")
 
propList.GetInfo
count = propList.PropertyCount
Debug.Print "Number of Properties Found: " & count

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If

    Set propList = Nothing
```



L’exemple de code suivant montre comment déterminer le nombre d’éléments dans une liste de propriétés.


```C++
int GetPropertyCacheCount(LPWSTR adsPath)
{
    IADsPropertyList *pList;
    IADs *pObj;
    HRESULT hr = S_OK;

    if(!adsPath)
    {
        _tprintf(TEXT("Invalid ADsPath."));
        return -1;
    }

    HRESULT hr = ADsGetObject(adsPath,
                          IID_IADsPropertyList,
                          (void**)&pList);
    // Initialize the property cache.
    hr = pList->QueryInterface(IID_IADs,(void**)&pObj);
    pObj->GetInfo();
    pObj->Release();

    // Get the property count.
    hr = pList->get_PropertyCount(&count);
    pList->Release();

    // Return the property count if it succeeded, otherwise
    // return -1.

    if(SUCCEEDED(hr))
    {
        return count;
    }
    else
    {
        return -1;
    }

}
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsPropertyList est défini en tant que C6F602B6-8F69-11D0-8528-00C04FD8D503<br/>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist)
</dt> <dt>

[Méthodes de propriété d’interface](interface-property-methods.md)
</dt> </dl>

 

 





