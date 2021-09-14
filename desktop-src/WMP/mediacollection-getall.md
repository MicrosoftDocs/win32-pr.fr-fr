---
title: MediaCollection. getAll, méthode
description: La méthode getAll récupère une sélection contenant tous les éléments multimédias de la bibliothèque.
ms.assetid: c22532ee-5714-4762-966f-7dc6543384f4
keywords:
- getAll, méthode Lecteur Windows Media
- getAll, méthode Lecteur Windows Media, classe MediaCollection
- MediaCollection, classe Lecteur Windows Media, getAll, méthode
topic_type:
- apiref
api_name:
- MediaCollection.getAll
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1681cd533be4084123cb80cdcc199ab5e1ce2981
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008385"
---
# <a name="mediacollectiongetall-method"></a>MediaCollection. getAll, méthode

La méthode **GetAll** récupère une sélection contenant tous les éléments multimédias de la bibliothèque.

## <a name="syntax"></a>Syntaxe


```JScript
retVal = MediaCollection.getAll()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Cette méthode retourne un objet **playlist** .

## <a name="remarks"></a>Notes

Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

## <a name="examples"></a>Exemples

l’exemple de JScript suivant utilise *MediaCollection*. **GetAll** pour lire des éléments multimédias de manière aléatoire à partir de la collection de médias. L’objet **Player** a été créé avec ID = "Player".


```JScript
// Store the count of all media items in the media collection.
var count = Player.mediaCollection.getAll().count;

// Generate a random number using the media count.
var rand = Math.random() * count;

// Round down the random number to the nearest integer.
rand = Math.floor(rand);

// Make the random media item the current media item.
Player.currentMedia = Player.mediaCollection.getAll().item(rand);

// Play the media item.
// Player.controls.play();

```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**Objet playlist**](playlist-object.md)
</dt> <dt>

[**Paramètres. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Paramètres. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





