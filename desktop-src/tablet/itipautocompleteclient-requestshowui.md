---
description: Détermine si le panneau de saisie est prêt à afficher la liste de saisie semi-automatique.
ms.assetid: 1e0d4bc6-e6a3-4123-a381-00a41ed9c848
title: 'ITipAutocompleteClient :: RequestShowUI, méthode (TipAutoComplete. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.RequestShowUI
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: e547376bf2e9c50c224d1917e00329e8d9555e6d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127530292"
---
# <a name="itipautocompleteclientrequestshowui-method"></a>ITipAutocompleteClient :: RequestShowUI, méthode

Détermine si le panneau de saisie est prêt à afficher la liste de saisie semi-automatique.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT RequestShowUI(
  [in]  HWND hWndACList,
  [out] BOOL *pfAllowShowing
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hWndACList* \[ dans\]
</dt> <dd>

Handle de fenêtre de l’interface utilisateur de la liste de saisie semi-automatique.

</dd> <dt>

*pfAllowShowing* \[ à\]
</dt> <dd>

**False** si le client recommande de ne pas afficher l’interface utilisateur de la liste de saisie semi-automatique. **True** si le fournisseur de saisie semi-automatique peut afficher l’interface utilisateur de la liste.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                            | Description                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>   | Réussite.<br/>                       |
| <dl> <dt>**E \_ échec**</dt> </dl> | Une erreur non spécifiée s'est produite.<br/> |



 

## <a name="remarks"></a>Notes

Cette méthode est appelée par le fournisseur de saisie semi-automatique lorsqu’il est sur le présent d’afficher l’interface utilisateur de saisie semi-automatique. Si l’état interne du client n’autorise pas le fournisseur à afficher l’interface utilisateur, *pfAllowShowing* est défini sur **false**. Par exemple, lorsque le texte est envoyé au champ à partir de l’apparence de l’écriture manuscrite dans le panneau de saisie Tablet PC et que l’utilisateur commence immédiatement l’entrée manuscrite, le client recommande de ne pas afficher l’interface utilisateur de saisie semi-automatique, afin d’éviter la destruction de l’entrée de l’utilisateur, en affectant à *pfAllowShowing* la **valeur false**.

Appelez **RequestShowUI** pour définir le handle de fenêtre de la liste de saisie semi-automatique contextuelle avant d’appeler la [**méthode ITipAutocompleteClient ::P referredrects**](itipautocompleteclient-preferredrects.md). Dans le cas contraire, une erreur d' **E \_ INVALIDARG** se produira lors de l’appel de **PreferredRects**.

## <a name="requirements"></a>Spécifications



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

[**ITipAutocompleteClient ::P méthode referredRects**](itipautocompleteclient-preferredrects.md)
</dt> <dt>

[Référence du panneau de saisie de texte](text-input-panel-reference.md)
</dt> </dl>

 

 




