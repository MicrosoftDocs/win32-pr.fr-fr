---
title: Ressources sur un serveur hôte de session Bureau à distance
description: Plusieurs utilisateurs peuvent se connecter simultanément à un seul serveur hôte de session Bureau à distance (hôte de session Bureau à distance), en partageant les ressources matérielles et logicielles du serveur.
ms.assetid: ab193a9f-7424-42bf-8cea-28628096edc6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81e099787ae3d0acd9028405b244f7fbc2e2117e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673813"
---
# <a name="resources-on-a-remote-desktop-session-host-server"></a>Ressources sur un serveur hôte de session Bureau à distance

Dans un environnement Services Bureau à distance, plusieurs utilisateurs peuvent se connecter simultanément à un seul serveur hôte de session Bureau à distance (hôte de session Bureau à distance) (anciennement appelé Terminal Server). Par conséquent, les utilisateurs partagent les ressources matérielles et logicielles du serveur, ce qui peut créer les zones de contention suivantes :

-   Temps processeur. Chaque utilisateur dispose d’un environnement de bureau et peut exécuter toutes les applications disponibles sur ce poste de travail. Toutefois, toutes les applications exécutées par tous les utilisateurs sont confrontées aux ressources processeur centrales disponibles sur le serveur hôte de session Bureau à distance. Si un utilisateur exécute une application mal écrite et gourmande en ressources processeur, les autres utilisateurs peuvent subir une perte de performances visible.
-   Accès au disque. Les utilisateurs se disputent l’accès aux applications et aux fichiers programme associés. En outre, les utilisateurs sont en concurrence pour les accès disque par le système d’exploitation serveur, tels que le chargement de dll ou l’échange de mémoire entre le fichier d’échange et la mémoire physique.
-   Mémoire vive (RAM). Chaque application exécutée par chaque utilisateur est confrontée aux ressources RAM disponibles sur le serveur hôte de session Bureau à distance. Si un utilisateur exécute une application gourmande en mémoire, d’autres utilisateurs peuvent subir une perte de performances.
-   Accès au réseau. L’accès au réseau est essentiel dans un environnement Services Bureau à distance, car toute l’activité du Bureau (sortie graphique et entrée de souris/clavier) circule sur les liaisons réseau entre le Bureau du client et le serveur. En outre, les applications des utilisateurs s’exécutant sur le serveur hôte de session Bureau à distance sont en concurrence pour l’accès aux autres ressources réseau.
-   Matériel serveur. Les composants matériels, tels que les CD-ROM, les lecteurs de disquettes, les ports série et les ports parallèles, sont souvent basés sur un serveur et non sur un client. Le partage de ces composants traditionnellement non partagés crée de nouveaux éléments à prendre en compte pour les utilisateurs et pour les applications qui accèdent à ces composants matériels. Pour plus d’informations, consultez [instructions relatives au matériel](peripheral-hardware-guidelines.md).
-   Accès aux objets et ressources globaux. Dans un environnement de Services Bureau à distance, les utilisateurs n’exécutent pas de copies individuelles de Windows, certains modules de base sont clonés, mais les autres modules sont partagés entre les utilisateurs. Ainsi, les utilisateurs sont en concurrence pour accéder au registre, au fichier d’échange, aux services système et à d’autres objets et ressources globaux.

La plupart des points de conflit précédents peuvent être atténués en redimensionnant le serveur hôte de session Bureau à distance avec suffisamment de ressources processeur, mémoire et disque pour gérer la demande du client. Par exemple, une configuration à plusieurs processeurs peut maximiser la disponibilité du processeur. La disponibilité de la mémoire peut être augmentée en installant de la mémoire physique supplémentaire (les limites de mémoire accrues pour les éditions Enterprise, Datacenter ou 64 bits de Windows Server peuvent être utiles). Enfin, les performances d’accès au disque peuvent être optimisées en configurant plusieurs canaux et en distribuant le système d’exploitation et les charges d’application sur différents lecteurs physiques. La configuration correcte d’un serveur hôte de session Bureau à distance est un élément essentiel des performances perçues de l’application.

Bien que le dimensionnement du matériel soit une partie importante de la création d’un environnement de Services Bureau à distance évolutif, les considérations relatives aux logiciels sont tout aussi importantes. En fait, le réglage fin d’une application peut souvent faire beaucoup pour réduire la concurrence des ressources et améliorer les performances perçues des applications.

Pour plus d’informations sur l’environnement de Services Bureau à distance, consultez les rubriques suivantes :

-   [Instructions de programmation Services Bureau à distance](terminal-services-programming-guidelines.md)
-   [Détection de l’environnement de Services Bureau à distance](detecting-the-terminal-services-environment.md)
-   [Détection de l’installation du rôle Services Bureau à distance](detecting-whether-terminal-services-is-installed.md)
-   [Sessions Services Bureau à distance](terminal-services-sessions.md)

 

 




