---
description: Objet de service
ms.assetid: 4ce4e7f7-579d-41a5-a4e1-935ba0afce83
title: Objet de service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a3aabfc4e4366c54a5d30dbe5825f178378133d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127522892"
---
# <a name="service-object"></a>Objet de service

L’objet de service doit prendre en charge les propriétés suivantes.



| Nom de la propriété                                                                                                                      | Obligatoire ou facultatif                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [\_ID d’objet wpd \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                                         | Obligatoire. .                                                                           |
| [\_ \_ ID parent de l’objet wpd \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                   | Obligatoire.                                                                             |
| [nom de l' \_ objet wpd \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                                   | Obligatoire.                                                                             |
| [\_ \_ \_ ID unique persistant de l’objet wpd \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85)) | Obligatoire.                                                                             |
| [WPD, \_ objet \_ ISHIDDEN](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                       | Obligatoire si l’objet de service ne doit pas être présenté à l’utilisateur.                       |
| [WPD, \_ objet \_ ISSYSTEM](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                       | Obligatoire si l’objet est un objet système (par exemple, il représente un fichier système). |
| [\_catégorie d' \_ objet \_ fonctionnel wpd](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))     | Obligatoire. Cela représente le type de service de l’appareil, tel que les contacts du SERVICE.          |
| [\_version du service wpd \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                       | Obligatoire.                                                                             |
| [\_type de stockage wpd \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                                | Obligatoire si le service est utilisé pour stocker des objets.                                     |
| [\_capacité de stockage wpd \_](/previous-versions/windows/hardware/drivers/ff597865(v=vs.85))                                    | Obligatoire si le service est utilisé pour stocker des objets.                                     |



 

## <a name="typical-resources"></a>Ressources standard

Ces objets n’hébergent généralement pas de ressources.

## <a name="typical-formats"></a>Formats standard

La liste suivante identifie les formats typiques utilisés par l’objet de service. Toutefois, cet objet n’est pas limité à ces formats.

-   \_format d’objet wpd \_ \_ non spécifié

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Conditions requises pour les objets**](requirements-for-objects.md)
</dt> </dl>

 

 
