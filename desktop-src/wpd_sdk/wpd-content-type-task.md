---
description: '\_tâche de \_ type de contenu wpd \_'
ms.assetid: 503d0b11-2113-4df4-8b6b-250f24d09b1f
title: WPD_CONTENT_TYPE_TASK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d42761fa8cbd96b4ce5b4085544906d2333b9d1317181b397140468145a4b37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118193533"
---
# <a name="wpd_content_type_task"></a>\_tâche de \_ type de contenu wpd \_

Un objet qui décrit son type de \_ tâche de \_ type de contenu wpd \_ représente une tâche, telle qu’un élément dans une liste de tâches.

Ce type d’objet prend en charge les propriétés suivantes.



| Nom de la propriété       | Obligatoire ou facultatif         |
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
| [l' \_ objet wpd \_ peut \_ Supprimer](object-properties.md)                                                                     | Obligatoire si l’objet ne peut pas être supprimé.                                      |
| [\_paramètres régionaux de la langue de l’objet wpd \_ \_](object-properties.md)                                                                | Facultatif.                                                                      |
| [\_objet d' \_ informations \_ communes wpd](object-properties.md)                                                            | Obligatoire.                                                                      |
| [\_ \_ \_ texte du corps d’informations communes wpd \_](object-properties.md)                                                         | Recommandé.                                                                   |
| [\_priorité des \_ informations \_ communes wpd](object-properties.md)                                                           | Recommandé.                                                                   |
| [\_date et \_ \_ heure de début des informations communes wpd \_](object-properties.md)                                                    | Recommandé.                                                                   |
| [\_date et \_ \_ heure de fin des informations communes wpd \_](object-properties.md)                                                      | Recommandé.                                                                   |
| [\_Notes d' \_ informations \_ communes wpd](object-properties.md)                                                              | Facultatif.                                                                      |
| [État de la \_ tâche wpd \_](task-properties.md)                                                              | Facultatif.                                                                      |
| [pourcentage d’achèvement de la \_ tâche wpd \_ \_](task-properties.md)                                         | Facultatif.                                                                      |
| [Date du rappel de la \_ tâche wpd \_ \_](task-properties.md)                                               | Facultatif.                                                                      |
| [propriétaire de la \_ tâche wpd \_](task-properties.md)                                                                | Facultatif.                                                                      |



 

## <a name="typical-resources"></a>Ressources standard

Ces objets n’hébergent généralement pas de ressources.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Conditions requises pour les objets**](requirements-for-objects.md)
</dt> </dl>

 

 



