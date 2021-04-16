---
title: La lecture de l’utilisateur ne peut pas changer le mot de passe (fournisseur LDAP)
description: La capacité d’un utilisateur à modifier son mot de passe est une autorisation qui peut être accordée ou refusée.
ms.assetid: d0d95d20-dcdb-453a-9d15-c386217927c8
ms.tgt_platform: multiple
keywords:
- La lecture de l’utilisateur ne peut pas changer le mot de passe (fournisseur LDAP)
- L’utilisateur ne peut pas modifier le mot de passe (fournisseur LDAP), en lisant
- ADSI Provider ADSI, gestion des utilisateurs, exemples, l’utilisateur doit modifier le mot de passe à la prochaine ouverture de session, en lisant
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ea818c8b01fbbac6b80037de13b25a82a07944
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104508125"
---
# <a name="reading-user-cannot-change-password-ldap-provider"></a><span data-ttu-id="b0436-106">La lecture de l’utilisateur ne peut pas changer le mot de passe (fournisseur LDAP)</span><span class="sxs-lookup"><span data-stu-id="b0436-106">Reading User Cannot Change Password (LDAP Provider)</span></span>

<span data-ttu-id="b0436-107">La capacité d’un utilisateur à modifier son mot de passe est une autorisation qui peut être accordée ou refusée.</span><span class="sxs-lookup"><span data-stu-id="b0436-107">The ability of a user to change their password is a permission that can be granted or denied.</span></span>

<span data-ttu-id="b0436-108">**Pour déterminer si l’autorisation Modifier le mot de passe est accordée ou refusée**</span><span class="sxs-lookup"><span data-stu-id="b0436-108">**To determine if the change password permission is granted or denied**</span></span>

1.  <span data-ttu-id="b0436-109">Lier à l’objet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b0436-109">Bind to the user object.</span></span>
2.  <span data-ttu-id="b0436-110">Obtenez l’objet [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) à partir de la propriété **ntSecurityDescriptor** de l’objet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b0436-110">Obtain the [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) object from the **ntSecurityDescriptor** property of the user object.</span></span>
3.  <span data-ttu-id="b0436-111">Obtenez une interface [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist) pour le descripteur de sécurité à partir de la propriété [**IADsSecurityDescriptor. DiscretionaryAcl**](iadssecuritydescriptor-property-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="b0436-111">Obtain an [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist) interface for the security descriptor from the [**IADsSecurityDescriptor.DiscretionaryAcl**](iadssecuritydescriptor-property-methods.md) property.</span></span>
4.  <span data-ttu-id="b0436-112">Énumérez les entrées de contrôle d’accès (ACE) pour l’objet et recherchez les ACE qui ont le GUID de modification du mot de passe ({AB721A53-1E2F-11D0-9819-00AA0040529B}) pour la propriété [**IADsAccessControlEntry. ObjectType**](iadsaccesscontrolentry-property-methods.md) et les principaux de sécurité « tout le monde » ou « \\ autonome » de l’autorité NT pour la propriété **IADsAccessControlEntry. Trusted** .</span><span class="sxs-lookup"><span data-stu-id="b0436-112">Enumerate the access control entries (ACE) for the object and search for the ACEs that have the change password GUID ({AB721A53-1E2F-11D0-9819-00AA0040529B}) for the [**IADsAccessControlEntry.ObjectType**](iadsaccesscontrolentry-property-methods.md) property and "Everyone" or "NT AUTHORITY\\SELF" well-known security principals for the **IADsAccessControlEntry.Trustee** property.</span></span>
    > [!Note]  
    > <span data-ttu-id="b0436-113">Les chaînes « tout le monde » et « Self de l’autorité NT \\ » sont localisées en fonction de la langue du premier contrôleur de domaine dans le domaine.</span><span class="sxs-lookup"><span data-stu-id="b0436-113">The "Everyone" and "NT AUTHORITY\\SELF" strings are localized based on the language of the first domain controller in the domain.</span></span> <span data-ttu-id="b0436-114">Par conséquent, les chaînes ne doivent pas être utilisées directement.</span><span class="sxs-lookup"><span data-stu-id="b0436-114">Therefore, the strings should not be used directly.</span></span> <span data-ttu-id="b0436-115">Les noms de comptes doivent être obtenus au moment de l’exécution en appelant la fonction [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) avec le SID pour les principaux de sécurité « tout le monde » (« s-1-1-0 ») et « autorité NT \\ auto » (« s-1-5-10 »).</span><span class="sxs-lookup"><span data-stu-id="b0436-115">The account names should be obtained at run time by calling the [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) function with the SID for the "Everyone" ("S-1-1-0") and "NT AUTHORITY\\SELF" ("S-1-5-10") well-known security principals.</span></span> <span data-ttu-id="b0436-116">Les exemples de code C++ **GetSidAccountName**, **GetSidAccountName \_ everyone** et **GetSidAccountName \_ Self** code montrent comment procéder.</span><span class="sxs-lookup"><span data-stu-id="b0436-116">The following C++ **GetSidAccountName**, **GetSidAccountName\_Everyone**, and **GetSidAccountName\_Self** code examples show how to do this.</span></span>

     

5.  <span data-ttu-id="b0436-117">Si les ACE « tout le monde » et « toutes les autorités NT » \\ ont la valeur **\_ objet ad ACETYPE \_ accès \_ refusé \_** pour la propriété [**IADsAccessControlEntry. ACETYPE**](iadsaccesscontrolentry-property-methods.md) , l’autorisation est refusée.</span><span class="sxs-lookup"><span data-stu-id="b0436-117">If both the "Everyone" and "NT AUTHORITY\\SELF" ACEs have the **ADS\_ACETYPE\_ACCESS\_DENIED\_OBJECT** value for the [**IADsAccessControlEntry.AceType**](iadsaccesscontrolentry-property-methods.md) property, then the permission is denied.</span></span>

## <a name="example-code"></a><span data-ttu-id="b0436-118">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="b0436-118">Example Code</span></span>

<span data-ttu-id="b0436-119">L’exemple de code suivant montre comment déterminer si l’utilisateur ne peut pas modifier l’autorisation de mot de passe à l’aide du fournisseur LDAP.</span><span class="sxs-lookup"><span data-stu-id="b0436-119">The following code example shows how to determine if the User Cannot Change Password Permission using the LDAP provider.</span></span>


```C++
/***************************************************************************

    GetSidAccountName()

    Retrieves the account name for the specified SID.

    pSid - Pointer to the SID that the account name should be retrieved for.

    pbstrAccountName - Pointer to a BSTR that receives the account name. The 
    caller must free this with SysFreeString when it is no longer required.

***************************************************************************/

HRESULT GetSidAccountName(PSID pSid, BSTR *pbstrAccountName)
{
    if(!pbstrAccountName)
    {
        return E_INVALIDARG;
    }
    
    HRESULT hr = E_FAIL;
    BOOL fReturn;

    WCHAR wszAccountName[MAX_PATH];
    DWORD dwAccountName;
    WCHAR wszDomainName[MAX_PATH];
    DWORD dwDomainName;
    SID_NAME_USE SidNameUse;
    DWORD dwSidSize;

    dwAccountName = MAX_PATH;
    dwDomainName = MAX_PATH;
    dwSidSize = SECURITY_MAX_SID_SIZE;

    /*
    Get the account name for the specified SID.
    */
    fReturn = LookupAccountSidW(
        NULL, 
        pSid, 
        wszAccountName, 
        &dwAccountName, 
        wszDomainName, 
        &dwDomainName, 
        &SidNameUse);
    if(fReturn)
    {
        CComBSTR sbstrReturn;

        if(lstrlenW(wszDomainName) > 0)
        {
            sbstrReturn = wszDomainName;
            sbstrReturn += "\\";
            sbstrReturn += wszAccountName;
        }
        else
        {
            sbstrReturn = wszAccountName;
        }

        *pbstrAccountName = sbstrReturn.Detach();
        hr = S_OK;
    }

    return hr;
}

/***************************************************************************

    GetSidAccountName_Everyone()

    Retrieves the local account name for the "World", also known as 
    "Everyone", account.

    pbstrAccountName - Pointer to a BSTR that receives the account name. The 
    caller must free this with SysFreeString when it is no longer required.

***************************************************************************/

HRESULT GetSidAccountName_Everyone(BSTR *pbstrAccountName)
{
    if(!pbstrAccountName)
    {
        return E_INVALIDARG;
    }
    
    HRESULT hr = E_FAIL;
    BOOL fReturn;
    PSID psidAlloc;

    // Create the SID for "Everyone".
    SID_IDENTIFIER_AUTHORITY SidAuth = SECURITY_WORLD_SID_AUTHORITY;
    fReturn = AllocateAndInitializeSid(
        &SidAuth, 
        1, 
        SECURITY_WORLD_RID, 
        0, 0, 0, 0, 0, 0, 0, 
        &psidAlloc);
    if(fReturn)
    {
        hr = GetSidAccountName(psidAlloc, pbstrAccountName);

        LocalFree(psidAlloc);
    }

    return hr;
}

/***************************************************************************

    GetSidAccountName_Self()

    Retrieves the local account name for the "NT AUTHORITY\SELF" account.

    pbstrAccountName - Pointer to a BSTR that receives the account name. The 
    caller must free this with SysFreeString when it is no longer required.

***************************************************************************/

HRESULT GetSidAccountName_Self(BSTR *pbstrAccountName)
{
    HRESULT hr = E_FAIL;
    BOOL fReturn;
    PSID psidAlloc;

    // Create the SID for "Everyone".
    SID_IDENTIFIER_AUTHORITY SidAuth = SECURITY_NT_AUTHORITY;
    fReturn = AllocateAndInitializeSid(
        &SidAuth, 
        1, 
        SECURITY_PRINCIPAL_SELF_RID, 
        0, 0, 0, 0, 0, 0, 0, 
        &psidAlloc);
    if(fReturn)
    {
        hr = GetSidAccountName(psidAlloc, pbstrAccountName);

        LocalFree(psidAlloc);
    }

    return hr;
}

#define CHANGE_PASSWORD_GUID_W L"{AB721A53-1E2F-11D0-9819-00AA0040529B}"

/***************************************************************************

    GetObjectACE()

    Retrieves the IADsAccessControlEntry for the ACE that matches the 
    specified object type and trustee in the specified IADsAccessControlList. 
    Returns a value other than S_OK if the ACE is not found.

    pACL - Pointer to an IADsAccessControlList object that will be searched.

    pwszObject - Pointer to a null-terminated Unicode string that contains 
    the object type to find.

    pwszTrustee - Pointer to a null-terminated Unicode string that contains 
    the trustee to find.

    ppACE - Pointer to an IADsAccessControlEntry pointer that receives the 
    ACE if successful. This receives NULL if not successful.

***************************************************************************/

HRESULT GetObjectACE(IADsAccessControlList* pACL, 
                     LPCWSTR pwszObject, 
                     LPCWSTR pwszTrustee, 
                     IADsAccessControlEntry** ppACE)
{
    if(NULL == pACL || NULL == pwszObject)
    {
        return E_INVALIDARG;
    }

    *ppACE = NULL;
                        
    HRESULT hr;
    IUnknown *pUnk;
    hr = pACL->get__NewEnum(&pUnk);
    if(FAILED(hr))
    {
        return hr;
    }

    IEnumVARIANT *pEnum;

    hr = pUnk->QueryInterface(IID_IEnumVARIANT, (LPVOID*)&pEnum);
    if(SUCCEEDED(hr)) 
    {
        ULONG ulFetched;
        BOOL fEveryone = FALSE;
        BOOL fSelf = FALSE;
        CComVariant svarACE;

        for(hr = pEnum->Next(1, &svarACE, &ulFetched); 
            S_OK == hr && 1 == ulFetched; 
            hr = pEnum->Next(1, &svarACE, &ulFetched))
        {
            if(VT_DISPATCH == svarACE.vt)
            {
                IADsAccessControlEntry *pACE;
                
                hr = svarACE.pdispVal->QueryInterface(IID_IADsAccessControlEntry, (void**)&pACE);
                if(SUCCEEDED(hr))
                {
                    CComBSTR sbstrObjectType;

                    hr = pACE->get_ObjectType(&sbstrObjectType);
                    if(SUCCEEDED(hr))
                    {
                        if(0 == lstrcmpiW(pwszObject, sbstrObjectType))
                        {
                            CComBSTR sbstrTrustee;

                            hr = pACE->get_Trustee(&sbstrTrustee);
                            if(SUCCEEDED(hr) && (0 == lstrcmpiW(sbstrTrustee, pwszTrustee)))
                            {
                                *ppACE = pACE;
                                break;
                            }
                        }
                    }

                    pACE->Release();
                }
            }
        }

        pEnum->Release();
    }

    return hr;
}

/***************************************************************************

    UserCannotChangePassword()

    Retrieves the "User Cannot Change Password" privilege using the LDAP 
    provider. This is determined by the presence and value of the change 
    password GUID ACE for the Everyone and Self trustees. The default result 
    of this function is that the user can change their password unless the 
    two ACEs specifically deny the privilege.

    pwszUserDN - A null-terminated Unicode string that contains the LDAP 
    ADsPath of the user object to verify.

    pwszUsername - A null-terminated Unicode string that contains the user 
    name to use for authorization. If this is NULL, the credentials of the 
    current user are used.

    pwszPassword - A null-terminated Unicode string that contains the 
    password to use for authorization. This is ignored if pwszUsername is 
    NULL.

    pfCannotChangePassword - Receives the setting for the privilege. 
    Receives nonzero if the user cannot change their password or zero if 
    the can change their password.

***************************************************************************/

HRESULT UserCannotChangePassword(LPCWSTR pwszUserDN, 
                                 LPCWSTR pwszUsername, 
                                 LPCWSTR pwszPassword, 
                                 BOOL *pfCannotChangePassword)
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
    *pfCannotChangePassword = FALSE;

    hr = ADsOpenObject( pwszUserDN,
                        pwszUsername,
                        pwszPassword,
                        ADS_SECURE_AUTHENTICATION,
                        IID_IADs, 
                        (LPVOID*)&pads);

    if(SUCCEEDED(hr))
    {
        CComVariant svar;
        
        hr = pads->Get(CComBSTR("ntSecurityDescriptor"), &svar);
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
                        BOOL fEveryone = FALSE;
                        BOOL fSelf = FALSE;
                        IADsAccessControlEntry *pACEEveryone = NULL;
                        IADsAccessControlEntry *pACESelf = NULL;

                        // Get the ACE for everyone.
                        hr = GetObjectACE(pACL, CHANGE_PASSWORD_GUID_W, sbstrEveryone, &pACEEveryone);
                        
                        // Get the ACE for self.
                        hr = GetObjectACE(pACL, CHANGE_PASSWORD_GUID_W, sbstrSelf, &pACESelf);
                        
                        if(pACEEveryone && pACESelf)
                        {
                            LONG lAceType;

                            hr = pACEEveryone->get_AceType(&lAceType);
                            if(SUCCEEDED(hr) && (ADS_ACETYPE_ACCESS_DENIED_OBJECT == lAceType))
                            {
                                fEveryone = TRUE;
                            }

                            hr = pACESelf->get_AceType(&lAceType);
                            if(SUCCEEDED(hr) && (ADS_ACETYPE_ACCESS_DENIED_OBJECT == lAceType))
                            {
                                fSelf = TRUE;
                            }
                        }

                        if(fEveryone && fSelf)
                        {
                            *pfCannotChangePassword = TRUE;
                        }
                        else
                        {
                            *pfCannotChangePassword = FALSE;
                        }
                    }

                    pDisp->Release();
                }
                
                psd->Release();
            }
        }
        
        pads->Release();
    }

    return hr;
}
```



<span data-ttu-id="b0436-120">L’exemple de code suivant montre comment déterminer si l’utilisateur ne peut pas modifier l’autorisation de mot de passe à l’aide du fournisseur LDAP.</span><span class="sxs-lookup"><span data-stu-id="b0436-120">The following code example shows how to determine the User Cannot Change Password Permission using the LDAP provider.</span></span>

> [!Note]  
> <span data-ttu-id="b0436-121">L’exemple de code suivant fonctionne uniquement pour les domaines dans lesquels la langue principale est l’anglais, car les chaînes « tout le monde » et « autorisations NT » \\ sont localisées en fonction de la langue du premier contrôleur de domaine dans le domaine.</span><span class="sxs-lookup"><span data-stu-id="b0436-121">The following code example only works for domains where the primary language is English, because the "Everyone" and "NT AUTHORITY\\SELF" strings are localized based on the language of the first domain controller in the domain.</span></span> <span data-ttu-id="b0436-122">Il n’existe aucun moyen de Visual Basic pour obtenir les noms de compte d’une entité de sécurité connue sans appeler la fonction [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) .</span><span class="sxs-lookup"><span data-stu-id="b0436-122">There is no way in Visual Basic to obtain the account names for a well-known security principal without calling the [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) function.</span></span> <span data-ttu-id="b0436-123">Si vous utilisez Visual Basic, il est recommandé d’utiliser le fournisseur WinNT pour déterminer si l’utilisateur ne peut pas modifier l’autorisation de mot de passe, comme indiqué dans lecture de l' [utilisateur ne peut pas changer de mot de passe (fournisseur WinNT)](reading-user-cannot-change-password-winnt-provider.md).</span><span class="sxs-lookup"><span data-stu-id="b0436-123">If using Visual Basic, it is suggested that you use the WinNT provider to determine the User Cannot Change Password Permission as shown in [Reading User Cannot Change Password (WinNT Provider)](reading-user-cannot-change-password-winnt-provider.md).</span></span>

 


```VB
Const CHANGE_PASSWORD_GUID = "{AB721A53-1E2F-11D0-9819-00AA0040529B}"
Const ADS_ACETYPE_ACCESS_DENIED_OBJECT = &H6

Function UserCannotChangePassword(strUserDN As String, strUsername As String, strPassword As String) As Boolean
    UserCannotChangePassword = False
    
    Dim oUser As IADs
    Dim oSecDesc As IADsSecurityDescriptor
    Dim oACL As IADsAccessControlList
    Dim oACE As IADsAccessControlEntry
    Dim fEveryone As Boolean
    Dim fSelf As Boolean
    
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
    
    For Each oACE In oACL
        If UCase(oACE.ObjectType) = UCase(CHANGE_PASSWORD_GUID) Then
            If oACE.Trustee = "Everyone" And oACE.AceType = ADS_ACETYPE_ACCESS_DENIED_OBJECT Then
                fEveryone = True
            End If
        
            If oACE.Trustee = "NT AUTHORITY\SELF" And oACE.AceType = ADS_ACETYPE_ACCESS_DENIED_OBJECT Then
                fSelf = True
            End If
        End If
    Next
    
    If fSelf And fEveryone Then
        UserCannotChangePassword = True
    Else
        UserCannotChangePassword = False
    End If
End Function
```



 

 