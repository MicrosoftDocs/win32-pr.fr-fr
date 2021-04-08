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
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2021
ms.locfileid: "104043072"
---
# <a name="user-creation-with-the-adsi-ldap-provider"></a><span data-ttu-id="9a8e9-104">Création de l’utilisateur avec le fournisseur LDAP ADSI</span><span class="sxs-lookup"><span data-stu-id="9a8e9-104">User Creation with the ADSI LDAP Provider</span></span>

<span data-ttu-id="9a8e9-105">Avec le fournisseur LDAP ADSI, vous pouvez uniquement créer un compte d’utilisateur global.</span><span class="sxs-lookup"><span data-stu-id="9a8e9-105">With the ADSI LDAP provider, you can only create a global user account.</span></span> <span data-ttu-id="9a8e9-106">Les comptes locaux résident dans la base de données SAM et doivent être créés à l’aide du fournisseur Winnt.</span><span class="sxs-lookup"><span data-stu-id="9a8e9-106">Local accounts reside in the SAM database and must be created using the WinNT provider.</span></span> <span data-ttu-id="9a8e9-107">Pour plus d’informations sur la création d’un objet utilisateur avec le fournisseur WinNT, consultez [objet utilisateur Winnt](winnt-user-object.md).</span><span class="sxs-lookup"><span data-stu-id="9a8e9-107">For more information about creating a user object with the WinNT provider, see [WinNT User Object](winnt-user-object.md).</span></span>

<span data-ttu-id="9a8e9-108">**Pour créer un objet utilisateur**</span><span class="sxs-lookup"><span data-stu-id="9a8e9-108">**To create a user object**</span></span>

1.  <span data-ttu-id="9a8e9-109">Effectuez une liaison au conteneur où se trouve l’objet utilisateur et obtenez l’interface [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) ou [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) pour le conteneur.</span><span class="sxs-lookup"><span data-stu-id="9a8e9-109">Bind to the container where the user object will reside and obtain either the [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) or [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) interface for the container.</span></span>
2.  <span data-ttu-id="9a8e9-110">Utilisez la méthode [**IADsContainer. Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) ou [**IDirectoryObject :: CreateDSObject**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-createdsobject) pour créer l’objet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9a8e9-110">Use the [**IADsContainer.Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) or [**IDirectoryObject::CreateDSObject**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-createdsobject) method to create the user object.</span></span>
3.  <span data-ttu-id="9a8e9-111">Les attributs minimaux requis pour créer un objet utilisateur dépendent du service d’annuaire utilisé.</span><span class="sxs-lookup"><span data-stu-id="9a8e9-111">The minimum attributes required to create a user object will depend on the directory service used.</span></span> <span data-ttu-id="9a8e9-112">Pour plus d’informations sur la création d’un utilisateur Active Directory, consultez [création d’un utilisateur](/windows/desktop/AD/creating-a-user).</span><span class="sxs-lookup"><span data-stu-id="9a8e9-112">For more information about creating an Active Directory user, see [Creating a User](/windows/desktop/AD/creating-a-user).</span></span>
4.  <span data-ttu-id="9a8e9-113">Si l’interface [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) est utilisée, le nouvel objet n’est pas réellement créé tant que la méthode [**IADs. setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) n’est pas appelée.</span><span class="sxs-lookup"><span data-stu-id="9a8e9-113">If the [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) interface is used, the new object is not actually created until the [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method is called.</span></span>

    <span data-ttu-id="9a8e9-114">Si l’interface [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) est utilisée, le nouvel objet est créé lorsque la méthode [**CreateDSObject**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-createdsobject) est appelée.</span><span class="sxs-lookup"><span data-stu-id="9a8e9-114">If the [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) interface is used, the new object is created when the [**CreateDSObject**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-createdsobject) method is called.</span></span> <span data-ttu-id="9a8e9-115">Les attributs minimaux, y compris [**objectClass**](/windows/desktop/ADSchema/a-objectclass), doivent être spécifiés dans le tableau d' [**\_ \_ informations attr ADS**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) transmis à la méthode **CreateDSObject** .</span><span class="sxs-lookup"><span data-stu-id="9a8e9-115">The minimum attributes, including the [**objectClass**](/windows/desktop/ADSchema/a-objectclass), must be specified in the [**ADS\_ATTR\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) array passed to the **CreateDSObject** method.</span></span>

## <a name="example-1"></a><span data-ttu-id="9a8e9-116">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="9a8e9-116">Example 1</span></span>

<span data-ttu-id="9a8e9-117">L’exemple de code suivant crée un compte d’utilisateur avec les attributs par défaut.</span><span class="sxs-lookup"><span data-stu-id="9a8e9-117">The following code example creates a user account with the default attributes.</span></span>


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



## <a name="example-2"></a><span data-ttu-id="9a8e9-118">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="9a8e9-118">Example 2</span></span>

<span data-ttu-id="9a8e9-119">L’exemple de code suivant crée un compte d’utilisateur avec les attributs par défaut.</span><span class="sxs-lookup"><span data-stu-id="9a8e9-119">The following code example creates a user account with the default attributes.</span></span> <span data-ttu-id="9a8e9-120">Par souci de concision, la vérification des erreurs est omise.</span><span class="sxs-lookup"><span data-stu-id="9a8e9-120">For brevity, error checking is omitted.</span></span>


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



 

 