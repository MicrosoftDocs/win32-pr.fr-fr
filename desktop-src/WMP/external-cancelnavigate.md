---
title: External. cancelNavigate, méthode
description: Remarque Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. | External. cancelNavigate, méthode
ms.assetid: e65d64fb-292c-4413-9727-b24609e78d68
keywords:
- Lecteur Windows Media de la méthode cancelNavigate
- méthode cancelNavigate Lecteur Windows Media, classe externe
- Lecteur Windows Media de classe externe, méthode cancelNavigate
topic_type:
- apiref
api_name:
- External.cancelNavigate
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 152594a427282a27c493f33f648b8a889a855f40a5fb13de69b7cc342099eed2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649429"
---
# <a name="externalcancelnavigate-method"></a>External. cancelNavigate, méthode

> [!Note]  
> Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

la méthode **cancelNavigate** informe Lecteur Windows Media qu’elle ne doit pas afficher une nouvelle page de découverte, même si la vue a été modifiée dans le lecteur.

## <a name="syntax"></a>Syntaxe


```JScript
External.cancelNavigate()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

lorsque la vue change dans Lecteur Windows Media, le lecteur appelle le plug-in du magasin en ligne pour déterminer quelle page de découverte afficher ensuite. Dans certains cas, toutefois, le magasin en ligne peut souhaiter que le lecteur continue à afficher la page de découverte existante. Le processus suivant détermine si le lecteur affiche une nouvelle page de découverte :

1.  Une action de l’utilisateur, que ce soit dans l’interface utilisateur du joueur ou sur la page de découverte, demande que le joueur modifie son affichage.
2.  Le lecteur appelle la méthode [GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) du plug-in pour déterminer quelle page de découverte afficher ensuite. Le lecteur stocke l’URL de la nouvelle page de découverte, mais n’affiche pas la nouvelle page de découverte pour l’instant.
3.  Le lecteur déclenche l’événement [OnViewChange](external-onviewchange-event.md) .
4.  Si le gestionnaire d’événements **OnViewChange** sur la page de découverte appelle **CancelNavigate**, le lecteur n’affiche pas la page nouvelle détection (déterminée à l’étape 2). Au lieu de cela, il continue d’afficher la page découverte existante. Si le gestionnaire d’événements **OnViewChange** n’appelle pas **CancelNavigate**, le lecteur affiche la page nouvelle détection.

Supposons, par exemple, que le joueur affiche actuellement la vue d’un album avec une certaine piste sélectionnée. Supposons également que la page détection en cours est la page qui représente l’intégralité de l’album. Si l’utilisateur clique sur une autre piste du même album, la vue du joueur change légèrement pour montrer que la nouvelle piste est sélectionnée. Mais il n’est pas nécessaire d’afficher une nouvelle page de découverte. La page de découverte qui représente l’intégralité de l’album est toujours la page appropriée à afficher par le lecteur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet externe pour les magasins de type 1 en ligne**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. changeViewOnlineList**](external-changeviewonlinelist.md)
</dt> <dt>

[**External. OnViewChange**](external-onviewchange-event.md)
</dt> </dl>

 

 





