---
description: Affiche ou masque la liste de saisie semi-automatique.
ms.assetid: 756ffa3d-03ee-4753-a826-3bc22ab16f5f
title: 'ITipAutocompleteProvider :: Show, méthode (TipAutoComplete. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteProvider.Show
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 2afc5fc264df4d38e85dfa3374714b06908eee8ec1c5517b49dc32cbcbd44f99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118716449"
---
# <a name="itipautocompleteprovidershow-method"></a>ITipAutocompleteProvider :: Show, méthode

Affiche ou masque la liste de saisie semi-automatique.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Show(
  [in] BOOL fShow
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*fShow* \[ dans\]
</dt> <dd>

**True** pour afficher l’interface utilisateur de saisie semi-automatique, **false** pour masquer l’interface utilisateur de la liste de saisie semi-automatique.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                            | Description                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>   | Réussite.<br/>                       |
| <dl> <dt>**E \_ échec**</dt> </dl> | Une erreur non spécifiée s'est produite.<br/> |



 

## <a name="remarks"></a>Remarques

Cette méthode est appelée par le client pour afficher ou masquer la liste de saisie semi-automatique. Si la liste de saisie semi-automatique n’est pas affichée et que *fShow* a la **valeur false**, cette méthode n’a aucun effet. Si la liste de saisie semi-automatique est affichée et que *fShow* a la **valeur true**, cette méthode n’a aucun effet.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                                   |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                                       |
| En-tête<br/>                   | <dl> <dt>TipAutoComplete. h (nécessite également PenInputPanel \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface ITipAutocompleteProvider**](itipautocompleteprovider.md)
</dt> <dt>

[Référence du panneau de saisie de texte](text-input-panel-reference.md)
</dt> </dl>

 

 




