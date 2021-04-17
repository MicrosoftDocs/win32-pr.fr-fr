---
title: Démarrage d’un exécutable lorsqu’un utilisateur ouvre une session
description: L’écriture d’une tâche qui démarre un exécutable quand un utilisateur se connecte est effectuée en définissant un déclencheur LOGON et une action exécutable.
ms.assetid: 0c5912aa-913d-42ce-a01b-b1359b49bb2f
keywords:
- Planificateur de tâches des exemples de Planificateur de tâches, déclencheur de connexion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ffa758546dbd08b6ccf27412f38891589cb9643
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379585"
---
# <a name="starting-an-executable-when-a-user-logs-on"></a><span data-ttu-id="e07f2-104">Démarrage d’un exécutable lorsqu’un utilisateur ouvre une session</span><span class="sxs-lookup"><span data-stu-id="e07f2-104">Starting an Executable When a User Logs On</span></span>

<span data-ttu-id="e07f2-105">L’écriture d’une tâche qui démarre un exécutable quand un utilisateur se connecte est effectuée en définissant un déclencheur LOGON et une action exécutable.</span><span class="sxs-lookup"><span data-stu-id="e07f2-105">Writing a task that starts an executable when a user logs on is done by defining a logon trigger and an executable action.</span></span>

## <a name="logon-trigger"></a><span data-ttu-id="e07f2-106">Déclencheur de connexion</span><span class="sxs-lookup"><span data-stu-id="e07f2-106">Logon Trigger</span></span>

<span data-ttu-id="e07f2-107">Les déclencheurs de connexion sont activés par leur limite de démarrage, mais ils ne démarrent pas l’exécutable tant qu’un utilisateur spécifié n’ouvre pas une session.</span><span class="sxs-lookup"><span data-stu-id="e07f2-107">Logon triggers are activated by their start boundary but they do not start the executable until a specified user logs on.</span></span> <span data-ttu-id="e07f2-108">Vous pouvez spécifier le déclencheur d’ouverture de session à démarrer lorsqu’un utilisateur se connecte en spécifiant l’utilisateur dans la propriété [**userid**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) de l’interface [**ILogonTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger) ([**LogonTrigger**](logontrigger.md) pour l’écriture de scripts).</span><span class="sxs-lookup"><span data-stu-id="e07f2-108">You can specify the logon trigger to start when a certain user logs on by specifying the user in the [**UserId**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) property of the [**ILogonTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger) interface ([**LogonTrigger**](logontrigger.md) for scripting).</span></span>

## <a name="logontrigger-examples"></a><span data-ttu-id="e07f2-109">Exemples LogonTrigger</span><span class="sxs-lookup"><span data-stu-id="e07f2-109">LogonTrigger Examples</span></span>

<span data-ttu-id="e07f2-110">Les exemples suivants démarrent le bloc-notes après qu’un utilisateur ouvre une session.</span><span class="sxs-lookup"><span data-stu-id="e07f2-110">The following examples start Notepad after a user logs on.</span></span>

-   [<span data-ttu-id="e07f2-111">Exemple de déclencheur LOGON (script)</span><span class="sxs-lookup"><span data-stu-id="e07f2-111">Logon Trigger Example (Scripting)</span></span>](logon-trigger-example--scripting-.md)
-   [<span data-ttu-id="e07f2-112">Exemple de déclencheur LOGON (C++)</span><span class="sxs-lookup"><span data-stu-id="e07f2-112">Logon Trigger Example (C++)</span></span>](logon-trigger-example--c---.md)
-   [<span data-ttu-id="e07f2-113">Exemple de déclencheur LOGON (XML)</span><span class="sxs-lookup"><span data-stu-id="e07f2-113">Logon Trigger Example (XML)</span></span>](logon-trigger-example--xml-.md)

## <a name="related-topics"></a><span data-ttu-id="e07f2-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e07f2-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e07f2-115">Utilisation de l’Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="e07f2-115">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




