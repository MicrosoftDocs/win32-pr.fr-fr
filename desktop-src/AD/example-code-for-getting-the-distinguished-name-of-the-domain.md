---
title: Exemple de code pour obtenir le nom unique du domaine
description: Cette rubrique contient un exemple de code qui obtient le nom unique du domaine dont l’ordinateur local est membre à l’aide d’une liaison sans serveur.
ms.assetid: 2b478c55-4683-48cd-bee9-385eea38d01d
ms.tgt_platform: multiple
keywords:
- Active Directory exemples Active Directory, obtention du nom unique du domaine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62ebf027e6c95915e34b70f942fdbf342b3f49b9695d7885c442f015d2a74077
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118693643"
---
# <a name="example-code-for-getting-the-distinguished-name-of-the-domain"></a>Exemple de code pour obtenir le nom unique du domaine

Cette rubrique contient un exemple de code qui obtient le nom unique du domaine dont l’ordinateur local est membre à l’aide d’une liaison sans serveur.

l’exemple de code Visual Basic suivant obtient le nom unique du domaine dont l’ordinateur local est membre à l’aide d’une liaison sans serveur.


```VB
Dim rootDSE As IADs
Dim DistinguishedName As String
 
Set rootDSE = GetObject("LDAP://rootDSE")
DistinguishedName = "LDAP://" & rootDSE.Get("defaultNamingContext")
```



L’exemple de code C# suivant obtient le nom unique du domaine dont l’ordinateur local est membre à l’aide d’une liaison sans serveur.


```CSharp
DirectoryEntry RootDirEntry = new DirectoryEntry("LDAP://RootDSE");
Object distinguishedName = RootDirEntry.Properties["defaultNamingContext"].Value;
```



L’exemple de code C/C++ suivant obtient le nom unique du domaine dont l’ordinateur local est membre à l’aide d’une liaison sans serveur.


```C++
IADs *pads;
hr = ADsGetObject(  L"LDAP://rootDSE",
                    IID_IADs, 
                    (void**)&pads);

if(SUCCEEDED(hr))
{
    VARIANT var;

    VariantInit(&var);
    
    hr = pads->Get(CComBSTR("defaultNamingContext"), &var);
    if(SUCCEEDED(hr))
    {
        if(VT_BSTR == var.vt)
        {
            wprintf(var.bstrVal);
        }
        
        VariantClear(&var);
    }
    
    pads->Release();
}
```



 

 




