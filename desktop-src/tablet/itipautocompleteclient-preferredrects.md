---
description: Permet au client de suggérer où placer la liste de saisie semi-automatique pour éviter le chevauchement du panneau de saisie.
ms.assetid: c82ffecb-f3e6-4c50-80bb-8393b39d3b2a
title: ITipAutocompleteClient ::P méthode referredRects (TipAutoComplete. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.PreferredRects
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: aa1fa4636b0302e058bc0a308e5d87da11d9bec3d12d678b9eb6057521479689
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119938589"
---
# <a name="itipautocompleteclientpreferredrects-method"></a>ITipAutocompleteClient ::P méthode referredRects

Permet au client de suggérer où placer la liste de saisie semi-automatique pour éviter le chevauchement du panneau de saisie.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT PreferredRects(
  [in]      RECT *prcACList,
  [in]      RECT *prcField,
  [out]     RECT *prcModified,
  [in, out] BOOL *pfShownAboveTip
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*prcACList* \[ dans\]
</dt> <dd>

Rectangle, en coordonnées d’écran, indiquant l’emplacement préféré du fournisseur et la taille de l’interface utilisateur de la liste de saisie semi-automatique.

</dd> <dt>

*prcField* \[ dans\]
</dt> <dd>

Rectangle, en coordonnées d’écran, indiquant l’emplacement et la taille du champ ayant le focus.

</dd> <dt>

*prcModified* \[ à\]
</dt> <dd>

Un rectangle basé sur l’état actuel de l’info-bulle et l’emplacement et la taille de la liste de saisie semi-automatique par défaut spécifiés par *prcACList*.

</dd> <dt>

*pfShownAboveTip* \[ in, out\]
</dt> <dd>

**True** si le rectangle modifié doit être affiché au-dessus de la zone cible du panneau de saisie du texte ; Sinon, **false**. Cette valeur doit être initialisée à l’orientation par défaut du fournisseur avant que la méthode ne soit appelée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                                  | Description                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Réussite.<br/>                                                                                                                                                                                                                                                            |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Appelez la [**méthode ITipAutocompleteClient :: RequestShowUI**](itipautocompleteclient-requestshowui.md) pour définir la fenêtre Liste de saisie semi-automatique des fenêtres contextuelles avant d’appeler la [**méthode ITipAutocompleteClient ::P referredrects**](itipautocompleteclient-preferredrects.md).<br/> |
| <dl> <dt>**E \_ échec**</dt> </dl>       | Une erreur non spécifiée s'est produite.<br/>                                                                                                                                                                                                                                      |



 

## <a name="remarks"></a>Remarques

Il s’agit de la méthode appelée par le fournisseur de saisie semi-automatique lorsqu’il est sur le présent d’afficher l’interface utilisateur de saisie semi-automatique. Le client modifie le rectangle préféré du fournisseur spécifié par *prcACList* à l’aide de l’argument *prcModified* .

Appelez la [**méthode ITipAutocompleteClient :: RequestShowUI**](itipautocompleteclient-requestshowui.md) pour définir le handle de fenêtre de la liste de saisie semi-automatique contextuelle avant d’appeler **PreferredRects**. Dans le cas contraire, une erreur d' **E \_ INVALIDARG** se produira lors de l’appel de **PreferredRects**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                                   |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                                       |
| En-tête<br/>                   | <dl> <dt>TipAutoComplete. h (nécessite également PenInputPanel \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface ITipAutocompleteClient**](itipautocompleteclient.md)
</dt> <dt>

[**ITipAutocompleteClient :: RequestShowUI, méthode**](itipautocompleteclient-requestshowui.md)
</dt> <dt>

[Référence du panneau de saisie de texte](text-input-panel-reference.md)
</dt> </dl>

 

 




