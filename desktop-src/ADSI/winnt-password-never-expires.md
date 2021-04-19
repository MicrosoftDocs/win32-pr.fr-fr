---
title: Le mot de passe n’expire jamais (fournisseur WinNT)
description: Pour activer cette option à l’aide du fournisseur ADSI WinNT, définissez l' \_ indicateur ADS UF \_ \_ nopirer \_ passwd (0x10000) sur l’attribut userFlags. Remarque pour Windows 2000 et versions ultérieures, utilisez le fournisseur ADSI LDAP pour les opérations de gestion des utilisateurs, comme indiqué.
ms.assetid: 9e38b31c-399b-447f-bceb-36c599b2714e
ms.tgt_platform: multiple
keywords:
- Le mot de passe n’expire jamais (fournisseur WinNT)
- Le mot de passe n’expire jamais ADSI, le fournisseur Winnt
- ADSI Provider ADSI, exemples de gestion des utilisateurs, mot de passe n’expire jamais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 343871e7ba8748b3e406f7c84a5a34c01a2793a7
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2021
ms.locfileid: "106538309"
---
# <a name="password-never-expires-winnt-provider"></a>Le mot de passe n’expire jamais (fournisseur WinNT)

Pour activer cette option à l’aide du fournisseur ADSI WinNT, définissez l’indicateur **ADS \_ UF \_ \_ nopirer \_ passwd** (0x10000) sur l’attribut **userFlags** .

> [!Note]  
> Pour Windows 2000 et versions ultérieures, utilisez le fournisseur ADSI LDAP pour les opérations de gestion des utilisateurs, comme indiqué. Pour plus d’informations, consultez [mot de passe n’expire jamais (fournisseur LDAP)](password-never-expires.md).

 

## <a name="example-1"></a>Exemple 1

L’exemple de code suivant montre comment définir l’option le mot de passe n’expire jamais à l’aide de Visual Basic avec ADSI.


```VB
Const ADS_UF_DONT_EXPIRE_PASSWD = &H10000
Dim usr as IADs

Set usr = GetObject("WinNT://Fabrikam/JeffSmith")
oldFlags = usr.Get("UserFlags")
newFlags = oldFlags Or ADS_UF_DONT_EXPIRE_PASSWD
usr.Put "UserFlags", newFlags
usr.SetInfo
```



## <a name="example-2"></a>Exemple 2

L’exemple de code suivant montre comment définir l’option le mot de passe n’expire jamais à l’aide de C++ avec ADSI.


```C++
#include <activeds.h>

IADsUser *pUser = NULL;
VARIANT var;
VariantInit(&var);

HRESULT hr = S_OK;
LPWSTR adsPath;
adsPath = L"WinNT://Fabrikam/JeffSmith";
hr = ADsGetObject(adsPath,IID_IADsUser, (void**)&pUser);

CComBSTR sbstrUserFlags = "UserFlags";
hr = pUser->Get(sbstrUserFlags, &var);

V_I4(&var) |= ADS_UF_DONT_EXPIRE_PASSWD;
hr = pUser->Put(sbstrUserFlags, var);

hr = pUser->SetInfo();

VariantClear(&var);

pUser->Release();
```



 

 




