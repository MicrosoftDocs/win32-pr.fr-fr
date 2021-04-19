---
title: Media. Duration
description: La propriété Duration récupère, en secondes, la durée de l’élément multimédia actuel.
ms.assetid: d7d36858-812d-471b-84ce-fe2ab96b86b3
keywords:
- Media. Duration Windows Media Player
topic_type:
- apiref
api_name:
- Media.duration
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71586f6aa37401d56a9e9537bfbea6c5af23f318
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529961"
---
# <a name="mediaduration"></a>Media. Duration

La propriété **Duration** récupère, en secondes, la durée de l’élément multimédia actuel.

## <a name="syntax"></a>Syntaxe

*lecteur*. *currentMedia*. **durée**

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est un **nombre** en lecture seule ( **double**).

## <a name="remarks"></a>Notes

Si cette propriété est utilisée avec un élément multimédia autre que celui spécifié dans le *lecteur*. **currentMedia**, il ne peut pas contenir une valeur valide.

Pour récupérer la durée des fichiers qui ne sont pas dans la bibliothèque de l’utilisateur, vous devez attendre que le lecteur Windows Media ouvre le fichier. autrement dit, le OpenState actuel doit être égal à MediaOpen. Vous pouvez le vérifier en gérant le *lecteur*. Événement **OpenStateChange** ou en vérifiant régulièrement la valeur de *Player*. **openState**.

Pour les sélections, la durée de chaque élément multimédia peut être récupérée lors de l’ouverture de l’élément multimédia individuel, plutôt que lors de l’ouverture de la sélection.

Pour récupérer la valeur de cette propriété, l’accès en lecture à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

L’exemple JScript suivant utilise un *média*. **durée** d’affichage de l’heure restante dans l’élément multimédia actuel. Un élément DIV HTML nommé RemTime affiche les informations. Un minuteur HTML met à jour le texte de l’élément DIV chaque seconde.

Le code JScript suivant démarre le minuteur :


```JScript
// Execute the update() function at one-second intervals.
idTmr = window.setInterval("update()",1000);
```



Le code JScript suivant arrête le minuteur :


```JScript
window.clearInterval(idTmr);
```



Utilisez le *lecteur*. Événement **PlayStateChange** avec une instruction **switch** pour déterminer quand démarrer et arrêter le minuteur.

Le code JScript suivant s’exécute chaque fois que la minuterie appelle la fonction de mise à jour :


```JScript
// Store the current position of the current media item.
var TimeNow = Player.controls.currentPosition;

// Display the time remaining information.
RemTime.innerHTML = "Seconds remaining: ";

// Subtract the current position from the duration of the current media.
// Use the Math.floor method to round the result down to the nearest integer.
RemTime.innerHTML += Math.floor(Player.currentMedia.duration - TimeNow);
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet Media**](media-object.md)
</dt> <dt>

[**Player. currentMedia**](player-currentmedia.md)
</dt> <dt>

[**Événement Player. PlayStateChange**](player-player-playstatechange.md)
</dt> <dt>

[**Paramètres. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Paramètres. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





