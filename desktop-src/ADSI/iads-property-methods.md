---
title: Méthodes de propriété IADs (IADs. h)
description: Les méthodes de propriété de l’interface IADss obtiennent ou définissent les propriétés décrites dans le tableau suivant. Pour plus d’informations sur les méthodes de propriété, consultez Méthodes de propriété d’interface.
ms.assetid: d2f6f686-a35a-4a9a-9b57-2ceb2f26ef12
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADs ADSI
topic_type:
- apiref
api_name:
- IADs Property Methods
- IADs.ADsPath
- IADs.get_ADsPath
- IADs.Class
- IADs.get_Class
- IADs.GUID
- IADs.get_GUID
- IADs.Name
- IADs.get_Name
- IADs.Parent
- IADs.get_Parent
- IADs.Schema
- IADs.get_Schema
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1134260c780958bcdba8d1f14eac535ddbf4ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508345"
---
# <a name="iads-property-methods"></a>Méthodes de propriété IADs

Les méthodes de propriété de l’interface [**iadss**](/windows/desktop/api/Iads/nn-iads-iads) obtiennent ou définissent les propriétés décrites dans le tableau suivant. Pour plus d’informations sur les méthodes de propriété, consultez [méthodes de propriété d’interface](interface-property-methods.md).

## <a name="properties"></a>Propriétés

<dl> <dt>

**ADsPath**
</dt> <dd> <dl>

Chaîne ADsPath de cet objet. La chaîne identifie cet objet de manière unique dans un environnement réseau. L’objet peut toujours être récupéré à l’aide de ce chemin d’accès.

<dt>

Type d'accès : Lecture seule
</dt> <dt>

Type de données de script : **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ADsPath(
  [out] BSTR* pbstrADsPath
);
```


</dt> </dl> </dd> <dt>

**Classe**
</dt> <dd> <dl>

Nom de la classe de schéma de l’objet.

<dt>

Type d'accès : Lecture seule
</dt> <dt>

Type de données de script : **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Class(
  [out] BSTR* pbstrClass
);
```


</dt> </dl> </dd> <dt>

**GUID**
</dt> <dd> <dl>

Identificateur global unique de l’objet d’annuaire. L’interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) convertit le **GUID** d’une chaîne d’octets, telle qu’elle est stockée sur un serveur d’annuaire, en un format de chaîne.

<dt>

Type d'accès : Lecture seule
</dt> <dt>

Type de données de script : **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_GUID(
  [out] BSTR* pbstrGUID
);
```


</dt> </dl> </dd> <dt>

**Nom**
</dt> <dd> <dl>

Nom relatif de l’objet, tel que nommé dans le service d’annuaire sous-jacent. Ce nom distingue cet objet de ses frères.

<dt>

Type d'accès : Lecture seule
</dt> <dt>

Type de données de script : **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Name(
  [out] BSTR* pbstrName
);
```


</dt> </dl> </dd> <dt>

**Parent**
</dt> <dd> <dl>

Chaîne ADsPath du conteneur parent. Active Directory n’autorise pas la formation de l’ADsPath d’un objet donné en concaténant les propriétés **parent** et **Name** . Bien que cette opération puisse fonctionner dans certains fournisseurs, il n’est pas garanti qu’elle fonctionne pour toutes les implémentations. La validité de l’ADsPath est garantie et doit toujours être utilisée pour récupérer le pointeur d’interface d’un objet.

<dt>

Type d'accès : Lecture seule
</dt> <dt>

Type de données de script : **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Parent(
  [out] BSTR* pbstrParent
);
```


</dt> </dl> </dd> <dt>

**Schéma**
</dt> <dd> <dl>

Chaîne ADsPath de l’objet de classe de schéma de cet objet.

<dt>

Type d'accès : Lecture seule
</dt> <dt>

Type de données de script : **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Schema(
  [out] BSTR* pbstrSchema
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>Notes

Dans Active Directory, le **GUID** renvoyé à partir du GUID est une chaîne de caractères hexadécimaux. Utilisez le **GUID** résultant pour effectuer une liaison directe à l’objet.


```VB
Dim x As IADs
Set x = GetObject("LDAP://servername/<GUID=xxx>")
```



où xxx est la valeur retournée par la propriété GUID. Pour plus d’informations, consultez [utilisation d’objectGUID pour la liaison à un objet](/windows/desktop/AD/using-objectguid-to-bind-to-an-object). Sachez que si vous utilisez un GUID pour établir une liaison à un objet, la méthode de propriété **ADsPath** retourne des valeurs qui sont différentes des valeurs normales qui seraient retournées si vous avez utilisé un nom unique (DN) pour créer une liaison avec le même objet. Par exemple, le tableau suivant répertorie les valeurs retournées lors de l’utilisation des deux méthodes de liaison différentes pour effectuer une liaison au même objet utilisateur.



|             | Lier à l’aide de DN                                           | Lier à l’aide du GUID                                             |
|-------------|---------------------------------------------------------|-------------------------------------------------------------|
| **Nom**    | CN = Jeff Smith                                           | CN = Jeff Smith                                               |
| **Parent**  | LDAP://server/CN=Users,DC=Fabrikam,DC=com               | LDAP://server/CN=Users,DC=Fabrikam,DC=com                   |
| **ADsPath** | LDAP://server/CN=Jeff Smith, CN = Users, DC = fabrikam, DC = com | LDAP://server/<GUID = c0f59dfcf507d311a99e0000f879f7c7> |



 

> [!Note]  
> Le fournisseur Winnt ne prend pas en charge la liaison à l’aide du **GUID** de l’objet et retourne la propriété **GUID** dans un format de chaîne légèrement différent.

 

## <a name="examples"></a>Exemples

L’exemple de code suivant montre comment récupérer des données d’objet à l’aide de méthodes de propriété de l’interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) .


```VB
Dim x As IADs
Dim parent As IADsContainer
Dim cls As IADsClass
Dim op As Variant

On Error GoTo Cleanup

Set x = GetObject("WinNT://Fabrikam/Administrator")
Debug.Print "Object Name: " & x.Name
Debug.Print "Object Path: " & x.ADsPath
Debug.Print "Object Class: " & x.Class
 
' Get more data about the object schema.
Set cls = GetObject(x.Schema)
Debug.Print "Class Name is: " & cls.Name
For Each op In cls.OptionalProperties
    Debug.Print "Optional Property: " & op
Next op

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set x = Nothing
    Set parent = Nothing
    Set cls = Nothing
```



L’exemple de code suivant montre comment récupérer des données d’objet à l’aide de méthodes de propriété de l’interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) .


```VB
<HTML>
<head><title></title></head>

<body>
<%
Dim x 
On Error Resume Next
 
Set x = GetObject("WinNT://Fabrikam/Administrator")
Response.Write "Object Name: " & x.Name & "<br>"
Response.Write "Object Path: " & x.ADsPath & "<br>"
Response.Write "Object Class: " & x.Class & "<br>"
 
' Get more data about the object schema.
Set cls = GetObject(x.Schema)
Response.Write "Class Name is: " & cls.Name & "<br>"
For Each op In cls.OptionalProperties
    Response.Write "Optional Property: " & op & "<br>"
Next op
%>

</body>
</html>
```



L’exemple de code suivant montre comment utiliser les méthodes de propriété de l’interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) .


```C++
#include <stdio.h>
#include <activeds.h>
 
int main(int argc, char* argv[])
{
    IADs *pADs = NULL;
    IADsUser *pADsUser = NULL;
    IADsClass *pCls = NULL;
    CComBSTR sbstr;
 
    HRESULT hr = CoInitialize(NULL);
    if (hr != S_OK) { return 0; }
 
    hr=ADsGetObject(L"WinNT://Fabrikam/Administrator",
                IID_IADsUser,
                (void**) &pADsUser);
    if (hr != S_OK) { goto Cleanup; }
 
    hr = pADsUser->QueryInterface(IID_IADs, (void**) &pADs);
    if( hr !=S_OK) { goto Cleanup;}
 
    pADsUser->Release();
 
    if( S_OK == pADs->get_Name(&sbstr) ) {
        printf("Object Name: %S\n",sbstr);
    }
 
    if( S_OK == pADs->get_ADsPath(&sbstr) ) {
        printf("Object path: %S\n",sbstr);
    }
 
    if( S_OK == pADs->get_Class(&sbstr) ) {
        printf("Object class: %S\n",sbstr);
    }
 
    hr = pADs->get_Schema(&sbstr);
    if ( hr != S_OK) {goto Cleanup;}
 
    hr = ADsGetObject(sbstr,IID_IADsClass, (void**)&pCls);
    if ( hr != S_OK) {goto Cleanup;}
    if( S_OK == pCls->get_Name(&sbstr) ) {
        printf("Class name is %S\n", sbstr);
    }
 
 Cleanup:
    if(pADs)
        pADs->Release();

    if(pIADsUser)
        pADsUser->Release();

    if(IADsClass)
        pADsClass->Release();

    CoUninitialize();

    if(hr==S_OK)
    {
        return 1;
    }
    else
    {
        return 0;
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
| IID<br/>                      | IID \_ IADs est défini en tant que FD8256D0-FD15-11CE-ABC4-02608C9E7553<br/>                 |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IADs**](/windows/desktop/api/Iads/nn-iads-iads)
</dt> <dt>

[**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)
</dt> </dl>

 

