---
title: Player. lecture
description: La propriété lecture récupère une valeur indiquant l’état de l’opération du lecteur Windows Media.
ms.assetid: 8ed1ee1f-8731-402a-aff5-5ae513a35eea
keywords:
- Lecteur Windows Media Player. lecture
topic_type:
- apiref
api_name:
- Player.playState
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c442b1be9e1ea15b8a54c2dafc264edf8aeb479
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542347"
---
# <a name="playerplaystate"></a>Player. lecture

La propriété **lecture** récupère une valeur indiquant l’état de l’opération du lecteur Windows Media.

## <a name="syntax"></a>Syntaxe

*lecteur* . **lecture**

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est un **nombre** en lecture seule (**long**). La constante d’énumération de style C peut être dérivée en préfixant la valeur d’État avec « wmpps ». Par exemple, la constante pour l’état de jeu est **wmppsPlaying**.



| Valeur | State         | Description                                                                                                                 |
|-------|---------------|-----------------------------------------------------------------------------------------------------------------------------|
| 0     | Indéfini     | Le lecteur Windows Media est dans un État non défini.                                                                              |
| 1     | Arrêté       | La lecture de l’élément multimédia en cours est arrêtée.                                                                              |
| 2     | Suspendu        | La lecture de l’élément multimédia actuel est suspendue. Lorsqu’un élément multimédia est suspendu, la reprise de la lecture commence à partir du même emplacement. |
| 3     | Lecture en cours       | L’élément multimédia actuel est en cours de diffusion.                                                                                          |
| 4     | ScanForward   | L’élément multimédia actuel est un transfert rapide.                                                                                  |
| 5     | ScanReverse   | L’élément multimédia actuel est un rembobinage rapide.                                                                                   |
| 6     | des réponses     | L’élément multimédia actuel reçoit des données supplémentaires à partir du serveur.                                                          |
| 7     | En attente       | La connexion est établie, mais le serveur n’envoie pas de données. En attente du début de la session.                                |
| 8     | MediaEnded    | La lecture de l’élément multimédia est terminée.                                                                                          |
| 9     | Transition | Préparation du nouvel élément multimédia.                                                                                                   |
| 10    | Ready         | Prêt à commencer la lecture.                                                                                                     |
| 11    | La reconnexion  | Reconnexion au flux.                                                                                                     |



 

## <a name="remarks"></a>Notes

Il n’est pas garanti que les États du lecteur Windows Media se produisent dans un ordre particulier. En outre, tous les États ne se produisent pas nécessairement au cours d’une séquence d’événements. Vous ne devez pas écrire du code qui s’appuie sur l’ordre de l’État.

## <a name="examples"></a>Exemples

Le code JScript suivant illustre l’utilisation du *lecteur*. propriété **lecture** . Un élément de texte HTML, nommé « myText », affiche l’état actuel. L’objet **Player** a été créé avec ID = "Player".


```JScript
// Test whether Windows Media Player is in the playing state.
if (3 == Player.playState)
    myText.value = "Windows Media Player is playing!";
else
    myText.value = "Windows Media Player is NOT playing!";
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet Player**](player-object.md)
</dt> <dt>

[**Événement Player. PlayStateChange**](player-player-playstatechange.md)
</dt> </dl>

 

 





