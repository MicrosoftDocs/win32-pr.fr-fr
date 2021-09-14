---
title: External. OnLoginChange, événement
description: Remarque Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. | External. OnLoginChange, événement
ms.assetid: 096794d5-977a-414f-8a98-b7998674c268
keywords:
- Lecteur Windows Media d’événements External. OnLoginChange
topic_type:
- apiref
api_name:
- External.OnLoginChange Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b7d54da86ffdde896a44580567b0cd381725d5e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127192352"
---
# <a name="externalonloginchange-event"></a>External. OnLoginChange, événement

> [!Note]  
> Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

L’événement **OnLoginChange** se produit lorsque l’état de la connexion de l’utilisateur change ou lorsqu’une tentative de connexion échoue.

``` syntax
window.external.OnLoginChange = FunctionName
```

## <a name="possible-values"></a>Valeurs possibles

il s’agit d’une propriété en écriture seule qui spécifie le nom de la fonction dans le script que Lecteur Windows Media appelle lorsque l’événement se produit.

## <a name="parameters"></a>Paramètres

La fonction qui gère cet événement n’accepte aucun paramètre.

## <a name="remarks"></a>Notes

Cet événement se produit chaque fois que le plug-in du magasin en ligne appelle [IWMPContentPartnerCallback :: Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify), en passant wmpcnLoginStateChange dans le paramètre de *type* . parfois, le plug-in effectue cet appel pour notifier Lecteur Windows Media qu’une modification a été apportée à l’état de connexion de l’utilisateur. Dans d’autres cas, le plug-in effectue cet appel pour informer le joueur qu’une tentative de connexion a échoué. Le paramètre *pContext* de la méthode **Notify** spécifie si la notification est destinée à un changement d’état de connexion ou à une tentative d’ouverture de session qui a échoué.

étant donné que chaque appel à `Notify(wmpcnLoginStateChange, ...)` amène Lecteur Windows Media à déclencher l’événement **OnLoginChange** , le gestionnaire d’événements **OnLoginChange** est parfois appelé à la suite d’une modification de l’état de connexion et parfois à la suite d’un échec de tentative de connexion. Pour déterminer l’état actuel de la connexion de l’utilisateur, le gestionnaire d’événements **OnLoginChange** doit appeler [External. userLoggedIn](external-userloggedin.md).

## <a name="requirements"></a>Spécifications



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

 

 





