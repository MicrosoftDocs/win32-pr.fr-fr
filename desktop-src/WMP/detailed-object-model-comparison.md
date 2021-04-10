---
title: Comparaison du modèle d’objet détaillé
description: Comparaison du modèle d’objet détaillé
ms.assetid: 8f08e2a6-1944-4814-b3b7-680a3722e1a0
keywords:
- Lecteur Windows Media, modèle objet
- Modèle d’objet du lecteur Windows Media, différences entre les versions
- modèle objet, différences de version
- Contrôle ActiveX du lecteur Windows Media, différences entre les versions
- Contrôle ActiveX, différences de version
- Windows Media Player Mobile contrôle ActiveX, différences de version
- Windows Media Player Mobile, modèle objet
- Guide de migration, différences de version
- versions du lecteur Windows Media, modèle objet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 086607a9d367f42479e155e3273c30d88425a457
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2020
ms.locfileid: "104030749"
---
# <a name="detailed-object-model-comparison"></a>Comparaison du modèle d’objet détaillé

Le tableau suivant compare les propriétés du modèle d’objet du lecteur Windows Media 6,4 au modèle objet Windows Media Player 7 ou version ultérieure.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Windows Media Player 6,4, propriété</th>
<th>Windows Media Player 7 ou une version ultérieure équivalente</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><em>Player6</em>. <strong>AllowChangeDisplaySize</strong></td>
<td>L’affichage du lecteur Windows Media 7 ou ultérieur est automatiquement redimensionné pour s’adapter au média. Vous pouvez définir les propriétés de hauteur et de largeur dans la <OBJECT> balise ou dans le script.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>AllowScan</strong></td>
<td><em>Contrôles</em>. <strong>fastForward</strong> et <em>contrôles</em>. les <strong>fastReverse</strong> sont automatiquement activés pour les types de fichiers qui prennent en charge ces méthodes.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>AnglesAvailable</strong></td>
<td>Non disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>AnimationAtStart</strong></td>
<td>Non disponible.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>AudioStream</strong></td>
<td>Utilisez des <em>contrôles</em>. <strong>currentAudioLanguageIndex</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>AudioStreamsAvailable</strong></td>
<td>Utilisez des <em>contrôles</em>. <strong>audioLanguageCount</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>AutoRewind</strong></td>
<td>Utilisez des <em>contrôles</em>. <strong>CurrentPosition</strong> dans le script pour spécifier ou récupérer la position actuelle. Vous pouvez également utiliser des marqueurs et le <em>lecteur</em>. événement <strong>markerHit</strong> .</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Redimensionnement automatique</strong></td>
<td>Le dimensionnement automatique est le comportement par défaut. Pour remplacer le dimensionnement automatique, définissez les propriétés de hauteur et de largeur dans la <OBJECT> balise ou dans le script.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Démarrage automatique</strong></td>
<td>Utilisez les <em>paramètres</em>. <strong>démarrage automatique</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Solde</strong></td>
<td>Utilisez les <em>paramètres</em>. <strong>équilibrer</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Bande passante</strong></td>
<td>Utilisez <em>réseau</em>. <strong>bande passante</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>BaseURL</strong></td>
<td>Utilisez les <em>paramètres</em>. <strong>baseURL</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>BufferingCount</strong></td>
<td>Utilisez <em>réseau.</em> <strong>bufferingCount</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>BufferingProgress</strong></td>
<td>Utilisez <em>réseau</em>. <strong>bufferingProgress</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>BufferingTime</strong></td>
<td>Utilisez <em>réseau</em>. <strong>bufferingTime</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ButtonsAvailable</strong></td>
<td>Non disponible.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CanPreview</strong></td>
<td>Non disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CanScan</strong></td>
<td>Utilisez des <em>contrôles</em>. <strong>isAvailable</strong>( &quot; Fastforward &quot; ) et <em>contrôles</em>.<strong> isAvailable</strong>( &quot; FastReverse &quot; ).</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CanSeek</strong></td>
<td>Utilisez des <em>contrôles</em>. <strong>isAvailable</strong> pour tester si une méthode de recherche particulière peut être exécutée.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CanSeekToMarkers</strong></td>
<td>Utilisez des <em>contrôles</em>. <strong>isAvailable</strong>( &quot; CurrentMarker &quot; ). Utilisez un <em>média</em>. <strong>markerCount</strong> pour récupérer le nombre de marqueurs dans un élément multimédia particulier. Utilisez des <em>contrôles</em>. <strong>currentMarker</strong> pour spécifier ou récupérer le numéro de marqueur actuel.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CaptioningID</strong></td>
<td>Utilisez <em>ClosedCaption</em>. <strong>captioningID</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CCActive</strong></td>
<td>Non disponible. Pour plus d’informations sur la façon dont les sous-titres ont été modifiés dans le lecteur Windows Media, consultez sous- <a href="closed-captioning.md">titrage</a> .</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ChannelDescription</strong></td>
<td>Non disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ChannelName</strong></td>
<td>Non disponible.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ChannelURL</strong></td>
<td>Non disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ClickToPlay</strong></td>
<td>Non disponible. Vous devez fournir des contrôles dans votre interface utilisateur pour démarrer la lecture. L’utilisateur peut également cliquer avec le bouton droit sur l’image vidéo pour ouvrir un menu contextuel qui contient une sélection de <strong>lecture/pause</strong> si le <em>joueur</em>. <strong>enableContextMenu</strong> est égal à true.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ClientID</strong></td>
<td>Non disponible. Le lecteur Windows Media série 9 ou version ultérieure permet à l’utilisateur de choisir si un ID de lecteur unique est transmis aux fournisseurs de contenu.<br/> Si l’utilisateur sélectionne cette option, le lecteur envoie un ID unique au serveur Windows Media. L’ID est enregistré dans le fichier journal du serveur, situé dans le.. <em>system32\logfiles</em> par défaut. Le nom du champ de journal est &quot; c-playerid &quot; . La journalisation du serveur n’est pas activée par défaut dans Windows Media Services.<br/> Si l’utilisateur ne sélectionne pas cette option, le serveur génère un ID de session aléatoire, qui est unique pour chaque client pour une session donnée.<br/> Pour plus d’informations, consultez la documentation de Windows Media Services série 9.<br/></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CodecCount</strong></td>
<td>Non disponible.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ColorKey</strong></td>
<td>Non disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ConnectionSpeed</strong></td>
<td>Non disponible. Utilisez <em>réseau</em>. <strong>débit</strong> binaire pour déterminer la vitesse de transmission actuelle.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ContactAddress</strong></td>
<td>Non disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ContactEmail</strong></td>
<td>Non disponible.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ContactPhone</strong></td>
<td>Non disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CreationDate</strong></td>
<td>Utilisez <em>MediaCollection</em>. <strong>getMediaAtom</strong>( &quot; CreationDate &quot; ) pour récupérer l’index de l’atome de date de création. Utilisez un <em>média</em>. <strong>getItemInfoByAtom</strong> pour récupérer les métadonnées.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CurrentAngle</strong></td>
<td>Non disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CurrentAudioStream</strong></td>
<td>Utilisez des <em>contrôles</em>. <strong>currentAudioLanguageIndex</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CurrentButton</strong></td>
<td>Non disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CurrentCCService</strong></td>
<td>Non disponible.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CurrentChapter</strong></td>
<td>Récupère la sélection actuelle. Si la sélection actuelle n’est pas la même que la sélection retournée par <em>cdrom</em>. <strong>sélection</strong>, aucun chapitre n’est actuellement présent. Dans le cas contraire, le numéro de chapitre actuel est l’index du média actuel dans la sélection actuelle.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CurrentDiscSide</strong></td>
<td>Non disponible.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CurrentDomain</strong></td>
<td>Utilisez un <em>DVD</em>. <strong>domaine</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CurrentMarker</strong></td>
<td>Utilisez des <em>contrôles</em>. <strong>currentMarker</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CurrentPosition</strong></td>
<td>Utilisez des <em>contrôles</em>. <strong>CurrentPosition</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CurrentSubpictureStream</strong></td>
<td>Non disponible.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CurrentTime</strong></td>
<td>Utilisez des <em>contrôles</em>. <strong>currentPositionTimeCode</strong>, <em>contrôles</em>. <strong>currentPositionString</strong>, ou <em>contrôles</em>. <strong>CurrentPosition.</strong></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CurrentTitle</strong></td>
<td>Récupère la sélection actuelle. Si la sélection actuelle est la même que celle de la sélection renvoyée par <em>cdrom</em>. <strong>sélection</strong>, le numéro de titre est l’index du média actuel dans la sélection actuelle.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CurrentVolume</strong></td>
<td>Non disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CursorType</strong></td>
<td>Non disponible. Utilisez les styles Internet Explorer à la place.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Defaultframe</strong></td>
<td>Utilisez les <em>paramètres</em>. <strong>defaultFrame</strong>, ou utilisez un <PARAM> attribut dans l' <OBJECT> élément : <pre data-space="preserve"><code><PARAM NAME=&quot;defaultFrame&quot; VALUE=&quot;right&quot;></code></pre></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>DisplayBackColor</strong></td>
<td>Non disponible.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>DisplayForeColor</strong></td>
<td>Non disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>DisplayMode</strong></td>
<td>La position actuelle peut être extraite en secondes depuis le début en tant que <strong>nombre</strong> à l’aide de <em>contrôles</em>. <strong>CurrentPosition</strong>, sous forme de <strong>chaîne</strong> au format hh : mm : SS (heures, minutes, secondes) à l’aide de <em>contrôles</em>. <strong>currentPositionString</strong>, ou format de code dans le temps à l’aide de <em>contrôles</em>. <strong>currentPositionTimeCode</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Diffuser</strong></td>
<td>L’affichage par défaut se redimensionne automatiquement pour s’adapter au média. Vous pouvez définir les propriétés de hauteur et de largeur dans la <OBJECT> balise ou dans le script. Utilisez le <em>lecteur</em>. <strong>plein</strong> écran pour basculer en mode plein écran.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Durée</strong></td>
<td>Utilisez un <em>média</em>. <strong>durée</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>DVD</strong></td>
<td>Utilisez le <em>lecteur</em>. <strong>DVD</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>EnableContextMenu</strong></td>
<td>Utilisez le <em>lecteur</em>. <strong>enableContextMenu</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Activé</strong></td>
<td>Utilisez le <em>lecteur</em>. <strong>activé</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>EnableFullScreenControls</strong></td>
<td>Lorsque vous utilisez le lecteur Windows Media série 9 ou une version ultérieure, les contrôles en plein écran sont automatiquement activés, sauf si vous utilisez <em>le lecteur.</em> <strong></strong>  =  UIMODE &quot; aucune &quot; .</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>EnablePositionControls</strong></td>
<td>Non disponible. Vous pouvez fournir des contrôles personnalisés ou utiliser <em>Player</em>. <strong>UIMODE</strong> pour choisir une configuration par défaut.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>EnableTracker</strong></td>
<td>Non disponible. Vous pouvez fournir un contrôle personnalisé ou utiliser le <em>joueur</em>. <strong>UIMODE</strong> pour choisir une configuration par défaut.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>EntryCount</strong></td>
<td>Utilisez la <em>sélection</em>. <strong>nombre</strong></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ErrorCode</strong></td>
<td>Utilisez <em>ErrorItem</em>. <strong>ErrorCode</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ErrorCorrection</strong></td>
<td>Non disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ErrorDescription</strong></td>
<td>Utilisez <em>ErrorItem</em>. <strong>errorDescription</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Nom du fichier</strong></td>
<td>Utilisez le <em>lecteur</em>. <strong>URL</strong> ou <em>lecteur</em>. <strong>currentMedia</strong>. Utilisez des <em>contrôles</em>. <strong>CurrentItem</strong> lorsque vous travaillez dans une sélection.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>FramesPerSecond</strong></td>
<td>Non disponible.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>HasError</strong></td>
<td>Utilisez l' <em>erreur</em>. <strong>errorCount</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>HasMultipleItems</strong></td>
<td>Non disponible.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ImageSourceHeight</strong></td>
<td>Utilisez un <em>média</em>. <strong>imageSourceHeight</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ImageSourceWidth</strong></td>
<td>Utilisez un <em>média</em>. <strong>imageSourceWidth</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>InvokeURLs</strong></td>
<td>Utilisez les <em>paramètres</em>. <strong>invokeURLs</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>IsBroadcast</strong></td>
<td>Utilisez <em>réseau</em>. <strong>sourceProtocol</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>IsDurationValid</strong></td>
<td>Non disponible. <em>Média</em>. <strong>Duration</strong> contient une valeur valide lorsqu’elle est utilisée avec l’objet Media actuel.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Langue</strong></td>
<td>Utilisez des <em>contrôles</em>. <strong>currentAudioLanguage</strong></td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>LostPackets</strong></td>
<td>Utilisez <em>réseau</em>. <strong>lostPackets</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>MarkerCount</strong></td>
<td>Utilisez un <em>média</em>. <strong>markerCount</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Muet</strong></td>
<td>Utilisez les <em>paramètres</em>. <strong>muet</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>OpenState</strong></td>
<td>Utilisez le <em>lecteur</em>. <strong>openState</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>PlayCount</strong></td>
<td>Utilisez les <em>paramètres</em>. <strong>playCount</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Lecture</strong></td>
<td>Utilisez le <em>lecteur</em>. <strong>lecture</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>PreviewMode</strong></td>
<td>Non disponible. Utilisez une structure de boucle de script avec un minuteur HTML pour dupliquer cette fonctionnalité.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Taux</strong></td>
<td>Utilisez les <em>paramètres</em>. <strong>taux</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ReadyState</strong></td>
<td>Utilisez le <em>lecteur</em>. <strong>openState</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ReceivedPackets</strong></td>
<td>Utilisez <em>réseau</em>. <strong>receivedPackets</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ReceptionQuality</strong></td>
<td>Utilisez <em>réseau</em>. <strong>receptionQuality</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>RecoveredPackets</strong></td>
<td>Utilisez <em>réseau</em>. <strong>recoveredPackets</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Racine</strong></td>
<td>Non disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>SAMIFileName</strong></td>
<td>Utilisez <em>ClosedCaption</em>. <strong>SAMIFileName</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>SAMILang</strong></td>
<td>Utilisez <em>ClosedCaption</em>. <strong>SAMILang</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>SAMIStyle</strong></td>
<td>Utilisez <em>ClosedCaption</em>. <strong>SAMIStyle</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>SelectionEnd</strong></td>
<td>Utilisez un <em>média</em>. <strong>durée</strong> pour déterminer la longueur d’un objet <strong>multimédia</strong> . Utilisez un marqueur avec des <em>contrôles</em>. <strong>currentMarker</strong> pour spécifier une position de fin personnalisée.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>SelectionStart</strong></td>
<td>Utilisez des <em>contrôles</em>. <strong>CurrentPosition</strong> pour commencer la lecture à partir d’une position particulière ou utiliser un marqueur avec des <em>contrôles</em>. <strong>currentMarker</strong> pour spécifier une position de départ personnalisée.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>SendErrorEvents</strong></td>
<td>Les erreurs sont mises en file d’attente. Utilisez l’objet <strong>Error</strong> et l’objet <strong>ErrorItem</strong> pour récupérer les informations d’erreur.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>SendKeyboardEvents</strong></td>
<td>Non disponible.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>SendMouseClickEvents</strong></td>
<td>Non disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>SendMouseMoveEvents</strong></td>
<td>Non disponible.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>SendOpenStateChangeEvents</strong></td>
<td>Non disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>SendPlayStateChangeEvents</strong></td>
<td>Non disponible.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>SendWarningEvents</strong></td>
<td>Non disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ShowAudioControls</strong></td>
<td>Non disponible. Vous pouvez fournir des contrôles personnalisés ou utiliser <em>Player</em>. <strong>UIMODE</strong> pour choisir une configuration par défaut.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ShowCaptioning</strong></td>
<td>Non disponible. Vous pouvez fournir un affichage de sous-titres personnalisé.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ShowControls</strong></td>
<td>Non disponible. Vous pouvez fournir des contrôles personnalisés ou utiliser <em>Player</em>. <strong>UIMODE</strong> pour choisir une configuration par défaut.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ShowDisplay</strong></td>
<td>Non disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ShowGotoBar</strong></td>
<td>Non disponible. Vous pouvez fournir des fonctionnalités personnalisées à l’aide de l’objet Media</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ShowPositionControls</strong></td>
<td>Non disponible. Vous pouvez fournir des contrôles personnalisés ou utiliser <em>Player</em>. <strong>UIMODE</strong> pour choisir une configuration par défaut.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ShowStatusBar</strong></td>
<td>Non disponible. Vous pouvez fournir des contrôles personnalisés ou utiliser <em>Player</em>. <strong>UIMODE</strong> pour choisir une configuration par défaut.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ShowTracker</strong></td>
<td>Non disponible. Vous pouvez fournir des contrôles personnalisés ou utiliser <em>Player</em>. <strong>UIMODE</strong> pour choisir une configuration par défaut.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>SourceLink</strong></td>
<td>Utilisez un <em>média</em>. <strong>sourceURL</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>SourceProtocol</strong></td>
<td>Utilisez <em>réseau</em>. <strong>sourceProtocol</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>StreamCount</strong></td>
<td>Non disponible. Utilisez des <em>contrôles</em>. <strong>audioLanguageCount</strong> pour récupérer le nombre de flux de langage audio.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>SubpictureOn</strong></td>
<td>Non disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>SubpictureStreamsAvailable</strong></td>
<td>Non disponible</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>TitlesAvailable</strong></td>
<td>Utilisez ce qui suit :<code>Player.Cdrom.playlist.count - 1</code><br/></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>TotalTitleTime</strong></td>
<td>Utilisez <em>currentMedia</em>. <strong>Duration</strong> ou <em>currentMedia</em>. <strong>durationString</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>TransparentAtStart</strong></td>
<td>Utilisez un script pour spécifier les valeurs de hauteur et de largeur pour rendre le lecteur visible ou invisible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>UniqueID</strong></td>
<td>Non disponible.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>VideoBorder3D</strong></td>
<td>Non disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>VideoBorderColor</strong></td>
<td>Non disponible.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>VideoBorderWidth</strong></td>
<td>Non disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Volume</strong></td>
<td>Utilisez les <em>paramètres</em>. <strong>Volume</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>VolumesAvailable</strong></td>
<td>Non disponible.</td>
</tr>
</tbody>
</table>



 

Le tableau suivant compare les méthodes du modèle d’objet Windows Media Player version 6,4 avec le modèle objet Windows Media Player 7 ou version ultérieure.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Lecteur Windows Media 6,4, méthode</th>
<th>Windows Media Player 7 ou une version ultérieure équivalente</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><em>Player6</em>. <strong>AboutBox</strong></td>
<td>Utilisez le <em>lecteur</em>. <strong>VERSIONINFO</strong> pour récupérer la version du lecteur Windows Media.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>BackwardScan</strong></td>
<td>Utilisez les <em>paramètres</em>. <strong>taux</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ButtonActivate</strong></td>
<td>Non disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ButtonSelectAndActivate</strong></td>
<td>Non disponible.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Annuler</strong></td>
<td>Non disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ChapterPlay</strong></td>
<td>Si vous jouez déjà à la sélection de titre spécifiée, récupérez le chapitre souhaité en tant qu’objet multimédia à l’aide de la syntaxe suivante :
<pre data-space="preserve"><code>var media = Player.currentPlaylist.item(index);</code></pre>
Ensuite, spécifiez <em>Player</em>. <strong>currentMedia</strong> à l’aide de l’objet multimédia retourné.<br/></td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ChapterPlayAutoStop</strong></td>
<td>Non disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ChapterSearch</strong></td>
<td>Si vous jouez déjà à la sélection de titre spécifiée, récupérez le chapitre souhaité en tant qu’objet multimédia à l’aide de la syntaxe suivante :
<pre data-space="preserve"><code>var media = Player.currentPlaylist.item(index);</code></pre>
Ensuite, spécifiez <em>Player</em>. <strong>currentMedia</strong> à l’aide de l’objet multimédia retourné.<br/></td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Fastforward</strong></td>
<td>Utilisez des <em>contrôles</em>. <strong>fastForward</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>FastReverse</strong></td>
<td>Utilisez des <em>contrôles</em>. <strong>fastReverse</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ForwardScan</strong></td>
<td>Utilisez les <em>paramètres</em>. <strong>taux</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>GetAllGPRMs</strong></td>
<td>Non disponible.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>GetAllSPRMs</strong></td>
<td>Non disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>GetAudioLanguage</strong></td>
<td>Utilisez des <em>contrôles</em>. <strong>currentAudioLanguage</strong> pour récupérer le LCID de la langue audio actuelle.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>GetCodecDescription</strong></td>
<td>Non disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>GetCodecInstalled</strong></td>
<td>Non disponible.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>GetCodecURL</strong></td>
<td>Utilisez <em>ErrorItem</em>. <strong>customUrl</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>GetCurrentEntry</strong></td>
<td>Utilisez le script pour effectuer une boucle dans la sélection actuelle. Utilisez un <em>média</em>. <strong>isIdentical</strong> pour comparer chaque entrée de la sélection au <em>lecteur</em>. objet <strong>currentMedia</strong> .</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>GetMarkerName</strong></td>
<td>Utilisez un <em>média</em>. <strong>getMarkerName</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>GetMarkerTime</strong></td>
<td>Utilisez un <em>média</em>. <strong>getMarkerTime</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>GetMediaInfoString</strong></td>
<td>Utilisez un <em>média</em>. <strong>getItemInfo</strong>, <em>média</em>. <strong>getItemInfoByAtom</strong>et leurs méthodes associées pour récupérer les métadonnées.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>GetMediaParameter</strong></td>
<td>Utilisez la <em>sélection</em>. <strong>élément</strong> permettant de récupérer un élément multimédia. Utilisez ensuite le <em>média</em>. <strong>getItemInfo</strong> pour récupérer la chaîne de paramètre.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>GetMediaParameterName</strong></td>
<td>Utilisez la <em>sélection</em>. <strong>élément</strong> permettant de récupérer un élément multimédia. Utilisez ensuite le <em>média</em>. <strong>getAttributeName</strong> pour récupérer la chaîne de paramètre.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>GetMoreInfoURL</strong></td>
<td>Non disponible.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>GetNumberOfChapters</strong></td>
<td>Si un titre est en cours de diffusion, utilisez <em>currentPlaylist</em>. <strong>nombre</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>GetStreamGroup</strong></td>
<td>Non disponible.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>GetStreamName</strong></td>
<td>Non disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>GetStreamSelected</strong></td>
<td>Non disponible.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>GetSubpictureLanguage</strong></td>
<td>Non disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Goup</strong></td>
<td>Utilisez un <em>DVD</em>. <strong>retour</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>IsSoundCardEnabled</strong></td>
<td>Non disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>LeftButtonSelect</strong></td>
<td>Non disponible.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>LowerButtonSelect</strong></td>
<td>Non disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>MenuCall</strong></td>
<td>Utilisez un <em>DVD</em>. <strong>titleMenu</strong> ou <em>DVD</em>. <strong>menu</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Suivant</strong></td>
<td>Utilisez des <em>contrôles</em>. <strong>suivant</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>NextPGSearch</strong></td>
<td>Utilisez des <em>contrôles</em>. <strong>suivant</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Ouvrir</strong></td>
<td>Utilisez le <em>lecteur</em>. <strong>URL</strong> ou <em>lecteur</em>. <strong>currentMedia</strong>. Les fichiers sont toujours ouverts de façon asynchrone.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Suspendre</strong></td>
<td>Utilisez des <em>contrôles</em>. <strong>suspendre</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Lire</strong></td>
<td>Utilisez des <em>contrôles</em>. <strong>jouez</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Précédent</strong></td>
<td>Utilisez des <em>contrôles</em>. <strong>précédent</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>PrevPGSearch</strong></td>
<td>Utilisez des <em>contrôles</em>. <strong>précédent</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ResumeFromMenu</strong></td>
<td>Utilisez un <em>DVD</em>. <strong>reprendre</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>RightButtonSelect</strong></td>
<td>Non disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>SetCurrentEntry</strong></td>
<td>Récupérez un objet multimédia à l’aide de <em>currentPlaylist</em>. <strong>Item</strong>(<em>entryNumber</em>). Ensuite, spécifiez l’objet multimédia récupéré à l’aide de <em>contrôles</em>. <strong>CurrentItem</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ShowDialog</strong></td>
<td>Non disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>StillOff</strong></td>
<td>Utilisez des <em>contrôles</em>. <strong>jouez</strong>. Vous pouvez également utiliser des <em>contrôles</em>. <strong>Next</strong> si actuellement en mode toujours.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Arrêter</strong></td>
<td>Utilisez des <em>contrôles</em>. <strong>Arrêtez</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>StreamSelect</strong></td>
<td>Non disponible. Utilisez des <em>contrôles</em>. <strong>currentAudioLanguage</strong> pour spécifier un flux de langue audio.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>TimePlay</strong></td>
<td>À partir de la sélection racine, utilisez <em>currentPlaylist</em>. <strong>Item</strong>(<em>index</em>) pour récupérer un objet multimédia. Ensuite, définissez l’objet multimédia en tant que l’objet en cours à l’aide de <em>contrôles</em>. <strong>CurrentItem</strong>. Ensuite, spécifiez les <em>contrôles</em>. <strong>CurrentPosition</strong> à l’aide d’une valeur de temps en secondes.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>TimeSearch</strong></td>
<td>Utilisez des <em>contrôles</em>. <strong>CurrentPosition</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>TitlePlay</strong></td>
<td>Si vous jouez déjà à la sélection de titre spécifiée, récupérez le chapitre souhaité en tant qu’objet multimédia à l’aide de la syntaxe suivante :
<pre data-space="preserve"><code>var media = Player.currentPlaylist.item(index);</code></pre>
Ensuite, spécifiez <em>Player</em>. <strong>currentMedia</strong> à l’aide de l’objet multimédia retourné.<br/> Vous pouvez également utiliser <em>currentPlaylist</em>. <strong>élément</strong> pour récupérer un objet multimédia, puis utilisez l’objet multimédia retourné pour spécifier des <em>contrôles</em>. <strong>CurrentItem</strong>.<br/></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>TopPGSearch</strong></td>
<td>Non disponible.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>UOPValid</strong></td>
<td>Non disponible</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>UpperButtonSelect</strong></td>
<td>Non disponible.</td>
</tr>
</tbody>
</table>



 

Le tableau suivant compare les événements du modèle d’objet Windows Media Player version 6,4 avec le modèle objet Windows Media Player 7 ou version ultérieure.



| Événement du lecteur Windows Media 6,4  | Windows Media Player 7 ou une version ultérieure équivalente                                                                                                                                                                               |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Player6*. **Mise en mémoire tampon**         | Utilisez le *lecteur*. **Mise en mémoire tampon**.                                                                                                                                                                                              |
| *Player6*. **Cliquez sur**             | Utilisez le *lecteur*. **Cliquez sur**                                                                                                                                                                                                   |
| *Player6*. **DblClick**          | Utilisez le *lecteur*. **DoubleClick**                                                                                                                                                                                             |
| *Player6*. Se **déconnecter**        | Non disponible.                                                                                                                                                                                                           |
| *Player6*. **DisplayModeChange** | Non disponible.                                                                                                                                                                                                           |
| *Player6*. **DVDNotify**         | *Lecteur*. **DomainChange** et *Player*. Les **OpenPlaylistSwitch** sont des événements spécifiques aux DVD. D’autres événements liés aux sélections, aux médias et aux supports de CD-ROM peuvent s’appliquer également en fonction de l’application.                        |
| *Player6*. **EndOfStream**       | Utilisez le *lecteur*. **Lecture**.                                                                                                                                                                                              |
| *Player6*. **Erreur**             | L’événement est inchangé. Toutefois, les erreurs sont mises en file d’attente. Utilisez l’objet **Error** avec l’objet **ErrorItem** pour récupérer les informations d’erreur à partir de la file d’attente. Consultez l’exemple de code dans la section précédente, gestion des erreurs. |
| *Player6*. **Touche PG. suiv**           | Utilisez le *lecteur*. **Touche PG. suiv**                                                                                                                                                                                                 |
| *Player6*. **Appuyez sur la touche**          | Utilisez le *lecteur*. **Appuyez sur la touche**                                                                                                                                                                                                |
| *Player6*. **KeyUp**             | Utilisez le *lecteur*. **KeyUp**                                                                                                                                                                                                   |
| *Player6*. **MarkerHit**         | Utilisez le *lecteur*. **MarkerHit**.                                                                                                                                                                                              |
| *Player6*. **MouseDown**         | Utilisez le *lecteur*. **MouseDown**                                                                                                                                                                                               |
| *Player6*. **MouseMove**         | Utilisez le *lecteur*. **MouseMove**                                                                                                                                                                                               |
| *Player6*. **MouseUp**           | Utilisez le *lecteur*. **MouseUp**                                                                                                                                                                                                 |
| *Player6*. **NewStream**         | Utilisez le *lecteur*. **OpenStateChange**                                                                                                                                                                                         |
| *Player6*. **OpenStateChange**   | Utilisez le *lecteur*. **OpenStateChange**.                                                                                                                                                                                        |
| *Player6*. **PlayStateChange**   | Utilisez le *lecteur*. **PlayStateChange**.                                                                                                                                                                                        |
| *Player6*. **PositionChange**    | Utilisez le *lecteur*. **PositionChange**.                                                                                                                                                                                         |
| *Player6*. **ReadyStateChange**  | Utilisez le *lecteur*. **PlayStateChange**.                                                                                                                                                                                        |
| *Player6*. **Commande**     | Utilisez le *lecteur*. **Commande**.                                                                                                                                                                                          |
| *Player6*. **Avertissement**           | Non disponible.                                                                                                                                                                                                           |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de migration du modèle objet**](object-model-migration-guide.md)
</dt> <dt>

[**Référence du modèle objet pour l’écriture de scripts**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 





