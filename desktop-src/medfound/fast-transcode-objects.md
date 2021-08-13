---
description: Cette rubrique explique comment utiliser l’API de transcodage pour encoder un fichier multimédia.
ms.assetid: 52b27359-b319-41a0-88e8-d23567420e92
title: Utilisation de l’API de transcodage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72e32ea24ebd4803319713be5fe7789cf41c3a99733338bdfe5ad69baf7396bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118742477"
---
# <a name="using-the-transcode-api"></a>Utilisation de l’API de transcodage

Cette rubrique explique comment utiliser l’API de transcodage pour encoder un fichier multimédia.

-   [Vue d'ensemble](#overview)
-   [Création d’une source de média](#creating-a-media-source)
-   [Création d’un profil de transcodage](#creating-a-transcode-profile)
    -   [Attributs audio](#audio-attributes)
    -   [Attributs vidéo](#video-attributes)
    -   [Attributs de conteneur](#container-attributes)
-   [Création d’une topologie de transcodage](#creating-a-transcode-topology)
-   [Exécution de la session d’encodage](#running-the-encoding-session)
-   [Rubriques connexes](#related-topics)

## <a name="overview"></a>Vue d’ensemble

Avant d’utiliser l’API de transcodage, l’application doit disposer des informations suivantes :

-   Le chemin d’accès ou l’URL d’un fichier multimédia existant qui sera à nouveau codé.
-   Nom du fichier de sortie.
-   Type de conteneur pour le fichier de sortie, tel que MP4 ou le format de streaming avancé (ASF).
-   Le format d'encodage. Ces informations incluent les types de médias qui décrivent les flux audio et vidéo encodés.

Pour utiliser l’API de transcodage, une application effectue les étapes suivantes.

1.  Créer une source de média pour lire le fichier source.
2.  Créez un profil de transcodage. Ajoutez des attributs qui décrivent le flux audio, le flux vidéo et le conteneur de fichiers.
3.  Utilisez le profil de transcodage pour créer une topologie d’encodage. (Pour plus d’informations sur les topologies, consultez [à propos des topologies](about-topologies.md).)
4.  Définissez la topologie sur la [session multimédia](media-session.md).
5.  Démarrez la session multimédia et attendez l’événement [MESessionEnded](mesessionended.md) .

Le reste de cette rubrique décrit ces étapes plus en détail.

## <a name="creating-a-media-source"></a>Création d’une source de média

Une source de média est un objet qui lit et analyse le fichier source. Pour créer une source de média, utilisez le programme de [résolution source](source-resolver.md). Vous pouvez trouver un exemple de code dans la rubrique [à l’aide du programme de résolution source](using-the-source-resolver.md).

## <a name="creating-a-transcode-profile"></a>Création d’un profil de transcodage

Un *profil de transcodage* décrit le format et les paramètres utilisés pour encoder le fichier de sortie. Le profil de transcodage contient trois ensembles d’attributs :

-   Attributs audio : décrivent le format audio cible et les paramètres de l’encodeur audio.
-   Attributs vidéo : décrivent le format vidéo cible et les paramètres de l’encodeur vidéo.
-   Attributs de conteneur : définissez le type de conteneur de fichiers, ainsi que certains paramètres globaux d’encodage.

Pour créer un profil de transcodage, appelez la fonction [**MFCreateTranscodeProfile**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) . Cette fonction retourne un pointeur vers l’interface [**IMFTranscodeProfile**](/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile) . L’objet de profil initial est vide ; il ne contient aucun attribut. L’étape suivante consiste à ajouter les attributs qui définissent le profil.

### <a name="audio-attributes"></a>Attributs audio

Pour ajouter des attributs pour le flux audio, appelez [**IMFTranscodeProfile :: SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes). Ces attributs spécifient la façon dont le flux audio est encodé. Si le fichier de sortie ne contient pas de flux audio, omettez ces attributs.

Les attributs audio se répartissent en deux catégories :

-   Attributs qui spécifient le format du flux encodé
-   Attributs qui spécifient d’autres paramètres d’encodage.

Les attributs de format sont simplement des attributs de type média, comme décrit dans la section [types de média audio](audio-media-types.md). Le jeu d’attributs de format exact dépend de l’encodeur. (Consultez [formats multimédias pris en charge dans Media Foundation](supported-media-formats-in-media-foundation.md).) Voici une liste d’attributs de format audio typiques :



| Attribut de format                                                                         | Description                                                      |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [\_sous- \_ type MF MT](mf-mt-subtype-attribute.md)                                           | Sous-type. Consultez [GUID de sous-type audio](audio-subtype-guids.md). |
| [\_canaux de \_ \_ numéros audio MF MT \_](mf-mt-audio-num-channels-attribute.md)                   | Nombre de canaux audio.                                    |
| [\_ \_ échantillons audio MF \_ MT \_ par \_ seconde](mf-mt-audio-samples-per-second-attribute.md)      | Nombre d’échantillons audio par seconde.                          |
| [\_alignement de \_ \_ bloc audio MF MT \_](mf-mt-audio-block-alignment-attribute.md)             | Alignement du bloc.                                             |
| [\_octets de \_ données audio MF MT- \_ \_ octets \_ par \_ seconde](mf-mt-audio-avg-bytes-per-second-attribute.md) | Nombre moyen d’octets par seconde (vitesse de transmission encodée).   |



 

Les paramètres d’encodage suivants sont définis.



| Paramètre d’encodage                                                             | Description                                                                |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [\_ \_ \_ encodeur d’insertion ne de transcodage MF \_](mf-transcode-donot-insert-encoder.md) | Empêche l’API de transcodage d’insérer un encodeur pour le flux audio. |
| [\_ENCODINGPROFILE de transcodage MF \_](mf-transcode-encodingprofile.md)             | Spécifie le modèle de conformité de périphérique. (S’applique uniquement aux fichiers ASF.)    |
| [\_QUALITYVSSPEED de transcodage MF \_](mf-transcode-qualityvsspeed.md)               | Spécifie le compromis entre la qualité et la vitesse du codage.                |



 

Vous devez définir les attributs de format. Les paramètres d’encodage sont facultatifs.

Une façon de trouver un format compatible avec l’encodeur consiste à appeler la fonction [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) . L’encodeur souhaité est spécifié par le sous-type. La fonction retourne une collection de types de médias pour cet encodeur. Vous pouvez sélectionner un type dans la liste et copier les attributs dans le profil. Pour obtenir un exemple de code qui utilise cette approche, consultez [Didacticiel : encodage d’un fichier WMA](tutorial--converting-an-mp3-file-to-a-wma-file.md).

### <a name="video-attributes"></a>Attributs vidéo

Pour ajouter des attributs pour le flux vidéo, appelez [**IMFTranscodeProfile :: SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes). Ces attributs spécifient la façon dont le flux vidéo est encodé. Si le fichier de sortie ne contient pas de flux vidéo, omettez ces attributs.

Comme avec les attributs audio, les attributs de la vidéo se répartissent en deux catégories :

-   Attributs qui spécifient le format du flux encodé
-   Attributs qui spécifient d’autres paramètres d’encodage.

Les attributs de format sont des attributs de type média, comme décrit dans la section [types de média vidéo](video-media-types.md). Voici une liste d’attributs de format vidéo classiques :



| Attribut de format                                                       | Description                                                      |
|------------------------------------------------------------------------|------------------------------------------------------------------|
| [\_sous- \_ type MF MT](mf-mt-subtype-attribute.md)                         | Sous-type. Consultez [GUID de sous-type de vidéo](video-subtype-guids.md). |
| [\_fréquence d' \_ images MF MF \_](mf-mt-frame-rate-attribute.md)                  | Fréquence d’images.                                                  |
| [\_taille de \_ trame MF MF \_](mf-mt-frame-size-attribute.md)                  | Taille du frame.                                                  |
| [**\_vitesse de \_ \_ transmission moy. MF**](mf-mt-avg-bitrate-attribute.md)            | Vitesse de transmission moyenne.                                            |
| [\_ \_ \_ rapport hauteur/largeur des pixels \_ MF](mf-mt-pixel-aspect-ratio-attribute.md) | Proportions de pixels.                                          |



 

Les paramètres d’encodage suivants sont définis.



| Paramètre d’encodage                                                             | Description                                                                |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [\_ \_ \_ encodeur d’insertion ne de transcodage MF \_](mf-transcode-donot-insert-encoder.md) | Empêche l’API de transcodage d’insérer un encodeur pour le flux vidéo. |
| [\_ENCODINGPROFILE de transcodage MF \_](mf-transcode-encodingprofile.md)             | Spécifie le modèle de conformité de périphérique. (S’applique uniquement aux fichiers ASF.)    |
| [\_QUALITYVSSPEED de transcodage MF \_](mf-transcode-qualityvsspeed.md)               | Spécifie le compromis entre la qualité et la vitesse du codage.                |



 

Vous devez définir les attributs de format. Les paramètres d’encodage sont facultatifs.

### <a name="container-attributes"></a>Attributs de conteneur

Les attributs de conteneur définissent les caractéristiques de niveau fichier du fichier de sortie. Pour définir des attributs de conteneur, appelez [**IMFTranscodeProfile :: SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes). Les attributs suivants sont définis.



| Attribut                                                                          | Description                                                                                                                                            |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_profil d’ajustement de transcodage MF \_ \_](mf-transcode-adjust-profile.md)                  | Définit les paramètres de flux à utiliser pour la topologie de transcodage. Vous pouvez définir les indicateurs pour utiliser les paramètres de la source d’entrée ou utiliser des attributs de flux personnalisés. |
| [\_CONTAINERTYPE de transcodage MF \_](mf-transcode-containertype.md)                     | Spécifie le format de fichier du fichier de sortie, tel que MP4 ou ASF. Sur la base de cette valeur, le récepteur multimédia approprié est ajouté à la topologie.            |
| [\_transfert de \_ \_ métadonnées d’omission de transcodage MF \_](mf-transcode-skip-metadata-transfer.md) | Spécifie si les métadonnées de la source sont copiées dans le fichier de sortie.                                                                               |
| [\_TOPOLOGYMODE de transcodage MF \_](mf-transcode-topologymode.md)                       | Spécifie si les codecs basés sur le matériel peuvent être utilisés lors du transcodage.                                                                                |
| [\_Attribut de \_ déverrouillage MFT FIELDOFUSE \_](mft-fieldofuse-unlock-attribute.md)          | Déverrouille un codec qui a des restrictions de champ d’utilisation. Pour plus d’informations, consultez [restrictions relatives au champ d’utilisation](field-of-use-restrictions.md).              |



 

L' [attribut \_ \_ CONTAINERTYPE de transcodage MF](mf-transcode-containertype.md) est requis. Les autres attributs de conteneur sont facultatifs.

## <a name="creating-a-transcode-topology"></a>Création d’une topologie de transcodage

La topologie de transcodage est une topologie partielle qui contient la source du média, les codecs appropriés et le récepteur multimédia. Pour créer la topologie de transcodage, appelez la fonction [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) . Cette fonction accepte les paramètres suivants comme entrée :

-   Pointeur vers l’interface [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) de la source du média.
-   Nom du fichier de sortie.
-   Pointeur vers l’interface [**IMFTranscodeProfile**](/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile) du profil de transcodage.

La fonction retourne un pointeur vers l’interface [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) .

## <a name="running-the-encoding-session"></a>Exécution de la session d’encodage

Une fois la topologie créée, vous êtes prêt à encoder le fichier. Vous pouvez ignorer le profil à ce stade.

1.  Appelez [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) pour créer la session multimédia.
2.  Appelez [**IMFMediaSession :: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) pour définir la topologie sur la session multimédia.
3.  Appelez [**IMFMediaSession :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) pour démarrer la session d’encodage.
4.  Attendez l’événement [MESessionEnded](mesessionended.md) .
5.  Appelez [**IMFMediaSession :: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) pour fermer la session multimédia.
6.  Attendez l’événement [MESessionClosed](mesessionclosed.md) .
7.  Appelez [**IMFMediaSource :: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).
8.  Appelez [**IMFMediaSession :: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).

La majeure partie du temps passé à l’encodage se produit entre les étapes 3 et 4.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[API de transcodage](transcode-api.md)
</dt> <dt>

[À propos de la session multimédia](about-the-media-session.md)
</dt> </dl>

 

 



