---
title: Contextes de sécurité pour les tâches
description: Les tâches sont inscrites et exécutées dans un contexte de sécurité spécifique.
ms.assetid: be86eb9f-f6ec-4dce-afe8-e3314a74062a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb6f49ef07818b1fe729fa96a2b5e0712979a17f300e4f411f96cefd2f3917f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119738249"
---
# <a name="security-contexts-for-tasks"></a>Contextes de sécurité pour les tâches

Les tâches sont inscrites et exécutées dans un contexte de sécurité spécifique. Les utilisateurs peuvent créer des applications qui inscrivent, mettent à jour, suppriment ou exécutent des tâches, mais l’utilisateur doit fournir les informations d’identification correctes lorsqu’une tâche est inscrite et l’application doit s’exécuter dans un processus avec les privilèges appropriés.

## <a name="specifying-credentials"></a>Spécification des informations d’identification

Vous pouvez spécifier le contexte de sécurité d’une tâche en spécifiant des informations d’identification dans les méthodes [**ITaskFolder :: RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ou [**ITaskFolder :: RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) ([**TaskFolder. RegisterTask**](taskfolder-registertask.md) ou [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) pour l’écriture de scripts) ou en affectant un principal à la [**propriété principale de ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_principal) ([**TaskDefinition. principal**](taskdefinition-principal.md) pour l’écriture de scripts). Si un principal est créé pour une définition de tâche, puis que la définition de tâche est inscrite à l’aide de la méthode **RegisterTaskDefinition** avec d’autres informations d’identification spécifiées dans les paramètres de la méthode, les informations d’identification spécifiées dans la méthode **RegisterTaskDefinition** remplacent les informations d’identification dans le principal. Si un principal est créé pour une définition de tâche à l’aide de XML, puis que le XML de la tâche est inscrit à l’aide de la méthode **RegisterTask** avec des informations d’identification différentes spécifiées dans les paramètres de la méthode, les informations d’identification spécifiées dans la méthode **RegisterTask** remplacent les informations d’identification dans le principal.

Vous spécifiez un compte d’utilisateur ou un groupe lors de l’inscription d’une tâche ou la spécification du principe d’une tâche. Le contexte de sécurité du compte d’utilisateur ou du groupe est utilisé pour le contexte de sécurité de la tâche. Dans ces méthodes et propriétés, vous définissez également le type d’ouverture de session. Le type d’ouverture de session est défini par l’une des constantes de l’énumération du [**\_ \_ type de connexion**](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type) à la tâche.

Les tâches inscrites avec \_ l' \_ indicateur de mot de passe d’ouverture de session ou d’ouverture de session de tâche s’exécutent \_ \_ uniquement si le privilège ouvrir une session en tant que par lot est activé pour l’utilisateur spécifié. Les utilisateurs du groupe administrateurs et opérateurs de sauvegarde disposent de ce privilège activé par défaut.

quand vous appelez la méthode [**la :: Connecter**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-connect) ([**TaskService. Connecter**](taskservice-connect.md) pour la création de scripts), tous les appels de méthode suivants au service Planificateur de tâches utilisent les informations d’identification passées à la méthode **Connecter** . Il est important de prendre en compte lors de l’enregistrement de tâches avec un type de connexion interactive. lorsque vous enregistrez une tâche avec le type de connexion égal à \_ jeton interactif d’ouverture de session \_ \_ et que la tâche ne contient pas d’informations d’identification spécifiées dans la propriété [**principale**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_principal) de la définition de tâche, spécifiées dans les paramètres à [**RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition), ou spécifiées dans le XML transmis à [**RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask), la tâche est inscrite avec les informations d’identification de l’utilisateur qui a appelé la méthode **Connecter** .

## <a name="user-account-control-uac-security-for-tasks"></a>Sécurité du contrôle de compte d’utilisateur (UAC) pour les tâches

[Le contrôle de compte d’utilisateur](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) (UAC) permet aux utilisateurs d’exercer des fonctionnalités générales telles que l’exécution de programmes et l’enregistrement et la modification de données sans exposer de privilèges d’administrateur. Par défaut, une tâche s’exécute avec des privilèges de bas niveau lorsque le contrôle de compte d’utilisateur est activé. Les tâches peuvent spécifier qu’elles s’exécutent avec des privilèges élevés ou des privilèges faibles en définissant un niveau de privilège à partir de l’énumération de [**\_ \_ type tâche RUNLEVEL**](/windows/win32/api/taskschd/ne-taskschd-task_runlevel_type) pour la [**propriété RUNLEVEL de IPrincipal**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) ([**principal. RUNLEVEL**](principal-runlevel.md) pour les scripts). La valeur de la propriété **runlevel** détermine le niveau de privilège à partir duquel les actions d’une tâche seront exécutées. Si les actions d’une tâche doivent avoir des privilèges élevés pour s’exécuter, vous devez définir la propriété **runlevel** sur la **tâche \_ runlevel la \_ plus élevée**. Si une tâche est inscrite à l’aide du groupe administrateurs pour le contexte de sécurité de la tâche, vous devez également définir la propriété **runlevel** sur la **tâche \_ runlevel la \_ plus élevée** si vous souhaitez exécuter la tâche. Si une tâche est inscrite à l’aide du \\ compte administrateur intégré ou des comptes système local ou service local, la propriété **runlevel** est ignorée. La valeur de propriété sera également ignorée si le contrôle de compte d’utilisateur (UAC) est désactivé. La valeur de la propriété **runlevel** n’affecte pas les autorisations nécessaires à l’exécution ou à la suppression d’une tâche.

> [!Note]  
> après la mise à niveau d’un système d’exploitation de Windows xp vers Windows Vista, les tâches qui ont été inscrites à l’aide du \\ compte administrateur intégré sur Windows XP auront la propriété [**RunLevel**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) définie sur **TASK \_ RunLevel \_ LUA**. Cela peut entraîner l’échec de certaines tâches. Vous pouvez mettre à jour cette propriété manuellement pour vous assurer que toutes les tâches s’exécuteront.

 

À partir d’un processus à faibles privilèges, vous ne pouvez pas inscrire une tâche avec la propriété [**runlevel**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) égale à la **tâche \_ runlevel la \_ plus élevée**, mais vous pouvez inscrire une tâche avec la propriété **runlevel** égale à **Task \_ runlevel \_ LUA**. Les actions de tâche sont exécutées avec des privilèges faibles. Vous n’êtes pas autorisé à inscrire la tâche en tant que builtin/administrateur, système local ou pour un groupe.

À partir d’un processus avec privilèges élevés, vous pouvez inscrire une tâche avec la propriété [**runlevel**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) égale à la **tâche \_ runlevel la \_ plus élevée** ou à la **tâche \_ runlevel \_ LUA**. La tâche est exécutée avec un niveau de privilège déterminé par la propriété **runlevel** , sauf si vous utilisez le compte d’administrateur, auquel cas la tâche est exécutée avec des privilèges élevés.

À partir d’un processus avec élévation de privilèges, vous pouvez inscrire une tâche Planificateur de tâches 1,0. Le service Planificateur de tâches définit le niveau d’exécution de la tâche sur tâche \_ RUNLEVEL le \_ plus élevé et la tâche s’exécute avec des privilèges élevés.

À partir d’un processus à faibles privilèges, vous pouvez également inscrire une tâche Planificateur de tâches 1,0. Le service Planificateur de tâches définit le niveau d’exécution de la tâche sur TASK \_ RUNLEVEL \_ LUA et la tâche s’exécute avec des privilèges faibles. Si cette tâche est mise à jour à partir d’un processus avec élévation de privilèges, le niveau d’exécution de la tâche reste tâche \_ RUNLEVEL \_ lua.

## <a name="security-for-registering-tasks"></a>Sécurité pour l’inscription des tâches

Lorsque vous inscrivez une tâche à partir d’un compte membre du groupe administrateurs, il vous suffit de spécifier un mot de passe lors de l’inscription de la tâche dans les cas suivants :

-   Si vous inscrivez la tâche pour qu’elle s’exécute sous le contexte de sécurité de votre compte ou d’un compte d’utilisateur différent et que vous utilisez l' \_ indicateur de mot de passe de connexion \_ à la tâche dans la méthode [**RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ou [**RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) .
-   Si vous inscrivez la tâche pour qu’elle s’exécute sous le contexte de sécurité d’un compte d’utilisateur différent et que vous utilisez l' \_ indicateur S4U d’ouverture de session de \_ la tâche dans la méthode [**RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ou [**RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) .

Vous ne pouvez pas utiliser un groupe d’utilisateurs comme contexte de sécurité d’une tâche lorsque vous inscrivez la tâche à l’aide de l' \_ indicateur S4U d’ouverture de session de la tâche \_ ou de l' \_ indicateur de mot de passe d’ouverture \_ de session de la tâche dans la méthode [**RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ou [**RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) .

Lorsque vous inscrivez une tâche à partir d’un compte d’utilisateur qui n’est pas membre du groupe administrateurs, vous n’avez pas besoin de spécifier un mot de passe lors de l’inscription de la tâche si vous inscrivez la tâche pour qu’elle s’exécute sous le contexte de sécurité de votre compte et que vous utilisiez le type d’ouverture de session S4U ou interactive. Dans le cas contraire, vous devez spécifier un mot de passe lors de l’inscription de la tâche. En outre, vous ne pouvez pas inscrire la tâche à l’aide du compte de service local ou à l’aide d’un groupe pour le contexte de sécurité de la tâche.

## <a name="security-for-reading-updating-deleting-and-running-tasks"></a>Sécurité pour la lecture, la mise à jour, la suppression et l’exécution de tâches

Par défaut, un utilisateur qui crée une tâche peut lire, mettre à jour, supprimer et exécuter la tâche. Un utilisateur doit disposer d’une autorisation d’écriture de fichier sur un fichier de tâche pour mettre à jour une tâche, une autorisation de lecture de fichier sur un fichier de tâche pour lire une tâche, l’autorisation supprimer sur un fichier de tâche pour supprimer une tâche et l’autorisation d’exécution de fichier sur une tâche pour exécuter une tâche à l' [**aide des méthodes**](registeredtask-runex.md) [**IRegisteredTask :: Run**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-run) ou [**RunEx**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-runex) ([**RegisteredTask. Run**](registeredtask-run.md) Les membres du groupe administrateurs ou du compte système peuvent lire, mettre à jour, supprimer et exécuter des tâches. Les membres du groupe utilisateurs, du compte LocalService et du compte NetworkService peuvent uniquement lire, mettre à jour, supprimer et exécuter les tâches qu’ils ont créées. Ce comportement par défaut est modifié lorsque la liste DACL du fichier de tâche est modifiée, auquel cas la liste DACL définit les utilisateurs qui disposent d’une autorisation d’écriture de fichier, de lecture, d’exécution et de suppression. Pour définir des autorisations pour un fichier de tâche, utilisez la méthode IRegisteredTask. SetSecurityDescriptor (RegisteredTask. SetSecurityDescriptor pour l’écriture de scripts) ou définissez le descripteur de sécurité lorsque vous inscrivez la tâche à l’aide des méthodes [**RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ou [**RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) .

Un utilisateur doit disposer de l’autorisation WriteDAC en plus des autorisations de lecture/écriture pour mettre à jour une tâche si la mise à jour de la tâche nécessite une modification de la liste DACL pour la tâche.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Informations d’inscription de la tâche](task-registration-information.md)
</dt> <dt>

[À propos de l’Planificateur de tâches](about-the-task-scheduler.md)
</dt> <dt>

[Renforcement de la sécurité des tâches](task-security-hardening.md)
</dt> <dt>

[**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md)
</dt> <dt>

[**ITaskFolder :: RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition)
</dt> <dt>

[**Propriété principal de ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_principal)
</dt> <dt>

[**\_type de connexion à la tâche \_**](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type)
</dt> </dl>

 

 




