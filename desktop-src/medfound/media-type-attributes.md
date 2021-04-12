---
description: Attributs du type de média
ms.assetid: e84ba3f6-4857-4340-baca-5847650ea7b8
title: Attributs du type de média
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fd3bc77197a3a897cd5280338451c33f1ea2637
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321601"
---
# <a name="media-type-attributes"></a>Attributs du type de média

Les attributs suivants s’appliquent aux types de média. Certains de ces attributs sont destinés uniquement à la conversion des formats de type de média hérité en Media Foundation types de média.

## <a name="general-format-attributes"></a>Attributs de format généraux

Ces attributs peuvent être appliqués à tous les types de supports.



| Attribut                                                                            | Description                                                                            |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**MF \_ MT \_ tous les \_ exemples \_ indépendants**](mf-mt-all-samples-independent-attribute.md) | Spécifie si chaque échantillon est indépendant des autres exemples dans le flux.       |
| [**\_type de \_ \_ format AM MT MF \_**](mf-mt-am-format-type-attribute.md)                   | GUID de format.                                                                           |
| [**compressé MF- \_ TM \_**](mf-mt-compressed-attribute.md)                             | Spécifie si les données multimédia sont compressées                                         |
| [**\_exemples de \_ \_ taille fixe \_ MF MF**](mf-mt-fixed-size-samples-attribute.md)           | Spécifie si les échantillons ont une taille fixe.                                       |
| [**\_type de \_ majeurese MF MT \_**](mf-mt-major-type-attribute.md)                            | GUID du type principal.                                                                       |
| [**taille de l’échantillon MF MF \_ \_ \_**](mf-mt-sample-size-attribute.md)                          | Taille de chaque échantillon, en octets.                                                         |
| [**\_sous- \_ type MF MT**](mf-mt-subtype-attribute.md)                                   | GUID de sous-type.                                                                          |
| [**\_ \_ données utilisateur MF \_ MT**](mf-mt-user-data-attribute.md)                              | Contient les données utilisateur pour un type de média qui a été converti à partir d’une structure de format héritée. |
| [**\_ \_ type encapsulé MF-MT \_**](mf-mt-wrapped-type-attribute.md)                        | Contient un type de média encapsulé dans un autre type de média.                     |



 

## <a name="audio-format-attributes"></a>Attributs de format audio

Ces attributs peuvent être appliqués aux types de médias dont le type majeur est égal à MFMediaType \_ audio.



| Attribut                                                                                            | Description                                                                                 |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [\_indication du \_ \_ niveau de \_ profil \_ audio MF MT AAC \_](mf-mt-aac-audio-profile-level-indication.md)       | Spécifie le profil et le niveau audio d’un flux de codage audio avancé (AAC).             |
| [\_type de \_ \_ charge utile de l’AAC MT \_](mf-mt-aac-payload-type.md)                                             | Spécifie le type de charge utile pour un flux de codage audio avancé (AAC).                       |
| [**\_octets de \_ données audio MF MT- \_ \_ octets \_ par \_ seconde**](mf-mt-audio-avg-bytes-per-second-attribute.md)         | Nombre moyen d’octets par seconde.                                                         |
| [**\_bits de \_ sortie audio MF \_ \_ par \_ échantillon**](mf-mt-audio-bits-per-sample-attribute.md)                    | Nombre de bits par échantillon audio.                                                            |
| [**\_alignement de \_ \_ bloc audio MF MT \_**](mf-mt-audio-block-alignment-attribute.md)                     | Alignement de bloc, en octets.                                                                  |
| [**\_masque de \_ \_ canal audio MF MT \_**](mf-mt-audio-channel-mask-attribute.md)                           | Spécifie l’affectation des canaux audio aux positions des haut-parleurs.                            |
| [**\_échantillons MF \_ audio flottant MF MT \_ \_ \_ par \_ seconde**](mf-mt-audio-float-samples-per-second-attribute.md) | Nombre d’échantillons audio par seconde (valeur à virgule flottante).                                  |
| [**\_ \_ \_ matrice FOLDDOWN audio MF \_ MT**](mf-mt-audio-folddown-matrix-attribute.md)                     | Spécifie comment un décodeur audio doit transformer l’audio multicanal en sortie stéréo.        |
| [**\_canaux de \_ \_ numéros audio MF MT \_**](mf-mt-audio-num-channels-attribute.md)                           | Nombre de canaux audio.                                                                   |
| [**MF \_ audio MF- \_ \_ préférer \_ WAVEFORMATEX**](mf-mt-audio-prefer-waveformatex-attribute.md)             | Spécifie la structure de format héritée par défaut à utiliser lors de la conversion d’un type de média audio. |
| [**\_ \_ échantillons audio MF \_ MT \_ par \_ bloc**](mf-mt-audio-samples-per-block-attribute.md)                | Nombre d’échantillons audio contenus dans un bloc compressé de données audio.                    |
| [**\_ \_ échantillons audio MF \_ MT \_ par \_ seconde**](mf-mt-audio-samples-per-second-attribute.md)              | Nombre d’échantillons audio par seconde (valeur entière).                                         |
| [**\_bits de \_ sortie audio MF- \_ octets valides \_ \_ par \_ exemple**](mf-mt-audio-valid-bits-per-sample-attribute.md)       | Nombre de bits de données audio valides dans chaque exemple audio.                                    |
| [**\_ \_ sortie audio MF \_ WMADRC \_ AVGREF**](mf-mt-audio-wmadrc-avgref-attribute.md)                         | Niveau de volume moyen de référence d’un fichier Windows Media Audio.                               |
| [**\_ \_ sortie audio MF \_ WMADRC \_ AVGTARGET**](mf-mt-audio-wmadrc-avgtarget-attribute.md)                   | Niveau de volume moyen cible d’un fichier Windows Media Audio.                                  |
| [**\_ \_ sortie audio MF \_ WMADRC \_ PEAKREF**](mf-mt-audio-wmadrc-peakref-attribute.md)                       | Niveau de volume maximal de référence d’un fichier Windows Media Audio.                                  |
| [**\_ \_ sortie audio MF \_ WMADRC \_ PEAKTARGET**](mf-mt-audio-wmadrc-peaktarget-attribute.md)                 | Niveau de volume maximal cible d’un fichier Windows Media Audio.                                     |
| [\_ \_ \_ \_ balise de format Wave MF d’origine \_](mf-mt-original-wave-format-tag.md)                            | Contient la balise WAVE format d’origine pour un flux audio.                                  |



 

## <a name="video-format-attributes"></a>Attributs de format vidéo

Ces attributs peuvent être appliqués aux types de médias dont le type principal est égal à la \_ vidéo MFMediaType.



| Attribut                                                                              | Description                                                                                                                             |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**\_taux d' \_ \_ erreur de bits Moy \_ \_ . MF**](mf-mt-avg-bit-error-rate-attribute.md)            | Taux d’erreur des données.                                                                                                                        |
| [**\_vitesse de \_ \_ transmission moy. MF**](mf-mt-avg-bitrate-attribute.md)                            | Débit de données approximatif du flux vidéo.                                                                                              |
| [**\_ \_ vidéos vidéo personnalisées MF MT \_ \_**](mf-mt-custom-video-primaries-attribute.md)     | Couleurs primaires personnalisées.                                                                                                                 |
| [**\_Stride MT \_ par défaut \_**](mf-mt-default-stride-attribute.md)                      | STRIDE de la surface par défaut.                                                                                                                 |
| [**\_ \_ indicateurs DRM pour MF MT \_**](mf-mt-drm-flags-attribute.md)                                | Spécifie si la vidéo requiert l’application de la protection contre la copie.                                                                         |
| [**\_fréquence d' \_ images MF MF \_**](mf-mt-frame-rate-attribute.md)                              | Fréquence d’images.                                                                                                                             |
| [\_plage de \_ fréquence d’images MF MT \_ \_ \_ Max](mf-mt-frame-rate-range-max.md)                      | La fréquence d’images maximale prise en charge par un périphérique de capture vidéo.                                                                             |
| [plage de fréquence d’images MF- \_ \_ \_ \_ \_ min](mf-mt-frame-rate-range-min.md)                      | La fréquence d’images minimale prise en charge par un périphérique de capture vidéo.                                                                             |
| [**\_taille de \_ trame MF MF \_**](mf-mt-frame-size-attribute.md)                              | Largeur et hauteur de l’image vidéo.                                                                                                    |
| [**\_ \_ ouverture géométrique MF \_ MF**](mf-mt-geometric-aperture-attribute.md)              | Ouverture géométrique.                                                                                                                     |
| [**\_ \_ mode entrelacé MF-MT \_**](mf-mt-interlace-mode-attribute.md)                      | Décrit comment les frames sont entrelacés.                                                                                                |
| [**\_ \_ \_ espacement des images clés de l’option MF MT Max \_**](mf-mt-max-keyframe-spacing-attribute.md)         | Nombre maximal de frames d’une image clé à la suivante.                                                                                |
| [**\_ouverture de \_ l' \_ affichage \_ de la version MF**](mf-mt-minimum-display-aperture-attribute.md) | Ouverture minimale de l’affichage.                                                                                                               |
| [**\_ \_ \_ en-tête de séquence MPEG MF MT \_**](mf-mt-mpeg-sequence-header-attribute.md)         | En-tête de séquence MPEG-1 ou MPEG-2.                                                                                                       |
| [**\_code d' \_ heure de début du MPEG MF MT \_ \_ \_**](mf-mt-mpeg-start-time-code-attribute.md)        | Code d’heure de début de groupe d’images (GOP).                                                                                                |
| [**\_ \_ Indicateurs MPEG2 MT \_ MPEG2**](mf-mt-mpeg2-flags-attribute.md)                            | Indicateurs divers pour la vidéo MPEG-2.                                                                                                   |
| [**\_ \_ Niveau MPEG2 MT \_ MPEG2**](mf-mt-mpeg2-level-attribute.md)                            | Niveau MPEG-2 ou H. 264.                                                                                                                  |
| [**\_Profil de \_ MPEG2 \_ MT pour MF**](mf-mt-mpeg2-profile-attribute.md)                        | Profil MPEG-2 ou H. 264.                                                                                                                |
| [\_ \_ 4cc d’origine MF MT \_](mf-mt-original-4cc.md)                                        | Contient le FOURCC du codec d’origine pour un flux vidéo.                                                                                  |
| [**\_indicateurs de \_ contrôle du PAD MT \_ MF \_**](mf-mt-pad-control-flags-attribute.md)               | Proportions du rectangle de sortie.                                                                                                   |
| [**\_palette MF MT \_**](mf-mt-palette-attribute.md)                                     | Entrées de palette.                                                                                                                        |
| [**\_ouverture de \_ l' \_ analyse \_ panoramique MF MT**](mf-mt-pan-scan-aperture-attribute.md)               | Définit la région 4 × 3 de la vidéo qui doit être affichée en mode panoramique/numérisation.                                                              |
| [**\_ \_ analyse panoramique MF \_ MT \_ activée**](mf-mt-pan-scan-enabled-attribute.md)                 | Spécifie si le mode panoramique/numérisation est activé.                                                                                             |
| [**\_ \_ \_ rapport hauteur/largeur des pixels \_ MF**](mf-mt-pixel-aspect-ratio-attribute.md)             | Proportions de pixels.                                                                                                                     |
| [**\_indicateur de \_ \_ contenu source \_ MF MF**](mf-mt-source-content-hint-attribute.md)           | Proportions prévues.                                                                                                                  |
| [**\_fonction de \_ transfert MF-MF \_**](mf-mt-transfer-function-attribute.md)                | Fonction de conversion de RGB en R’G’B'.                                                                                                 |
| [\_ \_ Vidéo 3D MF \_ MT](mf-mt-video-3d.md)                                                | Spécifie si un flux vidéo contient du contenu 3D.                                                                                   |
| [**vidéo MF MT-présentation de \_ \_ \_ chrominance \_**](mf-mt-video-chroma-siting-attribute.md)           | Décrit comment la chrominance a été échantillonnée pour la vidéo de Y’Cb’Cr.                                                                                    |
| [**\_ \_ éclairage vidéo MF \_ MT**](mf-mt-video-lighting-attribute.md)                      | Conditions d’éclairage optimales pour l’affichage.                                                                                                |
| [**\_ \_ plage nominale de vidéo MF MT \_ \_**](mf-mt-video-nominal-range-attribute.md)           | Plage nominale des informations de couleur                                                                                                  |
| [**\_vidéos de \_ \_ réamorçage de la vidéo MF**](mf-mt-video-primaries-attribute.md)                    | Couleurs primaires.                                                                                                                        |
| [ROTATION de la \_ vidéo MF MT \_ \_](mf-mt-video-rotation.md)                                    | Spécifie la rotation d’une image vidéo dans le sens des aiguilles d’une montre.                                                             |
| [**\_ \_ matrice YUV MT \_ YUV**](mf-mt-yuv-matrix-attribute.md)                              | Matrice de conversion de l’espace de couleurs Y’Cb’Cr vers l’espace de couleurs R’G’B.                                                              |
| [l' \_ appelant MF XVP \_ \_ alloue la \_ sortie](mf-xvp-caller-allocates-output.md)               | Spécifie si l’appelant doit allouer les textures utilisées pour la sortie par la [**MFT du processeur vidéo**](video-processor-mft.md). |
| [MF \_ XVP \_ désactiver \_ FRC](mf-xvp-disable-frc.md)                                        | Désactive la conversion de la fréquence des images dans la [**MFT du processeur vidéo**](video-processor-mft.md).                                               |



 

## <a name="other-format-attributes"></a>Autres attributs de format

Les attributs suivants s’appliquent à la vidéo DV entrelacée.



| Attribut                                                                      | Description                                                           |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [**Pack d’AAUX de la \_ vidéo numérique MF MT- \_ \_ \_ CTRL + \_ \_ 0**](mf-mt-dv-aaux-ctrl-pack-0-attribute.md) | Pack de contrôle source AAUX (audio auxiliaire) pour le premier bloc audio. |
| [**Pack d’AAUX de la \_ vidéo numérique MF MT- \_ \_ \_ CTRL + \_ \_ 1**](mf-mt-dv-aaux-ctrl-pack-1-attribute.md) | Pack de contrôle de code source AAUX pour le deuxième bloc audio.                  |
| [**\_Pack d' \_ AAUX de SRC MT DV-version \_ \_ \_ \_ 0**](mf-mt-dv-aaux-src-pack-0-attribute.md)   | AAUX source Pack pour le premier bloc audio.                           |
| [**\_Pack d' \_ AAUX de SRC MT DV version \_ \_ \_ \_ 1**](mf-mt-dv-aaux-src-pack-1-attribute.md)   | AAUX source Pack pour le second bloc audio.                          |
| [**\_Pack de \_ \_ CTRL Vaux \_ \_ pour la version de montage numérique MF**](mf-mt-dv-vaux-ctrl-pack-attribute.md)      | Pack de contrôle source VAUX (Video auxiliaire).                           |
| [**\_Pack de \_ \_ src Vaux \_ DV \_ MF**](mf-mt-dv-vaux-src-pack-attribute.md)        | Pack source VAUX.                                                     |



 

Les attributs suivants s’appliquent aux fichiers ASF (Advanced Streaming Format).



| Attribut                                                      | Description                                                      |
|----------------------------------------------------------------|------------------------------------------------------------------|
| [\_ \_ format arbitraire MT \_](mf-mt-arbitrary-format.md)        | Données de format supplémentaires pour un flux binaire dans un fichier ASF.       |
| [\_ \_ \_ en-tête arbitraire MT](mf-mt-arbitrary-header.md)        | Données spécifiques au type d’un flux binaire dans un fichier ASF.           |
| [tolérance à la \_ \_ perte d’image MT \_ MF \_](mf-mt-image-loss-tolerant.md) | Spécifie si un flux d’images ASF est un type JPEG dégradable. |



 

Les attributs suivants s’appliquent aux fichiers MPEG-4.



| Attribut                                                                     | Description                                                   |
|-------------------------------------------------------------------------------|---------------------------------------------------------------|
| [\_Entrée d' \_ exemple \_ de \_ \_ ligne de code MPEG4 MF](mf-mt-mpeg4-current-sample-entry.md) | Index de l’entrée actuelle dans la zone de description de l’exemple. |
| [\_Exemple de \_ Description du MPEG4 MF MT \_ \_](mf-mt-mpeg4-sample-description.md)      | Zone de description de l’exemple.                                   |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Attributs Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[Types de médias](media-types.md)
</dt> <dt>

[Types de média audio](audio-media-types.md)
</dt> <dt>

[Types de média vidéo](video-media-types.md)
</dt> </dl>

 

 



