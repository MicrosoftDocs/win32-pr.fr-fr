---
description: vidéo sur le \_ type de contenu wpd \_ \_
ms.assetid: d4a6bd98-c28e-487b-95cc-2c73cd44e3b5
title: WPD_CONTENT_TYPE_VIDEO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6aacf30a9e646a6089058104bd39577fad832e31
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404627"
---
# <a name="wpd_content_type_video"></a>vidéo sur le \_ type de contenu wpd \_ \_

Un objet qui décrit son type vidéo de \_ type de contenu wpd \_ \_ représente un fichier vidéo.

Ce type d’objet prend en charge les propriétés suivantes.



|  Nom de la propriété                             | Obligatoire ou facultatif              |
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [\_ID d’objet wpd \_](object-properties.md)                                                                | Obligatoire, en lecture seule. Un client ne peut pas définir cette propriété, même au moment de la création.                                               |
| [\_ \_ ID parent de l’objet wpd \_](object-properties.md)                                                 | Obligatoire.                                                                                                                    |
| [nom de l' \_ objet wpd \_](object-properties.md)                                                            | Obligatoire si l’objet représente un fichier.                                                                                    |
| [\_ \_ \_ ID unique persistant de l’objet wpd \_](object-properties.md)                          | Obligatoire, en lecture seule. Un client ne peut pas définir cette propriété, même au moment de la création.                                               |
| [\_format d’objet wpd \_](object-properties.md)                                                        | Obligatoire.                                                                                                                    |
| [TYPE de contenu de l' \_ objet wpd \_ \_](object-properties.md)                                           | Obligatoire.                                                                                                                    |
| [WPD, \_ objet \_ ISHIDDEN](object-properties.md)                                                    | Obligatoire si l’objet est masqué.                                                                                            |
| [WPD, \_ objet \_ ISSYSTEM](object-properties.md)                                                    | Obligatoire si l’objet est un objet système (représente un fichier système).                                                        |
| [taille de l' \_ objet wpd \_](object-properties.md)                                                            | Obligatoire si l’objet a au moins une ressource.                                                                            |
| [\_nom du \_ fichier d’origine de l’objet wpd \_ \_](object-properties.md)                              | Obligatoire si l’objet représente un fichier.                                                                                    |
| [\_objet wpd \_ non \_ utilisable](object-properties.md)                                       | Recommandé si l’objet n’est pas destiné à être consommé par l’appareil.                                                        |
| [\_références d’objets wpd \_](object-properties.md)                                                | Obligatoire si l’objet a des références à d’autres objets.                                                                      |
| [\_Mots clés d’objet wpd \_](object-properties.md)                                                    | Optionnel.                                                                                                                    |
| [ID de synchronisation de l' \_ objet wpd \_ \_](object-properties.md)                                                     | Optionnel.                                                                                                                    |
| [l' \_ objet \_ wpd \_ est \_ protégé par DRM](object-properties.md)                                  | Obligatoire si l’objet est protégé par la technologie DRM.                                                                       |
| [Date de création de l' \_ objet wpd \_ \_](object-properties.md)                                           | Optionnel.                                                                                                                    |
| [Date de modification de l' \_ objet wpd \_ \_](object-properties.md)                                         | Recommandé.                                                                                                                 |
| [Date de création de l' \_ objet wpd \_ \_](object-properties.md)                                         | Optionnel.                                                                                                                    |
| [\_ \_ références arrière des objets wpd \_](object-properties.md)                                                                | Recommandé si l’objet est référencé par un autre objet.                                                                   |
| [\_ID d' \_ \_ objet fonctionnel \_ du conteneur d’objets wpd \_](object-properties.md)     | Optionnel.                                                                                                                    |
| [\_objet wpd \_ générer une \_ miniature \_ à partir de la \_ ressource](object-properties.md) | Optionnel.                                                                                                                    |
| [l' \_ objet wpd \_ peut \_ Supprimer](object-properties.md)                                                                     | Obligatoire si l’objet ne peut pas être supprimé.                                                                                    |
| [\_paramètres régionaux de la langue de l’objet wpd \_ \_](object-properties.md)                                                                | Optionnel.                                                                                                                    |
| [\_ \_ débit binaire total des médias wpd \_](media-properties.md)                                            | Recommandé.                                                                                                                 |
| [\_type de \_ débit binaire \_ wpd](media-properties.md)                                              | facultatif.                                                                                                                    |
| [\_Copyright du support wpd \_](media-properties.md)                                                     | Optionnel.                                                                                                                    |
| [ID de contenu de l' \_ abonnement au support wpd \_ \_ \_](media-properties.md)                       | Recommandé, si cet objet représente le contenu d’un service d’abonnement en ligne.                                          |
| [\_nombre d' \_ utilisations du média wpd \_](media-properties.md)                                                    | Recommandé.                                                                                                                 |
| [\_nombre d' \_ omissions du support wpd \_](media-properties.md)                                                  | Optionnel.                                                                                                                    |
| [\_heure du \_ dernier \_ accès au support \_ wpd](media-properties.md)                                 | Optionnel.                                                                                                                    |
| [\_ \_ classification parentale des médias wpd \_](media-properties.md)                                        | Optionnel.                                                                                                                    |
| [\_méta- \_ \_ genre de média wpd](media-properties.md)                                                  | Optionnel.                                                                                                                    |
| [\_compositeur de médias wpd \_](media-properties.md)                                                       | Optionnel.                                                                                                                    |
| [\_ \_ évaluation efficace des médias wpd \_](media-properties.md)                                      | Optionnel.                                                                                                                    |
| [\_sous- \_ \_ titre du média wpd](media-properties.md)                                                    | Optionnel.                                                                                                                    |
| [\_Date de \_ publication du support wpd \_](media-properties.md)                                              | Recommandé.                                                                                                                 |
| [\_taux d' \_ échantillonnage du média wpd \_](media-properties.md)                                                | Optionnel.                                                                                                                    |
| [évaluation de l' \_ étoile du média wpd \_ \_](media-properties.md)                                                | Recommandé.                                                                                                                 |
| [\_ \_ \_ évaluation efficace de l’utilisateur multimédia wpd \_](media-properties.md)                           | Recommandé.                                                                                                                 |
| [\_titre du support wpd \_](media-properties.md)                                                             | Obligatoire.                                                                                                                    |
| [\_durée du média wpd \_](media-properties.md)                                                       | Obligatoire.                                                                                                                    |
| [\_achat de médias wpd \_ \_ maintenant](media-properties.md)                                                        | Recommandé.                                                                                                                 |
| [\_profil d' \_ encodage de média wpd \_](media-properties.md)                                      | Optionnel.                                                                                                                    |
| [\_largeur du média wpd \_](media-properties.md)                                                             | Obligatoire.                                                                                                                    |
| [\_hauteur du média wpd \_](media-properties.md)                                                           | Obligatoire.                                                                                                                    |
| [\_artiste multimédia \_ wpd](media-properties.md)                                                           | Recommandé.                                                                                                                 |
| [URL de la \_ source du média wpd \_ \_](media-properties.md)                                                  | Recommandé.                                                                                                                 |
| [\_URL de \_ destination du support wpd \_](media-properties.md)                                        | facultatif.                                                                                                                    |
| [\_Description du support wpd \_](media-properties.md)                                                 | Optionnel.                                                                                                                    |
| [\_genre de média wpd \_](media-properties.md)                                                             | Optionnel.                                                                                                                    |
| [\_signet d' \_ heure du média wpd \_](media-properties.md)                                            | Optionnel.                                                                                                                    |
| [\_signet d' \_ octet \_ multimédia wpd](media-properties.md)                                            | Optionnel.                                                                                                                    |
| [\_GUID du média wpd \_](media-properties.md)                                                               | Optionnel.                                                                                                                    |
| [\_sous- \_ \_ Description du média wpd](media-properties.md)                                        | Optionnel.                                                                                                                    |
| [\_auteur de vidéo wpd \_](video-properties.md)                                                           | Optionnel.                                                                                                                    |
| [\_nom de \_ la \_ station RECORDEDTV vidéo \_ wpd](video-properties.md)                       | Optionnel.                                                                                                                    |
| [\_numéro de \_ \_ canal RECORDEDTV vidéo wpd \_](video-properties.md)                   | Optionnel.                                                                                                                    |
| [\_RECORDEDTV vidéo \_ wpd \_ répéter](video-properties.md)                                    | Optionnel.                                                                                                                    |
| [taille de la \_ \_ mémoire tampon vidéo wpd \_](video-properties.md)                                                | Optionnel.                                                                                                                    |
| [\_crédits vidéo \_ wpd](video-properties.md)                                                         | Optionnel.                                                                                                                    |
| [DISTANCE de l’image de la \_ clé vidéo wpd \_ \_ \_](video-properties.md)                                 | Optionnel.                                                                                                                    |
| [\_paramètre de \_ qualité \_ vidéo wpd](video-properties.md)                                        | Optionnel.                                                                                                                    |
| [\_type d' \_ analyse \_ vidéo wpd](video-properties.md)                                                    | Obligatoire.                                                                                                                    |
| [\_vitesse de \_ transmission vidéo wpd](video-properties.md)                                                         | Obligatoire.                                                                                                                    |
| [\_ \_ code FourCC vidéo \_ wpd](video-properties.md)                                                | obligatoire si le codec est pris en charge par microsoft Video for Windows (VFW), microsoft DirectShow et Windows Format multimédia. |
| [\_fréquence d’images vidéo wpd \_](video-properties.md)                                                     | Optionnel.                                                                                                                    |



 

## <a name="typical-resources"></a>Ressources standard

Ces objets incluent généralement les ressources suivantes.



| Nom de la ressource                                              | Obligatoire ou facultatif       | Description                                                          |
|------------------------------------------------------------|----------------------------|----------------------------------------------------------------------|
| [**\_ressource wpd \_ par défaut**](wpd-resource-default.md)     | Obligatoire.                  | Contient les données de la vidéo (fichier).                                      |
| [**\_miniature des ressources wpd \_**](wpd-resource-thumbnail.md) | Recommandé, le cas échéant. | Contient l’image clé ou un autre Frame d’exemple non vide pour la vidéo. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Conditions requises pour les objets**](requirements-for-objects.md)
</dt> </dl>

 

 



