---
title: Paramètres. invokeURLs
description: La propriété invokeURLs spécifie ou récupère une valeur indiquant si les événements d’URL doivent lancer un navigateur Web.
ms.assetid: 3a28d949-96b7-4c21-97c5-2442c2f7baa5
keywords:
- Paramètres. invokeURLs Lecteur Windows Media
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
ms.openlocfilehash: 75de25c5b4a18b6d53423657dc7180fe58cb095f3244800c2c42593d1d450e7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002401"
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



 

## <a name="remarks"></a>Remarques

Les fichiers multimédias peuvent contenir des URL. quand une URL est envoyée au contrôle Lecteur Windows Media, elle est passée en premier au gestionnaire d’événements **commande** , quelle que soit la valeur de **invokeURLs**. une fois **commande** se termine, Lecteur Windows Media vérifie **invokeURLs** pour déterminer s’il faut lancer le navigateur Internet par défaut avec l’URL. Vous pouvez afficher des URL de manière sélective en les vérifiant dans **commande** et en définissant **invokeURLs** comme vous le souhaitez.

**Lecteur Windows Media 10 Mobile**: cette propriété accepte ou retourne la valeur false uniquement.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Événement Player. commande**](player-player-scriptcommand.md)
</dt> <dt>

[**Paramètres Dessin**](settings-object.md)
</dt> </dl>

 

 





