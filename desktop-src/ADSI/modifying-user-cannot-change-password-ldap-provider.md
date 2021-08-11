---
title: La modification de l’utilisateur ne peut pas changer le mot de passe (fournisseur LDAP)
description: La possibilité pour un utilisateur de modifier son propre mot de passe est une autorisation qui peut être accordée ou refusée.
ms.assetid: 9d5c2d6a-9997-4d0c-b896-bf1b578e64ac
ms.tgt_platform: multiple
keywords:
- Modification de l’utilisateur impossible de modifier le mot de passe (fournisseur LDAP) ADSI
- L’utilisateur ne peut pas modifier le mot de passe (fournisseur LDAP) ADSI, modification
- ADSI Provider ADSI, exemples de gestion des utilisateurs, l’utilisateur doit changer de mot de passe à la prochaine ouverture de session, modification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec664f9a79e0de4ff0b75ae31abd8dc1532cd17c0d3d35a934e094da45eb3383
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118179017"
---
# <a name="modifying-user-cannot-change-password-ldap-provider"></a>La modification de l’utilisateur ne peut pas changer le mot de passe (fournisseur LDAP)

La possibilité pour un utilisateur de modifier son propre mot de passe est une autorisation qui peut être accordée ou refusée. Pour refuser cette autorisation, définissez deux ACE dans la liste de contrôle d’accès discrétionnaire (DACL) du descripteur de sécurité de l’objet utilisateur avec le type d’ACE d' **\_ \_ \_ \_ objet accès refusé ADS ACETYPE** . Une entrée de contrôle d’accès refuse l’autorisation à l’utilisateur et une autre entrée de contrôle d’accès refuse l’autorisation au groupe tout le monde. Les deux ACE sont des ACE de refus spécifiques aux objets qui spécifient le GUID de l’autorisation étendue pour la modification des mots de passe. Pour accorder cette autorisation, définissez les mêmes entrées de contrôle d’accès avec le type d’ACE d' **\_ \_ \_ \_ objet accès autorisé ADS ACETYPE** .

La procédure suivante décrit comment modifier ou ajouter des ACE pour cette autorisation.

**Pour modifier ou ajouter les ACE pour cette autorisation**

1.  Lier à l’objet utilisateur.
2.  Obtenez l’objet [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) à partir de la propriété **ntSecurityDescriptor** de l’objet utilisateur.
3.  Obtenez une interface [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist) pour le descripteur de sécurité à partir de la propriété [**IADsSecurityDescriptor. DiscretionaryAcl**](iadssecuritydescriptor-property-methods.md) .
4.  Énumérez les ACE pour l’objet et recherchez les entrées de du mot de passe qui ont le GUID de modification du mot de passe ({AB721A53-1E2F-11D0-9819-00AA0040529B}) pour la propriété [**IADsAccessControlEntry. ObjectType**](iadsaccesscontrolentry-property-methods.md) et « tout le monde » ou « autorité NT \\ autonome » pour la propriété **IADsAccessControlEntry. Trusted** .

    > [!Note]  
    > Les chaînes « tout le monde » et « Self de l’autorité NT \\ » sont localisées en fonction de la langue du premier contrôleur de domaine dans le domaine. Pour cette raison, les chaînes ne doivent pas être utilisées directement. Les noms de comptes doivent être obtenus au moment de l’exécution en appelant la fonction [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) avec le SID pour « tout le monde » (« S-1-1-0 ») et les principaux de sécurité « NT Authority \\ Self » (« s-1-5-10 ») connus. Les exemples de fonctions **GetSidAccountName**, **GetSidAccountName \_ everyone** et **GetSidAccountName \_ Self** C++ illustrés dans lecture de l' [utilisateur ne peuvent pas changer de mot de passe (fournisseur LDAP)](reading-user-cannot-change-password-ldap-provider.md) montrent comment procéder.

     

5.  Modifiez la propriété [**IADsAccessControlEntry. AceType**](iadsaccesscontrolentry-property-methods.md) des ACE qui ont été trouvées pour les **publicités \_ AceType \_ \_ \_ objet accès refusé** si l’utilisateur ne peut pas modifier son mot de passe ou les **publicités AceType l' \_ \_ accès aux \_ \_ objets autorisés** si l’utilisateur peut modifier son mot de passe.
6.  Si l’ACE « tout le monde » est introuvable, créez un nouvel objet [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) qui contient les valeurs de propriété indiquées dans le tableau ci-dessous et ajoutez la nouvelle entrée à la liste de contrôle d’accès avec la méthode [**IADsAccessControlList. AddAce**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-addace) .
7.  Si l’entrée du contrôle d’accès de l’autorité NT \\ est introuvable, créez un objet [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) avec les mêmes valeurs de propriété que celles indiquées dans le tableau ci-dessous, à l’exception de la propriété [**Trusted**](iadsaccesscontrolentry-property-methods.md) contenant le nom de compte « S-1-5-10 » (« AUTORITE NT \\ Self »). Ajoutez l’entrée à la liste de contrôle d’accès avec la méthode [**IADsAccessControlList. AddAce**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-addace) .
8.  Pour mettre à jour la propriété **ntSecurityDescriptor** de l’objet, appelez la méthode [**IADs. put**](/windows/desktop/api/Iads/nf-iads-iads-put) avec le même [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) obtenu à l’étape 2.
9.  Validez les modifications locales sur le serveur à l’aide de la méthode [**IADs. setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) .
10. Si l’une des entrées de contrôle d’accès a été créée, vous devez réorganiser la liste de contrôle d’accès afin que les entrées du contrôle d’accès soient dans le bon ordre. Pour ce faire, appelez la fonction [**GetNamedSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getnamedsecurityinfoa) avec le chemin d’accès LDAP de l’objet, puis la fonction [**SetNamedSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setnamedsecurityinfoa) avec la même liste DACL. Cette réorganisation se produit automatiquement lors de l’ajout des ACE.

Le tableau suivant répertorie les valeurs des propriétés de l’objet [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) .



| Propriété IADsAccessControlEntry                                        | Valeur                                                                                                                                                                 |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AccessMask**](iadsaccesscontrolentry-property-methods.md)          | **\_ \_ \_ accès au contrôle du service d’annuaire AD Right \_**                                                                                                                                   |
| [**AceType**](iadsaccesscontrolentry-property-methods.md)             | **Annonces \_ ACETYPE \_ a \_ refusé l' \_ objet** si l’utilisateur ne peut pas modifier son mot de passe ou son **\_ objet ad ACETYPE \_ Access \_ allowed \_** si l’utilisateur peut modifier son mot de passe. |
| [**AceFlags**](iadsaccesscontrolentry-property-methods.md)            | 0                                                                                                                                                                     |
| [**Indicateurs**](iadsaccesscontrolentry-property-methods.md)               | **\_type d' \_ objet indicateur ADS \_ \_ présent**                                                                                                                                  |
| [**ObjectType**](iadsaccesscontrolentry-property-methods.md)          | « {AB721A53-1E2F-11D0-9819-00AA0040529B} », qui est le GUID de modification du mot de passe sous forme de chaîne.                                                                            |
| [**InheritedObjectType**](iadsaccesscontrolentry-property-methods.md) | Non utilisé                                                                                                                                                              |
| [**Tiers**](iadsaccesscontrolentry-property-methods.md)             | Nom de compte pour le SID « S-1-1-0 » (tout le monde).                                                                                                                            |



 

## <a name="example-code"></a>Exemple de code

L’exemple de code suivant montre comment obtenir une interface pour modifier une liste DACL. L’interface [**IADsObjectOptions**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions) peut être utilisée en définissant l’option DACL des **informations de \_ sécurité \_ \_ ADS** .

> [!Note]  
> Pour utiliser le code documenté dans cet exemple, vous devez être un administrateur. Si vous n’êtes pas administrateur, vous devez ajouter du code qui utilisera une interface qui permettra à un utilisateur de modifier la façon dont le cache côté client est vidé vers le service domaine Active Directory.

 


```C++
//
// Obtain an IADsObjectOptions interface from the object whose
// DACL you wish to modify.
//
long CanReadSetDACL = ADS_SECURITY_INFO_DACL;

CComPtr<IADsObjectOptions> spObjOps;

hr = pads->QueryInterface(IID_IADsObjectOptions, (void**)&spObjOps);

if(SUCCEEDED(hr))

{

//
// Set the option mask you want to change. In this case
// we want to change the objects security information, so we'll
// use the ADS_OPTION_SECURITY_MASK. Since we want to modify the 
// DACL, we'll set the variant to ADS_SEDCURITY_INFO_DACL flag. 
//

    CComVariant svar;
    svar = CanReadSetDACL;
    hr = spObjOps->SetOption(ADS_OPTION_SECURITY_MASK, svar); 

}
//
// The smart pointer declared for pObjOptions can be released
// or it will be destroyed and released once the pointer goes 
// out of scope.
//

```



L’exemple de code suivant montre comment modifier l’autorisation de l’utilisateur ne peut pas modifier le mot de passe à l’aide du fournisseur LDAP. Cet exemple de code utilise la fonction de l’utilitaire **GetObjectACE** définie ci-dessus.

Cet exemple utilise les exemples de fonctions **GetSidAccountName \_ everyone** et **GetSidAccountName \_ Self** C++ illustrés dans [Read user ne peut pas changer de mot de passe (fournisseur LDAP)](reading-user-cannot-change-password-ldap-provider.md).


```C++
#include <aclapi.h>

#define CHANGE_PASSWORD_GUID_W L"{AB721A53-1E2F-11D0-9819-00AA0040529B}"

/***************************************************************************

    CreateACE()

    Creates an ACE and returns the IDispatch pointer for the ACE. This 
    pointer can be passed directly to IADsAccessControlList::AddAce.

    bstrTrustee - Contains the Trustee for the ACE.

    bstrObjectType - Contains the ObjectType for the ACE.

    lAccessMask - Contains the AccessMask for the ACE.

    lACEType - Contains the ACEType for the ACE.

    lACEFlags - Contains the ACEFlags for the ACE.

    lFlags - Contains the Flags for the ACE.

***************************************************************************/

IDispatch* CreateACE(BSTR bstrTrustee, 
                     BSTR bstrObjectType, 
                     long lAccessMask, 
                     long lACEType, 
                     long lACEFlags, 
                     long lFlags)
{
    HRESULT hr;
    IDispatch *pDisp = NULL;
    IADsAccessControlEntry *pACE = NULL;

    hr = CoCreateInstance(CLSID_AccessControlEntry,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IADsAccessControlEntry,
                          (void**)&pACE);
    if(SUCCEEDED(hr)) 
    {
        hr = pACE->put_Trustee(bstrTrustee); 
        hr = pACE->put_ObjectType(bstrObjectType);
        hr = pACE->put_AccessMask(lAccessMask); 
        hr = pACE->put_AceType(lACEType);
        hr = pACE->put_AceFlags(lACEFlags);
        hr = pACE->put_Flags(lFlags);

        hr = pACE->QueryInterface(IID_IDispatch, (LPVOID*)&pDisp);

        pACE->Release();
    }

    return pDisp;
}

/***************************************************************************

    ReorderACEs()

    Causes the ACEs of an object DACL to be reordered properly. The ACEs are 
    automatically put in the proper order when they are added to the DACL. 
    On older systems however, this does not occur automatically, so this 
    function is necessary so the deny ACEs are ordered in the list before 
    the allow ACEs.

    pwszDN - A null-terminated Unicode string that contains the LDAP 
    ADsPath of the DS object to reorder the DACL for.

***************************************************************************/

HRESULT ReorderACEs(LPCWSTR pwszDN)
{
    HRESULT hr = E_FAIL;
    DWORD dwResult;
    ACL *pdacl;
    PSECURITY_DESCRIPTOR psd;
    
    dwResult = GetNamedSecurityInfoW(   (LPWSTR)pwszDN,
                                        SE_DS_OBJECT_ALL,
                                        DACL_SECURITY_INFORMATION,
                                        NULL,
                                        NULL,
                                        &pdacl,
                                        NULL,
                                        &psd);

    if(ERROR_SUCCESS == dwResult)
    {
        dwResult = SetNamedSecurityInfoW(   (LPWSTR)pwszDN,
                                            SE_DS_OBJECT_ALL,
                                            DACL_SECURITY_INFORMATION,
                                            NULL,
                                            NULL,
                                            pdacl,
                                            NULL);

        LocalFree(psd);
        
        if(ERROR_SUCCESS == dwResult)
        {
            hr = S_OK;
        }
    }
    
    return hr;
}

/***************************************************************************

    SetUserCannotChangePassword()

    Sets the "User Cannot Change Password" permission using the LDAP provider 
    to the specified setting. To do this, find the existing 
    ACEs and modify the AceType. If the ACE is not found, a new one of the 
    proper type is created and added. The ACEs should always be present, but 
    it is possible that the default DACL excludes them, so this situation 
    will be handled correctly.

    pwszUserDN - A null-terminated Unicode string that contains the LDAP 
    ADsPath of the user object to modify.

    pwszUsername - A null-terminated Unicode string that contains the user 
    name to use for authorization. If this is NULL, the credentials of the 
    current user are used.

    pwszPassword - A null-terminated Unicode string that contains the 
    password to use for authorization. This is ignored if pwszUsername is 
    NULL.

    fCannotChangePassword - Contains the new setting for the privilege. 
    Contains nonzero if the user cannot change their password or zero if 
    the can change their password.

***************************************************************************/

HRESULT SetUserCannotChangePassword(LPCWSTR pwszUserDN, 
                                    LPCWSTR pwszUsername, 
                                    LPCWSTR pwszPassword,
                                    BOOL fCannotChangePassword)
{
    HRESULT hr;

    CComBSTR sbstrEveryone;
    hr = GetSidAccountName_Everyone(&sbstrEveryone);
    if(FAILED(hr))
    {
        return hr;
    }

    CComBSTR sbstrSelf;
    hr = GetSidAccountName_Self(&sbstrSelf);
    if(FAILED(hr))
    {
        return hr;
    }

    if(NULL == pwszUserDN)
    {
        return E_INVALIDARG;
    }
    
    IADs *pads;

    hr = ADsOpenObject( pwszUserDN,
                        pwszUsername,
                        pwszPassword,
                        ADS_SECURE_AUTHENTICATION,
                        IID_IADs, 
                        (LPVOID*)&pads);

    if(SUCCEEDED(hr))
    {
        CComBSTR sbstrSecDesc = "ntSecurityDescriptor";
        CComVariant svar;
        
        hr = pads->Get(sbstrSecDesc, &svar);
        if(SUCCEEDED(hr))
        {
            IADsSecurityDescriptor *psd;

            hr = svar.pdispVal->QueryInterface(IID_IADsSecurityDescriptor, (LPVOID*)&psd);
            if(SUCCEEDED(hr))
            {
                IDispatch *pDisp;

                hr = psd->get_DiscretionaryAcl(&pDisp);
                if(SUCCEEDED(hr))
                {
                    IADsAccessControlList *pACL;

                    hr = pDisp->QueryInterface(IID_IADsAccessControlList, (void**)&pACL);
                    if(SUCCEEDED(hr)) 
                    {
                        BOOL fMustReorder = FALSE;
                        /*
                        Get the existing ACE for the change password permission 
                        for Everyone. If it exists, just modify the existing 
                        ACE. If it does not exist, create a new one and add it 
                        to the ACL.
                        */
                        IADsAccessControlEntry *pACEEveryone = NULL;
                        hr = GetObjectACE(pACL, CHANGE_PASSWORD_GUID_W, sbstrEveryone, &pACEEveryone);
                        if(pACEEveryone)
                        {
                            hr = pACEEveryone->put_AceType(fCannotChangePassword ? 
                                ADS_ACETYPE_ACCESS_DENIED_OBJECT : 
                                ADS_ACETYPE_ACCESS_ALLOWED_OBJECT);

                            pACEEveryone->Release();
                        }
                        else
                        {
                            IDispatch *pDispEveryone = NULL;
                            
                            pDispEveryone = CreateACE(sbstrEveryone, 
                                CComBSTR(CHANGE_PASSWORD_GUID_W),
                                ADS_RIGHT_DS_CONTROL_ACCESS, 
                                fCannotChangePassword ? 
                                    ADS_ACETYPE_ACCESS_DENIED_OBJECT : 
                                    ADS_ACETYPE_ACCESS_ALLOWED_OBJECT, 
                                0,
                                ADS_FLAG_OBJECT_TYPE_PRESENT);
                            
                            if(pDispEveryone)
                            {
                                //add the new ACE for everyone
                                hr = pACL->AddAce(pDispEveryone);

                                pDispEveryone->Release();

                                fMustReorder = TRUE;
                            }                            
                        }
                        
                        /*
                        Get the existing ACE for the change password permission 
                        for Self. If it exists, just modify the existing 
                        ACE. If it does not exist, create a new one and add it 
                        to the ACL.
                        */
                        IADsAccessControlEntry *pACESelf = NULL;
                        hr = GetObjectACE(pACL, CHANGE_PASSWORD_GUID_W, sbstrSelf, &pACESelf);
                        if(pACESelf)
                        {
                            hr = pACESelf->put_AceType(fCannotChangePassword ? 
                                ADS_ACETYPE_ACCESS_DENIED_OBJECT : 
                                ADS_ACETYPE_ACCESS_ALLOWED_OBJECT);
                        
                            pACESelf->Release();
                        }
                        else
                        {
                            IDispatch *pDispSelf = NULL;
                            
                            pDispSelf = CreateACE(sbstrSelf, 
                                CComBSTR(CHANGE_PASSWORD_GUID_W),
                                ADS_RIGHT_DS_CONTROL_ACCESS, 
                                fCannotChangePassword ? 
                                    ADS_ACETYPE_ACCESS_DENIED_OBJECT : 
                                    ADS_ACETYPE_ACCESS_ALLOWED_OBJECT, 
                                0,
                                ADS_FLAG_OBJECT_TYPE_PRESENT);

                            if(pDispSelf)
                            {
                                //add the new ACE for self
                                hr = pACL->AddAce(pDispSelf);

                                pDispSelf->Release();

                                fMustReorder = TRUE;
                            }                            
                        }

                        //update the security descriptor property
                        hr = pads->Put(sbstrSecDesc, svar);
                        
                        //commit the changes
                        hr = pads->SetInfo();

                        if(fMustReorder)
                        {
                            ReorderACEs(pwszUserDN);
                        }

                        pACL->Release();
                    }

                    pDisp->Release();
                }
                
                psd->Release();
            }
        }
    }

    return hr;
}
```



L’exemple de code suivant montre comment modifier l’autorisation de l’utilisateur ne peut pas modifier le mot de passe à l’aide du fournisseur LDAP.

> [!Note]  
> L’exemple ci-dessous fonctionne uniquement sur les domaines dont la langue principale est l’anglais, car les chaînes « tout le monde » et « autorisations NT » \\ sont localisées en fonction de la langue du premier contrôleur de domaine dans le domaine. il n’existe aucun moyen de Visual Basic pour obtenir les noms de compte d’une entité de sécurité connue sans appeler la fonction [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) . si vous utilisez Visual Basic, il est recommandé d’utiliser le fournisseur winnt pour modifier l’autorisation l’utilisateur ne peut pas modifier le mot de passe, comme indiqué dans modification de l' [utilisateur ne peut pas changer de mot de passe (fournisseur winnt)](modifying-user-cannot-change-password-winnt-provider.md).

 


```VB
'******************************************************************************
'
'    SetUserCannotChangePassword
'
'    Sets the "User Cannot Change Password" permission using the LDAP provider
'    to the specified setting. This is accomplished by finding the existing
'    ACEs and modifying the AceType. The ACEs should always be present, but
'    it is possible that the default DACL excludes them. This function will not
'    work correctly if both ACEs are not present.
'
'    strUserDN - A string that contains the LDAP ADsPath of the user object to
'    modify.
'
'    strUsername - A string that contains the user name to use for
'    authorization. If this is an empty string, the credentials of the current
'    user are used.
'
'    strPassword - A string that contains the password to use for authorization.
'    This is ignored if strUsername is empty.
'
'    fCannotChangePassword - Contains the new setting for the privilege.
'    Contains True if the user cannot change their password or False if
'    the can change their password.
'
'******************************************************************************
Sub SetUserCannotChangePassword(strUserDN As String, strUsername As String, strPassword As String, fUserCannotChangePassword As Boolean)
    Dim oUser As IADs
    Dim oSecDesc As IADsSecurityDescriptor
    Dim oACL As IADsAccessControlList
    Dim oACE As IADsAccessControlEntry
    
    fEveryone = False
    fSelf = False
    
    If "" <> strUsername Then
        Dim dso As IADsOpenDSObject
        
        ' Bind to the group with the specified user name and password.
        Set dso = GetObject("LDAP:")
        Set oUser = dso.OpenDSObject(strUserDN, strUsername, strPassword, 1)
    Else
        ' Bind to the group with the current credentials.
        Set oUser = GetObject(strUserDN)
    End If
    
    Set oSecDesc = oUser.Get("ntSecurityDescriptor")
    Set oACL = oSecDesc.DiscretionaryAcl
    
    ' Modify the existing entries.
    For Each oACE In oACL
        If UCase(oACE.ObjectType) = UCase(CHANGE_PASSWORD_GUID) Then
            If oACE.Trustee = "Everyone" Then
                ' Modify the ace type of the entry.
                If fUserCannotChangePassword Then
                    oACE.AceType = ADS_ACETYPE_ACCESS_DENIED_OBJECT
                Else
                    oACE.AceType = ADS_ACETYPE_ACCESS_ALLOWED_OBJECT
                End If
            End If
        
            If oACE.Trustee = "NT AUTHORITY\SELF" Then
                ' Modify the ace type of the entry.
                If fUserCannotChangePassword Then
                    oACE.AceType = ADS_ACETYPE_ACCESS_DENIED_OBJECT
                Else
                    oACE.AceType = ADS_ACETYPE_ACCESS_ALLOWED_OBJECT
                End If
            End If
        End If
    Next
    
    ' Update the ntSecurityDescriptor property.
    oUser.Put "ntSecurityDescriptor", oSecDesc
    
    ' Commit the changes to the server.
    oUser.SetInfo
End Sub
```



 

 