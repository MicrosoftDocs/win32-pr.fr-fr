---
title: LogonTrigger. UserId, propriété
description: Pour les scripts, obtient ou définit l’identificateur de l’utilisateur.
ms.assetid: d28eea9b-8238-49e7-afec-5a96281b3063
keywords:
- UserId, propriété Planificateur de tâches
- UserId, propriété Planificateur de tâches, objet LogonTrigger
- Objet LogonTrigger Planificateur de tâches, UserId, propriété
topic_type:
- apiref
api_name:
- LogonTrigger.UserId
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dde08f82742325303e62e405cd13d2b9e7c1191
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384107"
---
# <a name="logontriggeruserid-property"></a><span data-ttu-id="19b1f-106">LogonTrigger. UserId, propriété</span><span class="sxs-lookup"><span data-stu-id="19b1f-106">LogonTrigger.UserId property</span></span>

<span data-ttu-id="19b1f-107">Pour les scripts, obtient ou définit l’identificateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="19b1f-107">For scripting, gets or sets the identifier of the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="19b1f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="19b1f-108">Syntax</span></span>


```VB
LogonTrigger.UserId As String
```



## <a name="property-value"></a><span data-ttu-id="19b1f-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="19b1f-109">Property value</span></span>

<span data-ttu-id="19b1f-110">Identificateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="19b1f-110">The identifier of the user.</span></span> <span data-ttu-id="19b1f-111">Par exemple, « MyDomain \\ myname » ou pour un compte local, « administrateur ».</span><span class="sxs-lookup"><span data-stu-id="19b1f-111">For example, "MyDomain\\MyName" or for a local account, "Administrator".</span></span>

<span data-ttu-id="19b1f-112">Cette propriété peut être dans l’un des formats suivants :</span><span class="sxs-lookup"><span data-stu-id="19b1f-112">This property can be in one of the following formats:</span></span>

-   <span data-ttu-id="19b1f-113">Nom d’utilisateur ou SID : la tâche est démarrée lorsque l’utilisateur ouvre une session sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="19b1f-113">User name or SID: The task is started when the user logs on to the computer.</span></span>
-   <span data-ttu-id="19b1f-114">NULL : la tâche est démarrée quand un utilisateur ouvre une session sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="19b1f-114">NULL: The task is started when any user logs on to the computer.</span></span>

## <a name="remarks"></a><span data-ttu-id="19b1f-115">Notes</span><span class="sxs-lookup"><span data-stu-id="19b1f-115">Remarks</span></span>

<span data-ttu-id="19b1f-116">Si vous souhaitez qu’une tâche soit déclenchée lorsqu’un membre d’un groupe se connecte à l’ordinateur plutôt qu’à un utilisateur spécifique, n’affectez pas de valeur à la propriété **LogonTrigger. UserID** .</span><span class="sxs-lookup"><span data-stu-id="19b1f-116">If you want a task to be triggered when any member of a group logs on to the computer rather than when a specific user logs on, then do not assign a value to the **LogonTrigger.UserId** property.</span></span> <span data-ttu-id="19b1f-117">Au lieu de cela, créez un déclencheur LOGON avec une propriété **LogonTrigger. UserID** vide et attribuez une valeur au principal pour la tâche à l’aide de la propriété [**principal. GroupId**](principal-groupid.md) .</span><span class="sxs-lookup"><span data-stu-id="19b1f-117">Instead, create a logon trigger with an empty **LogonTrigger.UserId** property and assign a value to the principal for the task using the [**Principal.GroupId**](principal-groupid.md) property.</span></span>

<span data-ttu-id="19b1f-118">Lors de la lecture ou de l’écriture de données XML pour une tâche, l’identificateur d’utilisateur d’ouverture de session est spécifié à l’aide de l’élément [**userid**](taskschedulerschema-userid-logontriggertype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="19b1f-118">When reading or writing XML for a task, the logon user identifier is specified using the [**UserId**](taskschedulerschema-userid-logontriggertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="19b1f-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="19b1f-119">Requirements</span></span>



| <span data-ttu-id="19b1f-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="19b1f-120">Requirement</span></span> | <span data-ttu-id="19b1f-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="19b1f-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="19b1f-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="19b1f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="19b1f-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="19b1f-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="19b1f-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="19b1f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="19b1f-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="19b1f-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="19b1f-126">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="19b1f-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="19b1f-127"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="19b1f-127"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="19b1f-128">DLL</span><span class="sxs-lookup"><span data-stu-id="19b1f-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19b1f-129"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19b1f-129"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19b1f-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="19b1f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19b1f-131">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="19b1f-131">**LogonTrigger**</span></span>](logontrigger.md)
</dt> <dt>

[<span data-ttu-id="19b1f-132">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="19b1f-132">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





