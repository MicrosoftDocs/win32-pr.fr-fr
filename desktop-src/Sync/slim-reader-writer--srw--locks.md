---
description: Les verrous SRW (Slim Reader/Writer) activent les threads d’un processus unique pour accéder aux ressources partagées ; ils sont optimisés pour la vitesse et occupent très peu de mémoire.
ms.assetid: 2d439b21-291f-4ff0-910a-c1c27e800019
title: Verrous SRW (Slim Reader/Writer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bc478d5f9bbfec1268f65b3e4a7f562b9bdca3d2df21f4570a52782eec9f028
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959979"
---
# <a name="slim-readerwriter-srw-locks"></a>Verrous SRW (Slim Reader/Writer)

Les verrous SRW (Slim Reader/Writer) activent les threads d’un processus unique pour accéder aux ressources partagées ; ils sont optimisés pour la vitesse et occupent très peu de mémoire. Les verrous SRW Reader-Writer ne peuvent pas être partagés entre les processus.

Les threads de lecture lisent les données d’une ressource partagée, tandis que les threads d’écriture écrivent des données dans une ressource partagée. Lorsque plusieurs threads lisent et écrivent à l’aide d’une ressource partagée, des verrous exclusifs tels qu’une section critique ou un mutex peuvent devenir un goulot d’étranglement si les threads de lecteur s’exécutent en continu, mais les opérations d’écriture sont rares.

Les verrous SRW fournissent deux modes dans lesquels les threads peuvent accéder à une ressource partagée :

-   **Mode partagé**, qui accorde un accès en lecture seule partagé à plusieurs threads de lecture, ce qui leur permet de lire les données à partir de la ressource partagée simultanément. Si les opérations de lecture dépassent les opérations d’écriture, cette concurrence augmente les performances et le débit par rapport aux sections critiques.
    > [!NOTE]
    > Les verrous SRW en mode partagé ne doivent pas être acquis de manière récursive, car cela peut entraîner des blocages lorsqu’ils sont combinés avec l’acquisition exclusive.

-   **Mode exclusif**, qui accorde un accès en lecture/écriture à un thread d’écriture à la fois. Lorsque le verrou a été acquis en mode exclusif, aucun autre thread ne peut accéder à la ressource partagée tant que le Writer n’a pas libéré le verrou.
    > [!NOTE]
    > Les verrous SRW en mode exclusif ne peuvent pas être obtenus de manière récursive. Si un thread essaie d’acquérir un verrou qu’il détient déjà, cette tentative échoue (pour [**TryAcquireSRWLockExclusive**](/windows/win32/api/synchapi/nf-synchapi-tryacquiresrwlockexclusive)) ou un blocage (pour [**AcquireSRWLockExclusive**](/windows/win32/api/synchapi/nf-synchapi-acquiresrwlockexclusive))

Un seul verrou SRW peut être acquis dans l’un ou l’autre mode. les threads de lecture peuvent l’obtenir en mode partagé, tandis que les threads d’écriture peuvent l’acquérir en mode exclusif. Il n’existe aucune garantie quant à l’ordre dans lequel les threads qui demandent la propriété auront la propriété. Les verrous SRW ne sont ni équitables ni FIFO.

Un verrou SRW est la taille d’un pointeur. L’avantage est qu’il est rapide de mettre à jour l’état du verrou. L’inconvénient est que très peu d’informations d’État peuvent être stockées, de sorte que les verrous SRW ne détectent pas une utilisation récursive incorrecte en mode partagé. En outre, un thread qui possède un verrou SRW en mode partagé ne peut pas mettre à niveau sa propriété du verrou en mode exclusif.

L’appelant doit allouer une structure SRWLOCK et l’initialiser en appelant [**InitializeSRWLock**](/windows/win32/api/synchapi/nf-synchapi-initializesrwlock) (pour initialiser la structure dynamiquement) ou affecter la constante **SRWLock \_ init** à la variable de structure (pour initialiser la structure de manière statique).

Vous pouvez utiliser [Application Verifier](/windows-hardware/drivers/devtest/application-verifier) pour Rechercher l’utilisation récursive (réentrante) des verrous SRW.

Voici les fonctions de verrouillage SRW.

| Fonction de verrouillage SRW                                                | Description                                                                                                                                       |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AcquireSRWLockExclusive**](/windows/win32/api/synchapi/nf-synchapi-acquiresrwlockexclusive)       | Acquiert un verrou SRW en mode exclusif.                                                                                                           |
| [**AcquireSRWLockShared**](/windows/win32/api/synchapi/nf-synchapi-acquiresrwlockshared)             | Acquiert un verrou SRW en mode partagé.                                                                                                              |
| [**InitializeSRWLock**](/windows/win32/api/synchapi/nf-synchapi-initializesrwlock)                   | Initialise un verrou SRW.                                                                                                                           |
| [**ReleaseSRWLockExclusive**](/windows/win32/api/synchapi/nf-synchapi-releasesrwlockexclusive)       | Libère un verrou SRW qui a été ouvert en mode exclusif.                                                                                           |
| [**ReleaseSRWLockShared**](/windows/win32/api/synchapi/nf-synchapi-releasesrwlockshared)             | Libère un verrou SRW qui a été ouvert en mode partagé.                                                                                              |
| [**SleepConditionVariableSRW**](/windows/win32/api/synchapi/nf-synchapi-sleepconditionvariablesrw)   | Met en veille la variable de condition spécifiée et libère le verrou spécifié sous la forme d’une opération atomique.                                                |
| [**TryAcquireSRWLockExclusive**](/windows/win32/api/synchapi/nf-synchapi-tryacquiresrwlockexclusive) | Tente d’acquérir un verrou SRW (Slim Reader/Writer) en mode exclusif. Si l’appel réussit, le thread appelant prend la propriété du verrou. |
| [**TryAcquireSRWLockShared**](/windows/win32/api/synchapi/nf-synchapi-tryacquiresrwlockshared)       | Tente d’acquérir un verrou SRW (Slim Reader/Writer) en mode partagé. Si l’appel réussit, le thread appelant prend la propriété du verrou.    |

 
