---
description: '\_image de \_ type de contenu wpd \_'
ms.assetid: 87342ac7-3f4d-4ed2-99f1-843a79032c6e
title: WPD_CONTENT_TYPE_IMAGE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d547a6190df01f495c0a340010b4305f5c77bf5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534045"
---
# <a name="wpd_content_type_image"></a>\_image de \_ type de contenu wpd \_

Objet qui décrit son type en tant qu' \_ image de type de contenu wpd \_ \_ représente une image continue.

Ce type d’objet prend en charge les propriétés suivantes.



| Nom de la propriété                                                                                                         | Obligatoire ou facultatif                                                                             |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [\_ID d’objet wpd \_](object-properties.md)                                                                | Obligatoire, en lecture seule. Un client ne peut pas définir cette propriété, même au moment de la création.                   |
| [\_ \_ ID parent de l’objet wpd \_](object-properties.md)                                                 | Obligatoire.                                                                                        |
| [nom de l' \_ objet wpd \_](object-properties.md)                                                            | Obligatoire si l’objet représente un fichier.                                                        |
| [\_ \_ \_ ID unique persistant de l’objet wpd \_](object-properties.md)                          | Obligatoire, en lecture seule. Un client ne peut pas définir cette propriété, même au moment de la création.                   |
| [\_format d’objet wpd \_](object-properties.md)                                                        | Obligatoire.                                                                                        |
| [TYPE de contenu de l' \_ objet wpd \_ \_](object-properties.md)                                           | Obligatoire.                                                                                        |
| [WPD, \_ objet \_ ISHIDDEN](object-properties.md)                                                    | Obligatoire si l’objet est masqué.                                                                |
| [WPD, \_ objet \_ ISSYSTEM](object-properties.md)                                                    | Obligatoire si l’objet est un objet système (représente un fichier système).                            |
| [taille de l' \_ objet wpd \_](object-properties.md)                                                            | Obligatoire si l’objet a au moins une ressource.                                                |
| [\_nom du \_ fichier d’origine de l’objet wpd \_ \_](object-properties.md)                              | Obligatoire si l’objet représente un fichier.                                                        |
| [\_objet wpd \_ non \_ utilisable](object-properties.md)                                       | Recommandé si l’objet n’est pas destiné à être consommé par l’appareil.                            |
| [\_références d’objets wpd \_](object-properties.md)                                                | Obligatoire si l’objet a des références à d’autres objets.                                          |
| [\_Mots clés d’objet wpd \_](object-properties.md)                                                    | Optionnel.                                                                                        |
| [ID de synchronisation de l' \_ objet wpd \_ \_](object-properties.md)                                                     | Optionnel.                                                                                        |
| [l' \_ objet \_ wpd \_ est \_ protégé par DRM](object-properties.md)                                  | Obligatoire si l’objet est protégé par la technologie DRM.                                           |
| [Date de création de l' \_ objet wpd \_ \_](object-properties.md)                                           | Optionnel.                                                                                        |
| [Date de modification de l' \_ objet wpd \_ \_](object-properties.md)                                         | Recommandé.                                                                                     |
| [Date de création de l' \_ objet wpd \_ \_](object-properties.md)                                         | Optionnel.                                                                                        |
| [\_ \_ références arrière des objets wpd \_](object-properties.md)                                                                | Recommandé si l’objet est référencé par un autre objet.                                       |
| [\_ID d' \_ \_ objet fonctionnel \_ du conteneur d’objets wpd \_](object-properties.md)     | Optionnel.                                                                                        |
| [\_objet wpd \_ générer une \_ miniature \_ à partir de la \_ ressource](object-properties.md) | Optionnel.                                                                                        |
| [\_image wpd \_ BITDEPTH](image-properties.md)                                                       | Recommandé.                                                                                     |
| [\_ \_ État rogné de l’image wpd \_](image-properties.md)                                          | Optionnel.                                                                                        |
| [État de couleur de l' \_ image wpd \_ \_ corrigé \_](image-properties.md)                         | Optionnel.                                                                                        |
| [\_image wpd \_ FNUMBER](image-properties.md)                                                                           | Optionnel.                                                                                        |
| [temps d’exposition de l' \_ image wpd \_ \_](image-properties.md)                                                                    | Optionnel.                                                                                        |
| [\_index d' \_ exposition d’image wpd \_](image-properties.md)                                                                   | Optionnel.                                                                                        |
| [\_ \_ résolution horizontale de l’image wpd \_](image-properties.md)                                                            | Optionnel.                                                                                        |
| [\_ \_ résolution verticale de l’image wpd \_](image-properties.md)                                                              | Optionnel.                                                                                        |
| [\_Copyright du support wpd \_](media-properties.md)                                                     | Optionnel.                                                                                        |
| [\_largeur du média wpd \_](media-properties.md)                                                             | Obligatoire.                                                                                        |
| [\_hauteur du média wpd \_](media-properties.md)                                                           | Obligatoire.                                                                                        |
| [\_artiste multimédia \_ wpd](media-properties.md)                                                                            | Recommandé.                                                                                     |
| [artiste de l' \_ album multimédia wpd \_ \_](media-properties.md)                                                                     | Recommandé. Cette propriété identifie la personne ou les personnes qui ont créé cet objet à l’origine. |
| [URL de la \_ source du média wpd \_ \_](media-properties.md)                                                                       | Optionnel.                                                                                        |
| [\_URL de \_ destination du support wpd \_](media-properties.md)                                                                  | Optionnel.                                                                                        |
| [\_Description du support wpd \_](media-properties.md)                                                                       | Optionnel.                                                                                        |
| [\_genre de média wpd \_](media-properties.md)                                                                             | Optionnel.                                                                                        |
| [\_signet d' \_ octet \_ multimédia wpd](media-properties.md)                                                                    | Optionnel.                                                                                        |
| [\_GUID du média wpd \_](media-properties.md)                                                                              | Optionnel.                                                                                        |
| [\_sous- \_ \_ Description du média wpd](media-properties.md)                                                                  | Optionnel.                                                                                        |



 

## <a name="typical-resources"></a>Ressources standard

Ces objets incluent généralement les ressources suivantes.



| Nom de la ressource                                                 | Obligatoire ou facultatif | Description                                                                              |
|---------------------------------------------------------------|----------------------|------------------------------------------------------------------------------------------|
| [**\_ressource wpd \_ par défaut**](wpd-resource-default.md)        | Obligatoire.            | Contient les données d’image.                                                                 |
| [**\_miniature des ressources wpd \_**](wpd-resource-thumbnail.md)    | Recommandé.         | Contient la miniature de l’image.                                                    |
| [**\_ \_ clip audio de la ressource wpd \_**](wpd-resource-audio-clip.md) | Optionnel.            | Si cette image est associée à une annotation audio, cette ressource contient les données audio. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Conditions requises pour les objets**](requirements-for-objects.md)
</dt> </dl>

 

 



