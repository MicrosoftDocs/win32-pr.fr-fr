---
title: À propos des partitions de l’annuaire d’applications
description: Les développeurs qui utilisent ADSI ou LDAP pour stocker et accéder à des données relativement statiques et globales dans Active Directory Domain Services peuvent également préférer, pour des raisons de simplicité et d’uniformité, la poursuite de l’utilisation de l’accès ADSI ou LDAP pour leurs besoins en matière de données dynamiques. Les modifications de données dynamiques sont plus fréquentes que celles recommandées pour le stockage dans Active Directory Domain Services. Les données dynamiques changent généralement plus fréquemment que la latence de réplication impliquée dans la propagation de la modification à tous les réplicas des données.
ms.assetid: bf856c3a-9061-474a-a536-c87ca50d5f83
ms.tgt_platform: multiple
keywords:
- À propos des partitions de l’annuaire d’applications
- Partitions d’annuaire d’applications, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9063a05bdb6f04681f012f1e6317b3343833c79c8f6a5af39a1a7865eccbab63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117841029"
---
# <a name="about-application-directory-partitions"></a>À propos des partitions de l’annuaire d’applications

Les développeurs qui utilisent ADSI ou LDAP pour stocker et accéder à des données relativement statiques et globales dans Active Directory Domain Services peuvent également préférer, pour des raisons de simplicité et d’uniformité, la poursuite de l’utilisation de l’accès ADSI ou LDAP pour leurs besoins en matière de données dynamiques. Les modifications de données dynamiques sont plus fréquentes que celles recommandées pour le stockage dans Active Directory Domain Services. Les données dynamiques changent généralement plus fréquemment que la latence de réplication impliquée dans la propagation de la modification à tous les réplicas des données.

dans Windows 2000, la prise en charge des données dynamiques est limitée. Le stockage de données dynamiques dans une partition de domaine peut être compliqué. Les données sont répliquées sur tous les contrôleurs de domaine du domaine, ce qui est souvent inutile et peut entraîner des incohérences de données en raison de la latence de la réplication. Cela peut nuire aux performances du réseau. En outre, les partitions de domaine ne sont pas efficaces pour les applications qui doivent répliquer les données entre les limites de domaine. une autre option de Windows 2000 consiste à stocker des données dynamiques dans des attributs marqués comme non répliqués. Toutefois, cette configuration est limitée en ce qu’elle présente un point de défaillance unique, à savoir que le seul contrôleur de domaine héberge la seule copie des attributs non répliqués de l’objet.

Les partitions d’annuaire d’applications permettent de contrôler l’étendue de la réplication et d’autoriser le placement des réplicas de manière plus appropriée pour les données dynamiques. Par conséquent, la partition d’annuaire d’applications offre la possibilité d’héberger des données dynamiques dans le serveur Active Directory, autorisant ainsi l’accès ADSI/LDAP, sans impact significatif sur les performances du réseau.

le service DNS Windows 2000 est un exemple de service qui peut tirer parti des partitions de l’annuaire d’applications. dans Windows 2000, si le service dns est éventuellement configuré pour utiliser Active Directory Domain Services, les données de la zone dns sont stockées dans le serveur Active Directory dans une partition de domaine. Autrement dit, les données sont répliquées sur tous les contrôleurs de domaine du domaine, qu’un serveur DNS soit configuré ou non pour s’exécuter sur le contrôleur de domaine. Il s’agit d’une instance où la réplication complète au niveau du domaine est inutile. En stockant les données de zone DNS dans une partition d’annuaire d’applications, le service peut redéfinir l’étendue de la réplication sur ce sous-ensemble de contrôleurs de domaine dans le domaine qui exécute réellement le serveur DNS.

Tenez compte des scénarios suivants pour héberger un réplica d’une partition d’annuaire d’applications :

-   vous pouvez créer un réplica d’une partition d’annuaire d’applications sur n’importe quel système d’exploitation Windows Server 2003 et sur un contrôleur de domaine ultérieur dans une forêt Active Directory Domain Services.
-   Vous pouvez spécifier l’ensemble des contrôleurs de domaine qui hébergent des réplicas d’une partition d’annuaire d’applications. Contrairement à une partition de domaine, il n’est pas nécessaire qu’une partition d’annuaire d’applications soit répliquée sur tous les contrôleurs de domaine d’un domaine, et elle peut être répliquée sur des contrôleurs de domaine dans différents domaines de la forêt.
-   un contrôleur de domaine avec un réplica de partition d’annuaire d’applications peut coexister et fonctionner dans un environnement en mode mixte avec d’autres ordinateurs exécutant Windows 2000 ou Windows NT 4,0.

Les types de données qui peuvent être stockées dans une partition d’annuaire d’applications sont les suivants :

-   Une partition d’annuaire d’applications peut contenir des instances de tout type d’objet, à l’exception des principaux de sécurité, tels que les utilisateurs, les ordinateurs ou les groupes.
-   Les objets d’une partition d’annuaire d’applications peuvent gérer les références de valeurs DN à d’autres objets dans la même partition d’annuaire d’applications, aux objets des partitions de configuration et de schéma, et à n’importe quel en-tête de contexte d’appellation (qui est l’objet supérieur d’une partition d’annuaire, tel que l’objet **domainDNS** en haut d’une partition d’annuaire d’applications)
-   Pour plus d’informations et pour obtenir un exemple du type de données dynamiques pouvant être stockées dans une partition d’annuaire d’applications, consultez [objets dynamiques](dynamic-objects.md). les objets dynamiques sont pris en charge à partir de Windows Server 2003. Les objets dynamiques ont une propriété qui détermine la durée de vie, après laquelle l’objet est supprimé par le serveur de Active Directory.

Certaines limitations des partitions d’annuaire d’applications sont les suivantes :

-   Les objets d’une partition d’annuaire d’applications ne peuvent pas conserver les *références de valeurs DN* aux objets dans d’autres partitions d’annuaire d’applications ou partitions de domaine. (Les références de valeur DN sont des références persistantes à une valeur de nom unique telle que "CN = someuser, DC = Corp, DC = fabrikam, DC = com"). De même, les objets dans les partitions de domaine, de configuration et de schéma ne peuvent pas gérer les références de valeurs DN aux objets dans une partition d’annuaire d’applications. Une référence de valeur DN peut être conservée dans l’en-tête de contexte d’appellation. () )
-   Les objets d’une partition d’annuaire d’applications ne sont pas répliqués dans le catalogue global. Comme pour n’importe quel contrôleur de domaine, un serveur de catalogue global peut également être configuré pour contenir un réplica complet d’une partition d’annuaire d’applications, mais les données de partition de l’annuaire d’applications sont complètement séparées des données de catalogue global.
-   lors de la création d’un réplica de partition d’annuaire d’applications, le rôle Domain-Naming FSMO doit se trouver sur l’un des contrôleurs de domaine du système d’exploitation Windows Server 2003 et versions ultérieures. une fois le réplica de partition d’annuaire d’applications créé, le rôle FSMO d’attribution de noms de domaine peut être attribué à un contrôleur de domaine Windows 2000.
-   Les objets de partition d’annuaire d’applications ne peuvent pas être déplacés vers d’autres partitions de Active Directory en dehors de la partition dans laquelle elles ont été créées.

Les autres fonctionnalités de partition d’annuaire d’applications sont les suivantes :

-   Le modèle de sécurité et de contrôle d’accès pour la partition de l’annuaire d’applications est le même que pour les autres partitions de Active Directory Domain Services.
-   Les intervalles de temps qui contrôlent la latence de l’initiation d’une notification de modification d’origine aux partenaires de réplication au sein d’un site peuvent être configurés séparément pour chaque partition de l’annuaire d’applications.
-   les partitions d’annuaire d’applications peuvent être nommées en tant que domaines standard, attachés n’importe où dans l’espace de noms Active Directory où un domaine peut et découvert à l’aide de DNS, même avec des systèmes de Windows 2000 de niveau inférieure.
-   Une partition d’annuaire d’applications peut être créée, son étendue de réplication définie et ses paramètres configurables sont ajustés par programme à l’aide des API LDAP et ADSI standard. Pour plus d’informations sur la manipulation par programmation des partitions de l’annuaire d’applications, consultez partitions de l' [Annuaire d’applications](application-directory-partitions.md).

 

 




