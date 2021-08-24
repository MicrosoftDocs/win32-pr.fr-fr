---
title: External. Authenticate, méthode
description: La méthode Authenticate lance une tentative d’authentification de l’utilisateur.
ms.assetid: db4cd2c6-b735-40b1-af96-82a40bda9d97
keywords:
- méthode authenticate Lecteur Windows Media
- méthode authenticate Lecteur Windows Media, classe externe
- Lecteur Windows Media de classe externe, méthode authenticate
topic_type:
- apiref
api_name:
- External.authenticate
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b72c4d20cdd8232746175d966856a616bca9629657ca66c35727b8af8e21178
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649549"
---
# <a name="externalauthenticate-method"></a>External. Authenticate, méthode

La méthode **Authenticate** lance une tentative d’authentification de l’utilisateur.

## <a name="syntax"></a>Syntaxe


```JScript
External.authenticate(
  AuthenticationIndex
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*AuthenticationIndex* \[ dans\]
</dt> <dd>

**Nombre** (**long**) qui spécifie l’index d’une page Web d’authentification-réussite.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Certains liens sur une page de découverte ont des cibles qui ne doivent être affichées qu’une fois que l’utilisateur a été authentifié. la page détection, Lecteur Windows Media et le plug-in du magasin en ligne, utilisez les étapes suivantes pour authentifier l’utilisateur et afficher la page web cible :

1.  Un script sur une page de découverte appelle le *externe*. méthode **Authenticate** .
2.  Lecteur Windows Media affiche une boîte de dialogue pour obtenir un nom d’utilisateur et un mot de passe.
3.  Lecteur Windows Media appelle [IWMPContentPartner :: Authenticate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-authenticate), qui lance la tentative d’authentification et retourne immédiatement.
4.  Lorsque la tentative d’authentification est terminée, le plug-in du magasin en ligne appelle [IWMPContentPartnerCallback :: Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify), en passant wmpcnAuthResult et une valeur booléenne qui indique si la tentative a réussi.
5.  si la tentative d’authentification a réussi, Lecteur Windows Media appelle [IWMPContentPartner :: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo), en passant g \_ szItemInfo \_ AuthenticationSuccessURL, pour obtenir l’URL d’une page web d’authentification-réussite. dans cet appel, Lecteur Windows Media transmet le même index que la page de découverte transmise à l' *externe*. méthode **Authenticate** .
6.  Lecteur Windows Media affiche la page web de réussite de l’authentification.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet externe pour les magasins de type 1 en ligne**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. attemptLogin**](external-attemptlogin.md)
</dt> <dt>

[**External. userLoggedIn**](external-userloggedin.md)
</dt> </dl>

 

 





