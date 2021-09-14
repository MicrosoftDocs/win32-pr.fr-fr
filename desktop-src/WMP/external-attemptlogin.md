---
title: External. attemptLogin, méthode
description: La méthode attemptLogin affiche une boîte de dialogue qui permet à l’utilisateur d’essayer de se connecter au magasin en ligne.
ms.assetid: 04fe476f-6d0e-4faa-9e4a-f87bed782205
keywords:
- Lecteur Windows Media de la méthode attemptLogin
- méthode attemptLogin Lecteur Windows Media, classe externe
- Lecteur Windows Media de classe externe, méthode attemptLogin
topic_type:
- apiref
api_name:
- External.attemptLogin
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86958c241f2399efbe342371b8cd4cfd376ff628
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127191728"
---
# <a name="externalattemptlogin-method"></a>External. attemptLogin, méthode

La méthode **attemptLogin** affiche une boîte de dialogue qui permet à l’utilisateur d’essayer de se connecter au magasin en ligne.

## <a name="syntax"></a>Syntaxe


```JScript
External.attemptLogin()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

si la tentative de connexion entraîne une modification de l’état de la connexion, Lecteur Windows Media déclenche l’événement [OnLoginChange](external-onloginchange-event.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet externe pour les magasins de type 1 en ligne**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. OnLoginChange, événement**](external-onloginchange-event.md)
</dt> <dt>

[**External. userLoggedIn**](external-userloggedin.md)
</dt> <dt>

[**IWMPContentPartner :: login**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-login)
</dt> <dt>

[**Gestion de la connexion**](managing-login.md)
</dt> </dl>

 

 





