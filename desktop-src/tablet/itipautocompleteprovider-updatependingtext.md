---
description: Utilisé par le client de saisie semi-automatique pour notifier l’application du texte qu’un utilisateur a inséré dans le panneau de saisie.
ms.assetid: 68413836-321a-4e75-8538-c5a8fc577c0f
title: 'ITipAutocompleteProvider :: UpdatePendingText, méthode (TipAutoComplete. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteProvider.UpdatePendingText
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 5c66e625639aa7088b1b3934a2f984d0f4097536
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042828"
---
# <a name="itipautocompleteproviderupdatependingtext-method"></a>ITipAutocompleteProvider :: UpdatePendingText, méthode

Utilisé par le client de saisie semi-automatique pour notifier l’application du texte qu’un utilisateur a inséré dans le panneau de saisie.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT UpdatePendingText(
  [in] BSTR bstrPendingText
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrPendingText* \[ dans\]
</dt> <dd>

Texte source à utiliser pour générer la liste de saisie semi-automatique.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                            | Description                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>   | Opération réussie.<br/>                       |
| <dl> <dt>**E \_ échec**</dt> </dl> | Une erreur non spécifiée s'est produite.<br/> |



 

## <a name="remarks"></a>Notes

Ce texte ne contient pas le texte déjà inséré dans le champ ayant le focus. Le fournisseur de saisie semi-automatique est chargé de tenir compte du texte du champ actuel et de la sélection pour générer la liste de saisie semi-automatique. Quand *bstrPendingText* a la **valeur null**, la liste de saisie semi-automatique est générée avec le texte actuel à gauche de la sélection dans le champ.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                                                                   |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                                       |
| En-tête<br/>                   | <dl> <dt>TipAutoComplete. h (nécessite également PenInputPanel \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface ITipAutocompleteProvider**](itipautocompleteprovider.md)
</dt> <dt>

[Référence du panneau de saisie de texte](text-input-panel-reference.md)
</dt> </dl>

 

 




