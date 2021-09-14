---
description: '\_stockage des \_ catégories FONCTIONNELLEs wpd \_'
ms.assetid: 92a10de6-3e50-4042-a9b7-3c1d5944791f
title: WPD_FUNCTIONAL_CATEGORY_STORAGE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f3000c63207286bc1dae153e3f930231909e92f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127234414"
---
# <a name="wpd_functional_category_storage"></a>\_stockage des \_ catégories FONCTIONNELLEs wpd \_

Un \_ \_ objet fonctionnel de stockage de catégorie fonctionnelle wpd \_ encapsule le stockage de fichier physique sur l’appareil.



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
| [\_Mots clés d’objet wpd \_](object-properties.md)                                                    | Optionnel.                                                                                                                                              |
| [ID de synchronisation de l' \_ objet wpd \_ \_](object-properties.md)                                                     | Optionnel.                                                                                                                                              |
| [l' \_ objet \_ wpd \_ est \_ protégé par DRM](object-properties.md)                                  | Obligatoire si l’objet est protégé par la technologie DRM.                                                                                                 |
| [Date de création de l' \_ objet wpd \_ \_](object-properties.md)                                           | Optionnel.                                                                                                                                              |
| [Date de modification de l' \_ objet wpd \_ \_](object-properties.md)                                         | Recommandé.                                                                                                                                           |
| [Date de création de l' \_ objet wpd \_ \_](object-properties.md)                                         | Optionnel.                                                                                                                                              |
| [\_ \_ références arrière des objets wpd \_](object-properties.md)                                                                | Recommandé si l’objet est référencé par un autre objet.                                                                                             |
| [\_ID d' \_ \_ objet fonctionnel \_ du conteneur d’objets wpd \_](object-properties.md)     | Optionnel.                                                                                                                                              |
| [\_objet wpd \_ générer une \_ miniature \_ à partir de la \_ ressource](object-properties.md) | Optionnel.                                                                                                                                              |
| [l' \_ objet wpd \_ peut \_ Supprimer](object-properties.md)                                                                     | Obligatoire si l’objet ne peut pas être supprimé.                                                                                                              |
| [\_paramètres régionaux de la langue de l’objet wpd \_ \_](object-properties.md)                                                                | Optionnel.                                                                                                                                              |
| [\_catégorie d' \_ objet \_ fonctionnel wpd](miscellaneous-properties.md)                      | Obligatoire. consultez [**\_ \_ \_ \_ objet fonctionnel du TYPE de contenu WPD**](wpd-content-type-functional-object.md) pour les catégories définies par Windows appareils mobiles. |
| [\_type de stockage wpd \_](storage-properties.md)                                                         | Obligatoire.                                                                                                                                              |
| [\_type de \_ système de fichiers de stockage wpd \_ \_](storage-properties.md)                               | facultatif.                                                                                                                                              |
| [\_capacité de stockage wpd \_](storage-properties.md)                                                 | Obligatoire.                                                                                                                                              |
| [\_ \_ espace libre de stockage wpd \_ \_ en \_ octets](storage-properties.md)                        | facultatif.                                                                                                                                              |
| [\_ \_ espace libre de stockage wpd \_ dans les \_ \_ objets](storage-properties.md)                    | Optionnel.                                                                                                                                              |
| [\_Description du stockage wpd \_](storage-properties.md)                                           | Optionnel.                                                                                                                                              |
| [\_numéro de \_ série du stockage wpd \_](storage-properties.md)                                      | Optionnel.                                                                                                                                              |



 

## <a name="typical-resources"></a>Ressources standard

Ces objets incluent généralement les ressources suivantes.



| Nom de la ressource                                    | Obligatoire ou facultatif | Description                                        |
|--------------------------------------------------|----------------------|----------------------------------------------------|
| [**\_icône de ressource wpd \_**](wpd-resource-icon.md) | facultatif.            | Contient la représentation d’icône pour ce stockage. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**\_ \_ objet fonctionnel du type de contenu wpd \_ \_**](wpd-content-type-functional-object.md)
</dt> </dl>

 

 



