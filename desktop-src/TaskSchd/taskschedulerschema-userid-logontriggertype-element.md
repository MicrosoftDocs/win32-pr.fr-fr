---
title: Élément UserId (logonTriggerType)
description: Identificateur de l’utilisateur. La tâche est démarrée lorsque cet utilisateur ouvre une session sur l’ordinateur.
ms.assetid: 52568899-e351-4ee1-b613-d7c42d7b983d
keywords:
- UserId, élément Planificateur de tâches
topic_type:
- apiref
api_name:
- UserId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 69d6534122b4b5e11a18a64ffa9bbb5e29e2a68a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519106"
---
# <a name="userid-logontriggertype-element"></a><span data-ttu-id="673d5-105">Élément UserId (logonTriggerType)</span><span class="sxs-lookup"><span data-stu-id="673d5-105">UserId (logonTriggerType) Element</span></span>

<span data-ttu-id="673d5-106">Identificateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="673d5-106">Identifier of the user.</span></span> <span data-ttu-id="673d5-107">La tâche est démarrée lorsque cet utilisateur ouvre une session sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="673d5-107">The task is started when this user logs on to the computer.</span></span>

``` syntax
<xs:element name="UserId"
    type="nonEmptyString"
    maxOccurs="1"
    minOccurs="0"
 />
```

<span data-ttu-id="673d5-108">L’élément **userid** est défini par le type complexe [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="673d5-108">The **UserId** element is defined by the [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="673d5-109">Élément parent</span><span class="sxs-lookup"><span data-stu-id="673d5-109">Parent element</span></span>



| <span data-ttu-id="673d5-110">Élément</span><span class="sxs-lookup"><span data-stu-id="673d5-110">Element</span></span>                                                                       | <span data-ttu-id="673d5-111">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="673d5-111">Derived from</span></span>                                                                 | <span data-ttu-id="673d5-112">Description</span><span class="sxs-lookup"><span data-stu-id="673d5-112">Description</span></span>                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="673d5-113">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="673d5-113">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md) | [<span data-ttu-id="673d5-114">**logonTriggerType**</span><span class="sxs-lookup"><span data-stu-id="673d5-114">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md) | <span data-ttu-id="673d5-115">Spécifie un déclencheur qui démarre une tâche lorsqu’un utilisateur ouvre une session.</span><span class="sxs-lookup"><span data-stu-id="673d5-115">Specifies a trigger that starts a task when a user logs on.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="673d5-116">Notes</span><span class="sxs-lookup"><span data-stu-id="673d5-116">Remarks</span></span>

<span data-ttu-id="673d5-117">Pour le développement de script, l’identificateur d’utilisateur du déclencheur LOGON est spécifié à l’aide de la propriété [**LogonTrigger. UserID**](logontrigger-userid.md) .</span><span class="sxs-lookup"><span data-stu-id="673d5-117">For scripting development, the user identifier for the logon trigger is specified using the [**LogonTrigger.UserId**](logontrigger-userid.md) property.</span></span>

<span data-ttu-id="673d5-118">Pour le développement C++, l’identificateur d’utilisateur du déclencheur LOGON est spécifié à l’aide de la propriété [**ILogonTrigger :: userid**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) .</span><span class="sxs-lookup"><span data-stu-id="673d5-118">For C++ development, the user identifier for the logon trigger is specified using the [**ILogonTrigger::UserId**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) property.</span></span>

## <a name="examples"></a><span data-ttu-id="673d5-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="673d5-119">Examples</span></span>

<span data-ttu-id="673d5-120">Pour obtenir un exemple complet du code XML d’une tâche qui spécifie un déclencheur LOGON, consultez [exemple de déclencheur de connexion (XML)](logon-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="673d5-120">For a complete example of the XML for a task that specifies a logon trigger, see [Logon Trigger Example (XML)](logon-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="673d5-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="673d5-121">Requirements</span></span>



| <span data-ttu-id="673d5-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="673d5-122">Requirement</span></span> | <span data-ttu-id="673d5-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="673d5-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="673d5-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="673d5-124">Minimum supported client</span></span><br/> | <span data-ttu-id="673d5-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="673d5-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="673d5-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="673d5-126">Minimum supported server</span></span><br/> | <span data-ttu-id="673d5-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="673d5-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="673d5-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="673d5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="673d5-129">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="673d5-129">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="673d5-130">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="673d5-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





