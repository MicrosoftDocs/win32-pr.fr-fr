---
description: Configuration des applications de bibliothèque
ms.assetid: db375e0f-74ca-44df-918a-b0e48742a594
title: Configuration des applications de bibliothèque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b8ea0018d74070828384db25d76c73e7b5b3dba8a7dfc7d091c94e38aa0c3bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047497"
---
# <a name="configuring-library-applications"></a>Configuration des applications de bibliothèque

Étant donné que les applications de bibliothèque COM+ s’exécutent dans le processus du client, les éléments configurables pour les applications de bibliothèque sont considérablement différents de ceux des applications serveur. Vous ne pouvez pas configurer les aspects de l’application qui sont déterminés par le processus d’hébergement.

Au niveau de l’application, plusieurs paramètres sont soit limités, soit indisponibles pour les applications de bibliothèque. Ces contraintes sont décrites dans le tableau suivant :



| Attribut                                       | Description                                                                                                                                                                                                                                   |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Niveau de sécurité<br/>                       | Vous devez choisir les contrôles d’accès au niveau du composant. L’application de bibliothèque ne peut pas influencer les contrôles d’accès au niveau du processus. Consultez [définition d’un niveau de sécurité pour les vérifications d’accès](setting-a-security-level-for-access-checks.md).<br/>             |
| Activation ou désactivation de l’authentification<br/> | Vous pouvez indiquer si l’application de bibliothèque doit participer à l’authentification effectuée par le processus hôte. Consultez [activation de l’authentification pour une application de bibliothèque](enabling-authentication-for-a-library-application.md).<br/> |
| Niveau d'emprunt d'identité<br/>                  | Pas disponible. Le paramètre du processus hôte est utilisé. <br/>                                                                                                                                                                             |
| Identité de sécurité<br/>                    | Pas disponible. L’application s’exécute sous l’identité du processus hôte.<br/>                                                                                                                                                          |
| Arrêt du processus serveur<br/>              | Pas disponible.<br/>                                                                                                                                                                                                                       |
| Activer la prise en charge de 3 Go<br/>                  | Pas disponible.<br/>                                                                                                                                                                                                                       |
| Lancer dans le débogueur<br/>                   | Pas disponible.<br/>                                                                                                                                                                                                                       |
| Activer CRM<br/>                           | Pas disponible.<br/>                                                                                                                                                                                                                       |
| Queuing<br/>                              | Pas disponible.<br/>                                                                                                                                                                                                                       |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vue d’ensemble de l’application COM+](com--application-overview.md)
</dt> </dl>

 

 




