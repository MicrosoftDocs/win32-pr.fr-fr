---
description: Une liste à liaison unique interverrouillée (SList) facilite la tâche d’insertion et de suppression d’une liste liée.
ms.assetid: 35463ace-33ab-4eb9-9901-2504a92456e2
title: Listes liées de façon isolée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9af39847fa2fd1b1873c661d6ec904783e0139b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520646"
---
# <a name="interlocked-singly-linked-lists"></a>Listes liées de façon isolée

Une *liste à liaison unique interverrouillée* (SLIST) facilite la tâche d’insertion et de suppression d’une liste liée. Les SLists sont implémentés à l’aide d’un algorithme de non-blocage pour fournir une synchronisation atomique, accroître les performances du système et éviter des problèmes tels que l’inversion de priorité et les convois de verrouillage.

Les SLists sont faciles à implémenter et à utiliser dans le code 32 bits. Toutefois, il est difficile de les implémenter dans le code 64 bits, car la quantité de données échangées par les primitives Exchange verrouillées natives n’est pas le double de la taille de l’adresse, comme c’est le cas dans le code 32 bits. Par conséquent, SLists active le portage des algorithmes évolutifs haut de gamme vers Windows.

**Windows 8 :** À compter de Windows 8, les primitives d’Exchange natives verrouillées appropriées sont disponibles pour le code 64 bits, par exemple [**InterlockedCompare64Exchange128**](/previous-versions/windows/desktop/legacy/ms683553(v=vs.85)).

Les applications peuvent utiliser SLists en appelant la fonction [**InitializeSListHead**](/windows/win32/api/interlockedapi/nf-interlockedapi-initializeslisthead) pour initialiser l’en-tête de la liste. Pour insérer des éléments dans la liste, utilisez la fonction [**InterlockedPushEntrySList**](/windows/win32/api/interlockedapi/nf-interlockedapi-interlockedpushentryslist) . Pour supprimer des éléments de la liste, utilisez la fonction [**InterlockedPopEntrySList**](/windows/win32/api/interlockedapi/nf-interlockedapi-interlockedpopentryslist) .

Tous les éléments de liste doivent être alignés sur une limite d' **\_ \_ alignement d’allocation de mémoire** . Les éléments non alignés peuvent entraîner des résultats imprévisibles. Voir **\_ \_ malloc aligné**.

Pour obtenir un exemple, consultez [utilisation de listes à liaison unique](using-singly-linked-lists.md).

Le tableau suivant répertorie les fonctions SList.



| Fonction                                                         | Description                                                                                                                                               |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**InitializeSListHead**](/windows/win32/api/interlockedapi/nf-interlockedapi-initializeslisthead)               | Initialise le en-tête d’une liste liée de façon unique.                                                                                                             |
| [**InterlockedFlushSList**](/windows/win32/api/interlockedapi/nf-interlockedapi-interlockedflushslist)           | Vide l’intégralité de la liste d’éléments dans une liste à liaison unique.                                                                                                 |
| [**InterlockedPopEntrySList**](/windows/win32/api/interlockedapi/nf-interlockedapi-interlockedpopentryslist)     | Supprime un élément de l’avant d’une liste à liaison unique.                                                                                                   |
| [**InterlockedPushEntrySList**](/windows/win32/api/interlockedapi/nf-interlockedapi-interlockedpushentryslist)   | Insère un élément au début d’une liste à liaison unique.                                                                                                     |
| [**InterlockedPushListSList**](/previous-versions/windows/desktop/legacy/hh448545(v=vs.85))     | Insère une liste à liaison unique à l’avant d’une autre liste à liaison unique.                                                                                  |
| [**InterlockedPushListSListEx**](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex) | Insère une liste à liaison unique à l’avant d’une autre liste à liaison unique. Cette version de la méthode n’utilise pas la Convention d’appel **\_ \_ fastcall** . |
| [**RtlFirstEntrySList**](/windows/desktop/api/WinNT/nf-winnt-rtlfirstentryslist)                 | Récupère la première entrée d’une liste à liaison unique.                                                                                                        |
| [**QueryDepthSList**](/windows/win32/api/interlockedapi/nf-interlockedapi-querydepthslist)                       | Récupère le nombre d’entrées dans la liste liée unique spécifiée.                                                                                      |



 

 

 
