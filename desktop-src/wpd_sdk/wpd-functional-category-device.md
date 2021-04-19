---
description: '\_appareil de \_ catégorie \_ fonctionnelle wpd'
ms.assetid: 64b34490-1cb5-4915-ae1c-77bd4ab79ad7
title: WPD_FUNCTIONAL_CATEGORY_DEVICE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb179311af5fb3c3eef063157e3615b21eeb66a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530690"
---
# <a name="wpd_functional_category_device"></a>\_appareil de \_ catégorie \_ fonctionnelle wpd

Un \_ \_ \_ objet fonctionnel d’appareil de catégorie fonctionnelle wpd encapsule l’appareil (c’est-à-dire, l’objet le plus élevé de l’appareil). Si un appareil implémente cette catégorie fonctionnelle, il doit prendre en charge ces propriétés en plus des propriétés listées pour l' [objet périphérique](device-object.md).



| Nom de la propriété                                                                                                         | Obligatoire ou facultatif                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [\_ID d’objet wpd \_](object-properties.md)                                                                | Obligatoire, en lecture seule. Un client ne peut pas définir cette propriété, même au moment de la création.                                      |
| [\_ \_ ID parent de l’objet wpd \_](object-properties.md)                                                 | Obligatoire.                                                                                                           |
| [nom de l' \_ objet wpd \_](object-properties.md)                                                            | Obligatoire.                                                                                                           |
| [\_ \_ \_ ID unique persistant de l’objet wpd \_](object-properties.md)                          | Obligatoire, en lecture seule. Un client ne peut pas définir cette propriété, même au moment de la création.                                      |
| [\_format d’objet wpd \_](object-properties.md)                                                        | Obligatoire.                                                                                                           |
| [TYPE de contenu de l' \_ objet wpd \_ \_](object-properties.md)                                           | Obligatoire.                                                                                                           |
| [WPD, \_ objet \_ ISHIDDEN](object-properties.md)                                                    | Obligatoire si l’objet est masqué.                                                                                   |
| [WPD, \_ objet \_ ISSYSTEM](object-properties.md)                                                    | Obligatoire si l’objet est un objet système (représente un fichier système).                                               |
| [taille de l' \_ objet wpd \_](object-properties.md)                                                            | Obligatoire si l’objet a au moins une ressource.                                                                   |
| [\_nom du \_ fichier d’origine de l’objet wpd \_ \_](object-properties.md)                              | Obligatoire si l’objet représente un fichier.                                                                           |
| [\_objet wpd \_ non \_ utilisable](object-properties.md)                                       | Recommandé si l’objet n’est pas destiné à être consommé par l’appareil.                                               |
| [\_références d’objets wpd \_](object-properties.md)                                                | Obligatoire si l’objet a des références à d’autres objets.                                                             |
| [\_Mots clés d’objet wpd \_](object-properties.md)                                                    | Optionnel.                                                                                                           |
| [ID de synchronisation de l' \_ objet wpd \_ \_](object-properties.md)                                                     | Optionnel.                                                                                                           |
| [l' \_ objet \_ wpd \_ est \_ protégé par DRM](object-properties.md)                                  | Obligatoire si l’objet est protégé par la technologie DRM.                                                              |
| [Date de création de l' \_ objet wpd \_ \_](object-properties.md)                                           | Optionnel.                                                                                                           |
| [Date de modification de l' \_ objet wpd \_ \_](object-properties.md)                                         | Recommandé.                                                                                                        |
| [Date de création de l' \_ objet wpd \_ \_](object-properties.md)                                         | Optionnel.                                                                                                           |
| [\_ \_ références arrière des objets wpd \_](object-properties.md)                                                                | Recommandé si l’objet est référencé par un autre objet.                                                          |
| [\_ID d' \_ \_ objet fonctionnel \_ du conteneur d’objets wpd \_](object-properties.md)     | Optionnel.                                                                                                           |
| [\_objet wpd \_ générer une \_ miniature \_ à partir de la \_ ressource](object-properties.md) | Optionnel.                                                                                                           |
| [\_catégorie d' \_ objet \_ fonctionnel wpd](miscellaneous-properties.md)                      | Obligatoire.                                                                                                           |
| [\_partenaire de \_ synchronisation des appareils wpd \_](device-properties.md)                                           | Optionnel.                                                                                                           |
| [\_ \_ version du microprogramme de l’appareil wpd \_](device-properties.md)                                   | Obligatoire.                                                                                                           |
| [niveau de puissance de l' \_ appareil wpd \_ \_](device-properties.md)                                             | Recommandé si l’appareil dispose d’une batterie.                                                                                |
| [\_ \_ source d’alimentation de l’appareil wpd \_](device-properties.md)                                           | Recommandé.                                                                                                        |
| [\_protocole d’appareil wpd \_](device-properties.md)                                                    | Recommandé.                                                                                                        |
| [fabricant de l' \_ appareil wpd \_](device-properties.md)                                            | Obligatoire.                                                                                                           |
| [\_modèle d’appareil wpd \_](device-properties.md)                                                          | Obligatoire.                                                                                                           |
| [Numéro de série de l' \_ appareil wpd \_ \_](device-properties.md)                                         | Obligatoire.                                                                                                           |
| [l' \_ appareil wpd \_ prend en charge les appareils \_ non \_ consommables](device-properties.md)                    | Obligatoire si l’appareil prend en charge des objets non-consommables ; autrement dit, si l’appareil peut être utilisé pour le stockage de données simple. |
| [\_ \_ date/heure de l’appareil wpd](device-properties.md)                                                    | Optionnel.                                                                                                           |
| [\_ \_ nom convivial de l’appareil wpd \_](device-properties.md)                                         | Recommandé.                                                                                                        |
| [\_ \_ schémas DRM pris en charge par l’appareil wpd \_ \_](device-properties.md)                        | Recommandé si l’appareil prend en charge la technologie DRM.                                                                  |
| [\_ \_ les formats pris en charge pour les appareils wpd \_ \_ sont \_ classés](device-properties.md)       | Recommandé si l’appareil prend en charge la classification de format par défaut.                                                       |
| [\_type d’appareil wpd \_](device-properties.md)                                                            | Recommandé.                                                                                                        |



 

## <a name="typical-resources"></a>Ressources standard

Ces objets n’hébergent généralement pas de ressources.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**\_ \_ objet fonctionnel du type de contenu wpd \_ \_**](wpd-content-type-functional-object.md)
</dt> </dl>

 

 



