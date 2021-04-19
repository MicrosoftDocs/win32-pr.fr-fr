---
title: Paramètres. invokeURLs
description: La propriété invokeURLs spécifie ou récupère une valeur indiquant si les événements d’URL doivent lancer un navigateur Web.
ms.assetid: 3a28d949-96b7-4c21-97c5-2442c2f7baa5
keywords:
- Settings. invokeURLs Windows Media Player
topic_type:
- apiref
api_name:
- Settings.invokeURLs
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb55bb61243e6905a51a943a26adc120511335c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535963"
---
# <a name="settingsinvokeurls"></a>Paramètres. invokeURLs

La propriété **invokeURLs** spécifie ou récupère une valeur indiquant si les événements d’URL doivent lancer un navigateur Web.

## <a name="syntax"></a>Syntaxe

Player. Settings. invokeURLs

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est une **valeur booléenne** en lecture/écriture.



| Valeur | Description                                  |
|-------|----------------------------------------------|
| true  | Par défaut. Les événements d’URL doivent lancer un navigateur. |
| false | Les événements d’URL ne doivent pas lancer de navigateur.      |



 

## <a name="remarks"></a>Notes

Les fichiers multimédias peuvent contenir des URL. Quand une URL est envoyée au contrôle du lecteur Windows Media, elle est d’abord transmise au gestionnaire d’événements **commande** , quelle que soit la valeur de **invokeURLs**. Après la sortie de **commande** , le lecteur Windows Media vérifie **invokeURLs** pour déterminer s’il faut lancer le navigateur Internet par défaut avec l’URL. Vous pouvez afficher des URL de manière sélective en les vérifiant dans **commande** et en définissant **invokeURLs** comme vous le souhaitez.

**Windows Media Player 10 Mobile**: cette propriété accepte ou retourne la valeur false uniquement.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Événement Player. commande**](player-player-scriptcommand.md)
</dt> <dt>

[**Settings (objet)**](settings-object.md)
</dt> </dl>

 

 





