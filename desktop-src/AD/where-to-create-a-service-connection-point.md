---
title: Où créer un point de connexion de service
description: Lorsqu’une instance de Active Directory Domain Services est installée, le programme d’installation du service crée des objets point de connexion de service (SCP) dans Active Directory Domain Services.
ms.assetid: a90566d9-dd68-43e2-be9e-300d57a7fbf4
ms.tgt_platform: multiple
keywords:
- où créer un point de connexion de service AD
- Active Directory, où créer un point de connexion de service
- où créer un point de connexion de service AD
- création d’une publicité de point de connexion de service
- AD point de connexion de service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf122ebabcfd8085ebad46314ffd1c09f827e783
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028581"
---
# <a name="where-to-create-a-service-connection-point"></a>Où créer un point de connexion de service

Lorsqu’une instance de Active Directory Domain Services est installée, le programme d’installation du service crée des objets point de connexion de service (SCP) dans Active Directory Domain Services. L’objectif principal doit être de réduire le trafic de réplication et de permettre une administration et une maintenance efficaces des objets.

N’oubliez pas que les applications clientes trouvent les SCP en recherchant les mots clés dans le SCP dans le répertoire. L’attribut **Keywords** d’un SCP est inclus dans le catalogue global ; les clients peuvent rechercher dans le catalogue global les SCP de la forêt. Pour cette raison, le client n’a pas d’influence sur la publication des SCP.

## <a name="minimize-replication-traffic"></a>Réduire le trafic de réplication

Pour réduire le trafic de réplication, créez des SCP dans la partition de domaine du domaine de l’ordinateur hôte du service. Par exemple, vous pouvez créer des SCP en tant qu’objets enfants de l’objet ordinateur sur lequel le service est installé. Une partition de domaine de Active Directory Domain Services, parfois appelée contexte d’appellation de domaine, contient des objets spécifiques au domaine, tels que les objets pour les utilisateurs et les ordinateurs du domaine. Un réplica complet de tous les objets de la partition de domaine est répliqué sur chaque contrôleur de domaine pour le domaine, mais il n’est pas répliqué vers les contrôleurs de domaine d’autres domaines.

Ne créez pas des SCP dans la partition de configuration, également appelée contexte d’appellation de configuration, car les modifications apportées à la partition de configuration sont répliquées sur chaque contrôleur de groupe de la forêt. Comme indiqué ci-dessus, les clients de la forêt peuvent interroger le catalogue global pour trouver les SCP n’importe où dans la forêt, de sorte que la création de SCP dans la partition de configuration ne les rend pas plus visibles aux clients. il génère uniquement du trafic de réplication.

## <a name="ease-of-administration"></a>Facilité d’administration

Tenez compte des recommandations suivantes pour l’administration des objets :

-   Placez les objets spécifiques au service dans lesquels les administrateurs peuvent contrôler leur accès à l’aide de la stratégie et des autorisations d’accès héritées.
-   Placez les objets dans là où un administrateur peut les trouver facilement.

Un bon emplacement par défaut qui répond aux deux objectifs consiste à créer SCP et d’autres objets spécifiques au service sous l’objet ordinateur de l’ordinateur hôte de chaque instance de service. Pour plus d’informations, consultez [publication sous un objet ordinateur](publishing-under-a-computer-object.md).

Une bonne alternative pour les services qui ne sont pas liés à un seul hôte consiste à créer un conteneur pour les objets de service sous le conteneur système dans une partition de domaine. Pour plus d’informations, consultez [publication dans un conteneur de système de domaine](publishing-in-a-domain-system-container.md).

Le diagramme suivant illustre une partie de la hiérarchie de conteneurs par défaut pour une partition de domaine.

![hiérarchie de conteneur de partition de domaine par défaut](images/domain-container-heirarchy.png)

Le diagramme montre la hiérarchie de domaine par défaut incluse dans Active Directory Domain Services. Toutefois, de nombreuses entreprises créent une hiérarchie de conteneurs d’unités d’organisation (UO) pour regrouper des classes d’objets, telles que des utilisateurs et des ordinateurs, en vue de leur administration. Les administrateurs peuvent ensuite appliquer la stratégie et hériter les entrées de contrôle d’accès (ACE) à une unité d’organisation pour déléguer l’autorité administrative des objets dans l’unité d’organisation. Cela permet aux administrateurs de gérer efficacement une entreprise, mais présente quelques conséquences pour les programmeurs de service :

-   L’objet ordinateur d’un hôte de service peut ne pas se trouver sous le conteneur ordinateurs comme indiqué dans le diagramme. Pour plus d’informations sur la recherche de l’objet ordinateur pour l’ordinateur local, consultez [publication sous un objet ordinateur](publishing-under-a-computer-object.md).
-   Les administrateurs peuvent déplacer des objets en fonction de l’évolution de leurs besoins organisationnels. Cela signifie que vous ne pouvez pas dépendre de vos objets restants dans un emplacement fixe. autrement dit, votre service ne peut pas dépendre d’un nom unique d’objet restante. Au lieu de cela, utilisez l’attribut **objectGUID** d’un objet, qui ne change pas si l’objet est déplacé ou renommé. Pour plus d’informations et pour obtenir un exemple de code qui crée un SCP, stocke son **objectGUID** et récupère par la suite l' **objectGUID** à lier au SCP, consultez [création et gestion d’un point de connexion de service](creating-and-maintaining-a-service-connection-point.md).
-   Toutes les classes d’objets relatives au service standard, ainsi que les sous-classes de ces classes, sont des enfants valides des classes **Computer** et **OrganizationalUnit** . Si vous étendez le schéma pour définir votre propre classe propre à un service, assurez-vous que les classes **Computer** et **OrganizationalUnit** sont incluses dans les supérieurs possibles.
-   Le programme d’installation du service détermine l’emplacement par défaut pour la création de SCP. Vous pouvez autoriser l’administrateur à installer le service pour spécifier un autre chemin d’installation.

Les objets spécifiques au service ne doivent pas être créés dans les domaines suivants :

-   Les services ne doivent pas publier d’objets directement dans les conteneurs utilisateurs ou ordinateurs d’une partition de domaine, ni créer de conteneurs dans ces conteneurs. Toutefois, les services peuvent publier des objets en tant qu’objets enfants d’un objet ordinateur, que l’objet ordinateur soit ou non stocké dans le conteneur ordinateurs.
-   Les services, qui utilisent l’inscription et la résolution Windows Sockets (RnR) ou les API RpcNs (RPC Name Service) pour se publier eux-mêmes, créent les objets appropriés dans les conteneurs WinsockServices et RpcServices sous le conteneur système d’une partition de domaine. Ne créez pas explicitement des objets dans ces conteneurs. Cela ne provoque pas de dommages directs, mais peut prêter à confusion pour les administrateurs.

 

 




