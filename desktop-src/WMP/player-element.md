---
title: Élément PLAYER
description: Élément PLAYER
ms.assetid: 009090b3-0055-4700-9078-0749da239674
keywords:
- Apparences du lecteur Windows Media, élément lecteur
- Skins, élément PLAYER
- Élément PLAYER
- informations de référence sur les habillages, élément PLAYER
- éléments, joueur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a50eb4383eab279c28b75467a9ed803501e7720b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100757"
---
# <a name="player-element"></a>Élément PLAYER

L’élément **Player** vous permet de définir des gestionnaires d’événements et de spécifier la propriété **URL** de l’objet **Player** au moment du design au sein d’un fichier de définition d’apparence. Dans le code de script, l’objet **Player** est accessible par le biais de l’attribut global **Player** plutôt que via un nom spécifié par un attribut **ID** , ce qui n’est pas pris en charge par l’élément **Player** .

L’élément **Player** prend en charge l’attribut suivant.



| Attribut             | Description                                          |
|-----------------------|------------------------------------------------------|
| [URL](player-url.md) | Spécifie ou récupère le nom du fichier à lire. |



 

L’élément **Player** peut implémenter des gestionnaires d’événements pour les événements suivants déclenchés à partir de l’objet **Player** .



| Événement                                                                                            | Description                                                                      |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [AudioLanguageChange](player-player-audiolanguagechange.md)                                     | Se produit lorsque le langage audio actuel change.                                  |
| [des réponses](player-player-buffering.md)                                                         | Se produit lorsque le lecteur Windows Media commence ou met fin à la mise en mémoire tampon.                       |
| [CdromMediaChange](player-player-cdrommediachange.md)                                           | Se produit lorsque le support CD change.                                                |
| [CurrentItemChange](player-player-currentitemchange.md)                                         | Se produit lorsque l’élément actuel change.                                            |
| [CurrentMediaItemAvailable](player-player-currentmediaitemavailable.md)                         | Se produit lorsque l’élément multimédia actuel devient disponible.                            |
| [CurrentPlaylistChange](player-player-currentplaylistchange.md)                                 | Se produit lors de la modification de la sélection actuelle.                                        |
| [CurrentPlaylistItemAvailable](player-player-currentplaylistitemavailable.md)                   | Se produit lorsque l’élément de sélection actuel devient disponible.                         |
| [DomainChange](player-player-domainchange.md)                                                   | Se produit lorsque le domaine DVD change.                                              |
| [Error](player-player-error.md)                                                                 | Se produit lorsque le contrôle du lecteur Windows Media a une condition d’erreur.             |
| [MarkerHit](player-player-markerhit.md)                                                         | Se produit lorsque le lecteur Windows Media rencontre un marqueur dans le clip.                |
| [MediaChange](player-player-mediachange.md)                                                     | Se produit lorsqu’un élément multimédia change.                                                |
| [MediaCollectionAttributeStringAdded](player-player-mediacollectionattributestringadded.md)     | Se produit lorsqu’une valeur d’attribut est ajoutée à la bibliothèque.                          |
| [MediaCollectionAttributeStringChanged](player-player-mediacollectionattributestringchanged.md) | Se produit lorsqu’une valeur d’attribut de la bibliothèque est modifiée.                        |
| [MediaCollectionAttributeStringRemoved](player-player-mediacollectionattributestringremoved.md) | Se produit lorsqu’une valeur d’attribut est supprimée de la bibliothèque.                      |
| [MediaCollectionChange](player-player-mediacollectionchange.md)                                 | Se produit lorsque l’objet **MediaCollection** est modifié.                              |
| [MediaError](player-player-mediaerror.md)                                                       | Se produit lorsque l’objet **multimédia** a une condition d’erreur.                         |
| [ModeChange](player-player-modechange.md)                                                       | Se produit lors du basculement entre le mode aléatoire et le mode normal.                           |
| [OpenPlaylistSwitch](player-player-openplaylistswitch.md)                                       | Se produit lorsqu’un titre sur un DVD commence à être lu.                                     |
| [OpenStateChange](player-player-openstatechange.md)                                             | Se produit lorsque *Player*. **openState** change.                                      |
| [PlaylistChange](player-player-playlistchange.md)                                               | Se produit lorsqu’une sélection est modifiée.                                                  |
| [PlaylistCollectionChange](player-player-playlistcollectionchange.md)                           | Se produit lors d’une modification de la collection de sélections.                        |
| [PlaylistCollectionPlaylistAdded](player-player-playlistcollectionplaylistadded.md)             | Se produit lorsqu’une sélection est ajoutée à la collection de sélections.                      |
| [PlaylistCollectionPlaylistRemoved](player-player-playlistcollectionplaylistremoved.md)         | Se produit lorsqu’une sélection est supprimée de la collection de sélections.                  |
| [PlayStateChange](player-player-playstatechange.md)                                             | Se produit lorsque *Player*. **lecture** change.                                      |
| [PositionChange](player-player-positionchange.md)                                               | Se produit lorsque *Player*. *contrôles*. **CurrentPosition** change.                     |
| [ScriptCommand](player-player-scriptcommand.md)                                                 | Se produit lorsque le lecteur Windows Media rencontre une commande de script incorporée dans un fichier. |
| [StatusChange](player-player-statuschange.md)                                                   | Se produit lorsque la propriété **Status** change de valeur.                               |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Objet Player**](player-object.md)
</dt> <dt>

[**Référence de programmation de l’apparence**](skin-programming-reference.md)
</dt> </dl>

 

 




