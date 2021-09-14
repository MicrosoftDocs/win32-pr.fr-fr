---
description: Chaque processus fournit les ressources nécessaires à l’exécution d’un programme.
ms.assetid: 055458cf-9fc7-4a16-be14-1122b3cf0251
title: À propos des processus et des threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 650eab4421971bdc08e71c031aec433ed84471bf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119054"
---
# <a name="about-processes-and-threads"></a>À propos des processus et des threads

Chaque *processus* fournit les ressources nécessaires à l’exécution d’un programme. Un processus dispose d’un espace d’adressage virtuel, d’un code exécutable, de handles ouverts vers des objets système, d’un contexte de sécurité, d’un identificateur de processus unique, de variables d’environnement, d’une classe de priorité, de tailles de jeu de travail minimale et maximale, et d’au moins un thread d’exécution. Chaque processus est démarré avec un seul thread, souvent appelé *thread principal*, mais peut créer des threads supplémentaires à partir de l’un de ses threads.

Un *thread* est l’entité dans un processus qui peut être planifiée pour l’exécution. Tous les threads d’un processus partagent l’espace d’adressage virtuel et les ressources système. En outre, chaque thread gère des gestionnaires d’exceptions, une priorité de planification, un stockage local des threads, un identificateur de thread unique et un ensemble de structures que le système utilisera pour enregistrer le contexte de thread jusqu’à ce qu’il soit planifié. Le *contexte de thread* comprend l’ensemble des registres d’ordinateur, la pile de noyau, un bloc d’environnement de thread et une pile d’utilisateur dans l’espace d’adressage du processus du thread. Les threads peuvent également avoir leur propre contexte de sécurité, qui peut être utilisé pour emprunter l’identité des clients.

Microsoft Windows prend en charge le *multitâche préemptif*, qui crée l’effet de l’exécution simultanée de plusieurs threads à partir de plusieurs processus. Sur un ordinateur multiprocesseur, le système peut exécuter simultanément autant de threads qu’il y a de processeurs sur l’ordinateur.

Un *objet de traitement* permet de gérer des groupes de processus en tant qu’unité. Les objets de traitement sont des objets namable, sécurisables et partageables qui contrôlent les attributs des processus qui leur sont associés. Les opérations effectuées sur l’objet de traitement affectent tous les processus associés à l’objet de traitement.

Une application peut utiliser le *pool de threads* pour réduire le nombre de threads d’application et assurer la gestion des threads de travail. Les applications peuvent effectuer la mise en file d’attente des éléments de travail, associer un travail à des handles pouvant être programmés, effectuer la file d’attente automatiquement en fonction d’un minuteur et établir une liaison avec

La *planification en mode utilisateur* (UMS) est un mécanisme léger que les applications peuvent utiliser pour planifier leurs propres threads. Une application peut basculer entre les threads UMS en mode utilisateur sans impliquer le [planificateur système](scheduling.md) et regagner le contrôle du processeur si un thread UMS se bloque dans le noyau. Chaque thread UMS a son propre contexte de thread au lieu de partager le contexte de thread d’un thread unique. La possibilité de basculer entre les threads en mode utilisateur rend UMS plus efficace que les pools de threads pour les éléments de travail à durée réduite qui nécessitent peu d’appels système.

Une *fibre* est une unité d’exécution qui doit être planifiée manuellement par l’application. Les fibres s’exécutent dans le contexte des threads qui les planifient. Chaque thread peut planifier plusieurs fibres. En général, les fibres ne fournissent pas d’avantages par rapport à une application multithread bien conçue. Toutefois, l’utilisation de fibres peut faciliter le portage des applications conçues pour planifier leurs propres threads.

Pour plus d'informations, voir les rubriques suivantes :

-   [Multitâche](multitasking.md)
-   [Planification](scheduling.md)
-   [Threads multiples](multiple-threads.md)
-   [Processus enfants](child-processes.md)
-   [Pools de threads](thread-pools.md)
-   [Objets de traitement](job-objects.md)
-   [Planification en mode utilisateur](user-mode-scheduling.md)
-   [Fibres](fibers.md)

 

 



