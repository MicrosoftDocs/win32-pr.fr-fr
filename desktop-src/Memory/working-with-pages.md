---
description: Pour déterminer la taille d’une page sur l’ordinateur actuel, utilisez la fonction GetSystemInfo.
ms.assetid: 953ddfc4-6126-41fb-81a3-0ce1f0fb223f
title: Utilisation des pages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e47e8a352b13c12b38acca1a93f12886d83d24c4d43faa213a88cf5855b18c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067659"
---
# <a name="working-with-pages"></a>Utilisation des pages

Pour déterminer la taille d’une page sur l’ordinateur actuel, utilisez la fonction [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) .

Les fonctions [**VirtualQuery,**](/windows/win32/api/memoryapi/nf-memoryapi-virtualquery) et [**VirtualQueryEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualqueryex) retournent des informations sur une région de pages consécutives en commençant à une adresse spécifiée dans l’espace d’adressage d’un processus. **VirtualQuery,** retourne des informations sur la mémoire dans le processus appelant. **VirtualQueryEx** retourne des informations sur la mémoire dans un processus spécifié et est utilisé pour prendre en charge les débogueurs qui ont besoin d’informations sur un processus en cours de débogage. La région de pages est limitée par l’adresse spécifiée arrondie à la limite de page la plus proche. Il s’étend sur toutes les pages suivantes avec les attributs suivants en commun :

-   L’état de toutes les pages est le même : validé, réservé ou gratuit.
-   Si la page initiale n’est pas libre, toutes les pages de la région font partie de la même allocation initiale des pages qui ont été réservées par un appel à [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc).
-   La protection d’accès de toutes les pages est identique (c’est-à-dire **page \_ ReadOnly**, **page \_ ReadWrite** ou **page \_ NoAccess**).

La fonction [**VirtualLock**](/windows/win32/api/memoryapi/nf-memoryapi-virtuallock) permet à un processus de verrouiller une ou plusieurs pages de la mémoire allouée dans la mémoire physique (RAM), empêchant ainsi le système de permuter les pages dans le fichier d’échange. Il peut être utilisé pour s’assurer que les données critiques sont accessibles sans accès au disque. Le verrouillage des pages en mémoire est dangereux, car cela limite la capacité du système à gérer la mémoire. Une utilisation excessive des **VirtualLock** peut dégrader les performances du système en provoquant le remplacement du code exécutable dans le fichier d’échange. La fonction [**VirtualUnlock**](/windows/win32/api/memoryapi/nf-memoryapi-virtualunlock) déverrouille la mémoire verrouillée par **VirtualLock**.

La fonction [**VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect) permet à un processus de modifier la protection d’accès d’une page validée dans l’espace d’adressage d’un processus. Par exemple, un processus peut allouer des pages en lecture/écriture pour stocker des données sensibles, puis il peut modifier l’accès en lecture seule ou aucun accès pour se protéger contre un remplacement accidentel. **VirtualProtect** est généralement utilisé avec les pages allouées par [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc), mais il fonctionne également avec les pages validées par les autres fonctions d’allocation. Toutefois, **VirtualProtect** modifie la protection de pages entières et les pointeurs retournés par les autres fonctions ne sont pas nécessairement alignés sur les limites de la page. La fonction [**VirtualProtectEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotectex) est similaire à **VirtualProtect**, sauf qu’elle modifie la protection de la mémoire dans un processus spécifié. La modification de la protection est utile aux débogueurs pour accéder à la mémoire d’un processus en cours de débogage.

 

 
