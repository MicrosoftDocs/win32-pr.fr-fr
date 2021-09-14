---
description: '\_document de \_ type de contenu wpd \_'
ms.assetid: c3859590-7674-4315-b171-3747e5d9350b
title: WPD_CONTENT_TYPE_DOCUMENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af8a0a902fb30eb0343a3846eaf3668a4a005a82
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404421"
---
# <a name="wpd_content_type_document"></a>\_document de \_ type de contenu wpd \_

Un objet qui décrit son type comme \_ un document de type de contenu wpd \_ \_ représente un document. par exemple, Microsoft Office fichiers Word, les fichiers de Microsoft Office Excel, les fichiers en texte brut et d’autres formats de document propriétaires.

Ce type d’objet peut héberger les propriétés suivantes.



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
| [\_Mots clés d’objet wpd \_](object-properties.md)                                                    | Optionnel.                                                                      |
| [ID de synchronisation de l' \_ objet wpd \_ \_](object-properties.md)                                                     | Optionnel.                                                                      |
| [l' \_ objet \_ wpd \_ est \_ protégé par DRM](object-properties.md)                                  | Obligatoire si l’objet est protégé par la technologie DRM.                         |
| [Date de création de l' \_ objet wpd \_ \_](object-properties.md)                                           | Optionnel.                                                                      |
| [Date de modification de l' \_ objet wpd \_ \_](object-properties.md)                                         | Recommandé.                                                                   |
| [Date de création de l' \_ objet wpd \_ \_](object-properties.md)                                         | Optionnel.                                                                      |
| [\_ \_ références arrière des objets wpd \_](object-properties.md)                                                                | Recommandé si l’objet est référencé par un autre objet.                     |
| [\_ID d' \_ \_ objet fonctionnel \_ du conteneur d’objets wpd \_](object-properties.md)     | Optionnel.                                                                      |
| [\_objet wpd \_ générer une \_ miniature \_ à partir de la \_ ressource](object-properties.md) | Optionnel.                                                                      |
| [l' \_ objet wpd \_ peut \_ Supprimer](object-properties.md)                                                                     | Obligatoire si l’objet ne peut pas être supprimé.                                      |
| [\_paramètres régionaux de la langue de l’objet wpd \_ \_](object-properties.md)                                                                | Optionnel.                                                                      |
| [URL de la \_ source du média wpd \_ \_](object-properties.md)                                                                      | Optionnel.                                                                      |
| [\_URL de \_ destination du support wpd \_](object-properties.md)                                                                 | Optionnel.                                                                      |
| [\_Description du support wpd \_](object-properties.md)                                                                      | Optionnel.                                                                      |
| [\_genre de média wpd \_](object-properties.md)                                                                            | Optionnel.                                                                      |
| [\_signet d' \_ octet \_ multimédia wpd](object-properties.md)                                                                   | Optionnel.                                                                      |
| [\_GUID du média wpd \_](object-properties.md)                                                                             | Optionnel.                                                                      |
| [\_sous- \_ \_ Description du média wpd](object-properties.md)                                                                 | Optionnel.                                                                      |
| [\_informations courantes \_ sur wpd](object-properties.md)                                                                     | Recommandé.                                                                   |
| [\_ \_ \_ texte du corps d’informations communes wpd \_](object-properties.md)                                                         | Recommandé.                                                                   |



 

## <a name="typical-resources"></a>Ressources standard

Ces objets incluent généralement les ressources suivantes.



| Nom de la ressource                                          | Obligatoire ou facultatif | Description                     |
|--------------------------------------------------------|----------------------|---------------------------------|
| [**\_ressource wpd \_ par défaut**](wpd-resource-default.md) | Obligatoire             | Contient le document physique. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Conditions requises pour les objets**](requirements-for-objects.md)
</dt> </dl>

 

 



