---
description: '\_Association de \_ réseau de type de contenu wpd \_ \_'
ms.assetid: 5c17aba1-98f7-4d6c-a5d2-2b4623a65255
title: WPD_CONTENT_TYPE_NETWORK_ASSOCIATION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ab3fd2f76efef5b85991f1334977c17e34d06b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522153"
---
# <a name="wpd_content_type_network_association"></a>\_Association de \_ réseau de type de contenu wpd \_ \_

Objet qui décrit son type, l' \_ Association de type de contenu wpd \_ \_ \_ représente une association entre un hôte et un appareil.

Ce type d’objet prend en charge les propriétés suivantes.



|                                                                                                                                              |                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| **Nom de la propriété**                                                                                                                            | **Obligatoire ou facultatif**                                              |
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
| [\_Mots clés d’objet wpd \_](object-properties.md)                                                                           | Optionnel.                                                             |
| [ID de synchronisation de l' \_ objet wpd \_ \_](object-properties.md)                                                                            | Optionnel.                                                             |
| [l' \_ objet \_ wpd \_ est \_ protégé par DRM](object-properties.md)                                                         | Obligatoire si l’objet est protégé par la technologie DRM.                |
| [Date de création de l' \_ objet wpd \_ \_](object-properties.md)                                                                  | Optionnel.                                                             |
| [Date de modification de l' \_ objet wpd \_ \_](object-properties.md)                                                                | Recommandé.                                                          |
| [Date de création de l' \_ objet wpd \_ \_](object-properties.md)                                                                | Optionnel.                                                             |
| [\_ \_ références arrière des objets wpd \_](object-properties.md)                                                                                       | Recommandé si l’objet est référencé par un autre objet.            |
| [\_ID d' \_ \_ objet fonctionnel \_ du conteneur d’objets wpd \_](object-properties.md)                            | Optionnel.                                                             |
| [\_objet wpd \_ générer une \_ miniature \_ à partir de la \_ ressource](object-properties.md)                        | Optionnel.                                                             |
| [l' \_ objet wpd \_ peut \_ Supprimer](object-properties.md)                                                                      | Obligatoire si l’objet ne peut pas être supprimé.                             |
| [\_paramètres régionaux de la langue de l’objet wpd \_ \_](object-properties.md)                                                                                        | Optionnel.                                                             |
| [\_ \_ \_ \_ identificateurs de réseau hôte d’association de réseau wpd \_](network-association-properties.md) | Obligatoire.                                                             |
| [\_Association de réseau wpd \_ \_ X509V3SEQUENCE](network-association-properties.md)                       | Optionnel.                                                             |



 

## <a name="typical-resources"></a>Ressources standard

Ces objets n’hébergent généralement pas de ressources.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Conditions requises pour les objets**](requirements-for-objects.md)
</dt> </dl>

 

 



