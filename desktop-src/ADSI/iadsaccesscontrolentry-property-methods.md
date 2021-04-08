---
title: Méthodes de propriété IADsAccessControlEntry (IADs. h)
description: Les méthodes de propriété de l’interface IADsAccessControlEntry obtiennent ou définissent les propriétés décrites dans le tableau suivant. Pour plus d’informations, consultez Méthodes de propriété d’interface.
ms.assetid: dce11723-0e30-4baa-8666-0a32f0968ebb
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsAccessControlEntry ADSI
topic_type:
- apiref
api_name:
- IADsAccessControlEntry Property Methods
- IADsAccessControlEntry.AccessMask
- IADsAccessControlEntry.get_AccessMask
- IADsAccessControlEntry.put_AccessMask
- IADsAccessControlEntry.AceType
- IADsAccessControlEntry.get_AceType
- IADsAccessControlEntry.put_AceType
- IADsAccessControlEntry.AceFlags
- IADsAccessControlEntry.get_AceFlags
- IADsAccessControlEntry.put_AceFlags
- IADsAccessControlEntry.Flags
- IADsAccessControlEntry.get_Flags
- IADsAccessControlEntry.put_Flags
- IADsAccessControlEntry.ObjectType
- IADsAccessControlEntry.get_ObjectType
- IADsAccessControlEntry.put_ObjectType
- IADsAccessControlEntry.InheritedObjectType
- IADsAccessControlEntry.get_InheritedObjectType
- IADsAccessControlEntry.put_InheritedObjectType
- IADsAccessControlEntry.Trustee
- IADsAccessControlEntry.get_Trustee
- IADsAccessControlEntry.put_Trustee
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b8539807f21944ab6f4b2c03f04b14a53dffdb4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740525"
---
# <a name="iadsaccesscontrolentry-property-methods"></a><span data-ttu-id="9bac8-105">Méthodes de propriété IADsAccessControlEntry</span><span class="sxs-lookup"><span data-stu-id="9bac8-105">IADsAccessControlEntry Property Methods</span></span>

<span data-ttu-id="9bac8-106">Les méthodes de propriété de l’interface [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) obtiennent ou définissent les propriétés décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="9bac8-106">The property methods of the [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="9bac8-107">Pour plus d’informations, consultez [méthodes de propriété d’interface](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="9bac8-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="9bac8-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9bac8-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="9bac8-109">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="9bac8-109">**AccessMask**</span></span>
<span data-ttu-id="9bac8-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="9bac8-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="9bac8-111">Contient un jeu d’indicateurs qui spécifie des privilèges d’accès pour l’objet.</span><span class="sxs-lookup"><span data-stu-id="9bac8-111">Contains a set of flags that specifies access privileges for the object.</span></span> <span data-ttu-id="9bac8-112">Les valeurs valides pour les objets Active Directory sont définies dans l’énumération d’énumération des [**\_ \_ droits ADS**](/windows/win32/api/iads/ne-iads-ads_rights_enum) .</span><span class="sxs-lookup"><span data-stu-id="9bac8-112">Valid values for Active Directory objects are defined in the [**ADS\_RIGHTS\_ENUM**](/windows/win32/api/iads/ne-iads-ads_rights_enum) enumeration.</span></span>

<span data-ttu-id="9bac8-113">Pour plus d’informations et pour obtenir la liste des valeurs possibles pour les objets fichier ou partage de fichiers, consultez [sécurité des fichiers et droits d’accès](/windows/desktop/FileIO/file-security-and-access-rights).</span><span class="sxs-lookup"><span data-stu-id="9bac8-113">For more information and a list of possible values for file or file share objects, see [File Security and Access Rights](/windows/desktop/FileIO/file-security-and-access-rights).</span></span>

<span data-ttu-id="9bac8-114">Pour plus d’informations et pour obtenir la liste des valeurs possibles pour les objets du Registre, consultez [sécurité des clés de Registre et droits d’accès](/windows/desktop/SysInfo/registry-key-security-and-access-rights).</span><span class="sxs-lookup"><span data-stu-id="9bac8-114">For more information and a list of possible values for registry objects, see [Registry Key Security and Access Rights](/windows/desktop/SysInfo/registry-key-security-and-access-rights).</span></span>

<dt>

<span data-ttu-id="9bac8-115">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="9bac8-115">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="9bac8-116">Type de données de script : **long**</span><span class="sxs-lookup"><span data-stu-id="9bac8-116">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AccessMask(
  [out] LONG* plnAccessMask
);
HRESULT put_AccessMask(
  [in] LONG lnAccessMask
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="9bac8-117">**AceFlags**</span><span class="sxs-lookup"><span data-stu-id="9bac8-117">**AceFlags**</span></span>
<span data-ttu-id="9bac8-118"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="9bac8-118"></dt> <dd> <dl></span></span>

<span data-ttu-id="9bac8-119">Contient un jeu d’indicateurs qui spécifie si d’autres conteneurs ou objets peuvent hériter de l’entrée du contrôle d’accès.</span><span class="sxs-lookup"><span data-stu-id="9bac8-119">Contains a set of flags that specifies if other containers or objects can inherit the ACE.</span></span> <span data-ttu-id="9bac8-120">Les valeurs valides pour Active Directory objet sont définies dans l’énumération [**\_ \_ enum ACEFLAG ADS**](/windows/win32/api/iads/ne-iads-ads_aceflag_enum) .</span><span class="sxs-lookup"><span data-stu-id="9bac8-120">Valid values for Active Directory object are defined in the [**ADS\_ACEFLAG\_ENUM**](/windows/win32/api/iads/ne-iads-ads_aceflag_enum) enumeration.</span></span>

<span data-ttu-id="9bac8-121">Pour plus d’informations et pour obtenir des valeurs possibles pour les objets de fichier, de partage de fichiers et de Registre, consultez le membre **AceFlags** de la structure d' [**\_ en-tête ACE**](/windows/desktop/api/winnt/ns-winnt-ace_header) .</span><span class="sxs-lookup"><span data-stu-id="9bac8-121">For more information and possible values for file, file share, and registry objects, see the **AceFlags** member of the [**ACE\_HEADER**](/windows/desktop/api/winnt/ns-winnt-ace_header) structure.</span></span>

<dt>

<span data-ttu-id="9bac8-122">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="9bac8-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="9bac8-123">Type de données de script : **long**</span><span class="sxs-lookup"><span data-stu-id="9bac8-123">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AceFlags(
  [out] LONG* plnAceFlags
);
HRESULT put_AceFlags(
  [in] LONG lnAceFlags
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="9bac8-124">**AceType**</span><span class="sxs-lookup"><span data-stu-id="9bac8-124">**AceType**</span></span>
<span data-ttu-id="9bac8-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="9bac8-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="9bac8-126">Contient une valeur qui indique le type d’entrée du contrôle d’accès.</span><span class="sxs-lookup"><span data-stu-id="9bac8-126">Contains a value that indicates the type of ACE.</span></span> <span data-ttu-id="9bac8-127">Les valeurs valides pour les objets Active Directory sont définies dans l’énumération [**\_ \_ enum ACETYPE ADS**](/windows/win32/api/iads/ne-iads-ads_acetype_enum) .</span><span class="sxs-lookup"><span data-stu-id="9bac8-127">Valid values for Active Directory objects are defined in the [**ADS\_ACETYPE\_ENUM**](/windows/win32/api/iads/ne-iads-ads_acetype_enum) enumeration.</span></span>

<span data-ttu-id="9bac8-128">Pour plus d’informations et pour obtenir des valeurs possibles pour les objets de fichier, de partage de fichiers et de Registre, consultez le membre **AceType** de la structure d' [**\_ en-tête ACE**](/windows/desktop/api/winnt/ns-winnt-ace_header) .</span><span class="sxs-lookup"><span data-stu-id="9bac8-128">For more information and possible values for file, file share, and registry objects, see the **AceType** member of the [**ACE\_HEADER**](/windows/desktop/api/winnt/ns-winnt-ace_header) structure.</span></span>

<dt>

<span data-ttu-id="9bac8-129">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="9bac8-129">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="9bac8-130">Type de données de script : **long**</span><span class="sxs-lookup"><span data-stu-id="9bac8-130">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AceType(
  [out] LONG* plAceType
);
HRESULT put_AceType(
  [in] LONG lnAceType
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="9bac8-131">**Indicateurs**</span><span class="sxs-lookup"><span data-stu-id="9bac8-131">**Flags**</span></span>
<span data-ttu-id="9bac8-132"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="9bac8-132"></dt> <dd> <dl></span></span>

<span data-ttu-id="9bac8-133">Indicateur qui signale si l’entrée du contrôle d’accès a un type d’objet ou un type d’objet hérité.</span><span class="sxs-lookup"><span data-stu-id="9bac8-133">A flag that indicates if the ACE has an object type or inherited object type.</span></span> <span data-ttu-id="9bac8-134">Les indicateurs valides sont définis dans l’énumération [**\_ \_ enum FLAGTYPE ADS**](/windows/win32/api/iads/ne-iads-ads_flagtype_enum) .</span><span class="sxs-lookup"><span data-stu-id="9bac8-134">Valid flags are defined in the [**ADS\_FLAGTYPE\_ENUM**](/windows/win32/api/iads/ne-iads-ads_flagtype_enum) enumeration.</span></span>

<dt>

<span data-ttu-id="9bac8-135">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="9bac8-135">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="9bac8-136">Type de données de script : **long**</span><span class="sxs-lookup"><span data-stu-id="9bac8-136">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Flags(
  [out] LONG* lnflags
);
HRESULT put_Flags(
  [in] LONG lnflags
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="9bac8-137">**InheritedObjectType**</span><span class="sxs-lookup"><span data-stu-id="9bac8-137">**InheritedObjectType**</span></span>
<span data-ttu-id="9bac8-138"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="9bac8-138"></dt> <dd> <dl></span></span>

<span data-ttu-id="9bac8-139">Indicateur qui spécifie le type d’un objet enfant d’un objet ADSI.</span><span class="sxs-lookup"><span data-stu-id="9bac8-139">A flag that indicates the type of a child object of an ADSI object.</span></span> <span data-ttu-id="9bac8-140">Sa valeur est un **GUID** vers un objet dans un format de chaîne.</span><span class="sxs-lookup"><span data-stu-id="9bac8-140">Its value is a **GUID** to an object in string format.</span></span> <span data-ttu-id="9bac8-141">Lorsqu’un **GUID** de ce type est défini, l’entrée du contrôle d’accès s’applique uniquement à l’objet référencé par le **GUID**.</span><span class="sxs-lookup"><span data-stu-id="9bac8-141">When such a **GUID** is set, the ACE applies only to the object referred to by the **GUID**.</span></span>

<dt>

<span data-ttu-id="9bac8-142">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="9bac8-142">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="9bac8-143">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="9bac8-143">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_InheritedObjectType(
  [out] BSTR* bstrInheritedObjectType
);
HRESULT put_InheritedObjectType(
  [in] BSTR bstrInheritedObjectType
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="9bac8-144">**ObjectType**</span><span class="sxs-lookup"><span data-stu-id="9bac8-144">**ObjectType**</span></span>
<span data-ttu-id="9bac8-145"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="9bac8-145"></dt> <dd> <dl></span></span>

<span data-ttu-id="9bac8-146">Indicateur qui spécifie le type d’objet ADSI.</span><span class="sxs-lookup"><span data-stu-id="9bac8-146">A flag that indicates the ADSI object type.</span></span> <span data-ttu-id="9bac8-147">Sa valeur est un **GUID** d’une propriété ou d’un objet dans un format de chaîne.</span><span class="sxs-lookup"><span data-stu-id="9bac8-147">Its value is a **GUID** to a property or an object in string format.</span></span> <span data-ttu-id="9bac8-148">L' **identificateur global unique (GUID** ) fait référence à une propriété lorsque les masques d’accès aux propriétés de **\_ \_ \_ lecture \_** DS et d' **\_ \_ \_ écriture \_** des propriétés des services de domaine Active Directory appropriés sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="9bac8-148">The **GUID** refers to a property when **ADS\_RIGHT\_DS\_READ\_PROP** and **ADS\_RIGHT\_DS\_WRITE\_PROP** access masks are used.</span></span> <span data-ttu-id="9bac8-149">Le **GUID** spécifie un objet lorsque les **services de domaine Active Directory de \_ droite créer des \_ \_ \_ enfants** et des publicités droit de suppression des masques d’accès **\_ \_ \_ \_ enfants** sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="9bac8-149">The **GUID** specifies an object when **ADS\_RIGHT\_DS\_CREATE\_CHILD** and **ADS\_RIGHT\_DS\_DELETE\_CHILD** access masks are used.</span></span>

<dt>

<span data-ttu-id="9bac8-150">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="9bac8-150">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="9bac8-151">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="9bac8-151">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ObjectType(
  [out] BSTR* bstrObjectType
);
HRESULT put_ObjectType(
  [in] BSTR bstrObjectType
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="9bac8-152">**Tiers**</span><span class="sxs-lookup"><span data-stu-id="9bac8-152">**Trustee**</span></span>
<span data-ttu-id="9bac8-153"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="9bac8-153"></dt> <dd> <dl></span></span>

<span data-ttu-id="9bac8-154">Contient le nom du compte auquel s’applique l’entrée du contrôle d’accès.</span><span class="sxs-lookup"><span data-stu-id="9bac8-154">Contains the name of the account that the ACE applies to.</span></span>

<dt>

<span data-ttu-id="9bac8-155">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="9bac8-155">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="9bac8-156">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="9bac8-156">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Trustee(
  [out] BSTR* pbstrSecurityId
);
HRESULT put_Trustee(
  [in] BSTR bstrSecurityId
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="9bac8-157">Exemples</span><span class="sxs-lookup"><span data-stu-id="9bac8-157">Examples</span></span>

<span data-ttu-id="9bac8-158">L’exemple de code suivant montre comment ajouter des entrées à une liste de contrôle d’accès discrétionnaire à l’aide des méthodes de propriété [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) .</span><span class="sxs-lookup"><span data-stu-id="9bac8-158">The following code example shows how to add entries to a discretionary ACL using the [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) property methods.</span></span>


```VB
Dim x As IADs
Dim sd As IADsSecurityDescriptor
Dim ace As IADsAccessControlEntry
Dim Dacl As IADsAccessControlList
Dim Ace1 As New AccessControlEntry
Dim Ace2 As New AccessControlEntry

On Error GoTo Cleanup
 
Set x = GetObject("LDAP://OU=Sales, DC=Fabrikam,DC=com")
Set sd = x.Get("ntSecurityDescriptor")
Set Dacl = sd.DiscretionaryAcl
 
' Show the existing ACEs.
For Each ace In Dacl
  Debug.Print ace.Trustee
Next
 
 
' Setup the first ACE.
Ace1.AccessMask = -1 'Full Permission (Allowed)
Ace1.AceType = ADS_ACETYPE_ACCESS_ALLOWED
Ace1.AceFlags = ADS_ACEFLAG_INHERIT_ACE
Ace1.Trustee = "ACTIVED\Administrator"
 
' Setup the 2nd ACE.
Ace2.AccessMask = -1 'Full Permission (Denied)
Ace2.AceType = ADS_ACETYPE_ACCESS_DENIED
Ace2.AceFlags = ADS_ACEFLAG_INHERIT_ACE
Ace2.Trustee = "ACTIVED\Andyhar"
 
' Add the ACEs to the Discretionary ACL.
Dacl.AddAce Ace1
Dacl.AddAce Ace2
 
sd.DiscretionaryAcl = Dacl
x.Put "ntSecurityDescriptor", Array(sd)
x.SetInfo

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If

    Set x = Nothing
    Set sd = Nothing
    Set ace = Nothing
    Set Dacl = Nothing
    Set Ace1 = Nothing
    Set Ace2 = Nothing
    Set obj = Nothing
    Set cls = Nothing
```



<span data-ttu-id="9bac8-159">L’exemple de code suivant affiche les entrées de contrôle d’accès.</span><span class="sxs-lookup"><span data-stu-id="9bac8-159">The following code example displays access-control entries.</span></span>


```C++
IADs *pADs = NULL;
IDispatch *pDisp = NULL;
IADsSecurityDescriptor *pSD = NULL;
VARIANT var;
HRESULT hr = S_OK;
 
VariantInit(&var);

hr = ADsOpenObject(L"LDAP://OU=Sales, DC=Fabrikam,DC=com",NULL,NULL,
                   ADS_SECURE_AUTHENTICATION, IID_IADs,(void**)&pADs);
if(FAILED(hr)) {goto Cleanup;}

hr = pADs->Get(CComBSTR("ntSecurityDescriptor"),&var);
if(FAILED(hr)) {goto Cleanup;}

pDisp = V_DISPATCH(&var);

hr = pDisp->QueryInterface(IID_IADsSecurityDescriptor,(void**)&pSD);
if(FAILED(hr)) {goto Cleanup;}
pDisp->Release();


pSD->get_DiscretionaryAcl(&pDisp);

hr = pDisp->QueryInterface(IID_IADsAccessControlList,(void**)&pACL);
if(FAILED(hr)) {goto Cleanup;}

hr = DisplayAccessInfo(pSD);
if(FAILED(hr)) {goto Cleanup;}
VariantClear(&var);

Cleanup:
    if(pADs) pADs->Release();
    if(pDisp) pDisp->Release();
    if(pSD) pSD->Release();
    return hr;



HRESULT DisplayAccessInfo(IADsSecurityDescriptor *pSD)
{
    LPWSTR lpszFunction = L"DisplayAccessInfo";
    IDispatch *pDisp = NULL;
    IADsAccessControlList *pACL = NULL;
    IADsAccessControlEntry *pACE = NULL;
    IEnumVARIANT *pEnum = NULL;
    IUnknown *pUnk = NULL;
    HRESULT hr = S_OK;
    ULONG nFetch = 0;
    BSTR bstrValue = NULL;
    VARIANT var;
    LPWSTR lpszOutput = NULL;
    LPWSTR lpszMask = NULL;
    size_t nLength = 0;
    
    VariantInit(&var);
    
    hr = pSD->get_DiscretionaryAcl(&pDisp);
    if(FAILED(hr)){goto Cleanup;}
    hr = pDisp->QueryInterface(IID_IADsAccessControlList,(void**)&pACL);
    if(FAILED(hr)){goto Cleanup;}
    
    hr = pACL->get__NewEnum(&pUnk);
    if(FAILED(hr)){goto Cleanup;}
    
    hr = pUnk->QueryInterface(IID_IEnumVARIANT,(void**)&pEnum);
    
    if(FAILED(hr)){goto Cleanup;}
    hr = pEnum->Next(1,&var,&nFetch);
    
    while(hr == S_OK)
    {
        if(nFetch==1)
        {
            if(VT_DISPATCH != V_VT(&var))
            {
                goto Cleanup;
            }
            
            pDisp = V_DISPATCH(&var);
            hr = pDisp->QueryInterface(IID_IADsAccessControlEntry,(void**)&pACE);
            
            if(SUCCEEDED(hr))
            {
                lpszMask = L"Trustee: %s";
                hr = pACE->get_Trustee(&bstrValue);
                nLength = wcslen(lpszMask) + wcslen(bstrValue) + 1;
                lpszOutput = new WCHAR[nLength];
                swprintf_s(lpszOutput,lpszMask,bstrValue);
                printf(lpszOutput);
                delete [] lpszOutput;
                SysFreeString(bstrValue);
                
                pACE->Release();
                pACE = NULL;
                pDisp->Release();
                pDisp = NULL;
            }       
            
            VariantClear(&var);
        }       
        hr = pEnum->Next(1,&var,&nFetch);
    }
    
Cleanup:
    if(pDisp) pDisp->Release();
    if(pACL) pACL->Release();
    if(pACE) pACE->Release();
    if(pEnum) pEnum->Release();
    if(pUnk) pUnk->Release();
    if(szValue) SysFreeString(szValue);
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="9bac8-160">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9bac8-160">Requirements</span></span>



| <span data-ttu-id="9bac8-161">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9bac8-161">Requirement</span></span> | <span data-ttu-id="9bac8-162">Valeur</span><span class="sxs-lookup"><span data-stu-id="9bac8-162">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bac8-163">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9bac8-163">Minimum supported client</span></span><br/> | <span data-ttu-id="9bac8-164">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9bac8-164">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="9bac8-165">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9bac8-165">Minimum supported server</span></span><br/> | <span data-ttu-id="9bac8-166">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9bac8-166">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="9bac8-167">En-tête</span><span class="sxs-lookup"><span data-stu-id="9bac8-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="9bac8-168"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="9bac8-168"><dt>Iads.h</dt></span></span> </dl>         |
| <span data-ttu-id="9bac8-169">DLL</span><span class="sxs-lookup"><span data-stu-id="9bac8-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9bac8-170"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9bac8-170"><dt>Activeds.dll</dt></span></span> </dl>   |
| <span data-ttu-id="9bac8-171">IID</span><span class="sxs-lookup"><span data-stu-id="9bac8-171">IID</span></span><br/>                      | <span data-ttu-id="9bac8-172">IID \_ IADsAccessControlEntry est défini en tant que B4F3A14C-9BDD-11D0-852C-00C04FD8D503</span><span class="sxs-lookup"><span data-stu-id="9bac8-172">IID\_IADsAccessControlEntry is defined as B4F3A14C-9BDD-11D0-852C-00C04FD8D503</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9bac8-173">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9bac8-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bac8-174">**IADsAccessControlEntry**</span><span class="sxs-lookup"><span data-stu-id="9bac8-174">**IADsAccessControlEntry**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)
</dt> <dt>

[<span data-ttu-id="9bac8-175">**IADsAccessControlList**</span><span class="sxs-lookup"><span data-stu-id="9bac8-175">**IADsAccessControlList**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)
</dt> <dt>

[<span data-ttu-id="9bac8-176">**IADsSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="9bac8-176">**IADsSecurityDescriptor**</span></span>](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)
</dt> </dl>

 

