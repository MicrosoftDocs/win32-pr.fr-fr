---
title: Propriété de délai d’attente du serveur
description: .
ms.assetid: 5525c226-3786-41c4-86a2-3e077682313d
keywords:
- Propriété de délai d’attente du serveur HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8356c1e0d0e9eea2e5db9bf43882f26f9d7e3ddb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380101"
---
# <a name="server-timeouts-property"></a>Propriété de délai d’attente du serveur

L’API du serveur HTTP permet aux applications de définir les limites de délai de connexion au serveur sur une session serveur ou un groupe d’URL. La propriété HTTP timeouts est utilisée pour définir tous les délais d’attente sur une base spécifique à l’application. Les minuteurs **IdleConnection** et **HeaderWait** peuvent également être configurés à l’ensemble de l’API du serveur http. Lorsque les minuteurs sont configurés au niveau de l’API du serveur HTTP, ils s’appliquent à toutes les applications API du serveur HTTP sur l’ordinateur et les paramètres sont conservés lorsque le service est redémarré.

Pour plus d’informations sur la configuration des minuteurs, consultez [Configuration des délais d’attente spécifiques à l’application](configuring-the-application-specific-timeouts.md).

Lorsque les minuteurs ne sont pas configurés pour un groupe d’URL ou une session de serveur, les configurations par défaut de l’API du serveur HTTP s’appliquent.

L’ordre de mise en application du délai d’attente est le suivant :

1.  Les valeurs par défaut au niveau de l’API du serveur HTTP s’appliquent à toutes les applications API du serveur HTTP sur l’ordinateur.
2.  Les délais d’expiration de la session serveur remplacent les paramètres de l’API du serveur HTTP, lorsqu’ils sont définis.
3.  Les paramètres de groupe d’URL remplacent les configurations de session serveur quand elles sont définies.

Le tableau suivant répertorie les limites de délai d’attente de connexion par défaut



| Minuteur           | Définition                                                                                                        | API du serveur HTTP par défaut | Configurable à l’étendue de l’API serveur HTTP | Configurable comme spécifique à l’application |
|-----------------|-------------------------------------------------------------------------------------------------------------------|-------------------------|--------------------------------------|--------------------------------------|
| IdleConnection  | La connexion a expiré tout en restant inactive.                                                                        | 120 s                 | Oui                                  | Limité                              |
| HeaderWait      | La connexion a expiré lors de l’attente de l’analyse de l’en-tête par l’API du serveur HTTP.                                 | 120 s                 | Oui                                  | Limité                              |
| EntityBody      | La connexion a expiré en attendant l’arrivée du corps d’entité de la requête.                                       | 120 s                 | Non                                   | Oui                                  |
| DrainEntityBody | La connexion a expiré en attendant que l’API du serveur HTTP draine le corps d’entité sur une connexion Keep-Alive. | 120 s                 | Non                                   | Oui                                  |
| MinSendRate     | La connexion a expiré, car le taux d’envoi de la réponse est plus lent que la valeur par défaut de 150 octets/s.               | 150 s                 | Non                                   | Oui                                  |
| RequestQueue    | La connexion a expiré, car la demande est restée dans la file d’attente des demandes avant que l’application ne l’ait choisie.     | 120 octets/s           | Non                                   | Oui                                  |



 

 

 




