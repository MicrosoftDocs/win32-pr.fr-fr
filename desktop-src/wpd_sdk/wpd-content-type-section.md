---
description: '\_section du \_ type de contenu wpd \_'
ms.assetid: 8680a74b-9594-4271-a511-637f617aa12a
title: WPD_CONTENT_TYPE_SECTION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84294ff9949418ecc12f55472da202dddcc8f06c
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423779"
---
# <a name="wpd_content_type_section"></a>\_section du \_ type de contenu wpd \_

Un objet qui décrit son type comme \_ \_ \_ une section de type de contenu wpd représente une section de données contenue dans un autre objet. Par exemple, un fichier audio volumineux peut être décrit comme une collection de plusieurs chapitres, et chaque chapitre peut être un \_ objet de section de type de contenu wpd \_ \_ .

La \_ propriété références de l’objet wpd identifie l' \_ objet parent d’une section donnée.

Ce type d’objet prend en charge les propriétés suivantes.



| Nom de la propriété       | Obligatoire ou facultatif             |
|----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [\_ID d’objet wpd \_](object-properties.md)                                                                           | Obligatoire.                                                             |
| [\_ \_ ID parent de l’objet wpd \_](object-properties.md)                                                            | Obligatoire.                                                             |
| [nom de l' \_ objet wpd \_](object-properties.md)                                                                       | Obligatoire si l’objet représente un fichier.                             |
| [\_ \_ \_ ID unique persistant de l’objet wpd \_](object-properties.md)                                     | Obligatoire.                                                             |
| [\_format d’objet wpd \_](object-properties.md)                                                                   | Obligatoire.                                                             |
| [TYPE de contenu de l' \_ objet wpd \_ \_](object-properties.md)                                                      | Obligatoire.                                                             |
| [WPD, \_ objet \_ ISHIDDEN](object-properties.md)                                                               | Obligatoire si l’objet est masqué.                                     |
| [WPD, \_ objet \_ ISSYSTEM](object-properties.md)                                                               | Obligatoire si l’objet est un objet système (représente un fichier système). |
| [taille de l' \_ objet wpd \_](object-properties.md)                                                                       | Obligatoire si l’objet a au moins une ressource.                     |
| [\_nom du \_ fichier d’origine de l’objet wpd \_ \_](object-properties.md)                                         | Obligatoire si l’objet représente un fichier.                             |
| [\_objet wpd \_ non \_ utilisable](object-properties.md)                                                  | Recommandé si l’objet n’est pas destiné à être consommé par l’appareil. |
| [\_références d’objets wpd \_](object-properties.md)                                                           | Obligatoire si l’objet a des références à d’autres objets.               |
| [\_Mots clés d’objet wpd \_](object-properties.md)                                                               | facultatif.                                                             |
| [ID de synchronisation de l' \_ objet wpd \_ \_](object-properties.md)                                                                | facultatif.                                                             |
| [l' \_ objet \_ wpd \_ est \_ protégé par DRM](object-properties.md)                                             | Obligatoire si l’objet est protégé par la technologie DRM.                |
| [Date de création de l' \_ objet wpd \_ \_](object-properties.md)                                                      | facultatif.                                                             |
| [Date de modification de l' \_ objet wpd \_ \_](object-properties.md)                                                    | Recommandé.                                                          |
| [Date de création de l' \_ objet wpd \_ \_](object-properties.md)                                                    | facultatif.                                                             |
| [\_ \_ références arrière des objets wpd \_](object-properties.md)                                                | Recommandé si l’objet a des références à d’autres objets.            |
| [\_ID d' \_ \_ objet fonctionnel \_ du conteneur d’objets wpd \_](object-properties.md)                | facultatif.                                                             |
| [\_objet wpd \_ générer une \_ miniature \_ à partir de la \_ ressource](object-properties.md)            | facultatif.                                                             |
| [l' \_ objet wpd \_ peut \_ Supprimer](object-properties.md)                                                          | Obligatoire si l’objet ne peut pas être supprimé.                             |
| [\_paramètres régionaux de la langue de l’objet wpd \_ \_](object-properties.md)                                                                           | facultatif.                                                             |
| [décalage des données de la \_ section wpd \_ \_](section-attribute-properties.md)                                           | Obligatoire.                                                             |
| [longueur des données de la \_ section wpd \_ \_](section-attribute-properties.md)                                           | Obligatoire.                                                             |
| [unités de données de la \_ section wpd \_ \_](section-attribute-properties.md)                                             | Recommandé.                                                          |
| [\_ressource d' \_ objet de référence des données \_ \_ de la section wpd \_](section-attribute-properties.md) | Recommandé.                                                          |



 

## <a name="typical-resources"></a>Ressources standard

Ces objets n’hébergent généralement pas de ressources.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Conditions requises pour les objets**](requirements-for-objects.md)
</dt> </dl>

 

 



