---
title: L’utilisateur doit changer de mot de passe à la prochaine ouverture de session (fournisseur WinNT)
description: Pour activer cette option, affectez la valeur 1 à l’attribut PasswordExpired de l’utilisateur. L’affectation de la valeur zéro (0) à cet attribut permet à l’utilisateur de se connecter sans modifier le mot de passe.
ms.assetid: 97dd4232-dcd3-44bd-8a2a-1dcb0f85d53c
ms.tgt_platform: multiple
keywords:
- L’utilisateur doit changer de mot de passe à la prochaine ouverture de session (fournisseur WinNT) ADSI
- L’utilisateur doit changer de mot de passe à la prochaine ouverture de session ADSI, fournisseur Winnt
- ADSI Provider ADSI, exemples de gestion des utilisateurs, l’utilisateur doit changer de mot de passe à la prochaine ouverture de session
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be50e5cdccb4969e59a5b32516a35278b867062e8cced2e80d96b26c56c6173b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023037"
---
# <a name="user-must-change-password-at-next-logon-winnt-provider"></a>L’utilisateur doit changer de mot de passe à la prochaine ouverture de session (fournisseur WinNT)

Pour activer cette option, affectez la valeur 1 à l’attribut **PasswordExpired** de l’utilisateur. L’affectation de la valeur zéro (0) à cet attribut permet à l’utilisateur de se connecter sans modifier le mot de passe.

## <a name="example-1"></a>Exemple 1

l’exemple de code suivant montre comment définir l’option modifier le mot de passe lors de la prochaine ouverture de session à l’aide de Visual Basic avec ADSI.


```VB
Set usr = GetObject("WinNT://Fabrikam/jeffsmith,user")
usr.Put "PasswordExpired", CLng(1)   ' User must change password.
usr.SetInfo
```



## <a name="example-2"></a>Exemple 2

L’exemple de code suivant montre comment définir l’option modifier le mot de passe pour la prochaine ouverture de session à l’aide de C++ avec ADSI.


```C++
IADsUser *pUser = NULL;
HRESULT hr;

hr=ADsGetObject(L"WinNT://Fabrikam/jeffsmith,user",
                IID_IADsUser,
                (void**)&pUser);
VARIANT var;
VariantInit(&var);
V_I4(&var)=1;
V_VT(&var)=VT_I4;
hr = pUser->Put(_bstr_t("PasswordExpired"),var); // User must change password.
hr = pUser->SetInfo();

VariantClear(&var);
pUser->Release();
```



 

 




