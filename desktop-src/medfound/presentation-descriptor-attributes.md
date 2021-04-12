---
description: Attributs du descripteur de présentation
ms.assetid: 2a092a6a-956b-4c1f-955f-529ec08665fe
title: Attributs du descripteur de présentation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18bba97a0e0428bf2ceb91b04c79f69b557876a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527855"
---
# <a name="presentation-descriptor-attributes"></a>Attributs du descripteur de présentation

## <a name="common-presentation-descriptor-attributes"></a>Attributs courants du descripteur de présentation

Les attributs suivants peuvent s’appliquer à n’importe quel descripteur de présentation.



| Attribut                                                                          | Description                                                                                                                                     |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_contexte d' \_ application MF PD \_**](mf-pd-app-context-attribute.md)                        | Contient un pointeur vers le descripteur de présentation à partir du chemin d’accès du média protégé (PMP).                                                          |
| [**\_ \_ \_ débit binaire de codage \_ audio MF PD**](mf-pd-audio-encoding-bitrate-attribute.md) | Spécifie la vitesse de transmission de l’encodage audio pour la présentation, en bits par seconde.                                                                 |
| [\_ \_ ISVARIABLEBITRATE audio MF \_ PD](mf-pd-audio-isvariablebitrate.md)              | Spécifie si les flux audio de la présentation ont une vitesse de transmission variable.                                                               |
| [**\_durée MF PD \_**](mf-pd-duration-attribute.md)                               | Spécifie la durée d’une présentation, en unités de 100 nanosecondes.                                                                              |
| [**\_heure de \_ dernière \_ modification \_ de MF PD**](mf-pd-last-modified-time-attribute.md)         | Spécifie à quel moment une présentation a été modifiée pour la dernière fois.                                                                                                |
| [**\_ \_ type MIME MF \_ PD**](mf-pd-mime-type-attribute.md)                            | Spécifie le type MIME du contenu.                                                                                                         |
| [\_ \_ heure limite de lecture MF PD \_ \_](mf-pd-playback-boundary-time.md)               | Heure à laquelle la présentation doit commencer, par rapport au début de la source du média.                                                       |
| [\_ID d' \_ élément de lecture MF PD \_ \_](mf-pd-playback-element-id.md)                     | Identificateur de l’élément de sélection dans la présentation.                                                                                     |
| [**\_ \_ contexte PMPHOST-MF PD \_**](mf-pd-pmphost-context-attribute.md)                | Contient un pointeur vers l’objet proxy pour le descripteur de présentation de l’application.                                                           |
| [\_ \_ langue par défaut MF PD \_](mf-pd-preferred-language.md)                        | Contient le langage RFC 1766 par défaut de la source du média.                                                                                   |
| [**MF \_ PD \_ \_ STYLELIST sami**](mf-pd-sami-stylelist-attribute.md)                  | Contient le nom convivial des styles SAMI (Synchronized accessibles Media Interchange) pris en charge. Cet attribut s’applique uniquement aux fichiers SAMI. |
| [**\_ \_ taille totale des \_ fichiers MF PD \_**](mf-pd-total-file-size-attribute.md)               | Spécifie la taille totale, en octets, du fichier source.                                                                                          |
| [**\_ \_ \_ débit binaire d’encodage vidéo MF PD \_**](mf-pd-video-encoding-bitrate-attribute.md) | Spécifie la vitesse de transmission de l’encodage vidéo pour la présentation, en bits par seconde.                                                                 |



 

## <a name="presentation-descriptor-attributes-for-asf"></a>Attributs du descripteur de présentation pour ASF

Les attributs suivants s’appliquent aux descripteurs de présentation pour les fichiers ASF (Advanced Systems Format).



| Attribut                                                                                                             | Description                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**CODECLIST de la norme MF \_ PD \_ ASF \_**](mf-pd-asf-codeclist-attribute.md)                                                       | Contient des informations sur les codecs utilisés pour encoder le contenu dans un fichier ASF.                     |
| [**MF \_ PD \_ ASF \_ CONTENTENCRYPTION \_ KEYID**](mf-pd-asf-contentencryption-keyid-attribute.md)                          | Spécifie l’identificateur de clé pour un fichier ASF chiffré.                                              |
| [**\_URL de \_ la \_ \_ licence CONTENTENCRYPTION \_**](mf-pd-asf-contentencryption-license-url-attribute.md)             | Spécifie l’URL d’acquisition de licence pour un fichier ASF chiffré.                                     |
| [**\_données de \_ \_ secret CONTENTENCRYPTION \_ \_ pour MF PD ASF**](mf-pd-asf-contentencryption-secret-data-attribute.md)             | Contient des données secrètes pour un fichier ASF chiffré.                                                      |
| [**\_type de CONTENTENCRYPTION MF PD \_ ASF \_ \_**](mf-pd-asf-contentencryption-type-attribute.md)                            | Spécifie le type de mécanisme de protection utilisé dans un fichier ASF.                                      |
| [**\_données de \_ \_ \_ chiffrement de \_ CONTENTENCRYPTIONEX MF PD ASF**](mf-pd-asf-contentencryptionex-encryption-data-attribute.md) | Contient des données de chiffrement pour un fichier ASF.                                                            |
| [**\_longueur des \_ \_ données ASF \_ pour MF**](mf-pd-asf-data-length-attribute.md)                                                  | Spécifie la taille, en octets, de la section de données d’un fichier ASF.                                    |
| [**\_décalage de \_ \_ début de données ASF \_ \_ pour MF PD**](mf-pd-asf-data-start-offset-attribute.md)                                     | Spécifie l’offset, en octets, entre le début d’un fichier ASF et le début du premier paquet de données. |
| [**heure de création de MF \_ PD \_ ASF \_ FichierPropriétés \_ \_**](mf-pd-asf-fileproperties-creation-time-attribute.md)               | Spécifie la date et l’heure de la création initiale d’un fichier ASF.                                  |
| [**ID du fichier. MF \_ PD \_ ASF \_ FichierPropriétés \_ \_**](mf-pd-asf-fileproperties-file-id-attribute.md)                           | Spécifie l’identificateur de fichier d’un fichier ASF.                                                        |
| [**\_indicateurs FM PD \_ ASF \_ FichierPropriétés \_**](mf-pd-asf-fileproperties-flags-attribute.md)                                | Contient divers indicateurs d’un en-tête ASF.                                                     |
| [**\_vitesse de \_ \_ \_ \_ transmission maximale MF PD ASF FichierPropriétés**](mf-pd-asf-fileproperties-max-bitrate-attribute.md)                   | Spécifie la vitesse de transmission instantanée maximale, en bits par seconde, pour un fichier ASF.                   |
| [**\_ \_ \_ \_ taille maximale des \_ paquets \_ MF PD ASF FichierPropriétés**](mf-pd-asf-fileproperties-max-packet-size-attribute.md)          | Spécifie la taille de paquet maximale, en octets, d’un fichier ASF                                         |
| [**\_taille de \_ paquet min PD ASF \_ FichierPropriétés \_ Min \_ \_ .**](mf-pd-asf-fileproperties-min-packet-size-attribute.md)          | Spécifie la taille de paquet minimale, en octets, d’un fichier ASF.                                        |
| [**\_paquets MF PD \_ ASF FM \_ \_**](mf-pd-asf-fileproperties-packets-attribute.md)                            | Spécifie le nombre de paquets dans la section des données d’un fichier ASF.                                  |
| [**\_durée de \_ \_ \_ lecture \_ MF PD ASF**](mf-pd-asf-fileproperties-play-duration-attribute.md)               | Spécifie le temps nécessaire pour lire un fichier ASF, en unités de 100 nanosecondes.                              |
| [**préroll MF \_ PD \_ ASF \_ \_**](mf-pd-asf-fileproperties-preroll-attribute.md)                            | Spécifie la durée de la mise en mémoire tampon des données avant de commencer à lire un fichier ASF, en millisecondes.    |
| [**durée d’envoi de la norme MF \_ PD \_ ASF \_ \_ \_**](mf-pd-asf-fileproperties-send-duration-attribute.md)               | Spécifie le temps nécessaire pour envoyer un fichier ASF, en unités de 100 nanosecondes.                              |
| [**MF \_ PD \_ ASF \_ info \_ contient du \_ son**](mf-pd-asf-info-has-audio-attribute.md)                                           | Spécifie si un fichier ASF contient au moins un flux audio.                                    |
| [**les \_ \_ informations ASF de la carte ASF ne \_ \_ sont \_ pas \_ audio \_ .**](mf-pd-asf-info-has-non-audio-video-attribute.md)                     | Spécifie si un fichier ASF contient des flux non audio et non vidéo.                             |
| [**la \_ \_ \_ vidéo infos sur MF PD ASF \_ contient une \_ vidéo**](mf-pd-asf-info-has-video-attribute.md)                                           | Spécifie si un fichier ASF contient au moins un flux vidéo.                                    |
| [**LANGLIST de la norme MF \_ PD \_ ASF \_**](mf-pd-asf-langlist-attribute.md)                                                         | Spécifie la liste des langues utilisées dans un fichier ASF.                                                 |
| [MF \_ PD \_ ASF \_ LANGLIST \_ LEGACYORDER](mf-pd-asf-langlist-legacyorder.md)                                              | Contient la liste des langages RFC 1766 utilisés dans la présentation actuelle.                              |
| [**\_ \_ \_ MARQUEur ASF MF**](mf-pd-asf-marker-attribute.md)                                                             | Spécifie les marqueurs dans un fichier ASF.                                                                |
| [**les \_ \_ métadonnées MF PD ASF \_ \_ sont \_ VBR**](mf-pd-asf-metadata-is-vbr-attribute.md)                                         | Spécifie si un fichier ASF utilise l’encodage VBR (variable binaire rate).                                 |
| [**\_paires de \_ \_ \_ \_ compartiments de métadonnées ASF PD ASF \_**](mf-pd-asf-metadata-leaky-bucket-pairs-attribute.md)                | Décrit les exigences en matière de mise en mémoire tampon pour un fichier ASF VBR.                                             |
| [**\_ \_ BUFFERAVERAGEs MF PD ASF \_ Metadata \_ V8 \_**](mf-pd-asf-metadata-v8-bufferaverage-attribute.md)                     | Spécifie la taille moyenne de la mémoire tampon nécessaire pour un fichier ASF VBR.                                         |
| [**\_ \_ VBRPEAKs MF PD ASF \_ Metadata \_ V8 \_**](mf-pd-asf-metadata-v8-vbrpeak-attribute.md)                                 | Spécifie le taux binaire le plus élevé dans un fichier ASF VBR.                                          |
| [**\_écriture de \_ script ASF PD \_**](mf-pd-asf-script-attribute.md)                                                             | Spécifie les commandes de script dans un fichier ASF.                                                        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Attributs Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[Descripteurs de présentation](presentation-descriptors.md)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> </dl>

 

 



