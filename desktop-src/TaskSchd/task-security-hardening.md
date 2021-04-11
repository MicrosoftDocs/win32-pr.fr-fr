---
title: Renforcement de la sécurité des tâches
description: L’utilisation de la fonctionnalité de renforcement de la sécurité des tâches permet aux propriétaires de tâches d’exécuter leurs tâches avec les privilèges minimaux requis.
ms.assetid: ba03add5-aa05-4bef-baec-684ca17363bd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ab70679d605a9ad56c6d26116245ae17d41a7a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196793"
---
# <a name="task-security-hardening"></a>Renforcement de la sécurité des tâches

L’utilisation de la fonctionnalité de renforcement de la sécurité des tâches permet aux propriétaires de tâches d’exécuter leurs tâches avec les privilèges minimaux requis. Notez que cette fonctionnalité est activée par défaut et que les propriétaires de tâches peuvent effectuer des ajustements supplémentaires à l’aide du tableau des privilèges de type identificateur de sécurité du jeton de processus de tâche et de la tâche requise.

## <a name="task-process-token-sid-type-and-task-required-privileges-array"></a>Type de SID de jeton de processus de tâche et tableau des privilèges requis

La spécification de **ProcessTokenSidType** au niveau de la définition de tâche permet aux propriétaires de tâches de demander un processus de tâche à exécuter avec le type de sid « aucun » ou le type de sid « illimité ». Si le champ est présent dans la définition de tâche, la validation s’assure que la tâche UserId contient le nom ou la chaîne SID correspondante pour l’un de ces comptes de service intégrés de système d’exploitation : « SERVICE réseau » ou « SERVICE LOCAL ».

Le type SID « None » signifie que la tâche s’exécute dans un processus qui ne contient pas de SID de jeton de processus (aucune modification n’est apportée à la liste des groupes de jetons de processus). Dans ce cas, le SID de compte du principal de tâche (LocalService/NetworkService) dispose d’un accès complet au jeton de processus.

Le type de SID « illimité » signifie qu’un SID de tâche sera dérivé du chemin d’accès complet à la tâche et sera ajouté à la liste des groupes de jetons de processus. Par exemple, le \\ \\ RACTask Microsoft Windows \\ RAC \\ qui s’exécute dans le compte de service local, le SID de tâche est dérivé du nom Microsoft-Windows-RAC-RACTask où « - » remplace « \\ », car «» \\ est un caractère de nom d’utilisateur non valide. Le nom de groupe connu pour le SID de tâche serait « NT TASK \\ <modified full task path> » (NomDomaine \\ nom_utilisateur format). La liste de contrôle d’accès discrétionnaire (DACL) par défaut du jeton de processus sera également modifiée pour autoriser le contrôle total du SID de tâche et du SID de système local uniquement et le contrôle de lecture du SID de compte de principal de tâche. « schtasks.exe/showsid/TN <full task path> » affiche le SID de tâche correspondant à la tâche.

Lorsqu’une action de tâche non COM démarre, le moteur de planification se connecte au compte du principal de tâche, obtient le jeton de processus et interroge la liste des privilèges que le jeton a, puis compare celui-ci à la liste des privilèges spécifiée dans RequiredPrivileges. Si aucun privilège n’est spécifié dans le second, alors cela est marqué comme privilège de SE \_ \_ supprimé. L’action exécutable est ensuite démarrée avec le handle de jeton résultant à l’aide de l’API CreateProcessAsUser.

Lorsqu’une action de tâche COM démarre, elle doit être activée par le processus de taskhost.exe. Le moteur de planification interroge le bloc de contexte de chaque taskhost.exe en cours d’exécution avec le même compte que la tâche de démarrage. S’il détecte qu’un processus hôte a démarré avec un sur-ensemble de privilèges dont la tâche de démarrage a besoin, alors cette tâche est hébergée dans ce processus. S’il ne trouve pas un tel processus, il combine les informations de sécurisation renforcée de toutes les tâches qui s’exécutent dans le TaskHosts sous le compte du principal de la tâche avec le masque RequiredPrivileges spécifié, puis démarre une nouvelle instance de taskhost.exe.

Si RequiredPrivileges n’est pas présent dans la définition de tâche, les privilèges par défaut du compte de principal de tâche sans le SeImpersonatePrivilege sont utilisés pour le processus de tâche. Si **ProcessTokenSidType** n’est pas présent dans la définition de la tâche, la valeur par défaut est « Unrestricted ».

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Informations d’inscription de la tâche](task-registration-information.md)
</dt> <dt>

[À propos de l’Planificateur de tâches](about-the-task-scheduler.md)
</dt> <dt>

[Contextes de sécurité pour les tâches](security-contexts-for-running-tasks.md)
</dt> </dl>

 

 




