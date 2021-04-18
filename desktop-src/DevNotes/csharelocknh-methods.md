---
description: Groupe de méthodes utilisé pour manipuler des verrous.
ms.assetid: ba4cc37c-bd2f-446f-8b3d-bc2a2e2e4de4
title: Méthodes CShareLockNH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b16a979c5d1f111c92a64376c48f4c0ed1a165ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513128"
---
# <a name="csharelocknh-methods"></a>Méthodes CShareLockNH

Groupe de méthodes utilisé pour manipuler des verrous.

## <a name="methods"></a>Méthodes

Voici les méthodes exportées par Rwnh.dll.



| Méthode                                                                   | Description                                                     |
|--------------------------------------------------------------------------|-----------------------------------------------------------------|
| [**ExclusiveLock**](csharelocknh--exclusivelock.md)                     | Acquiert un verrou en lecture/écriture.                                  |
| [**ExclusiveToPartial**](csharelocknh--exclusivetopartial.md)           | Modifie l’État.                                              |
| [**ExclusiveUnlock**](csharelocknh--exclusiveunlock.md)                 | Libère un verrou.                                                |
| [**FirstPartialToExclusive**](csharelocknh--firstpartialtoexclusive.md) | Utilisé pour la conversion d’un verrou partiel en verrou exclusif.         |
| [**PartialLock**](csharelocknh--partiallock.md)                         | Empêche plusieurs threads de terminer l’acquisition d’un verrou. |
| [**PartialUnlock**](csharelocknh--partialunlock.md)                     | Libère un verrou partiel.                                        |
| [**ShareLock**](csharelocknh--sharelock.md)                             | Obtient un verrou pour le mode partagé.                                 |
| [**ShareUnlock**](csharelocknh--shareunlock.md)                         | Libère un verrou en mode partagé.                               |
| [**SharedToPartial**](csharelocknh--sharedtopartial.md)                 | Obtient un verrou partiel.                                         |
| [**TryExclusiveLock**](csharelocknh--tryexclusivelock.md)               | Obtient un verrou en mode exclusif.                                     |



 

 

 



