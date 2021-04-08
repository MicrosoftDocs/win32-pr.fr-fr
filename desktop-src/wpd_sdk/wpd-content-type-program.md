---
description: '\_programme de \_ type de contenu wpd \_'
ms.assetid: 81eaf8cf-0f4f-4587-911a-063630af1c8e
title: WPD_CONTENT_TYPE_PROGRAM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0187d4e87f47e8210e94a676ca9ccd1e1364cf1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758439"
---
# <a name="wpd_content_type_program"></a>\_programme de \_ type de contenu wpd \_

Un objet qui décrit son type comme \_ un programme de type de contenu wpd \_ \_ représente un programme exécutable.

Ce type d’objet prend en charge les propriétés suivantes.



|                                                                                                                       |                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| **Nom de la propriété**                                                                                                     | **Obligatoire ou facultatif**                                                           |
| [\_ID d’objet wpd \_](object-properties.md)                                                                | Obligatoire, mais en lecture seule. Un client ne peut pas définir cette propriété, même au moment de la création. |
| [\_ \_ ID parent de l’objet wpd \_](object-properties.md)                                                 | Obligatoire.                                                                          |
| [nom de l' \_ objet wpd \_](object-properties.md)                                                            | Obligatoire si l’objet représente un fichier.                                          |
| [\_ \_ \_ ID unique persistant de l’objet wpd \_](object-properties.md)                          | Obligatoire, en lecture seule. Un client ne peut pas définir cette propriété même au moment de la création.      |
| [\_format d’objet wpd \_](object-properties.md)                                                        | Obligatoire.                                                                          |
| [TYPE de contenu de l' \_ objet wpd \_ \_](object-properties.md)                                           | Obligatoire.                                                                          |
| [WPD, \_ objet \_ ISHIDDEN](object-properties.md)                                                    | Obligatoire si l’objet est masqué.                                                  |
| [WPD, \_ objet \_ ISSYSTEM](object-properties.md)                                                    | Obligatoire si l’objet est un objet système (représente un fichier système).              |
| [taille de l' \_ objet wpd \_](object-properties.md)                                                            | Obligatoire si l’objet a au moins une ressource.                                  |
| [\_nom du \_ fichier d’origine de l’objet wpd \_ \_](object-properties.md)                              | Obligatoire si l’objet représente un fichier.                                          |
| [\_objet wpd \_ non \_ utilisable](object-properties.md)                                       | Recommandé si l’objet n’est pas destiné à être consommé par l’appareil.              |
| [\_références d’objets wpd \_](object-properties.md)                                                | Obligatoire si l’objet a des références à d’autres objets.                            |
| [\_Mots clés d’objet wpd \_](object-properties.md)                                                    | Optionnel.                                                                          |
| [ID de synchronisation de l' \_ objet wpd \_ \_](object-properties.md)                                                     | Optionnel.                                                                          |
| [l' \_ objet \_ wpd \_ est \_ protégé par DRM](object-properties.md)                                  | Obligatoire si l’objet est protégé par la technologie DRM.                             |
| [Date de création de l' \_ objet wpd \_ \_](object-properties.md)                                           | Optionnel.                                                                          |
| [Date de modification de l' \_ objet wpd \_ \_](object-properties.md)                                         | Recommandé.                                                                       |
| [Date de création de l' \_ objet wpd \_ \_](object-properties.md)                                         | Optionnel.                                                                          |
| [\_ \_ références arrière des objets wpd \_](object-properties.md)                                                                | Recommandé si l’objet est référencé par un autre objet.                         |
| [\_ID d' \_ \_ objet fonctionnel \_ du conteneur d’objets wpd \_](object-properties.md)     | Optionnel.                                                                          |
| [\_objet wpd \_ générer une \_ miniature \_ à partir de la \_ ressource](object-properties.md) | Optionnel.                                                                          |
| [l' \_ objet wpd \_ peut \_ Supprimer](object-properties.md)                                                                     | Obligatoire si l’objet ne peut pas être supprimé.                                          |
| [\_paramètres régionaux de la langue de l’objet wpd \_ \_](object-properties.md)                                                                | Optionnel.                                                                          |



 

## <a name="typical-resources"></a>Ressources standard

Ces objets incluent généralement les ressources suivantes.



| Nom de la ressource                                          | Obligatoire ou facultatif | Description                |
|--------------------------------------------------------|----------------------|----------------------------|
| [**\_ressource wpd \_ par défaut**](wpd-resource-default.md) | Obligatoire.            | Contient le fichier programme. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Conditions requises pour les objets**](requirements-for-objects.md)
</dt> </dl>

 

 



