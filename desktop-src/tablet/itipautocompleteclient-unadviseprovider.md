---
description: Annule l’inscription du fournisseur associé.
ms.assetid: b5edc33d-dfd0-4350-b8cd-eaa30b726771
title: 'ITipAutocompleteClient :: UnadviseProvider, méthode (TipAutoComplete. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.UnadviseProvider
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: d4f573e1dab88e8556dc8c6011173cd3a2284a87d9f98ac6d05cea13cef65ab8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712099"
---
# <a name="itipautocompleteclientunadviseprovider-method"></a>ITipAutocompleteClient :: UnadviseProvider, méthode

Annule l’inscription du fournisseur associé.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT UnadviseProvider(
  [in] HWND                   hWndField,
  [in] ITipAutocompleProvider *pIACProvider
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hWndField* \[ dans\]
</dt> <dd>

Handle de fenêtre du champ qui fournit la fonctionnalité de saisie semi-automatique.

</dd> <dt>

*pIACProvider* \[ dans\]
</dt> <dd>

Pointeur d’interface vers l’interface du fournisseur de saisie semi-automatique dont l’inscription doit être annulée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                            | Description                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>   | Réussite.<br/>                       |
| <dl> <dt>**E \_ échec**</dt> </dl> | Une erreur non spécifiée s'est produite.<br/> |



 

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

[Référence du panneau de saisie de texte](text-input-panel-reference.md)
</dt> </dl>

 

 




