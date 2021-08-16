---
description: '\_type de contenu wpd \_ \_ audio'
ms.assetid: a3d84878-489b-489a-a67e-0e4d25ddd3f7
title: WPD_CONTENT_TYPE_AUDIO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd4aa78b7fa546fab9fe186265ca721e441860a2fc55c2ba0b384df377e1344b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117842353"
---
# <a name="wpd_content_type_audio"></a>\_type de contenu wpd \_ \_ audio

objet qui décrit son type en tant que \_ type de contenu WPD \_ \_ audio représente un fichier audio, tel qu’un Windows Media Audio (WMA) ou un fichier MP3.

Ce type d’objet prend en charge les propriétés suivantes.



| Nom de la propriété                                                                                                         | Obligatoire ou facultatif                                                               |
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [\_ID d’objet wpd \_](object-properties.md)                                                                | Obligatoire, en lecture seule. Un client ne peut pas définir cette propriété, même au moment de la création.     |
| [\_ \_ ID parent de l’objet wpd \_](object-properties.md)                                                 | Obligatoire.                                                                          |
| [nom de l' \_ objet wpd \_](object-properties.md)                                                            | Obligatoire si l’objet représente un fichier.                                          |
| [\_ \_ \_ ID unique persistant de l’objet wpd \_](object-properties.md)                          | Obligatoire, en lecture seule. Un client ne peut pas définir cette propriété, même au moment de la création.     |
| [\_format d’objet wpd \_](object-properties.md)                                                        | Obligatoire.                                                                          |
| [TYPE de contenu de l' \_ objet wpd \_ \_](object-properties.md)                                           | Obligatoire.                                                                          |
| [WPD, \_ objet \_ ISHIDDEN](object-properties.md)                                                    | Obligatoire si l’objet est masqué.                                                  |
| [WPD, \_ objet \_ ISSYSTEM](object-properties.md)                                                    | Obligatoire si l’objet est un objet système (représente un fichier système).              |
| [taille de l' \_ objet wpd \_](object-properties.md)                                                            | Obligatoire si l’objet a au moins une ressource.                                  |
| [\_nom du \_ fichier d’origine de l’objet wpd \_ \_](object-properties.md)                              | Obligatoire si l’objet représente un fichier.                                          |
| [\_objet wpd \_ non \_ utilisable](object-properties.md)                                       | Recommandé si l’objet n’est pas destiné à être consommé par l’appareil.              |
| [\_références d’objets wpd \_](object-properties.md)                                                | Obligatoire si l’objet a des références à d’autres objets.                            |
| [\_Mots clés d’objet wpd \_](object-properties.md)                                                    | Facultatif.                                                                          |
| [ID de synchronisation de l' \_ objet wpd \_ \_](object-properties.md)                                                     | Facultatif.                                                                          |
| [l' \_ objet \_ wpd \_ est \_ protégé par DRM](object-properties.md)                                  | Obligatoire si l’objet est protégé par la technologie DRM.                             |
| [Date de création de l' \_ objet wpd \_ \_](object-properties.md)                                           | Facultatif.                                                                          |
| [Date de modification de l' \_ objet wpd \_ \_](object-properties.md)                                         | Recommandé.                                                                       |
| [Date de création de l' \_ objet wpd \_ \_](object-properties.md)                                         | Facultatif.                                                                          |
| [\_ \_ références arrière des objets wpd \_](object-properties.md)                                                                | Recommandé si l’objet est référencé par un autre objet.                         |
| [\_ID d' \_ \_ objet fonctionnel \_ du conteneur d’objets wpd \_](object-properties.md)     | Facultatif.                                                                          |
| [\_objet wpd \_ générer une \_ miniature \_ à partir de la \_ ressource](object-properties.md) | Facultatif.                                                                          |
| [l' \_ objet wpd \_ peut \_ Supprimer](object-properties.md)                                                                     | Obligatoire si l’objet peut être supprimé.                                             |
| [\_paramètres régionaux de la langue de l’objet wpd \_ \_](object-properties.md)                                                                | Facultatif.                                                                          |
| [\_ \_ débit binaire total des médias wpd \_](media-properties.md)                                            | Recommandé.                                                                       |
| [\_type de \_ débit binaire \_ wpd](media-properties.md)                                              | Facultatif.                                                                          |
| [\_Copyright du support wpd \_](media-properties.md)                                                     | Facultatif.                                                                          |
| [ID de contenu de l' \_ abonnement au support wpd \_ \_ \_](media-properties.md)                       | Recommandé si cet objet représente le contenu d’un service d’abonnement en ligne. |
| [\_nombre d' \_ utilisations du média wpd \_](media-properties.md)                                                    | Recommandé.                                                                       |
| [\_nombre d' \_ omissions du support wpd \_](media-properties.md)                                                  | Facultatif.                                                                          |
| [\_heure du \_ dernier \_ accès au support \_ wpd](media-properties.md)                                 | Facultatif.                                                                          |
| [\_ \_ classification parentale des médias wpd \_](media-properties.md)                                        | Facultatif.                                                                          |
| [\_méta- \_ \_ genre de média wpd](media-properties.md)                                                  | Facultatif.                                                                          |
| [\_compositeur de médias wpd \_](media-properties.md)                                                       | Facultatif.                                                                          |
| [\_ \_ évaluation efficace des médias wpd \_](media-properties.md)                                      | Facultatif.                                                                          |
| [\_sous- \_ \_ titre du média wpd](media-properties.md)                                                    | Facultatif.                                                                          |
| [\_Date de \_ publication du support wpd \_](media-properties.md)                                              | Recommandé.                                                                       |
| [\_taux d' \_ échantillonnage du média wpd \_](media-properties.md)                                                | Facultatif.                                                                          |
| [évaluation de l' \_ étoile du média wpd \_ \_](media-properties.md)                                                | Recommandé.                                                                       |
| [\_ \_ \_ évaluation efficace de l’utilisateur multimédia wpd \_](media-properties.md)                           | Recommandé.                                                                       |
| [\_titre du support wpd \_](media-properties.md)                                                             | Obligatoire.                                                                          |
| [\_durée du média wpd \_](media-properties.md)                                                       | Obligatoire.                                                                          |
| [\_achat de médias wpd \_ \_ maintenant](media-properties.md)                                                        | Recommandé.                                                                       |
| [\_profil d' \_ encodage de média wpd \_](media-properties.md)                                      | Facultatif.                                                                          |
| [\_artiste multimédia \_ wpd](media-properties.md)                                                                            | Recommandé.                                                                       |
| [artiste de l' \_ album multimédia wpd \_ \_](media-properties.md)                                                                     | Recommandé.                                                                       |
| [URL de la \_ source du média wpd \_ \_](media-properties.md)                                                                       | Facultatif.                                                                          |
| [\_URL de \_ destination du support wpd \_](media-properties.md)                                                                  | Facultatif.                                                                          |
| [\_Description du support wpd \_](media-properties.md)                                                                       | Facultatif.                                                                          |
| [\_genre de média wpd \_](media-properties.md)                                                                             | Facultatif.                                                                          |
| [\_signet d' \_ heure du média wpd \_](media-properties.md)                                                                    | Facultatif.                                                                          |
| [\_signet d' \_ octet \_ multimédia wpd](media-properties.md)                                                                    | Facultatif.                                                                          |
| [\_GUID du média wpd \_](media-properties.md)                                                                              | Facultatif.                                                                          |
| [\_sous- \_ \_ Description du média wpd](media-properties.md)                                                                  | Facultatif.                                                                          |
| [\_album de musique wpd \_](music-properties.md)                                                             | Recommandé.                                                                       |
| [\_piste de musique wpd \_](music-properties.md)                                                             | Recommandé.                                                                       |
| [\_paroles de musique wpd \_](music-properties.md)                                                           | Facultatif.                                                                          |
| [\_ambiance musicale \_ wpd](music-properties.md)                                                               | Facultatif.                                                                          |
| [\_ \_ débit binaire wpd](audio-properties.md)                                                         | Recommandé.                                                                       |
| [\_nombre de \_ canaux \_ audio wpd](audio-properties.md)                                            | Facultatif.                                                                          |
| [\_Code de \_ format \_ audio wpd](audio-properties.md)                                                | Facultatif.                                                                          |
| [\_profondeur de \_ bits \_ audio wpd](audio-properties.md)                                                    | Facultatif.                                                                          |
| [\_alignement des \_ blocs \_ audio wpd](audio-properties.md)                                        | Facultatif.                                                                          |



 

## <a name="typical-resources"></a>Ressources standard

Ces objets incluent généralement les ressources suivantes.



| Nom de la ressource                                               | Obligatoire ou facultatif       | Description                                        |
|-------------------------------------------------------------|----------------------------|----------------------------------------------------|
| [**\_ressource wpd \_ par défaut**](wpd-resource-default.md)      | Facultatif.                  | Contient le fichier audio complet.                  |
| [**image de l' \_ album des ressources wpd \_ \_**](wpd-resource-album-art.md) | Recommandé, le cas échéant. | Contient l’image de l’album.                |
| [**\_AUDIOCLIP de ressources wpd \_**](wpd-resource-audio-clip.md) | Facultatif.                  | Contient un exemple de clip du fichier audio complet. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Conditions requises pour les objets**](requirements-for-objects.md)
</dt> </dl>

 

 



