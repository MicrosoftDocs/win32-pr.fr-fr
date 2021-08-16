---
description: '\_ \_ \_ capture vidéo de la catégorie fonctionnelle wpd \_'
ms.assetid: 3b7f7f5f-9cb7-450a-ad4c-ae1688cb7878
title: WPD_FUNCTIONAL_CATEGORY_VIDEO_CAPTURE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c1fc5879c7bf7644a785c93281eb73ffcaeba12256bb86a88b9bd41c443a674
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117842137"
---
# <a name="wpd_functional_category_video_capture"></a>\_ \_ \_ capture vidéo de la catégorie fonctionnelle wpd \_

Un \_ \_ \_ objet fonctionnel capture vidéo de la catégorie fonctionnelle wpd \_ encapsule la fonctionnalité de capture vidéo sur l’appareil, par exemple, un composant enregistreur vidéo. Une application utilise cet objet pour obtenir le contrôle par programmation.



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
| [\_Mots clés d’objet wpd \_](object-properties.md)                                                    | Facultatif.                                                                                                                                              |
| [ID de synchronisation de l' \_ objet wpd \_ \_](object-properties.md)                                                     | Facultatif.                                                                                                                                              |
| [l' \_ objet \_ wpd \_ est \_ protégé par DRM](object-properties.md)                                  | Obligatoire si l’objet est protégé par la technologie DRM.                                                                                                 |
| [Date de création de l' \_ objet wpd \_ \_](object-properties.md)                                           | Facultatif.                                                                                                                                              |
| [Date de modification de l' \_ objet wpd \_ \_](object-properties.md)                                         | Recommandé.                                                                                                                                           |
| [Date de création de l' \_ objet wpd \_ \_](object-properties.md)                                         | Facultatif.                                                                                                                                              |
| [\_ \_ références arrière des objets wpd \_](object-properties.md)                                                                | Recommandé si l’objet est référencé par un autre objet.                                                                                             |
| [\_ID d' \_ \_ objet fonctionnel \_ du conteneur d’objets wpd \_](object-properties.md)     | Facultatif.                                                                                                                                              |
| [\_objet wpd \_ générer une \_ miniature \_ à partir de la \_ ressource](object-properties.md) | Facultatif.                                                                                                                                              |
| [l' \_ objet wpd \_ peut \_ Supprimer](object-properties.md)                                                                     | Obligatoire si l’objet ne peut pas être supprimé.                                                                                                              |
| [\_paramètres régionaux de la langue de l’objet wpd \_ \_](object-properties.md)                                                                | Facultatif.                                                                                                                                              |
| [\_catégorie d' \_ objet \_ fonctionnel wpd](miscellaneous-properties.md)                      | Obligatoire. consultez [**\_ \_ \_ \_ objet fonctionnel du TYPE de contenu WPD**](wpd-content-type-functional-object.md) pour les catégories définies par Windows appareils mobiles. |



 

## <a name="typical-resources"></a>Ressources standard

Ces objets n’hébergent généralement pas de ressources.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**\_ \_ objet fonctionnel du type de contenu wpd \_ \_**](wpd-content-type-functional-object.md)
</dt> </dl>

 

 



