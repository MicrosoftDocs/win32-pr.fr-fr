---
description: Permet au client d’appeler l’objet fournisseur de saisie semi-automatique du panneau de saisie du texte de l’application.
ms.assetid: 448b8136-ebcb-4116-9a81-a77a37d69e24
title: Interface ITipAutocompleteClient (TipAutoComplete. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 7b9dad38d0e3f169019934b7e60a09096aced1b9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127530284"
---
# <a name="itipautocompleteclient-interface"></a>Interface ITipAutocompleteClient

Permet au client d’appeler l’objet fournisseur de saisie semi-automatique du panneau de saisie du texte de l’application.

## <a name="members"></a>Membres

L’interface **ITipAutocompleteClient** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITipAutocompleteClient** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ITipAutocompleteClient** possède ces méthodes.



| Méthode                                                              | Description                                                                                                                                                          |
|:--------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdviseProvider**](itipautocompleteclient-adviseprovider.md)     | Inscrit le fournisseur auprès du client pour permettre au client d’appeler l’objet fournisseur de saisie semi-automatique de l’application.<br/>                                      |
| [**PreferredRects**](itipautocompleteclient-preferredrects.md)     | Permet au client de suggérer où placer la liste de saisie semi-automatique pour éviter le chevauchement du panneau de saisie.<br/>                                               |
| [**RequestShowUI**](itipautocompleteclient-requestshowui.md)       | Détermine si le panneau de saisie est prêt à afficher la liste de saisie semi-automatique.<br/>                                                                             |
| [**UnadviseProvider**](itipautocompleteclient-unadviseprovider.md) | Annule l’inscription du fournisseur associé.<br/>                                                                                                                      |
| [**UserSelection**](itipautocompleteclient-userselection.md)       | Notifie le panneau de saisie que l’utilisateur a sélectionné un nom dans la liste de saisie semi-automatique et qu’il ignore tout le texte restant qui n’a pas encore été inséré.<br/> |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                                   |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                                       |
| En-tête<br/>                   | <dl> <dt>TipAutoComplete. h (nécessite également PenInputPanel \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



 

