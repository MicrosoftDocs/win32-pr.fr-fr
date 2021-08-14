---
description: '\_ \_ rendez-vous de type de contenu wpd \_'
ms.assetid: d41c26ef-9f51-4ba7-b1a4-57abec91925e
title: WPD_CONTENT_TYPE_APPOINTMENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 159f80246b14c121e386f1122a70dce27e717481ec02897c06b9061821a8c0fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118193543"
---
# <a name="wpd_content_type_appointment"></a>\_ \_ rendez-vous de type de contenu wpd \_

Objet qui décrit son type comme \_ \_ \_ un rendez-vous de type de contenu wpd représente un rendez-vous dans un calendrier.

Ce type d’objet prend en charge les propriétés suivantes.



| Nom de la propriété                                                                                                         | Obligatoire ou facultatif                                                           |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [\_ID d’objet wpd \_](object-properties.md)                                                                | Obligatoire, en lecture seule. Un client ne peut pas définir cette propriété, même au moment de la création. |
| [\_ \_ ID parent de l’objet wpd \_](object-properties.md)                                                 | Obligatoire.                                                                      |
| [nom de l' \_ objet wpd \_](object-properties.md)                                                            | Obligatoire si l’objet représente un fichier.                                      |
| [\_ \_ \_ ID unique persistant de l’objet wpd \_](object-properties.md)                          | Obligatoire, en lecture seule. Un client ne peut pas définir cette propriété, même au moment de la création. |
| [\_format d’objet wpd \_](object-properties.md)                                                        | Obligatoire.                                                                      |
| [TYPE de contenu de l' \_ objet wpd \_ \_](object-properties.md)                                           | Obligatoire.                                                                      |
| [WPD, \_ objet \_ ISHIDDEN](object-properties.md)                                                    | Obligatoire si l’objet est masqué.                                              |
| [WPD, \_ objet \_ ISSYSTEM](object-properties.md)                                                    | Obligatoire si l’objet est un objet système (représente un fichier système).          |
| [taille de l' \_ objet wpd \_](object-properties.md)                                                            | Obligatoire si l’objet a au moins une ressource.                              |
| [\_nom du \_ fichier d’origine de l’objet wpd \_ \_](object-properties.md)                              | Obligatoire si l’objet représente un fichier.                                      |
| [\_objet wpd \_ non \_ utilisable](object-properties.md)                                       | Recommandé si l’objet n’est pas destiné à être consommé par l’appareil.          |
| [\_références d’objets wpd \_](object-properties.md)                                                | Obligatoire si l’objet a des références à d’autres objets.                        |
| [\_Mots clés d’objet wpd \_](object-properties.md)                                                    | Facultatif.                                                                      |
| [ID de synchronisation de l' \_ objet wpd \_ \_](object-properties.md)                                                     | Facultatif.                                                                      |
| [l' \_ objet \_ wpd \_ est \_ protégé par DRM](object-properties.md)                                  | Obligatoire si l’objet est protégé par la technologie DRM.                         |
| [Date de création de l' \_ objet wpd \_ \_](object-properties.md)                                           | Facultatif.                                                                      |
| [Date de modification de l' \_ objet wpd \_ \_](object-properties.md)                                         | Recommandé.                                                                   |
| [Date de création de l' \_ objet wpd \_ \_](object-properties.md)                                         | Facultatif.                                                                      |
| [\_ \_ références arrière des objets wpd \_](object-properties.md)                                                                | Recommandé si l’objet est référencé par un autre objet.                     |
| [\_ID d' \_ \_ objet fonctionnel \_ du conteneur d’objets wpd \_](object-properties.md)     | Facultatif.                                                                      |
| [\_objet wpd \_ générer une \_ miniature \_ à partir de la \_ ressource](object-properties.md) | Facultatif.                                                                      |
| [\_emplacement du rendez-vous wpd \_](appointment-properties.md)                                     | Obligatoire.                                                                      |
| [l' \_ objet wpd \_ peut \_ Supprimer](object-properties.md)                                                                     | Obligatoire si l’objet peut être supprimé.                                         |
| [\_paramètres régionaux de la langue de l’objet wpd \_ \_](object-properties.md)                                                                | Facultatif.                                                                      |
| [\_objet d' \_ informations \_ communes wpd](object-properties.md)                                                            | Obligatoire.                                                                      |
| [\_ \_ \_ texte du corps d’informations communes wpd \_](object-properties.md)                                                         | Recommandé.                                                                   |
| [\_priorité des \_ informations \_ communes wpd](object-properties.md)                                                           | Recommandé.                                                                   |
| [\_date et \_ \_ heure de début des informations communes wpd \_](object-properties.md)                                                    | Recommandé.                                                                   |
| [\_date et \_ \_ heure de fin des informations communes wpd \_](object-properties.md)                                                      | Recommandé.                                                                   |
| [\_Notes d' \_ informations \_ communes wpd](object-properties.md)                                                              | Facultatif.                                                                      |
| [\_emplacement du rendez-vous wpd \_](object-properties.md)                                                                   | Obligatoire.                                                                      |
| [\_type de rendez-vous wpd \_](appointment-properties.md)                                             | Facultatif.                                                                      |
| [participants obligatoires à un \_ rendez-vous \_ \_](appointment-properties.md)                | Facultatif.                                                                      |
| [\_ \_ participants facultatifs RENDus wpd \_](appointment-properties.md)                | Facultatif.                                                                      |
| [participants à un \_ rendez-vous \_ accepté par wpd \_](appointment-properties.md)                | Facultatif.                                                                      |
| [\_ressources de rendez-vous wpd \_](appointment-properties.md)                                   | Facultatif.                                                                      |



 

## <a name="typical-resources"></a>Ressources standard

Ces objets n’hébergent généralement pas de ressources.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Conditions requises pour les objets**](requirements-for-objects.md)
</dt> </dl>

 

 



