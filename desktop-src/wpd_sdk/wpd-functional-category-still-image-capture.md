---
description: "\\_capture d' \\_ \\_ image continue \\_ de la catégorie fonctionnelle wpd \\_"
ms.assetid: fb434927-1548-4c6e-bfb7-3a99eef62a4a
title: WPD_FUNCTIONAL_CATEGORY_STILL_IMAGE_CAPTURE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88d821f1182012fbf29960fae4fc06b14ec53ecb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195791"
---
# <a name="wpd_functional_category_still_image_capture"></a>\_capture d' \_ \_ image continue \_ de la catégorie fonctionnelle wpd \_

Un \_ \_ \_ objet fonctionnel de capture d’image continue de catégorie fonctionnelle wpd \_ \_ encapsule la fonctionnalité de capture d’image continue sur un appareil, comme une caméra ou une pièce jointe d’appareil photo.



| Nom de la propriété                                                                                                            | Obligatoire ou facultatif                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_ID d’objet wpd \_](object-properties.md)                                                                   | Obligatoire, en lecture seule. Un client ne peut pas définir cette propriété, même au moment de la création.                                                                         |
| [\_ \_ ID parent de l’objet wpd \_](object-properties.md)                                                    | Obligatoire.                                                                                                                                              |
| [nom de l' \_ objet wpd \_](object-properties.md)                                                               | Obligatoire.                                                                                                                                              |
| [\_ \_ \_ ID unique persistant de l’objet wpd \_](object-properties.md)                             | Obligatoire, en lecture seule. Un client ne peut pas définir cette propriété, même au moment de la création.                                                                         |
| [\_format d’objet wpd \_](object-properties.md)                                                           | Obligatoire.                                                                                                                                              |
| [TYPE de contenu de l' \_ objet wpd \_ \_](object-properties.md)                                              | Obligatoire.                                                                                                                                              |
| [WPD, \_ objet \_ ISHIDDEN](object-properties.md)                                                       | Obligatoire si l’objet est masqué.                                                                                                                      |
| [WPD, \_ objet \_ ISSYSTEM](object-properties.md)                                                       | Obligatoire si l’objet est un objet système (représente un fichier système).                                                                                  |
| [taille de l' \_ objet wpd \_](object-properties.md)                                                               | Obligatoire si l’objet a au moins une ressource.                                                                                                      |
| [\_nom du \_ fichier d’origine de l’objet wpd \_ \_](object-properties.md)                                 | Obligatoire si l’objet représente un fichier.                                                                                                              |
| [\_objet wpd \_ non \_ utilisable](object-properties.md)                                          | Recommandé si l’objet n’est pas destiné à être consommé par l’appareil.                                                                                  |
| [\_références d’objets wpd \_](object-properties.md)                                                   | Obligatoire si l’objet a des références à d’autres objets.                                                                                                |
| [\_Mots clés d’objet wpd \_](object-properties.md)                                                       | Optionnel.                                                                                                                                              |
| [ID de synchronisation de l' \_ objet wpd \_ \_](object-properties.md)                                                        | Optionnel.                                                                                                                                              |
| [l' \_ objet \_ wpd \_ est \_ protégé par DRM](object-properties.md)                                     | Obligatoire si l’objet est protégé par la technologie DRM.                                                                                                 |
| [Date de création de l' \_ objet wpd \_ \_](object-properties.md)                                              | Optionnel.                                                                                                                                              |
| [Date de modification de l' \_ objet wpd \_ \_](object-properties.md)                                            | Recommandé.                                                                                                                                           |
| [Date de création de l' \_ objet wpd \_ \_](object-properties.md)                                            | Optionnel.                                                                                                                                              |
| [\_ \_ références arrière des objets wpd \_](object-properties.md)                                                                   | Recommandé si l’objet est référencé par un autre objet.                                                                                             |
| [\_ID d' \_ \_ objet fonctionnel \_ du conteneur d’objets wpd \_](object-properties.md)        | Optionnel.                                                                                                                                              |
| [\_objet wpd \_ générer une \_ miniature \_ à partir de la \_ ressource](object-properties.md)    | Optionnel.                                                                                                                                              |
| [l' \_ objet wpd \_ peut \_ Supprimer](object-properties.md)                                                                        | Obligatoire si l’objet ne peut pas être supprimé.                                                                                                              |
| [\_paramètres régionaux de la langue de l’objet wpd \_ \_](object-properties.md)                                                                   | Optionnel.                                                                                                                                              |
| [\_catégorie d' \_ objet \_ fonctionnel wpd](miscellaneous-properties.md)                         | Obligatoire. consultez [**\_ \_ \_ \_ objet fonctionnel du TYPE de contenu WPD**](wpd-content-type-functional-object.md) pour les catégories définies par Windows appareils mobiles. |
| [\_résolution de \_ capture d’images wpd toujours \_ \_](still-image-properties.md)                  | Obligatoire.                                                                                                                                              |
| [\_format de \_ capture d’images wpd toujours \_ \_](still-image-properties.md)                          | Obligatoire.                                                                                                                                              |
| [\_paramètre de \_ compression d’image wpd Still \_ \_](still-image-properties.md)                | Optionnel.                                                                                                                                              |
| [\_ \_ équilibrer l’image d’images wpd toujours \_ \_](still-image-properties.md)                            | Optionnel.                                                                                                                                              |
| [\_ \_ gain RVB d’image toujours \_ wpd \_](still-image-properties.md)                                      | Optionnel.                                                                                                                                              |
| [\_FNUMBER d' \_ image de l’API WPD \_](still-image-properties.md)                                         | Optionnel.                                                                                                                                              |
| [\_ \_ longueur focale d’image toujours \_ wpd \_](still-image-properties.md)                              | Optionnel.                                                                                                                                              |
| [la \_ \_ distance de \_ focus \_ de l’image de wpd est toujours](still-image-properties.md)                          | Optionnel.                                                                                                                                              |
| [WPD \_ toujours \_ \_ le \_ mode focus de l’image](still-image-properties.md)                                  | Optionnel.                                                                                                                                              |
| [le \_ mode de contrôle de l’exposition des images wpd continue \_ \_ \_ \_](still-image-properties.md)         | Optionnel.                                                                                                                                              |
| [WPD \_ - \_ image \_ toujours \_ en mode flash](still-image-properties.md)                                  | Optionnel.                                                                                                                                              |
| [heure d’exposition de l' \_ image wpd toujours \_ \_ \_](still-image-properties.md)                            | Optionnel.                                                                                                                                              |
| [le \_ \_ mode de \_ programme d’exposition des images wpd \_ continue \_](still-image-properties.md)           | Optionnel.                                                                                                                                              |
| [INDEX d’exposition de l' \_ \_ image de l' \_ API WPD \_](still-image-properties.md)                          | Optionnel.                                                                                                                                              |
| [correction du décalage de l’exposition de l' \_ image wpd continue \_ \_ \_ \_](still-image-properties.md) | Optionnel.                                                                                                                                              |
| [\_ \_ retardement de capture d’image wpd \_ \_](still-image-properties.md)                            | Optionnel.                                                                                                                                              |
| [\_mode de \_ capture d’image toujours \_ wpd \_](still-image-properties.md)                              | Optionnel.                                                                                                                                              |
| [le \_ \_ contraste des images wpd continue \_](still-image-properties.md)                                       | Optionnel.                                                                                                                                              |
| [la \_ \_ netteté de l’image wpd est toujours \_](still-image-properties.md)                                     | Optionnel.                                                                                                                                              |
| [réinitialisation du \_ \_ \_ Zoom numérique d’images wpd \_](still-image-properties.md)                              | Optionnel.                                                                                                                                              |
| [WPD \_ - \_ \_ mode d’effet d’image continue \_](still-image-properties.md)                                | Optionnel.                                                                                                                                              |
| [\_nombre de \_ \_ rafales d’images fixes wpd \_](still-image-properties.md)                              | Optionnel.                                                                                                                                              |
| [\_intervalle de \_ \_ rafales d’images fixes pour wpd \_](still-image-properties.md)                          | Optionnel.                                                                                                                                              |
| [\_TIMELAPSE images wpd toujours- \_ \_ \_ nombre](still-image-properties.md)                      | Optionnel.                                                                                                                                              |
| [\_intervalle de \_ TIMELAPSE d’image toujours \_ wpd \_](still-image-properties.md)                  | Optionnel.                                                                                                                                              |
| [\_ \_ \_ le \_ mode de contrôle du focus \_ de l’image wpd continue](still-image-properties.md)               | Optionnel.                                                                                                                                              |
| [\_URL de \_ chargement d’image wpd toujours \_ \_](still-image-properties.md)                                  | Optionnel.                                                                                                                                              |
| [l' \_ \_ artiste d’images fixes wpd \_](still-image-properties.md)                                           | Optionnel.                                                                                                                                              |



 

## <a name="typical-resources"></a>Ressources standard

Ces objets n’hébergent généralement pas de ressources.

La plupart de ces propriétés ont des effets interconnectés. Par exemple, si **le \_ \_ mode de \_ \_ contrôle \_** de l’exposition de l’image wpd est défini sur automatique, alors l’indicateur f-stop, le temps d’exposition et le compteur d’exposition sont liés ; en d’autres cas, les autres seront différents.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**\_ \_ objet fonctionnel du type de contenu wpd \_ \_**](wpd-content-type-functional-object.md)
</dt> </dl>

 

 



