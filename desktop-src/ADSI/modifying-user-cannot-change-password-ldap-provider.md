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
ms.openlocfilehash: 9e1628b113c2f15278bc72e41aa79e4be03a98f2
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730276"
---
# <a name="modifying-user-cannot-change-password-ldap-provider"></a><span data-ttu-id="7237d-106">La modification de l’utilisateur ne peut pas changer le mot de passe (fournisseur LDAP)</span><span class="sxs-lookup"><span data-stu-id="7237d-106">Modifying User Cannot Change Password (LDAP Provider)</span></span>

<span data-ttu-id="7237d-107">La possibilité pour un utilisateur de modifier son propre mot de passe est une autorisation qui peut être accordée ou refusée.</span><span class="sxs-lookup"><span data-stu-id="7237d-107">The ability of a user to change their own password is a permission that can be grant or denied.</span></span> <span data-ttu-id="7237d-108">Pour refuser cette autorisation, définissez deux ACE dans la liste de contrôle d’accès discrétionnaire (DACL) du descripteur de sécurité de l’objet utilisateur avec le type d’ACE d' **\_ \_ \_ \_ objet accès refusé ADS ACETYPE** .</span><span class="sxs-lookup"><span data-stu-id="7237d-108">To deny this permission, set two ACEs in the security descriptor discretionary access control list (DACL) of the user object with the **ADS\_ACETYPE\_ACCESS\_DENIED\_OBJECT** ace type.</span></span> <span data-ttu-id="7237d-109">Une entrée de contrôle d’accès refuse l’autorisation à l’utilisateur et une autre entrée de contrôle d’accès refuse l’autorisation au groupe tout le monde.</span><span class="sxs-lookup"><span data-stu-id="7237d-109">One ACE denies the permission to the user and another ACE denies the permission to the Everyone group.</span></span> <span data-ttu-id="7237d-110">Les deux ACE sont des ACE de refus spécifiques aux objets qui spécifient le GUID de l’autorisation étendue pour la modification des mots de passe.</span><span class="sxs-lookup"><span data-stu-id="7237d-110">Both ACEs are object-specific deny ACEs that specify the GUID of the extended permission for changing passwords.</span></span> <span data-ttu-id="7237d-111">Pour accorder cette autorisation, définissez les mêmes entrées de contrôle d’accès avec le type d’ACE d' **\_ \_ \_ \_ objet accès autorisé ADS ACETYPE** .</span><span class="sxs-lookup"><span data-stu-id="7237d-111">To grant this permission, set the same ACEs with the **ADS\_ACETYPE\_ACCESS\_ALLOWED\_OBJECT** ace type.</span></span>

<span data-ttu-id="7237d-112">La procédure suivante décrit comment modifier ou ajouter des ACE pour cette autorisation.</span><span class="sxs-lookup"><span data-stu-id="7237d-112">The following procedure describes how to modify or add ACEs for this permission.</span></span>

<span data-ttu-id="7237d-113">**Pour modifier ou ajouter les ACE pour cette autorisation**</span><span class="sxs-lookup"><span data-stu-id="7237d-113">**To modify or add the ACEs for this permission**</span></span>

1.  <span data-ttu-id="7237d-114">Lier à l’objet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7237d-114">Bind to the user object.</span></span>
2.  <span data-ttu-id="7237d-115">Obtenez l’objet [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) à partir de la propriété **ntSecurityDescriptor** de l’objet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7237d-115">Obtain the [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) object from the **ntSecurityDescriptor** property of the user object.</span></span>
3.  <span data-ttu-id="7237d-116">Obtenez une interface [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist) pour le descripteur de sécurité à partir de la propriété [**IADsSecurityDescriptor. DiscretionaryAcl**](iadssecuritydescriptor-property-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="7237d-116">Obtain an [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist) interface for the security descriptor from the [**IADsSecurityDescriptor.DiscretionaryAcl**](iadssecuritydescriptor-property-methods.md) property.</span></span>
4.  <span data-ttu-id="7237d-117">Énumérez les ACE pour l’objet et recherchez les entrées de du mot de passe qui ont le GUID de modification du mot de passe ({AB721A53-1E2F-11D0-9819-00AA0040529B}) pour la propriété [**IADsAccessControlEntry. ObjectType**](iadsaccesscontrolentry-property-methods.md) et « tout le monde » ou « autorité NT \\ autonome » pour la propriété **IADsAccessControlEntry. Trusted** .</span><span class="sxs-lookup"><span data-stu-id="7237d-117">Enumerate the ACEs for the object and search for the ACEs that have the change password GUID ({AB721A53-1E2F-11D0-9819-00AA0040529B}) for the [**IADsAccessControlEntry.ObjectType**](iadsaccesscontrolentry-property-methods.md) property and "Everyone" or "NT AUTHORITY\\SELF" for the **IADsAccessControlEntry.Trustee** property.</span></span>

    > [!Note]  
    > <span data-ttu-id="7237d-118">Les chaînes « tout le monde » et « Self de l’autorité NT \\ » sont localisées en fonction de la langue du premier contrôleur de domaine dans le domaine.</span><span class="sxs-lookup"><span data-stu-id="7237d-118">The "Everyone" and "NT AUTHORITY\\SELF" strings are localized based on the language of the first domain controller in the domain.</span></span> <span data-ttu-id="7237d-119">Pour cette raison, les chaînes ne doivent pas être utilisées directement.</span><span class="sxs-lookup"><span data-stu-id="7237d-119">Because of this, the strings should not be used directly.</span></span> <span data-ttu-id="7237d-120">Les noms de comptes doivent être obtenus au moment de l’exécution en appelant la fonction [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) avec le SID pour « tout le monde » (« S-1-1-0 ») et les principaux de sécurité « NT Authority \\ Self » (« s-1-5-10 ») connus.</span><span class="sxs-lookup"><span data-stu-id="7237d-120">The account names should be obtained at run time by calling the [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) function with the SID for "Everyone" ("S-1-1-0") and "NT AUTHORITY\\SELF" ("S-1-5-10") well-known security principals.</span></span> <span data-ttu-id="7237d-121">Les exemples de fonctions **GetSidAccountName**, **GetSidAccountName \_ everyone** et **GetSidAccountName \_ Self** C++ illustrés dans lecture de l' [utilisateur ne peuvent pas changer de mot de passe (fournisseur LDAP)](reading-user-cannot-change-password-ldap-provider.md) montrent comment procéder.</span><span class="sxs-lookup"><span data-stu-id="7237d-121">The **GetSidAccountName**, **GetSidAccountName\_Everyone**, and **GetSidAccountName\_Self** C++ example functions shown in [Reading User Cannot Change Password (LDAP Provider)](reading-user-cannot-change-password-ldap-provider.md) demonstrate how to do this.</span></span>

     

5.  <span data-ttu-id="7237d-122">Modifiez la propriété [**IADsAccessControlEntry. AceType**](iadsaccesscontrolentry-property-methods.md) des ACE qui ont été trouvées pour les **publicités \_ AceType \_ \_ \_ objet accès refusé** si l’utilisateur ne peut pas modifier son mot de passe ou les **publicités AceType l' \_ \_ accès aux \_ \_ objets autorisés** si l’utilisateur peut modifier son mot de passe.</span><span class="sxs-lookup"><span data-stu-id="7237d-122">Modify the [**IADsAccessControlEntry.AceType**](iadsaccesscontrolentry-property-methods.md) property of the ACEs that were found to **ADS\_ACETYPE\_ACCESS\_DENIED\_OBJECT** if the user cannot change their password or **ADS\_ACETYPE\_ACCESS\_ALLOWED\_OBJECT** if the user can change their password.</span></span>
6.  <span data-ttu-id="7237d-123">Si l’ACE « tout le monde » est introuvable, créez un nouvel objet [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) qui contient les valeurs de propriété indiquées dans le tableau ci-dessous et ajoutez la nouvelle entrée à la liste de contrôle d’accès avec la méthode [**IADsAccessControlList. AddAce**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-addace) .</span><span class="sxs-lookup"><span data-stu-id="7237d-123">If the "Everyone" ACE is not found, create a new [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) object that contains the property values shown in the table below and add the new entry to the ACL with the [**IADsAccessControlList.AddAce**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-addace) method.</span></span>
7.  <span data-ttu-id="7237d-124">Si l’entrée du contrôle d’accès de l’autorité NT \\ est introuvable, créez un objet [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) avec les mêmes valeurs de propriété que celles indiquées dans le tableau ci-dessous, à l’exception de la propriété [**Trusted**](iadsaccesscontrolentry-property-methods.md) contenant le nom de compte « S-1-5-10 » (« AUTORITE NT \\ Self »).</span><span class="sxs-lookup"><span data-stu-id="7237d-124">If the "NT AUTHORITY\\SELF" ACE is not found, create a new [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) object with the same property values shown in the table below except the [**Trustee**](iadsaccesscontrolentry-property-methods.md) property contains the account name for SID "S-1-5-10" ("NT AUTHORITY\\SELF").</span></span> <span data-ttu-id="7237d-125">Ajoutez l’entrée à la liste de contrôle d’accès avec la méthode [**IADsAccessControlList. AddAce**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-addace) .</span><span class="sxs-lookup"><span data-stu-id="7237d-125">Add the entry to the ACL with the [**IADsAccessControlList.AddAce**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-addace) method.</span></span>
8.  <span data-ttu-id="7237d-126">Pour mettre à jour la propriété **ntSecurityDescriptor** de l’objet, appelez la méthode [**IADs. put**](/windows/desktop/api/Iads/nf-iads-iads-put) avec le même [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) obtenu à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="7237d-126">To update the **ntSecurityDescriptor** property of the object, call the [**IADs.Put**](/windows/desktop/api/Iads/nf-iads-iads-put) method with the same [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) obtained in Step 2.</span></span>
9.  <span data-ttu-id="7237d-127">Validez les modifications locales sur le serveur à l’aide de la méthode [**IADs. setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) .</span><span class="sxs-lookup"><span data-stu-id="7237d-127">Commit the local changes to the server with the [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method.</span></span>
10. <span data-ttu-id="7237d-128">Si l’une des entrées de contrôle d’accès a été créée, vous devez réorganiser la liste de contrôle d’accès afin que les entrées du contrôle d’accès soient dans le bon ordre.</span><span class="sxs-lookup"><span data-stu-id="7237d-128">If either of the ACEs were created, you must reorder the ACL so that the ACEs are in the correct order.</span></span> <span data-ttu-id="7237d-129">Pour ce faire, appelez la fonction [**GetNamedSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getnamedsecurityinfoa) avec le chemin d’accès LDAP de l’objet, puis la fonction [**SetNamedSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setnamedsecurityinfoa) avec la même liste DACL.</span><span class="sxs-lookup"><span data-stu-id="7237d-129">To do this, call the [**GetNamedSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getnamedsecurityinfoa) function with the LDAP ADsPath of the object and then the [**SetNamedSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setnamedsecurityinfoa) function with the same DACL.</span></span> <span data-ttu-id="7237d-130">Cette réorganisation se produit automatiquement lors de l’ajout des ACE.</span><span class="sxs-lookup"><span data-stu-id="7237d-130">This reordering will occur automatically when the ACEs are added.</span></span>

<span data-ttu-id="7237d-131">Le tableau suivant répertorie les valeurs des propriétés de l’objet [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) .</span><span class="sxs-lookup"><span data-stu-id="7237d-131">The following table lists the [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) object property values.</span></span>



| <span data-ttu-id="7237d-132">Propriété IADsAccessControlEntry</span><span class="sxs-lookup"><span data-stu-id="7237d-132">IADsAccessControlEntry Property</span></span>                                        | <span data-ttu-id="7237d-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="7237d-133">Value</span></span>                                                                                                                                                                 |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7237d-134">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="7237d-134">**AccessMask**</span></span>](iadsaccesscontrolentry-property-methods.md)          | <span data-ttu-id="7237d-135">**\_ \_ \_ accès au contrôle du service d’annuaire AD Right \_**</span><span class="sxs-lookup"><span data-stu-id="7237d-135">**ADS\_RIGHT\_DS\_CONTROL\_ACCESS**</span></span>                                                                                                                                   |
| [<span data-ttu-id="7237d-136">**AceType**</span><span class="sxs-lookup"><span data-stu-id="7237d-136">**AceType**</span></span>](iadsaccesscontrolentry-property-methods.md)             | <span data-ttu-id="7237d-137">**Annonces \_ ACETYPE \_ a \_ refusé l' \_ objet** si l’utilisateur ne peut pas modifier son mot de passe ou son **\_ objet ad ACETYPE \_ Access \_ allowed \_** si l’utilisateur peut modifier son mot de passe.</span><span class="sxs-lookup"><span data-stu-id="7237d-137">**ADS\_ACETYPE\_ACCESS\_DENIED\_OBJECT** if the user cannot change their password or **ADS\_ACETYPE\_ACCESS\_ALLOWED\_OBJECT** if the user can change their password.</span></span> |
| [<span data-ttu-id="7237d-138">**AceFlags**</span><span class="sxs-lookup"><span data-stu-id="7237d-138">**AceFlags**</span></span>](iadsaccesscontrolentry-property-methods.md)            | <span data-ttu-id="7237d-139">0</span><span class="sxs-lookup"><span data-stu-id="7237d-139">0</span></span>                                                                                                                                                                     |
| [<span data-ttu-id="7237d-140">**Père**</span><span class="sxs-lookup"><span data-stu-id="7237d-140">**Flags**</span></span>](iadsaccesscontrolentry-property-methods.md)               | <span data-ttu-id="7237d-141">**\_type d' \_ objet indicateur ADS \_ \_ présent**</span><span class="sxs-lookup"><span data-stu-id="7237d-141">**ADS\_FLAG\_OBJECT\_TYPE\_PRESENT**</span></span>                                                                                                                                  |
| [<span data-ttu-id="7237d-142">**ObjectType**</span><span class="sxs-lookup"><span data-stu-id="7237d-142">**ObjectType**</span></span>](iadsaccesscontrolentry-property-methods.md)          | <span data-ttu-id="7237d-143">« {AB721A53-1E2F-11D0-9819-00AA0040529B} », qui est le GUID de modification du mot de passe sous forme de chaîne.</span><span class="sxs-lookup"><span data-stu-id="7237d-143">"{AB721A53-1E2F-11D0-9819-00AA0040529B}" which is the change password GUID in string form.</span></span>                                                                            |
| [<span data-ttu-id="7237d-144">**InheritedObjectType**</span><span class="sxs-lookup"><span data-stu-id="7237d-144">**InheritedObjectType**</span></span>](iadsaccesscontrolentry-property-methods.md) | <span data-ttu-id="7237d-145">Non utilisé</span><span class="sxs-lookup"><span data-stu-id="7237d-145">Not used</span></span>                                                                                                                                                              |
| [<span data-ttu-id="7237d-146">**Tiers**</span><span class="sxs-lookup"><span data-stu-id="7237d-146">**Trustee**</span></span>](iadsaccesscontrolentry-property-methods.md)             | <span data-ttu-id="7237d-147">Nom de compte pour le SID « S-1-1-0 » (tout le monde).</span><span class="sxs-lookup"><span data-stu-id="7237d-147">Account name for SID "S-1-1-0" (Everyone).</span></span>                                                                                                                            |



 

## <a name="example-code"></a><span data-ttu-id="7237d-148">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="7237d-148">Example Code</span></span>

<span data-ttu-id="7237d-149">L’exemple de code suivant montre comment obtenir une interface pour modifier une liste DACL.</span><span class="sxs-lookup"><span data-stu-id="7237d-149">The following code example shows how to obtain an interface to change a DACL.</span></span> <span data-ttu-id="7237d-150">L’interface [**IADsObjectOptions**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions) peut être utilisée en définissant l’option DACL des **informations de \_ sécurité \_ \_ ADS** .</span><span class="sxs-lookup"><span data-stu-id="7237d-150">The [**IADsObjectOptions**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions) interface can be used by setting the **ADS\_SECURITY\_INFO\_DACL** option.</span></span>

> [!Note]  
> <span data-ttu-id="7237d-151">Pour utiliser le code documenté dans cet exemple, vous devez être un administrateur.</span><span class="sxs-lookup"><span data-stu-id="7237d-151">To use the code documented in this example, you will need to be an Administrator.</span></span> <span data-ttu-id="7237d-152">Si vous n’êtes pas administrateur, vous devez ajouter du code qui utilisera une interface qui permettra à un utilisateur de modifier la façon dont le cache côté client est vidé vers le service domaine Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7237d-152">If you are not an Administrator, then you will need to add more code that will use an interface that will allow a user to change the way the client-side cache is flushed back to the Active Directory Domain Service.</span></span>

 


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



<span data-ttu-id="7237d-153">L’exemple de code suivant montre comment modifier l’autorisation de l’utilisateur ne peut pas modifier le mot de passe à l’aide du fournisseur LDAP.</span><span class="sxs-lookup"><span data-stu-id="7237d-153">The following code example shows how to modify the User Cannot Change Password Permission using the LDAP provider.</span></span> <span data-ttu-id="7237d-154">Cet exemple de code utilise la fonction de l’utilitaire **GetObjectACE** définie ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="7237d-154">This code example uses the **GetObjectACE** utility function defined above.</span></span>

<span data-ttu-id="7237d-155">Cet exemple utilise les exemples de fonctions **GetSidAccountName \_ everyone** et **GetSidAccountName \_ Self** C++ illustrés dans [Read user ne peut pas changer de mot de passe (fournisseur LDAP)](reading-user-cannot-change-password-ldap-provider.md).</span><span class="sxs-lookup"><span data-stu-id="7237d-155">This example uses the **GetSidAccountName\_Everyone** and **GetSidAccountName\_Self** C++ example functions shown in [Reading User Cannot Change Password (LDAP Provider)](reading-user-cannot-change-password-ldap-provider.md).</span></span>


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



<span data-ttu-id="7237d-156">L’exemple de code suivant montre comment modifier l’autorisation de l’utilisateur ne peut pas modifier le mot de passe à l’aide du fournisseur LDAP.</span><span class="sxs-lookup"><span data-stu-id="7237d-156">The following code example shows how to modify the User Cannot Change Password Permission using the LDAP provider.</span></span>

> [!Note]  
> <span data-ttu-id="7237d-157">L’exemple ci-dessous fonctionne uniquement sur les domaines dont la langue principale est l’anglais, car les chaînes « tout le monde » et « autorisations NT » \\ sont localisées en fonction de la langue du premier contrôleur de domaine dans le domaine.</span><span class="sxs-lookup"><span data-stu-id="7237d-157">The example below will only work on domains where the primary language is English because the "Everyone" and "NT AUTHORITY\\SELF" strings are localized based on the language of the first domain controller in the domain.</span></span> <span data-ttu-id="7237d-158">Il n’existe aucun moyen de Visual Basic pour obtenir les noms de compte d’une entité de sécurité connue sans appeler la fonction [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) .</span><span class="sxs-lookup"><span data-stu-id="7237d-158">There is no way in Visual Basic to obtain the account names for a well-known security principal without calling the [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) function.</span></span> <span data-ttu-id="7237d-159">Si vous utilisez Visual Basic, il est recommandé d’utiliser le fournisseur WinNT pour modifier l’autorisation l’utilisateur ne peut pas modifier le mot de passe, comme indiqué dans modification de l' [utilisateur ne peut pas changer de mot de passe (fournisseur WinNT)](modifying-user-cannot-change-password-winnt-provider.md).</span><span class="sxs-lookup"><span data-stu-id="7237d-159">If using Visual Basic, it is suggested that you use the WinNT provider to modify the User Cannot Change Password Permission as shown in [Modifying User Cannot Change Password (WinNT Provider)](modifying-user-cannot-change-password-winnt-provider.md).</span></span>

 


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



 

 