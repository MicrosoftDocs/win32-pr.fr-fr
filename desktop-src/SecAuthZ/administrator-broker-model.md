---
description: L’application est divisée en deux programmes. L’un des programmes s’exécute en tant qu’utilisateur standard et l’autre s’exécute avec des privilèges d’administrateur.
ms.assetid: 1e661915-5797-421d-b96f-72949f441aba
title: Modèle de Broker administrateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c67a68c823221226f56d01b750ab74a70ca30530f44cd174e333c3e4d7cbaa3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117784940"
---
# <a name="administrator-broker-model"></a>Modèle de Broker administrateur

Dans le modèle de Broker administrateur, l’application est divisée en deux programmes. L’un des programmes s’exécute en tant qu’utilisateur standard et l’autre s’exécute avec des privilèges d’administrateur.

À l’aide d’un manifeste d’application, marquez le programme utilisateur standard avec le **requestedExecutionLevel** de **asInvoker** et marquez le programme administratif avec un **requestedExecutionLevel** de **requireAdministrator**. Un utilisateur lance d’abord le programme utilisateur standard. Lorsque l’utilisateur tente d’effectuer une opération qui requiert un jeton d’accès administrateur complet, le programme utilisateur standard appelle la fonction [**ShellExecute**](/windows/desktop/api/shellapi/nf-shellapi-shellexecutea) pour lancer le programme administratif. La fonction **ShellExecute** invite l’utilisateur à approuver avant d’exécuter l’application avec le jeton d’accès administrateur complet de l’utilisateur. Le programme administratif peut ensuite effectuer des tâches qui requièrent des privilèges d’administrateur.

Le programme d’administration n’est pas complètement isolé du programme utilisateur standard. Le programme administratif peut activer la communication entre processus avec le programme utilisateur standard. Toutefois, ces communications sont limitées par la stratégie d’intégrité obligatoire par défaut. Pour plus d’informations sur les considérations relatives à l’intégrité obligatoire, consultez [conception d’applications pour qu’elles s’exécutent à un niveau d’intégrité faible](/previous-versions/dotnet/articles/bb625960(v=msdn.10)).

Voici les utilisations possibles du modèle Broker administrateur :

-   Développement des assistants. Quand un assistant matériel détermine qu’un pilote requis n’est pas installé sur l’ordinateur ou qu’il se trouve dans l’emplacement approuvé de l’entreprise, il appelle une application avec élévation de privilèges, avec la possibilité de déplacer un pilote dans le magasin de l’ordinateur.
-   Autorun.exe appelant Setup.exe. Lorsqu’un utilisateur exécute un logiciel à partir d’un CD, Autorun.exe, qui s’exécute en tant qu’utilisateur standard, démarre Setup.exe, qui s’exécute en tant qu’administrateur, pour installer le logiciel sur l’ordinateur.

Voici les inconvénients de l’utilisation du modèle Broker administrateur :

-   Les transitions entre l’application et l’application peuvent être confuses pour l’utilisateur. Il peut être difficile d’informer l’utilisateur de la raison pour laquelle une nouvelle application s’affiche sur le moniteur.
-   Il peut être difficile de transmettre des informations d’État entre les deux applications. Par exemple, vous ne devez pas utiliser ce modèle pour transmettre des informations d’État entre un panneau de configuration utilisateur standard (CPL) et son homologue d’administrateur simplement pour autoriser le même CPL à avoir des fonctionnalités d’administration et d’utilisateur standard. Le CPL standard de l’utilisateur devrait stocker son état quelque part.
-   Il peut y avoir un grand nombre de code répliqué lors du fractionnement des fonctionnalités entre deux programmes.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Développement d’applications nécessitant des privilèges d’administrateur](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[Modèle d’objet COM administrateur](administrator-com-object-model.md)
</dt> <dt>

[Modèle de service du système d’exploitation](operating-system-service-model.md)
</dt> <dt>

[Modèle de tâche avec élévation de privilèges](elevated-task-model.md)
</dt> </dl>

 

 
