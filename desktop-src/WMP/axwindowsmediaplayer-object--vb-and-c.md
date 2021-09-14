---
title: AxWindowsMediaPlayer, objet (VB et C)
description: objet AxWindowsMediaPlayer (VB et C \)
ms.assetid: d7eeac20-1afa-4e73-9af6-9772fbb65516
keywords:
- Lecteur Windows Media, objet AxWindowsMediaPlayer
- Lecteur Windows Media Mobile, objet AxWindowsMediaPlayer
- Lecteur Windows Media modèle objet, objet AxWindowsMediaPlayer
- modèle objet, objet AxWindowsMediaPlayer
- contrôle ActiveX, objet AxWindowsMediaPlayer
- Lecteur Windows Media ActiveX contrôle, objet AxWindowsMediaPlayer
- Lecteur Windows Media contrôle Mobile ActiveX, objet AxWindowsMediaPlayer
- référence pour le modèle objet, objet AxWindowsMediaPlayer
- Objet AxWindowsMediaPlayer
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 32f814560c8b6eb13dc5abb8736378432ec4565e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126856042"
---
# <a name="axwindowsmediaplayer-object-vb-and-c"></a>objet AxWindowsMediaPlayer (VB et C#)

l’objet AxWindowsMediaPlayer est l’objet racine du contrôle Lecteur Windows Media. Il prend en charge les propriétés, les méthodes et les événements énumérés dans les tableaux suivants.

L’objet AxWindowsMediaPlayer prend en charge les propriétés suivantes.



| Propriété                                                                             | Description                                                                                                                        |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [cdromCollection](axwmplib-axwindowsmediaplayer-cdromcollection--vb-and-c.md)       | Obtient une interface **IWMPCdromCollection** .                                                                                         |
| [closedCaption](axwmplib-axwindowsmediaplayer-closedcaption--vb-and-c.md)           | Obtient une interface IWMPClosedCaption.                                                                                               |
| [Ctlcontrols](axwmplib-axwindowsmediaplayer-ctlcontrols--vb-and-c.md)               | Obtient une interface IWMPControls.                                                                                                    |
| [Ctlenabled](axwmplib-axwindowsmediaplayer-ctlenabled--vb-and-c.md)                 | obtient ou définit une valeur indiquant si le contrôle de Lecteur Windows Media est activé.                                               |
| [currentMedia](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)             | Obtient ou définit l’interface IWMPMedia qui correspond à l’élément multimédia actuel.                                                   |
| [currentPlaylist](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md)       | Obtient ou définit l’interface **IWMPPlaylist** actuelle.                                                                               |
| [DVD](axwmplib-axwindowsmediaplayer-dvd--vb-and-c.md)                               | Obtient une interface IWMPDVD.                                                                                                         |
| [enableContextMenu](axwmplib-axwindowsmediaplayer-enablecontextmenu--vb-and-c.md)   | Obtient ou définit une valeur indiquant s’il faut activer le menu contextuel qui apparaît lorsque l’utilisateur clique sur le bouton droit de la souris.          |
| [Error](axwmplib-axwindowsmediaplayer-error--vb-and-c.md)                           | Obtient une interface IWMPError.                                                                                                       |
| [Large](axwmplib-axwindowsmediaplayer-fullscreen--vb-and-c.md)                 | Obtient ou définit une valeur indiquant si le contenu vidéo est lu en mode plein écran.                                          |
| [isOnline](axwmplib-axwindowsmediaplayer-isonline--vb-and-c.md)                     | Obtient une valeur indiquant si l’utilisateur est connecté à un réseau.                                                                |
| isRemote                                                                             | Non pris en charge pour la programmation .NET.                                                                                                |
| [mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)       | Obtient une interface IWMPMediaCollection.                                                                                             |
| [network](axwmplib-axwindowsmediaplayer-network--vb-and-c.md)                       | Obtient une interface IWMPNetwork.                                                                                                     |
| [openState](axwmplib-axwindowsmediaplayer-openstate--vb-and-c.md)                   | Obtient une valeur indiquant l’état de la source de contenu.                                                                           |
| playerApplication                                                                    | Non pris en charge pour la programmation .NET.                                                                                                |
| [playlistCollection](axwmplib-axwindowsmediaplayer-playlistcollection--vb-and-c.md) | Obtient une interface IWMPPlaylistCollection.                                                                                          |
| [Lecture](axwmplib-axwindowsmediaplayer-playstate--vb-and-c.md)                   | obtient une valeur indiquant l’état de l’opération de Lecteur Windows Media.                                                           |
| [settings](axwmplib-axwindowsmediaplayer-settings--vb-and-c.md)                     | Obtient une interface IWMPSettings.                                                                                                    |
| [statut](axwmplib-axwindowsmediaplayer-status--vb-and-c.md)                         | obtient une valeur indiquant l’état actuel de Lecteur Windows Media.                                                                |
| [stretchToFit](axwmplib-axwindowsmediaplayer-stretchtofit--vb-and-c.md)             | obtient ou définit une valeur indiquant si la vidéo est étirée pour s’ajuster à la taille de l’affichage vidéo du contrôle de Lecteur Windows Media.          |
| [uiMode](axwmplib-axwindowsmediaplayer-uimode--vb-and-c.md)                         | obtient ou définit une valeur indiquant les contrôles qui sont affichés dans l’interface utilisateur lorsque Lecteur Windows Media est incorporée dans une page web. |
| [URL](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)                               | Obtient ou définit le nom du clip à lire.                                                                                         |
| [versionInfo](axwmplib-axwindowsmediaplayer-versioninfo--vb-and-c.md)               | obtient une valeur qui spécifie la version du Lecteur Windows Media.                                                               |
| [windowlessVideo](axwmplib-axwindowsmediaplayer-windowlessvideo--vb-and-c.md)       | obtient ou définit une valeur indiquant si le contrôle de Lecteur Windows Media restitue la vidéo en mode sans fenêtre.                         |



 

L’objet AxWindowsMediaPlayer prend en charge les méthodes suivantes.



| Méthode                                                       | Description                                               |
|--------------------------------------------------------------|-----------------------------------------------------------|
| [close](axwmplib-axwindowsmediaplayer-close.md)             | libère Lecteur Windows Media ressources.                  |
| [launchURL](axwmplib-axwindowsmediaplayer-launchurl.md)     | Envoie une URL au navigateur par défaut de l’utilisateur à restituer. |
| [newMedia](axwmplib-axwindowsmediaplayer-newmedia.md)       | Retourne une interface IWMPMedia pour un nouvel élément multimédia.      |
| [newPlaylist](axwmplib-axwindowsmediaplayer-newplaylist.md) | retourne une interface IWMPPlaylist pour une nouvelle sélection.     |
| [openPlayer](axwmplib-axwindowsmediaplayer-openplayer.md)   | ouvre Lecteur Windows Media à l’aide de l’URL spécifiée.       |



 

L’objet AxWindowsMediaPlayer prend en charge les événements suivants.



| Événement                                                                                                              | Description                                                                                                |
|--------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [AudioLanguageChange](axwmplib-axwindowsmediaplayer-audiolanguagechange.md)                                       | Se produit lorsque le langage audio actuel change.                                                            |
| [des réponses](axwmplib-axwindowsmediaplayer-buffering.md)                                                           | se produit lorsque le contrôle de Lecteur Windows Media commence ou termine la mise en mémoire tampon.                                     |
| [CdromBurnError](axwmplib-axwindowsmediaplayer-cdromburnerror.md)                                                 | Se produit lorsqu’une erreur générique se produit pendant une opération de gravure de CD.                                         |
| [CdromBurnMediaError](axwmplib-axwindowsmediaplayer-cdromburnmediaerror.md)                                       | Se produit lorsqu’une erreur se produit lors de la gravure d’un élément multimédia individuel sur un CD.                               |
| [CdromBurnStateChange](axwmplib-axwindowsmediaplayer-cdromburnstatechange.md)                                     | Se produit lorsqu’une opération de gravure de CD-ROM change d’État.                                                          |
| [CdromMediaChange](axwmplib-axwindowsmediaplayer-cdrommediachange.md)                                             | Se produit lorsqu’un CD ou un DVD est inséré ou éjecté d’un lecteur de CD ou DVD.                                |
| [CdromRipMediaError](axwmplib-axwindowsmediaplayer-cdromripmediaerror.md)                                         | Se produit lorsqu’une erreur se produit lors de l’extraction d’une piste individuelle à partir d’un CD.                                  |
| [CdromRipStateChange](axwmplib-axwindowsmediaplayer-cdromripstatechange.md)                                       | Se produit lorsqu’une opération d’extraction de CD change d’État.                                                          |
| [Clic](axwmplib-axwindowsmediaplayer-click.md)                                                                   | Se produit lorsque l’utilisateur clique sur un bouton de la souris.                                                                |
| CreatePartnershipComplete                                                                                          | Non pris en charge pour la programmation .NET.                                                                        |
| [CurrentItemChange](axwmplib-axwindowsmediaplayer-currentitemchange.md)                                           | Se produit lorsque [IWMPControls. CurrentItem](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md) change. |
| [CurrentMediaItemAvailable](axwmplib-axwindowsmediaplayer-currentmediaitemavailable.md)                           | Se produit lorsqu’un élément de métadonnées graphiques dans l’élément multimédia actuel devient disponible.                           |
| [CurrentPlaylistChange](axwmplib-axwindowsmediaplayer-currentplaylistchange.md)                                   | Se produit lors d’un changement dans la sélection actuelle.                                                 |
| [CurrentPlaylistItemAvailable](axwmplib-axwindowsmediaplayer-currentplaylistitemavailable.md)                     | Se produit lorsque l’élément de sélection actuel devient disponible.                                                   |
| DeviceConnect.                                                                                                      | Non pris en charge pour la programmation .NET.                                                                        |
| DeviceDisconnect                                                                                                   | Non pris en charge pour la programmation .NET.                                                                        |
| DeviceStatusChange                                                                                                 | Non pris en charge pour la programmation .NET.                                                                        |
| DeviceSyncError                                                                                                    | Non pris en charge pour la programmation .NET.                                                                        |
| DeviceSyncStateChange                                                                                              | Non pris en charge pour la programmation .NET.                                                                        |
| [Déconnexion](axwmplib-axwindowsmediaplayer-disconnect.md)                                                         | Réservé pour un usage futur.                                                                                   |
| [DomainChange](axwmplib-axwindowsmediaplayer-domainchange.md)                                                     | Se produit lorsque le domaine DVD change.                                                                        |
| [DoubleClick](axwmplib-axwindowsmediaplayer-doubleclick.md)                                                       | Se produit lorsque l’utilisateur double-clique sur un bouton de la souris.                                                         |
| [DurationUnitChange](axwmplib-axwindowsmediaplayer-durationunitchange.md)                                         | Réservé pour un usage futur.                                                                                   |
| [EndOfStream](axwmplib-axwindowsmediaplayer-endofstream.md)                                                       | Réservé pour un usage futur.                                                                                   |
| [Error](axwmplib-axwindowsmediaplayer-error.md)                                                                   | se produit lorsque le contrôle de Lecteur Windows Media a une condition d’erreur.                                       |
| [FolderScanStateChange](axwmplib-axwindowsmediaplayer-folderscanstatechange.md)                                   | Se produit lorsqu’une opération de surveillance de dossier change d’État.                                                   |
| [KeyDown](axwmplib-axwindowsmediaplayer-keydown.md)                                                               | Se produit lors de la pression sur une touche.                                                                              |
| [KeyPress](axwmplib-axwindowsmediaplayer-keypress.md)                                                             | Se produit lorsqu’une touche est enfoncée, puis libérée.                                                            |
| [Événementiel](axwmplib-axwindowsmediaplayer-keyup.md)                                                                   | Se produit lors du relâchement d'une touche.                                                                             |
| [LibraryConnect](axwmplib-axwindowsmediaplayer-libraryconnect.md)                                                 | Se produit lorsqu’une bibliothèque devient disponible.                                                                   |
| [LibraryDisconnect](axwmplib-axwindowsmediaplayer-librarydisconnect.md)                                           | Se produit lorsqu’une bibliothèque n’est plus disponible.                                                              |
| [MarkerHit](axwmplib-axwindowsmediaplayer-markerhit.md)                                                           | Se produit lorsqu’un marqueur est atteint.                                                                           |
| [MediaChange](axwmplib-axwindowsmediaplayer-mediachange.md)                                                       | Se produit lorsqu’un élément multimédia change.                                                                          |
| [MediaCollectionAttributeStringAdded](axwmplib-axwindowsmediaplayer-mediacollectionattributestringadded.md)       | Se produit lorsqu’une valeur d’attribut est ajoutée à la bibliothèque.                                                    |
| [MediaCollectionAttributeStringChanged](axwmplib-axwindowsmediaplayer-mediacollectionattributestringchanged.md)   | Se produit lorsqu’une valeur d’attribut de la bibliothèque est modifiée.                                                  |
| [MediaCollectionAttributeStringRemoved](axwmplib-axwindowsmediaplayer-mediacollectionattributestringremoved.md)   | Se produit lorsqu’une valeur d’attribut est supprimée de la bibliothèque.                                                |
| [MediaCollectionChange](axwmplib-axwindowsmediaplayer-mediacollectionchange.md)                                   | Se produit lorsque la collection de médias change.                                                                  |
| [MediaCollectionMediaAdded](axwmplib-axwindowsmediaplayer-mediacollectionmediaadded.md)                           | Se produit lorsqu’un élément multimédia est ajouté à la bibliothèque locale.                                                    |
| [MediaCollectionMediaRemoved](axwmplib-axwindowsmediaplayer-mediacollectionmediaremoved.md)                       | Se produit lorsqu’un élément multimédia est supprimé de la bibliothèque locale.                                                |
| [MediaError](axwmplib-axwindowsmediaplayer-mediaerror.md)                                                         | Se produit lorsque l’objet **multimédia** a une condition d’erreur.                                                   |
| [ModeChange](axwmplib-axwindowsmediaplayer-modechange.md)                                                         | se produit lorsqu’un mode de Lecteur Windows Media est modifié.                                                     |
| [MouseDown](axwmplib-axwindowsmediaplayer-mousedown.md)                                                           | Se produit lorsqu’un bouton de la souris est enfoncé.                                                                     |
| [MouseMove](axwmplib-axwindowsmediaplayer-mousemove.md)                                                           | Se produit lorsque le pointeur de la souris est déplacé.                                                                    |
| [Lâché](axwmplib-axwindowsmediaplayer-mouseup.md)                                                               | Se produit lorsqu’un bouton de la souris est relâché.                                                                    |
| [NewStream](axwmplib-axwindowsmediaplayer-newstream.md)                                                           | Réservé pour un usage futur.                                                                                   |
| [OpenPlaylistSwitch](axwmplib-axwindowsmediaplayer-openplaylistswitch.md)                                         | Se produit lorsqu’un titre sur un DVD commence à être lu.                                                               |
| [OpenStateChange](axwmplib-axwindowsmediaplayer-openstatechange.md)                                               | se produit lorsque le contrôle de Lecteur Windows Media change d’état.                                                |
| PlayerDockedStateChange                                                                                            | Non pris en charge pour la programmation .NET.                                                                        |
| PlayerReconnect                                                                                                    | Non pris en charge pour la programmation .NET.                                                                        |
| [PlaylistChange](axwmplib-axwindowsmediaplayer-playlistchange.md)                                                 | Se produit lorsqu’une sélection est modifiée.                                                                            |
| [PlaylistCollectionChange](axwmplib-axwindowsmediaplayer-playlistcollectionchange.md)                             | Se produit lors d’une modification de la collection de sélections.                                                  |
| [PlaylistCollectionPlaylistAdded](axwmplib-axwindowsmediaplayer-playlistcollectionplaylistadded.md)               | Se produit lorsqu’une sélection est ajoutée à la collection de sélections.                                                |
| [PlaylistCollectionPlaylistRemoved](axwmplib-axwindowsmediaplayer-playlistcollectionplaylistremoved.md)           | Se produit lorsqu’une sélection est supprimée de la collection de sélections.                                            |
| [PlaylistCollectionPlaylistSetAsDeleted](axwmplib-axwindowsmediaplayer-playlistcollectionplaylistsetasdeleted.md) | Réservé pour un usage futur.                                                                                   |
| [PlayStateChange](axwmplib-axwindowsmediaplayer-playstatechange.md)                                               | se produit lorsque l’état de lecture du contrôle Lecteur Windows Media change.                                    |
| [PositionChange](axwmplib-axwindowsmediaplayer-positionchange.md)                                                 | Se produit lorsque la position actuelle de l’élément multimédia a été modifiée.                                       |
| [ScriptCommand](axwmplib-axwindowsmediaplayer-scriptcommand.md)                                                   | Se produit lors de la réception d’une commande ou d’une URL synchronisée.                                                     |
| [StatusChange](axwmplib-axwindowsmediaplayer-statuschange.md)                                                     | Se produit lorsque la propriété **Status** change de valeur.                                                         |
| [StringCollectionChange](axwmplib-axwindowsmediaplayer-stringcollectionchange.md)                                 | Se produit lorsqu’une collection de chaînes est modifiée.                                                                   |
| SwitchedToControl                                                                                                  | Non pris en charge pour la programmation .NET.                                                                        |
| SwitchedToPlayerApplication                                                                                        | Non pris en charge pour la programmation .NET.                                                                        |
| [Avertissement](axwmplib-axwindowsmediaplayer-warning.md)                                                               | Réservé pour un usage futur.                                                                                   |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interfaces pour Visual Basic .net et C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interface IWMPCdromCollection (VB et C#)**](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[**Interface IWMPClosedCaption (VB et C#)**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**Interface IWMPControls (VB et C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**Interface IWMPDVD (VB et C#)**](iwmpdvd--vb-and-c.md)
</dt> <dt>

[**Interface IWMPError (VB et C#)**](iwmperror--vb-and-c.md)
</dt> <dt>

[**Interface IWMPMedia (VB et C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Interface IWMPMediaCollection (VB et C#)**](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[**Interface IWMPNetwork (VB et C#)**](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[**Interface IWMPPlaylist (VB et C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**Interface IWMPPlaylistCollection (VB et C#)**](iwmpplaylistcollection--vb-and-c.md)
</dt> <dt>

[**Interface IWMPSettings (VB et C#)**](iwmpsettings--vb-and-c.md)
</dt> <dt>

[**référence du modèle objet pour Visual Basic .net et C #**](object-model-reference-for-visual-basic--net-and-c.md)
</dt> <dt>

[**WMPOpenState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpopenstate)
</dt> <dt>

[**WMPPlayState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpplaystate)
</dt> </dl>

 

 




