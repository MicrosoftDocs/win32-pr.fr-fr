---
description: Implémentez le multitâche, planifiez les priorités et travaillez avec les processus, les threads, les pools de threads, les objets de travail et les fibres. Utilisez la planification en mode utilisateur pour planifier les threads.
ms.assetid: 6bff848c-0c55-41e7-aff1-84c6b21a1b8d
title: Processus et threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f469806a5f803910a773c78c9847d0f7b0ecc7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519700"
---
# <a name="processes-and-threads"></a>Processus et threads

Une application se compose d’un ou plusieurs processus. Un *processus*, en termes simples, est un programme en cours d’exécution. Un ou plusieurs threads s’exécutent dans le contexte du processus. Un *thread* est l’unité de base à laquelle le système d’exploitation alloue du temps processeur. Un thread peut exécuter n’importe quelle partie du code de processus, y compris les composants en cours d’exécution par un autre thread.

Un *objet de traitement* permet de gérer des groupes de processus en tant qu’unité. Les objets de traitement sont des objets namable, sécurisables et partageables qui contrôlent les attributs des processus qui leur sont associés. Les opérations effectuées sur l’objet de traitement affectent tous les processus associés à l’objet de traitement.

Un *pool de threads* est une collection de threads de travail qui exécutent efficacement des rappels asynchrones pour le compte de l’application. Le pool de threads est principalement utilisé pour réduire le nombre de threads d’application et assurer la gestion des threads de travail.

Une *fibre* est une unité d’exécution qui doit être planifiée manuellement par l’application. Les fibres s’exécutent dans le contexte des threads qui les planifient.

La *planification en mode utilisateur* (UMS) est un mécanisme léger que les applications peuvent utiliser pour planifier leurs propres threads. Les threads UMS diffèrent des [fibres](fibers.md) en ce que chaque thread UMS a son propre contexte de thread au lieu de partager le contexte de thread d’un thread unique.

-   [Nouveautés des processus et des threads](what-s-new-in-processes-and-threads.md)
-   [À propos des processus et des threads](about-processes-and-threads.md)
-   [Utilisation des processus et des threads](using-processes-and-threads.md)
-   [Référence des processus et des threads](process-and-thread-reference.md)

 

 



