---
title: Points de connexion de service pour les services répliqués, basés sur l’hôte et sur la base de données
description: Lorsque vous publiez un service à l’aide d’un point de connexion de service (SCP), réfléchissez à la façon dont les clients localisent le SCP pour votre service.
ms.assetid: 944e8ecd-f8ea-4506-992c-bbbfc82d11f3
ms.tgt_platform: multiple
keywords:
- Points de connexion de service pour les services AD répliqués, basés sur l’hôte et les services de base de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a7658cc60704dbfc37009272e5f14f997d213ea993054fa22c1c5e0c307794b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024897"
---
# <a name="service-connection-points-for-replicated-host-based-and-database-services"></a>Points de connexion de service pour les services répliqués, basés sur l’hôte et sur la base de données

Lorsque vous publiez un service à l’aide d’un point de connexion de service (SCP), réfléchissez à la façon dont les clients localisent le SCP pour votre service. Si plusieurs instances du service existent, réfléchissez à la façon dont les clients distinguent le service des fonctionnalités souhaitées des services similaires avec des fonctionnalités différentes. Si vous publiez un service répliqué, réfléchissez à la façon dont un client choisit un réplica. Cette rubrique décrit ces problèmes pour différents types de services.

## <a name="replicable-services"></a>Services réplicables

Pour un service réplicable, il peut y avoir une ou plusieurs instances, ou réplicas, du service, et les clients ne se soucient pas du réplica auquel ils se connectent, car chacun fournit le même service. Active Directory Domain Services sont des exemples de services répliqués : tous les contrôleurs de domaine d’un domaine donné contiennent des données identiques, sujettes à la latence de la réplication, et fournissent des services identiques.

Les services réplicables peuvent stocker les SCP et d’autres objets spécifiques aux services pour plusieurs réplicas dans un seul conteneur. L’application d’installation pour le premier réplica peut créer le conteneur en tant qu’enfant du conteneur système du domaine local. Pour plus d’informations, consultez [publication dans un conteneur de système de domaine](publishing-in-a-domain-system-container.md). Assurez-vous que le descripteur de sécurité de votre conteneur permet aux programmes d’installation des réplicas suivants de créer leurs objets dans le même conteneur. Accordez des autorisations à l’administrateur d’installation pour spécifier les utilisateurs ou les groupes qui peuvent créer ou modifier des objets dans le conteneur.

Une stratégie pour un service réplicable consiste à créer un SCP pour chaque réplica. Lorsqu’un client demande le GUID du produit du service ou un autre mot clé d’identification, il recherche les objets SCP pour tous les réplicas et en sélectionne un au hasard ou en utilisant un algorithme d’équilibrage de charge. Par exemple, un administrateur peut spécifier des données de priorité et d’équilibrage de charge pour chaque réplica, de la même façon que les champs de priorité et de pondération d’un enregistrement SRV DNS. L’application d’installation du service peut stocker ces données dans l’attribut **serviceBindingInformation** du SCP de chaque réplica. Les clients récupèrent les données de chaque SCP et l’utilisent pour sélectionner un réplica.

Une autre stratégie consiste à créer un seul SCP pour tous les réplicas et à définir l’attribut SCP **servicednsname** sur le nom d’un enregistrement SRV DNS. Ensuite, l’application d’installation de chaque réplica inscrit un enregistrement SRV portant ce nom. Lorsqu’un client identifie le SCP seul du service, le client récupère le nom de l’enregistrement SRV et utilise la fonction [**DNSQuery**](/windows/desktop/api/windns/nf-windns-dnsquery_a) pour récupérer le tableau d’enregistrements SRV pour les réplicas. Chaque enregistrement SRV contient le nom d’un ordinateur hôte et les données supplémentaires que le client peut utiliser pour sélectionner un réplica.

## <a name="database-services"></a>Services de base de données

Les différentes instances d’un service de base de données peuvent contenir des données entièrement différentes, bien qu’elles soient toutes du même type de service, généralement appelée classe de service. Pour publier ce type de service, l’attribut **Keywords** du SCP peut identifier la classe de service et la base de données spécifique. Un client à usage général qui connaît uniquement le GUID de la classe de service peut interroger toutes les bases de données publiées par cette classe de service, puis présenter une interface utilisateur pour permettre à l’utilisateur d’en sélectionner un. Pour un client conçu spécifiquement pour la base de données cible, vous pouvez coder en dur le GUID de la base de données dans le code client.

## <a name="host-based-services"></a>Services basés sur l’hôte

Les services basés sur l’hôte sont des services qui sont étroitement liés à un seul ordinateur hôte. Vous pouvez installer des instances de la classe de service sur de nombreux ordinateurs et chaque instance fournit des services identifiés avec son ordinateur hôte.

Chaque instance d’un service basé sur l’hôte doit créer son propre SCP sous l’objet ordinateur de son hôte. Les clients qui utilisent un GUID de produit pour rechercher le SCP d’un service basé sur l’hôte trouvent généralement de nombreuses instances de la classe de service dans l’ensemble de la forêt d’entreprise. Les clients peuvent ensuite utiliser l’attribut **servicednsname** de l’SCP pour trouver le SCP de l’instance de service sur l’ordinateur hôte de votre choix.

 

 