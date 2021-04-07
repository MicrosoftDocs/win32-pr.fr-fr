---
title: Exemple de code pour la modification de l’étendue d’un groupe
description: Cette rubrique contient un exemple de code pour la modification de l’étendue d’un groupe.
ms.assetid: 4ae61101-f123-44bd-8bec-bade51d22217
ms.tgt_platform: multiple
keywords:
- Active Directory exemples Active Directory, modification de l’étendue d’un groupe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 641ad43604785a6aae5bb250061ff0a3b62c294e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028622"
---
# <a name="example-code-for-changing-the-scope-of-a-group"></a><span data-ttu-id="f2054-104">Exemple de code pour la modification de l’étendue d’un groupe</span><span class="sxs-lookup"><span data-stu-id="f2054-104">Example Code for Changing the Scope of a Group</span></span>

<span data-ttu-id="f2054-105">L’exemple de code C++ suivant modifie l’étendue d’un groupe.</span><span class="sxs-lookup"><span data-stu-id="f2054-105">The following C++ code example changes the scope of a group.</span></span>


```C++

    WCHAR *pwszLDAPPath = 
        L"LDAP://CN=mygroup,OU=myou,DC=Fabrikam,DC=com";
 
    HRESULT hr;
    IADsGroup * pGroup = NULL;
 
    // Initialize COM.
    CoInitialize(0);
 
    // Bind to the passed container. 
    hr = ADsGetObject( pwszLDAPPath, IID_IADsGroup,(void **)&pGroup);
 
    if (SUCCEEDED(hr))
    {
        VARIANT vValue;
        BSTR    bsValue = SysAllocString(L"groupType");
        VariantInit(&vValue);
    // Set a new GroupType Value.
        vValue.vt = VT_I4;
        vValue.lVal = ADS_GROUP_TYPE_GLOBAL_GROUP ;
 
        hr = pGroup->Put(bsValue,vValue);
        hr = pGroup->SetInfo();
        pGroup->Release();
        pGroup= NULL;
        SysFreeString(bsValue);
    }
 
    CoUninitialize();
```



<span data-ttu-id="f2054-106">L’exemple de code Visual Basic suivant modifie l’étendue d’un groupe.</span><span class="sxs-lookup"><span data-stu-id="f2054-106">The following Visual Basic code example changes the scope of a group.</span></span>


```VB
Dim x as IADs
On Error GoTo CleanUp
Set x = GetObject("LDAP://CN=mygroup,OU=myou,DC=Fabrikam,DC=com")
x.Put "groupType", 
    ADS_GROUP_TYPE_UNIVERSAL_GROUP|ADS_GROUP_TYPE_SECURITY_ENABLED
Exit Sub

CleanUp:
    MsgBox("An error has occurred.")
    x = Nothing
```



 

 




