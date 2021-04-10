---
description: '\_ \_ \_ Configuration réseau de la catégorie fonctionnelle wpd \_'
ms.assetid: c5c93ebf-0072-49c2-a109-a2edb7e1bd8d
title: WPD_FUNCTIONAL_CATEGORY_NETWORK_CONFIGURATION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6018243644cec4b1b83d14a51c153d9d6f5f8963
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952647"
---
# <a name="wpd_functional_category_network_configuration"></a>\_ \_ \_ Configuration réseau de la catégorie fonctionnelle wpd \_

Un \_ \_ \_ \_ objet fonctionnel configuration réseau de catégorie fonctionnelle wpd encapsule les fonctionnalités de configuration réseau pour l’appareil, par exemple, les profils Wi-Fi ou les partenariats.



| Nom de la propriété                                                                                                         | Obligatoire ou facultatif                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_ID d’objet wpd \_](object-properties.md)                                                                | Obligatoire, en lecture seule. Un client ne peut pas définir cette propriété, même au moment de la création.                                                                         |
| [\_ \_ ID parent de l’objet wpd \_](object-properties.md)                                                 | Obligatoire.                                                                                                                                              |
| [nom de l' \_ objet wpd \_](object-properties.md)                                                            | Obligatoire.                                                                                                                                              |
| [\_ \_ \_ ID unique persistant de l’objet wpd \_](object-properties.md)                          | Obligatoire, en lecture seule. Un client ne peut pas définir cette propriété, même au moment de la création.                                                                         |
| [\_format d’objet wpd \_](object-properties.md)                                                        | Obligatoire.                                                                                                                                              |
| [TYPE de contenu de l' \_ objet wpd \_ \_](object-properties.md)                                           | Obligatoire.                                                                                                                                              |
| [WPD, \_ objet \_ ISHIDDEN](object-properties.md)                                                    | Obligatoire si l’objet est masqué.                                                                                                                      |
| [WPD, \_ objet \_ ISSYSTEM](object-properties.md)                                                    | Obligatoire si l’objet est un objet système (représente un fichier système).                                                                                  |
| [taille de l' \_ objet wpd \_](object-properties.md)                                                            | Obligatoire si l’objet a au moins une ressource.                                                                                                      |
| [\_nom du \_ fichier d’origine de l’objet wpd \_ \_](object-properties.md)                              | Obligatoire si l’objet représente un fichier.                                                                                                              |
| [\_objet wpd \_ non \_ utilisable](object-properties.md)                                       | Recommandé si l’objet n’est pas destiné à être consommé par l’appareil.                                                                                  |
| [\_références d’objets wpd \_](object-properties.md)                                                | Obligatoire si l’objet a des références à d’autres objets.                                                                                                |
| [\_Mots clés d’objet wpd \_](object-properties.md)                                                    | Optionnel.                                                                                                                                              |
| [ID de synchronisation de l' \_ objet wpd \_ \_](object-properties.md)                                                     | Optionnel.                                                                                                                                              |
| [l' \_ objet \_ wpd \_ est \_ protégé par DRM](object-properties.md)                                  | Obligatoire si l’objet est protégé par la technologie DRM.                                                                                                 |
| [Date de création de l' \_ objet wpd \_ \_](object-properties.md)                                           | Optionnel.                                                                                                                                              |
| [Date de modification de l' \_ objet wpd \_ \_](object-properties.md)                                         | Recommandé.                                                                                                                                           |
| [Date de création de l' \_ objet wpd \_ \_](object-properties.md)                                         | Optionnel.                                                                                                                                              |
| [\_ \_ références arrière des objets wpd \_](object-properties.md)                                                                | Recommandé si l’objet est référencé par un autre objet.                                                                                             |
| [\_ID d' \_ \_ objet fonctionnel \_ du conteneur d’objets wpd \_](object-properties.md)     | Optionnel.                                                                                                                                              |
| [\_objet wpd \_ générer une \_ miniature \_ à partir de la \_ ressource](object-properties.md) | Optionnel.                                                                                                                                              |
| [l' \_ objet wpd \_ peut \_ Supprimer](object-properties.md)                                                                     | Obligatoire si l’objet ne peut pas être supprimé.                                                                                                              |
| [\_paramètres régionaux de la langue de l’objet wpd \_ \_](object-properties.md)                                                                | Optionnel.                                                                                                                                              |
| [\_catégorie d' \_ objet \_ fonctionnel wpd](miscellaneous-properties.md)                      | Obligatoire. Consultez [**\_ \_ \_ \_ objet fonctionnel du type de contenu wpd**](wpd-content-type-functional-object.md) pour les catégories définies par les appareils mobiles Windows. |
| [\_types de contenu de dossier wpd \_ \_ \_ autorisés](miscellaneous-properties.md)                 | Recommandé.                                                                                                                                           |



 

## <a name="typical-resources"></a>Ressources standard

Ces objets n’hébergent généralement pas de ressources.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**\_ \_ objet fonctionnel du type de contenu wpd \_ \_**](wpd-content-type-functional-object.md)
</dt> </dl>

 

 



