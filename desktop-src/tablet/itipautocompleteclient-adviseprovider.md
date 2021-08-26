---
description: Inscrit le fournisseur auprès du client pour permettre au client d’appeler l’objet fournisseur de saisie semi-automatique de l’application.
ms.assetid: 7b761b30-66f7-454a-9e0d-f45c8099f19f
title: 'ITipAutocompleteClient :: AdviseProvider, méthode (TipAutoComplete. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.AdviseProvider
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: dd48cdfbf35c5132b42f8185cdc93f53ec34c77df78a51d16da9fa5a5311c144
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119938579"
---
# <a name="itipautocompleteclientadviseprovider-method"></a>ITipAutocompleteClient :: AdviseProvider, méthode

Inscrit le fournisseur auprès du client pour permettre au client d’appeler l’objet fournisseur de saisie semi-automatique de l’application.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT AdviseProvider(
  [in] HWND                     hWndField,
  [in] ITipAutocompleteProvider *pIACProvider
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

Pointeur d’interface vers l’interface du fournisseur de saisie semi-automatique.

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

[**ITipAutocompleteClient :: UnadviseProvider, méthode**](itipautocompleteclient-unadviseprovider.md)
</dt> <dt>

[Référence du panneau de saisie de texte](text-input-panel-reference.md)
</dt> </dl>

 

 




