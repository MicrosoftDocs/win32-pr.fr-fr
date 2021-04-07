---
title: Actions et droits
description: Actions et droits
ms.assetid: 711c6a04-6c40-4ea5-8c4f-91d000286b7b
keywords:
- Kit de développement logiciel (SDK) Windows Media format, gestion des droits numériques (DRM)
- Windows Media Format SDK, licences DRM
- Windows Media Format SDK, licences pour DRM
- gestion des droits numériques (DRM), actions
- DRM (gestion des droits numériques), actions
- gestion des droits numériques (DRM), droits
- DRM (gestion des droits numériques), droits
- gestion des droits numériques (DRM), licences
- DRM (gestion des droits numériques), licences
- licences, DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1d044850bb5ee73e804065c67840362ec0b7b0d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028678"
---
# <a name="actions-and-rights"></a>Actions et droits

Lorsqu’un fichier est protégé à l’aide de Windows Media DRM, son utilisation est complètement restreinte. Les licences peuvent être émises pour permettre à un utilisateur d’utiliser le contenu de manière spécifique. Chaque méthode dans laquelle un utilisateur peut utiliser le contenu est décrite par une action. Par exemple, la réexécution d’un fichier sur un ordinateur est une action.

Une licence qui permet d’effectuer une action donnée est dite d’accorder un droit. Par exemple, une licence peut accorder le droit de lire du contenu sur un ordinateur.

Les actions et les droits font référence aux mêmes façons d’utiliser le contenu. La différence est que l’action fait référence à l’utilisation alors que le droit fait référence à l’autorisation. Malgré cette distinction, les mots action et Right sont souvent utilisés de façon interchangeable dans cette documentation et dans d’autres documents qui décrivent Windows Media DRM.

Les actions régies par les droits DRM Windows Media sont répertoriées dans la section des [constantes de droits](rights-constants.md) de cette documentation.

Certaines méthodes des API étendues du client Windows Media DRM utilisent des constantes différentes pour faire référence aux droits DRM de base. Par exemple, la méthode [**IWMDRMLicenseQuery :: QueryLicenseState**](iwmdrmlicensequery-querylicensestate.md) utilise un ensemble de chaînes spécifiques aux États de licence. Même si ces constantes définissent des chaînes différentes de celles des constantes de droits de base, elles font référence aux mêmes droits dans la licence.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Concepts**](drmconcepts.md)
</dt> </dl>

 

 




