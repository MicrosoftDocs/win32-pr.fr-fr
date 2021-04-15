---
title: Considérations relatives à la conception du serveur d’État
description: Selon votre conception, vous pouvez avoir besoin d’un serveur pour effectuer le suivi des utilisateurs qui sont actuellement connectés sur le réseau.
ms.assetid: 2f8d268b-5518-4ad2-aed6-5971c913db6d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a0ef654f3641138075acc667d733b20c94c4840
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380180"
---
# <a name="state-server-design-considerations"></a>Considérations relatives à la conception du serveur d’État

> [!Note]  
> Le service d’authentification Internet (IAS) a été renommé serveur NPS (Network Policy Server) à partir de Windows Server 2008. Le contenu de cette rubrique s’applique à IAS et à NPS. Dans le texte, NPS est utilisé pour faire référence à toutes les versions du service, y compris les versions initialement appelées IAS.

 

Selon votre conception, vous pouvez avoir besoin d’un serveur pour effectuer le suivi des utilisateurs qui sont actuellement connectés sur le réseau. Le principal défi avec le serveur d’État est de maintenir la synchronisation des informations de la base de données du serveur d’État avec celles qui sont actuellement connectées. Si les informations du serveur d’État ne sont pas synchronisées, les utilisateurs peuvent avoir plusieurs sessions lorsqu’ils ne sont pas autorisés à le faire. En outre, les utilisateurs qui n’ont pas plusieurs sessions peuvent être pénalisés par inadvertance.

Les éléments suivants doivent être pris en considération lors de l’implémentation du serveur d’État :

-   Le serveur d’État doit prendre la décision en ligne en quelques secondes. Pour cette raison, le serveur d’état requiert une infrastructure évolutive capable de prendre en charge de nombreuses mises à jour et requêtes par seconde. Les bases de données relationnelles ne sont pas appropriées pour ces requêtes volumineuses avec des mises à jour simultanées. Les bases de données relationnelles sont principalement conçues pour maintenir la cohérence des données et fournir une vue cohérente des données à tous les consommateurs. Elles ne sont pas conçues pour des mises à jour rapides.
-   La cohérence transactionnelle des mises à jour entre plusieurs objets n’est pas importante. Cela est dû au fait que le serveur d’État peut tolérer une petite fenêtre d’opportunités. Toutefois, la cohérence transactionnelle d’une seule mise à jour est importante pour réduire les risques de laisser le serveur d’État dans un état incohérent si l’un des serveurs RADIUS est arrêté au milieu de la mise à jour.
-   La persistance (enregistrement de l’état du réseau dans le stockage persistant) n’est pas importante, car les informations persistantes sont rapidement désynchronisées avec l’état réel du réseau.
-   Si RNIS ou d’autres formes de liaisons multiples sont prises en charge sur le réseau, le serveur d’État doit être en mesure de gérer les scénarios qui utilisent ces fonctionnalités.

Une conception possible consiste à implémenter à la fois une DLL d’extension d’authentification et une DLL d’extension d’autorisation. Chacune de ces dll peut communiquer sur le réseau avec une base de données. La DLL d’extension d’autorisation peut mettre à jour la base de données avec des informations sur la personne qui est actuellement connectée au réseau. La DLL d’extension d’authentification peut demander ces informations à la base de données pour décider s’il faut accepter ou refuser la demande d’authentification d’un utilisateur particulier. Si l’utilisateur est déjà connecté, la demande est rejetée.

L’avantage de disposer de la DLL d’extension d’autorisation pour mettre à jour la base de données du serveur d’État est que la DLL d’extension d’autorisation a accès à des informations supplémentaires sur l’utilisateur authentifié. La DLL d’extension d’autorisation a accès à tous les attributs d’autorisation à partir du mécanisme d’autorisation du serveur NPS. Par exemple, certains utilisateurs peuvent avoir des autorisations qui leur permettent d’avoir plusieurs sessions. Le serveur d’État doit traiter ces utilisateurs comme un cas spécial.

 

 




