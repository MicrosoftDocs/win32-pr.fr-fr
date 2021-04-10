---
title: Méthodes de propriété IADsContainer (IADs. h)
description: Les méthodes de propriété de l’interface IADsContainer obtiennent ou définissent les propriétés décrites dans le tableau suivant. Pour plus d’informations et pour obtenir une discussion générale sur les méthodes de propriété, consultez Méthodes de propriété d’interface.
ms.assetid: 74d348bf-7b7f-4971-ba03-f77940600674
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsContainer ADSI
topic_type:
- apiref
api_name:
- IADsContainer Property Methods
- IADsContainer.Count
- IADsContainer.get_Count
- IADsContainer.Filter
- IADsContainer.get_Filter
- IADsContainer.put_Filter
- IADsContainer.Hints
- IADsContainer.get_Hints
- IADsContainer.put_Hints
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5196addda0d9ff89f8a4976f3197bbeeae07044
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105151"
---
# <a name="iadscontainer-property-methods"></a>Méthodes de propriété IADsContainer

Les méthodes de propriété de l’interface [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) obtiennent ou définissent les propriétés décrites dans le tableau suivant. Pour plus d’informations et pour obtenir une discussion générale sur les méthodes de propriété, consultez [méthodes de propriété d’interface](interface-property-methods.md).

## <a name="properties"></a>Propriétés

<dl> <dt>

**Count**
</dt> <dd> <dl>

Récupère le nombre d’éléments dans le conteneur. Quand le **filtre** est défini, **Count** retourne uniquement le nombre d’éléments filtrés.

<dt>

Type d'accès : Lecture seule
</dt> <dt>

Type de données de script : **long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Count(
  [out] LONG* plCount
);
```


</dt> </dl> </dd> <dt>

**Filter**
</dt> <dd> <dl>

Récupère ou définit le filtre utilisé pour sélectionner des classes d’objet dans une énumération donnée. Il s’agit d’un tableau variant, dont chaque élément est le nom d’une classe de schéma. Si le **filtre** n’est pas défini ou n’est pas défini sur vide, tous les objets de toutes les classes sont récupérés par l’énumérateur.

<dt>

Type d’accès : lecture/écriture
</dt> <dt>

Type de données de script : **variante**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Filter(
  [out] VARIANT* pvFilter
);
HRESULT put_Filter(
  [in] VARIANT vFilter
);
```


</dt> </dl> </dd> <dt>

**Indicateurs**
</dt> <dd> <dl>

Tableau de variant de chaînes **BSTR** . Chaque élément identifie le nom d’une propriété trouvée dans la définition de schéma. Le paramètre *vHints* permet au client d’indiquer les attributs à charger pour chaque objet énuméré. Ces données peuvent être utilisées pour optimiser l’accès réseau. L’implémentation exacte, toutefois, est spécifique au fournisseur et n’est actuellement pas utilisée par le fournisseur Winnt.

<dt>

Type d’accès : lecture/écriture
</dt> <dt>

Type de données de script : **variante**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Hints(
  [out] VARIANT* pvHints
);
HRESULT put_Hints(
  [in] VARIANT vHints
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>Notes

Les processus d’énumération sous [**IADsContainer :: obten \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscontainer-get__newenum) et **IADsContainer :: obtient \_ Count** sont effectués sur les objets contenus dans le cache. Lorsqu’un conteneur contient un grand nombre d’objets, les performances peuvent être affectées. Pour améliorer les performances, désactivez le cache, configurez une taille de page appropriée et utilisez l’interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) . Pour cette raison, la propriété **obtenir le \_ nombre** n’est pas prise en charge dans le fournisseur LDAP Microsoft.

## <a name="examples"></a>Exemples

L’exemple de code Visual Basic suivant montre comment les méthodes de propriété de [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) peuvent être utilisées.


```VB
Dim cont As IADsContainer
Dim usr As IADsUser

On Error GoTo Cleanup
 
Set cont = GetObject("LDAP://OU=Sales, DC=Fabrikam, DC=COM")
cont.Hints = Array("adminDescription") ' Load this attribute. Optional.
Debug.Print cont.Get("adminDescription")

' Filter users.
cont.Filter = Array("user")

For Each usr In cont
  Debug.Print usr.Name
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set cont = Nothing
    Set usr = Nothing
```



L’exemple de code C++ suivant montre comment les méthodes de propriété de [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) peuvent être utilisées. Par souci de concision, la vérification des erreurs est omise.


```C++
IADsContainer *pCont;
IADs *pChild;
IADs *pADs;
 
HRESULT hr = ADsGetObject(L"LDAP://OU=Sales,DC=Fabrikam,DC=COM",
                          IID_IADsContainer, 
                          (void**)&pCont);

if(FAILED(hr)){goto Cleanup;}

LPWSTR pszArray[] = { L"adminDescription" };
DWORD dwNumber = sizeof(pszArray)/sizeof(LPWSTR);
hr = ADsBuildVarArrayStr( pszArray, dwNumber, &var);
if(FAILED(hr)){goto Cleanup;}

hr = pCont->put_Hints( var );
if(FAILED(hr)){goto Cleanup;}

VariantClear(&var);
 
hr = pCont->QueryInterface(IID_IADs, (void**)pADs);
if(FAILED(hr)){goto Cleanup;}
 
hr = pADs->Get(CComBSTR("adminDescription"), var);
 
LPWSTR pszUsers = {L"user"};
dwNumber = sizeof(pszUsers)/sizeof(LPWSTR);
hr = ADsBuildVarArrayStr(pszUsers, dwNumber, &var);
hr = pCont->put_Filter( var );
VariantClear(&var);
 
// Enumerate user objects in the container.
IEnumVARIANT *pEnum = NULL;
hr = ADsBuildEnumerator(pCont, &pEnum);
pCont->Release();    // Not required when users are enumerated.
 
ULONG lFetch;
VariantClear(&var);
while (SUCCEEDED(ADsEnumerateNext(pEnum, 1, &var, &lFetch)) && 
                      lFetch==1) {
    hr = V_DISPATCH(&var)->QueryInterface(IID_IADs, (void**)&pChild)
    if(SUCCEEDED(hr)) {
        BSTR bstrName;
        pChild->get_Name(&bstrName);
        printf("  %S\n", bstrName);
        SysFreeString(bstrName);
        pChild->Release();
    }
    VariantClear(&var);
}
Cleanup:
    if(pADs)
        pADs->Release();

    if(pCont)
        pCont->Release();

    if(pChild)
        pChild->Release();

    VariantClear(&var);
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsContainer est défini en tant que 001677D0-FD16-11CE-ABC4-02608C9E7553<br/>        |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)
</dt> <dt>

[**Rubrique IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)
</dt> </dl>

 

 





