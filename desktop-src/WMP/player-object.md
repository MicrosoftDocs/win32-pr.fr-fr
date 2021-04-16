---
title: Objet Player
description: L’objet lecteur est l’objet racine pour le contrôle du lecteur Windows Media. Il prend en charge les propriétés, les méthodes et les événements énumérés dans les tableaux suivants.
ms.assetid: 694bd6cc-c816-478a-87b9-1526e2d18869
keywords:
- Lecteur Windows Media de l’objet lecteur
topic_type:
- apiref
api_name:
- Player Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0bdf6443557477c15497a36d4976b13d0cfea2fc
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2019
ms.locfileid: "104507654"
---
# <a name="player-object"></a>Objet Player

L’objet lecteur est l’objet racine pour le contrôle du lecteur Windows Media. Il prend en charge les propriétés, les méthodes et les événements énumérés dans les tableaux suivants.

L’objet Player prend en charge les propriétés suivantes. Les propriétés marquées d’un astérisque ( \* ) ne sont pas accessibles aux apparences.



| Propriété                                             | Description                                                                                                                                  |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [cdromCollection](player-cdromcollection.md)        | Récupère l’objet [CdromCollection](cdromcollection-object.md) .                                                                          |
| [closedCaption](player-closedcaption.md)            | Récupère l’objet [ClosedCaption](closedcaption-object.md) .                                                                              |
| [commandes](player-controls.md)                      | Récupère l’objet [contrôles](controls-object.md) .                                                                                        |
| [currentMedia](player-currentmedia.md)              | Spécifie ou récupère l’objet [multimédia](media-object.md) actuel.                                                                         |
| [currentPlaylist](player-currentplaylist.md)        | Spécifie ou récupère l’objet de [sélection](playlist-object.md) actuel.                                                                   |
| [DVD](player-dvd.md)                                | Récupère l’objet [DVD](dvd-object.md) .                                                                                                  |
| [enableContextMenu](player-enablecontextmenu.md)\* | Spécifie ou récupère une valeur indiquant s’il faut activer le menu contextuel qui apparaît lorsque l’utilisateur clique sur le bouton droit de la souris.          |
| [activé](player-enabled.md)\*                     | Spécifie ou récupère une valeur indiquant si le contrôle du lecteur Windows Media est activé.                                               |
| [error](player-error.md)                            | Récupère l’objet d' [erreur](error-object.md) .                                                                                              |
| [plein écran](player-fullscreen.md)\*               | Spécifie ou récupère une valeur indiquant si le contenu vidéo est lu en mode plein écran.                                          |
| [isOnline](player-isonline.md)                      | Récupère une valeur indiquant si l’utilisateur est connecté à un réseau.                                                                     |
| [isRemote](player-isremote.md)\*                   | Récupère une valeur indiquant si le contrôle du lecteur Windows Media s’exécute en mode distant.                                             |
| [mediaCollection](player-mediacollection.md)        | Récupère l’objet [MediaCollection](mediacollection-object.md) .                                                                          |
| [network](player-network.md)                        | Récupère l’objet [réseau](network-object.md) .                                                                                          |
| [openState](player-openstate.md)                    | Récupère une valeur indiquant l’état de la source de contenu.                                                                                |
| [playerApplication](player-playerapplication.md)\* | Récupère l’objet [PlayerApplication](playerapplication-object.md) lorsqu’un contrôle du lecteur Windows Media distant est en cours d’exécution.               |
| [playlistCollection](player-playlistcollection.md)  | Récupère l’objet [PlaylistCollection](playlistcollection-object.md) .                                                                    |
| [Lecture](player-playstate.md)                    | Récupère une valeur indiquant l’état de l’opération du lecteur Windows Media.                                                                |
| [settings](player-settings.md)                      | Récupère l’objet de [paramètres](settings-object.md) .                                                                                        |
| [statut](player-status.md)                          | Récupère une valeur indiquant l’état actuel du lecteur Windows Media.                                                                     |
| [stretchToFit](player-stretchtofit.md)\*           | Spécifie ou récupère une valeur indiquant si la vidéo est étirée pour s’ajuster à la taille de l’affichage vidéo de contrôle du lecteur Windows Media.          |
| [UIMODE](player-uimode.md)\*                       | Spécifie ou récupère une valeur indiquant les contrôles qui sont affichés dans l’interface utilisateur lorsque le lecteur Windows Media est incorporé dans une page Web. |
| [URL](player-url.md)                                | Spécifie ou récupère le nom du clip à lire.                                                                                         |
| [versionInfo](player-versioninfo.md)                | Récupère une valeur de chaîne spécifiant la version du lecteur Windows Media.                                                                 |
| [windowlessVideo](player-windowlessvideo.md)\*     | Spécifie ou récupère une valeur indiquant si le contrôle du lecteur Windows Media affiche la vidéo en mode sans fenêtre.                         |



 

\* Inaccessible aux apparences.

L’objet Player prend en charge les méthodes suivantes.



| Méthode                                | Description                                               |
|---------------------------------------|-----------------------------------------------------------|
| [close](player-close.md)             | Libère les ressources du lecteur Windows Media.                  |
| [launchURL](player-launchurl.md)     | Envoie une URL au navigateur par défaut de l’utilisateur à restituer. |
| [newMedia](player-newmedia.md)       | Crée un objet de [média](media-object.md) .           |
| [newPlaylist](player-newplaylist.md) | Crée un objet de [sélection](playlist-object.md) .     |
| [openPlayer](player-openplayer.md)   | Ouvre le lecteur Windows Media à l’aide de l’URL spécifiée.       |



 

L’objet Player prend en charge les événements suivants. Les événements marqués d’un astérisque ( \* ) ne sont pas accessibles aux apparences. Pour plus d’informations sur la gestion des événements de souris et de clavier dans les apparences, consultez [événements externes](external-events.md).



| Événement                                                                                            | Description                                                                      |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [AudioLanguageChange](player-player-audiolanguagechange.md)                                     | Se produit lorsque le langage audio actuel change.                                  |
| [des réponses](player-player-buffering.md)                                                         | Se produit lorsque le contrôle du lecteur Windows Media démarre ou termine la mise en mémoire tampon.           |
| [CdromMediaChange](player-player-cdrommediachange.md)                                           | Se produit lorsqu’un CD ou un DVD est inséré ou éjecté d’un lecteur de CD ou DVD.      |
| [Cliquez sur](player-player-click.md)\*                                                              | Se produit lorsque l’utilisateur clique sur un bouton de la souris.                                      |
| [CurrentItemChange](player-player-currentitemchange.md)                                         | Se produit lorsque *contrôle*. modifications de **CurrentItem** .                                  |
| [CurrentMediaItemAvailable](player-player-currentmediaitemavailable.md)                         | Se produit lorsqu’un élément de métadonnées graphiques dans l’élément multimédia actuel devient disponible. |
| [CurrentPlaylistChange](player-player-currentplaylistchange.md)                                 | Se produit lors d’un changement dans la sélection actuelle.                       |
| [CurrentPlaylistItemAvailable](player-player-currentplaylistitemavailable.md)                   | Se produit lorsque l’élément de sélection actuel devient disponible.                         |
| **Déconnexion**                                                                                   | Réservé pour un usage futur.                                                         |
| [DomainChange](player-player-domainchange.md)                                                   | Se produit lorsque le domaine DVD change.                                              |
| [DoubleClick](player-player-doubleclick.md)\*                                                  | Se produit lorsque l’utilisateur double-clique sur un bouton de la souris.                               |
| **DurationUnitChange**                                                                           | Réservé pour un usage futur.                                                         |
| **EndOfStream**                                                                                  | Réservé pour un usage futur.                                                         |
| [Error](player-player-error.md)                                                                 | Se produit lorsque le contrôle du lecteur Windows Media a une condition d’erreur.             |
| [Touche PG. suiv](player-player-keydown.md)\*                                                          | Se produit lors de la pression sur une touche.                                                    |
| [Appuyez sur la touche](player-player-keypress.md)\*                                                        | Se produit lorsqu’une touche est enfoncée, puis libérée.                                  |
| [KeyUp](player-player-keyup.md)\*                                                              | Se produit lors du relâchement d'une touche.                                                   |
| [MarkerHit](player-player-markerhit.md)                                                         | Se produit lorsqu’un marqueur est atteint.                                                 |
| [MediaChange](player-player-mediachange.md)                                                     | Se produit lorsqu’un élément multimédia change.                                                |
| [MediaCollectionAttributeStringAdded](player-player-mediacollectionattributestringadded.md)     | Se produit lorsqu’une valeur d’attribut est ajoutée à la bibliothèque.                          |
| [MediaCollectionAttributeStringChanged](player-player-mediacollectionattributestringchanged.md) | Se produit lorsqu’une valeur d’attribut de la bibliothèque est modifiée.                        |
| [MediaCollectionAttributeStringRemoved](player-player-mediacollectionattributestringremoved.md) | Se produit lorsqu’une valeur d’attribut est supprimée de la bibliothèque.                      |
| [MediaCollectionChange](player-player-mediacollectionchange.md)                                 | Se produit lorsque la collection de médias change.                                        |
| [MediaCollectionMediaAdded](player-player-mediacollectionmediaadded.md)                         | Se produit lorsqu’un élément multimédia est ajouté à la bibliothèque locale.                          |
| [MediaCollectionMediaRemoved](player-player-mediacollectionmediaremoved.md)                     | Se produit lorsqu’un élément multimédia est supprimé de la bibliothèque locale.                      |
| [MediaError](player-player-mediaerror.md)                                                       | Se produit lorsque l’objet **multimédia** a une condition d’erreur.                         |
| [ModeChange](player-player-modechange.md)                                                       | Se produit lors de la modification d’un mode du lecteur Windows Media.                           |
| [MouseDown](player-player-mousedown.md)\*                                                      | Se produit lorsqu’un bouton de la souris est enfoncé.                                           |
| [MouseMove](player-player-mousemove.md)\*                                                      | Se produit lorsque le pointeur de la souris est déplacé.                                          |
| [MouseUp](player-player-mouseup.md)\*                                                          | Se produit lorsqu’un bouton de la souris est relâché.                                          |
| **NewStream**                                                                                    | Réservé pour un usage futur.                                                         |
| [OpenPlaylistSwitch](player-player-openplaylistswitch.md)                                       | Se produit lorsqu’un titre sur un DVD commence à être lu.                                     |
| [OpenStateChange](player-player-openstatechange.md)                                             | Se produit lorsque le contrôle du lecteur Windows Media change d’État.                      |
| [PlaylistChange](player-player-playlistchange.md)                                               | Se produit lorsqu’une sélection est modifiée.                                                  |
| [PlaylistCollectionChange](player-player-playlistcollectionchange.md)                           | Se produit lors d’une modification de la collection de sélections.                        |
| [PlaylistCollectionPlaylistAdded](player-player-playlistcollectionplaylistadded.md)             | Se produit lorsqu’une sélection est ajoutée à la collection de sélections.                      |
| [PlaylistCollectionPlaylistRemoved](player-player-playlistcollectionplaylistremoved.md)         | Se produit lorsqu’une sélection est supprimée de la collection de sélections.                  |
| **PlaylistCollectionPlaylistSetAsDeleted**                                                       | Réservé pour un usage futur.                                                         |
| [PlayStateChange](player-player-playstatechange.md)                                             | Se produit lorsque l’état de lecture du contrôle du lecteur Windows Media change.          |
| [PositionChange](player-player-positionchange.md)                                               | Se produit lorsque la position actuelle de l’élément multimédia a été modifiée.             |
| [ScriptCommand](player-player-scriptcommand.md)                                                 | Se produit lors de la réception d’une commande ou d’une URL synchronisée.                           |
| [StatusChange](player-player-statuschange.md)                                                   | Se produit lorsque la propriété **Status** change de valeur.                               |
| [StringCollectionChange](player-player-stringcollectionchange.md)                               | Se produit lorsqu’une collection de chaînes est modifiée.                                         |
| **Avertissement**                                                                                      | Réservé pour un usage futur.                                                         |



 

\* Inaccessible aux apparences. Pour plus d’informations sur la gestion des événements de souris et de clavier dans les apparences, consultez [gestionnaires d’événements ambiants](ambient-event-handlers.md).

Lorsqu’il est incorporé dans une page Web, l’objet **Player** est accessible à l’aide de la valeur d’ID spécifiée dans la balise Object. Dans un fichier de définition d’apparence, il est accessible à l’aide de l’attribut global **Player** . À des fins d’illustration, le **joueur** sera utilisé comme ID d’objet dans les sections de syntaxe de référence.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence du modèle objet pour l’écriture de scripts**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




