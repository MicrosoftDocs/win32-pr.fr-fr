---
title: Le mot de passe n’expire jamais (fournisseur LDAP)
description: Pour activer l’option le mot de passe n’expire jamais à l’aide du fournisseur LDAP, définissez l’indicateur ad uf ne pas faire \_ \_ \_ expirer \_ passwd sur l’attribut userAccountControl de l’utilisateur.
ms.assetid: b8d7e7fe-c846-45c4-9c5f-770530453836
ms.tgt_platform: multiple
keywords:
- Le mot de passe n’expire jamais ADSI, fournisseur LDAP
- ADSI Provider ADSI, exemples de gestion des utilisateurs, mot de passe n’expire jamais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94c0d9eb42d37c1bcc7d65495fa0d72609060407
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104382851"
---
# <a name="password-never-expires-ldap-provider"></a>Le mot de passe n’expire jamais (fournisseur LDAP)

Pour activer l’option le mot de passe n’expire jamais à l’aide du fournisseur LDAP, définissez l’indicateur ad uf ne pas faire [**\_ \_ \_ expirer \_ passwd**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum) sur l’attribut [**UserAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol) de l’utilisateur.


```VB
Const ADS_UF_DONT_EXPIRE_PASSWD = &H10000

Set usr = GetObject("LDAP://CN=jeffsmith,OU=Sales,DC=Fabrikam,DC=Com")
flag = usr.Get("userAccountControl")
newFlag = flag Or ADS_UF_DONT_EXPIRE_PASSWD
usr.Put "userAccountControl", newFlag
usr.SetInfo
```




```C++
#include <activeds.h>

IADsUser *pUser;
VARIANT var;
VariantInit(&var);

HRESULT hr = S_OK;
LPWSTR adsPath = L"LDAP://serv1/cn=Jeff Smith,cn=Users,dc=Fabrikam,dc=com";
hr = ADsGetObject(adsPath, IID_IADsUser, (void**)&pUser);

hr = pUser->Get(_bstr_t("userAccountControl"), &var);

V_I4(&var) |= ADS_UF_DONT_EXPIRE_PASSWD;
hr = pUser->Put(_bstr_t("userAccountControl"), var);

hr = pUser->SetInfo();
VariantClear(&var);
hr = pUser->Release();
```



 

 