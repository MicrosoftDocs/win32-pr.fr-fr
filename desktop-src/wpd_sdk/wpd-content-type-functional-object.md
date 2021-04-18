---
description: '\_ \_ objet fonctionnel du type de contenu wpd \_ \_'
ms.assetid: 112de70b-afcc-4fba-b74f-c33bd759d517
title: WPD_CONTENT_TYPE_FUNCTIONAL_OBJECT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8516d29bf08b4873dc80c72b9a23de19dc50d0e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520096"
---
# <a name="wpd_content_type_functional_object"></a>\_ \_ objet fonctionnel du type de contenu wpd \_ \_

Objet qui décrit son type en tant qu' \_ objet fonctionnel du contenu wpd \_ \_ représente un objet fonctionnel, en encapsulant les fonctionnalités de l’appareil.

Tous les objets fonctionnels, quel que soit le type, prennent en charge les propriétés suivantes. (Si vous définissez un objet fonctionnel personnalisé, il doit également prendre en charge ces propriétés.)



| Nom de la propriété                                                                                                         | Obligatoire ou facultatif                                                                  |
|-----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [\_ID d’objet wpd \_](object-properties.md)                                                                | Obligatoire, en lecture seule. Un client ne peut pas définir cette propriété, même au moment de la création.        |
| [\_ \_ ID parent de l’objet wpd \_](object-properties.md)                                                 | Obligatoire.                                                                             |
| [nom de l' \_ objet wpd \_](object-properties.md)                                                            | Obligatoire.                                                                             |
| [\_ \_ \_ ID unique persistant de l’objet wpd \_](object-properties.md)                          | Obligatoire, en lecture seule. Un client ne peut pas définir cette propriété, même au moment de la création.        |
| [\_format d’objet wpd \_](object-properties.md)                                                        | Obligatoire.                                                                             |
| [TYPE de contenu de l' \_ objet wpd \_ \_](object-properties.md)                                           | Obligatoire.                                                                             |
| [WPD, \_ objet \_ ISHIDDEN](object-properties.md)                                                    | Obligatoire si l’objet est masqué.                                                     |
| [WPD, \_ objet \_ ISSYSTEM](object-properties.md)                                                    | Obligatoire si l’objet est un objet système (représente un fichier système).                 |
| [taille de l' \_ objet wpd \_](object-properties.md)                                                            | Obligatoire si l’objet a au moins une ressource.                                     |
| [\_nom du \_ fichier d’origine de l’objet wpd \_ \_](object-properties.md)                              | Obligatoire si l’objet représente un fichier.                                             |
| [\_objet wpd \_ non \_ utilisable](object-properties.md)                                       | Recommandé si l’objet n’est pas destiné à être consommé par l’appareil.                 |
| [\_références d’objets wpd \_](object-properties.md)                                                | Obligatoire si l’objet a des références à d’autres objets.                               |
| [\_Mots clés d’objet wpd \_](object-properties.md)                                                    | Optionnel.                                                                             |
| [ID de synchronisation de l' \_ objet wpd \_ \_](object-properties.md)                                                     | Optionnel.                                                                             |
| [l' \_ objet \_ wpd \_ est \_ protégé par DRM](object-properties.md)                                  | Obligatoire si l’objet est protégé par la technologie DRM.                                |
| [Date de création de l' \_ objet wpd \_ \_](object-properties.md)                                           | Optionnel.                                                                             |
| [Date de modification de l' \_ objet wpd \_ \_](object-properties.md)                                         | Recommandé.                                                                          |
| [Date de création de l' \_ objet wpd \_ \_](object-properties.md)                                         | Optionnel.                                                                             |
| [\_ \_ références arrière des objets wpd \_](object-properties.md)                                                                | Recommandé si l’objet est référencé par un autre objet.                            |
| [\_ID d' \_ \_ objet fonctionnel \_ du conteneur d’objets wpd \_](object-properties.md)     | Optionnel.                                                                             |
| [\_objet wpd \_ générer une \_ miniature \_ à partir de la \_ ressource](object-properties.md) | Optionnel.                                                                             |
| [l' \_ objet wpd \_ peut \_ Supprimer](object-properties.md)                                                                     | Obligatoire si l’objet ne peut pas être supprimé.                                             |
| [\_paramètres régionaux de la langue de l’objet wpd \_ \_](object-properties.md)                                                                | Optionnel.                                                                             |
| [\_catégorie d' \_ objet \_ fonctionnel wpd](miscellaneous-properties.md)                      | Obligatoire. Consultez le tableau suivant pour les catégories définies par les appareils mobiles Windows. |



 

## <a name="typical-resources"></a>Ressources standard

Ces objets n’hébergent généralement pas de ressources.

## <a name="functional-object-categories"></a>Catégories d’objets fonctionnels

Les objets fonctionnels peuvent être regroupés en catégories, en fonction de leurs fonctions. Une catégorie est décrite par la propriété de la \_ catégorie d’objet fonctionnel wpd \_ \_ (valeur Guid). La catégorie détermine les propriétés supplémentaires qui sont prises en charge.

Le tableau suivant décrit les catégories définies par les appareils mobiles Windows. Consultez la description de la catégorie pour connaître les propriétés et ressources supplémentaires prises en charge par l’objet.



| Catégorie fonctionnelle                                                                                        | Description                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**la \_ catégorie fonctionnelle wpd \_ \_ tout**](wpd-functional-category-all.md)                                      | Cette catégorie fonctionnelle est valide uniquement en tant que paramètre pour certaines fonctions de requête (pour indiquer que tous les types d’objets fonctionnels sont acceptables) et n’est pas une catégorie fonctionnelle signalée par le pilote. |
| [**\_ \_ \_ capture audio de la catégorie fonctionnelle wpd \_**](wpd-functional-category-audio-capture.md)                 | L’objet encapsule la fonctionnalité de capture audio sur l’appareil, par exemple, un enregistreur vocal ou tout autre composant d’enregistrement audio.                                                                      |
| [**\_appareil de \_ catégorie \_ fonctionnelle wpd**](wpd-functional-category-device.md)                                | L’objet encapsule l’appareil (autrement dit, l’objet le plus élevé de l’appareil).                                                                                                                          |
| [**\_ \_ \_ Configuration réseau de la catégorie fonctionnelle wpd \_**](wpd-functional-category-network-configuration.md) | L’objet encapsule les fonctionnalités de configuration réseau pour l’appareil, par exemple des profils Wi-Fi ou des partenariats.                                                                                   |
| [**informations de rendu de la \_ catégorie fonctionnelle wpd \_ \_ \_**](wpd-functional-category-rendering-information.md) | L’objet décrit les types de fichiers multimédias que l’appareil est en mesure de lire.                                                                                                                            |
| [**\_catégorie fonctionnelle \_ wpd \_ SMS**](wpd-functional-category-sms.md)                                      | L’objet encapsule la fonctionnalité Short Message Service (communément appelée « messagerie texte ») sur l’appareil.                                                                                             |
| [**\_capture d' \_ \_ image continue \_ de la catégorie fonctionnelle wpd \_**](wpd-functional-category-still-image-capture.md)    | L’objet encapsule la fonctionnalité de capture d’image continue sur un appareil, tel qu’une caméra ou une pièce jointe d’appareil photo.                                                                                              |
| [**\_stockage des \_ catégories FONCTIONNELLEs wpd \_**](wpd-functional-category-storage.md)                              | L’objet encapsule le stockage de fichier physique sur l’appareil.                                                                                                                                              |
| [**\_ \_ \_ capture vidéo de la catégorie fonctionnelle wpd \_**](wpd-functional-category-video-capture.md)                 | L’objet encapsule la fonctionnalité de capture vidéo sur l’appareil, par exemple, un composant d’enregistreur vidéo. Une application utilise cet objet pour obtenir le contrôle par programmation.                                 |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Conditions requises pour les objets**](requirements-for-objects.md)
</dt> </dl>

 

 



