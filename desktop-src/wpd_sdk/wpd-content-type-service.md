---
description: '\_service de \_ type de contenu wpd \_'
ms.assetid: 87c4c228-69e0-4b55-b91f-fe6e561f6d18
title: WPD_CONTENT_TYPE_SERVICE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fc302c8bf884b58cab092a0a0e87a79f556b3b8178df0628622e2c3a323d49f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119703919"
---
# <a name="wpd_content_type_service"></a>\_service de \_ type de contenu wpd \_

Objet qui décrit son type en tant que \_ \_ service de type de contenu wpd \_ représente un service d’appareil.

Ce type d’objet prend en charge les propriétés suivantes.



| Nom de la propriété                                                                                        | Obligatoire ou facultatif                                                           |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [\_ID d’objet wpd \_](object-properties.md)                                               | Obligatoire, en lecture seule. Un client ne peut pas définir cette propriété, même au moment de la création. |
| [\_ \_ ID parent de l’objet wpd \_](object-properties.md)                                | Obligatoire.                                                                      |
| [nom de l' \_ objet wpd \_](object-properties.md)                                           | Obligatoire si l’objet représente un fichier.                                      |
| [\_ \_ \_ ID unique persistant de l’objet wpd \_](object-properties.md)         | Obligatoire, en lecture seule. Un client ne peut pas définir cette propriété, même au moment de la création. |
| [WPD, \_ objet \_ ISHIDDEN](object-properties.md)                                   | Obligatoire si le service ne doit pas être présenté à l’utilisateur.                       |
| [WPD, \_ objet \_ ISSYSTEM](object-properties.md)                                   | Obligatoire si l’objet est un objet système (représente un fichier système).          |
| [\_catégorie d' \_ objet \_ fonctionnel wpd](object-properties.md) | Obligatoire. Cela représente le type de service de l’appareil.                             |
| [\_version du service wpd \_](object-properties.md)           | Obligatoire.                                                                      |
| [\_type de stockage wpd \_](object-properties.md)                                                          | Obligatoire si le service est utilisé pour stocker des objets.                              |
| [\_capacité de stockage wpd \_](object-properties.md)                                                      | Obligatoire si le service est utilisé pour stocker des objets.                              |



 

## <a name="typical-resources"></a>Ressources standard

Ces objets n’hébergent pas de ressources.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Conditions requises pour les objets**](requirements-for-objects.md)
</dt> </dl>

 

 



