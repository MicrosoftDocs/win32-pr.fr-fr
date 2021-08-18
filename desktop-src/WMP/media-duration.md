---
title: Media. Duration
description: La propriété Duration récupère, en secondes, la durée de l’élément multimédia actuel.
ms.assetid: d7d36858-812d-471b-84ce-fe2ab96b86b3
keywords:
- Media. duration Lecteur Windows Media
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
ms.openlocfilehash: e89eab1ffbb8c9f3d48c3f61eb6d831af66b4931ed1d858658eed3fc21d08183
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118118799"
---
# <a name="mediaduration"></a>Media. Duration

La propriété **Duration** récupère, en secondes, la durée de l’élément multimédia actuel.

## <a name="syntax"></a>Syntaxe

*lecteur*. *currentMedia*. **durée**

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est un **nombre** en lecture seule ( **double**).

## <a name="remarks"></a>Remarques

Si cette propriété est utilisée avec un élément multimédia autre que celui spécifié dans le *lecteur*. **currentMedia**, il ne peut pas contenir une valeur valide.

pour récupérer la durée des fichiers qui ne sont pas dans la bibliothèque de l’utilisateur, vous devez attendre que Lecteur Windows Media ouvre le fichier ; autrement dit, le OpenState actuel doit être égal à MediaOpen. Vous pouvez le vérifier en gérant le *lecteur*. Événement **OpenStateChange** ou en vérifiant régulièrement la valeur de *Player*. **openState**.

Pour les sélections, la durée de chaque élément multimédia peut être récupérée lors de l’ouverture de l’élément multimédia individuel, plutôt que lors de l’ouverture de la sélection.

Pour récupérer la valeur de cette propriété, l’accès en lecture à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

l’exemple de JScript suivant utilise un *média*. **durée** d’affichage de l’heure restante dans l’élément multimédia actuel. Un élément DIV HTML nommé RemTime affiche les informations. Un minuteur HTML met à jour le texte de l’élément DIV chaque seconde.

le code JScript suivant démarre le minuteur :


```JScript
// Execute the update() function at one-second intervals.
idTmr = window.setInterval("update()",1000);
```



le code JScript suivant arrête le minuteur :


```JScript
window.clearInterval(idTmr);
```



Utilisez le *lecteur*. Événement **PlayStateChange** avec une instruction **switch** pour déterminer quand démarrer et arrêter le minuteur.

le code JScript suivant s’exécute chaque fois que la minuterie appelle la fonction de mise à jour :


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

 

 





