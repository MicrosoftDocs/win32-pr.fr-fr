---
description: "\\_album d' \\_ images de type de contenu wpd \\_ \\_"
ms.assetid: e2ae9f89-5a71-4443-b0c1-81e4c650e1bb
title: WPD_CONTENT_TYPE_IMAGE_ALBUM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cd4ebd352060ec68598d00e62dae29dc0a0e35a0d8e5d69bb84b20c5f695809
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117842326"
---
# <a name="wpd_content_type_image_album"></a>\_album d' \_ images de type de contenu wpd \_ \_

Objet qui décrit son type en tant que \_ type de contenu wpd l' \_ \_ \_ album d’images représente une collection d’images fixes. Un album d’images est fonctionnellement équivalent à une sélection de fichiers image, mais est utilisé pour représenter un album photo physique à l’utilisateur final.

Ce type d’objet prend en charge les propriétés suivantes.



| Nom de la propriété                                                                                                         | Obligatoire ou facultatif                                                              |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [\_ID d’objet wpd \_](object-properties.md)                                                                | Obligatoire, en lecture seule. Un client ne peut pas définir cette propriété, même au moment de la création.    |
| [\_ \_ ID parent de l’objet wpd \_](object-properties.md)                                                 | Obligatoire.                                                                         |
| [nom de l' \_ objet wpd \_](object-properties.md)                                                            | Obligatoire si l’objet représente un fichier.                                         |
| [\_ \_ \_ ID unique persistant de l’objet wpd \_](object-properties.md)                          | Obligatoire, en lecture seule. Un client ne peut pas définir cette propriété même au moment de la création.     |
| [\_format d’objet wpd \_](object-properties.md)                                                        | Obligatoire.                                                                         |
| [TYPE de contenu de l' \_ objet wpd \_ \_](object-properties.md)                                           | Obligatoire.                                                                         |
| [WPD, \_ objet \_ ISHIDDEN](object-properties.md)                                                    | Obligatoire si l’objet est masqué.                                                 |
| [WPD, \_ objet \_ ISSYSTEM](object-properties.md)                                                    | Obligatoire si l’objet est un objet système (autrement dit, il représente un fichier système). |
| [taille de l' \_ objet wpd \_](object-properties.md)                                                            | Obligatoire si l’objet a au moins une ressource.                                 |
| [\_nom du \_ fichier d’origine de l’objet wpd \_ \_](object-properties.md)                              | Obligatoire si l’objet représente un fichier.                                         |
| [\_objet wpd \_ non \_ utilisable](object-properties.md)                                       | Recommandé si l’objet n’est pas destiné à être consommé par l’appareil.             |
| [\_références d’objets wpd \_](object-properties.md)                                                | Obligatoire si l’objet a des références à d’autres objets.                           |
| [\_Mots clés d’objet wpd \_](object-properties.md)                                                    | Facultatif.                                                                         |
| [ID de synchronisation de l' \_ objet wpd \_ \_](object-properties.md)                                                     | Facultatif.                                                                         |
| [l' \_ objet \_ wpd \_ est \_ protégé par DRM](object-properties.md)                                  | Obligatoire si l’objet est protégé par la technologie DRM.                            |
| [Date de création de l' \_ objet wpd \_ \_](object-properties.md)                                           | Facultatif.                                                                         |
| [Date de modification de l' \_ objet wpd \_ \_](object-properties.md)                                         | Recommandé.                                                                      |
| [Date de création de l' \_ objet wpd \_ \_](object-properties.md)                                         | Facultatif.                                                                         |
| [\_ \_ références arrière des objets wpd \_](object-properties.md)                                                                | Recommandé si l’objet est référencé par un autre objet.                        |
| [\_ID d' \_ \_ objet fonctionnel \_ du conteneur d’objets wpd \_](object-properties.md)     | Facultatif.                                                                         |
| [\_objet wpd \_ générer une \_ miniature \_ à partir de la \_ ressource](object-properties.md) | Facultatif                                                                          |
| [l' \_ objet wpd \_ peut \_ Supprimer](object-properties.md)                                                                     | Obligatoire si l’objet ne peut pas être supprimé.                                         |
| [\_paramètres régionaux de la langue de l’objet wpd \_ \_](object-properties.md)                                                                | Facultatif.                                                                         |



 

## <a name="typical-resources"></a>Ressources standard

Ces objets n’hébergent généralement pas de ressources.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Conditions requises pour les objets**](requirements-for-objects.md)
</dt> </dl>

 

 



