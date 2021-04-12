---
description: Concepts des applications de service COM+
ms.assetid: d6b1cf4a-ca39-4d50-a33d-aa639937ef9e
title: Concepts des applications de service COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b24db7a031ed0520f30891d98688af67e853ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483065"
---
# <a name="com-service-application-concepts"></a>Concepts des applications de service COM+

Vous pouvez utiliser l’outil d’administration Services de composants pour configurer une application serveur COM+ en tant qu’application de service. L’exécution d’une application serveur COM+ en tant que service offre les avantages suivants :

-   Si votre application doit toujours être en cours d’exécution, les services de composants peuvent éventuellement démarrer le serveur automatiquement et redémarrer le serveur s’il expire. Par exemple, si un ordinateur exécutant les composants de l’écouteur de composants en file d’attente est redémarré, les écouteurs de composants en file d’attente peuvent être démarrés automatiquement s’ils sont configurés en tant que service.
-   Si votre application doit effectuer des opérations privilégiées, l’application peut s’exécuter en tant que compte système local. Seuls les services NT sont autorisés à s’exécuter avec ce niveau de sécurité. L’application est compatible avec Windows service de cluster, qui gère les services pendant le basculement du système.
-   Si d’autres services doivent être marqués comme étant dépendants, les services de composants fournissent cette option. Par exemple, si votre application utilise des fonctionnalités fournies par un autre service, le service marqué comme dépendant sera démarré avant le démarrage de votre application.

## <a name="starting-an-application-automatically"></a>Démarrage automatique d’une application

Lorsque l’application serveur COM+ est démarrée automatiquement, elle agit comme un service, ce qui oblige le développeur à gérer le serveur à l’aide de l’outil d’administration Services.

> [!Note]  
> L’outil d’administration Services est accessible en lançant l’outil d’administration Services de composants, puis en cliquant sur **services (local)**.

 

## <a name="starting-an-application-manually"></a>Démarrage manuel d’une application

Lorsque l’application serveur COM+ est démarrée manuellement, elle agit comme un hôte DLL avec les paramètres de sécurité d’un service. Le service est démarré manuellement lorsqu’il est activé et arrêté automatiquement lorsqu’il expire.

## <a name="service-configurations"></a>Configurations de service

Quel que soit le type de démarrage, l’application peut être configurée pour s’exécuter en tant que compte système local ou être affectée à un compte d’utilisateur. Le compte système local et le compte d’utilisateur peuvent être configurés au moment de la création du service. Pour configurer les paramètres de sécurité, l’outil d’administration Services doit être utilisé. Il est également possible de définir des dépendances pour le service.

L’application peut également être démarrée dans n’importe quel ordre particulier en sélectionnant dépendances dans une liste d’autres services système. Par exemple, les services système peuvent être marqués comme étant dépendants et ne démarrent pas l’application tant que les services système n’ont pas été démarrés dans l’ordre spécifié. L’application de service sera correctement initialisée avant d’être utilisée.

Pour obtenir des instructions pas à pas sur la configuration d’une application COM+ pour qu’elle s’exécute en tant que service, consultez [configuration d’une application serveur com+ en tant qu’application de service](configuring-a-com--server-application-as-a-service-application.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Tâches de l’application de service COM+](com--service-application-tasks.md)
</dt> </dl>

 

 



