---
title: Exemple de code pour obtenir le nom unique du domaine
description: Cette rubrique contient un exemple de code qui obtient le nom unique du domaine dont l’ordinateur local est membre à l’aide d’une liaison sans serveur.
ms.assetid: 2b478c55-4683-48cd-bee9-385eea38d01d
ms.tgt_platform: multiple
keywords:
- Active Directory exemples Active Directory, obtention du nom unique du domaine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4badd8cd356ce5adfb20470a969e6f7444c010a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104190765"
---
# <a name="example-code-for-getting-the-distinguished-name-of-the-domain"></a>Exemple de code pour obtenir le nom unique du domaine

Cette rubrique contient un exemple de code qui obtient le nom unique du domaine dont l’ordinateur local est membre à l’aide d’une liaison sans serveur.

L’exemple de code Visual Basic suivant obtient le nom unique du domaine dont l’ordinateur local est membre à l’aide d’une liaison sans serveur.


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



 

 




