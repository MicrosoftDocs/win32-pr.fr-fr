---
description: '\_type de contenu wpd \_ \_ tout'
ms.assetid: 99f9382d-9bfe-4cf6-982f-fcd37e965cae
title: WPD_CONTENT_TYPE_ALL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66523f18d563d7a2ba04e38da2ad760ab39eb307f2f71fac20119ec491a5934a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006099"
---
# <a name="wpd_content_type_all"></a>\_type de contenu wpd \_ \_ tout

Ce type de contenu est valide uniquement en tant que paramètre et n’est pas un type de contenu signalé par le pilote. Cela permet à votre application de poser des questions sur tous les types d’objets.

Si vous concevez un objet personnalisé, il doit au moins prendre en charge ces propriétés.



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
| [l' \_ objet \_ wpd \_ est \_ protégé par DRM](object-properties.md)                                  | Obligatoire si l’objet est protégé par la technologie de gestion des droits numériques (DRM). |
| [Date de création de l' \_ objet wpd \_ \_](object-properties.md)                                           | Facultatif.                                                                          |
| [Date de modification de l' \_ objet wpd \_ \_](object-properties.md)                                         | Recommandé.                                                                       |
| [Date de création de l' \_ objet wpd \_ \_](object-properties.md)                                         | Facultatif.                                                                          |
| [\_ \_ références arrière des objets wpd \_](object-properties.md)                                                                | Recommandé si l’objet est référencé par un autre objet.                         |
| [\_ID d' \_ \_ objet fonctionnel \_ du conteneur d’objets wpd \_](object-properties.md)     | Facultatif.                                                                          |
| [\_objet wpd \_ générer une \_ miniature \_ à partir de la \_ ressource](object-properties.md) | Facultatif.                                                                          |
| [l' \_ objet wpd \_ peut \_ Supprimer](object-properties.md)                                                                     | Obligatoire si l’objet ne peut pas être supprimé.                                          |
| [\_paramètres régionaux de la langue de l’objet wpd \_ \_](object-properties.md)                                                                | Facultatif.                                                                          |



 

## <a name="typical-resources"></a>Ressources standard

Ces objets n’hébergent généralement pas de ressources.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Conditions requises pour les objets**](requirements-for-objects.md)
</dt> </dl>

 

 



