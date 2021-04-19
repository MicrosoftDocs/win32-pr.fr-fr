---
title: Méthodes de propriété IADsGroup (IADs. h)
description: Méthodes de propriété de l’interface IADsGroup.
ms.assetid: a8aa88d4-4695-47bc-bf7f-a17236a5671c
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsGroup ADSI
topic_type:
- apiref
api_name:
- IADsGroup Property Methods
- IADsGroup.Description
- IADsGroup.get_Description
- IADsGroup.put_Description
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 665cb91a55298012e4e906c2972da5371e3960be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106515073"
---
# <a name="iadsgroup-property-methods"></a>Méthodes de propriété IADsGroup

Les méthodes de propriété de l’interface [**IADsGroup**](/windows/desktop/api/Iads/nn-iads-iadsgroup) lisent et écrivent les propriétés suivantes. Pour plus d’informations, consultez [méthodes de propriété d’interface](interface-property-methods.md).

## <a name="properties"></a>Propriétés

<dl> <dt>

**Description**
</dt> <dd> <dl>

Indique la description textuelle de l’appartenance au groupe.

<dt>

Type d’accès : lecture/écriture
</dt> <dt>

Type de données de script : **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Description(
  [out] BSTR* pbstrDescription
);
HRESULT put_Description(
  [in] BSTR bstrDescription
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>Notes

### <a name="using-iadsgroup-to-retrieve-descriptions-of-built-in-groups"></a>Utilisation de IADsGroup pour récupérer les descriptions des groupes prédéfinis

Les exemples suivants montrent comment récupérer des informations sur les objets de groupe Windows par nom. Dans un environnement multilingue, les groupes intégrés sont parfois connus par différents noms localisés, ce qui signifie qu’ils ne peuvent pas être récupérés directement à l’aide d’identificateurs de chaîne tels que « WinNT://Microsoft/Administrators ». Dans ce cas, l’utilisateur peut effectuer une liaison à l’objet SID connu pour le groupe, récupérer le nom de groupe localisé et le fournir à la méthode GetObject. Pour plus d’informations, consultez [sid connus](/windows/desktop/SecAuthZ/well-known-sids).

## <a name="examples"></a>Exemples

L’exemple de Visual Basic suivant montre comment effectuer une liaison à un objet de groupe et afficher la description du groupe.


```VB
Dim grp As IADsGroup
On Error GoTo Cleanup

Set grp = GetObject("WinNT://Microsoft/Administrators")
Debug.Print grp.Description

Cleanup
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set grp = Nothing
```



L’exemple C++ suivant montre comment effectuer une liaison à un objet de groupe et afficher la description du groupe.


```C++
IADsGroup *pGroup = NULL;
HRESULT hr = S_OK;
LPWSTR adsPath = L"WinNT://localHost/Administrators";
BSTR bstr;

hr = ADsGetObject(adsPath,IID_IADsGroup,(void**)&pGroup);

if(FAILED(hr)) {goto Cleanup;}

hr = pGroup->get_Description(&bstr);
if(FAILED(hr)) {goto Cleanup;}

printf("Description: %S\n",bstr);

Cleanup:
    SysFreeString(bstr);
    if(pGroup) 
        pGroup->Release();

    return hr;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsGroup est défini en tant que 27636B00-410f-11CF-B1FF-02608C9E7553<br/>            |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IADs**](/windows/desktop/api/Iads/nn-iads-iads)
</dt> <dt>

[**IADsGroup**](/windows/desktop/api/Iads/nn-iads-iadsgroup)
</dt> <dt>

[Méthodes de propriété d’interface](interface-property-methods.md)
</dt> </dl>

 

