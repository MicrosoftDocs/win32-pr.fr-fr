---
description: '\_Association de \_ réseau de type de contenu wpd \_ \_'
ms.assetid: 5c17aba1-98f7-4d6c-a5d2-2b4623a65255
title: WPD_CONTENT_TYPE_NETWORK_ASSOCIATION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63c383ac251d410e03fc5d26dd969d4161ae555ebf2cdd3802ca7228b1739ff0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117842289"
---
# <a name="wpd_content_type_network_association"></a>\_Association de \_ réseau de type de contenu wpd \_ \_

Objet qui décrit son type, l' \_ Association de type de contenu wpd \_ \_ \_ représente une association entre un hôte et un appareil.

Ce type d’objet prend en charge les propriétés suivantes.



| Nom de la propriété         | Obligatoire ou facultatif        |
|----------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [\_ID d’objet wpd \_](object-properties.md)                                                                                       | Obligatoire.                                                             |
| [\_ \_ ID parent de l’objet wpd \_](object-properties.md)                                                                        | Obligatoire.                                                             |
| [nom de l' \_ objet wpd \_](object-properties.md)                                                                                   | Obligatoire si l’objet représente un fichier.                             |
| [\_ \_ \_ ID unique persistant de l’objet wpd \_](object-properties.md)                                                 | Obligatoire.                                                             |
| [\_format d’objet wpd \_](object-properties.md)                                                                               | Obligatoire.                                                             |
| [TYPE de contenu de l' \_ objet wpd \_ \_](object-properties.md)                                                                  | Obligatoire.                                                             |
| [WPD, \_ objet \_ ISHIDDEN](object-properties.md)                                                                           | Obligatoire si l’objet est masqué.                                     |
| [WPD, \_ objet \_ ISSYSTEM](object-properties.md)                                                                           | Obligatoire si l’objet est un objet système (représente un fichier système). |
| [taille de l' \_ objet wpd \_](object-properties.md)                                                                                   | Obligatoire si l’objet a au moins une ressource.                     |
| [\_nom du \_ fichier d’origine de l’objet wpd \_ \_](object-properties.md)                                                     | Obligatoire si l’objet représente un fichier.                             |
| [\_objet wpd \_ non \_ utilisable](object-properties.md)                                                              | Recommandé si l’objet n’est pas destiné à être consommé par l’appareil. |
| [\_références d’objets wpd \_](object-properties.md)                                                                       | Obligatoire si l’objet a des références à d’autres objets.               |
| [\_Mots clés d’objet wpd \_](object-properties.md)                                                                           | Facultatif.                                                             |
| [ID de synchronisation de l' \_ objet wpd \_ \_](object-properties.md)                                                                            | Facultatif.                                                             |
| [l' \_ objet \_ wpd \_ est \_ protégé par DRM](object-properties.md)                                                         | Obligatoire si l’objet est protégé par la technologie DRM.                |
| [Date de création de l' \_ objet wpd \_ \_](object-properties.md)                                                                  | Facultatif.                                                             |
| [Date de modification de l' \_ objet wpd \_ \_](object-properties.md)                                                                | Recommandé.                                                          |
| [Date de création de l' \_ objet wpd \_ \_](object-properties.md)                                                                | Facultatif.                                                             |
| [\_ \_ références arrière des objets wpd \_](object-properties.md)                                                                                       | Recommandé si l’objet est référencé par un autre objet.            |
| [\_ID d' \_ \_ objet fonctionnel \_ du conteneur d’objets wpd \_](object-properties.md)                            | Facultatif.                                                             |
| [\_objet wpd \_ générer une \_ miniature \_ à partir de la \_ ressource](object-properties.md)                        | Facultatif.                                                             |
| [l' \_ objet wpd \_ peut \_ Supprimer](object-properties.md)                                                                      | Obligatoire si l’objet ne peut pas être supprimé.                             |
| [\_paramètres régionaux de la langue de l’objet wpd \_ \_](object-properties.md)                                                                                        | Facultatif.                                                             |
| [\_ \_ \_ \_ identificateurs de réseau hôte d’association de réseau wpd \_](network-association-properties.md) | Obligatoire.                                                             |
| [\_Association de réseau wpd \_ \_ X509V3SEQUENCE](network-association-properties.md)                       | Facultatif.                                                             |



 

## <a name="typical-resources"></a>Ressources standard

Ces objets n’hébergent généralement pas de ressources.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Conditions requises pour les objets**](requirements-for-objects.md)
</dt> </dl>

 

 



