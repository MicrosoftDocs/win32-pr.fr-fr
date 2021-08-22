---
description: Gère le côté de l’application de l’intégration de la saisie semi-automatique du panneau de saisie de texte.
ms.assetid: 02601258-d867-4c01-b094-bf9ff96d2f6e
title: Interface ITipAutocompleteProvider (TipAutoComplete. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteProvider
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 66c1e38c419e7eb37745864b447249d55b384b6c832293bd3fab4d0cc171e0fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119031867"
---
# <a name="itipautocompleteprovider-interface"></a>Interface ITipAutocompleteProvider

Gère le côté de l’application de l’intégration de la saisie semi-automatique du panneau de saisie de texte.

## <a name="members"></a>Membres

L’interface **ITipAutocompleteProvider** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITipAutocompleteProvider** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ITipAutocompleteProvider** possède ces méthodes.



| Méthode                                                                  | Description                                                                                                          |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**Afficher**](itipautocompleteprovider-show.md)                           | Affiche ou masque la liste de saisie semi-automatique.<br/>                                                                 |
| [**UpdatePendingText**](itipautocompleteprovider-updatependingtext.md) | Utilisé par le client de saisie semi-automatique pour notifier l’application du texte qu’un utilisateur a inséré dans le panneau de saisie.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                                   |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                                       |
| En-tête<br/>                   | <dl> <dt>TipAutoComplete. h (nécessite également PenInputPanel \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Référence du panneau de saisie de texte](text-input-panel-reference.md)
</dt> <dt>

[**Interface ITipAutocompleteClient**](itipautocompleteclient.md)
</dt> </dl>

 

