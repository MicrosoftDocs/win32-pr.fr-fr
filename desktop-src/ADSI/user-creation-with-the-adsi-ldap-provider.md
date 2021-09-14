---
title: Création de l’utilisateur avec le fournisseur LDAP ADSI
description: Avec le fournisseur LDAP ADSI, vous pouvez uniquement créer un compte d’utilisateur global.
ms.assetid: f99f85a8-9ced-4006-b95b-bd5671ba4c60
ms.tgt_platform: multiple
keywords:
- ADSI fournisseur LDAP, objet utilisateur, création d’utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 843bb5bc9d0696c3af7c5f06ce8c76123ae93c3a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012361"
---
# <a name="user-creation-with-the-adsi-ldap-provider"></a>Création de l’utilisateur avec le fournisseur LDAP ADSI

Avec le fournisseur LDAP ADSI, vous pouvez uniquement créer un compte d’utilisateur global. Les comptes locaux résident dans la base de données SAM et doivent être créés à l’aide du fournisseur Winnt. Pour plus d’informations sur la création d’un objet utilisateur avec le fournisseur WinNT, consultez [objet utilisateur Winnt](winnt-user-object.md).

**Pour créer un objet utilisateur**

1.  Effectuez une liaison au conteneur où se trouve l’objet utilisateur et obtenez l’interface [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) ou [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) pour le conteneur.
2.  Utilisez la méthode [**IADsContainer. Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) ou [**IDirectoryObject :: CreateDSObject**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-createdsobject) pour créer l’objet utilisateur.
3.  Les attributs minimaux requis pour créer un objet utilisateur dépendent du service d’annuaire utilisé. Pour plus d’informations sur la création d’un utilisateur Active Directory, consultez [création d’un utilisateur](/windows/desktop/AD/creating-a-user).
4.  Si l’interface [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) est utilisée, le nouvel objet n’est pas réellement créé tant que la méthode [**IADs. setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) n’est pas appelée.

    Si l’interface [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) est utilisée, le nouvel objet est créé lorsque la méthode [**CreateDSObject**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-createdsobject) est appelée. Les attributs minimaux, y compris [**objectClass**](/windows/desktop/ADSchema/a-objectclass), doivent être spécifiés dans le tableau d' [**\_ \_ informations attr ADS**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) transmis à la méthode **CreateDSObject** .

## <a name="example-1"></a>Exemple 1

L’exemple de code suivant crée un compte d’utilisateur avec les attributs par défaut.


```VB
Dim ou As IADs
Dim usr as IADsUser

On Error GoTo Cleanup

Set ou = GetObject("LDAP://OU=Finance,DC=Fabrikam,DC=COM")
Set usr = ou.Create("user", "cn=Jeff Smith")
usr.Put "samAccountName", "jeffsmith"
usr.SetInfo

Cleanup:
   If (Err.Number <> 0) Then
      MsgBox ("An error has occurred. " &  Err.Number)
   End If
   Set ou = Nothing
   Set usr = Nothing
```



## <a name="example-2"></a>Exemple 2

L’exemple de code suivant crée un compte d’utilisateur avec les attributs par défaut. Par souci de concision, la vérification des erreurs est omise.


```C++
#include <activeds.h>

int main()
{
   HRESULT hr = CoInitialize(NULL);

   IADsContainer *pCont;
   IADsUser *pUser;

   LPWSTR adsPath = L"LDAP://serv1/CN=Users,dc=Fabrikam,dc=com";
   LPWSTR usrPass = NULL;
   LPWSTR usrName = NULL;

   // Add code to securely get the user name and password or leave
   // as NULL to use the current security context.

   hr = ADsOpenObject(adsPath, 
                      usrName,
                      usrPass,
                      ADS_SECURE_AUTHENTICATION,
                      IID_IADsContainer,
                      (void**)&pCont);

   IDispatch *pDisp;
   hr = pCont->Create(CComBSTR("user"), CComBSTR("cn=Jeff Smith"), &pDisp);
   pCont->Release();

   hr = pDisp->QueryInterface(IID_IADsUser,(void**)&pUser);
   pDisp->Release();

   VARIANT var;
   VariantInit(&var);
   V_BSTR(&var) = L"jeffsmith";
   V_VT(&var)=VT_BSTR;
   hr = pUser->Put(CComBSTR("samAccountName"), var);

   hr = pUser->SetInfo();

   VariantClear(&var);
   pUser->Release();

   CoUninitialize();

   return 0;
}
```



 

 