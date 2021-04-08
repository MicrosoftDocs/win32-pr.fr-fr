---
title: SessionStateChangeTrigger. StateChange, propriété
description: Pour les scripts, obtient ou définit le type de Terminal Server modification de session qui déclencherait un lancement de tâche.
ms.assetid: ae1460c7-2939-4fcb-b7fc-edc859596bc4
keywords:
- StateChange, propriété Planificateur de tâches
- StateChange, propriété Planificateur de tâches, objet SessionStateChangeTrigger
- Objet SessionStateChangeTrigger Planificateur de tâches, propriété StateChange
topic_type:
- apiref
api_name:
- SessionStateChangeTrigger.StateChange
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac4be561482917788f6afb9b8eb7394cdcce7985
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740613"
---
# <a name="sessionstatechangetriggerstatechange-property"></a><span data-ttu-id="df382-106">SessionStateChangeTrigger. StateChange, propriété</span><span class="sxs-lookup"><span data-stu-id="df382-106">SessionStateChangeTrigger.StateChange property</span></span>

<span data-ttu-id="df382-107">Pour les scripts, obtient ou définit le type de Terminal Server modification de session qui déclencherait un lancement de tâche.</span><span class="sxs-lookup"><span data-stu-id="df382-107">For scripting, gets or sets the kind of Terminal Server session change that would trigger a task launch.</span></span>

## <a name="syntax"></a><span data-ttu-id="df382-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="df382-108">Syntax</span></span>


```VB
SessionStateChangeTrigger.StateChange As Integer
```



## <a name="property-value"></a><span data-ttu-id="df382-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="df382-109">Property value</span></span>

<span data-ttu-id="df382-110">Type de Terminal Server modification de session qui déclenche l’exécution d’une tâche.</span><span class="sxs-lookup"><span data-stu-id="df382-110">The kind of Terminal Server session change that triggers a task to launch.</span></span>

<span data-ttu-id="df382-111">Les valeurs possibles proviennent de l’énumération des [**types de changement d’état de session de tâche \_ \_ \_ \_**](/windows/desktop/api/taskschd/ne-taskschd-task_session_state_change_type) .</span><span class="sxs-lookup"><span data-stu-id="df382-111">The possible values are from the [**TASK\_SESSION\_STATE\_CHANGE\_TYPE**](/windows/desktop/api/taskschd/ne-taskschd-task_session_state_change_type) enumeration.</span></span>



| <span data-ttu-id="df382-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="df382-112">Value</span></span>                                                                                                                                                                                                                                               | <span data-ttu-id="df382-113">Signification</span><span class="sxs-lookup"><span data-stu-id="df382-113">Meaning</span></span>                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_CONSOLE_CONNECT"></span><span id="task_console_connect"></span><dl> <span data-ttu-id="df382-114"><dt>**Tâche \_ \_Connexion**</dt> de la console <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="df382-114"><dt>**TASK\_CONSOLE\_CONNECT**</dt> <dt>1</dt></span></span> </dl>          | <span data-ttu-id="df382-115">Modification de l’état de la connexion à la console Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="df382-115">Terminal Server console connection state change.</span></span> <span data-ttu-id="df382-116">Par exemple, lorsque vous vous connectez à une session utilisateur sur l’ordinateur local en basculant les utilisateurs sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="df382-116">For example, when you connect to a user session on the local computer by switching users on the computer.</span></span> <br/>                           |
| <span id="TASK_CONSOLE_DISCONNECT"></span><span id="task_console_disconnect"></span><dl> <span data-ttu-id="df382-117"><dt>**Tâche \_ \_Déconnexion**</dt> de la console <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="df382-117"><dt>**TASK\_CONSOLE\_DISCONNECT**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="df382-118">Modification de l’état de déconnexion de la console Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="df382-118">Terminal Server console disconnection state change.</span></span> <span data-ttu-id="df382-119">Par exemple, lorsque vous vous déconnectez à une session utilisateur sur l’ordinateur local en basculant les utilisateurs sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="df382-119">For example, when you disconnect to a user session on the local computer by switching users on the computer.</span></span><br/>                      |
| <span id="TASK_REMOTE_CONNECT"></span><span id="task_remote_connect"></span><dl> <span data-ttu-id="df382-120"><dt>**Tâche \_ \_Connexion à distance**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="df382-120"><dt>**TASK\_REMOTE\_CONNECT**</dt> <dt>3</dt></span></span> </dl>             | <span data-ttu-id="df382-121">Terminal Server modification de l’état de la connexion à distance.</span><span class="sxs-lookup"><span data-stu-id="df382-121">Terminal Server remote connection state change.</span></span> <span data-ttu-id="df382-122">Par exemple, lorsqu’un utilisateur se connecte à une session utilisateur à l’aide du programme Connexion Bureau à distance à partir d’un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="df382-122">For example, when a user connects to a user session by using the Remote Desktop Connection program from a remote computer.</span></span><br/>            |
| <span id="TASK_REMOTE_DISCONNECT"></span><span id="task_remote_disconnect"></span><dl> <span data-ttu-id="df382-123"><dt>**Tâche \_ \_Déconnexion à distance**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="df382-123"><dt>**TASK\_REMOTE\_DISCONNECT**</dt> <dt>4</dt></span></span> </dl>    | <span data-ttu-id="df382-124">Terminal Server modification de l’état de la déconnexion distante.</span><span class="sxs-lookup"><span data-stu-id="df382-124">Terminal Server remote disconnection state change.</span></span> <span data-ttu-id="df382-125">Par exemple, lorsqu’un utilisateur se déconnecte d’une session utilisateur lors de l’utilisation du programme Connexion Bureau à distance à partir d’un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="df382-125">For example, when a user disconnects from a user session while using the Remote Desktop Connection program from a remote computer.</span></span><br/> |
| <span id="TASK_SESSION_LOCK"></span><span id="task_session_lock"></span><dl> <span data-ttu-id="df382-126"><dt>**Tâche \_ \_Verrou de session**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="df382-126"><dt>**TASK\_SESSION\_LOCK**</dt> <dt>7</dt></span></span> </dl>                   | <span data-ttu-id="df382-127">Terminal Server modification de l’état verrouillé de la session.</span><span class="sxs-lookup"><span data-stu-id="df382-127">Terminal Server session locked state change.</span></span> <span data-ttu-id="df382-128">Par exemple, ce changement d’État provoque l’exécution de la tâche lorsque l’ordinateur est verrouillé.</span><span class="sxs-lookup"><span data-stu-id="df382-128">For example, this state change causes the task to run when the computer is locked.</span></span> <br/>                                                      |
| <span id="TASK_SESSION_UNLOCK"></span><span id="task_session_unlock"></span><dl> <span data-ttu-id="df382-129"><dt>**Tâche \_ \_Déverrouillage de session**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="df382-129"><dt>**TASK\_SESSION\_UNLOCK**</dt> <dt>8</dt></span></span> </dl>             | <span data-ttu-id="df382-130">Modification de l’état de déverrouillage de la session Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="df382-130">Terminal Server session unlocked state change.</span></span> <span data-ttu-id="df382-131">Par exemple, ce changement d’État provoque l’exécution de la tâche lorsque l’ordinateur est déverrouillé.</span><span class="sxs-lookup"><span data-stu-id="df382-131">For example, this state change causes the task to run when the computer is unlocked.</span></span><br/>                                                   |



 

## <a name="requirements"></a><span data-ttu-id="df382-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="df382-132">Requirements</span></span>



| <span data-ttu-id="df382-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="df382-133">Requirement</span></span> | <span data-ttu-id="df382-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="df382-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="df382-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="df382-135">Minimum supported client</span></span><br/> | <span data-ttu-id="df382-136">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="df382-136">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="df382-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="df382-137">Minimum supported server</span></span><br/> | <span data-ttu-id="df382-138">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="df382-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="df382-139">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="df382-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="df382-140"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="df382-140"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="df382-141">DLL</span><span class="sxs-lookup"><span data-stu-id="df382-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df382-142"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df382-142"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





